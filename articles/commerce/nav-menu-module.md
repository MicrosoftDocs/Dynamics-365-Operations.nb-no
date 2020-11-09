---
title: Navigasjonsmenymodul
description: Dette emnet dekker navigasjonsmenymoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055743"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="c2f39-103">Navigasjonsmenymodul</span><span class="sxs-lookup"><span data-stu-id="c2f39-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c2f39-104">Dette emnet dekker navigasjonsmenymoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c2f39-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c2f39-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="c2f39-105">Overview</span></span>

<span data-ttu-id="c2f39-106">Hovedformålet med navigasjonsmenymoduler er å gjøre det mulig for områdebrukere å bla gjennom produkter og områdesider i henhold til kanalnavigeringshierarkiet som er definert i Dynamics 365 Commerce-hovedkvarteret.</span><span class="sxs-lookup"><span data-stu-id="c2f39-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="c2f39-107">Elementer som er konfigurert i en navigasjonsmenymodul, vises som navigasjon i områdehodet.</span><span class="sxs-lookup"><span data-stu-id="c2f39-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="c2f39-108">Navigasjonsmenymoduler støtter også statiske menyelementer som kobles til andre sider på et e-handelsområde.</span><span class="sxs-lookup"><span data-stu-id="c2f39-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="c2f39-109">Navigasjonsmenymodulen kan legges til i topptekstmodulen på en side.</span><span class="sxs-lookup"><span data-stu-id="c2f39-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="c2f39-110">I Fabrikam-temaet viser navigasjonsmenyen to nivåer som standard.</span><span class="sxs-lookup"><span data-stu-id="c2f39-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="c2f39-111">I Starter-temaet viser navigasjonsmenyen tre nivåer som standard.</span><span class="sxs-lookup"><span data-stu-id="c2f39-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="c2f39-112">Hvis du vil endre antall nivåer, kreves det en visningsutvidelse i temaet.</span><span class="sxs-lookup"><span data-stu-id="c2f39-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="c2f39-113">Følgende illustrasjon viser et eksempel på en navigasjonsmeny for området Fabrikam med to nivåer med kategorihierarki og enkelte statiske menyelementer.</span><span class="sxs-lookup"><span data-stu-id="c2f39-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="c2f39-114">![Eksempel på en navigasjonsmenymodul](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="c2f39-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="c2f39-115">Egenskaper for navigasjonsmenymodul</span><span class="sxs-lookup"><span data-stu-id="c2f39-115">Navigation menu module properties</span></span>

| <span data-ttu-id="c2f39-116">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="c2f39-116">Property name</span></span>             | <span data-ttu-id="c2f39-117">Verdi</span><span class="sxs-lookup"><span data-stu-id="c2f39-117">Value</span></span>                 | <span data-ttu-id="c2f39-118">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c2f39-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="c2f39-119">Kilde</span><span class="sxs-lookup"><span data-stu-id="c2f39-119">Source</span></span>                  | <span data-ttu-id="c2f39-120">**Detaljhandel** , **Manuell redigering** , **Detaljhandel og manuell redigering**</span><span class="sxs-lookup"><span data-stu-id="c2f39-120">**Retail** , **Manual authoring** , **Retail and manual authoring**</span></span> | <span data-ttu-id="c2f39-121">Verdien for **Detaljhandel** gjør at kanalnavigasjonshierarkiet fra Commerce-hovedkontoret vises på navigasjonsmenyen.</span><span class="sxs-lookup"><span data-stu-id="c2f39-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="c2f39-122">Veridn for **Manuell redigering** tillater at statiske menyelementer blir kuratert.</span><span class="sxs-lookup"><span data-stu-id="c2f39-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="c2f39-123">Verdien for **Detaljhandel og manuell redigering** tilbyr en kombinasjon av begge.</span><span class="sxs-lookup"><span data-stu-id="c2f39-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="c2f39-124">Vise kategoribilder</span><span class="sxs-lookup"><span data-stu-id="c2f39-124">Show category images</span></span> | <span data-ttu-id="c2f39-125">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="c2f39-125">**True** or **False**</span></span>    | <span data-ttu-id="c2f39-126">Når denne egenskapen er aktivert, vises kategoribilder på navigasjonsmenyen, som definert i Commerce Headquarters for hver kategori.</span><span class="sxs-lookup"><span data-stu-id="c2f39-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="c2f39-127">Lagt til i Commerce-versjon 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="c2f39-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="c2f39-128">Aktiver navigasjonsmeny med flere nivåer</span><span class="sxs-lookup"><span data-stu-id="c2f39-128">Enable multi-level navigation menu</span></span> | <span data-ttu-id="c2f39-129">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="c2f39-129">**True** or **False**</span></span> | <span data-ttu-id="c2f39-130">Når denne egenskapen er aktivert, kan navigasjonsmenyen vise flere nivåer i navigasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="c2f39-130">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="c2f39-131">Denne funksjonen er tilgjengelig i Dynamics 365 Commerce versjon 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="c2f39-131">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="c2f39-132">Antall nivåer</span><span class="sxs-lookup"><span data-stu-id="c2f39-132">Number of levels</span></span> | <span data-ttu-id="c2f39-133">heltall</span><span class="sxs-lookup"><span data-stu-id="c2f39-133">integer</span></span> | <span data-ttu-id="c2f39-134">Denne egenskapen definerer antall nivåer som skal vises hvis egenskapen **Aktiver navigasjonsmeny med flere nivåer** er satt til **sann**.</span><span class="sxs-lookup"><span data-stu-id="c2f39-134">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="c2f39-135">Statisk menyelement</span><span class="sxs-lookup"><span data-stu-id="c2f39-135">Static menu item</span></span>| <span data-ttu-id="c2f39-136">Matrise med verdier</span><span class="sxs-lookup"><span data-stu-id="c2f39-136">Array of values</span></span>| <span data-ttu-id="c2f39-137">Statiske menyelementer som knytter et menyelementnavn til en kobling til en statisk områdeside.</span><span class="sxs-lookup"><span data-stu-id="c2f39-137">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="c2f39-138">Du kan opprette menyelementer under andre menyelementer.</span><span class="sxs-lookup"><span data-stu-id="c2f39-138">You can create menu items below other menu items.</span></span> <span data-ttu-id="c2f39-139">Som standard vises statiske menyer på rotnivå, og de blir lagt ved kanalnavigasjonshierarkiet hvis det finnes.</span><span class="sxs-lookup"><span data-stu-id="c2f39-139">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="c2f39-140">Vis rotmeny</span><span class="sxs-lookup"><span data-stu-id="c2f39-140">Show root menu</span></span> | <span data-ttu-id="c2f39-141">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="c2f39-141">**True** or **False**</span></span> | <span data-ttu-id="c2f39-142">Når denne egenskapen er aktivert, kan navigasjonsmenyen defineres under en egendefinert rot (for eksempel **Handle nå** ).</span><span class="sxs-lookup"><span data-stu-id="c2f39-142">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now** ).</span></span> <span data-ttu-id="c2f39-143">Denne funksjonen er tilgjengelig i Dynamics 365 Commerce versjon 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="c2f39-143">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="c2f39-144">Rotmeny</span><span class="sxs-lookup"><span data-stu-id="c2f39-144">Root menu</span></span> | <span data-ttu-id="c2f39-145">streng</span><span class="sxs-lookup"><span data-stu-id="c2f39-145">string</span></span> | <span data-ttu-id="c2f39-146">Denne egenskapen kan brukes til å definere tekst for en egendefinert rot hvis egenskapen **Vis rotmeny** er satt til **sann**.</span><span class="sxs-lookup"><span data-stu-id="c2f39-146">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="c2f39-147">Følgende illustrasjon viser et eksempel på et kategoribilde som vises på navigasjonsmenyen for Fabrikam-området.</span><span class="sxs-lookup"><span data-stu-id="c2f39-147">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="c2f39-148">![Eksempel på en navigasjonsmenymodul med kategoribilder](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="c2f39-148">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="c2f39-149">Legge til en navigasjonsmenymodul i en topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="c2f39-149">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="c2f39-150">Hvis du vil ha mer informasjon om hvordan du legger til en navigasjonsmenymodul i en topptekstmodul, kan du se [Topptekstmodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="c2f39-150">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2f39-151">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c2f39-151">Additional resources</span></span>

[<span data-ttu-id="c2f39-152">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="c2f39-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c2f39-153">Søkebanemodul</span><span class="sxs-lookup"><span data-stu-id="c2f39-153">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="c2f39-154">Områdevelgermodul</span><span class="sxs-lookup"><span data-stu-id="c2f39-154">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="c2f39-155">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="c2f39-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c2f39-156">Informasjonskapselsamsvar</span><span class="sxs-lookup"><span data-stu-id="c2f39-156">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="c2f39-157">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="c2f39-157">Header module</span></span>](author-header-module.md)
