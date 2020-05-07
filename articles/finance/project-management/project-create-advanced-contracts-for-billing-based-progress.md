---
title: Opprette avanserte kontrakter for fakturering basert på fremdriften
description: Dette emnet forklarer hvordan du oppretter prosjektkontrakter slik at du kan generere fakturaer for kunder, basert på en prosentdel av fullført arbeid.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
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
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282841"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="3985d-103">Opprette avanserte kontrakter for fakturering basert på fremdriften</span><span class="sxs-lookup"><span data-stu-id="3985d-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="3985d-104">Dette emnet forklarer hvordan du oppretter prosjektkontrakter slik at du kan generere fakturaer for kunder, basert på en prosentdel av fullført arbeid.</span><span class="sxs-lookup"><span data-stu-id="3985d-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="3985d-105">Fakturabeløpene beregnes automatisk for budsjettkategoriene av arbeid som du har definert for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="3985d-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="3985d-106">Tidsmålingen av fakturaer defineres når du forhandler frem prosjektkontrakten med kunden.</span><span class="sxs-lookup"><span data-stu-id="3985d-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="3985d-107">Bruk disse prosedyrene for å definere en kontrakt, et tilknyttet prosjekt og faktureringsreglene som skal brukes for å beregne fakturabeløp for budsjettkategoriene av arbeid som du har definert for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="3985d-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="3985d-108">Når du har opprettet kontrakten og prosjektet, kan du angi prosjektdetaljene.</span><span class="sxs-lookup"><span data-stu-id="3985d-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="3985d-109">Du kan for eksempel angi aktivitetene og tilordne arbeidere til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="3985d-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="3985d-110">Eksempel</span><span class="sxs-lookup"><span data-stu-id="3985d-110">Example</span></span>

<span data-ttu-id="3985d-111">Organisasjonen din er et firma som driver programvareutvikling.</span><span class="sxs-lookup"><span data-stu-id="3985d-111">Your organization is a software development firm.</span></span> <span data-ttu-id="3985d-112">Du avtaler utvikling av en lønnsregnskapspakke for en kunde mot et totalgebyr på USD 20 000.</span><span class="sxs-lookup"><span data-stu-id="3985d-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="3985d-113">Organisasjonen avtaler å sende en faktura til kunden etter hvert som du fullfører bestemte prosenter av prosjektet.</span><span class="sxs-lookup"><span data-stu-id="3985d-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="3985d-114">Du definerer følgende prosjektkategorier for arbeidet, slik at du kan bruke dem i betalingsprosessen:</span><span class="sxs-lookup"><span data-stu-id="3985d-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="3985d-115">Rådgivning</span><span class="sxs-lookup"><span data-stu-id="3985d-115">Consulting</span></span>
- <span data-ttu-id="3985d-116">Utforming</span><span class="sxs-lookup"><span data-stu-id="3985d-116">Design</span></span>
- <span data-ttu-id="3985d-117">Installasjon</span><span class="sxs-lookup"><span data-stu-id="3985d-117">Installation</span></span>

<span data-ttu-id="3985d-118">Du definerer også faktureringsregler som automatisk beregner fakturabeløpene for prosenten av prosjektet som er fullført i hver kategori.</span><span class="sxs-lookup"><span data-stu-id="3985d-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="3985d-119">Budsjettlederen oppretter et budsjett for prosjektkategoriene.</span><span class="sxs-lookup"><span data-stu-id="3985d-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="3985d-120">Beløpet for fullført arbeid beregnes automatisk som en prosent av faktisk arbeid, sammenlignet med budsjetterte beløp.</span><span class="sxs-lookup"><span data-stu-id="3985d-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3985d-121">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="3985d-121">Prerequisites</span></span>

<span data-ttu-id="3985d-122">Før du oppretter et prosjekt som bruker faktureringsregler, må du definere nummerseriene for faktureringsregler og en gebyrjournal som brukes til å postere fremdriftsfaktureringer.</span><span class="sxs-lookup"><span data-stu-id="3985d-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="3985d-123">Gå til **Prosjektstyring og regnskap** \> **Oppsett** \> **Prosjektstyrings- og regnskapsparametere**.</span><span class="sxs-lookup"><span data-stu-id="3985d-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="3985d-124">Definer nummerserien du vil bruk når det opprettes faktureringsregler, på siden **Parametere for prosjektstyring og regnskap** i kategorien **Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="3985d-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="3985d-125">Gå til **Prosjektstyring og regnskap** \> **Journaler** \> **Gebyr**.</span><span class="sxs-lookup"><span data-stu-id="3985d-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="3985d-126">Velg **Ny** på **Gebyrjournal**-siden, og angi journalnavnet.</span><span class="sxs-lookup"><span data-stu-id="3985d-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="3985d-127">Opprette kontrakt for fremdriftsfakturering</span><span class="sxs-lookup"><span data-stu-id="3985d-127">Create a contract for progress billings</span></span>

<span data-ttu-id="3985d-128">Bruk denne prosedyren til å opprette en prosjektkontrakt for et fastprisprosjekt.</span><span class="sxs-lookup"><span data-stu-id="3985d-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="3985d-129">Du oppretter en prosjektfaktura når arbeidet som er fullført på prosjektet når en bestemt prosent.</span><span class="sxs-lookup"><span data-stu-id="3985d-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="3985d-130">Gå til **Prosjektstyring og regnskap** \> **Projekter** \> **Prosjektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="3985d-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="3985d-131">Velg **Ny** på siden **Prosjektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="3985d-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="3985d-132">I dialogboksen **Ny prosjektkontrakt** angir du følgende felt:</span><span class="sxs-lookup"><span data-stu-id="3985d-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="3985d-133">**Navn**</span><span class="sxs-lookup"><span data-stu-id="3985d-133">**Name**</span></span>
    - <span data-ttu-id="3985d-134">**Finansieringstype**</span><span class="sxs-lookup"><span data-stu-id="3985d-134">**Funding type**</span></span>
    - <span data-ttu-id="3985d-135">**Finansieringskilde**</span><span class="sxs-lookup"><span data-stu-id="3985d-135">**Funding source**</span></span>
    - <span data-ttu-id="3985d-136">**Salgsvaluta** – Dette er standardvalutaen som brukes til kundefakturaer som er tilknyttet prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="3985d-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="3985d-137">Du kan imidlertid endre salgsvalutaen på en bestemt kundefaktura.</span><span class="sxs-lookup"><span data-stu-id="3985d-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="3985d-138">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3985d-138">Select **OK**.</span></span> <span data-ttu-id="3985d-139">Informasjonen kopieres til hodet på **Prosjektkontrakter**-siden.</span><span class="sxs-lookup"><span data-stu-id="3985d-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="3985d-140">På **Prosjektkontrakter**-siden fyller du ut resten av den nødvendige informasjonen for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="3985d-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="3985d-141">Opprette et prosjekt for fremdriftsfakturering</span><span class="sxs-lookup"><span data-stu-id="3985d-141">Create a project for progress billings</span></span>

<span data-ttu-id="3985d-142">Bruk denne fremgangsmåten for å opprette et prosjekt og eventuelle underprosjekter som er tilknyttet en prosjektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="3985d-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="3985d-143">Gå til **Prosjektstyring og regnskap** \> **Projekter** \> **Alle prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="3985d-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="3985d-144">Velg **Ny** på siden **Alle prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="3985d-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="3985d-145">I dialogboksen **Nytt prosjekt**, i feltet **Prosjekttype**, velger du **Tid og materialer**.</span><span class="sxs-lookup"><span data-stu-id="3985d-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="3985d-146">Velg en prosjektgruppe.</span><span class="sxs-lookup"><span data-stu-id="3985d-146">Select a project group.</span></span> <span data-ttu-id="3985d-147">En prosjektgruppe angir posteringsinformasjon for prosjekter som er tilordnet gruppen.</span><span class="sxs-lookup"><span data-stu-id="3985d-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="3985d-148">Velg **Opprett prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="3985d-148">Select **Create project**.</span></span>
6. <span data-ttu-id="3985d-149">Når du har opprettet prosjektet, setter du prosjektstadiet til **Pågår**.</span><span class="sxs-lookup"><span data-stu-id="3985d-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="3985d-150">Opprette et budsjett for et prosjekt</span><span class="sxs-lookup"><span data-stu-id="3985d-150">Create a budget for a project</span></span>

<span data-ttu-id="3985d-151">Budsjettkategoriene brukes til å automatisk beregne fakturabeløpene for arbeidsprosenten som er fullført for hver kategori.</span><span class="sxs-lookup"><span data-stu-id="3985d-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="3985d-152">Følg disse trinnene for å opprette budsjettkategorier for de estimerte kostnadene.</span><span class="sxs-lookup"><span data-stu-id="3985d-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="3985d-153">Gå til **Prosjektstyring og regnskap** \> **Projekter** \> **Alle prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="3985d-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="3985d-154">Velg og åpne prosjektet du vil bruke, på siden **Alle prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="3985d-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="3985d-155">På **Prosjekter**-siden i handlingsruten, i kategorien **Plan** i **Budsjett**-gruppen klikker du **Prosjektbudsjett** for å opprette et nytt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="3985d-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="3985d-156">Angi en estimert kost for hver kategori i prosjektet på siden **Prosjektbudjett**.</span><span class="sxs-lookup"><span data-stu-id="3985d-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="3985d-157">Opprette faktureringsregler for fremdriftsfakturering</span><span class="sxs-lookup"><span data-stu-id="3985d-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="3985d-158">Gå til **Prosjektstyring og regnskap** \> **Projekter** \> **Prosjektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="3985d-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="3985d-159">På **Prosjektkontrakter**-siden velger du og åpner en prosjektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="3985d-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="3985d-160">Velg **Legg til** på hurtigfanen **Faktureringsregler** på prosjektkontrakt-siden.</span><span class="sxs-lookup"><span data-stu-id="3985d-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="3985d-161">Velg **Fremdrift** på **Faktureringsregel**-siden i **Linjetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3985d-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="3985d-162">Angi totalverdien for kontrakten i feltet **Kontraktverdi** på hurtigfanen **Detaljer om faktureringsregellinje**.</span><span class="sxs-lookup"><span data-stu-id="3985d-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="3985d-163">Velg kategorien som gebyrtransaksjonen skal posteres til, i feltet **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="3985d-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="3985d-164">Velg prosjektet som bruker denne faktureringsregelen, i feltet **Prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="3985d-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="3985d-165">Valgfritt: Tilordne den samme faktureringsregelen til flere prosjekter.</span><span class="sxs-lookup"><span data-stu-id="3985d-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="3985d-166">Velg et prosjekt i delen **Tilgjengelige prosjekter** på hurtigfanen **Prosjekt**, og velg deretter høyre pilknapp for å legge til prosjektet i delen **Valgte prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="3985d-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="3985d-167">Valgfritt: Beregn prosentbeløpet som kunden holder tilbake fra betalinger på en faktura.</span><span class="sxs-lookup"><span data-stu-id="3985d-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="3985d-168">I hurtigfanen **Betingelser for tilbakeholdelse av betaling** velger du finansieringskilden, og deretter angir du tilbakeholdelsesprosenten i **Bevaringsprosent**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3985d-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="3985d-169">Gjenta denne prosedyren for å opprette ytterligere faktureringsregler for prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="3985d-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
