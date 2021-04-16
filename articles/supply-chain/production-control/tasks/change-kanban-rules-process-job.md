---
title: Endre Kanban-regler for en prosessjobb
description: Denne prosedyren fokuserer på å endre den brukte Kanban-regelen for en gitt Kanban.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bdbbbf8a8b3d1596c251224cba996c0631050c4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829312"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="ffe6a-103">Endre Kanban-regler for en prosessjobb</span><span class="sxs-lookup"><span data-stu-id="ffe6a-103">Change kanban rules for a process job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ffe6a-104">Denne prosedyren fokuserer på å endre den brukte Kanban-regelen for en gitt Kanban.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="ffe6a-105">Dette er nyttig for å nivåbelaste ressurser eller ved nedbryting.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="ffe6a-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ffe6a-107">Denne prosedyren er ment for planleggeren, som arbeider i et lean manufacturing-selskap, og som er ansvarlig for verdistrømmen.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="ffe6a-108">Kopiere Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="ffe6a-108">Copy kanban rule</span></span>
1. <span data-ttu-id="ffe6a-109">Gå til Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="ffe6a-110">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ffe6a-111">Velg Kanban-regel for hendelse 000022 for L0001.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="ffe6a-112">Klikk på Dupliser Kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="ffe6a-113">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="ffe6a-114">Endre Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="ffe6a-114">Change kanban rule</span></span>
1. <span data-ttu-id="ffe6a-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-115">Close the page.</span></span>
2. <span data-ttu-id="ffe6a-116">Gå til Kanban-jobbplanlegging.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="ffe6a-117">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ffe6a-118">Velg linjen med Kanban 000177.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="ffe6a-119">Klikk på Bruk alternativ Kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="ffe6a-120">Klikk på Neste.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-120">Click Next.</span></span>
6. <span data-ttu-id="ffe6a-121">Angi eller velg en verdi i feltet Kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="ffe6a-122">Velg Kanban-regelen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="ffe6a-123">Dette er Kanban-regelen med det høyeste nummeret.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="ffe6a-124">Klikk på Finish.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-124">Click Finish.</span></span>
    * <span data-ttu-id="ffe6a-125">Kanban-jobben bruker nå en annen Kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="ffe6a-126">Dette kan være nyttig for å nivålaste arbeidsceller.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-126">This can be useful to level load work cells.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]