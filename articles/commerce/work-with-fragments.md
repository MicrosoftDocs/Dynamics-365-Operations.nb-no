---
title: Arbeide med fragmenter
description: Dette emnet beskriver hvorfor, når og hvordan du bruker fragmenter i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3df2d99ef10f909cedef16167fb8d5a0024683b3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210953"
---
# <a name="work-with-fragments"></a><span data-ttu-id="d578b-103">Arbeide med fragmenter</span><span class="sxs-lookup"><span data-stu-id="d578b-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="d578b-104">Dette emnet beskriver hvorfor, når og hvordan du bruker fragmenter i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d578b-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d578b-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="d578b-105">Overview</span></span>

<span data-ttu-id="d578b-106">Fragmenter muliggjør en sentralisert redigeringsopplevelse for modulkonfigurasjoner som må brukes på nytt på hele området.</span><span class="sxs-lookup"><span data-stu-id="d578b-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="d578b-107">Topptekst, bunntekst og bannere er for eksempel ofte konfigurert som fragmenter, fordi de deles på tvers av mange sider.</span><span class="sxs-lookup"><span data-stu-id="d578b-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="d578b-108">Du kan betrakte fragmenter som små websider som kan settes inn i andre sider på området.</span><span class="sxs-lookup"><span data-stu-id="d578b-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="d578b-109">Fragmenter har sin egen livssyklus.</span><span class="sxs-lookup"><span data-stu-id="d578b-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="d578b-110">De opprettes, refereres til, oppdateres og slettet med andre ord som uavhengige enheter i redigeringsverktøyene.</span><span class="sxs-lookup"><span data-stu-id="d578b-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="d578b-111">Når fragmentene er konfigurert, kan de brukes overalt der moduler kan brukes i områdestrukturen.</span><span class="sxs-lookup"><span data-stu-id="d578b-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="d578b-112">Fragmenter kan refereres til på sider, i oppsett, i maler og i andre fragmenter.</span><span class="sxs-lookup"><span data-stu-id="d578b-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="d578b-113">Fragmenter kan nestes opp til sju nivåer i andre fragmenter.</span><span class="sxs-lookup"><span data-stu-id="d578b-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="d578b-114">Hvis du for eksempel vil fremme en sesonghendelse på mange sider på området, kan du bruke et fragment.</span><span class="sxs-lookup"><span data-stu-id="d578b-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="d578b-115">Det første trinnet i prosessen med å opprette et nytt fragment er å velge typen modul du vil starte fra.</span><span class="sxs-lookup"><span data-stu-id="d578b-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="d578b-116">I dette eksemplet kan du bygge fragmentet fra en hovedbannermodul.</span><span class="sxs-lookup"><span data-stu-id="d578b-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="d578b-117">Fragmenter kan bygges fra en hvilken som helst modultype.</span><span class="sxs-lookup"><span data-stu-id="d578b-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="d578b-118">Du kan deretter konfigurere hovedbannerfragmentet med ditt bestemte kampanjeinnhold.</span><span class="sxs-lookup"><span data-stu-id="d578b-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="d578b-119">Du kan også lokalisere den slik du ønsker.</span><span class="sxs-lookup"><span data-stu-id="d578b-119">You can also localize it as you require.</span></span> <span data-ttu-id="d578b-120">Det nye fritt stående hovedbannerfragmentet kan deretter brukes som en forhåndskonfigurert modul i området.</span><span class="sxs-lookup"><span data-stu-id="d578b-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="d578b-121">Det er enkelt å legge den til i maler, til bestemte sider eller til andre fragmenter som kan inneholde hovedbannermoduler.</span><span class="sxs-lookup"><span data-stu-id="d578b-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="d578b-122">Alle steder der fragmentet legges til, er referanser til det sentrale hovedbannerfragmentet du opprettet.</span><span class="sxs-lookup"><span data-stu-id="d578b-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="d578b-123">Hvis du publiserer endringer i fragmentet, vises disse endringene umiddelbart på alle steder der fragmentet blir referert på tvers av området.</span><span class="sxs-lookup"><span data-stu-id="d578b-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="d578b-124">Fragmenter kan derfor være en virkningsfull og effektiv måte å bruke modulkonfigurasjoner på nytt og administrere modulkonfigurasjoner på et område sentralt.</span><span class="sxs-lookup"><span data-stu-id="d578b-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="d578b-125">Ved å bruke dem på en effektiv måte kan du øke allsidigheten betraktelig og redusere kostnadene som er knyttet til administrasjon av områdeinnhold.</span><span class="sxs-lookup"><span data-stu-id="d578b-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="d578b-126">Illustrasjonen nedenfor viser hvordan fragmenter kan brukes til å sentralisere redigering av delte modulkonfigurasjoner på tvers av et e-handelsområde.</span><span class="sxs-lookup"><span data-stu-id="d578b-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![En illustrasjon som viser hvordan fragmenter kan brukes til å sentralisere redigering av delte modulkonfigurasjoner på tvers av et e-handelsområde.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="d578b-128">Opprette et fragment</span><span class="sxs-lookup"><span data-stu-id="d578b-128">Create a fragment</span></span>

<span data-ttu-id="d578b-129">Du kan enten opprette et nytt fragment eller lagre en eksisterende modulkonfigurasjon som et fragment.</span><span class="sxs-lookup"><span data-stu-id="d578b-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="d578b-130">Lagre en eksisterende modulkonfigurasjon som et fragment</span><span class="sxs-lookup"><span data-stu-id="d578b-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="d578b-131">Følg denne fremgangsmåten for å konvertere en tidligere konfigurert modul til et fragment i Commerce-områdebyggeren som kan brukes på nytt.</span><span class="sxs-lookup"><span data-stu-id="d578b-131">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d578b-132">Åpne en side eller mal som inneholder modulen du vil konvertere til et fragment.</span><span class="sxs-lookup"><span data-stu-id="d578b-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="d578b-133">I disposisjonsruten til venstre eller direkte i den visuelle sidebyggeren, velger du den tidligere konfigurerte modulen.</span><span class="sxs-lookup"><span data-stu-id="d578b-133">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="d578b-134">Velg ellipsen (**...**) ved siden av navnet på modulen enten i disposisjonsruten eller den valgte modulens verktøylinje i den visuelle sidebyggeren.</span><span class="sxs-lookup"><span data-stu-id="d578b-134">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="d578b-135">Velg **Del som fragment**.</span><span class="sxs-lookup"><span data-stu-id="d578b-135">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="d578b-136">I dialogboksen **Lagre som fragment** angir du et navn på fragmentet.</span><span class="sxs-lookup"><span data-stu-id="d578b-136">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="d578b-137">Velg **OK** for å lagre modulkonfigurasjonen som et fragment som kan legges til andre sider.</span><span class="sxs-lookup"><span data-stu-id="d578b-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="d578b-138">Opprett et nytt fragment</span><span class="sxs-lookup"><span data-stu-id="d578b-138">Create a new fragment</span></span>

<span data-ttu-id="d578b-139">Følg denne fremgangsmåten for å opprette et nytt fragment i Commerce-områdebygger.</span><span class="sxs-lookup"><span data-stu-id="d578b-139">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d578b-140">Velg **Fragmenter** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="d578b-140">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="d578b-141">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d578b-141">Select **New**.</span></span> <span data-ttu-id="d578b-142">Det vises en dialogboks **Nytt fragment** som viser alle de tilgjengelige modultypene.</span><span class="sxs-lookup"><span data-stu-id="d578b-142">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="d578b-143">Som ble nevnt tidligere kan fragmenter opprettes fra en hvilken som helst modultype.</span><span class="sxs-lookup"><span data-stu-id="d578b-143">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="d578b-144">Velg en modultype for fragmentet.</span><span class="sxs-lookup"><span data-stu-id="d578b-144">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="d578b-145">Når du velger en generisk containermodultype, får du størst fleksibilitet når du må oppdatere og konfigurere fragmentet senere.</span><span class="sxs-lookup"><span data-stu-id="d578b-145">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="d578b-146">Legge til, fjerne eller redigere fragmenter på en side</span><span class="sxs-lookup"><span data-stu-id="d578b-146">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="d578b-147">Følgende prosedyrer beskriver hvordan du legger til, fjerner eller redigerer fragmenter.</span><span class="sxs-lookup"><span data-stu-id="d578b-147">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="d578b-148">Legg til et fragment</span><span class="sxs-lookup"><span data-stu-id="d578b-148">Add a fragment</span></span>

<span data-ttu-id="d578b-149">Følg denne fremgangsmåten for å legge til et fragment i en side i Commerce-områdebygger.</span><span class="sxs-lookup"><span data-stu-id="d578b-149">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d578b-150">I disposisjonsruten til venstre eller direkte i den visuelle sidebyggeren, velger du en container eller et spor der underordnede moduler kan legges til.</span><span class="sxs-lookup"><span data-stu-id="d578b-150">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="d578b-151">Velg ellipsen (**...**) ved siden av navnet på containeren eller sporet.</span><span class="sxs-lookup"><span data-stu-id="d578b-151">Select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="d578b-152">Hvis du bruker den visuelle sidebyggeren, kan du eventuelt velge plusstegnet (**+**).</span><span class="sxs-lookup"><span data-stu-id="d578b-152">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="d578b-153">Velg **Legg til fragment**.</span><span class="sxs-lookup"><span data-stu-id="d578b-153">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="d578b-154">Hvis containeren eller sporet ikke støtter nye underordnede moduler, er alternativet **Legg til fragment** ikke tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="d578b-154">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="d578b-155">Søk etter og velg et fragment du vil legge til, i dialogboksen **Velg fragment**.</span><span class="sxs-lookup"><span data-stu-id="d578b-155">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="d578b-156">Hvis det ikke finnes noen tilgjengelige fragmenter, kan det være at du først må opprette et fragment fra en modultype som valgt container eller spor støtter.</span><span class="sxs-lookup"><span data-stu-id="d578b-156">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="d578b-157">Velg det ønskede fragmentet for å legge det til i containeren eller sporet på siden.</span><span class="sxs-lookup"><span data-stu-id="d578b-157">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="d578b-158">Modulene som er tillatt i en container eller et spor, er definert av malen for siden eller modulenes egne definisjoner.</span><span class="sxs-lookup"><span data-stu-id="d578b-158">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="d578b-159">Fjerne et fragment</span><span class="sxs-lookup"><span data-stu-id="d578b-159">Remove a fragment</span></span>

<span data-ttu-id="d578b-160">Hvis du vil fjerne et fragment fra et spor eller en container på en side i Commerce-områdebyggeren, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="d578b-160">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d578b-161">I disposisjonsruten til venstre velger du ellipsen (**...**) ved siden av navnet på fragmentet som skal fjernes, og deretter velger du papirkurvsymbolet.</span><span class="sxs-lookup"><span data-stu-id="d578b-161">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="d578b-162">Du kan også velge fragmentet i den visuelle sidebyggeren og velge papirkurvsymbolet på verktøylinjen til fragmentet.</span><span class="sxs-lookup"><span data-stu-id="d578b-162">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="d578b-163">Når du blir bedt om å bekrefte at du vil fjerne fragmentet, velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="d578b-163">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="d578b-164">Når du fjerner et fragment fra en side, fjerner du bare referansen til det fra den siden.</span><span class="sxs-lookup"><span data-stu-id="d578b-164">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="d578b-165">Du sletter **ikke** fragmentet fra området ditt.</span><span class="sxs-lookup"><span data-stu-id="d578b-165">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="d578b-166">Hvis du vil slette fragmenter fra området, må du bruke brukergrensesnittet for fragmentinspeksjonen.</span><span class="sxs-lookup"><span data-stu-id="d578b-166">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="d578b-167">Du kan bare slette fragmenter fra et område hvis de ikke er referert til av sider, maler eller andre fragmenter.</span><span class="sxs-lookup"><span data-stu-id="d578b-167">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="d578b-168">Redigere et fragment</span><span class="sxs-lookup"><span data-stu-id="d578b-168">Edit a fragment</span></span>

<span data-ttu-id="d578b-169">Hvis du vil redigere fragmenter, må du bruke brukergrensesnittet for fragmentredigering.</span><span class="sxs-lookup"><span data-stu-id="d578b-169">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="d578b-170">Denne begrensningen er standard.</span><span class="sxs-lookup"><span data-stu-id="d578b-170">This restriction is by design.</span></span> <span data-ttu-id="d578b-171">Den hjelper til med å garantere at forfattere ikke forveksler prosessen med å redigere modulene for en bestemt side med prosessen med å redigere fragmenter som kan deles på mange sider.</span><span class="sxs-lookup"><span data-stu-id="d578b-171">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="d578b-172">Følg denne fremgangsmåten for å redigere et nytt fragment i Commerce-områdebygger.</span><span class="sxs-lookup"><span data-stu-id="d578b-172">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d578b-173">Velg **Fragmenter** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="d578b-173">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="d578b-174">Under **Fragmenter** velger du fragmentet du vil redigere.</span><span class="sxs-lookup"><span data-stu-id="d578b-174">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="d578b-175">Rediger fragmentets modulegenskaper og struktur etter behov.</span><span class="sxs-lookup"><span data-stu-id="d578b-175">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="d578b-176">Prosessen ligner på redigeringsprosessen for moduler som redigeres i sideredigeringsvisning.</span><span class="sxs-lookup"><span data-stu-id="d578b-176">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="d578b-177">Du kan også redigere et fragment ved å velge det på en side, i en mal, eller i et overordnet fragment, og deretter velge **Rediger fragment** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="d578b-177">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d578b-178">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d578b-178">Additional resources</span></span>

[<span data-ttu-id="d578b-179">Oversikt over maler og oppsett</span><span class="sxs-lookup"><span data-stu-id="d578b-179">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="d578b-180">Arbeide med maler</span><span class="sxs-lookup"><span data-stu-id="d578b-180">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="d578b-181">Arbeide med forhåndsinnstilte oppsett</span><span class="sxs-lookup"><span data-stu-id="d578b-181">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="d578b-182">Arbeide med publiseringsgrupper</span><span class="sxs-lookup"><span data-stu-id="d578b-182">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]