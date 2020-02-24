---
title: Ordredetaljermodulen
description: Dette emnet dekker ordredetaljmoduler og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026023"
---
# <a name="order-details-module"></a><span data-ttu-id="7882a-103">Ordredetaljermodulen</span><span class="sxs-lookup"><span data-stu-id="7882a-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7882a-104">Dette emnet dekker ordredetaljmoduler og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7882a-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7882a-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="7882a-105">Overview</span></span>

<span data-ttu-id="7882a-106">Ordredetaljmodulen brukes til å vise ordrebekreftelsesdetaljer etter at en ordre er lagt inn.</span><span class="sxs-lookup"><span data-stu-id="7882a-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="7882a-107">Den viser ID-en for ordrebekreftelse, ordrekontaktinformasjon og andre ordredetaljer, for eksempel varene som ble kjøpt, betalingsinformasjon og forsendelsesmetoden.</span><span class="sxs-lookup"><span data-stu-id="7882a-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="7882a-108">Egenskaper for ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="7882a-108">Order confirmation module properties</span></span>

| <span data-ttu-id="7882a-109">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="7882a-109">Property name</span></span>  | <span data-ttu-id="7882a-110">Verdier</span><span class="sxs-lookup"><span data-stu-id="7882a-110">Values</span></span> | <span data-ttu-id="7882a-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="7882a-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="7882a-112">Overskrift</span><span class="sxs-lookup"><span data-stu-id="7882a-112">Heading</span></span>        | <span data-ttu-id="7882a-113">Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="7882a-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="7882a-114">Ordrebekreftelsesmodulen kan ha en overskrift.</span><span class="sxs-lookup"><span data-stu-id="7882a-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="7882a-115">Som standard brukes **H2**-overskriftskoden for overskriften.</span><span class="sxs-lookup"><span data-stu-id="7882a-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="7882a-116">Koden kan imidlertid endres for å oppfylle tilgjengelighetskravene.</span><span class="sxs-lookup"><span data-stu-id="7882a-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="7882a-117">Kontaktnummer</span><span class="sxs-lookup"><span data-stu-id="7882a-117">Contact number</span></span> | <span data-ttu-id="7882a-118">Text</span><span class="sxs-lookup"><span data-stu-id="7882a-118">Text</span></span> | <span data-ttu-id="7882a-119">Et kontaktnummer kan angis for spørsmål som er knyttet til ordren.</span><span class="sxs-lookup"><span data-stu-id="7882a-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="7882a-120">Moduler som kan brukes på en ordredetaljside</span><span class="sxs-lookup"><span data-stu-id="7882a-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="7882a-121">Når du oppretter en ordredetaljside, kan du legge til andre relevante moduler i tillegg til ordredetaljmodulen.</span><span class="sxs-lookup"><span data-stu-id="7882a-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="7882a-122">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="7882a-122">Here are some examples:</span></span>

- <span data-ttu-id="7882a-123">**Anbefalingsmodulen** – Anbefalingsmodulen kan legges til på ordredetaljsiden for å foreslå andre produkter for kunden.</span><span class="sxs-lookup"><span data-stu-id="7882a-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="7882a-124">**Markedsføringsmoduler** – Enhver markedsføringsmodul kan legges til på ordredetaljsiden for å vise markedsføringsinnhold.</span><span class="sxs-lookup"><span data-stu-id="7882a-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="create-an-order-details-page-module"></a><span data-ttu-id="7882a-125">Opprette en modul for ordredetaljside</span><span class="sxs-lookup"><span data-stu-id="7882a-125">Create an order details page module</span></span>

1. <span data-ttu-id="7882a-126">Opprett en sidemal som heter **Ordredetaljer**.</span><span class="sxs-lookup"><span data-stu-id="7882a-126">Create a page template that is named **Order details template**.</span></span>
1. <span data-ttu-id="7882a-127">I **Hoved**-sporet på standardsiden legger du til en ordredetaljmodul.</span><span class="sxs-lookup"><span data-stu-id="7882a-127">In the **Main** slot of the default page, add an order details module.</span></span>
1. <span data-ttu-id="7882a-128">I ordredetaljmodulen legger du til en anbefalingsmodul.</span><span class="sxs-lookup"><span data-stu-id="7882a-128">In the order details module, add a recommendations module.</span></span>
1. <span data-ttu-id="7882a-129">Lagre og forhåndsvis malen.</span><span class="sxs-lookup"><span data-stu-id="7882a-129">Save and preview the template.</span></span> <span data-ttu-id="7882a-130">Ordredetaljmodulen blir ikke gjengitt, fordi den krever konteksten til ordrebekreftelsesnummeret.</span><span class="sxs-lookup"><span data-stu-id="7882a-130">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="7882a-131">Fullfør redigeringen av malen, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="7882a-131">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="7882a-132">Bruk ordredetaljmalen du nettopp opprettet, til å opprette en side som heter **ordredetaljside**.</span><span class="sxs-lookup"><span data-stu-id="7882a-132">Use the order details template that you just created to create a page that is named **order details page**.</span></span>
1. <span data-ttu-id="7882a-133">Legg til standardsiden i sidedisposisjonen.</span><span class="sxs-lookup"><span data-stu-id="7882a-133">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="7882a-134">Legg til et topptekstfragment i **Hode**-sporet.</span><span class="sxs-lookup"><span data-stu-id="7882a-134">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="7882a-135">Legg til et bunntekstfragment i **Bunntekst**-sporet.</span><span class="sxs-lookup"><span data-stu-id="7882a-135">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="7882a-136">I **Hoved**-sporet legger du til en ordredetaljmodul.</span><span class="sxs-lookup"><span data-stu-id="7882a-136">In the **Main** slot, add an order details module.</span></span>
1. <span data-ttu-id="7882a-137">I egenskapsruten for ordredetaljmodulen legger du til overskriften **Ordredetaljer**.</span><span class="sxs-lookup"><span data-stu-id="7882a-137">In the property pane for the order details module, add the heading **Order details**.</span></span>
1. <span data-ttu-id="7882a-138">Under ordredetaljmodulen legger du til en anbefalingsmodul og konfigurerer den slik at den bruker innstillingene for **Nye** og **Bestselgere**.</span><span class="sxs-lookup"><span data-stu-id="7882a-138">Below the order details module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="7882a-139">Lagre og forhåndsvis siden.</span><span class="sxs-lookup"><span data-stu-id="7882a-139">Save and preview the page.</span></span>
1. <span data-ttu-id="7882a-140">Fullfør redigeringen av siden, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="7882a-140">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7882a-141">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="7882a-141">Additional resources</span></span>

[<span data-ttu-id="7882a-142">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="7882a-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7882a-143">Containermodul</span><span class="sxs-lookup"><span data-stu-id="7882a-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="7882a-144">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="7882a-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="7882a-145">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="7882a-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="7882a-146">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="7882a-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7882a-147">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="7882a-147">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="7882a-148">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="7882a-148">Footer module</span></span>](author-footer-module.md)
