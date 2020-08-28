---
title: Kjøpsboksmodul
description: Dette emnet dekker kjøpsboksmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3fe5c1eb5808ef778aeda29442fa884556671296
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686676"
---
# <a name="buy-box-module"></a><span data-ttu-id="aad2a-103">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="aad2a-103">Buy box module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="aad2a-104">Dette emnet dekker kjøpsboksmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="aad2a-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="aad2a-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="aad2a-105">Overview</span></span>

<span data-ttu-id="aad2a-106">Begrepet *kjøpsboks* refererer vanligvis til området på en produktdetaljside som er "over folden", og som er vert for all viktig informasjon som kreves for å opprette et produktinnkjøp.</span><span class="sxs-lookup"><span data-stu-id="aad2a-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="aad2a-107">(Et område som er "over folden", er synlig når siden lastes inn for første gang, slik at brukere ikke behøver å rulle ned for å se det.)</span><span class="sxs-lookup"><span data-stu-id="aad2a-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="aad2a-108">En kjøpsboks-modul er en spesiell container som brukes til å være vert for alle modulene som vises i innkjøpsboksområdet på en side i produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="aad2a-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="aad2a-109">URL-adressen til en produktdetaljside inneholder produkt-IDen.</span><span class="sxs-lookup"><span data-stu-id="aad2a-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="aad2a-110">All informasjon som kreves for å vise en kjøpsboksmodul, er avledet fra denne produkt-IDen.</span><span class="sxs-lookup"><span data-stu-id="aad2a-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="aad2a-111">Hvis det ikke er angitt noen produkt-ID, vil ikke modulen kjøpsboks vises riktig på en side.</span><span class="sxs-lookup"><span data-stu-id="aad2a-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="aad2a-112">Derfor kan en kjøpsboksmodul bare brukes på sider som har produktkontekst.</span><span class="sxs-lookup"><span data-stu-id="aad2a-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="aad2a-113">Hvis du vil bruke den på en side som ikke har produktkontekst (for eksempel en startside eller en markedsføringsside), må du gjøre flere tilpasninger.</span><span class="sxs-lookup"><span data-stu-id="aad2a-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

<span data-ttu-id="aad2a-114">Bildet nedenfor viser et eksempel på en kjøpsboks-modul på en side med produktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="aad2a-114">The following image shows an example of a buy box module on a product details page.</span></span>

![Eksempel på en kjøpsboks-modul](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="aad2a-116">Egenskaper og spor for kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="aad2a-116">Buy box module properties and slots</span></span> 

<span data-ttu-id="aad2a-117">På en produktdetaljside er en kjøpsboks delt inn i to områder: et medieområde til venstre og et innholdsområde til høyre.</span><span class="sxs-lookup"><span data-stu-id="aad2a-117">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="aad2a-118">Som standard er forholdet mellom bredden på medieområdekolonnen og bredden på innholdsområdekolonnen 2:1.</span><span class="sxs-lookup"><span data-stu-id="aad2a-118">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="aad2a-119">På mobilenheter er det stablet to områder, slik at ett område vises under det andre området.</span><span class="sxs-lookup"><span data-stu-id="aad2a-119">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="aad2a-120">Temaer kan brukes til å tilpasse kolonnebreddene og stablet rangering.</span><span class="sxs-lookup"><span data-stu-id="aad2a-120">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="aad2a-121">En kjøpsboksmodul gjengir tittel, beskrivelse, pris og vurdering av et produkt.</span><span class="sxs-lookup"><span data-stu-id="aad2a-121">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="aad2a-122">Den lar også kunder velge produktvarianter som har forskjellige produktattributter, for eksempel størrelse, stil og farge.</span><span class="sxs-lookup"><span data-stu-id="aad2a-122">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="aad2a-123">Når en produktvariant velges, oppdateres andre egenskaper i kjøpsboksen (for eksempel produktbeskrivelsen og bildene) for å gjenspeile variantinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="aad2a-123">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="aad2a-124">Det er angitt en antallsvelger, slik at kunder kan angi antallet varer som skal kjøpes.</span><span class="sxs-lookup"><span data-stu-id="aad2a-124">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="aad2a-125">Det maksimale antallet som kan kjøpes, kan defineres i områdeinnstillingene.</span><span class="sxs-lookup"><span data-stu-id="aad2a-125">The maximum quantity that can be purchased can be defined in the site settings.</span></span>

<span data-ttu-id="aad2a-126">Fra kjøpsboksen kan kunder også utføre handlinger som å legge til produkter i handlekurven, legge til produkter i ønskelisten og velge plukklokasjon.</span><span class="sxs-lookup"><span data-stu-id="aad2a-126">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="aad2a-127">Disse handlingene kan utføres på et produkt eller en produktvariant.</span><span class="sxs-lookup"><span data-stu-id="aad2a-127">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="aad2a-128">For å kunne legge til et produkt i en ønskeliste må kunden være pålogget.</span><span class="sxs-lookup"><span data-stu-id="aad2a-128">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="aad2a-129">Temaer kan brukes til å fjerne eller endre rekkefølgen på produktegenskaper og handlingskontroller i en kjøpsboks.</span><span class="sxs-lookup"><span data-stu-id="aad2a-129">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="aad2a-130">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="aad2a-130">Module properties</span></span>

- <span data-ttu-id="aad2a-131">**Overskriftsetikett** – Denne egenskapen definerer overskriftsetiketten for produkttittelen.</span><span class="sxs-lookup"><span data-stu-id="aad2a-131">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="aad2a-132">Hvis kjøpsboksen er øverst på siden, bør denne egenskapen settes til **h1** for å oppfylle tilgjengelighetsstandardene.</span><span class="sxs-lookup"><span data-stu-id="aad2a-132">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="aad2a-133">Moduler som kan brukes i kjøpsboksmodulen</span><span class="sxs-lookup"><span data-stu-id="aad2a-133">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="aad2a-134">**Mediegalleri** – Denne modulen brukes til å vise bilder av et produkt på en produktdetaljside.</span><span class="sxs-lookup"><span data-stu-id="aad2a-134">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="aad2a-135">Hvis du vil ha mer informasjon om denne modulen, kan du se [Mediegallerimodul](media-gallery-module.md).</span><span class="sxs-lookup"><span data-stu-id="aad2a-135">For more information about this module, see [Media gallery module](media-gallery-module.md).</span></span>
- <span data-ttu-id="aad2a-136">**Butikkvelger** – Denne modulen viser en liste over nærliggende butikker der en vare er tilgjengelig for henting.</span><span class="sxs-lookup"><span data-stu-id="aad2a-136">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="aad2a-137">Den lar brukere angi en plassering for å finne butikker i nærheten.</span><span class="sxs-lookup"><span data-stu-id="aad2a-137">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="aad2a-138">Hvis du vil ha mer informasjon om denne modulen, kan du se [Butikkvelgermodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="aad2a-138">For more information about this module, see [Store selector module](store-selector.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="aad2a-139">Innstillinger for kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="aad2a-139">Buy box module settings</span></span>

<span data-ttu-id="aad2a-140">Følgende innstillinger for kjøpsboks-modulen kan konfigureres under **Områdeinnstillinger \> Utvidelser**:</span><span class="sxs-lookup"><span data-stu-id="aad2a-140">The following buy box module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="aad2a-141">**Antallsgrense for handlevogn-linjeelement** – Denne egenskapen brukes til å angi maksimalt antall for hver vare som kan legges til i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="aad2a-141">**Cart line quantity limit** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="aad2a-142">En forhandler kan for eksempel bestemme at bare 10 av hvert produkt kan selges i en enkelt transaksjon.</span><span class="sxs-lookup"><span data-stu-id="aad2a-142">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="aad2a-143">**Beholdning** – Hvis du vil ha informasjon om hvordan du bruker beholdningsinnstillinger, kan du se [Bruk beholdningsinnstillinger](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="aad2a-143">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="aad2a-144">**Legg til i handlekurv** – denne egenskapen brukes til å angi atferden etter at en vare er lagt til i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="aad2a-144">**Add to cart** - This property is used to specify the behavior after an item is added to the cart.</span></span> <span data-ttu-id="aad2a-145">De mulige verdiene er **Naviger til handlekurv**, **Ikke naviger til handlekurv** og **Vis varsler**.</span><span class="sxs-lookup"><span data-stu-id="aad2a-145">The possible values are **Navigate to cart**, **Do not navigate to cart**, and **Show notifications**.</span></span> <span data-ttu-id="aad2a-146">Når verdien er satt til **Naviger til handlevogn**, sendes brukerne til handlekurvsiden når de har lagt til en vare.</span><span class="sxs-lookup"><span data-stu-id="aad2a-146">When the value is set to **Navigate to cart**, users are sent to the cart page after they add an item.</span></span> <span data-ttu-id="aad2a-147">Når verdien er satt til **Ikke naviger til handlevogn**, sendes ikke brukerne til handlekurvsiden når de har lagt til en vare.</span><span class="sxs-lookup"><span data-stu-id="aad2a-147">When the value is set to **Do not navigate to cart**, users aren't sent to the cart page after they add an item.</span></span> <span data-ttu-id="aad2a-148">Når verdien er satt til **Vis varsler**, vises det en bekreftelsesmelding, og brukerne kan fortsette å søke på siden med produktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="aad2a-148">When the value is set to **Show notifications**, users are shown a confirmation notification and can continue to browse on the product details page.</span></span> 

    <span data-ttu-id="aad2a-149">Følgende bilde viser et eksempel på bekreftelsesmeldingen "lagt til i handlekurv" på Fabrikam-området.</span><span class="sxs-lookup"><span data-stu-id="aad2a-149">The following image shows an example of an "added to cart" confirmation notification on the Fabrikam site.</span></span>

    ![Eksempel på en varslingsmodul](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="aad2a-151">Samhandling med Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="aad2a-151">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="aad2a-152">Modulen kjøpsboks henter produktinformasjon ved hjelp av API-er for Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="aad2a-152">The buy box module retrieves product information by using Commerce Scale Unit application programming interfaces (APIs).</span></span> <span data-ttu-id="aad2a-153">Produkt-IDen fra produktdetaljersiden brukes til å hente all informasjon.</span><span class="sxs-lookup"><span data-stu-id="aad2a-153">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="aad2a-154">Legge til en kjøpsboksmodul på en side</span><span class="sxs-lookup"><span data-stu-id="aad2a-154">Add a buy box module to a page</span></span>

<span data-ttu-id="aad2a-155">Hvis du vil legge til en kjøpsboksmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="aad2a-155">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="aad2a-156">Gå til **Fragmenter**, og velg **Nytt** for å opprette et nytt sidefragment.</span><span class="sxs-lookup"><span data-stu-id="aad2a-156">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="aad2a-157">I dialogboksen **Nytt sidefragment** velger du **Kjøpsboks**-modulen.</span><span class="sxs-lookup"><span data-stu-id="aad2a-157">In the **New page fragment** dialog box, select the **Buybox** module.</span></span>
1. <span data-ttu-id="aad2a-158">Under **Navn på sidefragment** angir du navnet **Kjøpsboksfragmentet**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="aad2a-158">Under **Page fragment name**, enter the name **Buy box fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="aad2a-159">I **Mediegalleri**-sporet i kjøpsboksmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="aad2a-159">In the **Media Gallery** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="aad2a-160">I dialogboksen **Legg til modul** velger du **Mediegalleri**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="aad2a-160">In the **Add Module** dialog box, select the **Media gallery** module, and then select **OK**.</span></span>
1. <span data-ttu-id="aad2a-161">I **Butikkvelger**-sporet i kjøpsboksmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="aad2a-161">In the **Store selector** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="aad2a-162">I dialogboksen **Legg til modul** velger du **Butikkvelger**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="aad2a-162">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="aad2a-163">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.</span><span class="sxs-lookup"><span data-stu-id="aad2a-163">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="aad2a-164">Gå til **Maler**, og velg **Ny** for å opprette en ny mal.</span><span class="sxs-lookup"><span data-stu-id="aad2a-164">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="aad2a-165">I dialogboksen **Ny mal**, under **Malnavn**, angir du **PDP-mal**, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="aad2a-165">In the **New Template** dialog box, under **Template name**, enter **PDP template**, and then select **OK**.</span></span>
1. <span data-ttu-id="aad2a-166">I **Tekst**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="aad2a-166">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="aad2a-167">I dialogboksen **Legg til modul** velger du **Standardside**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="aad2a-167">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="aad2a-168">På **Hoved**-sporet på standardsiden velger du ellipseknappen (**...**), og deretter velger du **Legg til sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="aad2a-168">In the **Main** slot of the default page, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="aad2a-169">I dialogboksen **Velg sidefragment** velger du **Kjøpsboksfragmentet** du opprettet tidligere, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="aad2a-169">In the **Select page fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="aad2a-170">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="aad2a-170">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="aad2a-171">Gå til **Sider**, og velg **Ny** for å opprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="aad2a-171">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="aad2a-172">I **Velg en mal**-dialogboksen velger du **PDP-mal**.</span><span class="sxs-lookup"><span data-stu-id="aad2a-172">In the **Choose a template** dialog box, select the **PDP template** template.</span></span> <span data-ttu-id="aad2a-173">Under **Sidenavn** angir du **PDP-side**, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="aad2a-173">Under **Page name**, enter **PDP page**, and then select **OK**.</span></span>
1. <span data-ttu-id="aad2a-174">På **Hoved**-sporet på den nye siden velger du ellipseknappen (**...**), og deretter velger du **Legg til sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="aad2a-174">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="aad2a-175">I dialogboksen **Velg sidefragment** velger du **Kjøpsboksfragmentet** du opprettet tidligere, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="aad2a-175">In the **Select page fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="aad2a-176">Lagre og forhåndsvis siden.</span><span class="sxs-lookup"><span data-stu-id="aad2a-176">Save and preview the page.</span></span> <span data-ttu-id="aad2a-177">Legg til spørringsstrengparameteren **?productid=&lt;product id&gt;** i URL-adressen for forhåndsvisningssiden.</span><span class="sxs-lookup"><span data-stu-id="aad2a-177">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="aad2a-178">På den måten brukes produktkonteksten til å laste inn og gjengi forhåndsvisningssiden.</span><span class="sxs-lookup"><span data-stu-id="aad2a-178">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="aad2a-179">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="aad2a-179">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="aad2a-180">En kjøpsboks skal vises på siden for produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="aad2a-180">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aad2a-181">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="aad2a-181">Additional resources</span></span>

[<span data-ttu-id="aad2a-182">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="aad2a-182">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="aad2a-183">Butikkvelgermodul</span><span class="sxs-lookup"><span data-stu-id="aad2a-183">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="aad2a-184">Mediegallerimodul</span><span class="sxs-lookup"><span data-stu-id="aad2a-184">Media gallery module</span></span>](media-gallery-module.md)

[<span data-ttu-id="aad2a-185">Containermodul</span><span class="sxs-lookup"><span data-stu-id="aad2a-185">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="aad2a-186">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="aad2a-186">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="aad2a-187">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="aad2a-187">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="aad2a-188">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="aad2a-188">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="aad2a-189">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="aad2a-189">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="aad2a-190">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="aad2a-190">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="aad2a-191">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="aad2a-191">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="aad2a-192">Beregne lagertilgjengelighet for detaljhandelskanaler</span><span class="sxs-lookup"><span data-stu-id="aad2a-192">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
