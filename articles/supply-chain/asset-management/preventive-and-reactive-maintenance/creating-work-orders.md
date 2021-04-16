---
title: Opprette arbeidsordrer
description: Dette emnet forklarer hvordan du oppretter arbeidsordrer i Aktivastyring.
author: johanhoffmann
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 3982232e5008d6f8c283d6cecfaf2fa6e66150a1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836740"
---
# <a name="creating-work-orders"></a><span data-ttu-id="b72b0-103">Opprette arbeidsordrer</span><span class="sxs-lookup"><span data-stu-id="b72b0-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b72b0-104">Etter at du har planlagt forebyggende vedlikeholdsjobber, er neste trinn å opprette arbeidsordrer for dem.</span><span class="sxs-lookup"><span data-stu-id="b72b0-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="b72b0-105">Du kan fullføre dette trinnet ved å bruke en av vedlikeholdsplanene.</span><span class="sxs-lookup"><span data-stu-id="b72b0-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="b72b0-106">De planlagte jobbene i en vedlikeholdsplan kan ha forskjellige referansetyper, som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="b72b0-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="b72b0-107">Referansetype</span><span class="sxs-lookup"><span data-stu-id="b72b0-107">Reference type</span></span> | <span data-ttu-id="b72b0-108">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b72b0-108">Description</span></span> |
|---|---|
| <span data-ttu-id="b72b0-109">Vedlikeholdsplaner</span><span class="sxs-lookup"><span data-stu-id="b72b0-109">Maintenance plans</span></span> | <span data-ttu-id="b72b0-110">Forebyggende vedlikeholdsjobber som er basert på vedlikeholdsplantypen *Tid* eller *Teller*.</span><span class="sxs-lookup"><span data-stu-id="b72b0-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="b72b0-111">Vedlikeholdsrunder</span><span class="sxs-lookup"><span data-stu-id="b72b0-111">Maintenance rounds</span></span> | <span data-ttu-id="b72b0-112">Forebyggende vedlikeholdsjobber som inneholder flere aktiva som krever en lignende type vedlikehold.</span><span class="sxs-lookup"><span data-stu-id="b72b0-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="b72b0-113">Melding</span><span class="sxs-lookup"><span data-stu-id="b72b0-113">Maintenance request</span></span> | <span data-ttu-id="b72b0-114">En manuelt opprettet forespørsel om vedlikehold eller reparasjon av et aktivum.</span><span class="sxs-lookup"><span data-stu-id="b72b0-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="b72b0-115">Denne forespørselen kan konverteres til en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="b72b0-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="b72b0-116">Opprette arbeidsordrer basert på vedlikeholdsplanen</span><span class="sxs-lookup"><span data-stu-id="b72b0-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="b72b0-117">Følg denne fremgangsmåten for å opprette arbeidsordrer som er basert på vedlikeholdsplanen.</span><span class="sxs-lookup"><span data-stu-id="b72b0-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="b72b0-118">Åpne en av følgende sider, avhengig av hvordan du vil planlegge varer for arbeidsordrene:</span><span class="sxs-lookup"><span data-stu-id="b72b0-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="b72b0-119">Alle vedlikeholdsplaner (**Aktivastyring \> Styringsplan \> Alle vedlikeholdsplaner**)</span><span class="sxs-lookup"><span data-stu-id="b72b0-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="b72b0-120">Åpne vedlikeholdsplanlinjer (**Aktivastyring \> Styringsplan \> Åpne vedlikeholdsplanlinjer**)</span><span class="sxs-lookup"><span data-stu-id="b72b0-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="b72b0-121">Åpne vedlikeholdsplanpuljer (**Aktivastyring \> Styringsplan \> Åpne vedlikeholdsplanpuljer**)</span><span class="sxs-lookup"><span data-stu-id="b72b0-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="b72b0-122">Merk av for hver planlagte vedlikeholdsjobb du vil opprette en arbeidsordre for, i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="b72b0-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="b72b0-123">Velg deretter **Arbeidsordre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b72b0-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="b72b0-124">Dialogboksen **Opprett arbeidsordrer** vises.</span><span class="sxs-lookup"><span data-stu-id="b72b0-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="b72b0-125">Det totale antallet prognosetimer for de valgte linjene vises i feltet **Vedlikeholdsprognosetimer**.</span><span class="sxs-lookup"><span data-stu-id="b72b0-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![Dialogboksen Opprett arbeidsordrer](media/18-preventive-maintenance.png)

1. <span data-ttu-id="b72b0-127">I **Parametere**-delen angir du antall arbeidsordrer som skal opprettes.</span><span class="sxs-lookup"><span data-stu-id="b72b0-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="b72b0-128">Velg ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="b72b0-128">Select one of the following options:</span></span>

    - <span data-ttu-id="b72b0-129">**Én arbeidsordre per linje** – Opprett én arbeidsordre per vedlikeholdsplanlinje.</span><span class="sxs-lookup"><span data-stu-id="b72b0-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="b72b0-130">**Én arbeidsordre per** – Opprett arbeidsordrer som grupperes i henhold til innstillingene for de andre alternativene som blir tilgjengelige når du velger dette alternativet.</span><span class="sxs-lookup"><span data-stu-id="b72b0-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="b72b0-131">I feltet **Arbeidsordretype** velger du arbeidsordretypen som skal brukes for alle arbeidsordrene du oppretter.</span><span class="sxs-lookup"><span data-stu-id="b72b0-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="b72b0-132">Velg **OK** for å opprette arbeidsordrene i henhold til innstillingene.</span><span class="sxs-lookup"><span data-stu-id="b72b0-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="b72b0-133">Gruppere arbeidsordrelinjer som opprettes automatisk mens en vedlikeholdsplan kjører</span><span class="sxs-lookup"><span data-stu-id="b72b0-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

<span data-ttu-id="b72b0-134">Med denne funksjonen kan du definere regler for gruppering av arbeidsordrelinjer under én arbeidsordre når systemet er konfigurert slik at det genererer arbeidsordrer automatisk, basert på en vedlikeholdsplan.</span><span class="sxs-lookup"><span data-stu-id="b72b0-134">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="b72b0-135">Tidligere kunne automatisk genererte arbeidsordrer bare inneholde én linje.</span><span class="sxs-lookup"><span data-stu-id="b72b0-135">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="b72b0-136">Nå kan du imidlertid gruppere arbeidsordrer etter for eksempel aktiva, aktivatype eller funksjonslokasjon.</span><span class="sxs-lookup"><span data-stu-id="b72b0-136">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="b72b0-137">(Manuelt genererte arbeidsordrer kan allerede grupperes på denne måten, som beskrevet i den forrige delen i dette emnet.)</span><span class="sxs-lookup"><span data-stu-id="b72b0-137">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="b72b0-138">Aktivere gruppering for automatisk genererte arbeidsordrer</span><span class="sxs-lookup"><span data-stu-id="b72b0-138">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="b72b0-139">Før du kan bruke denne funksjonen, må den være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="b72b0-139">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="b72b0-140">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den.</span><span class="sxs-lookup"><span data-stu-id="b72b0-140">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="b72b0-141">I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="b72b0-141">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b72b0-142">**Modul:** *Aktivastyring*</span><span class="sxs-lookup"><span data-stu-id="b72b0-142">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="b72b0-143">**Funksjonsnavn:** *Bruk regler for gruppering av arbeidsordrer mens en vedlikeholdsplan kjører*</span><span class="sxs-lookup"><span data-stu-id="b72b0-143">**Feature name:** *Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="b72b0-144">Konfigurere gruppering for automatisk genererte arbeidsordrer</span><span class="sxs-lookup"><span data-stu-id="b72b0-144">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="b72b0-145">Følg denne fremgangsmåten for å konfigurere gruppering for automatisk genererte arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="b72b0-145">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="b72b0-146">Gå til **Aktivastyring \> Oppsett \> Forebyggende vedlikehold \> Vedlikeholdsplaner**.</span><span class="sxs-lookup"><span data-stu-id="b72b0-146">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="b72b0-147">Følg denne fremgangsmåten for hver plan der du vil generere grupperte arbeidsordrer:</span><span class="sxs-lookup"><span data-stu-id="b72b0-147">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="b72b0-148">Velg planen i listeruten.</span><span class="sxs-lookup"><span data-stu-id="b72b0-148">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="b72b0-149">Kontroller at det er merket av for **Opprett automatisk** på hver linje i hurtigfanen **Linje**.</span><span class="sxs-lookup"><span data-stu-id="b72b0-149">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="b72b0-150">Gå til **Aktivastyring \> Periodisk \> Forebyggende vedlikehold \> Planlegg vedlikeholdsplaner**.</span><span class="sxs-lookup"><span data-stu-id="b72b0-150">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="b72b0-151">Angi tidshorisonten for planen (hvor langt fremover du skal se når du finner planlagte vedlikeholdsjobber du skal generere arbeid for) i **Periode**-delen i dialogboksen **Planlegg vedlikeholdsplaner**.</span><span class="sxs-lookup"><span data-stu-id="b72b0-151">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="b72b0-152">Angi *Ja* for alternativet **Opprett arbeidsordre fra plan automatisk**.</span><span class="sxs-lookup"><span data-stu-id="b72b0-152">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="b72b0-153">Velg ett av følgende alternativer i delen **Arbeidsordre**:</span><span class="sxs-lookup"><span data-stu-id="b72b0-153">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="b72b0-154">**Én arbeidsordre per linje** – Opprett én arbeidsordre per vedlikeholdsplanlinje.</span><span class="sxs-lookup"><span data-stu-id="b72b0-154">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="b72b0-155">(Dette alternativet gir samme funksjonalitet som er tilgjengelig når funksjonen *Bruk regler for gruppering av arbeidsordrer mens en vedlikeholdsplan kjører* er deaktivert.)</span><span class="sxs-lookup"><span data-stu-id="b72b0-155">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="b72b0-156">**Én arbeidsordre per** – Opprett arbeidsordrer som grupperes i henhold til innstillingene for de andre alternativene som blir tilgjengelige når du velger dette alternativet.</span><span class="sxs-lookup"><span data-stu-id="b72b0-156">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="b72b0-157">Hvis du vil at alternativene skal brukes når du bare kjører noen av vedlikeholdsplanene, legger du til filtre etter behov i hurtigfanen **Poster som skal inkluderes**, slik du kan gjøre for andre satsvise jobber i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b72b0-157">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="b72b0-158">Konfigurer alternativer for satsvise jobber og planlegging etter behov i hurtigfanen **Kjør i bakgrunnen**, slik du kan gjøre for andre satsvise jobber i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b72b0-158">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="b72b0-159">Velg **OK** for å kjøre og/eller planlegge de valgte vedlikeholdsplanene.</span><span class="sxs-lookup"><span data-stu-id="b72b0-159">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]