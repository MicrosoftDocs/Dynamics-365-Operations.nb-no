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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fed9f09b4e37da00a5d78fa088e8814db48456b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968935"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="80bce-103">Definere bonusavskrivning</span><span class="sxs-lookup"><span data-stu-id="80bce-103">Set up bonus depreciation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="80bce-104">Denne fremgangsmåten viser hvordan du oppretter et særskilt avskrivningsfradrag og knytter det til et anleggsmiddeltablå.</span><span class="sxs-lookup"><span data-stu-id="80bce-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="80bce-105">Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.</span><span class="sxs-lookup"><span data-stu-id="80bce-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="80bce-106">Opprette et særskilt avskrivningsfradrag</span><span class="sxs-lookup"><span data-stu-id="80bce-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="80bce-107">Gå til Anleggsmidler > Oppsett > Særskilte avskrivningsfradrag.</span><span class="sxs-lookup"><span data-stu-id="80bce-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="80bce-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="80bce-108">Click New.</span></span>
3. <span data-ttu-id="80bce-109">Skriv inn en verdi i feltet Særskilte avskrivningsfradrag.</span><span class="sxs-lookup"><span data-stu-id="80bce-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="80bce-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="80bce-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="80bce-111">Angi et tall i Prosent-feltet.</span><span class="sxs-lookup"><span data-stu-id="80bce-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="80bce-112">Hvis det ikke er angitt en prosent, angir du et beløp.</span><span class="sxs-lookup"><span data-stu-id="80bce-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="80bce-113">Tilknytte et særskilt avskrivningsfradrag til et anleggsmiddelgruppetablå</span><span class="sxs-lookup"><span data-stu-id="80bce-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="80bce-114">Gå til Anleggsmidler > Oppsett > Anleggsmiddelgrupper.</span><span class="sxs-lookup"><span data-stu-id="80bce-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="80bce-115">I listen velger du anleggsmiddelgruppen som er tilknyttet det særskilte avskrivningsfradraget.</span><span class="sxs-lookup"><span data-stu-id="80bce-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="80bce-116">Klikk Tablåer.</span><span class="sxs-lookup"><span data-stu-id="80bce-116">Click Books.</span></span>
4. <span data-ttu-id="80bce-117">I listen velger du tablået som er tilknyttet det særskilte avskrivningsfradraget.</span><span class="sxs-lookup"><span data-stu-id="80bce-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="80bce-118">Klikk Særskilt avskrivningsfradrag.</span><span class="sxs-lookup"><span data-stu-id="80bce-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="80bce-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="80bce-119">Click New.</span></span>
7. <span data-ttu-id="80bce-120">Skriv inn eller velg en verdi i feltet Særskilte avskrivningsfradrag.</span><span class="sxs-lookup"><span data-stu-id="80bce-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="80bce-121">Standard for prosenten eller beløpet hentes fra oppsettet for særskilte avskrivningsfradrag.</span><span class="sxs-lookup"><span data-stu-id="80bce-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="80bce-122">Angi et tall i Prioritet-feltet.</span><span class="sxs-lookup"><span data-stu-id="80bce-122">In the Priority field, enter a number.</span></span>

