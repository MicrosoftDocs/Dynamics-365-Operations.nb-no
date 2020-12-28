---
title: Planlegge kapasitet for arbeidsmengde
description: Dette emnet forklarer hvordan du definerer og planlegger arbeidsmengdekapasiteten for ansatte i et lager eller et helt lager.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd4225d9e7ad65939c57cb770ba521377c87dea3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434198"
---
# <a name="schedule-workload-capacity"></a><span data-ttu-id="ceb11-103">Planlegge kapasitet for arbeidsmengde</span><span class="sxs-lookup"><span data-stu-id="ceb11-103">Schedule workload capacity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ceb11-104">Du kan planlegge arbeidsmengdekapasitet for lagre, og du kan også projisere gjeldende og fremtidig arbeidsmengde for arbeiderne på individuelle lagre.</span><span class="sxs-lookup"><span data-stu-id="ceb11-104">You can schedule workload capacity for warehouses, and you can also project the current and future workloads for the workers in individual warehouses.</span></span> <span data-ttu-id="ceb11-105">Du kan projisere arbeidsmengden for hele lageret, eller du kan projisere arbeidsmengden separat for innkommende og utgående arbeidsmengde.</span><span class="sxs-lookup"><span data-stu-id="ceb11-105">You can project the workload for the whole warehouse, or you can project the workload separately for incoming and outgoing workloads.</span></span>

<span data-ttu-id="ceb11-106">For å projisere levert arbeidsmengde for valgte lagre må det finnes hovedplanleggingsdata tilgjengelige for disse lagrene.</span><span class="sxs-lookup"><span data-stu-id="ceb11-106">To project workload output for selected warehouses, master scheduling data must be available for those warehouses.</span></span> <span data-ttu-id="ceb11-107">Hvis du vil ha mer informasjon om hovedplaner, kan du se [Oversikt over hovedplaner](../master-planning/master-plans.md).</span><span class="sxs-lookup"><span data-stu-id="ceb11-107">For more information, see [Master plans overview](../master-planning/master-plans.md).</span></span>

## <a name="schedule-and-view-workloads-for-a-warehouse"></a><span data-ttu-id="ceb11-108">Planlegg og vis arbeidsmengder for et lager</span><span class="sxs-lookup"><span data-stu-id="ceb11-108">Schedule and view workloads for a warehouse</span></span>

<span data-ttu-id="ceb11-109">For å planlegge arbeidsmengdekapasitet for et lager oppretter du et arbeidsmengdeoppsett for et eller flere lagre, og tilknytter deretter arbeidsmengdeoppsett med en hovedplan.</span><span class="sxs-lookup"><span data-stu-id="ceb11-109">To schedule workload capacity for a warehouse, you create a workload setup for one or more warehouses, and then associate the workload setup with a master plan.</span></span> <span data-ttu-id="ceb11-110">I arbeidsmengdeoppsettet kan du definere grenser for vekt eller volum for innkommende og utgående transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="ceb11-110">In the workload capacity setup, you can define limits for the weight or volume for incoming and outgoing transactions.</span></span> <span data-ttu-id="ceb11-111">Du kan også opprette mer enn ett oppsett for hver lager og deretter knytte oppsettet til individuelle hovedplaner.</span><span class="sxs-lookup"><span data-stu-id="ceb11-111">You can also create more than one setup for each warehouse and then associate the setup with individual master plans.</span></span> <span data-ttu-id="ceb11-112">Du kan for eksempel bruke denne fremgangsmåten for å være i tråd med sesongendringer i arbeidsstyrken.</span><span class="sxs-lookup"><span data-stu-id="ceb11-112">For example, you might use this approach to accommodate seasonal changes in the workforce.</span></span>

<span data-ttu-id="ceb11-113">Hvis arbeiderne på et lager jobber med transaksjoner for både innkommende og utgående arbeidsmengder, kan du konfigurere lagerkapasitetsoppsettet, slik at arbeidsmengden prosjekteres i en kombinert visning.</span><span class="sxs-lookup"><span data-stu-id="ceb11-113">If the workers for a warehouse work with transactions for both incoming and outgoing workloads, you can configure the warehouse capacity setup so that the workload is projected in a combined view.</span></span>

<span data-ttu-id="ceb11-114">For å planlegge og vise arbeidsmengder for lagre, må du utføre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="ceb11-114">To schedule and view workloads for warehouses, you must complete the following tasks:</span></span>

1. <span data-ttu-id="ceb11-115">Opprett et arbeidsmengdekapasitetsoppsett og definer begrensninger for arbeidsmengdekapasitet for ett eller flere lagre.</span><span class="sxs-lookup"><span data-stu-id="ceb11-115">Create a workload capacity setup and define workload capacity limits for one or more warehouses.</span></span>
2. <span data-ttu-id="ceb11-116">Knytt arbeidsmengdekapasitetsoppsettet til en hovedplan for å opprette arbeidsmengdeprojeksjoner og spesifisere hvor lenge disse projeksjonene gjelder.</span><span class="sxs-lookup"><span data-stu-id="ceb11-116">Associate the workload capacity setup with a master plan to create workload projections and specify how long those projections will apply.</span></span>

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a><span data-ttu-id="ceb11-117">Opprett et arbeidsmengdekapasitetsoppsett for et lager</span><span class="sxs-lookup"><span data-stu-id="ceb11-117">Create a workload capacity setup for a warehouse</span></span>

1. <span data-ttu-id="ceb11-118">Velg **Lagerstyring** \> **Oppsett** \> **Lagerovervåking** \> **Arbeidsmengdekapasitet**.</span><span class="sxs-lookup"><span data-stu-id="ceb11-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="ceb11-119">I handlingsruten velger du **Ny** for å opprette et oppsett for arbeidsmengdekapasitet.</span><span class="sxs-lookup"><span data-stu-id="ceb11-119">On the Action Pane, select **New** to create a workload capacity setup.</span></span>
3. <span data-ttu-id="ceb11-120">På hurtigfanen **Lagre** velger du **Ny**, og angi deretter verdiene på linjen for å knytte et lager til arbeidsmengdekapasitetsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="ceb11-120">On the **Warehouses** FastTab, select **New**, and then enter values on the line to associate a warehouse with the workload capacity setup.</span></span>
4. <span data-ttu-id="ceb11-121">Merk av for **Kombinert innkommende og utgående arbeidsmengde** hvis rapporten **Arbeidsmengdekapasitet** skal vise den totale arbeidsmengden for innkommende og utgående transaksjoner i én visning.</span><span class="sxs-lookup"><span data-stu-id="ceb11-121">Select the **Combined inbound and outbound workload** check box if the **Workload capacity** report should show the total workload for incoming and outgoing transactions in one view.</span></span>
5. <span data-ttu-id="ceb11-122">På hurtigfanen **Transaksjonstyper** velger du de innkommende og utgående transaksjonstypene som arbeidsmengdebegrensningene gjelder.</span><span class="sxs-lookup"><span data-stu-id="ceb11-122">On the **Transaction types** FastTab, select the types of incoming and outgoing transactions that the workload limits will apply to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ceb11-123">Du må velge minst én transaksjonstype for både den innkommende og den utgående arbeidsmengden.</span><span class="sxs-lookup"><span data-stu-id="ceb11-123">You must select at least one transaction type for both the incoming workload and the outgoing workload.</span></span>

#### <a name="define-limits-for-volume-or-weight"></a><span data-ttu-id="ceb11-124">Definere grenser for volum eller vekt</span><span class="sxs-lookup"><span data-stu-id="ceb11-124">Define limits for volume or weight</span></span>

<span data-ttu-id="ceb11-125">Du kan definere grenser for volum eller vekt avhengig av begrensningene som gjelder for lagerets arbeidsstyrke.</span><span class="sxs-lookup"><span data-stu-id="ceb11-125">You can set up limits for volume or weight, depending on the limitation that is relevant for the warehouse workforce.</span></span> <span data-ttu-id="ceb11-126">Grensene du spesifiserer, inkluderes i projeksjonen av arbeidsmengdekapasitet som du kan se i rapporten **Arbeidsmengdekapasitet**.</span><span class="sxs-lookup"><span data-stu-id="ceb11-126">The limits that you specify are included in the workload capacity projection that you can view on the **Workload capacity** report.</span></span>

<span data-ttu-id="ceb11-127">For å prosjektere informasjon om volum og vekt for varer må standardvolumet til én lagervare og vekten av én lagervare spesifiseres for alle produkter.</span><span class="sxs-lookup"><span data-stu-id="ceb11-127">To project information about volume and weight for items, the standard volume of one inventory item and the weight of one inventory item must be specified for all products.</span></span> <span data-ttu-id="ceb11-128">Feltene som kreves er tilgjengelige i følgende feltgrupper på hurtigfanen **Administrer lager** på siden **Detaljer om frigitt produkt**:</span><span class="sxs-lookup"><span data-stu-id="ceb11-128">The fields that are required are available in the following field groups on the **Manage inventory** FastTab of the **Released product details** page:</span></span>

- <span data-ttu-id="ceb11-129">Behandling</span><span class="sxs-lookup"><span data-stu-id="ceb11-129">Handling</span></span>
- <span data-ttu-id="ceb11-130">Fysiske dimensjoner</span><span class="sxs-lookup"><span data-stu-id="ceb11-130">Physical dimensions</span></span>
- <span data-ttu-id="ceb11-131">Vektmålinger</span><span class="sxs-lookup"><span data-stu-id="ceb11-131">Weight measurements</span></span>

<span data-ttu-id="ceb11-132">Hvis denne informasjonen ikke blir korrekt spesifisert, vil du motta en melding når du genererer rapporten **Arbeidsmengdekapasitet**.</span><span class="sxs-lookup"><span data-stu-id="ceb11-132">If this information isn't specified correctly, you receive a message when you generate the **Workload capacity** report.</span></span> <span data-ttu-id="ceb11-133">Fra rapporten kan du vise flere detaljer for å identifisere den manglende informasjonen som kreves, for å prosjektere fremtidig arbeidsmengde.</span><span class="sxs-lookup"><span data-stu-id="ceb11-133">From the report, you can then drill down to identify the missing information that is required in order to project the future workload.</span></span>

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a><span data-ttu-id="ceb11-134">Knytt et arbeidsmengdekapasitetsoppsett til en hovedplan</span><span class="sxs-lookup"><span data-stu-id="ceb11-134">Associate a workload capacity setup with a master plan</span></span>

1. <span data-ttu-id="ceb11-135">Velg **Lagerstyring** \> **Periodiske oppgaver** \> **Planlegg arbeidsmengde**.</span><span class="sxs-lookup"><span data-stu-id="ceb11-135">Select **Inventory management** \> **Periodic** \> **Schedule workload**.</span></span>
2. <span data-ttu-id="ceb11-136">I **Hovedplan**-feltet velger du hovedplanen som skal brukes for arbeidsmengdeprojeksjoner.</span><span class="sxs-lookup"><span data-stu-id="ceb11-136">In the **Master plan** field, select the master plan to use for workload projections.</span></span>
3. <span data-ttu-id="ceb11-137">Spesifiser antall dager arbeidsmengdeprojeksjonen dekker i feltet **Antall dager**.</span><span class="sxs-lookup"><span data-stu-id="ceb11-137">In the **Number of days** field, specify the number of days that the workload projection covers.</span></span>
4. <span data-ttu-id="ceb11-138">Velg arbeidsmengdeoppsettet du vil knytte til hovedplanen, i **Arbeidsmengde**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ceb11-138">In the **Workload** field, select the workload setup to associate with the master plan.</span></span>

### <a name="view-workload-capacity"></a><span data-ttu-id="ceb11-139">Vis arbeidsmengdekapasitet</span><span class="sxs-lookup"><span data-stu-id="ceb11-139">View workload capacity</span></span>

1. <span data-ttu-id="ceb11-140">Velg **Lagerstyring** \> **Forespørsler og rapporter** \> **Rapporter for fysisk beholdning** \> **Arbeidsmengdekapasitet**.</span><span class="sxs-lookup"><span data-stu-id="ceb11-140">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="ceb11-141">Spesifiser antall kolonner som skal vises på rapporten, i feltet **Antall kolonner**.</span><span class="sxs-lookup"><span data-stu-id="ceb11-141">In the **Number of columns** field, specify the number of columns to show on the report.</span></span>
3. <span data-ttu-id="ceb11-142">I feltet **Ordretype** velger du **Planlagt og bekreftet**, **Planlagt** eller **Bekreftet** for å angi hvilke typer ordrer som skal prosjekteres i rapporten.</span><span class="sxs-lookup"><span data-stu-id="ceb11-142">In the **Order type** field, select **Planned and confirmed**, **Planned**, or **Confirmed** to indicate the type of orders to project on the report.</span></span>
4. <span data-ttu-id="ceb11-143">Velg en belastningstype i **Belastningstype**-feltet for å angi om arbeidsmengdekapasiteten skal prosjekteres for volum eller vekt.</span><span class="sxs-lookup"><span data-stu-id="ceb11-143">In the **Load type** field, select a load type to specify whether the workload capacity should be projected for volume or weight.</span></span>
5. <span data-ttu-id="ceb11-144">I feltet **Arbeidsmengdekapasitet** velger du et arbeidsmengdekapasitetsoppsett.</span><span class="sxs-lookup"><span data-stu-id="ceb11-144">In the **Workload capacity** field, select a workload capacity setup.</span></span>
