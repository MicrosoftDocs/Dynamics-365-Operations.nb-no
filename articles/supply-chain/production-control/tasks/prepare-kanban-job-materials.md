---
title: "Klargjøre en Kanban-prosessjobb når materialer er tilgjengelige for arbeidscellen"
description: "Denne oppgaven fokuserer på å klargjøre en kanban-prosessjobb når alle materialer er tilgjengelige for arbeidscellen."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: fdedab1bfccafb4f8592aea8ec421e3ba311a94a
ms.contentlocale: nb-no
ms.lasthandoff: 02/06/2018

---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="77a8c-103">Klargjøre en Kanban-prosessjobb når materialer er tilgjengelige for arbeidscellen</span><span class="sxs-lookup"><span data-stu-id="77a8c-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="77a8c-104">Denne oppgaven fokuserer på å klargjøre en kanban-prosessjobb når alle materialer er tilgjengelige for arbeidscellen.</span><span class="sxs-lookup"><span data-stu-id="77a8c-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="77a8c-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="77a8c-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="77a8c-106">Denne oppgaven er ment for maskinoperatøren.</span><span class="sxs-lookup"><span data-stu-id="77a8c-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="77a8c-107">Gå til Kanban-tavle for prosessjobber.</span><span class="sxs-lookup"><span data-stu-id="77a8c-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="77a8c-108">Klikk rullegardinknappen i Arbeidscelle-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="77a8c-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="77a8c-109">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="77a8c-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="77a8c-110">Velg arbeidscellen 1250, og klikk OK.</span><span class="sxs-lookup"><span data-stu-id="77a8c-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="77a8c-111">Velg rad 4 i listen.</span><span class="sxs-lookup"><span data-stu-id="77a8c-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="77a8c-112">I demonstrasjonsfirmaet er Kanban 000329 i rad 4 den første jobben som ikke er fullført.</span><span class="sxs-lookup"><span data-stu-id="77a8c-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="77a8c-113">Aktiver/deaktiver utvidelsen av delen Plukkliste.</span><span class="sxs-lookup"><span data-stu-id="77a8c-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="77a8c-114">Kontroller at forsyningsstatusen er tilgjengelig for alle varene i plukklisten.</span><span class="sxs-lookup"><span data-stu-id="77a8c-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="77a8c-115">Hvis flere jobber er valgt, vises summen av alle varer som behøves for de valgte jobbene, i plukklisten.</span><span class="sxs-lookup"><span data-stu-id="77a8c-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="77a8c-116">Klikk Klargjør.</span><span class="sxs-lookup"><span data-stu-id="77a8c-116">Click Prepare.</span></span>
    * <span data-ttu-id="77a8c-117">Klargjøringsprosessen er nå fullført.</span><span class="sxs-lookup"><span data-stu-id="77a8c-117">The preparation process is now completed.</span></span> <span data-ttu-id="77a8c-118">Den valgte avmerkingsboksen for alle rader i plukklisten angir at forsyningsstatusen er plukket.</span><span class="sxs-lookup"><span data-stu-id="77a8c-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  

