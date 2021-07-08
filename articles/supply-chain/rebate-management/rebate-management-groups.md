---
title: Rabattbehandlingsgrupper
description: Dette emnet beskriver hvordan du setter opp rabattbehandlingsgrupper. Rabattbehandlingsgrupper kan brukes under rabattberegninger, og kan knyttes til en hovedoppføring.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee5a195b3d2881ff70fb1f0d4063ed681e874648
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271083"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="214f3-104">Rabattbehandlingsgrupper</span><span class="sxs-lookup"><span data-stu-id="214f3-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="214f3-105">Beregninger av rabattbehandling kan drives av grupper.</span><span class="sxs-lookup"><span data-stu-id="214f3-105">Rebate management calculations can be driven by groups.</span></span> <span data-ttu-id="214f3-106">Rabattbehandlingsgrupper kan opprettes for kunder, leverandører og varer.</span><span class="sxs-lookup"><span data-stu-id="214f3-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="214f3-107">De kan knyttes til en hovedoppføring.</span><span class="sxs-lookup"><span data-stu-id="214f3-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="214f3-108">Rabattbehandlingskundegrupper</span><span class="sxs-lookup"><span data-stu-id="214f3-108">Rebate management customer groups</span></span>

<span data-ttu-id="214f3-109">Beregningen for en gruppe kunder opprettes ofte for en kjede av firmaer, for eksempel en butikkjede eller et franchisefirma.</span><span class="sxs-lookup"><span data-stu-id="214f3-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="214f3-110">Denne typen beregning er vanligvis knyttet til en rabatt.</span><span class="sxs-lookup"><span data-stu-id="214f3-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="214f3-111">Et fradrag beregnes ofte uten å vurdere hvem den kvalifiserende ordren ble solgt til.</span><span class="sxs-lookup"><span data-stu-id="214f3-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="214f3-112">Det finnes imidlertid noen unntak.</span><span class="sxs-lookup"><span data-stu-id="214f3-112">However, there are exceptions.</span></span> <span data-ttu-id="214f3-113">En lisenstaker kan for eksempel opprette en fradragsplan der kundegruppe A mottar 4 prosent, men kundegruppe B mottar bare 3 prosent.</span><span class="sxs-lookup"><span data-stu-id="214f3-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="214f3-114">Definer kundegrupper</span><span class="sxs-lookup"><span data-stu-id="214f3-114">Set up customer groups</span></span>

<span data-ttu-id="214f3-115">Hvis du vil arbeide med kundegrupper for rabattstyring, kan du gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Kundegrupper**.</span><span class="sxs-lookup"><span data-stu-id="214f3-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="214f3-116">Du kan bruke knappene i handlingsruten til å legge til og fjerne grupper etter behov.</span><span class="sxs-lookup"><span data-stu-id="214f3-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="214f3-117">For hver gruppe angir du feltene nedenfor:</span><span class="sxs-lookup"><span data-stu-id="214f3-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="214f3-118">**Rabattbehandlingsgruppe** – Angi et unikt navn for gruppen.</span><span class="sxs-lookup"><span data-stu-id="214f3-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="214f3-119">**Beskrivelse** – Angi en beskrivelse av gruppen for å få mer informasjon om hvordan den skal brukes.</span><span class="sxs-lookup"><span data-stu-id="214f3-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="214f3-120">Administrer tilordninger av kundegrupper</span><span class="sxs-lookup"><span data-stu-id="214f3-120">Manage customer group assignments</span></span>

<span data-ttu-id="214f3-121">Hver kunde kan tilhøre et hvilket som helst antall rabattbehandlingsgrupper.</span><span class="sxs-lookup"><span data-stu-id="214f3-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="214f3-122">Hvis du vil vise og tilordne gruppemedlemmer, kan du starte fra enten gruppelisten eller kundelisten.</span><span class="sxs-lookup"><span data-stu-id="214f3-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="214f3-123">Følg denne fremgangsmåten for å vise, legge til eller fjerne kunder for en valgt gruppe.</span><span class="sxs-lookup"><span data-stu-id="214f3-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="214f3-124">Gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Kundegrupper**.</span><span class="sxs-lookup"><span data-stu-id="214f3-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="214f3-125">Velg gruppen som skal administreres.</span><span class="sxs-lookup"><span data-stu-id="214f3-125">Select the group to manage.</span></span>
1. <span data-ttu-id="214f3-126">Velg **Kunder** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="214f3-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="214f3-127">Siden **Rabattbehandlingsgrupper** vises med en liste over kunder som allerede er medlemmer av den valgte gruppen.</span><span class="sxs-lookup"><span data-stu-id="214f3-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="214f3-128">Hvis du vil legge til en ny kunde i gruppen, velger du **Ny** i handlingsruten for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="214f3-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="214f3-129">Angi deretter følgende felt for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="214f3-129">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="214f3-130">**Kundekonto** – Velg kundekonto-ID-en.</span><span class="sxs-lookup"><span data-stu-id="214f3-130">**Customer account** – Select the customer account ID.</span></span>

1. <span data-ttu-id="214f3-131">Hvis du vil fjerne en kunde fra gruppen, velger du kunden og velger deretter **Slett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="214f3-131">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="214f3-132">Følg denne fremgangsmåten for å vise, legge til eller fjerne gruppetilordninger for en valgt kunde.</span><span class="sxs-lookup"><span data-stu-id="214f3-132">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="214f3-133">Gå til **Kunder \> Kunder \> Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="214f3-133">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="214f3-134">Velg kunden du vil arbeide med.</span><span class="sxs-lookup"><span data-stu-id="214f3-134">Select the customer to work with.</span></span>
1. <span data-ttu-id="214f3-135">I handlingsruten, på fanen **Kunde**, i **Rabattbehandling**-gruppen, velger du **Rabattbehandlingsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="214f3-135">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="214f3-136">Siden **Rabattbehandlingsgrupper** vises med en liste over grupper som den valgte kunden allerede hører til i.</span><span class="sxs-lookup"><span data-stu-id="214f3-136">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="214f3-137">Hvis du vil legge til kunden i en ny gruppe, velger du **Ny** i handlingsruten for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="214f3-137">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="214f3-138">Angi deretter følgende felt for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="214f3-138">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="214f3-139">**Rabattbehandlingsgruppe** – Velg gruppen du vil legge til kunden i.</span><span class="sxs-lookup"><span data-stu-id="214f3-139">**Rebate management group** – Select the group to add the customer to.</span></span>

1. <span data-ttu-id="214f3-140">Hvis du vil fjerne en kunde fra en gruppe, velger du gruppen og velger deretter **Slett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="214f3-140">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="214f3-141">Rabattbehandlingsleverandørgrupper</span><span class="sxs-lookup"><span data-stu-id="214f3-141">Rebate management vendor groups</span></span>

<span data-ttu-id="214f3-142">Beregningen for en gruppe med leverandører opprettes ofte for en gruppe med leveringspunkter.</span><span class="sxs-lookup"><span data-stu-id="214f3-142">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="214f3-143">Denne typen beregning er vanligvis knyttet til en rabatt.</span><span class="sxs-lookup"><span data-stu-id="214f3-143">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="214f3-144">Definer leverandørgrupper</span><span class="sxs-lookup"><span data-stu-id="214f3-144">Set up vendor groups</span></span>

<span data-ttu-id="214f3-145">Hvis du vil arbeide med leverandørgrupper for rabattstyring, kan du gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Leverandørgrupper**.</span><span class="sxs-lookup"><span data-stu-id="214f3-145">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="214f3-146">Du kan bruke knappene i handlingsruten til å legge til og fjerne grupper etter behov.</span><span class="sxs-lookup"><span data-stu-id="214f3-146">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="214f3-147">For hver gruppe angir du feltene nedenfor:</span><span class="sxs-lookup"><span data-stu-id="214f3-147">For each group, set the following fields:</span></span>

- <span data-ttu-id="214f3-148">**Rabattbehandlingsgruppe** – Angi et unikt navn for gruppen.</span><span class="sxs-lookup"><span data-stu-id="214f3-148">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="214f3-149">**Beskrivelse** – Angi en beskrivelse av gruppen for å få mer informasjon om hvordan den skal brukes.</span><span class="sxs-lookup"><span data-stu-id="214f3-149">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="214f3-150">Administrer tilordninger av leverandørgrupper</span><span class="sxs-lookup"><span data-stu-id="214f3-150">Manage vendor group assignments</span></span>

<span data-ttu-id="214f3-151">Hver leverandør kan tilhøre et hvilket som helst antall rabattbehandlingsgrupper.</span><span class="sxs-lookup"><span data-stu-id="214f3-151">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="214f3-152">Hvis du vil vise og tilordne gruppemedlemmer, kan du starte fra enten gruppelisten eller leverandørlisten.</span><span class="sxs-lookup"><span data-stu-id="214f3-152">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="214f3-153">Følg denne fremgangsmåten for å vise, legge til eller fjerne leverandører for en valgt gruppe.</span><span class="sxs-lookup"><span data-stu-id="214f3-153">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="214f3-154">Gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Leverandørgrupper**.</span><span class="sxs-lookup"><span data-stu-id="214f3-154">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="214f3-155">Velg gruppen som skal administreres.</span><span class="sxs-lookup"><span data-stu-id="214f3-155">Select the group to manage.</span></span>
1. <span data-ttu-id="214f3-156">Velg **Leverandører** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="214f3-156">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="214f3-157">Siden **Rabattbehandlingsgrupper** vises med en liste over leverandører som allerede er medlemmer av den valgte gruppen.</span><span class="sxs-lookup"><span data-stu-id="214f3-157">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="214f3-158">Hvis du vil legge til en ny leverandør i en gruppe, velger du **Ny** i handlingsruten for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="214f3-158">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="214f3-159">Angi deretter følgende felt for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="214f3-159">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="214f3-160">**Leverandørkonto** – Velg leverandørkonto-ID-en.</span><span class="sxs-lookup"><span data-stu-id="214f3-160">**Vendor account** – Select the vendor account ID.</span></span>

1. <span data-ttu-id="214f3-161">Hvis du vil fjerne en leverandør fra gruppen, velger du leverandøren og velger deretter **Slett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="214f3-161">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="214f3-162">Følg denne fremgangsmåten for å vise, legge til eller fjerne gruppetilordninger for en valgt leverandør.</span><span class="sxs-lookup"><span data-stu-id="214f3-162">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="214f3-163">Gå til **Leverandører \> Leverandører \> Alle leverandører**.</span><span class="sxs-lookup"><span data-stu-id="214f3-163">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="214f3-164">Velg leverandøren du vil arbeide med.</span><span class="sxs-lookup"><span data-stu-id="214f3-164">Select the vendor to work with.</span></span>
1. <span data-ttu-id="214f3-165">I handlingsruten, på fanen **Leverandør**, i **Rabattbehandling**-gruppen, velger du **Rabattbehandlingsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="214f3-165">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="214f3-166">Siden **Rabattbehandlingsgrupper** vises med en liste over grupper som den valgte leverandøren allerede hører til i.</span><span class="sxs-lookup"><span data-stu-id="214f3-166">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="214f3-167">Hvis du vil legge til leverandøren i en ny gruppe, velger du **Ny** i handlingsruten for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="214f3-167">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="214f3-168">Angi deretter følgende felt for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="214f3-168">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="214f3-169">**Rabattbehandlingsgruppe** – Velg gruppen du vil legge til leverandøren i.</span><span class="sxs-lookup"><span data-stu-id="214f3-169">**Rebate management group** – Select the group to add the vendor to.</span></span>

1. <span data-ttu-id="214f3-170">Hvis du vil fjerne en leverandør fra en gruppe, velger du gruppen og velger deretter **Slett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="214f3-170">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="214f3-171">Varerabattgrupper</span><span class="sxs-lookup"><span data-stu-id="214f3-171">Item rebate groups</span></span>

<span data-ttu-id="214f3-172">Ved å gruppere varer har du mer fleksibilitet når rabatter og fradrag beregnes.</span><span class="sxs-lookup"><span data-stu-id="214f3-172">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="214f3-173">Denne fremgangsmåten er ofte en mer effektiv måte å definere rabatter og fradrag for kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="214f3-173">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="214f3-174">Definer varegrupper</span><span class="sxs-lookup"><span data-stu-id="214f3-174">Set up item groups</span></span>

<span data-ttu-id="214f3-175">Hvis du vil arbeide med varegrupper for rabattstyring, kan du gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Varegrupper**.</span><span class="sxs-lookup"><span data-stu-id="214f3-175">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="214f3-176">Du kan bruke knappene i handlingsruten til å legge til og fjerne grupper etter behov.</span><span class="sxs-lookup"><span data-stu-id="214f3-176">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="214f3-177">For hver gruppe angir du feltene nedenfor:</span><span class="sxs-lookup"><span data-stu-id="214f3-177">For each group, set the following fields:</span></span>

- <span data-ttu-id="214f3-178">**Rabattbehandlingsgruppe** – Angi et unikt navn for gruppen.</span><span class="sxs-lookup"><span data-stu-id="214f3-178">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="214f3-179">**Beskrivelse** – Angi en beskrivelse av gruppen for å få mer informasjon om hvordan den skal brukes.</span><span class="sxs-lookup"><span data-stu-id="214f3-179">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="214f3-180">Administrer tilordninger av varegrupper</span><span class="sxs-lookup"><span data-stu-id="214f3-180">Manage item group assignments</span></span>

<span data-ttu-id="214f3-181">Hver vare kan tilhøre et hvilket som helst antall rabattbehandlingsgrupper.</span><span class="sxs-lookup"><span data-stu-id="214f3-181">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="214f3-182">Hvis du vil vise og tilordne gruppemedlemmer, kan du starte fra enten gruppelisten eller varelisten.</span><span class="sxs-lookup"><span data-stu-id="214f3-182">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="214f3-183">Du kan også legge til varer basert på kategorihierarkiet.</span><span class="sxs-lookup"><span data-stu-id="214f3-183">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="214f3-184">Følg denne fremgangsmåten for å vise, legge til eller fjerne varer for en valgt gruppe.</span><span class="sxs-lookup"><span data-stu-id="214f3-184">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="214f3-185">Gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Varegrupper**.</span><span class="sxs-lookup"><span data-stu-id="214f3-185">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="214f3-186">Velg gruppen som skal administreres.</span><span class="sxs-lookup"><span data-stu-id="214f3-186">Select the group to manage.</span></span>
1. <span data-ttu-id="214f3-187">Velg **Varer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="214f3-187">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="214f3-188">Siden **Rabattbehandlingsgrupper** vises med en liste over varer som allerede er medlemmer av den valgte gruppen.</span><span class="sxs-lookup"><span data-stu-id="214f3-188">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="214f3-189">Hvis du vil legge til en ny vare i gruppen, velger du **Ny** i handlingsruten for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="214f3-189">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="214f3-190">Angi deretter følgende felt for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="214f3-190">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="214f3-191">**Varekonto** – Velg varekonto-ID-en.</span><span class="sxs-lookup"><span data-stu-id="214f3-191">**Item account** – Select the item account ID.</span></span>

1. <span data-ttu-id="214f3-192">Hvis du vil fjerne en vare fra gruppen, velger du varen og velger deretter **Slett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="214f3-192">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="214f3-193">Følg denne fremgangsmåten for å vise, legge til eller fjerne gruppetilordninger for en valgt vare.</span><span class="sxs-lookup"><span data-stu-id="214f3-193">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="214f3-194">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="214f3-194">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="214f3-195">Velg varen du vil arbeide med.</span><span class="sxs-lookup"><span data-stu-id="214f3-195">Select the item to work with.</span></span>
1. <span data-ttu-id="214f3-196">I handlingsruten, på fanen **Produkt**, i **Rabattbehandling**-gruppen, velger du **Rabattbehandlingsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="214f3-196">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="214f3-197">Siden **Rabattbehandlingsgrupper** vises med en liste over grupper som den valgte varen allerede hører til i.</span><span class="sxs-lookup"><span data-stu-id="214f3-197">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="214f3-198">Hvis du vil legge til varen i en ny gruppe, velger du **Ny** i handlingsruten for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="214f3-198">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="214f3-199">Angi deretter følgende felt for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="214f3-199">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="214f3-200">**Rabattbehandlingsgruppe** – Velg gruppen du vil legge til varen i.</span><span class="sxs-lookup"><span data-stu-id="214f3-200">**Rebate management group** – Select the group to add the item to.</span></span>

1. <span data-ttu-id="214f3-201">Hvis du vil fjerne en vare fra en gruppe, velger du gruppen og velger deretter **Slett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="214f3-201">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="214f3-202">Følg denne fremgangsmåten for å legge til varer i en gruppe basert på kategorihierarkiet.</span><span class="sxs-lookup"><span data-stu-id="214f3-202">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="214f3-203">Gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Varegrupper**.</span><span class="sxs-lookup"><span data-stu-id="214f3-203">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="214f3-204">Velg gruppen som skal administreres.</span><span class="sxs-lookup"><span data-stu-id="214f3-204">Select the group to manage.</span></span>
1. <span data-ttu-id="214f3-205">Velg **Legg til varer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="214f3-205">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="214f3-206">I dialogboksen **Legg til varer**, i feltet **Kategorihierarki**, velger du en kategori på øverste nivå.</span><span class="sxs-lookup"><span data-stu-id="214f3-206">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="214f3-207">Varehierarkiet åpnes i den venstre ruten.</span><span class="sxs-lookup"><span data-stu-id="214f3-207">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="214f3-208">Velg hierarkinivået du vil se etter.</span><span class="sxs-lookup"><span data-stu-id="214f3-208">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="214f3-209">Varer fra det valgte hierarkiet og hierarkinivået vises nå i høyre rute.</span><span class="sxs-lookup"><span data-stu-id="214f3-209">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="214f3-210">Følg denne fremgangsmåten for å arbeide med ruten:</span><span class="sxs-lookup"><span data-stu-id="214f3-210">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="214f3-211">Merk av i avmerkingsboksen for hver vare du vil legge til.</span><span class="sxs-lookup"><span data-stu-id="214f3-211">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="214f3-212">Merk av i avmerkingsboksen på rutenetthodet for å velge alle varene som vises på listen.</span><span class="sxs-lookup"><span data-stu-id="214f3-212">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="214f3-213">Velg **Vis valgt**-knappen for å filtrere rutenettet slik at den bare viser varene du har valgt så langt.</span><span class="sxs-lookup"><span data-stu-id="214f3-213">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="214f3-214">Velg knappen på nytt for å gå tilbake til den fullstendige listen.</span><span class="sxs-lookup"><span data-stu-id="214f3-214">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="214f3-215">Velg **OK** for å bruke varevalget på den valgte gruppen.</span><span class="sxs-lookup"><span data-stu-id="214f3-215">Select **OK** to apply your item selection to the selected group.</span></span>
