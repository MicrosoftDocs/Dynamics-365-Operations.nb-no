---
title: Oversikt over forutsetninger for standardkostnader
description: Dette emnet beskiver de grunnleggende trinnene for bruk av standard kostpris.
author: AndersGirke
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9333bda96ceae378ab74892534db13761038a06c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967364"
---
# <a name="prerequisites-for-standard-costs-overview"></a><span data-ttu-id="86ecb-103">Oversikt over forutsetninger for standardkostnader</span><span class="sxs-lookup"><span data-stu-id="86ecb-103">Prerequisites for standard costs overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86ecb-104">Dette emnet beskiver de grunnleggende trinnene for bruk av standard kostpris.</span><span class="sxs-lookup"><span data-stu-id="86ecb-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="86ecb-105">Fremgangsmåten avhenger av firmaets opererasjoner.</span><span class="sxs-lookup"><span data-stu-id="86ecb-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="86ecb-106">Fremgangsmåten er for eksempel forskjellig for et firmaet uten egenproduksjon, et produksjonsmiljø som ikke bruker ruting og et produksjonsmiljø som bruker ruting.</span><span class="sxs-lookup"><span data-stu-id="86ecb-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="86ecb-107">Følg denne fremgangsmåten for å definere standard kostpris.</span><span class="sxs-lookup"><span data-stu-id="86ecb-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="86ecb-108">**1. Opprett en varemodellgruppe for standard kostpris.**</span><span class="sxs-lookup"><span data-stu-id="86ecb-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="86ecb-109">Bruk **Varemodellgrupper**-siden for å opprette en ny gruppe for standard kostpriser, og tilordne en lagermodell med **standardkost**.</span><span class="sxs-lookup"><span data-stu-id="86ecb-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="86ecb-110">Identifikatoren for varemodellgruppen bør ha mening, for eksempel **Std.kost**.</span><span class="sxs-lookup"><span data-stu-id="86ecb-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="86ecb-111">Merk av for å angi at gruppen skal tillate økonomisk negativt lager, og at det skal postere fysisk lager og økonomisk lager.</span><span class="sxs-lookup"><span data-stu-id="86ecb-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="86ecb-112">Denne standardkostgruppen vil tilordnes til varer.</span><span class="sxs-lookup"><span data-stu-id="86ecb-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="86ecb-113">**2. Definer finanskontoer som er relatert til avvik i standard kostpris.**</span><span class="sxs-lookup"><span data-stu-id="86ecb-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="86ecb-114">Bruk **Kontoplan**-siden for å definere finanskontoer som er relatert til avvik i standard kostpris.</span><span class="sxs-lookup"><span data-stu-id="86ecb-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="86ecb-115">Disse finanskontoene må være definert før de kan tilordnes på **Postering**-siden.</span><span class="sxs-lookup"><span data-stu-id="86ecb-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="86ecb-116">Finanskontoene kan gjenspeile varegrupper og kostgrupper.</span><span class="sxs-lookup"><span data-stu-id="86ecb-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="86ecb-117">**3. Tilordne finanskontoer til vareposteringer som er relatert til avvik i standard kostpris.**</span><span class="sxs-lookup"><span data-stu-id="86ecb-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="86ecb-118">Bruk **Postering**-siden til å tilordne finanskontoer som er relatert til avvik i standard kostpris.</span><span class="sxs-lookup"><span data-stu-id="86ecb-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="86ecb-119">Du kan angi en finanskonto for en variant etter vare (eller varegruppe) og kostgruppe (eller kostgruppetype), eller du kan angi at finanskontoen gjelder for alle varer og kostgrupper.</span><span class="sxs-lookup"><span data-stu-id="86ecb-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="86ecb-120">Disse alternativene tilsvarer kostrelasjoner for tabeller, grupper og alle.</span><span class="sxs-lookup"><span data-stu-id="86ecb-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="86ecb-121">Før du definerer vareposteringsreglene, bruker du siden **Transaksjonskombinasjoner** til å aktivere kostrelasjoner (for tabeller, grupper og alle).</span><span class="sxs-lookup"><span data-stu-id="86ecb-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="86ecb-122">**4. Definer lagerparameterne som er relatert til standard kostpris.**</span><span class="sxs-lookup"><span data-stu-id="86ecb-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="86ecb-123">Bruk fanen **Lagerregnskap** på siden **Oppsett for regnskapspolicyer for beholdning > Parametere** til å definere to kostkontrollparametere som er relatert til standard kostpris.</span><span class="sxs-lookup"><span data-stu-id="86ecb-123">Use the **Inventory accounting** tab on the **Inventory accounting policies setup > Parameters** page to define two cost control parameters that are related to standard costs.</span></span>

    -  <span data-ttu-id="86ecb-124">I **Oppdeling av kostnader**-feltet velger du **Ingen** eller **Underfinans**.</span><span class="sxs-lookup"><span data-stu-id="86ecb-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="86ecb-125">Hvis du velger **Underfinans**, er kostnadsoppdelingen en *aktiv* kostnadsoppdeling.</span><span class="sxs-lookup"><span data-stu-id="86ecb-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="86ecb-126">Aktiv kostnadsoppdeling er kritisk for beregning, opprettholding og visning av kostgruppesegmentering gjennom en produktstruktur på flere nivåer for varer med standard kostpris.</span><span class="sxs-lookup"><span data-stu-id="86ecb-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="86ecb-127">Når kostnadsoppdelingen er aktiv, kan du rapportere og analysere lagerbeholdningen, varer i arbeid (VIA) og kostnader for solgte varer per kostgruppe på ett enkelt nivå, over flere nivåer eller totalt.</span><span class="sxs-lookup"><span data-stu-id="86ecb-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="86ecb-128">Når kostnadsoppdelingen er aktiv, hvis du aktiverer en produsert vares kostnad, lagres kostgruppesegmenteringen i varens kostprispost.</span><span class="sxs-lookup"><span data-stu-id="86ecb-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="86ecb-129">Hvis du velger **Ingen**, vil ikke kostgruppesegmentering bli opprettholdt for standardkostvarer.</span><span class="sxs-lookup"><span data-stu-id="86ecb-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="86ecb-130">Med andre ord blir en produsert vares standardkost beregnet og opprettholdt som et enkelt beløp, uten kostgruppesegmentering.</span><span class="sxs-lookup"><span data-stu-id="86ecb-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="86ecb-131">Kostbidragene for produserte komponenter vil bli aggregert til ett enkeltbeløp.</span><span class="sxs-lookup"><span data-stu-id="86ecb-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="86ecb-132">I **Avvik for standard**-feltet velger du **Summert** eller **Per kostgruppe**.</span><span class="sxs-lookup"><span data-stu-id="86ecb-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="86ecb-133">Hvis du velger **Per kostgruppe**, kan du identifisere avvik i innkjøpspris og produksjonsavvik etter kostgruppe.</span><span class="sxs-lookup"><span data-stu-id="86ecb-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="86ecb-134">Du kan også identifisere de fire typene produksjonsavvik: avvik i partistørrelse, antall, pris og erstatning.</span><span class="sxs-lookup"><span data-stu-id="86ecb-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="86ecb-135">Hvis du valgte **Summert**, kan du ikke identifisere avvik etter kostgruppe, og du kan ikke identifisere de fire typene produksjonsavvik.</span><span class="sxs-lookup"><span data-stu-id="86ecb-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="86ecb-136">Du kan bare vise en oppsummering av produksjonsavviket.</span><span class="sxs-lookup"><span data-stu-id="86ecb-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="86ecb-137">Policyen om avvik for standard kostpris fungerer uavhengig av policyen for kostnadsoppdeling.</span><span class="sxs-lookup"><span data-stu-id="86ecb-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="86ecb-138">Det vil si at hvis du velger **Ingen** policy for kostnadsoppdeling samt avvik per kostgruppe, vil produksjonsavvik etter kostgruppe fremdeles vil bli fanget opp.</span><span class="sxs-lookup"><span data-stu-id="86ecb-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="86ecb-139">**5. Opprett kostnadsberegningsversjoner for standard kostpris.**</span><span class="sxs-lookup"><span data-stu-id="86ecb-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="86ecb-140">Bruk siden **Oppsett av etterkalkuleringsversjon** til å opprette én eller flere kostnadsberegningsversjoner for standard kostpris.</span><span class="sxs-lookup"><span data-stu-id="86ecb-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="86ecb-141">Hver kostnadsberegningsversjon må være definert med en kostnadsberegningstype for **Standard kostpris** og må tillate innhold som omfatter kostnadsdata.</span><span class="sxs-lookup"><span data-stu-id="86ecb-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="86ecb-142">**6. Klargjør en eksisterende kunde for bruk av standard kostpris.**</span><span class="sxs-lookup"><span data-stu-id="86ecb-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="86ecb-143">Kunder som vil endre sine eksisterende varer til en lagermodell med standard kostpris, må bruke siden **Standard kostnadskonvertering**.</span><span class="sxs-lookup"><span data-stu-id="86ecb-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="86ecb-144">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="86ecb-144">Related topics</span></span>
--------

[<span data-ttu-id="86ecb-145">Oversikt over konvertering av standardkostnad</span><span class="sxs-lookup"><span data-stu-id="86ecb-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)

### <a name="blogs"></a><span data-ttu-id="86ecb-146">Blogger</span><span class="sxs-lookup"><span data-stu-id="86ecb-146">Blogs</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="86ecb-147">Fellesskapsblogger</span><span class="sxs-lookup"><span data-stu-id="86ecb-147">Community blogs</span></span>

- [<span data-ttu-id="86ecb-148">Konfigurere standardkostnader for direkte materialer i Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="86ecb-148">How to set up standard costs for direct materials in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [<span data-ttu-id="86ecb-149">Standard direkte arbeidskostnader i Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="86ecb-149">Standard direct labor costs in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)
