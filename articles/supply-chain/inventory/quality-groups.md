---
title: Varekvalitetsgrupper
description: Dette emnet beskriver hvordan du kan bruke og opprette varekvalitetsgrupper for logisk å gruppere produkter slik at de kan tilordnes til kvalitetstilknytninger for automatisk generering av kvalitetsordrer.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272cb748e0a2722d9744fe6b357d767a1d6aeb26
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022258"
---
# <a name="item-quality-groups"></a><span data-ttu-id="724e8-103">Varekvalitetsgrupper</span><span class="sxs-lookup"><span data-stu-id="724e8-103">Item quality groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="724e8-104">En kvalitetsgruppe representerer felles testkrav for varer.</span><span class="sxs-lookup"><span data-stu-id="724e8-104">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="724e8-105">Dette emnet beskriver hvordan du kan bruke og opprette varekvalitetsgrupper for logisk å gruppere produkter slik at de kan tilordnes til kvalitetstilknytninger for automatisk generering av kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="724e8-105">This topic describes how to use and create item quality groups to logically group products so that they can be assigned to quality associations for the automatic generation of quality orders.</span></span>

<span data-ttu-id="724e8-106">Gå til **Lagerstyring \> Oppsett \> Kvalitetsgrupper** for å definere, redigere og vise varene som er tilordnet til en kvalitetsgruppe, eller kvalitetsgruppene som er tilordnet til en vare.</span><span class="sxs-lookup"><span data-stu-id="724e8-106">To set up, edit, and view the items that are assigned to a quality group, or the quality groups that are assigned to an item, go to **Inventory management \> Setup \> Quality groups**.</span></span> <span data-ttu-id="724e8-107">Når du har definert testkravene på siden **Testgrupper**, kan du definere reglene for automatisk generering av kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="724e8-107">After you define the test requirements on the **Test groups** page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="724e8-108">For å forenkle prosessen kan du ikke definere reglene for individuelle varer.</span><span class="sxs-lookup"><span data-stu-id="724e8-108">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="724e8-109">I stedet definerer du regler for en kvalitetsgruppe på siden **Kvalitetstilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="724e8-109">Instead, you can define the rules for a quality group on the **Quality associations** page.</span></span>

## <a name="example-of-an-item-quality-group"></a><span data-ttu-id="724e8-110">Eksempel på en varekvalitetsgruppe</span><span class="sxs-lookup"><span data-stu-id="724e8-110">Example of an item quality group</span></span>

<span data-ttu-id="724e8-111">Et produksjonsfirma kjøper inn ulike råmaterialer som har samme testkrav for innkommende inspeksjon.</span><span class="sxs-lookup"><span data-stu-id="724e8-111">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="724e8-112">Firmaet definerer derfor en kvalitetsgruppe og tilordner deretter varenumrene som er tilknyttet råvarene til denne gruppen.</span><span class="sxs-lookup"><span data-stu-id="724e8-112">Therefore, the company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="724e8-113">Senere kjøper selskapet en ny type råvarer som har samme testkrav.</span><span class="sxs-lookup"><span data-stu-id="724e8-113">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="724e8-114">I stedet for å opprette nye testkrav for det nye materialet, legger firmaet til varenummeret for det nye materialet i den eksisterende kvalitetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="724e8-114">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span>

<span data-ttu-id="724e8-115">Det samme firmaet produserer også varer med samme krav til produksjonstesting, og leverer varer med samme krav til utføring av tester før forsendelse.</span><span class="sxs-lookup"><span data-stu-id="724e8-115">The same company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="724e8-116">Firmaet definerer derfor to ekstra kvalitetsgrupper, og tilordner deretter de aktuelle varenumrene til hver gruppe.</span><span class="sxs-lookup"><span data-stu-id="724e8-116">Therefore, the company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="724e8-117">Opprette en kvalitetsgruppe</span><span class="sxs-lookup"><span data-stu-id="724e8-117">Create a quality group</span></span>

<span data-ttu-id="724e8-118">Hvis du vil opprette en kvalitetsgruppe, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="724e8-118">To create a quality group, follow these steps.</span></span>

1. <span data-ttu-id="724e8-119">Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Kvalitetsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="724e8-119">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="724e8-120">I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="724e8-120">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="724e8-121">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="724e8-121">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="724e8-122">**Kvalitetsgruppe** – Angi en unik ID eller et unikt navn for kvalitetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="724e8-122">**Quality group** – Enter a unique ID or name for the quality group.</span></span>
    - <span data-ttu-id="724e8-123">**Beskrivelse** – Angi en detaljert beskrivelse av kvalitetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="724e8-123">**Description** – Enter a detailed description of the quality group.</span></span>

1. <span data-ttu-id="724e8-124">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="724e8-124">Close the page.</span></span>

## <a name="manually-add-items-to-a-quality-group"></a><span data-ttu-id="724e8-125">Legge til varer i en kvalitetsgruppe manuelt</span><span class="sxs-lookup"><span data-stu-id="724e8-125">Manually add items to a quality group</span></span>

<span data-ttu-id="724e8-126">Følg denne fremgangsmåten for å legge til varer manuelt i en kvalitetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="724e8-126">To manually add items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="724e8-127">Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Kvalitetsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="724e8-127">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="724e8-128">Velg kvalitetsgruppen som du vil legge til varer i.</span><span class="sxs-lookup"><span data-stu-id="724e8-128">Select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="724e8-129">Velg **Varer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="724e8-129">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="724e8-130">Velg **Ny** i handlingsruten på siden **Varer i kvalitetsgrupper** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="724e8-130">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="724e8-131">Angi deretter **Varenummer**-feltet for den nye raden til varenummeret du vil legge til.</span><span class="sxs-lookup"><span data-stu-id="724e8-131">Then, for the new row, set the **Item number** field to the item number that you want to add.</span></span>
1. <span data-ttu-id="724e8-132">Gjenta det forrige trinnet for hver tilleggsvare du må legge til.</span><span class="sxs-lookup"><span data-stu-id="724e8-132">Repeat the previous step for each additional item that must be added.</span></span>
1. <span data-ttu-id="724e8-133">Lukk sidene.</span><span class="sxs-lookup"><span data-stu-id="724e8-133">Close the pages.</span></span>

## <a name="add-multiple-items-to-a-quality-group"></a><span data-ttu-id="724e8-134">Legge til flere varer i en kvalitetsgruppe</span><span class="sxs-lookup"><span data-stu-id="724e8-134">Add multiple items to a quality group</span></span>

<span data-ttu-id="724e8-135">Følg denne fremgangsmåten for å legge til flere varer i en kvalitetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="724e8-135">To add multiple items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="724e8-136">Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Kvalitetsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="724e8-136">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="724e8-137">Opprett eller velg kvalitetsgruppen som du vil legge til varer i.</span><span class="sxs-lookup"><span data-stu-id="724e8-137">Create or select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="724e8-138">Velg **Legg til varer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="724e8-138">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="724e8-139">I dialogboksen **Forespørsel** angir du filterkriteriene for varene du vil legge til.</span><span class="sxs-lookup"><span data-stu-id="724e8-139">In the **Inquiry** dialog box, enter the filter criteria for the items that you want to add.</span></span> <span data-ttu-id="724e8-140">Du kan for eksempel filtrere for alle varer i en bestemt varegruppe.</span><span class="sxs-lookup"><span data-stu-id="724e8-140">For example, you might filter for all items in a specific item group.</span></span>
1. <span data-ttu-id="724e8-141">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="724e8-141">Select **OK**.</span></span>
1. <span data-ttu-id="724e8-142">I dialogboksen **Legg til varer** viser et rutenett alle varene som samsvarer med spørringen.</span><span class="sxs-lookup"><span data-stu-id="724e8-142">In the **Add items** dialog box, a grid shows all the items that match your query.</span></span> <span data-ttu-id="724e8-143">Se gjennom resultatene.</span><span class="sxs-lookup"><span data-stu-id="724e8-143">Review the results.</span></span>

    <span data-ttu-id="724e8-144">Hvis det kreves endringer, velger du **Velg** for å gå tilbake til dialogboksen **Forespørsel**, og justerer spørringen.</span><span class="sxs-lookup"><span data-stu-id="724e8-144">If any changes are required, select **Select** to return to the **Inquiry** dialog box, and adjust your query.</span></span>

1. <span data-ttu-id="724e8-145">Når resultatene inkluderer alle varene du vil legge til, velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="724e8-145">When the results include all the items that you want to add, select **OK**.</span></span>
1. <span data-ttu-id="724e8-146">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="724e8-146">Close the page.</span></span>

## <a name="manually-associate-an-item-with-a-quality-group"></a><span data-ttu-id="724e8-147">Knytte en vare til en kvalitetsgruppe manuelt</span><span class="sxs-lookup"><span data-stu-id="724e8-147">Manually associate an item with a quality group</span></span>

<span data-ttu-id="724e8-148">Følg denne fremgangsmåten for å knytte til en vare manuelt i en kvalitetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="724e8-148">To manually associate an item with a quality group, follow these steps.</span></span>

1. <span data-ttu-id="724e8-149">Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Varekvalitetsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="724e8-149">Go to **Inventory management \> Setup \> Quality control \> Item quality groups**.</span></span>
1. <span data-ttu-id="724e8-150">I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="724e8-150">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="724e8-151">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="724e8-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="724e8-152">**Varenummer** – Velg varenummeret du vil legge til.</span><span class="sxs-lookup"><span data-stu-id="724e8-152">**Item number** – Select the item number to add.</span></span>
    - <span data-ttu-id="724e8-153">**Kvalitetsgruppe** – Velg kvalitetsgruppen som skal tilordnes varen.</span><span class="sxs-lookup"><span data-stu-id="724e8-153">**Quality group** – Select the quality group to assign to the item.</span></span>

1. <span data-ttu-id="724e8-154">Gjenta det forrige trinnet for hver ekstra kombinasjon av en vare og en kvalitetsgruppe som må legges til.</span><span class="sxs-lookup"><span data-stu-id="724e8-154">Repeat the previous step for each additional combination of an item and a quality group that must be added.</span></span>
1. <span data-ttu-id="724e8-155">Lukk sidene.</span><span class="sxs-lookup"><span data-stu-id="724e8-155">Close the pages.</span></span>

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a><span data-ttu-id="724e8-156">Legge til en kvalitetsgruppe manuelt fra Frigitte produkter-siden</span><span class="sxs-lookup"><span data-stu-id="724e8-156">Manually add a quality group from the Released products page</span></span>

<span data-ttu-id="724e8-157">Følg denne fremgangsmåten for å legge til en kvalitetsgruppe manuelt fra **Frigitte produkter**-siden.</span><span class="sxs-lookup"><span data-stu-id="724e8-157">To manually add a quality group from the **Released products** page, follow these steps.</span></span>

1. <span data-ttu-id="724e8-158">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="724e8-158">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="724e8-159">Velg produktet du vil tilordne en kvalitetsgruppe til.</span><span class="sxs-lookup"><span data-stu-id="724e8-159">Select the product that you want to assign a quality group to.</span></span>
1. <span data-ttu-id="724e8-160">I handlingsruten, i fanen **Administrer lager** i gruppen **Kvalitet**, velger du **Varekvalitetsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="724e8-160">On the Action Pane, on the **Manage inventory** tab, in the **Quality** group, select **Item quality groups**.</span></span>
1. <span data-ttu-id="724e8-161">Velg **Ny** i handlingsruten på siden **Varer i kvalitetsgrupper** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="724e8-161">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="724e8-162">Angi deretter **Kvalitetsgruppe**-feltet for den nye raden til kvalitetsgruppen du vil tilordne til produktet.</span><span class="sxs-lookup"><span data-stu-id="724e8-162">Then, for the new row, set the **Quality group** field to the quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="724e8-163">Gjenta det forrige trinnet for hver ekstra kvalitetsgruppe du vil tilordne til produktet.</span><span class="sxs-lookup"><span data-stu-id="724e8-163">Repeat the previous step for each additional quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="724e8-164">Lukk sidene.</span><span class="sxs-lookup"><span data-stu-id="724e8-164">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="724e8-165">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="724e8-165">Additional resources</span></span>

- [<span data-ttu-id="724e8-166">Testinstrumenter for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="724e8-166">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="724e8-167">Kvalitetsstyringstester</span><span class="sxs-lookup"><span data-stu-id="724e8-167">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="724e8-168">Testgrupper for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="724e8-168">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="724e8-169">Testvariabler for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="724e8-169">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="724e8-170">Kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="724e8-170">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
