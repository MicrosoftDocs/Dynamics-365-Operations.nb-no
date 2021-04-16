---
title: Ordrebekreftelsesmodul
description: Dette emnet dekker ordrebekreftelsesmoduler og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1f8742637cc8ed29abcfb9a8061a8d2602762d4f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804583"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="5183f-103">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="5183f-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5183f-104">Dette emnet dekker ordrebekreftelsesmoduler og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5183f-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5183f-105">Ordrebekreftelsesmodulen brukes til å vise ordrebekreftelsesdetaljer etter at en ordre er lagt inn.</span><span class="sxs-lookup"><span data-stu-id="5183f-105">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="5183f-106">Den viser ID-en for ordrebekreftelse, ordrekontaktinformasjon og andre ordredetaljer, for eksempel varene som ble kjøpt, betalingsinformasjon, hentealternativer og forsendelsesmetoden.</span><span class="sxs-lookup"><span data-stu-id="5183f-106">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="5183f-107">Egenskaper for ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="5183f-107">Order confirmation module properties</span></span>

| <span data-ttu-id="5183f-108">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="5183f-108">Property name</span></span>  | <span data-ttu-id="5183f-109">Verdier</span><span class="sxs-lookup"><span data-stu-id="5183f-109">Values</span></span> | <span data-ttu-id="5183f-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5183f-110">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="5183f-111">Overskrift</span><span class="sxs-lookup"><span data-stu-id="5183f-111">Heading</span></span>        | <span data-ttu-id="5183f-112">Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="5183f-112">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="5183f-113">Ordrebekreftelsesmodulen kan ha en overskrift.</span><span class="sxs-lookup"><span data-stu-id="5183f-113">The order confirmation module can have a heading.</span></span> <span data-ttu-id="5183f-114">Som standard brukes **H2**-overskriftskoden for overskriften.</span><span class="sxs-lookup"><span data-stu-id="5183f-114">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="5183f-115">Koden kan imidlertid endres for å oppfylle tilgjengelighetskravene.</span><span class="sxs-lookup"><span data-stu-id="5183f-115">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="5183f-116">Kontaktnummer</span><span class="sxs-lookup"><span data-stu-id="5183f-116">Contact number</span></span> | <span data-ttu-id="5183f-117">Text</span><span class="sxs-lookup"><span data-stu-id="5183f-117">Text</span></span> | <span data-ttu-id="5183f-118">Et kontaktnummer kan angis for spørsmål som er knyttet til ordren.</span><span class="sxs-lookup"><span data-stu-id="5183f-118">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="5183f-119">Vis informasjon om hentetidspunkt</span><span class="sxs-lookup"><span data-stu-id="5183f-119">Show pickup timeslot information</span></span> | <span data-ttu-id="5183f-120">Sann eller Usann</span><span class="sxs-lookup"><span data-stu-id="5183f-120">True or False</span></span> | <span data-ttu-id="5183f-121">Denne egenskapen er tilgjengelig i Dynamics 365 Commerce 10.0.15 og nyere.</span><span class="sxs-lookup"><span data-stu-id="5183f-121">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="5183f-122">Hvis den er Sann, vises informasjon om hentetidspunkt hvis det er angitt for en hentevare</span><span class="sxs-lookup"><span data-stu-id="5183f-122">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="5183f-123">Moduler som kan brukes på en ordrebekreftelsesside</span><span class="sxs-lookup"><span data-stu-id="5183f-123">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="5183f-124">Når du oppretter en ordrebekreftelsesside, kan du legge til andre relevante moduler i tillegg til ordrebekreftelsesmodulen.</span><span class="sxs-lookup"><span data-stu-id="5183f-124">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="5183f-125">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="5183f-125">Here are some examples:</span></span>

- <span data-ttu-id="5183f-126">**Anbefalingsmodulen** – Anbefalingsmodulen kan legges til på ordrebekreftelsessiden for å foreslå andre produkter for kunden.</span><span class="sxs-lookup"><span data-stu-id="5183f-126">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="5183f-127">**Markedsføringsmoduler** – Enhver markedsføringsmodul kan legges til på ordrebekreftelsessiden for å vise markedsføringsinnhold.</span><span class="sxs-lookup"><span data-stu-id="5183f-127">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="5183f-128">Legge til en ordrebekreftelsesmodul på en side</span><span class="sxs-lookup"><span data-stu-id="5183f-128">Add an order confirmation module to a page</span></span>

<span data-ttu-id="5183f-129">Hvis du vil legge til en ordrebekreftelsesmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="5183f-129">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="5183f-130">Gå til **Maler**, og velg **Ny** for å opprette en ny mal.</span><span class="sxs-lookup"><span data-stu-id="5183f-130">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="5183f-131">I dialogboksen **Ny mal**, under **Malnavn**, angir du navnet **Ordrebekreftelsesmal**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="5183f-131">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="5183f-132">I **Tekst**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="5183f-132">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5183f-133">I dialogboksen **Legg til modul** velger du **Standardside**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="5183f-133">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5183f-134">På **Hoved**-sporet på **Standardside**-modulen velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="5183f-134">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5183f-135">I dialogboksen **Legg til modul** velger du **Ordrebekreftelses**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="5183f-135">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5183f-136">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise malen.</span><span class="sxs-lookup"><span data-stu-id="5183f-136">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="5183f-137">Ordrebekreftelsesmodulen blir ikke gjengitt fordi den krever konteksten til ordrebekreftelsesnummeret.</span><span class="sxs-lookup"><span data-stu-id="5183f-137">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="5183f-138">Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="5183f-138">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="5183f-139">Gå til **Sider**, og velg **Ny** for å opprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="5183f-139">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="5183f-140">I **Velg en mal**-dialogboksen velger du **Ordrebekreftelsesmal**.</span><span class="sxs-lookup"><span data-stu-id="5183f-140">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="5183f-141">Under **Sidenavn** angir du **Side for ordrebekreftelse**, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="5183f-141">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="5183f-142">På **Hoved**-sporet på **Standardside**-modulen velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="5183f-142">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5183f-143">I dialogboksen **Legg til modul** velger du **Ordrebekreftelses**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="5183f-143">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5183f-144">I egenskapsruten for ordrebekreftelsesmodulen velger du **Overskrift** ved siden av blyantsymbolet.</span><span class="sxs-lookup"><span data-stu-id="5183f-144">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="5183f-145">I **Overskriftstekst**-feltet i dialogboksen **Overskrift** angir du overskriftsteksten **Ordrebekreftelse**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="5183f-145">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="5183f-146">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="5183f-146">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="5183f-147">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="5183f-147">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5183f-148">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5183f-148">Additional resources</span></span>

[<span data-ttu-id="5183f-149">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="5183f-149">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5183f-150">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="5183f-150">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="5183f-151">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="5183f-151">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="5183f-152">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="5183f-152">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="5183f-153">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="5183f-153">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="5183f-154">Leveringsalternativmodul</span><span class="sxs-lookup"><span data-stu-id="5183f-154">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="5183f-155">Henteinformasjonsmodul</span><span class="sxs-lookup"><span data-stu-id="5183f-155">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="5183f-156">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="5183f-156">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]