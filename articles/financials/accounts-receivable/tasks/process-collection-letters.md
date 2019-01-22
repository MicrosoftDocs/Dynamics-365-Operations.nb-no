--- 
title: Behandle purrebrev
description: Denne prosedyren viser hvordan du oppretter, skriver ut og posterer purringer.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.translationtype: HT
ms.sourcegitcommit: 18eaadf417ce6d0aacf0b13b3e4f857e06031e66
ms.openlocfilehash: 8a3f74d2891c050294e089eae14ba2386449d7c9
ms.contentlocale: nb-no
ms.lasthandoff: 01/22/2019

---
# <a name="process-collection-letters"></a><span data-ttu-id="78401-103">Behandle purrebrev</span><span class="sxs-lookup"><span data-stu-id="78401-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="78401-104">Denne prosedyren viser hvordan du oppretter, skriver ut og posterer purringer.</span><span class="sxs-lookup"><span data-stu-id="78401-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="78401-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="78401-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="78401-106">Angi et purreforløp på posteringsprofilen</span><span class="sxs-lookup"><span data-stu-id="78401-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="78401-107">Gå til **Kreditt og innkreving > Oppsett > Kundeposteringsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="78401-107">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="78401-108">Klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="78401-108">Click **Edit**.</span></span>
3. <span data-ttu-id="78401-109">Velg et purreforløp fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="78401-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="78401-110">Hvis du ikke vil generere purringer for transaksjoner ved hjelp av denne posteringsprofilen, lar du feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="78401-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="78401-111">Utvid fanen Tabellrestriksjoner for å endre måten purringer behandles på.</span><span class="sxs-lookup"><span data-stu-id="78401-111">Expand the table restriction tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="78401-112">Hvis dette feltet er satt til **Ja**, opprettes purringer for denne posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="78401-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="78401-113">Opprett purringer</span><span class="sxs-lookup"><span data-stu-id="78401-113">Create collection letters</span></span>
1. <span data-ttu-id="78401-114">Gå til **Kreditt og innkreving > Purring > Opprett purringer**.</span><span class="sxs-lookup"><span data-stu-id="78401-114">Go to **Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="78401-115">Velg transaksjonstypene for purringene.</span><span class="sxs-lookup"><span data-stu-id="78401-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="78401-116">Alle åpne transaksjoner for disse typene inkluderes i beregningen.</span><span class="sxs-lookup"><span data-stu-id="78401-116">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="78401-117">Velg et alternativ for **Purring**-feltet.</span><span class="sxs-lookup"><span data-stu-id="78401-117">In the **Collection letter** field, select an option.</span></span>
3. <span data-ttu-id="78401-118">Angi datoen på purringen.</span><span class="sxs-lookup"><span data-stu-id="78401-118">Enter the date of the collection letter.</span></span>
4. <span data-ttu-id="78401-119">Velg en posteringsprofil hvis du har endret **Bruk posteringsprofil fra** til **Velg**.</span><span class="sxs-lookup"><span data-stu-id="78401-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="78401-120">Det finnes to alternativer for posteringsprofil:</span><span class="sxs-lookup"><span data-stu-id="78401-120">There are two posting profile options:</span></span>   
   - <span data-ttu-id="78401-121">**Konto** – Bruk posteringsprofilen som er tilordnet kundekontoen for hver rentenota.</span><span class="sxs-lookup"><span data-stu-id="78401-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="78401-122">**Velg** – Bruk posteringsprofilen som du velger i **Posteringsprofil**-feltet.</span><span class="sxs-lookup"><span data-stu-id="78401-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  
5. <span data-ttu-id="78401-123">Utvid delen **Poster som skal inkluderes**.</span><span class="sxs-lookup"><span data-stu-id="78401-123">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="78401-124">Klikk **Filter**.</span><span class="sxs-lookup"><span data-stu-id="78401-124">Click **Filter**.</span></span>
7. <span data-ttu-id="78401-125">Angi en kunde-ID i **Kriterier**-feltet.</span><span class="sxs-lookup"><span data-stu-id="78401-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="78401-126">Skriv for eksempel inn US-001.</span><span class="sxs-lookup"><span data-stu-id="78401-126">For example, enter 'US-001'.</span></span>
8. <span data-ttu-id="78401-127">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="78401-127">Click **OK**.</span></span>
9. <span data-ttu-id="78401-128">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="78401-128">Click **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="78401-129">Skrive ut purringer</span><span class="sxs-lookup"><span data-stu-id="78401-129">Print collection letters</span></span>
1. <span data-ttu-id="78401-130">Gå til **Kreditt og innkreving > Purring > Gjennomgå og behandle purrebrev**.</span><span class="sxs-lookup"><span data-stu-id="78401-130">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="78401-131">Velg **Opprettet** i **Status**-feltet.</span><span class="sxs-lookup"><span data-stu-id="78401-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="78401-132">Velg **Ikke skrevet ut** i feltet **Utskrevet**.</span><span class="sxs-lookup"><span data-stu-id="78401-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="78401-133">Klikk **Skriv ut**.</span><span class="sxs-lookup"><span data-stu-id="78401-133">Click **Print**.</span></span>
5. <span data-ttu-id="78401-134">Klikk **Purrenota**.</span><span class="sxs-lookup"><span data-stu-id="78401-134">Click **Collection letter note**.</span></span>
6. <span data-ttu-id="78401-135">Utvid delen **Poster som skal inkluderes**.</span><span class="sxs-lookup"><span data-stu-id="78401-135">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="78401-136">Angi fristen for posteringer.</span><span class="sxs-lookup"><span data-stu-id="78401-136">Enter the cutoff date for postings.</span></span>
8. <span data-ttu-id="78401-137">Klikk **OK** for å skrive ut den valgte purringen.</span><span class="sxs-lookup"><span data-stu-id="78401-137">Click **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="78401-138">Poster purringen.</span><span class="sxs-lookup"><span data-stu-id="78401-138">Post the collection letter.</span></span>
   1. <span data-ttu-id="78401-139">Klikk **Poster**.</span><span class="sxs-lookup"><span data-stu-id="78401-139">Click **Post**.</span></span>
   2. <span data-ttu-id="78401-140">Angi posteringsdatoen for purringen.</span><span class="sxs-lookup"><span data-stu-id="78401-140">Enter the posting date for the collection letter.</span></span>
   3. <span data-ttu-id="78401-141">Utvid delen **Poster som skal inkluderes**.</span><span class="sxs-lookup"><span data-stu-id="78401-141">Expand the **Records to include** section.</span></span>
   4. <span data-ttu-id="78401-142">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="78401-142">Click **OK**.</span></span>
   5. <span data-ttu-id="78401-143">Velg **Postert** i **Status**-feltet.</span><span class="sxs-lookup"><span data-stu-id="78401-143">In the **Status** field, select **Posted**.</span></span>
   6. <span data-ttu-id="78401-144">Velg et alternativ i feltet **Utskrevet**.</span><span class="sxs-lookup"><span data-stu-id="78401-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="78401-145">Kontrollere purringer på kundenivå</span><span class="sxs-lookup"><span data-stu-id="78401-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="78401-146">Du kan også definere purringer på kundenivået slik at purrekoden for hver transaksjon spores, men behandlingen av purringer baseres på ett purrenivå som lagres for kunden.</span><span class="sxs-lookup"><span data-stu-id="78401-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="78401-147">Enkeltpurringen vil inneholde alle transaksjoner som er forfalt for kunden.</span><span class="sxs-lookup"><span data-stu-id="78401-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="78401-148">Fordi respittdagene nå spores på kundenivået, sendes ikke den neste purringen før antallet respittdager har gått for neste purring i sekvensen, selv om transaksjoner forfaller etter den siste purringen ble sendt.</span><span class="sxs-lookup"><span data-stu-id="78401-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="78401-149">Dette alternativet reduserer antall purringer som sendes per kunde.</span><span class="sxs-lookup"><span data-stu-id="78401-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="78401-150">Definere kunden for å kontrollere purringer på kundenivå</span><span class="sxs-lookup"><span data-stu-id="78401-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="78401-151">Gå til **Kreditt og innkreving > Oppsett > Kundeparametere**, og klikk på **Innkrevinger**-kategorien.</span><span class="sxs-lookup"><span data-stu-id="78401-151">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2.  <span data-ttu-id="78401-152">Endre verdien for **Opprett en purring per** til **Kunde**.</span><span class="sxs-lookup"><span data-stu-id="78401-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="78401-153">Gå til **Kreditt og innkreving > Purring > Gjennomgå og behandle purrebrev**.</span><span class="sxs-lookup"><span data-stu-id="78401-153">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="78401-154">Bare én purring genereres for en kunde med alle forfalte transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="78401-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="78401-155">Ignorere betalinger og kreditnotaer ved beregning av purrekoden</span><span class="sxs-lookup"><span data-stu-id="78401-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="78401-156">Hvis du tar med betalinger og kreditnotaer i transaksjonene som skal inkluderes i purringene, har du kanskje betalinger eller kreditnotaer som skal utløse en purring.</span><span class="sxs-lookup"><span data-stu-id="78401-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="78401-157">Du kan styre hvordan betalinger og kreditnotaer kontrollerer purrekoden ved å endre verdien for parameteren **Ignorer betalinger og kreditnotaer for beregning av purrekode**.</span><span class="sxs-lookup"><span data-stu-id="78401-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="78401-158">Når du skal ignorere betalinger og kreditnotaer ved beregning av purrekoden, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="78401-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>
1. <span data-ttu-id="78401-159">Gå til **Kreditt og innkreving > Oppsett > Kundeparametere**, og klikk på **Innkrevinger**-kategorien.</span><span class="sxs-lookup"><span data-stu-id="78401-159">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="78401-160">Ende verdien for **Ignorer betalinger og kreditnotaer for beregning av purrekode** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="78401-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>

