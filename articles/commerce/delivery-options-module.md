---
title: Modul for leveringsalternativer
description: Dette emnet dekker moduler for leveringsalternativer og forklarer hvordan du konfigurerer dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 8342afefa6eeda3a53decb39caddb62d1e4e1963
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270867"
---
# <a name="delivery-options-module"></a><span data-ttu-id="5dda2-103">Leveringsalternativmodul</span><span class="sxs-lookup"><span data-stu-id="5dda2-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5dda2-104">Dette emnet dekker moduler for leveringsalternativer og forklarer hvordan du konfigurerer dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5dda2-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5dda2-105">Med moduler for leveringsalternativer kan kunder velge en leveringsmodus, for eksempel forsendelse eller henting for bestillinger på nettet.</span><span class="sxs-lookup"><span data-stu-id="5dda2-105">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="5dda2-106">Det kreves en forsendelsesadresse for å bestemme leveringsmåten.</span><span class="sxs-lookup"><span data-stu-id="5dda2-106">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="5dda2-107">Hvis leveringsadressen endres, må leveringsalternativene hentes på nytt.</span><span class="sxs-lookup"><span data-stu-id="5dda2-107">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="5dda2-108">Hvis en ordre bare omfatter varer som skal plukkes i en butikk, blir denne modulen automatisk skjult.</span><span class="sxs-lookup"><span data-stu-id="5dda2-108">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="5dda2-109">Hvis du vil ha informasjon om hvordan du konfigurerer leveringsmoduser, kan du se [Konfigurasjon av Internett-kanal](channel-setup-online.md) og [Definere leveringsmåter](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="5dda2-109">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="5dda2-110">Hver leveringsmodus kan ha et tilknyttet gebyr.</span><span class="sxs-lookup"><span data-stu-id="5dda2-110">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="5dda2-111">Hvis du vil ha mer informasjon om hvordan du konfigurerer gebyrer for en nettbutikk, kan du se [Avanserte automatiske gebyrer for omnikanal](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="5dda2-111">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="5dda2-112">I Commerce versjon 10.0.13 er modulen for leveringsalternativer oppdatert for å støtte funksjonene **Hodegebyrer uten fordeling** og **Levering som et linjegebyr**.</span><span class="sxs-lookup"><span data-stu-id="5dda2-112">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="5dda2-113">Hvis fordeling er deaktivert, er forventningen at arbeidsflyten for e-handel ikke tillater en blandet leveringsmodus for varene i handlekurven (det vil si at noen varer er valgt for forsendelse, men andre er valgt for henting).</span><span class="sxs-lookup"><span data-stu-id="5dda2-113">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="5dda2-114">Funksjonen **Hodegebyrer uten fordeling** krever at flagget **Aktiver konsekvent behandling av leveringsmodus i kanal** er aktivert i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="5dda2-114">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag is turned on in Commerce headquarters.</span></span> <span data-ttu-id="5dda2-115">Når funksjonsflagget er aktivert, brukes forsendelsesgebyrer på hodenivå eller linjenivå, avhengig av konfigurasjonen i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="5dda2-115">When the feature flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="5dda2-116">Oppsettet fra Fabrikam støtter en blandet leveringsmodus, der noen varer er valgt for forsendelse, men andre velges for plukking.</span><span class="sxs-lookup"><span data-stu-id="5dda2-116">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="5dda2-117">I denne modusen blir forsendelsesgebyrer fordelt for alle varer som er valgt i leveringsmåten ved levering.</span><span class="sxs-lookup"><span data-stu-id="5dda2-117">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="5dda2-118">For at en blandet leveringsmodus skal fungere, må du først konfigurere funksjonen **Hodegebyrer med fordeling** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="5dda2-118">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="5dda2-119">Hvis du vil ha mer informasjon om denne konfigurasjonen, se [Fordele hodegebyrer for å matche salgslinjer](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="5dda2-119">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="5dda2-120">Hvis forsendelsesgebyrer gjelder for linjevarer, kan de vises på handlekurvlinjen for hver vare.</span><span class="sxs-lookup"><span data-stu-id="5dda2-120">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="5dda2-121">Denne funksjonaliteten krever at egenskapen **Vis forsendelseskostnader for linjevare** er aktivert for både handlekurv- og kassemodulen.</span><span class="sxs-lookup"><span data-stu-id="5dda2-121">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="5dda2-122">Hvis du vil ha mer informasjon, kan du se [Handlekurvmodul](add-cart-module.md) og [Kassemodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="5dda2-122">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="5dda2-123">Illustrasjonen nedenfor viser et eksempel på en leveringsalternativer-modul på en kasseside.</span><span class="sxs-lookup"><span data-stu-id="5dda2-123">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Eksempel på en modul for leveringsalternativer på en kasseside](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="5dda2-125">Egenskaper for modul for leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="5dda2-125">Delivery options module properties</span></span>

| <span data-ttu-id="5dda2-126">Egenskap</span><span class="sxs-lookup"><span data-stu-id="5dda2-126">Property</span></span> | <span data-ttu-id="5dda2-127">Verdier</span><span class="sxs-lookup"><span data-stu-id="5dda2-127">Values</span></span> | <span data-ttu-id="5dda2-128">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5dda2-128">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="5dda2-129">Overskrift</span><span class="sxs-lookup"><span data-stu-id="5dda2-129">Heading</span></span> | <span data-ttu-id="5dda2-130">Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="5dda2-130">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="5dda2-131">En valgfri overskrift for modulen for leveringsalternativer.</span><span class="sxs-lookup"><span data-stu-id="5dda2-131">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="5dda2-132">Egendefinert CSS-klassenavn</span><span class="sxs-lookup"><span data-stu-id="5dda2-132">Custom CSS class name</span></span> | <span data-ttu-id="5dda2-133">Tekst</span><span class="sxs-lookup"><span data-stu-id="5dda2-133">Text</span></span> | <span data-ttu-id="5dda2-134">Et egendefinert CSS-klassenavn (gjennomgripende stilark) som skal brukes til å gjengi denne modulen, hvis tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="5dda2-134">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="5dda2-135">Alternativ for leveringsmåte for filter</span><span class="sxs-lookup"><span data-stu-id="5dda2-135">Filter Delivery Mode Option</span></span> | <span data-ttu-id="5dda2-136">**Ikke filtrer** eller **Ikke-leveringsmoduser**</span><span class="sxs-lookup"><span data-stu-id="5dda2-136">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="5dda2-137">En verdi som angir om modulen for leveringsalternativer skal filtrere ut alle leveringsmoduser som ikke er forsendelse.</span><span class="sxs-lookup"><span data-stu-id="5dda2-137">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |
| <span data-ttu-id="5dda2-138">Velge et leveringsalternativ automatisk</span><span class="sxs-lookup"><span data-stu-id="5dda2-138">Auto select a delivery option</span></span> | <span data-ttu-id="5dda2-139">**Ikke filtrer**, **Velg leveringsalternativ automatisk og vis sammendrag** eller **Velg leveringsalternativ automatisk og ikke vis sammendrag**</span><span class="sxs-lookup"><span data-stu-id="5dda2-139">**Do not filter**, **Auto select delivery option and show summary**, or **Auto select delivery option and don't show summary**</span></span> | <span data-ttu-id="5dda2-140">Denne egenskapen bruker automatisk det første tilgjengelige leveringsalternativet til kassen, uten at brukeren behøver å velge det.</span><span class="sxs-lookup"><span data-stu-id="5dda2-140">This property automatically applies the first available delivery option to checkout without requiring the user to select it.</span></span> <span data-ttu-id="5dda2-141">Det bør bare brukes hvis det er ett tilgjengelig leveringsalternativ.</span><span class="sxs-lookup"><span data-stu-id="5dda2-141">It should be used only if there is one available delivery option.</span></span> <span data-ttu-id="5dda2-142">Denne egenskapen støttes fra og med Commerce versjon 10.0.19-utgivelsen.</span><span class="sxs-lookup"><span data-stu-id="5dda2-142">This property is supported as of the Commerce version 10.0.19 release.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="5dda2-143">Legge til en modul for leveringsalternativer på en kasseside og angi de nødvendige egenskapene</span><span class="sxs-lookup"><span data-stu-id="5dda2-143">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="5dda2-144">En modul for leveringsalternativer kan bare legges til i en kassemodul.</span><span class="sxs-lookup"><span data-stu-id="5dda2-144">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="5dda2-145">Hvis du vil ha mer informasjon om hvordan du konfigurerer modulen for leveringsalternativer og legger den til på en kasseside, se [Kassemodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="5dda2-145">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5dda2-146">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5dda2-146">Additional resources</span></span>

[<span data-ttu-id="5dda2-147">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="5dda2-147">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5dda2-148">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="5dda2-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="5dda2-149">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="5dda2-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="5dda2-150">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="5dda2-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="5dda2-151">Henteinformasjonsmodul</span><span class="sxs-lookup"><span data-stu-id="5dda2-151">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="5dda2-152">Ordredetaljermodul</span><span class="sxs-lookup"><span data-stu-id="5dda2-152">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="5dda2-153">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="5dda2-153">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="5dda2-154">Oppsett av nettkanal</span><span class="sxs-lookup"><span data-stu-id="5dda2-154">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="5dda2-155">Avanserte automatiske tillegg for omnikanal</span><span class="sxs-lookup"><span data-stu-id="5dda2-155">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="5dda2-156">Fordele hodegebyrer for å matche salgslinjer</span><span class="sxs-lookup"><span data-stu-id="5dda2-156">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="5dda2-157">Definer leveringsmåter</span><span class="sxs-lookup"><span data-stu-id="5dda2-157">Set up modes of delivery</span></span>](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
