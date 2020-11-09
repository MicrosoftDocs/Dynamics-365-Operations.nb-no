---
title: Definere en transportørdrivstoffindeks
description: Denne veiledningen viser hvordan du oppretter et område for drivstoffindeks, en drivstoffindeks og en drivstoffindeks for transportør.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFuelIndexRegion, TMSCarrierFuelIndexTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33441de148b7edc8c564465d94ccf5602acbbe67
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016753"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="4fe70-103">Definere en transportørdrivstoffindeks</span><span class="sxs-lookup"><span data-stu-id="4fe70-103">Set up a carrier fuel index</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4fe70-104">Denne veiledningen viser hvordan du oppretter et område for drivstoffindeks, en drivstoffindeks og en drivstoffindeks for transportør.</span><span class="sxs-lookup"><span data-stu-id="4fe70-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="4fe70-105">Området for drivstoffindeks angir hvilket område drivstoffindeksen skal gjelde for, og drivstoffindeksen angir en drivstoffpris for en bestemt tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="4fe70-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="4fe70-106">Hvis du vil gjenspeile endringen i drivstoffpriser over tid, kan du knytte flere drivstoffindekser til en transportør.</span><span class="sxs-lookup"><span data-stu-id="4fe70-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="4fe70-107">Disse oppgavene utføres vanligvis av en transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="4fe70-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="4fe70-108">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="4fe70-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="4fe70-109">Opprette et område for drivstoffindeks</span><span class="sxs-lookup"><span data-stu-id="4fe70-109">Create a fuel index region</span></span>
1. <span data-ttu-id="4fe70-110">Gå til Transportstyring > Oppsett > Drivstoffindekser > Områder for drivstoffindeks.</span><span class="sxs-lookup"><span data-stu-id="4fe70-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="4fe70-111">Først må du opprette ulike områder, der du arbeider og beregner ulike drivstofftillegg.</span><span class="sxs-lookup"><span data-stu-id="4fe70-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="4fe70-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4fe70-112">Click New.</span></span>
3. <span data-ttu-id="4fe70-113">Skriv inn en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="4fe70-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="4fe70-114">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4fe70-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="4fe70-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4fe70-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="4fe70-116">Opprette en drivstoffindeks</span><span class="sxs-lookup"><span data-stu-id="4fe70-116">Create a fuel index</span></span>
1. <span data-ttu-id="4fe70-117">Gå til Transportstyring > Oppsett > Drivstoffindekser > Drivstoffindekser.</span><span class="sxs-lookup"><span data-stu-id="4fe70-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="4fe70-118">Du må angi de gjeldende prisene for drivstoff for områdene du har definert.</span><span class="sxs-lookup"><span data-stu-id="4fe70-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="4fe70-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4fe70-119">Click New.</span></span>
3. <span data-ttu-id="4fe70-120">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4fe70-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4fe70-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4fe70-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4fe70-122">Skriv inn et tall i feltet Pris per liter.</span><span class="sxs-lookup"><span data-stu-id="4fe70-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="4fe70-123">Angi dato og klokkeslett i feltet Effektiv startdato og effektivt startklokkeslett.</span><span class="sxs-lookup"><span data-stu-id="4fe70-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="4fe70-124">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4fe70-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="4fe70-125">Opprette en drivstoffindeks for transportør</span><span class="sxs-lookup"><span data-stu-id="4fe70-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="4fe70-126">Gå til Transportstyring > Oppsett > Drivstoffindekser > Drivstoffindekser for transportør.</span><span class="sxs-lookup"><span data-stu-id="4fe70-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="4fe70-127">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4fe70-127">Click New.</span></span>
3. <span data-ttu-id="4fe70-128">Angi en verdi i feltet Drivstoffindeks for transportør.</span><span class="sxs-lookup"><span data-stu-id="4fe70-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="4fe70-129">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="4fe70-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4fe70-130">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4fe70-130">Click New.</span></span>
6. <span data-ttu-id="4fe70-131">Angi dato og klokkeslett i feltet Effektiv startdato og effektivt startklokkeslett.</span><span class="sxs-lookup"><span data-stu-id="4fe70-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="4fe70-132">Angi et tall i feltet PPG fra.</span><span class="sxs-lookup"><span data-stu-id="4fe70-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="4fe70-133">I dette eksemplet kan du angi PPG fra-feltet som 1,95.</span><span class="sxs-lookup"><span data-stu-id="4fe70-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="4fe70-134">I feltet PPG til angir du et tall.</span><span class="sxs-lookup"><span data-stu-id="4fe70-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="4fe70-135">I dette eksemplet kan du angi PPG til-feltet som 2.</span><span class="sxs-lookup"><span data-stu-id="4fe70-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="4fe70-136">Angi et tall i Prosent-feltet.</span><span class="sxs-lookup"><span data-stu-id="4fe70-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="4fe70-137">I dette eksemplet kan du angi prosenten som 3.</span><span class="sxs-lookup"><span data-stu-id="4fe70-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="4fe70-138">Klikk rullegardinknappen i Valuta-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4fe70-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="4fe70-139">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4fe70-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="4fe70-140">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4fe70-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="4fe70-141">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4fe70-141">Click Save.</span></span>

