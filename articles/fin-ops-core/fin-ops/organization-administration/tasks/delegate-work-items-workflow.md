---
title: Delegere arbeidselementer i en arbeidsflyt
description: Hvis du planlegger å være borte fra kontoret eller av andre grunner ikke er tilgjengelig til å behandle arbeidselementer, kan du delegere eller tilordne arbeidselementer til andre brukere.
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 054e183374d2b24f38b0f90ff90acfeeca013861
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560561"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="52beb-103">Delegere arbeidselementer i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="52beb-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="52beb-104">Delegere et arbeidselement manuelt</span><span class="sxs-lookup"><span data-stu-id="52beb-104">Manually delegate a work item</span></span>

<span data-ttu-id="52beb-105">For å delegere et individuelt arbeidselement, velg **Deleger**-alternativet på **Arbeidsflyt**-menyen, og angi deretter brukeren det skal delegeres til, sammen med en kommentar.</span><span class="sxs-lookup"><span data-stu-id="52beb-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="52beb-106">Dette vil tilordne arbeidselementet til denne brukeren, slik at vedkommende kan fullføre det.</span><span class="sxs-lookup"><span data-stu-id="52beb-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="52beb-107">Delegere flere arbeidselementer manuelt</span><span class="sxs-lookup"><span data-stu-id="52beb-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="52beb-108">Flere arbeidselementer kan delegeres sammen fra **Arbeidselementer som tilordnet til meg**-siden.</span><span class="sxs-lookup"><span data-stu-id="52beb-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="52beb-109">Følgende arbeidsflyttyper er berettiget til massedelegering: arbeidsflyt for godkjenning av kjøpsavtale, bestillingsarbeidsflyt, innkjøpsrekvisisjonsgjennomgang og leverandørfakturaarbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="52beb-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="52beb-110">**Deleger flere arbeidselementer**-funksjonen er deaktivert som standard, og kan aktiveres i **Arbeidsområder > Funksjonsstyring**.</span><span class="sxs-lookup"><span data-stu-id="52beb-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="52beb-111">Ta kontakt med systemansvarlig for å få hjelp til å aktivere denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="52beb-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="52beb-112">Gå til **Felles > Felles > Arbeidselementer > Arbeidselementer som er tilordnet til meg**.</span><span class="sxs-lookup"><span data-stu-id="52beb-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="52beb-113">Velg arbeidselementene som skal delegeres.</span><span class="sxs-lookup"><span data-stu-id="52beb-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="52beb-114">Klikk på **Deleger arbeidselementer**-menyen.</span><span class="sxs-lookup"><span data-stu-id="52beb-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="52beb-115">Velg brukeren som arbeidselementene skal delegeres til, i **Bruker**-feltet.</span><span class="sxs-lookup"><span data-stu-id="52beb-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="52beb-116">Angi en kommentar som forklarer hvorfor du delegerer arbeidselementene, i feltet **Kommentar**.</span><span class="sxs-lookup"><span data-stu-id="52beb-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="52beb-117">Klikk på **Deleger arbeidselementer**-knappen for å fullføre arbeidselementdelegeringen.</span><span class="sxs-lookup"><span data-stu-id="52beb-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="52beb-118">Automatisk delegere arbeidselementer</span><span class="sxs-lookup"><span data-stu-id="52beb-118">Automatically delegate work items</span></span>

<span data-ttu-id="52beb-119">Hvis du planlegger å være borte fra kontoret eller å ikke være tilgjengelig for jobb med arbeidselementer i en bestemt tidsperiode, kan du automatisk delegere nye arbeidselementer til andre brukere ved hjelp av siden **Brukeralternativer**.</span><span class="sxs-lookup"><span data-stu-id="52beb-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="52beb-120">Definere automatisk delegering</span><span class="sxs-lookup"><span data-stu-id="52beb-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="52beb-121">Gå til **Felles > Oppsett > Brukeralternativer**.</span><span class="sxs-lookup"><span data-stu-id="52beb-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="52beb-122">Klikk på fanen **Arbeidsflyt**. Kontroller at Delegering-delen er utvidet.</span><span class="sxs-lookup"><span data-stu-id="52beb-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="52beb-123">Hvis du vil konfigurere systemet slik at det automatisk delegerer arbeidselementene dine til andre brukere, må du opprette delegeringsregler, som angir når bestemte typer arbeidselementer delegeres.</span><span class="sxs-lookup"><span data-stu-id="52beb-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="52beb-124">Hvis du vil opprette en delegeringsregel, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="52beb-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="52beb-125">Klikk på **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="52beb-125">Click **Add**.</span></span>
4. <span data-ttu-id="52beb-126">Velg et alternativ i **Omfang**-feltet:</span><span class="sxs-lookup"><span data-stu-id="52beb-126">In the **Scope** field, select an option:</span></span>
    - <span data-ttu-id="52beb-127">Alle – deleger alle arbeidsenheter som er tilordnet til deg.</span><span class="sxs-lookup"><span data-stu-id="52beb-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="52beb-128">Modul – deleger bare arbeidselementene som er knyttet til en bestemt type arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="52beb-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="52beb-129">Hvis du velger dette alternativet, må du velge typen arbeidsflyt i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="52beb-129">If you select this option, you must select the type of workflow in the **Name** field.</span></span>
    - <span data-ttu-id="52beb-130">Arbeidsflyt – deleger bare arbeidselementene som er knyttet til en bestemt arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="52beb-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="52beb-131">Hvis du velger dette alternativet, må du velge arbeidsflyten i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="52beb-131">If you select this option, you must select the workflow in the **Name** field.</span></span>  
5. <span data-ttu-id="52beb-132">I **Navn**-feltet:</span><span class="sxs-lookup"><span data-stu-id="52beb-132">In the **Name** field:</span></span>
    - <span data-ttu-id="52beb-133">For **Modul**-området velger du målmodulen.</span><span class="sxs-lookup"><span data-stu-id="52beb-133">For **Module** scope, select the target module.</span></span>
    - <span data-ttu-id="52beb-134">For **Arbeidsflyt**-området velger du målarbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="52beb-134">For **Workflow** scope, select the target workflow.</span></span>
6. <span data-ttu-id="52beb-135">Velg brukeren som arbeidselementene skal delegeres til, i **Deleger**-feltet.</span><span class="sxs-lookup"><span data-stu-id="52beb-135">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="52beb-136">Bruk feltene **Startdato/-klokkeslett** og **Sluttdato/-klokkeslett** til å angi når du vil at arbeidselementer skal delegeres automatisk.</span><span class="sxs-lookup"><span data-stu-id="52beb-136">Use the **Start date/time** and **End date/time** fields to specify when you want the work items to be automatically delegated.</span></span>  
7. <span data-ttu-id="52beb-137">Angi dato og klokkeslett i feltet **Startdato/-klokkeslett**.</span><span class="sxs-lookup"><span data-stu-id="52beb-137">In the **Start date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="52beb-138">Angi dato og klokkeslett i feltet **Sluttdato/-klokkeslett**.</span><span class="sxs-lookup"><span data-stu-id="52beb-138">In the **End date/time** field, enter a date and time.</span></span>
9. <span data-ttu-id="52beb-139">Merk av for **Aktivert** for å aktivere denne delegeringsregelen.</span><span class="sxs-lookup"><span data-stu-id="52beb-139">Select the **Enabled** check box to activate the delegation rule.</span></span> 
10. <span data-ttu-id="52beb-140">Angi en kommentar som forklarer hvorfor du delegerer arbeidselementene, i feltet **Kommentar**.</span><span class="sxs-lookup"><span data-stu-id="52beb-140">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]