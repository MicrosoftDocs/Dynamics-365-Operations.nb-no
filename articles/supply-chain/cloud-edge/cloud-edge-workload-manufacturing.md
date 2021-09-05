---
title: Sky- og kantskalaenheter for arbeidsbelastninger for produksjonskjøring
description: Dette emnet beskriver hvordan arbeidsbelastninger for produksjonskjøringer fungerer med sky- og kantskalaenheter.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 77e0a0e0eb47c331b2b219dc523ecd2c706a4638
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345305"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a>Skalaenheter for sky og kant for arbeidsbelastninger for produksjonsutførelse

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Arbeidsbelastningen for produksjonsutførelse er tilgjengelig som forhåndsversjon på dette tidspunktet.
> Noen forretningsfunksjoner støttes ikke fullstendig i den offentlige forhåndsversjonen når arbeidsbelastningsskalaenheter brukes.

Ved produksjonsutførelse leverer skalaenheter følgende funksjoner:

- Maskinoperatører og produksjonsledere har tilgang til driftsproduksjonsplanen.
- Maskinoperatører kan holde planen oppdatert ved å kjøre separat og behandle produksjonsjobber.
- Produksjonslederen kan justere driftsplanen.
- Arbeidere kan få tilgang til tid og fremmøte for innstempling og utstempling på kanten for å sikre riktig beregning av arbeiderlønn.

Dette emnet beskriver hvordan arbeidsbelastninger for produksjonskjøringer fungerer med sky- og kantskalaenheter.

## <a name="the-manufacturing-lifecycle"></a>Produksjonslivssyklusen

Som den følgende illustrasjonen viser, er produksjonslivssyklusen delt inn i tre faser: *planlegge*, *kjøre* og *fullføre*.

[![Produksjonskjøringsfaser når ett enkelt miljø brukes](media/mes-phases.png "Produksjonskjøringsfaser når ett enkelt miljø brukes.")](media/mes-phases-large.png)

_Planlegge_-fasen omfatter produktdefinisjon, planlegging, oppretting og planlegging av ordrer og frigivelse. Frigivelsestrinnet viser overgangen fra _Planlegg_-fasen til _Kjøre_-fasen. Når en produksjonsordre frigis, vil produksjonsordrejobbene være synlige på produksjonsgulvet og klare til kjøring.

Når en produksjonsjobb er merket som fullført, flyttes den fra _Kjøre_-fasen til _Fullføre_-fasen. I _Fullføre_-fasen går registreringene fra *Kjøre*-fasen gjennom en godkjenningsarbeidsflyt, der de beregnes, godkjennes og overføres. På dette tidspunktet fullføres produksjonsordren. Derfor genereres grunnlaget for arbeiderens lønn.

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a>Dele Kjøre-fasen i en separat arbeidsbelastning

Som den følgende illustrasjonen viser, blir _Kjøre_-fasen delt som en egen arbeidsbelastning når du bruker skalaenheter.

[![Produksjonskjøringsfaser når skalaenheter brukes](media/mes-phases-workloads.png "Produksjonskjøringsfaser når skalaenheter brukes.")](media/mes-phases-workloads-large.png)

Modellen går nå fra en enkelt forekomstinstallasjon til en modell som er basert på senteret og skalaenhetene. _Planlegge_- og _Fullføre_-fasene kjører som Back-Office-operasjoner på senteret, og arbeidsbelastningen for produksjonskjøring kjører på skalaenhetene. Data overføres asynkront mellom senteret og skalaenhetene.

Når en produksjonsordre frigis på senteret, overføres alle data som kreves for å behandle produksjonsjobber, til skalaenheten. Disse dataene omfatter produksjonsordrer, produksjonsruter, stykklister og produkter. Data som ikke er knyttet til en produksjonsordre (for eksempel indirekte aktiviteter, fraværskoder og produksjonsparametere), overføres også fra senteret til skalaenheten. Som en regel kan data som kommer fra senteret, og som overføres til skalaenheten, bare opprettes eller oppdateres på senteret. En ny fraværskode eller indirekte aktivitet kan for eksempel ikke opprettes på en skalaenhet – de kan bare brukes til registrering. Registreringene som gjøres på skalaenheten under kjøring, blir deretter overført til senteret, der tids- og fremmøtegodkjenning, lager og økonomiske oppdateringer behandles.

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a>Produksjonskjøringsoppgaver som kan kjøres på arbeidsbelastninger

Følgende produksjonskjøringsoppgaver kan for øyeblikket kjøres på arbeidsbelastninger når skalaenheter brukes:

- Innstempling, pålogging, utstempling og fravær
- Start jobb
- Bunt jobber
- Rapportfremdrift
- Rapporter svinn
- Indirekte aktivitet
- Bryt
- Ferdigmeld og plasser (krever at du også kjører arbeidsmengden for lagerkjøring på skalaenheten, se også [Ferdigmeld og plasser på en skalaenhet](#RAF))

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a>Arbeide med arbeidsbelastninger for produksjonskjøring på senteret

Vanligvis kjøres prosessene som kreves for å kjøre arbeidsbelastninger for produksjonskjøring automatisk for å holde senteret og alle skalaenhetene synkronisert, etter behov. Hvis du har problemer, kan du imidlertid manuelt utløse behandlingen av råregistreringer som mottas fra arbeidsbelastninger, eller kontrollere registreringsbehandlingsloggen.

### <a name="manually-process-raw-registrations"></a>Behandle råregistreringer manuelt

En satsvis jobb i Supply Chain Management kjøres automatisk for å behandle alle registreringer som er mottatt fra arbeidsbelastningene. Denne jobben oppretter de nødvendige produksjonsjournalene og loggbokpostene når en registrering behandles for en fullført jobb i arbeidsbelastningen.

Selv om jobben vanligvis kjører automatisk, kan du kjøre den manuelt når som helst ved å logge deg på senteret og gå til **Produksjonskontroll \> Periodiske oppgaver \> Back-office-arbeidsbelastningsbehandling \> Råregistreringer**.

### <a name="check-the-raw-registration-processing-log"></a>Kontroller loggen for råregistreringsbehandling

Hvis du vil se gjennom registreringsbehandlingsloggen, logger du deg på senteret og går til **Produksjonskontroll \> Periodiske oppgaver \> Back-office-arbeidsbelastningsbehandling \> Logg over råregistreringsbehandling**. Siden **Logg for råregistreringsbehandling** viser en liste over behandlede råregistreringer og statusen for hver registrering.

![Siden Logg for råregistreringsbehandling.](media/mes-processing-log.png "Siden Logg for råregistreringsbehandling")

Du kan arbeide med en hvilken som helst registrering i listen ved å velge den og deretter velge en av følgende knapper i handlingsruten:

- **Behandle** – Behandle den valgte registreringen manuelt. Denne handlingen kan være nyttig hvis _Behandle råregistreringer_-jobben ikke er kjørt, eller hvis den mislyktes.
- **Avbryt** – Avbryt den valgte registreringen.

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a>Arbeide med arbeidsbelastninger for produksjonskjøring på en skalaenhet

Vanligvis kjøres prosessene som kreves for å kjøre arbeidsbelastninger for produksjonskjøring automatisk for å holde senteret og alle skalaenhetene synkronisert, etter behov. Hvis du har problemer, kan du imidlertid kontrollere historikken til ordrer som er behandlet på en skalaenhet, eller kjøre jobben _Prosessoren for produksjonssenter til skalaenhetsmelding_.

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a>Vis historikken for produksjonsjobber som er behandlet på en skalaenhet

Hvis du vil se gjennom historikken for produksjonsjobber som er behandlet på en skalaenhet, kan du logge på skalaenhetsmaskinen og gå til **Produksjonskontroll \> Periodiske oppgaver \> Back-office-arbeidsbelasatningsbehandling \> Behandlingslogg over produksjonsjobber**. Siden **Behandlingslogg over produksjonsjobber** viser behandlingsloggen for produksjonsordrene på skalaenheten. Du kan arbeide med en hvilken som helst produksjonsordre i listen ved å velge den og deretter velge en av følgende knapper i handlingsruten:

- **Behandle** – Behandle den valgte produksjonsordren manuelt.
- **Avbryt** – Avbryt den valgte produksjonsordren.

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a>Jobben Behandle produksjonssenter til skalaenhet

Jobben _Behandle produksjonssenter til skalaenhet_ behandler data fra senteret til skalaenheten. Denne jobben startes automatisk når arbeidsbelastningen for produksjonskjøring distribueres. Du kan imidlertid kjøre den manuelt når som helst ved å gå til **Produksjonskontroll \> Periodiske oppgaver \> Back-office-arbeidsbelastningsbehandling \> Behandle produksjonssenter til skalaenhet**.

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a>Ferdigmeld og plasser på en skalaenhet

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

I gjeldende utgivelse støttes operasjoner med ferdigmeld og plasser (for ferdige produkter, koprodukter og biprodukter) av [arbeidsmengden for lagerkjøring](cloud-edge-workload-warehousing.md) (ikke arbeidsmengden for produksjonskjøring). Du må derfor gjøre følgende hvis du vil bruke denne funksjonaliteten når du er koblet til en skalaenhet:

- Installer både arbeidsmengden for lagerkjøring og arbeidsmengden for produksjonskjøring på skalaenheten.
- Bruk mobilappen Warehouse Management til å ferdigmelde og behandle plasseringsarbeidet. Grensesnittet for produksjonsutførelse støtter ikke disse prosessene for øyeblikket.

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
