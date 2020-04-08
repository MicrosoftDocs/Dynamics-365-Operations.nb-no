---
title: Overføre prosjektbudsjetter ved regnskapsårets avslutning
description: Denne artikkelen gir informasjon om hvordan du overfører gjenstående budsjettbeløp til fremtidige år og oppretter budsjettregisterdetaljer.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172336"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="c712b-103">Overføre prosjektbudsjetter ved regnskapsårets avslutning</span><span class="sxs-lookup"><span data-stu-id="c712b-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c712b-104">Når du arbeider med et prosjekt med flere år, kan du ha gjenværende budsjett på slutten av regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="c712b-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="c712b-105">Du kan ovefføre de gjenstående budsjettbeløpene til et fremtidig år, og opprette budsjettregisterdetaljer for beløpene i de tilknyttede finanskontoene.</span><span class="sxs-lookup"><span data-stu-id="c712b-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="c712b-106">Før du overfører de gjenværende beløpene, kan du se over og analysere de gjenværende budsjettbeløpene.</span><span class="sxs-lookup"><span data-stu-id="c712b-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="c712b-107">Gå gjennom og analysere gjenstående budsjettbeløp</span><span class="sxs-lookup"><span data-stu-id="c712b-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="c712b-108">Fullfør fremgangsmåten nedenfor for å gå gjennom budsjettbeløpene for prosjekter ved årsavslutning, men ikke overføre beløpene.</span><span class="sxs-lookup"><span data-stu-id="c712b-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="c712b-109">Gå til **Prosjektstyring og regnskap** > **Tidsbestemt** > **Budsjetter** > **Overfør budsjetter**.</span><span class="sxs-lookup"><span data-stu-id="c712b-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="c712b-110">På siden **Overføringsprosess for prosjektbudsjett**, i kategorien **Alternativer for årsavslutning**, kontrollerer du at **Overfør gjenværende prosjektbudsjettbeløp** ikke er aktivert.</span><span class="sxs-lookup"><span data-stu-id="c712b-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="c712b-111">I kategorien **Parametere**, i feltet **Budsjettår for prosjekt** velger du regnskapsåret som du vil vise de gjenstående budsjettbeløpene for.</span><span class="sxs-lookup"><span data-stu-id="c712b-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="c712b-112">Velg regnskapsåret som du vil vise de gjenstående budsjettbeløpene for, i feltet **Føste regnskapsår**.</span><span class="sxs-lookup"><span data-stu-id="c712b-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="c712b-113">I feltet **Fra prognosemodell** velger du **Gjenstående budsjett**.</span><span class="sxs-lookup"><span data-stu-id="c712b-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="c712b-114">Hvis du vil ta med prosjekter som oppfyller de valgte kriteriene og ikke har noe gjenstående budsjett, velger du **Vis null gjenværende**.</span><span class="sxs-lookup"><span data-stu-id="c712b-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="c712b-115">I kategorien **Velg budsjetter** velger du **Hent alle budsjetter** for å laste alle budsjetter som samsvarer med de valgte kriteriene, og velg deretter **Behandle**.</span><span class="sxs-lookup"><span data-stu-id="c712b-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="c712b-116">Hvis du vil utforme en databasespørring som laster inn et bestemt sett med budsjetter i ruten, velger du **Hent valgte budsjetter**.</span><span class="sxs-lookup"><span data-stu-id="c712b-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="c712b-117">Hvis du vil ha mer informasjon om en bestemt linje i ruten, velger du linjen og velger deretter **Vis budsjettdetaljer** eller **Vis kontoer**.</span><span class="sxs-lookup"><span data-stu-id="c712b-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="c712b-118">Overfør gjenværende budsjettbeløp</span><span class="sxs-lookup"><span data-stu-id="c712b-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="c712b-119">Når du behandler gjenstående budsjettbeløp, kan du opprette transaksjoner i økonomimodulen for beløpene du overfører.</span><span class="sxs-lookup"><span data-stu-id="c712b-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="c712b-120">Hvis du vil opprette økonomimodultransaksjoner, fullfører du trinnene i delen [Overføre budsjettbeløp og opprette økonomimodultransaksjoner](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="c712b-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="c712b-121">Budsjettbeløp som overføres, sendes til prognosemodellen som er valgt som prognosemodell for overføring på siden **Prognosemodeller**.</span><span class="sxs-lookup"><span data-stu-id="c712b-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="c712b-122">Overføre budsjettbeløp og opprette økonomimodultransaksjoner</span><span class="sxs-lookup"><span data-stu-id="c712b-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="c712b-123">Velg **Prosjektstyring og regnskap** > **Tidsbestemt** > **Budsjetter** > **Overfør budsjetter**.</span><span class="sxs-lookup"><span data-stu-id="c712b-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="c712b-124">På siden **Overføringsprosess for prosjektbudsjett** velger du **Årsavslutning**, og deretter aktiverer du **Overfør gjenværende prosjektbudsjettbeløp** og **Opprett budsjettregisteroppføringer i økonomimodul**.</span><span class="sxs-lookup"><span data-stu-id="c712b-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="c712b-125">Velg følgende i kategorien **Parametere** i **Prosjektparametere**-feltgruppen:</span><span class="sxs-lookup"><span data-stu-id="c712b-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="c712b-126">**Budsjettår for prosjekt**: Velg begynnelsen på regnskapsåret som du vil vise de gjenstående budsjettbeløpene for.</span><span class="sxs-lookup"><span data-stu-id="c712b-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="c712b-127">**Resultat**: Opprett resultattransaksjoner i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="c712b-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="c712b-128">**VIA**: Opprett VIA-transaksjoner i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="c712b-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="c712b-129">**Lønn**: Opprett lønnsfordelingstransaksjoner i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="c712b-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="c712b-130">Angi følgende informasjon i **Økonomimodul**-feltgruppen:</span><span class="sxs-lookup"><span data-stu-id="c712b-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="c712b-131">Velg regnskapsåret du vil overføre de gjenstående budsjettbeløpene for prosjektene til, i feltet **Første regnskapsår**.</span><span class="sxs-lookup"><span data-stu-id="c712b-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="c712b-132">Standardverdien er ett år etter verdien i feltet **Budsjettår for prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="c712b-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="c712b-133">Velg perioden du vil opprette budsjettregisterdetaljene for i økonomimodulen i, i **Overføringsperiode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c712b-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="c712b-134">Dette er vanligvis den første perioden i det første regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="c712b-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="c712b-135">Angi følgende informasjon i **Kopier til/fra**-feltgruppen:</span><span class="sxs-lookup"><span data-stu-id="c712b-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="c712b-136">Velg prognosemodellen for prosjektbudsjett som er knyttet til de gjenstående budsjettbeløpene du vil overføre for prosjektene, i feltet **Fra prognosemodell**.</span><span class="sxs-lookup"><span data-stu-id="c712b-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="c712b-137">Velg finansbudsjettmodellen som er knyttet til de gjenstående budsjettbeløpene du vil overføre til økonomimodulen, i feltet **Finansbudsjettmodell**.</span><span class="sxs-lookup"><span data-stu-id="c712b-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="c712b-138">Velg **Overfør salgsvaluta** hvis du vil bruke prosjektets salgsvaluta for økonomimodultransaksjoner som opprettes når du overfører budsjettbeløpene for prosjektene.</span><span class="sxs-lookup"><span data-stu-id="c712b-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="c712b-139">Når alternativet ikke er valgt, bruker transaksjonene regnskapsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="c712b-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="c712b-140">Velg **Vis null gjenværende** hvis du vil ta med prosjekter som ikke har gjenstående budsjettbeløp, men som oppfyller de andre kriteriene du velger blant prosjektene som vises i den nedre ruten.</span><span class="sxs-lookup"><span data-stu-id="c712b-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="c712b-141">I kategorien **Velg budsjetter** velger du **Hent alle budsjetter** for å laste alle budsjetter som samsvarer med de valgte kriteriene.</span><span class="sxs-lookup"><span data-stu-id="c712b-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="c712b-142">Hvis du vil utforme en databasespørring som laster inn et bestemt sett med prosjektbudsjetter i ruten, velger du **Hent valgte budsjetter**.</span><span class="sxs-lookup"><span data-stu-id="c712b-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="c712b-143">Velg alternativet på begynnelsen av linjen for hvert prosjekt du vil behandle.</span><span class="sxs-lookup"><span data-stu-id="c712b-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="c712b-144">Hvis du vil merke alle eller de fleste av prosjektene, velger du avmerkingsboksen øverst til venstre.</span><span class="sxs-lookup"><span data-stu-id="c712b-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="c712b-145">Hvis du vil utelate behandling av prosjekter, fjerner du merket for dette prosjektet.</span><span class="sxs-lookup"><span data-stu-id="c712b-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="c712b-146">Velg **Behandle** hvis du vil overføre de gjenstående budsjettbeløpene for de valgte prosjektene til det valgte regnskapsåret og opprette budsjettregisterdetaljer i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="c712b-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="c712b-147">Overføre budsjettbeløp uten å opprette økonomimodultransaksjoner</span><span class="sxs-lookup"><span data-stu-id="c712b-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="c712b-148">Gå til **Prosjektstyring og regnskap** > **Tidsbestemt** > **Budsjetter** > **Overfør budsjetter**.</span><span class="sxs-lookup"><span data-stu-id="c712b-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="c712b-149">På siden **Overføringsprosess for prosjektbudsjett**, i feltet **Alternativer for årsavslutning**, velger du **Overfør gjenværende prosjektbudsjettbeløp**.</span><span class="sxs-lookup"><span data-stu-id="c712b-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="c712b-150">I **Parametere**-gruppen, i feltet **Budsjettår for prosjekt** velger du regnskapsåret som du vil vise det gjenstående budsjettbeløpet for.</span><span class="sxs-lookup"><span data-stu-id="c712b-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="c712b-151">Angi følgende informasjon i **Kopier til/fra**-gruppen:</span><span class="sxs-lookup"><span data-stu-id="c712b-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="c712b-152">Velg prognosemodellen for prosjektbudsjett som er knyttet til de gjenstående budsjettbeløpene du vil overføre for prosjektene, i feltet **Fra prognosemodell**.</span><span class="sxs-lookup"><span data-stu-id="c712b-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="c712b-153">Hvis du vil ta med prosjekter som oppfyller de valgte kriteriene, men ikke har noe gjenstående budsjettbeløp, velger du **Vis null gjenværende**.</span><span class="sxs-lookup"><span data-stu-id="c712b-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="c712b-154">I gruppen **Velg budsjetter** velger du **Hent alle budsjetter** for å laste alle budsjetter som samsvarer med de valgte kriteriene.</span><span class="sxs-lookup"><span data-stu-id="c712b-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="c712b-155">Hvis du vil utforme en databasespørring som laster inn et bestemt sett med prosjektbudsjetter i ruten, velger du **Hent valgte budsjetter**.</span><span class="sxs-lookup"><span data-stu-id="c712b-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="c712b-156">Velg alternativet på begynnelsen av linjen for hvert prosjekt du vil behandle.</span><span class="sxs-lookup"><span data-stu-id="c712b-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="c712b-157">Velg **Behandle** hvis du vil overføre de gjenstående budsjettbeløpene for de valgte prosjektene til valgt regnskapsår.</span><span class="sxs-lookup"><span data-stu-id="c712b-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>

