---
title: Strategier for containerpakking
description: Dette emnet beskriver forskjellene mellom strategier for containerpakking og gir eksempler.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f481f6ca047ee0285fe0e81d8fa96665e9d27cee
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292767"
---
# <a name="container-packing-strategies"></a><span data-ttu-id="4b3a8-103">Strategier for containerpakking</span><span class="sxs-lookup"><span data-stu-id="4b3a8-103">Container packing strategies</span></span>

<span data-ttu-id="4b3a8-104">En *containerpakkestrategi* er en strategi som du kan bruke til å definere varetilordninger på tvers av containere.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-104">A *container packing strategy* is a strategy that you can use to define item allocations across containers.</span></span> <span data-ttu-id="4b3a8-105">Dette emnet forklarer forskjellene mellom strategiene *Pakk i alle åpne containere* og *Pakk bare i gjeldende container*.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-105">This topic explains the differences between the *Pack into all open containers* and *Pack into current container only* strategies.</span></span>

- <span data-ttu-id="4b3a8-106">**Pakk inn i alle åpne containere** – Systemet må kontrollere alle åpne containere som allerede er opprettet i løpet av containerbruksyklusen, for å sikre at varen får plass i én av dem.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-106">**Pack into all open containers** – The system must check all open containers that have already been created during the containerization cycle, to make sure that the item will fit into one of them.</span></span> <span data-ttu-id="4b3a8-107">Under pakkingen kontrollerer systemet hver vare for å bestemme om den får plass i en av containerne som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-107">During packing, the system checks each item to determine whether it will fit into any of the previously created containers.</span></span> <span data-ttu-id="4b3a8-108">Hvis varen ikke passer i en eksisterende container, oppretter systemet en ny container og fortsetter til den er ferdig med å pakke hele ordren.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-108">If the item won't fit into an existing container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="4b3a8-109">For eksempel krever *n* bestilte varer containerbruk.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-109">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="4b3a8-110">Hver gang systemet behandler en vare som ikke passer inn i en eksisterende container, vil den gjøre totalt (\[(*n* – 1) × (*n* + 1)\] ÷ 2) kontroller for å evaluere om varen passer i de eksisterende containerne.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-110">In the worst case, every time that the system processes an item that doesn't fit into any existing container, it will do a total of (\[(*n* – 1) × (*n* + 1)\] ÷ 2) checks to evaluate whether the item fits into the existing containers.</span></span>

- <span data-ttu-id="4b3a8-111">**Pakk bare i gjeldende container** – Systemet må bare kontrollere containeren som ble opprettet sist, for å sørge for at varen passer i den.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-111">**Pack into current container only** – The system must check only the most recently created container to make sure that the item will fit into it.</span></span> <span data-ttu-id="4b3a8-112">Under pakkingen kontrollerer systemet hver vare for å bestemme om den får plass i containeren som ble opprettet sist.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-112">During packing, the system checks each item to determine whether it will fit into the most recently created container.</span></span> <span data-ttu-id="4b3a8-113">Hvis varen ikke passer i containeren, oppretter systemet en ny container og fortsetter til den er ferdig med å pakke hele ordren.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-113">If the item won't fit into that container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="4b3a8-114">For eksempel krever *n* bestilte varer containerbruk.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-114">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="4b3a8-115">I verste fall vil systemet gjøre totalt (*n* – 1) kontroller for å evaluere om varen passer i containerne.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-115">In the worst case, the system will do a total of (*n* – 1) checks to evaluate whether the item fits into the containers.</span></span>

## <a name="example-of-the-flow-for-container-packing-strategies"></a><span data-ttu-id="4b3a8-116">Eksempel på flyten for containerpakkestrategier</span><span class="sxs-lookup"><span data-stu-id="4b3a8-116">Example of the flow for container packing strategies</span></span>

<span data-ttu-id="4b3a8-117">Du definerer følgende varer for containerbruk.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-117">You set up the following items for containerization.</span></span>

| <span data-ttu-id="4b3a8-118">Element</span><span class="sxs-lookup"><span data-stu-id="4b3a8-118">Item</span></span> | <span data-ttu-id="4b3a8-119">Fysiske dimensjoner (bredde × dybde × høyde)</span><span class="sxs-lookup"><span data-stu-id="4b3a8-119">Physical dimensions (width × depth × height)</span></span> | <span data-ttu-id="4b3a8-120">Tykkelse</span><span class="sxs-lookup"><span data-stu-id="4b3a8-120">Weight</span></span> |
|---|---|---|
| <span data-ttu-id="4b3a8-121">HDMI-kabel 6'</span><span class="sxs-lookup"><span data-stu-id="4b3a8-121">HDMI Cable 6'</span></span> | <span data-ttu-id="4b3a8-122">1 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="4b3a8-122">1 × 1 × 1</span></span> | <span data-ttu-id="4b3a8-123">1</span><span class="sxs-lookup"><span data-stu-id="4b3a8-123">1</span></span> |
| <span data-ttu-id="4b3a8-124">HDMI-kabel 12'</span><span class="sxs-lookup"><span data-stu-id="4b3a8-124">HDMI Cable 12'</span></span> | <span data-ttu-id="4b3a8-125">2 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="4b3a8-125">2 × 1 × 1</span></span> | <span data-ttu-id="4b3a8-126">1</span><span class="sxs-lookup"><span data-stu-id="4b3a8-126">1</span></span> |
| <span data-ttu-id="4b3a8-127">HDMI-kabel 18'</span><span class="sxs-lookup"><span data-stu-id="4b3a8-127">HDMI Cable 18'</span></span> | <span data-ttu-id="4b3a8-128">3 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="4b3a8-128">3 × 1 × 1</span></span> | <span data-ttu-id="4b3a8-129">2</span><span class="sxs-lookup"><span data-stu-id="4b3a8-129">2</span></span> |

<span data-ttu-id="4b3a8-130">Du angir også følgende boks som skal brukes til pakking.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-130">You also set up the following box that will be used for packaging.</span></span>

| <span data-ttu-id="4b3a8-131">Container</span><span class="sxs-lookup"><span data-stu-id="4b3a8-131">Container</span></span> | <span data-ttu-id="4b3a8-132">Fysiske dimensjoner (lengde × bredde × høyde)</span><span class="sxs-lookup"><span data-stu-id="4b3a8-132">Physical dimensions (length × width × height)</span></span> | <span data-ttu-id="4b3a8-133">Tykkelse</span><span class="sxs-lookup"><span data-stu-id="4b3a8-133">Weight</span></span> | <span data-ttu-id="4b3a8-134">Volum</span><span class="sxs-lookup"><span data-stu-id="4b3a8-134">Volume</span></span> |
|---|---|---|---|
| <span data-ttu-id="4b3a8-135">Middels boks</span><span class="sxs-lookup"><span data-stu-id="4b3a8-135">Medium Box</span></span> | <span data-ttu-id="4b3a8-136">6 × 3 × 2</span><span class="sxs-lookup"><span data-stu-id="4b3a8-136">6 × 3 × 2</span></span> | <span data-ttu-id="4b3a8-137">10</span><span class="sxs-lookup"><span data-stu-id="4b3a8-137">10</span></span> | <span data-ttu-id="4b3a8-138">100</span><span class="sxs-lookup"><span data-stu-id="4b3a8-138">100</span></span> |

<span data-ttu-id="4b3a8-139">Til slutt definerer du en ordre som har følgende produkter og antall.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-139">Finally, you set up an order that has the following products and quantities.</span></span>

| <span data-ttu-id="4b3a8-140">Salgsordrelinje</span><span class="sxs-lookup"><span data-stu-id="4b3a8-140">Sales order line</span></span> | <span data-ttu-id="4b3a8-141">Antall</span><span class="sxs-lookup"><span data-stu-id="4b3a8-141">Quantity</span></span> |
|---|---|
| <span data-ttu-id="4b3a8-142">HDMI-kabel 12'</span><span class="sxs-lookup"><span data-stu-id="4b3a8-142">HDMI Cable 12'</span></span> | <span data-ttu-id="4b3a8-143">9</span><span class="sxs-lookup"><span data-stu-id="4b3a8-143">9</span></span> |
| <span data-ttu-id="4b3a8-144">HDMI-kabel 18'</span><span class="sxs-lookup"><span data-stu-id="4b3a8-144">HDMI Cable 18'</span></span> | <span data-ttu-id="4b3a8-145">8</span><span class="sxs-lookup"><span data-stu-id="4b3a8-145">8</span></span> |
| <span data-ttu-id="4b3a8-146">HDMI-kabel 6'</span><span class="sxs-lookup"><span data-stu-id="4b3a8-146">HDMI Cable 6'</span></span> | <span data-ttu-id="4b3a8-147">13</span><span class="sxs-lookup"><span data-stu-id="4b3a8-147">13</span></span> |

<span data-ttu-id="4b3a8-148">Tabellen nedenfor oppsummerer hvordan containerbruk fungerer når du bruker *Pakk i alle åpne containere*-strategien, og når du bruker *Pakk bare i gjeldende container*-strategien.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-148">The following table summarizes how containerization works when you use the *Pack into all open containers* strategy and when you use the *Pack into current container only* strategy.</span></span>

| <span data-ttu-id="4b3a8-149">Pakk inn i alle åpne containere</span><span class="sxs-lookup"><span data-stu-id="4b3a8-149">Pack into all open containers</span></span> | <span data-ttu-id="4b3a8-150">Pakk i gjeldende container</span><span class="sxs-lookup"><span data-stu-id="4b3a8-150">Pack into current container</span></span> |
|---|---|
| <p><span data-ttu-id="4b3a8-151">HDMI-kabel 12':</span><span class="sxs-lookup"><span data-stu-id="4b3a8-151">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="4b3a8-152">Opprett en ny container, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-152">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="4b3a8-153">Sett 9 ea inn i containeren CONT0001.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-153">Put 9 ea into container CONT0001.</span></span></li></ol> | <p><span data-ttu-id="4b3a8-154">HDMI-kabel 12':</span><span class="sxs-lookup"><span data-stu-id="4b3a8-154">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="4b3a8-155">Opprett en ny container, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-155">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="4b3a8-156">Sett 9 ea inn i containeren CONT0001.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-156">Put 9 ea into container CONT0001.</span></span></li></ol> |
| <p><span data-ttu-id="4b3a8-157">HDMI-kabel 18':</span><span class="sxs-lookup"><span data-stu-id="4b3a8-157">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="4b3a8-158">Kontroller om varen får plass i container CONT0001.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-158">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="4b3a8-159">Opprett en ny container, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-159">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="4b3a8-160">Sett 5 ea inn i containeren CONT0002.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-160">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="4b3a8-161">Opprett en ny container, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-161">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="4b3a8-162">Sett 3 ea inn i containeren CONT0003.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-162">Put 3 ea into container CONT0003.</span></span></li></ol> | <p><span data-ttu-id="4b3a8-163">HDMI-kabel 18':</span><span class="sxs-lookup"><span data-stu-id="4b3a8-163">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="4b3a8-164">Kontroller om varen får plass i container CONT0001.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-164">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="4b3a8-165">Opprett en ny container, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-165">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="4b3a8-166">Sett 5 ea inn i containeren CONT0002.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-166">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="4b3a8-167">Opprett en ny container, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-167">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="4b3a8-168">Sett 3 ea inn i containeren CONT0003.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-168">Put 3 ea into container CONT0003.</span></span></li></ol> |
| <p><span data-ttu-id="4b3a8-169">HDMI-kabel 6':</span><span class="sxs-lookup"><span data-stu-id="4b3a8-169">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="4b3a8-170">Kontroller om varen får plass i container CONT0001.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-170">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="4b3a8-171">Sett 1 ea inn i containeren CONT0001.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-171">Put 1 ea into container CONT0001.</span></span></li><li><span data-ttu-id="4b3a8-172">Kontroller om varen får plass i container CONT0002.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-172">Check whether the item can fit into container CONT0002.</span></span></li><li><span data-ttu-id="4b3a8-173">Kontroller om varen får plass i container CONT0003.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-173">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="4b3a8-174">Sett 4 ea inn i containeren CONT0003.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-174">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="4b3a8-175">Opprett en ny container, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-175">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="4b3a8-176">Sett 8 ea inn i containeren CONT0004.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-176">Put 8 ea into container CONT0004.</span></span></li></ol> | <p><span data-ttu-id="4b3a8-177">HDMI-kabel 6':</span><span class="sxs-lookup"><span data-stu-id="4b3a8-177">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="4b3a8-178">Kontroller om varen får plass i container CONT0003.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-178">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="4b3a8-179">Sett 4 ea inn i containeren CONT0003.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-179">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="4b3a8-180">Opprett en ny container, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-180">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="4b3a8-181">Sett 9 ea inn i containeren CONT0004.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-181">Put 9 ea into container CONT0004.</span></span></li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a><span data-ttu-id="4b3a8-182">Eksempelscenario: Pakke enkeltordrer per container</span><span class="sxs-lookup"><span data-stu-id="4b3a8-182">Example scenario: Pack single orders per container</span></span>

<span data-ttu-id="4b3a8-183">Denne delen presenterer et scenario der systemet er konfigurert til å konsolidere flere ordrer til én forsendelse.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-183">This section presents a scenario where the system is set up to consolidate multiple orders into one shipment.</span></span> <span data-ttu-id="4b3a8-184">Derfor blir containerbruken utført fra salgsordren for å sikre at hver ordre som inneholder flere produkter, blir pakket i sin egen container.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-184">Therefore, containerization will be done from the sales order to ensure that every order that contains multiple products is packed into its own container.</span></span>

<span data-ttu-id="4b3a8-185">Ved hjelp av denne funksjonaliteten kan du håndtere scenarier der du bare må pakke én salgsordre inn i hver container, slik at distribusjonssenteret kan direkteoverføre fulle containere mellom butikker.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-185">This functionality lets you handle scenarios where you must pack only one sales order into each container, so that the distribution center can cross-dock full containers between retail stores.</span></span> <span data-ttu-id="4b3a8-186">I tillegg til detaljhandelsscenarier (ordre per detaljhandel og forsendelse til et distribusjonssenter for direkteoverføring) brukes også denne teknikken i lean/forsyningskjeder (salgsordre per just-in-time-produksjonslinje).</span><span class="sxs-lookup"><span data-stu-id="4b3a8-186">In addition to the retail scenarios (order per retail store and shipping to a distribution center for cross-docking) this technique is also commonly used in lean supply chains (sales order per just-in-time production line).</span></span>

<span data-ttu-id="4b3a8-187">Dette scenariet viser hvordan du kan redusere antall containere som blir evaluert under pakking, ved å bruke *Pakk bare i gjeldende container*-strategi for containerbruk.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-187">This scenario shows how you can decrease the number of containers that are evaluated during packing by using the *Pack into current container only* strategy for containerization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="4b3a8-188">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="4b3a8-188">Prerequisites</span></span>

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a><span data-ttu-id="4b3a8-189">Slå på funksjonen Konsolider forsendelser i systemet</span><span class="sxs-lookup"><span data-stu-id="4b3a8-189">Turn on the Consolidate shipments feature in your system</span></span>

<span data-ttu-id="4b3a8-190">Dette scenariet bruker funksjonen *Konsolider forsendelser*.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-190">This scenario uses the *Consolidate shipments* feature.</span></span> <span data-ttu-id="4b3a8-191">Hvis funksjonen ikke allerede er tilgjengelig i systemet, må du aktivere den ved hjelp av [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4b3a8-191">If that feature isn't already available in your system, you must turn it on by using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

#### <a name="make-demo-data-available"></a><span data-ttu-id="4b3a8-192">Gjøre demodata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="4b3a8-192">Make demo data available</span></span>

<span data-ttu-id="4b3a8-193">Dette scenarioet refererer til verdier og poster som er inkludert i standard demodata som leveres med Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-193">This scenario references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="4b3a8-194">Hvis du vil bruke verdiene som angis her etter hvert som du utfører øvelsene, må du sørge for å arbeide i et miljø der demodataene er installert, og sette den juridiske enheten til **USMF** før du begynner.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-194">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

### <a name="inspect-or-create-container-types"></a><span data-ttu-id="4b3a8-195">Kontrollere eller opprette containertyper</span><span class="sxs-lookup"><span data-stu-id="4b3a8-195">Inspect or create container types</span></span>

<span data-ttu-id="4b3a8-196">Følg denne fremgangsmåten for å kontrollere containertypene eller opprette nye containertyper etter behov.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-196">To inspect your container types, or to create new container types if they are required, follow these steps.</span></span>

1. <span data-ttu-id="4b3a8-197">Gå til **Warehouse Management** \> **Oppsett** \> **Containere** \> **Containertyper**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-197">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>
1. <span data-ttu-id="4b3a8-198">Kontroller at hver av de følgende containertypene er tilgjengelige i demodataene.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-198">Make sure that each of the following container types is available in your demo data.</span></span> <span data-ttu-id="4b3a8-199">Rediger eller opprett containertyper etter behov.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-199">Edit or create container types as required.</span></span>

    - <span data-ttu-id="4b3a8-200">Containertype 1:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-200">Container type 1:</span></span>

        - <span data-ttu-id="4b3a8-201">**Containertypekode:** *Boks-Stor*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-201">**Container type code:** *Box-Large*</span></span>
        - <span data-ttu-id="4b3a8-202">**Beskrivelse:** *Stor boks*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-202">**Description:** *Large Box*</span></span>
        - <span data-ttu-id="4b3a8-203">**Maksimal nettovekt:** *100*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-203">**Maximum net weight:** *100*</span></span>
        - <span data-ttu-id="4b3a8-204">**Volum:** *400*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-204">**Volume:** *400*</span></span>
        - <span data-ttu-id="4b3a8-205">**Lengde:** *4*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-205">**Length:** *4*</span></span>
        - <span data-ttu-id="4b3a8-206">**Bredde:** *10*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-206">**Width:** *10*</span></span>
        - <span data-ttu-id="4b3a8-207">**Høyde:** *10*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-207">**Height:** *10*</span></span>

    - <span data-ttu-id="4b3a8-208">Containertype 2:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-208">Container type 2:</span></span>

        - <span data-ttu-id="4b3a8-209">**Containertypekode:** *Boks-Medium*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-209">**Container type code:** *Box-Medium*</span></span>
        - <span data-ttu-id="4b3a8-210">**Beskrivelse:** *Middels boks*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-210">**Description:** *Medium Box*</span></span>
        - <span data-ttu-id="4b3a8-211">**Maksimal nettovekt:** *50*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-211">**Maximum net weight:** *50*</span></span>
        - <span data-ttu-id="4b3a8-212">**Volum:** *200*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-212">**Volume:** *200*</span></span>
        - <span data-ttu-id="4b3a8-213">**Lengde:** *2*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-213">**Length:** *2*</span></span>
        - <span data-ttu-id="4b3a8-214">**Bredde:** *10*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-214">**Width:** *10*</span></span>
        - <span data-ttu-id="4b3a8-215">**Høyde:** *10*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-215">**Height:** *10*</span></span>

    - <span data-ttu-id="4b3a8-216">Containertype 3:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-216">Container type 3:</span></span>

        - <span data-ttu-id="4b3a8-217">**Containertypekode:** *Boks-Liten*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-217">**Container type code:** *Box-Small*</span></span>
        - <span data-ttu-id="4b3a8-218">**Beskrivelse:** *Liten boks*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-218">**Description:** *Small Box*</span></span>
        - <span data-ttu-id="4b3a8-219">**Maksimal nettovekt:** *20*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-219">**Maximum net weight:** *20*</span></span>
        - <span data-ttu-id="4b3a8-220">**Volum:** *100*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-220">**Volume:** *100*</span></span>
        - <span data-ttu-id="4b3a8-221">**Lengde:** *1*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-221">**Length:** *1*</span></span>
        - <span data-ttu-id="4b3a8-222">**Bredde:** *10*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-222">**Width:** *10*</span></span>
        - <span data-ttu-id="4b3a8-223">**Høyde:** *10*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-223">**Height:** *10*</span></span>

### <a name="inspect-or-create-container-groups"></a><span data-ttu-id="4b3a8-224">Kontrollere eller opprette containergrupper</span><span class="sxs-lookup"><span data-stu-id="4b3a8-224">Inspect or create container groups</span></span>

<span data-ttu-id="4b3a8-225">Følg denne fremgangsmåten for å kontrollere containergruppene eller opprette nye containergrupper etter behov.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-225">To inspect your container groups, or to create new container groups if they are required, follow these steps.</span></span>

1. <span data-ttu-id="4b3a8-226">Gå til **Lagerstyring** \> **Oppsett** \> **Containere** \> **Containergrupper**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-226">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**.</span></span>
1. <span data-ttu-id="4b3a8-227">Kontroller at følgende containergruppe er tilgjengelig i demodataene.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-227">Make sure that the following container group is available in your demo data.</span></span> <span data-ttu-id="4b3a8-228">Hvis den ikke er tilgjengelige, velger du **Ny** for å opprette den.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-228">If it isn't available, select **New** to create it.</span></span>

    - <span data-ttu-id="4b3a8-229">**Containergruppe-ID:** *Bokser*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-229">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="4b3a8-230">**Beskrivelse:** *Boksstørrelser*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-230">**Description:** *Box sizes*</span></span>

1. <span data-ttu-id="4b3a8-231">I hurtigkategorien **Detaljer** for *Bokser*-containergruppen kontrollerer du at følgende linjer finnes.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-231">On the **Details** FastTab for the *Boxes* container group, make sure that the following lines exist.</span></span> <span data-ttu-id="4b3a8-232">Hvis de ikke finnes, velger du **Ny** for å legge dem til.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-232">If they don't, select **New** to add them.</span></span>

    - <span data-ttu-id="4b3a8-233">Linje 1:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-233">Line 1:</span></span>

        - <span data-ttu-id="4b3a8-234">**Sekvensnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-234">**Sequence number:** *1*</span></span>
        - <span data-ttu-id="4b3a8-235">**Containertype:** *Boks-Stor*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-235">**Container type:** *Box-Large*</span></span>
        - <span data-ttu-id="4b3a8-236">**Containerutnyttelsesprosent:** *100*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-236">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="4b3a8-237">Linje 2:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-237">Line 2:</span></span>

        - <span data-ttu-id="4b3a8-238">**Sekvensnummer:** *2*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-238">**Sequence number:** *2*</span></span>
        - <span data-ttu-id="4b3a8-239">**Containertype:** *Boks-Medium*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-239">**Container type:** *Box-Medium*</span></span>
        - <span data-ttu-id="4b3a8-240">**Containerutnyttelsesprosent:** *100*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-240">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="4b3a8-241">Linje 3:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-241">Line 3:</span></span>

        - <span data-ttu-id="4b3a8-242">**Sekvensnummer:** *3*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-242">**Sequence number:** *3*</span></span>
        - <span data-ttu-id="4b3a8-243">**Containertype:** *Boks-Liten*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-243">**Container type:** *Box-Small*</span></span>
        - <span data-ttu-id="4b3a8-244">**Containerutnyttelsesprosent:** *100*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-244">**Container utilization percentage:** *100*</span></span>

### <a name="create-a-new-container-build-template"></a><span data-ttu-id="4b3a8-245">Opprette en ny mal for containerversjon</span><span class="sxs-lookup"><span data-stu-id="4b3a8-245">Create a new container build template</span></span>

<span data-ttu-id="4b3a8-246">Hvis du vil opprette en ny containerversjonsmal, følger du fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-246">To create a new container build template, follow these steps.</span></span>

1. <span data-ttu-id="4b3a8-247">Gå til **Lagerstyring** \> **Oppsett** \> **Containere** \> **Mal for build for container**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-247">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container build template**.</span></span>
1. <span data-ttu-id="4b3a8-248">Velg **Ny** for å opprette en containerversjonsmal med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-248">Select **New** to create a container build template that has the following settings:</span></span>

    - <span data-ttu-id="4b3a8-249">**Sekvensnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-249">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="4b3a8-250">**Containermal-ID:** *Boks*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-250">**Container template ID:** *Box*</span></span>
    - <span data-ttu-id="4b3a8-251">**Containergruppe-ID:** *Bokser*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-251">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="4b3a8-252">**Grunnleggende spørringstyper:** *Salgstildelingslinje*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-252">**Base query types:** *Sales allocation line*</span></span>
    - <span data-ttu-id="4b3a8-253">**Bølgetrinnkode:** *234*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-253">**Wave step code:** *234*</span></span>
    - <span data-ttu-id="4b3a8-254">**Tillat oppdeling av plukking:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-254">**Allow split picks:** *Yes*</span></span>
    - <span data-ttu-id="4b3a8-255">**Pakkestrategi for container:** *Pakk bare i gjeldende container*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-255">**Container packing strategy:** *Pack into current container only*</span></span>
    - <span data-ttu-id="4b3a8-256">**Pakk etter direktivenhet:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-256">**Pack by directive unit:** *No*</span></span>

1. <span data-ttu-id="4b3a8-257">Mens raden for den nye malen fremdeles er valgt, velger du **Rediger spørring** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-257">While the row for the new template is still selected, select **Edit query** on the Action Pane.</span></span>
1. <span data-ttu-id="4b3a8-258">En standard dialogboks for Power Query-redigering vises.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-258">A standard query editor dialog box appears.</span></span> <span data-ttu-id="4b3a8-259">I kategorien **Sortering** velger du **Legg til** for å legge til en rad som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-259">On the **Sorting** tab, select **Add** to add a row that has the following settings:</span></span>

    - <span data-ttu-id="4b3a8-260">**Tabell:** *Midlertidige arbeidstransaksjoner*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-260">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="4b3a8-261">**Avledet tabell:** *Midlertidige arbeidstransaksjoner*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-261">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="4b3a8-262">**Felt:** *Ordrenummer*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-262">**Field:** *Order number*</span></span>
    - <span data-ttu-id="4b3a8-263">**Søkeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-263">**Search direction:** *Ascending*</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="4b3a8-264">For å unngå å måtte sjekke alle åpne containerne og for å gjøre prosessen raskere ved å kontrollere én container om gangen, bruker du strategien *Pakk bare i gjeldende container* i tillegg til å sortere etter ordrenummer.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-264">To avoid cycling over all the other open containers, and to speed up the process by checking one container at a time, use the *Pack into current container only* strategy in addition to sorting by order number.</span></span> <span data-ttu-id="4b3a8-265">Denne kombinasjonen vil fungere som en arbeidspause i en arbeidsmal.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-265">This combination will work like a work break on a work template.</span></span>

1. <span data-ttu-id="4b3a8-266">Velg **OK** for å lukke dialogboksen for redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-266">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="4b3a8-267">Mens raden for den nye malen fremdeles er valgt, velger du **Begrensninger for containerkombinasjoner** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-267">While the row for the new template is still selected, select **Container mixing constraints** on the Action Pane.</span></span>

    <span data-ttu-id="4b3a8-268">Nå legger du til en begrensning som setter varer fra en enkelt ordre inn i en enkelt container.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-268">You will now add a constraint that puts items from a single order into a single container.</span></span> <span data-ttu-id="4b3a8-269">Varer fra en hvilken som helst annen ordre blir plassert i en separat container.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-269">Items from any other order will be put into a separate container.</span></span>

1. <span data-ttu-id="4b3a8-270">Velg **Ny** for å opprette en kombinasjonsbegrensning med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-270">Select **New** to create a mixing constraint that has the following settings:</span></span>

    - <span data-ttu-id="4b3a8-271">**Tabell:** *Salgsordrer*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-271">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="4b3a8-272">**Velg felt:** *SalesId* (Feltet vil vises som *Salgsordre* i rutenettet.)</span><span class="sxs-lookup"><span data-stu-id="4b3a8-272">**Field select:** *SalesId* (The field will appear as *Sales order* in the grid.)</span></span>

1. <span data-ttu-id="4b3a8-273">Velg **OK** for å legge til begrensningen.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-273">Select **OK** to add the constraint.</span></span>
1. <span data-ttu-id="4b3a8-274">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-274">Close the page.</span></span>

### <a name="set-up-a-wave-template-for-containerization"></a><span data-ttu-id="4b3a8-275">Definere en bølgemal for containerbruk</span><span class="sxs-lookup"><span data-stu-id="4b3a8-275">Set up a wave template for containerization</span></span>

<span data-ttu-id="4b3a8-276">Hvis du vil konfigurere en bølgemal, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-276">To set up a wave template, follow these steps.</span></span>

1. <span data-ttu-id="4b3a8-277">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-277">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="4b3a8-278">I listeruten setter du **Bølgemaltype**-feltet til *Forsendelse*.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-278">In the list pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="4b3a8-279">Velg **63 Containerbruk**-malen i listen.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-279">Select the **63 Containerization** template in the list.</span></span>
1. <span data-ttu-id="4b3a8-280">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-280">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4b3a8-281">På hurtigfanen **Metoder**, i kolonnen **Valgte metoder**, finner du følgende linje:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-281">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="4b3a8-282">**Metodenavn:** *containerbruk*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-282">**Method name:** *containerization*</span></span>
    - <span data-ttu-id="4b3a8-283">**Navn:** *Containerbruk*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-283">**Name:** *Containerization*</span></span>

1. <span data-ttu-id="4b3a8-284">Sett feltet **Bølgetrinnkode** for linjen til *234*.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-284">Set the **Wave step code** field for the line to *234*.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="4b3a8-285">Konfigurere en arbeidsmal</span><span class="sxs-lookup"><span data-stu-id="4b3a8-285">Set up a work template</span></span>

<span data-ttu-id="4b3a8-286">Hvis du vil konfigurere en arbeidsmal, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-286">To set up a work template, follow these steps.</span></span>

1. <span data-ttu-id="4b3a8-287">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-287">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="4b3a8-288">Sett feltet **Arbeidsordretype** til *Salgsordrer*.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-288">Set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="4b3a8-289">I rutenettet **Oversikt** finner og velger du arbeidsmalen som skal brukes for pakking av enkeltordrer per container.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-289">In the **Overview** grid, find and select the work template that should be used for packing single orders per container.</span></span> <span data-ttu-id="4b3a8-290">I dette scenarioet velger du malen **63 Plukk til container**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-290">For this scenario, select the **63 Pick to container** template.</span></span>
1. <span data-ttu-id="4b3a8-291">I handlingsruten velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-291">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="4b3a8-292">En standard dialogboks for Power Query-redigering vises.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-292">A standard query editor dialog box appears.</span></span> <span data-ttu-id="4b3a8-293">I kategorien **Sortering** legger du til følgende linjer:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-293">On the **Sorting** tab, add the following lines:</span></span>

    - <span data-ttu-id="4b3a8-294">Linje 1:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-294">Line 1:</span></span>

        - <span data-ttu-id="4b3a8-295">**Tabell:** *Midlertidige arbeidstransaksjoner*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-295">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="4b3a8-296">**Avledet tabell:** *Midlertidige arbeidstransaksjoner*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-296">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="4b3a8-297">**Felt:** *Leverings-ID*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-297">**Field:** *Shipment ID*</span></span>
        - <span data-ttu-id="4b3a8-298">**Søkeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-298">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="4b3a8-299">Linje 2:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-299">Line 2:</span></span>

        - <span data-ttu-id="4b3a8-300">**Tabell:** *Midlertidige arbeidstransaksjoner*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-300">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="4b3a8-301">**Avledet tabell:** *Midlertidige arbeidstransaksjoner*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-301">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="4b3a8-302">**Felt:** *Ordrenummer*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-302">**Field:** *Order number*</span></span>
        - <span data-ttu-id="4b3a8-303">**Søkeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-303">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="4b3a8-304">Linje 3:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-304">Line 3:</span></span>

        - <span data-ttu-id="4b3a8-305">**Tabell:** *Midlertidige arbeidstransaksjoner*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-305">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="4b3a8-306">**Avledet tabell:** *Midlertidige arbeidstransaksjoner*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-306">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="4b3a8-307">**Felt:** *Container-ID*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-307">**Field:** *Container ID*</span></span>
        - <span data-ttu-id="4b3a8-308">**Søkeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-308">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="4b3a8-309">Velg **OK** for å lukke dialogboksen for redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-309">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="4b3a8-310">Du får følgende melding: «Grupperingen blir tilbakeført – vil du fortsette?»</span><span class="sxs-lookup"><span data-stu-id="4b3a8-310">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="4b3a8-311">Klikk på **Ja** for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-311">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="4b3a8-312">Selv om malen **63 Plukk til container** er valgt, velger du **Arbeidshodeskift** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-312">While the **63 Pick to container** template is still selected, select **Work header breaks** on the Action Pane.</span></span>

    <span data-ttu-id="4b3a8-313">Du bruker nå innstillinger til å bryte arbeidet, slik at hver container i ordren er koblet til én arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-313">You will now apply settings to break the work so that each container in the order is linked to one work order.</span></span>

1. <span data-ttu-id="4b3a8-314">Merk av for **Grupper etter dette feltet** for hver rad på siden **Arbeidshodeskift** (**Forsendelses-ID**, **Ordrenummer** og **Container-ID**).</span><span class="sxs-lookup"><span data-stu-id="4b3a8-314">Select the **Group by this field** checkbox for each row on the **Work header breaks** page (**Shipment ID**, **Order number**, and **Container ID**).</span></span>
1. <span data-ttu-id="4b3a8-315">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-315">Close the page.</span></span>

### <a name="set-up-shipment-consolidation-policies"></a><span data-ttu-id="4b3a8-316">Konfigurere policyer for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="4b3a8-316">Set up shipment consolidation policies</span></span>

<span data-ttu-id="4b3a8-317">Følg denne fremgangsmåten for å definere en policy for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-317">To set up a shipment consolidation policy, follow these steps.</span></span>

1. <span data-ttu-id="4b3a8-318">Gå til **Lagerbehandling \> Oppsett \> Frigi til lager \> Policyer for forsendelseskonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-318">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="4b3a8-319">I listeruten setter du *Policytype* til **Salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-319">In the list pane, set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="4b3a8-320">Velg **Standard** policy i listen.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-320">Select the **Default** policy in the list.</span></span>
1. <span data-ttu-id="4b3a8-321">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-321">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4b3a8-322">I hurtigfanen **Konsolideringsfelt** i listen **Valgte felt** velger du raden der feltet **Feltnavn** er satt til *Ordrenummer*.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-322">On the **Consolidation fields** FastTab, in the **Selected fields** list, select the row where the **Field name** field is set to *Order number*.</span></span>
1. <span data-ttu-id="4b3a8-323">Velg **Fjern**-knappen ![Pil venstre](media/backward-button.png) for å flytte feltet til listen **Gjenværende felt**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-323">Select the **Remove** button ![Left arrow](media/backward-button.png) to move the field to the **Remaining fields** list.</span></span>
1. <span data-ttu-id="4b3a8-324">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-324">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-physical-dimensions-for-the-product"></a><span data-ttu-id="4b3a8-325">Konfigurere fysiske dimensjoner for produktet</span><span class="sxs-lookup"><span data-stu-id="4b3a8-325">Set up physical dimensions for the product</span></span>

<span data-ttu-id="4b3a8-326">Følg denne fremgangsmåten for å definere fysiske dimensjoner for produktene som skal brukes i dette scenariet.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-326">To set up physical dimensions for the products that will be used in this scenario, follow these steps.</span></span>

1. <span data-ttu-id="4b3a8-327">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-327">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="4b3a8-328">Velg produktet der feltet **Varenummer** er satt til *A0001*.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-328">Select the product where the **Item number** field is set to *A0001*.</span></span>
1. <span data-ttu-id="4b3a8-329">I handlingsruten i fanen **Administrer lager** i gruppen **Lager** velger du **Fysiske dimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-329">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="4b3a8-330">På siden **Fysiske dimensjoner** skal du se følgende linje i rutenettet:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-330">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="4b3a8-331">**Enhet:** *stk*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-331">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="4b3a8-332">**Bruttovekt:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-332">**Gross weight:** *3.00*</span></span>
    - <span data-ttu-id="4b3a8-333">**Bredde:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-333">**Width:** *2.00*</span></span>
    - <span data-ttu-id="4b3a8-334">**Dybde:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-334">**Depth:** *2.00*</span></span>
    - <span data-ttu-id="4b3a8-335">**Høyde:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-335">**Height:** *4.00*</span></span>
    - <span data-ttu-id="4b3a8-336">**Volum:** *16,00*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-336">**Volume:** *16.00*</span></span>

1. <span data-ttu-id="4b3a8-337">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-337">Close the page.</span></span>
1. <span data-ttu-id="4b3a8-338">Velg produktet der feltet **Varenummer** er satt til *A0002*.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-338">Select the product where the **Item number** field is set to *A0002*.</span></span>
1. <span data-ttu-id="4b3a8-339">I handlingsruten i fanen **Administrer lager** i gruppen **Lager** velger du **Fysiske dimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-339">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="4b3a8-340">På siden **Fysiske dimensjoner** skal du se følgende linje i rutenettet:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-340">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="4b3a8-341">**Enhet:** *stk*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-341">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="4b3a8-342">**Bruttovekt:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-342">**Gross weight:** *4.00*</span></span>
    - <span data-ttu-id="4b3a8-343">**Bredde:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-343">**Width:** *3.00*</span></span>
    - <span data-ttu-id="4b3a8-344">**Dybde:** *1,00*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-344">**Depth:** *1.00*</span></span>
    - <span data-ttu-id="4b3a8-345">**Høyde:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-345">**Height:** *3.00*</span></span>
    - <span data-ttu-id="4b3a8-346">**Volum:** *9,00*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-346">**Volume:** *9.00*</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="4b3a8-347">Opprett salgsordre 1</span><span class="sxs-lookup"><span data-stu-id="4b3a8-347">Create sales order 1</span></span>

<span data-ttu-id="4b3a8-348">Følg fremgangsmåten nedenfor for å opprette en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-348">To create a sales order, follow these steps.</span></span>

1. <span data-ttu-id="4b3a8-349">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-349">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="4b3a8-350">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-350">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4b3a8-351">Det vises en dialogboks for oppretting av en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-351">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="4b3a8-352">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-352">Set the following values:</span></span>

    - <span data-ttu-id="4b3a8-353">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-353">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="4b3a8-354">**Lager:** *63*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-354">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="4b3a8-355">Velg **OK** for å opprette salgsorden og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-355">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="4b3a8-356">Den nye salgsordren åpnes.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-356">The new sales order is opened.</span></span> <span data-ttu-id="4b3a8-357">Legg til følgende salgslinjer i hurtigfanen **Salgsordrelinjer**:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-357">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="4b3a8-358">Linje 1:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-358">Line 1:</span></span>

        - <span data-ttu-id="4b3a8-359">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-359">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="4b3a8-360">**Antall:** *2*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-360">**Quantity:** *2*</span></span>

    - <span data-ttu-id="4b3a8-361">Linje 2:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-361">Line 2:</span></span>

        - <span data-ttu-id="4b3a8-362">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-362">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="4b3a8-363">**Antall:** *2*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-363">**Quantity:** *2*</span></span>

1. <span data-ttu-id="4b3a8-364">Velg den første linjen, og velg deretter **Lager \> Reservasjon**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-364">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="4b3a8-365">På **Reservasjon**-siden velger du **Reserver parti**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-365">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="4b3a8-366">Lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-366">Then close the page.</span></span>
1. <span data-ttu-id="4b3a8-367">Gjenta de to forrige trinnene for den andre linjen.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-367">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="4b3a8-368">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-368">Close the page.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="4b3a8-369">Opprett salgsordre 2</span><span class="sxs-lookup"><span data-stu-id="4b3a8-369">Create sales order 2</span></span>

<span data-ttu-id="4b3a8-370">Følg denne fremgangsmåten for å opprette en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-370">To create a second sales order, follow these steps.</span></span>

1. <span data-ttu-id="4b3a8-371">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-371">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="4b3a8-372">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-372">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4b3a8-373">Det vises en dialogboks for oppretting av en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-373">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="4b3a8-374">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-374">Set the following values:</span></span>

    - <span data-ttu-id="4b3a8-375">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="4b3a8-376">**Lager:** *63*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-376">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="4b3a8-377">Velg **OK** for å opprette salgsorden og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-377">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="4b3a8-378">Den nye salgsordren åpnes.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-378">The new sales order is opened.</span></span> <span data-ttu-id="4b3a8-379">Legg til følgende salgslinjer i hurtigfanen **Salgsordrelinjer**:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-379">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="4b3a8-380">Linje 1:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-380">Line 1:</span></span>

        - <span data-ttu-id="4b3a8-381">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-381">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="4b3a8-382">**Antall:** *4*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-382">**Quantity:** *4*</span></span>

    - <span data-ttu-id="4b3a8-383">Linje 2:</span><span class="sxs-lookup"><span data-stu-id="4b3a8-383">Line 2:</span></span>

        - <span data-ttu-id="4b3a8-384">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-384">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="4b3a8-385">**Antall:** *4*</span><span class="sxs-lookup"><span data-stu-id="4b3a8-385">**Quantity:** *4*</span></span>

1. <span data-ttu-id="4b3a8-386">Velg den første linjen, og velg deretter **Lager \> Reservasjon**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-386">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="4b3a8-387">På **Reservasjon**-siden velger du **Reserver parti**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-387">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="4b3a8-388">Lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-388">Then close the page.</span></span>
1. <span data-ttu-id="4b3a8-389">Gjenta de to forrige trinnene for den andre linjen.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-389">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="4b3a8-390">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-390">Close the page.</span></span>

### <a name="create-the-load"></a><span data-ttu-id="4b3a8-391">Opprette lasten</span><span class="sxs-lookup"><span data-stu-id="4b3a8-391">Create the load</span></span>

<span data-ttu-id="4b3a8-392">Følg disse trinnene for å opprette en last for hvert ordresett du har opprettet for dette , og deretter frigi det til lageret.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-392">To create a load for each order that you created for this scenario and then release it to the warehouse, follow these steps.</span></span>

1. <span data-ttu-id="4b3a8-393">Gå til **Lagerstyring \> Laster \> Arbeidsområde for lastplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-393">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="4b3a8-394">I fanen **Salgslinjer** finner og velger du alle salgsordrelinjene fra salgsordrene du opprettet for dette scenarioet.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-394">On the **Sales lines** tab, find and select all the sales order lines from the sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="4b3a8-395">I handlingsruten, på **Forsyning og behov**-fanen, i **Legg til**-gruppen, velg **Til ny last**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-395">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span> <span data-ttu-id="4b3a8-396">De valgte ordrelinjene legges til i en ny last.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-396">The selected order lines are added to a new load.</span></span>
1. <span data-ttu-id="4b3a8-397">I dialogboksen **Tilordning av lastmal** i feltet **Lastmal-ID** velger du en lastmal, for eksempel *40' Container*.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-397">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *40' Container*.</span></span>
1. <span data-ttu-id="4b3a8-398">Velg **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-398">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="4b3a8-399">I delen **Laster** finner og velger du lasten du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-399">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="4b3a8-400">Velg **Frigivelse \> Frigi til lager**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-400">Select **Release \> Release to warehouse**.</span></span>
1. <span data-ttu-id="4b3a8-401">I dialogboksen **Frigi til lager** velger du **OK** for å frigi den valgte lasten til lageret.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-401">In the **Release to warehouse** dialog box, select **OK** to release the selected load to the warehouse.</span></span>

### <a name="verify-the-shipments-and-containers"></a><span data-ttu-id="4b3a8-402">Kontrollere forsendelsene og containerne</span><span class="sxs-lookup"><span data-stu-id="4b3a8-402">Verify the shipments and containers</span></span>

<span data-ttu-id="4b3a8-403">Ved hjelp av fremgangsmåten nedenfor kan du verifisere forsendelsene som er opprettet.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-403">The following procedure lets you verify the shipments that have been created.</span></span> <span data-ttu-id="4b3a8-404">Bruk det til å gå gjennom rekkefølgen du opprettet for dette scenariet, for å sikre at du har fått de forventede resultatene.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-404">Use it to review the order that you created for this scenario, to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="4b3a8-405">Gå til **Lagerstyring \> Forsendelser \> Alle forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-405">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="4b3a8-406">Finn og velg forsendelsen som ble opprettet for belastningen som du akkurat har frigitt.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-406">Find and select the shipment that was created for the load that you just released.</span></span>
1. <span data-ttu-id="4b3a8-407">I handlingsruten, i kategorien **Transport**, velger du **Vis containere**.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-407">On the Action Pane, on the **Transportation** tab, select **View containers**.</span></span>
1. <span data-ttu-id="4b3a8-408">Bekreft at varene fra salgsordrene ble containerbrukt i to ulike containere.</span><span class="sxs-lookup"><span data-stu-id="4b3a8-408">Confirm that the items from the sales orders were containerized into two different containers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4b3a8-409">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4b3a8-409">Additional resources</span></span>

- [<span data-ttu-id="4b3a8-410">Containerbruk</span><span class="sxs-lookup"><span data-stu-id="4b3a8-410">Containerization</span></span>](wave-containerization.md)
