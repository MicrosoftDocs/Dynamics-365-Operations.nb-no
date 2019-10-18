---
title: Oversikt over avansert bankavstemming
description: Denne artikkelen beskriver flyten for den avanserte bankavstemmingsprosessen. Funksjonen for den avanserte bankavstemmingen lar deg importere bankkontoutdrag som kan avstemmes automatisk fra banktransaksjoner.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 39ddfde74aaff8bf5d8f22861b7595be1f9b89a9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179249"
---
# <a name="advanced-bank-reconciliation-overview"></a>Oversikt over avansert bankavstemming

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver flyten for den avanserte bankavstemmingsprosessen. Funksjonen for den avanserte bankavstemmingen lar deg importere bankkontoutdrag som kan avstemmes automatisk fra banktransaksjoner.

Funksjonen for avanserte bankavstemming lar deg importere bankkontoutdrag. Det importerte bankkontoutdraget kan deretter avstemmes automatisk fra banktransaksjoner. Her er noen av trinnene i flyten for den avanserte bankavstemmingen.

1.  Definer import for bankkontoutdrag.
    -   Importer bankkontoutdrag gjennom rammeverket for dataenhet.
    -   Tre vanlige bankkontoutdragsformater er innebygd: ISO20022, BAI2 og MT940.
    -   Funksjonen kan utvides til et hvilken som helst format.

2.  Definer en nummerserie som skal brukes for avansert bankavstemming, og definer samsvarsregler for bankavstemmingen.
    -   En samsvarsregler for avstemming er et sett kriterier som brukes for å filtrere bankkontoutdragslinjer og Microsoft Dynamics 365 Finance-banktransaksjonslinjer under avstemmingsprosessen. Avhengig av firmaets praksis, kan du definere én eller flere samsvarsregler for å automatisere og optimalisere avstemmingsprosessen.

3.  Avstem bankkontoutdrag med banktransaksjoner i Finance.
    -   Utfør automatiske samsvaring og oppretting av avstemmingsjournaler.
    -   Vis bankkontoutdrag og banktransaksjoner i Finance ved siden av hverandre.
    -   Poster banktransaksjoner i Finance automatisk hvis de vises i et bankkontoutdrag, men ikke vises i Finance-appen.
    -   Generer et avstemmingsutdrag.





