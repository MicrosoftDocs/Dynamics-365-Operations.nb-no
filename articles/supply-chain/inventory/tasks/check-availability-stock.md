---
title: Kontrollere lagertilgjengeligheten
description: Denne fremgangsmåten viser hvordan du kontrollerer beholdning og fysisk lagerbeholdning for et bestemt varenummer.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26a8f51eda1f4249862a23fa0103b7a144d974a1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549888"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="0dcd9-103">Kontrollere lagertilgjengeligheten</span><span class="sxs-lookup"><span data-stu-id="0dcd9-103">Check the availability of stock</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0dcd9-104">Denne fremgangsmåten viser hvordan du kontrollerer beholdning og fysisk lagerbeholdning for et bestemt varenummer.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="0dcd9-105">Den viser også hvordan du henter forsyningsinformasjon som er knyttet til en vare.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="0dcd9-106">Fysisk lagerbeholdning er lagerbeholdningen som er tilgjengelig – det vil si den er kjøpt, mottatt og registrert.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-106">Physical on-hand inventory is the on-hand inventory that’s available – that is, it’s purchased, received and registered.</span></span> <span data-ttu-id="0dcd9-107">Lagerbeholdningen inkluderer den tilgjengelige lagerbeholdningen, men også lageret som er bestilt og forventet, men ennå ikke er mottatt eller registrert.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-107">On-hand inventory includes the available on-hand inventory, but also the inventory that’s been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="0dcd9-108">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="0dcd9-109">Hvis du bruker USMF, kan du bruke eksempelverdiene som vises.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="0dcd9-110">Disse oppgavene vil vanligvis utføres av en lagermedarbeider.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="0dcd9-111">Kontrollere lagerbeholdning for en vare</span><span class="sxs-lookup"><span data-stu-id="0dcd9-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="0dcd9-112">Gå til Lagerstyring > Forespørsler og rapporter > Lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-112">Go to Inventory management > Inquiries and reports > On-hand inventory.</span></span>
2. <span data-ttu-id="0dcd9-113">Velg varenummerraden.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-113">Select the Item number row.</span></span>
    * <span data-ttu-id="0dcd9-114">Hvis du vil spørre om lagerbeholdning etter varenummer, merker du raden der tabellen er satt til Lagerbeholdning og Felt er satt til Varenummer.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-114">To query the on-hand inventory by item number, select the row where the Table is set to On-hand inventory and Field is set to Item number.</span></span>  
3. <span data-ttu-id="0dcd9-115">Velg varen du vil utføre spørringer for, i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-115">In the Criteria field, select the item you want to query.</span></span>
    * <span data-ttu-id="0dcd9-116">Hvis du bruker demonstrasjonsdatafirmaet USMF, kan du velge M9201.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="0dcd9-117">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-117">Click OK.</span></span>
5. <span data-ttu-id="0dcd9-118">Klikk Dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-118">Click Dimensions.</span></span>
    * <span data-ttu-id="0dcd9-119">I kategorien Dimensjoner kan du velge hvor mange detaljer du vil se om lagerbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-119">The Dimensions tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="0dcd9-120">Hvis du trenger data som er relatert til reservering, må du vise alle lagerdimensjoner for varer som bruker avanserte lagerprosesser (WHS).</span><span class="sxs-lookup"><span data-stu-id="0dcd9-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WHS) processes.</span></span>  
6. <span data-ttu-id="0dcd9-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-121">Click OK.</span></span>
7. <span data-ttu-id="0dcd9-122">Klikk Relatert informasjon i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-122">On the Action Pane, click Related information.</span></span>
    * <span data-ttu-id="0dcd9-123">Hvis du ikke ser dette, må du kanskje klikke ellipseknappen (...) for å se alternativer for flere handlinger.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-123">If you don’t see this, you may need to click on the Ellipsis button (…) to see additional action pane options.</span></span>  
8. <span data-ttu-id="0dcd9-124">Klikk Forsyningsoversikt.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-124">Click Supply overview.</span></span>
    * <span data-ttu-id="0dcd9-125">Kategorien Forsyningsoversikt gir forsyningsinformasjonen for en bestemt vare, for eksempel antallet på lager, leveringstid og leverandørinformasjon.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-125">The Supply overview tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="0dcd9-126">Vis Beholdning-delen.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-126">Expand the On-hand section.</span></span>
10. <span data-ttu-id="0dcd9-127">Vis Leverandør-delen.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-127">Expand the Vendors section.</span></span>
11. <span data-ttu-id="0dcd9-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-128">Close the page.</span></span>
12. <span data-ttu-id="0dcd9-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="0dcd9-130">Kontrollere fysisk lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="0dcd9-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="0dcd9-131">Gå til Lagerstyring > Forespørsler og rapporter > Fysisk lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-131">Go to Warehouse management > Inquiries and reports > Physical on-hand inventory.</span></span>
2. <span data-ttu-id="0dcd9-132">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-132">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="0dcd9-133">Du kan bruke feltene Område og Lager til å filtrere listen over elementer.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-133">You can use the Site and Warehouse fields to filter the list of items.</span></span>  
3. <span data-ttu-id="0dcd9-134">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-134">Refresh the page.</span></span>
4. <span data-ttu-id="0dcd9-135">Klikk Visningsdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-135">Click Display Dimensions.</span></span>
    * <span data-ttu-id="0dcd9-136">I kategorien Dimensjonsvisning kan du velge hvor mange detaljer du vil se om lagerbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>  
5. <span data-ttu-id="0dcd9-137">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-137">Click OK.</span></span>
6. <span data-ttu-id="0dcd9-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="0dcd9-139">Kontrollere lagerbeholdning etter lokasjon</span><span class="sxs-lookup"><span data-stu-id="0dcd9-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="0dcd9-140">Gå til Lagerstyring > Forespørsler og rapporter > Beholdning etter lokasjon.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-140">Go to Warehouse management > Inquiries and reports > On hand by location.</span></span>
2. <span data-ttu-id="0dcd9-141">Skriv inn en verdi i Lager-feltet.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-141">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="0dcd9-142">Hvis du bruker demonstrasjonsdatafirmaet USMF, kan du bruke "51".</span><span class="sxs-lookup"><span data-stu-id="0dcd9-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="0dcd9-143">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-143">Refresh the page.</span></span>
4. <span data-ttu-id="0dcd9-144">Klikk Visningsdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-144">Click Display Dimensions.</span></span>
5. <span data-ttu-id="0dcd9-145">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-145">Click OK.</span></span>
6. <span data-ttu-id="0dcd9-146">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0dcd9-146">Close the page.</span></span>

