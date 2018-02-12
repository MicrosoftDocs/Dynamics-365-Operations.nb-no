--- 
title: " Parameterkonfigurasjoner for detaljhandelsutdrag"
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 731a3ec06efa103ba663df83240c77dfe78bb7cd
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="parameter-configurations-for-retail-statements"></a> Parameterkonfigurasjoner for detaljhandelsutdrag

[!include[task guide banner](../includes/task-guide-banner.md)]

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


