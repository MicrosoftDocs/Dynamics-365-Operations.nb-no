---
title: Importere historiske data for behovsprognoser
description: For å få nøyaktige behovsprognoser, trenger du historiske behovsdata per vare eller varetildelingsnøkkel. Dette emnet forklarer hvordan du bruker dataenheter til å importere historiske behovsdata fra alle systemer, slik at du har en lengre logg over behovsprognosedata.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de380113fe951f75c15f9e5526ad2f1f5cc84334
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908886"
---
# <a name="import-historical-data-for-demand-forecasts"></a>Importere historiske data for behovsprognoser

[!include [banner](../includes/banner.md)]

For å garantere nøyaktigheten til behovsprognoser må du ha så mange historiske behovsdata som du kan få per vare eller varetildelingsnøkkel. Hvis de historiske behovsdataene ikke allerede er importert, bruker du dataenheten **Historisk eksternt behov** (ReqDemPlanHistoricalExternalDemandEntity) i Dynamics 365 Supply Chain Management til å importere de.

I arbeidsområdet **Databehandling** kan du se en oversikt over alle feltene i enheten.

1. Åpne arbeidsområdet **Databehandling**.
2. Velg flisen **Dataenheter**.
3. Søk i enhetslisten etter **Historisk eksternt behov**.
4. Velg **Målfelt**. Feltene nedenfor er obligatoriske: område (**DeliveringSiteId**), dato (**DemandDate**), antall (**DemandQuantity**), og enten varenummer (**ItemNumber**) eller varefordelingsnøkkel (**ProductAllocationKeyId**).

Hvis du vil bruke dataenheten, må du ha en Microsoft Excel-fil eller CSV-fil (kommadelte verdier) som inneholder de historiske behovsdataene. Følgende eksempel viser hvordan du importerer data fra en CSV-fil.

Hvis du vil ha mer informasjon om hvordan du importerer data, inkludert hvordan du rydder opp data etter import, kan du se [Oversikt over dataimport- og -eksportjobber](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) og de beslektede emnene.

## <a name="example"></a>Eksempel

Du kan bruke følgende fil som et eksempel. Last ned [HistoricalDemandData](/dynamics/s-e/). Denne filen inneholder historiske behovsdata for vare D0001. Den inneholder bare følgende obligatoriske felter: område, antall og behovsdatoen.

1. Velg firmaet du vil importere de historiske behovsdataene til.
2. Åpne arbeidsområdet **Databehandling**.
3. Velg **Import**-flisen.
4. Angi et navn for importprosjektet, for eksempel **Importer historiske behovsdata for vare D0001**.
5. I feltet **Kildedataformat** velger du filformatet for filen du importerer. Hvis du vil importere filen HistoricalDemandData i dette eksemplet, velger du **CSV**.
6. I feltet **Enhetsnavn** velger du **Historisk eksternt behov**.
7. Lagre filen på datamaskinen, og last den deretter opp.
8. Velg **Import**.
9. Siden **Utførelsessammendrag** åpnes automatisk. Kontroller de importerte dataene på siden.

Når du har importert de historiske behovsdataene, kan du generere en behovsprognose.

## <a name="additional-resources"></a>Tilleggsressurser

[Generere en statistisk basislinjeprognose](generate-statistical-baseline-forecast.md)  
[Oversikt over dataimport- og -eksportjobber](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]