---
title: Navigasjonsmenymodul
description: Dette emnet dekker navigasjonsmenymoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3461993e2bd59d66be1640331e4ef315a078469
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251217"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="5297e-103">Navigasjonsmenymodul</span><span class="sxs-lookup"><span data-stu-id="5297e-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="5297e-104">Dette emnet dekker navigasjonsmenymoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5297e-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5297e-105">Hovedformålet med navigasjonsmenymoduler er å gjøre det mulig for områdebrukere å bla gjennom produkter og områdesider i henhold til kanalnavigeringshierarkiet som er definert i Dynamics 365 Commerce-hovedkvarteret.</span><span class="sxs-lookup"><span data-stu-id="5297e-105">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="5297e-106">Elementer som er konfigurert i en navigasjonsmenymodul, vises som navigasjon i områdehodet.</span><span class="sxs-lookup"><span data-stu-id="5297e-106">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="5297e-107">Navigasjonsmenymoduler støtter også statiske menyelementer som kobles til andre sider på et e-handelsområde.</span><span class="sxs-lookup"><span data-stu-id="5297e-107">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="5297e-108">Navigasjonsmenymodulen kan legges til i topptekstmodulen på en side.</span><span class="sxs-lookup"><span data-stu-id="5297e-108">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="5297e-109">I Fabrikam-temaet viser navigasjonsmenyen to nivåer som standard.</span><span class="sxs-lookup"><span data-stu-id="5297e-109">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="5297e-110">I Starter-temaet viser navigasjonsmenyen tre nivåer som standard.</span><span class="sxs-lookup"><span data-stu-id="5297e-110">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="5297e-111">Hvis du vil endre antall nivåer, kreves det en visningsutvidelse i temaet.</span><span class="sxs-lookup"><span data-stu-id="5297e-111">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="5297e-112">Følgende illustrasjon viser et eksempel på en navigasjonsmeny for området Fabrikam med to nivåer med kategorihierarki og enkelte statiske menyelementer.</span><span class="sxs-lookup"><span data-stu-id="5297e-112">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="5297e-113">![Eksempel på en navigasjonsmenymodul](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="5297e-113">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="5297e-114">Egenskaper for navigasjonsmenymodul</span><span class="sxs-lookup"><span data-stu-id="5297e-114">Navigation menu module properties</span></span>

| <span data-ttu-id="5297e-115">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="5297e-115">Property name</span></span>             | <span data-ttu-id="5297e-116">Verdi</span><span class="sxs-lookup"><span data-stu-id="5297e-116">Value</span></span>                 | <span data-ttu-id="5297e-117">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5297e-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="5297e-118">Kilde</span><span class="sxs-lookup"><span data-stu-id="5297e-118">Source</span></span>                  | <span data-ttu-id="5297e-119">**Detaljhandel**, **Manuell redigering**, **Detaljhandel og manuell redigering**</span><span class="sxs-lookup"><span data-stu-id="5297e-119">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="5297e-120">Verdien for **Detaljhandel** gjør at kanalnavigasjonshierarkiet fra Commerce-hovedkontoret vises på navigasjonsmenyen.</span><span class="sxs-lookup"><span data-stu-id="5297e-120">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="5297e-121">Veridn for **Manuell redigering** tillater at statiske menyelementer blir kuratert.</span><span class="sxs-lookup"><span data-stu-id="5297e-121">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="5297e-122">Verdien for **Detaljhandel og manuell redigering** tilbyr en kombinasjon av begge.</span><span class="sxs-lookup"><span data-stu-id="5297e-122">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="5297e-123">Vise kategoribilder</span><span class="sxs-lookup"><span data-stu-id="5297e-123">Show category images</span></span> | <span data-ttu-id="5297e-124">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="5297e-124">**True** or **False**</span></span>    | <span data-ttu-id="5297e-125">Når denne egenskapen er aktivert, vises kategoribilder på navigasjonsmenyen, som definert i Commerce Headquarters for hver kategori.</span><span class="sxs-lookup"><span data-stu-id="5297e-125">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="5297e-126">Lagt til i Commerce-versjon 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="5297e-126">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="5297e-127">Vis kampanjer</span><span class="sxs-lookup"><span data-stu-id="5297e-127">Show promotions</span></span> | <span data-ttu-id="5297e-128">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="5297e-128">**True** or **False**</span></span> | <span data-ttu-id="5297e-129">Når denne egenskapen er aktivert, kan kampanjer konfigureres ved hjelp av bilder, koblinger og tekst.</span><span class="sxs-lookup"><span data-stu-id="5297e-129">When this property is enabled, promotions can be configured by using images, links, and text.</span></span> <span data-ttu-id="5297e-130">Denne egenskapen ble lagt til i Commerce versjon 10.0.17-versjonen.</span><span class="sxs-lookup"><span data-stu-id="5297e-130">This property was added in the Commerce version 10.0.17 release.</span></span> |
| <span data-ttu-id="5297e-131">Legge til kampanjer</span><span class="sxs-lookup"><span data-stu-id="5297e-131">Add promotions</span></span> | <span data-ttu-id="5297e-132">Tekst, bilde eller kobling</span><span class="sxs-lookup"><span data-stu-id="5297e-132">Text, image, or link</span></span> | <span data-ttu-id="5297e-133">Når egenskapen **Vis kampanjer** er aktivert, kan du legge til tekst, et bilde eller en kobling som kampanjeinnhold på navigasjonsmenyen.</span><span class="sxs-lookup"><span data-stu-id="5297e-133">When the **Show promotions** property is enabled, you can add text, an image, or a link as promotional content on the navigation menu.</span></span> |
| <span data-ttu-id="5297e-134">Aktiver navigasjonsmeny med flere nivåer</span><span class="sxs-lookup"><span data-stu-id="5297e-134">Enable multi-level navigation menu</span></span> | <span data-ttu-id="5297e-135">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="5297e-135">**True** or **False**</span></span> | <span data-ttu-id="5297e-136">Når denne egenskapen er aktivert, kan navigasjonsmenyen vise flere nivåer i navigasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="5297e-136">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="5297e-137">Denne funksjonen er tilgjengelig i Commerce versjon 10.0.15-versjonen.</span><span class="sxs-lookup"><span data-stu-id="5297e-137">This feature is available in the Commerce version 10.0.15 release.</span></span> |
| <span data-ttu-id="5297e-138">Antall nivåer</span><span class="sxs-lookup"><span data-stu-id="5297e-138">Number of levels</span></span> | <span data-ttu-id="5297e-139">heltall</span><span class="sxs-lookup"><span data-stu-id="5297e-139">integer</span></span> | <span data-ttu-id="5297e-140">Denne egenskapen definerer antall nivåer som skal vises hvis egenskapen **Aktiver navigasjonsmeny med flere nivåer** er satt til **sann**.</span><span class="sxs-lookup"><span data-stu-id="5297e-140">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="5297e-141">Statisk menyelement</span><span class="sxs-lookup"><span data-stu-id="5297e-141">Static menu item</span></span>| <span data-ttu-id="5297e-142">Matrise med verdier</span><span class="sxs-lookup"><span data-stu-id="5297e-142">Array of values</span></span>| <span data-ttu-id="5297e-143">Statiske menyelementer som knytter et menyelementnavn til en kobling til en statisk områdeside.</span><span class="sxs-lookup"><span data-stu-id="5297e-143">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="5297e-144">Du kan opprette menyelementer under andre menyelementer.</span><span class="sxs-lookup"><span data-stu-id="5297e-144">You can create menu items below other menu items.</span></span> <span data-ttu-id="5297e-145">Som standard vises statiske menyer på rotnivå, og de blir lagt ved kanalnavigasjonshierarkiet hvis det finnes.</span><span class="sxs-lookup"><span data-stu-id="5297e-145">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="5297e-146">Vis rotmeny</span><span class="sxs-lookup"><span data-stu-id="5297e-146">Show root menu</span></span> | <span data-ttu-id="5297e-147">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="5297e-147">**True** or **False**</span></span> | <span data-ttu-id="5297e-148">Når denne egenskapen er aktivert, kan navigasjonsmenyen defineres under en egendefinert rot (for eksempel **Handle nå**).</span><span class="sxs-lookup"><span data-stu-id="5297e-148">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now**).</span></span> <span data-ttu-id="5297e-149">Denne funksjonen er tilgjengelig i Dynamics 365 Commerce versjon 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="5297e-149">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="5297e-150">Rotmeny</span><span class="sxs-lookup"><span data-stu-id="5297e-150">Root menu</span></span> | <span data-ttu-id="5297e-151">streng</span><span class="sxs-lookup"><span data-stu-id="5297e-151">string</span></span> | <span data-ttu-id="5297e-152">Denne egenskapen kan brukes til å definere tekst for en egendefinert rot hvis egenskapen **Vis rotmeny** er satt til **sann**.</span><span class="sxs-lookup"><span data-stu-id="5297e-152">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="5297e-153">Følgende illustrasjon viser et eksempel på et kategoribilde som vises på navigasjonsmenyen for Fabrikam-området.</span><span class="sxs-lookup"><span data-stu-id="5297e-153">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="5297e-154">![Eksempel på en navigasjonsmenymodul med kategoribilder](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="5297e-154">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="5297e-155">Legge til en navigasjonsmenymodul i en topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="5297e-155">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="5297e-156">Hvis du vil ha mer informasjon om hvordan du legger til en navigasjonsmenymodul i en topptekstmodul, kan du se [Topptekstmodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="5297e-156">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5297e-157">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5297e-157">Additional resources</span></span>

[<span data-ttu-id="5297e-158">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="5297e-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5297e-159">Søkebanemodul</span><span class="sxs-lookup"><span data-stu-id="5297e-159">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="5297e-160">Områdevelgermodul</span><span class="sxs-lookup"><span data-stu-id="5297e-160">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="5297e-161">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="5297e-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="5297e-162">Informasjonskapselsamsvar</span><span class="sxs-lookup"><span data-stu-id="5297e-162">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="5297e-163">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="5297e-163">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]