---
title: Fastslå stykklisteversjon
description: Hvis en vare har produksjon som type standard bestilling, finner planleggingsmotoren en gyldig stykklisteversjon basert på området når behov brytes ned.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 766c857cca603f84bb7fcef2c7eea3bc76620c19
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976898"
---
# <a name="determine-the-bom-version"></a><span data-ttu-id="b2029-103">Fastslå stykklisteversjon</span><span class="sxs-lookup"><span data-stu-id="b2029-103">Determine the BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2029-104">Hvis en vare har produksjon som type standard bestilling, finner planleggingsmotoren en gyldig stykklisteversjon basert på området når behov brytes ned.</span><span class="sxs-lookup"><span data-stu-id="b2029-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="b2029-105">Områdedimensjonen er alltid kjent og angis i behovstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="b2029-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="b2029-106">Følgende prosess brukes til å fastsette hvilken stykklisteversjon som skal brukes:</span><span class="sxs-lookup"><span data-stu-id="b2029-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="b2029-107">Hvis en stykklisteversjon er definert for varen i området med behov, brukes den områdespesifikke stykklisten.</span><span class="sxs-lookup"><span data-stu-id="b2029-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="b2029-108">Hvis ingen områdespesifikk stykklisteversjon er definert for en vare i området med behov, brukes en generell stykkliste.</span><span class="sxs-lookup"><span data-stu-id="b2029-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="b2029-109">En generell stykkliste viser ikke til noe område, og er gyldig for flere områder.</span><span class="sxs-lookup"><span data-stu-id="b2029-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="b2029-110">Hvis en generell stykkliste finnes, brukes den.</span><span class="sxs-lookup"><span data-stu-id="b2029-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="b2029-111">Hvis det ikke finnes noen generell stykklisteversjon som kan brukes, vil nedbrytingen av behov stoppe her.</span><span class="sxs-lookup"><span data-stu-id="b2029-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="b2029-112">En gyldig stykklisteversjon må oppfylle de obligatoriske kriteriene for dato og antall, uansett om den er områdespesifikk eller generell.</span><span class="sxs-lookup"><span data-stu-id="b2029-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>





