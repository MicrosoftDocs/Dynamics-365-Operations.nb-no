---
title: Vedlikeholdsprognoser
description: Dette emnet beskriver vedlikeholdsprognoser i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 383c910b40199f2da863144c6dc85a579d0091e9
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024505"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="b1e71-103">Vedlikeholdsprognoser</span><span class="sxs-lookup"><span data-stu-id="b1e71-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="b1e71-104">Når du oppretter en arbeidsordre, oppretter du arbeidsordrejobber med tilknyttede aktiva og vedlikeholdsjobbtyper.</span><span class="sxs-lookup"><span data-stu-id="b1e71-104">When you create a work order, you create work order jobs with related assets and maintenance job types.</span></span> <span data-ttu-id="b1e71-105">Når du velger en vedlikeholdsjobbtype som inneholder vedlikeholdsprognoser, kopieres prognosene automatisk til arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="b1e71-105">When you select a maintenance job type containing maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="b1e71-106">Du kan kanskje legge til eller slette prognoselinjer i en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="b1e71-106">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="b1e71-107">Oppsettet for en arbeidsordrelivssyklustilstand, den tilknyttede prosjekttypen og stadiereglene knyttet til prosjekttypen bestemmer om du kan legge til eller redigere prognoselinjer.</span><span class="sxs-lookup"><span data-stu-id="b1e71-107">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determines if you are able to add or edit forecast lines.</span></span> 

1. <span data-ttu-id="b1e71-108">Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="b1e71-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="b1e71-109">Velg arbeidsordren i listen, og klikk på **Prognose**.</span><span class="sxs-lookup"><span data-stu-id="b1e71-109">Select the work order in the list, and click **Forecast**.</span></span> <span data-ttu-id="b1e71-110">I **Vedlikeholdsprognose for arbeidsordre** vises prognoselinjer fra vedlikeholdsjobbtypen som er valgt i arbeidsordrejobben.</span><span class="sxs-lookup"><span data-stu-id="b1e71-110">In **Work order maintenance forecast**, forecast lines from the maintenance job type selected on the work order job are displayed.</span></span>


## <a name="add-hours-forecast-to-a-work-order"></a><span data-ttu-id="b1e71-111">Legge til prognose for timer i en arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="b1e71-111">Add hours forecast to a work order</span></span>

1. <span data-ttu-id="b1e71-112">Velg arbeidsordrejobben som du vil legge til en prognose for.</span><span class="sxs-lookup"><span data-stu-id="b1e71-112">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="b1e71-113">På hurtigfanen **Timer** klikker du på **Legg til** for å opprette en ny linje.</span><span class="sxs-lookup"><span data-stu-id="b1e71-113">On the **Hours** FastTab, click **Add** to create a new line.</span></span>

3. <span data-ttu-id="b1e71-114">Velg en kategori i **Kategori**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b1e71-114">Select a category in the **Category** field.</span></span>

4. <span data-ttu-id="b1e71-115">Sett inn antall prognosetimer i **Timer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b1e71-115">Insert number of forecasted hours in the **Hours** field.</span></span>

5. <span data-ttu-id="b1e71-116">I **Linjeegenskap**-feltet velger du tilleggstypen som skal brukes på linjen.</span><span class="sxs-lookup"><span data-stu-id="b1e71-116">In the **Line property** field, select the charge type to be used on the line.</span></span>


## <a name="add-items-forecast-to-a-work-order"></a><span data-ttu-id="b1e71-117">Legge til prognose for varer i en arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="b1e71-117">Add items forecast to a work order</span></span>

<span data-ttu-id="b1e71-118">Det finnes tre måter å legge til varer på i en vedlikeholdsprognose for arbeidsordre: Du kan opprette linjer for varer (reservedeler) som ikke er inkludert i reservedellisten eller stykklisten for aktiva, du kan velge reservedeler fra listen over godkjente reservedeler, og du kan velge varer fra stykklisten for aktiva.</span><span class="sxs-lookup"><span data-stu-id="b1e71-118">There are three ways to add items to a work order maintenance forecast: You can create lines for items (spare parts) that are not included in the spare parts list or asset BOM, you can select spare parts from the approved spare parts list, and you can select items from the asset BOM.</span></span>

1. <span data-ttu-id="b1e71-119">Velg arbeidsordrejobben som du vil legge til en prognose for.</span><span class="sxs-lookup"><span data-stu-id="b1e71-119">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="b1e71-120">Velg hurtigfanen **Varer**.</span><span class="sxs-lookup"><span data-stu-id="b1e71-120">Select the **Items** FastTab.</span></span>

3. <span data-ttu-id="b1e71-121">Klikk på **Legg til** for å opprette en ny linje for en reservedel som ikke er i reservedellisten eller stykklisten for aktiva.</span><span class="sxs-lookup"><span data-stu-id="b1e71-121">Click **Add** to create a new line for a spare part that is not on the spare parts list or the asset BOM list.</span></span>

4. <span data-ttu-id="b1e71-122">Velg varen i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b1e71-122">Select the item in the **Item number** field.</span></span>

5. <span data-ttu-id="b1e71-123">Sett inn antall i **Salgsantall**-feltet, og velg en antallsenhet i **Enhet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b1e71-123">Insert quantity in the **Sales quantity** field, and select a quantity unit in the **Unit** field.</span></span>

6. <span data-ttu-id="b1e71-124">Sett inn kostpris og valuta i de relevante feltene, og velg en **Linjeegenskap**.</span><span class="sxs-lookup"><span data-stu-id="b1e71-124">Insert cost price and currency in the relevant fields, and select a **Line property**.</span></span>

7. <span data-ttu-id="b1e71-125">Hvis du vil endre listen over dimensjoner som vises på varelinjene, kan du klikke på **Lager** > **Visningsdimensjoner**, velge dimensjonene og velge Ja på veksleknappen **Lagre oppsett**.</span><span class="sxs-lookup"><span data-stu-id="b1e71-125">If you want to change the list of dimensions displayed on the item lines, click **Inventory** > **Display dimensions**, select the dimensions, and select "Yes" on the **Save setup** toggle button.</span></span>

8. <span data-ttu-id="b1e71-126">Hvis du vil legge til en godkjent reservedel i vedlikeholdsprognosen, klikker du på **Legg til reservedeler**, velger reservedelen, redigerer relatert informasjon om nødvendig, og klikker på **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1e71-126">If you want to add an approved spare part to the maintenance forecast, click **Add spare parts**, select the spare part, edit related information if required, and click **OK**.</span></span>

9. <span data-ttu-id="b1e71-127">Hvis du vil legge til stykklistevarer for aktiva i prognosen, klikker du på **Legg til stykklistevarer**, velger varen, redigerer relatert informasjon hvis nødvendig, og klikker på **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1e71-127">If you want to add asset BOM items to the forecast, click **Add BOM items**, select the item, edit related information if required, and click **OK**.</span></span>

10. <span data-ttu-id="b1e71-128">Klikk på **Vare der brukt** hvis du vil ha en oversikt over hvor i Aktivastyring varen på den valgte linjen brukes, i forhold til aktiva, vedlikeholdsjobbtypestandarder, reservedeler og arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="b1e71-128">Click **Item where used** if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 



## <a name="add-expense-forecast-to-a-work-order"></a><span data-ttu-id="b1e71-129">Legge til utgiftsprognose i en arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="b1e71-129">Add expense forecast to a work order</span></span>

1. <span data-ttu-id="b1e71-130">Dette emnet forklarer hvordan du legger til en utgiftsprognose i en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="b1e71-130">This topic explains how to add an expense forecast to a work order.</span></span> <span data-ttu-id="b1e71-131">Til venstre i skjemaet velger du arbeidsordrejobben du vil legge til en prognose i.</span><span class="sxs-lookup"><span data-stu-id="b1e71-131">In the left-hand side of the form, select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="b1e71-132">Velg hurtigfanen **Utgift**.</span><span class="sxs-lookup"><span data-stu-id="b1e71-132">Select the **Expense** FastTab.</span></span>

3. <span data-ttu-id="b1e71-133">Klikk på **Legg til** for å opprette en ny linje.</span><span class="sxs-lookup"><span data-stu-id="b1e71-133">Click **Add** to create a new line.</span></span>

4. <span data-ttu-id="b1e71-134">Velg en kategori i **Kategori**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b1e71-134">Select a category in the **Category** field.</span></span>

5. <span data-ttu-id="b1e71-135">Sett inn antallet i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b1e71-135">Insert quantity in the **Quantity** field.</span></span>

6. <span data-ttu-id="b1e71-136">Sett inn kostpris, salgsvaluta og salgspris i de relevante feltene.</span><span class="sxs-lookup"><span data-stu-id="b1e71-136">Insert cost price, sales currency, and sales price in the relevant fields.</span></span>

7. <span data-ttu-id="b1e71-137">I **Linjeegenskap**-feltet velger du tilleggstypen som skal brukes på linjen.</span><span class="sxs-lookup"><span data-stu-id="b1e71-137">In the **Line property** field, select the charge type to be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="b1e71-138">I hurtigfanen **Totaler for vedlikeholdsprognose** får du en oversikt over antall linjer som er opprettet i hver kategori, for den valgte arbeidsordrejobben og for arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="b1e71-138">On the **Maintenance forecast totals** FastTab, you can see an overview of the number of lines created on each tab, for the selected work order job and for the work order.</span></span> <span data-ttu-id="b1e71-139">Du kan også se en sum for prognosearbeidstimer for arbeidsordrejobben og for arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="b1e71-139">Also, you can see a sum of forecasted work hours for the work order job and for the work order.</span></span>

![Figur 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="b1e71-141">Automatisk oppdatering av arbeidsordreprognoser</span><span class="sxs-lookup"><span data-stu-id="b1e71-141">Automatic update of work order forecasts</span></span>

<span data-ttu-id="b1e71-142">I Aktivastyring kan du automatisk oppdatere eventuelle endringer i arbeidsordreprognoser for timekostnader, varekost og utgifter som er oppdatert i andre moduler.</span><span class="sxs-lookup"><span data-stu-id="b1e71-142">In Asset Management, you can automatically update any changes in work order forecasts regarding hour costs, item costs, and expenses, which have been updated in other modules.</span></span> <span data-ttu-id="b1e71-143">Dette gjøres for å sikre at de siste kostprisene alltid brukes i arbeidsordreprognosene.</span><span class="sxs-lookup"><span data-stu-id="b1e71-143">This is done to ensure that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="b1e71-144">Det er også mulig å utføre lignende oppdateringer for [vedlikeholdsjobbtypeprognoser](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="b1e71-144">It is also possible to make similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="b1e71-145">Klikk på **Aktivastyring** > **Periodisk** > **Prognose** > **Oppdater arbeidsordreprognose**.</span><span class="sxs-lookup"><span data-stu-id="b1e71-145">Click **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="b1e71-146">I rullegardinlisten **Oppdater arbeidsordreprognose** kan du legge til valg for bestemte arbeidsordrer eller arbeidsordrejobber om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="b1e71-146">In the **Update work order forecast** drop-down dialog, you can add selections regarding specific work orders or work order jobs, if required.</span></span> <span data-ttu-id="b1e71-147">Klikk på **Filter** for å gjøre disse valgene.</span><span class="sxs-lookup"><span data-stu-id="b1e71-147">Click **Filter** to make those selections.</span></span>

3. <span data-ttu-id="b1e71-148">På hurtigfanen **Kjør i bakgrunnen** kan du definere den automatiske oppdateringen som en satsvis jobb, om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="b1e71-148">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

4. <span data-ttu-id="b1e71-149">Klikk på **OK** for å starte prognoseoppdateringen.</span><span class="sxs-lookup"><span data-stu-id="b1e71-149">Click **OK** to start the forecast update.</span></span>


![Figur 2](media/07-work-orders.png)

