---
title: Containermodul
description: Dette emnet dekker containermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 22a09b61fbe3bd1cca96011d3fb81a12ef1bc844
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697066"
---
# <a name="container-module"></a><span data-ttu-id="d882a-103">Containermodul</span><span class="sxs-lookup"><span data-stu-id="d882a-103">Container module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="d882a-104">Dette emnet dekker containermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d882a-104">This topic covers container modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d882a-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="d882a-105">Overview</span></span>

<span data-ttu-id="d882a-106">En containermodul er en modul som er vert for andre moduler i den.</span><span class="sxs-lookup"><span data-stu-id="d882a-106">A container module is a module that hosts other modules inside it.</span></span> <span data-ttu-id="d882a-107">Det er den mest generelle containeren som brukes i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d882a-107">It's the most generic container that is used in Dynamics 365 Commerce.</span></span> <span data-ttu-id="d882a-108">Hovedformålet med en containermodul er å definere, gjennom egenskapene som er angitt for den, oppsettet til modulene som er inni.</span><span class="sxs-lookup"><span data-stu-id="d882a-108">The primary purpose of a container module is to define, through the properties that are set for it, the layout of the modules that are inside.</span></span> <span data-ttu-id="d882a-109">Disse modulene kan for eksempel vises side ved side i et oppsett med to kolonner, tre kolonner, fire kolonner eller seks kolonner.</span><span class="sxs-lookup"><span data-stu-id="d882a-109">For example, those modules can appear side by side in a two-column, three-column, four-column, or six-column layout.</span></span> <span data-ttu-id="d882a-110">De kan også begrenses til bredden på containeren, eller de kan fylle skjermen.</span><span class="sxs-lookup"><span data-stu-id="d882a-110">They can also be limited to width of the container, or they can fill the screen.</span></span> <span data-ttu-id="d882a-111">En overskrift kan også legges til i hver containermodul.</span><span class="sxs-lookup"><span data-stu-id="d882a-111">A heading can also be added to every container module.</span></span>

<span data-ttu-id="d882a-112">Det finnes tre standardtyper containermoduler: container, container med 2 spor og container med 3 spor.</span><span class="sxs-lookup"><span data-stu-id="d882a-112">There are three standard types of container modules: container, container with 2-slots, and container with 3-slots.</span></span> <span data-ttu-id="d882a-113">Moduler av alle typer kan plasseres i disse containerne.</span><span class="sxs-lookup"><span data-stu-id="d882a-113">Modules of any type of module can be put inside these containers.</span></span> <span data-ttu-id="d882a-114">Det finnes også spesielle typer containermoduler, for eksempel karusell, innholdsrik blokk, innholdsplassering, handlekurv, kasse, kjøpsboks, topptekst og bunntekst.</span><span class="sxs-lookup"><span data-stu-id="d882a-114">There are also special types of container modules, such as carousel, content rich block, content placement, cart, checkout, buy box, header, and footer.</span></span> <span data-ttu-id="d882a-115">Disse containerne har bestemte formål, og bare bestemte typer moduler som støttes, kan plasseres inne i dem.</span><span class="sxs-lookup"><span data-stu-id="d882a-115">These containers have specific purposes, and only specific supported types of modules can be put inside them.</span></span>

<span data-ttu-id="d882a-116">Vi anbefaler at du plasserer moduler i en container, slik at de kan begrenses til bredden på containeren.</span><span class="sxs-lookup"><span data-stu-id="d882a-116">We recommend that you put modules inside a container, so that they can be limited to the width of the container.</span></span>

## <a name="examples-of-container-modules-in-e-commerce"></a><span data-ttu-id="d882a-117">Eksempler på containermoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="d882a-117">Examples of container modules in e-Commerce</span></span>

- <span data-ttu-id="d882a-118">En områdeforfatter vil ha et oppsett med tre kolonner, der tre moduler vises side om side.</span><span class="sxs-lookup"><span data-stu-id="d882a-118">A site author wants a three-column layout, where three modules appear side by side.</span></span> <span data-ttu-id="d882a-119">Derfor bruker områdeforfatteren en containermodul av containertypen med 3 spor.</span><span class="sxs-lookup"><span data-stu-id="d882a-119">Therefore, the site author uses a container module of the container with 3-slots type.</span></span>
- <span data-ttu-id="d882a-120">En områdeforfatter vil ha et oppsett med seks kolonner, der seks moduler vises side om side.</span><span class="sxs-lookup"><span data-stu-id="d882a-120">A site author wants a six-column layout, where six modules appear side by side.</span></span> <span data-ttu-id="d882a-121">Derfor bruker områdeforfatteren en container med containertypen med seks kolonner.</span><span class="sxs-lookup"><span data-stu-id="d882a-121">Therefore, the site author uses a container of the contain type that has six columns inside it.</span></span>
- <span data-ttu-id="d882a-122">En områdeforfatter vil legge en modul på en side, men vil ikke at den skal fylle skjermen.</span><span class="sxs-lookup"><span data-stu-id="d882a-122">A site author wants to put a module on a page but doesn't want it to fill the screen.</span></span> <span data-ttu-id="d882a-123">Derfor legger områdeforfatteren til modulen i en containermodul og setter containerens **Bredde**-egenskap til **Tilpass container**.</span><span class="sxs-lookup"><span data-stu-id="d882a-123">Therefore, the site author adds the module to a container module and sets the container's **Width** property to **Fit container**.</span></span>

## <a name="container-module-properties"></a><span data-ttu-id="d882a-124">Egenskaper for containermodul</span><span class="sxs-lookup"><span data-stu-id="d882a-124">Container module properties</span></span>

| <span data-ttu-id="d882a-125">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="d882a-125">Property name</span></span>     | <span data-ttu-id="d882a-126">Verdier</span><span class="sxs-lookup"><span data-stu-id="d882a-126">Values</span></span> | <span data-ttu-id="d882a-127">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d882a-127">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="d882a-128">Overskrift</span><span class="sxs-lookup"><span data-stu-id="d882a-128">Heading</span></span>           | <span data-ttu-id="d882a-129">Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="d882a-129">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="d882a-130">En valgfri overskrift kan angis for containeren.</span><span class="sxs-lookup"><span data-stu-id="d882a-130">An optional heading can be provided for the container.</span></span> <span data-ttu-id="d882a-131">Som standard brukes **H2**-overskriftskoden for overskriften.</span><span class="sxs-lookup"><span data-stu-id="d882a-131">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="d882a-132">Koden kan imidlertid endres for å oppfylle tilgjengelighetskravene.</span><span class="sxs-lookup"><span data-stu-id="d882a-132">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="d882a-133">Bredde</span><span class="sxs-lookup"><span data-stu-id="d882a-133">Width</span></span>             | <span data-ttu-id="d882a-134">**Tilpass container** eller **Fyll skjerm**</span><span class="sxs-lookup"><span data-stu-id="d882a-134">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="d882a-135">Hvis verdien er satt til **Tilpass container** (standardverdien), er modulene i containeren begrenset til bredden på containeren.</span><span class="sxs-lookup"><span data-stu-id="d882a-135">If the value is set to **Fit container** (the default value), the modules inside the container are limited to the width of the container.</span></span> <span data-ttu-id="d882a-136">Hvis verdien er satt til **Fyll skjerm**, er ikke modulene begrenset til containerbredden, men de kan fylle skjermen.</span><span class="sxs-lookup"><span data-stu-id="d882a-136">If the value is set to **Fill screen**, the modules aren't limited to the container width but can fill the screen.</span></span> |
| <span data-ttu-id="d882a-137">Antall kolonner</span><span class="sxs-lookup"><span data-stu-id="d882a-137">Number of columns</span></span> | <span data-ttu-id="d882a-138">**1**, **2**, **3**, **4**, **6** eller **12**</span><span class="sxs-lookup"><span data-stu-id="d882a-138">**1**, **2**, **3**, **4**, **6**, or **12**</span></span> | <span data-ttu-id="d882a-139">Denne egenskapen definerer antallet kolonner i containeren.</span><span class="sxs-lookup"><span data-stu-id="d882a-139">This property defines the number of columns in the container.</span></span> <span data-ttu-id="d882a-140">En container kan ha opptil 12 kolonner.</span><span class="sxs-lookup"><span data-stu-id="d882a-140">A container can have up to 12 columns.</span></span> |

## <a name="container-with-2-slots"></a><span data-ttu-id="d882a-141">Beholder med 2 spor</span><span class="sxs-lookup"><span data-stu-id="d882a-141">Container with 2-slots</span></span>

<span data-ttu-id="d882a-142">Containertypen med 2 spor er optimalisert for et oppsett med to kolonner.</span><span class="sxs-lookup"><span data-stu-id="d882a-142">The container with 2-slots type is optimized for a two-column layout.</span></span> <span data-ttu-id="d882a-143">Denne typen container har to spor for å tillate en side-ved-side-visning av modulene som er inni.</span><span class="sxs-lookup"><span data-stu-id="d882a-143">This type of container has two slots to allow for a side-by-side view of the modules that are inside.</span></span>

<span data-ttu-id="d882a-144">Du kan bruke flere egenskaper til å optimalisere oppsettet for forskjellige visningsporter (mobilenheter, nettbrett, datamaskiner og så videre).</span><span class="sxs-lookup"><span data-stu-id="d882a-144">Additional properties can be used to optimize the layout for different view ports (mobile devices, tablets, computers, and so on).</span></span> <span data-ttu-id="d882a-145">Bredden på hver kolonne kan defineres for hver visningsport.</span><span class="sxs-lookup"><span data-stu-id="d882a-145">For every view port, the width of each column can be defined.</span></span> <span data-ttu-id="d882a-146">Følgende kolonnebreddeinnstillinger er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="d882a-146">The following column width settings are available:</span></span>

- <span data-ttu-id="d882a-147">**75%/25%** – Den første modulen har en kolonnebredde på 75 prosent, og den andre modulen har en kolonnebredde på 25 prosent.</span><span class="sxs-lookup"><span data-stu-id="d882a-147">**75%/25%** – The first module has a column width of 75 percent, and the second module has a column width of 25 percent.</span></span> <span data-ttu-id="d882a-148">Et **25%/75%**-alternativ er også tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="d882a-148">A **25%/75%** option is also available.</span></span>
- <span data-ttu-id="d882a-149">**50%/50%** – begge modulene har samme kolonnebredde.</span><span class="sxs-lookup"><span data-stu-id="d882a-149">**50%/50%** – Both modules have equal column width.</span></span>
- <span data-ttu-id="d882a-150">**67%/33%** – Den første modulen har en kolonnebredde på 67 prosent, og den andre modulen har en kolonnebredde på 33 prosent.</span><span class="sxs-lookup"><span data-stu-id="d882a-150">**67%/33%** – The first module has a column width of 67 percent, and the second module has a column width of 33 percent.</span></span> <span data-ttu-id="d882a-151">Et **33%/67%**-alternativ er også tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="d882a-151">A **33%/67%** option is also available.</span></span>
- <span data-ttu-id="d882a-152">**100%** – begge modulene har full kolonnebredde.</span><span class="sxs-lookup"><span data-stu-id="d882a-152">**100%** – Both modules have a full-column width.</span></span> <span data-ttu-id="d882a-153">Modulene stables derfor loddrett i én enkelt kolonne.</span><span class="sxs-lookup"><span data-stu-id="d882a-153">Therefore, the modules are vertically stacked in a single column.</span></span> <span data-ttu-id="d882a-154">Selv om dette oppsettet til en enkeltkolonne går mot formålet til containertypen med 2 spor, kan det være ønskelig for noen visningsporter (for eksempel ekstra små visningsporter som mobilenheter).</span><span class="sxs-lookup"><span data-stu-id="d882a-154">Although this single-column layout goes against intent of the container with 2-slots type, it might be preferable for some view ports (for example, extra-small view ports such as mobile devices).</span></span>

### <a name="container-with-2-slots-properties"></a><span data-ttu-id="d882a-155">Container med 2-sporsegenskaper</span><span class="sxs-lookup"><span data-stu-id="d882a-155">Container with 2-slots properties</span></span>

| <span data-ttu-id="d882a-156">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="d882a-156">Property name</span></span>                   | <span data-ttu-id="d882a-157">Verdier</span><span class="sxs-lookup"><span data-stu-id="d882a-157">Values</span></span> | <span data-ttu-id="d882a-158">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d882a-158">Description</span></span> |
|---------------------------------|--------|-------------|
| <span data-ttu-id="d882a-159">Overskrift</span><span class="sxs-lookup"><span data-stu-id="d882a-159">Heading</span></span>                         | <span data-ttu-id="d882a-160">Overskriftstekst og overskriftskode</span><span class="sxs-lookup"><span data-stu-id="d882a-160">Heading text and heading tag</span></span> | <span data-ttu-id="d882a-161">En valgfri kan angis for containeren.</span><span class="sxs-lookup"><span data-stu-id="d882a-161">An optional can be provided for the container.</span></span> |
| <span data-ttu-id="d882a-162">Konfigurasjon av ekstra liten visningsport</span><span class="sxs-lookup"><span data-stu-id="d882a-162">X-Small view port configuration</span></span> | <span data-ttu-id="d882a-163">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** eller **100%**</span><span class="sxs-lookup"><span data-stu-id="d882a-163">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, or **100%**</span></span> | <span data-ttu-id="d882a-164">Denne egenskapen definerer oppsettet for ekstra små visningsporter.</span><span class="sxs-lookup"><span data-stu-id="d882a-164">This property defines the layout for extra-small view ports.</span></span> |
| <span data-ttu-id="d882a-165">Konfigurasjon av liten visningsport</span><span class="sxs-lookup"><span data-stu-id="d882a-165">Small view port configuration</span></span>   | <span data-ttu-id="d882a-166">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** eller **100%**</span><span class="sxs-lookup"><span data-stu-id="d882a-166">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, or **100%**</span></span> | <span data-ttu-id="d882a-167">Denne egenskapen definerer oppsettet for små visningsporter, for eksempel mobilenheter.</span><span class="sxs-lookup"><span data-stu-id="d882a-167">This property defines the layout for small view ports, such as mobile devices.</span></span> |
| <span data-ttu-id="d882a-168">Konfigurasjon av medium visningsport</span><span class="sxs-lookup"><span data-stu-id="d882a-168">Medium view port configuration</span></span>  | <span data-ttu-id="d882a-169">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** eller **100%**</span><span class="sxs-lookup"><span data-stu-id="d882a-169">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, or **100%**</span></span> | <span data-ttu-id="d882a-170">Denne egenskapen definerer oppsettet for medium visningsporter, for eksempel nettbrett.</span><span class="sxs-lookup"><span data-stu-id="d882a-170">This property defines the layout for medium view ports, such as tablets.</span></span> |
| <span data-ttu-id="d882a-171">Konfigurasjon av stor visningsport</span><span class="sxs-lookup"><span data-stu-id="d882a-171">Large view port configuration</span></span>   | <span data-ttu-id="d882a-172">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** eller **100%**</span><span class="sxs-lookup"><span data-stu-id="d882a-172">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, or **100%**</span></span> | <span data-ttu-id="d882a-173">Denne egenskapen definerer oppsettet for store visningsporter, for eksempel datamaskiner.</span><span class="sxs-lookup"><span data-stu-id="d882a-173">This property defines the layout for large view ports, such as computers.</span></span> |

## <a name="container-with-3-slots"></a><span data-ttu-id="d882a-174">Beholder med 3 spor</span><span class="sxs-lookup"><span data-stu-id="d882a-174">Container with 3-slots</span></span>

<span data-ttu-id="d882a-175">Containertypen med 3-sporsmoduler er optimalisert for et oppsett med tre kolonner.</span><span class="sxs-lookup"><span data-stu-id="d882a-175">The container with 3-slots modules type is optimized for a three-column layout.</span></span>

<span data-ttu-id="d882a-176">Du kan bruke flere egenskaper til å optimalisere oppsettet for forskjellige visningsporter.</span><span class="sxs-lookup"><span data-stu-id="d882a-176">Additional properties can be used to optimize the layout for different view ports.</span></span> <span data-ttu-id="d882a-177">Bredden på hver kolonne kan defineres for hver visningsport.</span><span class="sxs-lookup"><span data-stu-id="d882a-177">For every view port, the width of each column can be defined.</span></span> <span data-ttu-id="d882a-178">Følgende kolonnebreddeinnstillinger er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="d882a-178">The following column width settings are available:</span></span>

- <span data-ttu-id="d882a-179">**33%/33%/33%** – Alle tre moduler har samme kolonnebredde.</span><span class="sxs-lookup"><span data-stu-id="d882a-179">**33%/33%/33%** – All three modules have equal column width.</span></span>
- <span data-ttu-id="d882a-180">**50%/25%/25%** – Den første modulen har en kolonnebredde på 50 prosent, og hver av de to gjenværende modulene har en kolonnebredde på 25 prosent.</span><span class="sxs-lookup"><span data-stu-id="d882a-180">**50%/25%/25%** – The first module has a column width of 50 percent, and each of the remaining two modules has a column width of 25 percent.</span></span> <span data-ttu-id="d882a-181">**25%/50%/25%**- og **25%/25%/50%**-alternativer er også tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="d882a-181">**25%/50%/25%** and **25%/25%/50%** options are also available.</span></span>
- <span data-ttu-id="d882a-182">**16%/16%/67%** – Hver av de to første modulen har en kolonnebredde på 16 prosent, og den tredje modulen har en kolonnebredde på 67 prosent.</span><span class="sxs-lookup"><span data-stu-id="d882a-182">**16%/16%/67%** – Each of the first two modules has a column width of 16 percent, and the third module has a column width of 67 percent.</span></span> <span data-ttu-id="d882a-183">**16%/67%/16%**- og **67%/16%/16%**-alternativer er også tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="d882a-183">**16%/67%/16%** and **67%/16%/16%** options are also available.</span></span>

### <a name="container-with-3-slots-properties"></a><span data-ttu-id="d882a-184">Container med 3-sporsegenskaper</span><span class="sxs-lookup"><span data-stu-id="d882a-184">Container with 3-slots properties</span></span>

| <span data-ttu-id="d882a-185">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="d882a-185">Property name</span></span>                   | <span data-ttu-id="d882a-186">Verdier</span><span class="sxs-lookup"><span data-stu-id="d882a-186">Values</span></span> | <span data-ttu-id="d882a-187">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d882a-187">Description</span></span> |
|---------------------------------|--------|-------------|
| <span data-ttu-id="d882a-188">Overskrift</span><span class="sxs-lookup"><span data-stu-id="d882a-188">Heading</span></span>                         | <span data-ttu-id="d882a-189">Overskriftstekst og overskriftskode</span><span class="sxs-lookup"><span data-stu-id="d882a-189">Heading text and heading tag</span></span> | <span data-ttu-id="d882a-190">En valgfri overskrift kan legges til i containeren.</span><span class="sxs-lookup"><span data-stu-id="d882a-190">An optional heading can be added to the container.</span></span> |
| <span data-ttu-id="d882a-191">Konfigurasjon av ekstra liten visningsport</span><span class="sxs-lookup"><span data-stu-id="d882a-191">X-Small view port configuration</span></span> | <span data-ttu-id="d882a-192">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** eller **67%/16%/16%**</span><span class="sxs-lookup"><span data-stu-id="d882a-192">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, or **67%/16%/16%**</span></span> | <span data-ttu-id="d882a-193">Denne egenskapen definerer oppsettet for ekstra små visningsporter.</span><span class="sxs-lookup"><span data-stu-id="d882a-193">This property defines the layout for extra-small view ports.</span></span> |
| <span data-ttu-id="d882a-194">Konfigurasjon av liten visningsport</span><span class="sxs-lookup"><span data-stu-id="d882a-194">Small view port configuration</span></span>   | <span data-ttu-id="d882a-195">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** eller **67%/16%/16%**</span><span class="sxs-lookup"><span data-stu-id="d882a-195">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, or **67%/16%/16%**</span></span> | <span data-ttu-id="d882a-196">Denne egenskapen definerer oppsettet for små visningsporter, for eksempel mobilenheter.</span><span class="sxs-lookup"><span data-stu-id="d882a-196">This property defines the layout for small view ports, such as mobile devices.</span></span> |
| <span data-ttu-id="d882a-197">Konfigurasjon av medium visningsport</span><span class="sxs-lookup"><span data-stu-id="d882a-197">Medium view port configuration</span></span>  | <span data-ttu-id="d882a-198">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** eller **67%/16%/16%**</span><span class="sxs-lookup"><span data-stu-id="d882a-198">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, or **67%/16%/16%**</span></span> | <span data-ttu-id="d882a-199">Denne egenskapen definerer oppsettet for medium visningsporter, for eksempel nettbrett.</span><span class="sxs-lookup"><span data-stu-id="d882a-199">This property defines the layout for medium view ports, such as tablets.</span></span> |
| <span data-ttu-id="d882a-200">Konfigurasjon av stor visningsport</span><span class="sxs-lookup"><span data-stu-id="d882a-200">Large view port configuration</span></span>   | <span data-ttu-id="d882a-201">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** eller **67%/16%/16%**</span><span class="sxs-lookup"><span data-stu-id="d882a-201">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, or **67%/16%/16%**</span></span> | <span data-ttu-id="d882a-202">Denne egenskapen definerer oppsettet for store visningsporter, for eksempel datamaskiner.</span><span class="sxs-lookup"><span data-stu-id="d882a-202">This property defines the layout for large view ports, such as computers.</span></span> |

## <a name="add-a-container-module-to-a-page"></a><span data-ttu-id="d882a-203">Legge til en containermodul på en side</span><span class="sxs-lookup"><span data-stu-id="d882a-203">Add a container module to a page</span></span>

<span data-ttu-id="d882a-204">Hvis du vil legge til en containerspillermodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="d882a-204">To add a container player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="d882a-205">Opprett en sidemal som heter **containermal**.</span><span class="sxs-lookup"><span data-stu-id="d882a-205">Create a page template that is named **container template**.</span></span>
1. <span data-ttu-id="d882a-206">I **Hoved**-sporet på standardsiden legger du til en containermodul.</span><span class="sxs-lookup"><span data-stu-id="d882a-206">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="d882a-207">I containermodulen legger du til en funksjonsmodul.</span><span class="sxs-lookup"><span data-stu-id="d882a-207">In the container module, add a feature module.</span></span>
1. <span data-ttu-id="d882a-208">Sjekk inn malen, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="d882a-208">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="d882a-209">Bruk containermalen du nettopp opprettet, for å opprette en side som heter **containerside**.</span><span class="sxs-lookup"><span data-stu-id="d882a-209">Use the container template that you just created to create a page that is named **container page**.</span></span>
1. <span data-ttu-id="d882a-210">I **Hoved**-sporet på den nye siden legger du til en containermodul.</span><span class="sxs-lookup"><span data-stu-id="d882a-210">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="d882a-211">I egenskapsruten for containermodulen settes **Antall kolonner**-egenskapen til **1** og **Bredde**-egenskapen til **Tilpass container**.</span><span class="sxs-lookup"><span data-stu-id="d882a-211">In the property pane for the container module, set the **Number of columns** property to **1** and the **Width** property to **Fit container**.</span></span>
1. <span data-ttu-id="d882a-212">I containermodulen legger du til en funksjonsmodul.</span><span class="sxs-lookup"><span data-stu-id="d882a-212">In the container module, add a feature module.</span></span>
1. <span data-ttu-id="d882a-213">I egenskapsruten for funksjonsmodulen konfigurerer du en overskrift.</span><span class="sxs-lookup"><span data-stu-id="d882a-213">In the property pane for the feature module, configure a heading.</span></span>
1. <span data-ttu-id="d882a-214">Lagre og forhåndsvis siden.</span><span class="sxs-lookup"><span data-stu-id="d882a-214">Save and preview the page.</span></span> <span data-ttu-id="d882a-215">Du skal se én funksjonsmodul som passer innenfor bredden til containermodulen.</span><span class="sxs-lookup"><span data-stu-id="d882a-215">You should see one feature module that fits within the width of the container module.</span></span>
1. <span data-ttu-id="d882a-216">I egenskapsruten for containermodulen endrer du verdien til egenskapen **Antall kolonner** til **3**.</span><span class="sxs-lookup"><span data-stu-id="d882a-216">In the property pane for the container module, change the the value of the **Number of columns** property to **3**.</span></span>
1. <span data-ttu-id="d882a-217">Legg til to funksjonsmoduler til i containermodulen.</span><span class="sxs-lookup"><span data-stu-id="d882a-217">Add two more feature modules to the container module.</span></span>
1. <span data-ttu-id="d882a-218">Lagre og forhåndsvis siden.</span><span class="sxs-lookup"><span data-stu-id="d882a-218">Save and preview the page.</span></span> <span data-ttu-id="d882a-219">Nå skal du se tre funksjonsmoduler som vises side ved side.</span><span class="sxs-lookup"><span data-stu-id="d882a-219">You should now see three feature modules that appear side by side.</span></span>
1. <span data-ttu-id="d882a-220">Når du har fått oppsettet du vil bruke, sjekker du inn siden og publiserer den.</span><span class="sxs-lookup"><span data-stu-id="d882a-220">After you've achieved the layout that you want, check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d882a-221">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d882a-221">Additional resources</span></span>

[<span data-ttu-id="d882a-222">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="d882a-222">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d882a-223">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="d882a-223">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="d882a-224">Innholdsrik blokk-modul</span><span class="sxs-lookup"><span data-stu-id="d882a-224">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="d882a-225">Modul for innholdsplassering</span><span class="sxs-lookup"><span data-stu-id="d882a-225">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="d882a-226">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="d882a-226">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="d882a-227">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="d882a-227">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d882a-228">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="d882a-228">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d882a-229">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="d882a-229">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="d882a-230">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="d882a-230">Footer module</span></span>](author-footer-module.md)