---
title: Skjermoppsettet for demonstrasjonsdataene i MPOS/CPOS
description: Dette emnet inneholder informasjon om skjermoppsett som er inkludert i settet med demonstrasjonsdata for salgsstedsopplevelser i Microsoft Dynamics 365 for Retail.
author: zlinster
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: zlinster
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 797058bdbbdb63a08eb35034ffe3c913307f38df
ms.openlocfilehash: e812bb13c903e72e31e62effd0c70f9b9d62de55
ms.contentlocale: nb-no
ms.lasthandoff: 03/06/2018

---

# <a name="demo-data-screen-layouts-in-mposcpos"></a><span data-ttu-id="c14bd-103">Skjermoppsett for demonstrasjonsdata i MPOS/CPOS</span><span class="sxs-lookup"><span data-stu-id="c14bd-103">Demo data screen layouts in MPOS/CPOS</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="c14bd-104">Dette emnet inneholder informasjon om skjermoppsett som er inkludert i settet med demonstrasjonsdata for salgsstedsopplevelser i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="c14bd-104">This topic provides information about the screen layouts that are included with the demo data set for the point of sale (POS) experiences in Microsoft Dynamics 365 for Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="c14bd-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="c14bd-105">Overview</span></span>

<span data-ttu-id="c14bd-106">Eksempelskjermoppsett som er inkludert i Retail-demonstrasjonsdata har innhold som er optimalisert for forskjellige segmenter for detaljhandel, butikkarbeiderroller og enheter.</span><span class="sxs-lookup"><span data-stu-id="c14bd-106">The sample screen layouts that are included with Retail demo data provide content that is optimized for various retail segments, store worker roles, and devices.</span></span> <span data-ttu-id="c14bd-107">Ett enkelt oppsett kan inneholde flere oppsettstørrelser og kombinasjoner av knappegrupper for å sikre dekning når butikkarbeidere flytter mellom enheter og stasjoner.</span><span class="sxs-lookup"><span data-stu-id="c14bd-107">A single layout can contain several layout sizes and combinations of button grids, to help ensure coverage as store workers move between devices and stations.</span></span> <span data-ttu-id="c14bd-108">Dette emnet fremhever forskjellene mellom disse oppsettene, operasjonene som de gir og de helhetlige opplevelsene som de leverer.</span><span class="sxs-lookup"><span data-stu-id="c14bd-108">This topic highlights the differences between these layouts, the operations that they provide, and the overall experiences that they deliver.</span></span>

![Oppsett for demonstrasjonsdata på tvers av enheter](../retail/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a><span data-ttu-id="c14bd-110">Innholdet i en skjermoppsett-ID</span><span class="sxs-lookup"><span data-stu-id="c14bd-110">Anatomy of a screen layout ID</span></span>

<span data-ttu-id="c14bd-111">Du kan finne skjermoppsett i Retail ved å gå til **Retail** > **Kanaloppsett** > **Salgsstedsoppsett** > **Salgssted** > **Skjermoppsett**.</span><span class="sxs-lookup"><span data-stu-id="c14bd-111">To find screen layouts in Retail, go to **Retail** > **Channel setup** > **POS setup** > **POS** > **Screen layouts**.</span></span>

![Skjermoppsettside i Retail](../retail/media/demo-screen-layouts-fig-2-1.png)

<span data-ttu-id="c14bd-113">Skjermoppsett-ID-er kan inneholde opptil ti tegn.</span><span class="sxs-lookup"><span data-stu-id="c14bd-113">Screen layout IDs can have a maximum of 10 characters.</span></span> <span data-ttu-id="c14bd-114">ID-en er en streng som består av tre typer informasjon i denne rekkefølgen:</span><span class="sxs-lookup"><span data-stu-id="c14bd-114">The ID is a string that consists of three pieces of information, in this order:</span></span>

1. <span data-ttu-id="c14bd-115">Firma</span><span class="sxs-lookup"><span data-stu-id="c14bd-115">Company</span></span>
2. <span data-ttu-id="c14bd-116">Oppsettversjon</span><span class="sxs-lookup"><span data-stu-id="c14bd-116">Layout version</span></span>
3. <span data-ttu-id="c14bd-117">Egenskap</span><span class="sxs-lookup"><span data-stu-id="c14bd-117">Persona</span></span>

### <a name="company"></a><span data-ttu-id="c14bd-118">Firma</span><span class="sxs-lookup"><span data-stu-id="c14bd-118">Company</span></span>

| <span data-ttu-id="c14bd-119">Brev</span><span class="sxs-lookup"><span data-stu-id="c14bd-119">Letter</span></span> | <span data-ttu-id="c14bd-120">Firma</span><span class="sxs-lookup"><span data-stu-id="c14bd-120">Company</span></span>         |
|--------|-----------------|
| <span data-ttu-id="c14bd-121">A</span><span class="sxs-lookup"><span data-stu-id="c14bd-121">A</span></span>      | <span data-ttu-id="c14bd-122">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="c14bd-122">Adventure Works</span></span> |
| <span data-ttu-id="c14bd-123">Ø</span><span class="sxs-lookup"><span data-stu-id="c14bd-123">F</span></span>      | <span data-ttu-id="c14bd-124">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="c14bd-124">Fabrikam</span></span>        |
| <span data-ttu-id="c14bd-125">K</span><span class="sxs-lookup"><span data-stu-id="c14bd-125">C</span></span>      | <span data-ttu-id="c14bd-126">Contoso</span><span class="sxs-lookup"><span data-stu-id="c14bd-126">Contoso</span></span>         |

### <a name="layout-version"></a><span data-ttu-id="c14bd-127">Oppsettversjon</span><span class="sxs-lookup"><span data-stu-id="c14bd-127">Layout version</span></span>

| <span data-ttu-id="c14bd-128">Versjonsnummer</span><span class="sxs-lookup"><span data-stu-id="c14bd-128">Version number</span></span> | <span data-ttu-id="c14bd-129">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c14bd-129">Description</span></span>                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c14bd-130">3</span><span class="sxs-lookup"><span data-stu-id="c14bd-130">3</span></span>              | <span data-ttu-id="c14bd-131">Den grunnleggende versjonen som støtter flere skjermstørrelser for forskjellige enheter og sideforhold</span><span class="sxs-lookup"><span data-stu-id="c14bd-131">The base version that supports multiple screen sizes for various devices and aspect ratios</span></span> |
| <span data-ttu-id="c14bd-132">3.1</span><span class="sxs-lookup"><span data-stu-id="c14bd-132">3.1</span></span>            | <span data-ttu-id="c14bd-133">Den grunnleggende versjonen som har ekstra støtte for panelet **Anbefalte produkter**</span><span class="sxs-lookup"><span data-stu-id="c14bd-133">The base version that has additional support for the **Recommended products** panel</span></span>        |

### <a name="persona"></a><span data-ttu-id="c14bd-134">Egenskap</span><span class="sxs-lookup"><span data-stu-id="c14bd-134">Persona</span></span>

| <span data-ttu-id="c14bd-135">Forkortelse</span><span class="sxs-lookup"><span data-stu-id="c14bd-135">Abbreviation</span></span> | <span data-ttu-id="c14bd-136">Egenskap</span><span class="sxs-lookup"><span data-stu-id="c14bd-136">Persona</span></span>       | <span data-ttu-id="c14bd-137">Innhold</span><span class="sxs-lookup"><span data-stu-id="c14bd-137">Contents</span></span> |
|--------------|---------------|----------|
| <span data-ttu-id="c14bd-138">CSH</span><span class="sxs-lookup"><span data-stu-id="c14bd-138">CSH</span></span>          | <span data-ttu-id="c14bd-139">Kasserer</span><span class="sxs-lookup"><span data-stu-id="c14bd-139">Cashier</span></span>       | <span data-ttu-id="c14bd-140">Kassereroppsett inkluderer alle transaksjonsrelaterte operasjoner, for eksempel kundeordrer, returer, rabatter, annulleringer og gavekort.</span><span class="sxs-lookup"><span data-stu-id="c14bd-140">Cashier layouts include all transaction-related operations, such as customer orders, returns, discounts, voids, and gift cards.</span></span> <span data-ttu-id="c14bd-141">Disse oppsettene inkluderer også daglige oppgaver for lagerstyring, for eksempel priskontroller, lageroppslag og lagertellinger.</span><span class="sxs-lookup"><span data-stu-id="c14bd-141">These layouts also include daily tasks for inventory management, such price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="c14bd-142">Det finnes også grunnleggende skiftadministrasjon for startbeløp, suspendering av skift og tidsklokke.</span><span class="sxs-lookup"><span data-stu-id="c14bd-142">Basic shift management is also provided for start amounts, suspending shifts, and time clock.</span></span> |
| <span data-ttu-id="c14bd-143">MGR</span><span class="sxs-lookup"><span data-stu-id="c14bd-143">MGR</span></span>          | <span data-ttu-id="c14bd-144">Butikksjef</span><span class="sxs-lookup"><span data-stu-id="c14bd-144">Store Manager</span></span> | <span data-ttu-id="c14bd-145">Butikksjefoppsett inkluderer alle transaksjonsrelaterte operasjoner som finnes i et kassereroppsett, men det inneholder også mva-overstyringer.</span><span class="sxs-lookup"><span data-stu-id="c14bd-145">Store Manager layouts include all transaction-related operations that are found in the Cashier layouts but also include tax overrides.</span></span> <span data-ttu-id="c14bd-146">Disse oppsettene inkluderer også daglige oppgaver for lagerstyring, for eksempel priskontroller, lageroppslag og lagertellinger.</span><span class="sxs-lookup"><span data-stu-id="c14bd-146">These layouts also include daily tasks for inventory management, such as price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="c14bd-147">Skiftadministrasjon finnes for start, suspendering og avslutning av skift.</span><span class="sxs-lookup"><span data-stu-id="c14bd-147">Shift management is provided for starting, suspending, and closing shifts.</span></span> <span data-ttu-id="c14bd-148">I tillegg inkluderer oppsettene skuffoperasjoner for oppføring, fjerning, kasseoppgjør og safe- og banklevering.</span><span class="sxs-lookup"><span data-stu-id="c14bd-148">Additionally, the layouts include drawer operations for entries, removals, tender declarations, and safe and bank drops.</span></span> <span data-ttu-id="c14bd-149">Til slutt inkluderer disse oppsettene tilgangen til prestasjonsrapporter og tillater utskrift av X- og Z-rapporter.</span><span class="sxs-lookup"><span data-stu-id="c14bd-149">Finally, these layouts include access to performance reports, and enable X and Z reports to be printed.</span></span> |
| <span data-ttu-id="c14bd-150">STK</span><span class="sxs-lookup"><span data-stu-id="c14bd-150">STK</span></span>          | <span data-ttu-id="c14bd-151">Lagermedarbeider</span><span class="sxs-lookup"><span data-stu-id="c14bd-151">Stock Clerk</span></span>   | <span data-ttu-id="c14bd-152">Lagermedarbeideroppsett er optimalisert for lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="c14bd-152">Stock Clerk layouts are optimized for inventory management.</span></span> <span data-ttu-id="c14bd-153">De inkluderer tilgang til daglige oppgaver for priskontroller, lageroppslag, plukk og mottak, lagertelling og settdemontering.</span><span class="sxs-lookup"><span data-stu-id="c14bd-153">They include access to daily tasks for price checks, inventory lookups, picking and receiving, stock counts, and kit disassembly.</span></span> <span data-ttu-id="c14bd-154">Disse oppsettene gir også grunnleggende skiftoperasjoner for tidsklokke og suspendering av skift.</span><span class="sxs-lookup"><span data-stu-id="c14bd-154">These layouts also provide basic shift operations for time clock and suspending shifts.</span></span> <span data-ttu-id="c14bd-155">Selv om disse oppsettene først og fremst er beregnet for back office-oppgaver, har lagermedarbeidere de samme operasjonene som kasserere for transaksjonsskjermer.</span><span class="sxs-lookup"><span data-stu-id="c14bd-155">Although these layouts are intended mainly for back-office tasks, stock clerks have the same operations as cashiers for transaction screens.</span></span> |

### <a name="example-layout"></a><span data-ttu-id="c14bd-156">Eksempel-oppsett</span><span class="sxs-lookup"><span data-stu-id="c14bd-156">Example layout</span></span>

<span data-ttu-id="c14bd-157">Her er et eksempel på en skjermoppsett-ID for firmaet Fabrikam, oppsettversjon 3 og Butikksjef:</span><span class="sxs-lookup"><span data-stu-id="c14bd-157">Here is an example of a screen layout ID for the Fabrikam company, layout version 3, and the Store Manager persona:</span></span>

<span data-ttu-id="c14bd-158">F3MGR</span><span class="sxs-lookup"><span data-stu-id="c14bd-158">F3MGR</span></span>

<span data-ttu-id="c14bd-159">Illustrasjonen nedenfor viser et eksempel på velkomstskjermen for Fabrikam-butikksjef.</span><span class="sxs-lookup"><span data-stu-id="c14bd-159">The following illustration shows an example of the Welcome screen for a Fabrikam store manager.</span></span>

![Velkomstskjermen for Fabrikam-butikksjefen](../retail/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a><span data-ttu-id="c14bd-161">Oppsettstørrelser</span><span class="sxs-lookup"><span data-stu-id="c14bd-161">Layout sizes</span></span>

### <a name="full-vs-compact-layouts"></a><span data-ttu-id="c14bd-162">Fullstendige kontra kompakte oppsett</span><span class="sxs-lookup"><span data-stu-id="c14bd-162">Full vs. compact layouts</span></span>

<span data-ttu-id="c14bd-163">Et skjermoppsett kan ha konfigurasjoner for både fullstendige og kompakte enheter.</span><span class="sxs-lookup"><span data-stu-id="c14bd-163">A screen layout can have configurations for both full devices and compact devices.</span></span> <span data-ttu-id="c14bd-164">Derfor kan en bruker tilordnes til ett enkelt skjermoppsettet som fungerer på tvers av ulike størrelser og formfaktorer i butikken.</span><span class="sxs-lookup"><span data-stu-id="c14bd-164">Therefore, a user can be assigned to a single screen layout that will work across various sizes and form factors in the store.</span></span>

- <span data-ttu-id="c14bd-165">**Modern POS - Fullstendig** – Fullstendige oppsett brukes vanligvis helst for større skjermer, for eksempel PC-skjermer eller nettbrett.</span><span class="sxs-lookup"><span data-stu-id="c14bd-165">**Modern POS - Full** – Typically, full layouts are best used for larger displays, such as desktop computer monitors or tablets.</span></span> <span data-ttu-id="c14bd-166">Brukere kan velge elementene i brukergrensesnittet som oppsettet inneholder, angi størrelsen og plasseringen til elementene og konfigurere de detaljerte egenskapene.</span><span class="sxs-lookup"><span data-stu-id="c14bd-166">Users can select the UI elements that the layout includes, specify the size and placement of those elements, and configure their detailed properties.</span></span> <span data-ttu-id="c14bd-167">Fullstendig oppsett støtter både liggende og stående konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="c14bd-167">Full layouts support both portrait and landscape configurations.</span></span>
- <span data-ttu-id="c14bd-168">**Moderne POS - Kompakt** – Kompakt oppsett brukes vanligvis helst for telefoner eller små nettbrett.</span><span class="sxs-lookup"><span data-stu-id="c14bd-168">**Modern POS - Compact** – Typically, compact layouts are best used for phones or small tablets.</span></span> <span data-ttu-id="c14bd-169">Utformingsmulighetene er begrenset for kompakte enheter.</span><span class="sxs-lookup"><span data-stu-id="c14bd-169">Design possibilities are limited for compact devices.</span></span> <span data-ttu-id="c14bd-170">Brukere kan konfigurere kolonner og felt for rutene for kvittering og totaler.</span><span class="sxs-lookup"><span data-stu-id="c14bd-170">Users can configure the columns and fields for the receipt pane and the totals pane.</span></span>

### <a name="screen-resolutions-that-are-provided"></a><span data-ttu-id="c14bd-171">Skjermoppløsninger som tilbys</span><span class="sxs-lookup"><span data-stu-id="c14bd-171">Screen resolutions that are provided</span></span>

<span data-ttu-id="c14bd-172">Tabellen nedenfor viser oppsettstørrelsene som finnes for vanlige skjermoppløsninger.</span><span class="sxs-lookup"><span data-stu-id="c14bd-172">The following table shows the layout sizes that are provided for typical screen resolutions.</span></span>

| <span data-ttu-id="c14bd-173">Oppsettype</span><span class="sxs-lookup"><span data-stu-id="c14bd-173">Layout type</span></span> | <span data-ttu-id="c14bd-174">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="c14bd-174">Resolution</span></span> | <span data-ttu-id="c14bd-175">Størrelsesforhold</span><span class="sxs-lookup"><span data-stu-id="c14bd-175">Aspect ratio</span></span> | <span data-ttu-id="c14bd-176">Målskjerm</span><span class="sxs-lookup"><span data-stu-id="c14bd-176">Target display</span></span>          |
|-------------|------------|--------------|-------------------------|
| <span data-ttu-id="c14bd-177">Komprimer\*</span><span class="sxs-lookup"><span data-stu-id="c14bd-177">Compact\*</span></span>   | <span data-ttu-id="c14bd-178">480 × 853</span><span class="sxs-lookup"><span data-stu-id="c14bd-178">480 × 853</span></span>  | <span data-ttu-id="c14bd-179">16:9</span><span class="sxs-lookup"><span data-stu-id="c14bd-179">16:9</span></span>         | <span data-ttu-id="c14bd-180">Telefoner</span><span class="sxs-lookup"><span data-stu-id="c14bd-180">Phones</span></span>                  |
| <span data-ttu-id="c14bd-181">Full</span><span class="sxs-lookup"><span data-stu-id="c14bd-181">Full</span></span>        | <span data-ttu-id="c14bd-182">1024 × 768</span><span class="sxs-lookup"><span data-stu-id="c14bd-182">1024 × 768</span></span> | <span data-ttu-id="c14bd-183">4:3</span><span class="sxs-lookup"><span data-stu-id="c14bd-183">4:3</span></span>          | <span data-ttu-id="c14bd-184">Nettbrett</span><span class="sxs-lookup"><span data-stu-id="c14bd-184">Tablets</span></span>                 |
| <span data-ttu-id="c14bd-185">Full\*</span><span class="sxs-lookup"><span data-stu-id="c14bd-185">Full\*</span></span>      | <span data-ttu-id="c14bd-186">1280 × 720</span><span class="sxs-lookup"><span data-stu-id="c14bd-186">1280 × 720</span></span> | <span data-ttu-id="c14bd-187">16:9</span><span class="sxs-lookup"><span data-stu-id="c14bd-187">16:9</span></span>         | <span data-ttu-id="c14bd-188">Nettbrett</span><span class="sxs-lookup"><span data-stu-id="c14bd-188">Tablets</span></span>                 |
| <span data-ttu-id="c14bd-189">Full</span><span class="sxs-lookup"><span data-stu-id="c14bd-189">Full</span></span>        | <span data-ttu-id="c14bd-190">1366 × 768</span><span class="sxs-lookup"><span data-stu-id="c14bd-190">1366 × 768</span></span> | <span data-ttu-id="c14bd-191">16:9</span><span class="sxs-lookup"><span data-stu-id="c14bd-191">16:9</span></span>         | <span data-ttu-id="c14bd-192">Nettbrett, store skjermer</span><span class="sxs-lookup"><span data-stu-id="c14bd-192">Tablets, larger screens</span></span> |
| <span data-ttu-id="c14bd-193">Full</span><span class="sxs-lookup"><span data-stu-id="c14bd-193">Full</span></span>        | <span data-ttu-id="c14bd-194">1440 × 960</span><span class="sxs-lookup"><span data-stu-id="c14bd-194">1440 × 960</span></span> | <span data-ttu-id="c14bd-195">3:2</span><span class="sxs-lookup"><span data-stu-id="c14bd-195">3:2</span></span>          | <span data-ttu-id="c14bd-196">Nettbrett, store skjermer</span><span class="sxs-lookup"><span data-stu-id="c14bd-196">Tablets, larger screens</span></span> |

<span data-ttu-id="c14bd-197">\* Disse ekstra oppsettstørrelsene er bare tilgjengelige i oppsett for Adventure Works og Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="c14bd-197">\* These additional layout sizes are available only in Adventure Works and Fabrikam layouts.</span></span>


>[!TIP]
> <span data-ttu-id="c14bd-198">POS velger automatisk oppsettstørrelser basert på den nærmeste størrelsen som er tilgjengelig for skjermoppløsningen for gjeldende appvindu.</span><span class="sxs-lookup"><span data-stu-id="c14bd-198">POS automatically selects layout sizes, based on the closest size that is available for the screen resolution of the current app window.</span></span> <span data-ttu-id="c14bd-199">Hvis du vil finne skjermoppsett-ID og oppsettoppløsning som brukes for øyeblikket i Retail Modern POS (MPOS) eller Retail Cloud POS (CPOS), kan du åpne siden **Innstillinger** og se i delen **Øktinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="c14bd-199">To find the screen layout ID and layout resolution that are currently used, in Retail Modern POS (MPOS) or Retail Cloud POS (CPOS), open the **Settings** page, and look in the **Session information** section.</span></span> <span data-ttu-id="c14bd-200">Du kan også se den faktiske vindusoppløsningen for gjeldende appe eller nettleserramme.</span><span class="sxs-lookup"><span data-stu-id="c14bd-200">You can also see the actual window resolution for your current application or browser frame.</span></span> <span data-ttu-id="c14bd-201">Når du har denne informasjonen, kan du finne kilden til oppsettinnholdet i Retail ved å gå til **Kanaloppsett** > **Salgsstedsoppsett** > **Salgssted** > **Skjermoppsett**.</span><span class="sxs-lookup"><span data-stu-id="c14bd-201">After you have this information, you can find the source of the layout content in Retail by going to **Channel setup** > **POS setup** > **POS** > **Screen layouts**.</span></span>


![Skjermoppsett og oppsettoppløsninger/-størrelser og Retail POS](../retail/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a><span data-ttu-id="c14bd-203">Firmaer og merker</span><span class="sxs-lookup"><span data-stu-id="c14bd-203">Companies and brands</span></span>

<span data-ttu-id="c14bd-204">Hvert fiktive firma er rettet mot ulike detaljhandelsegmentet og inkluderer produktkataloger som er beregnet for firmaets marked.</span><span class="sxs-lookup"><span data-stu-id="c14bd-204">Each fictitious company is targeted to a different retail segment and includes product catalogs that are tuned for the company's market.</span></span> <span data-ttu-id="c14bd-205">Hvert firma har et unikt visuell merke som følger med produktene.</span><span class="sxs-lookup"><span data-stu-id="c14bd-205">Each company has a unique visual brand that accompanies its products.</span></span> <span data-ttu-id="c14bd-206">Varemerkeelementene omfatter uthevingsfargen, mørkt eller lyst tema og tilhørende bilder med realistiske opplevelser.</span><span class="sxs-lookup"><span data-stu-id="c14bd-206">Branding elements include the accent color, dark or light theme, and accompanying photographs that provide realistic experiences.</span></span>

### <a name="company-segment-and-visual-characteristics"></a><span data-ttu-id="c14bd-207">Firmasegmentet og visuelle egenskaper</span><span class="sxs-lookup"><span data-stu-id="c14bd-207">Company segment and visual characteristics</span></span>

| <span data-ttu-id="c14bd-208">Firma</span><span class="sxs-lookup"><span data-stu-id="c14bd-208">Company</span></span>         | <span data-ttu-id="c14bd-209">Sted</span><span class="sxs-lookup"><span data-stu-id="c14bd-209">Location</span></span> | <span data-ttu-id="c14bd-210">Segment</span><span class="sxs-lookup"><span data-stu-id="c14bd-210">Segment</span></span>        | <span data-ttu-id="c14bd-211">Utheving</span><span class="sxs-lookup"><span data-stu-id="c14bd-211">Accent</span></span> | <span data-ttu-id="c14bd-212">Tema</span><span class="sxs-lookup"><span data-stu-id="c14bd-212">Theme</span></span> |
|-----------------|----------|----------------|--------|-------|
| <span data-ttu-id="c14bd-213">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="c14bd-213">Adventure Works</span></span> | <span data-ttu-id="c14bd-214">Seattle</span><span class="sxs-lookup"><span data-stu-id="c14bd-214">Seattle</span></span>  | <span data-ttu-id="c14bd-215">Sportsartikler</span><span class="sxs-lookup"><span data-stu-id="c14bd-215">Sporting Goods</span></span> | <span data-ttu-id="c14bd-216">Blå</span><span class="sxs-lookup"><span data-stu-id="c14bd-216">Blue</span></span>   | <span data-ttu-id="c14bd-217">Mørkt</span><span class="sxs-lookup"><span data-stu-id="c14bd-217">Dark</span></span>  |
| <span data-ttu-id="c14bd-218">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="c14bd-218">Fabrikam</span></span>        | <span data-ttu-id="c14bd-219">Houston</span><span class="sxs-lookup"><span data-stu-id="c14bd-219">Houston</span></span>  | <span data-ttu-id="c14bd-220">Mote</span><span class="sxs-lookup"><span data-stu-id="c14bd-220">Fashion</span></span>        | <span data-ttu-id="c14bd-221">Grønn</span><span class="sxs-lookup"><span data-stu-id="c14bd-221">Green</span></span>  | <span data-ttu-id="c14bd-222">Lys</span><span class="sxs-lookup"><span data-stu-id="c14bd-222">Light</span></span> |
| <span data-ttu-id="c14bd-223">Contoso</span><span class="sxs-lookup"><span data-stu-id="c14bd-223">Contoso</span></span>         | <span data-ttu-id="c14bd-224">Boston</span><span class="sxs-lookup"><span data-stu-id="c14bd-224">Boston</span></span>   | <span data-ttu-id="c14bd-225">Elektronikk</span><span class="sxs-lookup"><span data-stu-id="c14bd-225">Electronics</span></span>    | <span data-ttu-id="c14bd-226">Rød</span><span class="sxs-lookup"><span data-stu-id="c14bd-226">Red</span></span>    | <span data-ttu-id="c14bd-227">Mørkt</span><span class="sxs-lookup"><span data-stu-id="c14bd-227">Dark</span></span>  |


>[!NOTE]
> <span data-ttu-id="c14bd-228">Adventure Works og Fabrikam er de to ledende merkene.</span><span class="sxs-lookup"><span data-stu-id="c14bd-228">Adventure Works and Fabrikam are the two flagship brands.</span></span> <span data-ttu-id="c14bd-229">Contoso er tilgjengelig, men ikke alle oppsettene følger med.</span><span class="sxs-lookup"><span data-stu-id="c14bd-229">Contoso is available, but not all layouts have been provided.</span></span>


<span data-ttu-id="c14bd-230">Illustrasjonene nedenfor viser eksempler på velkomstsiden og transaksjonssiden for de tre fiktive firmaene.</span><span class="sxs-lookup"><span data-stu-id="c14bd-230">The following illustrations show examples of the welcome page and transaction page for the three fictitious companies.</span></span>

### <a name="adventure-works"></a><span data-ttu-id="c14bd-231">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="c14bd-231">Adventure Works</span></span>

![Velkomstside for Adventure Works med demonstrasjonsdata](../retail/media/demo-screen-layouts-fig-4-1a.png)

![Transaksjonsside for Adventure Works med demonstrasjonsdata](../retail/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a><span data-ttu-id="c14bd-234">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="c14bd-234">Fabrikam</span></span>

![Velkomstside for Fabrikam med demonstrasjonsdata](../retail/media/demo-screen-layouts-fig-4-2a.png)

![Transaksjonsside for Fabrikam med demonstrasjonsdata](../retail/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a><span data-ttu-id="c14bd-237">Contoso</span><span class="sxs-lookup"><span data-stu-id="c14bd-237">Contoso</span></span>

![Oppsett for demonstrasjonsdata for Contoso](../retail/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a><span data-ttu-id="c14bd-239">Matrise for brukerpålogging</span><span class="sxs-lookup"><span data-stu-id="c14bd-239">User sign in matrix</span></span>

<span data-ttu-id="c14bd-240">Brukere er angitt for de forskjellige skjermoppsettene.</span><span class="sxs-lookup"><span data-stu-id="c14bd-240">Users have been provided for the various screen layouts.</span></span> <span data-ttu-id="c14bd-241">Ved å bruke tabellen nedenfor, får du tilgang til alle skjermene.</span><span class="sxs-lookup"><span data-stu-id="c14bd-241">By using the following table, you should be able to access any of the screens.</span></span> <span data-ttu-id="c14bd-242">Logg ganske enkelt på ved hjelp av en riktig operator-ID.</span><span class="sxs-lookup"><span data-stu-id="c14bd-242">Just sign in by using an appropriate operator ID.</span></span>

| <span data-ttu-id="c14bd-243">Firma</span><span class="sxs-lookup"><span data-stu-id="c14bd-243">Company</span></span>         | <span data-ttu-id="c14bd-244">Skjermoppsett-ID</span><span class="sxs-lookup"><span data-stu-id="c14bd-244">Screen layout ID</span></span> | <span data-ttu-id="c14bd-245">Egenskap</span><span class="sxs-lookup"><span data-stu-id="c14bd-245">Persona</span></span>          | <span data-ttu-id="c14bd-246">Operatør-ID-er</span><span class="sxs-lookup"><span data-stu-id="c14bd-246">Operator IDs</span></span>           |
|-----------------|------------------|---------------   |------------------------|
| <span data-ttu-id="c14bd-247">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="c14bd-247">Adventure Works</span></span> | <span data-ttu-id="c14bd-248">A3MGR</span><span class="sxs-lookup"><span data-stu-id="c14bd-248">A3MGR</span></span>            | <span data-ttu-id="c14bd-249">Butikksjef</span><span class="sxs-lookup"><span data-stu-id="c14bd-249">Store Manager</span></span>    | <span data-ttu-id="c14bd-250">000154, 000137, 000073</span><span class="sxs-lookup"><span data-stu-id="c14bd-250">000154, 000137, 000073</span></span> |
| <span data-ttu-id="c14bd-251">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="c14bd-251">Adventure Works</span></span> | <span data-ttu-id="c14bd-252">A3CSH</span><span class="sxs-lookup"><span data-stu-id="c14bd-252">A3CSH</span></span>            | <span data-ttu-id="c14bd-253">Kasserer</span><span class="sxs-lookup"><span data-stu-id="c14bd-253">Cashier</span></span>          | <span data-ttu-id="c14bd-254">000150, 000175, 000165</span><span class="sxs-lookup"><span data-stu-id="c14bd-254">000150, 000175, 000165</span></span> |
| <span data-ttu-id="c14bd-255">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="c14bd-255">Adventure Works</span></span> | <span data-ttu-id="c14bd-256">A3STK</span><span class="sxs-lookup"><span data-stu-id="c14bd-256">A3STK</span></span>            | <span data-ttu-id="c14bd-257">Lagermedarbeider</span><span class="sxs-lookup"><span data-stu-id="c14bd-257">Stock Clerk</span></span>      | <span data-ttu-id="c14bd-258">000155, 000181, 000152</span><span class="sxs-lookup"><span data-stu-id="c14bd-258">000155, 000181, 000152</span></span> |
| <span data-ttu-id="c14bd-259">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="c14bd-259">Fabrikam</span></span>        | <span data-ttu-id="c14bd-260">F3MGR</span><span class="sxs-lookup"><span data-stu-id="c14bd-260">F3MGR</span></span>            | <span data-ttu-id="c14bd-261">Butikksjef</span><span class="sxs-lookup"><span data-stu-id="c14bd-261">Store Manager</span></span>    | <span data-ttu-id="c14bd-262">000160, 000168, 000163</span><span class="sxs-lookup"><span data-stu-id="c14bd-262">000160, 000168, 000163</span></span> |
| <span data-ttu-id="c14bd-263">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="c14bd-263">Fabrikam</span></span>        | <span data-ttu-id="c14bd-264">F3CSH</span><span class="sxs-lookup"><span data-stu-id="c14bd-264">F3CSH</span></span>            | <span data-ttu-id="c14bd-265">Kasserer</span><span class="sxs-lookup"><span data-stu-id="c14bd-265">Cashier</span></span>          | <span data-ttu-id="c14bd-266">000161, 000113, 000114</span><span class="sxs-lookup"><span data-stu-id="c14bd-266">000161, 000113, 000114</span></span> |
| <span data-ttu-id="c14bd-267">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="c14bd-267">Fabrikam</span></span>        | <span data-ttu-id="c14bd-268">F3STK</span><span class="sxs-lookup"><span data-stu-id="c14bd-268">F3STK</span></span>            | <span data-ttu-id="c14bd-269">Lagermedarbeider</span><span class="sxs-lookup"><span data-stu-id="c14bd-269">Stock Clerk</span></span>      | <span data-ttu-id="c14bd-270">000164, 000112, 000123</span><span class="sxs-lookup"><span data-stu-id="c14bd-270">000164, 000112, 000123</span></span> |
| <span data-ttu-id="c14bd-271">Contoso</span><span class="sxs-lookup"><span data-stu-id="c14bd-271">Contoso</span></span>         | <span data-ttu-id="c14bd-272">C3MGR</span><span class="sxs-lookup"><span data-stu-id="c14bd-272">C3MGR</span></span>            | <span data-ttu-id="c14bd-273">Butikksjef</span><span class="sxs-lookup"><span data-stu-id="c14bd-273">Store Manager</span></span>    | <span data-ttu-id="c14bd-274">000100, 000111</span><span class="sxs-lookup"><span data-stu-id="c14bd-274">000100, 000111</span></span>         |
| <span data-ttu-id="c14bd-275">Contoso</span><span class="sxs-lookup"><span data-stu-id="c14bd-275">Contoso</span></span>         | <span data-ttu-id="c14bd-276">C3CSH</span><span class="sxs-lookup"><span data-stu-id="c14bd-276">C3CSH</span></span>            | <span data-ttu-id="c14bd-277">Kasserer</span><span class="sxs-lookup"><span data-stu-id="c14bd-277">Cashier</span></span>          | <span data-ttu-id="c14bd-278">000110, 000120</span><span class="sxs-lookup"><span data-stu-id="c14bd-278">000110, 000120</span></span>         |
| <span data-ttu-id="c14bd-279">Contoso</span><span class="sxs-lookup"><span data-stu-id="c14bd-279">Contoso</span></span>         | <span data-ttu-id="c14bd-280">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="c14bd-280">Not applicable</span></span>   | <span data-ttu-id="c14bd-281">Lagermedarbeider</span><span class="sxs-lookup"><span data-stu-id="c14bd-281">Stock Clerk</span></span>      | <span data-ttu-id="c14bd-282">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="c14bd-282">Not applicable</span></span>         |


>[!TIP]
> <span data-ttu-id="c14bd-283">Aktivere en kasse på den tilsvarende butikklokasjonen for best mulig resultat, og angi firmaet til personen som du vil bruke når du logger på.</span><span class="sxs-lookup"><span data-stu-id="c14bd-283">For best results, activate a register in the corresponding store location, and set the company to the company of the persona that you plan to use when you sign in.</span></span> <span data-ttu-id="c14bd-284">På denne måten kan bidra til å garantere at den visuelle profilen og merkebildene er justert på tvers av opplevelsen.</span><span class="sxs-lookup"><span data-stu-id="c14bd-284">In this way, you help guarantee that the visual profile and branding images are aligned across the experience.</span></span> <span data-ttu-id="c14bd-285">Hvis du for eksempel er interessert i å vise et Fabrikam-oppsett for en kasserer, kan du aktivere en kasse i Houston-butikken.</span><span class="sxs-lookup"><span data-stu-id="c14bd-285">For example, if you're interested in seeing a Fabrikam layout for a cashier, you should activate a register in the Houston store.</span></span>


<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail > Channel setup > POS setup > POS > Images**. -->

<!-- ![Images in Dynamics 365 for Retail](../retail/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../retail/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->

