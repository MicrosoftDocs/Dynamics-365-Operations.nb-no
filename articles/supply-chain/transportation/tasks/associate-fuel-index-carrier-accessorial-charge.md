---
title: Knytte en indeks for drivstoff til en operatør som et tilbehørsgebyr
description: Denne håndboken beskriver hvordan du oppretter en tilbehørstilordning, transportørens tilbehørsgebyr, tilbehørsmal for drivstofftillegg og knytter en drivstoffindeks for transportør til en transportør.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1f69a6350a5a84ed19dcb37e174c25b112c16bd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974141"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="3a81a-103">Knytte en indeks for drivstoff til en operatør som et tilbehørsgebyr</span><span class="sxs-lookup"><span data-stu-id="3a81a-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3a81a-104">Denne håndboken beskriver hvordan du oppretter en tilbehørstilordning, transportørens tilbehørsgebyr, tilbehørsmal for drivstofftillegg og knytter en drivstoffindeks for transportør til en transportør.</span><span class="sxs-lookup"><span data-stu-id="3a81a-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="3a81a-105">Du må ha definert en drivstoffindeks for transportør før du kjører denne håndboken.</span><span class="sxs-lookup"><span data-stu-id="3a81a-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="3a81a-106">Du kan bruke veiledningen Definere transportørdrivstoffindeks til å gjøre dette.</span><span class="sxs-lookup"><span data-stu-id="3a81a-106">You can use the "Set up a carrier fuel index" guide to do this.</span></span> <span data-ttu-id="3a81a-107">Disse oppsettoppgaver utføres vanligvis av prosjektleder logistikk.</span><span class="sxs-lookup"><span data-stu-id="3a81a-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="3a81a-108">Demonstrasjonsdataene USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="3a81a-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="3a81a-109">Opprett en tilbehørsmal</span><span class="sxs-lookup"><span data-stu-id="3a81a-109">Create an accessorial master</span></span>
1. <span data-ttu-id="3a81a-110">Gå til Transportstyring > Oppsett > Vurdering > Tilbehørsmaler.</span><span class="sxs-lookup"><span data-stu-id="3a81a-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="3a81a-111">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="3a81a-111">Click New.</span></span>
3. <span data-ttu-id="3a81a-112">Angi en verdi i Tilbehørsmal-feltet.</span><span class="sxs-lookup"><span data-stu-id="3a81a-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="3a81a-113">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="3a81a-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="3a81a-114">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="3a81a-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="3a81a-115">Opprett transportørens tilbehørsgebyr</span><span class="sxs-lookup"><span data-stu-id="3a81a-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="3a81a-116">Gå til Transportstyring > Oppsett > Vurdering > Transportørens tilbehørsgebyr.</span><span class="sxs-lookup"><span data-stu-id="3a81a-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="3a81a-117">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="3a81a-117">Click New.</span></span>
3. <span data-ttu-id="3a81a-118">Skriv inn en verdi i feltet ID for transportørtilbehør.</span><span class="sxs-lookup"><span data-stu-id="3a81a-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="3a81a-119">Klikk på rullegardinknappen i feltet Transportør for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="3a81a-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3a81a-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="3a81a-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3a81a-121">I dette eksemplet velger du lastebiltransportør.</span><span class="sxs-lookup"><span data-stu-id="3a81a-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="3a81a-122">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3a81a-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="3a81a-123">Klikk på rullegardinknappen i feltet Transportørtjeneste for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="3a81a-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="3a81a-124">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3a81a-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="3a81a-125">Klikk på rullegardinknappen i feltet Tilbehørsmal for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="3a81a-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="3a81a-126">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="3a81a-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3a81a-127">Velg den nyopprettede tilbehørsmalen i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="3a81a-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="3a81a-128">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="3a81a-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="3a81a-129">Opprett en tilbehørstilordning</span><span class="sxs-lookup"><span data-stu-id="3a81a-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="3a81a-130">Klikk på Tilbehørstilordninger.</span><span class="sxs-lookup"><span data-stu-id="3a81a-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="3a81a-131">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="3a81a-131">Click New.</span></span>
3. <span data-ttu-id="3a81a-132">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="3a81a-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="3a81a-133">Aktiver/deaktiver utvidelsen av Kriterier-delen.</span><span class="sxs-lookup"><span data-stu-id="3a81a-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="3a81a-134">I kriteriene kan du velge å alltid bruke drivstofftillegg eller for dette eksemplet velge at det bare gjelder innenfor et bestemt område.</span><span class="sxs-lookup"><span data-stu-id="3a81a-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="3a81a-135">Skriv inn en verdi i feltet Postnummer fra.</span><span class="sxs-lookup"><span data-stu-id="3a81a-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="3a81a-136">Skriv inn en verdi i feltet Postnummer til.</span><span class="sxs-lookup"><span data-stu-id="3a81a-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="3a81a-137">Aktiver/deaktiver utvidelsen av Beregning-delen.</span><span class="sxs-lookup"><span data-stu-id="3a81a-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="3a81a-138">Du kan angi hvordan du beregner drivstofftillegg i beregningsdelen.</span><span class="sxs-lookup"><span data-stu-id="3a81a-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="3a81a-139">Denne beregningen avhenger av den tilbehørsenheten som du har valgt som grunnlag for beregningen.</span><span class="sxs-lookup"><span data-stu-id="3a81a-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="3a81a-140">Velg Drivstofftillegg i feltet Tilbehørsgebyrtype.</span><span class="sxs-lookup"><span data-stu-id="3a81a-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="3a81a-141">Velg Kilometer i feltet Tilbehørsenhet.</span><span class="sxs-lookup"><span data-stu-id="3a81a-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="3a81a-142">Klikk på rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="3a81a-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="3a81a-143">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3a81a-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="3a81a-144">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="3a81a-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="3a81a-145">Oppdater vurderingsprofilen for transportør</span><span class="sxs-lookup"><span data-stu-id="3a81a-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="3a81a-146">Gå til Transportstyring > Oppsett > Transportører > Transportører.</span><span class="sxs-lookup"><span data-stu-id="3a81a-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="3a81a-147">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="3a81a-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3a81a-148">Aktiver/deaktiver utvidelsen av delen Vurderingsprofiler.</span><span class="sxs-lookup"><span data-stu-id="3a81a-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="3a81a-149">Klikk på Rediger</span><span class="sxs-lookup"><span data-stu-id="3a81a-149">Click Edit.</span></span>
5. <span data-ttu-id="3a81a-150">Klikk på rullegardinknappen i feltet Drivstoffindeks for transportør for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="3a81a-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="3a81a-151">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3a81a-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="3a81a-152">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="3a81a-152">Click Save.</span></span>

