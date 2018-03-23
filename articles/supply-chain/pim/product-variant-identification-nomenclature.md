---
title: Terminologi for produktvariantnumre og navn
description: "Dette emnet beskriver hvordan du kan definere en produktnummerterminologi for å erstatte det faste formatet [Produktstandardnummer - Konfigurasjon - Størrelse - Farge - Stil]."
author: roxanadiaconu
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 6a620f2a0105d578d419d3aac816c7d78fbf3e46
ms.contentlocale: nb-no
ms.lasthandoff: 03/08/2018

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="28bc3-103">Terminologi for produktvariantnumre og navn</span><span class="sxs-lookup"><span data-stu-id="28bc3-103">Nomenclature of product variant numbers and names</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="28bc3-104">Dette emnet beskriver hvordan du kan definere en produktnummerterminologi for å erstatte det faste formatet [Produktstandardnummer - Konfigurasjon - Størrelse - Farge - Stil].</span><span class="sxs-lookup"><span data-stu-id="28bc3-104">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="28bc3-105">Den nye terminologien har et bestemt format som inkluderer produktstandardnummer, aktive produktdimensjoner og skilletegn for tekst du velger.</span><span class="sxs-lookup"><span data-stu-id="28bc3-105">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="28bc3-106">Du kan også opprette en terminologi for produktnavn.</span><span class="sxs-lookup"><span data-stu-id="28bc3-106">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="28bc3-107">Du kan også bygge en terminologi for å identifisere konfigurasjonene som er opprettet av den restriksjonsbaserte produktkonfiguratoren.</span><span class="sxs-lookup"><span data-stu-id="28bc3-107">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="28bc3-108">Disse terminologiene kan inneholde attributtene du velger.</span><span class="sxs-lookup"><span data-stu-id="28bc3-108">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="28bc3-109">Med de nye terminologiene for produktvariantnumre og navn på produktvariant kan du ta med segmenter i identifikatorene for produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="28bc3-109">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="28bc3-110">Disse segmentene kan inkludere produktstandardnummer og navn, produktdimensjon-IDer og navn, nummerserier, tekstkonstanter og attributter.</span><span class="sxs-lookup"><span data-stu-id="28bc3-110">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="28bc3-111">Med denne funksjonen kan du raskt finne en bestemt produktvariant når du oppretter en salgsordre eller bestilling.</span><span class="sxs-lookup"><span data-stu-id="28bc3-111">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="28bc3-112">Du oppretter terminologier for både produktvariantnumre og produktvariantnavn fra siden **Produktterminologi**.</span><span class="sxs-lookup"><span data-stu-id="28bc3-112">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="28bc3-113">Du åpner denne siden ved å klikke **Behandling av produktinformasjon** &gt; **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="28bc3-113">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="28bc3-114">Terminologi for forhåndsdefinerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="28bc3-114">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="28bc3-115">Produktvarianter genereres for produktstandarder i henhold til én av tre konfigurasjonsteknologier:</span><span class="sxs-lookup"><span data-stu-id="28bc3-115">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="28bc3-116">Forhåndsdefinerte varianter</span><span class="sxs-lookup"><span data-stu-id="28bc3-116">Predefined variants</span></span>
-   <span data-ttu-id="28bc3-117">Restriksjonsbasert</span><span class="sxs-lookup"><span data-stu-id="28bc3-117">Constraint-based</span></span>
-   <span data-ttu-id="28bc3-118">Dimensjonsbasert</span><span class="sxs-lookup"><span data-stu-id="28bc3-118">Dimension-based</span></span>

<span data-ttu-id="28bc3-119">Hver produktvariant har et nummer og navn, og med terminologien for produktvariant-ID kan du velge segmentene som skal inkluderes i hvert produktnummervariant og navn.</span><span class="sxs-lookup"><span data-stu-id="28bc3-119">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="28bc3-120">Du kan velge de følgende segmentene på siden **Produktterminologi**:</span><span class="sxs-lookup"><span data-stu-id="28bc3-120">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="28bc3-121">Produktstandardnummer</span><span class="sxs-lookup"><span data-stu-id="28bc3-121">Product master number</span></span>
-   <span data-ttu-id="28bc3-122">Navn på produktstandard</span><span class="sxs-lookup"><span data-stu-id="28bc3-122">Product master name</span></span>
-   <span data-ttu-id="28bc3-123">Nummerserieverdi</span><span class="sxs-lookup"><span data-stu-id="28bc3-123">Number sequence value</span></span>
-   <span data-ttu-id="28bc3-124">Tekstkonstant</span><span class="sxs-lookup"><span data-stu-id="28bc3-124">Text constant</span></span>
-   <span data-ttu-id="28bc3-125">Produktdimensjoner</span><span class="sxs-lookup"><span data-stu-id="28bc3-125">Product dimensions</span></span>
    -   <span data-ttu-id="28bc3-126">Konfigurasjons-ID eller navn</span><span class="sxs-lookup"><span data-stu-id="28bc3-126">Configuration ID or name</span></span>
    -   <span data-ttu-id="28bc3-127">Farge-ID eller navn</span><span class="sxs-lookup"><span data-stu-id="28bc3-127">Color ID or name</span></span>
    -   <span data-ttu-id="28bc3-128">Størrelses-ID eller navn</span><span class="sxs-lookup"><span data-stu-id="28bc3-128">Size ID or name</span></span>
    -   <span data-ttu-id="28bc3-129">Stil-ID eller navn</span><span class="sxs-lookup"><span data-stu-id="28bc3-129">Style ID or name</span></span>

<span data-ttu-id="28bc3-130">Når terminologien for et produktvariant-ID-nummer er definert, kan det være tilknyttet en produktdimensjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="28bc3-130">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="28bc3-131">Alle produktstandarder som refererer til denne dimensjonsgruppen, blir deretter tilordnet produktvariantnumre i henhold til terminologien.</span><span class="sxs-lookup"><span data-stu-id="28bc3-131">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="28bc3-132">Terminologier for produktvariantnavn kan imidlertid ikke knyttes til produktdimensjonsgrupper.</span><span class="sxs-lookup"><span data-stu-id="28bc3-132">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="28bc3-133">Du kan også tilordne en terminologi for produktvariantidentifikasjon direkte til en produktstandard.</span><span class="sxs-lookup"><span data-stu-id="28bc3-133">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="28bc3-134">I så fall tilordnes produktvariantene som hører til produktstandarden, til produktvariantnumre og navn i henhold til terminologiene.</span><span class="sxs-lookup"><span data-stu-id="28bc3-134">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="28bc3-135">Eksempel</span><span class="sxs-lookup"><span data-stu-id="28bc3-135">Example</span></span>

<span data-ttu-id="28bc3-136">En T-skjorte (TS1234) er produsert i tre størrelser (S, M, L), fire farger (rød, grønn, blå, gul) og to stiler (Polo, V).</span><span class="sxs-lookup"><span data-stu-id="28bc3-136">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="28bc3-137">24 produktvarianter er derfor mulig (= 3 × 4 x 2).</span><span class="sxs-lookup"><span data-stu-id="28bc3-137">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="28bc3-138">Du kan opprette en terminologi for produktvariantnummer med følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="28bc3-138">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="28bc3-139">Produktstandardnummer</span><span class="sxs-lookup"><span data-stu-id="28bc3-139">Product master number</span></span>
2.  <span data-ttu-id="28bc3-140">Tekstkonstant: "-"</span><span class="sxs-lookup"><span data-stu-id="28bc3-140">Text constant: "-"</span></span>
3.  <span data-ttu-id="28bc3-141">Farge</span><span class="sxs-lookup"><span data-stu-id="28bc3-141">Color</span></span>
4.  <span data-ttu-id="28bc3-142">Tekstkonstant: "-"</span><span class="sxs-lookup"><span data-stu-id="28bc3-142">Text constant: "-"</span></span>
5.  <span data-ttu-id="28bc3-143">Størrelse</span><span class="sxs-lookup"><span data-stu-id="28bc3-143">Size</span></span>
6.  <span data-ttu-id="28bc3-144">Tekstkonstant: "-"</span><span class="sxs-lookup"><span data-stu-id="28bc3-144">Text constant: "-"</span></span>
7.  <span data-ttu-id="28bc3-145">Stil</span><span class="sxs-lookup"><span data-stu-id="28bc3-145">Style</span></span>

<span data-ttu-id="28bc3-146">I dette tilfellet er produktvariantnummeret for en rød, liten polo-T-skjorte: TS1234-Rød-Small-Polo.</span><span class="sxs-lookup"><span data-stu-id="28bc3-146">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraint-based-configurations"></a><span data-ttu-id="28bc3-147">Terminologi for restriksjonsbaserte konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="28bc3-147">Nomenclature of constraint-based configurations</span></span>
<span data-ttu-id="28bc3-148">For restriksjonsbaserte konfigurasjoner kan du opprette en dedikert terminologi for konfigurasjonsproduktdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="28bc3-148">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="28bc3-149">Du kan velge de følgende segmentene på siden **Produktterminologi**:</span><span class="sxs-lookup"><span data-stu-id="28bc3-149">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="28bc3-150">Nummerserieverdi</span><span class="sxs-lookup"><span data-stu-id="28bc3-150">Number sequence value</span></span>
-   <span data-ttu-id="28bc3-151">Tekstkonstant</span><span class="sxs-lookup"><span data-stu-id="28bc3-151">Text constant</span></span>
-   <span data-ttu-id="28bc3-152">Attributtverdi</span><span class="sxs-lookup"><span data-stu-id="28bc3-152">Attribute value</span></span>

<span data-ttu-id="28bc3-153">Hver komponent i en produktkonfigurasjonsmodell kan ha sin egen konfigurasjonsterminologi.</span><span class="sxs-lookup"><span data-stu-id="28bc3-153">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="28bc3-154">Bare attributtene som hører til komponenten, kan brukes.</span><span class="sxs-lookup"><span data-stu-id="28bc3-154">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="28bc3-155">Attributter fra delkomponenter eller brukerkrav kan ikke brukes.</span><span class="sxs-lookup"><span data-stu-id="28bc3-155">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="28bc3-156">Eksempel</span><span class="sxs-lookup"><span data-stu-id="28bc3-156">Example</span></span>

<span data-ttu-id="28bc3-157">En produktkonfigurasjonsmodell har en rotkomponenter med to attributter:</span><span class="sxs-lookup"><span data-stu-id="28bc3-157">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="28bc3-158">Materialer (plast, tre, stål)</span><span class="sxs-lookup"><span data-stu-id="28bc3-158">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="28bc3-159">Lengde (10... 100)</span><span class="sxs-lookup"><span data-stu-id="28bc3-159">Length (10...100)</span></span>

<span data-ttu-id="28bc3-160">Du kan opprette en konfigurasjonsterminologi med følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="28bc3-160">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="28bc3-161">Attributtverdi: Materiale</span><span class="sxs-lookup"><span data-stu-id="28bc3-161">Attribute value: Material</span></span>
2.  <span data-ttu-id="28bc3-162">Tekstkonstant: "AAA"</span><span class="sxs-lookup"><span data-stu-id="28bc3-162">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="28bc3-163">Attributtverdi: Lengde</span><span class="sxs-lookup"><span data-stu-id="28bc3-163">Attribute value: Length</span></span>

<span data-ttu-id="28bc3-164">I dette tilfellet blir konfigurasjons-ID-en for tremateriale som har en lengde på 78, WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="28bc3-164">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimension-based-configurations"></a><span data-ttu-id="28bc3-165">Terminologi for dimensjonsbasert konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="28bc3-165">Nomenclature of dimension-based configurations</span></span>
<span data-ttu-id="28bc3-166">For dimensjonsbaserte konfigurasjoner kan du opprette en dedikert terminologi for konfigurasjonsproduktdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="28bc3-166">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="28bc3-167">Du kan velge de følgende segmentene på siden **Produktterminologi**:</span><span class="sxs-lookup"><span data-stu-id="28bc3-167">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="28bc3-168">Nummerserieverdi</span><span class="sxs-lookup"><span data-stu-id="28bc3-168">Number sequence value</span></span>
-   <span data-ttu-id="28bc3-169">Tekstkonstant</span><span class="sxs-lookup"><span data-stu-id="28bc3-169">Text constant</span></span>
-   <span data-ttu-id="28bc3-170">Konfigurasjonsgruppeelement</span><span class="sxs-lookup"><span data-stu-id="28bc3-170">Configuration group item</span></span>

<span data-ttu-id="28bc3-171">Du kan definere en konfigurasjonsterminologi for en stykkliste.</span><span class="sxs-lookup"><span data-stu-id="28bc3-171">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="28bc3-172">Eksempel</span><span class="sxs-lookup"><span data-stu-id="28bc3-172">Example</span></span>

<span data-ttu-id="28bc3-173">En stykkliste har fire stykklistelinjer som er delt inn i to konfigurasjonsgrupper:</span><span class="sxs-lookup"><span data-stu-id="28bc3-173">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="28bc3-174">Stykklistelinje: M0007, Standardkabinett</span><span class="sxs-lookup"><span data-stu-id="28bc3-174">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="28bc3-175">Konfigurasjonsgruppe: Kabinett</span><span class="sxs-lookup"><span data-stu-id="28bc3-175">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="28bc3-176">Stykklistelinje: M0008, High end-kabinett</span><span class="sxs-lookup"><span data-stu-id="28bc3-176">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="28bc3-177">Konfigurasjonsgruppe: Kabinett</span><span class="sxs-lookup"><span data-stu-id="28bc3-177">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="28bc3-178">Stykklistelinje: M0021, Frontgrill av tøy</span><span class="sxs-lookup"><span data-stu-id="28bc3-178">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="28bc3-179">Konfigurasjonsgruppe: Frontgrill</span><span class="sxs-lookup"><span data-stu-id="28bc3-179">Configuration group: Front grill</span></span>
-   <span data-ttu-id="28bc3-180">Stykklistelinje: M0022, Frontgrill metall</span><span class="sxs-lookup"><span data-stu-id="28bc3-180">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="28bc3-181">Konfigurasjonsgruppe: Frontgrill</span><span class="sxs-lookup"><span data-stu-id="28bc3-181">Configuration group: Front grill</span></span>

<span data-ttu-id="28bc3-182">Du kan opprette en konfigurasjonsterminologi med følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="28bc3-182">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="28bc3-183">Konfigurasjonsgruppe: Kabinett</span><span class="sxs-lookup"><span data-stu-id="28bc3-183">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="28bc3-184">Tekstkonstant: "&"</span><span class="sxs-lookup"><span data-stu-id="28bc3-184">Text constant: "&"</span></span>
3.  <span data-ttu-id="28bc3-185">Konfigurasjonsgruppe: Frontgrill</span><span class="sxs-lookup"><span data-stu-id="28bc3-185">Configuration group: Front grill</span></span>

<span data-ttu-id="28bc3-186">I dette tilfellet er konfigurasjons-IDen for et standardkabinett med frontgrill av tøy: M0007 og M0021.</span><span class="sxs-lookup"><span data-stu-id="28bc3-186">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="28bc3-187">Terminologi for en kombinasjon av produktvarianter og konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="28bc3-187">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="28bc3-188">Når du bruker enten restriksjonsbasert eller dimensjonsbasert konfigurasjonsteknologi til å konfigurere produktvarianter for en produktstandard, kan produktvariantnumrene til produktvariantene inkludere terminologien fra konfigurasjonsdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="28bc3-188">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="28bc3-189">Hvis du vil konfigurere varianter, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="28bc3-189">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="28bc3-190">Definer en terminologi for et produktvariantnummer som inkluderer konfigurasjonsdimensjonen på siden **Produktterminologi**.</span><span class="sxs-lookup"><span data-stu-id="28bc3-190">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="28bc3-191">Tilordne terminologien til en produktdimensjonsgruppe som har konfigurasjonsdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="28bc3-191">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="28bc3-192">Definer en konfigurasjonsterminologi for komponentene eller stykklistene som skal brukes til å konfigurere produktvariantene.</span><span class="sxs-lookup"><span data-stu-id="28bc3-192">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="28bc3-193">Du kan også opprette en terminologi for produktvariantnavn.</span><span class="sxs-lookup"><span data-stu-id="28bc3-193">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="28bc3-194">Produktvariantnavnet kan konfigureres til å inkludere konfigurasjons-ID eller navn.</span><span class="sxs-lookup"><span data-stu-id="28bc3-194">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="28bc3-195">Eksempel for restriksjonsbaserte konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="28bc3-195">Example for constraint-based configurations</span></span>

<span data-ttu-id="28bc3-196">I dette eksemplet kan du bruke en terminologi for et produktvariantnummer som består av følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="28bc3-196">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="28bc3-197">Produktstandardnummer</span><span class="sxs-lookup"><span data-stu-id="28bc3-197">Product master number</span></span>
2.  <span data-ttu-id="28bc3-198">Tekstkonstant "\_"</span><span class="sxs-lookup"><span data-stu-id="28bc3-198">Text constant "\_"</span></span>
3.  <span data-ttu-id="28bc3-199">Konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="28bc3-199">Configuration</span></span>

<span data-ttu-id="28bc3-200">Konfigurasjonsterminologien består av følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="28bc3-200">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="28bc3-201">Attributtverdi: Materiale</span><span class="sxs-lookup"><span data-stu-id="28bc3-201">Attribute value: Material</span></span>
2.  <span data-ttu-id="28bc3-202">Tekstkonstant: "AAA"</span><span class="sxs-lookup"><span data-stu-id="28bc3-202">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="28bc3-203">Attributtverdi: Lengde</span><span class="sxs-lookup"><span data-stu-id="28bc3-203">Attribute value: Length</span></span>

<span data-ttu-id="28bc3-204">Du angir følgende verdier for segmenter:</span><span class="sxs-lookup"><span data-stu-id="28bc3-204">You enter the following values for segments:</span></span>

-   <span data-ttu-id="28bc3-205">Produktstandardnummer = **M0099**</span><span class="sxs-lookup"><span data-stu-id="28bc3-205">Product master number = **M0099**</span></span>
-   <span data-ttu-id="28bc3-206">Materiale = **plast**</span><span class="sxs-lookup"><span data-stu-id="28bc3-206">Material = **Plastic**</span></span>
-   <span data-ttu-id="28bc3-207">Lengde = **12**</span><span class="sxs-lookup"><span data-stu-id="28bc3-207">Length = **12**</span></span>

<span data-ttu-id="28bc3-208">I dette tilfellet er produktvariantnummeret M0099\_PlasticAAA12.</span><span class="sxs-lookup"><span data-stu-id="28bc3-208">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="28bc3-209">Eksempel for dimensjonsbaserte konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="28bc3-209">Example for dimension-based configurations</span></span>

<span data-ttu-id="28bc3-210">I dette eksemplet kan du bruke en terminologi for et produktvariantnummer som består av følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="28bc3-210">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="28bc3-211">Produktstandardnummer</span><span class="sxs-lookup"><span data-stu-id="28bc3-211">Product master number</span></span>
2.  <span data-ttu-id="28bc3-212">Tekstkonstant "//"</span><span class="sxs-lookup"><span data-stu-id="28bc3-212">Text constant "//"</span></span>
3.  <span data-ttu-id="28bc3-213">Konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="28bc3-213">Configuration</span></span>

<span data-ttu-id="28bc3-214">Konfigurasjonsterminologien består av følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="28bc3-214">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="28bc3-215">Konfigurasjonsgruppe: Kabinett</span><span class="sxs-lookup"><span data-stu-id="28bc3-215">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="28bc3-216">Tekstkonstant: "&"</span><span class="sxs-lookup"><span data-stu-id="28bc3-216">Text constant: "&"</span></span>
3.  <span data-ttu-id="28bc3-217">Konfigurasjonsgruppe: Frontgrill</span><span class="sxs-lookup"><span data-stu-id="28bc3-217">Configuration group: Front grill</span></span>

<span data-ttu-id="28bc3-218">Du angir følgende verdier for segmenter:</span><span class="sxs-lookup"><span data-stu-id="28bc3-218">You enter the following values for segments:</span></span>

-   <span data-ttu-id="28bc3-219">Produktstandardnummer = **D0123**</span><span class="sxs-lookup"><span data-stu-id="28bc3-219">Product master number = **D0123**</span></span>
-   <span data-ttu-id="28bc3-220">Kabinett = **M0008**</span><span class="sxs-lookup"><span data-stu-id="28bc3-220">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="28bc3-221">Frontgrill = **M0022**</span><span class="sxs-lookup"><span data-stu-id="28bc3-221">Front grill = **M0022**</span></span>

<span data-ttu-id="28bc3-222">I dette tilfellet er produktvariantnummeret D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="28bc3-222">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="28bc3-223">Nummereringskonflikter</span><span class="sxs-lookup"><span data-stu-id="28bc3-223">Numbering conflicts</span></span>
<span data-ttu-id="28bc3-224">I noen tilfeller kan det hende at en terminologi for produktvariantnummer du angir, ikke fører til ulike produktvariantnumre.</span><span class="sxs-lookup"><span data-stu-id="28bc3-224">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="28bc3-225">Dette kan for eksempel skje hvis produktvariantnumrene ikke er unike hvis én aktiv produktdimensjon ikke er inkludert i terminologien for en produktstandard som bruker forhåndsdefinerte variantkonfigurasjonsteknologi.</span><span class="sxs-lookup"><span data-stu-id="28bc3-225">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="28bc3-226">Måten du håndterer konflikter på, varierer avhengig av konfigurasjonsteknologien.</span><span class="sxs-lookup"><span data-stu-id="28bc3-226">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="28bc3-227">Forhåndsdefinerte varianter</span><span class="sxs-lookup"><span data-stu-id="28bc3-227">Predefined variants</span></span>

<span data-ttu-id="28bc3-228">Det vil oppstå en feil hvis du manuelt oppretter eller automatisk prøver å generere produktvarianter der én eller flere fører til samme produktvariantnummer.</span><span class="sxs-lookup"><span data-stu-id="28bc3-228">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="28bc3-229">Hvis du vil unngå denne situasjonen, bør du bruke alle aktive produktdimensjoner i produktdimensjonsgruppen.</span><span class="sxs-lookup"><span data-stu-id="28bc3-229">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="28bc3-230">Du kan også inkludere en nummerserie for å garantere at produktvariantnumrene er unike.</span><span class="sxs-lookup"><span data-stu-id="28bc3-230">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="28bc3-231">Restriksjonsbaserte konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="28bc3-231">Constraint-based configurations</span></span>

<span data-ttu-id="28bc3-232">Avhengig av terminologien kan systemet prøve å tilordne et ikke-unikt produktvariantnummer til en konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="28bc3-232">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="28bc3-233">I så fall vil systemet bruke nummerserien for konfigurasjonsdimensjonen som produktvariantnummer i stedet, og du får en advarsel.</span><span class="sxs-lookup"><span data-stu-id="28bc3-233">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="28bc3-234">Hvis du vil unngå denne situasjonen, bør du ta med nok attributter i terminologien for å garantere unike produktvariantnumre.</span><span class="sxs-lookup"><span data-stu-id="28bc3-234">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="28bc3-235">Du bør også kontrollere at alternativet **Bruk på nytt** er merket av for komponenten.</span><span class="sxs-lookup"><span data-stu-id="28bc3-235">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="28bc3-236">Dimensjonsbaserte konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="28bc3-236">Dimension-based configurations</span></span>

<span data-ttu-id="28bc3-237">Under ett trinn i konfigurasjonsprosessen foreslår systemet en konfigurasjonsverdi i henhold til terminologien.</span><span class="sxs-lookup"><span data-stu-id="28bc3-237">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="28bc3-238">I dette trinnet kan du endre konfigurasjonsverdien manuelt.</span><span class="sxs-lookup"><span data-stu-id="28bc3-238">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="28bc3-239">Når du lagrer konfigurasjonen, kontrolleres det om konfigurasjonsverdien er unik.</span><span class="sxs-lookup"><span data-stu-id="28bc3-239">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="28bc3-240">Hvis verdien du angav, ikke er unik, får du en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="28bc3-240">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="28bc3-241">For å lagre konfigurasjonen må du angi en unik konfigurasjonsverdi.</span><span class="sxs-lookup"><span data-stu-id="28bc3-241">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="see-also"></a><span data-ttu-id="28bc3-242">Se også</span><span class="sxs-lookup"><span data-stu-id="28bc3-242">See also</span></span>
--------

[<span data-ttu-id="28bc3-243">Opprette produktnummerterminologi for forhåndsdefinerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="28bc3-243">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="28bc3-244">Opprette produktnummerterminologi for konfigurerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="28bc3-244">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)


