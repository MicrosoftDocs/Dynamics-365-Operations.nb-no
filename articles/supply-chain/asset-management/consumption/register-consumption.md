---
title: Registrere forbruk
description: Dette emnet forklarer hvordan du registrerer forbruk i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderJournal, EntAssetWorkOrderAddSparePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ea1522f8a8e4867d8d70fea59b493d139a1b01ef
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020787"
---
# <a name="register-consumption"></a><span data-ttu-id="8e853-103">Registrere forbruk</span><span class="sxs-lookup"><span data-stu-id="8e853-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8e853-104">Når en vedlikeholdsjobb er fullført i en arbeidsordre, er neste trinn å gjøre forbruksregistreringer og postere journalene.</span><span class="sxs-lookup"><span data-stu-id="8e853-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="8e853-105">Du kan gjøre registreringer for følgende forbrukstyper: timer, varer og utgifter.</span><span class="sxs-lookup"><span data-stu-id="8e853-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="8e853-106">De forskjellige forbrukstypene registreres og posteres på siden **Arbeidsordrejournaler**.</span><span class="sxs-lookup"><span data-stu-id="8e853-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="8e853-107">Journaloppsettet i **Aktivastyring** brukes til å opprette og postere separate journaler for timer, varer og utgifter i modulen **Prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="8e853-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="8e853-108">I noen tilfeller kan du legge til eller slette prognoselinjer i en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="8e853-108">In some cases, you may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="8e853-109">Oppsettet for en arbeidsordrelivssyklustilstand, den tilknyttede prosjekttypen og stadiereglene knyttet til prosjekttypen bestemmer om du kan legge til eller redigere journallinjer.</span><span class="sxs-lookup"><span data-stu-id="8e853-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="8e853-110">Les mer om livssyklustilstander for arbeidsordrer og relaterte prosjektstadier i [Prognoser, arbeidsordrer og prosjekter](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="8e853-110">Read more about work order lifecycle states and related project stages in [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="8e853-111">Det er mulig å definere automatisk postering av journaler for en livssyklustilstand for arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="8e853-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="8e853-112">Se [Livssyklustilstand for arbeidsordre](../setup-for-work-orders/work-order-lifecycle-states.md) hvis du vil ha mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="8e853-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="8e853-113">Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="8e853-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="8e853-114">Velg arbeidsordren, og klikk på **Journaler**.</span><span class="sxs-lookup"><span data-stu-id="8e853-114">Select the work order, and click **Journals**.</span></span>

3. <span data-ttu-id="8e853-115">Klikk på **Kopier fra prognose** for å overføre eventuelle prognoselinjer som kan være knyttet til arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="8e853-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="8e853-116">Du kan velge hvilke forbrukstyper du vil overføre.</span><span class="sxs-lookup"><span data-stu-id="8e853-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="8e853-117">Hvis det er nødvendig, kan du legge til flere forbrukslinjer i den aktuelle hurtigfanen ved å klikke på **Legg til linje** og fylle ut data på linjen.</span><span class="sxs-lookup"><span data-stu-id="8e853-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="8e853-118">Klikk på **Valider journaler** for å validere journallinjene før postering.</span><span class="sxs-lookup"><span data-stu-id="8e853-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="8e853-119">Klikk på **Poster journaler** for å postere journallinjene.</span><span class="sxs-lookup"><span data-stu-id="8e853-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="8e853-120">Når du har postert forbruksjournalene, kan du oppdatere livssyklustilstanden for arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="8e853-120">After you've posted the consumption journals, you can update the work order lifecycle state.</span></span> <span data-ttu-id="8e853-121">Hvis du for eksempel vil angi at arbeidsordren er fullført, kan du oppdatere livssyklustilstanden til "Avsluttet".</span><span class="sxs-lookup"><span data-stu-id="8e853-121">For example, to indicate that the work order has been completed, you can update the lifecycle state to "Ended".</span></span>

    - <span data-ttu-id="8e853-122">I **Vis**-feltet som er plassert øverst på siden **Arbeidsordrejournaler**, velger du hvilke journallinjer du vil vise: **Alle**, **Ikke postert** eller **Postert**.</span><span class="sxs-lookup"><span data-stu-id="8e853-122">In the **Show** field at the top of the **Work order journals** page, select which journal lines you want to see: **All**, **Not posted**, or **Posted**.</span></span> <span data-ttu-id="8e853-123">Posterte journaler har en hake i avmerkingsboksen **Postert**.</span><span class="sxs-lookup"><span data-stu-id="8e853-123">Posted journals have a check mark in the **Posted** check box.</span></span>  
    - <span data-ttu-id="8e853-124">Når varelinjer opprettes i arbeidsordrejournalen, blir produktdimensjoner og sporingsdimensjoner som er knyttet til varen, automatisk overført til journallinjen.</span><span class="sxs-lookup"><span data-stu-id="8e853-124">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="8e853-125">Skjermbildet nedenfor viser et eksempel på time- og vareregistreringer for en arbeidsordre i **Arbeidsordrejournaler**.</span><span class="sxs-lookup"><span data-stu-id="8e853-125">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![Figur 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="8e853-127">Dele timer i arbeidsordrer med flere arbeidsordrejobber</span><span class="sxs-lookup"><span data-stu-id="8e853-127">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="8e853-128">Hvis en arbeidsordre inneholder flere arbeidsordrejobber, kan du registrere arbeidstimer ved hjelp av funksjonaliteten **Del timer**, som betyr at én timeregistreringslinje kan distribueres likt på hver arbeidsordrejobb.</span><span class="sxs-lookup"><span data-stu-id="8e853-128">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="8e853-129">Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="8e853-129">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="8e853-130">Velg arbeidsordren, og klikk på **Journaler**.</span><span class="sxs-lookup"><span data-stu-id="8e853-130">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="8e853-131">Velg timeregistreringslinjen du vil dele, og klikk på **Del timer**.</span><span class="sxs-lookup"><span data-stu-id="8e853-131">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="8e853-132">I dialogboksen **Del timer for vedlikeholdsjobber for arbeidsordre** vises navnet på arbeideren som er logget på, automatisk, i **Arbeider**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8e853-132">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="8e853-133">Hvis det er nødvendig, kan du velge en annen arbeider.</span><span class="sxs-lookup"><span data-stu-id="8e853-133">If required, you can select another worker.</span></span>

5. <span data-ttu-id="8e853-134">Velg en kategori for timeregistreringen i **Kategori**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8e853-134">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="8e853-135">Sett inn antall arbeidstimer som skal deles, i **Timer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8e853-135">Insert number of work hours to be split in the **Hours** field.</span></span>

    ![Figur 2](media/02-consumption.png)

7. <span data-ttu-id="8e853-137">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e853-137">Click **OK**.</span></span>

<span data-ttu-id="8e853-138">*Eksempel:* I skjermbildet nedenfor vises journallinjer for en arbeidsordre som inneholder tre arbeidsordrejobber.</span><span class="sxs-lookup"><span data-stu-id="8e853-138">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="8e853-139">Den første linjen som inneholder tre arbeidstimer, er delt, og én arbeidstime er registrert på hver arbeidsordrejobb.</span><span class="sxs-lookup"><span data-stu-id="8e853-139">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="8e853-140">Når de tre timeregistreringslinjene er opprettet, bestemmer du hva du skal gjøre med den opprinnelige timeregistreringslinjen (den første linjen i eksemplet).</span><span class="sxs-lookup"><span data-stu-id="8e853-140">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="8e853-141">Du kan beholde den slik den er, eller slette den.</span><span class="sxs-lookup"><span data-stu-id="8e853-141">You can keep it as is or delete it.</span></span> 

![Figur 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="8e853-143">Finansdimensjoner på forbruksregistreringer</span><span class="sxs-lookup"><span data-stu-id="8e853-143">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="8e853-144">Når du utfører forbruksregistreringer, legges finansdimensjoner som er knyttet til de ulike registreringstypene, til i registreringene i en bestemt rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="8e853-144">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

- <span data-ttu-id="8e853-145">*Time- og utgiftsregistreringer:* Først blir finansdimensjoner fra journalhodet lagt til.</span><span class="sxs-lookup"><span data-stu-id="8e853-145">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="8e853-146">Så legges finansdimensjoner fra det tilknyttede arbeidsordreprosjektet til.</span><span class="sxs-lookup"><span data-stu-id="8e853-146">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="8e853-147">Til slutt legges finansdimensjoner fra ressursen (arbeideren) til.</span><span class="sxs-lookup"><span data-stu-id="8e853-147">Finally, financial dimensions from the resource (worker) are added.</span></span>

- <span data-ttu-id="8e853-148">*Vareregistreringer:* Først blir finansdimensjoner fra journalhodet lagt til.</span><span class="sxs-lookup"><span data-stu-id="8e853-148">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="8e853-149">Så legges finansdimensjoner fra det tilknyttede arbeidsordreprosjektet til.</span><span class="sxs-lookup"><span data-stu-id="8e853-149">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="8e853-150">Deretter legges finansdimensjoner fra området til.</span><span class="sxs-lookup"><span data-stu-id="8e853-150">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="8e853-151">Til slutt legges finansdimensjoner fra varen til.</span><span class="sxs-lookup"><span data-stu-id="8e853-151">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="8e853-152">For alle tre registreringstypene valideres finansdimensjonskombinasjonen, og ugyldige kombinasjoner er tomme.</span><span class="sxs-lookup"><span data-stu-id="8e853-152">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="8e853-153">Dette er standard oppsett med andre Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="8e853-153">This is standard setup with other Finance and Operations apps.</span></span>

