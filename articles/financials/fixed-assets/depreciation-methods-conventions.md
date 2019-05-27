---
title: Avskrivningsmetoder og -konvensjoner
description: Denne artikkelen gir en oversikt over avskrivningskonvensjoner og avskrivningsmetoder som støttes av Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be8e05a386178b9172a906109e015269dc72b32e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569661"
---
# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="d5a2a-103">Avskrivningsmetoder og -konvensjoner</span><span class="sxs-lookup"><span data-stu-id="d5a2a-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5a2a-104">Denne artikkelen gir en oversikt over avskrivningskonvensjoner og avskrivningsmetoder som støttes av Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d5a2a-104">This article provides an overview of the depreciation conventions and depreciation methods that are supported by Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="d5a2a-105">Du kan velge forskjellige avskrivningsmetoder og -konvensjoner.</span><span class="sxs-lookup"><span data-stu-id="d5a2a-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="d5a2a-106">Formålet med metodene er å tildele den avskrivbare verdien til anleggsmiddelet i regnskapsperioder.</span><span class="sxs-lookup"><span data-stu-id="d5a2a-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="d5a2a-107">Den avskrivbare verdien til anleggsmiddelet er anskaffelsesprisen minus eventuell svinnverdi.</span><span class="sxs-lookup"><span data-stu-id="d5a2a-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="d5a2a-108">Hvis du bruker avskrivningskonvensjoner, og du endrer den siste avskrivningskjøringsdatoen for en vare, noe som hopper over visse avskrivninger, kan avskrivningen for forrige år være større eller mindre enn forventet.</span><span class="sxs-lookup"><span data-stu-id="d5a2a-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="d5a2a-109">Avskrivningen justeres etter hvor mange avskrivningsperioder som påvirkes av endringen i den siste avskrivningskjøringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="d5a2a-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="d5a2a-110">Hvis du for eksempel bruker konvensjonen med halvårlig avskrivning over tre år, skjer avskrivningen vanligvis over 3,5 år.</span><span class="sxs-lookup"><span data-stu-id="d5a2a-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="d5a2a-111">Hvis du endrer den siste avskrivningskjøringsdatoen i løpet av de 3,5 årene, fjernes de periodene som påvirkes, fra det siste avskrivningsåret.</span><span class="sxs-lookup"><span data-stu-id="d5a2a-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="d5a2a-112">Hvis du flytter datoen med tre måneder, får du ni måneder med avskrivning det siste året i motsetning til de vanlige seks månedene.</span><span class="sxs-lookup"><span data-stu-id="d5a2a-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="d5a2a-113">Du kan velge mellom følgende avskrivningskonvensjoner.</span><span class="sxs-lookup"><span data-stu-id="d5a2a-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="d5a2a-114">Halvår</span><span class="sxs-lookup"><span data-stu-id="d5a2a-114">Half year</span></span>
-   <span data-ttu-id="d5a2a-115">Hele måneden</span><span class="sxs-lookup"><span data-stu-id="d5a2a-115">Full month</span></span>
-   <span data-ttu-id="d5a2a-116">Midt i kvartal</span><span class="sxs-lookup"><span data-stu-id="d5a2a-116">Mid quarter</span></span>
-   <span data-ttu-id="d5a2a-117">Midt i måneden (1. i måned)</span><span class="sxs-lookup"><span data-stu-id="d5a2a-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="d5a2a-118">Midt i måneden (15. i måned)</span><span class="sxs-lookup"><span data-stu-id="d5a2a-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="d5a2a-119">Halvår (starten på året)</span><span class="sxs-lookup"><span data-stu-id="d5a2a-119">Half year (start of year)</span></span>
-   <span data-ttu-id="d5a2a-120">Halvår (neste år)</span><span class="sxs-lookup"><span data-stu-id="d5a2a-120">Half year (next year)</span></span>

<span data-ttu-id="d5a2a-121">Du kan velge mellom følgende avskrivningsmetoder:</span><span class="sxs-lookup"><span data-stu-id="d5a2a-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="d5a2a-122">Lineær levetid</span><span class="sxs-lookup"><span data-stu-id="d5a2a-122">Straight line service life</span></span>
-   <span data-ttu-id="d5a2a-123">Saldoverdi</span><span class="sxs-lookup"><span data-stu-id="d5a2a-123">Reducing balance</span></span>
-   <span data-ttu-id="d5a2a-124">Manuelt</span><span class="sxs-lookup"><span data-stu-id="d5a2a-124">Manual</span></span>
-   <span data-ttu-id="d5a2a-125">Faktor</span><span class="sxs-lookup"><span data-stu-id="d5a2a-125">Factor</span></span>
-   <span data-ttu-id="d5a2a-126">Forbruk</span><span class="sxs-lookup"><span data-stu-id="d5a2a-126">Consumption</span></span>
-   <span data-ttu-id="d5a2a-127">Lineær levetid som gjenstår</span><span class="sxs-lookup"><span data-stu-id="d5a2a-127">Straight line life remaining</span></span>
-   <span data-ttu-id="d5a2a-128">200 % saldoverdi</span><span class="sxs-lookup"><span data-stu-id="d5a2a-128">200% reducing balance</span></span>
-   <span data-ttu-id="d5a2a-129">175 % saldoverdi</span><span class="sxs-lookup"><span data-stu-id="d5a2a-129">175% reducing balance</span></span>
-   <span data-ttu-id="d5a2a-130">150 % saldoverdi</span><span class="sxs-lookup"><span data-stu-id="d5a2a-130">150% reducing balance</span></span>
-   <span data-ttu-id="d5a2a-131">125 % saldoverdi</span><span class="sxs-lookup"><span data-stu-id="d5a2a-131">125% reducing balance</span></span>





<a name="additional-resources"></a><span data-ttu-id="d5a2a-132">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d5a2a-132">Additional resources</span></span>
--------

[<span data-ttu-id="d5a2a-133">Avskrivning av anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="d5a2a-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="d5a2a-134">Lineær levetidsavskrivning</span><span class="sxs-lookup"><span data-stu-id="d5a2a-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="d5a2a-135">Redusere saldoavskrivning</span><span class="sxs-lookup"><span data-stu-id="d5a2a-135">Reducing balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="d5a2a-136">Manuell avskrivning</span><span class="sxs-lookup"><span data-stu-id="d5a2a-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="d5a2a-137">Faktoravskrivning</span><span class="sxs-lookup"><span data-stu-id="d5a2a-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="d5a2a-138">Forbruksavskrivning</span><span class="sxs-lookup"><span data-stu-id="d5a2a-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="d5a2a-139">Gjenstående lineær levetidsavskrivning</span><span class="sxs-lookup"><span data-stu-id="d5a2a-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="d5a2a-140">125 prosent redusert saldoavskrivning</span><span class="sxs-lookup"><span data-stu-id="d5a2a-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="d5a2a-141">150 prosent redusert saldoavskrivning</span><span class="sxs-lookup"><span data-stu-id="d5a2a-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="d5a2a-142">175 prosent redusert saldoavskrivning</span><span class="sxs-lookup"><span data-stu-id="d5a2a-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="d5a2a-143">200 prosent redusert saldoavskrivning</span><span class="sxs-lookup"><span data-stu-id="d5a2a-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)



