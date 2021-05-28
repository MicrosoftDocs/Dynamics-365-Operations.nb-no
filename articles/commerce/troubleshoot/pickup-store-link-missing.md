---
title: Alternativet Hent vises ikke på handlekurv- eller produktdetaljsidene
description: Dette emnet gir feilsøkingsretningsinformasjon som kan hjelpe når alternativet for henting i butikken ikke vises på handlekurvsiden eller produktdetaljersidene.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: f692d73bf1755422e9bfc8314c1156e043ccf761
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020818"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="0e046-103">Alternativet Hent vises ikke på handlekurv- eller produktdetaljsidene</span><span class="sxs-lookup"><span data-stu-id="0e046-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e046-104">Dette emnet gir feilsøkingsretningsinformasjon som kan hjelpe når alternativet for henting i butikken ikke vises på handlekurvsiden eller produktdetaljersidene.</span><span class="sxs-lookup"><span data-stu-id="0e046-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="0e046-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0e046-105">Description</span></span>

<span data-ttu-id="0e046-106">Knappen **Hent** vises ikke på handlekurv- eller produktdetaljsidene.</span><span class="sxs-lookup"><span data-stu-id="0e046-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="0e046-107">Illustrasjonen nedenfor viser et eksempel på en side som inneholder knappen **Hent**.</span><span class="sxs-lookup"><span data-stu-id="0e046-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![Knappen Hent](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="0e046-109">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="0e046-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="0e046-110">Aktivere BOPIS-tillegget i Commerce-områdebyggeren</span><span class="sxs-lookup"><span data-stu-id="0e046-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="0e046-111">Følg denne fremgangsmåten for å aktivere tillegget Kjøpe på Internett og hente i butikk (BOPIS) i Commerce-områdebyggeren:</span><span class="sxs-lookup"><span data-stu-id="0e046-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="0e046-112">Velg området ditt.</span><span class="sxs-lookup"><span data-stu-id="0e046-112">Select your site.</span></span>
1. <span data-ttu-id="0e046-113">Velg **Områdeinnstillinger** og deretter **Utvidelser**.</span><span class="sxs-lookup"><span data-stu-id="0e046-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="0e046-114">Kontroller at det ikke er merket av for alternativet **Deaktiver BOPIS**.</span><span class="sxs-lookup"><span data-stu-id="0e046-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="0e046-115">Konfigurere leveringsmåter i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="0e046-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="0e046-116">Følg denne fremgangsmåten for å konfigurere leveringsmåter i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="0e046-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="0e046-117">Gå til **Innkjøp og leverandører \> Oppsett \> Leveringsmåter**.</span><span class="sxs-lookup"><span data-stu-id="0e046-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="0e046-118">Kontroller at leveringsmåten **Kundehenting** er opprettet, og at det er tilordnet produkter og adresser til den.</span><span class="sxs-lookup"><span data-stu-id="0e046-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="0e046-119">Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere**.</span><span class="sxs-lookup"><span data-stu-id="0e046-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="0e046-120">Velg **Kundeordrer** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="0e046-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="0e046-121">Kontroller at **Henteleveringsmåte** er riktig konfigurert.</span><span class="sxs-lookup"><span data-stu-id="0e046-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="0e046-122">Konfigurere betalinger for kundeordrer</span><span class="sxs-lookup"><span data-stu-id="0e046-122">Configure customer orders payments</span></span>

<span data-ttu-id="0e046-123">Følg denne fremgangsmåten for å konfigurere betalinger for kundeordrer i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="0e046-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="0e046-124">Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere**.</span><span class="sxs-lookup"><span data-stu-id="0e046-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="0e046-125">Velg **Kundeordrer** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="0e046-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="0e046-126">Kontroller at feltene **Betalingsbetingelser** og **Betalingsmåte** er riktig angitt i hurtigfanen **Betalinger**.</span><span class="sxs-lookup"><span data-stu-id="0e046-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e046-127">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0e046-127">Additional resources</span></span>

[<span data-ttu-id="0e046-128">Konfigurere BOPIS</span><span class="sxs-lookup"><span data-stu-id="0e046-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="0e046-129">Aktiver flere henteleveringsmåter for kundeordrer</span><span class="sxs-lookup"><span data-stu-id="0e046-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="0e046-130">Commerce-ordrebetalinger for omnikanal</span><span class="sxs-lookup"><span data-stu-id="0e046-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="0e046-131">Butikkvelgermodul</span><span class="sxs-lookup"><span data-stu-id="0e046-131">Store selector module</span></span>](../store-selector.md)
