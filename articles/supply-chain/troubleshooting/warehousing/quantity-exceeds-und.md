---
title: Du kan ikke bekrefte en forsendelse fordi antallet overskrider underleveringsprosenten
description: Du kan ikke bekrefte en forsendelse fordi antallet overskrider underleveringsprosenten
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm,WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 625003731485329b93f5f9454ccece580c889613
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123825"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a><span data-ttu-id="bb93d-103">Du kan ikke bekrefte en forsendelse fordi antallet overskrider underleveringsprosenten</span><span class="sxs-lookup"><span data-stu-id="bb93d-103">You can't confirm a shipment because the quantity exceeds the underdelivery percentage</span></span>

<span data-ttu-id="bb93d-104">Feilkode: WAX1686</span><span class="sxs-lookup"><span data-stu-id="bb93d-104">Error code: WAX1686</span></span>

## <a name="symptoms"></a><span data-ttu-id="bb93d-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="bb93d-105">Symptoms</span></span>

<span data-ttu-id="bb93d-106">Når du prøver å bekrefte en forsendelse, viser systemet følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="bb93d-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="bb93d-107">Forsendelsen for last %1 kan ikke bekreftes, fordi antallet for varen %2 overskrider prosenten som er definert for underlevering.</span><span class="sxs-lookup"><span data-stu-id="bb93d-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for underdelivery.</span></span>

<span data-ttu-id="bb93d-108">Derfor kan du ikke bekrefte forsendelsen for belastningen.</span><span class="sxs-lookup"><span data-stu-id="bb93d-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="bb93d-109">Årsak</span><span class="sxs-lookup"><span data-stu-id="bb93d-109">Cause</span></span>

<span data-ttu-id="bb93d-110">Antallet for lasten eller forsendelsen er bare delvis plukket.</span><span class="sxs-lookup"><span data-stu-id="bb93d-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="bb93d-111">Antallet er under det plukkede antallet med en prosent som er utenfor den tillatte underleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="bb93d-111">The quantity is currently less than the picked quantity by a percentage that is outside the allowed underdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="bb93d-112">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="bb93d-112">Resolution</span></span>

<span data-ttu-id="bb93d-113">Du kan løse dette problemet ved å fullføre én eller flere av følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="bb93d-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="bb93d-114">Angi lastlinjeantallet.</span><span class="sxs-lookup"><span data-stu-id="bb93d-114">Set the load line quantity.</span></span>
- <span data-ttu-id="bb93d-115">Angi underleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="bb93d-115">Set the underdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="bb93d-116">Angi lastlinjeantallet</span><span class="sxs-lookup"><span data-stu-id="bb93d-116">Set the load line quantity</span></span>

<span data-ttu-id="bb93d-117">Følg denne fremgangsmåten for å angi lastlinjeantallet.</span><span class="sxs-lookup"><span data-stu-id="bb93d-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="bb93d-118">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="bb93d-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="bb93d-119">Velg belastningen som forsendelsen ikke kan bekreftes for.</span><span class="sxs-lookup"><span data-stu-id="bb93d-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="bb93d-120">I hurtigfanen **Lastlinjer** velger du lastlinjen for varen som overskrider underleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="bb93d-120">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="bb93d-121">I hurtigfanen **Linjedetaljer** velger du **Ordre**.</span><span class="sxs-lookup"><span data-stu-id="bb93d-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="bb93d-122">I **Antall**-feltet angir du verdien til det plukkede antallet (det vil si til verdien **Antall for arbeid opprettet**), slik at forsendelsesbekreftelse kan skje.</span><span class="sxs-lookup"><span data-stu-id="bb93d-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-underdelivery-percentage"></a><span data-ttu-id="bb93d-123">Angi underleveringsprosenten</span><span class="sxs-lookup"><span data-stu-id="bb93d-123">Set the underdelivery percentage</span></span>

<span data-ttu-id="bb93d-124">Følg denne fremgangsmåten for å angi underleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="bb93d-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="bb93d-125">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="bb93d-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="bb93d-126">Velg belastningen som forsendelsen ikke kan bekreftes for.</span><span class="sxs-lookup"><span data-stu-id="bb93d-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="bb93d-127">I hurtigfanen **Lastlinjer** velger du lastlinjen for varen som overskrider underleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="bb93d-127">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="bb93d-128">I hurtigfanen **Linjedetaljer** velger du **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="bb93d-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="bb93d-129">I **Underlevering**-feltet angir du verdien til en større prosent som legger til rette for antallet som er plukket mot lastantallet, slik at forsendelsesbekreftelsen kan skje.</span><span class="sxs-lookup"><span data-stu-id="bb93d-129">In the **Underdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
