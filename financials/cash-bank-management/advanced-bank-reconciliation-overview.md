---
title: Oversikt over avansert bankavstemming
description: Denne artikkelen beskriver flyten for den avanserte bankavstemmingsprosessen. Funksjonen for den avanserte bankavstemmingen lar deg importere bankkontoutdrag som kan avstemmes automatisk fra banktransaksjoner.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 6977cb3b315a90b504fc6748d2a4d02854a9d5ef
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Oversikt over avansert bankavstemming

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver flyten for den avanserte bankavstemmingsprosessen. Funksjonen for den avanserte bankavstemmingen lar deg importere bankkontoutdrag som kan avstemmes automatisk fra banktransaksjoner.

Funksjonen for avanserte bankavstemming lar deg importere bankkontoutdrag. Det importerte bankkontoutdraget kan deretter avstemmes automatisk fra banktransaksjoner. Her er noen av trinnene i flyten for den avanserte bankavstemmingen.

1.  Definer import for bankkontoutdrag.
    -   Importer bankkontoutdrag gjennom rammeverket for dataenhet.
    -   Tre vanlige bankkontoutdragsformater er innebygd: ISO20022, BAI2 og MT940.
    -   Funksjonen kan utvides til et hvilken som helst format.

2.  Definer en nummerserie som skal brukes for avansert bankavstemming, og definer samsvarsregler for bankavstemmingen.
    -   En samsvarsregel for avstemming er et sett kriterier som brukes for å filtrere bankkontoutdragslinjer og Microsoft Dynamics 365 for Operations-banktransaksjonslinjer under avstemmingsprosessen. Avhengig av firmaets praksis, kan du definere én eller flere samsvarsregler for å automatisere og optimalisere avstemmingsprosessen.

3.  Avstem bankkontoutdrag med banktransaksjoner i Dynamics 365 for Operations.
    -   Utfør automatiske samsvaring og oppretting av avstemmingsjournaler.
    -   Vis bankkontoutdrag og banktransaksjoner i Dynamics 365 for Operations ved siden av hverandre.
    -   Bokfør banktransaksjoner i Dynamics 365 for Operations automatisk hvis de vises i et bankkontoutdrag, men ikke vises i Dynamics 365 for Operations.
    -   Generer et avstemmingsutdrag.






