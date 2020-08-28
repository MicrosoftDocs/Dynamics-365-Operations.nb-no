---
title: Betalingsmodul
description: Dette emnet dekker betalingsmodulen og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: f4f6baa3c4a42a2994cab772c98d373996e2648b
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661219"
---
# <a name="payment-module"></a><span data-ttu-id="84d78-103">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="84d78-103">Payment module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="84d78-104">Dette emnet dekker betalingsmodulen og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="84d78-104">This topic covers the payment module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="84d78-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="84d78-105">Overview</span></span>

<span data-ttu-id="84d78-106">Betalingsmodulen lar kunder betale for ordrer ved å bruke et kredittkort eller et debetkort.</span><span class="sxs-lookup"><span data-stu-id="84d78-106">The payment module lets customers pay for orders by using credit or debit cards.</span></span> <span data-ttu-id="84d78-107">Betalingsintegrasjon for denne modulen leveres av Dynamics 365-betalingskoblingen for Adyen.</span><span class="sxs-lookup"><span data-stu-id="84d78-107">Payment integration for this module is provided by the Dynamics 365 Payment Connector for Adyen.</span></span> <span data-ttu-id="84d78-108">Hvis du vil ha mer informasjon om hvordan du setter opp og konfigurerer betalingskoblingen, kan du se [Adyen-betalingskobling i Dynamics 365](dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="84d78-108">For more information about how to set up and configure the payment connector, see [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).</span></span>

<span data-ttu-id="84d78-109">Betalingsmodulen er vert for betalingsinformasjonen som leveres via Adyen i en HTML-innebygd ramme (iframe).</span><span class="sxs-lookup"><span data-stu-id="84d78-109">The payment module hosts the payment information that is served via Adyen in an HTML inline frame (iframe).</span></span> <span data-ttu-id="84d78-110">Betalingsmodulen fungerer sammen med Commerce Scale Unit for å hente Adyen-betalingsinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="84d78-110">The payment module interacts with the Commerce Scale Unit to retrieve the Adyen payment information.</span></span> <span data-ttu-id="84d78-111">Som en del av samhandlingen med Commerce Scale Unit kan betalingsmodulen tillate at informasjon om faktureringsadresse blir behandlet enten i iFrame eller som en separat modul.</span><span class="sxs-lookup"><span data-stu-id="84d78-111">As part of the Commerce Scale Unit interaction, the payment module can allow billing address information to be served either in the iframe or as a separate module.</span></span> <span data-ttu-id="84d78-112">I Fabrikam-temaet vises faktureringsadressen i en egen modul.</span><span class="sxs-lookup"><span data-stu-id="84d78-112">In the Fabrikam theme, the billing address is shown in a separate module.</span></span> <span data-ttu-id="84d78-113">Denne fremgangsmåten gjør at du får mer fleksibilitet i formateringen, fordi adresselinjene kan gjengis slik at de ligner på linjene i leveringsadressen.</span><span class="sxs-lookup"><span data-stu-id="84d78-113">This approach allows for more formatting flexibility, because the address lines can be rendered so that they resemble the lines of the shipping address.</span></span>

<span data-ttu-id="84d78-114">Betalingsmodulen lar også de påloggede kundene lagre betalingsinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="84d78-114">The payment module also lets signed-in customers save their payment information.</span></span> <span data-ttu-id="84d78-115">Betalingsinformasjonen og faktureringsadressen lagres og administreres via Adyen-betalingskoblingen.</span><span class="sxs-lookup"><span data-stu-id="84d78-115">The payment information and billing address are saved and managed via the Adyen payment connector.</span></span>

<span data-ttu-id="84d78-116">Betalingsmodulen dekker eventuelle ordretillegg som ikke allerede dekkes av fordelspoeng eller et gavekort.</span><span class="sxs-lookup"><span data-stu-id="84d78-116">The payment module covers any order charges that aren't already covered by loyalty points or a gift card.</span></span> <span data-ttu-id="84d78-117">Hvis totalen for en ordre er dekket av fordelspoeng eller gavekortkreditt, vil betalingsmodulen være skjult, og kunden kan plassere ordren uten den.</span><span class="sxs-lookup"><span data-stu-id="84d78-117">If the total for an order is fully covered by loyalty points or gift card credits, the payment module will be hidden, and the customer will be able to place the order without it.</span></span>

<span data-ttu-id="84d78-118">Adyen-betalingskoblingen støtter også sterk kundegodkjenning (SCA).</span><span class="sxs-lookup"><span data-stu-id="84d78-118">The Adyen payment connector also supports strong customer authentication (SCA).</span></span> <span data-ttu-id="84d78-119">En del av PSD-direktiv 2.0 (Payment Services Directive) i EU krever at netthandlere godkjennes utenfor den elektroniske handleopplevelsen når de bruker en elektronisk betalingsmetode.</span><span class="sxs-lookup"><span data-stu-id="84d78-119">Part of the European Union (EU) Payment Services Directive 2.0 (PSD2.0) requires that online shoppers be authenticated outside their online shopping experience when they use an electronic payment method.</span></span> <span data-ttu-id="84d78-120">Under betalingsflyten blir kunder omadressert til banknettstedet.</span><span class="sxs-lookup"><span data-stu-id="84d78-120">During the checkout flow,  customers are redirected to their banking site.</span></span> <span data-ttu-id="84d78-121">Etter godkjenning omadresseres de deretter tilbake til Commerce-betalingsflyten.</span><span class="sxs-lookup"><span data-stu-id="84d78-121">Then, after authentication, they are redirected back to the Commerce checkout flow.</span></span> <span data-ttu-id="84d78-122">Under denne omadresseringen vil informasjonen som en kunde har angitt i betalingsflyten (for eksempel leveringsadresse, leveringsalternativer, informasjon om gavekort og fordelsinformasjon), beholdes.</span><span class="sxs-lookup"><span data-stu-id="84d78-122">During this redirection, the information that a customer entered in the checkout flow (for example, the shipping address, delivery options, gift card information, and loyalty information) will persist.</span></span> <span data-ttu-id="84d78-123">Før du kan aktivere denne funksjonen, må betalingskoblingen være konfigurert for SCA i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="84d78-123">Before you can turn on this feature, the payment connector must be configured for SCA in Commerce headquarters.</span></span> <span data-ttu-id="84d78-124">Hvis du vil ha mer informasjon, kan du se [Sterk kundegodkjenning ved hjelp av Adyen](adyen_redirect.md).</span><span class="sxs-lookup"><span data-stu-id="84d78-124">For more information, see [Strong Customer Authentication using Adyen](adyen_redirect.md).</span></span>

<span data-ttu-id="84d78-125">Følgende illustrasjon viser et eksempel på en gavekort-, fordels- og betalingsmodul på en kasseside.</span><span class="sxs-lookup"><span data-stu-id="84d78-125">The following illustration shows an example of gift card, loyalty, and payment modules on a checkout page.</span></span>

![Eksempel på en gavekort-, fordels- og betalingsmodul på en kasseside](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a><span data-ttu-id="84d78-127">Egenskaper for betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="84d78-127">Payment module properties</span></span>

| <span data-ttu-id="84d78-128">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="84d78-128">Property name</span></span> | <span data-ttu-id="84d78-129">Verdier</span><span class="sxs-lookup"><span data-stu-id="84d78-129">Values</span></span> | <span data-ttu-id="84d78-130">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="84d78-130">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="84d78-131">Overskrift</span><span class="sxs-lookup"><span data-stu-id="84d78-131">Heading</span></span> | <span data-ttu-id="84d78-132">Overskriftstekst</span><span class="sxs-lookup"><span data-stu-id="84d78-132">Heading text</span></span> | <span data-ttu-id="84d78-133">En valgfri overskrift for betalingsmodulen.</span><span class="sxs-lookup"><span data-stu-id="84d78-133">An optional heading for the payment module.</span></span> |
| <span data-ttu-id="84d78-134">Høyden på iFrame</span><span class="sxs-lookup"><span data-stu-id="84d78-134">Height of the iframe</span></span> | <span data-ttu-id="84d78-135">Piksler</span><span class="sxs-lookup"><span data-stu-id="84d78-135">Pixels</span></span> | <span data-ttu-id="84d78-136">IFrame-høyden, i piksler.</span><span class="sxs-lookup"><span data-stu-id="84d78-136">The iframe height, in pixels.</span></span> <span data-ttu-id="84d78-137">Høyden kan imidlertid justeres etter behov.</span><span class="sxs-lookup"><span data-stu-id="84d78-137">The height can be adjusted as required.</span></span> |
| <span data-ttu-id="84d78-138">Vis faktureringsadresse</span><span class="sxs-lookup"><span data-stu-id="84d78-138">Show billing address</span></span> | <span data-ttu-id="84d78-139">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="84d78-139">**True** or **False**</span></span> | <span data-ttu-id="84d78-140">Hvis denne egenskapen er satt til **Sann**, vil faktureringsadressen bli betjent av Adyen inne i betalingsmodulen iFrame.</span><span class="sxs-lookup"><span data-stu-id="84d78-140">If this property is set to **True**, the billing address will be served by Adyen inside the payment module iframe.</span></span> <span data-ttu-id="84d78-141">Hvis den er satt til **Usann**, blir faktureringsadressen ikke betjent av Adyen, og en Commerce-bruker må konfigurere en modul til å vise faktureringsadressen på betalingssiden.</span><span class="sxs-lookup"><span data-stu-id="84d78-141">If it's set to **False**, the billing address won't be served by Adyen, and a Commerce user will have to configure a module to show the billing address on the checkout page.</span></span> |
| <span data-ttu-id="84d78-142">Overstyring av betalingsstil</span><span class="sxs-lookup"><span data-stu-id="84d78-142">Payment style override</span></span> | <span data-ttu-id="84d78-143">CSS-kode (gjennomgripende stilark)</span><span class="sxs-lookup"><span data-stu-id="84d78-143">Cascading Style Sheets (CSS) code</span></span> | <span data-ttu-id="84d78-144">Fordi betalingsmodulen ligger i en iFrame, er det begrenset stilfunksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="84d78-144">Because the payment module is hosted in an iframe, there is limited styling capability.</span></span> <span data-ttu-id="84d78-145">Du kan oppnå en viss stil ved hjelp av denne egenskapen.</span><span class="sxs-lookup"><span data-stu-id="84d78-145">You can achieve some styling by using this property.</span></span> <span data-ttu-id="84d78-146">Hvis du vil overstyre områdestiler, må du lime inn CSS-koden som verdien for denne egenskapen.</span><span class="sxs-lookup"><span data-stu-id="84d78-146">To override site styles, you must paste the CSS code as the value of this property.</span></span> <span data-ttu-id="84d78-147">Områdebygger for CSS overstyrer dette, og stiler gjelder ikke for denne modulen.</span><span class="sxs-lookup"><span data-stu-id="84d78-147">Site builder CSS overrides and styles don't apply to this module.</span></span> |

## <a name="billing-address"></a><span data-ttu-id="84d78-148">Faktureringsadresse</span><span class="sxs-lookup"><span data-stu-id="84d78-148">Billing address</span></span>

<span data-ttu-id="84d78-149">I betalingsmodulen kan kundene oppgi en faktureringsadresse for betalingsinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="84d78-149">The payment module lets customers provide a billing address for their payment information.</span></span> <span data-ttu-id="84d78-150">I tillegg kan de bruke leveringsadressen som faktureringsadresse, slik at betalingsflyten blir enklere og raskere.</span><span class="sxs-lookup"><span data-stu-id="84d78-150">It also lets them  use their shipping address as the billing address, to make the checkout flow easier and faster.</span></span> <span data-ttu-id="84d78-151">Hvis egenskapen **Vis faktureringsadresse** er satt til **Usann**, må betalingsmodulen konfigureres på betalingssiden.</span><span class="sxs-lookup"><span data-stu-id="84d78-151">If the **Show billing address** property is set to **False**, the payment module should be configured on the checkout page.</span></span>

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="84d78-152">Legge til en betalingsmodul på en kasseside og angi de nødvendige egenskapene</span><span class="sxs-lookup"><span data-stu-id="84d78-152">Add a payment module to a checkout page and set the required properties</span></span>

<span data-ttu-id="84d78-153">En betalingsmodul kan bare legges til i en kassemodul.</span><span class="sxs-lookup"><span data-stu-id="84d78-153">A payment module can be added only to a checkout module.</span></span> <span data-ttu-id="84d78-154">Hvis du vil ha mer informasjon om hvordan du konfigurerer en betalingsmodul for en kasseside, se [Kassemodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="84d78-154">For more information about how to configure a payment module for a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="84d78-155">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="84d78-155">Additional resources</span></span>

[<span data-ttu-id="84d78-156">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="84d78-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="84d78-157">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="84d78-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="84d78-158">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="84d78-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="84d78-159">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="84d78-159">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="84d78-160">Modul for leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="84d78-160">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="84d78-161">Ordredetaljermodul</span><span class="sxs-lookup"><span data-stu-id="84d78-161">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="84d78-162">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="84d78-162">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="84d78-163">Dynamics 365 Payment Connector for Adyen</span><span class="sxs-lookup"><span data-stu-id="84d78-163">Dynamics 365 Payment Connector for Adyen</span></span>](dev-itpro/adyen-connector.md)

[<span data-ttu-id="84d78-164">Sterk kundegodkjenning ved hjelp av Adyen</span><span class="sxs-lookup"><span data-stu-id="84d78-164">Strong Customer Authentication using Adyen</span></span>](adyen_redirect.md)
