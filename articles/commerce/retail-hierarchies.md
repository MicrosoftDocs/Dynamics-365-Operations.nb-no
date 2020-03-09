---
title: Detaljhandelhierarkier
description: Denne artikkelen beskriver detaljhandelshierarkier i Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: cf8db2c828f99dfd4c220966e31894dcd6eda572
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023579"
---
# <a name="retail-hierarchies"></a><span data-ttu-id="94d4d-103">Detaljhandelshierarkier</span><span class="sxs-lookup"><span data-stu-id="94d4d-103">Retail hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="94d4d-104">Denne artikkelen beskriver hierarkier i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="94d4d-104">This article describes hierarchies in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="94d4d-105">Du kan opprette et kategorihierarki for å organisere produktene du selger gjennom kanalene dine.</span><span class="sxs-lookup"><span data-stu-id="94d4d-105">You can create a category hierarchy to organize the products that you sell through your channels.</span></span> <span data-ttu-id="94d4d-106">Du kan bruke produkthierarkier til å kategorisere eller gruppere produkter.</span><span class="sxs-lookup"><span data-stu-id="94d4d-106">You can use product hierarchies to categorize or group products.</span></span> <span data-ttu-id="94d4d-107">Du kan deretter bruke disse produktene til å opprette produktsortimenter og fordelsprogrammer for kunden.</span><span class="sxs-lookup"><span data-stu-id="94d4d-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="94d4d-108">Du kan også tilordne produktattributter og egenskaper, tilordne en prissettingsstruktur, ta med produktene i produktkampanjer og bruke produktene for rapportering.</span><span class="sxs-lookup"><span data-stu-id="94d4d-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="94d4d-109">Du kan opprette ett kategorihierarki som representerer alle produkter og kategorier i organisasjonen og deretter bruke dette kategorihierarkiet til flere formål.</span><span class="sxs-lookup"><span data-stu-id="94d4d-109">You can create one category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="94d4d-110">Du kan alternativt opprette flere kategorihierarkier til spesielle formål, for eksempel produktkampanjer.</span><span class="sxs-lookup"><span data-stu-id="94d4d-110">Alternatively, you can create multiple category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="94d4d-111">Når du oppretter et produkthierarki, må du tilordne en kategorihierarkitype for å identifisere formålet med kategorihierarkiet.</span><span class="sxs-lookup"><span data-stu-id="94d4d-111">When you create a product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="94d4d-112">Det er for eksempel bare produkthierarkier som er tilordnet typen **Navigasjonshierarki for handel**, som refereres når du blar gjennom produkter etter kategori elektronisk eller på et salgssted.</span><span class="sxs-lookup"><span data-stu-id="94d4d-112">For example, only product hierarchies that are assigned the **Commerce navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="hierarchy-types"></a><span data-ttu-id="94d4d-113">Hierarkityper</span><span class="sxs-lookup"><span data-stu-id="94d4d-113">Hierarchy types</span></span>

<span data-ttu-id="94d4d-114">Tabellen nedenfor viser de tilgjengelige typene kategorihierarkier og det generelle formålet med hver type.</span><span class="sxs-lookup"><span data-stu-id="94d4d-114">The following table lists the types of category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="94d4d-115">Kategorihierarkitype</span><span class="sxs-lookup"><span data-stu-id="94d4d-115">Category hierarchy type</span></span>       | <span data-ttu-id="94d4d-116">Formål</span><span class="sxs-lookup"><span data-stu-id="94d4d-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="94d4d-117">Produkthierarki</span><span class="sxs-lookup"><span data-stu-id="94d4d-117">Product hierarchy</span></span>      | <span data-ttu-id="94d4d-118">Bruk denne hierarkitypen til å definere det overordnede hovedprodukthierarkiet for organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="94d4d-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="94d4d-119">Du kan bruke denne hierarkitypen for varehandel, prissetting og kampanjer, rapportering og planlegging av sortimentet.</span><span class="sxs-lookup"><span data-stu-id="94d4d-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="94d4d-120">Bare ett produkthierarki kan tilordnes denne hierarkitypen.</span><span class="sxs-lookup"><span data-stu-id="94d4d-120">Only one product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="94d4d-121">Spesialhierarki</span><span class="sxs-lookup"><span data-stu-id="94d4d-121">Supplemental hierarchy</span></span> | <span data-ttu-id="94d4d-122">Bruk denne hierarkitypen hvis du vil opprette flere kategorihierarkier.</span><span class="sxs-lookup"><span data-stu-id="94d4d-122">Use this hierarchy type for any additional category hierarchies that you want to create.</span></span> <span data-ttu-id="94d4d-123">Om våren har du for eksempel en kampanje for badetøy.</span><span class="sxs-lookup"><span data-stu-id="94d4d-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="94d4d-124">Du inkluderer derfor badetøyproduktene i et eget kategorihierarki og bruker kampanjeprisen på de ulike produktkategoriene.</span><span class="sxs-lookup"><span data-stu-id="94d4d-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="94d4d-125">Navigeringshierarki</span><span class="sxs-lookup"><span data-stu-id="94d4d-125">Navigation hierarchy</span></span>   | <span data-ttu-id="94d4d-126">Bruk denne hierarkitypen til å gruppere og ordne produkter i kategorier slik at produktene kan blas gjennom på Internett eller på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="94d4d-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="94d4d-127">Ved å bruke et kategorihierarki til å strukturere produktene kan du definere og vedlikeholde produktattributter og egenskaper på kategorinivå.</span><span class="sxs-lookup"><span data-stu-id="94d4d-127">By using a category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="94d4d-128">Disse attributtene og egenskapene omfatter innstillinger for produktdimensjoner og POS-innstillinger.</span><span class="sxs-lookup"><span data-stu-id="94d4d-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="94d4d-129">Alle produkter som du tilordner til kategoriene automatisk, arver attributtene og egenskapene som du definerer.</span><span class="sxs-lookup"><span data-stu-id="94d4d-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="94d4d-130">Du kan også kopiere egenskapsinnstillingene for et produkt til flere produkter i en valgt kategori samtidig.</span><span class="sxs-lookup"><span data-stu-id="94d4d-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>