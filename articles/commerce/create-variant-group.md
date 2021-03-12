---
title: Opprette en variantgruppe
description: Dette emnet beskriver hvordan du oppretter en størrelses-, stil- eller fargevariantgruppe for et produkt i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e19d9a2549fa9957126592f3db7e468147997261
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965159"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="4a267-103">Opprette en variantgruppe</span><span class="sxs-lookup"><span data-stu-id="4a267-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4a267-104">Dette emnet beskriver hvordan du oppretter en størrelses-, stil- eller fargevariantgruppe for et produkt i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4a267-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4a267-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="4a267-105">Overview</span></span>

<span data-ttu-id="4a267-106">Dynamics 365 Commerce støtter flere varianter for produkter.</span><span class="sxs-lookup"><span data-stu-id="4a267-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="4a267-107">Det ideelle er å definere variantgrupper for forskjellige produktkategorier.</span><span class="sxs-lookup"><span data-stu-id="4a267-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="4a267-108">En størrelsesgruppe kan for eksempel opprettes for t-skjorter med størrelser ekstra liten, liten, middels, stor og ekstra stor. Alternativt kan det opprettes en fargegruppe som inneholder alle tilgjengelige farger av et produkt.</span><span class="sxs-lookup"><span data-stu-id="4a267-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="4a267-109">Variantgrupper må legges til før produkter legges til.</span><span class="sxs-lookup"><span data-stu-id="4a267-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="4a267-110">I dette emnet skal vi opprette og konfigurere en størrelsesgruppe.</span><span class="sxs-lookup"><span data-stu-id="4a267-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="4a267-111">Lignende prosedyrer kan brukes til å legge til og konfigurere stilgrupper og fargegrupper.</span><span class="sxs-lookup"><span data-stu-id="4a267-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="4a267-112">Opprette en størrelsesgruppe</span><span class="sxs-lookup"><span data-stu-id="4a267-112">Create a size group</span></span>

<span data-ttu-id="4a267-113">Hvis du vil opprette en størrelsesgruppe, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="4a267-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="4a267-114">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Produkter og kategorier \> Variantgrupper \> Størrelsesgrupper**.</span><span class="sxs-lookup"><span data-stu-id="4a267-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="4a267-115">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4a267-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4a267-116">I **Størrelsesgruppe**-boksen angir du et navn for størrelsesgruppen.</span><span class="sxs-lookup"><span data-stu-id="4a267-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="4a267-117">I **Beskrivelse**-boksen angir du en passende beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="4a267-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="4a267-118">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4a267-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="4a267-119">Legge til attributter i størrelsesgruppen</span><span class="sxs-lookup"><span data-stu-id="4a267-119">Add attributes to the size group</span></span>

<span data-ttu-id="4a267-120">Bruk følgende fremgangsmåte for å legge til attributter i en størrelsesgruppe.</span><span class="sxs-lookup"><span data-stu-id="4a267-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="4a267-121">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Produkter og kategorier \> Variantgrupper \> Størrelsesgrupper**</span><span class="sxs-lookup"><span data-stu-id="4a267-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="4a267-122">Velg en størrelsesgruppe i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="4a267-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="4a267-123">Under **Størrelsesgruppelinjer** velger du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="4a267-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="4a267-124">I **Størrelse**-boksen angir du en streng som representerer størrelsen (for eksempel "XL").</span><span class="sxs-lookup"><span data-stu-id="4a267-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="4a267-125">I **Størrelsesnavn**-boksen angir du inn et navn på størrelsen (for eksempel "Ekstra stor").</span><span class="sxs-lookup"><span data-stu-id="4a267-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="4a267-126">I **Etterfyllingsvekt**-boksen angir du et nummer som representerer etterfyllingsvekten.</span><span class="sxs-lookup"><span data-stu-id="4a267-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="4a267-127">I **Nummer i strekkode**-boksen angir du et nummer som representerer strekkoden.</span><span class="sxs-lookup"><span data-stu-id="4a267-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="4a267-128">I **Visningsrekkefølge**-boksen angir du et nummer som representerer visningsrekkefølgen.</span><span class="sxs-lookup"><span data-stu-id="4a267-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="4a267-129">Når du er ferdig med å legge til størrelser, velger du **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4a267-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="4a267-130">Det følgende bildet viser et eksempel på en størrelsesgruppe for "vanlige skjortestørrelser".</span><span class="sxs-lookup"><span data-stu-id="4a267-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![Opprette størrelsesgruppe](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="4a267-132">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4a267-132">Additional resources</span></span>

[<span data-ttu-id="4a267-133">Oversikt over produktinformasjon</span><span class="sxs-lookup"><span data-stu-id="4a267-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="4a267-134">Definere detaljhandelsprodukter</span><span class="sxs-lookup"><span data-stu-id="4a267-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="4a267-135">Produktdimensjoner</span><span class="sxs-lookup"><span data-stu-id="4a267-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)
