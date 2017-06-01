---
title: Importere historiske data for behovsprognoser
description: "For å få nøyaktige behovsprognoser, trenger du historiske behovsdata per vare eller varetildelingsnøkkel. Dette emnet forklarer hvordan du bruker dataenheter til å importere historiske behovsdata fra alle systemer, slik at du har en lengre logg over behovsprognosedata."
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0d1e2b9a51c2d7a7c30c2458b7babf8ac5c08118
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="import-historical-data-for-demand-forecasts"></a>Importere historiske data for behovsprognoser

[!include[banner](../includes/banner.md)]

For å garantere nøyaktigheten til behovsprognoser må du ha så mange historiske behovsdata som du kan få per vare eller varetildelingsnøkkel. Hvis de historiske behovsdataene ikke allerede er importert, bruker du dataenheten **Historisk eksternt behov** (ReqDemPlanHistoricalExternalDemandEntity) i Microsoft Dynamics 365 for Operations til å importere de.

I arbeidsområdet **Databehandling** kan du se en oversikt over alle feltene i enheten.

1. Åpne arbeidsområdet **Databehandling**.
2. Klikk flisen **Dataenheter**.
3. Søk i enhetslisten etter **Historisk eksternt behov**.
4. Klikk **Målfelt**. Feltene nedenfor er obligatoriske: område (**DeliveringSiteId**), dato (**DemandDate**), antall (**DemandQuantity**), og enten varenummer (**ItemNumber**) eller varefordelingsnøkkel (**ProductAllocationKeyId**).

Hvis du vil bruke dataenheten, må du ha en Microsoft Excel-fil eller CSV-fil (kommadelte verdier) som inneholder de historiske behovsdataene. Følgende eksempel viser hvordan du importerer data fra en CSV-fil.

## <a name="example"></a>Eksempel

Du kan bruke følgende fil som et eksempel. Last ned [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast). Denne filen inneholder historiske behovsdata for vare D0001. Den inneholder bare følgende obligatoriske felter: område, antall og behovsdatoen.

1. Velg firmaet du vil importere de historiske behovsdataene til.
2. Åpne arbeidsområdet **Databehandling**.
3. Klikk flisen **Importer**.
4. Angi et navn for importprosjektet, for eksempel **Importer historiske behovsdata for vare D0001**.
5. I feltet **Kildedataformat** velger du filformatet for filen du importerer. Hvis du vil importere filen HistoricalDemandData i dette eksemplet, velger du **CSV**.
6. I feltet **Enhetsnavn** velger du **Historisk eksternt behov**.
7. Lagre filen på datamaskinen, og last den deretter opp.
8. Klikk **Importer**.
9. Siden **Utførelsessammendrag** åpnes automatisk. Kontroller de importerte dataene på siden.

Når du har importert de historiske behovsdataene, kan du generere en behovsprognose.

## <a name="see-also"></a>Se også

[Generere en statistisk basislinjeprognose](generate-statistical-baseline-forecast.md)

