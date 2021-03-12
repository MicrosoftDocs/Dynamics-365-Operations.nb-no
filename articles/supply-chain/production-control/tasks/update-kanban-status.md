---
title: Oppdatere Kanban-status
description: Når en kanban tømmes ved en feiltakelse eller en mottatt kanban må tømmes, må du oppdatere kanban-statusen.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1161e642f8b3b1cd0a2568e0745caa6db5fe5afb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981008"
---
# <a name="update-kanban-status"></a><span data-ttu-id="61791-103">Oppdatere Kanban-status</span><span class="sxs-lookup"><span data-stu-id="61791-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="61791-104">Når en kanban tømmes ved en feiltakelse eller en mottatt kanban må tømmes, må du oppdatere kanban-statusen.</span><span class="sxs-lookup"><span data-stu-id="61791-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="61791-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="61791-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="61791-106">Denne fremgangsmåten er ment for verkstedslederen.</span><span class="sxs-lookup"><span data-stu-id="61791-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="61791-107">Finn kanbanen.</span><span class="sxs-lookup"><span data-stu-id="61791-107">Find the kanban.</span></span>
1. <span data-ttu-id="61791-108">Gå til Produksjonskontroll > Kanban > Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="61791-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="61791-109">Åpne kolonnefilteret Status for håndteringsenhet.</span><span class="sxs-lookup"><span data-stu-id="61791-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="61791-110">Klikk på Fjern.</span><span class="sxs-lookup"><span data-stu-id="61791-110">Click Clear.</span></span>
    * <span data-ttu-id="61791-111">Dette tilbakestiller filtrene.</span><span class="sxs-lookup"><span data-stu-id="61791-111">This resets the filters.</span></span>  
4. <span data-ttu-id="61791-112">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="61791-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="61791-113">Du kan for eksempel filtrere på Kortnummer-feltet med verdien 000149.</span><span class="sxs-lookup"><span data-stu-id="61791-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="61791-114">Endre tømtstatus til mottattstatus</span><span class="sxs-lookup"><span data-stu-id="61791-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="61791-115">Klikk på Reverser tom håndteringsenhet.</span><span class="sxs-lookup"><span data-stu-id="61791-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="61791-116">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="61791-116">Click OK.</span></span>
    * <span data-ttu-id="61791-117">Legg merke til at statusen Håndteringsenhet er Mottatt.</span><span class="sxs-lookup"><span data-stu-id="61791-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="61791-118">Endre mottattstatus til tømtstatus</span><span class="sxs-lookup"><span data-stu-id="61791-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="61791-119">Klikk på Tøm Kanban.</span><span class="sxs-lookup"><span data-stu-id="61791-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="61791-120">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="61791-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="61791-121">Legg merke til at statusen Håndteringsenhet er Tømt.</span><span class="sxs-lookup"><span data-stu-id="61791-121">Notice that the Handling unit status is Emptied.</span></span>  

