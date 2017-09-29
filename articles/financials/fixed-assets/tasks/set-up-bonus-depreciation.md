--- 
title: Definere bonusavskrivning
description: "Denne fremgangsmåten viser hvordan du oppretter et særskilt avskrivningsfradrag og knytter det til et anleggsmiddeltablå."
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7e6ebb13084626b477b6e0b24acdc09e2c0d3d6d
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="efcaf-103">Definere bonusavskrivning</span><span class="sxs-lookup"><span data-stu-id="efcaf-103">Set up bonus depreciation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="efcaf-104">Denne fremgangsmåten viser hvordan du oppretter et særskilt avskrivningsfradrag og knytter det til et anleggsmiddeltablå.</span><span class="sxs-lookup"><span data-stu-id="efcaf-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="efcaf-105">Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.</span><span class="sxs-lookup"><span data-stu-id="efcaf-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="efcaf-106">Opprette et særskilt avskrivningsfradrag</span><span class="sxs-lookup"><span data-stu-id="efcaf-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="efcaf-107">Gå til Anleggsmidler > Oppsett > Særskilte avskrivningsfradrag.</span><span class="sxs-lookup"><span data-stu-id="efcaf-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="efcaf-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="efcaf-108">Click New.</span></span>
3. <span data-ttu-id="efcaf-109">Skriv inn en verdi i feltet Særskilte avskrivningsfradrag.</span><span class="sxs-lookup"><span data-stu-id="efcaf-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="efcaf-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="efcaf-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="efcaf-111">Angi et tall i Prosent-feltet.</span><span class="sxs-lookup"><span data-stu-id="efcaf-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="efcaf-112">Hvis det ikke er angitt en prosent, angir du et beløp.</span><span class="sxs-lookup"><span data-stu-id="efcaf-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="efcaf-113">Tilknytte et særskilt avskrivningsfradrag til et anleggsmiddelgruppetablå</span><span class="sxs-lookup"><span data-stu-id="efcaf-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="efcaf-114">Gå til Anleggsmidler > Oppsett > Anleggsmiddelgrupper.</span><span class="sxs-lookup"><span data-stu-id="efcaf-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="efcaf-115">I listen velger du anleggsmiddelgruppen som er tilknyttet det særskilte avskrivningsfradraget.</span><span class="sxs-lookup"><span data-stu-id="efcaf-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="efcaf-116">Klikk Tablåer.</span><span class="sxs-lookup"><span data-stu-id="efcaf-116">Click Books.</span></span>
4. <span data-ttu-id="efcaf-117">I listen velger du tablået som er tilknyttet det særskilte avskrivningsfradraget.</span><span class="sxs-lookup"><span data-stu-id="efcaf-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="efcaf-118">Klikk Særskilt avskrivningsfradrag.</span><span class="sxs-lookup"><span data-stu-id="efcaf-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="efcaf-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="efcaf-119">Click New.</span></span>
7. <span data-ttu-id="efcaf-120">Skriv inn eller velg en verdi i feltet Særskilte avskrivningsfradrag.</span><span class="sxs-lookup"><span data-stu-id="efcaf-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="efcaf-121">Standard for prosenten eller beløpet hentes fra oppsettet for særskilte avskrivningsfradrag.</span><span class="sxs-lookup"><span data-stu-id="efcaf-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="efcaf-122">Angi et tall i Prioritet-feltet.</span><span class="sxs-lookup"><span data-stu-id="efcaf-122">In the Priority field, enter a number.</span></span>


