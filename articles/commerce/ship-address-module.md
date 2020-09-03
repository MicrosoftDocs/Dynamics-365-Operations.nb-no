---
title: Leveringsadressemodul
description: Dette emnet dekker leveringsadressemodulen og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 380d268ec0ba64367f090c31408eac1c54d0ff17
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661447"
---
# <a name="shipping-address-module"></a><span data-ttu-id="b4d76-103">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="b4d76-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="b4d76-104">Dette emnet beskriver leveringsadressemodulen og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b4d76-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b4d76-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="b4d76-105">Overview</span></span>

<span data-ttu-id="b4d76-106">Med leveringsadressemodulen kan kunder legge til eller velge leveringsadressen for en ordre under betalingen.</span><span class="sxs-lookup"><span data-stu-id="b4d76-106">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="b4d76-107">Hvis en kunde er logget på, vises alle adresser som tidligere ble lagret for denne kunden, og kunden kan velge mellom dem.</span><span class="sxs-lookup"><span data-stu-id="b4d76-107">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="b4d76-108">Kunden kan også legge til en ny adresse.</span><span class="sxs-lookup"><span data-stu-id="b4d76-108">The customer can also add a new address.</span></span> <span data-ttu-id="b4d76-109">Leveringsadressemodulen brukes for alle varer i en ordre som krever levering.</span><span class="sxs-lookup"><span data-stu-id="b4d76-109">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="b4d76-110">Leveringsadresseformater kan defineres i Commerce Headquarters for hvert land eller område, og leveringsadressemodulen håndhever deretter regler som er spesifikk for land/område.</span><span class="sxs-lookup"><span data-stu-id="b4d76-110">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="b4d76-111">Når kunder angir en leveringsadresse under betalingen, har de muligheten til å lagre adressen som en primær adresse.</span><span class="sxs-lookup"><span data-stu-id="b4d76-111">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="b4d76-112">Dette alternativet vises bare hvis en kunde er logget på.</span><span class="sxs-lookup"><span data-stu-id="b4d76-112">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="b4d76-113">Selv om denne leveringsadressemodulen ikke tilbyr adressevalidering, kan denne funksjonaliteten implementeres ved hjelp av tilpassing.</span><span class="sxs-lookup"><span data-stu-id="b4d76-113">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="b4d76-114">Illustrasjonen nedenfor viser et eksempel på en ny leveringsadressemodul på en kasseside.</span><span class="sxs-lookup"><span data-stu-id="b4d76-114">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Eksempel på en leveringsadressemodul på en kasseside](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="b4d76-116">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="b4d76-116">Module properties</span></span>

| <span data-ttu-id="b4d76-117">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="b4d76-117">Property name</span></span> | <span data-ttu-id="b4d76-118">Verdier</span><span class="sxs-lookup"><span data-stu-id="b4d76-118">Values</span></span> | <span data-ttu-id="b4d76-119">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b4d76-119">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="b4d76-120">Overskrift</span><span class="sxs-lookup"><span data-stu-id="b4d76-120">Heading</span></span> | <span data-ttu-id="b4d76-121">Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="b4d76-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="b4d76-122">En valgfri overskrift for leveringsadressemodulen.</span><span class="sxs-lookup"><span data-stu-id="b4d76-122">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="b4d76-123">Vis adressetype</span><span class="sxs-lookup"><span data-stu-id="b4d76-123">Show address type</span></span> | <span data-ttu-id="b4d76-124">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="b4d76-124">**True** or **False**</span></span> | <span data-ttu-id="b4d76-125">Hvis denne valgfrie egenskapen er satt til **Sann**, vises en adressetype, for eksempel **Hjem** eller **Bedrift**.</span><span class="sxs-lookup"><span data-stu-id="b4d76-125">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="b4d76-126">Hvis ingen adressetype er angitt, lagres adressen automatisk som **Type**=**Annet**.</span><span class="sxs-lookup"><span data-stu-id="b4d76-126">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="b4d76-127">Legge til en leveringsadressemodul på en kasseside og angi de nødvendige egenskapene</span><span class="sxs-lookup"><span data-stu-id="b4d76-127">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="b4d76-128">En leveringsadressemodul kan bare legges til i en kassemodul.</span><span class="sxs-lookup"><span data-stu-id="b4d76-128">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="b4d76-129">Hvis du vil ha mer informasjon om hvordan du konfigurerer leveringsadressemodulen og legger den til på en kasseside, se [Kassemodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="b4d76-129">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4d76-130">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b4d76-130">Additional resources</span></span>

[<span data-ttu-id="b4d76-131">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="b4d76-131">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b4d76-132">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="b4d76-132">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b4d76-133">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="b4d76-133">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b4d76-134">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="b4d76-134">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b4d76-135">Leveringsalternativmodul</span><span class="sxs-lookup"><span data-stu-id="b4d76-135">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b4d76-136">Ordredetaljermodul</span><span class="sxs-lookup"><span data-stu-id="b4d76-136">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b4d76-137">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="b4d76-137">Gift card module</span></span>](add-giftcard.md)