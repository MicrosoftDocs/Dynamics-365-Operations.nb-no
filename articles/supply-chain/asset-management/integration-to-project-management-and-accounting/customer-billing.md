---
title: Fakturere for vedlikehold av aktiva som eies av kunden
description: Dette emnet beskriver hvordan du oppretter, behandler og fakturerer for vedlikeholdsarbeid på aktiva som kundene eier.
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 643e59f082949ed51ab61d79648a98b83a7f0b03
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131847"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a><span data-ttu-id="c1b33-103">Fakturere for vedlikehold av aktiva som eies av kunden</span><span class="sxs-lookup"><span data-stu-id="c1b33-103">Bill for maintenance on customer-owned assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1b33-104">Med funksjonen *Arbeidsordrefakturering* kan du opprette, behandle og fakturere for vedlikeholdsarbeid på aktiva som kundene eier.</span><span class="sxs-lookup"><span data-stu-id="c1b33-104">The *Work order billing* feature lets you create, process, and bill maintenance work that is done on assets that your customers own.</span></span> <span data-ttu-id="c1b33-105">Denne funksjonen lar deg utføre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="c1b33-105">This feature lets you perform the following tasks:</span></span>

- <span data-ttu-id="c1b33-106">Koble kunder til aktivaene de eier.</span><span class="sxs-lookup"><span data-stu-id="c1b33-106">Connect customers to the assets that they own.</span></span>
- <span data-ttu-id="c1b33-107">Velg en kunde, og vis aktivaene som kunden eier, når du oppretter en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="c1b33-107">Select a customer and view the assets that customer owns when you create a work order.</span></span>
- <span data-ttu-id="c1b33-108">Definer et hovedprosjekt for hver kunde.</span><span class="sxs-lookup"><span data-stu-id="c1b33-108">Set up a parent project for each customer.</span></span>
- <span data-ttu-id="c1b33-109">Registrer timer, varer, utgifter og gebyrer mot arbeidsordren, og opprett senere et fakturaforslag for kunden.</span><span class="sxs-lookup"><span data-stu-id="c1b33-109">Register hours, items, expenses, and fees against the work order, and then create an invoice proposal for the customer later.</span></span>

<span data-ttu-id="c1b33-110">Funksjonen har i tillegg følgende funksjonalitet:</span><span class="sxs-lookup"><span data-stu-id="c1b33-110">In addition, the feature provides the following functionality:</span></span>

- <span data-ttu-id="c1b33-111">Prosjektkontrakten fra et hovedprosjekt for en kunde kopieres automatisk til det relevante arbeidsordreprosjektet.</span><span class="sxs-lookup"><span data-stu-id="c1b33-111">The project contract from a customer's parent project is automatically copied to the relevant work order project.</span></span>
- <span data-ttu-id="c1b33-112">Aktivastyring kan nå bruke prosjekttransaksjonstypen *gebyr* i både arbeidsordreprognoser og arbeidsordrejournaler.</span><span class="sxs-lookup"><span data-stu-id="c1b33-112">Asset management can now use the *fee* project transaction type on both work order forecasts and work order journals.</span></span>

## <a name="turn-on-the-customer-billing-feature"></a><span data-ttu-id="c1b33-113">Aktivere funksjonen for kundefakturering</span><span class="sxs-lookup"><span data-stu-id="c1b33-113">Turn on the customer billing feature</span></span>

<span data-ttu-id="c1b33-114">Før du kan bruke denne funksjonen, må den være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="c1b33-114">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="c1b33-115">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den.</span><span class="sxs-lookup"><span data-stu-id="c1b33-115">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="c1b33-116">I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="c1b33-116">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c1b33-117">**Modul:** *Prosjektstyring og regnskap*</span><span class="sxs-lookup"><span data-stu-id="c1b33-117">**Module:** *Project management and accounting*</span></span>
- <span data-ttu-id="c1b33-118">**Funksjonsnavn:** *Arbeidsordrefakturering*</span><span class="sxs-lookup"><span data-stu-id="c1b33-118">**Feature name:** *Work order billing*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="c1b33-119">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="c1b33-119">Example scenario</span></span>

<span data-ttu-id="c1b33-120">Hvis du vil vite hvordan denne funksjonen fungerer, kan du gå gjennom følgende eksempelscenario.</span><span class="sxs-lookup"><span data-stu-id="c1b33-120">To learn how this feature works, work through the following example scenario.</span></span>

<span data-ttu-id="c1b33-121">For å arbeide deg gjennom dette scenariet ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert.</span><span class="sxs-lookup"><span data-stu-id="c1b33-121">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="c1b33-122">Du må velge den juridiske enheten **USMF** før du begynner.</span><span class="sxs-lookup"><span data-stu-id="c1b33-122">You must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="c1b33-123">Du kan også bruke dette scenariet som en veiledning for å bruke funksjonen når du arbeider i et produksjonssystem.</span><span class="sxs-lookup"><span data-stu-id="c1b33-123">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="c1b33-124">I så fall må du imidlertid erstatte dine egne verdier, og det kan hende du mangler noen typer obligatoriske oppføringer som standard demonstrasjonsdata gir.</span><span class="sxs-lookup"><span data-stu-id="c1b33-124">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a><span data-ttu-id="c1b33-125">Trinn 1: Opprette en ny prosjektkontrakt for kunden</span><span class="sxs-lookup"><span data-stu-id="c1b33-125">Step 1: Create a new project contract for the customer</span></span>

1. <span data-ttu-id="c1b33-126">Gå til **Prosjektstyring og regnskap \> Prosjekter \> Prosjektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="c1b33-126">Go to **Project management and accounting \> Projects \> Project contracts**.</span></span>
1. <span data-ttu-id="c1b33-127">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c1b33-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c1b33-128">I dialogboksen **Ny prosjektkontrakt** angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="c1b33-128">In the **New project contract** dialog box, set the following values:</span></span>

    - <span data-ttu-id="c1b33-129">**Navn:** *Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="c1b33-129">**Name:** *Pelican Wholesales*</span></span>
    - <span data-ttu-id="c1b33-130">**Finansieringstype:** *Kunde*</span><span class="sxs-lookup"><span data-stu-id="c1b33-130">**Funding type:** *Customer*</span></span>
    - <span data-ttu-id="c1b33-131">**Finansieringskilde:** *US-013* (*Pelican Wholesales)*</span><span class="sxs-lookup"><span data-stu-id="c1b33-131">**Funding source:** *US-013* (*Pelican Wholesales*)</span></span>

1. <span data-ttu-id="c1b33-132">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1b33-132">Select **OK**.</span></span>

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a><span data-ttu-id="c1b33-133">Trinn 2: Opprette et nytt hovedprosjekt for kunden</span><span class="sxs-lookup"><span data-stu-id="c1b33-133">Step 2: Create a new parent project for the customer</span></span>

<span data-ttu-id="c1b33-134">Hovedprosjektet du oppretter her, blir brukt når arbeidsordrer for kunden opprettes.</span><span class="sxs-lookup"><span data-stu-id="c1b33-134">The parent project that you create here will be used when work orders for the customer are created.</span></span>

1. <span data-ttu-id="c1b33-135">Gå til **Prosjektstyring og regnskap \> Prosjekter \> Alle prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="c1b33-135">Go to **Project management and accounting \> Projects \> All projects**.</span></span>
1. <span data-ttu-id="c1b33-136">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c1b33-136">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c1b33-137">Angi følgende verdier i dialogboksen **Nytt prosjekt**:</span><span class="sxs-lookup"><span data-stu-id="c1b33-137">In the **New project** dialog box, set the following values:</span></span>

    - <span data-ttu-id="c1b33-138">**Prosjekttype:** *Tid og materialer*</span><span class="sxs-lookup"><span data-stu-id="c1b33-138">**Project type:** *Time and material*</span></span>
    - <span data-ttu-id="c1b33-139">**Prosjektnavn:** *Arbeidsordrer for Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="c1b33-139">**Project name:** *Pelican Wholesales work orders*</span></span>
    - <span data-ttu-id="c1b33-140">**Prosjektgruppe:** *TM*</span><span class="sxs-lookup"><span data-stu-id="c1b33-140">**Project group:** *TM*</span></span>
    - <span data-ttu-id="c1b33-141">**Prosjektkontrakt-ID:** *Pelican Wholesales* (kontrakten du opprettet tidligere)</span><span class="sxs-lookup"><span data-stu-id="c1b33-141">**Project contract ID:** *Pelican Wholesales* (the contract that you created earlier)</span></span>
    - <span data-ttu-id="c1b33-142">**Startdato:** Velg dagens dato.</span><span class="sxs-lookup"><span data-stu-id="c1b33-142">**Start date:** Select today's date.</span></span>

1. <span data-ttu-id="c1b33-143">Velg **Opprett prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="c1b33-143">Select **Create project**.</span></span>
1. <span data-ttu-id="c1b33-144">Det nye prosjektet åpnes.</span><span class="sxs-lookup"><span data-stu-id="c1b33-144">The new project is opened.</span></span> <span data-ttu-id="c1b33-145">Noter verdien for **Prosjekt-ID**.</span><span class="sxs-lookup"><span data-stu-id="c1b33-145">Make a note of the **Project ID** value.</span></span> <span data-ttu-id="c1b33-146">Du må angi den senere.</span><span class="sxs-lookup"><span data-stu-id="c1b33-146">You will have to enter it later.</span></span>

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a><span data-ttu-id="c1b33-147">Trinn 3: Opprette en ny arbeidsordretype i Aktivastyring</span><span class="sxs-lookup"><span data-stu-id="c1b33-147">Step 3: Create a new work order type in Asset management</span></span>

1. <span data-ttu-id="c1b33-148">Gå til **Aktivastyring \> Oppsett \> Arbeidsordre \> Arbeidsordretyper**.</span><span class="sxs-lookup"><span data-stu-id="c1b33-148">Go to **Asset management \> Setup \> Work order \> Work order types**.</span></span>
1. <span data-ttu-id="c1b33-149">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c1b33-149">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c1b33-150">Det blir lagt til en ny post i listen.</span><span class="sxs-lookup"><span data-stu-id="c1b33-150">A new record is added to the list.</span></span> <span data-ttu-id="c1b33-151">Angi følgende verdier for den:</span><span class="sxs-lookup"><span data-stu-id="c1b33-151">Set the following values for it:</span></span>

    - <span data-ttu-id="c1b33-152">**Arbeidsordretype:** *Service*</span><span class="sxs-lookup"><span data-stu-id="c1b33-152">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="c1b33-153">**Navn:** *Servicearbeidsordrer*</span><span class="sxs-lookup"><span data-stu-id="c1b33-153">**Name:** *Service work orders*</span></span>
    - <span data-ttu-id="c1b33-154">**Livssyklustilstand for arbeidsordre:** *Standard*</span><span class="sxs-lookup"><span data-stu-id="c1b33-154">**Work order lifecycle state:** *Standard*</span></span>

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a><span data-ttu-id="c1b33-155">Trinn 4: Koble kundekontoen til hovedprosjektet</span><span class="sxs-lookup"><span data-stu-id="c1b33-155">Step 4: Link the customer account to the parent project</span></span>

<span data-ttu-id="c1b33-156">Du må nå koble kundekontoen til hovedprosjektet i prosjektoppsettet i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="c1b33-156">You must now link the customer account to the parent project in the project setup in Asset management.</span></span>

1. <span data-ttu-id="c1b33-157">Gå til **Aktivastyring \> Oppsett \> Arbeidsordrer \> Prosjektoppsett**.</span><span class="sxs-lookup"><span data-stu-id="c1b33-157">Go to **Asset management \> Setup \> Work orders \> Project setup**.</span></span>
1. <span data-ttu-id="c1b33-158">I fanen **Hovedprosjekt** velger du **Legg til** for å legge til en linje.</span><span class="sxs-lookup"><span data-stu-id="c1b33-158">On the **Parent project** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="c1b33-159">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="c1b33-159">On the new line, set the following values:</span></span>

    - <span data-ttu-id="c1b33-160">**Kundekonto:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="c1b33-160">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="c1b33-161">**Prosjekt-ID:** Angi prosjekt-ID-en du noterte tidligere.</span><span class="sxs-lookup"><span data-stu-id="c1b33-161">**Project ID:** Enter the project ID that you made a note of earlier.</span></span>

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a><span data-ttu-id="c1b33-162">Trinn 5: Koble prosjektgruppen og -typen til arbeidsordreprosjektet</span><span class="sxs-lookup"><span data-stu-id="c1b33-162">Step 5: Link the project group and type to the work order project</span></span>

<span data-ttu-id="c1b33-163">Du skal fortsatt være på siden **Prosjektoppsett** (**Aktivastyring \> Oppsett \> Arbeidsordrer \> Prosjektoppsett**).</span><span class="sxs-lookup"><span data-stu-id="c1b33-163">You should still be on the **Project setup** page (**Asset management \> Setup \> Work orders \> Project setup**).</span></span>

1. <span data-ttu-id="c1b33-164">I fanen **Prosjektgruppe** velger du **Legg til** for å legge til en linje.</span><span class="sxs-lookup"><span data-stu-id="c1b33-164">On the **Project group** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="c1b33-165">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="c1b33-165">On the new line, set the following values:</span></span>

    - <span data-ttu-id="c1b33-166">**Arbeidsordretype:** *Service* (arbeidsordretypen du opprettet tidligere)</span><span class="sxs-lookup"><span data-stu-id="c1b33-166">**Work order type:** *Service* (the work order type that you created earlier)</span></span>
    - <span data-ttu-id="c1b33-167">**Prosjektgruppe:** *TM*</span><span class="sxs-lookup"><span data-stu-id="c1b33-167">**Project group:** *TM*</span></span>

> [!NOTE]
> <span data-ttu-id="c1b33-168">Prosjektkontrakten på arbeidsordreprosjektet arves alltid fra hovedprosjektet.</span><span class="sxs-lookup"><span data-stu-id="c1b33-168">The project contract on the work order project is always inherited from the parent project.</span></span>

### <a name="step-6-link-an-asset-to-the-customer-id"></a><span data-ttu-id="c1b33-169">Trinn 6: Koble et aktivum til kunde-ID-en</span><span class="sxs-lookup"><span data-stu-id="c1b33-169">Step 6: Link an asset to the customer ID</span></span>

1. <span data-ttu-id="c1b33-170">Gå til **Aktivastyring \> Aktiva \> Aktive aktiva**.</span><span class="sxs-lookup"><span data-stu-id="c1b33-170">Go to **Asset management \> Assets \> Active assets**.</span></span>
1. <span data-ttu-id="c1b33-171">Angi *VE-102* i **Filter**-feltet, og velg å filtrere etter **Aktivum**.</span><span class="sxs-lookup"><span data-stu-id="c1b33-171">In the **Filter** field, enter *VE-102*, and select to filter by **Asset**.</span></span>
1. <span data-ttu-id="c1b33-172">Velg aktivumet for å åpne innstillingene for det.</span><span class="sxs-lookup"><span data-stu-id="c1b33-172">Select the asset to open its settings.</span></span>
1. <span data-ttu-id="c1b33-173">I hurtigfanen **Kunde** angir du *US-013* (*Pelican Wholesales*) i **Kundekonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c1b33-173">On the **Customer** FastTab, set the **Customer account** field to *US-013* (*Pelican Wholesales*).</span></span>

    <span data-ttu-id="c1b33-174">**Navn**-feltet oppdateres automatisk til *Pelican Wholesales*.</span><span class="sxs-lookup"><span data-stu-id="c1b33-174">The **Name** field is automatically updated to *Pelican Wholesales*.</span></span>

### <a name="step-7-create-a-new-work-order-on-the-asset"></a><span data-ttu-id="c1b33-175">Trinn 7: Opprette en ny arbeidsordre for aktivumet</span><span class="sxs-lookup"><span data-stu-id="c1b33-175">Step 7: Create a new work order on the asset</span></span>

1. <span data-ttu-id="c1b33-176">Gå til **Aktivastyring \> Arbeidsordrer \> Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="c1b33-176">Go to **Asset management \> Work orders \> Active work orders**.</span></span>
1. <span data-ttu-id="c1b33-177">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c1b33-177">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c1b33-178">I dialogboksen **Opprett arbeidsordre** angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="c1b33-178">In the **Create work order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="c1b33-179">**Arbeidsordretype:** *Service*</span><span class="sxs-lookup"><span data-stu-id="c1b33-179">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="c1b33-180">**Beskrivelse:** *Reparer lastebil*</span><span class="sxs-lookup"><span data-stu-id="c1b33-180">**Description:** *Repair Truck*</span></span>
    - <span data-ttu-id="c1b33-181">**Kundekonto:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="c1b33-181">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="c1b33-182">**Aktivum:** *VE-102*</span><span class="sxs-lookup"><span data-stu-id="c1b33-182">**Asset:** *VE-102*</span></span>

        > [!NOTE]
        > <span data-ttu-id="c1b33-183">Oppslaget viser bare aktiva som er koblet til den valgte kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="c1b33-183">The lookup shows only assets that are linked to the selected customer account.</span></span>

    - <span data-ttu-id="c1b33-184">**Vedlikeholdsjobbtype:** *Reparasjon*</span><span class="sxs-lookup"><span data-stu-id="c1b33-184">**Maintenance job type:** *Repair*</span></span>
    - <span data-ttu-id="c1b33-185">**Yrke:** *Mekaniker*</span><span class="sxs-lookup"><span data-stu-id="c1b33-185">**Trade:** *Mechanic*</span></span>
    - <span data-ttu-id="c1b33-186">**Servicenivå:** *4*</span><span class="sxs-lookup"><span data-stu-id="c1b33-186">**Service level:** *4*</span></span>

1. <span data-ttu-id="c1b33-187">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1b33-187">Select **OK**.</span></span>

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a><span data-ttu-id="c1b33-188">Trinn 8: Gå gjennom arbeidsordren og begynne å arbeide på den</span><span class="sxs-lookup"><span data-stu-id="c1b33-188">Step 8: Review the work order and start to work on it</span></span>

<span data-ttu-id="c1b33-189">I denne delen skal du arbeide på arbeidsordren du opprettet i den forrige delen.</span><span class="sxs-lookup"><span data-stu-id="c1b33-189">In this section, you will work on the work order that you created in the previous section.</span></span>

1. <span data-ttu-id="c1b33-190">Følg denne fremgangsmåten for å kontrollere at hovedprosjektet er prosjektet *Arbeidsordre for Pelican wholesales*:</span><span class="sxs-lookup"><span data-stu-id="c1b33-190">Follow these steps to verify that the parent project is the *Pelican wholesales Work order* project:</span></span>

    1. <span data-ttu-id="c1b33-191">Velg en linje i delen **Vedlikeholdsjobber for arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="c1b33-191">In the **Work order maintenance jobs** section, select a line.</span></span>
    1. <span data-ttu-id="c1b33-192">Kontroller **Prosjekt-ID**-verdien i hurtigfanen **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="c1b33-192">On the **Line details** FastTab, inspect the **Project ID** value.</span></span> <span data-ttu-id="c1b33-193">Det skal være et nummer med bindestrek i skjemaet *\<Parent-Project-ID\>-\<Project-ID\>*.</span><span class="sxs-lookup"><span data-stu-id="c1b33-193">It should be a hyphenated number in the form *\<Parent-Project-ID\>-\<Project-ID\>*.</span></span> <span data-ttu-id="c1b33-194">Denne verdien er en kobling.</span><span class="sxs-lookup"><span data-stu-id="c1b33-194">This value is a link.</span></span>
    1. <span data-ttu-id="c1b33-195">Velg koblingen for prosjekt-ID for å åpne en side der du kan vise hovedprosjektet og prosjektnavnene.</span><span class="sxs-lookup"><span data-stu-id="c1b33-195">Select the project ID link to open a page where you can view the parent project and project names.</span></span>

1. <span data-ttu-id="c1b33-196">Velg **Oppdater tilstand for arbeidsordre** i gruppen **Livssyklustilstand** i **Arbeidsordre**-fanen i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c1b33-196">On the Action Pane, on the **Work order** tab, in the **Lifecycle state** group, select **Update work order state**.</span></span>
1. <span data-ttu-id="c1b33-197">Merk av for raden der feltet **Livssyklustilstand** er satt til *Pågår* i **Velg**-kolonnen i dialogboksen **Oppdater tilstand for arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="c1b33-197">In the **Update work order state** dialog box, in the **Select** column, select the check box for the row where the **Lifecycle state** field is set to *In progress*.</span></span>
1. <span data-ttu-id="c1b33-198">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1b33-198">Select **OK**.</span></span>
1. <span data-ttu-id="c1b33-199">Velg **OK** i dialogboksen **Livssyklustilstand: InProgress**.</span><span class="sxs-lookup"><span data-stu-id="c1b33-199">In the **Lifecycle state: InProgress** dialog box, select **OK**.</span></span>

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a><span data-ttu-id="c1b33-200">Trinn 9: Postere timene som ble brukt på arbeidsordren, og opprette et nytt fakturaforslag</span><span class="sxs-lookup"><span data-stu-id="c1b33-200">Step 9: Post the hours that were spent on the work order and create a new invoice proposal</span></span>

<span data-ttu-id="c1b33-201">I denne delen skal du fortsette å arbeide på arbeidsordren du arbeidet på i den forrige delen.</span><span class="sxs-lookup"><span data-stu-id="c1b33-201">In this section, you will continue to work on the work order that you worked on in the previous section.</span></span>

1. <span data-ttu-id="c1b33-202">Velg **Journaler** i **Prosjekt**-gruppen i **Arbeidsordre**-fanen i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c1b33-202">On the Action Pane, on the **Work order** tab, in the **Project** group, select **Journals**.</span></span>

    <span data-ttu-id="c1b33-203">Siden **Arbeidsordrejournaler** vises.</span><span class="sxs-lookup"><span data-stu-id="c1b33-203">The **Work order journals** page appears.</span></span> <span data-ttu-id="c1b33-204">Her kan du registrere tiden du har brukt på arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="c1b33-204">Here, you can register the time that you spent on the work order.</span></span>

1. <span data-ttu-id="c1b33-205">Velg **Legg til linje** i hurtigfanen **Timer**.</span><span class="sxs-lookup"><span data-stu-id="c1b33-205">On the **Hours** FastTab, select **Add line**.</span></span>
1. <span data-ttu-id="c1b33-206">Angi *4* i feltet **Timer** på den nye linjen.</span><span class="sxs-lookup"><span data-stu-id="c1b33-206">On the new, line, set the **Hours** field to *4*.</span></span>
1. <span data-ttu-id="c1b33-207">Velg **Poster journaler** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c1b33-207">On the Action Pane, select **Post journals**.</span></span>
1. <span data-ttu-id="c1b33-208">Lukk siden **Arbeidsordrejournaler** for å gå tilbake til arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="c1b33-208">Close the **Work order journals** page to return to the work order.</span></span>
1. <span data-ttu-id="c1b33-209">Velg **Nytt fakturaforslag** i **Fakturering**-fanen i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c1b33-209">On the Action Pane, on the **Invoicing** tab, select **New invoice proposal**.</span></span>
1. <span data-ttu-id="c1b33-210">Merk av for **Velg** for hver linje du vil fakturere, under **Prosjekttransaksjoner** i dialogboksen **Opprett fakturaforslag**.</span><span class="sxs-lookup"><span data-stu-id="c1b33-210">In the **Create invoice proposal** dialog box, in the **Project transactions** section, select the **Select** check box for every line  that you want to invoice.</span></span>
1. <span data-ttu-id="c1b33-211">Velg **OK** for å lukke dialogboksen og vise det nye fakturaforslaget.</span><span class="sxs-lookup"><span data-stu-id="c1b33-211">Select **OK** to close the dialog box and view the new invoice proposal.</span></span>
