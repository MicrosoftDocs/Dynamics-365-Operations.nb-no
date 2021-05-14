---
title: Opprette og behandle avvik
description: Dette emnet beskriver hvordan du utfører behandling av avvik, basert på en eksisterende kvalitetsordre.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956212"
---
# <a name="create-and-process-nonconformances"></a><span data-ttu-id="014e4-103">Opprette og behandle avvik</span><span class="sxs-lookup"><span data-stu-id="014e4-103">Create and process nonconformances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="014e4-104">Dette emnet beskriver hvordan du utfører behandling av avvik, basert på en eksisterende kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="014e4-104">This topic describes how to perform nonconformance management based on an existing quality order.</span></span> <span data-ttu-id="014e4-105">Avviksbehandling utføres vanligvis av en kvalitetsassistent.</span><span class="sxs-lookup"><span data-stu-id="014e4-105">Typically, nonconformance management is done by a quality clerk.</span></span> <span data-ttu-id="014e4-106">Det er en forutsetning at du har en tilgjengelig kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="014e4-106">As a prerequisite, you must have a quality order available.</span></span> <span data-ttu-id="014e4-107">(Hvis du vil ha informasjon om hvordan du oppretter en kvalitetsordre, kan du se [Inspisere kvaliteten på varer](inspect-quality-goods.md).)</span><span class="sxs-lookup"><span data-stu-id="014e4-107">(For information about how to create a quality order, see [Inspect the quality of goods](inspect-quality-goods.md).)</span></span>

<span data-ttu-id="014e4-108">Før en bruker kan behandle godkjenningen av et avvik, må en arbeider tilordnes dem i **Person**-feltet på **Brukere**-siden.</span><span class="sxs-lookup"><span data-stu-id="014e4-108">Before a user can process the approval of a nonconformance, a worker must be assigned to them in the **Person** field on the **Users** page.</span></span> <span data-ttu-id="014e4-109">Før brukeren kan bruke dokumentnotatene, må alternativet **Aktiver dokumentoversikt** være satt til *Ja* i brukeralternativene.</span><span class="sxs-lookup"><span data-stu-id="014e4-109">Additionally, before the user can use the document notes, the **Enable document handling** option must be set to *Yes* in their user options.</span></span>

## <a name="create-a-nonconformance"></a><span data-ttu-id="014e4-110">Opprette et avvik</span><span class="sxs-lookup"><span data-stu-id="014e4-110">Create a nonconformance</span></span>

<span data-ttu-id="014e4-111">Hvis du vil opprette et avvik, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="014e4-111">To create a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="014e4-112">Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Avvik**.</span><span class="sxs-lookup"><span data-stu-id="014e4-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="014e4-113">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="014e4-113">On the Action pane, select **New**.</span></span>
1. <span data-ttu-id="014e4-114">Velg problemtypen som ble funnet under inspeksjonsprosessen, i **Problemtype**-feltet i dialogboksen **Opprett avvik**.</span><span class="sxs-lookup"><span data-stu-id="014e4-114">In the **Create non conformance** dialog box, in **Problem type** field, select the type of problem that was found during the inspection process.</span></span>
1. <span data-ttu-id="014e4-115">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="014e4-115">Select **OK**.</span></span>

## <a name="approve-or-reject-a-nonconformance"></a><span data-ttu-id="014e4-116">Godkjenne eller avvise et avvik</span><span class="sxs-lookup"><span data-stu-id="014e4-116">Approve or reject a nonconformance</span></span>

<span data-ttu-id="014e4-117">Hvis du vil godkjenne eller avvise et avvik, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="014e4-117">To approve or reject a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="014e4-118">Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Avvik**.</span><span class="sxs-lookup"><span data-stu-id="014e4-118">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="014e4-119">Velg avviket du vil oppdatere, i listen.</span><span class="sxs-lookup"><span data-stu-id="014e4-119">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="014e4-120">Du kan bare legge til en rettelse i avvik som er godkjent.</span><span class="sxs-lookup"><span data-stu-id="014e4-120">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="014e4-121">Velg **Funksjoner \> Godkjenn avvik** i handlingsruten for å godkjenne avviket, eller **Funksjoner \> Avvis avvik** for å avvise det.</span><span class="sxs-lookup"><span data-stu-id="014e4-121">On the Action Pane, select **Functions \> Approve non conformance** to approve the nonconformance or **Functions \> Refuse non conformance** to reject it.</span></span> <span data-ttu-id="014e4-122">Du kan knytte godkjente avvik til [relaterte operasjoner](../quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="014e4-122">You can associate approved nonconformances with [related operations](../quality-operations.md).</span></span> <span data-ttu-id="014e4-123">På denne måten kan du registrere arbeid som er utført som en del av avvikshåndteringen og behandlingen av rettelsesbehandling.</span><span class="sxs-lookup"><span data-stu-id="014e4-123">In this way, you can record work that is done as part of the nonconformance handling and the processing of correction handling.</span></span>
1. <span data-ttu-id="014e4-124">Du blir bedt om å bekrefte valget.</span><span class="sxs-lookup"><span data-stu-id="014e4-124">You're prompted to confirm your selection.</span></span> <span data-ttu-id="014e4-125">Klikk på **Ja** for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="014e4-125">Select **Yes** to continue.</span></span>

## <a name="add-operations-and-other-details-to-nonconformances"></a><span data-ttu-id="014e4-126">Legge til operasjoner og andre detaljer i avvik</span><span class="sxs-lookup"><span data-stu-id="014e4-126">Add operations and other details to nonconformances</span></span>

<span data-ttu-id="014e4-127">Når du har opprettet et avvik, kan du begynne å legge til tilknyttede operasjoner og angi tilleggsinformasjon om disse operasjonene.</span><span class="sxs-lookup"><span data-stu-id="014e4-127">After you've created a nonconformance, you can start to add related operations and specify additional information about those operations.</span></span> <span data-ttu-id="014e4-128">Du kan bare legge til relaterte operasjoner i avvik som er godkjent.</span><span class="sxs-lookup"><span data-stu-id="014e4-128">You can add related operations only to nonconformances that are approved.</span></span>

<span data-ttu-id="014e4-129">I tillegg til den grunnleggende informasjonen kan du legge til følgende detaljer i en operasjon:</span><span class="sxs-lookup"><span data-stu-id="014e4-129">Besides the basic information, you can add the following details to an operation:</span></span>

- <span data-ttu-id="014e4-130">**Varer** – Du kan opprette en liste over varer som forbrukes for å utføre rettelsen.</span><span class="sxs-lookup"><span data-stu-id="014e4-130">**Items** – You can create a list of items that are consumed to perform the correction.</span></span> <span data-ttu-id="014e4-131">Varene kan for eksempel være produkter som kreves for å reparere utstyr eller ingredienser som kreves for å omarbeide et ferdig produkt.</span><span class="sxs-lookup"><span data-stu-id="014e4-131">For example, the items might be products that are required to repair equipment or ingredients that are required to rework a finished product.</span></span>
- <span data-ttu-id="014e4-132">**Kvalitetsstyringstillegg** – Du kan opprette en liste over tillegg som påløper eller faktureres eksterne kilder.</span><span class="sxs-lookup"><span data-stu-id="014e4-132">**Quality charges** – You can create a list of charges that are incurred or billed out to external sources.</span></span>
- <span data-ttu-id="014e4-133">**Timeregistrering** – Du kan opprette en logg over tiden som hver arbeider bruker på operasjonen.</span><span class="sxs-lookup"><span data-stu-id="014e4-133">**Timesheet** – You can create a log of the time that each worker spends on the operation.</span></span>

<span data-ttu-id="014e4-134">De gjenværende innstillingene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="014e4-134">The remaining settings are optional.</span></span> <span data-ttu-id="014e4-135">Kostnaden for hver vare, kvalitetsgebyr og timeregistreringen summeres og vises på operasjonen.</span><span class="sxs-lookup"><span data-stu-id="014e4-135">The cost for each item, quality charges, and the timesheet are summed and shown on the operation.</span></span> <span data-ttu-id="014e4-136">Du kan ikke redigere **Kostnad**-feltet direkte på operasjonen.</span><span class="sxs-lookup"><span data-stu-id="014e4-136">You can't directly edit the **Cost** field on the operation.</span></span>

### <a name="create-an-operation-for-a-nonconformance"></a><span data-ttu-id="014e4-137">Opprette en operasjon for et avvik</span><span class="sxs-lookup"><span data-stu-id="014e4-137">Create an operation for a nonconformance</span></span>

<span data-ttu-id="014e4-138">Hvis du vil opprette en operasjon for et avvik, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="014e4-138">To create an operation for a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="014e4-139">Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Avvik**.</span><span class="sxs-lookup"><span data-stu-id="014e4-139">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="014e4-140">Velg avviket du vil oppdatere, i listen.</span><span class="sxs-lookup"><span data-stu-id="014e4-140">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="014e4-141">Du kan bare legge til eller opprette operasjoner i avvik som er godkjent.</span><span class="sxs-lookup"><span data-stu-id="014e4-141">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="014e4-142">I handlingsruten velger du **Relaterte operasjoner**.</span><span class="sxs-lookup"><span data-stu-id="014e4-142">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="014e4-143">Velg **Ny** i handlingsruten på siden **Relaterte operasjoner** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="014e4-143">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="014e4-144">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="014e4-144">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="014e4-145">**Operasjon** – Velg koden for operasjonen som skal utføres for avviket.</span><span class="sxs-lookup"><span data-stu-id="014e4-145">**Operation** – Select the code of the operation that will be performed for the nonconformance.</span></span>
    - <span data-ttu-id="014e4-146">**Årsak** – Angi en detaljert beskrivelse som forklarer hvorfor operasjonen er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="014e4-146">**Reason** – Enter a detailed description that explains why the operation is required.</span></span>
    - <span data-ttu-id="014e4-147">**Salgsordre** – Hvis den valgte operasjonskoden er knyttet til salgsordretypen, velger du salgsordren du kobler operasjonen til.</span><span class="sxs-lookup"><span data-stu-id="014e4-147">**Sales order** – If the selected operation code is related to the sales order type, select the sales order that you're linking the operation to.</span></span>
    - <span data-ttu-id="014e4-148">**Bestilling** – Hvis den valgte operasjonskoden er knyttet til bestillingstypen, velger du bestillingen du kobler operasjonen til.</span><span class="sxs-lookup"><span data-stu-id="014e4-148">**Purchase order** – If the selected operation code is related to the purchase order type, select the purchase order that you're linking the operation to.</span></span>

1. <span data-ttu-id="014e4-149">Lukk sidene.</span><span class="sxs-lookup"><span data-stu-id="014e4-149">Close the pages.</span></span>

### <a name="add-items-to-an-operation"></a><span data-ttu-id="014e4-150">Legge til varer i en operasjon</span><span class="sxs-lookup"><span data-stu-id="014e4-150">Add items to an operation</span></span>

<span data-ttu-id="014e4-151">Følg denne fremgangsmåten for å legge til varer i en operasjon.</span><span class="sxs-lookup"><span data-stu-id="014e4-151">To add items to an operation, follow these steps.</span></span>

1. <span data-ttu-id="014e4-152">Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Avvik**.</span><span class="sxs-lookup"><span data-stu-id="014e4-152">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="014e4-153">Velg avviket du vil oppdatere, i listen.</span><span class="sxs-lookup"><span data-stu-id="014e4-153">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="014e4-154">Du kan bare legge til eller opprette operasjoner i avvik som er godkjent.</span><span class="sxs-lookup"><span data-stu-id="014e4-154">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="014e4-155">I handlingsruten velger du **Relaterte operasjoner**.</span><span class="sxs-lookup"><span data-stu-id="014e4-155">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="014e4-156">På siden **Relaterte operasjoner** velger du operasjonen du vil legge til varer i.</span><span class="sxs-lookup"><span data-stu-id="014e4-156">On the **Related operations** page, select the operation that you want to add items to.</span></span>
1. <span data-ttu-id="014e4-157">Velg **Varer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="014e4-157">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="014e4-158">Velg **Ny** i handlingsruten på siden **Relaterte operasjoner** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="014e4-158">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="014e4-159">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="014e4-159">Then set the following fields for new row:</span></span>

    - <span data-ttu-id="014e4-160">**Varenummer** – Velg produktet som skal forbrukes som del av den valgte operasjonen.</span><span class="sxs-lookup"><span data-stu-id="014e4-160">**Item number** – Select the product that will be consumed as part of the selected operation.</span></span>
    - <span data-ttu-id="014e4-161">**Antall** – Angi antall varer som skal forbrukes.</span><span class="sxs-lookup"><span data-stu-id="014e4-161">**Quantity** – Enter the number of items that will be consumed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="014e4-162">Du kan vise kostnaden for varen i feltet **Kostnad** i kategorien **Generelt**. Kostnaden som vises der, kommer fra kostnaden som er definert på **Frigitt produkt**-siden.</span><span class="sxs-lookup"><span data-stu-id="014e4-162">You can view the cost for the item in the **Cost** field on the **General** tab. The cost that is shown there comes from the cost that is set up on the **Released product** page.</span></span> <span data-ttu-id="014e4-163">Kostnaden kan ikke oppdateres direkte på siden **Relatert operasjonsvare**.</span><span class="sxs-lookup"><span data-stu-id="014e4-163">The cost can't be updated directly on the **Related operation item** page.</span></span> <span data-ttu-id="014e4-164">Kostnadene for alle varer som legges til på siden **Relaterte operasjonsvarer**, legges automatisk til i **Kostnad**-feltet på **Relaterte operasjoner**-siden.</span><span class="sxs-lookup"><span data-stu-id="014e4-164">The cost of all items that are added on the **Related operation items** page is automatically added to the **Cost** field on the **Related operations** page.</span></span>

1. <span data-ttu-id="014e4-165">Gjenta det forrige trinnet for hver tilleggsvare du må legge til.</span><span class="sxs-lookup"><span data-stu-id="014e4-165">Repeat the previous step for each additional item that you must add.</span></span>
1. <span data-ttu-id="014e4-166">Lukk sidene.</span><span class="sxs-lookup"><span data-stu-id="014e4-166">Close the pages.</span></span>

### <a name="add-quality-charges-to-an-operation"></a><span data-ttu-id="014e4-167">Legge til kvalitetsgebyrer i en operasjon</span><span class="sxs-lookup"><span data-stu-id="014e4-167">Add quality charges to an operation</span></span>

<span data-ttu-id="014e4-168">Følg denne fremgangsmåten for å legge til kvalitetsstyringstillegg i en operasjon.</span><span class="sxs-lookup"><span data-stu-id="014e4-168">To add quality charges to an operation, follow these steps.</span></span>

1. <span data-ttu-id="014e4-169">Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Avvik**.</span><span class="sxs-lookup"><span data-stu-id="014e4-169">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="014e4-170">Velg avviket du vil oppdatere, i listen.</span><span class="sxs-lookup"><span data-stu-id="014e4-170">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="014e4-171">Du kan bare legge til eller opprette operasjoner i avvik som er godkjent.</span><span class="sxs-lookup"><span data-stu-id="014e4-171">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="014e4-172">I handlingsruten velger du **Relaterte operasjoner**.</span><span class="sxs-lookup"><span data-stu-id="014e4-172">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="014e4-173">På siden **Relaterte operasjoner** velger du operasjonen du vil legge til kvalitetsstyringstillegg i.</span><span class="sxs-lookup"><span data-stu-id="014e4-173">On the **Related operations** page, select the operation that you want to add quality charges to.</span></span>
1. <span data-ttu-id="014e4-174">I handlingsruten velger du **Kvalitetsstyringstillegg**.</span><span class="sxs-lookup"><span data-stu-id="014e4-174">On the Action Pane, select **Quality charges**.</span></span>
1. <span data-ttu-id="014e4-175">Velg **Ny** i handlingsruten på siden **Relaterte operasjonstillegg** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="014e4-175">On the **Related operation charges** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="014e4-176">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="014e4-176">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="014e4-177">**Tilleggskode** – Velg kvalitetstillegget du vil legge til.</span><span class="sxs-lookup"><span data-stu-id="014e4-177">**Charges code** – Select the quality charge that you want to add.</span></span>
    - <span data-ttu-id="014e4-178">**Beskrivelse** – Angi en detaljert beskrivelse av tillegget.</span><span class="sxs-lookup"><span data-stu-id="014e4-178">**Description** – Enter a detailed description of the charge.</span></span>
    - <span data-ttu-id="014e4-179">**Gebyrverdi** – Angi gebyrbeløpet.</span><span class="sxs-lookup"><span data-stu-id="014e4-179">**Charges value** – Enter the amount of the charge.</span></span>

1. <span data-ttu-id="014e4-180">Gjenta det forrige trinnet for hvert tilleggsgebyr du må legge til.</span><span class="sxs-lookup"><span data-stu-id="014e4-180">Repeat the previous step for each additional charge that you must add.</span></span>
1. <span data-ttu-id="014e4-181">Lukk sidene.</span><span class="sxs-lookup"><span data-stu-id="014e4-181">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="014e4-182">Beløpet i feltet **Gebyrverdi** summeres automatisk for alle kvalitetstillegg, og legges til andre beløp i **Kostnad**-feltet på siden **Relaterte operasjoner**.</span><span class="sxs-lookup"><span data-stu-id="014e4-182">The amount in the **Charges value** field is automatically summed for all quality charges and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

### <a name="create-a-timesheet-on-an-operation"></a><span data-ttu-id="014e4-183">Opprette en timeregistrering for en operasjon</span><span class="sxs-lookup"><span data-stu-id="014e4-183">Create a timesheet on an operation</span></span>

<span data-ttu-id="014e4-184">Følg denne fremgangsmåten for å legge til en timeregistrering i en operasjon.</span><span class="sxs-lookup"><span data-stu-id="014e4-184">To add a timesheet to an operation, follow these steps.</span></span>

1. <span data-ttu-id="014e4-185">Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Avvik**.</span><span class="sxs-lookup"><span data-stu-id="014e4-185">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="014e4-186">Velg avviket du vil oppdatere, i listen.</span><span class="sxs-lookup"><span data-stu-id="014e4-186">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="014e4-187">Du kan bare legge til eller opprette operasjoner i avvik som er godkjent.</span><span class="sxs-lookup"><span data-stu-id="014e4-187">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="014e4-188">I handlingsruten velger du **Relaterte operasjoner**.</span><span class="sxs-lookup"><span data-stu-id="014e4-188">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="014e4-189">På siden **Relaterte operasjoner** velger du operasjonen du vil legge til en timeregistrering i.</span><span class="sxs-lookup"><span data-stu-id="014e4-189">On the **Related operations** page, select the operation that you want to add a timesheet to.</span></span>
1. <span data-ttu-id="014e4-190">Velg **Timeregistrering** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="014e4-190">On the Action Pane, select **Timesheet**.</span></span>
1. <span data-ttu-id="014e4-191">Velg **Ny** i handlingsruten på siden **Relaterte operasjonstimeregistreringer** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="014e4-191">On the **Related operation time sheets** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="014e4-192">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="014e4-192">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="014e4-193">**Dato** – Angi datoen da arbeidet ble utført.</span><span class="sxs-lookup"><span data-stu-id="014e4-193">**Date** – Specify the date when work was done.</span></span> <span data-ttu-id="014e4-194">Som standard settes feltet til gjeldende dato.</span><span class="sxs-lookup"><span data-stu-id="014e4-194">By default, this field is set to the current date.</span></span>
    - <span data-ttu-id="014e4-195">**Arbeider** – Velg arbeideren som utførte arbeidet.</span><span class="sxs-lookup"><span data-stu-id="014e4-195">**Worker** – Select the worker who did the work.</span></span> <span data-ttu-id="014e4-196">Som standard er dette feltet satt til den arbeideren som er tilordnet den gjeldende brukeren.</span><span class="sxs-lookup"><span data-stu-id="014e4-196">By default, this field is set to the worker that is assigned to the current user.</span></span>
    - <span data-ttu-id="014e4-197">**Operasjonstimer** – Angi antall timer som ble arbeidet på den valgte operasjonen.</span><span class="sxs-lookup"><span data-stu-id="014e4-197">**Operation hours** – Enter the number of hours that were worked on the selected operation.</span></span>
    - <span data-ttu-id="014e4-198">**Fakturert** – Merk av i denne avmerkingsboksen hvis tiden er belastet en kunde eller leverandør på en faktura.</span><span class="sxs-lookup"><span data-stu-id="014e4-198">**Invoiced** – Select this check box if the time has been charged to a customer or vendor on an invoice.</span></span>

    > [!NOTE]
    > <span data-ttu-id="014e4-199">Du kan vise kostnaden i **Kostnad**-feltet i kategorien **Generelt**. Kostnaden beregnes ved å bruke satsen du definerer på siden **Lagerstyringsparametere**.</span><span class="sxs-lookup"><span data-stu-id="014e4-199">You can view the cost in the **Cost** field on the **General** tab. The cost is calculated by using the rate that you define on the **Inventory management parameters** page.</span></span>

1. <span data-ttu-id="014e4-200">Gjenta det forrige trinnet for hver timeregistreringslinje du må legge til.</span><span class="sxs-lookup"><span data-stu-id="014e4-200">Repeat the previous step for each additional timesheet line that you must add.</span></span>
1. <span data-ttu-id="014e4-201">Lukk sidene.</span><span class="sxs-lookup"><span data-stu-id="014e4-201">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="014e4-202">Beløpet i feltet **Kostnad** summeres for alle timeregistreringslinjer og legges til andre beløp i **Kostnad**-feltet på siden **Relaterte operasjoner**.</span><span class="sxs-lookup"><span data-stu-id="014e4-202">The amount in the **Cost** field is summed for all timesheet lines and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

## <a name="add-a-correction-to-a-nonconformance"></a><span data-ttu-id="014e4-203">Legge til en rettelse i et avvik</span><span class="sxs-lookup"><span data-stu-id="014e4-203">Add a correction to a nonconformance</span></span>

<span data-ttu-id="014e4-204">Hvis du vil legge til en rettelse i et avvik, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="014e4-204">To add a correction to a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="014e4-205">Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Avvik**.</span><span class="sxs-lookup"><span data-stu-id="014e4-205">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="014e4-206">Velg avviket du vil oppdatere, i listen.</span><span class="sxs-lookup"><span data-stu-id="014e4-206">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="014e4-207">Du kan bare legge til en rettelse i avvik som er godkjent.</span><span class="sxs-lookup"><span data-stu-id="014e4-207">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="014e4-208">I handlingsruten velger du **Korreksjoner**.</span><span class="sxs-lookup"><span data-stu-id="014e4-208">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="014e4-209">I handlingsruten velger du **Ny** for å legge til en rad i rutenettet på siden **Rettelser**.</span><span class="sxs-lookup"><span data-stu-id="014e4-209">On the **Corrections** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="014e4-210">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="014e4-210">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="014e4-211">**Diagnose** – Velg diagnosetypen som identifiserer rettelsestypen du oppretter.</span><span class="sxs-lookup"><span data-stu-id="014e4-211">**Diagnostic** – Select the diagnostic type that identifies the type of correction that you're creating.</span></span>
    - <span data-ttu-id="014e4-212">**Arbeider** – Velg personen som er økonomisk ansvarlig for rettelsen.</span><span class="sxs-lookup"><span data-stu-id="014e4-212">**Worker** – Select the person who is responsible for the correction.</span></span>
    - <span data-ttu-id="014e4-213">**Rettelsesprioritet** – Velg et alternativ for å angi hvordan rettelsen skal prioriteres (*Lav*, *Normal* eller *Høy*).</span><span class="sxs-lookup"><span data-stu-id="014e4-213">**Correction priority** – Select an option to indicate how the correction should be prioritized (*Low*, *Normal*, or *High*).</span></span>
    - <span data-ttu-id="014e4-214">**Ønsket dato** – Angi datoen da den korrigerende handlingen ble forespurt.</span><span class="sxs-lookup"><span data-stu-id="014e4-214">**Requested date** – Enter the date when the corrective action was requested.</span></span>
    - <span data-ttu-id="014e4-215">**Planlagt dato** – Angi datoen da rettelsen forventes å være fullført.</span><span class="sxs-lookup"><span data-stu-id="014e4-215">**Planned date** – Enter the date when the correction is expected to be completed.</span></span>
    - <span data-ttu-id="014e4-216">**Kortsiktig løsning** – Merk av i denne avmerkingsboksen hvis den korrigerende handlingen retter avviket bare i en kort tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="014e4-216">**Short term solution** – Select this check box if the corrective action corrects the nonconformance only for a short time.</span></span>

1. <span data-ttu-id="014e4-217">Lukk sidene.</span><span class="sxs-lookup"><span data-stu-id="014e4-217">Close the pages.</span></span>

## <a name="mark-a-correction-as-completed"></a><span data-ttu-id="014e4-218">Merke en rettelse som fullført</span><span class="sxs-lookup"><span data-stu-id="014e4-218">Mark a correction as completed</span></span>

<span data-ttu-id="014e4-219">Hvis du vil merke en avviksrettelse som fullført, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="014e4-219">To mark a nonconformance correction as completed, follow these steps.</span></span>

1. <span data-ttu-id="014e4-220">Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Avvik**.</span><span class="sxs-lookup"><span data-stu-id="014e4-220">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="014e4-221">Velg avviket du vil oppdatere, i listen.</span><span class="sxs-lookup"><span data-stu-id="014e4-221">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="014e4-222">Du kan bare legge til en rettelse i avvik som er godkjent.</span><span class="sxs-lookup"><span data-stu-id="014e4-222">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="014e4-223">I handlingsruten velger du **Korreksjoner**.</span><span class="sxs-lookup"><span data-stu-id="014e4-223">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="014e4-224">Velg **Rettelser**-siden i rutenettet, og velg rettelsen du vil merke som fullført.</span><span class="sxs-lookup"><span data-stu-id="014e4-224">On the **Corrections** page, in the grid, select the correction that you want to mark as completed.</span></span>
1. <span data-ttu-id="014e4-225">Velg **Merk som fullført** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="014e4-225">On the Action Pane, select **Mark complete**.</span></span>
1. <span data-ttu-id="014e4-226">Du blir bedt om å bekrefte valget.</span><span class="sxs-lookup"><span data-stu-id="014e4-226">You're prompted to confirm your selection.</span></span> <span data-ttu-id="014e4-227">Velg **OK** for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="014e4-227">Select **OK** to continue.</span></span> <span data-ttu-id="014e4-228">**Fullføringsdato- og -klokkeslett**-feltet settes til gjeldende dato og klokkeslett, og det merkes av i avmerkingsboksen **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="014e4-228">The **Completion date and time** field is set to the current date and time, and the **Completed** check box is selected.</span></span>
1. <span data-ttu-id="014e4-229">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="014e4-229">Close the page.</span></span>

## <a name="reopen-a-completed-correction"></a><span data-ttu-id="014e4-230">Åpne en fullført rettelse på nytt</span><span class="sxs-lookup"><span data-stu-id="014e4-230">Reopen a completed correction</span></span>

<span data-ttu-id="014e4-231">Hvis du vil åpne er fullført rettelse på nytt, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="014e4-231">To reopen a completed correction, follow these steps.</span></span>

1. <span data-ttu-id="014e4-232">Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Avvik**.</span><span class="sxs-lookup"><span data-stu-id="014e4-232">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="014e4-233">Velg avviket du vil oppdatere, i listen.</span><span class="sxs-lookup"><span data-stu-id="014e4-233">In the list, select the nonconformance that you want to update.</span></span>
1. <span data-ttu-id="014e4-234">I handlingsruten velger du **Korreksjoner**.</span><span class="sxs-lookup"><span data-stu-id="014e4-234">On the Action pane, select **Corrections**.</span></span>
1. <span data-ttu-id="014e4-235">På **Rettelser**-siden i rutenettet velger du rettelsen du vil åpne på nytt.</span><span class="sxs-lookup"><span data-stu-id="014e4-235">On the **Corrections** page, in the grid, select the correction that you want to reopen.</span></span>
1. <span data-ttu-id="014e4-236">I handlingsruten velger du **Åpne på nytt**.</span><span class="sxs-lookup"><span data-stu-id="014e4-236">On the Action Pane, select **Reopen**.</span></span>
1. <span data-ttu-id="014e4-237">Du blir bedt om å bekrefte valget.</span><span class="sxs-lookup"><span data-stu-id="014e4-237">You're prompted to confirm your selection.</span></span> <span data-ttu-id="014e4-238">Velg **OK** for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="014e4-238">Select **OK** to continue.</span></span> <span data-ttu-id="014e4-239">Verdien tømmes fra **Fullføringsdato- og -klokkeslettfeltet**, og det er ikke merket av for **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="014e4-239">The value is cleared from the **Completion date and time** field, and the **Completed** check box is cleared.</span></span>
1. <span data-ttu-id="014e4-240">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="014e4-240">Close the page.</span></span>

<span data-ttu-id="014e4-241">Du kan nå foreta flere endringer eller oppdateringer i rettelsen.</span><span class="sxs-lookup"><span data-stu-id="014e4-241">You can now make additional edits or updates to the correction.</span></span> <span data-ttu-id="014e4-242">Når du er ferdig, kan du merke rettelsen som fullført på nytt.</span><span class="sxs-lookup"><span data-stu-id="014e4-242">When you've finished, you can mark the correction as completed again.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="014e4-243">Lukke et avvik</span><span class="sxs-lookup"><span data-stu-id="014e4-243">Close a nonconformance</span></span>

<span data-ttu-id="014e4-244">Hvis du vil lukke et avvik, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="014e4-244">To close a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="014e4-245">Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Kvalitetsordrer**.</span><span class="sxs-lookup"><span data-stu-id="014e4-245">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="014e4-246">Velg en kvalitetsordre i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="014e4-246">Select a quality order in the grid.</span></span>
1. <span data-ttu-id="014e4-247">Velg **Forespørsler \> Avvik** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="014e4-247">On the Action Pane, select **Inquiries \> Non conformances**.</span></span>
1. <span data-ttu-id="014e4-248">På **Avvik**-siden velger du målavviket i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="014e4-248">On the **Non conformances** page, select the target nonconformance in the grid.</span></span>
1. <span data-ttu-id="014e4-249">Velg **Funksjoner \> Lukk avvik** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="014e4-249">On the Action Pane, select **Functions \> Close non conformance**.</span></span>
1. <span data-ttu-id="014e4-250">Du blir bedt om å bekrefte valget.</span><span class="sxs-lookup"><span data-stu-id="014e4-250">You're prompted to confirm your selection.</span></span> <span data-ttu-id="014e4-251">Klikk på **Ja** for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="014e4-251">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="014e4-252">Lukk sidene.</span><span class="sxs-lookup"><span data-stu-id="014e4-252">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="014e4-253">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="014e4-253">Additional resources</span></span>

- [<span data-ttu-id="014e4-254">Oversikt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="014e4-254">Quality management overview</span></span>](../quality-management-processes.md)
- [<span data-ttu-id="014e4-255">Aktivere kvalitets- og avviksstyring</span><span class="sxs-lookup"><span data-stu-id="014e4-255">Enable quality and nonconformance management</span></span>](../enable-quality-management.md)
- [<span data-ttu-id="014e4-256">Arbeidere som er ansvarlige for å godkjenne avvik</span><span class="sxs-lookup"><span data-stu-id="014e4-256">Workers responsible for approving nonconformances</span></span>](../quality-responsible-workers.md)
- [<span data-ttu-id="014e4-257">Karantenesoner for avvik</span><span class="sxs-lookup"><span data-stu-id="014e4-257">Quarantine zones for nonconformances</span></span>](../quality-quarantine-zones.md)
- [<span data-ttu-id="014e4-258">Diagnosetyper for avvik</span><span class="sxs-lookup"><span data-stu-id="014e4-258">Diagnostic types for nonconformances</span></span>](../quality-diagnostic-types.md)
- [<span data-ttu-id="014e4-259">Kvalitetsendringer for avvik</span><span class="sxs-lookup"><span data-stu-id="014e4-259">Quality charges for nonconformances</span></span>](../quality-charges.md)
- [<span data-ttu-id="014e4-260">Operasjoner for avvik</span><span class="sxs-lookup"><span data-stu-id="014e4-260">Operations for nonconformances</span></span>](../quality-operations.md)
- [<span data-ttu-id="014e4-261">Kvalitetsstyring for lagerprosesser</span><span class="sxs-lookup"><span data-stu-id="014e4-261">Quality management for warehouse processes</span></span>](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
