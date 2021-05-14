---
title: Rabattbehandlingsgrupper
description: Dette emnet beskriver hvordan du setter opp rabattbehandlingsgrupper. Rabattbehandlingsgrupper kan brukes under rabattberegninger, og kan knyttes til en hovedoppføring.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: cef7abbbf2a94e26b6b9e66492cd7347d3b4d1f2
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920067"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="e246e-104">Rabattbehandlingsgrupper</span><span class="sxs-lookup"><span data-stu-id="e246e-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e246e-105">Beregninger av rabatt og fradrag kan drives av grupper.</span><span class="sxs-lookup"><span data-stu-id="e246e-105">Rebate and deduction calculations can be driven by groups.</span></span> <span data-ttu-id="e246e-106">Rabattbehandlingsgrupper kan opprettes for kunder, leverandører og varer.</span><span class="sxs-lookup"><span data-stu-id="e246e-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="e246e-107">De kan knyttes til en hovedoppføring.</span><span class="sxs-lookup"><span data-stu-id="e246e-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="e246e-108">Rabattbehandlingskundegrupper</span><span class="sxs-lookup"><span data-stu-id="e246e-108">Rebate management customer groups</span></span>

<span data-ttu-id="e246e-109">Beregningen for en gruppe kunder opprettes ofte for en kjede av firmaer, for eksempel en butikkjede eller et franchisefirma.</span><span class="sxs-lookup"><span data-stu-id="e246e-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="e246e-110">Denne typen beregning er vanligvis knyttet til en rabatt.</span><span class="sxs-lookup"><span data-stu-id="e246e-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="e246e-111">Et fradrag beregnes ofte uten å vurdere hvem den kvalifiserende ordren ble solgt til.</span><span class="sxs-lookup"><span data-stu-id="e246e-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="e246e-112">Det finnes imidlertid noen unntak.</span><span class="sxs-lookup"><span data-stu-id="e246e-112">However, there are exceptions.</span></span> <span data-ttu-id="e246e-113">En lisenstaker kan for eksempel opprette en fradragsplan der kundegruppe A mottar 4 prosent, men kundegruppe B mottar bare 3 prosent.</span><span class="sxs-lookup"><span data-stu-id="e246e-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="e246e-114">Definer kundegrupper</span><span class="sxs-lookup"><span data-stu-id="e246e-114">Set up customer groups</span></span>

<span data-ttu-id="e246e-115">Hvis du vil arbeide med kundegrupper for rabattstyring, kan du gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Kundegrupper**.</span><span class="sxs-lookup"><span data-stu-id="e246e-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="e246e-116">Du kan bruke knappene i handlingsruten til å legge til og fjerne grupper etter behov.</span><span class="sxs-lookup"><span data-stu-id="e246e-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="e246e-117">For hver gruppe angir du feltene nedenfor:</span><span class="sxs-lookup"><span data-stu-id="e246e-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="e246e-118">**Rabattbehandlingsgruppe** – Angi et unikt navn for gruppen.</span><span class="sxs-lookup"><span data-stu-id="e246e-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="e246e-119">**Beskrivelse** – Angi en beskrivelse av gruppen for å få mer informasjon om hvordan den skal brukes.</span><span class="sxs-lookup"><span data-stu-id="e246e-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="e246e-120">Administrer tilordninger av kundegrupper</span><span class="sxs-lookup"><span data-stu-id="e246e-120">Manage customer group assignments</span></span>

<span data-ttu-id="e246e-121">Hver kunde kan tilhøre et hvilket som helst antall rabattbehandlingsgrupper.</span><span class="sxs-lookup"><span data-stu-id="e246e-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="e246e-122">Hvis du vil vise og tilordne gruppemedlemmer, kan du starte fra enten gruppelisten eller kundelisten.</span><span class="sxs-lookup"><span data-stu-id="e246e-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="e246e-123">Følg denne fremgangsmåten for å vise, legge til eller fjerne kunder for en valgt gruppe.</span><span class="sxs-lookup"><span data-stu-id="e246e-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="e246e-124">Gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Kundegrupper**.</span><span class="sxs-lookup"><span data-stu-id="e246e-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="e246e-125">Velg gruppen som skal administreres.</span><span class="sxs-lookup"><span data-stu-id="e246e-125">Select the group to manage.</span></span>
1. <span data-ttu-id="e246e-126">Velg **Kunder** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e246e-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="e246e-127">Siden **Rabattbehandlingsgrupper** vises med en liste over kunder som allerede er medlemmer av den valgte gruppen.</span><span class="sxs-lookup"><span data-stu-id="e246e-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="e246e-128">Hvis du vil legge til en ny kunde i gruppen, velger du **Ny** i handlingsruten for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="e246e-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="e246e-129">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="e246e-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e246e-130">**Kundekonto** – Velg kundekonto-ID-en.</span><span class="sxs-lookup"><span data-stu-id="e246e-130">**Customer account** – Select the customer account ID.</span></span>
    - <span data-ttu-id="e246e-131">**Navn** – Angi et navn og/eller en beskrivelse for kunden.</span><span class="sxs-lookup"><span data-stu-id="e246e-131">**Name** – Enter a name and/or description of the customer.</span></span>

1. <span data-ttu-id="e246e-132">Hvis du vil fjerne en kunde fra gruppen, velger du kunden og velger deretter **Slett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e246e-132">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="e246e-133">Følg denne fremgangsmåten for å vise, legge til eller fjerne gruppetilordninger for en valgt kunde.</span><span class="sxs-lookup"><span data-stu-id="e246e-133">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="e246e-134">Gå til **Kunder \> Kunder \> Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="e246e-134">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="e246e-135">Velg kunden du vil arbeide med.</span><span class="sxs-lookup"><span data-stu-id="e246e-135">Select the customer to work with.</span></span>
1. <span data-ttu-id="e246e-136">I handlingsruten, på fanen **Kunde**, i **Rabattbehandling**-gruppen, velger du **Rabattbehandlingsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="e246e-136">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="e246e-137">Siden **Rabattbehandlingsgrupper** vises med en liste over grupper som den valgte kunden allerede hører til i.</span><span class="sxs-lookup"><span data-stu-id="e246e-137">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="e246e-138">Hvis du vil legge til kunden i en ny gruppe, velger du **Ny** i handlingsruten for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="e246e-138">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="e246e-139">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="e246e-139">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e246e-140">**Rabattbehandlingsgruppe** – Velg gruppen du vil legge til kunden i.</span><span class="sxs-lookup"><span data-stu-id="e246e-140">**Rebate management group** – Select the group to add the customer to.</span></span>
    - <span data-ttu-id="e246e-141">**Beskrivelse** – Angi en beskrivelse av gruppen (for eksempel for å forklare hvorfor kunden er medlem av den).</span><span class="sxs-lookup"><span data-stu-id="e246e-141">**Description** – Enter a description of the group (for example, to explain why the customer is a member of it).</span></span>

1. <span data-ttu-id="e246e-142">Hvis du vil fjerne en kunde fra en gruppe, velger du gruppen og velger deretter **Slett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e246e-142">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="e246e-143">Rabattbehandlingsleverandørgrupper</span><span class="sxs-lookup"><span data-stu-id="e246e-143">Rebate management vendor groups</span></span>

<span data-ttu-id="e246e-144">Beregningen for en gruppe med leverandører opprettes ofte for en gruppe med leveringspunkter.</span><span class="sxs-lookup"><span data-stu-id="e246e-144">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="e246e-145">Denne typen beregning er vanligvis knyttet til en rabatt.</span><span class="sxs-lookup"><span data-stu-id="e246e-145">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="e246e-146">Definer leverandørgrupper</span><span class="sxs-lookup"><span data-stu-id="e246e-146">Set up vendor groups</span></span>

<span data-ttu-id="e246e-147">Hvis du vil arbeide med leverandørgrupper for rabattstyring, kan du gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Leverandørgrupper**.</span><span class="sxs-lookup"><span data-stu-id="e246e-147">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="e246e-148">Du kan bruke knappene i handlingsruten til å legge til og fjerne grupper etter behov.</span><span class="sxs-lookup"><span data-stu-id="e246e-148">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="e246e-149">For hver gruppe angir du feltene nedenfor:</span><span class="sxs-lookup"><span data-stu-id="e246e-149">For each group, set the following fields:</span></span>

- <span data-ttu-id="e246e-150">**Rabattbehandlingsgruppe** – Angi et unikt navn for gruppen.</span><span class="sxs-lookup"><span data-stu-id="e246e-150">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="e246e-151">**Beskrivelse** – Angi en beskrivelse av gruppen for å få mer informasjon om hvordan den skal brukes.</span><span class="sxs-lookup"><span data-stu-id="e246e-151">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="e246e-152">Administrer tilordninger av leverandørgrupper</span><span class="sxs-lookup"><span data-stu-id="e246e-152">Manage vendor group assignments</span></span>

<span data-ttu-id="e246e-153">Hver leverandør kan tilhøre et hvilket som helst antall rabattbehandlingsgrupper.</span><span class="sxs-lookup"><span data-stu-id="e246e-153">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="e246e-154">Hvis du vil vise og tilordne gruppemedlemmer, kan du starte fra enten gruppelisten eller leverandørlisten.</span><span class="sxs-lookup"><span data-stu-id="e246e-154">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="e246e-155">Følg denne fremgangsmåten for å vise, legge til eller fjerne leverandører for en valgt gruppe.</span><span class="sxs-lookup"><span data-stu-id="e246e-155">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="e246e-156">Gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Leverandørgrupper**.</span><span class="sxs-lookup"><span data-stu-id="e246e-156">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="e246e-157">Velg gruppen som skal administreres.</span><span class="sxs-lookup"><span data-stu-id="e246e-157">Select the group to manage.</span></span>
1. <span data-ttu-id="e246e-158">Velg **Leverandører** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e246e-158">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="e246e-159">Siden **Rabattbehandlingsgrupper** vises med en liste over leverandører som allerede er medlemmer av den valgte gruppen.</span><span class="sxs-lookup"><span data-stu-id="e246e-159">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="e246e-160">Hvis du vil legge til en ny leverandør i en gruppe, velger du **Ny** i handlingsruten for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="e246e-160">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="e246e-161">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="e246e-161">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e246e-162">**Leverandørkonto** – Velg leverandørkonto-ID-en.</span><span class="sxs-lookup"><span data-stu-id="e246e-162">**Vendor account** – Select the vendor account ID.</span></span>
    - <span data-ttu-id="e246e-163">**Navn** – Angi et navn og/eller en beskrivelse for leverandøren.</span><span class="sxs-lookup"><span data-stu-id="e246e-163">**Name** – Enter a name and/or description of the vendor.</span></span>

1. <span data-ttu-id="e246e-164">Hvis du vil fjerne en leverandør fra gruppen, velger du leverandøren og velger deretter **Slett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e246e-164">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="e246e-165">Følg denne fremgangsmåten for å vise, legge til eller fjerne gruppetilordninger for en valgt leverandør.</span><span class="sxs-lookup"><span data-stu-id="e246e-165">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="e246e-166">Gå til **Leverandører \> Leverandører \> Alle leverandører**.</span><span class="sxs-lookup"><span data-stu-id="e246e-166">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="e246e-167">Velg leverandøren du vil arbeide med.</span><span class="sxs-lookup"><span data-stu-id="e246e-167">Select the vendor to work with.</span></span>
1. <span data-ttu-id="e246e-168">I handlingsruten, på fanen **Leverandør**, i **Rabattbehandling**-gruppen, velger du **Rabattbehandlingsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="e246e-168">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="e246e-169">Siden **Rabattbehandlingsgrupper** vises med en liste over grupper som den valgte leverandøren allerede hører til i.</span><span class="sxs-lookup"><span data-stu-id="e246e-169">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="e246e-170">Hvis du vil legge til leverandøren i en ny gruppe, velger du **Ny** i handlingsruten for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="e246e-170">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="e246e-171">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="e246e-171">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e246e-172">**Rabattbehandlingsgruppe** – Velg gruppen du vil legge til leverandøren i.</span><span class="sxs-lookup"><span data-stu-id="e246e-172">**Rebate management group** – Select the group to add the vendor to.</span></span>
    - <span data-ttu-id="e246e-173">**Beskrivelse** – Angi en beskrivelse av gruppen (for eksempel for å forklare hvorfor leverandøren er medlem av den).</span><span class="sxs-lookup"><span data-stu-id="e246e-173">**Description** – Enter a description of the group (for example, to explain why the vendor is a member of it).</span></span>

1. <span data-ttu-id="e246e-174">Hvis du vil fjerne en leverandør fra en gruppe, velger du gruppen og velger deretter **Slett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e246e-174">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="e246e-175">Varerabattgrupper</span><span class="sxs-lookup"><span data-stu-id="e246e-175">Item rebate groups</span></span>

<span data-ttu-id="e246e-176">Ved å gruppere varer har du mer fleksibilitet når rabatter og fradrag beregnes.</span><span class="sxs-lookup"><span data-stu-id="e246e-176">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="e246e-177">Denne fremgangsmåten er ofte en mer effektiv måte å definere rabatter og fradrag for kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="e246e-177">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="e246e-178">Definer varegrupper</span><span class="sxs-lookup"><span data-stu-id="e246e-178">Set up item groups</span></span>

<span data-ttu-id="e246e-179">Hvis du vil arbeide med varegrupper for rabattstyring, kan du gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Varegrupper**.</span><span class="sxs-lookup"><span data-stu-id="e246e-179">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="e246e-180">Du kan bruke knappene i handlingsruten til å legge til og fjerne grupper etter behov.</span><span class="sxs-lookup"><span data-stu-id="e246e-180">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="e246e-181">For hver gruppe angir du feltene nedenfor:</span><span class="sxs-lookup"><span data-stu-id="e246e-181">For each group, set the following fields:</span></span>

- <span data-ttu-id="e246e-182">**Rabattbehandlingsgruppe** – Angi et unikt navn for gruppen.</span><span class="sxs-lookup"><span data-stu-id="e246e-182">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="e246e-183">**Beskrivelse** – Angi en beskrivelse av gruppen for å få mer informasjon om hvordan den skal brukes.</span><span class="sxs-lookup"><span data-stu-id="e246e-183">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="e246e-184">Administrer tilordninger av varegrupper</span><span class="sxs-lookup"><span data-stu-id="e246e-184">Manage item group assignments</span></span>

<span data-ttu-id="e246e-185">Hver vare kan tilhøre et hvilket som helst antall rabattbehandlingsgrupper.</span><span class="sxs-lookup"><span data-stu-id="e246e-185">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="e246e-186">Hvis du vil vise og tilordne gruppemedlemmer, kan du starte fra enten gruppelisten eller varelisten.</span><span class="sxs-lookup"><span data-stu-id="e246e-186">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="e246e-187">Du kan også legge til varer basert på kategorihierarkiet.</span><span class="sxs-lookup"><span data-stu-id="e246e-187">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="e246e-188">Følg denne fremgangsmåten for å vise, legge til eller fjerne varer for en valgt gruppe.</span><span class="sxs-lookup"><span data-stu-id="e246e-188">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="e246e-189">Gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Varegrupper**.</span><span class="sxs-lookup"><span data-stu-id="e246e-189">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="e246e-190">Velg gruppen som skal administreres.</span><span class="sxs-lookup"><span data-stu-id="e246e-190">Select the group to manage.</span></span>
1. <span data-ttu-id="e246e-191">Velg **Varer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e246e-191">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="e246e-192">Siden **Rabattbehandlingsgrupper** vises med en liste over varer som allerede er medlemmer av den valgte gruppen.</span><span class="sxs-lookup"><span data-stu-id="e246e-192">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="e246e-193">Hvis du vil legge til en ny vare i gruppen, velger du **Ny** i handlingsruten for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="e246e-193">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="e246e-194">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="e246e-194">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e246e-195">**Varekonto** – Velg varekonto-ID-en.</span><span class="sxs-lookup"><span data-stu-id="e246e-195">**Item account** – Select the item account ID.</span></span>
    - <span data-ttu-id="e246e-196">**Produktnavn** – Angi et navn og/eller en beskrivelse for varen.</span><span class="sxs-lookup"><span data-stu-id="e246e-196">**Product name** – Enter a name and/or description of the item.</span></span>

1. <span data-ttu-id="e246e-197">Hvis du vil fjerne en vare fra gruppen, velger du varen og velger deretter **Slett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e246e-197">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="e246e-198">Følg denne fremgangsmåten for å vise, legge til eller fjerne gruppetilordninger for en valgt vare.</span><span class="sxs-lookup"><span data-stu-id="e246e-198">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="e246e-199">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="e246e-199">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="e246e-200">Velg varen du vil arbeide med.</span><span class="sxs-lookup"><span data-stu-id="e246e-200">Select the item to work with.</span></span>
1. <span data-ttu-id="e246e-201">I handlingsruten, på fanen **Produkt**, i **Rabattbehandling**-gruppen, velger du **Rabattbehandlingsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="e246e-201">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="e246e-202">Siden **Rabattbehandlingsgrupper** vises med en liste over grupper som den valgte varen allerede hører til i.</span><span class="sxs-lookup"><span data-stu-id="e246e-202">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="e246e-203">Hvis du vil legge til varen i en ny gruppe, velger du **Ny** i handlingsruten for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="e246e-203">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="e246e-204">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="e246e-204">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e246e-205">**Rabattbehandlingsgruppe** – Velg gruppen du vil legge til varen i.</span><span class="sxs-lookup"><span data-stu-id="e246e-205">**Rebate management group** – Select the group to add the item to.</span></span>
    - <span data-ttu-id="e246e-206">**Beskrivelse** – Angi en beskrivelse av gruppen (for eksempel for å forklare hvorfor varen er medlem av den).</span><span class="sxs-lookup"><span data-stu-id="e246e-206">**Description** – Enter a description of the group (for example, to explain why the item is a member of it).</span></span>

1. <span data-ttu-id="e246e-207">Hvis du vil fjerne en vare fra en gruppe, velger du gruppen og velger deretter **Slett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e246e-207">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="e246e-208">Følg denne fremgangsmåten for å legge til varer i en gruppe basert på kategorihierarkiet.</span><span class="sxs-lookup"><span data-stu-id="e246e-208">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="e246e-209">Gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Varegrupper**.</span><span class="sxs-lookup"><span data-stu-id="e246e-209">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="e246e-210">Velg gruppen som skal administreres.</span><span class="sxs-lookup"><span data-stu-id="e246e-210">Select the group to manage.</span></span>
1. <span data-ttu-id="e246e-211">Velg **Legg til varer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e246e-211">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="e246e-212">I dialogboksen **Legg til varer**, i feltet **Kategorihierarki**, velger du en kategori på øverste nivå.</span><span class="sxs-lookup"><span data-stu-id="e246e-212">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="e246e-213">Varehierarkiet åpnes i den venstre ruten.</span><span class="sxs-lookup"><span data-stu-id="e246e-213">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="e246e-214">Velg hierarkinivået du vil se etter.</span><span class="sxs-lookup"><span data-stu-id="e246e-214">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="e246e-215">Varer fra det valgte hierarkiet og hierarkinivået vises nå i høyre rute.</span><span class="sxs-lookup"><span data-stu-id="e246e-215">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="e246e-216">Følg denne fremgangsmåten for å arbeide med ruten:</span><span class="sxs-lookup"><span data-stu-id="e246e-216">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="e246e-217">Merk av i avmerkingsboksen for hver vare du vil legge til.</span><span class="sxs-lookup"><span data-stu-id="e246e-217">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="e246e-218">Merk av i avmerkingsboksen på rutenetthodet for å velge alle varene som vises på listen.</span><span class="sxs-lookup"><span data-stu-id="e246e-218">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="e246e-219">Velg **Vis valgt**-knappen for å filtrere rutenettet slik at den bare viser varene du har valgt så langt.</span><span class="sxs-lookup"><span data-stu-id="e246e-219">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="e246e-220">Velg knappen på nytt for å gå tilbake til den fullstendige listen.</span><span class="sxs-lookup"><span data-stu-id="e246e-220">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="e246e-221">Velg **OK** for å bruke varevalget på den valgte gruppen.</span><span class="sxs-lookup"><span data-stu-id="e246e-221">Select **OK** to apply your item selection to the selected group.</span></span>
