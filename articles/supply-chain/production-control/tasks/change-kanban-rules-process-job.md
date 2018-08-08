--- 
title: Endre Kanban-regler for en prosessjobb
description: "Denne prosedyren fokuserer på å endre den brukte Kanban-regelen for en gitt Kanban."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 8fc47751534af69300bf8f0bdb7424043cab7b26
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="fee74-103">Endre Kanban-regler for en prosessjobb</span><span class="sxs-lookup"><span data-stu-id="fee74-103">Change kanban rules for a process job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fee74-104">Denne prosedyren fokuserer på å endre den brukte Kanban-regelen for en gitt Kanban.</span><span class="sxs-lookup"><span data-stu-id="fee74-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="fee74-105">Dette er nyttig for å nivåbelaste ressurser eller ved nedbryting.</span><span class="sxs-lookup"><span data-stu-id="fee74-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="fee74-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="fee74-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="fee74-107">Denne prosedyren er ment for planleggeren, som arbeider i et lean manufacturing-selskap, og som er ansvarlig for verdistrømmen.</span><span class="sxs-lookup"><span data-stu-id="fee74-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="fee74-108">Kopiere Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="fee74-108">Copy kanban rule</span></span>
1. <span data-ttu-id="fee74-109">Gå til Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="fee74-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="fee74-110">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="fee74-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fee74-111">Velg Kanban-regel for hendelse 000022 for L0001.</span><span class="sxs-lookup"><span data-stu-id="fee74-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="fee74-112">Klikk Dupliser Kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="fee74-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="fee74-113">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="fee74-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="fee74-114">Endre Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="fee74-114">Change kanban rule</span></span>
1. <span data-ttu-id="fee74-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fee74-115">Close the page.</span></span>
2. <span data-ttu-id="fee74-116">Gå til Kanban-jobbplanlegging.</span><span class="sxs-lookup"><span data-stu-id="fee74-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="fee74-117">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fee74-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="fee74-118">Velg linjen med Kanban 000177.</span><span class="sxs-lookup"><span data-stu-id="fee74-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="fee74-119">Klikk Bruk alternativ Kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="fee74-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="fee74-120">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="fee74-120">Click Next.</span></span>
6. <span data-ttu-id="fee74-121">Angi eller velg en verdi i feltet Kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="fee74-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="fee74-122">Velg Kanban-regelen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="fee74-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="fee74-123">Dette er Kanban-regelen med det høyeste nummeret.</span><span class="sxs-lookup"><span data-stu-id="fee74-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="fee74-124">Klikk Finish.</span><span class="sxs-lookup"><span data-stu-id="fee74-124">Click Finish.</span></span>
    * <span data-ttu-id="fee74-125">Kanban-jobben bruker nå en annen Kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="fee74-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="fee74-126">Dette kan være nyttig for å nivålaste arbeidsceller.</span><span class="sxs-lookup"><span data-stu-id="fee74-126">This can be useful to level load work cells.</span></span>  


