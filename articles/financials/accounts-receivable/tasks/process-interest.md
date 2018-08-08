--- 
title: Behandle rente
description: Denne prosedyren viser hvordan du oppretter, skriver ut og posterer rentenotaer.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 3264ea08b93f8c9ed7dc2792db2e3878cae188a4
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="process-interest"></a><span data-ttu-id="55ad3-103">Behandle rente</span><span class="sxs-lookup"><span data-stu-id="55ad3-103">Process interest</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="55ad3-104">Denne prosedyren viser hvordan du oppretter, skriver ut og posterer rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="55ad3-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="55ad3-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="55ad3-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="55ad3-106">Konfigurere rente i posteringsprofilen</span><span class="sxs-lookup"><span data-stu-id="55ad3-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="55ad3-107">Gå til Kreditt og innkreving > Oppsett > Kundeposteringsprofiler.</span><span class="sxs-lookup"><span data-stu-id="55ad3-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="55ad3-108">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="55ad3-108">Click Edit.</span></span>
    * <span data-ttu-id="55ad3-109">Velg en rentekode fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="55ad3-109">Select an interest code from the drop-down list.</span></span> <span data-ttu-id="55ad3-110">Hvis du ikke vil beregne rente for transaksjoner ved hjelp av denne posteringsprofilen, lar du feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="55ad3-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="55ad3-111">I fanen Tabellrestriksjoner kan du endre måten renter behandles på.</span><span class="sxs-lookup"><span data-stu-id="55ad3-111">The Table restriction tab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="55ad3-112">Hvis dette feltet er satt til Ja, beregnes rente for denne posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="55ad3-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="55ad3-113">Beregn rente</span><span class="sxs-lookup"><span data-stu-id="55ad3-113">Calculate interest</span></span>
1. <span data-ttu-id="55ad3-114">Gå til Kreditt og innkreving > Rente > Opprett rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="55ad3-114">Go to Credit and collections > Interest > Create interest notes.</span></span>
    * <span data-ttu-id="55ad3-115">Du må velge transaksjonstypene du vil beregne rente for.</span><span class="sxs-lookup"><span data-stu-id="55ad3-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="55ad3-116">Alle åpne transaksjoner for disse typene inkluderes i beregningen.</span><span class="sxs-lookup"><span data-stu-id="55ad3-116">All of the open transactions for these types will be included in the calculation.</span></span>  
    * <span data-ttu-id="55ad3-117">Hvis du velger Rente, vil du beregne rente på rente.</span><span class="sxs-lookup"><span data-stu-id="55ad3-117">If you select Interest, you will calculate interest on interest.</span></span> <span data-ttu-id="55ad3-118">Du bør kontrollere lovene som gjelder for beregning av rente på rente før du inkluderer disse transaksjonene.</span><span class="sxs-lookup"><span data-stu-id="55ad3-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
    * <span data-ttu-id="55ad3-119">Rente beregnes fra denne datoen til "Til dato".</span><span class="sxs-lookup"><span data-stu-id="55ad3-119">Interest will be calculated from this date to the "To date".</span></span> <span data-ttu-id="55ad3-120">Hvis du ikke angir en "Fra dato", blir alle uposterte rentenotaer avbrutt og rente beregnes på nytt fra transaksjonsdatoen.</span><span class="sxs-lookup"><span data-stu-id="55ad3-120">If you do not specific a "From date", then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>  
2. <span data-ttu-id="55ad3-121">Angi datoen for rentenotaen.</span><span class="sxs-lookup"><span data-stu-id="55ad3-121">Enter the date of the interest note.</span></span>
    * <span data-ttu-id="55ad3-122">Det er tre alternativer for posteringsprofil: Konto – bruk posteringsprofilen som er tilordnet kundekontoen for hver rentenota.</span><span class="sxs-lookup"><span data-stu-id="55ad3-122">There are three posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="55ad3-123">Velg – Bruk posteringsprofilen som du velger i Posteringsprofil-feltet.</span><span class="sxs-lookup"><span data-stu-id="55ad3-123">Select – Use the posting profile that you select in the Posting profile field.</span></span>   <span data-ttu-id="55ad3-124">Transaksjon – Bruk den individuelle posteringsprofilen fra transaksjoner der rente er beregnet for hver rentenota.</span><span class="sxs-lookup"><span data-stu-id="55ad3-124">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="55ad3-125">Transaksjoner som ikke har en tilordnet posteringsprofil, bruker posteringsprofilen som er angitt i Finans og merverdiavgift-området i Kundeparametere-skjemaet).</span><span class="sxs-lookup"><span data-stu-id="55ad3-125">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
    * <span data-ttu-id="55ad3-126">Velg en posteringsprofil her hvis du har endret "Bruk posteringsprofil fra" til "Velg".</span><span class="sxs-lookup"><span data-stu-id="55ad3-126">Select a posting profile here if you changed "Use posting profile from" to "Select".</span></span>  
3. <span data-ttu-id="55ad3-127">Vis eller skjul delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="55ad3-127">Expand or collapse the Records to include section.</span></span>
4. <span data-ttu-id="55ad3-128">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="55ad3-128">Click Filter.</span></span>
5. <span data-ttu-id="55ad3-129">Angi en kunde-ID i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="55ad3-129">In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="55ad3-130">Skriv for eksempel inn USA-001.</span><span class="sxs-lookup"><span data-stu-id="55ad3-130">For example, enter 'US-001'..</span></span>
6. <span data-ttu-id="55ad3-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="55ad3-131">Click OK.</span></span>
7. <span data-ttu-id="55ad3-132">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="55ad3-132">Click OK.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="55ad3-133">Skriv ut rentenotaer</span><span class="sxs-lookup"><span data-stu-id="55ad3-133">Print interest notes</span></span>
1. <span data-ttu-id="55ad3-134">Gå til Kreditt og innkreving > Rente > Gjennomgå og behandle rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="55ad3-134">Go to Credit and collections > Interest > Review and process interest notes.</span></span>
2. <span data-ttu-id="55ad3-135">Velg Opprettet i Status-feltet.</span><span class="sxs-lookup"><span data-stu-id="55ad3-135">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="55ad3-136">Velg Ikke skrevet ut i feltet Utskrevet.</span><span class="sxs-lookup"><span data-stu-id="55ad3-136">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="55ad3-137">Klikk Skriv ut.</span><span class="sxs-lookup"><span data-stu-id="55ad3-137">Click Print.</span></span>
5. <span data-ttu-id="55ad3-138">Vis eller skjul delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="55ad3-138">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="55ad3-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="55ad3-139">Click OK.</span></span>
7. <span data-ttu-id="55ad3-140">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="55ad3-140">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="55ad3-141">Postere rentenotaen</span><span class="sxs-lookup"><span data-stu-id="55ad3-141">Post the interest note</span></span>
1. <span data-ttu-id="55ad3-142">Velg en rentenota som er klar til å posteres (statusen er opprettet).</span><span class="sxs-lookup"><span data-stu-id="55ad3-142">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="55ad3-143">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="55ad3-143">Click Post.</span></span>
3. <span data-ttu-id="55ad3-144">Angir posteringsdatoen for rentenotaen.</span><span class="sxs-lookup"><span data-stu-id="55ad3-144">Enter the posting date for the interest note.</span></span>
    * <span data-ttu-id="55ad3-145">Velg Ja hvis du vil opprette en økonomimodultransaksjon for hver rentenota.</span><span class="sxs-lookup"><span data-stu-id="55ad3-145">Select Yes to create a general ledger transaction for each interest note.</span></span>     <span data-ttu-id="55ad3-146">Hvis du ikke velger Ja, akkumuleres renten på alle rentenotaene for kunden og posteres til økonomimodulen i én transaksjon.</span><span class="sxs-lookup"><span data-stu-id="55ad3-146">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="55ad3-147">Vis eller skjul delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="55ad3-147">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="55ad3-148">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="55ad3-148">Click OK.</span></span>
6. <span data-ttu-id="55ad3-149">Velg Postert i Status-feltet.</span><span class="sxs-lookup"><span data-stu-id="55ad3-149">In the Status field, select 'Posted'.</span></span>


