---
title: Prosjektkontrakter
description: "Denne artikkelen beskriver og gir eksempler på prosjektkontrakter som du kan opprette for forskjellige typer prosjekter og finansieringskilder, og hvordan du kan behandle kontrakter og fakturere prosjektkunder i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0d7d3b64b0d6a662246074b12e3a3fe105dfae47
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="project-contracts"></a><span data-ttu-id="a4bcb-103">Prosjektkontrakter</span><span class="sxs-lookup"><span data-stu-id="a4bcb-103">Project contracts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a4bcb-104">Denne artikkelen beskriver og gir eksempler på prosjektkontrakter som du kan opprette for forskjellige typer prosjekter og finansieringskilder, og hvordan du kan behandle kontrakter og fakturere prosjektkunder i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-104">This article describes and provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<span data-ttu-id="a4bcb-105">Prosjekttypen du oppretter for en prosjektkontrakt, fastsetter metoden som brukes til å fakturere prosjektkunder.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="a4bcb-106">Du kan endre en prosjektkontrakt og det tilknyttede prosjektet, men du kan ikke endre prosjekttypen.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="a4bcb-107">Ved å bruke en prosjektkontrakt kan du fakturere ett eller flere prosjekter samtidig.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="a4bcb-108">Prosjektkontrakten bidrar også til å sikre en enhetlig faktureringsprosedyre på hvert underprosjekt i en prosjektstruktur.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="a4bcb-109">Hvert prosjekt som faktureres, må være tilknyttet en prosjektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="a4bcb-110">Innstillingene for en prosjektkontrakt gjelder alle prosjekter og underprosjekter som er tilknyttet prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="a4bcb-111">En prosjektkontrakt kan angi en eller flere kilder for finansiering.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="a4bcb-112">Derfor kan du dele fakturering mellom flere kapitalinnskytere, definere finansieringsgrenser slik at finansieringskilder ikke faktureres mer enn et bestemt beløp, og konfigurere finansieringsregler for belastning av utgifter.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="a4bcb-113">Finansiering for prosjektkontrakter</span><span class="sxs-lookup"><span data-stu-id="a4bcb-113">Funding for project contracts</span></span>
<span data-ttu-id="a4bcb-114">Noen prosjektkontrakter angir at flere parter deler ansvaret for finansiering av prosjektkostnadene.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="a4bcb-115">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="a4bcb-115">Here are some examples:</span></span>

-   <span data-ttu-id="a4bcb-116">En stor kunde som har flere avdelinger, ber om at finansiering for et prosjekt deles opp etter avdeling.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="a4bcb-117">Firmaet ditt deler kostnadene for et stort prosjekt med en ekstern organisasjon.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="a4bcb-118">Et veiprosjekt er delfinansiert av to kommuner.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="a4bcb-119">Et broprosjekt finansieres av offentlige tilskudd og et privat selskap.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="a4bcb-120">I Finance and Operations kan du dele faktureringen for en enkelt transaksjon eller et helt prosjekt blant flere kunder, tilskudd eller organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-120">In Finance and Operations, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="a4bcb-121">I prosjekter som har flere kapitalinnskytere, kalles alle parter som bidrar til finansieringen av et avansert finansieringsprosjekt, finansieringskilder.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="a4bcb-122">Når en kunde, en organisasjon eller et tilskudd er definert som en finansieringskilde, kan den/det tilordnes til én eller flere finansieringsregler.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="a4bcb-123">Finansieringsregler inneholder kriteriene som bestemmer hvordan tillegg tilordnes de forskjellige finansieringskildene for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="a4bcb-124">Fordi lagerførte varer, blant annet de som vises på innkjøpsrekvisisjoner og bestillinger, ikke kan deles, kan ikke kostnadsbeløpet deles mellom flere finansieringskilder ved distribusjon.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="a4bcb-125">Finansieringskildeverdien forblir derfor 0 (null) helt til lageravgangen er postert.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="a4bcb-126">Når lageravgangen er postert, fordeles kostnadsbeløpet i henhold til reglene for kontodistribusjon for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="a4bcb-127">Her er noen fremgangsmåter du kan bruke for å gjøre det enklere å dele faktureringen mellom flere finansieringskilder:</span><span class="sxs-lookup"><span data-stu-id="a4bcb-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="a4bcb-128">Angi at alle transaksjoner som er angitt for et prosjekt, bruker den samme salgsvalutaen som prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="a4bcb-129">Sett opp finansieringsgrenser slik at en finansieringskilde ikke faktureres mer enn et angitt beløp mot et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="a4bcb-130">Konfigurer finansieringsregler og finansieringsgrenser for hver arbeider, vare, kategori, kategorigruppe og transaksjonstype (eller for alle transaksjonstyper).</span><span class="sxs-lookup"><span data-stu-id="a4bcb-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="a4bcb-131">Velg valgfrie start- og sluttdatoer for å definere perioden når hver finansieringsregel er gyldig.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="a4bcb-132">Angi prosentdelen som hver finansieringskilde er ansvarlig for.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="a4bcb-133">Angi hvilken finansieringskilde som er ansvarlig for avrundingsdifferanser som skyldes finansieringstildelingsberegninger.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="a4bcb-134">Definer regler som bestemmer hvordan prosjektkostnader faktureres til eksterne kunder og belastes interne organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="a4bcb-135">Registrer transaksjoner på finansieringskonto på vent til ytterligere finansiering kan anskaffes, eller til du beslutter å bære kostnadene internt.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="a4bcb-136">For å fastsette hvilken avgiftsgruppe som skal knyttes til en transaksjon, søkes det etter en mva-gruppetilordning i prosjektet.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="a4bcb-137">Hvis ingen mva-gruppetilordning er gjort på prosjektnivå, søkes det i prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="a4bcb-138">Eksempel: Flere finansieringskilder (enkel)</span><span class="sxs-lookup"><span data-stu-id="a4bcb-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="a4bcb-139">Tabellen nedenfor gir scenarier for behandling av finansieringskildetilordning mellom flere finansieringskilder.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="a4bcb-140">Disse scenariene er basert på følgende forutsetninger:</span><span class="sxs-lookup"><span data-stu-id="a4bcb-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="a4bcb-141">Prioritetsinnstillingene tas med i tildelingen av midler før andre finansieringsregelkriterier brukes.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="a4bcb-142">Ingen datointervall er angitt for å definere perioden d når finansieringsregelen gjelder.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4bcb-143"><strong>Scenario</strong></span><span class="sxs-lookup"><span data-stu-id="a4bcb-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="a4bcb-144"><strong>Finansieringskilde </strong></span><span class="sxs-lookup"><span data-stu-id="a4bcb-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="a4bcb-145"><strong>Tildelingsprosent </strong></span><span class="sxs-lookup"><span data-stu-id="a4bcb-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="a4bcb-146"><strong>Tildelingsprioritet </strong></span><span class="sxs-lookup"><span data-stu-id="a4bcb-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4bcb-147">Du vil tildele kostnader til én finansieringskilde før midlene er oppbrukt, tildele kostnader til en finansieringskilde nummer to før midlene er oppbrukt, og til slutt tildele de gjenstående kostnadene til en tredje finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="a4bcb-148">Finansierinskilde 1</span><span class="sxs-lookup"><span data-stu-id="a4bcb-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="a4bcb-149">Finansieringskilde 2</span><span class="sxs-lookup"><span data-stu-id="a4bcb-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="a4bcb-150">Finansieringskilde 3</span><span class="sxs-lookup"><span data-stu-id="a4bcb-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a4bcb-151">100 %</span><span class="sxs-lookup"><span data-stu-id="a4bcb-151">100%</span></span></li>
<li><span data-ttu-id="a4bcb-152">100 %</span><span class="sxs-lookup"><span data-stu-id="a4bcb-152">100%</span></span></li>
<li><span data-ttu-id="a4bcb-153">100 %</span><span class="sxs-lookup"><span data-stu-id="a4bcb-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a4bcb-154">1</span><span class="sxs-lookup"><span data-stu-id="a4bcb-154">1</span></span></li>
<li><span data-ttu-id="a4bcb-155">2</span><span class="sxs-lookup"><span data-stu-id="a4bcb-155">2</span></span></li>
<li><span data-ttu-id="a4bcb-156">3</span><span class="sxs-lookup"><span data-stu-id="a4bcb-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4bcb-157">Du ønsker å tildele 75 prosent av kostnadene til én finansieringskilde og 25 prosent til en annen finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="a4bcb-158">Når disse finansieringskildene er oppbrukt, vil du betale de gjenstående kostnadene fra en tredje finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="a4bcb-159">Finansierinskilde 1</span><span class="sxs-lookup"><span data-stu-id="a4bcb-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="a4bcb-160">Finansieringskilde 2</span><span class="sxs-lookup"><span data-stu-id="a4bcb-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="a4bcb-161">Finansieringskilde 3</span><span class="sxs-lookup"><span data-stu-id="a4bcb-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a4bcb-162">75 %</span><span class="sxs-lookup"><span data-stu-id="a4bcb-162">75%</span></span></li>
<li><span data-ttu-id="a4bcb-163">25 %</span><span class="sxs-lookup"><span data-stu-id="a4bcb-163">25%</span></span></li>
<li><span data-ttu-id="a4bcb-164">100 %</span><span class="sxs-lookup"><span data-stu-id="a4bcb-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a4bcb-165">1</span><span class="sxs-lookup"><span data-stu-id="a4bcb-165">1</span></span></li>
<li><span data-ttu-id="a4bcb-166">1</span><span class="sxs-lookup"><span data-stu-id="a4bcb-166">1</span></span></li>
<li><span data-ttu-id="a4bcb-167">2</span><span class="sxs-lookup"><span data-stu-id="a4bcb-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4bcb-168">Du ønsker å tildele 75 prosent av kostnadene til én finansieringskilde og 25 prosent til en annen finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="a4bcb-169">Når disse finansieringskildene er oppbrukt, ønsker du å dele de gjenstående kostnadene mellom en tredje finansieringskilde og en fjerde finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="a4bcb-170">Finansierinskilde 1</span><span class="sxs-lookup"><span data-stu-id="a4bcb-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="a4bcb-171">Finansieringskilde 2</span><span class="sxs-lookup"><span data-stu-id="a4bcb-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="a4bcb-172">Finansieringskilde 3</span><span class="sxs-lookup"><span data-stu-id="a4bcb-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="a4bcb-173">Finansieringskilde 4</span><span class="sxs-lookup"><span data-stu-id="a4bcb-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a4bcb-174">75 %</span><span class="sxs-lookup"><span data-stu-id="a4bcb-174">75%</span></span></li>
<li><span data-ttu-id="a4bcb-175">25 %</span><span class="sxs-lookup"><span data-stu-id="a4bcb-175">25%</span></span></li>
<li><span data-ttu-id="a4bcb-176">50 %</span><span class="sxs-lookup"><span data-stu-id="a4bcb-176">50%</span></span></li>
<li><span data-ttu-id="a4bcb-177">50 %</span><span class="sxs-lookup"><span data-stu-id="a4bcb-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a4bcb-178">1</span><span class="sxs-lookup"><span data-stu-id="a4bcb-178">1</span></span></li>
<li><span data-ttu-id="a4bcb-179">1</span><span class="sxs-lookup"><span data-stu-id="a4bcb-179">1</span></span></li>
<li><span data-ttu-id="a4bcb-180">2</span><span class="sxs-lookup"><span data-stu-id="a4bcb-180">2</span></span></li>
<li><span data-ttu-id="a4bcb-181">2</span><span class="sxs-lookup"><span data-stu-id="a4bcb-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4bcb-182">Du ønsker å tildele de første 25 prosentene av kostnadene til én finansieringskilde og resten til en finansieringskilde nummer to.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="a4bcb-183">Finansierinskilde 1</span><span class="sxs-lookup"><span data-stu-id="a4bcb-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="a4bcb-184">Finansieringskilde 2</span><span class="sxs-lookup"><span data-stu-id="a4bcb-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a4bcb-185">25 %</span><span class="sxs-lookup"><span data-stu-id="a4bcb-185">25%</span></span></li>
<li><span data-ttu-id="a4bcb-186">100 %</span><span class="sxs-lookup"><span data-stu-id="a4bcb-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a4bcb-187">1</span><span class="sxs-lookup"><span data-stu-id="a4bcb-187">1</span></span></li>
<li><span data-ttu-id="a4bcb-188">2</span><span class="sxs-lookup"><span data-stu-id="a4bcb-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="a4bcb-189">Eksempel: Flere finansieringskilder (kompleks)</span><span class="sxs-lookup"><span data-stu-id="a4bcb-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="a4bcb-190">Du har tre finansieringskilder som du vil bruke i følgende rekkefølge:</span><span class="sxs-lookup"><span data-stu-id="a4bcb-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="a4bcb-191">Bruk finansieringskilde 2 og finansieringskilde 3 likt helt til finansieringskilde 2 er oppbrukt.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="a4bcb-192">Fortsett å bruke finansieringskilde 3 helt til den er oppbrukt.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="a4bcb-193">Bruk finansieringskilde 1 når finansieringskilde 3 er oppbrukt.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="a4bcb-194">For å nå dette målet må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="a4bcb-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="a4bcb-195">Definere finansieringsgrenser for finansieringskilde 2 og finansieringskilde 3 for de respektive beløpene.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="a4bcb-196">Opprette følgende finansieringsregler:</span><span class="sxs-lookup"><span data-stu-id="a4bcb-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="a4bcb-197">Regel 1 (prioritet 1): Tildele 50 prosent av transaksjoner til finansieringskilde 2 og 50 prosent til finansieringskilde 3.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="a4bcb-198">Regel 2 (prioritet 2): Fordele 100 prosent av transaksjoner til finansieringskilde 3.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="a4bcb-199">Regel 3 (prioritet 3): Fordele 100 prosent av transaksjoner til finansieringskilde 1.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="a4bcb-200">Dette oppsettet fungerer fordi transaksjoner er kontrollert mot reglene og begrensningene for å finne ut om noen av dem gjelder for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="a4bcb-201">Hvis ingen bestemte regler eller begrensninger gjelder for transaksjonen, gjelder Alle transaksjoner-regelen.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="a4bcb-202">Alle transaksjoner-regelen samsvarer med alle transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="a4bcb-203">Hvis det finnes en regel som samsvarer med en transaksjon, brukes prosenten som er tildelt regelen, først, men bare etter at treffene er kontrollert mot eventuelle begrensninger som er angitt.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="a4bcb-204">Hvis en grense er nådd og en finansieringskildes midler er oppbrukt, ignoreres finansieringsregelen som er tilknyttet finansieringsgrensen, og det søkes automatisk etter den neste regelen som gjelder.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="a4bcb-205">I noen tilfeller kan du fordele bare en del av en transaksjon under en regel.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="a4bcb-206">Dette kan skje fordi en grense nås når transaksjonen er tildelt.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="a4bcb-207">I så fall tildeles bare et bestemt beløp i henhold til denne regelen, for eksempel 50 prosent til hver finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="a4bcb-208">Dette er tilfelle i regelen 1, som er beskrevet tidligere i denne delen.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="a4bcb-209">Resten tildeles i henhold til den neste regelen i sekvensen.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="a4bcb-210">Tabellen nedenfor illustrerer dette scenarioet mer detaljert.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4bcb-211"><strong>Fokus </strong></span><span class="sxs-lookup"><span data-stu-id="a4bcb-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="a4bcb-212"><strong>Detaljer</strong></span><span class="sxs-lookup"><span data-stu-id="a4bcb-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4bcb-213">Finansieringsregler</span><span class="sxs-lookup"><span data-stu-id="a4bcb-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="a4bcb-214">Regel 1 (prioritet 1): Alle transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="a4bcb-215">Tildel finansieringskilde 2 med 50 % og finansieringskilde 3 med 50 %.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="a4bcb-216">Regel 2 (prioritet 2): Alle transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="a4bcb-217">Tildel finansieringskilde 3 med 100 %.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="a4bcb-218">Regel 3 (prioritet 2): Alle transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="a4bcb-219">Tildel finansieringskilde 1 med 100 %.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4bcb-220">Finansieringsgrenser</span><span class="sxs-lookup"><span data-stu-id="a4bcb-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="a4bcb-221">Finansieringskilde 1-grense = 10 000,00</span><span class="sxs-lookup"><span data-stu-id="a4bcb-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="a4bcb-222">Finansieringskilde 2-grense = 500,00</span><span class="sxs-lookup"><span data-stu-id="a4bcb-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="a4bcb-223">Finansieringskilde 3-grense = 750,00</span><span class="sxs-lookup"><span data-stu-id="a4bcb-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4bcb-224">Transaksjon 1</span><span class="sxs-lookup"><span data-stu-id="a4bcb-224">Transaction 1</span></span></td>
<td><span data-ttu-id="a4bcb-225"><strong>Transaksjonsbeløp:</strong> 100,00<strong>Finansiering:</strong> Transaksjonen betales bare i henhold til regel 1, fordi transaksjonen betales i sin helhet når regel 1 er brukt.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="a4bcb-226">Transaksjonen finansieres likt mellom finansieringskilde 2 og finansieringskilde 3.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="a4bcb-227">Finansieringskilde 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="a4bcb-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="a4bcb-228">Finansieringskilde 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="a4bcb-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4bcb-229">Transaksjon 2</span><span class="sxs-lookup"><span data-stu-id="a4bcb-229">Transaction 2</span></span></td>
<td><span data-ttu-id="a4bcb-230"><strong>Transaksjonsbeløp:</strong> 5 000,00<strong>Finansiering:</strong> Transaksjonen betales i henhold til alle tre regler.<strong>Regel 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="a4bcb-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.<strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="a4bcb-231">Finansieringskilde 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="a4bcb-231">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="a4bcb-232">Finansieringskilde 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="a4bcb-232">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="a4bcb-233">
<strong>Regel 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="a4bcb-233">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="a4bcb-234">Finansieringskilde 3: 250,00 (= 750,00 - 50,00 - 450,00)</span><span class="sxs-lookup"><span data-stu-id="a4bcb-234">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="a4bcb-235">
<strong>Regel 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="a4bcb-235">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="a4bcb-236">Finansieringskilde 1: 3 850,00 (= 5 000,00 - 450,00 - 450,00 - 250,00)</span><span class="sxs-lookup"><span data-stu-id="a4bcb-236">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4bcb-237">Totale midler som fordeles for hver finansieringskilde</span><span class="sxs-lookup"><span data-stu-id="a4bcb-237">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="a4bcb-238">Finansieringskilde 1: 3 850,00</span><span class="sxs-lookup"><span data-stu-id="a4bcb-238">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="a4bcb-239">Finansieringskilde 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="a4bcb-239">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="a4bcb-240">Finansieringskilde 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="a4bcb-240">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="a4bcb-241">Faktureringsregler</span><span class="sxs-lookup"><span data-stu-id="a4bcb-241">Billing rules</span></span>
<span data-ttu-id="a4bcb-242">Når du forhandler med en kunde om en prosjektkontrakt, definerer du hvordan og når kan du fakturere kunden for arbeid på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-242">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="a4bcb-243">Når du har definert prosjektkontrakten og prosjektet, kan du definere faktureringsregler for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-243">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="a4bcb-244">Faktureringsregler er basert på prosjektvilkårene som er angitt i prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-244">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="a4bcb-245">Faktureringsreglene du kan opprette avhenger av betingelsene i prosjektkontrakten og av prosjekttypen, for eksempel Etter regning eller Fastpris som du knytter til faktureringsregelen.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-245">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="a4bcb-246">Du kan opprette mer enn n faktureringsregel for en prosjektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-246">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="a4bcb-247">Du kan også tilordne en faktureringsregel til flere prosjekter som er knyttet til samme prosjektkontrakt og har lignende faktureringsvilkår.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-247">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="a4bcb-248">Du kan definere følgende typer faktureringsregler:</span><span class="sxs-lookup"><span data-stu-id="a4bcb-248">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="a4bcb-249">**Leveringsenhet** – Fakturer en kunde når du fullfører en leveringsenhet.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-249">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="a4bcb-250">Du definerer leveringsenhetene i kontrakten.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-250">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="a4bcb-251">**Fremdrift** – Fakturer en kunde når du fullfører en bestemt prosentandel av prosjektet.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-251">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="a4bcb-252">Du kan definere en faktureringsregel for å beregne en prosentandel av fullført arbeid automatisk, eller du kan manuelt beregne prosentandelen av fullført arbeid og beløpet som skal faktureres kunden.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-252">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="a4bcb-253">**Milepæl** – Fakturer en kunde for hele beløpet for en prosjektmilepæl når milepælen er nådd.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-253">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="a4bcb-254">**Gebyr** – Fakturer en kunde for tjenestene dine i tillegg til et behandlingsgebyr, som vanligvis er en prosentandel av tjenestenes kostnad.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-254">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="a4bcb-255">**Tid og materialer** – Fakturer en kunde for verdien av tid og materialer som brukes på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-255">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="a4bcb-256">For alle typer faktureringsregler kan du angi en bevaringsprosent som trekkes fra kundefakturaer helt til et prosjekt når et avtalt stadium.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-256">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="a4bcb-257">Prosenten for betalingsbevaring er angitt i prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-257">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="a4bcb-258">Beløpet beregnes basert på, og trekkes fra, den totale verdien av linjene i en kundefaktura.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-258">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="a4bcb-259">For **Tid og materialer**- og **Fremdrift**-faktureringsregler kan du tilordne belastbare kategorier.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-259">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="a4bcb-260">Belastbare kategorier angir transaksjonene som skal inkluderes i kundefakturaer.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-260">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="a4bcb-261">Når du er klar til å fakturere en kunden, beregnes beløpet som skal faktureres for prosjektet, basert på faktureringsreglene, og det genereres et prosjektfakturaforslag.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-261">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="a4bcb-262">Delene nedenfor innholder eksempler som viser hvordan du definerer og administrerer en faktureringsregler for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-262">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="a4bcb-263">Eksempel: Opprett en fakturaregel som er basert på antall leverte enheter</span><span class="sxs-lookup"><span data-stu-id="a4bcb-263">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="a4bcb-264">Organisasjonen din inngår en avtale om å levere totalt fem opplæringsøkter til en kundes ansatte til en kostnad på 10 000 per opplæringsøkt.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-264">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="a4bcb-265">Du fakturerer kunden etter hver opplæringsøkt.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-265">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="a4bcb-266">Når du definerer faktureringsregler for kontrakten, bruker du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a4bcb-266">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="a4bcb-267">Leveringsenheten er én opplæringsøkt.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-267">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="a4bcb-268">Enhetsprisen er 10 000 per opplæringsøkt.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-268">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="a4bcb-269">Totalt antall enheter er fem opplæringsøkter.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-269">The total number of units is five training sessions.</span></span>

<span data-ttu-id="a4bcb-270">Når du har fullført én opplæringsøkt, kan du opprette en faktura på 10 000 for den første enheten som ble levert, og sende fakturaen til kunden.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-270">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="a4bcb-271">Eksempel: Opprett en fakturaregel som er basert på en angitt fullføringsprosent av prosjektet (beregnes manuelt)</span><span class="sxs-lookup"><span data-stu-id="a4bcb-271">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="a4bcb-272">Organisasjonen din er et programvarekonsulentfirma som inngår en avtale med en kunde om å utvikle en del av et produkt som kunden utvikler.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-272">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="a4bcb-273">Organisasjonen godtar å levere programvarekode over en periode på seks måneder.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-273">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="a4bcb-274">Kunden godtar å betale organisasjonen totalt 100 000 for arbeidet.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-274">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="a4bcb-275">Du oppretter en faktureringsregel for å fakturere kunden basert på prosenten av fullført arbeid på prosjektet, som angitt i kontrakten.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-275">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="a4bcb-276">På slutten av den første måneden møter du kunden for å finne ut hvor stor prosentandel av arbeidet er fullført.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-276">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="a4bcb-277">Når du og kunden går gjennom prosjektet, fastsetter dere at prosjektet er 15 prosent fullført.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-277">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="a4bcb-278">Du oppretter en faktura på 15 000 (15 prosent av 100 000) og sender den til kunden.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-278">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="a4bcb-279">Eksempel: Opprett en fakturaregel som er basert på en angitt fullføringsprosent av prosjektet (beregnes automatisk)</span><span class="sxs-lookup"><span data-stu-id="a4bcb-279">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="a4bcb-280">Organisasjonen din, et programvareutviklingsfirma, avtaler å utvikle en lønnsregnskapspakke for en kunde for 30 000.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-280">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="a4bcb-281">Kunden godtar å betale organisasjonen på grunnlag av prosenten av fullført arbeid.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-281">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="a4bcb-282">Du beregner prosjektkostnadene til 20 000.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-282">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="a4bcb-283">Prosjektkontrakten angir arbeidskategoriene du bruker i faktureringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-283">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="a4bcb-284">Du definerer faktureringsregler som automatisk beregner fakturabeløpene for arbeidsprosenten som er fullført for hver kategori.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-284">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="a4bcb-285">Du definerer et budsjett for hver kategori:</span><span class="sxs-lookup"><span data-stu-id="a4bcb-285">You set up a budget for each category:</span></span>

-   <span data-ttu-id="a4bcb-286">**Utvikling** – Kostnad på 15 000 og omsetning på 20 000</span><span class="sxs-lookup"><span data-stu-id="a4bcb-286">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="a4bcb-287">**Installasjon** – Kostnad på 5 000 og omsetning på 10 000</span><span class="sxs-lookup"><span data-stu-id="a4bcb-287">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="a4bcb-288">Når du oppretter en kundefaktura for første gang, beregnes fakturabeløpet automatisk basert på følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="a4bcb-288">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="a4bcb-289">Etter en måned sender arbeideren på prosjektet en timeregistrering for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-289">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="a4bcb-290">Kostnaden til arbeiderens timer er 5000 for utvikling og 1000 for installasjon.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-290">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="a4bcb-291">Utviklingsarbeidet er 33 prosent fullført (5 000 i faktiske kostnader / 15 000 i budsjettkostnader), og installasjonsarbeidet er 20 prosent fullført (1 000 i faktiske kostnader / 5 000 i budsjettkostnader).</span><span class="sxs-lookup"><span data-stu-id="a4bcb-291">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="a4bcb-292">Fakturabeløpet på 8 667 beregnes automatisk (33 prosent av 20 000 + 20 prosent av 10 000).</span><span class="sxs-lookup"><span data-stu-id="a4bcb-292">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="a4bcb-293">Du oppretter en faktura på 8 667 og sender den til kunden.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-293">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="a4bcb-294">Eksempel: Opprett en fakturaregel som er basert på avtalte milepæler</span><span class="sxs-lookup"><span data-stu-id="a4bcb-294">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="a4bcb-295">Organisasjonen din er et rådgivningsfirma og avtaler å utføre markedsundersøkelser for et forbrukerprodukt som kunden planlegger å selge.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-295">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="a4bcb-296">Kunden godtar å bruke dine tjenester over en periode på tre måneder med start i mars, og godtar å betale organisasjonen 50 000.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-296">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="a4bcb-297">Prosjektet har tre milepæler:</span><span class="sxs-lookup"><span data-stu-id="a4bcb-297">The project has three milestones:</span></span>

-   <span data-ttu-id="a4bcb-298">Milepæl 1: Samle inn forbrukerdata – 31. mars</span><span class="sxs-lookup"><span data-stu-id="a4bcb-298">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="a4bcb-299">Milepæl 2: Analysere forbrukerdata – 30. april</span><span class="sxs-lookup"><span data-stu-id="a4bcb-299">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="a4bcb-300">Milepæl 3: Presentere et forslag for levedyktighet for produktet – 31. mai</span><span class="sxs-lookup"><span data-stu-id="a4bcb-300">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="a4bcb-301">Kunden godtar å betale organisasjonen 10 000 for den første milepælen, 20 000 for milepæl nummer to og 20 000 for tredje milepæl.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-301">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="a4bcb-302">Når du definerer prosjektkontrakten, godtar du å fakturere kunden basert på milepælen som er fullført.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-302">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="a4bcb-303">Faktureringsregeloppsettet omfatter følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="a4bcb-303">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="a4bcb-304">Definer milepælene i prosjektet.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-304">Define the project milestones.</span></span>
-   <span data-ttu-id="a4bcb-305">Angi beløpet som skal faktureres kunden når hver milepæl er fullført.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-305">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="a4bcb-306">Når den første milepælen fullføres 31. mars, merker du milepælen som fullført, og deretter oppretter du en faktura på 10 000 og sender den til kunden.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-306">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="a4bcb-307">Du kan ikke opprette en faktura for en milepæl før du har merket milepælen som fullført.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-307">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="a4bcb-308">Eksempel: Opprett en faktureringsregel som er basert på tjenester i tillegg til et gebyr for administrasjon</span><span class="sxs-lookup"><span data-stu-id="a4bcb-308">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="a4bcb-309">Organisasjonen din, som er et rådgivningsfirma, avtaler å utføre markedsundersøkelser for å evaluere gjennomføringen av et produkt som kunden, et detaljhandelsfirma, utvikler.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-309">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="a4bcb-310">Vilkårene i avtalen angir at tjenestene skal utføres av de tre beste konsulentene, som skal utføre undersøkelsen på grunnlag av tid og materialer.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-310">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="a4bcb-311">Kunden godtar å betale 100 per time pluss et administrasjonsgebyr på ti prosent for konsultasjonstimene som faktureres til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-311">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="a4bcb-312">Når du definerer prosjektkontrakten, oppretter du en faktureringsregel for å legge til et administrasjonsgebyr på 10 prosent for konsultasjonstimene som prosjektet belastes med.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-312">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="a4bcb-313">Når du oppretter en faktura for kunden, faktureres kunden et administrasjonsgebyr på 10 prosent samt kostnadene for konsultasjonstimene.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-313">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="a4bcb-314">Hvis de tre konsulentene for eksempel arbeidet totalt 200 timer på prosjektet, opprettes en faktura på 22 000 basert på følgende beregning:</span><span class="sxs-lookup"><span data-stu-id="a4bcb-314">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="a4bcb-315">200 timer til 100 per time = 20 000</span><span class="sxs-lookup"><span data-stu-id="a4bcb-315">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="a4bcb-316">10 prosent administrasjonsgebyr = 2000</span><span class="sxs-lookup"><span data-stu-id="a4bcb-316">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="a4bcb-317">Totalt fakturabeløp = 22 000</span><span class="sxs-lookup"><span data-stu-id="a4bcb-317">Total invoice amount = 22,000</span></span>

<span data-ttu-id="a4bcb-318">Hvis gebyrer er avgiftspliktige for en kunde og du velger en mva-gruppe i prosjektkontrakten, registreres mva-gruppen automatisk i en faktureringsregel for gebyrer.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-318">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="a4bcb-319">Eksempel: Opprett en faktureringsregel for verdien av tid og materialer</span><span class="sxs-lookup"><span data-stu-id="a4bcb-319">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="a4bcb-320">Organisasjonen din, som er et programvarekonsulentfirma, avtaler å stille med fem tekniske konsulenter som skal jobbe på et programvareutviklingsprosjekt for en kunde over de neste seks månedene.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-320">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="a4bcb-321">Kunden godtar å betale 150 for hver konsulenttime i tillegg til kostnaden for kontorutstyr.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-321">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="a4bcb-322">Organisasjonen din sender en faktura til kunden på slutten av hver måned.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-322">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="a4bcb-323">Når du definerer prosjektkontrakten, godtar du å fakturere kunden månedlig for tid og materialer på prosjektet.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-323">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="a4bcb-324">Du oppretter en faktueringsregel som inkluderer følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="a4bcb-324">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="a4bcb-325">Kontraktperioden er seks måneder.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-325">The contract period is six months.</span></span>
-   <span data-ttu-id="a4bcb-326">Rådgivningstid beregnes med en sats på 150 per time.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-326">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="a4bcb-327">Kontorutstyr faktureres til kostpris, og totalkostnad for prosjektet kan ikke overskride 10 000.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-327">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="a4bcb-328">Du oppretter en kundefaktura på slutten av hver kalendermåned i løpet av prosjektet.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-328">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="a4bcb-329">I løpet av den første måneden registrerer konsulentene totalt 800 timer på prosjektet.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-329">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="a4bcb-330">Kostnaden for kontorutstyr som belastes prosjektet, er 2000.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-330">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="a4bcb-331">På slutten av måneden kan du derfor opprette en faktura på 122 000, som beregnes til 800 timer til 150 per time, pluss 2 000 for kontorrekvisita.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-331">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>




