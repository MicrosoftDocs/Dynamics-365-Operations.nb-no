---
title: Delegere arbeidselementer i en arbeidsflyt
description: Hvis du planlegger å være borte fra kontoret eller av andre grunner ikke er tilgjengelig til å behandle arbeidselementer, kan du delegere eller tilordne arbeidselementer til andre brukere.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: f85a1318822ceaf829134bf2eb3581e350d5bea4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "346255"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="4f251-103">Delegere arbeidselementer i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="4f251-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4f251-104">Hvis du planlegger å være borte fra kontoret eller av andre grunner ikke er tilgjengelig til å behandle arbeidselementer, kan du delegere eller tilordne arbeidselementer til andre brukere.</span><span class="sxs-lookup"><span data-stu-id="4f251-104">If you plan to be out of the office or otherwise unavailable to act on work items, you can delegate, or reassign, your work items to other users.</span></span> <span data-ttu-id="4f251-105">Dette hjelper deg med å konfigurere systemet slik at det automatisk delegerer arbeidsenhetene dine til en annen bruker.</span><span class="sxs-lookup"><span data-stu-id="4f251-105">This procedure helps you configure the system to automatically delegate your work items to another user.</span></span>



<span data-ttu-id="4f251-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="4f251-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-automatic-delegation"></a><span data-ttu-id="4f251-107">Definere automatisk delegering</span><span class="sxs-lookup"><span data-stu-id="4f251-107">Set up automatic delegation</span></span>
1. <span data-ttu-id="4f251-108">Gå til Felles > Oppsett > Brukeralternativer.</span><span class="sxs-lookup"><span data-stu-id="4f251-108">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="4f251-109">Klikk Arbeidsflyt-kategorien.</span><span class="sxs-lookup"><span data-stu-id="4f251-109">Click the Workflow tab.</span></span>
    * <span data-ttu-id="4f251-110">Kontroller at delen Delegering er utvidet.</span><span class="sxs-lookup"><span data-stu-id="4f251-110">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="4f251-111">Hvis du vil konfigurere systemet slik at det automatisk delegerer arbeidselementene dine til andre brukere, må du opprette delegeringsregler, som angir når bestemte typer arbeidselementer delegeres.</span><span class="sxs-lookup"><span data-stu-id="4f251-111">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="4f251-112">Hvis du vil opprette en delegeringsregel, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="4f251-112">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="4f251-113">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4f251-113">Click Add.</span></span>
4. <span data-ttu-id="4f251-114">Velg et alternativ i Omfang-feltet.</span><span class="sxs-lookup"><span data-stu-id="4f251-114">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="4f251-115">Alle – deleger alle arbeidsenheter som er tilordnet til deg.</span><span class="sxs-lookup"><span data-stu-id="4f251-115">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="4f251-116">Modul – deleger bare arbeidselementene som er knyttet til en bestemt type arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="4f251-116">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="4f251-117">Hvis du velger dette alternativet, må du velge typen arbeidsflyt i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4f251-117">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="4f251-118">Arbeidsflyt – deleger bare arbeidselementene som er knyttet til en bestemt arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="4f251-118">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="4f251-119">Hvis du velger dette alternativet, må du velge arbeidsflyten i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4f251-119">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="4f251-120">Velg brukeren som arbeidselementene skal delegeres til, i Deleger-feltet.</span><span class="sxs-lookup"><span data-stu-id="4f251-120">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="4f251-121">Bruk feltene Startdato/-klokkeslett og Sluttdato/-klokkeslett til å angi når du vil at arbeidselementer skal delegeres automatisk.</span><span class="sxs-lookup"><span data-stu-id="4f251-121">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="4f251-122">Angi dato og klokkeslett i feltet Startdato/-klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="4f251-122">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="4f251-123">Angi dato og klokkeslett i feltet Sluttdato/-klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="4f251-123">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="4f251-124">Merk av for Aktivert for å aktivere denne delegeringsregelen.</span><span class="sxs-lookup"><span data-stu-id="4f251-124">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="4f251-125">Hvis du valgte Modul som omfanget, må du velge modulen i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4f251-125">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="4f251-126">Hvis du valgte Arbeidsflyt som omfanget, må du velge den bestemte arbeidsflyten som skal delegeres, i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4f251-126">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="4f251-127">Angi en kommentar som forklarer hvorfor du delegerer arbeidselementene, i feltet Kommentar.</span><span class="sxs-lookup"><span data-stu-id="4f251-127">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>

