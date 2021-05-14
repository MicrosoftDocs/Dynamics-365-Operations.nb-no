---
title: Opprette et kanalnavigasjonshierarki
description: Dette emnet beskriver hvordan du oppretter et kanalnavigeringshierarki i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5df46de9dadfa0b7160a9b340ef36fdf963a0ad3
ms.sourcegitcommit: 6c2f5c3b038f696532c335e20b0fbafa155d6858
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951914"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="ecd6c-103">Opprett et hierarki for kanalnavigasjon</span><span class="sxs-lookup"><span data-stu-id="ecd6c-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ecd6c-104">Dette emnet beskriver hvordan du oppretter et kanalnavigeringshierarki i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ecd6c-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="ecd6c-105">Overview</span></span>

<span data-ttu-id="ecd6c-106">Et kanalnavigeringshierarki brukes til å gruppere og organisere produkter i kategorier, slik at produktene kan blas gjennom på nettet eller på salgsstedet (POS).</span><span class="sxs-lookup"><span data-stu-id="ecd6c-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="ecd6c-107">Opprette et kanalnavigasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="ecd6c-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="ecd6c-108">Følg denne fremgangsmåten for å opprette et kanalnavigasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="ecd6c-109">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Produkter og kategorier \> Kanalnavigasjonskategorier**.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="ecd6c-110">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ecd6c-111">I **Navn**-boksen angir du et navn.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="ecd6c-112">I **Beskrivelse**-boksen angir du en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="ecd6c-113">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-113">Select **Create**.</span></span>
1. <span data-ttu-id="ecd6c-114">I handlingsruten velger du **Ny kategorinode** for å opprette en rotnode.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="ecd6c-115">I **Navn**-boksen angir du et navn.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="ecd6c-116">I **Beskrivelse**-boksen angir du en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="ecd6c-117">I **Brukervennlig navn**-boksen angir du et brukervennlig navn.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="ecd6c-118">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ecd6c-119">Bildet nedenfor viser et eksempel på en rotnode.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-119">The following image shows a example root node.</span></span>

![Eksempel på rotnode](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="ecd6c-121">Opprette navigasjonskategorinoder</span><span class="sxs-lookup"><span data-stu-id="ecd6c-121">Create navigation category nodes</span></span>

<span data-ttu-id="ecd6c-122">Hvis du vil opprette eventuelle ekstra navigasjonskategorinoder for å representere produktkategoriene på kanalen, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="ecd6c-123">I navigasjonsruten velger du den overordnede noden du vil legge til en kategori i.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="ecd6c-124">I handlingsruten velger du **Ny kategorinode**.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="ecd6c-125">I **Navn**-boksen angir du et navn.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="ecd6c-126">I **Beskrivelse**-boksen angir du en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="ecd6c-127">I **Brukervennlig navn**-boksen angir du et brukervennlig navn.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="ecd6c-128">I **Visningsrekkefølge**-boksen angir du en visningsrekkefølge (valgfritt).</span><span class="sxs-lookup"><span data-stu-id="ecd6c-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="ecd6c-129">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ecd6c-130">Følgende bilde viser et eksempel på et fullført kanalnavigasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Eksempel på kanalhierarki](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="ecd6c-132">Legge til produkter i kategorinoder</span><span class="sxs-lookup"><span data-stu-id="ecd6c-132">Add products to category nodes</span></span>

<span data-ttu-id="ecd6c-133">Hvis du vil legge til produkter i kategorinoder, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="ecd6c-134">Velg en kategorinode.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-134">Select a category node.</span></span>
1. <span data-ttu-id="ecd6c-135">Under **Produkter** velger du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="ecd6c-136">Finn det nye produktet / de nye produktene du vil legge til, ved hjelp av produktnummer eller produktnavn, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="ecd6c-137">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="ecd6c-138">Tilføying av produkter i en node i kanalnavigasjonshierarkiet er ikke tilstrekkelig for produktene som vises på en valgt kanal. Produktene må også være sortert til en kanal.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a channel.</span></span> <span data-ttu-id="ecd6c-139">Hvis du vil ha mer informasjon om sortimenter, kan du se [Sortimentstyring](assortments.md).</span><span class="sxs-lookup"><span data-stu-id="ecd6c-139">For more information on assortments, see [Assortment management](assortments.md).</span></span>

<span data-ttu-id="ecd6c-140">Det følgende bildet viser en eksempelnode med produkter lagt til.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-140">The following image shows an example node with products added.</span></span>

![Produkter lagt til i en kategorinode](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="ecd6c-142">Legge til produktattributtgrupper i kategorinoder</span><span class="sxs-lookup"><span data-stu-id="ecd6c-142">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="ecd6c-143">Attributtgrupper må opprettes før du kan legge dem til i en node i kanalnavigasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-143">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="ecd6c-144">Hvis du vil legge til en attributtgruppe i en kategorinode, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-144">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="ecd6c-145">Velg en kategorinode.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-145">Select a category node.</span></span>
1. <span data-ttu-id="ecd6c-146">Under **Produktattributtgruppe** velger du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-146">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="ecd6c-147">Finn attributtgruppen(e) du vil legge til, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-147">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="ecd6c-148">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ecd6c-149">Det følgende bildet viser en eksempelnode med produktattributtgrupper lagt til.</span><span class="sxs-lookup"><span data-stu-id="ecd6c-149">The following image shows a sample node with product attribute groups added.</span></span>

![Produktattributtgrupper i en node](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="ecd6c-151">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ecd6c-151">Additional resources</span></span>

[<span data-ttu-id="ecd6c-152">Definere sortimenter</span><span class="sxs-lookup"><span data-stu-id="ecd6c-152">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="ecd6c-153">Administrere attributter og attributtgrupper</span><span class="sxs-lookup"><span data-stu-id="ecd6c-153">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
