---
title: Ordrebekreftelsesmodul
description: Dette emnet dekker ordrebekreftelsesmoduler og beskriver hvordan du oppretter dem i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698332"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="30cbe-103">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="30cbe-103">Order confirmation module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="30cbe-104">Dette emnet dekker ordrebekreftelsesmoduler og beskriver hvordan du oppretter dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="30cbe-104">This topic covers order confirmation modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="30cbe-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="30cbe-105">Overview</span></span>

<span data-ttu-id="30cbe-106">En ordrebekreftelsesmodul brukes til å vise en bekreftelsesmelding på en ordrebekreftelsesside etter at en ordre er plassert.</span><span class="sxs-lookup"><span data-stu-id="30cbe-106">An order confirmation module is used to show a confirmation message on an order confirmation page after an order is placed.</span></span> <span data-ttu-id="30cbe-107">Ordrebekreftelsesmodulen viser ordrebekreftelsesnummeret og kundens e-postadresse som ble angitt ved utsjekking.</span><span class="sxs-lookup"><span data-stu-id="30cbe-107">The order confirmation module shows the order confirmation number and the customer email address that was provided during checkout.</span></span>

<span data-ttu-id="30cbe-108">Når en ordre blir lagt inn under utsjekking, sendes ordrebekreftelsesnummeret og kundens e-postadresse til ordrebekreftelsessiden som en spørringsstreng i URL-adressen til siden.</span><span class="sxs-lookup"><span data-stu-id="30cbe-108">When an order is placed during checkout, the order confirmation number and customer email address are passed to the order confirmation page as a query string in the page's URL.</span></span> <span data-ttu-id="30cbe-109">Ordrebekreftelsesmodulen mottar denne informasjonen og gjengir ordrestatusen på ordrebekreftelsessiden.</span><span class="sxs-lookup"><span data-stu-id="30cbe-109">The order confirmation module receives this information and renders the order status on the order confirmation page.</span></span> <span data-ttu-id="30cbe-110">Ordrebekreftelsesmodulen krever denne sidekonteksten for å angi statusen for ordren.</span><span class="sxs-lookup"><span data-stu-id="30cbe-110">The order confirmation module requires this page context to provide the status of the order.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="30cbe-111">Egenskaper for ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="30cbe-111">Order confirmation module properties</span></span>

| <span data-ttu-id="30cbe-112">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="30cbe-112">Property name</span></span> | <span data-ttu-id="30cbe-113">Verdier</span><span class="sxs-lookup"><span data-stu-id="30cbe-113">Values</span></span> | <span data-ttu-id="30cbe-114">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="30cbe-114">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="30cbe-115">Overskrift</span><span class="sxs-lookup"><span data-stu-id="30cbe-115">Heading</span></span>       | <span data-ttu-id="30cbe-116">Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="30cbe-116">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="30cbe-117">Ordrebekreftelsesmodulen kan ha en overskrift.</span><span class="sxs-lookup"><span data-stu-id="30cbe-117">The order confirmation module can have a heading.</span></span> <span data-ttu-id="30cbe-118">Som standard brukes **H2**-overskriftskoden for overskriften.</span><span class="sxs-lookup"><span data-stu-id="30cbe-118">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="30cbe-119">Koden kan imidlertid endres for å oppfylle tilgjengelighetskravene.</span><span class="sxs-lookup"><span data-stu-id="30cbe-119">However, the tag can be changed to meet accessibility requirements.</span></span> |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a><span data-ttu-id="30cbe-120">Moduler som kan brukes i en modul for ordrebekreftelsesside</span><span class="sxs-lookup"><span data-stu-id="30cbe-120">Modules that can be used in an order confirmation page module</span></span> 

- <span data-ttu-id="30cbe-121">**Anbefalinger** – Anbefalingsmodulen kan plasseres på ordrebekreftelsessiden for å foreslå andre produkter for kunden.</span><span class="sxs-lookup"><span data-stu-id="30cbe-121">**Recommendations** – The recommendations module can be put on the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="30cbe-122">**Markedsføring** – Markedsføringsmodulen kan legge til markedsføringsinnhold på ordrebekreftelsessiden.</span><span class="sxs-lookup"><span data-stu-id="30cbe-122">**Marketing** – The marketing module can add marketing content to the order confirmation page.</span></span>

## <a name="create-an-order-confirmation-page-module"></a><span data-ttu-id="30cbe-123">Opprette en modul for ordrebekreftelsesside</span><span class="sxs-lookup"><span data-stu-id="30cbe-123">Create an order confirmation page module</span></span>

1. <span data-ttu-id="30cbe-124">Opprett en sidemal som heter **ordrebekreftelsesmal**.</span><span class="sxs-lookup"><span data-stu-id="30cbe-124">Create a page template that is named **order confirmation template**.</span></span>
1. <span data-ttu-id="30cbe-125">I **Hoved**-sporet på standardsiden legger du til en ordrebekreftelsesmodul.</span><span class="sxs-lookup"><span data-stu-id="30cbe-125">In the **Main** slot of the default page, add an order confirmation module.</span></span>
1. <span data-ttu-id="30cbe-126">I ordrebekreftelsesmodulen legger du til en anbefalingsmodul.</span><span class="sxs-lookup"><span data-stu-id="30cbe-126">In the order confirmation module, add a recommendations module.</span></span>
1. <span data-ttu-id="30cbe-127">Lagre og forhåndsvis malen.</span><span class="sxs-lookup"><span data-stu-id="30cbe-127">Save and preview the template.</span></span> <span data-ttu-id="30cbe-128">Ordrebekreftelsesmodulen skal ikke gjengis, fordi den krever konteksten til ordrebekreftelsesnummeret.</span><span class="sxs-lookup"><span data-stu-id="30cbe-128">The order confirmation module should not be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="30cbe-129">Sjekk inn malen, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="30cbe-129">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="30cbe-130">Bruk ordrebekreftelsesmalen du nettopp opprettet, til å opprette en side som heter **ordrebekreftelsesside**.</span><span class="sxs-lookup"><span data-stu-id="30cbe-130">Use the order confirmation template that you just created to create a page that is named **order confirmation page**.</span></span>
1. <span data-ttu-id="30cbe-131">Legg til standardsiden i sidedisposisjonen.</span><span class="sxs-lookup"><span data-stu-id="30cbe-131">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="30cbe-132">Legg til et topptekstfragment i **Hode**-sporet.</span><span class="sxs-lookup"><span data-stu-id="30cbe-132">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="30cbe-133">Legg til et bunntekstfragment i **Bunntekst**-sporet.</span><span class="sxs-lookup"><span data-stu-id="30cbe-133">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="30cbe-134">I **Hoved**-sporet legger du til en ordrebekreftelsesmodul.</span><span class="sxs-lookup"><span data-stu-id="30cbe-134">In the **Main** slot, add an order confirmation module.</span></span>
1. <span data-ttu-id="30cbe-135">I egenskapsruten i ordrebekreftelsesmodulen legger du til overskriften **Ordrebekreftelse**.</span><span class="sxs-lookup"><span data-stu-id="30cbe-135">In the property pane of the order confirmation module, add the heading **Order confirmation**.</span></span>
1. <span data-ttu-id="30cbe-136">Under ordrebekreftelsesmodulen legger du til en anbefalingsmodul og konfigurerer den slik at den bruker innstillingene for **Nye** og **Bestselgere**.</span><span class="sxs-lookup"><span data-stu-id="30cbe-136">Below the order confirmation module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="30cbe-137">Lagre og forhåndsvis siden, sjekk det inn, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="30cbe-137">Save and preview the page, check it in, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30cbe-138">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="30cbe-138">Additional resources</span></span>

[<span data-ttu-id="30cbe-139">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="30cbe-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="30cbe-140">Containermodul</span><span class="sxs-lookup"><span data-stu-id="30cbe-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="30cbe-141">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="30cbe-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="30cbe-142">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="30cbe-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="30cbe-143">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="30cbe-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="30cbe-144">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="30cbe-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="30cbe-145">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="30cbe-145">Footer module</span></span>](author-footer-module.md)
