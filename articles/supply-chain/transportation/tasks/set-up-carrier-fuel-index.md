---
title: Definere en transportørdrivstoffindeks
description: Denne veiledningen viser hvordan du oppretter et område for drivstoffindeks, en drivstoffindeks og en drivstoffindeks for transportør.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6f72de7ad54a2b2dc1bf40fd8cb86d8b055e2d1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552098"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="97a34-103">Definere en transportørdrivstoffindeks</span><span class="sxs-lookup"><span data-stu-id="97a34-103">Set up a carrier fuel index</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97a34-104">Denne veiledningen viser hvordan du oppretter et område for drivstoffindeks, en drivstoffindeks og en drivstoffindeks for transportør.</span><span class="sxs-lookup"><span data-stu-id="97a34-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="97a34-105">Området for drivstoffindeks angir hvilket område drivstoffindeksen skal gjelde for, og drivstoffindeksen angir en drivstoffpris for en bestemt tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="97a34-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="97a34-106">Hvis du vil gjenspeile endringen i drivstoffpriser over tid, kan du knytte flere drivstoffindekser til en transportør.</span><span class="sxs-lookup"><span data-stu-id="97a34-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="97a34-107">Disse oppgavene utføres vanligvis av en transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="97a34-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="97a34-108">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="97a34-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="97a34-109">Opprette et område for drivstoffindeks</span><span class="sxs-lookup"><span data-stu-id="97a34-109">Create a fuel index region</span></span>
1. <span data-ttu-id="97a34-110">Gå til Transportstyring > Oppsett > Drivstoffindekser > Områder for drivstoffindeks.</span><span class="sxs-lookup"><span data-stu-id="97a34-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="97a34-111">Først må du opprette ulike områder, der du arbeider og beregner ulike drivstofftillegg.</span><span class="sxs-lookup"><span data-stu-id="97a34-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="97a34-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="97a34-112">Click New.</span></span>
3. <span data-ttu-id="97a34-113">Skriv inn en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="97a34-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="97a34-114">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="97a34-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="97a34-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="97a34-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="97a34-116">Opprette en drivstoffindeks</span><span class="sxs-lookup"><span data-stu-id="97a34-116">Create a fuel index</span></span>
1. <span data-ttu-id="97a34-117">Gå til Transportstyring > Oppsett > Drivstoffindekser > Drivstoffindekser.</span><span class="sxs-lookup"><span data-stu-id="97a34-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="97a34-118">Du må angi de gjeldende prisene for drivstoff for områdene du har definert.</span><span class="sxs-lookup"><span data-stu-id="97a34-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="97a34-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="97a34-119">Click New.</span></span>
3. <span data-ttu-id="97a34-120">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="97a34-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="97a34-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="97a34-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="97a34-122">Skriv inn et tall i feltet Pris per liter.</span><span class="sxs-lookup"><span data-stu-id="97a34-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="97a34-123">Angi dato og klokkeslett i feltet Effektiv startdato og effektivt startklokkeslett.</span><span class="sxs-lookup"><span data-stu-id="97a34-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="97a34-124">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="97a34-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="97a34-125">Opprette en drivstoffindeks for transportør</span><span class="sxs-lookup"><span data-stu-id="97a34-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="97a34-126">Gå til Transportstyring > Oppsett > Drivstoffindekser > Drivstoffindekser for transportør.</span><span class="sxs-lookup"><span data-stu-id="97a34-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="97a34-127">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="97a34-127">Click New.</span></span>
3. <span data-ttu-id="97a34-128">Angi en verdi i feltet Drivstoffindeks for transportør.</span><span class="sxs-lookup"><span data-stu-id="97a34-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="97a34-129">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="97a34-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="97a34-130">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="97a34-130">Click New.</span></span>
6. <span data-ttu-id="97a34-131">Angi dato og klokkeslett i feltet Effektiv startdato og effektivt startklokkeslett.</span><span class="sxs-lookup"><span data-stu-id="97a34-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="97a34-132">Angi et tall i feltet PPG fra.</span><span class="sxs-lookup"><span data-stu-id="97a34-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="97a34-133">I dette eksemplet kan du angi PPG fra-feltet som 1,95.</span><span class="sxs-lookup"><span data-stu-id="97a34-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="97a34-134">I feltet PPG til angir du et tall.</span><span class="sxs-lookup"><span data-stu-id="97a34-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="97a34-135">I dette eksemplet kan du angi PPG til-feltet som 2.</span><span class="sxs-lookup"><span data-stu-id="97a34-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="97a34-136">Angi et tall i Prosent-feltet.</span><span class="sxs-lookup"><span data-stu-id="97a34-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="97a34-137">I dette eksemplet kan du angi prosenten som 3.</span><span class="sxs-lookup"><span data-stu-id="97a34-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="97a34-138">Klikk rullegardinknappen i Valuta-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="97a34-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="97a34-139">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="97a34-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="97a34-140">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="97a34-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="97a34-141">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="97a34-141">Click Save.</span></span>

