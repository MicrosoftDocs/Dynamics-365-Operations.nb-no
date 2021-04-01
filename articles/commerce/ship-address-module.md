---
title: Leveringsadressemodul
description: Dette emnet dekker leveringsadressemodulen og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 02/11/2021
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e590c966ca6bd8111df5f91cbac0485afaa45c78
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234419"
---
# <a name="shipping-address-module"></a><span data-ttu-id="fe464-103">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="fe464-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fe464-104">Dette emnet beskriver leveringsadressemodulen og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fe464-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fe464-105">Med leveringsadressemodulen kan kunder legge til eller velge leveringsadressen for en ordre under betalingen.</span><span class="sxs-lookup"><span data-stu-id="fe464-105">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="fe464-106">Hvis en kunde er logget på, vises alle adresser som tidligere ble lagret for denne kunden, og kunden kan velge mellom dem.</span><span class="sxs-lookup"><span data-stu-id="fe464-106">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="fe464-107">Kunden kan også legge til en ny adresse.</span><span class="sxs-lookup"><span data-stu-id="fe464-107">The customer can also add a new address.</span></span> <span data-ttu-id="fe464-108">Leveringsadressemodulen brukes for alle varer i en ordre som krever levering.</span><span class="sxs-lookup"><span data-stu-id="fe464-108">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="fe464-109">Leveringsadresseformater kan defineres i Commerce Headquarters for hvert land eller område, og leveringsadressemodulen håndhever deretter regler som er spesifikk for land/område.</span><span class="sxs-lookup"><span data-stu-id="fe464-109">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="fe464-110">Når kunder angir en leveringsadresse under betalingen, har de muligheten til å lagre adressen som en primær adresse.</span><span class="sxs-lookup"><span data-stu-id="fe464-110">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="fe464-111">Dette alternativet vises bare hvis en kunde er logget på.</span><span class="sxs-lookup"><span data-stu-id="fe464-111">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="fe464-112">Selv om denne leveringsadressemodulen ikke tilbyr adressevalidering, kan denne funksjonaliteten implementeres ved hjelp av tilpassing.</span><span class="sxs-lookup"><span data-stu-id="fe464-112">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="fe464-113">Illustrasjonen nedenfor viser et eksempel på en ny leveringsadressemodul på en kasseside.</span><span class="sxs-lookup"><span data-stu-id="fe464-113">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Eksempel på en leveringsadressemodul på en kasseside](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="fe464-115">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="fe464-115">Module properties</span></span>

| <span data-ttu-id="fe464-116">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="fe464-116">Property name</span></span> | <span data-ttu-id="fe464-117">Verdier</span><span class="sxs-lookup"><span data-stu-id="fe464-117">Values</span></span> | <span data-ttu-id="fe464-118">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fe464-118">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="fe464-119">Overskrift</span><span class="sxs-lookup"><span data-stu-id="fe464-119">Heading</span></span> | <span data-ttu-id="fe464-120">Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="fe464-120">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="fe464-121">En valgfri overskrift for leveringsadressemodulen.</span><span class="sxs-lookup"><span data-stu-id="fe464-121">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="fe464-122">Vis adressetype</span><span class="sxs-lookup"><span data-stu-id="fe464-122">Show address type</span></span> | <span data-ttu-id="fe464-123">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="fe464-123">**True** or **False**</span></span> | <span data-ttu-id="fe464-124">Hvis denne valgfrie egenskapen er satt til **Sann**, vises en adressetype, for eksempel **Hjem** eller **Bedrift**.</span><span class="sxs-lookup"><span data-stu-id="fe464-124">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="fe464-125">Hvis ingen adressetype er angitt, lagres adressen automatisk som **Type**=**Annet**.</span><span class="sxs-lookup"><span data-stu-id="fe464-125">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |
| <span data-ttu-id="fe464-126">Aktiver automatisk forslag</span><span class="sxs-lookup"><span data-stu-id="fe464-126">Enable auto suggestion</span></span>| <span data-ttu-id="fe464-127">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="fe464-127">**True** or **False**</span></span> | <span data-ttu-id="fe464-128">Hvis denne valgfrie egenskapen er satt til **Sann**, vises automatiske adresseforslag.</span><span class="sxs-lookup"><span data-stu-id="fe464-128">If this optional property is set to **True**, automatic address suggestions will be provided.</span></span> <span data-ttu-id="fe464-129">Du får disse forslagene fra Bing-kart.</span><span class="sxs-lookup"><span data-stu-id="fe464-129">These suggestions are powered by Bing Maps.</span></span> <span data-ttu-id="fe464-130">Hvis du vil ha informasjon om hvordan du konfigurerer integrering av Bing-kart for området, kan du se [Butikkvelgermodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="fe464-130">For information about how to set up Bing Maps integration for your site, see [Store selector module](store-selector.md).</span></span> <span data-ttu-id="fe464-131">Denne funksjonen er tilgjengelig fra og med Commerce-versjon 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="fe464-131">This feature is available as of the Commerce version 10.0.15 release.</span></span>|
|<span data-ttu-id="fe464-132">Alternativer for automatisk forslag</span><span class="sxs-lookup"><span data-stu-id="fe464-132">Auto suggest options</span></span>| <span data-ttu-id="fe464-133">Et nummer</span><span class="sxs-lookup"><span data-stu-id="fe464-133">A number</span></span>| <span data-ttu-id="fe464-134">Hvis automatiske adresseforslag er aktivert, kan du angi flere alternativer, for eksempel maksimalt antall forslag som skal gis.</span><span class="sxs-lookup"><span data-stu-id="fe464-134">If automatic address suggestions are enabled, you can specify additional options, such as the maximum number of suggestions that should be provided.</span></span>|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="fe464-135">Legge til en leveringsadressemodul på en kasseside og angi de nødvendige egenskapene</span><span class="sxs-lookup"><span data-stu-id="fe464-135">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="fe464-136">En leveringsadressemodul kan bare legges til i en kassemodul.</span><span class="sxs-lookup"><span data-stu-id="fe464-136">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="fe464-137">Hvis du vil ha mer informasjon om hvordan du konfigurerer leveringsadressemodulen og legger den til på en kasseside, se [Kassemodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="fe464-137">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe464-138">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="fe464-138">Additional resources</span></span>

[<span data-ttu-id="fe464-139">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="fe464-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="fe464-140">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="fe464-140">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="fe464-141">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="fe464-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fe464-142">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="fe464-142">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="fe464-143">Leveringsalternativmodul</span><span class="sxs-lookup"><span data-stu-id="fe464-143">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="fe464-144">Hente informasjonsmodul</span><span class="sxs-lookup"><span data-stu-id="fe464-144">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="fe464-145">Modul for ordredetaljer</span><span class="sxs-lookup"><span data-stu-id="fe464-145">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="fe464-146">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="fe464-146">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="fe464-147">Butikkvelgermodul</span><span class="sxs-lookup"><span data-stu-id="fe464-147">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]