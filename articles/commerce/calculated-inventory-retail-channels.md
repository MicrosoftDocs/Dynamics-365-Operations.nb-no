---
title: Beregne beholdningstilgjengelighet for detaljhandelskanaler
description: Dette emnet beskriver alternativene som er tilgjengelige for å vise lagerbeholdningen for butikken og Internett-kanalene.
author: hhainesms
manager: annbe
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: de4ee98198f441b8f42a8a55aa5ff1015f485234
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414631"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Beregne beholdningstilgjengelighet for detaljhandelskanaler

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan et firma kan bruke Microsoft Dynamics 365 Commerce til å vise estimert beholdningstilgjengelighet for produkter i nett- og butikkanaler.

## <a name="accuracy-of-calculation"></a>Beregningens nøyaktighet

Commerce bruker flere servere og databaser for å sikre skalerbarhet og ytelse. Det er derfor viktig at du forstår at de tilgjengelige beholdningsverdiene som gis via POS-programmet (salgssted), e-Commerce API-ene for beholdningstilgjengelighet (APIer) og lagerbeholdningssidene i Commerce Headquarters ikke kan være 100 prosent nøyaktig i sanntid. Hvis transaksjoner som er opprettet for produkter i nett- eller butikkanalen ennå ikke er synkronisert med Commerce Headquarters-serveren og -databasen, kan det hende at lagerbeholdnings sidene i Commerce Headquarters ikke viser en nøyaktig lagerverdi i sanntid for disse produktene. Hvis du har konfigurert firmaet slik at brukere i Commerce Headquarters eller andre integrerte programmer kan selge, motta, returnere eller på annen måte justere lageret ut av en butikk eller et elektronisk lager, kan det hende at salgsstedet eller den elektroniske kanalen ikke har all informasjon som kreves for å vise en nøyaktig beholdningsverdi for varer i sanntid.

Dette emnet beskriver datasynkroniseringsprosessene som kan kjøres ofte for å begrense ventetiden for data mellom programmer og kanaler. Det er imidlertid viktig at du forstår at alle tilgjengelige lagerbeholdningsdata som oppgis i løpet av driftsdagen, regnes som en anslått verdi. Hvis du prøver å sammenligne lagerbeholdningsinformasjonen som programmet har, med faktisk fysisk lager på hyllene, eller hvis du prøver å sammenligne lagerbeholdnings verdiene som vises i salgsstedet med lagerbeholdningsdataene du finner for det samme lageret i Commerce Headquarters, kan verdiene være forskjellige. Denne forskjellen i løpet av driftsdagen er forventet og må ikke regnes som et problem. Hvis du vil revidere data og kontrollere at verdiene som oppgis i API-ene for lagertilgjengelighet og i handelshovedkvarteret samsvarer med de faktiske fysiske enhetene du finner på butikken eller i lagerhyllene, er det best å gjøre det etter at kanaloperasjonene er stoppet for dagen, og alle transaksjoner er riktig synkronisert mellom handelshovedkvarteret og kanalen.

## <a name="use-inventory-lookup-apis-for-e-commerce-inventory-availability-requests"></a>Bruk AP-Ier for lageroppslag for e-handelsforespørsler om lagertilgjengelighet

Du kan bruke følgende API-er til å vise lagertilgjengelighet for et produkt når kundene handler i et område for e-handel.

- **GetEstimatedAvailability** – Bruk denne API-en til å få lagertilgjengelighet for varen i lageret for e-handelskanalen eller alle lagre som er koblet til konfigurasjonen av oppfyllelsesgruppen for e-handelskanalen. Denne API-en kan også brukes på lagre i et bestemt søkeområde eller en radius, basert på data lengdegrad og breddegrad.
- **GetEstimatedProductWarehouseAvailability** – Bruk denne API-en til å be om beholdning for en vare fra et bestemt lager. Du kan for eksempel bruke den til å vise lagertilgjengelighet i scenarioer som involverer ordreplukking.

> [!NOTE]
> Disse API-ene erstatter API-ene **GetProductAvailabilities** og **GetAvailableInventoryNearby** i Dynamics 365 Retail versjon 10.0.7 og tidligere.

Begge API-ene henter data fra Commerce-serveren og gir et overslag over lagerbeholdningen for en bestemt kombinasjon av et produkt eller en produktvariant og et lager. Selv om andre API-er som er tilgjengelige på Commerce-serveren, kan gå direkte til handelshovedkvarteret for å hente lagerbeholdningsantall for produkter, anbefaler vi ikke at de brukes i et miljø med e-handel, på grunn av potensielle ytelsesproblemer og den relaterte innvirkningen som disse hyppige forespørslene kan ha på Commerce Headquarters-serverne. Hvis lagerbeholdningen blir beregnet gjennom Commerce-serveren, er det mer sannsynlig at beregningen tar med varer som ble solgt i nylige e-handelstransaksjoner som ennå ikke er synkronisert til Commerce Headquarters. Selv om det er mulig at Commerce Headquarters ikke har informasjon om disse transaksjonene, har Commerce-serveren og kanaldatabasen dataene. Derfor blir det tatt hensyn til dataene, og dette kan bidra til å gi et mer nøyaktig estimat over den tilgjengelige beholdningen for et produkt.

### <a name="get-started-with-e-commerce-calculated-inventory-availability"></a>Kom i gang med beregnet lager tilgjengelighet for e-handel

Før du bruker de to APIene som ble nevnt tidligere, må du aktivere funksjonen **Beregning av optimalisert produkttilgjengelighet** via arbeidsområdet **Funksjonsbehandling** i Commerce Headquarters.

Før API-ene kan beregne det beste estimatet for beholdningstilgjengelighet for en vare, må et periodisk statisk utvalg av beholdsningstilgjengelighet fra Commerce Headquarters behandles og sendes til kanaldatabasen som Commerce Scale Unit for e-handel bruker. Det statiske utvalget representerer informasjonen som Commerce Headquarters har om beholdningstilgjengelighet for en bestemt kombinasjon av et produkt eller en produktvariant og et lager. Dette kan inkludere lagerjusteringer eller bevegelser som forårsakes av lagertilganger, eller av forsendelser eller andre prosesser som utføres i Commerce Headquarters, og som e-handelskanalen har informasjon om, bare på grunn av synkroniseringsprosessen.

Det statiske utvalget av databasen som jobben **Produkttilgjengelighet** oppretter, beregner bare beholdningstransaksjonene som ble behandlet og postert i Commerce Headquarters da det statiske utvalget ble tatt. Hvis beholdningen ble solgt for et produkt i et butikklager gjennom et kontantsalg eller et asynkront kundeordresalg i POS-programmet, har ikke Commerce Headquarters direkte informasjon om den tilknyttede lageravgangstransaksjonen for salget. Det vil ha informasjon om beholdningen som er solgt for disse typene butikksalg, bare etter at P-jobben laster opp den tilknyttede transaksjonen fra butikkens kanaldatabase til Commerce Headquarters, og den tilknyttede salgsordren opprettes via utdragspostering eller posteringsprosessene for fordelingsfeed. Prosessen med å opprette ordren i Commerce Headquarters oppretter de tilknyttede beholdningstransaksjonene. For ordrer for e-handelskanalen har Commerce Headquarters bare informasjon om beholdningstransaksjonene, etter at transaksjonene er sendt til Commerce Headquarters via P-jobben, og ordresynkroniseringsprosessen er fullført. Det er derfor viktig at du forstår at verdien for lagerets statiske utvalg som er oppgitt i jobben **Produkttilgjengelighet**, ikke er 100 prosent nøyaktig i sanntid på grunn av den konstante salgsbehandlingen som skjer på tvers av distribuerte servere.

Følg denne fremgangsmåten for å ta et øyeblikksbilde av lager i Commerce Headquarters.

1. Gå til **Retail og Commerce \> IT for Retail og Commerce \> Produkter og beholdning \> Produkttilgjengelighet**.
1. Velg **OK** for å kjøre jobben **Produkttilgjengelighet**. Du kan også planlegge denne jobben slik at den kjøres i et parti.

Når jobben **Produkttilgjengelighet** er ferdig kjørt, må dataene som ble tatt opp, sendes til databasene for e-handelskanalen, slik at det siste statiske utvalget av Commerce Headquarters-beholdningen kan vurderes i beregningen av den estimerte lagerbeholdningen.

1. Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.
1. Kjør jobben **1130** (**Produkttilgjengelighet**) for å synkronisere dataene fra det statiske utvalget som jobben **Produkttilgjengelighet** opprettet fra Commerce Headquarters til kanaldatabasene dine.

Når beholdningstilgjengelighet forespørres fra fra API-en **GetEstimatedAvailability** eller **GetEstimatedProductWarehouseAvailability**, kjøres en beregning for å få best mulig beregning av beholdningen for produktet. Beregningen refererer til en hvilken som helst e-handelskundeordre i kanaldatabasen, men som ikke ble tatt med i dataene for det statiske utvalget som 1130-jobben leverte. Denne logikken utføres ved å spore den siste behandlede lagertransaksjonen fra Commerce Headquarters og sammenligne den med transaksjonene i kanaldatabasen. Det gir et utgangspunkt for logikken for beregning på kanalsiden, slik at de ekstra lagerflyttingene som oppstod for salgstransaksjoner for kundeordre i kanal for e-handel, kan settes sammen til den estimerte lagerverdien som API-en viser.

Logikken for beregning av kanalsiden returnerer en estimert fysisk tilgjengelig verdi og en total tilgjengelig verdi for det forespurte produktet og lageret. Verdiene kan vises på ditt e-handelsområde hvis du vil, eller de kan brukes til å utløse andre forretningslogikker på ditt e-handelsområde. Du kan for eksempel vise en "ikke på lager"-melding i stedet for det faktiske lagerantallet som API-en sendte.

Beregningslogikken som API-ene for e-handel på kanalsiden bruker for den estimerte lagerverdien, kan evaluere lageret basert bare på kundeordrer som er opprettet i kanaldatabasen, men som ennå ikke er synkronisert og postert i Commerce Headquarters. Hvis kanaldatabasen også inneholder transaksjonsdata for kontantsalg for butikkspesifikke lagre, vil kontantsalget ikke faktoreres til beregning av ehandel på kanalsiden for disse lagrene.

## <a name="configure-the-inventory-lookup-operation-in-the-pos-channel"></a>Konfigurer lageroppslagsoperasjonen i POS-kanalen

I Retail versjon 10.0.9 og tidligere brukte operasjonen **Beholdningsoppslag** fra POS et servicekall i sanntid til Commerce Headquarters for å få beholdningsinformasjon for det valgte produktet, både for brukerens gjeldende butikk og andre butikker som er konfigurert for oppfyllelsesgruppen som en del av kanalkonfigurasjonen for butikken. I Commerce versjon 10.0.10 og senere kan du slå av servicekall i sanntid til Commerce Headquarters. I stedet kan du bruke beregning på kanalsiden på Commerce-serveren til å fastslå lagerbeholdningen som er fysisk tilgjengelig for butikken og andre lokasjoner som er definert i oppfyllelsesgruppen. Denne kanalberegnede lagerkonfigurasjonen er også nyttig for steder der Internett-tilkoblingen er upålitelig, fordi du ikke behøver å være tilkoblet for å få lageroppslag fra Commerce Headquarters.

Når beregning på kanalsiden er riktig konfigurert og administrert, kan det gi et mer pålitelig estimat over gjeldende butikkbeholdning, fordi dette bruker transaksjonsdataene som er i handelskanaldatabasen, men som Commerce Headquarters kanskje ikke har informasjon om ennå. Hvis du for eksempel bruker det eksisterende servicekallet i sanntid for lageroppslag i POS, vil ikke Commerce Headquarters ennå ha informasjon om kontantsalg som akkurat har skjedd for et produkt. Derfor vil lagerbeholdningsverdien som er returnert av Commerce Headquarters for dette produktet, sannsynligvis overskride butikkens faktiske lagerbeholdning med én enhet. Hvis du imidlertid bruker beregning på kanalsiden, kan kontantsalget faktoreres inn i beregningen og trekkes fra beholdningsverdien som vises. Selv om verdiene som både kanalsiden og servicekallet i sanntid oppgir, bare er estimater av lagerbeholdningen, er verdien som beregning på kanalsiden oppgir, mye mer sannsynlig å være nøyaktig for den gjeldende butikken.

### <a name="get-started-with-pos-channel-side-calculated-inventory-availability"></a>Kom i gang med beregnet lagertilgjengelighet for POS-kanalsiden

Hvis du vil bruke logikken for beregning av tilgjengelighet og slå av sanntidstjenestekall for lageroppslag fra salgsstedsappen, må du først aktivere funksjonen **Beregning av optimalisert produkttilgjengelighet** via arbeidsområdet **Funksjonsbehandling** i Commerce Headquarters. I tillegg til å aktivere funksjonen, må du endre **funksjonalitetsprofilen**.

Hvis du vil endre **funksjonalitetsprofilen**, gjør du følgende:

1. Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Funksjonalitetsprofiler**.
1. Velg en funksjonalitetsprofil.
1. I hurtigfanen **Funksjoner**, i delen **Beregning av lagertilgjengelighet** endrer du verdien i feltet **Modus for beregning av lagertilgjengelighet** fra **Sanntidstjeneste** til **Kanal**. Som standard bruker alle funksjonalitetsprofiler servicekall i sanntid. Derfor må du endre verdien i dette feltet hvis du vil bruke logikken for beregning på kanalsiden. Hver detaljhandelsbutikk som er koblet til den valgte funksjonalitetsprofilen, påvirkes av denne endringen.

Du må deretter synkronisere endringene i kanalen via distribusjonsplanprosessen, ved å gjøre følgende:

1. Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.
1. Kjør jobben **1070** (**Kanalkonfigurasjon**).

Når konfigurasjonen er fullført, bruker informasjonen som er oppgitt om fysisk tilgjengelig lager, ikke lenger et servicekall i sanntid når en bruker i POS-programmet bruker operasjonen **Lageroppslag** (standard- og matrisevisning). I stedet beregnes data om fysisk tilgjengelig lager for den gjeldende butikken og alle butikkene i oppfyllelsesgruppen på grunnlag av det siste kjente statiske utvalget som ble levert til kanaldatabasen fra Commerce Headquarters. Verdien for det statiske utvalget revideres ytterligere av beregningen på kanalsiden for å justere den fysisk tilgjengelige verdien, basert på andre salgs- eller returtransaksjoner som finnes for det valgte produktet i kanaldatabasen, og som ikke var inkludert i det siste synkroniserte øyeblikksbildet fra 1130-jobben. Hvis kanaldatabasen ikke inneholder transaksjonsdata for noen av lagrene eller butikkene i oppfyllelsesgruppen, inneholder den ingen ekstra transaksjoner som kan beregnes i en omberegning av verdien. Derfor er det beste estimatet for lagerbeholdningen som kan vises for disse lagrene eller butikkene, dataene fra det siste kjente statiske utvalget for Commerce Headquarters.

Skjermene **Ordreoppfyllelse** i POS drar også nytte av beregningen på kanalsiden for å vise lagerbeholdning for varer når en ordreoppfyllelseslinje er valgt, og en bruker viser **Detaljer**-panelet for lagerbeholdningen for den valgte varen.

## <a name="optimize-your-inventory-data"></a>Optimalisere beholdningsdataene

Hvis du vil sikre det best mulige estimatet for lageret, er det viktig at du bruker følgende satsvise jobber for handel og kjører dem ofte:

- **P-jobben** – P-jobben finnes på siden **Ddistribusjonsplaner** og bør kjøres ofte. Denne jobben bringer e-handelsordrer, asynkrone kundeordrer som POS oppretter, og kontantbestillinger som er opprettet fra kanaldatabasene, til Commerce Headquarters, slik at de kan behandles videre. Før disse dataene er synkronisert fra kanalen til Commerce Headquarters, har ikke Commerce Headquarters informasjon om lagerjusteringer av produkter i lagrene som blir resultatet av disse transaksjonene.
- **Synkroniser ordrer** – Denne jobben behandler rå transaksjonsdata i Commerce Headquarters som P-jobben tilbyr, og konverterer e-handel og asynkrone kundeordretransaksjoner til salgsordrer i Commerce Headquarters. Før denne jobben er behandlet og salgsordrene er opprettet, blir det ikke opprettet noen lagertransaksjoner. Lagerbeholdningen i Commerce Headquarters vil derfor ikke vurdere transaksjonene.
- **Beregn transaksjonsutdrag satsvis** – For kontanttransaksjoner som opprettes i butikken, sikrer fordelingsfeedposteringen at lageret som er knyttet til salget, oppdateres effektivt. Hvis du vil ha den mest effektive behandlingen av lagertransaksjoner for kontant, må du konfigurere systemet til å bruke [fordelingsfeedpostering](https://docs.microsoft.com/dynamics365/commerce/trickle-feed).
- **Poster transaksjonsutdrag satsvis** – Denne jobben er også nødvendig for fordelingsfeedpostering. Den følger etter jobben **Beregn transaksjonsutdrag satsvis**. Denne jobben posterer de beregnede utdragene systematisk, slik at salgsordrer for kontantsalg opprettes i Commerce Headquarters og Commerce Headquarters mer nøyaktig gjenspeiler butikkens lager.
- **Produkttilgjengelighet** – Denne jobben oppretter et øyeblikksbilde av lageret fra Commerce Headquarters.
- **1130 (Produkttilgjengelighet)** – Denne jobben finnes på siden **Distribusjonsplaner**, og bør kjøres umiddelbart etter jobben **Produkttilgjengelighet**. Denne jobben transporterer lagerutvalgsdata fra Commerce Headquarters til kanaldatabasene.

Det anbefales at du ikke kjører disse satsvise jobbene for ofte (med bare noen minutters mellomrom). Hyppige kjøringer vil overbelaste Commerce Headquarters (HQ) og kan påvirke ytelsen. Generelt er det god praksis å kjøre produkttilgjengelighet og 1130-jobber på en timesbasis, og planlegge P-jobb, synkronisere ordrer og trickle feed posteringsrelaterte jobber med samme eller høyere frekvens.

> [!NOTE]
> Av hensyn til ytelsen vil beregningen bruke en hurtigbuffer for å finne ut om det er gått lang nok tid til å rettferdiggjøre kjøring av logikken på nytt, når beregninger av beholdningstilgjengelighet på kanalsiden brukes til å lage en forespørsel om beholdningstilgjengelighet ved hjelp av API-er for e-handel eller den nye beholdningslogikken på POS-kanalsiden. Standard hurtigbuffer er satt til 60 sekunder. Du har for eksempel slått på beregning på kanalsiden for butikken og vist lagerbeholdningen for et produkt på siden oppslags **Beholdningsoppslag**. Hvis én enhet av produktet deretter blir solgt, vil ikke siden **Beholdningsoppslag** vise den reduserte beholdningen før hurtigbufferen er tømt. Når brukere har postert transaksjoner i POS, skal de vente 60 sekunder før de kontrollerer at lagerbeholdningen er redusert.

Hvis forretnings krever mindre buffertid, kan du kontakte kundestøtterepresentanten for å få hjelp.


[!INCLUDE[footer-include](../includes/footer-banner.md)]