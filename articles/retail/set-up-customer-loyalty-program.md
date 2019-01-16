---
title: Fordelsoversikt
description: "Dette emnet beskriver fordelsfunksjonene i Microsoft Dynamics 365 for Retail og de tilhørende oppsettrinnene som hjelper forhandleren med å komme i gang med sine fordelsprogrammer."
author: scott-tucker
manager: AnnBe
ms.date: 10/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailLoyaltyPrograms, RetailPriceDiscGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16201
ms.assetid: f79559d2-bc2d-4f0b-a938-e7a61524ed80
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 09d4e46694e89b648981352f64da4a43ab1522e1
ms.contentlocale: nb-no
ms.lasthandoff: 01/04/2019

---

# <a name="loyalty-overview"></a>Fordelsoversikt

[!include [banner](includes/banner.md)]

Fordelsprogrammer kan hjelpe deg med å øke kundenes lojalitet gjennom å belønne kunder for deres interaksjon med forhandlerens merke. I Microsoft Dynamics 365 for Retail kan du definere enkle eller komplekse fordelsprogrammer som gjelder på tvers av juridiske enheter i enhver detaljhandelskanal. Dette emnet beskriver fordelsfunksjonene i Microsoft Dynamics 365 for Retail og de tilhørende oppsettrinnene som hjelper forhandleren med å komme i gang med sine fordelsprogrammer.

Du kan definere fordelsprogrammet slik at det inneholder følgende alternativer:

- Definer flere typer belønninger du tilbyr i fordelsprogrammene, og spor deltakelse i fordelsprogrammene.
- Definer fordelsprogrammer som representerer de ulike fordelsinsentivene du tilbyr. Du kan inkludere fordelsprogramlag for å gi større insitamenter og fordeler for kunder som handler oftere eller bruker mer penger i butikkene.
- Definer opptjeningsregler for å identifisere aktivitetene som en kunde må fullføre for å oppnå fordeler. Du kan også definere innløsingsregler for å identifisere når og hvordan en kunde kan løse inn fordeler.
- Utsted fordelskort fra en hvilken som helst kanal for detaljhandel som deltar i fordelsprogrammet, og koble fordelskort til ett eller flere fordelsprogrammer som kunden kan delta i. Du kan også koble en kundepost til et fordelskort for å la kunden samle fordelspoeng fra flere kort og løse dem inn.
- Juster fordelskort manuelt, eller overføre fordelssaldoen fra ett kort til et annet for å ta hensyn til eller belønner en kunde.

## <a name="setting-up-loyalty-programs"></a>Konfigurering av fordelsprogrammer

Du må definere flere komponenter for å aktivere fordelsfunksjonen i Dynamics 365 for Retail. Diagrammet nedenfor illustrerer fordelskomponentene og hvordan de er relatert til hverandre.

![Lojalitetsoppsett, prosessflyt](./media/loyaltyprocess.gif "Lojalitetskomponenter og hvordan de er relatert til hverandre")

## <a name="loyalty-components"></a>Fordelskomponenter

Tabellen nedenfor beskriver hver komponent og hvor den brukes i fordelsoppsettet.

| Komponent                                        | beskrivelse | Hvor den brukes |
|--------------------------------------------------|-------------|-----------------|
| Definere rabatter (forutsetning)                  | Definer rabattene du tilbyr fordelskundene. Du kan for eksempel gi 5 prosent avslag på alle klesprodukter. | Rabatter må legges til prisgrupper for å bli inkludert i et fordelsprogram. Prisgrupper tilordnes fordelsprogrammer og lojalitetslag. |
| Definee prisgrupper (forutsetning)               | Prisgruppene brukes til å opprette og administrere priser og rabatter for detaljhandelsprodukter. Definere prisgrupper som inneholder rabattene som gjelder for fordelsprogrammene. | Prisgrupper tilordnes fordelsprogrammene og lojalitetslagene. |
| Definere kanaler (forutsetning)                   | Detaljhandelskanaler er butikker som deltar i fordelsprogrammene, for eksempel fysiske butikker, nettbutikker eller telefonsentre. Du må definere detaljsalgskanaler før du kan tilordne fordelsprogrammer til dem. | Du tilordner detaljhandelskanaler til et fordelsprogram hvis detaljhandelskanalen deltar i fordelsprogrammet. |
| Definere betalingsmåte for fordel (forutsetning) | Du må definere en betalingsmåte før et fordelskort kan brukes i en kasse, og før det kan innløses fordelspoeng som del av et fordelsprogram. Du må også legge til fordelsbetalingsmåten i detaljhandelskanalen før kunder kan løse inn fordelspoengene som betaling for produkter. | Definer en betalingsmåte for fordelstypen, og tilordne deretter fordelsbetalingsmåten til detaljhandelskanalene som deltar i fordelsprogrammet. |
| Definer datointervaller                            | Datointervaller er en fleksibel måte å angi tidsrommet som gjelder for fordelslag. Bruk datointervaller for å angi hvor lenge en kunde kan bli på et lag eller hvor lang tid en kunde har på å fullføre en aktivitet for å være kvalifisert for et lag. | Datointervaller gjelder bare hvis du bruker lag i fordelsprogrammene. Du velger datointervallet som gjelder for programlag, samt datointervallene som gjelder regler for programlag. |
| Definere fordelspoent                             | Fordelspoeng er fordelstypene du tilbyr kundene dine. Fordelspoeng kan være innløsbare eller ikke-innløsbare. Fordelspoeng som kan løses inn, kan byttes mot produkter. Fordelspoeng som ikke kan løses inn brukes til sporingsformål eller for å flytte en kunde til det neste laget i et fordelsprogram. | Fordelspoeng er nevnt i lagregler og brukes til å kvalifisere en kunde for et bestemt lag. Det refereres også til fordelspoeng i fordelsplaner i reglene for opptjening og innløsning. I opptjeningsregler angir du fordelene som en kunde kan oppnå for en bestemt aktivitet. I innløsingsregler angir du fordelen som kunden kan løse inn. |
| Konfigurere fordelsprogrammer                          | Fordelsprogrammer er hovedlojalitetsenheten du tilbyr. Hver fordelsprogram kan også ha tilordnede fordelslag. Rabatter og prisgrupper er tilordnet fordelsprogrammer enten på programnivå eller lagsnivå. | Du oppretter fordelsplaner for fordelsprogrammene. Du tilordner fordelskort til fordelsprogrammene, og fordelskort kan tilordnes til en kunde. Detaljhandelskanaler deltar i fordelsprogrammene som er tilordnet til fordelsplanene. Kunder som har et fordelskort, kan delta i fordelsprogrammer som er tilordnet til kortet. |
| Definere fordelslag og lagregler              | Fordelslag er valgfrie nivåer som du kan definere for fordelsprogrammer. Du kan definere grunnleggende rabatter og fordeler for alle kunder som deltar i fordelsprogrammet, og du kan definere flere rabatter og fordeler for kunder som når de ulike nivåene i programmet. For hvert fordelslag du definerer, kan du definere reglene som kvalifiserer en kunde for dette laget. Du kan også angi hvor lenge kunder kan være på dette laget etter at de har nådd det. | Regler for fordelsklasser og fordelslag er definert i fordelsprogrammene. Hvis du ikke definerer fordelslag, er alle kunder som skal deltar i fordelsprogrammet, kvalifisert for rabatten du tilordner i prisgruppen for fordelsprogrammet. Hvis du definerer fordelslag, kan du definere opptjeningsregler og innløsingsregler for fordelslagene i fordelsskjemaet. |
| Konfigurere fordelsplaner                           | Fordelsplaner angir opptjenings- og innløsingsreglene som gjelder for et bestemt fordelsprogram. Du tilordner detaljhandelskanaler til en fordelsplan for å identifisere hvilke fordelsprogrammer, opptjeningsregler og innløsingsregler som gjelder for en detaljhandelbutikk. | En fordelsplan tilordnes et fordelsprogram og kanaler for detaljhandel. Du kan tilordne mange fordelsplaner til samme fordelsprogram, og du kan tilordne mange fordelsplaner til mange detaljhandelskanaler. |
| Konfigurere fordelskort                             | Et fordelskort gir kortolderen mulighet til å delta i fordelsprogrammer som er tilordnet til kortet. Fordelskort kan utstedes anonymt, eller de kan tilordnes til en bestemt kunde. Du kan vise fordelstransaksjoner for et bestemt kort, og du kan vise et sammendrag av fordelspoeng som har blitt samlet på kortet. Du kan utstede fordelskort fra en hvilken som helst detaljhandelskanal. Du kan også manuelt justere et fordelskort for å oppgradere kunden til et annet lag, legge til fordelspoeng eller overføre fordelspoengsaldoen fra ett kort til et annet. | Du tilordner fordelsprogrammer til et fordelskort. |

## <a name="loyalty-processes"></a>Lojalitetsprosesser

Tabellen nedenfor beskriver prosessene som må kjøres for å sende fordelskonfigurasjoner og data til butikkene, og hente fordelstransaksjoner fra butikkene.

| Prosessnavn                         | Beskrivelse | Sidenavn |
|--------------------------------------|-------------|-----------|
| 1050 (fordelsinformasjon)           | Kjør denne prosessen for å sende fordelsdataene fra Dynamics 365 for Retail til detaljhandelbutikkene. Det er lurt å planlegge denne prosessen til å kjøres ofte, slik at fordelsdata sendes til alle butikker. | Distribusjonsplan |
| Behandle fordelsplaner              | Kjør denne prosessen for å knytte fordelsplaner til detaljhandelskanalene som fordelsplanen er tilordnet til. Denne prosessen kan planlegges å kjøres som en satsvis prosess. Hvis du endrer fordelskonfigurasjonsdata, for eksempel fordelsplaner, fordelsprogrammer eller fordelspoeng, må du kjøre denne prosessen. | Behandle fordelsplaner |
| Behandle frakoblede fordelstransaksjoner | Kjør denne prosessen for å oppdatere fordelskort til å ta med transaksjoner som ble behandlet frakoblet. Denne prosessen gjelder bare hvis det er merket av for **Opptjen frakoblet** på siden **Delte parametere for detaljhandel**, slik at belønninger kan opptjenes frakoblet. | Behandle frakoblede fordelstransaksjoner |
| Oppdater lag for fordelskort            | Kjør denne prosessen for å evaluere kundens opptjeningsaktivitet mot reglene for lag i et fordelsprogram, og oppdater kundens lagstatus. Denne prosessen kreves bare hvis du endrer lagreglene i fordelsprogrammer og du vil at de oppdaterte reglene skal brukes i ettertid for fordelskort som allerede er utstedt. Denne prosessen kan kjøres som en satsvis prosess eller for individuelle kort. | Oppdater lag for fordelskort |

## <a name="loyalty-enhancements"></a>Fordelsforbedringer

Retail har nye fordelsfunksjoner som en del av oktober 2018-utgivelsen. Hver av de nye forbedringene blir forklart nedenfor.

- Som en del av en fordelsplan i tidligere versjoner kunne forhandlerne opprette forskjellige opptjenings- og innløsingsregler etter lag for å skille fordelene for kunder i ulike lag. Forhandlere kan nå inkludere "tilknytninger" som en del av inntjenings- og innløsningsreglene, slik at visse kundegrupper kan være en del av eksisterende lag, men likevel tjene opp på en annen måte. Dette forhindrer behovet for å opprette flere lag.
    
    > [!NOTE]
    > Opptjeningsreglene i en fordelsplan kommer i tillegg. Hvis du for eksempel oppretter en regel som belønner et gullnivåmedlem med 10 poeng for hvert amerikanske dollar, og du også oppretter en regel for en kunde med "veteran"-tilknytning, slik at en fordel på 5 poeng for hvert amerikanske dollar oppnås, vil en veteran som også er gullmedlem, oppnå 15 poeng for 1 amerikansk dollar, fordi kunden er kvalifisert for begge. Men hvis veterankunden ikke er gullmedlem, vil han oppnå 5 poeng for hver dollar. For å gjenspeile endringene i kanalene, kan du kjøre **Behandle fordelsplaner**- og **1050**-jobbene (fordelskortinformasjon).
    
    ![Tilknytningsbasert opptjening](./media/Affiliation%20based%20earning.png "Tilknytningsbasert opptjening")

- Forhandlere har ofte spesialpriser for en bestemt gruppe av kunder som de ikke vil at fordelsprogrammene skal gjelde for. For eksempel grossister eller ansatte som får spesialpriser og ingen fordelspoeng. "Tilknytninger" brukes vanligvis til å gi spesialpriser til slike kundegrupper. Hvis du vil hindre at bestemte kundegrupper oppnår fordelspoeng, kan forhandleren angi én eller flere tilknytninger i delen **Utelatte tilknytninger** i fordelsplanen. På denne måten, når kunder som tilhører ekskluderte tilknytninger, allerede er fordelsmedlemmer, vil de ikke kunne oppnå fordelspoeng for innkjøpene sine. For å gjenspeile endringene i kanalene, kan du kjøre **Behandle fordelsplaner**- og **1050**-jobbene (fordelskortinformasjon).

    ![Utelatte tilknytninger](./media/Excluded%20affiliations.png "Utelate tilknytninger fra å tjene opp fordelspoeng")
    
- Forhandlere kan generere fordelskortnumre i kanalene. Før oktober 2018-oppdateringen kunne forhandlerne bruke fysiske fordelskort eller generere et fordelskort ved hjelp av en unik kundeinformasjonen, for eksempel et telefonnummer. Hvis du vil aktivere den automatiske genereringen av fordelskort i detaljhandel, kan du slå på **Generer fordelskortnummer** i funksjonalitetsprofilen som er knyttet til butikken. For Internett-kanaler kan forhandlerne bruke API-en IssueLoyaltyCard til å utstede fordelskort til kunder. Forhandlere kan enten oppgi et fordelskortnummer til denne API-en, som skal brukes til å generere fordelskortet, eller systemet vil bruke fordelskortnummerserien i Dynamics 365 for Retail. Men hvis nummerserien ikke finnes, og forhandleren ikke oppgir et fordelskortnummer ved å kalle opp API-en, vises en feilmelding.

    ![Generer fordelskort](./media/Generate%20loyalty%20card.png "Generer fordelskortnummer automatisk")

- Opptjente og innløste fordelspoeng lagres nå for hver transaksjon og salgsordre mot salgslinjen, slik at det samme beløpet kan refunderes eller hentes tilbake ved fullstendige eller delvise returer. I tillegg gir poengsynlighet på salgslinjenivå mulighet for telefonsenterbrukere å svare på kundespørsmål om hvor mange poeng som er opptjent eller innløst for hver linje. Før denne endringen ble alltid fordelspoeng kalkulert på nytt under returnerer, som resulterte i et annet beløp enn det opprinnelige hvis opptjenings- eller innløsningsreglene ble endret. Dessuten hadde ikke telefonsenterbrukere synlighet med hensyn til poengnedbryting. Poengene vises i skjemaet **Korttransaksjoner** for hvert fordelskort.    
- Forhandlere kan nå definere rettighetsperioden for hvert fordelspoeng. En rettighetsperiodekonfigurasjon definerer varigheten fra opptjeningsdatoen, og deretter blir fordelspoengene tilgjengelige for kundene. Ikke opptjente poeng vises i kolonnen **Ikke opptjente poeng** på siden **Fordelskort**. Forhandlere kan også definere grensen for maksimale fordelspoeng per fordelskort. Dette feltet kan brukes til å redusere virkningen av fordelssvindel. Når de maksimale fordelspoengene er nådd, kan ikke brukeren få flere poeng. Forhandlere kan velge å blokkere slike kort helt til de har undersøkt en potensiell svindel. Hvis forhandleren avdekker svindel, kan ikke forhandleren bare blokkere fordelskortet for kunden, men også merke til kunden som blokkert. Hvis du vil gjøre dette, kan du sette egenskapen **Blokker kunde for fordelsregistrering** til **Ja** under **Alle kunder** på hurtigkategorien **Detaljhandel**. De blokkerte kundene vil ikke kunne få utstedt et fordelskort i noen av kanalene.

    ![Opptjening og maksimalt antall fordelspoeng](./media/Vesting%20and%20maximum%20reward%20points.png "Definere opptjening og maksimalt antall fordelspoeng")

- Tilknytninger brukes til å gi spesiell prissetting og rabatter, men det finnes noen tilknytninger som forhandlerne ikke vil at kundene skal se. En tilknytningen med navnet "Kunde med stort forbruk" vil kanskje ikke bli godt mottatt av noen kunder. Det finnes dessuten noen tilknytninger som ikke bør administreres i butikken, for eksempel ansatte, fordi du ikke vil at kasserere skal avgjøre hvem som er en ansatt, og dermed gi ansattbaserte rabatter. Forhandlere kan nå velge tilknytninger som bør skjules i detaljhandelskanalene. Tilknytningsforhold merket som **Skjul i kanaler**, kan ikke vises, legges til eller fjernes på salgsstedet. Prissettingen og rabattene som er knyttet til tilknytningen, vil imidlertid fortsatt brukes på produktene.

    ![Skjul tilknytninger](./media/Hide%20affiliations.png "Skjul tilknytninger i kanaler")
    
- Telefonsenterbrukere kan nå enklere søke etter en kunde med deres fordelskortinformasjon og navigere til kundens fordelskort- og fordelskorttransaksjonssider fra siden **Kundeservice**.

    ![Kundeservice](./media/Customer%20service.png "Finn lojalitetsinformasjon for kunden")
    
- Hvis et fordelskort settes på spill, må et erstatningskort genereres, og de eksisterende poengene må overføres til det nye kortet. Erstatningskortflyten er forenklet i denne versjonen. I tillegg kan kunder gi noen eller alle fordelspoengene til venner og familie. Når det overføres poeng, opprettes poengjusteringsposter for hvert fordelskort. Funksjonaliteten for erstatningskortet og saldooverføring er tilgjengelig på siden **Fordelskort**.

    ![Erstatt og overfør poeng](./media/Replace%20and%20transfer%20points.png "Erstatt fordelskort eller overfør saldo")
    
- Forhandlere vil kanskje registrere effektiviteten til en bestemt kanal for å registrere kundene i et fordelsprogram. Registreringskilden for fordelskortene er nå lagret slik at forhandlere kan kjøre rapporter på disse dataene. Registreringskilden registreres automatisk for alle utstedte fordelskort fra MPOS/CPOS eller e-handelskanaler. For fordelskort som er utstedt fra back office-programmet, kan telefonsenterbrukeren velge en riktig kanal.
- I tidligere versjoner kunne forhandlere bruke MPOS/CPOS til å løse inn fordelspoeng for kunder i en butikk. I disse versjonene kunne ikke kassereren vise valutaverdibeløpet som kunne brukes mot den gjeldende transaksjonen, fordi fordelssaldoen vises i fordelspoeng. Kassereren måtte utføre valutaomregning på poengene før betaling med fordelspoeng. I den gjeldende versjonen, etter at linjer er lagt til i transaksjonen, kan kassereren se beløpet som fordelspoengene kan dekke for den gjeldende transaksjon, noe som gjør det enkelt å bruke noen av eller alle fordelspoengene på transaksjonen. Kassereren kan også se poengene som utløper neste 30 dagene, slik at de kan utføre mersalg eller kryssalg for å motivere kunden til å bruke poengene som utløper på den gjeldende transaksjonen.

    ![Poeng som dekkes av fordelssaldoen](./media/Points%20covered%20by%20loyalty%20balance.png "Vis saldo som dekkes av fordelspoeng")

    ![Poeng som utløper](./media/Expiring%20points.png "Vis poeng som utløper")
    
## <a name="upcoming-enhancements"></a>Forestående forbedringer

Følgende funksjoner vil være tilgjengelige i de fremtidige månedlige oppdateringene av Dynamics 365 for Retail.
    
- Kunder ønsker muligheten til å vise sine fordelssaldodetaljer på kanalene som er rettet mot forbruker. På samme måte er det viktig for kasserere å vise kundens logg for fordelspoeng i MPOS/CPOS, for å svare raskt på spørsmål fra kunden. I en kommende månedlige utgivelse, vil kunder og kasserere kunne se historikken for fordelsdetaljer.
- Mange forhandlere kan gi fordelspoeng bare basert på salgstransaksjonene, men jo mer vil kundefokuserte forhandlere belønne kundene for å engasjere seg i merkevaren deres. De vil for eksempel gi fordeler for å fylle ut en Internett-undersøkelse, besøke en butikk, like forhandlerne på Facebook, tvitre om forhandlere og så videre. I fremtiden vil vi legge til muligheten til å gi fordelspoeng for all kundeaktivitet. For å gjøre dette kan forhandleren definere "Andre aktivitetstyper" og definere opptjeningsreglene for disse aktivitetene. Vi vil også vise en detaljhandelsserver-API som kan kalles opp når en aktivitet identifiseres som bruker opptjeningsregelen til å tildele de nødvendige fordelspoengene.
- For å aktivere en ekte omnikanal-detaljhandelsopplevelse lar vi kundene tjene opp og løse inn fordelspoeng på tvers av alle kanaler.
- Gratis eller til rabattert levering er et av de svært motivering faktorene for kunder som handler på Internett. For å gjøre det mulig for forhandlerne å definere forsendelseskampanjer, skal vi introduserer en ny type kampanje der forhandleren kan definere terskler som, når de er oppfylt, vil du gjøre kunder berettiget til rabattert eller gratis levering.

