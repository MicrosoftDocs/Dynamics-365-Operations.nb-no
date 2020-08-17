---
title: Automatisering av betalingsforslag for leverandører
description: Dette emnet beskriver hvordan organisasjoner som betaler leverandører i henhold til en regelmessig plan, kan automatisere prosessen med å generere betalingsforslag for leverandører.
author: kweekley
manager: AnnBe
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: a1e3305bff99fa39240176ac9fc7aaee84b98e6c
ms.sourcegitcommit: be51e892003778e71b67fb409a8e16965c89b5ac
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/23/2020
ms.locfileid: "3618417"
---
# <a name="automate-vendor-payment-proposals"></a>Automatisering av betalingsforslag for leverandører

[!include [banner](../includes/banner.md)]

Organisasjoner som betaler leverandører i henhold til en regelmessig plan, kan nå automatisere prosessen med å generere betalingsforslag for leverandører. Automatisering av betalingsforslag for leverandører definerer følgende detaljer:

- Når betalingsforslag kjøres
- Hvilke kriterier som brukes for å velge fakturaene som skal betales
- Hvilken journal for leverandørbetaling de resulterende betalingene blir lagret i

Automatisering av betalingsforslag fører ikke til at betalingene posteres automatisk. Du kan derfor fortsette å bruke alle validerings- og arbeidsflytprosesser du bruker for øyeblikket, for å godkjenne betalingene som opprettes.

## <a name="define-the-occurrence-of-vendor-payment-proposals"></a>Definer forekomsten av leverandørbetalingsforslag

Automatisering av leverandørbetalingsforslag bruker rammeverket for prosessautomatisering. Forskjellige forretningsprosesser bruker dette rammeverket til å definere gjentakelsen av en valgt prosess. Når det gjelder betalingsforslag for leverandører, kan du få tilgang til automatisering på **Leverandører \> Betalingsprosess \> Prosessautomatisering**.

Først bruker du **Opprett ny prosess**-automatiseringsvalget, og velger **Betalingsforslag for leverandører**. En veiviser fører deg deretter gjennom prosessen med å definere leverandørbetalingsforslaget.

## <a name="general-page"></a>Generelt-siden

På **Generelt**-siden i veiviseren angir du navnet på leverandørbetalingsforslaget du oppretter. Hvis du for eksempel betaler alle innenlandsleverandører med bankoverføring på mandag, angir du et beskrivende navn som for eksempel **Innenlands\_bank**. Navnet du angir, vises i ukesvisningen for prosessautomatisering i **Leverandørbetalinger**-arbeidsområdet.

Deretter definerer du eieren av betalingsjournalen som ble opprettet. Eieren er vanligvis den hos leverandøren som er ansvarlig for betalingsjournalen etter at den er opprettet.

De gjenværende innstillingene på siden er generiske, og brukes til å definere forekomstmønsteret for denne versjonen av leverandørbetalingsforslaget. Hvis for eksempel en forekomst gjelder bankoverføringer på mandag, kan du definere den slik at den kjøres ukentlig, og du kan velge mandag som dagen i uken når den kjøres. Du kan også angi en tidlig planleggingstid, for eksempel kl. 02.00, slik at prosessautomatiseringen fullføres før neste arbeidsdag begynner.

Det er viktig at du har forstått at du bruker veiviseren til å definere når leverandørbetalingsforslaget skal behandles. Du definerer ikke når leverandørbetalinger skal genereres, skrives ut og posteres. I ukesvisningen vises prosessautomatisering for leverandørbetalingsforslag på de dagene som er valgt i forekomstmønsteret.

Hvis du vil ha mer informasjon om de andre feltene på **Generelt** -siden, kan du se dokumentasjonen for prosessautomatisering.

## <a name="vendor-payment-proposal-page"></a>Leverandørbetalingsforslag-siden

Den neste siden i veiviseren er **Leverandørbetalingsforslag**-siden. Den brukes til å definere kriteriene for å velge leverandørfakturaene som skal betales. Generelt sett finnes vanligvis de samme alternativene i betalingsforslaget i leverandørbetalingsjournalen. Det finnes imidlertid noen få unntak. Alle datoer på denne siden må for eksempel være definert som relative datoer, fordi datoen for betalingsforslaget endres hver gang forslaget kjøres.

### <a name="journal-name"></a>Journalnavn

**Journalnavn**-feltet definerer journalnavnet som leverandørbetalingene opprettes i. Resultatene av automatisering av leverandørbetalingsforslag oppretter betalinger i den definerte journalen, men journalen posteres ikke.

### <a name="from-date-and-to-date"></a>"Fra"-dato og "til"-dato

I stedet for å definere en "fra"-dato og en "til"-dato for å velge fakturaer basert på forfallsdatoen eller kontantrabattdatoen, må du bruke alternativet **Definer kriterier for "til"-dato** og feltet **Antall dager for justering av "til"-dato** for definere "til"-datoen. Det finnes ikke noe konsept som tilsvarer en "fra"-dato i automatisering av betalingsforslag.

Som standard er **Definer kriterier for "til"-dato**-alternativet satt til **Nei**. Hvis du bruker denne standardverdien, vil prosessen velge alle fakturaer for betaling når prosessen kjøres, fordi det ikke er definert noen "til"-dato.

Hvis du setter **Definer kriterier for "til"-dato** til **Ja**, bruker du **Antall dager for justering av "til"-dato**-feltet til å definere datoen når fakturaer velges som det angitte antallet dager før eller etter datoen når prosessen kjøres. Tallet kan være positivt, negativt eller 0 (null). Systemet vil deretter betale fakturaer der forfallsdatoene eller kontantrabattdatoene tilsvarer det angitte antallet dager før eller etter datoen når prosessen kjøres. For alle fakturaer som forfaller på eller før fredag, vil betalingsserien for eksempel opprette betalinger til alle leverandører via bankoverføring på onsdag. I dette tilfellet angir du **antall dager med justering for "til"-dato**-feltet til **2**. Når forekomsten av betalingsforslaget kjøres onsdag 25. mars, blir alle fakturaer som har forfallsdato eller kontantrabattdato på eller før 27. mars, valgt for betaling.

### <a name="minimum-payment-date"></a>Minste betalingsdato

Den minste betalingsdatoen definerer den tidligste datoen som brukes når betalinger opprettes. Du må først sette **Definer minimumskriterier for betalingsdato**-alternativet til **Ja**. Ved hjelp av denne innstillingen kan du bruke funksjonaliteten for minste betalingsdato. Hvis dette alternativet er satt til **Ja**, bruker du **Antall dager for justering av minste betalingsdato**-feltet til å definere den minste betalingsdatoen som det angitte antallet dager før eller etter datoen når prosessen kjøres. Tallet kan være positivt, negativt eller 0 (null). Betalingsseriene genererer for eksempel betalinger på onsdag som inkluderer alle betalinger som har en minstedato som tilsvarer foregående mandag. I dette tilfellet angir du **Antall dager med justering for minste betalingsdato**-feltet til **-2**.

Her er et eksempel som viser hvordan feltene for "til"-datoen og minste betalingsdato fungerer sammen. Automatisering av betalingsforslag er konfigurert for kjøring på onsdag. **Antall dager for justering av "til"-dato**-feltet er satt til **1** for å definere "til"-datoen på grunnlag av forfallsdatoen. **Antall dager med justering for minste betalingsdato**-feltet er satt til **-2**. Hvis automatisering av betalingsprosessen starter på onsdag 25. mars, vil alle fakturaer som forfaller på eller før 26. mars, bli inkludert i betalingsforslaget. Betalingsforslag genereres på følgende måte:

- Alle fakturaer som forfaller på eller før 23. mars, får 23. mars som betalingsdato.
- Fakturaer som forfaller 24. mars, får 24. mars som betalingsdato.
- Fakturaer som forfaller 25. mars, får 25. mars som betalingsdato.
- Fakturaer som forfaller 26. mars, får 26. mars som betalingsdato.

### <a name="summarized-payment-date"></a>Dato for summert betaling

Den summerte betalingsdatoen brukes bare når **Periode**-feltet er satt til **Totalt** for betalingsmåten for fakturaene. Hvis **Periode**-feltet er satt til **Totalt** for betalingsmåtene dine, må du sette **Definer kriterier for summert betalingsdato** til **Ja**. Hvis dette alternativet er satt til **Ja**, bruker du **Antall dager for justering av summert betalingsdato**-feltet til å definere den summerte betalingsdatoen som det angitte antallet dager før eller etter datoen når prosessen kjøres. Tallet kan være positivt, negativt eller 0 (null). Serien genererer for eksempel betalinger på onsdag, og firmaet ønsker å opprette en summert betaling på onsdag. I dette tilfellet angir du **Antall dager med justering for summert betalingsdato**-feltet til **0**.

### <a name="records-to-include"></a>Poster som skal inkluderes

Filteralternativene kan fremdeles defineres for betalingsforslaget. Hvis et filter er definert, vises ikke filterkriteriene på veivisersiden. De kan imidlertid vises ved å åpne filteret på nytt.

De gjenværende feltene for forslaget fungerer på samme måte som for betalingsforslaget i journalen for leverandørbetaling. Hvis du vil ha informasjon om de andre feltene, kan du se [Opprette leverandørbetalinger ved hjelp av et betalingsforslag](create-vendor-payments-payment-proposal.md).

> [!NOTE]
> Enkelte land-/områdespesifikke felt og noen felt for offentlige sektor er ennå ikke tilgjengelige i automatisering av leverandørbetalingsforslag.

Vi anbefaler at du vurderer om automatiseringen er nyttig for organisasjonen, basert på behovene deres.

## <a name="view-the-results-of-a-vendor-payment-proposal-automation"></a>Se resultatene av en automatisering av leverandørbetalingsforslag

Når automatiseringsserien for leverandørbetalingsforslag er opprettet, vises forekomstene for hver enkelt betaling i ukevisningen for prosessautomatisering. For leverandørbetalinger er ukesvisningen av prosessautomatisering lagt til både i **Leverandørbetalinger**-arbeidsområdet og på **Prosessautomatisering**-siden.

[![Ukesvisning for prosessautomatisering i Leverandørbetalinger-arbeidsområdet](./media/vendor-payment-proposal-1.png)](./media/vendor-payment-proposal-1.png)

Ukesvisningen for prosessautomatisering i **Leverandørbetalinger**-arbeidsområdet viser bare automatiseringer av leverandørbetalingsforslag. Den viser alle forekomster av betalinger for den gjeldende uken, for alle juridiske enheter som den påloggede brukeren har sikkerhetstillatelser for. Hvis for eksempel AP-betalingsassistenten er ansvarlig for betalinger i USMF- og USSI-firmaene, vil vedkommende se forekomstene av automatisering av leverandørbetalingsforslag for disse to firmaene, men ikke for andre firmaer.

[![Ukesvisning for prosessautomatisering av USMF- og USSI-firmaene](./media/vendor-payment-proposal-2.png)](./media/vendor-payment-proposal-2.png)

Hver forekomst viser firmaet som betalingsjournalen ble eller blir opprettet for. Hvis betalinger opprettes ved hjelp av sentraliserte betalinger, vises firmaet som betalinger opprettes for. Forekomsten viser ikke nødvendigvis hvilke firmaer hvis fakturaer skal betales.

Navnet på hver forekomst vises også for å gjøre det enklere å identifisere betalingsforslaget.

I tillegg vises statusen for hver forekomst. Følgende statuser brukes:

- **Planlagt** – betalingsforslaget er planlagt, men ikke kjørt ennå.
- **Feil** – betalingsforslaget er kjørt, men det oppstod en feil. Du kan se feilene ved å velge **Vis resultater**-knappen.
- **Fullført** – betalingsforslaget er kjørt uten feil. Du kan se betalingene ved å velge **Vis betalinger**-koblingen. Denne koblingen åpner betalingsjournalen som ble opprettet av forekomsten.

Når betalingene er opprettet, kan du vise betalingsbeløpene i journalen. Beløpene vises i transaksjonsvalutaene. Hvis betalingsjournalen for eksempel inneholder betalinger i både amerikanske dollar og kanadiske dollar, vises de totale betalingene for hver enkelt valuta. 

Betalingsjournalen kan slettes etter at den er opprettet gjennom prosessautomatisering. Hvis en betaling slettes fullstendig, oppstår følgende hendelser:

- Statusen for prosessautomatiseringen for uken forblir **Fullført**.
- Prosessen fjerner betalingssummene, og **Vis betalinger**-koblingen erstattes av **Vis resultater**-knappen.
- Når du ser resultatene, får du en melding om at den opprinnelige journalen ble slettet.

Når en betaling er slettet, åpnes fakturaene for betaling igjen. Du kan deretter opprette en ny forekomst for å betale fakturaene på nytt.

## <a name="edit-a-vendor-payment-proposal-automation"></a>Rediger en automatisering av betalingsforslag for leverandør

Ved hjelp av rammeverket for prosessautomatisering kan du redigere betalingen, seriene og forekomstene som er opprettet for betalingsforslaget. Serien kan redigeres enten fra siden for **Prosessautomatisering** eller den ukentlige visningen for prosessautomatisering. Hvis AP-administratoren for eksempel bestemmer seg for å generere alle betalinger til innenlandske leverandører på onsdag i stedet for mandag, kan han eller hun finne en forekomst i den ukentlige visningen, og velge **Vis/Rediger – Serier**. Hvis du redigerer en serie, blir du bedt om å angi om endringen skal gjøres i alle eksisterende forekomster, eller bare i nye forekomster. Historiske forekomster som allerede har statusen **Fullført**, eller som ble avsluttet i en **Feil**-status, endres ikke.

Du kan også legge til en ny forekomst eller endre en eksisterende forekomst. Eksempel: Den neste betalingsforslagsforekomsten er planlagt for kjøring onsdag 1. januar, men denne datoen er en rød dag. Du kan endre forekomsten enten fra ukesvisningen for prosessautomatisering eller fra siden for **Prosessautomatisering**. En side åpnes som viser plandetaljene og kriteriene for betalingsforslaget. Her kan du redigere planlagt klokkeslett og dato. Du kan også redigere kriteriene for betalingsforslaget hvis det kreves endringer. Hvis du for eksempel endrer den planlagte datoen for betalingsforekomsten fra 1. januar til 2. januar, vil du kanskje også endre de tilsvarende datoene for "til"-datoen.

Du kan også deaktivere en forekomst eller en serie. Hvis du vil deaktivere en forekomst og utsette behandlingen av den, velger du den i ukesvisningen for prosessautomatisering og velger deretter **Deaktiver**. Du kan deaktivere en serie på **Prosessautomatisering**-siden.

## <a name="security-for-payment-proposal-automations"></a>Sikkerhet for automatisering av betalingsforslag

Følgende plikter og rettigheter er lagt til automatisering av leverandørbetalingsforslag. Disse pliktene og rettighetene er standard sikkerhetsinnstillinger, men de kan endres basert på organisasjonens behov. Hvis for eksempel ikke bare AP-administratoren, men også AP-betalingsassistenten kan redigere og opprette regelmessighetsplaner, tilordner du **Oppretthold tidsplanforekomster**-plikten til personen som har rollen som AP-betalingsassistent.

| Plikt                              | Rolle                                                                       | Rettigheter |
|-----------------------------------|----------------------------------------------------------------------------|------------|
| Oppretthold tidsplanserier          | Regnskapssjef leverandørreskontro                                                   | Denne plikten gir rett til å opprette og vedlikeholde automatiseringsseriene for betalingsforslag samt forekomster via følgende rettigheter:<ul><li>Oppretthold tidsplanforekomster</li><li>Oppretthold tidsplanserier</li><li>ProcessScheduleOccurrenceListMaintain</li><li>Se ukentlig visning av forekomster</li></ul> |
| Forespørsel om tidsplanforekomster | Betalingsassistent for leverandør, sentralisert betalingsassistent for leverandør | Denne plikten gir rett til å vise forekomster av automatisering av betalingsforslag via følgende rettigheter:<ul><li>Se tidsplanforekomster</li><li>Se ukentlig visning av forekomst</li></ul> |
| Forespørsel om tidsplanserier      | None                                                                       | Denne plikten gir rett til å vise innstillingene for serien og forekomster via følgende rettigheter:<ul><li>Se tidsplanforekomster</li><li>Se listeside over forekomster</li><li>Se ukentlig visning av forekomst</li></ul>|
| Oppretthold tidsplanforekomster     | None                                                                       | Denne plikten gir rett til å opprette og vedlikeholde en forekomst via følgende rettigheter:<ul><li>Oppretthold tidsplanforekomster</li><li>Se ukentlig visning av forekomst</li></ul> |
