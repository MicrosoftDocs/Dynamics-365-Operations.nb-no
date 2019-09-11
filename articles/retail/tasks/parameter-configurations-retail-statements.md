---
title: Konfigurere detaljhandelsparametere som påvirker detaljhandelsutdrag
description: Dette emnet beskriver konfigurasjoner for detaljhandelsparametere som påvirker hvordan detaljhandelsutdrag opprettes og posteres.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b9a0386a4d61395903e82d988244dd131c1febaf
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867277"
---
# <a name="configure-retail-parameters-that-affect-retail-statements"></a>Konfigurere detaljhandelsparametere som påvirker detaljhandelsutdrag

[!include[task guide banner](../includes/task-guide-banner.md)]

Dette emnet beskriver konfigurasjoner for detaljhandelsparametere som påvirker hvordan detaljhandelsutdrag opprettes og posteres. Denne prosedyren bruker demonstrasjonsfirmaet USRT.

1. I navigasjonsruten går du til **Moduler > Detaljhandel og handel > Hovedkvarteroppsett > Parametere > Detaljhandelsparametere**.
2. Velg kategorien **Postering**.
    - Velg **Ja** hvis du vil postere de tidsbestemte rabattbeløpene spesielt.  
    - Velg **Standard** for å bruke standardkontoer, eller velg **Tidsbestemt** hvis du vil definere hvilken konto som skal brukes for hver tidsbestemt rabatt.  
      - Velg **Sammendrag** hvis lagerlinjer skal aggregeres når det er mulig.  
      - Velg **Ja** hvis fakturaer og betalinger skal utlignes automatisk som en del av utdragsposteringsprosessen.  
      - Velg **Ja** hvis transaksjoner for safedeponering skal aggregeres.  
      - Velg **Ja** hvis transaksjoner for bankdeponering skal aggregeres.  
      - Velg **Ja** hvis du vil aktivere aggregering for utdragspostering.  
      - Velg **Ja** for å opprette og behandle order parallelt når utdrag posteres.  
      - Angi maksimalt antall order som skal behandles i hver satsvis jobboppgave.  
3. Velg **Lagre**.

