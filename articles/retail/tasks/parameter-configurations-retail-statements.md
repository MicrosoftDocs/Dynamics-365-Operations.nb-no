---
title: " Parameterkonfigurasjoner for detaljhandelsutdrag"
description: Denne prosedyren beskriver konfigurasjoner for detaljhandelsparametere som påvirker hvordan detaljhandelsutdrag opprettes og posteres.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 6dacd2b80ca0d51d81d2bdf5bc2636b47da621ee
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564299"
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

