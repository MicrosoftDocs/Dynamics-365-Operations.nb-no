---
title: Opprette en ny etterfyllingsordre for forsendelse
description: Dette emnet forklarer hvordan du oppretter en etterfyllingsordre for forsendelse der du kan spore forventet levering fra en leverandør til forsendelseslageret.
author: sherry-zheng
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: chuzheng
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0d2030277e0810bebef9356136b0e11effc6d5b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834031"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="7c7e1-103">Opprette en ny etterfyllingsordre for forsendelse</span><span class="sxs-lookup"><span data-stu-id="7c7e1-103">Create a consignment replenishment order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7c7e1-104">Dette emnet forklarer hvordan du oppretter en etterfyllingsordre for forsendelse der du kan spore forventet levering fra en leverandør til forsendelseslageret.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-104">This topic explains how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="7c7e1-105">Den viser også hvordan du registrerer et mottak av produkter slik at forsendelseslageret registreres som tilgjengelig lagerbeholdning eid av leverandøren.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="7c7e1-106">Dette gjøres vanligvis av en innkjøpansvarlig.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="7c7e1-107">Du kan bruke denne veiledningen i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="7c7e1-108">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="7c7e1-109">Opprette en ny etterfyllingsordre for forsendelse</span><span class="sxs-lookup"><span data-stu-id="7c7e1-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="7c7e1-110">I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Forsendelse > Etterfyllingsordrer for forsendelse**.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-110">In the navigation pane, go to **Modules > Procurement and sourcing > Consignment > Consignment replenishment orders**.</span></span>
2. <span data-ttu-id="7c7e1-111">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-111">Select **New**.</span></span>
3. <span data-ttu-id="7c7e1-112">I **Leverandørkonto**-feltet velger du leverandør **US-104** (du må velge en leverandør som er registrert som en eier på **lagereiere**-siden).</span><span class="sxs-lookup"><span data-stu-id="7c7e1-112">In the **Vendor account** field, select vendor **US-104** (you must select a vendor that's registered as an owner in the **inventory owners** page).</span></span> 
4. <span data-ttu-id="7c7e1-113">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-113">Select **OK**.</span></span>
5. <span data-ttu-id="7c7e1-114">Velg **Legg til linje**.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-114">Select **Add line**.</span></span>
6. <span data-ttu-id="7c7e1-115">I **Varenummer**-feltet skriver du inn `M9211CI` (du må velge en vare som er definert for forsendelseslager).</span><span class="sxs-lookup"><span data-stu-id="7c7e1-115">In the **Item number** field, type `M9211CI` (you must select an item that is set up for consignment inventory).</span></span>
7. <span data-ttu-id="7c7e1-116">Angi et tall i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-116">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="7c7e1-117">Angi en dato i feltet **Ønsket leveringsdato**.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-117">In the **Requested delivery date** field, enter a date.</span></span> <span data-ttu-id="7c7e1-118">Ønskede og bekreftede datoer brukes av MRP-motoren for den forventede ankomsten av varene.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-118">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="7c7e1-119">Angi en dato i feltet **Bekreftet leveringsdato**.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-119">In the **Confirmed delivery date** field, enter a date.</span></span>
10. <span data-ttu-id="7c7e1-120">Vis delen **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-120">Expand the **Line details** section.</span></span>
11. <span data-ttu-id="7c7e1-121">Velg fanen **Lagerdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-121">Select the **Inventory dimensions** tab.</span></span>
12. <span data-ttu-id="7c7e1-122">Hvis du vil vise eieren i feltet **Lagerdimensjonseier**, må du oppdatere siden.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-122">To show the owner in the **Inventory dimensions owner** field, refresh the page.</span></span> <span data-ttu-id="7c7e1-123">Leverandør US-104 er nå oppført som eier.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-123">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="7c7e1-124">Kontrollere lagertransaksjonsstatusen</span><span class="sxs-lookup"><span data-stu-id="7c7e1-124">Check the inventory transaction status</span></span>
1. <span data-ttu-id="7c7e1-125">Velg **Lager**.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-125">Select **Inventory**.</span></span>
2. <span data-ttu-id="7c7e1-126">Velg **Transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-126">Select **Transactions**.</span></span>
3. <span data-ttu-id="7c7e1-127">Legg merke til at **Mottak**-feltet er satt til **Bestilt** i den ønskede raden.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-127">In the desired row, notice that the **Receipt** field is set to **Ordered**.</span></span>  
4. <span data-ttu-id="7c7e1-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-128">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="7c7e1-129">Motta varer</span><span class="sxs-lookup"><span data-stu-id="7c7e1-129">Receive items</span></span>
1. <span data-ttu-id="7c7e1-130">Velg **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-130">Select **Product receipt**.</span></span>
2. <span data-ttu-id="7c7e1-131">Skriv inn en verdi i feltet **Ekstern mottaksseddel**.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-131">In the **External product receipt** field, type a value.</span></span>
3. <span data-ttu-id="7c7e1-132">I **Antall**-feltet skriver du inn et tall som er lavere enn antallet som vises.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-132">In the **Quantity** field, enter a number that's lower than the number that's shown there.</span></span> 
4. <span data-ttu-id="7c7e1-133">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-133">Select **OK**.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="7c7e1-134">Kontrollere lagerbeholdningen</span><span class="sxs-lookup"><span data-stu-id="7c7e1-134">Check the on-hand inventory</span></span>
1. <span data-ttu-id="7c7e1-135">Velg **Lager**.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="7c7e1-136">Velg **Beholdning**.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-136">Select **On-hand**.</span></span>
3. <span data-ttu-id="7c7e1-137">Velg **Oversikt**.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-137">Select **Overview**.</span></span> <span data-ttu-id="7c7e1-138">Varene som er mottatt som forsendelseslager og som eies av leverandøren, er tilgjengelig lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-138">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="7c7e1-139">Restantall på etterfyllingsordren for forsendelsen vises i feltet **Bestilt i alt**.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-139">The remaining quantity on the consignment replenishment order is shown in the **Ordered in total** field.</span></span>  
4. <span data-ttu-id="7c7e1-140">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-140">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]