---
title: Forbruksavskrivning
description: Denne artikkelen gir en oversikt over forbruksmetoden for avskrivning.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c9d95a7a45ed99c63516749285126c786685c87
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840703"
---
# <a name="consumption-depreciation"></a><span data-ttu-id="ecdb9-103">Forbruksavskrivning</span><span class="sxs-lookup"><span data-stu-id="ecdb9-103">Consumption depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecdb9-104">Denne artikkelen gir en oversikt over forbruksmetoden for avskrivning.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-104">This article gives an overview of the Consumption method of depreciation.</span></span>

<span data-ttu-id="ecdb9-105">Hvis du definerer en avskrivingsprofil for anleggsmidler og velger **Forbruk** i feltet **Metode** på siden **Avskrivningsprofiler**, tilordnes anleggsmidler til avskrivningsprofilen basert på bruken.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-105">If you set up a depreciation profile for fixed assets and select **Consumption** in the **Method** field on the **Depreciation profiles** page, fixed assets are assigned to the depreciation profile based on their usage.</span></span> <span data-ttu-id="ecdb9-106">Du trenger ikke definere prosenter og intervaller på siden **Avskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-106">You don't have to set up percentages and intervals on the **Depreciation profiles** page.</span></span> <span data-ttu-id="ecdb9-107">Når du har opprettet en avskrivingsprofil som bruker forbruksmetoden, kan du definere metoden på ulike måter.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-107">After you create a depreciation profile that uses the Consumption method, you can set up the method in various ways.</span></span>

## <a name="set-up-and-use-consumption-depreciation"></a><span data-ttu-id="ecdb9-108">Definere og bruke forbruksavskrivning</span><span class="sxs-lookup"><span data-stu-id="ecdb9-108">Set up and use consumption depreciation</span></span>
1.  <span data-ttu-id="ecdb9-109">På siden **Avskrivningsprofiler** oppretter du avskrivingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-109">On the **Depreciation profiles** page, create the depreciation profile.</span></span> <span data-ttu-id="ecdb9-110">For forbruksberegninger må avskrivningsprofilen inneholde en ID og et navn, og **Forbruk** må velges i feltet **Metode**.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-110">For consumption calculations, the depreciation profile must have an ID and a name, and **Consumption** must be selected in the **Method** field.</span></span>
2.  <span data-ttu-id="ecdb9-111">På siden **Avskrivningsfaktorer** definerer du avskrivningsfaktorer.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-111">On the **Consumption factors** page, set up consumption factors.</span></span> <span data-ttu-id="ecdb9-112">Hver avskrivningsfaktor må ha en ID og et navn og en avskrivningsfaktor som er angitt som et antall eller en prosent.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-112">Each consumption factor must have an ID and a name, and a consumption factor that is specified as either a quantity or a percentage.</span></span>
3.  <span data-ttu-id="ecdb9-113">På siden **Forbruksenheter** definerer du forbruksenheter.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-113">On the **Consumption units** page, set up consumption units.</span></span> <span data-ttu-id="ecdb9-114">Hver forbruksenhet må ha en ID og et navn.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-114">Each consumption unit must have an ID and a name.</span></span> <span data-ttu-id="ecdb9-115">Avskrivningsenheter brukes til å beregne forbruksavskrivning på siden **Forbruksavskrivning**.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-115">Depreciation units are used to calculate consumption depreciation on the **Consumption depreciation** page.</span></span> <span data-ttu-id="ecdb9-116">Eksempler på enheter er kilometer (km), kilogram (kg) og time.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-116">Examples of units are kilometer (km), kilogram (kg), and hour.</span></span>
4.  <span data-ttu-id="ecdb9-117">På siden **Anleggsmidler** definerer du enkle anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-117">On the **Fixed assets** page, set up individual fixed assets.</span></span> <span data-ttu-id="ecdb9-118">For hvert anleggsmiddel velger du verdimodeller og avskrivningstablåer som har avskrivningsprofiler.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-118">For each fixed asset, select value models and depreciation books that have depreciation profiles.</span></span> <span data-ttu-id="ecdb9-119">Du må definere verdimodeller eller avskrivningstablåer for forbruksavskrivning hvis noen av anleggsmidlene bruker avskrivningsprofiler som er basert på forbruksmetoden.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-119">You must set up value models or depreciation books for consumption depreciation if any of your fixed assets use depreciation profiles that are based on the Consumption method.</span></span> <span data-ttu-id="ecdb9-120">Dette oppsettet utføres enten i fanen **Avskrivning** på siden **Verdimodeller** eller på hurtigfanen **Generelt** på siden **Avskrivningsprofil**.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-120">This setup is done either on the **Depreciation** tab of the **Value models** page or on the **General** FastTab of the **Depreciation profile** page.</span></span> <span data-ttu-id="ecdb9-121">Du kan bruke den samme verdimodellen for flere anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-121">You can use the same value model for multiple fixed assets.</span></span> <span data-ttu-id="ecdb9-122">Avskrivningsprofiler er en del av verdimodellen eller avskrivningstablået du velger for hvert anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-122">Depreciation profiles are part of the value model or depreciation book that you select for each fixed asset.</span></span> <span data-ttu-id="ecdb9-123">Du kan ikke legge til eller endre avskrivningsprofilene direkte på siden **Anleggsmidler**.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-123">You can't add or modify depreciation profiles directly on the **Fixed assets** page.</span></span> <span data-ttu-id="ecdb9-124">Du kan endre avskrivningsprofilene bare på siden **Avskrivningstablåer**.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-124">You can modify depreciation profiles only on the **Depreciation books** page.</span></span>
5.  <span data-ttu-id="ecdb9-125">På siden **Verdimodeller** eller **Avskrivningstablå** i feltgruppen **Forbruksavskrivning** skriver du inn informasjon i følgende felt:</span><span class="sxs-lookup"><span data-stu-id="ecdb9-125">On the **Value models** page or the **Depreciation books** page, in the **Consumption depreciation** field group, enter information in the following fields:</span></span>
    -   <span data-ttu-id="ecdb9-126">Avskrivningsfaktor</span><span class="sxs-lookup"><span data-stu-id="ecdb9-126">Consumption factor</span></span>
    -   <span data-ttu-id="ecdb9-127">Enhet</span><span class="sxs-lookup"><span data-stu-id="ecdb9-127">Unit</span></span>
    -   <span data-ttu-id="ecdb9-128">Enhetsavskrivning</span><span class="sxs-lookup"><span data-stu-id="ecdb9-128">Unit depreciation</span></span>
    -   <span data-ttu-id="ecdb9-129">Estimert forbruk</span><span class="sxs-lookup"><span data-stu-id="ecdb9-129">Estimated consumption</span></span>

    <span data-ttu-id="ecdb9-130">I **Postert forbruk**-feltet vises forbruksavskrivningen, i enheter, som allerede er postert enten for kombinasjonen av anleggsmidlet og verdimodellen eller for avskrivningstablået.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-130">The **Posted consumption** field shows the consumption depreciation, in units, that has already been posted either for the combination of the fixed asset and value model, or for the depreciation book.</span></span> <span data-ttu-id="ecdb9-131">Du kan ikke oppdatere verdien i dette feltet manuelt.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-131">You can't manually update the value in this field.</span></span>

## <a name="examples"></a><span data-ttu-id="ecdb9-132">Eksempler</span><span class="sxs-lookup"><span data-stu-id="ecdb9-132">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="ecdb9-133">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="ecdb9-133">Example 1</span></span>

<span data-ttu-id="ecdb9-134">Følgende forbruksfaktor er definert for 31. januar:</span><span class="sxs-lookup"><span data-stu-id="ecdb9-134">The following consumption factor is set up for January 31:</span></span>

-   <span data-ttu-id="ecdb9-135">Antallet er 1 000.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-135">The quantity is 1,000.</span></span>
-   <span data-ttu-id="ecdb9-136">Enhetsavskrivningsprisen som er angitt for anleggsmidlet, er 1,5.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-136">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>

<span data-ttu-id="ecdb9-137">Avskrivningsforslaget 31. januar er som følger: antall × enhetsavskrivning 1 000 x 1,5 = 1 500 Hvis faktoren som er angitt for anleggsmidlet, er en prosentfaktor, multipliseres antallet som er beregnet i feltet **Estimert forbruk** for verdimodellen for anleggsmidlet, med prosenten som er definert for den valgte sluttdatoen.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-137">The depreciation proposal on January 31 is as follows: Quantity × Unit depreciation 1,000 × 1.5 = 1,500 If the factor that is specified for the fixed asset is a percentage factor, the quantity that is estimated in the **Estimated consumption** field for the value model of the fixed asset is multiplied by the percentage that is set up for the selected end date.</span></span> <span data-ttu-id="ecdb9-138">Det resulterende antallet foreslås deretter som avskrivningsantall for perioden.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-138">The resulting quantity is then suggested as the depreciation quantity for the period.</span></span>

### <a name="example-2"></a><span data-ttu-id="ecdb9-139">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="ecdb9-139">Example 2</span></span>

<span data-ttu-id="ecdb9-140">Følgende faktor for forbruksavskrivning er definert for 31. januar:</span><span class="sxs-lookup"><span data-stu-id="ecdb9-140">The following factor for consumption depreciation is set up for January 31:</span></span>

-   <span data-ttu-id="ecdb9-141">Prosenten er 10 prosent.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-141">The percentage is 10 percent.</span></span>
-   <span data-ttu-id="ecdb9-142">Enhetsavskrivningsprisen som er angitt for anleggsmidlet, er 1,5.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-142">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>
-   <span data-ttu-id="ecdb9-143">Estimert antall for et anleggsmiddel er 2 000.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-143">The estimated quantity of the fixed asset is 2,000.</span></span>

<span data-ttu-id="ecdb9-144">Avskrivningsforslaget den 31. januar er som følger: estimert antall × prosent × enhetsavskrivning 2 000 x 0,10 x 1,5 = 300</span><span class="sxs-lookup"><span data-stu-id="ecdb9-144">The depreciation proposal on January 31 is as follows: Estimated quantity × Percentage × Unit depreciation 2,000 × .10 × 1.5 = 300</span></span>



