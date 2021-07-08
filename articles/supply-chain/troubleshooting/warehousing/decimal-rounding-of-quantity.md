---
title: Desimalrunding av det fysiske oppdateringsantallet er feil
description: Når du genererer en følgeseddel, inneholder den utgående lasten et antall som ikke samsvarer med desimalpresisjonen som er angitt i enheten.
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
ms.openlocfilehash: 1e63440834f516879aa8ad711bd789e62b0ee993
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248797"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a><span data-ttu-id="562b7-103">Desimalrunding av det fysiske oppdateringsantallet er feil</span><span class="sxs-lookup"><span data-stu-id="562b7-103">Decimal rounding of the physical updating quantity is incorrect</span></span>

<span data-ttu-id="562b7-104">Feilkode: SYS19589</span><span class="sxs-lookup"><span data-stu-id="562b7-104">Error code: SYS19589</span></span>

## <a name="symptoms"></a><span data-ttu-id="562b7-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="562b7-105">Symptoms</span></span>

<span data-ttu-id="562b7-106">Når du genererer en følgeseddel, inneholder den utgående lasten et antall som ikke samsvarer med desimalpresisjonen som er angitt i enheten.</span><span class="sxs-lookup"><span data-stu-id="562b7-106">When you generate a packing slip, the outbound load contains a quantity that doesn't match the decimal precision that is defined in the unit.</span></span>

<span data-ttu-id="562b7-107">Når du prøver å generere en følgeseddel, viser systemet følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="562b7-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="562b7-108">Desimalavrunding av det fysiske oppdateringsantallet i enheten %1 er feil.</span><span class="sxs-lookup"><span data-stu-id="562b7-108">Decimal rounding of the physical updating quantity in the unit %1 is incorrect.</span></span>

<span data-ttu-id="562b7-109">Derfor kan du ikke generere følgeseddelen for belastningen.</span><span class="sxs-lookup"><span data-stu-id="562b7-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="562b7-110">Årsak</span><span class="sxs-lookup"><span data-stu-id="562b7-110">Cause</span></span>

<span data-ttu-id="562b7-111">Systemet evaluerer om desimalavrundingen av forsendelsesantallet tilsvarer desimalpresisjonen som er definert for forsendelsesenheten.</span><span class="sxs-lookup"><span data-stu-id="562b7-111">The system evaluates whether the decimal rounding of the shipping quantity corresponds to the decimal precision that is defined for the shipping unit.</span></span> <span data-ttu-id="562b7-112">Når systemet runder av forsendelsesantallet til det angitte antallet desimaler, og det blir funnet ut at det avrundede forsendelsesantallet ikke samsvarer med det faktiske forsendelsesantallet, kan du ikke generere følgeseddelen.</span><span class="sxs-lookup"><span data-stu-id="562b7-112">When the system rounds the shipping quantity to the specified number of decimal places, if it finds that the rounded shipping quantity doesn't match the actual shipping quantity, you can't generate the packing slip.</span></span> <span data-ttu-id="562b7-113">Dette problemet kan for eksempel oppstå hvis salgsantallet er 1,75 kilogram (kg), men desimalpresisjonen er satt til *1*.</span><span class="sxs-lookup"><span data-stu-id="562b7-113">For example, this issue might occur if the sales quantity is 1.75 kilograms (kg), but the decimal precision is set to *1*.</span></span>

## <a name="resolution"></a><span data-ttu-id="562b7-114">Løsning</span><span class="sxs-lookup"><span data-stu-id="562b7-114">Resolution</span></span>

<span data-ttu-id="562b7-115">Lasten eller forsendelsen er for øyeblikket i en tilstand der generering av følgeseddel mislykkes.</span><span class="sxs-lookup"><span data-stu-id="562b7-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="562b7-116">Du kan løse dette problemet ved å fullføre én eller flere av følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="562b7-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="562b7-117">Gå gjennom lastlinjene, og gjør justeringer for å sikre at antallet kan konverteres rent uten desimalnumre og andre avrundingsproblemer.</span><span class="sxs-lookup"><span data-stu-id="562b7-117">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>
- <span data-ttu-id="562b7-118">Gjennomgå lastlinjene, og juster for å sikre at enheten og mengden justeres med desimalpresisjonen til enheten.</span><span class="sxs-lookup"><span data-stu-id="562b7-118">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a><span data-ttu-id="562b7-119">Gå gjennom lastlinjene, og gjør justeringer for å sikre at antallet kan konverteres rent uten desimalnumre og andre avrundingsproblemer</span><span class="sxs-lookup"><span data-stu-id="562b7-119">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues</span></span>

<span data-ttu-id="562b7-120">Bruk følgende prosedyre til å gå gjennom lastlinjene, og gjør justeringer for å sikre at antallet kan konverteres rent uten desimalnumre og andre avrundingsproblemer.</span><span class="sxs-lookup"><span data-stu-id="562b7-120">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>

1. <span data-ttu-id="562b7-121">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="562b7-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="562b7-122">Velg lasten som følgeseddelen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="562b7-122">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="562b7-123">I handlingsruten, i fanen **Send og motta** i gruppen  **Omvendt**, velger du  **Reverser forsendelsesbekreftelse**.</span><span class="sxs-lookup"><span data-stu-id="562b7-123">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="562b7-124">I fanen  **Lastlinjer** velger du lastlinjen for varen som forårsaker problemet.</span><span class="sxs-lookup"><span data-stu-id="562b7-124">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="562b7-125">Velg **Reduser plukket antall** for å justere det plukkede antallet.</span><span class="sxs-lookup"><span data-stu-id="562b7-125">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="562b7-126">Velg  **Ordre** i kategorien **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="562b7-126">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="562b7-127">Angi **Antall**-feltet til det plukkede antallet (det vil si til verdien til feltet **Antall for arbeid opprettet**), slik at generering av følgeseddel kan fortsette.</span><span class="sxs-lookup"><span data-stu-id="562b7-127">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="562b7-128">Gjennomgå lastlinjene, og juster for å sikre at enheten og mengden justeres med desimalpresisjonen til enheten</span><span class="sxs-lookup"><span data-stu-id="562b7-128">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="562b7-129">Bruk følgende prosedyre til å gjennomgå lastlinjene, og juster for å sikre at enheten og mengden justeres med desimalpresisjonen til enheten.</span><span class="sxs-lookup"><span data-stu-id="562b7-129">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="562b7-130">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="562b7-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="562b7-131">Velg lasten som følgeseddelen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="562b7-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="562b7-132">I hurtigfanen **Lastlinjer** velger du lastlinjen for varen som forårsaker problemet.</span><span class="sxs-lookup"><span data-stu-id="562b7-132">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="562b7-133">Noter verdien i feltene **Antall** og **Enhet**.</span><span class="sxs-lookup"><span data-stu-id="562b7-133">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="562b7-134">Gå til **Organisasjonsstyring \> Enheter \> Enheter**.</span><span class="sxs-lookup"><span data-stu-id="562b7-134">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="562b7-135">Velg enheten som følgeseddelen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="562b7-135">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="562b7-136">Juster verdien i feltet **Desimalpresisjon** etter behov.</span><span class="sxs-lookup"><span data-stu-id="562b7-136">Adjust the value of the **Decimal precision** field as required.</span></span>
