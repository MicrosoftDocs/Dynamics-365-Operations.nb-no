---
title: Behandle rente
description: Denne prosedyren viser hvordan du oppretter, skriver ut og posterer rentenotaer.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7170a7a14237058064ed3091e9437cae312e6bd5
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916282"
---
# <a name="process-interest"></a><span data-ttu-id="21dfc-103">Behandle rente</span><span class="sxs-lookup"><span data-stu-id="21dfc-103">Process interest</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="21dfc-104">Denne prosedyren viser hvordan du oppretter, skriver ut og posterer rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="21dfc-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="21dfc-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="21dfc-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="21dfc-106">Konfigurere rente i posteringsprofilen</span><span class="sxs-lookup"><span data-stu-id="21dfc-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="21dfc-107">I **navigasjonsruten** går du til > **Moduler > Kreditt og innkreving > Oppsett > Kundeposteringsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="21dfc-107">In the **Navigation pane**, go to **Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="21dfc-108">Klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="21dfc-108">Click **Edit**.</span></span>
3. <span data-ttu-id="21dfc-109">I **Oppsett**-hurtigfanen i **Rentekode**-feltet velger du en rentekode fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="21dfc-109">In the **Setup fastTab**, in the **Interest code** field, select an interest code from the drop-down list.</span></span> <span data-ttu-id="21dfc-110">Hvis du ikke vil beregne rente for transaksjoner ved hjelp av denne posteringsprofilen, lar du feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="21dfc-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span> <span data-ttu-id="21dfc-111">I hurtigfanen **Tabellrestriksjoner** kan du endre måten renter behandles på.</span><span class="sxs-lookup"><span data-stu-id="21dfc-111">The **Table restriction** fastTab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="21dfc-112">Hvis dette feltet er satt til Ja, beregnes rente for denne posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="21dfc-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="21dfc-113">Beregn rente</span><span class="sxs-lookup"><span data-stu-id="21dfc-113">Calculate interest</span></span>
1. <span data-ttu-id="21dfc-114">I **navigasjonsruten** går du til > **Moduler > Kreditt og innkreving > Rente > Opprett rentenotaer**.</span><span class="sxs-lookup"><span data-stu-id="21dfc-114">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Create interest notes**.</span></span>
2. <span data-ttu-id="21dfc-115">Du må velge transaksjonstypene du vil beregne rente for.</span><span class="sxs-lookup"><span data-stu-id="21dfc-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="21dfc-116">Alle åpne transaksjoner for disse typene inkluderes i beregningen.</span><span class="sxs-lookup"><span data-stu-id="21dfc-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="21dfc-117">Hvis du setter **Rente** til Ja, vil du beregne rente på rente.</span><span class="sxs-lookup"><span data-stu-id="21dfc-117">If you set **Interest** to 'Yes', you will calculate interest on interest.</span></span> <span data-ttu-id="21dfc-118">Du bør kontrollere lovene som gjelder for beregning av rente på rente før du inkluderer disse transaksjonene.</span><span class="sxs-lookup"><span data-stu-id="21dfc-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
4. <span data-ttu-id="21dfc-119">I **Fra dato**-feltet angir du en dato som renten skal beregnes fra.</span><span class="sxs-lookup"><span data-stu-id="21dfc-119">In the **From date** field, enter a date from which the interest will be calculated.</span></span> <span data-ttu-id="21dfc-120">Hvis du ikke angir en **Fra dato**, blir alle uposterte rentenotaer avbrutt og rente beregnes på nytt fra transaksjonsdatoen.</span><span class="sxs-lookup"><span data-stu-id="21dfc-120">If you do not specific a **From date**, then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>
5. <span data-ttu-id="21dfc-121">I **Til dato**-feltet angir du en dato som renten skal beregnes til.</span><span class="sxs-lookup"><span data-stu-id="21dfc-121">In the **To date** field, enter a date to which the interest would be calculated.</span></span>
6. <span data-ttu-id="21dfc-122">Velg et alternativ i feltet **Bruk posteringsprofil fra**.</span><span class="sxs-lookup"><span data-stu-id="21dfc-122">In the **Use posting profile from** field, select an option.</span></span> <span data-ttu-id="21dfc-123">Det finnes tre alternativer for posteringsprofil:</span><span class="sxs-lookup"><span data-stu-id="21dfc-123">There are three posting profile options:</span></span>
    - <span data-ttu-id="21dfc-124">Konto – Bruk posteringsprofilen som er tilordnet kundekontoen for hver rentenota.</span><span class="sxs-lookup"><span data-stu-id="21dfc-124">Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span> 
    - <span data-ttu-id="21dfc-125">Velg – Bruk posteringsprofilen som du velger i Posteringsprofil-feltet.</span><span class="sxs-lookup"><span data-stu-id="21dfc-125">Select – Use the posting profile that you select in the Posting profile field.</span></span>
    - <span data-ttu-id="21dfc-126">Transaksjon – Bruk den individuelle posteringsprofilen fra transaksjoner der rente er beregnet for hver rentenota.</span><span class="sxs-lookup"><span data-stu-id="21dfc-126">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="21dfc-127">Transaksjoner som ikke har en tilordnet posteringsprofil, bruker posteringsprofilen som er angitt i Finans og merverdiavgift-området i Kundeparametere-skjemaet).</span><span class="sxs-lookup"><span data-stu-id="21dfc-127">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
7. <span data-ttu-id="21dfc-128">Utvid hurtigfanen **Poster som skal inkluderes**.</span><span class="sxs-lookup"><span data-stu-id="21dfc-128">Expand the **Records to include** fastTab.</span></span>
8. <span data-ttu-id="21dfc-129">Klikk **Filter**.</span><span class="sxs-lookup"><span data-stu-id="21dfc-129">Click **Filter**.</span></span>
9. <span data-ttu-id="21dfc-130">Angi en kunde-ID i **Kriterier**-feltet.</span><span class="sxs-lookup"><span data-stu-id="21dfc-130">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="21dfc-131">Skriv for eksempel inn US-001.</span><span class="sxs-lookup"><span data-stu-id="21dfc-131">For example, enter 'US-001'.</span></span>
6. <span data-ttu-id="21dfc-132">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="21dfc-132">Click **OK**.</span></span>
7. <span data-ttu-id="21dfc-133">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="21dfc-133">Click **OK**.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="21dfc-134">Skriv ut rentenotaer</span><span class="sxs-lookup"><span data-stu-id="21dfc-134">Print interest notes</span></span>
1. <span data-ttu-id="21dfc-135">I **navigasjonsruten** går du til > **Moduler > Kreditt og innkreving > Rente > Gjennomgå og behandle rentenotaer**.</span><span class="sxs-lookup"><span data-stu-id="21dfc-135">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Review and process interest notes**.</span></span>
2. <span data-ttu-id="21dfc-136">Velg Opprettet i **Status**-feltet.</span><span class="sxs-lookup"><span data-stu-id="21dfc-136">In the **Status** field, select 'Created'.</span></span>
3. <span data-ttu-id="21dfc-137">Velg Ikke skrevet ut i feltet **Utskrevet**.</span><span class="sxs-lookup"><span data-stu-id="21dfc-137">In the **Printed** field, select 'Not printed'.</span></span>
4. <span data-ttu-id="21dfc-138">Klikk **Skriv ut**.</span><span class="sxs-lookup"><span data-stu-id="21dfc-138">Click **Print**.</span></span>
5. <span data-ttu-id="21dfc-139">Utvid hurtigfanen **Poster som skal inkluderes**.</span><span class="sxs-lookup"><span data-stu-id="21dfc-139">Expand the **Records to include** fastTab.</span></span>
6. <span data-ttu-id="21dfc-140">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="21dfc-140">Click **OK**.</span></span>
7. <span data-ttu-id="21dfc-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="21dfc-141">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="21dfc-142">Postere rentenotaen</span><span class="sxs-lookup"><span data-stu-id="21dfc-142">Post the interest note</span></span>
1. <span data-ttu-id="21dfc-143">Velg en rentenota som er klar til å posteres (statusen er opprettet).</span><span class="sxs-lookup"><span data-stu-id="21dfc-143">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="21dfc-144">Klikk **Poster**.</span><span class="sxs-lookup"><span data-stu-id="21dfc-144">Click **Post**.</span></span>
3. <span data-ttu-id="21dfc-145">Angir posteringsdatoen for rentenotaen.</span><span class="sxs-lookup"><span data-stu-id="21dfc-145">Enter the posting date for the interest note.</span></span> <span data-ttu-id="21dfc-146">Velg Ja hvis du vil opprette en økonomimodultransaksjon for hver rentenota.</span><span class="sxs-lookup"><span data-stu-id="21dfc-146">Select Yes to create a general ledger transaction for each interest note.</span></span> <span data-ttu-id="21dfc-147">Hvis du ikke velger Ja, akkumuleres renten på alle rentenotaene for kunden og posteres til økonomimodulen i én transaksjon.</span><span class="sxs-lookup"><span data-stu-id="21dfc-147">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="21dfc-148">Utvid hurtigfanen **Poster som skal inkluderes**.</span><span class="sxs-lookup"><span data-stu-id="21dfc-148">Expand the **Records to include** fastTab.</span></span>
5. <span data-ttu-id="21dfc-149">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="21dfc-149">Click **OK**.</span></span>
6. <span data-ttu-id="21dfc-150">Velg Postert i **Status**-feltet.</span><span class="sxs-lookup"><span data-stu-id="21dfc-150">In the **Status** field, select 'Posted'.</span></span>

