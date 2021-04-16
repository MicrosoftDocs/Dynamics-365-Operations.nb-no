---
title: Oppdatere Kanban-status
description: Når en kanban tømmes ved en feiltakelse eller en mottatt kanban må tømmes, må du oppdatere kanban-statusen.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a0e03da4671ffec4ecf4835b20a00ef87971c94
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831823"
---
# <a name="update-kanban-status"></a><span data-ttu-id="3c4ca-103">Oppdatere Kanban-status</span><span class="sxs-lookup"><span data-stu-id="3c4ca-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3c4ca-104">Når en kanban tømmes ved en feiltakelse eller en mottatt kanban må tømmes, må du oppdatere kanban-statusen.</span><span class="sxs-lookup"><span data-stu-id="3c4ca-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="3c4ca-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="3c4ca-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3c4ca-106">Denne fremgangsmåten er ment for verkstedslederen.</span><span class="sxs-lookup"><span data-stu-id="3c4ca-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="3c4ca-107">Finn kanbanen.</span><span class="sxs-lookup"><span data-stu-id="3c4ca-107">Find the kanban.</span></span>
1. <span data-ttu-id="3c4ca-108">Gå til Produksjonskontroll > Kanban > Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="3c4ca-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="3c4ca-109">Åpne kolonnefilteret Status for håndteringsenhet.</span><span class="sxs-lookup"><span data-stu-id="3c4ca-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="3c4ca-110">Klikk på Fjern.</span><span class="sxs-lookup"><span data-stu-id="3c4ca-110">Click Clear.</span></span>
    * <span data-ttu-id="3c4ca-111">Dette tilbakestiller filtrene.</span><span class="sxs-lookup"><span data-stu-id="3c4ca-111">This resets the filters.</span></span>  
4. <span data-ttu-id="3c4ca-112">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="3c4ca-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3c4ca-113">Du kan for eksempel filtrere på Kortnummer-feltet med verdien 000149.</span><span class="sxs-lookup"><span data-stu-id="3c4ca-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="3c4ca-114">Endre tømtstatus til mottattstatus</span><span class="sxs-lookup"><span data-stu-id="3c4ca-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="3c4ca-115">Klikk på Reverser tom håndteringsenhet.</span><span class="sxs-lookup"><span data-stu-id="3c4ca-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="3c4ca-116">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="3c4ca-116">Click OK.</span></span>
    * <span data-ttu-id="3c4ca-117">Legg merke til at statusen Håndteringsenhet er Mottatt.</span><span class="sxs-lookup"><span data-stu-id="3c4ca-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="3c4ca-118">Endre mottattstatus til tømtstatus</span><span class="sxs-lookup"><span data-stu-id="3c4ca-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="3c4ca-119">Klikk på Tøm Kanban.</span><span class="sxs-lookup"><span data-stu-id="3c4ca-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="3c4ca-120">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3c4ca-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="3c4ca-121">Legg merke til at statusen Håndteringsenhet er Tømt.</span><span class="sxs-lookup"><span data-stu-id="3c4ca-121">Notice that the Handling unit status is Emptied.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]