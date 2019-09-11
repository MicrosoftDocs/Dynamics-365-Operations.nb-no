---
title: Behandle purrebrev
description: Dette emnet viser hvordan du oppretter, skriver ut og posterer purringer.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 326d9375670cb4f4990a4f7070bf923a28b2c025
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867661"
---
# <a name="process-collection-letters"></a><span data-ttu-id="ff113-103">Behandle purrebrev</span><span class="sxs-lookup"><span data-stu-id="ff113-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff113-104">Dette emnet viser hvordan du oppretter, skriver ut og posterer purringer.</span><span class="sxs-lookup"><span data-stu-id="ff113-104">This topic shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="ff113-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="ff113-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="ff113-106">Angi et purreforløp på posteringsprofilen</span><span class="sxs-lookup"><span data-stu-id="ff113-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="ff113-107">Gå til **navigasjonsruten > Moduler > Kreditt og innkreving > Oppsett > Kundeposteringsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="ff113-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="ff113-108">Klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="ff113-108">Click **Edit**.</span></span>
3. <span data-ttu-id="ff113-109">Velg et purreforløp fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="ff113-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="ff113-110">Hvis du ikke vil generere purringer for transaksjoner ved hjelp av denne posteringsprofilen, lar du feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="ff113-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="ff113-111">Utvid fanen **Tabellrestriksjoner** for å endre måten purringer behandles på.</span><span class="sxs-lookup"><span data-stu-id="ff113-111">Expand the **Table restrictions** tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="ff113-112">Hvis dette feltet er satt til **Ja**, opprettes purringer for denne posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="ff113-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="ff113-113">Opprett purringer</span><span class="sxs-lookup"><span data-stu-id="ff113-113">Create collection letters</span></span>
1. <span data-ttu-id="ff113-114">Gå til **navigasjonsruten > Moduler > Kreditt og innkreving > Purring > Opprett purringer**.</span><span class="sxs-lookup"><span data-stu-id="ff113-114">Go to **Navigation pane > Modules > Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="ff113-115">Velg transaksjonstypene for purringene.</span><span class="sxs-lookup"><span data-stu-id="ff113-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="ff113-116">Alle åpne transaksjoner for disse typene inkluderes i beregningen.</span><span class="sxs-lookup"><span data-stu-id="ff113-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="ff113-117">Velg et alternativ for **Purring**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff113-117">In the **Collection letter** field, select an option.</span></span>
4. <span data-ttu-id="ff113-118">I feltet **Purredato** angir du datoen for purringen.</span><span class="sxs-lookup"><span data-stu-id="ff113-118">In the **Collection letter date** field, enter the date of the collection letter.</span></span>
5. <span data-ttu-id="ff113-119">Velg en posteringsprofil hvis du har endret **Bruk posteringsprofil fra** til **Velg**.</span><span class="sxs-lookup"><span data-stu-id="ff113-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="ff113-120">Det finnes to alternativer for posteringsprofil:</span><span class="sxs-lookup"><span data-stu-id="ff113-120">There are two posting profile options:</span></span>   

   - <span data-ttu-id="ff113-121">**Konto** – Bruk posteringsprofilen som er tilordnet kundekontoen for hver rentenota.</span><span class="sxs-lookup"><span data-stu-id="ff113-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="ff113-122">**Velg** – Bruk posteringsprofilen som du velger i **Posteringsprofil**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff113-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  

6. <span data-ttu-id="ff113-123">Utvid delen **Poster som skal inkluderes**.</span><span class="sxs-lookup"><span data-stu-id="ff113-123">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="ff113-124">Velg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="ff113-124">Select **Filter**.</span></span>
8. <span data-ttu-id="ff113-125">Angi en kunde-ID i **Kriterier**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff113-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="ff113-126">Skriv for eksempel inn US-001.</span><span class="sxs-lookup"><span data-stu-id="ff113-126">For example, enter 'US-001'.</span></span>
9. <span data-ttu-id="ff113-127">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff113-127">Select **OK**.</span></span>
10. <span data-ttu-id="ff113-128">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff113-128">Select **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="ff113-129">Skrive ut purringer</span><span class="sxs-lookup"><span data-stu-id="ff113-129">Print collection letters</span></span>
1. <span data-ttu-id="ff113-130">Gå til **navigasjonsruten > Moduler > Kreditt og innkreving > Purring > Gjennomgå og behandle purrebrev**.</span><span class="sxs-lookup"><span data-stu-id="ff113-130">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="ff113-131">Velg **Opprettet** i **Status**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff113-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="ff113-132">Velg **Ikke skrevet ut** i feltet **Utskrevet**.</span><span class="sxs-lookup"><span data-stu-id="ff113-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="ff113-133">Velg **Skriv ut**.</span><span class="sxs-lookup"><span data-stu-id="ff113-133">Select **Print**.</span></span>
5. <span data-ttu-id="ff113-134">Velg **Purrenota**.</span><span class="sxs-lookup"><span data-stu-id="ff113-134">Select **Collection letter note**.</span></span>
6. <span data-ttu-id="ff113-135">I **Parametere**-delen angir du fristen for posteringer.</span><span class="sxs-lookup"><span data-stu-id="ff113-135">In the **Parameters** section, enter the cutoff date for postings.</span></span>
7. <span data-ttu-id="ff113-136">Utvid delen **Poster som skal inkluderes**, og angi detaljene for purrenotaen.</span><span class="sxs-lookup"><span data-stu-id="ff113-136">Expand the **Records to include** section and enter the details of the Collection letter note.</span></span>
8. <span data-ttu-id="ff113-137">Velg **OK** for å skrive ut purringen.</span><span class="sxs-lookup"><span data-stu-id="ff113-137">Select **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="ff113-138">Poster purringen.</span><span class="sxs-lookup"><span data-stu-id="ff113-138">Post the collection letter.</span></span>

    1. <span data-ttu-id="ff113-139">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="ff113-139">Select **Post**.</span></span>
    1. <span data-ttu-id="ff113-140">Angi posteringsdatoen for purringen.</span><span class="sxs-lookup"><span data-stu-id="ff113-140">Enter the posting date for the collection letter.</span></span>
    1. <span data-ttu-id="ff113-141">Utvid delen **Poster som skal inkluderes**.</span><span class="sxs-lookup"><span data-stu-id="ff113-141">Expand the **Records to include** section.</span></span>
    1. <span data-ttu-id="ff113-142">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff113-142">Select **OK**.</span></span>
    1. <span data-ttu-id="ff113-143">Velg **Postert** i **Status**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff113-143">In the **Status** field, select **Posted**.</span></span>
    1. <span data-ttu-id="ff113-144">Velg et alternativ i feltet **Utskrevet**.</span><span class="sxs-lookup"><span data-stu-id="ff113-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="ff113-145">Kontrollere purringer på kundenivå</span><span class="sxs-lookup"><span data-stu-id="ff113-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="ff113-146">Du kan også definere purringer på kundenivået slik at purrekoden for hver transaksjon spores, men behandlingen av purringer baseres på ett purrenivå som lagres for kunden.</span><span class="sxs-lookup"><span data-stu-id="ff113-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="ff113-147">Enkeltpurringen vil inneholde alle transaksjoner som er forfalt for kunden.</span><span class="sxs-lookup"><span data-stu-id="ff113-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="ff113-148">Fordi respittdagene nå spores på kundenivået, sendes ikke den neste purringen før antallet respittdager har gått for neste purring i sekvensen, selv om transaksjoner forfaller etter den siste purringen ble sendt.</span><span class="sxs-lookup"><span data-stu-id="ff113-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="ff113-149">Dette alternativet reduserer antall purringer som sendes per kunde.</span><span class="sxs-lookup"><span data-stu-id="ff113-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="ff113-150">Definere kunden for å kontrollere purringer på kundenivå</span><span class="sxs-lookup"><span data-stu-id="ff113-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="ff113-151">Gå til **Navigasjonsrute > Moduler > Kreditt og innkreving > Oppsett > Kundeparametere**, og velg **Innkrevinger**-kategorien.</span><span class="sxs-lookup"><span data-stu-id="ff113-151">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and select the **Collections** tab.</span></span> 
2.  <span data-ttu-id="ff113-152">Endre verdien for **Opprett en purring per** til **Kunde**.</span><span class="sxs-lookup"><span data-stu-id="ff113-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="ff113-153">Gå til **navigasjonsruten > Moduler > Kreditt og innkreving > Purring > Gjennomgå og behandle purrebrev**.</span><span class="sxs-lookup"><span data-stu-id="ff113-153">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="ff113-154">Bare én purring genereres for en kunde med alle forfalte transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="ff113-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="ff113-155">Ignorere betalinger og kreditnotaer ved beregning av purrekoden</span><span class="sxs-lookup"><span data-stu-id="ff113-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="ff113-156">Hvis du tar med betalinger og kreditnotaer i transaksjonene som skal inkluderes i purringene, har du kanskje betalinger eller kreditnotaer som skal utløse en purring.</span><span class="sxs-lookup"><span data-stu-id="ff113-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="ff113-157">Du kan styre hvordan betalinger og kreditnotaer kontrollerer purrekoden ved å endre verdien for parameteren **Ignorer betalinger og kreditnotaer for beregning av purrekode**.</span><span class="sxs-lookup"><span data-stu-id="ff113-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="ff113-158">Når du skal ignorere betalinger og kreditnotaer ved beregning av purrekoden, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="ff113-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>

1. <span data-ttu-id="ff113-159">Gå til **Navigasjonsrute > Moduler > Kreditt og innkreving > Oppsett > Kundeparametere**, og klikk på **Innkrevinger**-kategorien.</span><span class="sxs-lookup"><span data-stu-id="ff113-159">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="ff113-160">Ende verdien for **Ignorer betalinger og kreditnotaer for beregning av purrekode** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ff113-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>
