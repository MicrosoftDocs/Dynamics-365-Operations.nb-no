---
title: Uttrykksbegrensninger og tabellbegrensninger i produktkonfigurasjonsmodeller
description: "Dette emnet beskriver bruken av uttrykks- og tabellbegrensninger. Begrensninger kontrollerer attributtverdiene du kan velge når du konfigurerer produkter for en salgsordre, et salgstilbud, en bestilling eller en produksjonsordre. Du kan bruke uttrykksbegrensninger eller tabellbegrensninger, avhengig av hvordan du foretrekker å bygge begrensningene."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 3206e53c4f2659c6d9b9be64b01ac28cdd17bc88
ms.contentlocale: nb-no
ms.lasthandoff: 02/07/2018

---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="85514-105">Uttrykksbegrensninger og tabellbegrensninger i produktkonfigurasjonsmodeller</span><span class="sxs-lookup"><span data-stu-id="85514-105">Expression constraints and table constraints in product configuration models</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="85514-106">Dette emnet beskriver bruken av uttrykks- og tabellbegrensninger.</span><span class="sxs-lookup"><span data-stu-id="85514-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="85514-107">Begrensninger kontrollerer attributtverdiene du kan velge når du konfigurerer produkter for en salgsordre, et salgstilbud, en bestilling eller en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="85514-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="85514-108">Du kan bruke uttrykksbegrensninger eller tabellbegrensninger, avhengig av hvordan du foretrekker å bygge begrensningene.</span><span class="sxs-lookup"><span data-stu-id="85514-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="85514-109">Begrensninger brukes til å kontrollere attributtverdiene du kan velge når du konfigurerer produkter for en salgsordre, et salgstilbud, en bestilling eller en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="85514-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="85514-110">Du kan bruke uttrykksbegrensninger eller tabellbegrensninger, avhengig av hvordan du foretrekker å bygge begrensningene.</span><span class="sxs-lookup"><span data-stu-id="85514-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="85514-111">Hva er uttrykksbegrensninger?</span><span class="sxs-lookup"><span data-stu-id="85514-111">What are expression constraints?</span></span>
<span data-ttu-id="85514-112">Uttrykksbegrensninger kjennetegnes ved et uttrykk som bruker aritmetiske og boolske operatorer og funksjoner.</span><span class="sxs-lookup"><span data-stu-id="85514-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="85514-113">En uttrykksrestriksjon skrives for en bestemt komponent i en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="85514-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="85514-114">Det kan ikke brukes på nytt eller deles med en annen komponent.</span><span class="sxs-lookup"><span data-stu-id="85514-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="85514-115">Uttrykksbegrensningene for en komponent kan imidlertid referere til attributter for delkomponenter for komponenten.</span><span class="sxs-lookup"><span data-stu-id="85514-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="85514-116">Hva er tabellbegrensninger?</span><span class="sxs-lookup"><span data-stu-id="85514-116">What are table constraints?</span></span>
<span data-ttu-id="85514-117">Tabellbegrensninger viser kombinasjonene av verdier som er tillatt for attributter når du konfigurerer et produkt.</span><span class="sxs-lookup"><span data-stu-id="85514-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="85514-118">Definisjoner av tabellbegrensninger kan brukes generelt.</span><span class="sxs-lookup"><span data-stu-id="85514-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="85514-119">Når du oppretter en tabellbegrensning for en komponent i en produktkonfigurasjonsmodell, velger du en tabellbegrensningsdefinisjon.</span><span class="sxs-lookup"><span data-stu-id="85514-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="85514-120">Hvis du vil opprette kombinasjonene som er tillatt, legger du til attributter for bestemte typer i komponentene.</span><span class="sxs-lookup"><span data-stu-id="85514-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="85514-121">Hver attributt har en bestemt verdi.</span><span class="sxs-lookup"><span data-stu-id="85514-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="85514-122">Eksempel på tabellbegrensning</span><span class="sxs-lookup"><span data-stu-id="85514-122">Example of a table constraint</span></span>

<span data-ttu-id="85514-123">Dette eksemplet viser hvordan du kan begrense konfigurasjonen av en høyttaler til bestemte kabinettyper og fronter.</span><span class="sxs-lookup"><span data-stu-id="85514-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="85514-124">Den første tabellen viser kabinettyper og fronter som vanligvis er tilgjengelige for konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="85514-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="85514-125">Verdiene er definert for attribyttypene **Kabinettyper** og **Frontgrill**.</span><span class="sxs-lookup"><span data-stu-id="85514-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="85514-126">Attributtype</span><span class="sxs-lookup"><span data-stu-id="85514-126">Attribute type</span></span> | <span data-ttu-id="85514-127">Verdier</span><span class="sxs-lookup"><span data-stu-id="85514-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="85514-128">Kabinettyper</span><span class="sxs-lookup"><span data-stu-id="85514-128">Cabinet finish</span></span> | <span data-ttu-id="85514-129">Svart, eik, Rosewood, hvit</span><span class="sxs-lookup"><span data-stu-id="85514-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="85514-130">Frontgrill</span><span class="sxs-lookup"><span data-stu-id="85514-130">Front grill</span></span>    | <span data-ttu-id="85514-131">Svart, metall, hvit</span><span class="sxs-lookup"><span data-stu-id="85514-131">Black, Metal, White</span></span>         |

<span data-ttu-id="85514-132">Den neste tabellen viser kombinasjonene som er definert av tabellbegrensningen **Farge og finish**.</span><span class="sxs-lookup"><span data-stu-id="85514-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="85514-133">Ved å bruke denne tabellbegrensningen, kan du konfigurere en høyttaler som har eik-finish og en svart grill, en Rosewood-finish og en hvit grill og så videre.</span><span class="sxs-lookup"><span data-stu-id="85514-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="85514-134">Ferdig</span><span class="sxs-lookup"><span data-stu-id="85514-134">Finish</span></span>         | <span data-ttu-id="85514-135">Grill</span><span class="sxs-lookup"><span data-stu-id="85514-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="85514-136">Eik</span><span class="sxs-lookup"><span data-stu-id="85514-136">Oak</span></span>            | <span data-ttu-id="85514-137">Svart</span><span class="sxs-lookup"><span data-stu-id="85514-137">Black</span></span>                       |
| <span data-ttu-id="85514-138">Rosewood</span><span class="sxs-lookup"><span data-stu-id="85514-138">Rosewood</span></span>       | <span data-ttu-id="85514-139">Hvit</span><span class="sxs-lookup"><span data-stu-id="85514-139">White</span></span>                       |
| <span data-ttu-id="85514-140">Hvit</span><span class="sxs-lookup"><span data-stu-id="85514-140">White</span></span>          | <span data-ttu-id="85514-141">Svart</span><span class="sxs-lookup"><span data-stu-id="85514-141">Black</span></span>                       |
| <span data-ttu-id="85514-142">Hvit</span><span class="sxs-lookup"><span data-stu-id="85514-142">White</span></span>          | <span data-ttu-id="85514-143">Hvit</span><span class="sxs-lookup"><span data-stu-id="85514-143">White</span></span>                       |
| <span data-ttu-id="85514-144">Svart</span><span class="sxs-lookup"><span data-stu-id="85514-144">Black</span></span>          | <span data-ttu-id="85514-145">Svart</span><span class="sxs-lookup"><span data-stu-id="85514-145">Black</span></span>                       |
| <span data-ttu-id="85514-146">Svart</span><span class="sxs-lookup"><span data-stu-id="85514-146">Black</span></span>          | <span data-ttu-id="85514-147">Metall</span><span class="sxs-lookup"><span data-stu-id="85514-147">Metal</span></span>                       | 

<span data-ttu-id="85514-148">Du kan opprette systemdefinerte og brukerdefinerte tabellbegrensninger.</span><span class="sxs-lookup"><span data-stu-id="85514-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="85514-149">Hvis du vil ha mer informasjon, se [Sy
stemdefinerte og brukerdefinerte tabellbegrensninger](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="85514-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="85514-150">Hvilken syntaks skal brukes for å skrive begrensninger?</span><span class="sxs-lookup"><span data-stu-id="85514-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="85514-151">Du må bruke OML-syntaks (Optimization Modeling Language) når skriver begrensningene.</span><span class="sxs-lookup"><span data-stu-id="85514-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="85514-152">Systemet bruker Microsoft Solver Foundation-begrensningsløseren til å løse begrensningene.</span><span class="sxs-lookup"><span data-stu-id="85514-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="85514-153">Bør jeg bruke tabellbegrensninger eller uttrykksbegrensninger?</span><span class="sxs-lookup"><span data-stu-id="85514-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="85514-154">Du kan enten bruke uttrykksbegrensninger eller tabellbegrensninger, avhengig av hvordan du foretrekker å bygge begrensningene.</span><span class="sxs-lookup"><span data-stu-id="85514-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="85514-155">Du bygger opp en tabellbegrensning som en matrise, mens en uttrykksrestriksjon er et enkeltuttrykk.</span><span class="sxs-lookup"><span data-stu-id="85514-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="85514-156">Når du konfigurerer et produkt, spiller det ingen rolle hvilken type betingelse som brukes.</span><span class="sxs-lookup"><span data-stu-id="85514-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="85514-157">Følgende eksempel viser forskjellen mellom de to metodene.</span><span class="sxs-lookup"><span data-stu-id="85514-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="85514-158">Når du konfigurerer et produkt ved hjelp av følgende begrensningsoppsett, er disse kombinasjonene tillatt:</span><span class="sxs-lookup"><span data-stu-id="85514-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="85514-159">Et produkt i fargen svart og størrelse 30 eller 50</span><span class="sxs-lookup"><span data-stu-id="85514-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="85514-160">Et produkt i fargen rødt og størrelse 20</span><span class="sxs-lookup"><span data-stu-id="85514-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="85514-161">Tabellbegrensningsoppsett</span><span class="sxs-lookup"><span data-stu-id="85514-161">Table constraint setup</span></span>

| <span data-ttu-id="85514-162">Farge</span><span class="sxs-lookup"><span data-stu-id="85514-162">Color</span></span> | <span data-ttu-id="85514-163">Størrelse</span><span class="sxs-lookup"><span data-stu-id="85514-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="85514-164">Svart</span><span class="sxs-lookup"><span data-stu-id="85514-164">Black</span></span> | <span data-ttu-id="85514-165">30</span><span class="sxs-lookup"><span data-stu-id="85514-165">30</span></span>   |
| <span data-ttu-id="85514-166">Svart</span><span class="sxs-lookup"><span data-stu-id="85514-166">Black</span></span> | <span data-ttu-id="85514-167">50</span><span class="sxs-lookup"><span data-stu-id="85514-167">50</span></span>   |
| <span data-ttu-id="85514-168">Rød</span><span class="sxs-lookup"><span data-stu-id="85514-168">Red</span></span>   | <span data-ttu-id="85514-169">20</span><span class="sxs-lookup"><span data-stu-id="85514-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="85514-170">Uttrykksrestriksjonsoppsett</span><span class="sxs-lookup"><span data-stu-id="85514-170">Expression constraint setup</span></span>

<span data-ttu-id="85514-171">(Farge == "Svart" & (størrelse == "30" | størrelse == "50")) | (farge == "Rød" & størrelse = "20")</span><span class="sxs-lookup"><span data-stu-id="85514-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="85514-172">Bør jeg bruke operatorer eller infiksnotasjoner når jeg skriver uttrykksbegrensninger?</span><span class="sxs-lookup"><span data-stu-id="85514-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="85514-173">Du kan skrive en uttrykksbegrensning ved å bruke de tilgjengelige prefiksoperatorene eller ved hjelp av en infix-notasjon.</span><span class="sxs-lookup"><span data-stu-id="85514-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="85514-174">For operatorene **Min**, **Maks** og **Abs** kan du ikke bruke en infix-notasjon.</span><span class="sxs-lookup"><span data-stu-id="85514-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="85514-175">Disse operatorene er inkludert som standard i de fleste programmeringsspråk.</span><span class="sxs-lookup"><span data-stu-id="85514-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="85514-176">Hvilke operatorer og infiksnotasjoner kan jeg bruke når jeg skriver uttrykksbegrensninger?</span><span class="sxs-lookup"><span data-stu-id="85514-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="85514-177">Tabellen nedenfor viser operatorene og infix-notasjonene som du kan bruke når du skriver en uttrykksrestriksjon for en komponent i en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="85514-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="85514-178">I eksemplene i den første tabellen kan du se hvordan du skriver inn et uttrykk med infiksnotasjon eller operatorer.</span><span class="sxs-lookup"><span data-stu-id="85514-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85514-179">Operatør</span><span class="sxs-lookup"><span data-stu-id="85514-179">Operator</span></span></th>
<th><span data-ttu-id="85514-180">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="85514-180">Description</span></span></th>
<th><span data-ttu-id="85514-181">Syntaks</span><span class="sxs-lookup"><span data-stu-id="85514-181">Syntax</span></span></th>
<th><span data-ttu-id="85514-182">Eksempler</span><span class="sxs-lookup"><span data-stu-id="85514-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="85514-183">Implies</span><span class="sxs-lookup"><span data-stu-id="85514-183">Implies</span></span></td>
<td><span data-ttu-id="85514-184">Dette er tilfelle hvis den første betingelsen er Usann, den andre betingelsen er Sann, eller begge deler.</span><span class="sxs-lookup"><span data-stu-id="85514-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="85514-185">Implies[a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="85514-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="85514-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="85514-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="85514-187"><strong>Infiksnotasjon:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="85514-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85514-188">Og</span><span class="sxs-lookup"><span data-stu-id="85514-188">And</span></span></td>
<td><span data-ttu-id="85514-189">Dette gjelder bare hvis alle betingelsene er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="85514-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="85514-190">Hvis antallet betingelser er 0 (null), gir den <strong>True</strong>.</span><span class="sxs-lookup"><span data-stu-id="85514-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="85514-191">And[argumenter], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="85514-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="85514-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="85514-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="85514-193"><strong>Infiksnotasjon:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="85514-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85514-194">Eller</span><span class="sxs-lookup"><span data-stu-id="85514-194">Or</span></span></td>
<td><span data-ttu-id="85514-195">Dette er tilfelle hvis en betingelse er Sann.</span><span class="sxs-lookup"><span data-stu-id="85514-195">This is true if any condition is true.</span></span> <span data-ttu-id="85514-196">Hvis antallet betingelser er 0 (null), gir den <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="85514-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="85514-197">Or[argumenter], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="85514-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="85514-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="85514-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="85514-199"><strong>Infiksnotasjon:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="85514-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85514-200">Pluss</span><span class="sxs-lookup"><span data-stu-id="85514-200">Plus</span></span></td>
<td><span data-ttu-id="85514-201">Det summerer betingelsene.</span><span class="sxs-lookup"><span data-stu-id="85514-201">This sums its conditions.</span></span> <span data-ttu-id="85514-202">Hvis antallet betingelser er 0 (null), gir den <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="85514-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="85514-203">Plus[argumenter], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="85514-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="85514-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="85514-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="85514-205"><strong>Infiksnotasjon:</strong> x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="85514-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85514-206">Minus</span><span class="sxs-lookup"><span data-stu-id="85514-206">Minus</span></span></td>
<td><span data-ttu-id="85514-207">Dette opphever argumentet.</span><span class="sxs-lookup"><span data-stu-id="85514-207">This negates its argument.</span></span> <span data-ttu-id="85514-208">Dette må ha nøyaktig én betingelse.</span><span class="sxs-lookup"><span data-stu-id="85514-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="85514-209">Minus[uttrykk], infiks: -uttrykk</span><span class="sxs-lookup"><span data-stu-id="85514-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="85514-210"><strong>Operator:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="85514-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="85514-211"><strong>Infiksnotasjon:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="85514-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85514-212">Abs</span><span class="sxs-lookup"><span data-stu-id="85514-212">Abs</span></span></td>
<td><span data-ttu-id="85514-213">Dette krever absoluttverdien til betingelsen.</span><span class="sxs-lookup"><span data-stu-id="85514-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="85514-214">Dette må ha nøyaktig én betingelse.</span><span class="sxs-lookup"><span data-stu-id="85514-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="85514-215">Abs[expr]</span><span class="sxs-lookup"><span data-stu-id="85514-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="85514-216"><strong>Operator:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="85514-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85514-217">Klokkeslett</span><span class="sxs-lookup"><span data-stu-id="85514-217">Times</span></span></td>
<td><span data-ttu-id="85514-218">Dette tar produktet for betingelsene.</span><span class="sxs-lookup"><span data-stu-id="85514-218">This takes the product of its conditions.</span></span> <span data-ttu-id="85514-219">Hvis antallet betingelser er 0 (null), gir den <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="85514-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="85514-220">Times[argumenter], infix: a \* b \* ... \* z</span><span class="sxs-lookup"><span data-stu-id="85514-220">Times[args], infix: a \* b \* ... \* z</span></span></td>
<td><ul>
<li><span data-ttu-id="85514-221"><strong>Operator:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="85514-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="85514-222"><strong>Infiksnotasjon:</strong> x * y * 2 == z</span><span class="sxs-lookup"><span data-stu-id="85514-222"><strong>Infix notation:</strong> x * y * 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85514-223">Styrke</span><span class="sxs-lookup"><span data-stu-id="85514-223">Power</span></span></td>
<td><span data-ttu-id="85514-224">Dette krever en eksponentiell verdi.</span><span class="sxs-lookup"><span data-stu-id="85514-224">This takes an exponential.</span></span> <span data-ttu-id="85514-225">Dette gjelder eksponentiering fra høyre mot venstre.</span><span class="sxs-lookup"><span data-stu-id="85514-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="85514-226">Det vil si den er høyre-assosiativ, og derfor tilsvarer <strong>Kraft[a, b, c]</strong> <strong>Kraft[a, Kraft[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="85514-226">(In other words, it's right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="85514-227"><strong>Styrke</strong> kan bare brukes med en positiv konstant som eksponent.</span><span class="sxs-lookup"><span data-stu-id="85514-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="85514-228">Styrke[argumenter], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="85514-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="85514-229"><strong>Operator:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="85514-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="85514-230"><strong>Infiksnotasjon:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="85514-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85514-231">Maks.</span><span class="sxs-lookup"><span data-stu-id="85514-231">Max</span></span></td>
<td><span data-ttu-id="85514-232">Dette gir den største betingelsen.</span><span class="sxs-lookup"><span data-stu-id="85514-232">This produces the largest condition.</span></span> <span data-ttu-id="85514-233">Hvis antallet betingelser er 0 (null), gir den <strong>Infinity</strong>.</span><span class="sxs-lookup"><span data-stu-id="85514-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="85514-234">Max[argumenter]</span><span class="sxs-lookup"><span data-stu-id="85514-234">Max[args]</span></span></td>
<td><span data-ttu-id="85514-235"><strong>Operator:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="85514-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85514-236">Min.</span><span class="sxs-lookup"><span data-stu-id="85514-236">Min</span></span></td>
<td><span data-ttu-id="85514-237">Dette gir den minste betingelsen.</span><span class="sxs-lookup"><span data-stu-id="85514-237">This produces the smallest condition.</span></span> <span data-ttu-id="85514-238">Hvis antallet betingelser er 0 (null), gir den <strong>Infinity</strong>.</span><span class="sxs-lookup"><span data-stu-id="85514-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="85514-239">Min[argumenter]</span><span class="sxs-lookup"><span data-stu-id="85514-239">Min[args]</span></span></td>
<td><span data-ttu-id="85514-240"><strong>Operator:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="85514-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85514-241">Ikke</span><span class="sxs-lookup"><span data-stu-id="85514-241">Not</span></span></td>
<td><span data-ttu-id="85514-242">Dette gir det logisk motsatte av betingelsen.</span><span class="sxs-lookup"><span data-stu-id="85514-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="85514-243">Dette må ha nøyaktig én betingelse.</span><span class="sxs-lookup"><span data-stu-id="85514-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="85514-244">Not[uttrykk], infiks: !uttrykk</span><span class="sxs-lookup"><span data-stu-id="85514-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="85514-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span><span class="sxs-lookup"><span data-stu-id="85514-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="85514-246"><strong>Infiksnotasjon:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="85514-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="85514-247">Eksemplene i den neste tabellen viser hvordan du skriver en infix-notasjon.</span><span class="sxs-lookup"><span data-stu-id="85514-247">The examples in the next table show how to write infix notation.</span></span>

| <span data-ttu-id="85514-248">Infiksnotasjon</span><span class="sxs-lookup"><span data-stu-id="85514-248">Infix notation</span></span>    | <span data-ttu-id="85514-249">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="85514-249">Description</span></span>                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="85514-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="85514-250">x + y + z</span></span>         | <span data-ttu-id="85514-251">Tillegg</span><span class="sxs-lookup"><span data-stu-id="85514-251">Addition</span></span>                                                                                      |
| <span data-ttu-id="85514-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="85514-252">x \* y \* z</span></span>       | <span data-ttu-id="85514-253">Multiplikasjon</span><span class="sxs-lookup"><span data-stu-id="85514-253">Multiplication</span></span>                                                                                |
| <span data-ttu-id="85514-254">x - y</span><span class="sxs-lookup"><span data-stu-id="85514-254">x - y</span></span>             | <span data-ttu-id="85514-255">Binær subtraksjon oversettes på samme måte som binær addisjon med en negert andreverdi.</span><span class="sxs-lookup"><span data-stu-id="85514-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
| <span data-ttu-id="85514-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="85514-256">x ^ y ^ z</span></span>         | <span data-ttu-id="85514-257">Eksponentiering med høyre-assosiativitet</span><span class="sxs-lookup"><span data-stu-id="85514-257">Exponentiation that has right associativity</span></span>                                                   |
| <span data-ttu-id="85514-258">!x</span><span class="sxs-lookup"><span data-stu-id="85514-258">!x</span></span>                | <span data-ttu-id="85514-259">Boolsk ikke</span><span class="sxs-lookup"><span data-stu-id="85514-259">Boolean not</span></span>                                                                                   |
| <span data-ttu-id="85514-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="85514-260">x -: y</span></span>            | <span data-ttu-id="85514-261">Boolsk implikasjon</span><span class="sxs-lookup"><span data-stu-id="85514-261">Boolean implication</span></span>                                                                           |
| <span data-ttu-id="85514-262">x</span><span class="sxs-lookup"><span data-stu-id="85514-262">x</span></span> | <span data-ttu-id="85514-263">y</span><span class="sxs-lookup"><span data-stu-id="85514-263">y</span></span> | <span data-ttu-id="85514-264">z</span><span class="sxs-lookup"><span data-stu-id="85514-264">z</span></span>         | <span data-ttu-id="85514-265">Boolsk eller</span><span class="sxs-lookup"><span data-stu-id="85514-265">Boolean or</span></span>                                                                                    |
| <span data-ttu-id="85514-266">x & y & z</span><span class="sxs-lookup"><span data-stu-id="85514-266">x & y & z</span></span>         | <span data-ttu-id="85514-267">Boolsk og</span><span class="sxs-lookup"><span data-stu-id="85514-267">Boolean and</span></span>                                                                                   |
| <span data-ttu-id="85514-268">x == y == z</span><span class="sxs-lookup"><span data-stu-id="85514-268">x == y == z</span></span>       | <span data-ttu-id="85514-269">Likhet</span><span class="sxs-lookup"><span data-stu-id="85514-269">Equality</span></span>                                                                                      |
| <span data-ttu-id="85514-270">x != y != z</span><span class="sxs-lookup"><span data-stu-id="85514-270">x != y != z</span></span>       | <span data-ttu-id="85514-271">Spesifikk</span><span class="sxs-lookup"><span data-stu-id="85514-271">Distinct</span></span>                                                                                      |
| <span data-ttu-id="85514-272">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="85514-272">x &lt; y &lt; z</span></span>   | <span data-ttu-id="85514-273">Mindre enn</span><span class="sxs-lookup"><span data-stu-id="85514-273">Less than</span></span>                                                                                     |
| <span data-ttu-id="85514-274">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="85514-274">x &gt; y &gt; z</span></span>   | <span data-ttu-id="85514-275">Større enn</span><span class="sxs-lookup"><span data-stu-id="85514-275">Greater than</span></span>                                                                                  |
| <span data-ttu-id="85514-276">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="85514-276">x &lt;= y &lt;= z</span></span> | <span data-ttu-id="85514-277">Mindre eller lik</span><span class="sxs-lookup"><span data-stu-id="85514-277">Less than or equal to</span></span>                                                                         |
| <span data-ttu-id="85514-278">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="85514-278">x &gt;= y &gt;= z</span></span> | <span data-ttu-id="85514-279">Større enn eller lik</span><span class="sxs-lookup"><span data-stu-id="85514-279">Greater than or equal to</span></span>                                                                      |
| <span data-ttu-id="85514-280">(x)</span><span class="sxs-lookup"><span data-stu-id="85514-280">(x)</span></span>               | <span data-ttu-id="85514-281">Parenteser overstyrer standardprioritet.</span><span class="sxs-lookup"><span data-stu-id="85514-281">Parentheses override default precedence.</span></span>                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="85514-282">Hvorfor valideres ikke uttrykksbegrensningene mine riktig?</span><span class="sxs-lookup"><span data-stu-id="85514-282">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="85514-283">Du kan ikke bruke reserverte nøkkelord som problemløsernavn for attributter, komponenter eller delkomponenter i en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="85514-283">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span> <span data-ttu-id="85514-284">Her er en liste over reserverte nøkkelord som du ikke kan bruke:</span><span class="sxs-lookup"><span data-stu-id="85514-284">Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="85514-285">Tak</span><span class="sxs-lookup"><span data-stu-id="85514-285">Ceiling</span></span>
-   <span data-ttu-id="85514-286">Element</span><span class="sxs-lookup"><span data-stu-id="85514-286">Element</span></span>
-   <span data-ttu-id="85514-287">Lik</span><span class="sxs-lookup"><span data-stu-id="85514-287">Equal</span></span>
-   <span data-ttu-id="85514-288">Gulv</span><span class="sxs-lookup"><span data-stu-id="85514-288">Floor</span></span>
-   <span data-ttu-id="85514-289">Hvis</span><span class="sxs-lookup"><span data-stu-id="85514-289">If</span></span>
-   <span data-ttu-id="85514-290">Mindre</span><span class="sxs-lookup"><span data-stu-id="85514-290">Less</span></span>
-   <span data-ttu-id="85514-291">Større</span><span class="sxs-lookup"><span data-stu-id="85514-291">Greater</span></span>
-   <span data-ttu-id="85514-292">Implies</span><span class="sxs-lookup"><span data-stu-id="85514-292">Implies</span></span>
-   <span data-ttu-id="85514-293">Logg</span><span class="sxs-lookup"><span data-stu-id="85514-293">Log</span></span>
-   <span data-ttu-id="85514-294">Maks.</span><span class="sxs-lookup"><span data-stu-id="85514-294">Max</span></span>
-   <span data-ttu-id="85514-295">Min.</span><span class="sxs-lookup"><span data-stu-id="85514-295">Min</span></span>
-   <span data-ttu-id="85514-296">Minus</span><span class="sxs-lookup"><span data-stu-id="85514-296">Minus</span></span>
-   <span data-ttu-id="85514-297">Pluss</span><span class="sxs-lookup"><span data-stu-id="85514-297">Plus</span></span>
-   <span data-ttu-id="85514-298">Styrke</span><span class="sxs-lookup"><span data-stu-id="85514-298">Power</span></span>
-   <span data-ttu-id="85514-299">Tider</span><span class="sxs-lookup"><span data-stu-id="85514-299">Times</span></span>
-   <span data-ttu-id="85514-300">Spor</span><span class="sxs-lookup"><span data-stu-id="85514-300">Slot</span></span>
-   <span data-ttu-id="85514-301">Modell</span><span class="sxs-lookup"><span data-stu-id="85514-301">Model</span></span>
-   <span data-ttu-id="85514-302">Beslutningsprofil</span><span class="sxs-lookup"><span data-stu-id="85514-302">Decision</span></span>
-   <span data-ttu-id="85514-303">Mål</span><span class="sxs-lookup"><span data-stu-id="85514-303">Goal</span></span>


<a name="see-also"></a><span data-ttu-id="85514-304">Se også</span><span class="sxs-lookup"><span data-stu-id="85514-304">See also</span></span>
--------

<span data-ttu-id="85514-305">[Opprett en uttrykksbegrensning (Oppgaveguide)](tasks/add-expression-constraint-product-configuration-model.md)</span><span class="sxs-lookup"><span data-stu-id="85514-305">[Create an expression constraint (Task guide)(tasks/add-expression-constraint-product-configuration-model.md)</span></span>

[<span data-ttu-id="85514-306">Legge til beregning i en produktkonfigurasjonsmodell (oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="85514-306">Add a calculation to a product configuration model (Task guide)</span></span>](tasks/add-calculation-product-configuration-model.md)




