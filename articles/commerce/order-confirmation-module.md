---
title: Ordredetaljermodulen
description: Dette emnet dekker ordredetaljmoduler og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 06/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5876b953a3b3d960c106acf37731fde13b93f8e7
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661178"
---
# <a name="order-details-module"></a><span data-ttu-id="0eb1b-103">Ordredetaljermodulen</span><span class="sxs-lookup"><span data-stu-id="0eb1b-103">Order details module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0eb1b-104">Dette emnet dekker ordredetaljmoduler og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0eb1b-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="0eb1b-105">Overview</span></span>

<span data-ttu-id="0eb1b-106">Ordredetaljmodulen brukes til å vise ordrebekreftelsesdetaljer etter at en ordre er lagt inn.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="0eb1b-107">Den viser ID-en for ordrebekreftelse, ordrekontaktinformasjon og andre ordredetaljer, for eksempel varene som ble kjøpt, betalingsinformasjon og forsendelsesmetoden.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-details-module-properties"></a><span data-ttu-id="0eb1b-108">Egenskaper for ordredetaljermodul</span><span class="sxs-lookup"><span data-stu-id="0eb1b-108">Order details module properties</span></span>

| <span data-ttu-id="0eb1b-109">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="0eb1b-109">Property name</span></span>  | <span data-ttu-id="0eb1b-110">Verdier</span><span class="sxs-lookup"><span data-stu-id="0eb1b-110">Values</span></span> | <span data-ttu-id="0eb1b-111">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0eb1b-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="0eb1b-112">Overskrift</span><span class="sxs-lookup"><span data-stu-id="0eb1b-112">Heading</span></span>        | <span data-ttu-id="0eb1b-113">Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="0eb1b-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="0eb1b-114">Ordredetaljermodulen kan ha en overskrift.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-114">The order details module can have a heading.</span></span> <span data-ttu-id="0eb1b-115">Som standard brukes **H2**-overskriftskoden for overskriften.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="0eb1b-116">Koden kan imidlertid endres for å oppfylle tilgjengelighetskravene.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="0eb1b-117">Kontaktnummer</span><span class="sxs-lookup"><span data-stu-id="0eb1b-117">Contact number</span></span> | <span data-ttu-id="0eb1b-118">Text</span><span class="sxs-lookup"><span data-stu-id="0eb1b-118">Text</span></span> | <span data-ttu-id="0eb1b-119">Et kontaktnummer kan angis for spørsmål som er knyttet til ordren.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="0eb1b-120">Moduler som kan brukes på en ordredetaljside</span><span class="sxs-lookup"><span data-stu-id="0eb1b-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="0eb1b-121">Når du oppretter en ordredetaljside, kan du legge til andre relevante moduler i tillegg til ordredetaljmodulen.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="0eb1b-122">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="0eb1b-122">Here are some examples:</span></span>

- <span data-ttu-id="0eb1b-123">**Anbefalingsmodulen** – Anbefalingsmodulen kan legges til på ordredetaljsiden for å foreslå andre produkter for kunden.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="0eb1b-124">**Markedsføringsmoduler** – Enhver markedsføringsmodul kan legges til på ordredetaljsiden for å vise markedsføringsinnhold.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="add-an-order-details-module-to-a-page"></a><span data-ttu-id="0eb1b-125">Legge til en ordredetaljermodul på en side</span><span class="sxs-lookup"><span data-stu-id="0eb1b-125">Add an order details module to a page</span></span>

<span data-ttu-id="0eb1b-126">Hvis du vil legge til en ordredetaljermodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-126">To add an order details module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="0eb1b-127">Gå til **Maler**, og velg **Ny** for å opprette en ny mal.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-127">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="0eb1b-128">I dialogboksen **Ny mal**, under **Malnavn**, angir du navnet **Ordredetaljmal**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-128">In the **New Template** dialog box, under **Template name**, enter the name **Order details template**, and then select **OK**.</span></span>
1. <span data-ttu-id="0eb1b-129">I **Tekst**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-129">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0eb1b-130">I dialogboksen **Legg til modul** velger du **Standardside**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-130">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0eb1b-131">På **Hoved**-sporet på **Standardside**-modulen velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-131">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0eb1b-132">I dialogboksen **Legg til modul** velger du **Ordredetaljer**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-132">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0eb1b-133">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise malen.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-133">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="0eb1b-134">Ordredetaljmodulen blir ikke gjengitt, fordi den krever konteksten til ordrebekreftelsesnummeret.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-134">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="0eb1b-135">Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="0eb1b-136">Gå til **Sider**, og velg **Ny** for å opprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-136">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="0eb1b-137">I **Velg en mal**-dialogboksen velger du **Ordredetaljmal**.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-137">In the **Choose a template** dialog box, select **Order details template**.</span></span> <span data-ttu-id="0eb1b-138">Under **Sidenavn** angir du **Side for ordredetaljer**, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-138">Under **Page name**, enter **Order details page**, and then select **OK**.</span></span>
1. <span data-ttu-id="0eb1b-139">På **Hoved**-sporet på **Standardside**-modulen velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-139">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0eb1b-140">I dialogboksen **Legg til modul** velger du **Ordredetaljer**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-140">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0eb1b-141">I egenskapsruten for ordredetaljmodulen velger du **Overskrift** ved siden av blyantsymbolet.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-141">In the properties pane for the order details module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="0eb1b-142">I **Overskriftstekst**-feltet i dialogboksen **Overskrift** angir du overskriftsteksten **Ordredetaljer**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-142">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order details**, and then select **OK**.</span></span>
1. <span data-ttu-id="0eb1b-143">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-143">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="0eb1b-144">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-144">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0eb1b-145">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0eb1b-145">Additional resources</span></span>

[<span data-ttu-id="0eb1b-146">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="0eb1b-146">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0eb1b-147">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="0eb1b-147">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="0eb1b-148">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="0eb1b-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0eb1b-149">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="0eb1b-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="0eb1b-150">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="0eb1b-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="0eb1b-151">Leveringsalternativmodul</span><span class="sxs-lookup"><span data-stu-id="0eb1b-151">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="0eb1b-152">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="0eb1b-152">Gift card module</span></span>](add-giftcard.md)
