---
title: Beregn lagertilgjengelighet for detaljhandelskanaler
description: Denne artikkelen beskriver hvordan et firma kan bruke Microsoft Dynamics 365 Commerce til å vise estimert beholdningstilgjengelighet for produkter i nett- og butikkanaler.
author: hhainesms
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 952acf4cc26815822436bb7a5117775a5f12200c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884117"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Beregn lagertilgjengelighet for detaljhandelskanaler

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan et firma kan bruke Microsoft Dynamics 365 Commerce til å vise estimert beholdningstilgjengelighet for produkter i nett- og butikkanaler.

## <a name="accuracy-of-inventory-availability"></a>Nøyaktighet for lagertilgjengelighet

Commerce bruker flere servere og databaser for å sikre skalerbarhet og ytelse. Det er derfor viktig at du forstår at de tilgjengelige beholdningsverdiene som gis via POS-programmet (salgssted), e-Commerce API-ene for beholdningstilgjengelighet (APIer) og lagerbeholdningssidene i Commerce Headquarters ikke kan være 100 prosent nøyaktig i sanntid. Hvis transaksjoner som er opprettet for produkter i nett- eller butikkanalen ennå ikke er synkronisert med Headquarters, kan det hende at lagerbeholdningssidene i Headquarters ikke viser en nøyaktig lagerverdi i sanntid for disse produktene. Hvis du har konfigurert firmaet slik at brukere i Headquarters eller andre integrerte programmer kan selge, motta, returnere eller på annen måte justere lageret ut av en butikk eller et elektronisk lager, kan det hende at salgsstedet eller den elektroniske kanalen ikke har all informasjon som kreves for å vise nøyaktige sanntidsverdier for varer.

Det er viktig å forstå at alle tilgjengelige lagerbeholdningsdata som oppgis i løpet av driftsdagen, regnes som en anslått verdi. Hvis du prøver å sammenligne lagerbeholdningsinformasjonen som programmet har, med faktisk fysisk lager på hyllene, eller hvis du prøver å sammenligne lagerbeholdnings verdiene som vises i salgsstedet med lagerbeholdningsdataene du finner for det samme lageret i Headquarters, kan verdiene være forskjellige. Denne forskjellen i løpet av driftsdagen er forventet og må ikke regnes som et problem. Hvis du vil revidere data og kontrollere at verdiene som oppgis på salgsstedet, i API-ene og i headquarters, samsvarer med de faktiske fysiske enhetene du finner på butikken eller i lagerhyllene, er det best å gjøre det etter at kanaloperasjonene er stoppet for dagen, og alle transaksjoner er riktig synkronisert mellom headquarters og kanalene.

## <a name="channel-side-inventory-calculation"></a>Lagerberegning på kanalsiden

Lagerberegningen på kanalsiden er en mekanisme som tar de siste kjente kanallagerdataene i Commerce Headquarters som en basislinje og deretter faktorer i flere lagerendringer som oppstod på kanalsiden, som ikke er inkludert i denne basislinjen for å beregne en forhåndsberegnet lagerbeholdning i nær sanntid. 

Følgende lagerendringer vurderes for øyeblikket i logikken for lagerberegning på kanalsiden:

- Lager solgt via hentesalgstransaksjoner i butikk
- Lager solgt via kundeordrer i butikk eller online-kanal
- Lager returnert til butikk
- Lager oppfylt (plukk, pakke, forsendelse) fra butikklager

Hvis du vil bruke lagerberegningen på kanalsiden, må du aktivere funksjonen **Beregning av optimalisert produkttilgjengelighet**.

Hvis Commerce-miljøet er i versjon **10.0.8 til 10.0.11**, kan du gjøre følgende:

1. I Commerce Headquarters går du til **Retail og Commerce** \> **Delte handelsparametere**.
1. I kategorien **Beholdning** i feltet **Produkttilgjengelighetsjobb** velger du **Bruk optimalisert prosess for produkttilgjengelighetsjobb**.

Hvis Commerce-miljøet er i versjon **10.0.12 eller senere**, kan du gjøre følgende:

1. I Commerce Headquarters går du til **Arbeidsområder \> Funksjonsbehandling** og aktiverer funksjonen **Beregning av optimalisert produkttilgjengelighet**.
1. Hvis nettkanalene og butikkkanalene bruker de samme oppfyllelseslagrene, må du også aktivere funksjonen for **utvidet logikk for lagerberegning på e-handelskanalene**. På den måten vil beregningslogikken på kanalsiden vurdere de uposterte transaksjonene som opprettes i butikkkanalen. (Disse transaksjonene kan være hentesalgstransaksjoner, kundeordrer og returer.)
1. Kjør jobben **1070** (**Kanalkonfigurasjon**).

Hvis Commerce-miljøet ble oppgradert fra en versjon som er tidligere enn Commerce versjon 10.0.8, etter at du har aktivert funksjonen **Beregning av optimalisert produkttilgjengelighet**, må du også kjøre **Initialiser handelsplanlegger** for at funksjonen skal tre i kraft. For å kjøre initialisering går du til **Retail og Commerce** \> **Hovedkvarteroppsett** \> **Handel-planlegger**.

Før du kan bruke lagerberegningen på kanalsiden, må du sende et periodisk øyeblikksbilde av lagerdata fra hovedkontoret som opprettes av **Produkttilgjengelighet**-jobben, til kanaldatabasene. Det statiske utvalget representerer informasjonen som Headquarters har om beholdningstilgjengelighet for en bestemt kombinasjon av et produkt eller en produktvariant og et lager. Det omfatter bare lagertransaksjonene som ble behandlet og postert i Headquarters da øyeblikksbildet ble tatt, og det kan hende at det ikke er 100 prosent nøyaktig i sanntid på grunn av den konstante salgsbehandlingen som skjer på tvers av distribuerte servere.

- Hvis beholdningen ble solgt for et produkt i en butikk via hentesalgs- eller asynkront kundeordresalg i POS-programmet, har ikke Headquarters direkte informasjon om den tilknyttede lageravgangstransaksjonen for salget. Headquarters vil ha informasjon om beholdningen som er solgt for disse typene butikksalg, bare etter at P-jobben laster opp den tilknyttede transaksjonen fra butikkens kanaldatabase til Headquarters, og de tilknyttede salgsordrene opprettes via utdragspostering eller posteringsprosessene for fordelingsfeed. Prosessen med å opprette ordren i Headquarters oppretter de tilknyttede beholdningstransaksjonene. 
- For ordrer for e-handelskanalen har Headquarters bare informasjon om beholdningstransaksjonene etter at transaksjonene er sendt til Headquarters via P-jobben og ordresynkroniseringsprosessen er fullført.

Følg denne fremgangsmåten for å ta et øyeblikksbilde av lager i Commerce Headquarters.

1. Gå til **Retail og Commerce \> IT for Retail og Commerce \> Produkter og beholdning \> Produkttilgjengelighet**.
1. Velg **OK** for å kjøre jobben **Produkttilgjengelighet**. Du kan også planlegge denne jobben, slik at den kjøres i et parti.

Når jobben **Produkttilgjengelighet** er ferdig kjørt, må dataene som ble tatt opp, sendes til kanaldatabasene, slik at det siste statiske utvalget av Headquarters-beholdningen kan vurderes i beregningen av den estimerte lagerbeholdningen.

Følg denne fremgangsmåten for å synkronisere øyeblikksbildedata fra hovedkontoret til kanaldatabasene.

1. Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.
1. Kjør jobben **1130** (**Produkttilgjengelighet**) for å synkronisere dataene fra det statiske utvalget som jobben **Produkttilgjengelighet** opprettet fra Headquarters til kanaldatabasene dine.

## <a name="inventory-availability-apis-for-e-commerce"></a>API-er for lagertilgjengelighet for e-handel

Commerce inneholder følgende APIer for e-handelscenarier for å spørre etter lagertilgjengelighet for et produkt:

- **GetEstimatedAvailability** – Bruk denne API-en til å spørre etter lagerbeholdning for et produkt eller en produktvariant i det elektroniske kanallageret eller lagrene som er koblet til den elektroniske kanalens innfrielsesgruppe.
- **GetEstimatedProductWarehouseAvailability** – Bruk denne API-en til å spørre om beholdning for et produkt eller en produktvariant fra et bestemt lager.

> [!NOTE]
> Disse API-ene erstatter API-ene **GetProductAvailabilities** og **GetAvailableInventoryNearby** i Commerce-versjon 10.0.7 og tidligere.

Begge APIer brukes internt i beregningslogikken på kanalsiden og returner estimert **fysisk tilgjengelig** antall, **totalt tilgjengelig antall** , **måleenhet (UoM)** og **lagernivå** for det ønskede produktet og lageret. De returnerte verdiene kan vises på ditt e-handelsområde hvis du vil, eller de kan brukes til å utløse andre forretningslogikker på ditt e-handelsområde. Du kan for eksempel hindre innkjøp av produkter med et lager uten lagernivå.

Selv om andre API-er som er tilgjengelige på Commerce-serveren, kan gå direkte til headquarters for å hente lagerbeholdningsantall for produkter, anbefaler vi ikke at de brukes i et miljø med e-handel, på grunn av potensielle ytelsesproblemer og den relaterte innvirkningen som disse hyppige forespørslene kan ha på Headquarters-serverne. Med beregning på kanalsiden kan de to APIene som er nevnt ovenfor, i tillegg gi et mer nøyaktig estimat over tilgjengeligheten til et produkt ved å ta hensyn til transaksjonene som er opprettet i kanalene som ennå ikke er kjent for headquarters.

Følg denne fremgangsmåten for å definere hvordan produktantallet skal returneres i API-resultatet.

1. Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> Handelsparametere**.
1. Velg kategorien **Lager**. Deretter konfigurerer du verdien for innstillingen **Antall i API-utdata** i hurtigfanen for **Lagertilgjengelighet for APIer for e-Commerce**.
1. Kjør jobben **1070** (**Kanalkonfigurasjon**) for å synkronisere den siste innstillingen for kanalene.

Innstillingen **Antall i API-utdata** gir tre alternativer:

- **Returlagerantall** – Fysisk tilgjengelig og totalt tilgjengelig antall for et forespurt produkt returneres i API-utdata.
- **Returlagerantall som trekker fra lagerbufferen** – Antallet som returneres i API-utdataene, justeres ved å trekke fra lagerbufferverdien. Hvis du vil ha mer informasjon om lagerbufferen, kan du se [Konfigurere lagerbuffere og lagernivåer](inventory-buffers-levels.md).
- **Ikke returlagerantall** – Bare lagernivået returneres i API-utdataene. Hvis du vil ha mer informasjon om lagernivå, kan du se [Konfigurere lagerbuffere og lagernivåer](inventory-buffers-levels.md).

Du kan bruke `QuantityUnitTypeValue`-API-parameteren til å angi enhetstypen du vil at APIene skal returnere antall i. Denne parameteren støtter alternativene **lagerenheten** (standard), **innkjøpsenhet** og **salgsenhet**. Det returnerte antallet avrundes til den definerte presisjonen i tilsvarende måleenhet (måleenhet) i hovedkontoret.

**GetEstimatedAvailability**-API-en tilbyr følgende inndataparametere som støtter forskjellige spørringsscenarier:

- `DefaultWarehouseOnly` – Bruk denne parameteren til å spørre etter lagerbeholdning for et produkt i den elektroniske k+analens standardlager. 
- `FilterByChannelFulfillmentGroup` og `SearchArea` – Bruk disse to parameterne til å spørre etter lager for et produkt fra alle plukklokasjoner innenfor et bestemt søkeområde, basert på `longitude`, `latitude` og `radius`. 
- `FilterByChannelFulfillmentGroup` og `DeliveryModeTypeFilterValue` – Bruk disse to parameterne til å spørre etter lagerbeholdning for et produkt fra bestemte lagre som er koblet til innfrielsesgruppen for en online-kanal, og er konfigurert til å støtte bestemte leveringsmåter. Parameteren `DeliveryModeTypeFilterValue` støtter alternativene **alle** (standard), **forsendelse** og **henting**. I et scenario der en nettordre kan oppfylles fra flere forsendelseslagre, kan du for eksempel bruke disse to parameterne til å utføre spørringer mot tilgjengelighet av et produkts lager i alle disse forsendelseslagrene. API-en i dette tilfellet returnerer produktets beholdningsantall og lagernivå i hvert forsendelseslager, pluss et aggregert antall og et akkumulert lagernivå fra alle forsendelseslagre i spørringsområdet.
 
Commerce-modulene kjøpsboks, butikkvelger, ønskerliste, handlekurv og handlekurvikon bruker APIene og parameterne som er nevnt ovenfor, for å vise lagernivåmeldinger for hele e-handelområdet. Commerce-områdebygger inneholder ulike lagerinnstillinger for å kontrollere salgs- og innkjøpsvirkemåten. For mer informasjon, se [Bruke beholdningsinnstillinger](inventory-settings.md).

## <a name="pos-inventory-lookup-with-channel-side-calculation"></a>Lageroppslag for salgssted med beregning på kanalsiden

I Commerce-versjon 10.0.9 og tidligere brukte operasjonen **Beholdningsoppslag** på salgsstedet et servicekall i sanntid til Headquarters for å få beholdningsinformasjon for det valgte produktet, både for brukerens gjeldende butikk og andre butikker som er konfigurert for oppfyllelsesgruppen som en del av kanalkonfigurasjonen for butikken. I Commerce-versjon 10.0.10 og senere kan du slå av serviceanrop i sanntid til hovedkontoret og i stedet bruke beregning på kanalsiden på Commerce-serveren til å fastslå lagerbeholdningen som er fysisk tilgjengelig for butikken og andre lokasjoner som er definert i innfrielsesgruppen. Denne kanalberegnede lagerkonfigurasjonen er også nyttig for steder der Internett-tilkoblingen er upålitelig, fordi du ikke behøver å være tilkoblet for å få lageroppslag fra hovedkvarteret.

Når beregning på kanalsiden er riktig konfigurert og administrert, kan det gi et mer pålitelig estimat over gjeldende butikkbeholdning, fordi dette bruker transaksjonsdataene som er i handelskanaldatabasen, men som hovedkvarteret kanskje ikke har informasjon om ennå. Hvis du for eksempel bruker det eksisterende servicekallet i sanntid for lageroppslag på salgsstedet, vil ikke hovedkvarteret ennå ha informasjon om kontantsalg som akkurat har skjedd for et produkt. Derfor vil lagerbeholdningsverdien som er returnert av hovedkvarteret for dette produktet, sannsynligvis overskride butikkens faktiske lagerbeholdning med én enhet. Hvis du imidlertid bruker beregning på kanalsiden, kan kontantsalget faktoreres inn i beregningen og trekkes fra beholdningsverdien som vises. Selv om verdiene som både kanalsiden og servicekallet i sanntid oppgir, bare er estimater av lagerbeholdningen, er verdien som beregning på kanalsiden oppgir, mye mer sannsynlig å være nøyaktig for den gjeldende butikken.

Hvis du vil konfigurere **Lageroppslag** for salgsstedet i Commerce Headquarters for å bruke beregningslogikken på kanalsiden og slå av servicekall i sanntid, må du først aktivere funksjonen **Beregning av optimalisert produkttilgjengelighet** via arbeidsområdet **Funksjonsbehandling** i Commerce Headquarters, og deretter følge denne fremgangsmåten.

1. Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Funksjonalitetsprofiler**.
1. Velg en funksjonalitetsprofil.
1. I hurtigfanen **Funksjoner**, i delen **Beregning av lagertilgjengelighet** endrer du verdien i feltet **Modus for beregning av lagertilgjengelighet** fra **Sanntidstjeneste** til **Kanal**. Som standard bruker alle funksjonalitetsprofiler servicekall i sanntid. Du må endre verdien i dette feltet hvis du vil bruke logikken for beregning på kanalsiden. Hver detaljhandelsbutikk som er koblet til den valgte funksjonalitetsprofilen, påvirkes av denne endringen.

Du må deretter synkronisere endringene i kanalene via distribusjonsplanprosessen i Headquarters, ved å gjøre følgende:

1. Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.
1. Kjør jobben **1070** (**Kanalkonfigurasjon**).

Når konfigurasjonen er fullført, bruker informasjonen som er oppgitt om fysisk tilgjengelig lager, ikke lenger et servicekall i sanntid når en bruker i POS-programmet bruker operasjonen **Lageroppslag** (standard- og matrisevisning). I stedet beregnes data om fysisk tilgjengelig lager for den gjeldende butikken og alle butikkene i oppfyllelsesgruppen på grunnlag av det siste kjente statiske utvalget som ble levert til kanaldatabasen fra Commerce Headquarters. Verdien for det statiske utvalget revideres ytterligere av beregningen på kanalsiden for å justere den fysisk tilgjengelige verdien, basert på andre salgs- eller returtransaksjoner som finnes for det valgte produktet i kanaldatabasen, og som ikke var inkludert i det siste synkroniserte øyeblikksbildet fra 1130-jobben. Hvis kanaldatabasen ikke inneholder transaksjonsdata for noen av lagrene eller butikkene i oppfyllelsesgruppen, inneholder den ingen ekstra transaksjoner som kan beregnes i en omberegning av verdien. Derfor er det beste estimatet for lagerbeholdningen som kan vises for disse lagrene eller butikkene, dataene fra det siste kjente statiske utvalget for Commerce Headquarters.

Skjermene **Ordreoppfyllelse** i POS drar også nytte av beregningen på kanalsiden for å vise lagerbeholdning for varer når en ordreoppfyllelseslinje er valgt, og en bruker viser **Detaljer**-panelet for lagerbeholdningen for den valgte varen.

## <a name="optimize-your-inventory-data"></a>Optimalisere beholdningsdataene

Hvis du vil sikre det best mulige estimatet for lageret, er det viktig at du bruker følgende satsvise jobber for handel og kjører dem ofte:

- **P-jobben** – P-jobben finnes på siden **Ddistribusjonsplaner** og bør kjøres ofte. Denne jobben bringer e-handelsordrer, asynkrone kundeordrer som POS oppretter, og kontantbestillinger som er opprettet fra kanaldatabasene, til Commerce Headquarters, slik at de kan behandles videre. Før disse dataene er synkronisert fra kanalen til Commerce Headquarters, har ikke Commerce Headquarters informasjon om lagerjusteringer av produkter i lagrene som blir resultatet av disse transaksjonene.
- **Synkroniser ordrer** – Denne jobben behandler rå transaksjonsdata i Commerce Headquarters som P-jobben tilbyr, og konverterer e-handel og asynkrone kundeordretransaksjoner til salgsordrer i Commerce Headquarters. Før denne jobben er behandlet og salgsordrene er opprettet, blir det ikke opprettet noen lagertransaksjoner. Lagerbeholdningen i Commerce Headquarters vil derfor ikke vurdere transaksjonene.
- **Beregn transaksjonsutdrag satsvis** – For kontanttransaksjoner som opprettes i butikken, sikrer fordelingsfeedposteringen at lageret som er knyttet til salget, oppdateres effektivt. Hvis du vil ha den mest effektive behandlingen av lagertransaksjoner for kontant, må du konfigurere systemet til å bruke [fordelingsfeedpostering](./trickle-feed.md).
- **Poster transaksjonsutdrag satsvis** – Denne jobben er også nødvendig for fordelingsfeedpostering. Den følger etter jobben **Beregn transaksjonsutdrag satsvis**. Denne jobben posterer de beregnede utdragene systematisk, slik at salgsordrer for kontantsalg opprettes i Commerce Headquarters og Commerce Headquarters mer nøyaktig gjenspeiler butikkens lager.
- **Produkttilgjengelighet** – Denne jobben oppretter et øyeblikksbilde av lageret fra Commerce Headquarters.
- **1130 (Produkttilgjengelighet)** – Denne jobben finnes på siden **Distribusjonsplaner**, og bør kjøres umiddelbart etter jobben **Produkttilgjengelighet**. Denne jobben transporterer lagerutvalgsdata fra Commerce Headquarters til kanaldatabasene.

> [!NOTE]
> - Det er god praksis å kjøre **Produkttilgjengelighet** og **1130**-jobber på en timesbasis og planlegge P-jobb, synkronisere ordrer og fordelingsfeedbaserte jobber med samme eller høyere frekvens.
> - Av hensyn til ytelsen vil beregningen bruke en hurtigbuffer for å finne ut om det er gått lang nok tid til å rettferdiggjøre kjøring av logikken på nytt, når beregninger av beholdningstilgjengelighet på kanalsiden brukes til å lage en forespørsel om beholdningstilgjengelighet ved hjelp av API-er for e-handel eller beholdningslogikken på POS-kanalsiden. Standard hurtigbuffer er satt til 60 sekunder. Du har for eksempel slått på beregning på kanalsiden for butikken og vist lagerbeholdningen for et produkt på siden oppslags **Beholdningsoppslag**. Hvis én enhet av produktet deretter blir solgt, vil ikke siden **Beholdningsoppslag** vise den reduserte beholdningen før hurtigbufferen er tømt. Når brukere har postert transaksjoner i POS, skal de vente 60 sekunder før de kontrollerer at lagerbeholdningen er redusert.

Hvis forretnings krever mindre buffertid, kan du kontakte kundestøtterepresentanten for å få assistanse.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
