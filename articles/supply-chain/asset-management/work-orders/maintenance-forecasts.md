---
title: Vedlikeholdsprognoser
description: Dette emnet beskriver vedlikeholdsprognoser i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2686dd6db032239e2a3aac03f3998cee055302f6
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/29/2020
ms.locfileid: "4434858"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="4057b-103">Vedlikeholdsprognoser</span><span class="sxs-lookup"><span data-stu-id="4057b-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="4057b-104">Når du oppretter en arbeidsordre, oppretter du arbeidsordrejobber med tilknyttede aktiva og vedlikeholdsjobbtyper.</span><span class="sxs-lookup"><span data-stu-id="4057b-104">When you create a work order, you create work order jobs that have related assets and maintenance job types.</span></span> <span data-ttu-id="4057b-105">Når du velger en vedlikeholdsjobbtype som inneholder vedlikeholdsprognoser, kopieres prognosene automatisk til arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="4057b-105">When you select a maintenance job type that contains maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="4057b-106">Det kan hende at du kan legge til prognoselinjer i en arbeidsordre eller slette dem fra en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="4057b-106">You might be able to add forecast lines to a work order or delete them from a work order.</span></span> <span data-ttu-id="4057b-107">Oppsettet for arbeidsordrelivssyklustilstanden, den tilknyttede prosjekttypen og stadiereglene som er knyttet til prosjekttypen, bestemmer om du kan legge til eller redigere prognoselinjer.</span><span class="sxs-lookup"><span data-stu-id="4057b-107">The setup of the work order lifecycle state, the related project type, and the stage rules that are related to the project type determine whether you can add or edit forecast lines.</span></span> <span data-ttu-id="4057b-108">Hvis du vil ha mer informasjon om livssyklustilstander for arbeidsordrer og relaterte prosjektstadier, kan du se [Prognoser, arbeidsordrer og prosjekter](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="4057b-108">For more information about work order lifecycle states and related project stages, see [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

1. <span data-ttu-id="4057b-109">Velg **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="4057b-109">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="4057b-110">Velg arbeidsordren i listen, og deretter, i handlingsruten > kategorien **Arbeidsordre** > gruppen **Prosjekt** og deretter **Prognose**.</span><span class="sxs-lookup"><span data-stu-id="4057b-110">Select the work order in the list, and then, on the Action Pane > **Work order** tab > the **Project** group, select **Forecast**.</span></span> <span data-ttu-id="4057b-111">Siden **Vedlikeholdsprognose for arbeidsordre** viser prognoselinjer fra vedlikeholdsjobbtypen som velges i arbeidsordrejobben.</span><span class="sxs-lookup"><span data-stu-id="4057b-111">The **Work order maintenance forecast** page shows forecast lines from the maintenance job type that is selected on the work order job.</span></span>


## <a name="add-an-hours-forecast-to-a-work-order"></a><span data-ttu-id="4057b-112">Legge til prognose for timer i en arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="4057b-112">Add an hours forecast to a work order</span></span>

1. <span data-ttu-id="4057b-113">På siden **Prognose for vedlikehold av arbeidsordre** velger du arbeidsordrejobben du vil legge til en prognose i.</span><span class="sxs-lookup"><span data-stu-id="4057b-113">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="4057b-114">På hurtigfanen **Timer** velger du **Legg til** for å opprette en ny linje.</span><span class="sxs-lookup"><span data-stu-id="4057b-114">On the **Hours** FastTab, select **Add** to create a new line.</span></span>

3. <span data-ttu-id="4057b-115">Velg en kategori i feltet **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="4057b-115">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="4057b-116">Sett inn antall prognosetimer i **Timer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4057b-116">In the **Hours** field, enter the number of forecasted hours.</span></span>

5. <span data-ttu-id="4057b-117">I **Linjeegenskap**-feltet velger du tilleggstypen som skal brukes på linjen.</span><span class="sxs-lookup"><span data-stu-id="4057b-117">In the **Line property** field, select the type of charge that should be used on the line.</span></span>


## <a name="add-an-items-forecast-to-a-work-order"></a><span data-ttu-id="4057b-118">Legge til prognoser for varer i en arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="4057b-118">Add an items forecast to a work order</span></span>

<span data-ttu-id="4057b-119">Det er tre måter å legge til varer i en vedlikeholdsprognose for arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="4057b-119">There are three ways to add items to a work order maintenance forecast.</span></span> <span data-ttu-id="4057b-120">Du kan opprette linjer for varer (reservedeler) som ikke er inkludert i reservedellisten eller stykklisten for aktiva, du kan velge reservedeler fra listen over godkjente reservedeler, eller du kan velge varer fra stykklisten for aktiva.</span><span class="sxs-lookup"><span data-stu-id="4057b-120">You can create lines for items (spare parts) that aren't included on the spare parts list or the asset bill of materials (BOM), you can select spare parts from the approved spare parts list, or you can select items from the asset BOM.</span></span>

- <span data-ttu-id="4057b-121">På siden **Prognose for vedlikehold av arbeidsordre** velger du arbeidsordrejobben du vil legge til en prognose i.</span><span class="sxs-lookup"><span data-stu-id="4057b-121">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

- <span data-ttu-id="4057b-122">I hurtigfanen **Varer** legger du til varer i vedlikeholdsprognosen ved å bruke den riktige metoden.</span><span class="sxs-lookup"><span data-stu-id="4057b-122">On the **Items** FastTab, add items to the maintenance forecast by using the appropriate method.</span></span>

<span data-ttu-id="4057b-123">For å opprette en linje for en reservedel som ikke er i reservedellisten eller stykklisten for aktiva, følger du disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="4057b-123">To create a line for a spare part that isn't on the spare parts list or the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="4057b-124">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="4057b-124">Select **Add**.</span></span>
2. <span data-ttu-id="4057b-125">Velg varen i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4057b-125">In the **Item number** field, select the item.</span></span>
3. <span data-ttu-id="4057b-126">Angi antallet i **Salgsantall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4057b-126">In the **Sales quantity** field, enter the quantity.</span></span>
4. <span data-ttu-id="4057b-127">I **Enhet**-feltet velger du måleenheten for antallet.</span><span class="sxs-lookup"><span data-stu-id="4057b-127">In the **Unit** field, select the unit of measure for the quantity.</span></span>
5. <span data-ttu-id="4057b-128">I feltene **Kostpris** og **Valuta** angir du riktige verdier.</span><span class="sxs-lookup"><span data-stu-id="4057b-128">In the **Cost price** and **Currency** fields, enter appropriate values.</span></span>
6. <span data-ttu-id="4057b-129">I feltet **Linjeegenskap** velger du en linjeegenskap.</span><span class="sxs-lookup"><span data-stu-id="4057b-129">In the **Line property** field, select a line property.</span></span>
7. <span data-ttu-id="4057b-130">Hvis du vil endre listen over dimensjoner som vises på varelinjene, velger du **Lager** > **Visningsdimensjoner**, velger dimensjonene, og deretter setter du **Lagre oppsett** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="4057b-130">To change the list of dimensions that is shown on the item lines, select **Inventory** > **Display dimensions**, select the dimensions, and then set the **Save setup** option to **Yes**.</span></span>

<span data-ttu-id="4057b-131">Hvis du vil legge til en reservedel fra en godkjent reservedelsliste, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="4057b-131">To add a spare part from an approved spare parts list, follow these steps:</span></span>

1. <span data-ttu-id="4057b-132">Velg **Legg til reservedeler**.</span><span class="sxs-lookup"><span data-stu-id="4057b-132">Select **Add spare parts**.</span></span>
2. <span data-ttu-id="4057b-133">Velg reservedelen, og rediger den tilknyttede informasjonen slik du ønsker.</span><span class="sxs-lookup"><span data-stu-id="4057b-133">Select the spare part, and edit the related information as you require.</span></span>
3. <span data-ttu-id="4057b-134">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="4057b-134">Select **OK**.</span></span>

<span data-ttu-id="4057b-135">Følg denne fremgangsmåten for å legge til en vare fra stykklisten for aktiva:</span><span class="sxs-lookup"><span data-stu-id="4057b-135">To add an item from the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="4057b-136">Velg **Legg til stykklistevarer**.</span><span class="sxs-lookup"><span data-stu-id="4057b-136">Select **Add BOM items**.</span></span>
2. <span data-ttu-id="4057b-137">Velg varen, og rediger den tilknyttede informasjonen slik du ønsker.</span><span class="sxs-lookup"><span data-stu-id="4057b-137">Select the item, and edit the related information as you require.</span></span>
3. <span data-ttu-id="4057b-138">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="4057b-138">Select **OK**.</span></span>

<span data-ttu-id="4057b-139">Hvis du vil ha en oversikt som viser hvor varen på den valgte linjen brukes i forhold til aktiva, vedlikeholdjobbtypestandarder, reservedeler og arbeidsordrer i Aktivastyring, velger du **Vare der brukt**.</span><span class="sxs-lookup"><span data-stu-id="4057b-139">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="4057b-140">Hvis du vil ha mer informasjon om denne oversikten, kan du se [Brukssted for vare](../controlling-and-reporting/item-where-used.md).</span><span class="sxs-lookup"><span data-stu-id="4057b-140">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>


## <a name="add-an-expense-forecast-to-a-work-order"></a><span data-ttu-id="4057b-141">Legge til en utgiftsprognose i en arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="4057b-141">Add an expense forecast to a work order</span></span>

1. <span data-ttu-id="4057b-142">På siden **Prognose for vedlikehold av arbeidsordre** velger du arbeidsordrejobben du vil legge til en prognose i.</span><span class="sxs-lookup"><span data-stu-id="4057b-142">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="4057b-143">På hurtigfanen **Utgift** velger du **Legg til** for å opprette en linje.</span><span class="sxs-lookup"><span data-stu-id="4057b-143">On the **Expense** FastTab, select **Add** to create a line.</span></span>

3. <span data-ttu-id="4057b-144">Velg en kategori i feltet **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="4057b-144">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="4057b-145">Angi antallet i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4057b-145">In the **Quantity** field, enter the quantity.</span></span>

5. <span data-ttu-id="4057b-146">I feltene **Kostpris**, **Salgsvaluta** og **Salgspris** angir du de gjeldende verdiene.</span><span class="sxs-lookup"><span data-stu-id="4057b-146">In the **Cost price**, **Sales currency**, and **Sales price** fields, enter appropriate values.</span></span>

6. <span data-ttu-id="4057b-147">I **Linjeegenskap**-feltet velger du tilleggstypen som skal brukes på linjen.</span><span class="sxs-lookup"><span data-stu-id="4057b-147">In the **Line property** field, select the type of charge that should be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="4057b-148">Hurtigfanen **Totaler for vedlikeholdsprognose** viser en oversikt over antall linjer som er opprettet, for den valgte arbeidsordrejobben og for arbeidsordren, på hver hurtigfane.</span><span class="sxs-lookup"><span data-stu-id="4057b-148">The **Maintenance forecast totals** FastTab shows an overview of the number of lines that have been created, for the selected work order job and for the work order, on each FastTab.</span></span> <span data-ttu-id="4057b-149">Den viser også totale prognosearbeidstimer for arbeidsordrejobben og arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="4057b-149">It also shows the total forecasted work hours for the work order job and the work order.</span></span>

<span data-ttu-id="4057b-150">Illustrasjonen nedenfor viser et eksempel på siden **Prognose for vedlikehold av arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="4057b-150">The illustration below shows an example of the **Work order maintenance forecast** page.</span></span>

![Figur 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="4057b-152">Automatisk oppdatering av arbeidsordreprognoser</span><span class="sxs-lookup"><span data-stu-id="4057b-152">Automatic update of work order forecasts</span></span>

<span data-ttu-id="4057b-153">Hvis timekostnader, varekost og utgifter oppdateres i andre moduler i Microsoft Dynamics 365 for Finance and Operations, kan arbeidsordreprognoser i Aktivastyring oppdateres automatisk for å reflektere disse endringene.</span><span class="sxs-lookup"><span data-stu-id="4057b-153">If hour costs, item costs, and expenses are updated in other modules in Microsoft Dynamics 365 for Finance and Operations, work order forecasts in Asset Management can automatically be updated to reflect those changes.</span></span> <span data-ttu-id="4057b-154">Denne funksjonaliteten garanterer at de siste kostprisene alltid brukes i arbeidsordreprognosene.</span><span class="sxs-lookup"><span data-stu-id="4057b-154">This capability helps guarantee that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="4057b-155">Du kan også gjøre lignende oppdateringer for [vedlikeholdsjobbtypeprognoser](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="4057b-155">You can also do similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="4057b-156">Velg **Aktivastyring** > **Periodisk** > **Prognose** > **Oppdater arbeidsordreprognose**.</span><span class="sxs-lookup"><span data-stu-id="4057b-156">Select **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="4057b-157">I dialogboksen **Oppdater arbeidsordreprognose** på hurtigfanen **Poster som skal inkluderes** kan du legge til valg for bestemte arbeidsordrer eller arbeidsordrejobber, etter behov.</span><span class="sxs-lookup"><span data-stu-id="4057b-157">In the **Update work order forecast** dialog, on the **Records to include** FastTab, you can add selections regarding specific work orders or work order jobs, as you require.</span></span> <span data-ttu-id="4057b-158">Klikk på **Filter** for å gjøre de relevante valgene.</span><span class="sxs-lookup"><span data-stu-id="4057b-158">Click **Filter** to make the relevant selections.</span></span>

3. <span data-ttu-id="4057b-159">På hurtigfanen **Kjør i bakgrunnen** kan du definere den automatiske oppdateringen som en satsvis jobb, slik du ønsker.</span><span class="sxs-lookup"><span data-stu-id="4057b-159">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

4. <span data-ttu-id="4057b-160">Velg **OK** for å starte prognoseoppdateringen.</span><span class="sxs-lookup"><span data-stu-id="4057b-160">Select **OK** to start the forecast update.</span></span>


<span data-ttu-id="4057b-161">Illustrasjonen nedenfor viser et eksempel på dialogboksen **Oppdater arbeidsordreprognose**.</span><span class="sxs-lookup"><span data-stu-id="4057b-161">The illustration below shows an example of the **Update work order forecast** dialog.</span></span>

![Figur 2](media/07-work-orders.png)
