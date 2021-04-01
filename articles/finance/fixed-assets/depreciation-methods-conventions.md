---
title: Avskrivningsmetoder og -konvensjoner
description: Denne artikkelen gir en oversikt over avskrivningskonvensjoner og avskrivningsmetoder som støttes av Microsoft Dynamics 365 Finance.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1aacc57051f21b992d9f7feb44c99511fc2a65bb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241296"
---
# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="46ea4-103">Avskrivningsmetoder og -konvensjoner</span><span class="sxs-lookup"><span data-stu-id="46ea4-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46ea4-104">Denne artikkelen gir en oversikt over avskrivningskonvensjoner og avskrivningsmetoder som støttes.</span><span class="sxs-lookup"><span data-stu-id="46ea4-104">This article provides an overview of the supported depreciation conventions and depreciation methods.</span></span>

<span data-ttu-id="46ea4-105">Du kan velge forskjellige avskrivningsmetoder og -konvensjoner.</span><span class="sxs-lookup"><span data-stu-id="46ea4-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="46ea4-106">Formålet med metodene er å tildele den avskrivbare verdien til anleggsmiddelet i regnskapsperioder.</span><span class="sxs-lookup"><span data-stu-id="46ea4-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="46ea4-107">Den avskrivbare verdien til anleggsmiddelet er anskaffelsesprisen minus eventuell svinnverdi.</span><span class="sxs-lookup"><span data-stu-id="46ea4-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="46ea4-108">Hvis du bruker avskrivningskonvensjoner, og du endrer den siste avskrivningskjøringsdatoen for en vare, noe som hopper over visse avskrivninger, kan avskrivningen for forrige år være større eller mindre enn forventet.</span><span class="sxs-lookup"><span data-stu-id="46ea4-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="46ea4-109">Avskrivningen justeres etter hvor mange avskrivningsperioder som påvirkes av endringen i den siste avskrivningskjøringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="46ea4-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="46ea4-110">Hvis du for eksempel bruker konvensjonen med halvårlig avskrivning over tre år, skjer avskrivningen vanligvis over 3,5 år.</span><span class="sxs-lookup"><span data-stu-id="46ea4-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="46ea4-111">Hvis du endrer den siste avskrivningskjøringsdatoen i løpet av de 3,5 årene, fjernes de periodene som påvirkes, fra det siste avskrivningsåret.</span><span class="sxs-lookup"><span data-stu-id="46ea4-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="46ea4-112">Hvis du flytter datoen med tre måneder, får du ni måneder med avskrivning det siste året i motsetning til de vanlige seks månedene.</span><span class="sxs-lookup"><span data-stu-id="46ea4-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="46ea4-113">Du kan velge mellom følgende avskrivningskonvensjoner.</span><span class="sxs-lookup"><span data-stu-id="46ea4-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="46ea4-114">Halvår</span><span class="sxs-lookup"><span data-stu-id="46ea4-114">Half year</span></span>
-   <span data-ttu-id="46ea4-115">Hele måneden</span><span class="sxs-lookup"><span data-stu-id="46ea4-115">Full month</span></span>
-   <span data-ttu-id="46ea4-116">Midt i kvartal</span><span class="sxs-lookup"><span data-stu-id="46ea4-116">Mid quarter</span></span>
-   <span data-ttu-id="46ea4-117">Midt i måneden (1. i måned)</span><span class="sxs-lookup"><span data-stu-id="46ea4-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="46ea4-118">Midt i måneden (15. i måned)</span><span class="sxs-lookup"><span data-stu-id="46ea4-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="46ea4-119">Halvår (starten på året)</span><span class="sxs-lookup"><span data-stu-id="46ea4-119">Half year (start of year)</span></span>
-   <span data-ttu-id="46ea4-120">Halvår (neste år)</span><span class="sxs-lookup"><span data-stu-id="46ea4-120">Half year (next year)</span></span>

<span data-ttu-id="46ea4-121">Du kan velge mellom følgende avskrivningsmetoder:</span><span class="sxs-lookup"><span data-stu-id="46ea4-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="46ea4-122">Lineær levetid</span><span class="sxs-lookup"><span data-stu-id="46ea4-122">Straight line service life</span></span>
-   <span data-ttu-id="46ea4-123">Saldoverdi</span><span class="sxs-lookup"><span data-stu-id="46ea4-123">Reducing balance</span></span>
-   <span data-ttu-id="46ea4-124">Manuelt</span><span class="sxs-lookup"><span data-stu-id="46ea4-124">Manual</span></span>
-   <span data-ttu-id="46ea4-125">Faktor</span><span class="sxs-lookup"><span data-stu-id="46ea4-125">Factor</span></span>
-   <span data-ttu-id="46ea4-126">Forbruk</span><span class="sxs-lookup"><span data-stu-id="46ea4-126">Consumption</span></span>
-   <span data-ttu-id="46ea4-127">Lineær levetid som gjenstår</span><span class="sxs-lookup"><span data-stu-id="46ea4-127">Straight line life remaining</span></span>
-   <span data-ttu-id="46ea4-128">200 % saldoverdi</span><span class="sxs-lookup"><span data-stu-id="46ea4-128">200% reducing balance</span></span>
-   <span data-ttu-id="46ea4-129">175 % saldoverdi</span><span class="sxs-lookup"><span data-stu-id="46ea4-129">175% reducing balance</span></span>
-   <span data-ttu-id="46ea4-130">150 % saldoverdi</span><span class="sxs-lookup"><span data-stu-id="46ea4-130">150% reducing balance</span></span>
-   <span data-ttu-id="46ea4-131">125 % saldoverdi</span><span class="sxs-lookup"><span data-stu-id="46ea4-131">125% reducing balance</span></span>





<a name="additional-resources"></a><span data-ttu-id="46ea4-132">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="46ea4-132">Additional resources</span></span>
--------

[<span data-ttu-id="46ea4-133">Avskrivning av anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="46ea4-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="46ea4-134">Lineær levetidsavskrivning</span><span class="sxs-lookup"><span data-stu-id="46ea4-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="46ea4-135">Redusere saldoavskrivning</span><span class="sxs-lookup"><span data-stu-id="46ea4-135">Reduce balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="46ea4-136">Manuell avskrivning</span><span class="sxs-lookup"><span data-stu-id="46ea4-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="46ea4-137">Faktoravskrivning</span><span class="sxs-lookup"><span data-stu-id="46ea4-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="46ea4-138">Forbruksavskrivning</span><span class="sxs-lookup"><span data-stu-id="46ea4-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="46ea4-139">Gjenstående lineær levetidsavskrivning</span><span class="sxs-lookup"><span data-stu-id="46ea4-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="46ea4-140">125 prosent redusert saldoavskrivning</span><span class="sxs-lookup"><span data-stu-id="46ea4-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="46ea4-141">150 prosent redusert saldoavskrivning</span><span class="sxs-lookup"><span data-stu-id="46ea4-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="46ea4-142">175 prosent redusert saldoavskrivning</span><span class="sxs-lookup"><span data-stu-id="46ea4-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="46ea4-143">200 prosent redusert saldoavskrivning</span><span class="sxs-lookup"><span data-stu-id="46ea4-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]