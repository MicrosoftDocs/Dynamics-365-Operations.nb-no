---
title: Arbeidspolicyer for lager
description: "Arbeidspolicyer for lager kontrollerer om lagerarbeid opprettes for lagerprosesser i produksjon, basert på arbeidsordretype, lagerlokasjon og produkt."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6023f74972bcc3c3110b8efb5ce9bb1558aa2efb
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="warehouse-work-policies"></a><span data-ttu-id="360a7-103">Arbeidspolicyer for lager</span><span class="sxs-lookup"><span data-stu-id="360a7-103">Warehouse work policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="360a7-104">Arbeidspolicyer i Microsoft Dynamics 365 for Finance and Operations kontrollerer om lagerarbeid opprettes for lagerprosesser i produksjon, basert på arbeidsordretype, lagerlokasjon og produkt.</span><span class="sxs-lookup"><span data-stu-id="360a7-104">Warehouse work policies in Microsoft Dynamics 365 for Finance and Operations control whether warehouse work is created by warehouse processes in manufacturing, based on work order type, inventory location, and product.</span></span>

<span data-ttu-id="360a7-105">Denne arbeidspolicyen kontrollerer om lagerarbeid opprettes for lagerprosesser i produksjon.</span><span class="sxs-lookup"><span data-stu-id="360a7-105">This work policy controls whether warehouse work is created for warehouse processes in manufacturing.</span></span> <span data-ttu-id="360a7-106">Du kan definere arbeidspolicyen ved hjelp av en kombinasjon av **arbeidsordretyper**, en **lagerplassering** og et **produkt**.</span><span class="sxs-lookup"><span data-stu-id="360a7-106">You can set up the work policy by using a combination of **work order types**, an **inventory location**, and a **product**.</span></span> <span data-ttu-id="360a7-107">Produkt L0101 rapporteres for eksempel som ferdig til utleveringslokasjon 001.</span><span class="sxs-lookup"><span data-stu-id="360a7-107">For example, product L0101 is reported as finished to output location 001.</span></span> <span data-ttu-id="360a7-108">Den ferdige varen forbrukes senere i en annen produksjonsordre på utleveringslokasjon 001.</span><span class="sxs-lookup"><span data-stu-id="360a7-108">The finished good is later consumed in another production order at output location 001.</span></span> <span data-ttu-id="360a7-109">I så fall kan du definere en arbeidspolicy for å hindre at arbeidet for plassering av ferdigvarer blir opprettet når du rapporterer produkt L0101 som ferdige, til utleveringslokasjon 001.</span><span class="sxs-lookup"><span data-stu-id="360a7-109">In this case, you can set up a work policy to prevent the work for finished goods put-away from being created when you report product L0101 as finished to output location 001.</span></span> <span data-ttu-id="360a7-110">Arbeidspolicyen er en enkeltenhet som kan beskrives ved hjelp av følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="360a7-110">The work policy is an individual entity that can be described through the following information:</span></span>

-   <span data-ttu-id="360a7-111">**Arbeidspolicynavn**(den unike ID-en for arbeidspolicyen)</span><span class="sxs-lookup"><span data-stu-id="360a7-111">**Work policy name** (the unique identifier of the work policy)</span></span>
-   <span data-ttu-id="360a7-112">**Arbeideordretyper** og **arbeidsopprettelsesmetode**</span><span class="sxs-lookup"><span data-stu-id="360a7-112">**Work order types** and **Work creation method**</span></span>
-   <span data-ttu-id="360a7-113">**Lagerlokasjoner**</span><span class="sxs-lookup"><span data-stu-id="360a7-113">**Inventory locations**</span></span>
-   <span data-ttu-id="360a7-114">**Produkter**</span><span class="sxs-lookup"><span data-stu-id="360a7-114">**Products**</span></span>

## <a name="work-order-types"></a><span data-ttu-id="360a7-115">Arbeidsordretyper</span><span class="sxs-lookup"><span data-stu-id="360a7-115">Work order types</span></span>
<span data-ttu-id="360a7-116">Du kan velge blant følgende arbeidsordretyper:</span><span class="sxs-lookup"><span data-stu-id="360a7-116">You can select the following work order types:</span></span>

-   <span data-ttu-id="360a7-117">Plasser ferdigvarer</span><span class="sxs-lookup"><span data-stu-id="360a7-117">Finished goods put away</span></span>
-   <span data-ttu-id="360a7-118">Plasser koprodukt og biprodukt</span><span class="sxs-lookup"><span data-stu-id="360a7-118">Co-product and by-product put away</span></span>
-   <span data-ttu-id="360a7-119">Råvareplukking</span><span class="sxs-lookup"><span data-stu-id="360a7-119">Raw material picking</span></span>

<span data-ttu-id="360a7-120">**Arbeidsopprettelsesmetode**-feltet har verdien **Aldri**.</span><span class="sxs-lookup"><span data-stu-id="360a7-120">The **Work creation method** field has the value **Never**.</span></span> <span data-ttu-id="360a7-121">Denne verdien angir at arbeidspolicyen hindrer at lagerarbeid opprettes for den valgte arbeidsordretypen.</span><span class="sxs-lookup"><span data-stu-id="360a7-121">This value indicates that the work policy will prevent warehouse work from being created for the selected work order type.</span></span>

## <a name="inventory-locations"></a><span data-ttu-id="360a7-122">Lagerlokasjoner</span><span class="sxs-lookup"><span data-stu-id="360a7-122">Inventory locations</span></span>
<span data-ttu-id="360a7-123">Du kan velge en lokasjon som arbeidspolicyen gjelder for.</span><span class="sxs-lookup"><span data-stu-id="360a7-123">You can select a location that the work policy applies to.</span></span> <span data-ttu-id="360a7-124">Hvis ingen lokasjon er knyttet til en arbeidspolicy, gjelder ikke arbeidspolicyen for noen prosesser.</span><span class="sxs-lookup"><span data-stu-id="360a7-124">If no location is associated with a work policy, the work policy doesn’t apply to any processes.</span></span> <span data-ttu-id="360a7-125">På **Lokasjoner**-siden du kan også merke eller fjerne merkingen av arbeidspolicyen for en bestemt lokasjon.</span><span class="sxs-lookup"><span data-stu-id="360a7-125">On the **Locations** page, you can also select or cancel the selection of the work policy for a specific location.</span></span>

## <a name="products"></a><span data-ttu-id="360a7-126">Produkter</span><span class="sxs-lookup"><span data-stu-id="360a7-126">Products</span></span>
<span data-ttu-id="360a7-127">Du kan velge et produkt som arbeidspolicyen gjelder for.</span><span class="sxs-lookup"><span data-stu-id="360a7-127">You can select a product that the work policy applies to.</span></span> <span data-ttu-id="360a7-128">Du kan bruke arbeidspolicyen på alle produkter eller valgte produkter.</span><span class="sxs-lookup"><span data-stu-id="360a7-128">You can apply the work policy to either all products or selected products.</span></span>

## <a name="example"></a><span data-ttu-id="360a7-129">Eksempel</span><span class="sxs-lookup"><span data-stu-id="360a7-129">Example</span></span>
<span data-ttu-id="360a7-130">I eksemplet nedenfor er det to produksjonsordrer, PRD-001 og PRD 00*2*.</span><span class="sxs-lookup"><span data-stu-id="360a7-130">In the following example, there are two production orders, PRD-001 and PRD-00*2*.</span></span> <span data-ttu-id="360a7-131">Produksjonsordren PRD-001 har en operasjon kalt **Montering**, der produktet SC1 rapporteres som ferdig til lokasjonen O1.</span><span class="sxs-lookup"><span data-stu-id="360a7-131">Production order PRD-001 has an operation that is named **Assembly**, where product SC1 is being reported as finished to location O1.</span></span> <span data-ttu-id="360a7-132">Produksjonsordren PRD-002 er en operasjon kalt **Maling**, og den bruker SC1-produktet fra lokasjonen O1.</span><span class="sxs-lookup"><span data-stu-id="360a7-132">Production order PRD-002 has an operation that is named **Painting** and consumes product SC1 from location O1.</span></span> <span data-ttu-id="360a7-133">Produksjonsordren PRD-002 bruker også råvaren RM1 fra lokasjonen O1.</span><span class="sxs-lookup"><span data-stu-id="360a7-133">Production order PRD-002 also consumes raw material RM1 from location O1.</span></span> <span data-ttu-id="360a7-134">RM1 er lagret i lagerlokasjonen BULK-001 og blir plukket til lokasjon O1 av lagerarbeid for plukking av råvarer.</span><span class="sxs-lookup"><span data-stu-id="360a7-134">RM1 is stored in warehouse location BULK-001 and will be picked to location O1 by warehouse work for raw material picking.</span></span> <span data-ttu-id="360a7-135">Plukkarbeidet blir generert når produksjonen PRD-002 frigis.</span><span class="sxs-lookup"><span data-stu-id="360a7-135">The picking work is generated when production PRD-002 is released.</span></span> 

<span data-ttu-id="360a7-136">[![Arbeidspolicyer for lager](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="360a7-136">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span> 

<span data-ttu-id="360a7-137">Når du skal konfigurere en arbeidspolicy for lageret i dette scenariet, bør du vurdere følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="360a7-137">When you plan to configure a warehouse work policy for this scenario, you should consider the following information:</span></span>

-   <span data-ttu-id="360a7-138">Lagerarbeid for plassering av ferdigvarer er ikke nødvendig når du rapporterer produktet SC1 som ferdig fra produksjonordren PRD-001 til lokasjonen O1.</span><span class="sxs-lookup"><span data-stu-id="360a7-138">Warehouse work for finished goods put-away isn’t required when you report product SC1 as finished from production order PRD-001 to location O1.</span></span> <span data-ttu-id="360a7-139">Dette skjer fordi operasjonen **Maling** for produksjonsordre PRD-002 bruker SC1 på samme lokasjon.</span><span class="sxs-lookup"><span data-stu-id="360a7-139">This is because the **Painting** operation for production order PRD-002 consumes SC1 at the same location.</span></span>
-   <span data-ttu-id="360a7-140">Lagerarbeid for plukking av råvarer kreves for å flytte råvaren RM1 fra lagerlokasjonen BULK-001 til lokasjonen O1.</span><span class="sxs-lookup"><span data-stu-id="360a7-140">Warehouse work for raw material picking is required in order to move raw material RM1 from warehouse location BULK-001 to location O1.</span></span>

<span data-ttu-id="360a7-141">Her er et eksempel på arbeidspolicyen som du kan sette opp, basert på disse hensynene.</span><span class="sxs-lookup"><span data-stu-id="360a7-141">Here is an example of the work policy that you can set up, based on these considerations.</span></span>


|                                       |                                       |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="360a7-142"><strong>Arbeidspolicynavn</strong></span><span class="sxs-lookup"><span data-stu-id="360a7-142"><strong>Work policy name</strong></span></span><br> | <span data-ttu-id="360a7-143"><strong>Arbeidsordretyper</strong></span><span class="sxs-lookup"><span data-stu-id="360a7-143"><strong>Work order types</strong></span></span><br> |
|         <span data-ttu-id="360a7-144">Ingen plassering 01     \`</span><span class="sxs-lookup"><span data-stu-id="360a7-144">No put away 01     \`</span></span>          |     <span data-ttu-id="360a7-145">- Plassering av ferdigvare</span><span class="sxs-lookup"><span data-stu-id="360a7-145">- Finished good put away</span></span><br>      |
|                                       |    <span data-ttu-id="360a7-146"><strong>Lokasjoner</strong></span><span class="sxs-lookup"><span data-stu-id="360a7-146"><strong>Locations</strong></span></span><br>     |
|                                       |                 <span data-ttu-id="360a7-147">- O1</span><span class="sxs-lookup"><span data-stu-id="360a7-147">- O1</span></span>                  |
|                                       |    <span data-ttu-id="360a7-148"><strong>Produkter</strong></span><span class="sxs-lookup"><span data-stu-id="360a7-148"><strong>Products</strong></span></span> <br>     |
|                                       |                 <span data-ttu-id="360a7-149">- SC1</span><span class="sxs-lookup"><span data-stu-id="360a7-149">- SC1</span></span>                 |

<span data-ttu-id="360a7-150">Fremgangsmåtene nedenfor inneholder trinnvise instruksjoner om hvordan du definerer lagerarbeidspolicyen i dette scenariet.</span><span class="sxs-lookup"><span data-stu-id="360a7-150">The following procedures provide step-by-step instructions about how to set up the warehouse work policy for this scenario.</span></span> <span data-ttu-id="360a7-151">Et eksempeloppsett som viser hvordan du rapporterer en produksjonsordre som ferdig til en lokasjon som ikke er nummerskiltkontrollert beskrives også.</span><span class="sxs-lookup"><span data-stu-id="360a7-151">A sample setup showing how to report a production order as finished to a location that isn’t license plate–controlled is also described.</span></span>

## <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="360a7-152">Definere en lagerarbeidspolicy</span><span class="sxs-lookup"><span data-stu-id="360a7-152">Set up a warehouse work policy</span></span>
<span data-ttu-id="360a7-153">Lagerprosesser inkluderer ikke alltid lagerarbeid.</span><span class="sxs-lookup"><span data-stu-id="360a7-153">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="360a7-154">Ved å definere en arbeidspolicy, kan du hindre oppretting av arbeid for råvareplukking og plassering av ferdige varer for et sett med produkter på bestemte lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="360a7-154">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="360a7-155">Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="360a7-155">The USMF demo data company was used to create this procedure.</span></span> 

<span data-ttu-id="360a7-156">TRINN (21)</span><span class="sxs-lookup"><span data-stu-id="360a7-156">STEPS (21)</span></span>

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| <span data-ttu-id="360a7-157">1</span><span class="sxs-lookup"><span data-stu-id="360a7-157">1.</span></span>  | <span data-ttu-id="360a7-158">Gå til Lagerstyring &gt; Oppsett &gt; Arbeid &gt; Arbeidspolicyer.</span><span class="sxs-lookup"><span data-stu-id="360a7-158">Go to Warehouse management &gt; Setup &gt; Work &gt; Work policies.</span></span>        |
| <span data-ttu-id="360a7-159">2</span><span class="sxs-lookup"><span data-stu-id="360a7-159">2.</span></span>  | <span data-ttu-id="360a7-160">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="360a7-160">Click New.</span></span>                                                                 |
| <span data-ttu-id="360a7-161">3</span><span class="sxs-lookup"><span data-stu-id="360a7-161">3.</span></span>  | <span data-ttu-id="360a7-162">Skriv inn 'Ingen ferdigvarearbeid' i navnefeltet for arbeidspolicyen.</span><span class="sxs-lookup"><span data-stu-id="360a7-162">In the Work policy name field, type 'No put-away work'.</span></span>                    |
| <span data-ttu-id="360a7-163">4</span><span class="sxs-lookup"><span data-stu-id="360a7-163">4.</span></span>  | <span data-ttu-id="360a7-164">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="360a7-164">Click Save.</span></span>                                                                |
| <span data-ttu-id="360a7-165">5</span><span class="sxs-lookup"><span data-stu-id="360a7-165">5.</span></span>  | <span data-ttu-id="360a7-166">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="360a7-166">Click Add.</span></span>                                                                 |
| <span data-ttu-id="360a7-167">6</span><span class="sxs-lookup"><span data-stu-id="360a7-167">6.</span></span>  | <span data-ttu-id="360a7-168">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="360a7-168">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="360a7-169">7</span><span class="sxs-lookup"><span data-stu-id="360a7-169">7.</span></span>  | <span data-ttu-id="360a7-170">Velg Plasser ferdigvarer i feltet for Arbeidsordretype.</span><span class="sxs-lookup"><span data-stu-id="360a7-170">In the Work order type field, select 'Finished goods put away'.</span></span>            |
| <span data-ttu-id="360a7-171">8</span><span class="sxs-lookup"><span data-stu-id="360a7-171">8.</span></span>  | <span data-ttu-id="360a7-172">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="360a7-172">Click Add.</span></span>                                                                 |
| <span data-ttu-id="360a7-173">9</span><span class="sxs-lookup"><span data-stu-id="360a7-173">9.</span></span>  | <span data-ttu-id="360a7-174">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="360a7-174">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="360a7-175">10.</span><span class="sxs-lookup"><span data-stu-id="360a7-175">10.</span></span> | <span data-ttu-id="360a7-176">Velg Plasser koprodukt og biprodukt i feltet Arbeidsordretype.</span><span class="sxs-lookup"><span data-stu-id="360a7-176">In the Work order type field, select 'Co-product and by-product put away'.</span></span> |
| <span data-ttu-id="360a7-177">11.</span><span class="sxs-lookup"><span data-stu-id="360a7-177">11.</span></span> | <span data-ttu-id="360a7-178">Vis delen Lagerlokasjoner.</span><span class="sxs-lookup"><span data-stu-id="360a7-178">Expand the Inventory locations section.</span></span>                                    |
| <span data-ttu-id="360a7-179">12.</span><span class="sxs-lookup"><span data-stu-id="360a7-179">12.</span></span> | <span data-ttu-id="360a7-180">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="360a7-180">Click Add.</span></span>                                                                 |
| <span data-ttu-id="360a7-181">13</span><span class="sxs-lookup"><span data-stu-id="360a7-181">13.</span></span> | <span data-ttu-id="360a7-182">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="360a7-182">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="360a7-183">14.</span><span class="sxs-lookup"><span data-stu-id="360a7-183">14.</span></span> | <span data-ttu-id="360a7-184">Angi 51 i Lager-listen.</span><span class="sxs-lookup"><span data-stu-id="360a7-184">In the Warehouse list, enter '51'.</span></span>                                         |
| <span data-ttu-id="360a7-185">15.</span><span class="sxs-lookup"><span data-stu-id="360a7-185">15.</span></span> | <span data-ttu-id="360a7-186">Velg 001 i feltet Lokasjon.</span><span class="sxs-lookup"><span data-stu-id="360a7-186">In the Location field, enter or select '001'.</span></span>                              |
| <span data-ttu-id="360a7-187">16.</span><span class="sxs-lookup"><span data-stu-id="360a7-187">16.</span></span> | <span data-ttu-id="360a7-188">Utvid seksjonen Produkter.</span><span class="sxs-lookup"><span data-stu-id="360a7-188">Expand the Products section.</span></span>                                               |
| <span data-ttu-id="360a7-189">17.</span><span class="sxs-lookup"><span data-stu-id="360a7-189">17.</span></span> | <span data-ttu-id="360a7-190">Velg Valgt i feltet Produktvalg.</span><span class="sxs-lookup"><span data-stu-id="360a7-190">In the Product selection field, select 'Selected'.</span></span>                         |
| <span data-ttu-id="360a7-191">18.</span><span class="sxs-lookup"><span data-stu-id="360a7-191">18.</span></span> | <span data-ttu-id="360a7-192">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="360a7-192">Click Add.</span></span>                                                                 |
| <span data-ttu-id="360a7-193">19.</span><span class="sxs-lookup"><span data-stu-id="360a7-193">19.</span></span> | <span data-ttu-id="360a7-194">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="360a7-194">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="360a7-195">20.</span><span class="sxs-lookup"><span data-stu-id="360a7-195">20.</span></span> | <span data-ttu-id="360a7-196">Angi eller velg L0101 i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="360a7-196">In the Item number field, enter or select 'L0101'.</span></span>                         |
| <span data-ttu-id="360a7-197">21.</span><span class="sxs-lookup"><span data-stu-id="360a7-197">21.</span></span> | <span data-ttu-id="360a7-198">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="360a7-198">Click Save.</span></span>                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="360a7-199">Rapportere en produksjonsordre som ferdig til en lokasjon som ikke er nummerskiltkontrollert</span><span class="sxs-lookup"><span data-stu-id="360a7-199">Report a production order as finished to a location that isn’t license plate–controlled</span></span>
<span data-ttu-id="360a7-200">Denne fremgangsmåten viser et eksempel på rapportering som ferdig til en lokasjon som ikke er nummerskiltkontrollert.</span><span class="sxs-lookup"><span data-stu-id="360a7-200">This procedure shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="360a7-201">En gjeldende arbeidspolicy er en forutsetning for denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="360a7-201">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="360a7-202">Den tidligere fremgangsmåten viste oppsettet av arbeidspolicyen.</span><span class="sxs-lookup"><span data-stu-id="360a7-202">The previous procedure shows the setup of the work policy.</span></span> 

<span data-ttu-id="360a7-203">TRINN (25)</span><span class="sxs-lookup"><span data-stu-id="360a7-203">STEPS (25)</span></span>

<table>
<tbody>
<tr>
<td colspan="3"><span data-ttu-id="360a7-204"><strong>Underoppgave: Definere en utleveringslokasjon.</strong></span><span class="sxs-lookup"><span data-stu-id="360a7-204"><strong>Sub-task: Set up an output location.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="360a7-205">Gå til Organisasjonsstyring &gt; Ressurser &gt; Ressursgrupper.</span><span class="sxs-lookup"><span data-stu-id="360a7-205">Go to Organization administration &gt; Resources &gt; Resource groups.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="360a7-206">Velg ressursgruppe &#39;5102&#39; i listen.</span><span class="sxs-lookup"><span data-stu-id="360a7-206">In the list, select resource group &#39;5102&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="360a7-207">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="360a7-207">Click Edit.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="360a7-208">Angi &#39;51&#39; i feltet Utleveringslager.</span><span class="sxs-lookup"><span data-stu-id="360a7-208">In the Output warehouse field, enter &#39;51&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="360a7-209">Angi &#39;001&#39; i feltet Utleveringslokasjon.</span><span class="sxs-lookup"><span data-stu-id="360a7-209">In the Output location field, enter &#39;001&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="360a7-210">Lokasjonen 001 er ikke en nummerskiltkontrollert lokasjon.</span><span class="sxs-lookup"><span data-stu-id="360a7-210">Location 001 isn&#39;t a license plate–controlled location.</span></span> <span data-ttu-id="360a7-211">Du kan definere en utleveringslokasjon uten nummerskilt hvis det finnes en gjeldende arbeidspolicy for lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="360a7-211">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span></td>
</tr>
<tr>
<td colspan="3"><span data-ttu-id="360a7-212"><strong>Underoppgave: Opprette en produksjonsordre og rapportere den som avsluttet.</strong></span><span class="sxs-lookup"><span data-stu-id="360a7-212"><strong>Sub-task: Create a production order and report it as finished.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="360a7-213">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="360a7-213">Close the page.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="360a7-214">Gå til Produksjonskontroll &gt; Produksjonsordrer &gt; Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="360a7-214">Go to Production control &gt; Production orders &gt; All production orders.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="360a7-215">Klikk Ny produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="360a7-215">Click New production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="360a7-216">Angi &#39;L0101&#39; i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="360a7-216">In the Item number field, enter &#39;L0101&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="360a7-217">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="360a7-217">Click Create.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="360a7-218">Klikk Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="360a7-218">On the Action Pane, click Production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td><span data-ttu-id="360a7-219">Klikk Estimer.</span><span class="sxs-lookup"><span data-stu-id="360a7-219">Click Estimate.</span></span></td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td><span data-ttu-id="360a7-220">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="360a7-220">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td><span data-ttu-id="360a7-221">Klikk Start.</span><span class="sxs-lookup"><span data-stu-id="360a7-221">Click Start.</span></span></td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td><span data-ttu-id="360a7-222">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="360a7-222">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td><span data-ttu-id="360a7-223">Velg &#39;Aldri&#39; i feltet Automatisk stykklisteforbruk.</span><span class="sxs-lookup"><span data-stu-id="360a7-223">In the Automatic BOM consumption field, select &#39;Never&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td><span data-ttu-id="360a7-224">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="360a7-224">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td><span data-ttu-id="360a7-225">Klikk Rapporter som fullført.</span><span class="sxs-lookup"><span data-stu-id="360a7-225">Click Report as finished.</span></span></td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td><span data-ttu-id="360a7-226">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="360a7-226">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td><span data-ttu-id="360a7-227">Velg Ja i feltet Godtar feil.</span><span class="sxs-lookup"><span data-stu-id="360a7-227">Select Yes in the Accept error field.</span></span></td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td><span data-ttu-id="360a7-228">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="360a7-228">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td><span data-ttu-id="360a7-229">Klikk Lager i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="360a7-229">On the Action Pane, click Warehouse.</span></span></td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td><span data-ttu-id="360a7-230">Klikk Arbeidsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="360a7-230">Click Work details.</span></span></td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td><span data-ttu-id="360a7-231">Når produksjonsordren ble rapportert som fullført, ble det ikke generert arbeid for plassering.</span><span class="sxs-lookup"><span data-stu-id="360a7-231">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="360a7-232">Dette skjer fordi en arbeidspolicy er definert som hindrer at arbeidet blir generert når produktet L0101 rapporteres som ferdig til lokasjon 001.</span><span class="sxs-lookup"><span data-stu-id="360a7-232">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span></td>
</tr>
</tbody>
</table>




