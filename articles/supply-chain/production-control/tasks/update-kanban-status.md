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
ms.openlocfilehash: 055765452579b1de74f1c2158de9c6cb4ee80f16
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252828"
---
# <a name="update-kanban-status"></a><span data-ttu-id="9428d-103">Oppdatere Kanban-status</span><span class="sxs-lookup"><span data-stu-id="9428d-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9428d-104">Når en kanban tømmes ved en feiltakelse eller en mottatt kanban må tømmes, må du oppdatere kanban-statusen.</span><span class="sxs-lookup"><span data-stu-id="9428d-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="9428d-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="9428d-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9428d-106">Denne fremgangsmåten er ment for verkstedslederen.</span><span class="sxs-lookup"><span data-stu-id="9428d-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="9428d-107">Finn kanbanen.</span><span class="sxs-lookup"><span data-stu-id="9428d-107">Find the kanban.</span></span>
1. <span data-ttu-id="9428d-108">Gå til Produksjonskontroll > Kanban > Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="9428d-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="9428d-109">Åpne kolonnefilteret Status for håndteringsenhet.</span><span class="sxs-lookup"><span data-stu-id="9428d-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="9428d-110">Klikk på Fjern.</span><span class="sxs-lookup"><span data-stu-id="9428d-110">Click Clear.</span></span>
    * <span data-ttu-id="9428d-111">Dette tilbakestiller filtrene.</span><span class="sxs-lookup"><span data-stu-id="9428d-111">This resets the filters.</span></span>  
4. <span data-ttu-id="9428d-112">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="9428d-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9428d-113">Du kan for eksempel filtrere på Kortnummer-feltet med verdien 000149.</span><span class="sxs-lookup"><span data-stu-id="9428d-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="9428d-114">Endre tømtstatus til mottattstatus</span><span class="sxs-lookup"><span data-stu-id="9428d-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="9428d-115">Klikk på Reverser tom håndteringsenhet.</span><span class="sxs-lookup"><span data-stu-id="9428d-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="9428d-116">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="9428d-116">Click OK.</span></span>
    * <span data-ttu-id="9428d-117">Legg merke til at statusen Håndteringsenhet er Mottatt.</span><span class="sxs-lookup"><span data-stu-id="9428d-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="9428d-118">Endre mottattstatus til tømtstatus</span><span class="sxs-lookup"><span data-stu-id="9428d-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="9428d-119">Klikk på Tøm Kanban.</span><span class="sxs-lookup"><span data-stu-id="9428d-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="9428d-120">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9428d-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9428d-121">Legg merke til at statusen Håndteringsenhet er Tømt.</span><span class="sxs-lookup"><span data-stu-id="9428d-121">Notice that the Handling unit status is Emptied.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]