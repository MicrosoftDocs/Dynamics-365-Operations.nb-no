---
title: Bruke sikkerhetslagerjournalen til å oppdatere minste dekning
description: Denne fremgangsmåten viser hvordan du beregner minste dekningsforslag basert på historiske transaksjoner, og deretter oppdaterer varedekningen med forslagene.
author: ChristianRytt
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1624f84db10ea7cc80bb94757f19484b8c403c5c
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148777"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="01231-103">Bruke sikkerhetslagerjournalen til å oppdatere minste dekning</span><span class="sxs-lookup"><span data-stu-id="01231-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="01231-104">Denne fremgangsmåten viser hvordan du beregner minste dekningsforslag basert på historiske transaksjoner, og deretter oppdaterer varedekningen med forslagene.</span><span class="sxs-lookup"><span data-stu-id="01231-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="01231-105">Dette gjøres ved hjelp av sikkerhetslagerjournalen.</span><span class="sxs-lookup"><span data-stu-id="01231-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="01231-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="01231-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="01231-107">Denne oppgaven er ment for produksjonsplanleggeren for å bidra til å opprettholde minste dekning.</span><span class="sxs-lookup"><span data-stu-id="01231-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="01231-108">Opprette en nytt journalnavn for sikkerhetslager</span><span class="sxs-lookup"><span data-stu-id="01231-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="01231-109">I **navigasjonsruten** går du til **Hovedplanlegging > Oppsett > Journalnavn for sikkerhetslager**.</span><span class="sxs-lookup"><span data-stu-id="01231-109">In the **Navigation pane**, go to **Master planning > Setup > Safety stock journal names**.</span></span>
2. <span data-ttu-id="01231-110">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="01231-110">Click **New**.</span></span>
3. <span data-ttu-id="01231-111">Skriv inn Materiale i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="01231-111">In the **Name** field, type 'Material'.</span></span>
4. <span data-ttu-id="01231-112">Skriv inn Materiale i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="01231-112">In the **Description** field, type 'Material'.</span></span>
5. <span data-ttu-id="01231-113">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="01231-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="01231-114">Opprette en sikkerhetslagerjournal</span><span class="sxs-lookup"><span data-stu-id="01231-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="01231-115">I **navigasjonsruten** går du til **Hovedplanlegging > Hovedplanlegging > Kjør > Beregning av sikkerhetslager**.</span><span class="sxs-lookup"><span data-stu-id="01231-115">In the **Navigation pane**, go to **Master planning > Master planning > Run > Safety stock calculation**.</span></span>
2. <span data-ttu-id="01231-116">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="01231-116">Click **New**.</span></span>
3. <span data-ttu-id="01231-117">Angi eller velg en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="01231-117">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="01231-118">Velg journalnavnet for sikkerhetslageret som du opprettet, for eksempel Materiale.</span><span class="sxs-lookup"><span data-stu-id="01231-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="01231-119">Klikk på **Opprett linjer**.</span><span class="sxs-lookup"><span data-stu-id="01231-119">Click **Create lines**.</span></span>
5. <span data-ttu-id="01231-120">Angi en dato i **Fra dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="01231-120">In the **From date** field, enter a date.</span></span>  
6. <span data-ttu-id="01231-121">Angi en dato i **Til dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="01231-121">In the **To date** field, enter a date.</span></span>
7. <span data-ttu-id="01231-122">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="01231-122">Click **OK**.</span></span> <span data-ttu-id="01231-123">Dette vil opprette linjer for dimensjonene som har lagertransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="01231-123">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="01231-124">Beregn forslag</span><span class="sxs-lookup"><span data-stu-id="01231-124">Calculate proposal</span></span>
1. <span data-ttu-id="01231-125">Klikk på **Beregn forslag.**</span><span class="sxs-lookup"><span data-stu-id="01231-125">Click **Calculate proposal**.</span></span>
2. <span data-ttu-id="01231-126">Velg alternativet **Bruk gjennomsnittlig avgang i leveringstid**.</span><span class="sxs-lookup"><span data-stu-id="01231-126">Select the **Use average issue during lead time** option.</span></span>
3. <span data-ttu-id="01231-127">Sett **Multiplikasjonsfaktor** til 10.</span><span class="sxs-lookup"><span data-stu-id="01231-127">Set **Multiplication factor** to '10'.</span></span> <span data-ttu-id="01231-128">Multiplikasjonsfaktoren brukes til å justere forslaget.</span><span class="sxs-lookup"><span data-stu-id="01231-128">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="01231-129">Siden demonstrasjonsdataene bare har noen få transaksjoner, må du angi faktoren for å få et realistisk forslag.</span><span class="sxs-lookup"><span data-stu-id="01231-129">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="01231-130">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="01231-130">Click **OK**.</span></span> <span data-ttu-id="01231-131">Bla nedover for å finne M0002 og M0003.</span><span class="sxs-lookup"><span data-stu-id="01231-131">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="01231-132">Vis kolonnen **Beregnet minimumsantall**.</span><span class="sxs-lookup"><span data-stu-id="01231-132">View the **Calculated minimum** quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="01231-133">Oppdatere minimumsantall</span><span class="sxs-lookup"><span data-stu-id="01231-133">Update minimum quantity</span></span>
1. <span data-ttu-id="01231-134">Angi et tall i feltet **Nytt minimumsantall**.</span><span class="sxs-lookup"><span data-stu-id="01231-134">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="01231-135">Oppdater Nytt minimumsantall slik at det samsvarer med verdien i Beregnet minimumsantall.</span><span class="sxs-lookup"><span data-stu-id="01231-135">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="01231-136">Hvis Beregnet minimumsantall er null, kan du angi ønsket fremtidig verdi.</span><span class="sxs-lookup"><span data-stu-id="01231-136">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="01231-137">Du kan for eksempel angi Beregnet minimumsantall i dette feltet for M0002, som har lager 12.</span><span class="sxs-lookup"><span data-stu-id="01231-137">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="01231-138">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="01231-138">In the list, find and select the desired record.</span></span> <span data-ttu-id="01231-139">Du kan for eksempel velge M0002, som har lager 12.</span><span class="sxs-lookup"><span data-stu-id="01231-139">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="01231-140">Angi et tall i feltet **Nytt minimumsantall**.</span><span class="sxs-lookup"><span data-stu-id="01231-140">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="01231-141">Oppdater Nytt minimumsantall slik at det samsvarer med verdien i Beregnet minimumsantall.</span><span class="sxs-lookup"><span data-stu-id="01231-141">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="01231-142">Hvis Beregnet minimumsantall er null, kan du angi ønsket fremtidig verdi.</span><span class="sxs-lookup"><span data-stu-id="01231-142">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="01231-143">Postere det nye minimumsantallet og validere resultatet</span><span class="sxs-lookup"><span data-stu-id="01231-143">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="01231-144">Klikk **Poster**.</span><span class="sxs-lookup"><span data-stu-id="01231-144">Click **Post**.</span></span>
2. <span data-ttu-id="01231-145">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="01231-145">Click **OK**.</span></span>
3. <span data-ttu-id="01231-146">Klikk for å følge koblingen i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="01231-146">Click to follow the link in the **Item number** field.</span></span>
4. <span data-ttu-id="01231-147">Klikk for å følge koblingen i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="01231-147">Click to follow the link in the **Item number** field.</span></span>
5. <span data-ttu-id="01231-148">Klikk på Plan i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="01231-148">On the **Action Pane**, click Plan.</span></span>
6. <span data-ttu-id="01231-149">Klikk på **Varedekning**.</span><span class="sxs-lookup"><span data-stu-id="01231-149">Click **Item coverage**.</span></span> <span data-ttu-id="01231-150">Legg merke til at **Minimumsantall** er oppdatert med det nye minimumsantallet fra sikkerhetslagerjournalen.</span><span class="sxs-lookup"><span data-stu-id="01231-150">Notice that the **Minimum quantity** has been updated with the new minimum quantity from the safety stock journal.</span></span>  

