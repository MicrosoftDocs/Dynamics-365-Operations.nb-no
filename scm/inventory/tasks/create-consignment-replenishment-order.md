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
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 6286e8f52b8131a8e4779f1e11d84233b8e0760e
ms.contentlocale: nb-no
ms.lasthandoff: 09/12/2017

---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="4b770-103">Opprette en ny etterfyllingsordre for forsendelse</span><span class="sxs-lookup"><span data-stu-id="4b770-103">Create a consignment replenishment order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4b770-104">Denne fremgangsmåten viser hvordan du oppretter en etterfyllingsordre for forsendelse der du kan spore forventet levering fra en leverandør til forsendelseslageret.</span><span class="sxs-lookup"><span data-stu-id="4b770-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="4b770-105">Den viser også hvordan du registrerer et mottak av produkter slik at forsendelseslageret registreres som tilgjengelig lagerbeholdning eid av leverandøren.</span><span class="sxs-lookup"><span data-stu-id="4b770-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="4b770-106">Dette gjøres vanligvis av en innkjøpansvarlig.</span><span class="sxs-lookup"><span data-stu-id="4b770-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="4b770-107">Du kan bruke denne veiledningen i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="4b770-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="4b770-108">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="4b770-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="4b770-109">Opprette en ny etterfyllingsordre for forsendelse</span><span class="sxs-lookup"><span data-stu-id="4b770-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="4b770-110">Gå til Innkjøp og leverandører > Forsendelse > Etterfyllingsordrer for forsendelse.</span><span class="sxs-lookup"><span data-stu-id="4b770-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="4b770-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4b770-111">Click New.</span></span>
3. <span data-ttu-id="4b770-112">Angi leverandøren US-104 i Leverandørkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b770-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="4b770-113">Du må velge en leverandør som er registrert som eier på siden Beholdningseiere.</span><span class="sxs-lookup"><span data-stu-id="4b770-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="4b770-114">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4b770-114">Click OK.</span></span>
5. <span data-ttu-id="4b770-115">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="4b770-115">Click Add line.</span></span>
6. <span data-ttu-id="4b770-116">Skriv inn M9211CI i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b770-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="4b770-117">Du må velge en vare som er definert for forsendelseslager.</span><span class="sxs-lookup"><span data-stu-id="4b770-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="4b770-118">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="4b770-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="4b770-119">Angi en dato i feltet Ønsket leveringsdato.</span><span class="sxs-lookup"><span data-stu-id="4b770-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="4b770-120">Ønskede og bekreftede datoer brukes av MRP-motoren for den forventede ankomsten av varene.</span><span class="sxs-lookup"><span data-stu-id="4b770-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="4b770-121">Angi en dato i Bekreftet leveringsdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b770-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="4b770-122">Vis seksjonen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="4b770-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="4b770-123">Klikk kategorien Lagerdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="4b770-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="4b770-124">Hvis du vil vise eieren i feltet Lagerdimensjonseier, må du oppdatere siden.</span><span class="sxs-lookup"><span data-stu-id="4b770-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="4b770-125">Leverandør US-104 er nå oppført som eier.</span><span class="sxs-lookup"><span data-stu-id="4b770-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="4b770-126">Kontrollere lagertransaksjonsstatusen</span><span class="sxs-lookup"><span data-stu-id="4b770-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="4b770-127">Klikk Lager.</span><span class="sxs-lookup"><span data-stu-id="4b770-127">Click Inventory.</span></span>
2. <span data-ttu-id="4b770-128">Klikk Transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="4b770-128">Click Transactions.</span></span>
3. <span data-ttu-id="4b770-129">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4b770-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4b770-130">Legg merke til at Mottak-feltet er satt til Bestilt.</span><span class="sxs-lookup"><span data-stu-id="4b770-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="4b770-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4b770-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="4b770-132">Motta varer</span><span class="sxs-lookup"><span data-stu-id="4b770-132">Receive items</span></span>
1. <span data-ttu-id="4b770-133">Klikk Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="4b770-133">Click Product receipt.</span></span>
2. <span data-ttu-id="4b770-134">Skriv inn en verdi i feltet Ekstern mottaksseddel.</span><span class="sxs-lookup"><span data-stu-id="4b770-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="4b770-135">I Antall-feltet skriver du inn et tall som er lavere enn antallet som vises.</span><span class="sxs-lookup"><span data-stu-id="4b770-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span>
4. <span data-ttu-id="4b770-136">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4b770-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="4b770-137">Kontrollere lagerbeholdningen</span><span class="sxs-lookup"><span data-stu-id="4b770-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="4b770-138">Klikk Lager.</span><span class="sxs-lookup"><span data-stu-id="4b770-138">Click Inventory.</span></span>
2. <span data-ttu-id="4b770-139">Klikk På lager.</span><span class="sxs-lookup"><span data-stu-id="4b770-139">Click On-hand.</span></span>
3. <span data-ttu-id="4b770-140">Klikk Oversikt.</span><span class="sxs-lookup"><span data-stu-id="4b770-140">Click Overview.</span></span>
    * <span data-ttu-id="4b770-141">Varene som er mottatt som forsendelseslager og som eies av leverandøren, er tilgjengelig lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="4b770-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="4b770-142">Restantall på etterfyllingsordren for forsendelsen vises i Bestilt i alt-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b770-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="4b770-143">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4b770-143">Close the page.</span></span>
5. <span data-ttu-id="4b770-144">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="4b770-144">Click Close.</span></span>

