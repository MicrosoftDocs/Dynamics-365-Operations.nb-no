---
title: Generere et overføringsdokument for en intern lageroverføring
description: Denne fremgangsmåten viser hvordan du oppretter overføringsdokumenter for flytting av varer i et selskap.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5cb0d3d51bf30717f05a4daf1a098565d5d48621
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143415"
---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a><span data-ttu-id="9dde9-103">Generere et overføringsdokument for en intern lageroverføring</span><span class="sxs-lookup"><span data-stu-id="9dde9-103">Generate a transfer document for an internal inventory transfer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9dde9-104">Denne fremgangsmåten viser hvordan du oppretter overføringsdokumenter for flytting av varer i et selskap.</span><span class="sxs-lookup"><span data-stu-id="9dde9-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="9dde9-105">Denne fremgangsmåten er bare tilgjengelig for juridiske enheter med hovedadresse i Litauen.</span><span class="sxs-lookup"><span data-stu-id="9dde9-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="9dde9-106">Prosedyren ble opprettet med demonstrasjonsdatafirmaet DEMF med en primæradresse i Litauen.</span><span class="sxs-lookup"><span data-stu-id="9dde9-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="9dde9-107">Før du kan fullføre denne prosedyren, må du fullføre fremgangsmåten Konfigurere overføringsdokumenter for flytting av varer i et selskap.</span><span class="sxs-lookup"><span data-stu-id="9dde9-107">Before you can complete this procedure, you must complete the "Set up transfer documents for goods movement inside a company" procedure.</span></span> <span data-ttu-id="9dde9-108">Denne prosedyren er ment for lagerregnskapsførere.</span><span class="sxs-lookup"><span data-stu-id="9dde9-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="9dde9-109">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="9dde9-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="9dde9-110">Opprett overføringsordre</span><span class="sxs-lookup"><span data-stu-id="9dde9-110">Create a transfer order</span></span>
1. <span data-ttu-id="9dde9-111">Gå til Lagerstyring > Innkommende ordrer > Overføringsordre.</span><span class="sxs-lookup"><span data-stu-id="9dde9-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="9dde9-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9dde9-112">Click New.</span></span>
3. <span data-ttu-id="9dde9-113">Angi eller velg en verdi i feltet Fra lager.</span><span class="sxs-lookup"><span data-stu-id="9dde9-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="9dde9-114">Angi eller velg en verdi i feltet Til lager.</span><span class="sxs-lookup"><span data-stu-id="9dde9-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="9dde9-115">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="9dde9-115">Click Add.</span></span>
6. <span data-ttu-id="9dde9-116">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9dde9-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="9dde9-117">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="9dde9-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="9dde9-118">Angi transportdetaljer for overføringsordren</span><span class="sxs-lookup"><span data-stu-id="9dde9-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="9dde9-119">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9dde9-119">Click Save.</span></span>
2. <span data-ttu-id="9dde9-120">Klikk Send i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9dde9-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="9dde9-121">Klikk Transportdetaljer.</span><span class="sxs-lookup"><span data-stu-id="9dde9-121">Click Transportation details.</span></span>
4. <span data-ttu-id="9dde9-122">Velg Ja i feltet Skriv ut transportdetaljer.</span><span class="sxs-lookup"><span data-stu-id="9dde9-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="9dde9-123">Angi eller velg en verdi i feltet Utstedte varer.</span><span class="sxs-lookup"><span data-stu-id="9dde9-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="9dde9-124">Skriv inn en verdi i feltet Pakke.</span><span class="sxs-lookup"><span data-stu-id="9dde9-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="9dde9-125">Skriv inn en verdi i feltet Risikonivå for lasten.</span><span class="sxs-lookup"><span data-stu-id="9dde9-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="9dde9-126">Angi eller velg en verdi i feltet Transportør.</span><span class="sxs-lookup"><span data-stu-id="9dde9-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="9dde9-127">Angi eller velg en verdi i feltet Modell.</span><span class="sxs-lookup"><span data-stu-id="9dde9-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="9dde9-128">Skriv inn en verdi i feltet Registreringsnummer.</span><span class="sxs-lookup"><span data-stu-id="9dde9-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="9dde9-129">Skriv inn en verdi i feltet Registreringsnummer for lastebil</span><span class="sxs-lookup"><span data-stu-id="9dde9-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="9dde9-130">Angi eller velg en verdi i feltet Sjåfør.</span><span class="sxs-lookup"><span data-stu-id="9dde9-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="9dde9-131">Skriv inn en verdi i feltet for sjåførnavn.</span><span class="sxs-lookup"><span data-stu-id="9dde9-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="9dde9-132">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9dde9-132">Click Save.</span></span>
15. <span data-ttu-id="9dde9-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9dde9-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="9dde9-134">Vise følgeseddelen for den uposterte overføringsordren</span><span class="sxs-lookup"><span data-stu-id="9dde9-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="9dde9-135">Klikk Følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="9dde9-135">Click Packing slip.</span></span>
2. <span data-ttu-id="9dde9-136">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9dde9-136">Click OK.</span></span>
3. <span data-ttu-id="9dde9-137">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9dde9-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="9dde9-138">Vise følgeseddelen for den posterte overføringsordren</span><span class="sxs-lookup"><span data-stu-id="9dde9-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="9dde9-139">Klikk Overføringsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9dde9-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="9dde9-140">Klikk Send i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9dde9-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="9dde9-141">Klikk Send overføringsordre.</span><span class="sxs-lookup"><span data-stu-id="9dde9-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="9dde9-142">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="9dde9-142">Click the General tab.</span></span>
5. <span data-ttu-id="9dde9-143">Velg et alternativ i feltet Oppdater.</span><span class="sxs-lookup"><span data-stu-id="9dde9-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="9dde9-144">Klikk kategorien Oversikt.</span><span class="sxs-lookup"><span data-stu-id="9dde9-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="9dde9-145">Skriv inn en verdi i Følgeseddel-feltet.</span><span class="sxs-lookup"><span data-stu-id="9dde9-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="9dde9-146">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9dde9-146">Click OK.</span></span>
9. <span data-ttu-id="9dde9-147">Klikk Send i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9dde9-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="9dde9-148">Klikk Følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="9dde9-148">Click Packing slip.</span></span>
11. <span data-ttu-id="9dde9-149">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9dde9-149">Click OK.</span></span>

