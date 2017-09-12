---
title: Terminologi for produktvariantnumre og navn
description: "Dette emnet beskriver hvordan du kan definere en produktnummerterminologi for å erstatte det faste formatet [Produktstandardnummer - Konfigurasjon - Størrelse - Farge - Stil]. Den nye terminologien har et bestemt format som inkluderer produktstandardnummer, aktive produktdimensjoner og skilletegn for tekst du velger. Du kan også opprette en terminologi for produktnavn. Du kan også bygge en terminologi for å identifisere konfigurasjonene som er opprettet av den restriksjonsbaserte produktkonfiguratoren. Disse terminologiene kan inneholde attributtene du velger."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d1a9ced00d8dc09e59512056392a250a76ba5b97
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="59223-107">Terminologi for produktvariantnumre og navn</span><span class="sxs-lookup"><span data-stu-id="59223-107">Nomenclature of product variant numbers and names</span></span>

<span data-ttu-id="59223-108">Dette emnet beskriver hvordan du kan definere en produktnummerterminologi for å erstatte det faste formatet [Produktstandardnummer - Konfigurasjon - Størrelse - Farge - Stil].</span><span class="sxs-lookup"><span data-stu-id="59223-108">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="59223-109">Den nye terminologien har et bestemt format som inkluderer produktstandardnummer, aktive produktdimensjoner og skilletegn for tekst du velger.</span><span class="sxs-lookup"><span data-stu-id="59223-109">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="59223-110">Du kan også opprette en terminologi for produktnavn.</span><span class="sxs-lookup"><span data-stu-id="59223-110">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="59223-111">Du kan også bygge en terminologi for å identifisere konfigurasjonene som er opprettet av den restriksjonsbaserte produktkonfiguratoren.</span><span class="sxs-lookup"><span data-stu-id="59223-111">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="59223-112">Disse terminologiene kan inneholde attributtene du velger.</span><span class="sxs-lookup"><span data-stu-id="59223-112">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="59223-113">Med de nye terminologiene for produktvariantnumre og navn på produktvariant kan du ta med segmenter i identifikatorene for produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="59223-113">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="59223-114">Disse segmentene kan inkludere produktstandardnummer og navn, produktdimensjon-IDer og navn, nummerserier, tekstkonstanter og attributter.</span><span class="sxs-lookup"><span data-stu-id="59223-114">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="59223-115">Med denne funksjonen kan du raskt finne en bestemt produktvariant når du oppretter en salgsordre eller bestilling.</span><span class="sxs-lookup"><span data-stu-id="59223-115">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="59223-116">Du oppretter terminologier for både produktvariantnumre og produktvariantnavn fra siden **Produktterminologi**.</span><span class="sxs-lookup"><span data-stu-id="59223-116">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="59223-117">Du åpner denne siden ved å klikke **Behandling av produktinformasjon** &gt; **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="59223-117">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="59223-118">Terminologi for forhåndsdefinerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="59223-118">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="59223-119">Produktvarianter genereres for produktstandarder i henhold til én av tre konfigurasjonsteknologier:</span><span class="sxs-lookup"><span data-stu-id="59223-119">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="59223-120">Forhåndsdefinerte varianter</span><span class="sxs-lookup"><span data-stu-id="59223-120">Predefined variants</span></span>
-   <span data-ttu-id="59223-121">Restriksjonsbasert</span><span class="sxs-lookup"><span data-stu-id="59223-121">Constraint-based</span></span>
-   <span data-ttu-id="59223-122">Dimensjonsbasert</span><span class="sxs-lookup"><span data-stu-id="59223-122">Dimension-based</span></span>

<span data-ttu-id="59223-123">Hver produktvariant har et nummer og navn, og med terminologien for produktvariant-ID kan du velge segmentene som skal inkluderes i hvert produktnummervariant og navn.</span><span class="sxs-lookup"><span data-stu-id="59223-123">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="59223-124">Du kan velge de følgende segmentene på siden **Produktterminologi**:</span><span class="sxs-lookup"><span data-stu-id="59223-124">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="59223-125">Produktstandardnummer</span><span class="sxs-lookup"><span data-stu-id="59223-125">Product master number</span></span>
-   <span data-ttu-id="59223-126">Navn på produktstandard</span><span class="sxs-lookup"><span data-stu-id="59223-126">Product master name</span></span>
-   <span data-ttu-id="59223-127">Nummerserieverdi</span><span class="sxs-lookup"><span data-stu-id="59223-127">Number sequence value</span></span>
-   <span data-ttu-id="59223-128">Tekstkonstant</span><span class="sxs-lookup"><span data-stu-id="59223-128">Text constant</span></span>
-   <span data-ttu-id="59223-129">Produktdimensjoner</span><span class="sxs-lookup"><span data-stu-id="59223-129">Product dimensions</span></span>
    -   <span data-ttu-id="59223-130">Konfigurasjons-ID eller navn</span><span class="sxs-lookup"><span data-stu-id="59223-130">Configuration ID or name</span></span>
    -   <span data-ttu-id="59223-131">Farge-ID eller navn</span><span class="sxs-lookup"><span data-stu-id="59223-131">Color ID or name</span></span>
    -   <span data-ttu-id="59223-132">Størrelses-ID eller navn</span><span class="sxs-lookup"><span data-stu-id="59223-132">Size ID or name</span></span>
    -   <span data-ttu-id="59223-133">Stil-ID eller navn</span><span class="sxs-lookup"><span data-stu-id="59223-133">Style ID or name</span></span>

<span data-ttu-id="59223-134">Når terminologien for et produktvariant-ID-nummer er definert, kan det være tilknyttet en produktdimensjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="59223-134">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="59223-135">Alle produktstandarder som refererer til denne dimensjonsgruppen, blir deretter tilordnet produktvariantnumre i henhold til terminologien.</span><span class="sxs-lookup"><span data-stu-id="59223-135">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="59223-136">Terminologier for produktvariantnavn kan imidlertid ikke knyttes til produktdimensjonsgrupper.</span><span class="sxs-lookup"><span data-stu-id="59223-136">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="59223-137">Du kan også tilordne en terminologi for produktvariantidentifikasjon direkte til en produktstandard.</span><span class="sxs-lookup"><span data-stu-id="59223-137">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="59223-138">I så fall tilordnes produktvariantene som hører til produktstandarden, til produktvariantnumre og navn i henhold til terminologiene.</span><span class="sxs-lookup"><span data-stu-id="59223-138">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="59223-139">Eksempel</span><span class="sxs-lookup"><span data-stu-id="59223-139">Example</span></span>

<span data-ttu-id="59223-140">En T-skjorte (TS1234) er produsert i tre størrelser (S, M, L), fire farger (rød, grønn, blå, gul) og to stiler (Polo, V).</span><span class="sxs-lookup"><span data-stu-id="59223-140">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="59223-141">24 produktvarianter er derfor mulig (= 3 × 4 x 2).</span><span class="sxs-lookup"><span data-stu-id="59223-141">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="59223-142">Du kan opprette en terminologi for produktvariantnummer med følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="59223-142">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="59223-143">Produktstandardnummer</span><span class="sxs-lookup"><span data-stu-id="59223-143">Product master number</span></span>
2.  <span data-ttu-id="59223-144">Tekstkonstant: "-"</span><span class="sxs-lookup"><span data-stu-id="59223-144">Text constant: "-"</span></span>
3.  <span data-ttu-id="59223-145">Farge</span><span class="sxs-lookup"><span data-stu-id="59223-145">Color</span></span>
4.  <span data-ttu-id="59223-146">Tekstkonstant: "-"</span><span class="sxs-lookup"><span data-stu-id="59223-146">Text constant: "-"</span></span>
5.  <span data-ttu-id="59223-147">Størrelse</span><span class="sxs-lookup"><span data-stu-id="59223-147">Size</span></span>
6.  <span data-ttu-id="59223-148">Tekstkonstant: "-"</span><span class="sxs-lookup"><span data-stu-id="59223-148">Text constant: "-"</span></span>
7.  <span data-ttu-id="59223-149">Stil</span><span class="sxs-lookup"><span data-stu-id="59223-149">Style</span></span>

<span data-ttu-id="59223-150">I dette tilfellet er produktvariantnummeret for en rød, liten polo-T-skjorte: TS1234-Rød-Small-Polo.</span><span class="sxs-lookup"><span data-stu-id="59223-150">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraintbased-configurations"></a><span data-ttu-id="59223-151">Terminologi for restriksjonsbaserte konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="59223-151">Nomenclature of constraintbased configurations</span></span>
<span data-ttu-id="59223-152">For restriksjonsbaserte konfigurasjoner kan du opprette en dedikert terminologi for konfigurasjonsproduktdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="59223-152">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="59223-153">Du kan velge de følgende segmentene på siden **Produktterminologi**:</span><span class="sxs-lookup"><span data-stu-id="59223-153">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="59223-154">Nummerserieverdi</span><span class="sxs-lookup"><span data-stu-id="59223-154">Number sequence value</span></span>
-   <span data-ttu-id="59223-155">Tekstkonstant</span><span class="sxs-lookup"><span data-stu-id="59223-155">Text constant</span></span>
-   <span data-ttu-id="59223-156">Attributtverdi</span><span class="sxs-lookup"><span data-stu-id="59223-156">Attribute value</span></span>

<span data-ttu-id="59223-157">Hver komponent i en produktkonfigurasjonsmodell kan ha sin egen konfigurasjonsterminologi.</span><span class="sxs-lookup"><span data-stu-id="59223-157">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="59223-158">Bare attributtene som hører til komponenten, kan brukes.</span><span class="sxs-lookup"><span data-stu-id="59223-158">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="59223-159">Attributter fra delkomponenter eller brukerkrav kan ikke brukes.</span><span class="sxs-lookup"><span data-stu-id="59223-159">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="59223-160">Eksempel</span><span class="sxs-lookup"><span data-stu-id="59223-160">Example</span></span>

<span data-ttu-id="59223-161">En produktkonfigurasjonsmodell har en rotkomponenter med to attributter:</span><span class="sxs-lookup"><span data-stu-id="59223-161">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="59223-162">Materialer (plast, tre, stål)</span><span class="sxs-lookup"><span data-stu-id="59223-162">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="59223-163">Lengde (10... 100)</span><span class="sxs-lookup"><span data-stu-id="59223-163">Length (10...100)</span></span>

<span data-ttu-id="59223-164">Du kan opprette en konfigurasjonsterminologi med følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="59223-164">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="59223-165">Attributtverdi: Materiale</span><span class="sxs-lookup"><span data-stu-id="59223-165">Attribute value: Material</span></span>
2.  <span data-ttu-id="59223-166">Tekstkonstant: "AAA"</span><span class="sxs-lookup"><span data-stu-id="59223-166">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="59223-167">Attributtverdi: Lengde</span><span class="sxs-lookup"><span data-stu-id="59223-167">Attribute value: Length</span></span>

<span data-ttu-id="59223-168">I dette tilfellet blir konfigurasjons-ID-en for tremateriale som har en lengde på 78, WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="59223-168">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimensionbased-configurations"></a><span data-ttu-id="59223-169">Terminologi for dimensjonsbasert konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="59223-169">Nomenclature of dimensionbased configurations</span></span>
<span data-ttu-id="59223-170">For dimensjonsbaserte konfigurasjoner kan du opprette en dedikert terminologi for konfigurasjonsproduktdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="59223-170">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="59223-171">Du kan velge de følgende segmentene på siden **Produktterminologi**:</span><span class="sxs-lookup"><span data-stu-id="59223-171">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="59223-172">Nummerserieverdi</span><span class="sxs-lookup"><span data-stu-id="59223-172">Number sequence value</span></span>
-   <span data-ttu-id="59223-173">Tekstkonstant</span><span class="sxs-lookup"><span data-stu-id="59223-173">Text constant</span></span>
-   <span data-ttu-id="59223-174">Konfigurasjonsgruppeelement</span><span class="sxs-lookup"><span data-stu-id="59223-174">Configuration group item</span></span>

<span data-ttu-id="59223-175">Du kan definere en konfigurasjonsterminologi for en stykkliste.</span><span class="sxs-lookup"><span data-stu-id="59223-175">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="59223-176">Eksempel</span><span class="sxs-lookup"><span data-stu-id="59223-176">Example</span></span>

<span data-ttu-id="59223-177">En stykkliste har fire stykklistelinjer som er delt inn i to konfigurasjonsgrupper:</span><span class="sxs-lookup"><span data-stu-id="59223-177">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="59223-178">Stykklistelinje: M0007, Standardkabinett</span><span class="sxs-lookup"><span data-stu-id="59223-178">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="59223-179">Konfigurasjonsgruppe: Kabinett</span><span class="sxs-lookup"><span data-stu-id="59223-179">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="59223-180">Stykklistelinje: M0008, High end-kabinett</span><span class="sxs-lookup"><span data-stu-id="59223-180">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="59223-181">Konfigurasjonsgruppe: Kabinett</span><span class="sxs-lookup"><span data-stu-id="59223-181">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="59223-182">Stykklistelinje: M0021, Frontgrill av tøy</span><span class="sxs-lookup"><span data-stu-id="59223-182">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="59223-183">Konfigurasjonsgruppe: Frontgrill</span><span class="sxs-lookup"><span data-stu-id="59223-183">Configuration group: Front grill</span></span>
-   <span data-ttu-id="59223-184">Stykklistelinje: M0022, Frontgrill metall</span><span class="sxs-lookup"><span data-stu-id="59223-184">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="59223-185">Konfigurasjonsgruppe: Frontgrill</span><span class="sxs-lookup"><span data-stu-id="59223-185">Configuration group: Front grill</span></span>

<span data-ttu-id="59223-186">Du kan opprette en konfigurasjonsterminologi med følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="59223-186">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="59223-187">Konfigurasjonsgruppe: Kabinett</span><span class="sxs-lookup"><span data-stu-id="59223-187">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="59223-188">Tekstkonstant: "&"</span><span class="sxs-lookup"><span data-stu-id="59223-188">Text constant: "&"</span></span>
3.  <span data-ttu-id="59223-189">Konfigurasjonsgruppe: Frontgrill</span><span class="sxs-lookup"><span data-stu-id="59223-189">Configuration group: Front grill</span></span>

<span data-ttu-id="59223-190">I dette tilfellet er konfigurasjons-IDen for et standardkabinett med frontgrill av tøy: M0007 og M0021.</span><span class="sxs-lookup"><span data-stu-id="59223-190">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="59223-191">Terminologi for en kombinasjon av produktvarianter og konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="59223-191">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="59223-192">Når du bruker enten restriksjonsbasert eller dimensjonsbasert konfigurasjonsteknologi til å konfigurere produktvarianter for en produktstandard, kan produktvariantnumrene til produktvariantene inkludere terminologien fra konfigurasjonsdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="59223-192">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="59223-193">Hvis du vil konfigurere varianter, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="59223-193">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="59223-194">Definer en terminologi for et produktvariantnummer som inkluderer konfigurasjonsdimensjonen på siden **Produktterminologi**.</span><span class="sxs-lookup"><span data-stu-id="59223-194">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="59223-195">Tilordne terminologien til en produktdimensjonsgruppe som har konfigurasjonsdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="59223-195">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="59223-196">Definer en konfigurasjonsterminologi for komponentene eller stykklistene som skal brukes til å konfigurere produktvariantene.</span><span class="sxs-lookup"><span data-stu-id="59223-196">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="59223-197">Du kan også opprette en terminologi for produktvariantnavn.</span><span class="sxs-lookup"><span data-stu-id="59223-197">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="59223-198">Produktvariantnavnet kan konfigureres til å inkludere konfigurasjons-ID eller navn.</span><span class="sxs-lookup"><span data-stu-id="59223-198">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="59223-199">Eksempel for restriksjonsbaserte konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="59223-199">Example for constraint-based configurations</span></span>

<span data-ttu-id="59223-200">I dette eksemplet kan du bruke en terminologi for et produktvariantnummer som består av følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="59223-200">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="59223-201">Produktstandardnummer</span><span class="sxs-lookup"><span data-stu-id="59223-201">Product master number</span></span>
2.  <span data-ttu-id="59223-202">Tekstkonstant "\_"</span><span class="sxs-lookup"><span data-stu-id="59223-202">Text constant "\_"</span></span>
3.  <span data-ttu-id="59223-203">Konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="59223-203">Configuration</span></span>

<span data-ttu-id="59223-204">Konfigurasjonsterminologien består av følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="59223-204">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="59223-205">Attributtverdi: Materiale</span><span class="sxs-lookup"><span data-stu-id="59223-205">Attribute value: Material</span></span>
2.  <span data-ttu-id="59223-206">Tekstkonstant: "AAA"</span><span class="sxs-lookup"><span data-stu-id="59223-206">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="59223-207">Attributtverdi: Lengde</span><span class="sxs-lookup"><span data-stu-id="59223-207">Attribute value: Length</span></span>

<span data-ttu-id="59223-208">Du angir følgende verdier for segmenter:</span><span class="sxs-lookup"><span data-stu-id="59223-208">You enter the following values for segments:</span></span>

-   <span data-ttu-id="59223-209">Produktstandardnummer = **M0099**</span><span class="sxs-lookup"><span data-stu-id="59223-209">Product master number = **M0099**</span></span>
-   <span data-ttu-id="59223-210">Materiale = **plast**</span><span class="sxs-lookup"><span data-stu-id="59223-210">Material = **Plastic**</span></span>
-   <span data-ttu-id="59223-211">Lengde = **12**</span><span class="sxs-lookup"><span data-stu-id="59223-211">Length = **12**</span></span>

<span data-ttu-id="59223-212">I dette tilfellet er produktvariantnummeret M0099\_PlasticAAA12.</span><span class="sxs-lookup"><span data-stu-id="59223-212">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="59223-213">Eksempel for dimensjonsbaserte konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="59223-213">Example for dimension-based configurations</span></span>

<span data-ttu-id="59223-214">I dette eksemplet kan du bruke en terminologi for et produktvariantnummer som består av følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="59223-214">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="59223-215">Produktstandardnummer</span><span class="sxs-lookup"><span data-stu-id="59223-215">Product master number</span></span>
2.  <span data-ttu-id="59223-216">Tekstkonstant "//"</span><span class="sxs-lookup"><span data-stu-id="59223-216">Text constant "//"</span></span>
3.  <span data-ttu-id="59223-217">Konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="59223-217">Configuration</span></span>

<span data-ttu-id="59223-218">Konfigurasjonsterminologien består av følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="59223-218">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="59223-219">Konfigurasjonsgruppe: Kabinett</span><span class="sxs-lookup"><span data-stu-id="59223-219">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="59223-220">Tekstkonstant: "&"</span><span class="sxs-lookup"><span data-stu-id="59223-220">Text constant: "&"</span></span>
3.  <span data-ttu-id="59223-221">Konfigurasjonsgruppe: Frontgrill</span><span class="sxs-lookup"><span data-stu-id="59223-221">Configuration group: Front grill</span></span>

<span data-ttu-id="59223-222">Du angir følgende verdier for segmenter:</span><span class="sxs-lookup"><span data-stu-id="59223-222">You enter the following values for segments:</span></span>

-   <span data-ttu-id="59223-223">Produktstandardnummer = **D0123**</span><span class="sxs-lookup"><span data-stu-id="59223-223">Product master number = **D0123**</span></span>
-   <span data-ttu-id="59223-224">Kabinett = **M0008**</span><span class="sxs-lookup"><span data-stu-id="59223-224">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="59223-225">Frontgrill = **M0022**</span><span class="sxs-lookup"><span data-stu-id="59223-225">Front grill = **M0022**</span></span>

<span data-ttu-id="59223-226">I dette tilfellet er produktvariantnummeret D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="59223-226">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="59223-227">Nummereringskonflikter</span><span class="sxs-lookup"><span data-stu-id="59223-227">Numbering conflicts</span></span>
<span data-ttu-id="59223-228">I noen tilfeller kan det hende at en terminologi for produktvariantnummer du angir, ikke fører til ulike produktvariantnumre.</span><span class="sxs-lookup"><span data-stu-id="59223-228">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="59223-229">Dette kan for eksempel skje hvis produktvariantnumrene ikke er unike hvis én aktiv produktdimensjon ikke er inkludert i terminologien for en produktstandard som bruker forhåndsdefinerte variantkonfigurasjonsteknologi.</span><span class="sxs-lookup"><span data-stu-id="59223-229">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="59223-230">Måten du håndterer konflikter på, varierer avhengig av konfigurasjonsteknologien.</span><span class="sxs-lookup"><span data-stu-id="59223-230">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="59223-231">Forhåndsdefinerte varianter</span><span class="sxs-lookup"><span data-stu-id="59223-231">Predefined variants</span></span>

<span data-ttu-id="59223-232">Det vil oppstå en feil hvis du manuelt oppretter eller automatisk prøver å generere produktvarianter der én eller flere fører til samme produktvariantnummer.</span><span class="sxs-lookup"><span data-stu-id="59223-232">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="59223-233">Hvis du vil unngå denne situasjonen, bør du bruke alle aktive produktdimensjoner i produktdimensjonsgruppen.</span><span class="sxs-lookup"><span data-stu-id="59223-233">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="59223-234">Du kan også inkludere en nummerserie for å garantere at produktvariantnumrene er unike.</span><span class="sxs-lookup"><span data-stu-id="59223-234">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="59223-235">Restriksjonsbaserte konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="59223-235">Constraint-based configurations</span></span>

<span data-ttu-id="59223-236">Avhengig av terminologien kan systemet prøve å tilordne et ikke-unikt produktvariantnummer til en konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="59223-236">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="59223-237">I så fall vil systemet bruke nummerserien for konfigurasjonsdimensjonen som produktvariantnummer i stedet, og du får en advarsel.</span><span class="sxs-lookup"><span data-stu-id="59223-237">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="59223-238">Hvis du vil unngå denne situasjonen, bør du ta med nok attributter i terminologien for å garantere unike produktvariantnumre.</span><span class="sxs-lookup"><span data-stu-id="59223-238">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="59223-239">Du bør også kontrollere at alternativet **Bruk på nytt** er merket av for komponenten.</span><span class="sxs-lookup"><span data-stu-id="59223-239">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="59223-240">Dimensjonsbaserte konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="59223-240">Dimension-based configurations</span></span>

<span data-ttu-id="59223-241">Under ett trinn i konfigurasjonsprosessen foreslår systemet en konfigurasjonsverdi i henhold til terminologien.</span><span class="sxs-lookup"><span data-stu-id="59223-241">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="59223-242">I dette trinnet kan du endre konfigurasjonsverdien manuelt.</span><span class="sxs-lookup"><span data-stu-id="59223-242">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="59223-243">Når du lagrer konfigurasjonen, kontrolleres det om konfigurasjonsverdien er unik.</span><span class="sxs-lookup"><span data-stu-id="59223-243">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="59223-244">Hvis verdien du angav, ikke er unik, får du en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="59223-244">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="59223-245">For å lagre konfigurasjonen må du angi en unik konfigurasjonsverdi.</span><span class="sxs-lookup"><span data-stu-id="59223-245">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="see-also"></a><span data-ttu-id="59223-246">Se også</span><span class="sxs-lookup"><span data-stu-id="59223-246">See also</span></span>
--------

[<span data-ttu-id="59223-247">Opprette produktnummerterminologi for forhåndsdefinerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="59223-247">Create a product number nomenclature for predefined product variants</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/create-product-number-nomenclature-predefined-variants-2016-11)

[<span data-ttu-id="59223-248">Opprette produktnummerterminologi for konfigurerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="59223-248">Create a product number nomenclature for configured product variants</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/create-product-number-nomenclature-product-variants_2016_11)


