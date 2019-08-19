---
title: Definere bonusavskrivning
description: Denne fremgangsmåten viser hvordan du oppretter et særskilt avskrivningsfradrag og knytter det til et anleggsmiddeltablå.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 788cddf4d822fe3d3d6a33e83d7b30f32f4b6b9c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839887"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="35205-103">Definere bonusavskrivning</span><span class="sxs-lookup"><span data-stu-id="35205-103">Set up bonus depreciation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="35205-104">Denne fremgangsmåten viser hvordan du oppretter et særskilt avskrivningsfradrag og knytter det til et anleggsmiddeltablå.</span><span class="sxs-lookup"><span data-stu-id="35205-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="35205-105">Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.</span><span class="sxs-lookup"><span data-stu-id="35205-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="35205-106">Opprette et særskilt avskrivningsfradrag</span><span class="sxs-lookup"><span data-stu-id="35205-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="35205-107">Gå til Anleggsmidler > Oppsett > Særskilte avskrivningsfradrag.</span><span class="sxs-lookup"><span data-stu-id="35205-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="35205-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="35205-108">Click New.</span></span>
3. <span data-ttu-id="35205-109">Skriv inn en verdi i feltet Særskilte avskrivningsfradrag.</span><span class="sxs-lookup"><span data-stu-id="35205-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="35205-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="35205-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="35205-111">Angi et tall i Prosent-feltet.</span><span class="sxs-lookup"><span data-stu-id="35205-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="35205-112">Hvis det ikke er angitt en prosent, angir du et beløp.</span><span class="sxs-lookup"><span data-stu-id="35205-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="35205-113">Tilknytte et særskilt avskrivningsfradrag til et anleggsmiddelgruppetablå</span><span class="sxs-lookup"><span data-stu-id="35205-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="35205-114">Gå til Anleggsmidler > Oppsett > Anleggsmiddelgrupper.</span><span class="sxs-lookup"><span data-stu-id="35205-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="35205-115">I listen velger du anleggsmiddelgruppen som er tilknyttet det særskilte avskrivningsfradraget.</span><span class="sxs-lookup"><span data-stu-id="35205-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="35205-116">Klikk Tablåer.</span><span class="sxs-lookup"><span data-stu-id="35205-116">Click Books.</span></span>
4. <span data-ttu-id="35205-117">I listen velger du tablået som er tilknyttet det særskilte avskrivningsfradraget.</span><span class="sxs-lookup"><span data-stu-id="35205-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="35205-118">Klikk Særskilt avskrivningsfradrag.</span><span class="sxs-lookup"><span data-stu-id="35205-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="35205-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="35205-119">Click New.</span></span>
7. <span data-ttu-id="35205-120">Skriv inn eller velg en verdi i feltet Særskilte avskrivningsfradrag.</span><span class="sxs-lookup"><span data-stu-id="35205-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="35205-121">Standard for prosenten eller beløpet hentes fra oppsettet for særskilte avskrivningsfradrag.</span><span class="sxs-lookup"><span data-stu-id="35205-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="35205-122">Angi et tall i Prioritet-feltet.</span><span class="sxs-lookup"><span data-stu-id="35205-122">In the Priority field, enter a number.</span></span>

