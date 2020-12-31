---
title: Faktoravskrivning
description: Denne artikkelen gir en oversikt over faktoravskrivningsmetoden.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5c36441e926cd5a82c802a350adf6b2ed6d6387
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446334"
---
# <a name="factor-depreciation"></a>Faktoravskrivning

[!include [banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over faktoravskrivningsmetoden.

Faktorer er prosentandeler som brukes til å avskrive midler. Når du definerer en avskrivningsprofil for anleggsmidler og velger **Faktor** i **Metode**-feltet på **Avskrivningsprofiler**, kan du definere progressiv, degressiv eller lineær avskrivning:

-   Ved progressiv avskrivning øker avskrivningsbeløpet for hver avskrivningsperiode.
-   Ved degressiv avskrivning reduseres avskrivningsbeløpet over tid.
-   Ved lineær avskrivning er avskrivningen den samme i hver periode.

Reglene og eksemplene nedenfor indikerer hvordan du kan definere faktorer for hver avskrivningstype. 

> [!NOTE] 
> Når du velger **Faktor** i **Metode**-feltet, vises **Faktor**-feltet og **Intervall**-feltet.

## <a name="progressive-depreciation"></a>Progressiv avskrivning
Verdien i **Faktor**-feltet er større enn **50**.

### <a name="example"></a>Eksempel

Anskaffelsesprisen er 100 000, faktoren er 70, levetiden er 10 år og avskrivningen starter 1. januar. Avskrivningsbeløpet og beløpet for netto bokført verdi vises kun i de første seks årene av levetiden.

| År | Periode      | Avskrivningsbeløp | Netto bokført verdibeløp |
|------|-------------|---------------------|-----------------------|
| 1    | 31. desember | 307,69              | 99 692,31             |
| 2    | 31. desember | 1 447,21            | 98,245.10             |
| 3    | 31. desember | 3 104,50            | 95,140.60             |
| 4    | 31. desember | 5 150,21            | 89,990.39             |
| 5    | 31. desember | 7 522,95            | 82,467.44             |
| 6    | 31. desember | 10 184,06           | 72,283.38             |

## <a name="digressive-depreciation"></a>Degressiv avskrivning
Verdien i **Faktor**-feltet er mindre enn **50**.

### <a name="example"></a>Eksempel

Anskaffelsesprisen er 100 000, faktoren er 20, levetiden er 10 år og avskrivningen starter 1. januar. Avskrivningsbeløpet og beløpet for netto bokført verdi vises kun i de første seks årene av levetiden.

| År | Periode      | Avskrivningsbeløp | Netto bokført verdibeløp |
|------|-------------|---------------------|-----------------------|
| 1    | 31. desember | 56 080,43           | 43,919.57             |
| 2    | 31. desember | 10 665,70           | 33,253.87             |
| 3    | 31. desember | 7 156,22            | 26,097.65             |
| 4    | 31. desember | 5 538,06            | 20,559.59             |
| 5    | 31. desember | 4 579,89            | 15,979.70             |
| 6    | 31. desember | 3 937,36            | 12,042.34             |

## <a name="straight-line-depreciation"></a>Lineær avskrivning
Verdien i **Faktor**-feltet er lik **50**. I dette tilfellet er avskrivningen den samme i hver periode, og du bør vurdere hvilke implikasjoner dette valget kan ha for andre felt. Les mer i [Lineær levetidsavskrivning](straight-line-service-life-depreciation.md).



