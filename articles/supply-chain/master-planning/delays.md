---
title: Forsinkelser
description: Dette emnet inneholder informasjon om forsinkede datoer i hovedplanlegging. En forsinket dato er en realistisk forfallsdato som en transaksjon mottar hvis den tidligste datoen for fullføring som hovedplanleggingen beregner er senere enn ønsket dato.
author: roxanadiaconu
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da09d670fd952d885f013693b6362cf9002343ff
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982702"
---
# <a name="delays"></a><span data-ttu-id="48159-104">Forsinkelser</span><span class="sxs-lookup"><span data-stu-id="48159-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48159-105">Dette emnet inneholder informasjon om forsinkede datoer i hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="48159-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="48159-106">En forsinket dato er en realistisk forfallsdato som en transaksjon mottar hvis den tidligste datoen for fullføring som hovedplanleggingen beregner er senere enn ønsket dato.</span><span class="sxs-lookup"><span data-stu-id="48159-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="48159-107">Hovedplanlegging kan beregne den tidligste fullføringsdatoen for en transaksjon, basert på leveringstider, materialtilgjengelighet, tilgjengelig kapasitet og forskjellige planleggingsparametere.</span><span class="sxs-lookup"><span data-stu-id="48159-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="48159-108">Hvis hovedplanleggingen beregner en ordredato som kommer før gjeldende dato, kan ikke ordren fullføres i tide.</span><span class="sxs-lookup"><span data-stu-id="48159-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="48159-109">Derfor er ordren forsinket.</span><span class="sxs-lookup"><span data-stu-id="48159-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="48159-110">I så fall fremoverplanlegger hovedplanleggingen ordren fra gjeldende dato og inkluderer leveringstider.</span><span class="sxs-lookup"><span data-stu-id="48159-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="48159-111">Disse leveringstidene starter med komponentvarer på lavere nivå.</span><span class="sxs-lookup"><span data-stu-id="48159-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="48159-112">Ordren får deretter en forsinkelsesdato.</span><span class="sxs-lookup"><span data-stu-id="48159-112">The order then receives a delayed date.</span></span> <span data-ttu-id="48159-113">En forsinket dato er en realistisk forfallsdato basert på gjeldende data.</span><span class="sxs-lookup"><span data-stu-id="48159-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="48159-114">Hovedplanlegging beregner også antall dager forsinket.</span><span class="sxs-lookup"><span data-stu-id="48159-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="48159-115">I noen tilfeller kan det hende du velger ikke å beregne forsinkelser, for eksempel når brukerne vet at de kan fremskynde leveringstider ved å velge alternative leveringsmåter.</span><span class="sxs-lookup"><span data-stu-id="48159-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="48159-116">Du kan konfigurere hvordan forsinkelser beregnes for en dekningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="48159-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="48159-117">Du kan deretter knytte dekningsgruppen til en vare senere.</span><span class="sxs-lookup"><span data-stu-id="48159-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="48159-118">På siden **Hovedplanleggingsparametere** kan du angi starttidspunktet for beregning av forsinkelser.</span><span class="sxs-lookup"><span data-stu-id="48159-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="48159-119">Hvis en ordre er utført etter dette tidspunktet, legges det til én dag i forsinkelsen av ordren.</span><span class="sxs-lookup"><span data-stu-id="48159-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> [!NOTE]
> <span data-ttu-id="48159-120">I tidligere versjoner ble beregnede forsinkelser kalt *terminmeldinger* , forsinkelsesdatoen ble kalt *termindatoen* og en forsinket transaksjon ble kalt *en transaksjon som var satt til fremtiden* .</span><span class="sxs-lookup"><span data-stu-id="48159-120">In earlier versions, calculated delays were known as *futures messages* , the delayed date was known as the *futures date* , and a delayed transaction was referred to as *a transaction that was future set* .</span></span>

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a><span data-ttu-id="48159-121">Begrensede forsinkelser i produksjonsoppsettet med flere stykklistenivåer</span><span class="sxs-lookup"><span data-stu-id="48159-121">Limited delays in production setup with multiple BOM levels</span></span>
<span data-ttu-id="48159-122">Når du arbeider med forsinkelser i et produksjonsoppsett som har flere stykklistenivåer, er det viktig å være oppmerksom på at bare varene som er direkte over varen (i stykklistestrukturen) som forårsaker forsinkelsen, blir oppdatert med en forsinkelse som del av hovedplanleggingen som kjøres.</span><span class="sxs-lookup"><span data-stu-id="48159-122">When you work with delays in a production setup that has multiple BOM levels, it is important to note that only the items directly above the item (in the BOM structure) causing the delay, will be updated with a delay as part of the master planning run.</span></span> <span data-ttu-id="48159-123">Andre varer i stykklistestrukturen vil ikke få forsinkelsen gjeldende før den første hovedplanleggingen kjøres, når den planlagte bestillingen for det øverste nivået er godkjent eller autorisert.</span><span class="sxs-lookup"><span data-stu-id="48159-123">Other items in the BOM structure will not get the delay applied until the first master planning run, when the planned order for the top level is approved or firmed.</span></span> 

<span data-ttu-id="48159-124">For å omgå denne kjente begrensningen kan produksjonsordrene øverst i stykklistestrukturen med forsinkelser godkjennes (eller autoriseres) før den neste hovedplanleggingen kjøres.</span><span class="sxs-lookup"><span data-stu-id="48159-124">To work around this known limitation, the production orders on the top of the BOM structure with delays can be approved (or firmed) prior to the next master planning run.</span></span> <span data-ttu-id="48159-125">Dermed beholdes forsinkelsen fra den forsinkede, godkjente planlagte produksjonsordren, og alle underliggende komponenter blir oppdatert i henhold til dette.</span><span class="sxs-lookup"><span data-stu-id="48159-125">This way the delay from the delayed approved planned production order will be kept and all underlying components will be updated accordingly.</span></span>
<span data-ttu-id="48159-126">Handlingsmeldinger kan også brukes til å identifisere planlagte bestillinger som kan flyttes til en senere dato på grunn av andre forsinkelser i stykklistestrukturen.</span><span class="sxs-lookup"><span data-stu-id="48159-126">Action messages can also be used to identify planned orders that can be moved to a later date, due to other delays in the BOM structure.</span></span>

## <a name="desired-date"></a><span data-ttu-id="48159-127">Ønsket dato</span><span class="sxs-lookup"><span data-stu-id="48159-127">Desired date</span></span>

<span data-ttu-id="48159-128">På siden **Planlagt ordre** , i kategorien **Forsinkelser** finnes **Ønsket dato** for den planlagte bestillingen.</span><span class="sxs-lookup"><span data-stu-id="48159-128">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="48159-129">Den ønskede datoen for en planlagt bestilling er den grunnleggende datoen for forsinkelser, som er en beregnet dato som tilsvarer **Ønsket dato** som beregnes fra **Nettobehov** .</span><span class="sxs-lookup"><span data-stu-id="48159-129">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement** .</span></span> <span data-ttu-id="48159-130">Hvis den planlagte ordren er en stykklistelinje, produksjonslinje eller kanban-linje, er den ønskede datoen basert på **Behovsdato** , og den ønskede datoen vil ikke bli vist på siden **Planlagt ordre** .</span><span class="sxs-lookup"><span data-stu-id="48159-130">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="48159-131">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="48159-131">Additional resources</span></span>
--------

[<span data-ttu-id="48159-132">Dekningsinnstillinger</span><span class="sxs-lookup"><span data-stu-id="48159-132">Coverage settings</span></span>](coverage-settings.md)
