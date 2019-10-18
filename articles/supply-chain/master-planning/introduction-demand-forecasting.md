---
title: Oversikt over behovsprognose
description: Behovsprognose brukes til å forutse uavhengig behov fra salgsordrer og avhengig behov på et hvilket som helst frakoblingspunkt for kundeordrer. Reglene for utvidet behovsprognosereduksjon er en ideell løsning for massetilpasning.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42631e8a5ac03eda65bf0f6ede03fa40a5ed2c4e
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250766"
---
# <a name="demand-forecasting-overview"></a>Oversikt over behovsprognose

[!include [banner](../includes/banner.md)]

Behovsprognose brukes til å forutse uavhengig behov fra salgsordrer og avhengig behov på et hvilket som helst frakoblingspunkt for kundeordrer. Reglene for utvidet behovsprognosereduksjon er en ideell løsning for massetilpasning.

For å generere basislinjeprognosen sendes et sammendrag av historiske transaksjoner til en Microsoft Azure Machine Learning-tjeneste med Azure som vert. Fordi denne tjenesten ikke er delt mellom brukere kan den lett tilpasses for å dekke bransjespesifikke behov. Du kan bruke Supply Chain Management for å visualisere prognosen, justere prognosen og vise nøkkelytelsesindikatorer (KPI-er) om prognosenøyaktighet.

## <a name="key-features-of-demand-forecasting"></a>Nøkkelfunksjoner for behovsprognose
Her er noen av de viktigste funksjonene i behovsprognose:

-   Generere en statistisk basislinjeprognose som er basert på historiske data.
-   Bruke et dynamisk sett med prognosedimensjoner.
-   Visualisere behovstrender, konfidensintervaller og justeringer av prognosen.
-   Autorisere den justerte prognosen som skal brukes i planleggingsprosesser.
-   Fjerne utestående.
-   Opprette målinger av prognosenøyaktighet.

## <a name="major-themes-in-demand-forecasting"></a>Viktige temaer i behovsprognose
Tre viktige temaer er implementert i behovsprognose:

-   **Modularitet** – behovsprognose er modulær og enkel å konfigurere. Du kan aktivere eller deaktivere funksjonen ved å endre konfigurasjonsnøkkelen på **Handel** &gt; **Lagerprognose** &gt; **Behovsprognose**.
-   **Gjenbruk av Microsoft-stakken** – Microsoft startet Machine Learning-plattformen i februar 2015. Machine Learning, som nå er en del av Microsoft Cortana Analytics Suite, lar deg raskt og enkelt opprette prediksjonsanalyseeksperimenter, for eksempel behovsanslagseksperimenter, ved hjelp av algoritmene R eller Python programmeringsspråk og et enkelt dra-og-slipp-grensesnitt.
    -   Du kan laste ned behovsprognoseeksperimenter, endre dem slik at de overholder dine forretningskrav, publisere dem som en webtjeneste på Azure og bruke dem til å generere behovsprognoser. Eksperimentene er tilgjengelige for nedlasting hvis du har kjøpt et abonnement for Finance and Operations for produksjonsplanlegger som bruker på virksomhetsnivå.
    -   Du kan laste ned de tilgjengelige behovsprediksjonseksperimentene fra [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/). Mens behovsprognoseeksperimenter automatisk er integrert med Finance and Operations, må kunder og partnere håndtere integreringen av eksperimenter de laster ned fra [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/). Derfor er ikke eksperimenter fra [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) like enkle å bruke som behovsprognoseeksperimenter for Finance and Operations. Du må endre koden for eksperimentene slik at de bruker Finance and Operations Application Programming Interface (API).
    -   Du kan opprette dine egne eksperimenter i Microsoft Azure Machine Learning Studio, publisere dem som tjenester på Azure og bruke dem til å generere behovsprognoser.
    -   Hvis du ikke trenger høy ytelse, eller hvis du ikke krever at en stor mengde data skal behandles, kan du bruke gratisnivået for Machine Learning. Vi anbefaler at du alltid starter fra dette nivået, spesielt ved implementerings- og testfaser. Hvis du trenger høyere ytelse og ekstra lagringsplass, kan du bruke standardnivået for Machine Learning. Dette nivået krever et abonnement på Azure og omfatter ekstra kostnader. For opplysninger om priser for Machine Learning kan du se [Machine Learning Studio-priser](https://aka.ms/machine-learning-price-info).
-   **Prognosereduksjon på et hvilket som helst frakoblingspunkt** – Behovsprognose i Finance and Operations bygger på denne funksjonaliteten, som lar deg prognostisere både avhengig og uavhengig behov på et hvilket som helst frakoblingspunkt.

## <a name="basic-flow-in-demand-forecasting"></a>Grunnleggende flyt i behovsprognose
Diagrammet nedenfor viser grunnleggende flyt i behovsprognose. 

[![diagram for innføring i behovsprognose](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Generering av behovsprognose starter i Supply Chain Management. Historiske transaksjonsdata fra Supply Chain Management-transaksjonsdatabasen samles inn og fyller ut en oppsamlingstabell. Denne oppsamlingstabellen mates senere til en Machine Learning-tjeneste. Ved å utføre minimal tilpassing kan du koble ulike datakilder til oppsamlingstabellen. Datakildene kan omfatte Microsoft Excel-filer, kommadelte (CSV)-filer og data fra Microsoft Dynamics AX 2009 og Microsoft Dynamics AX 2012. Derfor kan du generere behovsprognoser som vurderer historiske data som er spredt mellom flere systemer. Hoveddata, for eksempel elementnavn og enheter, må imidlertid være de samme på tvers av ulike datakilder.

Hvis du bruker Machine Learning-eksperimentene behovsprognose, ser de etter en beste tilpasning blant tidsserieprognosemetoder for å beregne en basislinjeprognose. Parameterne for disse prognosemetodene styres i Supply Chain Management. 

Prognosene, historiske data og eventuelle endringer som ble gjort i behovsprognosene i tidligere gjentakelser, er deretter tilgjengelige i Finance and Operations. 

Du kan bruke Supply Chain Management til å visualisere og endre basislinjeprognosene. Manuelle justeringer må være autorisert før prognosene kan brukes til planlegging.

## <a name="limitations"></a>Begrensninger
Behovsprognose er et verktøy som hjelper kunder i fabrikasjonsbransjen med å opprette prognoseprosesser. Det tilbyr kjernefunksjonaliteten for en behovsprognoseløsning og er utformet slik at det kan enkelt utvides. Behovsprognose egner seg kanskje ikke best for kunder i bransjer som detaljhandel, engros, lager, transport eller andre profesjonelle tjenester.

<a name="additional-resources"></a>Tilleggsressurser
--------

[Oppsett av behovsprognose](demand-forecasting-setup.md)

[Generere en statistisk basislinjeprognose](generate-statistical-baseline-forecast.md)

[Gjøre manuelle justeringer i basislinjeprognosen](manual-adjustments-baseline-forecast.md)

[Godkjenne den justerte prognosen](authorize-adjusted-forecast.md)

[Overvåke prognosenøyaktighet](monitor-forecast-accuracy.md)

[Fjerne utestående fra historiske transaksjonsdata ved beregning av en behovsprognose](remove-historical-outliers-calculating-demand-forecast.md)

[Utvide funksjonaliteten for behovsprognose](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)



