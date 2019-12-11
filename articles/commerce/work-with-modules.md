---
title: Arbeide med moduler
description: Dette emnet beskriver hvordan og når du bruker moduler i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
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
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 06a26e5dfd35bf229e67ed27213210d0da726bdf
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698079"
---
# <a name="work-with-modules"></a><span data-ttu-id="4eb01-103">Arbeide med moduler</span><span class="sxs-lookup"><span data-stu-id="4eb01-103">Work with modules</span></span>

<span data-ttu-id="4eb01-104">Dette emnet beskriver hvordan og når du bruker moduler i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4eb01-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="4eb01-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="4eb01-105">Overview</span></span>

<span data-ttu-id="4eb01-106">Moduler er logiske byggeblokker som utgjør sidestrukturen, og de har forskjellige formål og omfang.</span><span class="sxs-lookup"><span data-stu-id="4eb01-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="4eb01-107">Noen moduler er containere på høyt nivå, og det eneste formålet er å oppbevare og organisere andre moduler (underordnede moduler).</span><span class="sxs-lookup"><span data-stu-id="4eb01-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="4eb01-108">Andre moduler, for eksempel en enkel bildeplasseringsmodul, har et svært bestemt formål.</span><span class="sxs-lookup"><span data-stu-id="4eb01-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="4eb01-109">Andre moduler, for eksempel en karusellmodul, faller et sted mellom disse to kategoriene.</span><span class="sxs-lookup"><span data-stu-id="4eb01-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="4eb01-110">Som standard inneholder Dynamics 365 Commerce-området et startpakkemodulbibliotek som lar deg utføre de mest grunnleggende e-handelsscenarioene.</span><span class="sxs-lookup"><span data-stu-id="4eb01-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="4eb01-111">Du skal kunne konstruere et ende-til-ende-område for e-handel bare ved å bruke disse modulene.</span><span class="sxs-lookup"><span data-stu-id="4eb01-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="4eb01-112">Det kan imidlertid hende at du også vil tilpasse disse modulene eller bygge nye, tilpassede moduler for bestemte behov.</span><span class="sxs-lookup"><span data-stu-id="4eb01-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="4eb01-113">Hvis du vil bygge egendefinerte moduler, er en modul-SDK (Software Development Kit) tilgjengelig slik at du kan opprette et egendefinert modulbibliotek.</span><span class="sxs-lookup"><span data-stu-id="4eb01-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="4eb01-114">Containermoduler og -spor</span><span class="sxs-lookup"><span data-stu-id="4eb01-114">Container modules and slots</span></span>

<span data-ttu-id="4eb01-115">Som nevnt tidligere er noen moduler utformet for å inneholde underordnede moduler.</span><span class="sxs-lookup"><span data-stu-id="4eb01-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="4eb01-116">Disse modulene kalles *containere* og tillater hierarkier av nestede moduler.</span><span class="sxs-lookup"><span data-stu-id="4eb01-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="4eb01-117">Containermoduler inneholder *spor*.</span><span class="sxs-lookup"><span data-stu-id="4eb01-117">Container modules include *slots*.</span></span> <span data-ttu-id="4eb01-118">Spor brukes til å håndtere oppsettet og formålet med underordnede moduler i containeren.</span><span class="sxs-lookup"><span data-stu-id="4eb01-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="4eb01-119">Et eksempel er en grunnleggende sidecontainermodul (en modul på øverste nivå for alle sider) som definerer flere viktige spor:</span><span class="sxs-lookup"><span data-stu-id="4eb01-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="4eb01-120">Et overskriftsspor</span><span class="sxs-lookup"><span data-stu-id="4eb01-120">A header slot</span></span>
- <span data-ttu-id="4eb01-121">Et brødtekstspor</span><span class="sxs-lookup"><span data-stu-id="4eb01-121">A body slot</span></span>
- <span data-ttu-id="4eb01-122">Et bunntekstspor</span><span class="sxs-lookup"><span data-stu-id="4eb01-122">A footer slot</span></span>

<span data-ttu-id="4eb01-123">Utvikleren av modulen definerer disse sporene og bestemmer hvilke underordnede moduler og hvor mange underordnede moduler som kan plasseres direkte i den.</span><span class="sxs-lookup"><span data-stu-id="4eb01-123">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="4eb01-124">Overskriftssporet kan for eksempel støtte bare én modul av typen **Topptekst**, mens brødtekstsporet kan støtte et ubegrenset antall moduler av alle typer (bortsett fra andre sidecontainermoduler).</span><span class="sxs-lookup"><span data-stu-id="4eb01-124">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="4eb01-125">I redigeringsverktøyene trenger ikke sideforfattere å vite på forhånd hvilke moduler som kan og ikke kan legges i hvert spor.</span><span class="sxs-lookup"><span data-stu-id="4eb01-125">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="4eb01-126">Når sideforfattere velger et spor, og deretter prøver å velge en modul som skal legges til, vil de se en filtrert visning av modultyper som støttes for dette sporet.</span><span class="sxs-lookup"><span data-stu-id="4eb01-126">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="4eb01-127">Innholdsmoduler</span><span class="sxs-lookup"><span data-stu-id="4eb01-127">Content modules</span></span>

<span data-ttu-id="4eb01-128">Innholdsmoduler inneholder innholds- og medieelementer, for eksempel tekst (f.eks. overskrifter, avsnitt og koblinger) eller aktivareferanser (for eksempel bilder, videoer og PDF-filer).</span><span class="sxs-lookup"><span data-stu-id="4eb01-128">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="4eb01-129">Eksempler på typiske innholdsmodultyper er **Hovedbanner**, **Funksjon** og **Banner**.</span><span class="sxs-lookup"><span data-stu-id="4eb01-129">Examples of typical content module types are **Hero**, **Feature**, and **Banner**.</span></span> <span data-ttu-id="4eb01-130">Moduler av disse tre typene kan inneholde tekst eller medier, og de krever ingen underordnede moduler for å gjøre noe synlig på en side.</span><span class="sxs-lookup"><span data-stu-id="4eb01-130">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="4eb01-131">De fleste av de typiske, daglige side- og innholdsredigeringsaktivitetene omfatter innholdsmoduler, først og fremst siden disse modulene definerer det faktiske innholdet som gjengis i de overordnede containermodulene.</span><span class="sxs-lookup"><span data-stu-id="4eb01-131">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="4eb01-132">Mange innholdsmoduler er tilgjengelige, og disse modulene er vanligvis de siste brikkene du legger til i sidehierarkiet for nestede moduler.</span><span class="sxs-lookup"><span data-stu-id="4eb01-132">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="4eb01-133">Illustrasjonen nedenfor viser hvordan moduler er nestet i overordnede containermodulspor.</span><span class="sxs-lookup"><span data-stu-id="4eb01-133">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Neste moduler](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="4eb01-135">Legge til eller fjerne moduler</span><span class="sxs-lookup"><span data-stu-id="4eb01-135">Add or remove modules</span></span>

<span data-ttu-id="4eb01-136">Følgende prosedyrer beskriver hvordan du legger til og fjerner moduler.</span><span class="sxs-lookup"><span data-stu-id="4eb01-136">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="4eb01-137">Legge til en modul</span><span class="sxs-lookup"><span data-stu-id="4eb01-137">Add a module</span></span>

<span data-ttu-id="4eb01-138">Følg disse trinnene for å legge til en modul i et spor eller en container på en side.</span><span class="sxs-lookup"><span data-stu-id="4eb01-138">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="4eb01-139">I disposisjonsruten til venstre velger du en container eller et spor som en underordnet modul kan legges til i.</span><span class="sxs-lookup"><span data-stu-id="4eb01-139">In the outline pane on the left, select a container or slot that a child module can be added to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4eb01-140">Modulutforming definerer listen over modultyper som kan legges til i et bestemt modulspor.</span><span class="sxs-lookup"><span data-stu-id="4eb01-140">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="4eb01-141">Malredigerere kan deretter forbedre de tillatte modulalternativene for å sikre konsekvent søkemotoroptimalisering (SEO) og administrasjonseffektivitet for alle sidene som er bygget fra en bestemt mal.</span><span class="sxs-lookup"><span data-stu-id="4eb01-141">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages pages that are built from a specific template.</span></span>

1. <span data-ttu-id="4eb01-142">Velg ellipseknappen (**...**) for modulen, og velg deretter **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="4eb01-142">Select the ellipsis button (**...**) for the module, and then select **Add Module**.</span></span> <span data-ttu-id="4eb01-143">Dialogboksen **Legg til modul** vises.</span><span class="sxs-lookup"><span data-stu-id="4eb01-143">The **Add Module** dialog box appears.</span></span> <span data-ttu-id="4eb01-144">Denne dialogboksen blir automatisk filtrert, slik at den bare viser moduler som støttes i valgt container eller spor.</span><span class="sxs-lookup"><span data-stu-id="4eb01-144">This dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="4eb01-145">Listen over moduler bestemmes av sidens mal eller containermoduldefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="4eb01-145">The list of modules is determined by the page's template or the container module definition.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4eb01-146">Hvis en container eller et spor ikke støtter nye underordnede moduler, er alternativet **Legg til modul** ikke tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="4eb01-146">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="4eb01-147">Søk etter og velg en modul du vil legge til på siden, i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="4eb01-147">In the dialog box, search for and select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="4eb01-148">**Funksjon** og **Hovedbanner** er gode modultyper som nybegynnere kan jobbe med.</span><span class="sxs-lookup"><span data-stu-id="4eb01-148">**Feature** and **Hero** are good module types for beginners to work with.</span></span>

1. <span data-ttu-id="4eb01-149">Velg **OK** for å legge den valgte modulen til valgt container eller spor på siden.</span><span class="sxs-lookup"><span data-stu-id="4eb01-149">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="4eb01-150">Fjerne en modul</span><span class="sxs-lookup"><span data-stu-id="4eb01-150">Remove a module</span></span>

<span data-ttu-id="4eb01-151">Følg disse trinnene for å fjerne en modul fra sporet eller containeren på en side.</span><span class="sxs-lookup"><span data-stu-id="4eb01-151">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="4eb01-152">I disposisjonsruten til venstre velger du ellipseknappen ved siden av navnet på modulen som skal fjernes, og deretter velger du papirkurvknappen.</span><span class="sxs-lookup"><span data-stu-id="4eb01-152">In the outline pane on the left, select the ellipsis button next to the name of the module to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="4eb01-153">Når du blir bedt om å bekrefte at du vil fjerne modulen, velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="4eb01-153">When you're prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="4eb01-154">Konfigurere moduler</span><span class="sxs-lookup"><span data-stu-id="4eb01-154">Configure modules</span></span>

<span data-ttu-id="4eb01-155">Følgende prosedyrer beskriver hvordan du konfigurerer innhold og innholdsmoduler.</span><span class="sxs-lookup"><span data-stu-id="4eb01-155">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="4eb01-156">Konfigurere en innholdsmodul</span><span class="sxs-lookup"><span data-stu-id="4eb01-156">Configure a content module</span></span>

<span data-ttu-id="4eb01-157">Hvis du vil konfigurere en innholdsmodul på en side, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="4eb01-157">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="4eb01-158">I disposisjonsruten til venstre velger du en innholdsmodultype (for eksempel **Funksjon**, **Hovedbanner** eller **Banner**).</span><span class="sxs-lookup"><span data-stu-id="4eb01-158">In the outline pane on the left, select a content module type (for example, **Feature**, **Hero**, or **Banner**).</span></span>
1. <span data-ttu-id="4eb01-159">I egenskapsruten til høyre utvider du de nestede kontrollene ved å velge overskriftene og angi eventuelle nødvendige kontrollverdier.</span><span class="sxs-lookup"><span data-stu-id="4eb01-159">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="4eb01-160">Hvis egenskapsruten har en **Datakonfigurasjon**-del, merker du den for å utvide den.</span><span class="sxs-lookup"><span data-stu-id="4eb01-160">If the properties pane has a **Data Configuration** section, select it to expand it.</span></span> <span data-ttu-id="4eb01-161">Hvis ikke går du til trinn 5.</span><span class="sxs-lookup"><span data-stu-id="4eb01-161">Otherwise, go to step 5.</span></span>
1. <span data-ttu-id="4eb01-162">Hvis det finnes en **Legg til datakilde**-knapp, velger du den, og deretter velger du innholdselementene for å legge til.</span><span class="sxs-lookup"><span data-stu-id="4eb01-162">If there is a **Add Data Source** button, select it, and then select the content items to add.</span></span>
1. <span data-ttu-id="4eb01-163">Angi innstillinger for eventuelle nødvendige eller ønskede modulkontroller.</span><span class="sxs-lookup"><span data-stu-id="4eb01-163">Enter settings for any required or desired module controls.</span></span>
1. <span data-ttu-id="4eb01-164">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="4eb01-164">Select **Save**.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="4eb01-165">Konfigurere en containermodul</span><span class="sxs-lookup"><span data-stu-id="4eb01-165">Configure a container module</span></span>

<span data-ttu-id="4eb01-166">Hvis du vil konfigurere en containermodul på en side, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="4eb01-166">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="4eb01-167">Velg en containermodul på siden (for eksempel en karusell eller en modul for flytende container).</span><span class="sxs-lookup"><span data-stu-id="4eb01-167">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="4eb01-168">I egenskapsruten til høyre utvider du de nestede kontrollene ved å velge overskriftene og angi eventuelle nødvendige kontrollverdier.</span><span class="sxs-lookup"><span data-stu-id="4eb01-168">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="4eb01-169">I disposisjonsruten til venstre velger du ellipseknappen ved siden av navnet på enten containeren eller eventuelle spor i containeren, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="4eb01-169">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="4eb01-170">Deretter legger du til underordnede moduler i den valgte containeren.</span><span class="sxs-lookup"><span data-stu-id="4eb01-170">Then add child modules to the selected container.</span></span> <span data-ttu-id="4eb01-171">Hvis du ha mer informasjon, kan du se prosedyren [Legge til en modul](#add-a-module) tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="4eb01-171">For more information, see the [Add a module](#add-a-module) procedure earlier in this topic.</span></span>
1. <span data-ttu-id="4eb01-172">Hvis det finnes flere underordnede moduler som sideordnede i en overordnet container, kan du endre visningsrekkefølgen i den overordnede containeren.</span><span class="sxs-lookup"><span data-stu-id="4eb01-172">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="4eb01-173">Velg ellipseknappen for en modul, og bruk deretter tastene for pil opp og pil ned.</span><span class="sxs-lookup"><span data-stu-id="4eb01-173">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4eb01-174">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4eb01-174">Additional resources</span></span>

[<span data-ttu-id="4eb01-175">Oversikt over maler og oppsett</span><span class="sxs-lookup"><span data-stu-id="4eb01-175">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="4eb01-176">Arbeide med maler</span><span class="sxs-lookup"><span data-stu-id="4eb01-176">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="4eb01-177">Arbeide med forhåndsinnstilte oppsett</span><span class="sxs-lookup"><span data-stu-id="4eb01-177">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="4eb01-178">Arbeide med fragmenter</span><span class="sxs-lookup"><span data-stu-id="4eb01-178">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="4eb01-179">Legge til en containermodul på en side</span><span class="sxs-lookup"><span data-stu-id="4eb01-179">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="4eb01-180">Legge til moduler for innholdsplassering på en side</span><span class="sxs-lookup"><span data-stu-id="4eb01-180">Add content placement modules to a page</span></span>](add-content-placement-modules.md)

