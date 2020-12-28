---
title: Opprette et nytt produkthierarki
description: Dette emnet beskriver hvordan du oppretter et nytt produkthierarki i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 724ec2e5af7837d574298d662911cd9c6ee9e9f2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414569"
---
# <a name="create-a-new-product-hierarchy"></a><span data-ttu-id="0936f-103">Opprette et nytt produkthierarki</span><span class="sxs-lookup"><span data-stu-id="0936f-103">Create a new product hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0936f-104">Dette emnet beskriver hvordan du oppretter et nytt produkthierarki i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0936f-104">This topic describes how to create a new product hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0936f-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="0936f-105">Overview</span></span>

<span data-ttu-id="0936f-106">Dynamics 365 Commerce støtter flere kanaler for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="0936f-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="0936f-107">Disse detaljhandelskanalene omfatter nettbutikker, telefonsentre og detaljhandelsbutikker (også kalt fysiske butikker).</span><span class="sxs-lookup"><span data-stu-id="0936f-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="0936f-108">Hver detaljhandelsbutikkanal kan ha sine egne betalingsmåter, prisgrupper, salgsstedskasser, inntekts- og utgiftskontoer og ansatte.</span><span class="sxs-lookup"><span data-stu-id="0936f-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="0936f-109">Du må sette opp alle disse elementene før du kan opprette en detaljhandelsbutikkanal.</span><span class="sxs-lookup"><span data-stu-id="0936f-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="0936f-110">Et handelsprodukthierarki brukes til å definere det overordnede hovedprodukthierarkiet for organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="0936f-110">A Commerce product hierarchy is used to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="0936f-111">Du kan bruke et handelsprodukthierarki for varehandel, prissetting og kampanjer, rapportering og planlegging av sortimentet.</span><span class="sxs-lookup"><span data-stu-id="0936f-111">You can use a Commerce product hierarchy for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="0936f-112">Bare ett handelsprodukthierarki kan tilordnes per organisasjon.</span><span class="sxs-lookup"><span data-stu-id="0936f-112">Only one Commerce product hierarchy can be assigned per organization.</span></span>

## <a name="create-and-configure-a-product-hierarchy"></a><span data-ttu-id="0936f-113">Opprette og konfigurere et produkthierarki</span><span class="sxs-lookup"><span data-stu-id="0936f-113">Create and configure a product hierarchy</span></span>

<span data-ttu-id="0936f-114">Hvis du vil opprette og konfigurere et handelsprodukthierarki, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="0936f-114">To create and configure a Commerce product hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="0936f-115">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Produkter og kategorier \> Handelsprodukthierarki**.</span><span class="sxs-lookup"><span data-stu-id="0936f-115">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="0936f-116">Hvis det ikke finnes noe hierarki enda, går du til **Handlingsrute** og velger **Nytt** for å opprette roten til hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="0936f-116">If no hierachy exists yet, on the **Action pane**, select **New** to create the root of the hierarchy.</span></span>
1. <span data-ttu-id="0936f-117">Under **Generelt**:</span><span class="sxs-lookup"><span data-stu-id="0936f-117">Under **General**:</span></span>
    1. <span data-ttu-id="0936f-118">I **Navn**-boksen angir du et navn.</span><span class="sxs-lookup"><span data-stu-id="0936f-118">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="0936f-119">I **Beskrivelse**-boksen angir du en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="0936f-119">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="0936f-120">I **Brukervennlig navn**-boksen angir du et brukervennlig navn.</span><span class="sxs-lookup"><span data-stu-id="0936f-120">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="0936f-121">Sett **Aktivt** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0936f-121">Set **Active** to **Yes**.</span></span>

## <a name="add-hierarchy-nodes"></a><span data-ttu-id="0936f-122">Legge til hierarkinoder</span><span class="sxs-lookup"><span data-stu-id="0936f-122">Add hierarchy nodes</span></span>

<span data-ttu-id="0936f-123">Hvis du vil legge til hierarkinoder, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="0936f-123">To add hierarchy nodes, follow these steps.</span></span>

1. <span data-ttu-id="0936f-124">I handlingsruten velger du **Rediger kategorihierarki**.</span><span class="sxs-lookup"><span data-stu-id="0936f-124">On the action pane, select **Edit category hierarchy**.</span></span>
1. <span data-ttu-id="0936f-125">Velg den overordnede noden du vil legge til en ny node for, og velg deretter **Ny kategorinode**.</span><span class="sxs-lookup"><span data-stu-id="0936f-125">Select the parent node you want to add a new node to, and then select **New category node**.</span></span>
1. <span data-ttu-id="0936f-126">I **Generelt**-delen oppgir du **Navn**, **Beskrivelse**, **Brukervennlig navn** og **Nøkkelord**.</span><span class="sxs-lookup"><span data-stu-id="0936f-126">In the **General** section provide a **Name**, **Description**, **Friendly name** and **Keywords**.</span></span>
1. <span data-ttu-id="0936f-127">Under **Generelt**:</span><span class="sxs-lookup"><span data-stu-id="0936f-127">Under **General**:</span></span>
    1. <span data-ttu-id="0936f-128">I **Navn**-boksen angir du et navn.</span><span class="sxs-lookup"><span data-stu-id="0936f-128">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="0936f-129">I **Beskrivelse**-boksen angir du en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="0936f-129">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="0936f-130">I **Brukervennlig navn**-boksen angir du et brukervennlig navn.</span><span class="sxs-lookup"><span data-stu-id="0936f-130">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="0936f-131">I **Nøkkelord**-boksen angir du relevante nøkkelord.</span><span class="sxs-lookup"><span data-stu-id="0936f-131">In the **Keywords** box, enter relevant keywords.</span></span>
    1. <span data-ttu-id="0936f-132">I **Visningsrekkefølge**-boksen angir du et nummer for visningsrekkefølgen (valgfritt).</span><span class="sxs-lookup"><span data-stu-id="0936f-132">In the **Display order** box, enter a number for the display order (optional).</span></span>
1. <span data-ttu-id="0936f-133">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="0936f-133">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="0936f-134">Gjenta trinnene ovenfor for å legge til flere noder.</span><span class="sxs-lookup"><span data-stu-id="0936f-134">Repeat the steps above to add additional nodes.</span></span>

<span data-ttu-id="0936f-135">Bildet nedenfor viser opprettelsen av en ny produkthierarkinode.</span><span class="sxs-lookup"><span data-stu-id="0936f-135">The following image shows the creation of a new product hierarchy node.</span></span>

![Opprette et produkthierarki](media/create-product-hierarchy.png)

## <a name="other-settings"></a><span data-ttu-id="0936f-137">Andre innstillinger</span><span class="sxs-lookup"><span data-stu-id="0936f-137">Other settings</span></span>

<span data-ttu-id="0936f-138">Kategoriattributtgrupper kan også tilordnes til hver gruppe etter behov.</span><span class="sxs-lookup"><span data-stu-id="0936f-138">Category attribute groups can also be assigned to each group as required.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="0936f-139">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0936f-139">Additional resources</span></span>

[<span data-ttu-id="0936f-140">Commerce-hierarkier</span><span class="sxs-lookup"><span data-stu-id="0936f-140">commerce hierarchies</span></span>](retail-hierarchies.md)

[<span data-ttu-id="0936f-141">Administrere produktkategorier og produkter </span><span class="sxs-lookup"><span data-stu-id="0936f-141">Manage product categories and products </span></span>](category-management-product-creation.md)

[<span data-ttu-id="0936f-142">Endre sorteringsrekkefølgen for varehandelsenheter</span><span class="sxs-lookup"><span data-stu-id="0936f-142">Change the sort order for merchandizing entities</span></span>](custom-order-categories-nav-retail-prod-hierarchy.md)
