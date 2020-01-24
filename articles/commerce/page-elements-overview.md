---
title: Ordliste for sidemodell
description: Dette emnet beskriver de ulike elementene som brukes på sidene på et Microsoft Dynamics 365 Commerce-område.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
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
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0285af2f73a25db3199b3cb089bc0b253a3b3f00
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914870"
---
# <a name="page-model-glossary"></a><span data-ttu-id="91cb3-103">Ordliste for sidemodell</span><span class="sxs-lookup"><span data-stu-id="91cb3-103">Page model glossary</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="91cb3-104">Dette emnet beskriver de ulike elementene som brukes på sidene på et Microsoft Dynamics 365 Commerce-område.</span><span class="sxs-lookup"><span data-stu-id="91cb3-104">This topic describes the various elements that are used on the pages of a Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="page-element-definitions"></a><span data-ttu-id="91cb3-105">Sideelementdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="91cb3-105">Page element definitions</span></span>

<span data-ttu-id="91cb3-106">Følgende tabell gir et sammendrag av termene du bør være kjent med når du endrer utseendet, følelsen og innholdet på området.</span><span class="sxs-lookup"><span data-stu-id="91cb3-106">The following table provides a summary of terms that you should be familiar with when you change the look, feel, and content of your site.</span></span> <span data-ttu-id="91cb3-107">Følg koblingene for mer grundige forklaringer og prosedyrer.</span><span class="sxs-lookup"><span data-stu-id="91cb3-107">For more thorough explanations and procedures, follow the links.</span></span>

| <span data-ttu-id="91cb3-108">Semester</span><span class="sxs-lookup"><span data-stu-id="91cb3-108">Term</span></span> | <span data-ttu-id="91cb3-109">Beskrivelse og merknader</span><span class="sxs-lookup"><span data-stu-id="91cb3-109">Description and notes</span></span> |
|------|-----------------------|
| [<span data-ttu-id="91cb3-110">Modul</span><span class="sxs-lookup"><span data-stu-id="91cb3-110">Module</span></span>](work-with-modules.md) | <p><span data-ttu-id="91cb3-111">**Definisjon:** Moduler er byggeblokker som kan forfattes og utgjør skjelettet til en webside.</span><span class="sxs-lookup"><span data-stu-id="91cb3-111">**Definition:** Modules are building block that can be authored and make up the skeleton of a webpage.</span></span> <span data-ttu-id="91cb3-112">Eksempler kan være topptekst-, hovedbanner- og karusellmoduler.</span><span class="sxs-lookup"><span data-stu-id="91cb3-112">Examples include header, hero, and carousel modules.</span></span></p><p><span data-ttu-id="91cb3-113">**Hvor den velges:** Distribuerte moduler kan velges og konfigureres i ulike stadier i redigeringsarbeidsflyten for området, for eksempel i redigeringstrinnene for mal, oppsett, side og fragment.</span><span class="sxs-lookup"><span data-stu-id="91cb3-113">**Where it's selected:** Deployed modules can be selected and configured in various stages of the site authoring workflow, such as the template, layout, page, and fragment authoring stages.</span></span></p><p><span data-ttu-id="91cb3-114">**Hvor den redigeres:** Egendefinerte moduler opprettes i kode ved hjelp av SDK (Software Development Kit).</span><span class="sxs-lookup"><span data-stu-id="91cb3-114">**Where it's edited:** Custom modules are created in code by using the software development kit (SDK).</span></span> <span data-ttu-id="91cb3-115">Deretter lastes de opp til området, der de blir tilgjengelige for valg.</span><span class="sxs-lookup"><span data-stu-id="91cb3-115">They are then uploaded to your site, where they become available for selection.</span></span></p> |
| <span data-ttu-id="91cb3-116">Modulegenskap</span><span class="sxs-lookup"><span data-stu-id="91cb3-116">Module property</span></span> | <p><span data-ttu-id="91cb3-117">**Definisjon:** Modulegenskaper er bestemte innstillinger som defineres av modulen.</span><span class="sxs-lookup"><span data-stu-id="91cb3-117">**Definition:** Module properties are specific settings that are defined by the module.</span></span> <span data-ttu-id="91cb3-118">De kan redigeres i redigeringsverktøyene for e-handel.</span><span class="sxs-lookup"><span data-stu-id="91cb3-118">They can be edited in the e-Commerce authoring tools.</span></span> <span data-ttu-id="91cb3-119">Modulegenskaper brukes for eksempel til å angi overskrifts- og bakgrunnsbildet for en bannermodul.</span><span class="sxs-lookup"><span data-stu-id="91cb3-119">For example, module properties are used to set the heading and background image of a banner module.</span></span></p><p><span data-ttu-id="91cb3-120">**Hvor de konfigureres:** Det velges og konfigureres modulegenskaper i egenskapsruten som vises i redigeringsmiljøene (redigeringsprogrammer) for maler, oppsett, sider, fragmenter og appinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="91cb3-120">**Where it's configured:** Module properties are selected and configured in the property pane that appears in the authoring environments (editors) for templates, layouts, pages, fragments, and app settings.</span></span></p> |
| [<span data-ttu-id="91cb3-121">Mal</span><span class="sxs-lookup"><span data-stu-id="91cb3-121">Template</span></span>](templates-layouts-overview.md) | <p><span data-ttu-id="91cb3-122">**Definisjon:** Maler definerer modulkombinasjonene og alternativene som skal brukes for en kategori med sider (for eksempel markedsføringssider, kategorisider og produktsider).</span><span class="sxs-lookup"><span data-stu-id="91cb3-122">**Definition:** Templates define the module combinations and options that should be used for a category of pages (for example, marketing pages, category pages, and product pages).</span></span></p><p><span data-ttu-id="91cb3-123">**Hvor de velges:** Maler kan velges under opprettingsarbeidsflyter for side eller oppsett.</span><span class="sxs-lookup"><span data-stu-id="91cb3-123">**Where it's selected:** Templates can be selected during page or layout creation workflows.</span></span></p><p><span data-ttu-id="91cb3-124">**Hvor de redigeres:** Maler redigeres i redigeringsprogrammet for maler.</span><span class="sxs-lookup"><span data-stu-id="91cb3-124">**Where it's edited:** Templates are authored in the template editor.</span></span> <span data-ttu-id="91cb3-125">Det kreves ingen kode for å opprette eller endre dem.</span><span class="sxs-lookup"><span data-stu-id="91cb3-125">No code is required to create or modify them.</span></span></p> |
| [<span data-ttu-id="91cb3-126">Oppsett</span><span class="sxs-lookup"><span data-stu-id="91cb3-126">Layout</span></span>](templates-layouts-overview.md) | <p><span data-ttu-id="91cb3-127">**Definisjon:** Oppsett definerer det endelige utvalget og ordningen av moduler fra settet med alternativer for den overordnede malen.</span><span class="sxs-lookup"><span data-stu-id="91cb3-127">**Definition:** Layouts define the final selection and arrangement of modules from the parent template's set of options.</span></span> <span data-ttu-id="91cb3-128">Et oppsett kan konfigureres for en enkelt side (*egendefinert oppsett*), eller den kan deles av flere sider (*forhåndsdefinert oppsett*).</span><span class="sxs-lookup"><span data-stu-id="91cb3-128">A layout can be configured for a single page (*custom layout*), or it can be shared by multiple pages (*preset layout*).</span></span></p><p><span data-ttu-id="91cb3-129">**Hvor de velges:** Oppsett kan velges ved oppretting av nye sider eller når det er nødvendig med et annet oppsett for en eksisterende side.</span><span class="sxs-lookup"><span data-stu-id="91cb3-129">**Where it's selected:** Layouts can be selected during new page creation or when a different layout is required for an existing page.</span></span></p><p><span data-ttu-id="91cb3-130">**Hvor de redigeres:** Oppsett redigeres i redigeringsprogrammet for oppsett.</span><span class="sxs-lookup"><span data-stu-id="91cb3-130">**Where it's edited:** Layouts are authored in the layout editor.</span></span> <span data-ttu-id="91cb3-131">Det kreves ingen kode for å opprette eller endre dem.</span><span class="sxs-lookup"><span data-stu-id="91cb3-131">No code is required to create or modify them.</span></span></p> |
| <span data-ttu-id="91cb3-132">Sideforekomst</span><span class="sxs-lookup"><span data-stu-id="91cb3-132">Page instance</span></span> | <p><span data-ttu-id="91cb3-133">**Definisjon:** Sideforekomster definerer det endelige, sidespesifikke lokaliserte innholdet for én enkelt side.</span><span class="sxs-lookup"><span data-stu-id="91cb3-133">**Definition:** Page instances define the final, page-specific localized content for a single page.</span></span> <span data-ttu-id="91cb3-134">Dette innholdet er avledet fra verdiene i modulegenskapene.</span><span class="sxs-lookup"><span data-stu-id="91cb3-134">This content is derived from the values of module properties.</span></span></p><p><span data-ttu-id="91cb3-135">**Hvor de velges:** Sider velges når URL-adresser tilordnes.</span><span class="sxs-lookup"><span data-stu-id="91cb3-135">**Where it's selected:** Pages are selected when URLs are assigned.</span></span></p><p><span data-ttu-id="91cb3-136">**Hvor de redigeres:** Sider redigeres i redigeringsprogrammet for side.</span><span class="sxs-lookup"><span data-stu-id="91cb3-136">**Where it's edited:** Pages are edited in the page editor.</span></span> <span data-ttu-id="91cb3-137">Det kreves ingen kode for å opprette eller endre dem.</span><span class="sxs-lookup"><span data-stu-id="91cb3-137">No code is required to create or modify them.</span></span></p> |
| [<span data-ttu-id="91cb3-138">Tema</span><span class="sxs-lookup"><span data-stu-id="91cb3-138">Theme</span></span>](select-site-theme.md) | <p><span data-ttu-id="91cb3-139">**Definisjon:** Temaer definerer det gjennomgripende stilarket (CSS) og bestemmer utseendet og funksjonaliteten til modulene som vises på en side.</span><span class="sxs-lookup"><span data-stu-id="91cb3-139">**Definition:** Themes define the Cascading Style Sheet (CSS), and determine the look and feel of the modules that are rendered on a page.</span></span></p><p><span data-ttu-id="91cb3-140">**Hvor de velges:** Når et tema lastes opp til området ved hjelp av Microsoft Dynamics Lifecycle Services (LCS), kan det velges som en egenskap for sidecontainermodulen.</span><span class="sxs-lookup"><span data-stu-id="91cb3-140">**Where it's selected:** After a theme is uploaded to your site by using Microsoft Dynamics Lifecycle Services (LCS), it can be selected as a property of the page container module.</span></span></p><p><span data-ttu-id="91cb3-141">**Hvor de redigeres:** Temaer opprettes og redigeres for øyeblikket ved hjelp av SDK.</span><span class="sxs-lookup"><span data-stu-id="91cb3-141">**Where it's edited:** Themes are currently created and edited by using the SDK.</span></span> <span data-ttu-id="91cb3-142">Deretter lastes de opp til området ved hjelp av LCS.</span><span class="sxs-lookup"><span data-stu-id="91cb3-142">They are then uploaded to your site by using LCS.</span></span></p> |
| [<span data-ttu-id="91cb3-143">Fragment</span><span class="sxs-lookup"><span data-stu-id="91cb3-143">Fragment</span></span>](work-with-fragments.md) | <p><span data-ttu-id="91cb3-144">**Definisjon:** Fragmenter er fullstendig konfigurerte moduler som har lokalisert innhold som kan brukes på nytt, og sentralt oppdateres på tvers av flere sider.</span><span class="sxs-lookup"><span data-stu-id="91cb3-144">**Definition:** Fragments are fully configured modules that have localized content that can be reused and centrally updated across multiple pages.</span></span> <span data-ttu-id="91cb3-145">Et fragment som er opprettet fra en topptekstmodul, kan for eksempel brukes i alle maler og på alle sider på tvers av området, og oppdateres sentralt på ett sted.</span><span class="sxs-lookup"><span data-stu-id="91cb3-145">For example, a fragment that is created from a header module can be used in all templates and on all pages across your site, and centrally updated in one place.</span></span></p><p><span data-ttu-id="91cb3-146">**Hvor de velges:** Fragmenter kan velges der moduler kan velges.</span><span class="sxs-lookup"><span data-stu-id="91cb3-146">**Where it's selected:** Fragments can be selected wherever modules can be selected.</span></span> <span data-ttu-id="91cb3-147">De kan erstattes for en modul for å bidra til å øke effektiviteten via redigering som er sentralisert og kan brukes på nytt.</span><span class="sxs-lookup"><span data-stu-id="91cb3-147">They can be substituted for a module to help increase efficiency through reusable and centralized authoring.</span></span></p><p><span data-ttu-id="91cb3-148">**Hvor de redigeres:** Fragmenter redigeres i redigeringsprogrammet for fragment.</span><span class="sxs-lookup"><span data-stu-id="91cb3-148">**Where it's edited:** Fragments are edited in the fragment editor.</span></span> <span data-ttu-id="91cb3-149">Det kreves ingen kode for å opprette eller endre dem.</span><span class="sxs-lookup"><span data-stu-id="91cb3-149">No code is required to create or modify them.</span></span></p> |
| <span data-ttu-id="91cb3-150">URL-adresse</span><span class="sxs-lookup"><span data-stu-id="91cb3-150">URL</span></span> | <p><span data-ttu-id="91cb3-151">**Definisjon:** Uniform Resource Locator (URL) er adresser som peker til nettsider eller andre URL-adresser.</span><span class="sxs-lookup"><span data-stu-id="91cb3-151">**Definition:** Uniform resource locators (URLs) are addresses that point to webpages or other URLs.</span></span></p><p><span data-ttu-id="91cb3-152">**Hvor de velges:** URL-adresser velges når det kreves koblinger mellom sider.</span><span class="sxs-lookup"><span data-stu-id="91cb3-152">**Where it's selected:** URLs are selected wherever links between pages are required.</span></span></p><p><span data-ttu-id="91cb3-153">**Hvor de redigeres:** URL-adresser redigeres i redigeringsprogrammet for URL-adresser.</span><span class="sxs-lookup"><span data-stu-id="91cb3-153">**Where it's edited:** URLs are edited in the URL editor.</span></span> <span data-ttu-id="91cb3-154">Det kreves ingen kode for å opprette eller endre dem.</span><span class="sxs-lookup"><span data-stu-id="91cb3-154">No code is required to create or modify them.</span></span></p> |
| <span data-ttu-id="91cb3-155">Aktivum</span><span class="sxs-lookup"><span data-stu-id="91cb3-155">Asset</span></span> | <p><span data-ttu-id="91cb3-156">**Definisjon:** Aktiva er binære filer med filtyper som jpg, docx, pdf eller mpg.</span><span class="sxs-lookup"><span data-stu-id="91cb3-156">**Definition:** Assets are file binaries that have an extension such as .jpg, .docx, .pdf, or .mpg.</span></span></p><p><span data-ttu-id="91cb3-157">**Hvor de velges:** Aktiva velges som modulegenskaper for moduler som krever dem.</span><span class="sxs-lookup"><span data-stu-id="91cb3-157">**Where it's selected:** Assets are selected as module properties for modules that require them.</span></span></p><p><span data-ttu-id="91cb3-158">**Hvor de redigeres:** Aktivva lastes opp, og tilknyttede metadata redigeres i aktivabehandling.</span><span class="sxs-lookup"><span data-stu-id="91cb3-158">**Where it's edited:** Assets are uploaded, and associated metadata is edited in the asset manager.</span></span></p> |

## <a name="additional-resources"></a><span data-ttu-id="91cb3-159">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="91cb3-159">Additional resources</span></span>

[<span data-ttu-id="91cb3-160">Måter å legge til innhold på</span><span class="sxs-lookup"><span data-stu-id="91cb3-160">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="91cb3-161">Dokumentere statuser og livssyklus</span><span class="sxs-lookup"><span data-stu-id="91cb3-161">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="91cb3-162">Arbeide med publiseringsgrupper</span><span class="sxs-lookup"><span data-stu-id="91cb3-162">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="91cb3-163">Arbeide med moduler</span><span class="sxs-lookup"><span data-stu-id="91cb3-163">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="91cb3-164">Arbeide med fragmenter</span><span class="sxs-lookup"><span data-stu-id="91cb3-164">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="91cb3-165">Oversikt over maler og oppsett</span><span class="sxs-lookup"><span data-stu-id="91cb3-165">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="91cb3-166">Tilpasse områdenavigering</span><span class="sxs-lookup"><span data-stu-id="91cb3-166">Customize site navigation</span></span>](customize-site-navigation.md)