--- 
title: "Definere transportører"
description: "Denne prosedyren viser hvordan du konfigurerer en transportør og definere operasjoner, for eksempel service, forsendelsesmåte, transportbetalingsmiddel, transportbegrensninger og forsendelsessats."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e27be049bebd63c9266029b8981874417a9f0a8c
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="06f08-103">Definere transportører</span><span class="sxs-lookup"><span data-stu-id="06f08-103">Set up shipping carriers</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="06f08-104">Denne prosedyren viser hvordan du konfigurerer en transportør og definere operasjoner, for eksempel service, forsendelsesmåte, transportbetalingsmiddel, transportbegrensninger og forsendelsessats.</span><span class="sxs-lookup"><span data-stu-id="06f08-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="06f08-105">En transportkoordinator kan deretter tilordne en transportør til en innkommende eller utgående last.</span><span class="sxs-lookup"><span data-stu-id="06f08-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="06f08-106">Opprett en ny transportør</span><span class="sxs-lookup"><span data-stu-id="06f08-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="06f08-107">Gå til Transportstyring > Oppsett > Transportører > Transportører.</span><span class="sxs-lookup"><span data-stu-id="06f08-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="06f08-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="06f08-108">Click New.</span></span>
3. <span data-ttu-id="06f08-109">Skriv inn en verdi i Transportør-feltet.</span><span class="sxs-lookup"><span data-stu-id="06f08-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="06f08-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="06f08-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="06f08-111">Klikk rullegardinknappen i Modus-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="06f08-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="06f08-112">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="06f08-113">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="06f08-114">Fyll ut generell informasjon om transportøren</span><span class="sxs-lookup"><span data-stu-id="06f08-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="06f08-115">Aktiver/deaktiver utvidelsen av delen Oversikt.</span><span class="sxs-lookup"><span data-stu-id="06f08-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="06f08-116">Merk eller fjern merket for Aktiver transportør.</span><span class="sxs-lookup"><span data-stu-id="06f08-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="06f08-117">Klikk rullegardinknappen i feltet Leverandør for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="06f08-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="06f08-118">Velg leverandørkontoen som transportøren skal tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="06f08-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="06f08-119">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="06f08-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="06f08-121">Velg et alternativ i feltet Transportbetalingsmiddel.</span><span class="sxs-lookup"><span data-stu-id="06f08-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="06f08-122">Velg Manuell for å bruke siden Transportbetalingsmiddel, eller velg EDI for å oppdatere betalingsmiddelet ved hjelp av utveksling av elektroniske data (EDI – Electronic Data Interchange).</span><span class="sxs-lookup"><span data-stu-id="06f08-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="06f08-123">Merk eller fjern merket for Aktiver transportørrangering.</span><span class="sxs-lookup"><span data-stu-id="06f08-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="06f08-124">Opprett de nødvendige tjenestene for transportøren</span><span class="sxs-lookup"><span data-stu-id="06f08-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="06f08-125">Aktiver/deaktiver utvidelsen av delen Tjenester.</span><span class="sxs-lookup"><span data-stu-id="06f08-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="06f08-126">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="06f08-126">Click New.</span></span>
3. <span data-ttu-id="06f08-127">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="06f08-128">Skriv inn en verdi i Transportørtjeneste-feltet.</span><span class="sxs-lookup"><span data-stu-id="06f08-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="06f08-129">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="06f08-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="06f08-130">Klikk rullegardinknappen i feltet Transportmetode for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="06f08-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="06f08-131">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="06f08-132">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="06f08-133">Definer adressen for transportør (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="06f08-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="06f08-134">Aktiver/deaktiver utvidelsen av delen Adresser.</span><span class="sxs-lookup"><span data-stu-id="06f08-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="06f08-135">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="06f08-135">Click New.</span></span>
3. <span data-ttu-id="06f08-136">Skriv inn en verdi i feltet Navn eller beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="06f08-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="06f08-137">Klikk rullegardinknappen i feltet Land/område for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="06f08-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="06f08-138">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="06f08-139">Klikk rullegardinknappen i feltet Postnummer for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="06f08-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="06f08-140">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="06f08-141">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="06f08-142">Skriv inn en verdi i Gate-feltet.</span><span class="sxs-lookup"><span data-stu-id="06f08-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="06f08-143">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="06f08-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="06f08-144">Definer vurderingsprofilen for transportøren</span><span class="sxs-lookup"><span data-stu-id="06f08-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="06f08-145">Aktiver/deaktiver utvidelsen av delen Vurderingsprofiler.</span><span class="sxs-lookup"><span data-stu-id="06f08-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="06f08-146">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="06f08-146">Click New.</span></span>
3. <span data-ttu-id="06f08-147">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="06f08-148">Skriv inn en verdi i feltet Vurderingsprofil.</span><span class="sxs-lookup"><span data-stu-id="06f08-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="06f08-149">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="06f08-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="06f08-150">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="06f08-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="06f08-151">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="06f08-152">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="06f08-153">Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="06f08-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="06f08-154">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="06f08-155">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="06f08-156">Klikk rullegardinknappen i feltet Ratemotor for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="06f08-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="06f08-157">Velg ratemotoren som er i samsvar med kontrakten du har med transportøren.</span><span class="sxs-lookup"><span data-stu-id="06f08-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="06f08-158">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="06f08-159">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="06f08-160">Klikk rullegardinknappen i feltet Vurderingsstandard for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="06f08-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="06f08-161">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="06f08-162">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="06f08-163">Klikk rullegardinknappen i feltet Transittidmotor for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="06f08-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="06f08-164">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="06f08-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="06f08-165">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="06f08-165">Click Save.</span></span>


