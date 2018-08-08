--- 
title: "Definere transportører"
description: "Denne prosedyren viser hvordan du konfigurerer en transportør og definere operasjoner, for eksempel service, forsendelsesmåte, transportbetalingsmiddel, transportbegrensninger og forsendelsessats."
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 6c5ac13d17c97f20ee79e7faf57c570f02158424
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="f48b7-103">Definere transportører</span><span class="sxs-lookup"><span data-stu-id="f48b7-103">Set up shipping carriers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f48b7-104">Denne prosedyren viser hvordan du konfigurerer en transportør og definere operasjoner, for eksempel service, forsendelsesmåte, transportbetalingsmiddel, transportbegrensninger og forsendelsessats.</span><span class="sxs-lookup"><span data-stu-id="f48b7-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="f48b7-105">En transportkoordinator kan deretter tilordne en transportør til en innkommende eller utgående last.</span><span class="sxs-lookup"><span data-stu-id="f48b7-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="f48b7-106">Opprett en ny transportør</span><span class="sxs-lookup"><span data-stu-id="f48b7-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="f48b7-107">Gå til Transportstyring > Oppsett > Transportører > Transportører.</span><span class="sxs-lookup"><span data-stu-id="f48b7-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="f48b7-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f48b7-108">Click New.</span></span>
3. <span data-ttu-id="f48b7-109">Skriv inn en verdi i Transportør-feltet.</span><span class="sxs-lookup"><span data-stu-id="f48b7-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="f48b7-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f48b7-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f48b7-111">Klikk rullegardinknappen i Modus-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f48b7-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f48b7-112">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f48b7-113">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="f48b7-114">Fyll ut generell informasjon om transportøren</span><span class="sxs-lookup"><span data-stu-id="f48b7-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="f48b7-115">Aktiver/deaktiver utvidelsen av delen Oversikt.</span><span class="sxs-lookup"><span data-stu-id="f48b7-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="f48b7-116">Merk eller fjern merket for Aktiver transportør.</span><span class="sxs-lookup"><span data-stu-id="f48b7-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="f48b7-117">Klikk rullegardinknappen i feltet Leverandør for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f48b7-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f48b7-118">Velg leverandørkontoen som transportøren skal tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="f48b7-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="f48b7-119">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f48b7-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f48b7-121">Velg et alternativ i feltet Transportbetalingsmiddel.</span><span class="sxs-lookup"><span data-stu-id="f48b7-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="f48b7-122">Velg Manuell for å bruke siden Transportbetalingsmiddel, eller velg EDI for å oppdatere betalingsmiddelet ved hjelp av utveksling av elektroniske data (EDI – Electronic Data Interchange).</span><span class="sxs-lookup"><span data-stu-id="f48b7-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="f48b7-123">Merk eller fjern merket for Aktiver transportørrangering.</span><span class="sxs-lookup"><span data-stu-id="f48b7-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="f48b7-124">Opprett de nødvendige tjenestene for transportøren</span><span class="sxs-lookup"><span data-stu-id="f48b7-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="f48b7-125">Aktiver/deaktiver utvidelsen av delen Tjenester.</span><span class="sxs-lookup"><span data-stu-id="f48b7-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="f48b7-126">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f48b7-126">Click New.</span></span>
3. <span data-ttu-id="f48b7-127">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f48b7-128">Skriv inn en verdi i Transportørtjeneste-feltet.</span><span class="sxs-lookup"><span data-stu-id="f48b7-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="f48b7-129">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f48b7-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="f48b7-130">Klikk rullegardinknappen i feltet Transportmetode for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f48b7-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f48b7-131">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="f48b7-132">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="f48b7-133">Definer adressen for transportør (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="f48b7-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="f48b7-134">Aktiver/deaktiver utvidelsen av delen Adresser.</span><span class="sxs-lookup"><span data-stu-id="f48b7-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="f48b7-135">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f48b7-135">Click New.</span></span>
3. <span data-ttu-id="f48b7-136">Skriv inn en verdi i feltet Navn eller beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f48b7-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="f48b7-137">Klikk rullegardinknappen i feltet Land/område for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f48b7-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f48b7-138">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f48b7-139">Klikk rullegardinknappen i feltet Postnummer for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f48b7-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f48b7-140">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="f48b7-141">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f48b7-142">Skriv inn en verdi i Gate-feltet.</span><span class="sxs-lookup"><span data-stu-id="f48b7-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="f48b7-143">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f48b7-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="f48b7-144">Definer vurderingsprofilen for transportøren</span><span class="sxs-lookup"><span data-stu-id="f48b7-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="f48b7-145">Aktiver/deaktiver utvidelsen av delen Vurderingsprofiler.</span><span class="sxs-lookup"><span data-stu-id="f48b7-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="f48b7-146">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f48b7-146">Click New.</span></span>
3. <span data-ttu-id="f48b7-147">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f48b7-148">Skriv inn en verdi i feltet Vurderingsprofil.</span><span class="sxs-lookup"><span data-stu-id="f48b7-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="f48b7-149">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f48b7-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="f48b7-150">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f48b7-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f48b7-151">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="f48b7-152">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f48b7-153">Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f48b7-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="f48b7-154">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="f48b7-155">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="f48b7-156">Klikk rullegardinknappen i feltet Ratemotor for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f48b7-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f48b7-157">Velg ratemotoren som er i samsvar med kontrakten du har med transportøren.</span><span class="sxs-lookup"><span data-stu-id="f48b7-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="f48b7-158">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="f48b7-159">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="f48b7-160">Klikk rullegardinknappen i feltet Vurderingsstandard for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f48b7-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="f48b7-161">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="f48b7-162">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="f48b7-163">Klikk rullegardinknappen i feltet Transittidmotor for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f48b7-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="f48b7-164">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f48b7-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="f48b7-165">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f48b7-165">Click Save.</span></span>


