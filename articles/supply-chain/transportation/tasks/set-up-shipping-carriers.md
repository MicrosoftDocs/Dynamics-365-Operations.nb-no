---
title: Definere transportører
description: Dette emnet viser hvordan du konfigurerer en transportør og definere operasjoner, for eksempel service, forsendelsesmåte, transportbetalingsmiddel, transportbegrensninger og forsendelsessats.
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1ec19288f01ceb0bb3021cf549af1c38746785c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233589"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="d3830-103">Definere transportører</span><span class="sxs-lookup"><span data-stu-id="d3830-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d3830-104">Dette emnet viser hvordan du konfigurerer en transportør og definere operasjoner, for eksempel service, forsendelsesmåte, transportbetalingsmiddel, transportbegrensninger og forsendelsessats.</span><span class="sxs-lookup"><span data-stu-id="d3830-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="d3830-105">En transportkoordinator kan deretter tilordne en transportør til en innkommende eller utgående last.</span><span class="sxs-lookup"><span data-stu-id="d3830-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="d3830-106">Opprett en ny transportør</span><span class="sxs-lookup"><span data-stu-id="d3830-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="d3830-107">Gå til **Navigasjonsrute > Moduler > Transportstyring > Oppsett > Transportører > Transportører**.</span><span class="sxs-lookup"><span data-stu-id="d3830-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="d3830-108">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d3830-108">Select **New** on the Action Pane.</span></span>
3. <span data-ttu-id="d3830-109">Skriv inn en verdi i **Transportør**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3830-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="d3830-110">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3830-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="d3830-111">I **Modus**-feltet velger du et alternativ fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="d3830-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="d3830-112">Fyll ut generell informasjon om transportøren</span><span class="sxs-lookup"><span data-stu-id="d3830-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="d3830-113">Aktiver/deaktiver utvidelsen av delen **Oversikt**.</span><span class="sxs-lookup"><span data-stu-id="d3830-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="d3830-114">Merk eller fjern merket for **Aktiver transportør**.</span><span class="sxs-lookup"><span data-stu-id="d3830-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="d3830-115">I **Leverandørnummer**-feltet velger du et alternativ fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="d3830-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="d3830-116">Velg leverandørkontoen som transportøren skal tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="d3830-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="d3830-117">Velg et alternativ i feltet **Transportbetalingsmiddel**.</span><span class="sxs-lookup"><span data-stu-id="d3830-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="d3830-118">Velg **Manuell** for å bruke siden Transportbetalingsmiddel, eller velg **EDI** for å oppdatere betalingsmiddelet ved hjelp av utveksling av elektroniske data (EDI – Electronic Data Interchange).</span><span class="sxs-lookup"><span data-stu-id="d3830-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="d3830-119">Merk eller fjern merket for **Aktiver transportørrangering**.</span><span class="sxs-lookup"><span data-stu-id="d3830-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="d3830-120">Opprett de nødvendige tjenestene for transportøren</span><span class="sxs-lookup"><span data-stu-id="d3830-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="d3830-121">Aktiver/deaktiver utvidelsen av delen **Tjenester**.</span><span class="sxs-lookup"><span data-stu-id="d3830-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="d3830-122">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d3830-122">Select **New**.</span></span>
3. <span data-ttu-id="d3830-123">Skriv inn en verdi i **Transportørtjeneste**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3830-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="d3830-124">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3830-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="d3830-125">I **Transportmetode**-feltet velger du et alternativ fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="d3830-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="d3830-126">Definer adressen for transportør (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="d3830-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="d3830-127">Aktiver/deaktiver utvidelsen av delen **Adresser**.</span><span class="sxs-lookup"><span data-stu-id="d3830-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="d3830-128">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d3830-128">Select **New**.</span></span>
3. <span data-ttu-id="d3830-129">Skriv inn en verdi i feltet **Navn eller beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="d3830-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="d3830-130">I **Land/område**-feltet velger du et alternativ fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="d3830-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="d3830-131">I **Postnummer**-feltet velger du et alternativ fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="d3830-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="d3830-132">Skriv inn en verdi i **Gate**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3830-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="d3830-133">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d3830-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="d3830-134">Definer vurderingsprofilen for transportøren</span><span class="sxs-lookup"><span data-stu-id="d3830-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="d3830-135">Aktiver/deaktiver utvidelsen av delen **Vurderingsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="d3830-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="d3830-136">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d3830-136">Select **New**.</span></span>
3. <span data-ttu-id="d3830-137">Skriv inn en verdi i feltet **Vurderingsprofil**.</span><span class="sxs-lookup"><span data-stu-id="d3830-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="d3830-138">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3830-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="d3830-139">I **Område**-feltet velger du et alternativ fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="d3830-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="d3830-140">I **Lager**-feltet velger du et alternativ fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="d3830-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="d3830-141">I **Ratemotor**-feltet velger du et alternativ fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="d3830-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="d3830-142">Velg ratemotoren som er i samsvar med kontrakten du har med transportøren.</span><span class="sxs-lookup"><span data-stu-id="d3830-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="d3830-143">I **Vurderingsstandard**-feltet velger du et alternativ fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="d3830-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="d3830-144">I **Transittidmotor**-feltet velger du et alternativ fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="d3830-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="d3830-145">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="d3830-145">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]