---
title: Handlekurvmodul
description: Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: abb9909c03577763ff7e6242c9395a58159df6ca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985985"
---
# <a name="cart-module"></a><span data-ttu-id="3e7ff-103">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="3e7ff-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3e7ff-104">Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3e7ff-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="3e7ff-105">Overview</span></span>

<span data-ttu-id="3e7ff-106">En handlekurvmodul viser varene som er lagt til i handlekurven før kunden går videre til kassen.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="3e7ff-107">Modulen viser også et ordresammendrag som lar kunden bruke eller fjerne kampanjekoder.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="3e7ff-108">Handlekurvmodulen støtter pålogget utsjekking og Sjekk ut som gjest.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="3e7ff-109">Den støtter også koblingen **Tilbake til shopping**.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="3e7ff-110">Du kan konfigurere ruten for denne koblingen under **Områdeinnstillinger \> Utvidelser \> Ruter**.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="3e7ff-111">Handlekurvmodulen gjengir data basert på handlekurv-IDen, som er en informasjonskapsel i leseren som er tilgjengelig i hele området.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="3e7ff-112">Bildet nedenfor viser et eksempel på en handlekurvside på Fabrikam-området.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Eksempel på en handlekurvmodul på Fabrikam-området](./media/cart2.PNG)

<span data-ttu-id="3e7ff-114">Bildet nedenfor viser et eksempel på en handlekurvside på Fabrikam-området.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="3e7ff-115">I dette eksemplet er det et behandlingsgebyr for en linjevare.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-115">In this example, there is a handling fee for a line item.</span></span>

![Eksempel på en handlekurvmodul med et behandlingsgebyr for et linjeelement](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="3e7ff-117">Egenskaper og spor for handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="3e7ff-117">Cart module properties and slots</span></span>

| <span data-ttu-id="3e7ff-118">Egenskap</span><span class="sxs-lookup"><span data-stu-id="3e7ff-118">Property</span></span> | <span data-ttu-id="3e7ff-119">Verdier</span><span class="sxs-lookup"><span data-stu-id="3e7ff-119">Values</span></span> | <span data-ttu-id="3e7ff-120">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="3e7ff-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="3e7ff-121">Overskrift</span><span class="sxs-lookup"><span data-stu-id="3e7ff-121">Heading</span></span> | <span data-ttu-id="3e7ff-122">Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="3e7ff-122">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="3e7ff-123">En overskrift for handlekurven, for eksempel "Handlepose" eller "Varer i handlekurven".</span><span class="sxs-lookup"><span data-stu-id="3e7ff-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="3e7ff-124">Vis feil for utsolgte varer</span><span class="sxs-lookup"><span data-stu-id="3e7ff-124">Show out of stock errors</span></span> | <span data-ttu-id="3e7ff-125">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="3e7ff-125">**True** or **False**</span></span> | <span data-ttu-id="3e7ff-126">Hvis denne egenskapen er satt til **Sann**, viser handlekurvsiden lagerrelaterte feil.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-126">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="3e7ff-127">Vi anbefaler at du setter denne egenskapen til **Sann** hvis det brukes beholdningskontroller på stedet.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="3e7ff-128">Vis forsendelseskostnader for linjevarer</span><span class="sxs-lookup"><span data-stu-id="3e7ff-128">Show shipping charges for line items</span></span> | <span data-ttu-id="3e7ff-129">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="3e7ff-129">**True** or **False**</span></span> | <span data-ttu-id="3e7ff-130">Hvis denne egenskapen er satt til **Sann**, viser handlekurvlinjer forsendelseskostnadene, hvis denne informasjonen er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-130">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="3e7ff-131">Denne funksjonen støttes ikke i Fabrikam-temaet fordi brukere velger bare levering i kasseflyten.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="3e7ff-132">Denne funksjonen kan imidlertid aktiveres i andre arbeidsflyter hvis den gjelder.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |
| <span data-ttu-id="3e7ff-133">Vis tilgjengelige kampanjer</span><span class="sxs-lookup"><span data-stu-id="3e7ff-133">Show available promotions</span></span>| <span data-ttu-id="3e7ff-134">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="3e7ff-134">**True** or **False**</span></span> | <span data-ttu-id="3e7ff-135">Hvis egenskapen er satt til **Sann**, viser handlekurven tilgjengelige kampanjer basert på varene i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-135">If this property is set to **True**, the cart shows available promotions, based on items in the cart.</span></span> <span data-ttu-id="3e7ff-136">Denne funksjonen er tilgjengelig i Dynamics 365 Commerce versjon 10.0.16.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-136">This capability is available in the Dynamics 365 Commerce 10.0.16 release.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="3e7ff-137">Moduler som kan brukes i handlekurvmodulen</span><span class="sxs-lookup"><span data-stu-id="3e7ff-137">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="3e7ff-138">**Tekstblokk** – Denne modulen støtter tilpassede meldinger i handlekurvmodulen.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-138">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="3e7ff-139">Meldingene drives av innholdsbehandlingssystemet (CMS).</span><span class="sxs-lookup"><span data-stu-id="3e7ff-139">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="3e7ff-140">Alle meldinger kan legges til, for eksempel "For problemer med ordren, kontakt 1-800-Fabrikam."</span><span class="sxs-lookup"><span data-stu-id="3e7ff-140">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="3e7ff-141">**Butikkvelger** – Denne modulen viser en liste over nærliggende butikker der en vare er tilgjengelig for henting.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-141">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="3e7ff-142">Den lar brukere angi en plassering for å finne butikker i nærheten.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-142">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="3e7ff-143">Hvis du vil ha mer informasjon om denne modulen, se [Butikkvelgermodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="3e7ff-143">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="3e7ff-144">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="3e7ff-144">Module properties</span></span>

<span data-ttu-id="3e7ff-145">Følgende innstillinger for handlevognmodulen kan konfigureres under **Områdeinnstillinger \> Utvidelser**:</span><span class="sxs-lookup"><span data-stu-id="3e7ff-145">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="3e7ff-146">**Maksimalt antall** – Denne egenskapen brukes til å angi maksimalt antall for hver vare som kan legges til i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-146">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="3e7ff-147">En forhandler kan for eksempel bestemme at bare 10 av hvert produkt kan selges i en enkelt transaksjon.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-147">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="3e7ff-148">**Beholdning** – Hvis du vil ha informasjon om hvordan du bruker beholdningsinnstillinger, kan du se [Bruk beholdningsinnstillinger](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="3e7ff-148">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="3e7ff-149">**Tilbake til shopping** – Denne egenskapen brukes til å angi ruten for **Tilbake til shopping**-koblingen.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-149">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="3e7ff-150">Ruten kan konfigureres på områdenivå, slik at forhandlere kan bringe kunden tilbake til hjemmesiden eller en hvilken som helst annen side på området.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-150">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e7ff-151">I Dynamics 365 Commerce 10.0.14 versjonen og senere samles varer i handlekurven basert på innstillingene som er definert i den elektroniske funksjonalitetsprofilen for nettbutikken i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-151">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="3e7ff-152">Hvis du vil ha mer informasjon om hvordan du oppretter en nettbasert funksjonalitetsprofil og angir egenskapene som kreves for aggregering, kan du se [Opprette en nettbasert funksjonalitetsprofil](online-functionality-profile.md).</span><span class="sxs-lookup"><span data-stu-id="3e7ff-152">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="3e7ff-153">Samhandling med Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="3e7ff-153">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="3e7ff-154">Handlekurvmodulen henter produktinformasjon ved hjelp av API-er for Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-154">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="3e7ff-155">Handlekurv-IDen fra leserinformasjonskapselen brukes til å hente all produktinformasjon fra Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-155">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="3e7ff-156">Legge til en handlekurvmodul på en side</span><span class="sxs-lookup"><span data-stu-id="3e7ff-156">Add a cart module to a page</span></span>

<span data-ttu-id="3e7ff-157">Hvis du vil legge til en handlekurvmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-157">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="3e7ff-158">Gå til **Fragmenter**, og velg **Nytt** for å opprette et nytt sidefragment.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-158">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="3e7ff-159">I dialogboksen **Nytt fragment** velger du **Handlekurv**-modulen.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-159">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="3e7ff-160">Under **Navn på fragment** angir du navnet **Handlevognfragment**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-160">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="3e7ff-161">Velg **Handlevogn**-sporet.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-161">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="3e7ff-162">I egenskapsruten til høyre velger du blyantsymbolet, angir overskriftsteksten i feltet, og merker av for avmerkingssymbolet.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-162">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="3e7ff-163">I **Handlevogn**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-163">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3e7ff-164">I dialogboksen **Legg til modul** velger du **Butikkvelger**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-164">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3e7ff-165">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-165">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="3e7ff-166">Gå til **Maler**, og velg **Ny** for å opprette en ny mal.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-166">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="3e7ff-167">I dialogboksen **Ny mal**, under **Malnavn**, angir du et navn på malen.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-167">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="3e7ff-168">Velg **Brødtekst**-sporet i disposisjonstreet, velg ellipseknappen (**…**), og velg deretter **Legg til fragment**.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-168">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="3e7ff-169">I dialogboksen **Velg fragment** velger du **Handlevognfragmentet**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-169">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="3e7ff-170">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-170">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="3e7ff-171">Gå til **Sider**, og velg **Ny** for å opprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-171">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="3e7ff-172">I dialogboksen **Velg en mal** velger du malen du opprettet, angir et sidenavn, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-172">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="3e7ff-173">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-173">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="3e7ff-174">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-174">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e7ff-175">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="3e7ff-175">Additional resources</span></span>

[<span data-ttu-id="3e7ff-176">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="3e7ff-176">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="3e7ff-177">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="3e7ff-177">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="3e7ff-178">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="3e7ff-178">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="3e7ff-179">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="3e7ff-179">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="3e7ff-180">Leveringsalternativmodul</span><span class="sxs-lookup"><span data-stu-id="3e7ff-180">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="3e7ff-181">Henteinformasjonsmodul</span><span class="sxs-lookup"><span data-stu-id="3e7ff-181">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="3e7ff-182">Ordredetaljermodul</span><span class="sxs-lookup"><span data-stu-id="3e7ff-182">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="3e7ff-183">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="3e7ff-183">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="3e7ff-184">Beregne lagertilgjengelighet for detaljhandelskanaler</span><span class="sxs-lookup"><span data-stu-id="3e7ff-184">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="3e7ff-185">Opprette en nettbasert funksjonalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="3e7ff-185">Create an online functionality profile</span></span>](online-functionality-profile.md)
