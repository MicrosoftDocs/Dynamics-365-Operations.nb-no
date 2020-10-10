---
title: Commerce-hierarkier
description: Denne artikkelen beskriver hierarkier i Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
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
ms.openlocfilehash: 8f7e4d01970f459f66934fe434ec7307104b39b2
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895287"
---
# <a name="commerce-hierarchies"></a><span data-ttu-id="905ab-103">Commerce-hierarkier</span><span class="sxs-lookup"><span data-stu-id="905ab-103">Commerce hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="905ab-104">Denne artikkelen beskriver hierarkier i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="905ab-104">This article describes hierarchies in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="905ab-105">Du kan opprette et kategorihierarki for å organisere produktene du selger gjennom kanalene dine.</span><span class="sxs-lookup"><span data-stu-id="905ab-105">You can create a category hierarchy to organize the products that you sell through your channels.</span></span> <span data-ttu-id="905ab-106">Du kan bruke produkthierarkier til å kategorisere eller gruppere produkter.</span><span class="sxs-lookup"><span data-stu-id="905ab-106">You can use product hierarchies to categorize or group products.</span></span> <span data-ttu-id="905ab-107">Du kan deretter bruke disse produktene til å opprette produktsortimenter og fordelsprogrammer for kunden.</span><span class="sxs-lookup"><span data-stu-id="905ab-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="905ab-108">Du kan også tilordne produktattributter og egenskaper, tilordne en prissettingsstruktur, ta med produktene i produktkampanjer og bruke produktene for rapportering.</span><span class="sxs-lookup"><span data-stu-id="905ab-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="905ab-109">Du kan opprette ett kategorihierarki som representerer alle produkter og kategorier i organisasjonen og deretter bruke dette kategorihierarkiet til flere formål.</span><span class="sxs-lookup"><span data-stu-id="905ab-109">You can create one category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="905ab-110">Du kan alternativt opprette flere kategorihierarkier til spesielle formål, for eksempel produktkampanjer.</span><span class="sxs-lookup"><span data-stu-id="905ab-110">Alternatively, you can create multiple category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="905ab-111">Når du oppretter et produkthierarki, må du tilordne en kategorihierarkitype for å identifisere formålet med kategorihierarkiet.</span><span class="sxs-lookup"><span data-stu-id="905ab-111">When you create a product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="905ab-112">Det er for eksempel bare produkthierarkier som er tilordnet typen **Navigasjonshierarki for handel**, som refereres når du blar gjennom produkter etter kategori elektronisk eller på et salgssted.</span><span class="sxs-lookup"><span data-stu-id="905ab-112">For example, only product hierarchies that are assigned the **Commerce navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="hierarchy-types"></a><span data-ttu-id="905ab-113">Hierarkityper</span><span class="sxs-lookup"><span data-stu-id="905ab-113">Hierarchy types</span></span>

<span data-ttu-id="905ab-114">Tabellen nedenfor viser de tilgjengelige typene kategorihierarkier og det generelle formålet med hver type.</span><span class="sxs-lookup"><span data-stu-id="905ab-114">The following table lists the types of category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="905ab-115">Kategorihierarkitype</span><span class="sxs-lookup"><span data-stu-id="905ab-115">Category hierarchy type</span></span>       | <span data-ttu-id="905ab-116">Formål</span><span class="sxs-lookup"><span data-stu-id="905ab-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="905ab-117">Produkthierarki</span><span class="sxs-lookup"><span data-stu-id="905ab-117">Product hierarchy</span></span>      | <span data-ttu-id="905ab-118">Bruk denne hierarkitypen til å definere det overordnede hovedprodukthierarkiet for organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="905ab-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="905ab-119">Du kan bruke denne hierarkitypen for varehandel, prissetting og kampanjer, rapportering og planlegging av sortimentet.</span><span class="sxs-lookup"><span data-stu-id="905ab-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="905ab-120">Bare ett produkthierarki kan tilordnes denne hierarkitypen.</span><span class="sxs-lookup"><span data-stu-id="905ab-120">Only one product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="905ab-121">Spesialhierarki</span><span class="sxs-lookup"><span data-stu-id="905ab-121">Supplemental hierarchy</span></span> | <span data-ttu-id="905ab-122">Bruk denne hierarkitypen hvis du vil opprette flere kategorihierarkier.</span><span class="sxs-lookup"><span data-stu-id="905ab-122">Use this hierarchy type for any additional category hierarchies that you want to create.</span></span> <span data-ttu-id="905ab-123">Om våren har du for eksempel en kampanje for badetøy.</span><span class="sxs-lookup"><span data-stu-id="905ab-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="905ab-124">Du inkluderer derfor badetøyproduktene i et eget kategorihierarki og bruker kampanjeprisen på de ulike produktkategoriene.</span><span class="sxs-lookup"><span data-stu-id="905ab-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="905ab-125">Navigeringshierarki</span><span class="sxs-lookup"><span data-stu-id="905ab-125">Navigation hierarchy</span></span>   | <span data-ttu-id="905ab-126">Bruk denne hierarkitypen til å gruppere og ordne produkter i kategorier slik at produktene kan blas gjennom på Internett eller på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="905ab-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="905ab-127">Ved å bruke et kategorihierarki til å strukturere produktene kan du definere og vedlikeholde produktattributter og egenskaper på kategorinivå.</span><span class="sxs-lookup"><span data-stu-id="905ab-127">By using a category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="905ab-128">Disse attributtene og egenskapene omfatter innstillinger for produktdimensjoner og POS-innstillinger.</span><span class="sxs-lookup"><span data-stu-id="905ab-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="905ab-129">Alle produkter som du tilordner til kategoriene automatisk, arver attributtene og egenskapene som du definerer.</span><span class="sxs-lookup"><span data-stu-id="905ab-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="905ab-130">Du kan også kopiere egenskapsinnstillingene for et produkt til flere produkter i en valgt kategori samtidig.</span><span class="sxs-lookup"><span data-stu-id="905ab-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>
