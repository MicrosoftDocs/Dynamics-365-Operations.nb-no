---
title: Legge til eller kopiere leieavtaler (forhåndsversjon)
description: Dette emnet beskriver hvordan du oppretter en ny leieavtale ved å angi informasjon for den i Aktivaleie, eller kopierer informasjon fra en eksisterende leieavtale.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: abbf04d009a4b347792cd8b317e334da2a4cbbee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969609"
---
# <a name="add-or-copy-leases-preview"></a><span data-ttu-id="2f430-103">Legge til eller kopiere leieavtaler (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="2f430-103">Add or copy leases (Preview)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f430-104">Dette emnet forklarer hvordan du oppretter en leieavtale fra grunnen av i Aktivaleie, og hvordan du oppretter en leieavtale ved å kopiere en eksisterende leieavtale.</span><span class="sxs-lookup"><span data-stu-id="2f430-104">This topic explains how to create a lease from scratch in Asset leasing, and also how to create a lease by copying an existing lease.</span></span> <span data-ttu-id="2f430-105">Fremgangsmåten for å opprette en leieavtale fra grunnen av, omfatter å registrere informasjon for den nye leieavtalen og deretter opprette en leieplan.</span><span class="sxs-lookup"><span data-stu-id="2f430-105">The process for creating a lease from scratch involves entering information for the new lease and then creating a lease schedule.</span></span> <span data-ttu-id="2f430-106">Etter at minst én leieavtale er opprettet, kan det være enklere å kopiere informasjonen fra en eksisterende leieavtale og deretter redigere denne informasjonen etter behov for å opprette en ny leieavtale.</span><span class="sxs-lookup"><span data-stu-id="2f430-106">After at least one lease has been set up, you might find it easier to copy the information from an existing lease and then edit that information as you require to create a new lease.</span></span>

## <a name="create-a-lease"></a><span data-ttu-id="2f430-107">Opprette en leieavtale</span><span class="sxs-lookup"><span data-stu-id="2f430-107">Create a lease</span></span>

<span data-ttu-id="2f430-108">Følg disse trinnene for å opprette en leieavtale i Aktivaleie.</span><span class="sxs-lookup"><span data-stu-id="2f430-108">Follow these steps to create a lease in Asset leasing.</span></span>

1. <span data-ttu-id="2f430-109">I handlingsruten på siden **Leiesammendrag** i velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2f430-109">On the **Lease summary** page, on the Action Pane, select **New**.</span></span>
2. <span data-ttu-id="2f430-110">Angi leieavtaleinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="2f430-110">Enter the lease information.</span></span> <span data-ttu-id="2f430-111">Obligatoriske felt har røde kantlinjer.</span><span class="sxs-lookup"><span data-stu-id="2f430-111">Fields that are required have red borders.</span></span>

## <a name="create-a-lease-schedule"></a><span data-ttu-id="2f430-112">Opprette en leieplan</span><span class="sxs-lookup"><span data-stu-id="2f430-112">Create a lease schedule</span></span>

<span data-ttu-id="2f430-113">Når du er ferdig å registrere informasjon for leieavtalen, kan du følge disse trinnene for å opprette en leieplan.</span><span class="sxs-lookup"><span data-stu-id="2f430-113">After you've finished entering information for the lease, follow these steps to create a lease schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="2f430-114">Finansdimensjonene kan endres, avhengig av eventuelle egendefinerte finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="2f430-114">The financial dimensions might change based on any custom financial dimensions.</span></span>

1. <span data-ttu-id="2f430-115">Velg **Opprett tidsplaner** for å generere leietablåene.</span><span class="sxs-lookup"><span data-stu-id="2f430-115">Select **Create schedules** to generate the lease books.</span></span> <span data-ttu-id="2f430-116">Leietablåene inneholder tidsplaner for betaling, nedbetaling, avskrivning og utgift.</span><span class="sxs-lookup"><span data-stu-id="2f430-116">The lease books include the payment, amortization, depreciation, and expense schedules.</span></span>
2. <span data-ttu-id="2f430-117">Hvis du vil ha tilgang til leietablåene og vise nyopprettede tidsplaner, velger du **Tablåer**-fanen.</span><span class="sxs-lookup"><span data-stu-id="2f430-117">To access the lease books and view the newly created schedules, select the **Books** tab.</span></span>

    <span data-ttu-id="2f430-118">Siden **Tablådetaljer** viser hvordan leieavtalen gjøres rede for av tablåene som er tilordnet den.</span><span class="sxs-lookup"><span data-stu-id="2f430-118">The **Book details** page shows how the lease is accounted for by the books that have been allocated to it.</span></span> <span data-ttu-id="2f430-119">Herfra kan du vise leieplanene.</span><span class="sxs-lookup"><span data-stu-id="2f430-119">From here, you can view the lease schedules.</span></span>

    <span data-ttu-id="2f430-120">Betalingsplanen inneholder inndataene fra fanen **Linjer i betalingsplan** på siden **Legg til leieavtale**.</span><span class="sxs-lookup"><span data-stu-id="2f430-120">The payment schedule contains the inputs from the **Payment schedule lines** tab on the **Add lease** page.</span></span> <span data-ttu-id="2f430-121">Du kan fortsatt endre hvert betalingsbeløp og hver variable betaling.</span><span class="sxs-lookup"><span data-stu-id="2f430-121">You can still change each payment amount and variable payment.</span></span> <span data-ttu-id="2f430-122">Leieforpliktelsen beregnes på grunnlag av den endrede betalingsplanen.</span><span class="sxs-lookup"><span data-stu-id="2f430-122">The lease liability is calculated based on the modified payment schedule.</span></span>

4. <span data-ttu-id="2f430-123">Når du er ferdig å se gjennom betalingsplanen, velger du **Bekreft tidsplan**.</span><span class="sxs-lookup"><span data-stu-id="2f430-123">After you've finished reviewing the payment schedule, select **Confirm schedule**.</span></span> <span data-ttu-id="2f430-124">Etter at tidsplanen er bekreftet, er ikke leieavtalen lenger tilgjengelig for redigering.</span><span class="sxs-lookup"><span data-stu-id="2f430-124">After the schedule is confirmed, the lease is no longer available for editing.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2f430-125">Systemet beregner automatisk leieperioden fra linjene i betalingsplanen på siden **Legg til leieavtale**.</span><span class="sxs-lookup"><span data-stu-id="2f430-125">The system automatically calculates the lease term from the payment schedule lines on the **Add lease** page.</span></span>
    >
    > <span data-ttu-id="2f430-126">For å beregne leieperioden i måneder finner systemet differansen mellom startdatoen og sluttdatoen for en bestemt linje i betalingsplanen.</span><span class="sxs-lookup"><span data-stu-id="2f430-126">To calculate the lease term in months, the system finds the difference between the start date and the end date for a specific payment schedule line.</span></span> <span data-ttu-id="2f430-127">Den går deretter videre til neste linje i betalingsplanen og finner differansen på nytt.</span><span class="sxs-lookup"><span data-stu-id="2f430-127">It then moves to the next payment schedule line and finds the difference again.</span></span> <span data-ttu-id="2f430-128">Til slutt summerer systemet alle beløpene for å fastsette leieperioden i måneder.</span><span class="sxs-lookup"><span data-stu-id="2f430-128">Finally, the system sums all the amounts to determine the lease term in months.</span></span>

5. <span data-ttu-id="2f430-129">Hvis du vil vise de beregnede renteutgiftene for perioden, åpner du siden **Nedbetalingsplan for gjeld**.</span><span class="sxs-lookup"><span data-stu-id="2f430-129">To view the calculated period interest expenses, open the **Liability amortization schedule** page.</span></span> <span data-ttu-id="2f430-130">Hvis du vil vise beregnet lineær avskrivning, åpner du siden **Avskrivningsplan for aktiva**.</span><span class="sxs-lookup"><span data-stu-id="2f430-130">To view calculated straight-line depreciation, open the **Asset depreciation schedule** page.</span></span>
6. <span data-ttu-id="2f430-131">Når du er ferdig å se gjennom det beregnede beløpet, kan du opprette journaloppføringen for opprinnelig føring på siden **Opprinnelig føring**.</span><span class="sxs-lookup"><span data-stu-id="2f430-131">After you've finished reviewing the calculated amount, you can create the initial recognition journal entry on the **Initial recognition** page.</span></span> <span data-ttu-id="2f430-132">Du får en melding om at journalen er opprettet.</span><span class="sxs-lookup"><span data-stu-id="2f430-132">You receive a message that states that the journal has been created.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2f430-133">Journaloppføringen posteres ikke i Økonomimodul før du posterer oppføringen manuelt.</span><span class="sxs-lookup"><span data-stu-id="2f430-133">The journal entry isn't posted to General ledger until you manually post the entry.</span></span>

7. <span data-ttu-id="2f430-134">Hvis du vil se gjennom den foreslåtte oppføringen for opprinnelig føring før du posterer den, velger du **Journal for aktivaleie**.</span><span class="sxs-lookup"><span data-stu-id="2f430-134">To review the proposed initial recognition entry before you post it, select **Asset leasing journal**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2f430-135">Du kan ikke opprette journalen for aktivaleie manuelt.</span><span class="sxs-lookup"><span data-stu-id="2f430-135">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="2f430-136">Den blir automatisk opprettet når leieplaner opprettes.</span><span class="sxs-lookup"><span data-stu-id="2f430-136">It's automatically created when lease schedules are created.</span></span>

8. <span data-ttu-id="2f430-137">Når du er ferdig å se gjennom journaloppføringen for opprinnelig føring og er klar til å postere den, velger du **Poster** for å føre bruksrettseiendelen og leieforpliktelsen i Økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="2f430-137">When you've finished reviewing the initial recognition journal entry and are ready to post it, select **Post** to recognize the right-of-use (ROU) asset and lease liability in General ledger.</span></span>

## <a name="copy-a-lease"></a><span data-ttu-id="2f430-138">Kopiere en leieavtale</span><span class="sxs-lookup"><span data-stu-id="2f430-138">Copy a lease</span></span>

<span data-ttu-id="2f430-139">Aktivaleie lar deg kopiere detaljene for en leieavtale for å opprette en ny leieavtale med samme informasjon.</span><span class="sxs-lookup"><span data-stu-id="2f430-139">Asset leasing lets you copy the details of a lease to create a new lease that has the same information.</span></span> <span data-ttu-id="2f430-140">Du kan deretter endre leieavtalefeltene før du oppretter tidsplanene for den kopierte leieavtalen.</span><span class="sxs-lookup"><span data-stu-id="2f430-140">You can then change the lease fields before you create the schedules for the copied lease.</span></span>

1. <span data-ttu-id="2f430-141">På siden **Leiesammendrag** velger du leieavtalen du vil kopiere, og deretter velger du **Kopier leieavtale** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2f430-141">On the **Lease summary** page, select the lease to copy, and then, on the Action Pane, select **Copy lease**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2f430-142">Hvis parameteren **Manuell** er deaktivert for nummerserien for leie-ID-er, genereres neste nummer i serien automatisk som leie-ID-en til den kopierte leieavtalen.</span><span class="sxs-lookup"><span data-stu-id="2f430-142">If the **Manual** parameter is turned off for the number sequence for lease IDs, the next number in the sequence is automatically generated as the lease ID of the copied lease.</span></span> <span data-ttu-id="2f430-143">Hvis parameteren **Manuell** er aktivert, får du en melding der du blir bedt om å angi leie-ID-en før du kopierer leieavtalen.</span><span class="sxs-lookup"><span data-stu-id="2f430-143">If the **Manual** parameter is turned on, you receive a message that prompts you to enter the lease ID before you proceed to copy the lease.</span></span>

2. <span data-ttu-id="2f430-144">Velg **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="2f430-144">Select **Copy**.</span></span> <span data-ttu-id="2f430-145">Leieavtaledetaljene fra den valgte leieavtalen kopieres til en ny leieavtale.</span><span class="sxs-lookup"><span data-stu-id="2f430-145">The lease details from the selected lease are copied to a new lease.</span></span> <span data-ttu-id="2f430-146">Du kan deretter redigere detaljene i den nye leieavtalen før du lagrer den og oppretter leieplanene.</span><span class="sxs-lookup"><span data-stu-id="2f430-146">You can then edit the details of the new lease before you save it and create the lease schedules.</span></span>

## <a name="asset-leasing-journal"></a><span data-ttu-id="2f430-147">Journal for aktivaleie</span><span class="sxs-lookup"><span data-stu-id="2f430-147">Asset leasing journal</span></span>

<span data-ttu-id="2f430-148">Alle journaloppføringer som opprettes i Aktivaleie, befinner seg i journalen for aktivaleie.</span><span class="sxs-lookup"><span data-stu-id="2f430-148">All journal entries that are created in Asset leasing are contained in the Asset leasing journal.</span></span> <span data-ttu-id="2f430-149">På siden **Journal for aktivaleie** (**Aktivaleie \> Journaloppføringer \> Journal for aktivaleie**) kan du filtrere etter posteringsstatus, vise bestemte journaloppføringer og bilagene og postere uposterte journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="2f430-149">On the **Asset leasing journal** page (**Asset leasing \> Journal entries \> Asset leasing journal**), you can filter by posting status, view specific journal entries and the vouchers, and post unposted journal entries.</span></span>

> [!NOTE]
> <span data-ttu-id="2f430-150">Du kan ikke opprette journalen for aktivaleie manuelt.</span><span class="sxs-lookup"><span data-stu-id="2f430-150">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="2f430-151">Den blir automatisk opprettet når leieplaner opprettes.</span><span class="sxs-lookup"><span data-stu-id="2f430-151">It's automatically created when lease schedules are created.</span></span>
