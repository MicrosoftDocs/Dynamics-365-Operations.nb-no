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
ms.openlocfilehash: 7892a216d836ebcc297a5b7eb87bc996dd9b91bf
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140848"
---
# <a name="configure-parameters-that-affect-retail-statements"></a>Konfigurere parametere som påvirker detaljhandelsutdrag

[!include [banner](../includes/banner.md)]

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

