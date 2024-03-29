---
title: Foreta manuelle justeringer i basislinjeprognosen
description: Denne artikkelen forklarer hvordan du gjør manuelle justeringer i en basislinjeprognose og viser detaljer for prognosen.
author: t-benebo
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3b2cc172e551096492f2aebfd8b81eb3f9c471b
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741264"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a>Foreta manuelle justeringer i basislinjeprognosen

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du gjør manuelle justeringer i en basislinjeprognose og viser detaljer for prognosen. 

Før du gjør manuelle justeringer, er det viktig at du forstår noen nøkkelbegreper om forskjellige sider.

## <a name="grid-on-the-adjusted-demand-forecast-page"></a>Rutenett på siden Justert behovsprognose
Siden **Justert behovsprognose** inneholder et rutenett med følgende struktur:

-   Den første kolonnen viser varene, varefordelingsnøkler, firmaer, og så videre som prognosen er generert for. Undertittelen på siden gir en beskrivelse av gjeldende prognosedimensjoner som vises i rutenettet. Hvis undertittelen på siden for eksempel er **firma / område / varefordelingsnøkkel**, og en av radoverskriftene i rutenettet er **USMF / 1 / D\_Alloc**, viser denne raden prognosen for firmaet USMF, område 1, og varefordelingsnøkkel **D\_Alloc**.
-   Etterfølgende kolonner representerer prognoseperioder som prognosen er generert for. Hver kolonneoverskrift er den første datoen i prognoseperioden som kolonnen viser.
-   Verdiene i cellene representerer prognosen for én vare, varefordelingsnøkkel og så videre, for den bestemte prognoseperioden.

## <a name="forecast-aggregation-and-de-aggregation"></a>Prognoseaggregering og -deaggregering
Undertittelen på siden viser nivået på prognoseaggregering. 

Hvis undertittelen på siden for eksempel er **firma / område / tilordningsnøkkel / varenummer / farge / størrelse / konfigurasjon / stil**, er det ingen prognoseaggregering, og prognosen vises på nivået for varen og dens dimensjoner. For å endre aggregering bruk siden **Endre prognosedimensjoner** som du kan åpne fra programmenyen. 

Hvis du vil endre prognosen, klikker du i noen av cellene som er tilgjengelige, og Skriv inn den justerte prognoseverdi. Den redigerte cellen blir umiddelbart fet for å angi at prognosen som den viser, ikke er prognosen som behovsprognosetjenesten opprettet, men er justert manuelt. 

Hvis du endrer aggregering for å la siden vise mer aggregerte data, kan du bruke siden **Behovsprognoselinjer** for å vise individuelle prognoselinjer som utgjør den aggregerte prognosen. 

Du har for eksempel generert prognosen på varenivå, men du vet at behovet for denne varen vil øke på tvers av alle områder på grunn av en kampanje eller en annen lignende hendelse. I så fall kan du sette aggregeringen til **firma / varefordelingsnøkkel / vare** på siden **Endre prognosedimensjoner**. Du kan justere den globale prognosen for varen på tvers av alle områder i rutenettet **Justert behovsprognose**. Hvis du vil se effekten av endringen på tvers av alle områder, kan du åpne siden **Behovsprognoselinjer**. På denne siden vises én linje for varen for hvert område, det justerte prognoseantallet og det opprinnelige prognoseantallet. 

Når justeringen av det prognoseberegnede antall er utført på et aggregert nivå, bruker systemet avveid tildeling for å distribuere endringen mellom linjene som oppretter aggregeringen. 

Du kan også gjøre manuelle justeringer på siden **Behovsprognoselinjer** ved å endre enten **Totalt antall**-verdien eller **Antall**-cellene i deaggregeringsrutenettet.

## <a name="viewing-details-of-the-forecast"></a>Vise detaljer for prognosen
Du kan åpne siden **Detaljer om behovsprognose** for å vise mer informasjon om prognosen. 

Siden **Detaljer om behovsprognose** viser følgende informasjon i grafisk format og tabellformat:

-   Det historiske behovet som prognoseforutsigelser er basert på.
-   Gjeldende prognose som brukes i hovedplanlegging.
-   De nye behovsprognoseverdiene og beløpene som de er justert manuelt med.
-   Konfidensintervallet for prognoseverdiene.
-   Prognosemodellen som ble brukt til å generere prognosen. Hvis du viser samlede data, vises listen over alle metodene som ble brukt for den aggregerte tidsserien.
-   Intern modellnøyaktighet (MAPE). Hvis du vil ha mer informasjon om prognosenøyaktighet, se [Overvåke prognosenøyaktighet](monitor-forecast-accuracy.md).

**Merknader:**

- Funksjonen *Valg av prognosemodell i Detaljer om behovsprognose* legger til innstillinger på siden **Detaljer om behovsprognose** som lar deg velge prognosemodellene som skal tas med. Per Supply Chain Management versjon 10.0.21 er denne funksjonen aktivert som standard. Denne funksjonen er obligatorisk fra og med Supply Chain Management 10.0.25 og kan ikke deaktiveres. Hvis du kjører en eldre versjon enn 10.0.25, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Valg av prognosemodell i Detaljer om behovsprognose* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Konfidensintervallet som vises i delen **Prognose** på siden, representerer forskjellen mellom den øvre grensen for konfidensintervallet og den nedre grensen for konfidensintervallet. Hvis du vil se verdiene for øvre og nedre grense, holder du musepekeren over diagrammet i delen **Grafisk presentasjon av historisk behov og prognose**.
- Hvis du bruker behovsprognose og Microsoft Azure Machine Learning, kan du angi konfidensnivåprosenten som prognosen som genereres, skal ha. Konfidensintervallet består av et verdiområde som fungerer som gode estimater for behovsprognosen. En konfidensnivåprosent på 95 angir at det er 5 prosent risiko for at behovsprognosen faller utenfor området for konfidensintervallet.

Du kan også gjøre manuelle justeringer i prognosen på siden **Detaljer om behovsprognose** ved å endre verdiene i **Prognose**-raden i delen **Prognose**.

## <a name="additional-resources"></a>Tilleggsressurser

- [Overvåke prognosenøyaktighet](monitor-forecast-accuracy.md)
- [Generere en statistisk basislinjeprognose](generate-statistical-baseline-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]