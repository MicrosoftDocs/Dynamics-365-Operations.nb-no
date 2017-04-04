---
title: "Etterspørselen prognoser, oversikt"
description: "Behovsprognose brukes til å forutse uavhengig behov fra salgsordrer og avhengig behov på et hvilket som helst frakoblingspunkt for kundeordrer. Den forbedrede etterspørselen prognose reduksjon regler er en ideell løsning for masse tilpassing."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9152616b81e7873426f296376b5e57c94439379d
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-overview"></a>Etterspørselen prognoser, oversikt

Behovsprognose brukes til å forutse uavhengig behov fra salgsordrer og avhengig behov på et hvilket som helst frakoblingspunkt for kundeordrer. Den forbedrede etterspørselen prognose reduksjon regler er en ideell løsning for masse tilpassing.

For å generere basislinjeprognosen sendes et sammendrag av historiske transaksjoner til en Microsoft Azure Machine Learning-tjeneste med Azure som vert. Fordi denne tjenesten ikke er delt mellom brukere kan den lett tilpasses for å dekke bransjespesifikke behov. Du kan bruke Dynamics 365 for operasjoner å visualisere prognosen, justere prognosen og vise viktige ytelsesindikatorer (KPIer) om prognosen nøyaktighet.

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

-   **Modularitet** – behovsprognose er modulær og enkel å konfigurere. Du kan slå funksjonen av og på ved å endre konfigurasjonsnøkkelen på **Trade**&gt;**Lagerprognose**&gt;**prognoser for behov**.
-   **Gjenbruk av Microsoft-stakk** – Microsoft startet maskinen læring plattformen i februar 2015. Maskin-læring, som nå er en del av Microsoft Cortana Analytics Suite, kan du raskt og enkelt opprette prediksjonsanalyse Eksperimenter, for eksempel behov anslag Eksperimenter ved hjelp av algoritmer R eller Python programmeringsspråk og et enkelt dra-og-slipp-grensesnitt.
    -   Du kan laste ned Dynamics-365 for operasjoner etterspørselen prognoser Eksperimenter, endre dem for å oppfylle dine forretningskrav, publisere dem som en webtjeneste på Azure og bruke dem til å generere behovsprognoser. Eksperimenter er tilgjengelige for nedlasting, hvis du har kjøpt en Dynamics 365 for operasjoner abonnement for en produksjonsplanlegger som enterprise nivå bruker.
    -   Du kan laste ned de tilgjengelige behovsprediksjonseksperimentene fra [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/). Mens Dynamics-365 for operasjoner behov prognostisering Eksperimenter er automatisk integrert med Dynamics 365 for operasjoner, kunder og partnere må håndtere integrering av Eksperimenter som de lastes ned fra den [Cortana Analytics galleri](https://gallery.cortanaanalytics.com/). Derfor Eksperimenter fra den [Cortana Analytics galleri](https://gallery.cortanaanalytics.com/) ikke er like enkelt å bruke som Dynamics-365 for operasjoner etterspørselen prognoser Eksperimenter. Slik at de bruker Dynamics-365 for operasjoner programmeringsgrensesnitt (API), må du endre koden for Eksperimenter.
    -   Du kan opprette dine egne eksperimenter i Microsoft Azure Machine Learning Studio, publisere dem som tjenester på Azure og bruke dem til å generere behovsprognoser.
    -   Hvis du ikke trenger høy ytelse, eller hvis du ikke krever at en stor mengde data skal behandles, kan du bruke gratisnivået for Machine Learning. Vi anbefaler at du alltid starter fra dette nivået, spesielt ved implementerings- og testfaser. Hvis du trenger høyere ytelse og ekstra lagringsplass, kan du bruke standardnivået for Machine Learning. Dette nivået krever et abonnement på Azure og omfatter ekstra kostnader. Hvis du vil ha detaljer om priser for Machine Learning, se <http://aka.ms/machine-learning-price-info>.
-   **Prognosereduksjon når som helst decoupling** – etterspørselen prognoser i Dynamics 365 for versjoner av operasjoner på denne funksjonen, som lar deg beregne både avhengig og uavhengig behov når som helst decoupling.

## <a name="basic-flow-in-demand-forecasting"></a>Grunnleggende flyt i behovsprognose
Diagrammet nedenfor viser grunnleggende flyt i behovsprognose. 

[![etterspørselen prognoser innføring i diagram](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Behov prognose generasjon starter i Dynamics 365 for operasjoner. Historiske transaksjonsdata fra Dynamics-365 for operasjoner overførbar databasen ble samlet inn og fyller ut en oppsamlingstabell. Denne oppsamlingstabell mates senere til en maskin læring-tjeneste. Ved å utføre minimale tilpassing, kan du koble ulike datakilder til sette opp tabell. Datakildene kan inneholde Microsoft Excel-filer, filer med kommaseparerte verdier (CSV), og data fra Microsoft Dynamics AX 2009 og Microsoft Dynamics AX 2012. Derfor kan du generere etterspørselen prognoser som anser historiske data som er spredt mellom flere systemer. Hoveddata, for eksempel elementnavn og enheter, må imidlertid være de samme på tvers av ulike datakilder.

Hvis du bruker Dynamics-365 for operasjoner behov prognostisering maskin læring Eksperimenter, ser de for en beste tilpassing mellom tiden serien prognostisering metoder til å beregne en plan prognose. Parameterne for metodene forecasting administreres i Dynamics 365 for operasjoner. 

Prognosene, historiske data, og endringer som ble gjort i behovsprognoser i forrige gjentakelser er deretter tilgjengelig i Dynamics 365 for operasjoner. 

Du kan bruke Dynamics 365 for operasjoner å visualisere og endre planlagte prognosene. Manuelle justeringer må være autorisert før prognosene kan brukes til planlegging.

## <a name="limitations"></a>Begrensninger
Etterspørselen prognoser, i Dynamics 365 for operasjoner er et verktøy som hjelper kunder i fabrikasjonsbransjen opprette prognoser prosesser. Den gir kjernefunksjonaliteten for et behov prognostisering løsning og er utformet slik at den kan enkelt utvides. Krev prognoser kan ikke være best tilpassing for kunder i bransjer som detaljhandel, engros, lager, transport eller andre profesjonelle tjenester.

<a name="see-also"></a>Se også
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


