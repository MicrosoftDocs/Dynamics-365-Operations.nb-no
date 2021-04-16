---
title: Klargjøre en Kanban-prosessjobb når materialer er tilgjengelige for arbeidscellen
description: Denne oppgaven fokuserer på å klargjøre en kanban-prosessjobb når alle materialer er tilgjengelige for arbeidscellen.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 460d55a8c4b8a8401db7abc43721cf0d114c27c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807830"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="bc90e-103">Klargjøre en Kanban-prosessjobb når materialer er tilgjengelige for arbeidscellen</span><span class="sxs-lookup"><span data-stu-id="bc90e-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bc90e-104">Denne oppgaven fokuserer på å klargjøre en kanban-prosessjobb når alle materialer er tilgjengelige for arbeidscellen.</span><span class="sxs-lookup"><span data-stu-id="bc90e-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="bc90e-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="bc90e-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="bc90e-106">Denne oppgaven er ment for maskinoperatøren.</span><span class="sxs-lookup"><span data-stu-id="bc90e-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="bc90e-107">Gå til Kanban-tavle for prosessjobber.</span><span class="sxs-lookup"><span data-stu-id="bc90e-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="bc90e-108">Klikk på rullegardinknappen i Arbeidscelle-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="bc90e-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="bc90e-109">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="bc90e-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="bc90e-110">Velg arbeidscellen 1250, og klikk OK.</span><span class="sxs-lookup"><span data-stu-id="bc90e-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="bc90e-111">Velg rad 4 i listen.</span><span class="sxs-lookup"><span data-stu-id="bc90e-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="bc90e-112">I demonstrasjonsfirmaet er Kanban 000329 i rad 4 den første jobben som ikke er fullført.</span><span class="sxs-lookup"><span data-stu-id="bc90e-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="bc90e-113">Aktiver/deaktiver utvidelsen av delen Plukkliste.</span><span class="sxs-lookup"><span data-stu-id="bc90e-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="bc90e-114">Kontroller at forsyningsstatusen er tilgjengelig for alle varene i plukklisten.</span><span class="sxs-lookup"><span data-stu-id="bc90e-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="bc90e-115">Hvis flere jobber er valgt, vises summen av alle varer som behøves for de valgte jobbene, i plukklisten.</span><span class="sxs-lookup"><span data-stu-id="bc90e-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="bc90e-116">Klikk på Klargjør.</span><span class="sxs-lookup"><span data-stu-id="bc90e-116">Click Prepare.</span></span>
    * <span data-ttu-id="bc90e-117">Klargjøringsprosessen er nå fullført.</span><span class="sxs-lookup"><span data-stu-id="bc90e-117">The preparation process is now completed.</span></span> <span data-ttu-id="bc90e-118">Den valgte avmerkingsboksen for alle rader i plukklisten angir at forsyningsstatusen er plukket.</span><span class="sxs-lookup"><span data-stu-id="bc90e-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]