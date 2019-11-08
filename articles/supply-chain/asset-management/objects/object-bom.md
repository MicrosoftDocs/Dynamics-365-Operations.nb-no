---
title: Stykklister for aktiva
description: Dette emnet beskriver stykklister for aktiva i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 02686c97a19fa86c3ea93d7c400067f0855b5c4d
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571490"
---
# <a name="asset-boms"></a><span data-ttu-id="494f8-103">Stykklister for aktiva</span><span class="sxs-lookup"><span data-stu-id="494f8-103">Asset BOMs</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="494f8-104">Dette emnet beskriver stykklister for aktiva i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="494f8-104">This topic describes asset bills of materials (BOMs) in Asset Management.</span></span> <span data-ttu-id="494f8-105">Siden **Stykklister for aktiva** viser en liste over alle varer (reservedeler og andre varer) som brukes på et aktivum i løpet av hele levetiden.</span><span class="sxs-lookup"><span data-stu-id="494f8-105">The **Asset BOM** page shows a list of all items (spare parts and other items) that are used on an asset during its whole lifetime.</span></span> <span data-ttu-id="494f8-106">Når du oppretter et nytt aktivum, bør du vurdere å definere en stykkliste for aktiva som en del av installasjonsprosedyren.</span><span class="sxs-lookup"><span data-stu-id="494f8-106">When you create a new asset, you should consider setting up an asset BOM as a part of the setup procedure.</span></span> <span data-ttu-id="494f8-107">På denne måten kan du spore vareloggen for aktivaet fra opprettelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="494f8-107">In this way, you can track item history for the asset from the creation date.</span></span>

<span data-ttu-id="494f8-108">Når du har fullført en vedlikeholdsjobb, og vareforbruket er registrert på en arbeidsordre, kan du spore forbruk av reservedeler og andre varer som brukes på aktivumet.</span><span class="sxs-lookup"><span data-stu-id="494f8-108">After you've completed a maintenance job, and item consumption has been registered on a work order, you can track consumption of spare parts and other items that are used on the asset.</span></span> <span data-ttu-id="494f8-109">Med denne funksjonen kan du beholde en fullstendig vareforbrukspost for alle ressursene dine.</span><span class="sxs-lookup"><span data-stu-id="494f8-109">This functionality lets you keep a complete item consumption record for all your assets.</span></span> <span data-ttu-id="494f8-110">Du kan for eksempel bruke posten til å overvåke om en bestemt reservedel ofte erstattes, eller til å holde rede på reservedelene eller andre elementer som for øyeblikket brukes på et anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="494f8-110">For example, you can use the record to monitor whether a specific spare part is often replaced, or to keep track of the spare parts or other items that are currently used on an asset.</span></span>

> [!NOTE]
> <span data-ttu-id="494f8-111">På en Arbeidsordre kan vareforbruk inkludere både reservedeler og andre tilleggsvarer, for eksempel smøremidler, bolter og pakninger.</span><span class="sxs-lookup"><span data-stu-id="494f8-111">On a work order, item consumption might include both spare parts and other, additional items, such as lubricants, bolts, and gaskets.</span></span>

<span data-ttu-id="494f8-112">En STYKKLISTE for aktiva kan oppdateres automatisk basert på oppsettet i Asset Management.</span><span class="sxs-lookup"><span data-stu-id="494f8-112">An asset BOM can be automatically updated based on the setup in Asset Management.</span></span> <span data-ttu-id="494f8-113">Hvis en livsløpstilstand for arbeidsordre er opprettet for å håndtere fullførte arbeidsordrer, og hvis alternativet **Oppdater stykkliste for aktiva** er satt til **Ja** på siden **Livsløpstilstander for arbeidsordre**, oppdateres alle varer som brukes i arbeidsordren, automatisk på siden **Stykkliste for aktiva** når arbeidsordren oppdateres til denne livsløpstilstanden.</span><span class="sxs-lookup"><span data-stu-id="494f8-113">If a work order lifecycle state has been created to handle finished or completed work orders, and if the **Update asset BOM** option for that work order lifecycle state is set to **Yes** on the **Work order lifecycle states** page, all items that are used on the work order will be automatically updated on the **Asset BOM** page when the work order is updated to that lifecycle state.</span></span> 


<span data-ttu-id="494f8-114">Du kan også oppdatere en stykkliste for aktiva manuelt ved å opprette nye varelinjer på siden **Stykkliste for aktiva**.</span><span class="sxs-lookup"><span data-stu-id="494f8-114">You can also manually update an asset BOM by creating new item lines on the **Asset BOM** page.</span></span>

<span data-ttu-id="494f8-115">På siden **Stykkliste for aktiva** kan du spore historikk for reservedeler for aktiva etter at vareforbruk er registrert på en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="494f8-115">On the **Asset BOM** page, you can track spare parts history for assets after item consumption is registered on a work order.</span></span> <span data-ttu-id="494f8-116">Hvis du vil bruke denne funksjonaliteten, må du velge varegruppene som skal brukes til reservedelsregistrering på siden **Varegrupper for reservedeler**.</span><span class="sxs-lookup"><span data-stu-id="494f8-116">To use this functionality, you must select the item groups that should be used for spare parts registration on the **Spare parts item groups** page.</span></span>

<span data-ttu-id="494f8-117">Hvis du vil bruke funksjonaliteten for stykkliste for aktiva, må du først definere de nødvendige varegruppene for reservedeler.</span><span class="sxs-lookup"><span data-stu-id="494f8-117">To use asset BOM functionality, you must first set up the required spare parts items groups.</span></span> <span data-ttu-id="494f8-118">Hvis du vil at stykklisten for aktiva skal oppdateres automatisk når en arbeidsordre er fullført, kan du definere en livsløpstilstand for arbeidsordre for å håndtere denne oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="494f8-118">Then, if you want the asset BOM to be automatically updated when a work order is completed, you can set up a work order lifecycle state to handle that update.</span></span> 


## <a name="set-up-spare-parts-item-groups"></a><span data-ttu-id="494f8-119">Definere varegrupper for reservedeler</span><span class="sxs-lookup"><span data-stu-id="494f8-119">Set up spare parts item groups</span></span>

<span data-ttu-id="494f8-120">Oppsettet av reservedelsloggen er basert på varegrupper som er opprettet i modulen **Lagerstyring**.</span><span class="sxs-lookup"><span data-stu-id="494f8-120">The setup of spare parts history is based on item groups that are created in the **Inventory and warehouse management** module.</span></span> <span data-ttu-id="494f8-121">I Aktivastyring definerer du varegrupper slik at du kan spore historikk for reservedeler for varene i de valgte varegruppene.</span><span class="sxs-lookup"><span data-stu-id="494f8-121">In Asset Management, you set up item groups so that you can track spare parts history for the items in the selected item groups.</span></span>

1. <span data-ttu-id="494f8-122">Velg **Aktivastyring** \> **Oppsett** \> **Aktivum** \> **Varegrupper for reservedeler**.</span><span class="sxs-lookup"><span data-stu-id="494f8-122">Select **Asset management** \> **Setup** \> **Asset** \> **Spare parts item groups**.</span></span>
2. <span data-ttu-id="494f8-123">Velg **Ny** for å definere en varegruppe.</span><span class="sxs-lookup"><span data-stu-id="494f8-123">Select **New** to set up an item group.</span></span>
3. <span data-ttu-id="494f8-124">Velg gruppen i **Varegruppe**-feltet.</span><span class="sxs-lookup"><span data-stu-id="494f8-124">In the **Item group** field, select the group.</span></span> <span data-ttu-id="494f8-125">Navnet på gruppen angis automatisk i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="494f8-125">The name of the group is automatically entered in the **Name** field.</span></span>

## <a name="view-and-update-asset-boms"></a><span data-ttu-id="494f8-126">Vis og oppdater stykklister for aktiva</span><span class="sxs-lookup"><span data-stu-id="494f8-126">View and update asset BOMs</span></span>

<span data-ttu-id="494f8-127">Når du bokfører vareforbruk på en arbeidsordre, kan du vise det registrerte vareforbruket på siden **Stykkliste for aktiva**.</span><span class="sxs-lookup"><span data-stu-id="494f8-127">After you post item consumption on a work order, you can view the registered item consumption on the **Asset BOM** page.</span></span>

1. <span data-ttu-id="494f8-128">Velg **Aktivastyring** \> **Felles** \> **Aktiva** \> **Aktive aktiva**.</span><span class="sxs-lookup"><span data-stu-id="494f8-128">Select **Asset management** \> **Common** \> **Assets** \> **Active assets**.</span></span> <span data-ttu-id="494f8-129">Velg aktivumet i listen, og velg **Stykkliste for aktiva**.</span><span class="sxs-lookup"><span data-stu-id="494f8-129">Select the asset in the list, and then select **Asset BOM**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="494f8-130">Hvis du vil vise alle vareforbruksregistreringer på alle aktiva, velger du **Aktivastyring** \> **Forespørsler** \> **Aktiva** \> **Stykkliste for aktiva**.</span><span class="sxs-lookup"><span data-stu-id="494f8-130">To view all item consumption registrations on all assets, select **Asset management** \> **Inquiries** \> **Assets** \> **Asset BOM**.</span></span>

2. <span data-ttu-id="494f8-131">Velg **Oppdater stykkliste for aktiva**.</span><span class="sxs-lookup"><span data-stu-id="494f8-131">Select **Update asset BOM**.</span></span> <span data-ttu-id="494f8-132">Du kan legge til aktiva, aktivatyper og ressurser i oppdateringen etter behov ved å velge **Velg.**</span><span class="sxs-lookup"><span data-stu-id="494f8-132">You can add assets, asset types, and resources to the update as you require by selecting **Select**.</span></span> <span data-ttu-id="494f8-133">Velg **OK** for å starte oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="494f8-133">Select **OK** to start the update.</span></span> <span data-ttu-id="494f8-134">Du kan også definere oppdateringsfunksjonen som en satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="494f8-134">You can also set up the Update function as a batch job.</span></span>
3. <span data-ttu-id="494f8-135">Hvis du vil se mer informasjon som er knyttet til varene, kan du legge til lagerdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="494f8-135">If you want to see more information that is related to the items, you can add inventory dimensions.</span></span> <span data-ttu-id="494f8-136">Velg **Beholdning** \> **Dimensjonsvisning**, og merk deretter av i boksene for dimensjonene du vil se.</span><span class="sxs-lookup"><span data-stu-id="494f8-136">Select **Inventory** \> **Dimensions display**, and then select the check boxes for the dimensions that you want to see.</span></span> <span data-ttu-id="494f8-137">Hvis du vil beholde dette oppsettet for alle aktiva på siden **Stykkliste for aktiva**, setter du **Lagre oppsett** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="494f8-137">To keep this setup for all assets on the **Asset BOM** page, set the **Save setup** option to **Yes**.</span></span>
4. <span data-ttu-id="494f8-138">Hvis du vil ha en oversikt over hvor i Aktivastyring varen på den valgte linjen brukes, i forhold til aktiva, jobbtype standarder, reservedeler og arbeidsordrer, velger du **Vare der brukt**.</span><span class="sxs-lookup"><span data-stu-id="494f8-138">To get an overview of where in Asset Management the item on the selected line is used, in relation to assets, job type defaults, spare parts, and work orders, select **Item where used**.</span></span> 
5. <span data-ttu-id="494f8-139">Hvis du bare vil se aktive varelinjer, velger du **Vis** \> **Gjeldende**.</span><span class="sxs-lookup"><span data-stu-id="494f8-139">If you want to see only active item lines, select **View** \> **Current**.</span></span> <span data-ttu-id="494f8-140">Hvis du vil se alle varelinjer, inkludert linjer der utløpsdatoen er tidligere enn gjeldende dato, velger du **Vis** \> **Alle**.</span><span class="sxs-lookup"><span data-stu-id="494f8-140">To see all item lines, including lines where the expiration date is earlier than the current date, select **View** \> **All**.</span></span>

> [!NOTE]
> <span data-ttu-id="494f8-141">Når du har fullført en arbeidsordre, og hvis noen varer eller reservedeler som er relatert til det relaterte aktivumet er utløpt eller har blitt erstattet av andre varer eller reservedeler, anbefaler vi at du oppdaterer stykklisten for aktiva tilsvarende.</span><span class="sxs-lookup"><span data-stu-id="494f8-141">When you've completed a work order, if some items or spare parts that are related to the related asset have expired or have been replaced by other items or spare parts, we recommend that you update the asset BOM accordingly.</span></span>

## <a name="create-a-new-item-line-in-an-asset-bom"></a><span data-ttu-id="494f8-142">Opprette en ny varelinje i en stykkliste for aktiva</span><span class="sxs-lookup"><span data-stu-id="494f8-142">Create a new item line in an asset BOM</span></span>

<span data-ttu-id="494f8-143">Du kan opprette varelinjer manuelt for aktiva.</span><span class="sxs-lookup"><span data-stu-id="494f8-143">You can manually create item lines for assets.</span></span>

1. <span data-ttu-id="494f8-144">Velg **Ny** på siden **Stykkliste for aktiva**.</span><span class="sxs-lookup"><span data-stu-id="494f8-144">On the **Asset BOM** page, select **New**.</span></span>
2. <span data-ttu-id="494f8-145">Velg aktivaet du vil legge til en varelinje for, i **Aktivum**-feltet.</span><span class="sxs-lookup"><span data-stu-id="494f8-145">In the **Asset** field, select the asset to add an item line for.</span></span>
3. <span data-ttu-id="494f8-146">Angi et sekvensielt linjenummer i feltet **Linjenummer**.</span><span class="sxs-lookup"><span data-stu-id="494f8-146">In the **Line number** field, enter a sequential line number.</span></span>
4. <span data-ttu-id="494f8-147">I **Gyldig**-feltet angir du en startdato for varen.</span><span class="sxs-lookup"><span data-stu-id="494f8-147">In the **Effective** field, enter a start date for the item.</span></span>
5. <span data-ttu-id="494f8-148">Hvis varen utløper, angir du en sluttdato i **Utløp**-feltet.</span><span class="sxs-lookup"><span data-stu-id="494f8-148">If the item will expire, in the **Expiration** field, enter an end date.</span></span>
6. <span data-ttu-id="494f8-149">Velg varen i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="494f8-149">In the **Item number** field, select the item.</span></span> <span data-ttu-id="494f8-150">Navnet angis automatisk i **Produktnavn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="494f8-150">The name is automatically entered in the **Product name** field.</span></span>
7. <span data-ttu-id="494f8-151">Angi antallet som brukes, i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="494f8-151">In the **Quantity** field, enter the quantity that is used.</span></span> <span data-ttu-id="494f8-152">**Enhet**-feltet oppdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="494f8-152">The **Unit** field is automatically updated.</span></span>
