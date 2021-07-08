---
title: Forsinkelsestoleranse (negative dager)
description: Dette emnet gir informasjon om forsinkelsestoleranseberegningen og hvordan den påvirker oppretting av planlagte bestillinger i planleggingsoptimaliseringen.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 748e047e89747f2eabccc04a40c79bcb1e6f3dea
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306469"
---
# <a name="delay-tolerance-negative-days"></a><span data-ttu-id="f26bc-103">Forsinkelsestoleranse (negative dager)</span><span class="sxs-lookup"><span data-stu-id="f26bc-103">Delay tolerance (negative days)</span></span>

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="f26bc-104">Med funksjonaliteten for forsinkelsestoleranse kan planleggingsoptimalisering vurdere verdien for **Negative dager** som er angitt for dekningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="f26bc-104">The delay tolerance functionality enables Planning Optimization to consider the **Negative days** value that is set for coverage groups.</span></span> <span data-ttu-id="f26bc-105">Den brukes til å forlenge toleranseperioden for forsinkelsestoleranse som brukes under hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="f26bc-105">It's used to extend the delay tolerance period that is applied during master planning.</span></span> <span data-ttu-id="f26bc-106">På denne måten kan du unngå å opprette nye forsyningsordrer hvis eksisterende forsyning vil være i stand til å dekke behovet etter en kort forsinkelse.</span><span class="sxs-lookup"><span data-stu-id="f26bc-106">In this way, you can avoid creating new supply orders if existing supply will be able to cover the demand after a short delay.</span></span> <span data-ttu-id="f26bc-107">Formålet med funksjonen er å fastslå om det er fornuftig å opprette en ny forsyningsordre for et gitt behov.</span><span class="sxs-lookup"><span data-stu-id="f26bc-107">The purpose of the functionality is to determine whether it makes sense to create a new supply order for a given demand.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="f26bc-108">Aktivere funksjonen i systemet</span><span class="sxs-lookup"><span data-stu-id="f26bc-108">Turn on the feature in your system</span></span>

<span data-ttu-id="f26bc-109">Hvis du vil gjøre denne funksjonaliteten for forsinkelsestoleranse tilgjengelig i systemet, kan du gå til [Funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funksjonen *Negative dager for Planleggingsoptimalisering*.</span><span class="sxs-lookup"><span data-stu-id="f26bc-109">To make the delay tolerance functionality available in your system, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Negative days for Planning Optimization* feature.</span></span>

## <a name="delay-tolerance-in-planning-optimization"></a><span data-ttu-id="f26bc-110">Forsinkelsestoleranse i planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="f26bc-110">Delay tolerance in Planning Optimization</span></span>

<span data-ttu-id="f26bc-111">Forsinkelsestoleranse representerer antall dager utover leveringstiden som du er villig til å vente før du bestiller ny etterfylling når eksisterende forsyning allerede er planlagt.</span><span class="sxs-lookup"><span data-stu-id="f26bc-111">Delay tolerance represents the number of days beyond the lead time that you're willing to wait before you order new replenishment when existing supply is already planned.</span></span> <span data-ttu-id="f26bc-112">Forsinkelsestoleranse defineres ved å bruke kalenderdager, ikke virkedager.</span><span class="sxs-lookup"><span data-stu-id="f26bc-112">Delay tolerance is defined by using calendar days, not business days.</span></span>

<span data-ttu-id="f26bc-113">Når systemet beregner forsinkelsestoleransen under hovedplanleggingen, vurderer det innstillingen for **Negative dager**.</span><span class="sxs-lookup"><span data-stu-id="f26bc-113">At the time of master planning, when the system calculates the delay tolerance, it considers the **Negative days** setting.</span></span> <span data-ttu-id="f26bc-114">Du kan angi verdien **Negative dager** på **Varedekning**-siden eller **Dekningsgrupper**-siden.</span><span class="sxs-lookup"><span data-stu-id="f26bc-114">You can set the **Negative days** value on either the **Coverage groups** page or the **Item coverage** page.</span></span>

<span data-ttu-id="f26bc-115">Systemet kobler beregningen av forsinkelsestoleranse til den *tidligste etterfyllingsdatoen*, som er lik dagens dato pluss leveringstiden.</span><span class="sxs-lookup"><span data-stu-id="f26bc-115">The system links the delay tolerance calculation to the *earliest replenishment date*, which equals today's date plus the lead time.</span></span> <span data-ttu-id="f26bc-116">Forsinkelsestoleransen beregnes ved å bruke følgende formel, der *maks()* finner den største av to verdier:</span><span class="sxs-lookup"><span data-stu-id="f26bc-116">The delay tolerance is calculated by using following formula, where *max()* finds the larger of two values:</span></span>

<span data-ttu-id="f26bc-117">*maks(Tidligste etterfyllingsdato, Forfallsdato for etterspørsel)* – *Forfallsdato for etterspørsel* + *Negative dager*</span><span class="sxs-lookup"><span data-stu-id="f26bc-117">*max(Earliest replenishment date, Demand due date)* – *Demand due date* + *Negative days*</span></span>

<span data-ttu-id="f26bc-118">Denne formelen sikrer at hovedplanlegging ikke oppretter nye forsyningsordrer når det finnes nok forsyning i løpet av leveringstiden for produktet.</span><span class="sxs-lookup"><span data-stu-id="f26bc-118">This formula ensures that master planning doesn't create new supply orders when enough supply exists during the product lead time.</span></span>

> [!NOTE]
> <span data-ttu-id="f26bc-119">Beregningen av forsinkelsestoleranse i Planleggingsoptimalisering bruker alltid beregning av dynamiske negative dager fra innebygd hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="f26bc-119">The delay tolerance calculation in Planning Optimization always uses the dynamic negative days calculation from built-in master planning.</span></span> <span data-ttu-id="f26bc-120">Innstillingen **Bruk dynamiske negative dager** på siden **Hovedplanleggingsparametere** har ingen innvirkning på denne virkemåten.</span><span class="sxs-lookup"><span data-stu-id="f26bc-120">The **Use dynamic negative days** setting on the **Master planning parameters** page has no effect on this behavior.</span></span>

<span data-ttu-id="f26bc-121">Hvis den eksisterende forsyningen innebærer en forsinkelse i etterspørselen som er mindre enn eller lik den beregnede forsinkelsestoleransen, utligner Planleggingsoptimalisering eksisterende forsyning med behovet.</span><span class="sxs-lookup"><span data-stu-id="f26bc-121">If the existing supply implies a demand delay that is less than or equal to the calculated delay tolerance, Planning Optimization pegs existing supply with the demand.</span></span> <span data-ttu-id="f26bc-122">I noen tilfeller er det bedre å forsinke behovet enn å ende opp med for stor forsyning.</span><span class="sxs-lookup"><span data-stu-id="f26bc-122">In some cases, it's better to delay the demand than to end up with oversupply.</span></span>

<span data-ttu-id="f26bc-123">Følgende underdeler er eksempler som viser hvordan forsinkelsestoleranse påvirker oppretting av planlagte ordrer i Planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="f26bc-123">The following subsections provide examples that show how delay tolerance affects the creation of planned orders in Planning Optimization.</span></span>

### <a name="example-1"></a><span data-ttu-id="f26bc-124">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="f26bc-124">Example 1</span></span>

<span data-ttu-id="f26bc-125">Et produkt har følgende konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="f26bc-125">A product has the following configuration:</span></span>

- <span data-ttu-id="f26bc-126">**Leveringstid:** *10*</span><span class="sxs-lookup"><span data-stu-id="f26bc-126">**Lead time:** *10*</span></span>
- <span data-ttu-id="f26bc-127">**Negative dager:** *2*</span><span class="sxs-lookup"><span data-stu-id="f26bc-127">**Negative days:** *2*</span></span>

<span data-ttu-id="f26bc-128">Følgende tilbud og etterspørsel finnes for produktet:</span><span class="sxs-lookup"><span data-stu-id="f26bc-128">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="f26bc-129">**Behov for i dag:** En salgsordre for et antall på 10</span><span class="sxs-lookup"><span data-stu-id="f26bc-129">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="f26bc-130">**Forsyning om 12 dager:** En bestilling av et antall på 10</span><span class="sxs-lookup"><span data-stu-id="f26bc-130">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="f26bc-131">Eksisterende forsyning kan dekke behovet innen 12 dager, og denne perioden er lik forsinkelsestoleransen.</span><span class="sxs-lookup"><span data-stu-id="f26bc-131">Existing supply can cover the demand within 12 days, and that period equals the delay tolerance.</span></span> <span data-ttu-id="f26bc-132">Når hovedplanleggingen kjøres, blir det derfor ikke opprettet noen planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="f26bc-132">Therefore, when master planning runs, no planned orders are created.</span></span>

### <a name="example-2"></a><span data-ttu-id="f26bc-133">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="f26bc-133">Example 2</span></span>

<span data-ttu-id="f26bc-134">Et produkt har følgende konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="f26bc-134">A product has the following configuration:</span></span>

- <span data-ttu-id="f26bc-135">**Leveringstid:** *10*</span><span class="sxs-lookup"><span data-stu-id="f26bc-135">**Lead time:** *10*</span></span>
- <span data-ttu-id="f26bc-136">**Negative dager:** *0*</span><span class="sxs-lookup"><span data-stu-id="f26bc-136">**Negative days:** *0*</span></span>

<span data-ttu-id="f26bc-137">Følgende tilbud og etterspørsel finnes for produktet:</span><span class="sxs-lookup"><span data-stu-id="f26bc-137">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="f26bc-138">**Behov for i dag:** En salgsordre for et antall på 10</span><span class="sxs-lookup"><span data-stu-id="f26bc-138">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="f26bc-139">**Forsyning om 12 dager:** En bestilling av et antall på 10</span><span class="sxs-lookup"><span data-stu-id="f26bc-139">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="f26bc-140">Eksisterende forsyning kan dekke behovet bare etter 12 dager.</span><span class="sxs-lookup"><span data-stu-id="f26bc-140">Existing supply can cover the demand only after 12 days.</span></span> <span data-ttu-id="f26bc-141">Forsinkelsestoleransen er imidlertid 10 dager.</span><span class="sxs-lookup"><span data-stu-id="f26bc-141">However, the delay tolerance is 10 days.</span></span> <span data-ttu-id="f26bc-142">Når hovedplanleggingen kjøres, vil det derfor opprettes en planlagt bestilling på et antall på 10.</span><span class="sxs-lookup"><span data-stu-id="f26bc-142">Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>

### <a name="example-3"></a><span data-ttu-id="f26bc-143">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="f26bc-143">Example 3</span></span>

<span data-ttu-id="f26bc-144">Et produkt har følgende konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="f26bc-144">A product has the following configuration:</span></span>

- <span data-ttu-id="f26bc-145">**Leveringstid:** *10*</span><span class="sxs-lookup"><span data-stu-id="f26bc-145">**Lead time:** *10*</span></span>
- <span data-ttu-id="f26bc-146">**Negative dager:** *2*</span><span class="sxs-lookup"><span data-stu-id="f26bc-146">**Negative days:** *2*</span></span>

<span data-ttu-id="f26bc-147">Følgende tilbud og etterspørsel finnes for produktet:</span><span class="sxs-lookup"><span data-stu-id="f26bc-147">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="f26bc-148">**Behov om 11 dager:** En salgsordre for et antall på 10</span><span class="sxs-lookup"><span data-stu-id="f26bc-148">**Demand in 11 days:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="f26bc-149">**Forsyning om 14 dager:** En bestilling av et antall på 10</span><span class="sxs-lookup"><span data-stu-id="f26bc-149">**Supply in 14 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="f26bc-150">Eksisterende forsyning kan dekke behovet bare etter tre dager.</span><span class="sxs-lookup"><span data-stu-id="f26bc-150">Existing supply can cover the demand only after three days.</span></span> <span data-ttu-id="f26bc-151">Forsinkelsestoleransen er imidlertid to dager.</span><span class="sxs-lookup"><span data-stu-id="f26bc-151">However, the delay tolerance is two days.</span></span> <span data-ttu-id="f26bc-152">(I dette tilfellet inkluderer forsinkelsestoleransen bare de to negative dagene.</span><span class="sxs-lookup"><span data-stu-id="f26bc-152">(In this case, the delay tolerance includes only the two negative days.</span></span> <span data-ttu-id="f26bc-153">Behovsdatoen er ikke inkludert, fordi den er etter produktets leveringstid.) Når hovedplanleggingen kjøres, vil det derfor opprettes en planlagt bestilling på et antall på 10.</span><span class="sxs-lookup"><span data-stu-id="f26bc-153">The demand date isn't included because it's after the product lead time.) Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>
