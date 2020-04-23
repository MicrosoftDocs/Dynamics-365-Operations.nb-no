---
title: Planlegg kapasitetsutnyttelse
description: Dette emnet forklarer hvordan du definerer og planlegger belastningen på et lager.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87455077c69834c9ace6409f4cc611ae6e14beb4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204637"
---
# <a name="schedule-load-utilization"></a><span data-ttu-id="4adea-103">Planlegg kapasitetsutnyttelse</span><span class="sxs-lookup"><span data-stu-id="4adea-103">Schedule load utilization</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4adea-104">Du kan planlegge kapasitetsutnyttelse for valgte lokasjonstyper, og du kan også prosjektere gjeldende og fremtidig kapasitetsutnyttelse.</span><span class="sxs-lookup"><span data-stu-id="4adea-104">You can schedule load utilization for selected location types, and you can also project the current and future load utilization.</span></span> <span data-ttu-id="4adea-105">Du kan prosjektere belastningen av ett eller flere områder, for belastningsenhetene (sone eller lager), eller for en kombinasjon av sone og lager.</span><span class="sxs-lookup"><span data-stu-id="4adea-105">You can project the load for one or more sites, for the load units (zone or warehouse), or for a combination of a zone and a warehouse.</span></span>

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a><span data-ttu-id="4adea-106">Planlegge og vise belastningen for et lager eller område</span><span class="sxs-lookup"><span data-stu-id="4adea-106">Schedule and view the load for a warehouse or site</span></span>

<span data-ttu-id="4adea-107">Hvis du vil planlegge belastningen for områder, lagre, eller soner, oppretter du et oppsett for plassutnyttelse og knytter den til en hovedplan.</span><span class="sxs-lookup"><span data-stu-id="4adea-107">To schedule the load for sites, warehouses, or zones, you create a space utilization setup and associate it with a master plan.</span></span>

<span data-ttu-id="4adea-108">I oppsettet for plassutnyttelse du bruker lokasjonstyper, som **Masseplassering** og **Plukklokasjon**, til å angi hvordan plassbruk skal prosjekteres.</span><span class="sxs-lookup"><span data-stu-id="4adea-108">In the space utilization setup, you use location types, such as **Bulk location** and **Picking location**, to specify how space utilization should be projected.</span></span> <span data-ttu-id="4adea-109">Du angir også en lagerbelastningsmodus, for eksempel **Sone**.</span><span class="sxs-lookup"><span data-stu-id="4adea-109">You also specify a storage load mode, such as **Zone**.</span></span>

<span data-ttu-id="4adea-110">Prosjekteringen av fremtidig plassutnyttelse er basert på informasjon som beregnes i den tilknyttede hovedplanen.</span><span class="sxs-lookup"><span data-stu-id="4adea-110">The projection of future space utilization is based on information that is calculated on the associated master plan.</span></span> <span data-ttu-id="4adea-111">Hovedplaner forutsier ressursplanleggingen for innkommende og utgående ordrer for produksjon og operasjoner.</span><span class="sxs-lookup"><span data-stu-id="4adea-111">Master plans forecast the resource planning for incoming and outgoing orders for production and operations.</span></span> <span data-ttu-id="4adea-112">Prosjekteringen av tilgjengelig plass er basert på forholdet mellom oppsettet for plassutnyttelse og den valgte hovedplanen.</span><span class="sxs-lookup"><span data-stu-id="4adea-112">The projection of available space is based on the relation between the space utilization setup and the selected master plan.</span></span>

<span data-ttu-id="4adea-113">Ved hjelp av lagerbelastningsmodusen du valgte i oppsettet for plassutnyttelse, kan du angi om belastningen skal prosjekteres for hvert lager eller hver sone, eller om prosjekteringene skal inkludere informasjon om både varehus og soner.</span><span class="sxs-lookup"><span data-stu-id="4adea-113">By using the storage load mode that you selected in the space utilization setup, you can specify whether the load should be projected for each warehouse or zone, or whether the projections should include information about both warehouses and zones.</span></span> <span data-ttu-id="4adea-114">Du angir også om blokkerte lokasjoner skal ekskluderes fra beregningen av plassutnyttelse.</span><span class="sxs-lookup"><span data-stu-id="4adea-114">You also specify whether blocked locations should be excluded from the calculation of load utilization.</span></span>

<span data-ttu-id="4adea-115">Du kan prosjektere plassutnyttelsen ved å generere rapporten **Utnyttelse av lagerkapasitet**.</span><span class="sxs-lookup"><span data-stu-id="4adea-115">You can project the space utilization by generating the **Warehouse load utilization** report.</span></span> <span data-ttu-id="4adea-116">Når du genererer denne rapporten, kan du angi om plassutnyttelsen skal prosjekteres for hvert område eller på tvers av områder for den valgte belastningsenheten, for eksempel sone eller lager.</span><span class="sxs-lookup"><span data-stu-id="4adea-116">When you generate this report, you can specify whether the load utilization should be projected for each site, across sites, or for the selected load unit, such as zone or warehouse.</span></span>

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a><span data-ttu-id="4adea-117">Opprette et oppsett for utnyttelse av lagerplass</span><span class="sxs-lookup"><span data-stu-id="4adea-117">Create a space utilization setup for a warehouse</span></span>

1. <span data-ttu-id="4adea-118">Velg **Lagerstyring** \> **Oppsett** \> **Lagerovervåking** \> **Plassbruk**.</span><span class="sxs-lookup"><span data-stu-id="4adea-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Space utilization**.</span></span>
2. <span data-ttu-id="4adea-119">Velg **Ny** for å opprette et oppsett for plassutnyttelse.</span><span class="sxs-lookup"><span data-stu-id="4adea-119">Select **New** to create a space utilization setup.</span></span> <span data-ttu-id="4adea-120">Angi en ID og et navn for det nye oppsettet.</span><span class="sxs-lookup"><span data-stu-id="4adea-120">Specify an ID and a name for the new setup.</span></span>
3. <span data-ttu-id="4adea-121">Velg om oversikten over plassutnyttelse skal vise informasjon etter lager, sone eller lager og sone, i feltet **Lagerbelastningsmodus**.</span><span class="sxs-lookup"><span data-stu-id="4adea-121">In the **Storage load mode** field, select whether the overview of space utilization should show information by warehouse, zone, or warehouse and zone.</span></span>
4. <span data-ttu-id="4adea-122">Angi alternativet **Utelat blokkerte lokasjoner** til **Ja** for å utelate blokkerte lagerlokasjoner fra beregningen av tilgjengelig plass.</span><span class="sxs-lookup"><span data-stu-id="4adea-122">Set the **Exclude blocked locations** option to **Yes** to exclude blocked inventory locations from the calculation of available space.</span></span> <span data-ttu-id="4adea-123">Du kan blokkere en lagerlokasjon for innlevering eller utlevering ved å angi en blokkeringsårsak for lokasjonen i feltet **Innlevering blokkert** eller **Utlevering blokkert** på hurtigfanen **Andre** på siden **Lagerlokasjoner**.</span><span class="sxs-lookup"><span data-stu-id="4adea-123">You can block an inventory location for input and output by specifying a blocking cause for the location in the **Input blocked** or **Output blocked** field on the **Other** FastTab on the **Inventory locations** page.</span></span>
5. <span data-ttu-id="4adea-124">Velg lokasjonstyper som skal inkluderes i beregningen av plassutnyttelse, på hurtigfanen **Lokasjonstype**.</span><span class="sxs-lookup"><span data-stu-id="4adea-124">On the **Location type** FastTab, select the location types to include in the space utilization calculation.</span></span> <span data-ttu-id="4adea-125">Du må velge minst én lokasjonstype for prosjekteringen.</span><span class="sxs-lookup"><span data-stu-id="4adea-125">You must select at least one location type for the projection.</span></span>

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a><span data-ttu-id="4adea-126">Knytte et oppsett for plassutnyttelse til en hovedplan</span><span class="sxs-lookup"><span data-stu-id="4adea-126">Associate a space utilization setup with a master plan</span></span>

1. <span data-ttu-id="4adea-127">Velg **Lagerstyring** \> **Periodiske oppgaver** \> **Planlegg kapasitetsutnyttelse**.</span><span class="sxs-lookup"><span data-stu-id="4adea-127">Select **Inventory management** \> **Periodic tasks** \> **Schedule load utilization**.</span></span>
2. <span data-ttu-id="4adea-128">Velg en hovedplan i feltet **Hovedplan**.</span><span class="sxs-lookup"><span data-stu-id="4adea-128">In the **Master plan** field, select a master plan.</span></span>
3. <span data-ttu-id="4adea-129">Angi antall dager som skal inkluderes i prosjekteringen av gjeldende og fremtidig arbeidsmengde, i feltet **Antall dager**.</span><span class="sxs-lookup"><span data-stu-id="4adea-129">In the **Number of days** field, specify the number of days to include in the projection of current and future workloads.</span></span>
4. <span data-ttu-id="4adea-130">Angi oppsettet for plassutnyttelse som skal brukes i prosjekteringen av gjeldende og fremtidig arbeidsmengde, i feltet **Plassbruk**.</span><span class="sxs-lookup"><span data-stu-id="4adea-130">In the **Space utilization** field, select the space utilization setup to use for the projection of current and future workloads.</span></span>

### <a name="specify-the-load-utilization-projection-and-view-information"></a><span data-ttu-id="4adea-131">Angi prosjekteringen av plassutnyttelse og vise informasjon</span><span class="sxs-lookup"><span data-stu-id="4adea-131">Specify the load utilization projection and view information</span></span>

1. <span data-ttu-id="4adea-132">Velg **Lagerstyring** \> **Forespørsler og rapporter** \> **Rapporter for fysisk beholdning** \> **Utnyttelse av lagerkapasitet**.</span><span class="sxs-lookup"><span data-stu-id="4adea-132">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Warehouse load utilization**.</span></span>
2. <span data-ttu-id="4adea-133">Velg prosjekteringsnivået for plassutnyttelse i feltet **Vis etter**:</span><span class="sxs-lookup"><span data-stu-id="4adea-133">In the **Show by** field, select the level of the space utilization projection:</span></span>

    - <span data-ttu-id="4adea-134">**Område** – prosjekter plassutnyttelsen for hvert område.</span><span class="sxs-lookup"><span data-stu-id="4adea-134">**Site** – Project the space utilization for each site.</span></span> <span data-ttu-id="4adea-135">Denne prosjekteringen er nyttig hvis du for eksempel vil vise alle lagrene for et område, slik at du kan balansere plassutnyttelsen mellom lagrene.</span><span class="sxs-lookup"><span data-stu-id="4adea-135">This projection is useful if, for example, you want to view all the warehouses for a site so that you can balance the space utilization between the warehouses.</span></span>
    - <span data-ttu-id="4adea-136">**Belastningsenhet** – prosjekter plassutnyttelsen for soner eller lagre.</span><span class="sxs-lookup"><span data-stu-id="4adea-136">**Load unit** – Project the space utilization for zones or warehouses.</span></span> <span data-ttu-id="4adea-137">Den tilgjengelige plassen prosjekteres deretter i henhold til verdien du valgte i feltet **Lagerbelastningsmodus** på siden **Plassbruk**, da du opprettet plassbrukoppsettet.</span><span class="sxs-lookup"><span data-stu-id="4adea-137">The available space is then projected according to the value that you selected in the **Storage load mode** field on the **Space utilization** page when you created the space utilization setup.</span></span>

3. <span data-ttu-id="4adea-138">Flkg ett av disse trinnene, avhengig av verdien du valgte i forrige trinn:</span><span class="sxs-lookup"><span data-stu-id="4adea-138">Follow one of these steps, depending on the value that you selected in the previous step:</span></span>

    - <span data-ttu-id="4adea-139">Hvis du valgte **Område** i **Vis etter**-feltet, er **Område**-feltet tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="4adea-139">If you selected **Site** in the **Show by** field, the **Site** field is available.</span></span> <span data-ttu-id="4adea-140">Velg ett eller flere områder du vil inkludere i prosjekteringen.</span><span class="sxs-lookup"><span data-stu-id="4adea-140">Select one or more sites to include in the projection.</span></span>
    - <span data-ttu-id="4adea-141">Hvis du valgte **Belastningsenhet** i **Vis etter**-feltet, er **Belastningsenhet**-feltet tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="4adea-141">If you selected **Load unit** in the **Show by** field, the **Load unit** field is available.</span></span> <span data-ttu-id="4adea-142">Velg belastningsenheten.</span><span class="sxs-lookup"><span data-stu-id="4adea-142">Select the load unit.</span></span>

4. <span data-ttu-id="4adea-143">I feltet **Belastningstype** velger du **Volum** eller **Vekt** for å angi to lagerdriftsenheten du vil prosjektere plass for.</span><span class="sxs-lookup"><span data-stu-id="4adea-143">In the **Load type** field, select **Volume** or **Weight** to specify the warehouse operating unit to project space for.</span></span>
5. <span data-ttu-id="4adea-144">Angi oppsettet for plassbruk som prosjekteringen skal baseres på, i feltet **Plassbrukoppsett**.</span><span class="sxs-lookup"><span data-stu-id="4adea-144">In the **Space utilization setup** field, select the space utilization setup that the projection should be based on.</span></span>
