---
title: Fysisk restantall i enheten kan ikke være null
description: Når du genererer en følgeseddel, har dataene som leveres til den, et lagerantall som ikke er null, men et null salgsantall.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248796"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a><span data-ttu-id="7b1a0-103">Fysisk restantall i enheten kan ikke være null</span><span class="sxs-lookup"><span data-stu-id="7b1a0-103">Physical remaining quantity in the unit must not be zero</span></span>

<span data-ttu-id="7b1a0-104">Feilkode: SYS19591</span><span class="sxs-lookup"><span data-stu-id="7b1a0-104">Error code: SYS19591</span></span>

## <a name="symptoms"></a><span data-ttu-id="7b1a0-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="7b1a0-105">Symptoms</span></span>

<span data-ttu-id="7b1a0-106">Når du genererer en følgeseddel, har dataene som leveres til den, et lagerantall som ikke er null, men et null salgsantall.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-106">When you generate a packing slip, the data that is supplied to it has a non-zero inventory quantity but a zero sales quantity.</span></span>

<span data-ttu-id="7b1a0-107">Når du prøver å generere følgeseddelen, viser systemet følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="7b1a0-107">When you try to generate the packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="7b1a0-108">Fysisk rest i enheten %1 må være forskjellig fra null.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-108">Physical remaining quantity in the unit %1 must be other than zero.</span></span>

<span data-ttu-id="7b1a0-109">Derfor kan du ikke generere følgeseddelen for belastningen.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="7b1a0-110">Årsak</span><span class="sxs-lookup"><span data-stu-id="7b1a0-110">Cause</span></span>

<span data-ttu-id="7b1a0-111">Systemet evaluerer det fysiske restantallet i lagerenheten og det fysiske restantallet i forsendelsesenheten.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-111">The system evaluates the physical remaining quantity in the inventory unit and the physical remaining quantity in the shipping unit.</span></span> <span data-ttu-id="7b1a0-112">Hvis systemet finner ut at det fysiske restantallet i forsendelsesenheten er 0 (null), men det fysiske restantallet i lagerenheten ikke er 0, kan du ikke generere følgeseddelen.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-112">If the system finds that the physical remaining quantity in the shipping unit is 0 (zero), but the physical remaining quantity in the inventory unit isn't 0, you can't generate the packing slip.</span></span> <span data-ttu-id="7b1a0-113">Dette problemet kan for eksempel oppstå hvis salgsenheten og lagerenheten for varen er forskjellig, og omregningen mellom enheter ikke er nøyaktig.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-113">For example, this issue might occur if the sales unit and inventory unit for the item differ, and the conversion between units isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="7b1a0-114">Løsning</span><span class="sxs-lookup"><span data-stu-id="7b1a0-114">Resolution</span></span>

<span data-ttu-id="7b1a0-115">Lasten eller forsendelsen er for øyeblikket i en tilstand der generering av følgeseddel mislykkes.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="7b1a0-116">Du kan løse dette problemet ved å fullføre én eller flere av følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="7b1a0-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="7b1a0-117">Gå gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-117">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="7b1a0-118">Gå gjennom belastningslinjene, og gjør justeringer for å sikre at antallet kan konverteres rent uten avrundingsproblemer.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-118">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>
- <span data-ttu-id="7b1a0-119">Gjennomgå lastlinjene, og juster for å sikre at enheten og mengden justeres med desimalpresisjonen til enheten.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-119">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>
- <span data-ttu-id="7b1a0-120">Kontroller at lagermåleenheten er mindre enn salgsmåleenheten.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-120">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="7b1a0-121">Gå gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer</span><span class="sxs-lookup"><span data-stu-id="7b1a0-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="7b1a0-122">Bruk følgende fremgangsmåte til å g gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="7b1a0-123">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="7b1a0-124">Velg belastningen som forsendelsen ikke kan bekreftes for.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-124">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="7b1a0-125">I hurtigfanen **Lastlinjer** velger du lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="7b1a0-126">Legg merke til verdien i feltet **Antall for arbeid opprettet**.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="7b1a0-127">I handlingsruten, i fanen **Laster** i gruppen **Relatert informasjon**, velger du **Arbeid**.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="7b1a0-128">Kontroller at arbeidet er fullført på det endelige forsendelsesstedet, og at det plukkede arbeidsantallet samsvarer med det opprettede arbeidsantallet på belastningslinjen.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="7b1a0-129">Gjenta denne fremgangsmåten for alle belastningslinjer for å være sikker på at alle kriteriene er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a><span data-ttu-id="7b1a0-130">Gå gjennom belastningslinjene, og gjør justeringer for å sikre at antallet kan konverteres rent uten avrundingsproblemer</span><span class="sxs-lookup"><span data-stu-id="7b1a0-130">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues</span></span>

<span data-ttu-id="7b1a0-131">Bruke følgende prosedyre til å gå gjennom belastningslinjene, og gjør justeringer for å sikre at antallet kan konverteres rent uten avrundingsproblemer.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-131">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>

1. <span data-ttu-id="7b1a0-132">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="7b1a0-133">Velg lasten som følgeseddelen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="7b1a0-134">I handlingsruten, i fanen **Send og motta** i gruppen  **Omvendt**, velger du  **Reverser forsendelsesbekreftelse**.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="7b1a0-135">I fanen  **Lastlinjer** velger du lastlinjen for varen som overskrider overleveringen.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-135">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery.</span></span>
1. <span data-ttu-id="7b1a0-136">Velg **Reduser plukket antall** for å justere det plukkede antallet.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="7b1a0-137">Velg  **Ordre** i kategorien **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-137">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="7b1a0-138">Angi **Antall**-feltet til det plukkede antallet (det vil si til verdien til feltet **Antall for arbeid opprettet**), slik at generering av følgeseddel kan fortsette.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-138">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="7b1a0-139">Gjennomgå lastlinjene, og juster for å sikre at enheten og mengden justeres med desimalpresisjonen til enheten</span><span class="sxs-lookup"><span data-stu-id="7b1a0-139">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="7b1a0-140">Bruk følgende prosedyre til å gjennomgå lastlinjene, og juster for å sikre at enheten og mengden justeres med desimalpresisjonen til enheten.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-140">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="7b1a0-141">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-141">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="7b1a0-142">Velg lasten som følgeseddelen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-142">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="7b1a0-143">I hurtigfanen **Lastlinjer** velger du lastlinjen for varen som forårsaker problemet.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-143">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="7b1a0-144">Noter verdien i feltene **Antall** og **Enhet**.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-144">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="7b1a0-145">Gå til **Organisasjonsstyring \> Enheter \> Enheter**.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-145">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="7b1a0-146">Velg enheten som følgeseddelen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-146">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="7b1a0-147">Juster verdien i feltet **Desimalpresisjon** etter behov.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-147">Adjust the value of the **Decimal precision** field as required.</span></span>

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a><span data-ttu-id="7b1a0-148">Kontroller at lagermåleenheten er mindre enn salgsmåleenheten</span><span class="sxs-lookup"><span data-stu-id="7b1a0-148">Make sure that the inventory unit of measure is smaller than the sales unit of measure</span></span>

<span data-ttu-id="7b1a0-149">Kontroller at lagermåleenheten er mindre enn salgsmåleenheten.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-149">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span> <span data-ttu-id="7b1a0-150">Vurder om du skal konfigurere måleenheten for varen på nytt etter behov.</span><span class="sxs-lookup"><span data-stu-id="7b1a0-150">Consider reconfiguring the unit of measure for the item as required.</span></span>
