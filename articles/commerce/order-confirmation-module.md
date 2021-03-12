---
title: Ordrebekreftelsesmodul
description: Dette emnet dekker ordrebekreftelsesmoduler og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9d916d2687777403f2b0df7c35171948ad2fb7db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972755"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="c4bb8-103">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="c4bb8-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c4bb8-104">Dette emnet dekker ordrebekreftelsesmoduler og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c4bb8-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="c4bb8-105">Overview</span></span>

<span data-ttu-id="c4bb8-106">Ordrebekreftelsesmodulen brukes til å vise ordrebekreftelsesdetaljer etter at en ordre er lagt inn.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-106">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="c4bb8-107">Den viser ID-en for ordrebekreftelse, ordrekontaktinformasjon og andre ordredetaljer, for eksempel varene som ble kjøpt, betalingsinformasjon, hentealternativer og forsendelsesmetoden.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="c4bb8-108">Egenskaper for ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="c4bb8-108">Order confirmation module properties</span></span>

| <span data-ttu-id="c4bb8-109">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="c4bb8-109">Property name</span></span>  | <span data-ttu-id="c4bb8-110">Verdier</span><span class="sxs-lookup"><span data-stu-id="c4bb8-110">Values</span></span> | <span data-ttu-id="c4bb8-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c4bb8-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="c4bb8-112">Overskrift</span><span class="sxs-lookup"><span data-stu-id="c4bb8-112">Heading</span></span>        | <span data-ttu-id="c4bb8-113">Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="c4bb8-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="c4bb8-114">Ordrebekreftelsesmodulen kan ha en overskrift.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="c4bb8-115">Som standard brukes **H2**-overskriftskoden for overskriften.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="c4bb8-116">Koden kan imidlertid endres for å oppfylle tilgjengelighetskravene.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="c4bb8-117">Kontaktnummer</span><span class="sxs-lookup"><span data-stu-id="c4bb8-117">Contact number</span></span> | <span data-ttu-id="c4bb8-118">Text</span><span class="sxs-lookup"><span data-stu-id="c4bb8-118">Text</span></span> | <span data-ttu-id="c4bb8-119">Et kontaktnummer kan angis for spørsmål som er knyttet til ordren.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-119">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="c4bb8-120">Vis informasjon om hentetidspunkt</span><span class="sxs-lookup"><span data-stu-id="c4bb8-120">Show pickup timeslot information</span></span> | <span data-ttu-id="c4bb8-121">Sann eller Usann</span><span class="sxs-lookup"><span data-stu-id="c4bb8-121">True or False</span></span> | <span data-ttu-id="c4bb8-122">Denne egenskapen er tilgjengelig i Dynamics 365 Commerce 10.0.15 og nyere.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-122">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="c4bb8-123">Hvis den er Sann, vises informasjon om hentetidspunkt hvis det er angitt for en hentevare</span><span class="sxs-lookup"><span data-stu-id="c4bb8-123">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="c4bb8-124">Moduler som kan brukes på en ordrebekreftelsesside</span><span class="sxs-lookup"><span data-stu-id="c4bb8-124">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="c4bb8-125">Når du oppretter en ordrebekreftelsesside, kan du legge til andre relevante moduler i tillegg til ordrebekreftelsesmodulen.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-125">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="c4bb8-126">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="c4bb8-126">Here are some examples:</span></span>

- <span data-ttu-id="c4bb8-127">**Anbefalingsmodulen** – Anbefalingsmodulen kan legges til på ordrebekreftelsessiden for å foreslå andre produkter for kunden.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-127">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="c4bb8-128">**Markedsføringsmoduler** – Enhver markedsføringsmodul kan legges til på ordrebekreftelsessiden for å vise markedsføringsinnhold.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-128">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="c4bb8-129">Legge til en ordrebekreftelsesmodul på en side</span><span class="sxs-lookup"><span data-stu-id="c4bb8-129">Add an order confirmation module to a page</span></span>

<span data-ttu-id="c4bb8-130">Hvis du vil legge til en ordrebekreftelsesmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-130">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="c4bb8-131">Gå til **Maler**, og velg **Ny** for å opprette en ny mal.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-131">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="c4bb8-132">I dialogboksen **Ny mal**, under **Malnavn**, angir du navnet **Ordrebekreftelsesmal**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-132">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="c4bb8-133">I **Tekst**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-133">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c4bb8-134">I dialogboksen **Legg til modul** velger du **Standardside**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-134">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c4bb8-135">På **Hoved**-sporet på **Standardside**-modulen velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-135">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c4bb8-136">I dialogboksen **Legg til modul** velger du **Ordrebekreftelses**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-136">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c4bb8-137">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise malen.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-137">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="c4bb8-138">Ordrebekreftelsesmodulen blir ikke gjengitt fordi den krever konteksten til ordrebekreftelsesnummeret.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-138">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="c4bb8-139">Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="c4bb8-140">Gå til **Sider**, og velg **Ny** for å opprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-140">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="c4bb8-141">I **Velg en mal**-dialogboksen velger du **Ordrebekreftelsesmal**.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-141">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="c4bb8-142">Under **Sidenavn** angir du **Side for ordrebekreftelse**, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-142">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="c4bb8-143">På **Hoved**-sporet på **Standardside**-modulen velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-143">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c4bb8-144">I dialogboksen **Legg til modul** velger du **Ordrebekreftelses**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-144">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c4bb8-145">I egenskapsruten for ordrebekreftelsesmodulen velger du **Overskrift** ved siden av blyantsymbolet.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-145">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="c4bb8-146">I **Overskriftstekst**-feltet i dialogboksen **Overskrift** angir du overskriftsteksten **Ordrebekreftelse**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-146">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="c4bb8-147">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-147">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="c4bb8-148">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="c4bb8-148">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c4bb8-149">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c4bb8-149">Additional resources</span></span>

[<span data-ttu-id="c4bb8-150">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="c4bb8-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c4bb8-151">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="c4bb8-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="c4bb8-152">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="c4bb8-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c4bb8-153">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="c4bb8-153">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="c4bb8-154">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="c4bb8-154">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="c4bb8-155">Leveringsalternativmodul</span><span class="sxs-lookup"><span data-stu-id="c4bb8-155">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="c4bb8-156">Henteinformasjonsmodul</span><span class="sxs-lookup"><span data-stu-id="c4bb8-156">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="c4bb8-157">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="c4bb8-157">Gift card module</span></span>](add-giftcard.md)
