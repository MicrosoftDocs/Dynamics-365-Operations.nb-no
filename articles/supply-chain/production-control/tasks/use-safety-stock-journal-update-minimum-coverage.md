---
title: Bruke sikkerhetslagerjournalen til å oppdatere minste dekning
description: Denne fremgangsmåten viser hvordan du beregner minste dekningsforslag basert på historiske transaksjoner, og deretter oppdaterer varedekningen med forslagene.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a6e217d476cedc0318c382e12b7dc2036e557c3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "341103"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="b0fc0-103">Bruke sikkerhetslagerjournalen til å oppdatere minste dekning</span><span class="sxs-lookup"><span data-stu-id="b0fc0-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b0fc0-104">Denne fremgangsmåten viser hvordan du beregner minste dekningsforslag basert på historiske transaksjoner, og deretter oppdaterer varedekningen med forslagene.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="b0fc0-105">Dette gjøres ved hjelp av sikkerhetslagerjournalen.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="b0fc0-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="b0fc0-107">Denne oppgaven er ment for produksjonsplanleggeren for å bidra til å opprettholde minste dekning.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="b0fc0-108">Opprette en nytt journalnavn for sikkerhetslager</span><span class="sxs-lookup"><span data-stu-id="b0fc0-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="b0fc0-109">Gå til Journalnavn for sikkerhetslager.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-109">Go to Safety stock journal names.</span></span>
2. <span data-ttu-id="b0fc0-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-110">Click New.</span></span>
3. <span data-ttu-id="b0fc0-111">Skriv inn Materiale i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-111">In the Name field, type 'Material'.</span></span>
4. <span data-ttu-id="b0fc0-112">Skriv inn Materiale i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-112">In the Description field, type 'Material'.</span></span>
5. <span data-ttu-id="b0fc0-113">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="b0fc0-114">Opprette en sikkerhetslagerjournal</span><span class="sxs-lookup"><span data-stu-id="b0fc0-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="b0fc0-115">Gå til Beregning av sikkerhetslager.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-115">Go to Safety stock calculation.</span></span>
2. <span data-ttu-id="b0fc0-116">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-116">Click New.</span></span>
3. <span data-ttu-id="b0fc0-117">Angi eller velg en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="b0fc0-118">Velg journalnavnet for sikkerhetslageret som du opprettet, for eksempel Materiale.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="b0fc0-119">Klikk Opprett linjer.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-119">Click Create lines.</span></span>
5. <span data-ttu-id="b0fc0-120">Angi en dato i Fra dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-120">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="b0fc0-121">Sett datoen til 2015-01-02.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-121">Set the date to '2015-01-02'.</span></span>  
6. <span data-ttu-id="b0fc0-122">Angi en dato i Til dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-122">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="b0fc0-123">Sett datoen til 2015-12-30.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-123">Set the date to '2015-12-30'.</span></span>  
7. <span data-ttu-id="b0fc0-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-124">Click OK.</span></span>
    * <span data-ttu-id="b0fc0-125">Dette vil opprette linjer for dimensjonene som har lagertransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-125">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="b0fc0-126">Beregn forslag</span><span class="sxs-lookup"><span data-stu-id="b0fc0-126">Calculate proposal</span></span>
1. <span data-ttu-id="b0fc0-127">Klikk Beregn forslag.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-127">Click Calculate proposal.</span></span>
2. <span data-ttu-id="b0fc0-128">Velg alternativet Bruk gjennomsnittlig avgang i leveringstid.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-128">Select the Use average issue during lead time option.</span></span>
3. <span data-ttu-id="b0fc0-129">Sett Multiplikasjonsfaktor til 10.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-129">Set Multiplication factor to '10'.</span></span>
    * <span data-ttu-id="b0fc0-130">Multiplikasjonsfaktoren brukes til å justere forslaget.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-130">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="b0fc0-131">Siden demonstrasjonsdataene bare har noen få transaksjoner, må du angi faktoren for å få et realistisk forslag.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-131">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="b0fc0-132">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-132">Click OK.</span></span>
    * <span data-ttu-id="b0fc0-133">Bla nedover for å finne M0002 og M0003.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-133">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="b0fc0-134">Vis kolonnen Beregnet minimumsantall.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-134">View the Calculated minimum quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="b0fc0-135">Oppdatere minimumsantall</span><span class="sxs-lookup"><span data-stu-id="b0fc0-135">Update minimum quantity</span></span>
1. <span data-ttu-id="b0fc0-136">Angi et tall i feltet Nytt minimumsantall.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-136">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="b0fc0-137">Oppdater Nytt minimumsantall slik at det samsvarer med verdien i Beregnet minimumsantall.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-137">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="b0fc0-138">Hvis Beregnet minimumsantall er null, kan du angi ønsket fremtidig verdi.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-138">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="b0fc0-139">Du kan for eksempel angi Beregnet minimumsantall i dette feltet for M0002, som har lager 12.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-139">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="b0fc0-140">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b0fc0-141">Du kan for eksempel velge M0002, som har lager 12.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-141">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="b0fc0-142">Angi et tall i feltet Nytt minimumsantall.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-142">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="b0fc0-143">Oppdater Nytt minimumsantall slik at det samsvarer med verdien i Beregnet minimumsantall.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-143">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="b0fc0-144">Hvis Beregnet minimumsantall er null, kan du angi ønsket fremtidig verdi.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-144">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="b0fc0-145">Postere det nye minimumsantallet og validere resultatet</span><span class="sxs-lookup"><span data-stu-id="b0fc0-145">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="b0fc0-146">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-146">Click Post.</span></span>
2. <span data-ttu-id="b0fc0-147">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-147">Click OK.</span></span>
3. <span data-ttu-id="b0fc0-148">Klikk for å følge koblingen i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-148">Click to follow the link in the Item number field.</span></span>
4. <span data-ttu-id="b0fc0-149">Klikk for å følge koblingen i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-149">Click to follow the link in the Item number field.</span></span>
5. <span data-ttu-id="b0fc0-150">Klikk Plan i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-150">On the Action Pane, click Plan.</span></span>
6. <span data-ttu-id="b0fc0-151">Klikk Varedekning.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-151">Click Item coverage.</span></span>
    * <span data-ttu-id="b0fc0-152">Legg merke til at Minimumsantall er oppdatert med det nye minimumsantallet fra sikkerhetslagerjournalen.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-152">Notice that the Minimum quantity has been updated with the new minimum quantity from the safety stock journal.</span></span>  

