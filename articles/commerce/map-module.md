---
title: Kartmodul
description: Dette emnet dekker kartmoduler og beskriver hvordan du konfigurerer dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e93358a9c76e8eb7bfb4ade4f772dece2aa5f7d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982497"
---
# <a name="map-module"></a><span data-ttu-id="e168c-103">Kartmodul</span><span class="sxs-lookup"><span data-stu-id="e168c-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="e168c-104">Dette emnet dekker kartmoduler og beskriver hvordan du konfigurerer dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e168c-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e168c-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="e168c-105">Overview</span></span>

<span data-ttu-id="e168c-106">En kartmodul viser plasseringen av butikker på et interaktivt kart som gjengis ved hjelp av [Bing Maps V8-webkontrollen](https://docs.microsoft.com/bingmaps/v8-web-control/).</span><span class="sxs-lookup"><span data-stu-id="e168c-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="e168c-107">En API-nøkkel for Bing-kart kreves, og den må legges til på siden Delte parametere for Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="e168c-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="e168c-108">Kartmoduler gir forskjellige visninger, for eksempel veier, fra luften og på gatenivå, som brukerne kan velge for å vise kartstedene.</span><span class="sxs-lookup"><span data-stu-id="e168c-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="e168c-109">De tillater også samhandlinger, som å zoome og bruke brukerens plassering.</span><span class="sxs-lookup"><span data-stu-id="e168c-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="e168c-110">En kartmodul fungerer sammen med butikkvelgermodulen for å bestemme de geografiske lokasjonene til butikkene som må gjengis på et kart.</span><span class="sxs-lookup"><span data-stu-id="e168c-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="e168c-111">Butikkvelgeren og kartmodulene fungerer sammen når en bruker velger en butikk i en av disse modulene på en områdeside.</span><span class="sxs-lookup"><span data-stu-id="e168c-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="e168c-112">Kartmoduler kan utvides for andre scenarier, utover samhandling med butikkvelgermoduler.</span><span class="sxs-lookup"><span data-stu-id="e168c-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="e168c-113">Modultilpassing er imidlertid nødvendig.</span><span class="sxs-lookup"><span data-stu-id="e168c-113">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="e168c-114">Kartmodulen er tilgjengelig i Dynamics 365 Commerce 10.0.13-versjonen.</span><span class="sxs-lookup"><span data-stu-id="e168c-114">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="e168c-115">Bildet nedenfor viser et eksempel på en kartmodul som brukes på en side med butikkplasseringer.</span><span class="sxs-lookup"><span data-stu-id="e168c-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Eksempel på en butikkvelgermodul](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="e168c-117">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="e168c-117">Module properties</span></span>

| <span data-ttu-id="e168c-118">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="e168c-118">Property name</span></span>             | <span data-ttu-id="e168c-119">Verdi</span><span class="sxs-lookup"><span data-stu-id="e168c-119">Value</span></span>                 | <span data-ttu-id="e168c-120">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e168c-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="e168c-121">Overskrift</span><span class="sxs-lookup"><span data-stu-id="e168c-121">Heading</span></span> | <span data-ttu-id="e168c-122">Tekst</span><span class="sxs-lookup"><span data-stu-id="e168c-122">Text</span></span> | <span data-ttu-id="e168c-123">Overskriften for modulen.</span><span class="sxs-lookup"><span data-stu-id="e168c-123">The heading for the module.</span></span> |
| <span data-ttu-id="e168c-124">Alternativer for stift: standardikon</span><span class="sxs-lookup"><span data-stu-id="e168c-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="e168c-125">Bilde</span><span class="sxs-lookup"><span data-stu-id="e168c-125">Image</span></span> | <span data-ttu-id="e168c-126">Bildet for stiftsymbolen som skal brukes for butikker som vises på et kart.</span><span class="sxs-lookup"><span data-stu-id="e168c-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="e168c-127">Alternativer for stift: aktivt ikon</span><span class="sxs-lookup"><span data-stu-id="e168c-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="e168c-128">Bilde</span><span class="sxs-lookup"><span data-stu-id="e168c-128">Image</span></span> | <span data-ttu-id="e168c-129">Bildet for stiftsymbolen som skal brukes for en butikk som er valgt på et kart.</span><span class="sxs-lookup"><span data-stu-id="e168c-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="e168c-130">Alternativer for stift: standard ikonfarge</span><span class="sxs-lookup"><span data-stu-id="e168c-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="e168c-131">Tegnstreng</span><span class="sxs-lookup"><span data-stu-id="e168c-131">Character string</span></span> | <span data-ttu-id="e168c-132">Teksten eller den heksadesimale verdien for stiftsymboler på et kart.</span><span class="sxs-lookup"><span data-stu-id="e168c-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="e168c-133">Alternativer for stift: farge for aktivt ikon</span><span class="sxs-lookup"><span data-stu-id="e168c-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="e168c-134">Tegnstreng</span><span class="sxs-lookup"><span data-stu-id="e168c-134">Character string</span></span> | <span data-ttu-id="e168c-135">Teksten eller den heksadesimale verdien for valgte stiftsymboler på et kart.</span><span class="sxs-lookup"><span data-stu-id="e168c-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="e168c-136">Vis indeks</span><span class="sxs-lookup"><span data-stu-id="e168c-136">Show index</span></span> | <span data-ttu-id="e168c-137">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="e168c-137">**True** or **False**</span></span> | <span data-ttu-id="e168c-138">Hvis denne egenskapen er satt til **Sann**, vil hvert stiftsymbol som angir en butikk, vise en indeks.</span><span class="sxs-lookup"><span data-stu-id="e168c-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="e168c-139">Denne indeksen samsvarer med indeksen i listevisningen som butikkvelgermodulen viser.</span><span class="sxs-lookup"><span data-stu-id="e168c-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="e168c-140">Legge til tillatte URL-adresser for tilordning til et områdes sikkerhetspolicy for innhold</span><span class="sxs-lookup"><span data-stu-id="e168c-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="e168c-141">For at kartmodulen skal kunne kommunisere med Bing Maps, må du kontrollere at følgende URL-adresser for tilordning er tillatt i henhold til områdets sikkerhetspolicy for innhold (CSP).</span><span class="sxs-lookup"><span data-stu-id="e168c-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="e168c-142">Dette oppsettet gjøres i Commerce-områdebygger ved å legge til tillatte URL-adresser i CSP-direktiver for ulike områder (for eksempel **img-src**).</span><span class="sxs-lookup"><span data-stu-id="e168c-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="e168c-143">Hvis du vil ha mer informasjon, se [Innholdssikkerhetspolicy](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="e168c-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="e168c-144">For direktivet **connect-src** legger du til **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="e168c-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="e168c-145">For direktivet **img-src** legger du til **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="e168c-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="e168c-146">For direktivet **script-src** legger du til **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="e168c-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="e168c-147">For direktivet **script style-src** legger du til **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="e168c-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="e168c-148">Legge til en kartmodul på en side</span><span class="sxs-lookup"><span data-stu-id="e168c-148">Add a map module to a page</span></span>

<span data-ttu-id="e168c-149">Hvis du vil ha detaljert informasjon om hvordan du konfigurerer en kartmodul på en side, kan du se [Butikkvelgermodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="e168c-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="e168c-150">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e168c-150">Additional resources</span></span>

[<span data-ttu-id="e168c-151">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="e168c-151">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e168c-152">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="e168c-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e168c-153">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="e168c-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e168c-154">Butikkvelgermodul</span><span class="sxs-lookup"><span data-stu-id="e168c-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="e168c-155">Behandle Bing-kart for organisasjonen</span><span class="sxs-lookup"><span data-stu-id="e168c-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="e168c-156">Bing Maps V8-webkontrollen</span><span class="sxs-lookup"><span data-stu-id="e168c-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
