--- 
title: "Konfigurere detaljhandelsparametere som påvirker detaljhandelsutdrag"
description: "Denne prosedyren beskriver konfigurasjoner for detaljhandelsparametere som påvirker hvordan detaljhandelsutdrag opprettes og posteres."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: ff12587d8332801131d5b0cac84e0db38f8f6142
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---
# <a name="configure-retail-parameters-that-affect-retail-statements"></a>Konfigurere detaljhandelsparametere som påvirker detaljhandelsutdrag

[!include [task guide banner](../includes/task-guide-banner.md)]

Denne prosedyren beskriver konfigurasjoner for detaljhandelsparametere som påvirker hvordan detaljhandelsutdrag opprettes og posteres. Denne prosedyren bruker demonstrasjonsfirmaet USRT.

1. Gå til Detaljhandel og handel > Hovedkvarteroppsett > Parametere > Detaljhandelsparametere.
2. Klikk kategorien Postering.
    * Velg Ja hvis du vil postere de tidsbestemte rabattbeløpene spesielt.  
    * Velg Standard for å bruke standardkontoer, eller velg Tidsbestemt hvis du vil definere hvilken konto som skal brukes for hver tidsbestemt rabatt.  
    * Velg Sammendrag hvis lagerlinjer skal aggregeres når det er mulig.  
    * Velg Ja hvis fakturaer og betalinger skal utlignes automatisk som en del av utdragsposteringsprosessen.  
    * Velg Ja hvis transaksjoner for safedeponering skal aggregeres.  
    * Velg Ja hvis transaksjoner for bankdeponering skal aggregeres.  
    * Velg Ja hvis du vil aktivere aggregering for utdragspostering.  
    * Velg Ja for å opprette og behandle order parallelt når utdrag posteres.  
    * Angi maksimalt antall order som skal behandles i hver satsvis jobboppgave.  
3. Klikk Lagre.


