---
title: Registrere forbruk
description: Dette emnet forklarer hvordan du registrerer forbruk i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7f785b0935b952d6de68fd120a3639077ad124bd
ms.sourcegitcommit: c0b581e4c647b6c47bc14d1d7bfe267832afecba
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/21/2019
ms.locfileid: "1913101"
---
# <a name="register-consumption"></a><span data-ttu-id="0100d-103">Registrere forbruk</span><span class="sxs-lookup"><span data-stu-id="0100d-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="0100d-104">Når en vedlikeholdsjobb er fullført i en arbeidsordre, er neste trinn å gjøre forbruksregistreringer og postere journalene.</span><span class="sxs-lookup"><span data-stu-id="0100d-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="0100d-105">Du kan gjøre registreringer for følgende forbrukstyper: timer, varer og utgifter.</span><span class="sxs-lookup"><span data-stu-id="0100d-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="0100d-106">De forskjellige forbrukstypene registreres og posteres på siden **Arbeidsordrejournaler**.</span><span class="sxs-lookup"><span data-stu-id="0100d-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="0100d-107">Journaloppsettet i **Aktivastyring** brukes til å opprette og postere separate journaler for timer, varer og utgifter i modulen **Prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="0100d-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="0100d-108">Du kan kanskje legge til eller slette prognoselinjer i en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="0100d-108">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="0100d-109">Oppsettet for en arbeidsordrelivssyklustilstand, den tilknyttede prosjekttypen og stadiereglene knyttet til prosjekttypen bestemmer om du kan legge til eller redigere journallinjer.</span><span class="sxs-lookup"><span data-stu-id="0100d-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="0100d-110">Les mer om livssyklustilstander for arbeidsordrer og relaterte prosjektstadier i [Integrering til prosjektstyring og regnskap](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="0100d-110">Read more about work order lifecycle states and related project stages in [Integration to project management and accounting](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="0100d-111">Det er mulig å definere automatisk postering av journaler for en livssyklustilstand for arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="0100d-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="0100d-112">Se [Livssyklustilstand for arbeidsordre](../setup-for-work-orders/work-order-lifecycle-states.md) hvis du vil ha mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="0100d-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="0100d-113">Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="0100d-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0100d-114">Velg arbeidsordren, og klikk på **Journaler**.</span><span class="sxs-lookup"><span data-stu-id="0100d-114">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="0100d-115">Klikk på **Kopier fra prognose** for å overføre eventuelle prognoselinjer som kan være knyttet til arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="0100d-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="0100d-116">Du kan velge hvilke forbrukstyper du vil overføre.</span><span class="sxs-lookup"><span data-stu-id="0100d-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="0100d-117">Hvis det er nødvendig, kan du legge til flere forbrukslinjer i den aktuelle hurtigfanen ved å klikke på **Legg til linje** og fylle ut data på linjen.</span><span class="sxs-lookup"><span data-stu-id="0100d-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="0100d-118">Klikk på **Valider journaler** for å validere journallinjene før postering.</span><span class="sxs-lookup"><span data-stu-id="0100d-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="0100d-119">Klikk på **Poster journaler** for å postere journallinjene.</span><span class="sxs-lookup"><span data-stu-id="0100d-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="0100d-120">Når du har postert forbruksjournalene, kan du oppdatere livssyklustilstanden for arbeidsordren, for eksempel Avsluttet, for å angi at arbeidsordren er fullført.</span><span class="sxs-lookup"><span data-stu-id="0100d-120">After you've posted the consumption journals, you can update the work order lifecycle state, for example to "Ended", to indicate that the work order has been completed.</span></span>

- <span data-ttu-id="0100d-121">I **Vis**-feltet som er plassert øverst på siden **Arbeidsordrejournaler**, velger du hvilke journallinjer du vil vise: alle, ikke postert eller postert.</span><span class="sxs-lookup"><span data-stu-id="0100d-121">In the **Show** field placed at the top of the **Work order journals** page, select which journal lines you want to see: All, Not posted, or Posted.</span></span> <span data-ttu-id="0100d-122">Posterte journaler har en hake i avmerkingsboksen **Postert**.</span><span class="sxs-lookup"><span data-stu-id="0100d-122">Posted journals have a check mark in the **Posted** check box.</span></span>  
- <span data-ttu-id="0100d-123">Når varelinjer opprettes i arbeidsordrejournalen, blir produktdimensjoner og sporingsdimensjoner som er knyttet til varen, automatisk overført til journallinjen.</span><span class="sxs-lookup"><span data-stu-id="0100d-123">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="0100d-124">Skjermbildet nedenfor viser et eksempel på time- og vareregistreringer for en arbeidsordre i **Arbeidsordrejournaler**.</span><span class="sxs-lookup"><span data-stu-id="0100d-124">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![Figur 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="0100d-126">Dele timer i arbeidsordrer med flere arbeidsordrejobber</span><span class="sxs-lookup"><span data-stu-id="0100d-126">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="0100d-127">Hvis en arbeidsordre inneholder flere arbeidsordrejobber, kan du registrere arbeidstimer ved hjelp av funksjonaliteten **Del timer**, som betyr at én timeregistreringslinje kan distribueres likt på hver arbeidsordrejobb.</span><span class="sxs-lookup"><span data-stu-id="0100d-127">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="0100d-128">Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="0100d-128">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0100d-129">Velg arbeidsordren, og klikk på **Journaler**.</span><span class="sxs-lookup"><span data-stu-id="0100d-129">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="0100d-130">Velg timeregistreringslinjen du vil dele, og klikk på **Del timer**.</span><span class="sxs-lookup"><span data-stu-id="0100d-130">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="0100d-131">I dialogboksen **Del timer for vedlikeholdsjobber for arbeidsordre** vises navnet på arbeideren som er logget på, automatisk, i **Arbeider**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0100d-131">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="0100d-132">Hvis det er nødvendig, kan du velge en annen arbeider.</span><span class="sxs-lookup"><span data-stu-id="0100d-132">If required, you can select another worker.</span></span>

5. <span data-ttu-id="0100d-133">Velg en kategori for timeregistreringen i **Kategori**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0100d-133">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="0100d-134">Sett inn antall arbeidstimer som skal deles, i **Timer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0100d-134">Insert number of work hours to be split in the **Hours** field.</span></span>

![Figur 2](media/02-consumption.png)

7. <span data-ttu-id="0100d-136">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="0100d-136">Click **OK**.</span></span>

<span data-ttu-id="0100d-137">*Eksempel:* I skjermbildet nedenfor vises journallinjer for en arbeidsordre som inneholder tre arbeidsordrejobber.</span><span class="sxs-lookup"><span data-stu-id="0100d-137">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="0100d-138">Den første linjen som inneholder tre arbeidstimer, er delt, og én arbeidstime er registrert på hver arbeidsordrejobb.</span><span class="sxs-lookup"><span data-stu-id="0100d-138">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="0100d-139">Når de tre timeregistreringslinjene er opprettet, bestemmer du hva du skal gjøre med den opprinnelige timeregistreringslinjen (den første linjen i eksemplet).</span><span class="sxs-lookup"><span data-stu-id="0100d-139">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="0100d-140">Du kan beholde den slik den er, eller slette den.</span><span class="sxs-lookup"><span data-stu-id="0100d-140">You can keep it as is or delete it.</span></span> 

![Figur 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="0100d-142">Finansdimensjoner på forbruksregistreringer</span><span class="sxs-lookup"><span data-stu-id="0100d-142">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="0100d-143">Når du utfører forbruksregistreringer, legges finansdimensjoner som er knyttet til de ulike registreringstypene, til i registreringene i en bestemt rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="0100d-143">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

<span data-ttu-id="0100d-144">*Time- og utgiftsregistreringer:* Først blir finansdimensjoner fra journalhodet lagt til.</span><span class="sxs-lookup"><span data-stu-id="0100d-144">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="0100d-145">Så legges finansdimensjoner fra det tilknyttede arbeidsordreprosjektet til.</span><span class="sxs-lookup"><span data-stu-id="0100d-145">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="0100d-146">Til slutt legges finansdimensjoner fra ressursen (arbeideren) til.</span><span class="sxs-lookup"><span data-stu-id="0100d-146">Finally, financial dimensions from the resource (worker) are added.</span></span>

<span data-ttu-id="0100d-147">*Vareregistreringer:* Først blir finansdimensjoner fra journalhodet lagt til.</span><span class="sxs-lookup"><span data-stu-id="0100d-147">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="0100d-148">Så legges finansdimensjoner fra det tilknyttede arbeidsordreprosjektet til.</span><span class="sxs-lookup"><span data-stu-id="0100d-148">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="0100d-149">Deretter legges finansdimensjoner fra området til.</span><span class="sxs-lookup"><span data-stu-id="0100d-149">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="0100d-150">Til slutt legges finansdimensjoner fra varen til.</span><span class="sxs-lookup"><span data-stu-id="0100d-150">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="0100d-151">For alle tre registreringstypene valideres finansdimensjonskombinasjonen, og ugyldige kombinasjoner er tomme.</span><span class="sxs-lookup"><span data-stu-id="0100d-151">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="0100d-152">Dette er standardoppsett i Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0100d-152">This is standard setup in Dynamics 365 for Finance and Operations.</span></span>

