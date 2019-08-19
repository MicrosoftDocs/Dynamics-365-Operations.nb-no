---
title: Kjøre Kanban-prosessjobber
description: Denne prosedyren fokuserer på utfører Kanban-prosessjobber.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08fddd6404bf835283adaca14ad7ceb851f5a489
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837644"
---
# <a name="execute-kanban-process-jobs"></a><span data-ttu-id="35b75-103">Kjøre Kanban-prosessjobber</span><span class="sxs-lookup"><span data-stu-id="35b75-103">Execute kanban process jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="35b75-104">Denne prosedyren fokuserer på utfører Kanban-prosessjobber.</span><span class="sxs-lookup"><span data-stu-id="35b75-104">This procedure focuses on executing kanban process jobs.</span></span> <span data-ttu-id="35b75-105">Den første jobben fullføres med det forventede antallet og har ingen feil.</span><span class="sxs-lookup"><span data-stu-id="35b75-105">The first job is completed with the expected quantity and has no errors.</span></span> <span data-ttu-id="35b75-106">Den andre jobben fullføres med feil.</span><span class="sxs-lookup"><span data-stu-id="35b75-106">The second job is completed with errors.</span></span> <span data-ttu-id="35b75-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="35b75-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="35b75-108">Denne prosedyren er ment for maskinoperatøren.</span><span class="sxs-lookup"><span data-stu-id="35b75-108">This procedure is intended for the machine operator.</span></span>


## <a name="select-a-kanban-job"></a><span data-ttu-id="35b75-109">Merke en Kanban-jobb</span><span class="sxs-lookup"><span data-stu-id="35b75-109">Select a kanban job</span></span>
1. <span data-ttu-id="35b75-110">Gå til Produksjonskontroll > Kanban > Kanban-tavle for prosessjobber.</span><span class="sxs-lookup"><span data-stu-id="35b75-110">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="35b75-111">Klikk rullegardinknappen i Arbeidscelle-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="35b75-111">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="35b75-112">Klikk raden med ressursgruppe 1250.</span><span class="sxs-lookup"><span data-stu-id="35b75-112">Click the row with resource group 1250.</span></span> <span data-ttu-id="35b75-113">Dette filtrerer jobblisten slik at bare jobbene for arbeidscelle 1250 vises.</span><span class="sxs-lookup"><span data-stu-id="35b75-113">This filters the Jobs list to display only the jobs for work cell 1250.</span></span>
    * <span data-ttu-id="35b75-114">Merke raden som har jobbstatusen Planlagt.</span><span class="sxs-lookup"><span data-stu-id="35b75-114">Mark the row that has the Planned job status.</span></span>  

## <a name="complete-a-job-with-expected-quantity"></a><span data-ttu-id="35b75-115">Fullføre en jobb med forventet antall</span><span class="sxs-lookup"><span data-stu-id="35b75-115">Complete a job with expected quantity</span></span>
1. <span data-ttu-id="35b75-116">Vis eller skjul delen Detaljer.</span><span class="sxs-lookup"><span data-stu-id="35b75-116">Expand or collapse the Details section.</span></span>
    * <span data-ttu-id="35b75-117">Denne delen viser viktig informasjon om kortnummer, varenummer, antall bestilt og aktivitetsnavn.</span><span class="sxs-lookup"><span data-stu-id="35b75-117">This section displays important information about card number, item number, quantity ordered, and activity name.</span></span>  
2. <span data-ttu-id="35b75-118">Vis eller skjul delen Produksjonsinstruksjoner.</span><span class="sxs-lookup"><span data-stu-id="35b75-118">Expand or collapse the Production instructions section.</span></span>
    * <span data-ttu-id="35b75-119">Denne delen viser produksjonsinstruksjoner for aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="35b75-119">This section displays production instructions for the activity.</span></span> <span data-ttu-id="35b75-120">Instruksjonene kan være tekst, bilder, tegninger og andre dokumenter.</span><span class="sxs-lookup"><span data-stu-id="35b75-120">The instructions can be text, pictures, drawings, and other documents.</span></span>  
3. <span data-ttu-id="35b75-121">Klikk Start.</span><span class="sxs-lookup"><span data-stu-id="35b75-121">Click Start.</span></span>
    * <span data-ttu-id="35b75-122">Velg en jobb som ikke er fullført.</span><span class="sxs-lookup"><span data-stu-id="35b75-122">Select a job that is not completed.</span></span> <span data-ttu-id="35b75-123">Bruk statusikoner i statusfeltet for jobben for å vise jobbstatus.</span><span class="sxs-lookup"><span data-stu-id="35b75-123">Use status icons in the Job status field to view job status.</span></span>      
4. <span data-ttu-id="35b75-124">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="35b75-124">Click Complete.</span></span>
    * <span data-ttu-id="35b75-125">Jobben er fullført med den forventede kvaliteten.</span><span class="sxs-lookup"><span data-stu-id="35b75-125">The job is completed with the expected quality.</span></span>  

## <a name="complete-a-job-with-errors"></a><span data-ttu-id="35b75-126">Fullføre en jobb med feil</span><span class="sxs-lookup"><span data-stu-id="35b75-126">Complete a job with errors</span></span>
1. <span data-ttu-id="35b75-127">Klikk Start.</span><span class="sxs-lookup"><span data-stu-id="35b75-127">Click Start.</span></span>
    * <span data-ttu-id="35b75-128">Når en jobb er fullført, velges den neste jobben i listen automatisk.</span><span class="sxs-lookup"><span data-stu-id="35b75-128">When a job is completed, the next job on the list is selected automatically.</span></span> <span data-ttu-id="35b75-129">Dette er grunnen til at du ikke trenger å velge en jobb før du klikker Start.</span><span class="sxs-lookup"><span data-stu-id="35b75-129">This is why you don't need to select a job before you click Start.</span></span>  
2. <span data-ttu-id="35b75-130">Klikk Produksjon i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="35b75-130">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="35b75-131">Klikk Fullfør (detaljer).</span><span class="sxs-lookup"><span data-stu-id="35b75-131">Click Complete (details).</span></span>
4. <span data-ttu-id="35b75-132">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="35b75-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="35b75-133">Angi et tall i Antall feil-feltet.</span><span class="sxs-lookup"><span data-stu-id="35b75-133">In the Error quantity field, enter a number.</span></span>
6. <span data-ttu-id="35b75-134">Angi et tall i feltet Antall korrekte-antall.</span><span class="sxs-lookup"><span data-stu-id="35b75-134">In the Good quantity field, enter a number.</span></span>
7. <span data-ttu-id="35b75-135">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="35b75-135">Click OK.</span></span>

