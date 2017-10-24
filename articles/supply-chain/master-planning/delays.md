---
title: Forsinkelser
description: "Denne artikkelen inneholder informasjon om forsinkede datoer i hovedplanlegging. En forsinket dato er en realistisk forfallsdato som en transaksjon mottar hvis den tidligste datoen for fullføring som hovedplanleggingen beregner er senere enn ønsket dato."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8db5c507fbc68e637dbbc4ef3311d1fbd298f24f
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="delays"></a><span data-ttu-id="3d87c-104">Forsinkelser</span><span class="sxs-lookup"><span data-stu-id="3d87c-104">Delays</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3d87c-105">Denne artikkelen inneholder informasjon om forsinkede datoer i hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="3d87c-105">This article provides information about delayed dates in master planning.</span></span> <span data-ttu-id="3d87c-106">En forsinket dato er en realistisk forfallsdato som en transaksjon mottar hvis den tidligste datoen for fullføring som hovedplanleggingen beregner er senere enn ønsket dato.</span><span class="sxs-lookup"><span data-stu-id="3d87c-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="3d87c-107">Hovedplanlegging kan beregne den tidligste fullføringsdatoen for en transaksjon, basert på leveringstider, materialtilgjengelighet, tilgjengelig kapasitet og forskjellige planleggingsparametere.</span><span class="sxs-lookup"><span data-stu-id="3d87c-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="3d87c-108">Hvis hovedplanleggingen beregner en ordredato som kommer før gjeldende dato, kan ikke ordren fullføres i tide.</span><span class="sxs-lookup"><span data-stu-id="3d87c-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="3d87c-109">Derfor er ordren forsinket.</span><span class="sxs-lookup"><span data-stu-id="3d87c-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="3d87c-110">I så fall fremoverplanlegger hovedplanleggingen ordren fra gjeldende dato og inkluderer leveringstider.</span><span class="sxs-lookup"><span data-stu-id="3d87c-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="3d87c-111">Disse leveringstidene starter med komponentvarer på lavere nivå.</span><span class="sxs-lookup"><span data-stu-id="3d87c-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="3d87c-112">Ordren får deretter en forsinkelsesdato.</span><span class="sxs-lookup"><span data-stu-id="3d87c-112">The order then receives a delayed date.</span></span> <span data-ttu-id="3d87c-113">En forsinket dato er en realistisk forfallsdato basert på gjeldende data.</span><span class="sxs-lookup"><span data-stu-id="3d87c-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="3d87c-114">Hovedplanlegging beregner også antall dager forsinket.</span><span class="sxs-lookup"><span data-stu-id="3d87c-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="3d87c-115">I noen tilfeller kan det hende du velger ikke å beregne forsinkelser, for eksempel når brukerne vet at de kan fremskynde leveringstider ved å velge alternative leveringsmåter.</span><span class="sxs-lookup"><span data-stu-id="3d87c-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="3d87c-116">Du kan konfigurere hvordan forsinkelser beregnes for en dekningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3d87c-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="3d87c-117">Du kan deretter knytte dekningsgruppen til en vare senere.</span><span class="sxs-lookup"><span data-stu-id="3d87c-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="3d87c-118">På siden **Hovedplanleggingsparametere** kan du angi starttidspunktet for beregning av forsinkelser.</span><span class="sxs-lookup"><span data-stu-id="3d87c-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="3d87c-119">Hvis en ordre er utført etter dette tidspunktet, legges det til én dag i forsinkelsen av ordren.</span><span class="sxs-lookup"><span data-stu-id="3d87c-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

<span data-ttu-id="3d87c-120">**Obs!**  I tidligere versjoner ble beregnede forsinkelser kalt *terminmeldinger*, forsinkelsesdatoen ble kalt *termindatoen*, og en forsinket transaksjon ble kalt *en transaksjon som var satt til fremtiden*.</span><span class="sxs-lookup"><span data-stu-id="3d87c-120">**Note:** In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

<a name="see-also"></a><span data-ttu-id="3d87c-121">Se også</span><span class="sxs-lookup"><span data-stu-id="3d87c-121">See also</span></span>
--------

[<span data-ttu-id="3d87c-122">Dekningsinnstillinger</span><span class="sxs-lookup"><span data-stu-id="3d87c-122">Coverage settings</span></span>](coverage-settings.md)




