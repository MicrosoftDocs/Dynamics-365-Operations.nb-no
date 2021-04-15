---
title: Handlekurvmodul
description: Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ec8e89ed82bcdffdc21e62d24ad8c8a7d939cdf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797869"
---
# <a name="cart-module"></a><span data-ttu-id="32435-103">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="32435-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="32435-104">Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="32435-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="32435-105">En handlekurvmodul viser varene som er lagt til i handlekurven før kunden går videre til kassen.</span><span class="sxs-lookup"><span data-stu-id="32435-105">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="32435-106">Modulen viser også et ordresammendrag som lar kunden bruke eller fjerne kampanjekoder.</span><span class="sxs-lookup"><span data-stu-id="32435-106">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="32435-107">Handlekurvmodulen støtter pålogget utsjekking og Sjekk ut som gjest.</span><span class="sxs-lookup"><span data-stu-id="32435-107">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="32435-108">Den støtter også koblingen **Tilbake til shopping**.</span><span class="sxs-lookup"><span data-stu-id="32435-108">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="32435-109">Du kan konfigurere ruten for denne koblingen under **Områdeinnstillinger \> Utvidelser \> Ruter**.</span><span class="sxs-lookup"><span data-stu-id="32435-109">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="32435-110">Handlekurvmodulen gjengir data basert på handlekurv-IDen, som er en informasjonskapsel i leseren som er tilgjengelig i hele området.</span><span class="sxs-lookup"><span data-stu-id="32435-110">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="32435-111">Bildet nedenfor viser et eksempel på en handlekurvside på Fabrikam-området.</span><span class="sxs-lookup"><span data-stu-id="32435-111">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Eksempel på en handlekurvmodul på Fabrikam-området](./media/cart2.PNG)

<span data-ttu-id="32435-113">Bildet nedenfor viser et eksempel på en handlekurvside på Fabrikam-området.</span><span class="sxs-lookup"><span data-stu-id="32435-113">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="32435-114">I dette eksemplet er det et behandlingsgebyr for en linjevare.</span><span class="sxs-lookup"><span data-stu-id="32435-114">In this example, there is a handling fee for a line item.</span></span>

![Eksempel på en handlekurvmodul med et behandlingsgebyr for et linjeelement](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="32435-116">Egenskaper og spor for handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="32435-116">Cart module properties and slots</span></span>

| <span data-ttu-id="32435-117">Egenskap</span><span class="sxs-lookup"><span data-stu-id="32435-117">Property</span></span> | <span data-ttu-id="32435-118">Verdier</span><span class="sxs-lookup"><span data-stu-id="32435-118">Values</span></span> | <span data-ttu-id="32435-119">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="32435-119">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="32435-120">Overskrift</span><span class="sxs-lookup"><span data-stu-id="32435-120">Heading</span></span> | <span data-ttu-id="32435-121">Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="32435-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="32435-122">En overskrift for handlekurven, for eksempel "Handlepose" eller "Varer i handlekurven".</span><span class="sxs-lookup"><span data-stu-id="32435-122">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="32435-123">Vis feil for utsolgte varer</span><span class="sxs-lookup"><span data-stu-id="32435-123">Show out of stock errors</span></span> | <span data-ttu-id="32435-124">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="32435-124">**True** or **False**</span></span> | <span data-ttu-id="32435-125">Hvis denne egenskapen er satt til **Sann**, viser handlekurvsiden lagerrelaterte feil.</span><span class="sxs-lookup"><span data-stu-id="32435-125">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="32435-126">Vi anbefaler at du setter denne egenskapen til **Sann** hvis det brukes beholdningskontroller på stedet.</span><span class="sxs-lookup"><span data-stu-id="32435-126">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="32435-127">Vis forsendelseskostnader for linjevarer</span><span class="sxs-lookup"><span data-stu-id="32435-127">Show shipping charges for line items</span></span> | <span data-ttu-id="32435-128">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="32435-128">**True** or **False**</span></span> | <span data-ttu-id="32435-129">Hvis denne egenskapen er satt til **Sann**, viser handlekurvlinjer forsendelseskostnadene, hvis denne informasjonen er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="32435-129">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="32435-130">Denne funksjonen støttes ikke i Fabrikam-temaet fordi brukere velger bare levering i kasseflyten.</span><span class="sxs-lookup"><span data-stu-id="32435-130">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="32435-131">Denne funksjonen kan imidlertid aktiveres i andre arbeidsflyter hvis den gjelder.</span><span class="sxs-lookup"><span data-stu-id="32435-131">However, this feature can be turned on in other workflows if it's applicable.</span></span> |
| <span data-ttu-id="32435-132">Vis tilgjengelige kampanjer</span><span class="sxs-lookup"><span data-stu-id="32435-132">Show available promotions</span></span>| <span data-ttu-id="32435-133">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="32435-133">**True** or **False**</span></span> | <span data-ttu-id="32435-134">Hvis egenskapen er satt til **Sann**, viser handlekurven tilgjengelige kampanjer basert på varene i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="32435-134">If this property is set to **True**, the cart shows available promotions, based on items in the cart.</span></span> <span data-ttu-id="32435-135">Denne funksjonen er tilgjengelig i Dynamics 365 Commerce versjon 10.0.16.</span><span class="sxs-lookup"><span data-stu-id="32435-135">This capability is available in the Dynamics 365 Commerce 10.0.16 release.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="32435-136">Moduler som kan brukes i handlekurvmodulen</span><span class="sxs-lookup"><span data-stu-id="32435-136">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="32435-137">**Tekstblokk** – Denne modulen støtter tilpassede meldinger i handlekurvmodulen.</span><span class="sxs-lookup"><span data-stu-id="32435-137">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="32435-138">Meldingene drives av innholdsbehandlingssystemet (CMS).</span><span class="sxs-lookup"><span data-stu-id="32435-138">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="32435-139">Alle meldinger kan legges til, for eksempel "For problemer med ordren, kontakt 1-800-Fabrikam."</span><span class="sxs-lookup"><span data-stu-id="32435-139">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="32435-140">**Butikkvelger** – Denne modulen viser en liste over nærliggende butikker der en vare er tilgjengelig for henting.</span><span class="sxs-lookup"><span data-stu-id="32435-140">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="32435-141">Den lar brukere angi en plassering for å finne butikker i nærheten.</span><span class="sxs-lookup"><span data-stu-id="32435-141">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="32435-142">Hvis du vil ha mer informasjon om denne modulen, se [Butikkvelgermodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="32435-142">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="32435-143">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="32435-143">Module properties</span></span>

<span data-ttu-id="32435-144">Følgende innstillinger for handlevognmodulen kan konfigureres under **Områdeinnstillinger \> Utvidelser**:</span><span class="sxs-lookup"><span data-stu-id="32435-144">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="32435-145">**Maksimalt antall** – Denne egenskapen brukes til å angi maksimalt antall for hver vare som kan legges til i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="32435-145">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="32435-146">En forhandler kan for eksempel bestemme at bare 10 av hvert produkt kan selges i en enkelt transaksjon.</span><span class="sxs-lookup"><span data-stu-id="32435-146">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="32435-147">**Beholdning** – Hvis du vil ha informasjon om hvordan du bruker beholdningsinnstillinger, kan du se [Bruk beholdningsinnstillinger](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="32435-147">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="32435-148">**Tilbake til shopping** – Denne egenskapen brukes til å angi ruten for **Tilbake til shopping**-koblingen.</span><span class="sxs-lookup"><span data-stu-id="32435-148">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="32435-149">Ruten kan konfigureres på områdenivå, slik at forhandlere kan bringe kunden tilbake til hjemmesiden eller en hvilken som helst annen side på området.</span><span class="sxs-lookup"><span data-stu-id="32435-149">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32435-150">I Dynamics 365 Commerce 10.0.14 versjonen og senere samles varer i handlekurven basert på innstillingene som er definert i den elektroniske funksjonalitetsprofilen for nettbutikken i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="32435-150">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="32435-151">Hvis du vil ha mer informasjon om hvordan du oppretter en nettbasert funksjonalitetsprofil og angir egenskapene som kreves for aggregering, kan du se [Opprette en nettbasert funksjonalitetsprofil](online-functionality-profile.md).</span><span class="sxs-lookup"><span data-stu-id="32435-151">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="32435-152">Samhandling med Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="32435-152">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="32435-153">Handlekurvmodulen henter produktinformasjon ved hjelp av API-er for Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="32435-153">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="32435-154">Handlekurv-IDen fra leserinformasjonskapselen brukes til å hente all produktinformasjon fra Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="32435-154">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="32435-155">Legge til en handlekurvmodul på en side</span><span class="sxs-lookup"><span data-stu-id="32435-155">Add a cart module to a page</span></span>

<span data-ttu-id="32435-156">Hvis du vil legge til en handlekurvmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="32435-156">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="32435-157">Gå til **Fragmenter**, og velg **Nytt** for å opprette et nytt sidefragment.</span><span class="sxs-lookup"><span data-stu-id="32435-157">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="32435-158">I dialogboksen **Nytt fragment** velger du **Handlekurv**-modulen.</span><span class="sxs-lookup"><span data-stu-id="32435-158">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="32435-159">Under **Navn på fragment** angir du navnet **Handlevognfragment**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="32435-159">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="32435-160">Velg **Handlevogn**-sporet.</span><span class="sxs-lookup"><span data-stu-id="32435-160">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="32435-161">I egenskapsruten til høyre velger du blyantsymbolet, angir overskriftsteksten i feltet, og merker av for avmerkingssymbolet.</span><span class="sxs-lookup"><span data-stu-id="32435-161">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="32435-162">I **Handlevogn**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="32435-162">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="32435-163">I dialogboksen **Legg til modul** velger du **Butikkvelger**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="32435-163">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="32435-164">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.</span><span class="sxs-lookup"><span data-stu-id="32435-164">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="32435-165">Gå til **Maler**, og velg **Ny** for å opprette en ny mal.</span><span class="sxs-lookup"><span data-stu-id="32435-165">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="32435-166">I dialogboksen **Ny mal**, under **Malnavn**, angir du et navn på malen.</span><span class="sxs-lookup"><span data-stu-id="32435-166">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="32435-167">Velg **Brødtekst**-sporet i disposisjonstreet, velg ellipseknappen (**…**), og velg deretter **Legg til fragment**.</span><span class="sxs-lookup"><span data-stu-id="32435-167">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="32435-168">I dialogboksen **Velg fragment** velger du **Handlevognfragmentet**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="32435-168">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="32435-169">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="32435-169">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="32435-170">Gå til **Sider**, og velg **Ny** for å opprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="32435-170">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="32435-171">I dialogboksen **Velg en mal** velger du malen du opprettet, angir et sidenavn, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="32435-171">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="32435-172">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="32435-172">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="32435-173">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="32435-173">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32435-174">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="32435-174">Additional resources</span></span>

[<span data-ttu-id="32435-175">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="32435-175">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="32435-176">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="32435-176">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="32435-177">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="32435-177">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="32435-178">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="32435-178">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="32435-179">Leveringsalternativmodul</span><span class="sxs-lookup"><span data-stu-id="32435-179">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="32435-180">Henteinformasjonsmodul</span><span class="sxs-lookup"><span data-stu-id="32435-180">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="32435-181">Ordredetaljermodul</span><span class="sxs-lookup"><span data-stu-id="32435-181">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="32435-182">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="32435-182">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="32435-183">Beregne lagertilgjengelighet for detaljhandelskanaler</span><span class="sxs-lookup"><span data-stu-id="32435-183">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="32435-184">Opprette en nettbasert funksjonalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="32435-184">Create an online functionality profile</span></span>](online-functionality-profile.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]