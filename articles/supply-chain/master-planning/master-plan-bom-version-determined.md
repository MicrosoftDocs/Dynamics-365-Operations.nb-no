---
title: Fastslå stykklisteversjon
description: Hvis en vare har produksjon som type standard bestilling, finner planleggingsmotoren en gyldig stykklisteversjon basert på området når behov brytes ned.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf125e2b75c4dfa406f4f05b249e6fdb49c84b7d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "325095"
---
# <a name="determine-the-bom-version"></a><span data-ttu-id="60727-103">Fastslå stykklisteversjon</span><span class="sxs-lookup"><span data-stu-id="60727-103">Determine the BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60727-104">Hvis en vare har produksjon som type standard bestilling, finner planleggingsmotoren en gyldig stykklisteversjon basert på området når behov brytes ned.</span><span class="sxs-lookup"><span data-stu-id="60727-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="60727-105">Områdedimensjonen er alltid kjent og angis i behovstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="60727-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="60727-106">Følgende prosess brukes til å fastsette hvilken stykklisteversjon som skal brukes:</span><span class="sxs-lookup"><span data-stu-id="60727-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="60727-107">Hvis en stykklisteversjon er definert for varen i området med behov, brukes den områdespesifikke stykklisten.</span><span class="sxs-lookup"><span data-stu-id="60727-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="60727-108">Hvis ingen områdespesifikk stykklisteversjon er definert for en vare i området med behov, brukes en generell stykkliste.</span><span class="sxs-lookup"><span data-stu-id="60727-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="60727-109">En generell stykkliste viser ikke til noe område, og er gyldig for flere områder.</span><span class="sxs-lookup"><span data-stu-id="60727-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="60727-110">Hvis en generell stykkliste finnes, brukes den.</span><span class="sxs-lookup"><span data-stu-id="60727-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="60727-111">Hvis det ikke finnes noen generell stykklisteversjon som kan brukes, vil nedbrytingen av behov stoppe her.</span><span class="sxs-lookup"><span data-stu-id="60727-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="60727-112">En gyldig stykklisteversjon må oppfylle de obligatoriske kriteriene for dato og antall, uansett om den er områdespesifikk eller generell.</span><span class="sxs-lookup"><span data-stu-id="60727-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>





