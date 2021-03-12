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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 89e24496d35ea0a02bd985f76d7579e1914d9290
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972988"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="f5590-103">Opprette et kanalnavigasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="f5590-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f5590-104">Dette emnet beskriver hvordan du oppretter et kanalnavigeringshierarki i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f5590-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f5590-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="f5590-105">Overview</span></span>

<span data-ttu-id="f5590-106">Et kanalnavigeringshierarki brukes til å gruppere og organisere produkter i kategorier, slik at produktene kan blas gjennom på nettet eller på salgsstedet (POS).</span><span class="sxs-lookup"><span data-stu-id="f5590-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="f5590-107">Opprette et kanalnavigasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="f5590-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="f5590-108">Følg denne fremgangsmåten for å opprette et kanalnavigasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="f5590-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="f5590-109">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Produkter og kategorier \> Kanalnavigasjonskategorier**.</span><span class="sxs-lookup"><span data-stu-id="f5590-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="f5590-110">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f5590-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f5590-111">I **Navn**-boksen angir du et navn.</span><span class="sxs-lookup"><span data-stu-id="f5590-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="f5590-112">I **Beskrivelse**-boksen angir du en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f5590-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="f5590-113">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="f5590-113">Select **Create**.</span></span>
1. <span data-ttu-id="f5590-114">I handlingsruten velger du **Ny kategorinode** for å opprette en rotnode.</span><span class="sxs-lookup"><span data-stu-id="f5590-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="f5590-115">I **Navn**-boksen angir du et navn.</span><span class="sxs-lookup"><span data-stu-id="f5590-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="f5590-116">I **Beskrivelse**-boksen angir du en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f5590-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="f5590-117">I **Brukervennlig navn**-boksen angir du et brukervennlig navn.</span><span class="sxs-lookup"><span data-stu-id="f5590-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="f5590-118">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f5590-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="f5590-119">Bildet nedenfor viser et eksempel på en rotnode.</span><span class="sxs-lookup"><span data-stu-id="f5590-119">The following image shows a example root node.</span></span>

![Eksempel på rotnode](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="f5590-121">Opprette navigasjonskategorinoder</span><span class="sxs-lookup"><span data-stu-id="f5590-121">Create navigation category nodes</span></span>

<span data-ttu-id="f5590-122">Hvis du vil opprette eventuelle ekstra navigasjonskategorinoder for å representere produktkategoriene på kanalen, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="f5590-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="f5590-123">I navigasjonsruten velger du den overordnede noden du vil legge til en kategori i.</span><span class="sxs-lookup"><span data-stu-id="f5590-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="f5590-124">I handlingsruten velger du **Ny kategorinode**.</span><span class="sxs-lookup"><span data-stu-id="f5590-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="f5590-125">I **Navn**-boksen angir du et navn.</span><span class="sxs-lookup"><span data-stu-id="f5590-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="f5590-126">I **Beskrivelse**-boksen angir du en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f5590-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="f5590-127">I **Brukervennlig navn**-boksen angir du et brukervennlig navn.</span><span class="sxs-lookup"><span data-stu-id="f5590-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="f5590-128">I **Visningsrekkefølge**-boksen angir du en visningsrekkefølge (valgfritt).</span><span class="sxs-lookup"><span data-stu-id="f5590-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="f5590-129">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f5590-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="f5590-130">Følgende bilde viser et eksempel på et fullført kanalnavigasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="f5590-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Eksempel på kanalhierarki](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="f5590-132">Legge til produkter i kategorinoder</span><span class="sxs-lookup"><span data-stu-id="f5590-132">Add products to category nodes</span></span>

<span data-ttu-id="f5590-133">Hvis du vil legge til produkter i kategorinoder, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="f5590-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="f5590-134">Velg en kategorinode.</span><span class="sxs-lookup"><span data-stu-id="f5590-134">Select a category node.</span></span>
1. <span data-ttu-id="f5590-135">Under **Produkter** velger du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="f5590-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="f5590-136">Finn det nye produktet / de nye produktene du vil legge til, ved hjelp av produktnummer eller produktnavn, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f5590-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="f5590-137">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f5590-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="f5590-138">Tilføying av produkter i en node i kanalnavigasjonshierarkiet er ikke tilstrekkelig for produktene som vises på en valgt kanal. Produktene må også være sortert til et produkt.</span><span class="sxs-lookup"><span data-stu-id="f5590-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a product.</span></span>

<span data-ttu-id="f5590-139">Det følgende bildet viser en eksempelnode med produkter lagt til.</span><span class="sxs-lookup"><span data-stu-id="f5590-139">The following image shows an example node with products added.</span></span>

![Produkter lagt til i en kategorinode](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="f5590-141">Legge til produktattributtgrupper i kategorinoder</span><span class="sxs-lookup"><span data-stu-id="f5590-141">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="f5590-142">Attributtgrupper må opprettes før du kan legge dem til i en node i kanalnavigasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="f5590-142">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="f5590-143">Hvis du vil legge til en attributtgruppe i en kategorinode, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="f5590-143">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="f5590-144">Velg en kategorinode.</span><span class="sxs-lookup"><span data-stu-id="f5590-144">Select a category node.</span></span>
1. <span data-ttu-id="f5590-145">Under **Produktattributtgruppe** velger du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="f5590-145">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="f5590-146">Finn attributtgruppen(e) du vil legge til, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f5590-146">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="f5590-147">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f5590-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="f5590-148">Det følgende bildet viser en eksempelnode med produktattributtgrupper lagt til.</span><span class="sxs-lookup"><span data-stu-id="f5590-148">The following image shows a sample node with product attribute groups added.</span></span>

![Produktattributtgrupper i en node](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="f5590-150">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f5590-150">Additional resources</span></span>

[<span data-ttu-id="f5590-151">Definere sortimenter</span><span class="sxs-lookup"><span data-stu-id="f5590-151">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="f5590-152">Administrere attributter og attributtgrupper</span><span class="sxs-lookup"><span data-stu-id="f5590-152">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)
