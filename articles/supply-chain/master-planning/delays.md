---
title: Forsinkelser
description: Dette emnet inneholder informasjon om forsinkede datoer i hovedplanlegging. En forsinket dato er en realistisk forfallsdato som en transaksjon mottar hvis den tidligste datoen for fullføring som hovedplanleggingen beregner er senere enn ønsket dato.
author: roxanadiaconu
manager: AnnBe
ms.date: 03/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c26fedf15118a304469604527c33a25871356be
ms.sourcegitcommit: 8eac5eee94bb32143df44c82a2dfdbe903967af8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/20/2019
ms.locfileid: "878316"
---
# <a name="delays"></a><span data-ttu-id="a5470-104">Forsinkelser</span><span class="sxs-lookup"><span data-stu-id="a5470-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5470-105">Dette emnet inneholder informasjon om forsinkede datoer i hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="a5470-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="a5470-106">En forsinket dato er en realistisk forfallsdato som en transaksjon mottar hvis den tidligste datoen for fullføring som hovedplanleggingen beregner er senere enn ønsket dato.</span><span class="sxs-lookup"><span data-stu-id="a5470-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="a5470-107">Hovedplanlegging kan beregne den tidligste fullføringsdatoen for en transaksjon, basert på leveringstider, materialtilgjengelighet, tilgjengelig kapasitet og forskjellige planleggingsparametere.</span><span class="sxs-lookup"><span data-stu-id="a5470-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="a5470-108">Hvis hovedplanleggingen beregner en ordredato som kommer før gjeldende dato, kan ikke ordren fullføres i tide.</span><span class="sxs-lookup"><span data-stu-id="a5470-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="a5470-109">Derfor er ordren forsinket.</span><span class="sxs-lookup"><span data-stu-id="a5470-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="a5470-110">I så fall fremoverplanlegger hovedplanleggingen ordren fra gjeldende dato og inkluderer leveringstider.</span><span class="sxs-lookup"><span data-stu-id="a5470-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="a5470-111">Disse leveringstidene starter med komponentvarer på lavere nivå.</span><span class="sxs-lookup"><span data-stu-id="a5470-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="a5470-112">Ordren får deretter en forsinkelsesdato.</span><span class="sxs-lookup"><span data-stu-id="a5470-112">The order then receives a delayed date.</span></span> <span data-ttu-id="a5470-113">En forsinket dato er en realistisk forfallsdato basert på gjeldende data.</span><span class="sxs-lookup"><span data-stu-id="a5470-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="a5470-114">Hovedplanlegging beregner også antall dager forsinket.</span><span class="sxs-lookup"><span data-stu-id="a5470-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="a5470-115">I noen tilfeller kan det hende du velger ikke å beregne forsinkelser, for eksempel når brukerne vet at de kan fremskynde leveringstider ved å velge alternative leveringsmåter.</span><span class="sxs-lookup"><span data-stu-id="a5470-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="a5470-116">Du kan konfigurere hvordan forsinkelser beregnes for en dekningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a5470-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="a5470-117">Du kan deretter knytte dekningsgruppen til en vare senere.</span><span class="sxs-lookup"><span data-stu-id="a5470-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="a5470-118">På siden **Hovedplanleggingsparametere** kan du angi starttidspunktet for beregning av forsinkelser.</span><span class="sxs-lookup"><span data-stu-id="a5470-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="a5470-119">Hvis en ordre er utført etter dette tidspunktet, legges det til én dag i forsinkelsen av ordren.</span><span class="sxs-lookup"><span data-stu-id="a5470-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> <span data-ttu-id="a5470-120">[!Obs!} I tidligere versjoner ble beregnede forsinkelser kalt *terminmeldinger*, forsinkelsesdatoen ble kalt *termindatoen* og en forsinket transaksjon ble kalt *en transaksjon som var satt til fremtiden*.</span><span class="sxs-lookup"><span data-stu-id="a5470-120">[!NOTE} In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="desired-date"></a><span data-ttu-id="a5470-121">Ønsket dato</span><span class="sxs-lookup"><span data-stu-id="a5470-121">Desired date</span></span>

<span data-ttu-id="a5470-122">På siden **Planlagt ordre**, i kategorien **Forsinkelser** finnes **Ønsket dato** for den planlagte bestillingen.</span><span class="sxs-lookup"><span data-stu-id="a5470-122">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="a5470-123">Den ønskede datoen for en planlagt bestilling er den grunnleggende datoen for forsinkelser, som er en beregnet dato som tilsvarer **Ønsket dato** som beregnes fra **Nettobehov**.</span><span class="sxs-lookup"><span data-stu-id="a5470-123">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="a5470-124">Hvis den planlagte ordren er en stykklistelinje, produksjonslinje eller kanban-linje, er den ønskede datoen basert på **Behovsdato**, og den ønskede datoen vil ikke bli vist på siden **Planlagt ordre**.</span><span class="sxs-lookup"><span data-stu-id="a5470-124">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="a5470-125">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a5470-125">Additional resources</span></span>
--------

[<span data-ttu-id="a5470-126">Dekningsinnstillinger</span><span class="sxs-lookup"><span data-stu-id="a5470-126">Coverage settings</span></span>](coverage-settings.md)
