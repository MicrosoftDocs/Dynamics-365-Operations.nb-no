---
title: Arbeide med moduler
description: Dette emnet beskriver hvordan og når du bruker moduler i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 09/15/2020
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
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 301eb6206fb9e02c3aa7d3c07cf368ba800a1ab9
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818428"
---
# <a name="work-with-modules"></a><span data-ttu-id="86bd9-103">Arbeide med moduler</span><span class="sxs-lookup"><span data-stu-id="86bd9-103">Work with modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="86bd9-104">Dette emnet beskriver hvordan og når du bruker moduler i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="86bd9-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="86bd9-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="86bd9-105">Overview</span></span>

<span data-ttu-id="86bd9-106">Moduler er logiske byggeblokker som utgjør sidestrukturen, og de har forskjellige formål og omfang.</span><span class="sxs-lookup"><span data-stu-id="86bd9-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="86bd9-107">Noen moduler er containere på høyt nivå, og det eneste formålet er å oppbevare og organisere andre moduler (underordnede moduler).</span><span class="sxs-lookup"><span data-stu-id="86bd9-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="86bd9-108">Andre moduler, for eksempel en enkel bildeplasseringsmodul, har et svært bestemt formål.</span><span class="sxs-lookup"><span data-stu-id="86bd9-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="86bd9-109">Andre moduler, for eksempel en karusellmodul, faller et sted mellom disse to kategoriene.</span><span class="sxs-lookup"><span data-stu-id="86bd9-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="86bd9-110">Som standard inneholder Dynamics 365 Commerce-området et modulbibliotek som lar deg utføre de mest grunnleggende e-handelsscenarioene.</span><span class="sxs-lookup"><span data-stu-id="86bd9-110">By default, your Dynamics 365 Commerce site includes a module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="86bd9-111">Du skal kunne konstruere et ende-til-ende-område for e-handel bare ved å bruke disse modulene.</span><span class="sxs-lookup"><span data-stu-id="86bd9-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="86bd9-112">Det kan imidlertid hende at du også vil tilpasse disse modulene eller bygge nye, tilpassede moduler for bestemte behov.</span><span class="sxs-lookup"><span data-stu-id="86bd9-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="86bd9-113">Hvis du vil bygge egendefinerte moduler, er en modul-SDK (Software Development Kit) tilgjengelig slik at du kan opprette et egendefinert modulbibliotek.</span><span class="sxs-lookup"><span data-stu-id="86bd9-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="86bd9-114">Containermoduler og -spor</span><span class="sxs-lookup"><span data-stu-id="86bd9-114">Container modules and slots</span></span>

<span data-ttu-id="86bd9-115">Som nevnt tidligere er noen moduler utformet for å inneholde underordnede moduler.</span><span class="sxs-lookup"><span data-stu-id="86bd9-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="86bd9-116">Disse modulene kalles *containere* og tillater hierarkier av nestede moduler.</span><span class="sxs-lookup"><span data-stu-id="86bd9-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="86bd9-117">Containermoduler inneholder *spor*.</span><span class="sxs-lookup"><span data-stu-id="86bd9-117">Container modules include *slots*.</span></span> <span data-ttu-id="86bd9-118">Spor brukes til å håndtere oppsettet og formålet med underordnede moduler i containeren.</span><span class="sxs-lookup"><span data-stu-id="86bd9-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="86bd9-119">Et eksempel er en grunnleggende sidecontainermodul (en modul på øverste nivå for alle sider) som definerer flere viktige spor:</span><span class="sxs-lookup"><span data-stu-id="86bd9-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="86bd9-120">Et overskriftsspor</span><span class="sxs-lookup"><span data-stu-id="86bd9-120">A header slot</span></span>
- <span data-ttu-id="86bd9-121">Et underoverskriftsspor</span><span class="sxs-lookup"><span data-stu-id="86bd9-121">A sub-header slot</span></span>
- <span data-ttu-id="86bd9-122">Et hovedspor</span><span class="sxs-lookup"><span data-stu-id="86bd9-122">A main slot</span></span>
- <span data-ttu-id="86bd9-123">Et bunntekstspor</span><span class="sxs-lookup"><span data-stu-id="86bd9-123">A footer slot</span></span>
- <span data-ttu-id="86bd9-124">Et underbunntekstsspor</span><span class="sxs-lookup"><span data-stu-id="86bd9-124">A sub-footer slot</span></span>

<span data-ttu-id="86bd9-125">Utvikleren av modulen definerer disse sporene og bestemmer hvilke underordnede moduler og hvor mange underordnede moduler som kan plasseres direkte i den.</span><span class="sxs-lookup"><span data-stu-id="86bd9-125">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="86bd9-126">Overskriftssporet kan for eksempel støtte bare én modul av typen **Topptekst**, mens brødtekstsporet kan støtte et ubegrenset antall moduler av alle typer (bortsett fra andre sidecontainermoduler).</span><span class="sxs-lookup"><span data-stu-id="86bd9-126">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="86bd9-127">I redigeringsverktøyene trenger ikke sideforfattere å vite på forhånd hvilke moduler som kan og ikke kan legges i hvert spor.</span><span class="sxs-lookup"><span data-stu-id="86bd9-127">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="86bd9-128">Når sideforfattere velger et spor, og deretter prøver å velge en modul som skal legges til, vil de se en filtrert visning av modultyper som støttes for dette sporet.</span><span class="sxs-lookup"><span data-stu-id="86bd9-128">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="86bd9-129">Innholdsmoduler</span><span class="sxs-lookup"><span data-stu-id="86bd9-129">Content modules</span></span>

<span data-ttu-id="86bd9-130">Innholdsmoduler inneholder innholds- og medieelementer, for eksempel tekst (f.eks. overskrifter, avsnitt og koblinger) eller aktivareferanser (for eksempel bilder, videoer og PDF-filer).</span><span class="sxs-lookup"><span data-stu-id="86bd9-130">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="86bd9-131">Vanlige innholdsmodultyper inkluderer moduler for innholdsblokk, tekstblokk og promobanner.</span><span class="sxs-lookup"><span data-stu-id="86bd9-131">Typical content module types include content block, text block, and promo banner modules.</span></span> <span data-ttu-id="86bd9-132">Moduler av disse tre typene kan inneholde tekst eller medier, og de krever ingen underordnede moduler for å gjøre noe synlig på en side.</span><span class="sxs-lookup"><span data-stu-id="86bd9-132">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="86bd9-133">De fleste av de typiske, daglige side- og innholdsredigeringsaktivitetene omfatter innholdsmoduler, først og fremst siden disse modulene definerer det faktiske innholdet som gjengis i de overordnede containermodulene.</span><span class="sxs-lookup"><span data-stu-id="86bd9-133">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="86bd9-134">Mange innholdsmoduler er tilgjengelige, og disse modulene er vanligvis de siste brikkene du legger til i sidehierarkiet for nestede moduler.</span><span class="sxs-lookup"><span data-stu-id="86bd9-134">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="86bd9-135">Illustrasjonen nedenfor viser hvordan moduler er nestet i overordnede containermodulspor.</span><span class="sxs-lookup"><span data-stu-id="86bd9-135">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Neste moduler](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="86bd9-137">Legge til eller fjerne moduler</span><span class="sxs-lookup"><span data-stu-id="86bd9-137">Add or remove modules</span></span>

<span data-ttu-id="86bd9-138">Følgende prosedyrer beskriver hvordan du legger til og fjerner moduler.</span><span class="sxs-lookup"><span data-stu-id="86bd9-138">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="86bd9-139">Legge til en modul</span><span class="sxs-lookup"><span data-stu-id="86bd9-139">Add a module</span></span>

<span data-ttu-id="86bd9-140">Følg disse trinnene for å legge til en modul i et spor eller en container på en side.</span><span class="sxs-lookup"><span data-stu-id="86bd9-140">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="86bd9-141">I disposisjonsruten til venstre eller direkte på hovedlerretet velger du en container eller et spor der en underordnet modul kan legges til.</span><span class="sxs-lookup"><span data-stu-id="86bd9-141">In the outline pane on the left or directly in the main canvas, select a container or slot to which a child module can be added.</span></span>

    > [!NOTE]
    > <span data-ttu-id="86bd9-142">Modulutforming definerer listen over modultyper som kan legges til i et bestemt modulspor.</span><span class="sxs-lookup"><span data-stu-id="86bd9-142">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="86bd9-143">Malredigerere kan deretter forbedre de tillatte modulalternativene for å sikre konsekvent søkemotoroptimalisering (SEO) og administrasjonseffektivitet for alle sidene som er bygget fra en bestemt mal.</span><span class="sxs-lookup"><span data-stu-id="86bd9-143">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages that are built from a specific template.</span></span> <span data-ttu-id="86bd9-144">Når du legger til en modul for et spor, blir dialogboksen **Legg til modul** automatisk filtrert, slik at den bare viser moduler som støttes i valgt container eller spor.</span><span class="sxs-lookup"><span data-stu-id="86bd9-144">When adding a module to a slot, the **Add Module** dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="86bd9-145">Denne listen over tillatte moduler bestemmes av sidens mal eller containermoduldefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="86bd9-145">This list of allowed modules is determined by the page's template or the container's module definition.</span></span>

1. <span data-ttu-id="86bd9-146">Hvis du bruker disposisjonsruten, velger du ellipsen (**...**) ved siden av modulnavnet, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="86bd9-146">If using the outline pane, select the ellipsis (**...**) next to the module name, and then select **Add Module**.</span></span> <span data-ttu-id="86bd9-147">Hvis du bruker kontrollene direkte i lerretet, velger du plusstegnet (**+**) i et tomt spor eller ved siden av den valgte modulen, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="86bd9-147">If using the controls directly within the canvas, select the plus symbol (**+**) in an empty slot or adjacent to the currently selected module, and then select **Add Module**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="86bd9-148">Hvis en container eller et spor ikke støtter nye underordnede moduler, er alternativet **Legg til modul** ikke tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="86bd9-148">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="86bd9-149">Velg en modul du vil legge til på siden, i dialogboksen **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="86bd9-149">In the **Add Module** dialog box, select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="86bd9-150">**Innholdsblokk** er en god modultype for nybegynnere til å arbeide med.</span><span class="sxs-lookup"><span data-stu-id="86bd9-150">**Content block** is a good module type for beginners to work with.</span></span>

1. <span data-ttu-id="86bd9-151">Velg **OK** for å legge den valgte modulen til valgt container eller spor på siden.</span><span class="sxs-lookup"><span data-stu-id="86bd9-151">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="86bd9-152">Fjerne en modul</span><span class="sxs-lookup"><span data-stu-id="86bd9-152">Remove a module</span></span>

<span data-ttu-id="86bd9-153">Følg disse trinnene for å fjerne en modul fra sporet eller containeren på en side.</span><span class="sxs-lookup"><span data-stu-id="86bd9-153">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="86bd9-154">I disposisjonsruten til venstre velger du ellipsen (**...**) ved siden av navnet på modulen som skal fjernes, og deretter velger du papirkurvsymbolet.</span><span class="sxs-lookup"><span data-stu-id="86bd9-154">In the outline pane on the left, select the ellipsis (**...**) next to the name of the module to be removed, and then select the trash can symbol.</span></span> <span data-ttu-id="86bd9-155">På hovedlerretet kan du også velge papirkurvsymbolet på verktøylinjen i en valgt modul.</span><span class="sxs-lookup"><span data-stu-id="86bd9-155">Alternately, in the main canvas you can select the trash can symbol on a selected module's toolbar.</span></span>
1. <span data-ttu-id="86bd9-156">Når du blir bedt om å bekrefte at du vil fjerne modulen, velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="86bd9-156">When prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="move-a-module-to-a-new-position"></a><span data-ttu-id="86bd9-157">Flytte en modul til en ny posisjon</span><span class="sxs-lookup"><span data-stu-id="86bd9-157">Move a module to a new position</span></span>

<span data-ttu-id="86bd9-158">Hvis du vil flytte en modul til en ny plassering på siden, kan du bruke en av følgende metoder.</span><span class="sxs-lookup"><span data-stu-id="86bd9-158">To move a module to a new position within your page, use any of the following methods.</span></span>

### <a name="move-a-module-using-the-outline-pane"></a><span data-ttu-id="86bd9-159">Flytte en modul ved hjelp av disposisjonsruten</span><span class="sxs-lookup"><span data-stu-id="86bd9-159">Move a module using the outline pane</span></span>

<span data-ttu-id="86bd9-160">Følg denne fremgangsmåten for å flytte en modul ved hjelp av disposisjonsruten.</span><span class="sxs-lookup"><span data-stu-id="86bd9-160">To move a module using the outline pane, follow these steps.</span></span>

1. <span data-ttu-id="86bd9-161">Velg og hold modulen du vil flytte, i disposisjonsruten, og dra deretter modulen til en ny posisjon i disposisjonen.</span><span class="sxs-lookup"><span data-stu-id="86bd9-161">Select and hold the module you want to move in the outline pane, then drag the module to a new position in the outline.</span></span> <span data-ttu-id="86bd9-162">Den blå linjen i disposisjonen og på lerretet viser hvor modulen kan plasseres.</span><span class="sxs-lookup"><span data-stu-id="86bd9-162">The blue line in the outline and on the canvas indicates where the module can be placed.</span></span>
1. <span data-ttu-id="86bd9-163">Frigi modulen for å slippe den i den nye stillingen.</span><span class="sxs-lookup"><span data-stu-id="86bd9-163">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-directly-within-the-canvas"></a><span data-ttu-id="86bd9-164">Flytte en modul direkte på lerretet</span><span class="sxs-lookup"><span data-stu-id="86bd9-164">Move a module directly within the canvas</span></span>

<span data-ttu-id="86bd9-165">Følg denne fremgangsmåten for å flytte en modul direkte ved hjelp av lerretet.</span><span class="sxs-lookup"><span data-stu-id="86bd9-165">To move a module directly within the canvas, follow these steps.</span></span>

1. <span data-ttu-id="86bd9-166">Velg modulen du vil flytte, på lerretet.</span><span class="sxs-lookup"><span data-stu-id="86bd9-166">Select the module you want to move in the canvas.</span></span> 
1. <span data-ttu-id="86bd9-167">Velg et pilsymbol som peker oppover eller nedover på verktøylinjen for modulen, og dra deretter pilen til en ny plassering på siden.</span><span class="sxs-lookup"><span data-stu-id="86bd9-167">Select either an upward or downward pointing arrow symbol in the module's toolbar, and then drag the arrow to a new position on the page.</span></span> <span data-ttu-id="86bd9-168">Den blå linjen på lerretet og i disposisjonen viser hvor modulen kan plasseres.</span><span class="sxs-lookup"><span data-stu-id="86bd9-168">The blue line in the canvas and outline indicates where the module can be placed.</span></span> <span data-ttu-id="86bd9-169">Hvis en modul ikke kan flyttes opp eller ned, vil dette pilsymbolet være nedtonet.</span><span class="sxs-lookup"><span data-stu-id="86bd9-169">If a module cannot be moved up or down, that arrow symbol will be grayed out.</span></span> 
1. <span data-ttu-id="86bd9-170">Frigi modulen for å slippe den i den nye stillingen.</span><span class="sxs-lookup"><span data-stu-id="86bd9-170">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-using-the-ellipsis-menu"></a><span data-ttu-id="86bd9-171">Flytte en modul ved hjelp av ellipsemenyen</span><span class="sxs-lookup"><span data-stu-id="86bd9-171">Move a module using the ellipsis menu</span></span>

<span data-ttu-id="86bd9-172">Følg denne fremgangsmåten for å flytte en modul ved hjelp av ellipsemenyen.</span><span class="sxs-lookup"><span data-stu-id="86bd9-172">To move a module using the ellipsis menu, follow these steps.</span></span>

1. <span data-ttu-id="86bd9-173">Velg en modul enten i disposisjonen eller på lerretet.</span><span class="sxs-lookup"><span data-stu-id="86bd9-173">Select a module in either the outline or the canvas.</span></span>
1. <span data-ttu-id="86bd9-174">Velg ellipsen (**...**) ved siden av modulens navn i disposisjonsruten eller modulens verktøylinje i lerretet.</span><span class="sxs-lookup"><span data-stu-id="86bd9-174">Select the ellipsis (**...**) next to the module's name in the outline pane, or in the module's toolbar in the canvas.</span></span>
1. <span data-ttu-id="86bd9-175">Hvis modulen kan flyttes opp eller ned i containeren eller sporet, vil du se alternativer for **Flytt opp** eller **Flytt ned**.</span><span class="sxs-lookup"><span data-stu-id="86bd9-175">If the module can be moved up or down within the container or slot, you will see options for **Move up** or **Move down**.</span></span> <span data-ttu-id="86bd9-176">Velg ønsket flyttealternativ for å flytte modulen opp eller ned i forhold dens sideordnede elementer.</span><span class="sxs-lookup"><span data-stu-id="86bd9-176">Select the desired move option to move the module up or down relative to its siblings.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="86bd9-177">Konfigurere moduler</span><span class="sxs-lookup"><span data-stu-id="86bd9-177">Configure modules</span></span>

<span data-ttu-id="86bd9-178">Følgende prosedyrer beskriver hvordan du konfigurerer innhold og innholdsmoduler.</span><span class="sxs-lookup"><span data-stu-id="86bd9-178">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="86bd9-179">Konfigurere en innholdsmodul</span><span class="sxs-lookup"><span data-stu-id="86bd9-179">Configure a content module</span></span>

<span data-ttu-id="86bd9-180">Hvis du vil konfigurere en innholdsmodul på en side, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="86bd9-180">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="86bd9-181">I disposisjonsruten til venstre utvider du treet og velger en innholdsmodul (for eksempel **Innholdsblokk**).</span><span class="sxs-lookup"><span data-stu-id="86bd9-181">In the outline pane on the left, expand the tree and select any content module (for example, **Content block**).</span></span> <span data-ttu-id="86bd9-182">Du kan også velge modulen på hovedlerretet.</span><span class="sxs-lookup"><span data-stu-id="86bd9-182">Alternately, you can select the module in the main canvas.</span></span>
1. <span data-ttu-id="86bd9-183">Angi egenskaper for eventuelle modulkontroller i modulegenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="86bd9-183">In the module properties pane on the right, enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="86bd9-184">Velg **Lagre** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="86bd9-184">On the command bar, select **Save**.</span></span> <span data-ttu-id="86bd9-185">Dette vil også oppdatere forhåndsvisningslerretet.</span><span class="sxs-lookup"><span data-stu-id="86bd9-185">This will also refresh the preview canvas.</span></span>

### <a name="edit-module-text-properties"></a><span data-ttu-id="86bd9-186">Redigere tekstegenskaper for modul</span><span class="sxs-lookup"><span data-stu-id="86bd9-186">Edit module text properties</span></span>

<span data-ttu-id="86bd9-187">Tekstegenskaper for modul som ikke er skrivebeskyttet, kan redigeres direkte på lerretet.</span><span class="sxs-lookup"><span data-stu-id="86bd9-187">Module text properties that are not read-only can be edited directly in the canvas.</span></span>

<span data-ttu-id="86bd9-188">Følg denne fremgangs måten for å redigere tekstegenskaper for modul.</span><span class="sxs-lookup"><span data-stu-id="86bd9-188">To edit module text properties, follow these steps.</span></span>

1. <span data-ttu-id="86bd9-189">Merk tekstkontrollen på lerretet, og plasser deretter markøren der du vil redigere tekst.</span><span class="sxs-lookup"><span data-stu-id="86bd9-189">Select the text control in the canvas, then place your cursor where you wish to edit text.</span></span>
1. <span data-ttu-id="86bd9-190">Skriv inn tekstinnholdet.</span><span class="sxs-lookup"><span data-stu-id="86bd9-190">Enter your text content.</span></span>
1. <span data-ttu-id="86bd9-191">Merk hvor som helst utenfor tekstinnholdet for å fortsette å redigere annet innhold.</span><span class="sxs-lookup"><span data-stu-id="86bd9-191">Select anywhere outside the text content to continue editing other content.</span></span>

### <a name="inline-image-selection"></a><span data-ttu-id="86bd9-192">Valg av innebygd bilde</span><span class="sxs-lookup"><span data-stu-id="86bd9-192">Inline image selection</span></span>

<span data-ttu-id="86bd9-193">Modulbilder som ikke er skrivebeskyttet, kan endres direkte fra lerretet.</span><span class="sxs-lookup"><span data-stu-id="86bd9-193">Module images that are not read-only can be changed directly from the canvas.</span></span>

<span data-ttu-id="86bd9-194">Hvis du vil velge et nytt bilde for en innholdsmodul, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="86bd9-194">To choose a new image for a content module, follow these steps.</span></span>

1. <span data-ttu-id="86bd9-195">Dobbeltklikk bildet på lerretet.</span><span class="sxs-lookup"><span data-stu-id="86bd9-195">In the canvas, double-click the image.</span></span> <span data-ttu-id="86bd9-196">Dette henter frem medievelgervinduet.</span><span class="sxs-lookup"><span data-stu-id="86bd9-196">This will bring up the media picker window.</span></span>
1. <span data-ttu-id="86bd9-197">Finn og velg et nytt bilde som du vil bruke, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="86bd9-197">Find and select a new image you want to use, and then select **OK**.</span></span> <span data-ttu-id="86bd9-198">Det nye bildet vises nå på lerretet.</span><span class="sxs-lookup"><span data-stu-id="86bd9-198">The new image is now rendered in the canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="86bd9-199">Konfigurere en containermodul</span><span class="sxs-lookup"><span data-stu-id="86bd9-199">Configure a container module</span></span>

<span data-ttu-id="86bd9-200">Hvis du vil konfigurere en containermodul på en side, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="86bd9-200">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="86bd9-201">Velg en containermodul på siden (for eksempel en karusell eller en modul for flytende container).</span><span class="sxs-lookup"><span data-stu-id="86bd9-201">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="86bd9-202">I egenskapsruten til høyre utvider du de nestede kontrollene ved å velge overskriftene og angi eventuelle nødvendige kontrollverdier.</span><span class="sxs-lookup"><span data-stu-id="86bd9-202">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="86bd9-203">I disposisjonsruten til venstre velger du ellipseknappen ved siden av navnet på enten containeren eller eventuelle spor i containeren, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="86bd9-203">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="86bd9-204">Deretter legger du til underordnede moduler i den valgte containeren.</span><span class="sxs-lookup"><span data-stu-id="86bd9-204">Then, add child modules to the selected container.</span></span> <span data-ttu-id="86bd9-205">Hvis du ha mer informasjon, kan du se delen [Arbeide med moduler](#add-a-module) tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="86bd9-205">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="86bd9-206">Hvis det finnes flere underordnede moduler som sideordnede i en overordnet container, kan du endre visningsrekkefølgen i den overordnede containeren.</span><span class="sxs-lookup"><span data-stu-id="86bd9-206">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="86bd9-207">Velg ellipseknappen for en modul, og bruk deretter tastene for pil opp og pil ned.</span><span class="sxs-lookup"><span data-stu-id="86bd9-207">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86bd9-208">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="86bd9-208">Additional resources</span></span>

[<span data-ttu-id="86bd9-209">Oversikt over maler og oppsett</span><span class="sxs-lookup"><span data-stu-id="86bd9-209">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="86bd9-210">Arbeide med maler</span><span class="sxs-lookup"><span data-stu-id="86bd9-210">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="86bd9-211">Arbeide med forhåndsinnstilte oppsett</span><span class="sxs-lookup"><span data-stu-id="86bd9-211">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="86bd9-212">Arbeide med fragmenter</span><span class="sxs-lookup"><span data-stu-id="86bd9-212">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="86bd9-213">Legge til en containermodul på en side</span><span class="sxs-lookup"><span data-stu-id="86bd9-213">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="86bd9-214">Arbeide med publiseringsgrupper</span><span class="sxs-lookup"><span data-stu-id="86bd9-214">Work with publish groups</span></span>](publish-groups.md)

