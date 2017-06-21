---
title: Forbruksavskrivning
description: Denne artikkelen gir en oversikt over forbruksmetoden for avskrivning.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a8afea937087ac046f9933eb0ccedf4854515d9f
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="consumption-depreciation"></a>Forbruksavskrivning

[!include[banner](../includes/banner.md)]


Denne artikkelen gir en oversikt over forbruksmetoden for avskrivning.

Hvis du definerer en avskrivingsprofil for anleggsmidler og velger **Forbruk** i feltet **Metode** på siden **Avskrivningsprofiler**, tilordnes anleggsmidler til avskrivningsprofilen basert på bruken. Du trenger ikke definere prosenter og intervaller på siden **Avskrivningsprofiler**. Når du har opprettet en avskrivingsprofil som bruker forbruksmetoden, kan du definere metoden på ulike måter.

## <a name="set-up-and-use-consumption-depreciation"></a>Definere og bruke forbruksavskrivning
1.  På siden **Avskrivningsprofiler** oppretter du avskrivingsprofilen. For forbruksberegninger må avskrivningsprofilen inneholde en ID og et navn, og **Forbruk** må velges i feltet **Metode**.
2.  På siden **Avskrivningsfaktorer** definerer du avskrivningsfaktorer. Hver avskrivningsfaktor må ha en ID og et navn og en avskrivningsfaktor som er angitt som et antall eller en prosent.
3.  På siden **Forbruksenheter** definerer du forbruksenheter. Hver forbruksenhet må ha en ID og et navn. Avskrivningsenheter brukes til å beregne forbruksavskrivning på siden **Forbruksavskrivning**. Eksempler på enheter er kilometer (km), kilogram (kg) og time.
4.  På siden **Anleggsmidler** definerer du enkle anleggsmidler. For hvert anleggsmiddel velger du verdimodeller og avskrivningstablåer som har avskrivningsprofiler. Du må definere verdimodeller eller avskrivningstablåer for forbruksavskrivning hvis noen av anleggsmidlene bruker avskrivningsprofiler som er basert på forbruksmetoden. Dette oppsettet utføres enten i fanen **Avskrivning** på siden **Verdimodeller** eller på hurtigfanen **Generelt** på siden **Avskrivningsprofil**. Du kan bruke den samme verdimodellen for flere anleggsmidler. Avskrivningsprofiler er en del av verdimodellen eller avskrivningstablået du velger for hvert anleggsmiddel. Du kan ikke legge til eller endre avskrivningsprofilene direkte på siden **Anleggsmidler**. Du kan endre avskrivningsprofilene bare på siden **Avskrivningstablåer**.
5.  På siden **Verdimodeller** eller **Avskrivningstablå** i feltgruppen **Forbruksavskrivning** skriver du inn informasjon i følgende felt:
    -   Avskrivningsfaktor
    -   Enhet
    -   Enhetsavskrivning
    -   Estimert forbruk

    I **Postert forbruk**-feltet vises forbruksavskrivningen, i enheter, som allerede er postert enten for kombinasjonen av anleggsmidlet og verdimodellen eller for avskrivningstablået. Du kan ikke oppdatere verdien i dette feltet manuelt.

## <a name="examples"></a>Eksempler
### <a name="example-1"></a>Eksempel 1

Følgende forbruksfaktor er definert for 31. januar:

-   Antallet er 1 000.
-   Enhetsavskrivningsprisen som er angitt for anleggsmidlet, er 1,5.

Avskrivningsforslaget 31. januar er som følger: antall × enhetsavskrivning 1 000 x 1,5 = 1 500 Hvis faktoren som er angitt for anleggsmidlet, er en prosentfaktor, multipliseres antallet som er beregnet i feltet **Estimert forbruk** for verdimodellen for anleggsmidlet, med prosenten som er definert for den valgte sluttdatoen. Det resulterende antallet foreslås deretter som avskrivningsantall for perioden.

### <a name="example-2"></a>Eksempel 2

Følgende faktor for forbruksavskrivning er definert for 31. januar:

-   Prosenten er 10 prosent.
-   Enhetsavskrivningsprisen som er angitt for anleggsmidlet, er 1,5.
-   Estimert antall for et anleggsmiddel er 2 000.

Avskrivningsforslaget den 31. januar er som følger: estimert antall × prosent × enhetsavskrivning 2 000 x 0,10 x 1,5 = 300




