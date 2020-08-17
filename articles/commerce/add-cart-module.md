---
title: Handlekurvmodul
description: Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f21268ed4cffed1d5c789f722796cdf05e965819
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621042"
---
# <a name="cart-module"></a><span data-ttu-id="ce955-103">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="ce955-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ce955-104">Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ce955-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ce955-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="ce955-105">Overview</span></span>

<span data-ttu-id="ce955-106">En handlekurvmodul viser varene som er lagt til i handlekurven før kunden går videre til kassen.</span><span class="sxs-lookup"><span data-stu-id="ce955-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="ce955-107">Modulen viser også et ordresammendrag som lar kunden bruke eller fjerne kampanjekoder.</span><span class="sxs-lookup"><span data-stu-id="ce955-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="ce955-108">Handlekurvmodulen støtter pålogget utsjekking og Sjekk ut som gjest.</span><span class="sxs-lookup"><span data-stu-id="ce955-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="ce955-109">Den støtter også koblingen **Tilbake til shopping**.</span><span class="sxs-lookup"><span data-stu-id="ce955-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="ce955-110">Du kan konfigurere ruten for denne koblingen under **Områdeinnstillinger \> Utvidelser \> Ruter**.</span><span class="sxs-lookup"><span data-stu-id="ce955-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="ce955-111">Handlekurvmodulen gjengir data basert på handlekurv-IDen, som er en informasjonskapsel i leseren som er tilgjengelig i hele området.</span><span class="sxs-lookup"><span data-stu-id="ce955-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="ce955-112">Bildet nedenfor viser et eksempel på en handlekurvside på Fabrikam-området.</span><span class="sxs-lookup"><span data-stu-id="ce955-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Eksempel på en handlevognmodul](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="ce955-114">Egenskaper og spor for handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="ce955-114">Cart module properties and slots</span></span>

<span data-ttu-id="ce955-115">Handlekurvmodulen har egenskapen **Overskrift** som kan settes til verdier som **Handlepose** og **Varer i handlekurven**.</span><span class="sxs-lookup"><span data-stu-id="ce955-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="ce955-116">Moduler som kan brukes i handlekurvmodulen</span><span class="sxs-lookup"><span data-stu-id="ce955-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="ce955-117">**Tekstblokk** – Denne modulen støtter tilpassede meldinger i handlekurvmodulen.</span><span class="sxs-lookup"><span data-stu-id="ce955-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="ce955-118">Meldingene drives av innholdsbehandlingssystemet (CMS).</span><span class="sxs-lookup"><span data-stu-id="ce955-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="ce955-119">Alle meldinger kan legges til, for eksempel "For problemer med ordren, kontakt 1-800-Fabrikam."</span><span class="sxs-lookup"><span data-stu-id="ce955-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="ce955-120">**Butikkvelger** – Denne modulen viser en liste over nærliggende butikker der en vare er tilgjengelig for henting.</span><span class="sxs-lookup"><span data-stu-id="ce955-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="ce955-121">Den lar brukere angi en plassering for å finne butikker i nærheten.</span><span class="sxs-lookup"><span data-stu-id="ce955-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="ce955-122">Hvis du vil ha mer informasjon om denne modulen, se [Butikkvelgermodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="ce955-122">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="ce955-123">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="ce955-123">Module properties</span></span>

<span data-ttu-id="ce955-124">Følgende innstillinger for handlevognmodulen kan konfigureres under **Områdeinnstillinger \> Utvidelser**:</span><span class="sxs-lookup"><span data-stu-id="ce955-124">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="ce955-125">**Maksimalt antall** – Denne egenskapen brukes til å angi maksimalt antall for hver vare som kan legges til i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="ce955-125">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="ce955-126">En forhandler kan for eksempel bestemme at bare 10 av hvert produkt kan selges i en enkelt transaksjon.</span><span class="sxs-lookup"><span data-stu-id="ce955-126">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="ce955-127">**Beholdning** – Hvis du vil ha informasjon om hvordan du bruker beholdningsinnstillinger, kan du se [Bruk beholdningsinnstillinger](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="ce955-127">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="ce955-128">**Tilbake til shopping** – Denne egenskapen brukes til å angi ruten for **Tilbake til shopping**-koblingen.</span><span class="sxs-lookup"><span data-stu-id="ce955-128">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="ce955-129">Ruten kan konfigureres på områdenivå, slik at forhandlere kan bringe kunden tilbake til hjemmesiden eller en hvilken som helst annen side på området.</span><span class="sxs-lookup"><span data-stu-id="ce955-129">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="ce955-130">Samhandling med Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="ce955-130">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="ce955-131">Handlekurvmodulen henter produktinformasjon ved hjelp av API-er for Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="ce955-131">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="ce955-132">Handlekurv-IDen fra leserinformasjonskapselen brukes til å hente all produktinformasjon fra Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="ce955-132">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="ce955-133">Legge til en handlekurvmodul på en side</span><span class="sxs-lookup"><span data-stu-id="ce955-133">Add a cart module to a page</span></span>

<span data-ttu-id="ce955-134">Hvis du vil legge til en handlekurvmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="ce955-134">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="ce955-135">Gå til **Sidefragmenter**, og velg **Ny** for å opprette et nytt sidefragment.</span><span class="sxs-lookup"><span data-stu-id="ce955-135">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="ce955-136">I dialogboksen **Nytt sidefragment** velger du **Handlevogn**-modulen.</span><span class="sxs-lookup"><span data-stu-id="ce955-136">In the **New Page Fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="ce955-137">Under **Navn på sidefragment** angir navnet **Handlevognfragment**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce955-137">Under **Page Fragment Name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="ce955-138">Velg **Handlevogn**-sporet.</span><span class="sxs-lookup"><span data-stu-id="ce955-138">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="ce955-139">I egenskapsruten til høyre velger du blyantsymbolet, angir overskriftsteksten i feltet, og merker av for avmerkingssymbolet.</span><span class="sxs-lookup"><span data-stu-id="ce955-139">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="ce955-140">I **Handlevogn**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="ce955-140">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="ce955-141">I dialogboksen **Legg til modul** velger du **Butikkvelger**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce955-141">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="ce955-142">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.</span><span class="sxs-lookup"><span data-stu-id="ce955-142">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="ce955-143">Gå til **Maler**, og velg **Ny** for å opprette en ny mal.</span><span class="sxs-lookup"><span data-stu-id="ce955-143">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="ce955-144">I dialogboksen **Ny mal**, under **Malnavn**, angir du et navn på malen.</span><span class="sxs-lookup"><span data-stu-id="ce955-144">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="ce955-145">Velg **Brødtekst**-sporet i disposisjonstreet, velg ellipseknappen (**…**), og velg deretter **Legg til fragment**.</span><span class="sxs-lookup"><span data-stu-id="ce955-145">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="ce955-146">I dialogboksen **Velg sidefragment** velger du **Handlevognfragmentet**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce955-146">In the **Select Page Fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="ce955-147">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="ce955-147">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="ce955-148">Gå til **Sider**, og velg **Ny** for å opprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="ce955-148">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="ce955-149">I dialogboksen **Velg en mal** velger du malen du opprettet, angir et sidenavn, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce955-149">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="ce955-150">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="ce955-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="ce955-151">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="ce955-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce955-152">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ce955-152">Additional resources</span></span>

[<span data-ttu-id="ce955-153">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="ce955-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ce955-154">Containermodul</span><span class="sxs-lookup"><span data-stu-id="ce955-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="ce955-155">Butikkvelgermodul</span><span class="sxs-lookup"><span data-stu-id="ce955-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="ce955-156">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="ce955-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="ce955-157">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="ce955-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="ce955-158">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="ce955-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="ce955-159">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="ce955-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="ce955-160">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="ce955-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="ce955-161">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="ce955-161">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="ce955-162">Beregne lagertilgjengelighet for detaljhandelskanaler</span><span class="sxs-lookup"><span data-stu-id="ce955-162">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
