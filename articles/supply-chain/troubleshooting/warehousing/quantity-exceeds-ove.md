---
title: Du kan ikke bekrefte en forsendelse fordi antallet overskrider overleveringsprosenten
description: Du kan ikke bekrefte en forsendelse fordi antallet overskrider overleveringsprosenten
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c9b5ba8dedb927ee049d7e53e9a666902f563f49
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938528"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a><span data-ttu-id="da66d-103">Du kan ikke bekrefte en forsendelse fordi antallet overskrider overleveringsprosenten</span><span class="sxs-lookup"><span data-stu-id="da66d-103">You can't confirm a shipment because the quantity exceeds the overdelivery percentage</span></span>

<span data-ttu-id="da66d-104">Feilkode: WAX1687</span><span class="sxs-lookup"><span data-stu-id="da66d-104">Error code: WAX1687</span></span>

## <a name="symptoms"></a><span data-ttu-id="da66d-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="da66d-105">Symptoms</span></span>

<span data-ttu-id="da66d-106">Når du prøver å bekrefte en forsendelse, viser systemet følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="da66d-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="da66d-107">Forsendelsen for last %1 kan ikke bekreftes, fordi antallet for varen %2 overskrider prosenten som er definert for overlevering.</span><span class="sxs-lookup"><span data-stu-id="da66d-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for overdelivery.</span></span>

<span data-ttu-id="da66d-108">Derfor kan du ikke bekrefte forsendelsen for belastningen.</span><span class="sxs-lookup"><span data-stu-id="da66d-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="da66d-109">Årsak</span><span class="sxs-lookup"><span data-stu-id="da66d-109">Cause</span></span>

<span data-ttu-id="da66d-110">Antallet for lasten eller forsendelsen er bare delvis plukket.</span><span class="sxs-lookup"><span data-stu-id="da66d-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="da66d-111">Antallet overskrider det plukkede antallet med en prosent som er utenfor den tillatte overleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="da66d-111">The quantity currently exceeds the picked quantity by a percentage that is outside the allowed overdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="da66d-112">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="da66d-112">Resolution</span></span>

<span data-ttu-id="da66d-113">Du kan løse dette problemet ved å fullføre én eller flere av følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="da66d-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="da66d-114">Angi lastlinjeantallet.</span><span class="sxs-lookup"><span data-stu-id="da66d-114">Set the load line quantity.</span></span>
- <span data-ttu-id="da66d-115">Angi overleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="da66d-115">Set the overdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="da66d-116">Angi lastlinjeantallet</span><span class="sxs-lookup"><span data-stu-id="da66d-116">Set the load line quantity</span></span>

<span data-ttu-id="da66d-117">Følg denne fremgangsmåten for å angi lastlinjeantallet.</span><span class="sxs-lookup"><span data-stu-id="da66d-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="da66d-118">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="da66d-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="da66d-119">Velg belastningen som forsendelsen ikke kan bekreftes for.</span><span class="sxs-lookup"><span data-stu-id="da66d-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="da66d-120">I hurtigfanen **Lastlinjer** velger du lastlinjen for varen som overskrider overleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="da66d-120">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="da66d-121">I hurtigfanen **Linjedetaljer** velger du **Ordre**.</span><span class="sxs-lookup"><span data-stu-id="da66d-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="da66d-122">I **Antall**-feltet angir du verdien til det plukkede antallet (det vil si til verdien **Antall for arbeid opprettet**), slik at forsendelsesbekreftelse kan skje.</span><span class="sxs-lookup"><span data-stu-id="da66d-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-overdelivery-percentage"></a><span data-ttu-id="da66d-123">Angi overleveringsprosenten</span><span class="sxs-lookup"><span data-stu-id="da66d-123">Set the overdelivery percentage</span></span>

<span data-ttu-id="da66d-124">Følg denne fremgangsmåten for å angi underleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="da66d-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="da66d-125">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="da66d-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="da66d-126">Velg belastningen som forsendelsen ikke kan bekreftes for.</span><span class="sxs-lookup"><span data-stu-id="da66d-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="da66d-127">I hurtigfanen **Lastlinjer** velger du lastlinjen for varen som overskrider overleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="da66d-127">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="da66d-128">I hurtigfanen **Linjedetaljer** velger du **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="da66d-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="da66d-129">I **Overlevering**-feltet angir du verdien til en større prosent som legger til rette for antallet som er plukket mot lastantallet, slik at forsendelsesbekreftelsen kan skje.</span><span class="sxs-lookup"><span data-stu-id="da66d-129">In the **Overdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
