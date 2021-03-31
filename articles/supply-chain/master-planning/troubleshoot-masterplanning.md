---
title: Feilsøke hovedplanlegging
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med hovedplanlegging.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: db336946873fa1b5cc3f669823541af8cab4115b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216111"
---
# <a name="troubleshoot-master-planning"></a><span data-ttu-id="b7ce9-103">Feilsøke hovedplanlegging</span><span class="sxs-lookup"><span data-stu-id="b7ce9-103">Troubleshoot master planning</span></span>

<span data-ttu-id="b7ce9-104">Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-104">This topic describes how to fix issues that you might encounter while you work with master planning.</span></span>

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a><span data-ttu-id="b7ce9-105">Stykklistenedbryting er forskjellig for autoriserte produksjonsordrer og for estimerte produksjonsordrer for manuelt opprettet arbeid.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-105">Bill of materials explosion behaves differently for firmed production orders and for estimated production orders for manually created work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b7ce9-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b7ce9-106">Issue description</span></span>

<span data-ttu-id="b7ce9-107">Når en produksjonsordre blir autorisert, blir ikke varene nedbrutt når du deler opp stykklisten.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-107">When a production order is firmed, the items aren't exploded when you explode the bill of materials (BOM).</span></span> <span data-ttu-id="b7ce9-108">Når du oppretter en arbeidsordre manuelt og deretter estimerer produksjonsordren, deles imidlertid varene opp.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-108">However, when you manually create a work order and then estimate the production order, the items are exploded.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b7ce9-109">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="b7ce9-109">Issue resolution</span></span>

<span data-ttu-id="b7ce9-110">Systemet fungerer som forventet.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-110">The system is working as expected.</span></span> <span data-ttu-id="b7ce9-111">Nedbrytingen som skjer når produksjonsordren autoriseres, vil peke mot den planlagte ordren, men den viser ikke at den planlagte ordren for øyeblikket er autorisert i dette tilfellet.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-111">The explosion that occurs when the production order is firmed will point to the planned order, but it doesn't appear that the planned order is currently firmed in this case.</span></span> <span data-ttu-id="b7ce9-112">Hvis imidlertid produksjonsordren er estimert, utløses nedbrytingen fra den frigitte produksjonsordren der det ikke finnes noen planlagt ordre.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-112">However, if the production order has been estimated, the explosion is triggered from the released production order where no planned order exists.</span></span>

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a><span data-ttu-id="b7ce9-113">Forsinkelsesverdien oppdateres ikke når jeg planlegger en planlagt ordre på nytt.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-113">The Delay value isn't updated when I reschedule a planned order.</span></span>

<span data-ttu-id="b7ce9-114">Hvis du vil oppdatere forsinkelsen for planlagte ordrer, åpner du dialogboksen **Ny planlegging** for den planlagte ordren.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-114">To update the delay for planned orders, open the **Rescheduling** dialog box for the planned order.</span></span> <span data-ttu-id="b7ce9-115">I hurtigfanen **Nedbryting** kontrollerer du at alternativet **Utfør nedbryting etter ny planlegging** er satt til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-115">On the **Explosion** FastTab, make sure that the **Perform explosion after rescheduling** option is set to *Yes*.</span></span>

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a><span data-ttu-id="b7ce9-116">Produksjonsplanlegging tar ikke hensyn til sikkerhetsmarginene som er angitt for varedekningen for tilknyttet forsyning.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-116">Production scheduling doesn't consider the safety margins that are set on the item coverage for pegged supply.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b7ce9-117">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b7ce9-117">Issue description</span></span>

<span data-ttu-id="b7ce9-118">Hovedplanleggingen anser sikkerhetsmarginene.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-118">Master planning considers the safety margins.</span></span> <span data-ttu-id="b7ce9-119">Sikkerhetsmarginer ignoreres imidlertid når planlagte produksjonsordrer planlegges.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-119">However, the safety margins are ignored when planned production orders are scheduled.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b7ce9-120">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="b7ce9-120">Issue resolution</span></span>

<span data-ttu-id="b7ce9-121">Marger vurderes bare under hovedplanlegging, ikke under manuell planlegging.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-121">Margins are considered only during master planning, not during manual scheduling.</span></span> <span data-ttu-id="b7ce9-122">Marger er utformet for å fungere som en buffer i planleggingsfasen for å gi litt margin for den faktiske prosessen.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-122">Margins are designed to act as a buffer during the planning phase, to give some "margin" for the actual process.</span></span>

<span data-ttu-id="b7ce9-123">Hvis du vil oppnå ønsket resultat, kan du fjerne marginen.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-123">To get the desired result, you can remove the margin.</span></span> <span data-ttu-id="b7ce9-124">Ruten må deretter oppdateres slik at den inneholder ønsket tid (for eksempel køtid).</span><span class="sxs-lookup"><span data-stu-id="b7ce9-124">The route must then be updated so that it includes the desired time (for example, as queue time).</span></span> <span data-ttu-id="b7ce9-125">Samtidig skal både hovedplanlegging og manuell planlegging gi samme resultat.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-125">Both master planning and manual scheduling should then produce the same result.</span></span>

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a><span data-ttu-id="b7ce9-126">Planlagte ordrer genereres selv om vi har varer på lager og produksjonsordrer allerede finnes for dem.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-126">Planned orders are generated even though we have items in stock and production orders already exist for them.</span></span>

<span data-ttu-id="b7ce9-127">Det kan hende at du kan løse dette problemet ved å øke verdien **Positive dager** for de relevante gruppene på siden **Dekningsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-127">You might be able to fix this issue by increasing the **Positive days** value for the relevant groups on the **Coverage group** page.</span></span> <span data-ttu-id="b7ce9-128">Denne endringen vil føre til at systemet fastslår om lagerbeholdningen kan brukes for behovet.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-128">This change will cause the system to determine whether on-hand inventory can be used for the demand.</span></span> <span data-ttu-id="b7ce9-129">Da vil det ikke bli generert en ny planlagt ordre for varene som er på lager.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-129">Then a new planned order won't be generated for the items that are in stock.</span></span>

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a><span data-ttu-id="b7ce9-130">Hovedplanleggingen ser ikke ut til å respektere kapasitetsbegrensninger og planlegger mer enn tilgjengelig kapasitet.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-130">Master planning doesn't seem to respect capacity limitations and is scheduling more than the available capacity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b7ce9-131">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b7ce9-131">Issue description</span></span>

<span data-ttu-id="b7ce9-132">Når du bruker grovplanlegging der det er begrenset kapasitet, og der ruten angir en blanding av krav for både en ressursgruppe og individuelle ressurser, er det en liten sjanse for overbestilling på grunn av måten algoritmen validerer på kapasitetskonflikter på.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-132">When you use operation scheduling where there is finite capacity, and where the route specifies a mix of requirements for both a resource group and individual resources, there is a small chance of overbooking because of the way that the algorithm validates for capacity conflicts.</span></span> <span data-ttu-id="b7ce9-133">Denne overbestillingen kan forekomme når du bruker hjelpeprogrammer til å kjøre hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-133">This overbooking can occur when you use helpers to run master planning.</span></span> <span data-ttu-id="b7ce9-134">Det er mest sannsynlig at det oppstår hvis det finnes mange jobber som har en relativt kort kjøretid.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-134">It's most likely to occur if there are many jobs that have a relatively short runtime.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b7ce9-135">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="b7ce9-135">Issue resolution</span></span>

<span data-ttu-id="b7ce9-136">Hvis det er viktig at ingen overbestilling forekommer for grovplanlegging, kan du gjøre planleggingsdelen av enkelttrådbasert hovedplanlegging ved å aktivere alternativet **Nøyaktig, begrenset kapasitet for grovplanlegging** på siden **Parametere for hovedplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-136">If it's essential that no overbooking occur for operation scheduling, you can make the scheduling part of master planning single-threaded by turning on the **Accurate finite capacity for Operation Scheduling** option on the **Master planning parameters** page.</span></span> <span data-ttu-id="b7ce9-137">Dette alternativet er ikke tilgjengelig som standard.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-137">This option isn't available by default.</span></span> <span data-ttu-id="b7ce9-138">Du må legge den til siden manuelt ved hjelp av tilpasningsfunksjonene.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-138">You must manually add it to the page by using personalization features.</span></span> <span data-ttu-id="b7ce9-139">Når du bruker dette alternativet, vil planleggingen kjøre saktere på grunn av mangelen på parallell behandling.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-139">When you use this option, scheduling will run more slowly because of the lack of parallel processing.</span></span>

## <a name="planned-orders-take-a-long-time-to-update"></a><span data-ttu-id="b7ce9-140">Det tar lang tid å oppdatere planlagte ordrer.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-140">Planned orders take a long time to update.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b7ce9-141">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b7ce9-141">Issue description</span></span>

<span data-ttu-id="b7ce9-142">Når du oppdaterer behovsantallet eller leveringsdatoen på en planlagt ordre, tar det vanligvis minst 30 sekunder per ordre for å lagre oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-142">When updating the requirement quantity and/or delivery date on a planned order, it typically takes at least 30 seconds per order to save the update.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b7ce9-143">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="b7ce9-143">Issue resolution</span></span>

<span data-ttu-id="b7ce9-144">Dette er et kjent problem med den innebygde hovedplanleggingsmotoren.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-144">This is a known issue with the built-in master planning engine.</span></span> <span data-ttu-id="b7ce9-145">Det skyldes den underliggende automatiske nedbrytingen gjennom stykklistestrukturen under redigeringer.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-145">It is caused by the underlying auto explosion through the BOM structure during edits.</span></span> <span data-ttu-id="b7ce9-146">Dette problemet omtales i planleggingsoptimalisering, der en planlegger kan oppdatere og godkjenne de relevante ordrene og, når det er ønskelig, utløse en planleggingskjøring for å oppdatere planlagte ordrer for den underliggende stykklistestrukturen.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-146">This issue is addressed in Planning Optimization, where a planner can update and approve the relevant orders and, when desired, trigger a planning run to update planned orders for the underlying BOM structure.</span></span>

<span data-ttu-id="b7ce9-147">Én måte å forbedre ytelsen med den innebygde hovedplanleggingsmotoren på er å gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="b7ce9-147">One way to improve performance with the built-in master planning engine is to do the following:</span></span>

1. <span data-ttu-id="b7ce9-148">Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-148">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="b7ce9-149">Velg en plan.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-149">Select a plan.</span></span>
1. <span data-ttu-id="b7ce9-150">Utvid hurtigfanen **Horisont i dager**.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-150">Expand the **Time fence in days** FastTab.</span></span>
1. <span data-ttu-id="b7ce9-151">Angi **Nedbryting** til *Ja*, og sett feltet under denne innstillingen til 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b7ce9-151">Set **Explosion** to *Yes*, and set the field below this setting to 0 (zero).</span></span>

> [!NOTE]
> <span data-ttu-id="b7ce9-152">Dette vil begrense perioden for nedbrytinger som utføres for denne hovedplanen, til én enkelt dag.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-152">This will limit the period for explosions performed for this master plan to a single day.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]