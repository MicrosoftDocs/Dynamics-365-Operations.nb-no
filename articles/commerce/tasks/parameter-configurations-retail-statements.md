---
title: Konfigurere parametere som påvirker detaljhandelsutdrag
description: Dette emnet beskriver konfigurasjoner for handelsparametere som påvirker hvordan utdrag opprettes og posteres.
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
ms.openlocfilehash: d8cae6d2fa7c469f50fa92141a6cb5a0af1df4b0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023534"
---
# <a name="configure-parameters-that-affect-retail-statements"></a>Konfigurere parametere som påvirker detaljhandelsutdrag

[!include[task guide banner](../includes/task-guide-banner.md)]

Dette emnet beskriver konfigurasjoner for handelsparametere som påvirker hvordan utdrag opprettes og posteres. Denne prosedyren bruker demonstrasjonsfirmaet USRT.

1. I navigasjonsruten går du til **Moduler > Retail og Commerce > Hovedkvarteroppsett > Parametere > Handelsparametere**.
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

