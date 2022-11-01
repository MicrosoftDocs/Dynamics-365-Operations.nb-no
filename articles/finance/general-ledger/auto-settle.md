---
title: Automatisering av utligninger
description: Denne artikkelen inneholder generell informasjon om automatisering av utligninger.
author: abruer
ms.date: 9/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: b43eeeefa581b5d8b40dc2cf0187c7c781b18be3
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708334"
---
# <a name="automate-ledger-settlements"></a>Automatisering av utligninger

[!include [banner](../includes/banner.md)]

I Microsoft Dynamics 365 Finance versjon 10.0.31 er funksjonen **Automatiser utligninger** tilgjengelig i arbeidsområdet  **Funksjonsbehandling** . Du kan bare aktivere funksjonen **Automatiser utligninger** hvis funksjonen **Forståelse av finansutligning og årsavslutning** er aktivert.

Utligning er prosessen ved å samsvare debet- og kredittransaksjoner i økonomimodulen. Organisasjoner som utfører finansutligningsaktiviteter etter en regelmessig tidsplan, kan nå automatisere prosessen. Under den automatiske finansutligningsprosessen kan en debettransaksjon og en kredittransaksjon bare samsvares automatisk hvis beløpene i regnskapsvalutaen er like. Et debetbeløp på NOK 1,00 kan for eksempel samsvares automatisk med et kreditbeløp NOK 1,00. En debetverdi på NOK 1,00 samsvarer imidlertid ikke automatisk med to krediteringer, der hver verdi er NOK 0,50. Delvis samsvar av finanstransaksjonsbeløp støttes ikke.

Automatisk utligning definerer følgende detaljer:

- Når finansutligninger kjøres
- Hvilke kriterier som brukes til å samsvare debeter og krediter som kan utlignes automatisk
- Hvilken rekkefølge finansutligningsinformasjonen behandles i

## <a name="define-the-occurrence-of-ledger-settlements"></a>Definere forekomsten av finansutligninger

Automatisk utligning bruker Prosessautomatisering-rammeverket. Forskjellige forretningsprosesser bruker dette rammeverket til å definere gjentakelsen av en valgt prosess. For finansutligninger kan du gå til  **Systemadministrasjon \> Oppsett \> Prosessautomatiseringer** eller **Økonomimodul \> Finansoppsett \> Prosessautomatiseringer**.

Først velger du alternativet **Opprett ny prosessautomatisering** og deretter **Utligninger**. En veiviser fører deg deretter gjennom prosessen med å definere automatisering.

## <a name="general-page"></a>Generelt-siden

På **Generelt** -siden i veiviseren angir du navnet på utligningsforekomsten du oppretter. Hvis du for eksempel de samsvarende debiteringene og krediteringene utlignes på mandag, angir du et beskrivende navn,for eksempel **Utligning\_Man**. Navnet du angir, vises i kolonnen **Automatiseringsregel** på siden **Utligninger** .

De gjenværende innstillingene på siden er generiske, og brukes til å definere forekomstmønsteret for denne versjonen av finansutligningene. Hvis for eksempel en forekomst gjelder for mandag, kan du definere den slik at den kjøres ukentlig, og du kan velge mandag som dagen i uken når den kjøres. Du kan også angi en tidlig planleggingstid, for eksempel kl. 02.00, slik at prosessautomatiseringen fullføres før neste arbeidsdag begynner. Vi anbefaler at du planlegger automatisk behandling slik at den utføres utenfor den vanlige arbeidstiden. På denne måten kan du redusere innvirkningen regnskapspersonalet får på arbeidsdagen.

Hvis du vil ha mer informasjon om de andre feltene på **Generelt** -siden, kan du se dokumentasjonen for prosessautomatisering.

## <a name="ledger-settlements-match-criteria-page"></a>Siden Samsvarskriterier for utligninger

Neste side i veiviseren er siden **Samsvarskriterier for utligninger** . Den brukes til å definere hovedkontoene som skal tas med i prosessautomatiseringsforekomsten, og kriteriene som brukes til å bestemme samsvarende debeter og krediter.

### <a name="account-selection"></a>Kontovalg

Hovedkontoene du tidligere har definert som utligningskontoer for den juridiske enheten, vises. (Du definerer hovedkontoer som utligningskontoer i **Økonomimodul \> Finansoppsett \> Parametere for økonomimodul \> Utligninger**.)

### <a name="main-account-and-posting-layer"></a>Hovedkonto og posteringslag

Verdiene  **Hovedkonto** og **Posteringslag** er nødvendige samsvarskriterier. Verdiene **Hovedkonto** og **Posteringslag** for finansdebet- og kredittransaksjonene må ha samme posteringstype for å kunne samsvares under den automatiske utligningsprosessen.

### <a name="posting-type"></a>Posteringstype

Velg alternativet **Posteringstype** hvis finansdebet- og kredittransaksjonene må ha samme posteringstype for å kunne samsvares under den automatiske utligningsprosessen.

### <a name="financial-dimensions"></a>Finansdimensjoner

Velg alternativet **Finansdimensjoner** hvis finansdebet- og kredittransaksjonene må ha samme finansdimensjoner for å kunne samsvares under den automatiske utligningsprosessen. Når dette alternativet er valgt, må kriteriene for finansdimensjonsverdier velges i listen **Tilgjengelige finansdimensjoner**. Listen **Tilgjengelige finansdimensjoner** inneholder ikke hovedkontodimensjonen, fordi den kreves automatisk som en del av samsvarskriteriene.

## <a name="view-the-results-of-a-ledger-settlement-automation"></a>Se resultatene av en utligningsautomatisering

Når serien for utligningsautomatisering er opprettet, vises forekomstene for hver enkelt utligning i ukevisningen for prosessautomatisering. I tillegg vises statusen for hver forekomst. Følgende statuser brukes:

- **Planlagt**  – Automatiseringen er planlagt, men ikke kjørt ennå.
- **Utfører** – Automatiseringen kjører.
- **Feil**  – Automatiseringen er kjørt, men det oppstod en feil. Du kan se feilene ved å velge **Vis resultater** -knappen.
- **Fullført**  – Automatiseringen er kjørt uten feil. Du kan vise utligningsresultatene på siden **Utligninger**.

Hvis du vil vise de samsvarende resultatene, kan du gå **Økonomimodul \> Periodiske oppgaver \> Utligninger**. Feltet **Automatisk regel** på siden **Utligninger** viser navnet på den planlagte automatiserte utligningsoppgaven som ble brukt til å utligne transaksjonen. Mislykkede utligningsforsøk vil ikke oppdatere verdien **Automatisk regel**. Hvis du tilbakefører en transaksjon som tidligere ble utlignet av den automatiske prosessen, fjernes verdien **Automatisk regel**.

Feltet **Dato for utligning** for postene med samsvar viser datoen da den automatiske prosessen ble utført.

## <a name="editing-a-ledger-settlement-automation"></a>Redigere en utligningsautomatiseringen

Ved hjelp av rammeverket for prosessautomatisering kan du redigere serien og forekomstene som er opprettet for utligningen. Serien kan redigeres enten fra siden for **Prosessautomatisering** eller den ukentlige visningen for prosessautomatisering. Hvis administratoren for eksempel bestemmer seg for å utføre utligninger på onsdag i stedet for mandag, kan vedkommende finne en forekomst i den ukentlige visningen, og velge  **Vis/Rediger – Serier**.

Hvis du redigerer en serie, blir du bedt om å angi om endringen skal gjøres i alle eksisterende forekomster, eller bare i nye forekomster. Historiske forekomster som allerede har statusen **Fullført**, eller som ble avsluttet i en **Feil** -status, endres ikke.

Du kan også legge til en ny forekomst eller endre en eksisterende forekomst. Eksempel: Den neste utligningsforekomsten er planlagt for kjøring onsdag 1. januar, men denne datoen er en rød dag. Du kan endre forekomsten enten fra ukesvisningen for **Prosessautomatisering**  eller fra ukevisning for prosessautomatisering. En side åpnes som viser plandetaljene og kriteriene for samsvar. Her kan du redigere planlagt klokkeslett og dato. Du kan også redigere kriteriene for samsvar hvis det kreves endringer. 

Du kan også deaktivere en forekomst eller en serie. Hvis du vil deaktivere en forekomst og utsette behandlingen av den, velger du den i ukesvisningen for prosessautomatisering og velger deretter **Deaktiver**. Du kan deaktivere en serie på **Prosessautomatisering** -siden.

## <a name="security-for-ledger-settlement-automation"></a>Sikkerhet for utligningsautomatisering

Plikten **Vedlikehold innstillinger for utligningsautomatiseringsserie** er lagt til i rollene Regnskapssjef og Regnskapsleder, og plikten **Vis innstillinger for utligningsautomatiseringsserie** er lagt til i Regnskapsfører-, Regnskapssjef- og Regnskapsansvarlig-rollene for automatisk utligning. Disse pliktene er standard sikkerhetsinnstillinger, men de kan endres basert på organisasjonens behov.

## <a name="general-ledger-parameters-for-ledger-settlement-automation"></a>Økonomimodulparametere for utligningsautomatisering

Feltet **Typisk saldo for utligning** angir ordren som den automatiske finansutligingen blir behandlet i. Hvis du vil definere eller vise verdien **Typisk saldo for utligning**, går du til **Økonomimodul \> Oppsett \> Parametere for økonomimodul** og velger kategorien **Utligninger**.

Hvis **Debet** er valgt, starter den automatiserte utligningsprosessen på debetsiden og søker etter tilsvarende krediteringer. Hvis **Kredit** er valgt, starter den automatiserte utligningsprosessen på kreditsiden og søker etter tilsvarende debiteringer. Dette alternativet bør gjenspeile hovedkontoens vanlige saldo.

## <a name="processing-a-ledger-settlement-automation"></a>Behandle en utligningsautomatisering

Når automatiseringen kjøres, velger systemet finanstransaksjonene for hovedkontoene som er definert for prosessautomasjonsserien. Den bestiller transaksjonene etter dato, ved hjelp av et datoområde fra begynnelsen av regnskapsåret til datoen når prosessautomatiseringen kjøres. Samsvarer basert på de angitte samsvarskriteriene. De absolutte verdiene til regnskapsvalutabeløpene for debet og kredit må samsvare for å være utlignet.

Mens en hovedkonto behandles av en forekomst av utligningsautomatiseringen, kan du ikke vise den på siden for **Utligninger**. Du må vente til automatisk behandling er fullført. Vi anbefaler at du planlegger at prosessen automatisk kjører utenom arbeidstiden, for å forhindre konflikter.

Automatiseringsprosessen inkluderer alle transaksjoner som oppfyller kriteriene, bortsett fra transaksjoner som er manuelt merket for utligning på siden **Utligninger**.

## <a name="reversal-of-transactions-that-are-settled-by-the-automation-process"></a>Tilbakeføring av transaksjoner som er utlignet av automatiseringsprosessen

Du kan tilbakeføre en utligning som ble gjort av den automatiserte utligningsprosessen. Når en transaksjon som tidligere ble utlignet av den automatiske prosessen reverseres, fjernes verdien **Automatisk regel**.
