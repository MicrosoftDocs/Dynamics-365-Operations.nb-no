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
translationtype: Human Translation
ms.sourcegitcommit: 00f022da597b1de2454e93123de31731c6a65962
ms.openlocfilehash: 20363ef1917f7d0796cb0d5cd8e623c598b5ee01
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Oversikt over avansert bankavstemming

Denne artikkelen beskriver flyten for den avanserte bankavstemmingsprosessen. Funksjonen for den avanserte bankavstemmingen lar deg importere bankkontoutdrag som kan avstemmes automatisk fra banktransaksjoner.

Funksjonen for avanserte bankavstemming lar deg importere bankkontoutdrag. Det importerte bankkontoutdraget kan deretter avstemmes automatisk fra banktransaksjoner. Her er noen av trinnene i flyten for den avanserte bankavstemmingen.

1.  Definer import for bankkontoutdrag.
    -   Importer bankkontoutdrag gjennom rammeverket for dataenhet.
    -   Tre vanlige bankkontoutdragsformater er innebygd: ISO20022, BAI2 og MT940.
    -   Funksjonen kan utvides til et hvilken som helst format.

2.  Definer en nummerserie som skal brukes for avansert bankavstemming, og definer samsvarsregler for bankavstemmingen.
    -   En søkeregel for avstemming er et sett med kriterier som brukes til å filtrere bankkontoutdragslinjer og Microsoft Dynamics 365 for operasjoner bank transaksjonslinjer i løpet av avstemmingsprosessen. Avhengig av firmaets praksis, kan du sette opp mer enn én samsvarende regelen til å automatisere og optimalisere avstemmingsprosessen.

3.  Avstemme bankkontoutdrag med Dynamics 365 for operasjoner banktransaksjoner.
    -   Utfør automatiske samsvaring og oppretting av avstemmingsjournaler.
    -   Ser du bankkontoutdrag og Dynamics 365 for operasjoner banktransaksjoner side ved side.
    -   Postere automatisk Dynamics 365 for operasjoner banktransaksjoner hvis de vises på et bankkontoutdrag, men vises ikke i Dynamics 365 for operasjoner.
    -   Generer et avstemmingsutdrag.




