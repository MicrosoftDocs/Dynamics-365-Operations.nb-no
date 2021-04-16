---
title: Arbeide med fragmenter
description: Dette emnet beskriver hvorfor, når og hvordan du bruker fragmenter i Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1fa55ab83562983273768895db61032ec7199fa6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793951"
---
# <a name="work-with-fragments"></a><span data-ttu-id="6941f-103">Arbeide med fragmenter</span><span class="sxs-lookup"><span data-stu-id="6941f-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="6941f-104">Dette emnet beskriver hvorfor, når og hvordan du bruker fragmenter i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6941f-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6941f-105">Fragmenter muliggjør en sentralisert redigeringsopplevelse for modulkonfigurasjoner som må brukes på nytt på hele området.</span><span class="sxs-lookup"><span data-stu-id="6941f-105">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="6941f-106">Topptekst, bunntekst og bannere er for eksempel ofte konfigurert som fragmenter, fordi de deles på tvers av mange sider.</span><span class="sxs-lookup"><span data-stu-id="6941f-106">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="6941f-107">Du kan betrakte fragmenter som små websider som kan settes inn i andre sider på området.</span><span class="sxs-lookup"><span data-stu-id="6941f-107">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="6941f-108">Fragmenter har sin egen livssyklus.</span><span class="sxs-lookup"><span data-stu-id="6941f-108">Fragments have their own lifecycle.</span></span> <span data-ttu-id="6941f-109">De opprettes, refereres til, oppdateres og slettet med andre ord som uavhengige enheter i redigeringsverktøyene.</span><span class="sxs-lookup"><span data-stu-id="6941f-109">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="6941f-110">Når fragmentene er konfigurert, kan de brukes overalt der moduler kan brukes i områdestrukturen.</span><span class="sxs-lookup"><span data-stu-id="6941f-110">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="6941f-111">Fragmenter kan refereres til på sider, i oppsett, i maler og i andre fragmenter.</span><span class="sxs-lookup"><span data-stu-id="6941f-111">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="6941f-112">Fragmenter kan nestes opp til sju nivåer i andre fragmenter.</span><span class="sxs-lookup"><span data-stu-id="6941f-112">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="6941f-113">Hvis du for eksempel vil fremme en sesonghendelse på mange sider på området, kan du bruke et fragment.</span><span class="sxs-lookup"><span data-stu-id="6941f-113">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="6941f-114">Det første trinnet i prosessen med å opprette et nytt fragment er å velge typen modul du vil starte fra.</span><span class="sxs-lookup"><span data-stu-id="6941f-114">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="6941f-115">I dette eksemplet kan du bygge fragmentet fra en hovedbannermodul.</span><span class="sxs-lookup"><span data-stu-id="6941f-115">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="6941f-116">Fragmenter kan bygges fra en hvilken som helst modultype.</span><span class="sxs-lookup"><span data-stu-id="6941f-116">Fragments can be built from any module type.</span></span>

<span data-ttu-id="6941f-117">Du kan deretter konfigurere hovedbannerfragmentet med ditt bestemte kampanjeinnhold.</span><span class="sxs-lookup"><span data-stu-id="6941f-117">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="6941f-118">Du kan også lokalisere den slik du ønsker.</span><span class="sxs-lookup"><span data-stu-id="6941f-118">You can also localize it as you require.</span></span> <span data-ttu-id="6941f-119">Det nye fritt stående hovedbannerfragmentet kan deretter brukes som en forhåndskonfigurert modul i området.</span><span class="sxs-lookup"><span data-stu-id="6941f-119">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="6941f-120">Det er enkelt å legge den til i maler, til bestemte sider eller til andre fragmenter som kan inneholde hovedbannermoduler.</span><span class="sxs-lookup"><span data-stu-id="6941f-120">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="6941f-121">Alle steder der fragmentet legges til, er referanser til det sentrale hovedbannerfragmentet du opprettet.</span><span class="sxs-lookup"><span data-stu-id="6941f-121">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="6941f-122">Hvis du publiserer endringer i fragmentet, vises disse endringene umiddelbart på alle steder der fragmentet blir referert på tvers av området.</span><span class="sxs-lookup"><span data-stu-id="6941f-122">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="6941f-123">Fragmenter kan derfor være en virkningsfull og effektiv måte å bruke modulkonfigurasjoner på nytt og administrere modulkonfigurasjoner på et område sentralt.</span><span class="sxs-lookup"><span data-stu-id="6941f-123">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="6941f-124">Ved å bruke dem på en effektiv måte kan du øke allsidigheten betraktelig og redusere kostnadene som er knyttet til administrasjon av områdeinnhold.</span><span class="sxs-lookup"><span data-stu-id="6941f-124">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="6941f-125">Illustrasjonen nedenfor viser hvordan fragmenter kan brukes til å sentralisere redigering av delte modulkonfigurasjoner på tvers av et e-handelsområde.</span><span class="sxs-lookup"><span data-stu-id="6941f-125">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![En illustrasjon som viser hvordan fragmenter kan brukes til å sentralisere redigering av delte modulkonfigurasjoner på tvers av et e-handelsområde.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="6941f-127">Opprette et fragment</span><span class="sxs-lookup"><span data-stu-id="6941f-127">Create a fragment</span></span>

<span data-ttu-id="6941f-128">Du kan enten opprette et nytt fragment eller lagre en eksisterende modulkonfigurasjon som et fragment.</span><span class="sxs-lookup"><span data-stu-id="6941f-128">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="6941f-129">Lagre en eksisterende modulkonfigurasjon som et fragment</span><span class="sxs-lookup"><span data-stu-id="6941f-129">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="6941f-130">Følg denne fremgangsmåten for å konvertere en tidligere konfigurert modul til et fragment i Commerce-områdebyggeren som kan brukes på nytt.</span><span class="sxs-lookup"><span data-stu-id="6941f-130">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6941f-131">Åpne en side eller mal som inneholder modulen du vil konvertere til et fragment.</span><span class="sxs-lookup"><span data-stu-id="6941f-131">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="6941f-132">I disposisjonsruten til venstre eller direkte i den visuelle sidebyggeren, velger du den tidligere konfigurerte modulen.</span><span class="sxs-lookup"><span data-stu-id="6941f-132">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="6941f-133">Velg ellipsen (**...**) ved siden av navnet på modulen enten i disposisjonsruten eller den valgte modulens verktøylinje i den visuelle sidebyggeren.</span><span class="sxs-lookup"><span data-stu-id="6941f-133">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="6941f-134">Velg **Del som fragment**.</span><span class="sxs-lookup"><span data-stu-id="6941f-134">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="6941f-135">I dialogboksen **Lagre som fragment** angir du et navn på fragmentet.</span><span class="sxs-lookup"><span data-stu-id="6941f-135">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="6941f-136">Velg **OK** for å lagre modulkonfigurasjonen som et fragment som kan legges til andre sider.</span><span class="sxs-lookup"><span data-stu-id="6941f-136">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="6941f-137">Opprett et nytt fragment</span><span class="sxs-lookup"><span data-stu-id="6941f-137">Create a new fragment</span></span>

<span data-ttu-id="6941f-138">Følg denne fremgangsmåten for å opprette et nytt fragment i Commerce-områdebygger.</span><span class="sxs-lookup"><span data-stu-id="6941f-138">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6941f-139">Velg **Fragmenter** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="6941f-139">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="6941f-140">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6941f-140">Select **New**.</span></span> <span data-ttu-id="6941f-141">Det vises en dialogboks **Nytt fragment** som viser alle de tilgjengelige modultypene.</span><span class="sxs-lookup"><span data-stu-id="6941f-141">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="6941f-142">Som ble nevnt tidligere kan fragmenter opprettes fra en hvilken som helst modultype.</span><span class="sxs-lookup"><span data-stu-id="6941f-142">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="6941f-143">Velg en modultype for fragmentet.</span><span class="sxs-lookup"><span data-stu-id="6941f-143">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="6941f-144">Når du velger en generisk containermodultype, får du størst fleksibilitet når du må oppdatere og konfigurere fragmentet senere.</span><span class="sxs-lookup"><span data-stu-id="6941f-144">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="6941f-145">Legge til, fjerne eller redigere fragmenter på en side</span><span class="sxs-lookup"><span data-stu-id="6941f-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="6941f-146">Følgende prosedyrer beskriver hvordan du legger til, fjerner eller redigerer fragmenter.</span><span class="sxs-lookup"><span data-stu-id="6941f-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="6941f-147">Legg til et fragment</span><span class="sxs-lookup"><span data-stu-id="6941f-147">Add a fragment</span></span>

<span data-ttu-id="6941f-148">Følg denne fremgangsmåten for å legge til et fragment i en side i Commerce-områdebygger.</span><span class="sxs-lookup"><span data-stu-id="6941f-148">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6941f-149">I disposisjonsruten til venstre eller direkte i den visuelle sidebyggeren, velger du en container eller et spor der underordnede moduler kan legges til.</span><span class="sxs-lookup"><span data-stu-id="6941f-149">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="6941f-150">Velg ellipsen (**...**) ved siden av navnet på containeren eller sporet.</span><span class="sxs-lookup"><span data-stu-id="6941f-150">Select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="6941f-151">Hvis du bruker den visuelle sidebyggeren, kan du eventuelt velge plusstegnet (**+**).</span><span class="sxs-lookup"><span data-stu-id="6941f-151">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="6941f-152">Velg **Legg til fragment**.</span><span class="sxs-lookup"><span data-stu-id="6941f-152">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="6941f-153">Hvis containeren eller sporet ikke støtter nye underordnede moduler, er alternativet **Legg til fragment** ikke tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="6941f-153">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="6941f-154">Søk etter og velg et fragment du vil legge til, i dialogboksen **Velg fragment**.</span><span class="sxs-lookup"><span data-stu-id="6941f-154">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="6941f-155">Hvis det ikke finnes noen tilgjengelige fragmenter, kan det være at du først må opprette et fragment fra en modultype som valgt container eller spor støtter.</span><span class="sxs-lookup"><span data-stu-id="6941f-155">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="6941f-156">Velg det ønskede fragmentet for å legge det til i containeren eller sporet på siden.</span><span class="sxs-lookup"><span data-stu-id="6941f-156">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="6941f-157">Modulene som er tillatt i en container eller et spor, er definert av malen for siden eller modulenes egne definisjoner.</span><span class="sxs-lookup"><span data-stu-id="6941f-157">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="6941f-158">Fjerne et fragment</span><span class="sxs-lookup"><span data-stu-id="6941f-158">Remove a fragment</span></span>

<span data-ttu-id="6941f-159">Hvis du vil fjerne et fragment fra et spor eller en container på en side i Commerce-områdebyggeren, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="6941f-159">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6941f-160">I disposisjonsruten til venstre velger du ellipsen (**...**) ved siden av navnet på fragmentet som skal fjernes, og deretter velger du papirkurvsymbolet.</span><span class="sxs-lookup"><span data-stu-id="6941f-160">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="6941f-161">Du kan også velge fragmentet i den visuelle sidebyggeren og velge papirkurvsymbolet på verktøylinjen til fragmentet.</span><span class="sxs-lookup"><span data-stu-id="6941f-161">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="6941f-162">Når du blir bedt om å bekrefte at du vil fjerne fragmentet, velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="6941f-162">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="6941f-163">Når du fjerner et fragment fra en side, fjerner du bare referansen til det fra den siden.</span><span class="sxs-lookup"><span data-stu-id="6941f-163">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="6941f-164">Du sletter **ikke** fragmentet fra området ditt.</span><span class="sxs-lookup"><span data-stu-id="6941f-164">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="6941f-165">Hvis du vil slette fragmenter fra området, må du bruke brukergrensesnittet for fragmentinspeksjonen.</span><span class="sxs-lookup"><span data-stu-id="6941f-165">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="6941f-166">Du kan bare slette fragmenter fra et område hvis de ikke er referert til av sider, maler eller andre fragmenter.</span><span class="sxs-lookup"><span data-stu-id="6941f-166">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="6941f-167">Redigere et fragment</span><span class="sxs-lookup"><span data-stu-id="6941f-167">Edit a fragment</span></span>

<span data-ttu-id="6941f-168">Hvis du vil redigere fragmenter, må du bruke brukergrensesnittet for fragmentredigering.</span><span class="sxs-lookup"><span data-stu-id="6941f-168">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="6941f-169">Denne begrensningen er standard.</span><span class="sxs-lookup"><span data-stu-id="6941f-169">This restriction is by design.</span></span> <span data-ttu-id="6941f-170">Den hjelper til med å garantere at forfattere ikke forveksler prosessen med å redigere modulene for en bestemt side med prosessen med å redigere fragmenter som kan deles på mange sider.</span><span class="sxs-lookup"><span data-stu-id="6941f-170">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="6941f-171">Følg denne fremgangsmåten for å redigere et nytt fragment i Commerce-områdebygger.</span><span class="sxs-lookup"><span data-stu-id="6941f-171">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6941f-172">Velg **Fragmenter** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="6941f-172">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="6941f-173">Under **Fragmenter** velger du fragmentet du vil redigere.</span><span class="sxs-lookup"><span data-stu-id="6941f-173">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="6941f-174">Rediger fragmentets modulegenskaper og struktur etter behov.</span><span class="sxs-lookup"><span data-stu-id="6941f-174">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="6941f-175">Prosessen ligner på redigeringsprosessen for moduler som redigeres i sideredigeringsvisning.</span><span class="sxs-lookup"><span data-stu-id="6941f-175">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="6941f-176">Du kan også redigere et fragment ved å velge det på en side, i en mal, eller i et overordnet fragment, og deretter velge **Rediger fragment** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="6941f-176">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6941f-177">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6941f-177">Additional resources</span></span>

[<span data-ttu-id="6941f-178">Oversikt over maler og oppsett</span><span class="sxs-lookup"><span data-stu-id="6941f-178">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="6941f-179">Arbeide med maler</span><span class="sxs-lookup"><span data-stu-id="6941f-179">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="6941f-180">Arbeide med forhåndsinnstilte oppsett</span><span class="sxs-lookup"><span data-stu-id="6941f-180">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="6941f-181">Arbeide med publiseringsgrupper</span><span class="sxs-lookup"><span data-stu-id="6941f-181">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
