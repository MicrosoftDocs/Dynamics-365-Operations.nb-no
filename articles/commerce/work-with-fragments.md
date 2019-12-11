---
title: Arbeide med fragmenter
description: Dette emnet beskriver hvorfor, når og hvordan du bruker fragmenter i Microsoft Dynamics 365 Commerce.
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
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d92b9077f8584bfa0710bbaacbc7caa3220baa4a
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698102"
---
# <a name="work-with-fragments"></a><span data-ttu-id="bd2f8-103">Arbeide med fragmenter</span><span class="sxs-lookup"><span data-stu-id="bd2f8-103">Work with fragments</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="bd2f8-104">Dette emnet beskriver hvorfor, når og hvordan du bruker fragmenter i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bd2f8-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="bd2f8-105">Overview</span></span>

<span data-ttu-id="bd2f8-106">Fragmenter muliggjør en sentralisert redigeringsopplevelse for modulkonfigurasjoner som må brukes på nytt på hele området.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="bd2f8-107">Topptekst, bunntekst og bannere er for eksempel ofte konfigurert som fragmenter, fordi de deles på tvers av mange sider.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="bd2f8-108">Du kan betrakte fragmenter som små websider som kan settes inn i andre sider på området.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="bd2f8-109">Fragmenter har sin egen livssyklus.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="bd2f8-110">De opprettes, refereres til, oppdateres og slettet med andre ord som uavhengige enheter i redigeringsverktøyene.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="bd2f8-111">Når fragmentene er konfigurert, kan de brukes overalt der moduler kan brukes i områdestrukturen.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="bd2f8-112">Fragmenter kan refereres til på sider, i oppsett, i maler og i andre fragmenter.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="bd2f8-113">Fragmenter kan nestes opp til sju nivåer i andre fragmenter.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="bd2f8-114">Hvis du for eksempel vil fremme en sesonghendelse på mange sider på området, kan du bruke et fragment.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="bd2f8-115">Det første trinnet i prosessen med å opprette et nytt fragment er å velge typen modul du vil starte fra.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="bd2f8-116">I dette eksemplet kan du bygge fragmentet fra en hovedbannermodul.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="bd2f8-117">Fragmenter kan bygges fra en hvilken som helst modultype.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="bd2f8-118">Du kan deretter konfigurere hovedbannerfragmentet med ditt bestemte kampanjeinnhold.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="bd2f8-119">Du kan også lokalisere den slik du ønsker.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-119">You can also localize it as you require.</span></span> <span data-ttu-id="bd2f8-120">Det nye fritt stående hovedbannerfragmentet kan deretter brukes som en forhåndskonfigurert modul i området.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="bd2f8-121">Det er enkelt å legge den til i maler, til bestemte sider eller til andre fragmenter som kan inneholde hovedbannermoduler.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="bd2f8-122">Alle steder der fragmentet legges til, er referanser til det sentrale hovedbannerfragmentet du opprettet.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="bd2f8-123">Hvis du publiserer endringer i fragmentet, vises disse endringene umiddelbart på alle steder der fragmentet blir referert på tvers av området.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="bd2f8-124">Fragmenter kan derfor være en virkningsfull og effektiv måte å bruke modulkonfigurasjoner på nytt og administrere modulkonfigurasjoner på et område sentralt.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="bd2f8-125">Ved å bruke dem på en effektiv måte kan du øke allsidigheten betraktelig og redusere kostnadene som er knyttet til administrasjon av områdeinnhold.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="bd2f8-126">Illustrasjonen nedenfor viser hvordan fragmenter kan brukes til å sentralisere redigering av delte modulkonfigurasjoner på tvers av et e-handelsområde.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![En illustrasjon som viser hvordan fragmenter kan brukes til å sentralisere redigering av delte modulkonfigurasjoner på tvers av et e-handelsområde.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="bd2f8-128">Opprette et fragment</span><span class="sxs-lookup"><span data-stu-id="bd2f8-128">Create a fragment</span></span>

<span data-ttu-id="bd2f8-129">Du kan enten opprette et nytt fragment eller lagre en eksisterende modulkonfigurasjon som et fragment.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="create-a-new-fragment"></a><span data-ttu-id="bd2f8-130">Opprette et nytt fragment</span><span class="sxs-lookup"><span data-stu-id="bd2f8-130">Create a new fragment</span></span>

<span data-ttu-id="bd2f8-131">Hvis du vil opprette en nytt fragment, følger du trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-131">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="bd2f8-132">Velg **Fragmenter**i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-132">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="bd2f8-133">Velg **Nytt sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-133">Select **New Page Fragment**.</span></span> <span data-ttu-id="bd2f8-134">Det vises en dialogboks som viser alle de tilgjengelige modultypene.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-134">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="bd2f8-135">Som ble nevnt tidligere kan fragmenter opprettes fra en hvilken som helst modultype.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-135">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="bd2f8-136">Velg en modultype for fragmentet, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-136">Select a module type for your fragment, and then select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="bd2f8-137">Når du velger en generisk containermodultype, får du størst fleksibilitet når du må oppdatere og konfigurere fragmentet senere.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-137">By selecting a generic container module type, you get the most flexibility when you must update and configure your fragment later.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="bd2f8-138">Lagre en eksisterende modulkonfigurasjon som et fragment</span><span class="sxs-lookup"><span data-stu-id="bd2f8-138">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="bd2f8-139">Følg denne fremgangsmåten for å konvertere en tidligere konfigurert modul til et fragment som kan brukes på nytt.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-139">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="bd2f8-140">Åpne en side eller mal som inneholder modulen du vil konvertere til et fragment.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-140">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="bd2f8-141">I disposisjonsruten til venstre velger du ellipseknappen (**...**) ved siden av navnet på modulen, og deretter velger du **Lagre som fragment**.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-141">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module, and then select **Save as Fragment**.</span></span> <span data-ttu-id="bd2f8-142">En dialogboks vises.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-142">A dialog box appears.</span></span>
1. <span data-ttu-id="bd2f8-143">Angi et navn og metadata for fragmentet.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-143">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="bd2f8-144">Velg **OK** for å lagre modulkonfigurasjonen som et fragment som kan legges til andre sider.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-144">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="bd2f8-145">Legge til, fjerne eller redigere fragmenter på en side</span><span class="sxs-lookup"><span data-stu-id="bd2f8-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="bd2f8-146">Følgende prosedyrer beskriver hvordan du legger til, fjerner eller redigerer fragmenter.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="bd2f8-147">Legg til et fragment</span><span class="sxs-lookup"><span data-stu-id="bd2f8-147">Add a fragment</span></span>

<span data-ttu-id="bd2f8-148">Hvis du vil legge til et fragment på en side, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-148">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="bd2f8-149">I disposisjonsruten til venstre velger du en container eller et spor som underordnede moduler kan legges til i.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-149">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="bd2f8-150">Velg ellipseknappen ved siden av navnet på containeren eller sporet, og velg deretter **Legg til fragment**.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-150">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="bd2f8-151">En dialogboks vises.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-151">A dialog box appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bd2f8-152">Hvis containeren eller sporet ikke støtter nye underordnede moduler, er alternativet **Legg til fragment** ikke tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-152">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>

1. <span data-ttu-id="bd2f8-153">Søk etter og velg et fragment du vil legge til, i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-153">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="bd2f8-154">Hvis det ikke finnes noen tilgjengelige fragmenter, kan det være at du først må opprette et fragment fra en modultype som valgt container eller spor støtter.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-154">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="bd2f8-155">Velg **OK** for å legge det valgte fragmentet til valgt container eller spor på siden.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-155">Select **OK** to add the selected fragment to the selected container or slot on your page.</span></span>

> [!NOTE]
> <span data-ttu-id="bd2f8-156">Modulene som er tillatt i en container eller et spor, er definert av malen for siden eller modulenes egne definisjoner.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-156">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="bd2f8-157">Fjerne et fragment</span><span class="sxs-lookup"><span data-stu-id="bd2f8-157">Remove a fragment</span></span>

<span data-ttu-id="bd2f8-158">Følg disse trinnene for å fjerne et fragment fra sporet eller containeren på en side.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-158">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="bd2f8-159">I disposisjonsruten til venstre velger du ellipseknappen ved siden av navnet på fragmentet som skal fjernes, og deretter velger du papirkurvknappen.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-159">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="bd2f8-160">Når du blir bedt om å bekrefte at du vil fjerne fragmentet, velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-160">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="bd2f8-161">Når du fjerner et fragment fra en side, fjerner du bare referansen til det fra den siden.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-161">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="bd2f8-162">Du sletter **ikke** fragmentet fra området ditt.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-162">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="bd2f8-163">Hvis du vil slette fragmenter fra området, må du bruke brukergrensesnittet for fragmentinspeksjonen.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-163">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="bd2f8-164">Du kan bare slette fragmenter fra et område hvis de ikke er referert til av sider, maler eller andre fragmenter.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-164">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="bd2f8-165">Redigere et fragment</span><span class="sxs-lookup"><span data-stu-id="bd2f8-165">Edit a fragment</span></span>

<span data-ttu-id="bd2f8-166">Hvis du vil redigere fragmenter, må du bruke brukergrensesnittet for fragmentredigering.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-166">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="bd2f8-167">Denne begrensningen er standard.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-167">This restriction is by design.</span></span> <span data-ttu-id="bd2f8-168">Den hjelper til med å garantere at forfattere ikke forveksler prosessen med å redigere modulene for en bestemt side med prosessen med å redigere fragmenter som kan deles på mange sider.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-168">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="bd2f8-169">Hvis du vil redigere et fragment, følger du trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-169">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="bd2f8-170">Velg **Fragmenter**i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-170">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="bd2f8-171">Under **Fragmenter** velger du fragmentet du vil redigere.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-171">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="bd2f8-172">Rediger fragmentets modulegenskaper og struktur etter behov.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-172">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="bd2f8-173">Prosessen ligner på redigeringsprosessen for moduler som redigeres i sideredigeringsvisning.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-173">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="bd2f8-174">Du kan også redigere et fragment ved å velge det på en side, i en mal, eller i et overordnet fragment, og deretter velge **Rediger fragment** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="bd2f8-174">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bd2f8-175">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="bd2f8-175">Additional resources</span></span>

[<span data-ttu-id="bd2f8-176">Oversikt over maler og oppsett</span><span class="sxs-lookup"><span data-stu-id="bd2f8-176">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="bd2f8-177">Arbeide med maler</span><span class="sxs-lookup"><span data-stu-id="bd2f8-177">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="bd2f8-178">Arbeide med forhåndsinnstilte oppsett</span><span class="sxs-lookup"><span data-stu-id="bd2f8-178">Work with preset layouts</span></span>](work-with-layouts.md)
