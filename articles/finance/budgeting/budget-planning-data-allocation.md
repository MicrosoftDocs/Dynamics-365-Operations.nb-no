---
title: Datafordeling for budsjettplanlegging
description: Dette emnet beskriver tildelingsmetodene som er tilgjengelige i Microsoft Dynamics 365 Finance, og hvordan de kan brukes.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8bcfb4d3720d03ce84024766a66ccfc546767ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772082"
---
# <a name="budget-planning-data-allocation"></a><span data-ttu-id="d1405-103">Datafordeling for budsjettplanlegging</span><span class="sxs-lookup"><span data-stu-id="d1405-103">Budget planning data allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1405-104">Denne artikkelen beskriver tildelingsmetodene som er tilgjengelige i Microsoft Dynamics 365 Finance, og hvordan de kan brukes.</span><span class="sxs-lookup"><span data-stu-id="d1405-104">This article describes the allocation methods that are available in Microsoft Dynamics 365 Finance and how they can be used.</span></span>  

<span data-ttu-id="d1405-105">Du kan distribuere dataene i en budsjettplan på flere måter for å vise nøyaktig de forventede beløpene.</span><span class="sxs-lookup"><span data-stu-id="d1405-105">You can distribute the data in a budget plan in a number of ways to accurately portray the projected amounts.</span></span>

## <a name="allocation-methods"></a><span data-ttu-id="d1405-106">Tildelingsmetoder</span><span class="sxs-lookup"><span data-stu-id="d1405-106">Allocation methods</span></span>
<span data-ttu-id="d1405-107">Tre tildelingsmetoder (tildele på tvers av perioder, tildele til dimensjoner og bruke finansfordelingsregler) kan opprette budsjettplanlinjer som er basert på linjene i den samme budsjettplanen.</span><span class="sxs-lookup"><span data-stu-id="d1405-107">Three allocation methods (Allocate across periods, Allocate to dimensions, and Use ledger allocation rules) can create budget plan lines that are based on lines in the same budget plan.</span></span> <span data-ttu-id="d1405-108">Tre andre metoder (aggregere, distribuere og kopiere fra budsjettplanen) kan opprette budsjettplanlinjer i andre budsjettplaner.</span><span class="sxs-lookup"><span data-stu-id="d1405-108">Three other methods (Aggregate, Distribute, and Copy from budget plan) can create budget plan lines in other budget plans.</span></span> <span data-ttu-id="d1405-109">Du kan angi målscenariet for alle seks tildelingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="d1405-109">For all six allocation methods, you specify the destination scenario.</span></span> <span data-ttu-id="d1405-110">Målscenariet kan være det samme som kildescenariet eller forskjellig fra kildescenariet.</span><span class="sxs-lookup"><span data-stu-id="d1405-110">The destination scenario can be either the same as the source scenario or different from the source scenario.</span></span> <span data-ttu-id="d1405-111">Du kan også angi om nye linjer legges til budsjettplanen eller erstatter gjeldende linjer i budsjettplanen.</span><span class="sxs-lookup"><span data-stu-id="d1405-111">Additionally, you can specify whether new lines are appended to the budget plan or replace the current lines in the budget plan.</span></span>

<span data-ttu-id="d1405-112">[![Tildelingsmetoden Tildele på tvers av perioder](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Tildele på tvers av perioder** – En periodetildelingskategori brukes for å tildele budsjettplanlinjer fra kildebudsjettplanscenariet på tvers av perioder i målscenariet.</span><span class="sxs-lookup"><span data-stu-id="d1405-112">[![Allocate across Periods allocation method](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Allocate across periods** – A period allocation category is used to allocate the budget plan lines from the source budget plan scenario across periods in the destination scenario.</span></span> <span data-ttu-id="d1405-113">Kildebeløpet tilordnes til flere linjer i målscenariet, basert på prosentdelen og datoen som er definert i periodetildelingsperioden.</span><span class="sxs-lookup"><span data-stu-id="d1405-113">The source amount is assigned to multiple lines in the destination scenario, based on the percentage and date that are defined in the period allocation category.</span></span>         

<span data-ttu-id="d1405-114">[![Tildeldingsmetoden Tildele til dimensjoner](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Tildele til dimensjoner** – Budsjettplanlinjene tildeles fra kildebudsjettplanleggingsscenariet til én eller flere linjer i målscenariet, basert på prosentdelene og finansdimensjonene som er definert i en valgt budsjettfordelingsbetingelse.</span><span class="sxs-lookup"><span data-stu-id="d1405-114">[![Allocate to Dimensions allocation method](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Allocate to dimensions** – The budget plan lines are allocated from the source budget planning scenario to one or more lines in the destination scenario, based on the percentages and financial dimensions that are defined in a selected budget allocation term.</span></span>           

<span data-ttu-id="d1405-115">![Aggregere diagram](./media/aggregatechart-300x230.png)
**Aggregere** – Budsjettplanlinjene aggregeres fra kildebudsjettplanscenariet i de tilknyttede (underordnede) budsjettplanene til målscenariet i den overordnede budsjettplanen.</span><span class="sxs-lookup"><span data-stu-id="d1405-115">![Aggregate chart](./media/aggregatechart-300x230.png)
**Aggregate** – The budget plan lines are aggregated from the source budget plan scenario in the associated (child) budget plans to the destination scenario in the parent budget plan.</span></span> <span data-ttu-id="d1405-116">Denne metoden gjør det mulig for budsjetterte beløp som er klargjort på et lavere nivå i organisasjonen, å konsolideres på et høyere nivå.</span><span class="sxs-lookup"><span data-stu-id="d1405-116">This method enables budget amounts that are prepared at a lower level in the organization to be consolidated at a higher level.</span></span>          

<span data-ttu-id="d1405-117">[![Fordele diagram](./media/distributechart-300x230.png)](./media/distributechart.png)
**Fordele** – Budsjettplanlinjene fordeles fra kildebudsjettplanleggingsscenariet i den overordnede budsjettplanen, til målscenariet i de tilknyttede (underordnede) budsjettplanene, basert på finansdimensjonene for organisasjonsenhetene for de tilknyttede planene.</span><span class="sxs-lookup"><span data-stu-id="d1405-117">[![Distribute chart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Distribute** – The budget plan lines are distributed from the source budget planning scenario in the parent budget plan to the destination scenario in the associated (child) budget plans, based on the financial dimensions of the organization units of the associated plans.</span></span> <span data-ttu-id="d1405-118">Denne metoden gjør det mulig for budsjetterte beløp som er klargjort på et høyere nivå i organisasjonen, å spres ut for mer lokalisert gjennomgang.</span><span class="sxs-lookup"><span data-stu-id="d1405-118">This method enables budget amounts that are prepared at a higher level in the organization to be spread out for more localized review.</span></span>           

<span data-ttu-id="d1405-119">[![Finansfordelingsregler](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Bruk finansfordelingsregler** – Budsjettplanlinjene fordeles fra kildebudsjettplanscenariet i til målbudsjettplanleggingsscenariet basert på den valgte finansfordelingsregelen.</span><span class="sxs-lookup"><span data-stu-id="d1405-119">[![Ledger allocation rules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Use ledger allocation rules** – The budget plan lines are distributed from the source budget planning scenario to the destination scenario, based on the ledger allocation rule that is selected.</span></span> 

<span data-ttu-id="d1405-120">[![Kopier fra budsjettplan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopier fra budsjettplan** – Som i fordelingstildelingsmetoden, opprettes budsjettplanlinjer i målet, basert på linjene i en tilknyttet budsjettplan.</span><span class="sxs-lookup"><span data-stu-id="d1405-120">[![Copy from budget plan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Copy from budget plan** – As in the Distribute allocation method, budget plan lines are created in the destination, based on lines in a related budget plan.</span></span> <span data-ttu-id="d1405-121">For demme metoden trenger imidlertid ikke kildebudsjettplanen å være overordnet, men kan være på et høyere nivåer i budsjettplanhierarkiet.</span><span class="sxs-lookup"><span data-stu-id="d1405-121">However, for this method, the source budget plan doesn't have to be the parent but can be at any higher level in the budget plan hierarchy.</span></span> <span data-ttu-id="d1405-122">Denne tildelingsmetoden er nyttig hvis konsoliderte beløp opprinnelig budsjetteres på et mye høyere nivå og må overføres til et lavere nivå i organisasjonen for detaljert gjennomgang og justering, før vedkommende kan motta godkjenning på øverste nivå.</span><span class="sxs-lookup"><span data-stu-id="d1405-122">This allocation method is useful if consolidated amounts are originally budgeted at a much higher level, and must be transferred to a lower level of the organization for detailed review and adjustment before they can receive upper-level approval.</span></span>          

## <a name="using-allocation-methods-in-a-budget-plan"></a><span data-ttu-id="d1405-123">Bruke tildelingsmetoder i en budsjettplan</span><span class="sxs-lookup"><span data-stu-id="d1405-123">Using allocation methods in a budget plan</span></span>
<span data-ttu-id="d1405-124">Hvis du vil utføre tildelinger på pudsjettplansiden, velger du linjene som skal tildele og klikker deretter **Tildel budsjett**.</span><span class="sxs-lookup"><span data-stu-id="d1405-124">To perform allocations on the budget plan page, select the lines to allocate, and then click **Allocate budget**.</span></span>

<span data-ttu-id="d1405-125">[![Tildel budsjett-knapp](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span><span class="sxs-lookup"><span data-stu-id="d1405-125">[![Allocate budget button](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span></span> 

<span data-ttu-id="d1405-126">Velg en tildelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="d1405-126">Next, select an allocation method.</span></span> <span data-ttu-id="d1405-127">Deretter angis de gjenværende feltene i samsvar med metoden du har valgt.</span><span class="sxs-lookup"><span data-stu-id="d1405-127">The remaining fields are then set, based on the method that you selected.</span></span> <span data-ttu-id="d1405-128">Disse feltene inneholder kilden og målet for budsjettplandataene og et alternativ som lar deg multiplisere kilden med en bestemt faktor når målbeløpene opprettes, for å forenkle samlet justering.</span><span class="sxs-lookup"><span data-stu-id="d1405-128">These fields include the source and destination of the budget plan data, and an option that lets you multiply the source by a specified factor when the destination amounts are created, to simplify bulk adjustment.</span></span> <span data-ttu-id="d1405-129">Du kan også angi alternativet **Legg til i plan**.</span><span class="sxs-lookup"><span data-stu-id="d1405-129">You can also set the **Append to plan** option.</span></span> <span data-ttu-id="d1405-130">Velg **Nei** for å erstatte de eksisterende budsjettplanlinjene, eller velg **Ja** for å beholde de eksisterende budsjettplanlinjene og legge til nye linjer for de tilordnede beløpene.</span><span class="sxs-lookup"><span data-stu-id="d1405-130">Select **No** to replace the existing budget plan lines, or select **Yes** to retain the existing budget plan lines and add new lines for the allocated amounts.</span></span>

## <a name="automating-allocations-during-a-workflow"></a><span data-ttu-id="d1405-131">Automatisere tildelinger under en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="d1405-131">Automating allocations during a workflow</span></span>
<span data-ttu-id="d1405-132">En kraftig funksjon gjør det mulig å utføre tildelinger automatisk som en del av en arbeidsflyt for budsjettplanlegging.</span><span class="sxs-lookup"><span data-stu-id="d1405-132">One powerful feature enables allocations to be performed automatically as part of a budget planning workflow.</span></span> <span data-ttu-id="d1405-133">Når en budsjettplan flyttes gjennom arbeidsflyten, kan automatiserte oppgaver starte en tildeling på et bestemt budsjettplanleggingsstadium.</span><span class="sxs-lookup"><span data-stu-id="d1405-133">As a budget plan moves through its workflow, automated tasks can invoke an allocation at a specified budget planning stage.</span></span> 

<span data-ttu-id="d1405-134">Hvis du vil angi automatisk tildeling, må du først opprette en tildelingsplan på siden **Budsjettplanleggingskonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="d1405-134">To set up automated allocation, you must first create an allocation schedule on the **Budget planning configuration** page.</span></span> <span data-ttu-id="d1405-135">Tildelingsplanen definerer tildelingsmetoden som skal brukes når den automatisk tildelingen kjøres, og verdiene for de ulike alternativene for tildeling (se avsnittet for beskrivelser).</span><span class="sxs-lookup"><span data-stu-id="d1405-135">The allocation schedule defines the allocation method that will be used when the automated allocation is run, and the values of the various allocation options (see the previous section for descriptions).</span></span> 

<span data-ttu-id="d1405-136">Deretter oppretter du en stadietildeling på siden **Budsjettplanleggingskonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="d1405-136">Next, you create a stage allocation on the **Budget planning configuration** page.</span></span> <span data-ttu-id="d1405-137">Stadietildelingen tildeler en tildelingsplan til arbeidsflyten for budsjettplanlegging og stadiet.</span><span class="sxs-lookup"><span data-stu-id="d1405-137">The stage allocation assigns an allocation schedule to the budget planning workflow and stage.</span></span> 

<span data-ttu-id="d1405-138">Til slutt legger du til en automatisert oppgave for tildeling for budsjettplanleggingsstadiet på det aktuelle arbeidsflytstadiet.</span><span class="sxs-lookup"><span data-stu-id="d1405-138">Finally, add an automated task for budget planning stage allocation at the desired workflow stage.</span></span> <span data-ttu-id="d1405-139">I eksemplet nedenfor er to tildelinger for budsjettplanleggingsstadiet (uthevet i rødt) satt inn i arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="d1405-139">In the following example, two budget planning stage allocations (outlined in red) have been inserted into the workflow.</span></span>

<span data-ttu-id="d1405-140">[![Fordelinger for budsjettplanleggingsstadium](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span><span class="sxs-lookup"><span data-stu-id="d1405-140">[![Budget planning stage allocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span></span>



