---
title: Avskrivningsmetoder og -konvensjoner
description: Denne artikkelen gir en oversikt over avskrivningskonvensjoner og avskrivningsmetoder som støttes av Microsoft Dynamics 365 Finance.
author: moaamer
ms.date: 12/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: kfend
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 066e571485602907d167b2ed1f7530b2285a02b6
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714180"
---
# <a name="depreciation-methods-and-conventions"></a>Avskrivningsmetoder og -konvensjoner

[!include [banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over avskrivningskonvensjoner og avskrivningsmetoder som støttes.

Du kan velge forskjellige avskrivningsmetoder og -konvensjoner. Formålet med metodene er å tildele den avskrivbare verdien til anleggsmiddelet i regnskapsperioder. Den avskrivbare verdien til anleggsmiddelet er anskaffelsesprisen minus eventuell svinnverdi. 

Hvis du bruker avskrivningskonvensjoner, og du endrer den siste avskrivningskjøringsdatoen for en vare, noe som hopper over visse avskrivninger, kan avskrivningen for forrige år være større eller mindre enn forventet. Avskrivningen justeres etter hvor mange avskrivningsperioder som påvirkes av endringen i den siste avskrivningskjøringsdatoen.

Hvis du for eksempel bruker konvensjonen med halvårlig avskrivning over tre år, skjer avskrivningen vanligvis over tre og et halv år. Hvis du endrer den siste avskrivningskjøringsdatoen i løpet av de tre og et halvt årene, fjernes de periodene som påvirkes, fra det siste avskrivningsåret. Hvis du flytter datoen med tre måneder, får du ni måneder med avskrivning det siste året i motsetning til de vanlige seks månedene.

Du kan velge mellom følgende avskrivningskonvensjoner.


-   Halvår
-   Hele måneden
-   Midt i kvartal
-   Midt i måneden (1. i måned)
-   Midt i måneden (15. i måned)
-   Halvår (starten på året)
-   Halvår (neste år)

Du kan velge mellom følgende avskrivningsmetoder:
-   Lineær levetid
-   Saldoverdi
-   Manuell
-   Omregningsfaktor
-   Forbruk
-   Lineær levetid som gjenstår
-   200 % saldoverdi
-   175 % saldoverdi
-   150 % saldoverdi
-   125 % saldoverdi





## <a name="additional-resources"></a>Tilleggsressurser

[Avskrivning av anleggsmidler](fixed-asset-depreciation.md)

[Lineær levetidsavskrivning](Straight-line-service-life-depreciation.md)

[Redusere saldoavskrivning](reduce-balance-depreciation.md)

[Manuell avskrivning](manual-depreciation.md)

[Faktoravskrivning](factor-depreciation.md)

[Forbruksavskrivning](consumption-depreciation.md)

[Gjenstående lineær levetidsavskrivning](straight-line-life-remaining-depreciation.md)

[125 % redusert saldoavskrivning](125-percent-reducing-balance-depreciation.md)

[150 prosent redusert saldoavskrivning](150-percent-reducing-balance-depreciation.md)

[175 prosent redusert saldoavskrivning](175-percent-reducing-balance-depreciation.md)

[200 prosent redusert saldoavskrivning](200-percent-reducing-balance-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
