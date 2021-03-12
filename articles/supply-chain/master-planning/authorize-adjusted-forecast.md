---
title: Autoriser en justert prognose
description: Ikke alle prognosedata må autoriseres umiddelbart. Denne artikkelen forklarer hvordan du kan angi perioden som en prognose er autorisert for. Den forklarer også hvordan du godkjenner prognosen for bestemte firmaer og prognosemodeller.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ab8558f25f5ffd3b7eb3e1bc5680b1a1f8d5139
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961461"
---
# <a name="authorize-an-adjusted-forecast"></a><span data-ttu-id="5eff4-105">Autoriser en justert prognose</span><span class="sxs-lookup"><span data-stu-id="5eff4-105">Authorize an adjusted forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5eff4-106">Ikke alle prognosedata må autoriseres umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="5eff4-106">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="5eff4-107">Denne artikkelen forklarer hvordan du kan angi perioden som en prognose er autorisert for.</span><span class="sxs-lookup"><span data-stu-id="5eff4-107">This article explains how you can specify the period that a forecast is authorized for.</span></span> <span data-ttu-id="5eff4-108">Den forklarer også hvordan du godkjenner prognosen for bestemte firmaer og prognosemodeller.</span><span class="sxs-lookup"><span data-stu-id="5eff4-108">It also explains how you can authorize the forecast for specific companies and forecast models.</span></span>

<span data-ttu-id="5eff4-109">Ikke alle prognosedata må autoriseres umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="5eff4-109">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="5eff4-110">Du kan angi i start- og sluttdatoene for perioden som prognosen er autorisert for.</span><span class="sxs-lookup"><span data-stu-id="5eff4-110">You can specify the start and end dates of the period that the forecast is authorized for.</span></span> <span data-ttu-id="5eff4-111">Denne funksjonen lar deg låse bestemt perioder.</span><span class="sxs-lookup"><span data-stu-id="5eff4-111">This functionality lets you freeze specific buckets.</span></span> 

<span data-ttu-id="5eff4-112">Start- og sluttdatoene du angir, må samsvare med start- og sluttdatoene for perioden som prognosen er generert i.</span><span class="sxs-lookup"><span data-stu-id="5eff4-112">The start and end dates that you specify must correspond to the start and end dates of the bucket that the forecast is generated in.</span></span> <span data-ttu-id="5eff4-113">Systemet håndhever denne begrensningen, og justerer automatisk datoene hvis justering er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="5eff4-113">The system enforces this restriction and automatically adjusts the dates, if adjustment is required.</span></span> 

<span data-ttu-id="5eff4-114">I **Detaljer** -fanen på siden **Autorisasjon** kan du vise detaljer om prognosen som sist ble generert.</span><span class="sxs-lookup"><span data-stu-id="5eff4-114">On the **Details** tab of the **Authorization** page, you can view details about the forecast that was most recently generated.</span></span> 

<span data-ttu-id="5eff4-115">Du kan velge firmaene og prognosemodellene for å autorisere prognosen for bruk.</span><span class="sxs-lookup"><span data-stu-id="5eff4-115">You can select the companies and the forecast models to authorize the forecast for use.</span></span> <span data-ttu-id="5eff4-116">Rutenettet omfatter som standard alle firmaene som prognosebehov er opprettet for.</span><span class="sxs-lookup"><span data-stu-id="5eff4-116">By default, the grid includes all the companies that forecast demand has been created for.</span></span> <span data-ttu-id="5eff4-117">Prognosemodellen som samsvarer med den gjeldende prognoseplanen som er angitt i hovedplanleggingsparametere, er forhåndsutfylt for hvert firma.</span><span class="sxs-lookup"><span data-stu-id="5eff4-117">For each company, the forecast model that corresponds to the current forecast plan that is set up in the master planning parameters is prefilled.</span></span> <span data-ttu-id="5eff4-118">Du kan imidlertid endre denne prognosemodellen til en hvilken som helst prognosemodell som tilhører selskapet.</span><span class="sxs-lookup"><span data-stu-id="5eff4-118">However, you can change this forecast model to any forecast model that belongs to that company.</span></span> <span data-ttu-id="5eff4-119">Hvis ingen prognosebehovsdata er generert for et selskap som er valgt, får du en advarsel ved importen.</span><span class="sxs-lookup"><span data-stu-id="5eff4-119">If no forecast demand data has been generated for a selected company, you receive a warning message at import time.</span></span> 

<span data-ttu-id="5eff4-120">Det er svært viktig at du forstår hvordan avmerkingsboksen **Lagre de manuelle justeringene som er gjort i behovsprognosen for basislinjen** fungerer.</span><span class="sxs-lookup"><span data-stu-id="5eff4-120">It's very important that you understand how the **Save the manual adjustments made to the baseline demand forecast** check box works.</span></span> <span data-ttu-id="5eff4-121">Hvis du har foretatt manuelle justeringer i den statistiske basislinjeprognosen, er de justerte verdiene autorisert for bruk, selv om denne avmerkingsboksen er deaktivert.</span><span class="sxs-lookup"><span data-stu-id="5eff4-121">If you've made manual adjustments to the statistical baseline forecast, the adjusted values are authorized for use, even if this check box is cleared.</span></span> <span data-ttu-id="5eff4-122">Endringene forkastes imidlertid etter godkjenning.</span><span class="sxs-lookup"><span data-stu-id="5eff4-122">However, the changes are discarded after the authorization.</span></span> <span data-ttu-id="5eff4-123">Neste gang det opprettes en prognose, er denne prognosen derfor bare en statistisk prognose og har ikke noen manuell overstyring, selv om **Overfør manuelle justeringer til behovsprognosen** er valgt.</span><span class="sxs-lookup"><span data-stu-id="5eff4-123">Therefore, the next time that a forecast is generated, that forecast is only a statistical forecast and doesn't have any manual overrides, even if **Transfer manual adjustments to the demand forecast** is selected.</span></span> <span data-ttu-id="5eff4-124">Derfor kan du betrakte avmerkingsboksen **Lagre de manuelle justeringene som er gjort i behovsprognosen for basislinjen** som en mekanisme som lar deg beholde eller forkaste alle manuelle endringer.</span><span class="sxs-lookup"><span data-stu-id="5eff4-124">Therefore, you can consider the **Save the manual adjustments made to the baseline demand forecast** check box a mechanism that lets you keep or discard all manual changes.</span></span>

<a name="additional-resources"></a><span data-ttu-id="5eff4-125">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5eff4-125">Additional resources</span></span>
--------

[<span data-ttu-id="5eff4-126">Foreta manuelle justeringer i basislinjeprognosen</span><span class="sxs-lookup"><span data-stu-id="5eff4-126">Make manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="5eff4-127">Overvåke prognosenøyaktighet</span><span class="sxs-lookup"><span data-stu-id="5eff4-127">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)



