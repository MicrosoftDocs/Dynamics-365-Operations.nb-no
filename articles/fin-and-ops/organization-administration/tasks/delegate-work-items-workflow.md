---
title: Delegere arbeidselementer i en arbeidsflyt
description: Hvis du planlegger å være borte fra kontoret eller av andre grunner ikke er tilgjengelig til å behandle arbeidselementer, kan du delegere eller tilordne arbeidselementer til andre brukere.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44dc747543e32b54729d12c89a401b0187e25a61
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916421"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="10355-103">Delegere arbeidselementer i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="10355-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="10355-104">Delegere et arbeidselement manuelt</span><span class="sxs-lookup"><span data-stu-id="10355-104">Manually delegate a work item</span></span>

<span data-ttu-id="10355-105">For å delegere et individuelt arbeidselement, velg **Deleger**-alternativet på **Arbeidsflyt**-menyen, og angi deretter brukeren det skal delegeres til, sammen med en kommentar.</span><span class="sxs-lookup"><span data-stu-id="10355-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="10355-106">Dette vil tilordne arbeidselementet til denne brukeren, slik at vedkommende kan fullføre det.</span><span class="sxs-lookup"><span data-stu-id="10355-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="10355-107">Automatisk delegere arbeidselementer</span><span class="sxs-lookup"><span data-stu-id="10355-107">Automatically delegate work items</span></span>

<span data-ttu-id="10355-108">Hvis du planlegger å være borte fra kontoret eller å ikke være tilgjengelig for jobb med arbeidselementer i en bestemt tidsperiode, kan du automatisk delegere nye arbeidselementer til andre brukere ved hjelp av siden **Brukeralternativer**.</span><span class="sxs-lookup"><span data-stu-id="10355-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="10355-109">Definere automatisk delegering</span><span class="sxs-lookup"><span data-stu-id="10355-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="10355-110">Gå til **Felles > Oppsett > Brukeralternativer**.</span><span class="sxs-lookup"><span data-stu-id="10355-110">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="10355-111">Klikk på kategorien **Arbeidsflyt**. Kontroller at Delegering-delen er utvidet.</span><span class="sxs-lookup"><span data-stu-id="10355-111">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="10355-112">Hvis du vil konfigurere systemet slik at det automatisk delegerer arbeidselementene dine til andre brukere, må du opprette delegeringsregler, som angir når bestemte typer arbeidselementer delegeres.</span><span class="sxs-lookup"><span data-stu-id="10355-112">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="10355-113">Hvis du vil opprette en delegeringsregel, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="10355-113">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="10355-114">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="10355-114">Click **Add**.</span></span>
4. <span data-ttu-id="10355-115">Velg et alternativ i **Omfang**-feltet.</span><span class="sxs-lookup"><span data-stu-id="10355-115">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="10355-116">Alle – deleger alle arbeidsenheter som er tilordnet til deg.</span><span class="sxs-lookup"><span data-stu-id="10355-116">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="10355-117">Modul – deleger bare arbeidselementene som er knyttet til en bestemt type arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="10355-117">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="10355-118">Hvis du velger dette alternativet, må du velge typen arbeidsflyt i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="10355-118">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="10355-119">Arbeidsflyt – deleger bare arbeidselementene som er knyttet til en bestemt arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="10355-119">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="10355-120">Hvis du velger dette alternativet, må du velge arbeidsflyten i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="10355-120">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="10355-121">Velg brukeren som arbeidselementene skal delegeres til, i **Deleger**-feltet.</span><span class="sxs-lookup"><span data-stu-id="10355-121">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="10355-122">Bruk feltene Startdato/-klokkeslett og Sluttdato/-klokkeslett til å angi når du vil at arbeidselementer skal delegeres automatisk.</span><span class="sxs-lookup"><span data-stu-id="10355-122">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="10355-123">Angi dato og klokkeslett i feltet **Startdato/-klokkeslett**.</span><span class="sxs-lookup"><span data-stu-id="10355-123">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="10355-124">Angi dato og klokkeslett i feltet **Sluttdato/-klokkeslett**.</span><span class="sxs-lookup"><span data-stu-id="10355-124">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="10355-125">Merk av for **Aktivert** for å aktivere denne delegeringsregelen.</span><span class="sxs-lookup"><span data-stu-id="10355-125">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="10355-126">Hvis du valgte **Modul** som omfanget, må du velge modulen i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="10355-126">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="10355-127">Hvis du valgte **Arbeidsflyt** som omfanget, må du velge den bestemte arbeidsflyten som skal delegeres, i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="10355-127">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="10355-128">Angi en **kommentar** som forklarer hvorfor du delegerer arbeidselementene, i feltet Kommentar.</span><span class="sxs-lookup"><span data-stu-id="10355-128">In the **Comment** field, enter a comment that explains why you are delegating the work items.</span></span>

