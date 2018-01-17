---
title: Opprette en ny etterfyllingsordre for forsendelse
description: "Denne fremgangsmåten viser hvordan du oppretter en etterfyllingsordre for forsendelse der du kan spore forventet levering fra en leverandør til forsendelseslageret."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: c9d142e50d39f9e98adeef170da93b8137de4131
ms.contentlocale: nb-no
ms.lasthandoff: 01/17/2018

---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="94027-103">Opprette en ny etterfyllingsordre for forsendelse</span><span class="sxs-lookup"><span data-stu-id="94027-103">Create a consignment replenishment order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="94027-104">Denne fremgangsmåten viser hvordan du oppretter en etterfyllingsordre for forsendelse der du kan spore forventet levering fra en leverandør til forsendelseslageret.</span><span class="sxs-lookup"><span data-stu-id="94027-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="94027-105">Den viser også hvordan du registrerer et mottak av produkter slik at forsendelseslageret registreres som tilgjengelig lagerbeholdning eid av leverandøren.</span><span class="sxs-lookup"><span data-stu-id="94027-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="94027-106">Dette gjøres vanligvis av en innkjøpansvarlig.</span><span class="sxs-lookup"><span data-stu-id="94027-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="94027-107">Du kan bruke denne veiledningen i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="94027-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="94027-108">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="94027-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="94027-109">Opprette en ny etterfyllingsordre for forsendelse</span><span class="sxs-lookup"><span data-stu-id="94027-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="94027-110">Gå til Innkjøp og leverandører > Forsendelse > Etterfyllingsordrer for forsendelse.</span><span class="sxs-lookup"><span data-stu-id="94027-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="94027-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="94027-111">Click New.</span></span>
3. <span data-ttu-id="94027-112">Angi leverandøren US-104 i Leverandørkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="94027-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="94027-113">Du må velge en leverandør som er registrert som eier på siden Beholdningseiere.</span><span class="sxs-lookup"><span data-stu-id="94027-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="94027-114">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="94027-114">Click OK.</span></span>
5. <span data-ttu-id="94027-115">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="94027-115">Click Add line.</span></span>
6. <span data-ttu-id="94027-116">Skriv inn M9211CI i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="94027-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="94027-117">Du må velge en vare som er definert for forsendelseslager.</span><span class="sxs-lookup"><span data-stu-id="94027-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="94027-118">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="94027-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="94027-119">Angi en dato i feltet Ønsket leveringsdato.</span><span class="sxs-lookup"><span data-stu-id="94027-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="94027-120">Ønskede og bekreftede datoer brukes av MRP-motoren for den forventede ankomsten av varene.</span><span class="sxs-lookup"><span data-stu-id="94027-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="94027-121">Angi en dato i Bekreftet leveringsdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="94027-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="94027-122">Vis seksjonen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="94027-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="94027-123">Klikk kategorien Lagerdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="94027-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="94027-124">Hvis du vil vise eieren i feltet Lagerdimensjonseier, må du oppdatere siden.</span><span class="sxs-lookup"><span data-stu-id="94027-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="94027-125">Leverandør US-104 er nå oppført som eier.</span><span class="sxs-lookup"><span data-stu-id="94027-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="94027-126">Kontrollere lagertransaksjonsstatusen</span><span class="sxs-lookup"><span data-stu-id="94027-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="94027-127">Klikk Lager.</span><span class="sxs-lookup"><span data-stu-id="94027-127">Click Inventory.</span></span>
2. <span data-ttu-id="94027-128">Klikk Transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="94027-128">Click Transactions.</span></span>
3. <span data-ttu-id="94027-129">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="94027-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="94027-130">Legg merke til at Mottak-feltet er satt til Bestilt.</span><span class="sxs-lookup"><span data-stu-id="94027-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="94027-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="94027-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="94027-132">Motta varer</span><span class="sxs-lookup"><span data-stu-id="94027-132">Receive items</span></span>
1. <span data-ttu-id="94027-133">Klikk Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="94027-133">Click Product receipt.</span></span>
2. <span data-ttu-id="94027-134">Skriv inn en verdi i feltet Ekstern mottaksseddel.</span><span class="sxs-lookup"><span data-stu-id="94027-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="94027-135">I Antall-feltet skriver du inn et tall som er lavere enn antallet som vises.</span><span class="sxs-lookup"><span data-stu-id="94027-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span>
4. <span data-ttu-id="94027-136">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="94027-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="94027-137">Kontrollere lagerbeholdningen</span><span class="sxs-lookup"><span data-stu-id="94027-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="94027-138">Klikk Lager.</span><span class="sxs-lookup"><span data-stu-id="94027-138">Click Inventory.</span></span>
2. <span data-ttu-id="94027-139">Klikk På lager.</span><span class="sxs-lookup"><span data-stu-id="94027-139">Click On-hand.</span></span>
3. <span data-ttu-id="94027-140">Klikk Oversikt.</span><span class="sxs-lookup"><span data-stu-id="94027-140">Click Overview.</span></span>
    * <span data-ttu-id="94027-141">Varene som er mottatt som forsendelseslager og som eies av leverandøren, er tilgjengelig lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="94027-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="94027-142">Restantall på etterfyllingsordren for forsendelsen vises i Bestilt i alt-feltet.</span><span class="sxs-lookup"><span data-stu-id="94027-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="94027-143">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="94027-143">Close the page.</span></span>
5. <span data-ttu-id="94027-144">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="94027-144">Click Close.</span></span>

