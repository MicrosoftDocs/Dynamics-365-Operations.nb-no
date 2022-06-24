---
title: Importere historiske data for behovsprognoser
description: For å få nøyaktige behovsprognoser, trenger du historiske behovsdata per vare eller varetildelingsnøkkel. Denne artikkelen forklarer hvordan du bruker dataenheter til å importere historiske behovsdata fra alle systemer, slik at du har en lengre logg over behovsprognosedata.
author: t-benebo
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
ms.author: benebotg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e36ea72322c31f7e0ea3377b474cd148d78bdd3d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877602"
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

Hvis du vil ha mer informasjon om hvordan du importerer data, inkludert hvordan du rydder opp data etter import, kan du se [Oversikt over dataimport- og -eksportjobber](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) og de beslektede artiklene.

Se også [Generer en statistisk basislinjeprognose](generate-statistical-baseline-forecast.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]