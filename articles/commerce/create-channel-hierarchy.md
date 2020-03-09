---
title: Opprette et kanalnavigasjonshierarki
description: Dette emnet beskriver hvordan du oppretter et kanalnavigeringshierarki i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e83860667f142adcc85cd8542d521e18f16dbc2c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002042"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="93085-103">Opprette et kanalnavigasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="93085-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="93085-104">Dette emnet beskriver hvordan du oppretter et kanalnavigeringshierarki i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="93085-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="93085-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="93085-105">Overview</span></span>

<span data-ttu-id="93085-106">Et kanalnavigeringshierarki brukes til å gruppere og organisere produkter i kategorier, slik at produktene kan blas gjennom på nettet eller på salgsstedet (POS).</span><span class="sxs-lookup"><span data-stu-id="93085-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="93085-107">Opprette et kanalnavigasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="93085-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="93085-108">Følg denne fremgangsmåten for å opprette et kanalnavigasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="93085-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="93085-109">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Produkter og kategorier \> Kanalnavigasjonskategorier**.</span><span class="sxs-lookup"><span data-stu-id="93085-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="93085-110">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="93085-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="93085-111">I **Navn**-boksen angir du et navn.</span><span class="sxs-lookup"><span data-stu-id="93085-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="93085-112">I **Beskrivelse**-boksen angir du en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="93085-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="93085-113">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="93085-113">Select **Create**.</span></span>
1. <span data-ttu-id="93085-114">I handlingsruten velger du **Ny kategorinode** for å opprette en rotnode.</span><span class="sxs-lookup"><span data-stu-id="93085-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="93085-115">I **Navn**-boksen angir du et navn.</span><span class="sxs-lookup"><span data-stu-id="93085-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="93085-116">I **Beskrivelse**-boksen angir du en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="93085-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="93085-117">I **Brukervennlig navn**-boksen angir du et brukervennlig navn.</span><span class="sxs-lookup"><span data-stu-id="93085-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="93085-118">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="93085-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="93085-119">Bildet nedenfor viser et eksempel på en rotnode.</span><span class="sxs-lookup"><span data-stu-id="93085-119">The following image shows a example root node.</span></span>

![Eksempel på rotnode](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="93085-121">Opprette navigasjonskategorinoder</span><span class="sxs-lookup"><span data-stu-id="93085-121">Create navigation category nodes</span></span>

<span data-ttu-id="93085-122">Hvis du vil opprette eventuelle ekstra navigasjonskategorinoder for å representere produktkategoriene på kanalen, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="93085-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="93085-123">I navigasjonsruten velger du den overordnede noden du vil legge til en kategori i.</span><span class="sxs-lookup"><span data-stu-id="93085-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="93085-124">I handlingsruten velger du **Ny kategorinode**.</span><span class="sxs-lookup"><span data-stu-id="93085-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="93085-125">I **Navn**-boksen angir du et navn.</span><span class="sxs-lookup"><span data-stu-id="93085-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="93085-126">I **Beskrivelse**-boksen angir du en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="93085-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="93085-127">I **Brukervennlig navn**-boksen angir du et brukervennlig navn.</span><span class="sxs-lookup"><span data-stu-id="93085-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="93085-128">I **Visningsrekkefølge**-boksen angir du en visningsrekkefølge (valgfritt).</span><span class="sxs-lookup"><span data-stu-id="93085-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="93085-129">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="93085-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="93085-130">Følgende bilde viser et eksempel på et fullført kanalnavigasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="93085-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Eksempel på kanalhierarki](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="93085-132">Legge til produkter i kategorinoder</span><span class="sxs-lookup"><span data-stu-id="93085-132">Add products to category nodes</span></span>

<span data-ttu-id="93085-133">Hvis du vil legge til produkter i kategorinoder, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="93085-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="93085-134">Velg en kategorinode.</span><span class="sxs-lookup"><span data-stu-id="93085-134">Select a category node.</span></span>
1. <span data-ttu-id="93085-135">Under **Produkter** velger du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="93085-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="93085-136">Finn det nye produktet / de nye produktene du vil legge til, ved hjelp av produktnummer eller produktnavn, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="93085-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="93085-137">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="93085-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="93085-138">Tilføying av produkter i en node i kanalnavigasjonshierarkiet er ikke tilstrekkelig for produktene som vises på en valgt kanal. Produktene må også være sortert til et produkt.</span><span class="sxs-lookup"><span data-stu-id="93085-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a product.</span></span>

<span data-ttu-id="93085-139">Det følgende bildet viser en eksempelnode med produkter lagt til.</span><span class="sxs-lookup"><span data-stu-id="93085-139">The following image shows an example node with products added.</span></span>

![Produkter lagt til i en kategorinode](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="93085-141">Legge til produktattributtgrupper i kategorinoder</span><span class="sxs-lookup"><span data-stu-id="93085-141">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="93085-142">Attributtgrupper må opprettes før du kan legge dem til i en node i kanalnavigasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="93085-142">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="93085-143">Hvis du vil legge til en attributtgruppe i en kategorinode, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="93085-143">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="93085-144">Velg en kategorinode.</span><span class="sxs-lookup"><span data-stu-id="93085-144">Select a category node.</span></span>
1. <span data-ttu-id="93085-145">Under **Produktattributtgruppe** velger du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="93085-145">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="93085-146">Finn attributtgruppen(e) du vil legge til, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="93085-146">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="93085-147">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="93085-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="93085-148">Det følgende bildet viser en eksempelnode med produktattributtgrupper lagt til.</span><span class="sxs-lookup"><span data-stu-id="93085-148">The following image shows a sample node with product attribute groups added.</span></span>

![Produktattributtgrupper i en node](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="93085-150">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="93085-150">Additional resources</span></span>

[<span data-ttu-id="93085-151">Definere sortimenter</span><span class="sxs-lookup"><span data-stu-id="93085-151">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="93085-152">Administrere attributter og attributtgrupper</span><span class="sxs-lookup"><span data-stu-id="93085-152">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)