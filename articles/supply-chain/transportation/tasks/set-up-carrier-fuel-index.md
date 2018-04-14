--- 
title: "Definere en transportørdrivstoffindeks"
description: "Denne veiledningen viser hvordan du oppretter et område for drivstoffindeks, en drivstoffindeks og en drivstoffindeks for transportør."
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: cd9842a14d512353bda399a9d83eb7296a75d982
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="9c574-103">Definere en transportørdrivstoffindeks</span><span class="sxs-lookup"><span data-stu-id="9c574-103">Set up a carrier fuel index</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9c574-104">Denne veiledningen viser hvordan du oppretter et område for drivstoffindeks, en drivstoffindeks og en drivstoffindeks for transportør.</span><span class="sxs-lookup"><span data-stu-id="9c574-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="9c574-105">Området for drivstoffindeks angir hvilket område drivstoffindeksen skal gjelde for, og drivstoffindeksen angir en drivstoffpris for en bestemt tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="9c574-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="9c574-106">Hvis du vil gjenspeile endringen i drivstoffpriser over tid, kan du knytte flere drivstoffindekser til en transportør.</span><span class="sxs-lookup"><span data-stu-id="9c574-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="9c574-107">Disse oppgavene utføres vanligvis av en transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="9c574-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="9c574-108">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="9c574-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="9c574-109">Opprette et område for drivstoffindeks</span><span class="sxs-lookup"><span data-stu-id="9c574-109">Create a fuel index region</span></span>
1. <span data-ttu-id="9c574-110">Gå til Transportstyring > Oppsett > Drivstoffindekser > Områder for drivstoffindeks.</span><span class="sxs-lookup"><span data-stu-id="9c574-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="9c574-111">Først må du opprette ulike områder, der du arbeider og beregner ulike drivstofftillegg.</span><span class="sxs-lookup"><span data-stu-id="9c574-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="9c574-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9c574-112">Click New.</span></span>
3. <span data-ttu-id="9c574-113">Skriv inn en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="9c574-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="9c574-114">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9c574-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9c574-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9c574-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="9c574-116">Opprette en drivstoffindeks</span><span class="sxs-lookup"><span data-stu-id="9c574-116">Create a fuel index</span></span>
1. <span data-ttu-id="9c574-117">Gå til Transportstyring > Oppsett > Drivstoffindekser > Drivstoffindekser.</span><span class="sxs-lookup"><span data-stu-id="9c574-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="9c574-118">Du må angi de gjeldende prisene for drivstoff for områdene du har definert.</span><span class="sxs-lookup"><span data-stu-id="9c574-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="9c574-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9c574-119">Click New.</span></span>
3. <span data-ttu-id="9c574-120">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="9c574-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9c574-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9c574-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9c574-122">Skriv inn et tall i feltet Pris per liter.</span><span class="sxs-lookup"><span data-stu-id="9c574-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="9c574-123">Angi dato og klokkeslett i feltet Effektiv startdato og effektivt startklokkeslett.</span><span class="sxs-lookup"><span data-stu-id="9c574-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="9c574-124">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9c574-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="9c574-125">Opprette en drivstoffindeks for transportør</span><span class="sxs-lookup"><span data-stu-id="9c574-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="9c574-126">Gå til Transportstyring > Oppsett > Drivstoffindekser > Drivstoffindekser for transportør.</span><span class="sxs-lookup"><span data-stu-id="9c574-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="9c574-127">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9c574-127">Click New.</span></span>
3. <span data-ttu-id="9c574-128">Angi en verdi i feltet Drivstoffindeks for transportør.</span><span class="sxs-lookup"><span data-stu-id="9c574-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="9c574-129">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="9c574-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9c574-130">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9c574-130">Click New.</span></span>
6. <span data-ttu-id="9c574-131">Angi dato og klokkeslett i feltet Effektiv startdato og effektivt startklokkeslett.</span><span class="sxs-lookup"><span data-stu-id="9c574-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="9c574-132">Angi et tall i feltet PPG fra.</span><span class="sxs-lookup"><span data-stu-id="9c574-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="9c574-133">I dette eksemplet kan du angi PPG fra-feltet som 1,95.</span><span class="sxs-lookup"><span data-stu-id="9c574-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="9c574-134">I feltet PPG til angir du et tall.</span><span class="sxs-lookup"><span data-stu-id="9c574-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="9c574-135">I dette eksemplet kan du angi PPG til-feltet som 2.</span><span class="sxs-lookup"><span data-stu-id="9c574-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="9c574-136">Angi et tall i Prosent-feltet.</span><span class="sxs-lookup"><span data-stu-id="9c574-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="9c574-137">I dette eksemplet kan du angi prosenten som 3.</span><span class="sxs-lookup"><span data-stu-id="9c574-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="9c574-138">Klikk rullegardinknappen i Valuta-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="9c574-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="9c574-139">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9c574-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="9c574-140">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9c574-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="9c574-141">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9c574-141">Click Save.</span></span>


