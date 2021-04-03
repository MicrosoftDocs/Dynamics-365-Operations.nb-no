---
title: Produksjonsplanlegging
description: Dette emnet beskriver planlegging for produksjon, og forklarer hvordan du endrer planlagte produksjonsordrer ved å bruke planleggingsoptimalisering.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f9b5e4122fbd83ff76e0605b2f0816e10d2d9aab
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470839"
---
# <a name="production-planning"></a><span data-ttu-id="56b96-103">Produksjonsplanlegging</span><span class="sxs-lookup"><span data-stu-id="56b96-103">Production planning</span></span>

<span data-ttu-id="56b96-104">Planleggingsoptimalisering støtter flere produksjonsscenarioer.</span><span class="sxs-lookup"><span data-stu-id="56b96-104">Planning Optimizations supports several production scenarios.</span></span> <span data-ttu-id="56b96-105">Hvis du går over fra den eksisterende, innebygde hovedplanleggingsmotoren, er det viktig at du er oppmerksom på noen endrede virkemåter.</span><span class="sxs-lookup"><span data-stu-id="56b96-105">If you're migrating from the existing, built-in master planning engine, it's important that you be aware of some changed behavior.</span></span>

<span data-ttu-id="56b96-106">Følgende video gir en kort innføring i noen av begrepene som omhandles i dette emnet: [Dynamics 365 Supply Chain Management: Planlegge optimaliseringsforbedringer](https://youtu.be/u1pcmZuZBTw).</span><span class="sxs-lookup"><span data-stu-id="56b96-106">The following video gives a short introduction to some of the concepts discussed in this topic: [Dynamics 365 Supply Chain Management: Planning Optimization enhancements](https://youtu.be/u1pcmZuZBTw).</span></span>

## <a name="planned-production-orders"></a><span data-ttu-id="56b96-107">Planlagte produksjonsordrer</span><span class="sxs-lookup"><span data-stu-id="56b96-107">Planned production orders</span></span>

<span data-ttu-id="56b96-108">Når hovedplanleggingen oppretter planlagte bestillinger for å oppfylle behov, fastsettes ordretypen av verdien i feltet **Type planlagt bestilling**.</span><span class="sxs-lookup"><span data-stu-id="56b96-108">When master planning creates planned orders to fulfill requirements, the order type is determined by the value of the **Planned order type** field.</span></span> <span data-ttu-id="56b96-109">Hvis feltet **Type planlagt bestilling** er satt til *Produksjon*, opprettes planlagte produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="56b96-109">If the **Planned order type** field is set to *Production*, planned production orders are created.</span></span> <span data-ttu-id="56b96-110">Disse planlagte produksjonsordrene inneholder informasjon om den aktive stykklisten og rute-ID-en fra det relaterte produksjonsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="56b96-110">These planned production orders include information about the active bill of materials (BOM) and the route ID from the related production setup.</span></span>

## <a name="requirements-from-boms"></a><span data-ttu-id="56b96-111">Behov fra stykklister</span><span class="sxs-lookup"><span data-stu-id="56b96-111">Requirements from BOMs</span></span>

<span data-ttu-id="56b96-112">Det tas hensyn til stykklisteinformasjon under hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="56b96-112">BOM information is honored during master planning.</span></span> <span data-ttu-id="56b96-113">Planresultatet omfatter materialforsyning for å dekke relatert materialbehov for produksjon.</span><span class="sxs-lookup"><span data-stu-id="56b96-113">The plan output includes material supply to cover related material demand for production.</span></span>

<span data-ttu-id="56b96-114">Under hovedplanlegging brukes den gjeldende, aktive stykklisten til å fastsette hvilke materialer som trengs for produksjon.</span><span class="sxs-lookup"><span data-stu-id="56b96-114">During master planning, the current, active BOM is used to determine the materials that are required for production.</span></span> <span data-ttu-id="56b96-115">Dette trinnet utføres gjennom alle nivåer i stykklistestrukturen som er knyttet til produksjonsordren som kreves.</span><span class="sxs-lookup"><span data-stu-id="56b96-115">This step is done through all levels of the BOM structure that is related to the required production order.</span></span> <span data-ttu-id="56b96-116">Materialbehov oppfylles ved å bruke tilgjengelig lagerbeholdning, eksisterende bestilt forsyning og godkjente planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="56b96-116">Material requirement is fulfilled by using available on-hand inventory, existing on-order supply, and approved planned orders.</span></span> <span data-ttu-id="56b96-117">Hvis det kreves mer materiale et sted, opprettes det en planlagt bestilling for å dekke behovet.</span><span class="sxs-lookup"><span data-stu-id="56b96-117">If additional material is required anywhere, a planned order is created to cover the demand.</span></span>

## <a name="scheduling-during-firming"></a><span data-ttu-id="56b96-118">Planlegging under autorisering</span><span class="sxs-lookup"><span data-stu-id="56b96-118">Scheduling during firming</span></span>

<span data-ttu-id="56b96-119">Planlagte produksjonsordrer omfatter rute-ID-en som kreves for produksjonsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="56b96-119">Planned production orders include the route ID that is required for production scheduling.</span></span> <span data-ttu-id="56b96-120">Planleggingsstøtte under planleggingskjøringen for planlagte bestillinger er imidlertid ventende.</span><span class="sxs-lookup"><span data-stu-id="56b96-120">However, scheduling support during the planning run for planned orders is pending.</span></span> <span data-ttu-id="56b96-121">Rute-ID-en brukes til å planlegge planlagte produksjonsordrer under autorisering.</span><span class="sxs-lookup"><span data-stu-id="56b96-121">The route ID is used to schedule planned production orders during firming.</span></span> <span data-ttu-id="56b96-122">Derfor kan leveringstiden for planlagte produksjonsordrer avvike fra leveringstiden for tilknyttede planlagte, autoriserte produksjonsordrer som genereres fra dem, som beskrevet her:</span><span class="sxs-lookup"><span data-stu-id="56b96-122">Therefore, the lead time on planned production orders can differ from the lead time on related scheduled, firmed production orders that are generated from them, as described here:</span></span>

- <span data-ttu-id="56b96-123">**Planlagt produksjonsordre** – Leveringstiden er basert på den statiske leveringstiden fra det frigitte produktet.</span><span class="sxs-lookup"><span data-stu-id="56b96-123">**Planned production order** – The lead time is based on the static lead time from the released product.</span></span>
- <span data-ttu-id="56b96-124">**Autorisert produksjonsordre** – Leveringstiden er basert på planlegging som bruker ruteinformasjon og relaterte ressursbegrensninger.</span><span class="sxs-lookup"><span data-stu-id="56b96-124">**Firmed production order** – The lead time is based on scheduling that uses route information and related resource constraints.</span></span>

<span data-ttu-id="56b96-125">Hvis du vil ha mer informasjon om forventet funksjonstilgjengelighet, kan du se [Analyse for tilpassing av planleggingsoptimalisering](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="56b96-125">For more information about expected feature availability, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="56b96-126">Hvis du er avhengig av produksjonsfunksjonalitet som ennå ikke er tilgjengelig for planleggingsoptimalisering, kan du fortsette å bruke den innebygde hovedplanleggingsmotoren.</span><span class="sxs-lookup"><span data-stu-id="56b96-126">If you depend on production functionality that isn't yet available for Planning Optimization, you can continue to use the built-in master planning engine.</span></span> <span data-ttu-id="56b96-127">Ingen unntak er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="56b96-127">No exception is required.</span></span>

## <a name="delays"></a><span data-ttu-id="56b96-128">Forsinkelser</span><span class="sxs-lookup"><span data-stu-id="56b96-128">Delays</span></span>

<span data-ttu-id="56b96-129">Hvis leveringstiden for nødvendig materiale er lengre enn perioden mellom dagens dato og materialbehovsdatoen, blir den planlagte bestillingen for det nødvendige materialet og den tilknyttede produksjonsordren forsinket.</span><span class="sxs-lookup"><span data-stu-id="56b96-129">If the lead time for required material is longer than the period between today's date and the material requirement date, the planned order for the required material and the related production order will be delayed.</span></span> <span data-ttu-id="56b96-130">Når det gjelder planlagte bestillinger, beregnes forsinkelsen (i dager) basert på leveringstiden fra det frigitte produktet.</span><span class="sxs-lookup"><span data-stu-id="56b96-130">For planned orders, the delay (in days) is calculated based on the lead time from the released product.</span></span> <span data-ttu-id="56b96-131">Forsinkelsesinformasjonen spres deretter til alle nivåer i stykklistestrukturen.</span><span class="sxs-lookup"><span data-stu-id="56b96-131">The delay information is then propagated through all levels of the BOM structure.</span></span> <span data-ttu-id="56b96-132">Derfor kan du følge virkningen av forsinket råvare hele veien til kundesalgsordren.</span><span class="sxs-lookup"><span data-stu-id="56b96-132">Therefore, you can follow the impact of delayed raw material all the way to the customer sales order.</span></span>

## <a name="modifying-planned-orders"></a><span data-ttu-id="56b96-133">Endre planlagte bestillinger</span><span class="sxs-lookup"><span data-stu-id="56b96-133">Modifying planned orders</span></span>

<span data-ttu-id="56b96-134">Når du endrer informasjon i en planlagt bestilling, får du en melding om at virkningen av manuelle endringer i planlagte bestillinger ikke gjenspeiles i resten av planen før neste hovedplanlegging kjøres.</span><span class="sxs-lookup"><span data-stu-id="56b96-134">When you change information on a planned order, you receive the following message: "Note that the impact of manual changes on planned orders won't be reflected in the rest of the plan until the next master planning run."</span></span>

<span data-ttu-id="56b96-135">Hvis du vil endre informasjon i en planlagt bestilling og se hvordan de relaterte materialbehovene påvirkes, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="56b96-135">If you want to change information on a planned order and see the impact on the related material requirements, follow these steps.</span></span>

1. <span data-ttu-id="56b96-136">Oppdater den planlagte bestillingen.</span><span class="sxs-lookup"><span data-stu-id="56b96-136">Update the planned order.</span></span>
2. <span data-ttu-id="56b96-137">Godkjenn den planlagte bestillingen.</span><span class="sxs-lookup"><span data-stu-id="56b96-137">Approve the planned order.</span></span>
3. <span data-ttu-id="56b96-138">Kjør hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="56b96-138">Run master planning.</span></span>

<span data-ttu-id="56b96-139">Når du kjører hovedplanlegging, skal du ikke bruke filtre hvis planlagte produksjonsordrer er inkludert.</span><span class="sxs-lookup"><span data-stu-id="56b96-139">When you run master planning, you should not use filters if planned production orders are included.</span></span> <span data-ttu-id="56b96-140">Hvis du vil ha mer informasjon, kan du se delen [Filtre](#filters) senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="56b96-140">For more information, see the [Filters](#filters) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="56b96-141">Hvis leveringsdatoen for den planlagte bestillingen endres til en senere dato, kan behovet bli utlignet mot en ny planlagt bestilling.</span><span class="sxs-lookup"><span data-stu-id="56b96-141">If the delivery date of the planned order is changed to a later date, the demand might be pegged against a new planned order.</span></span> <span data-ttu-id="56b96-142">Dette skjer når den nye forsyningsdatoen forårsaker en forsinkelse for det utlignede behovet, men forsinkelsen kan unngås i henhold til innstillingene for leveringstid.</span><span class="sxs-lookup"><span data-stu-id="56b96-142">This behavior occurs when the new supply date causes a delay for the pegged demand but, according to the lead time settings, the delay can be avoided.</span></span>

## <a name="explosion-page"></a><span data-ttu-id="56b96-143">Nedbryting-siden</span><span class="sxs-lookup"><span data-stu-id="56b96-143">Explosion page</span></span>

<span data-ttu-id="56b96-144">Du kan bruke **Nedbryting**-siden til å analysere behovet som er nødvendig for en bestemt produksjonsordre eller planlagt produksjonsordre, tilknyttet dekning og utligningsinformasjon.</span><span class="sxs-lookup"><span data-stu-id="56b96-144">You can use the **Explosion** page to analyze the demand that is required for a specific production order or planned production order, the related coverage, and pegging information.</span></span> <span data-ttu-id="56b96-145">Informasjon på **Nedbryting**-siden oppdateres under hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="56b96-145">Information on the **Explosion** page is updated during master planning.</span></span> <span data-ttu-id="56b96-146">Du kan ikke oppdatere informasjonen direkte fra **Nedbryting**-siden.</span><span class="sxs-lookup"><span data-stu-id="56b96-146">You can't update the information directly from the **Explosion** page.</span></span>

## <a name="filters"></a><a name="filters"></a><span data-ttu-id="56b96-147">Filtre</span><span class="sxs-lookup"><span data-stu-id="56b96-147">Filters</span></span>

<span data-ttu-id="56b96-148">Når det gjelder planleggingsscenarioer som omfatter produksjon, anbefaler vi at du unngår filtrerte kjøringer av hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="56b96-148">For planning scenarios that include production, we recommend that you avoid filtered master planning runs.</span></span> <span data-ttu-id="56b96-149">For å sikre at planleggingsoptimalisering har informasjonen som trengs for å beregne riktig resultat, må du ta med alle produkter som har en hvilken som helst tilknytning til produkter i hele stykklistestrukturen for den planlagte bestillingen.</span><span class="sxs-lookup"><span data-stu-id="56b96-149">To ensure that Planning Optimization has the information that is required to calculate the correct result, you must include all products that have any relation to products in the whole BOM structure of the planned order.</span></span>

<span data-ttu-id="56b96-150">Selv om avhengige underordnede varer automatisk blir oppdaget og tatt med i kjøringer av hovedplanlegging når den innebygde hovedplanleggingsmotoren brukes, utfører ikke planleggingsoptimalisering denne handlingen.</span><span class="sxs-lookup"><span data-stu-id="56b96-150">Although dependent child items are automatically detected and included in master planning runs when the built-in master planning engine is used, Planning Optimization doesn't perform this action.</span></span>

<span data-ttu-id="56b96-151">Hvis for eksempel én bolt fra stykklistestrukturen for produkt A også brukes til å produsere produkt B, må alle produkter i stykklistestrukturen for produktene A og B tas med i filteret.</span><span class="sxs-lookup"><span data-stu-id="56b96-151">For example, if a single bolt from the BOM structure of product A is also used to produce product B, all products in the BOM structure of products A and B must be included in the filter.</span></span> <span data-ttu-id="56b96-152">Siden det kan bli svært komplekst å sikre at alle produkter er en del av filteret, anbefaler vi at du unngår filtrerte kjøringer av hovedplanlegging når produksjonsordrer er involvert.</span><span class="sxs-lookup"><span data-stu-id="56b96-152">Because it can be very complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]