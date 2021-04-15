---
title: Alternativet Hent vises ikke på handlekurv- eller produktdetaljsidene
description: Dette emnet gir feilsøkingsretningsinformasjon som kan hjelpe når alternativet for henting i butikken ikke vises på handlekurvsiden eller produktdetaljersidene.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 46eeed18bb547035603d7e9a01e8f131a2393f01
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801633"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="64f35-103">Alternativet Hent vises ikke på handlekurv- eller produktdetaljsidene</span><span class="sxs-lookup"><span data-stu-id="64f35-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64f35-104">Dette emnet gir feilsøkingsretningsinformasjon som kan hjelpe når alternativet for henting i butikken ikke vises på handlekurvsiden eller produktdetaljersidene.</span><span class="sxs-lookup"><span data-stu-id="64f35-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="64f35-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="64f35-105">Description</span></span>

<span data-ttu-id="64f35-106">Knappen **Hent** vises ikke på handlekurv- eller produktdetaljsidene.</span><span class="sxs-lookup"><span data-stu-id="64f35-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="64f35-107">Illustrasjonen nedenfor viser et eksempel på en side som inneholder knappen **Hent**.</span><span class="sxs-lookup"><span data-stu-id="64f35-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![Knappen Hent](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="64f35-109">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="64f35-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="64f35-110">Aktivere BOPIS-tillegget i Commerce-områdebyggeren</span><span class="sxs-lookup"><span data-stu-id="64f35-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="64f35-111">Følg denne fremgangsmåten for å aktivere tillegget Kjøpe på Internett og hente i butikk (BOPIS) i Commerce-områdebyggeren:</span><span class="sxs-lookup"><span data-stu-id="64f35-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="64f35-112">Velg området ditt.</span><span class="sxs-lookup"><span data-stu-id="64f35-112">Select your site.</span></span>
1. <span data-ttu-id="64f35-113">Velg **Områdeinnstillinger** og deretter **Utvidelser**.</span><span class="sxs-lookup"><span data-stu-id="64f35-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="64f35-114">Kontroller at det ikke er merket av for alternativet **Deaktiver BOPIS**.</span><span class="sxs-lookup"><span data-stu-id="64f35-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="64f35-115">Konfigurere leveringsmåter i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="64f35-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="64f35-116">Følg denne fremgangsmåten for å konfigurere leveringsmåter i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="64f35-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="64f35-117">Gå til **Innkjøp og leverandører \> Oppsett \> Leveringsmåter**.</span><span class="sxs-lookup"><span data-stu-id="64f35-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="64f35-118">Kontroller at leveringsmåten **Kundehenting** er opprettet, og at det er tilordnet produkter og adresser til den.</span><span class="sxs-lookup"><span data-stu-id="64f35-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="64f35-119">Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere**.</span><span class="sxs-lookup"><span data-stu-id="64f35-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="64f35-120">Velg **Kundeordrer** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="64f35-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="64f35-121">Kontroller at **Henteleveringsmåte** er riktig konfigurert.</span><span class="sxs-lookup"><span data-stu-id="64f35-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="64f35-122">Konfigurere betalinger for kundeordrer</span><span class="sxs-lookup"><span data-stu-id="64f35-122">Configure customer orders payments</span></span>

<span data-ttu-id="64f35-123">Følg denne fremgangsmåten for å konfigurere betalinger for kundeordrer i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="64f35-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="64f35-124">Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere**.</span><span class="sxs-lookup"><span data-stu-id="64f35-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="64f35-125">Velg **Kundeordrer** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="64f35-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="64f35-126">Kontroller at feltene **Betalingsbetingelser** og **Betalingsmåte** er riktig angitt i hurtigfanen **Betalinger**.</span><span class="sxs-lookup"><span data-stu-id="64f35-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64f35-127">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="64f35-127">Additional resources</span></span>

[<span data-ttu-id="64f35-128">Konfigurere BOPIS</span><span class="sxs-lookup"><span data-stu-id="64f35-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="64f35-129">Aktiver flere henteleveringsmåter for kundeordrer</span><span class="sxs-lookup"><span data-stu-id="64f35-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="64f35-130">Commerce-ordrebetalinger for omnikanal</span><span class="sxs-lookup"><span data-stu-id="64f35-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="64f35-131">Butikkvelgermodul</span><span class="sxs-lookup"><span data-stu-id="64f35-131">Store selector module</span></span>](../store-selector.md)
