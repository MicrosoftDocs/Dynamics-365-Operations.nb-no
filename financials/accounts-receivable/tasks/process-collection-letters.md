--- 
title: Behandle purrebrev
description: Denne prosedyren viser hvordan du oppretter, skriver ut og posterer purringer.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="process-collection-letters"></a><span data-ttu-id="c49c1-103">Behandle purrebrev</span><span class="sxs-lookup"><span data-stu-id="c49c1-103">Process collection letters</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c49c1-104">Denne prosedyren viser hvordan du oppretter, skriver ut og posterer purringer.</span><span class="sxs-lookup"><span data-stu-id="c49c1-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="c49c1-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="c49c1-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="c49c1-106">Angi et purreforløp på posteringsprofilen</span><span class="sxs-lookup"><span data-stu-id="c49c1-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="c49c1-107">Gå til Kreditt og innkreving > Oppsett > Kundeposteringsprofiler.</span><span class="sxs-lookup"><span data-stu-id="c49c1-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="c49c1-108">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="c49c1-108">Click Edit.</span></span>
    * <span data-ttu-id="c49c1-109">Velg et purreforløp fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="c49c1-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="c49c1-110">Hvis du ikke vil generere purringer for transaksjoner ved hjelp av denne posteringsprofilen, lar du feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="c49c1-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="c49c1-111">I fanen Tabellrestriksjoner kan du endre måten purringer behandles på.</span><span class="sxs-lookup"><span data-stu-id="c49c1-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="c49c1-112">Hvis dette feltet er satt til Ja, opprettes purringer for denne posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="c49c1-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="c49c1-113">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c49c1-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="c49c1-114">Opprett purringer</span><span class="sxs-lookup"><span data-stu-id="c49c1-114">Create collection letters</span></span>
1. <span data-ttu-id="c49c1-115">Gå til Kreditt og innkreving > Purring > Opprett purringer.</span><span class="sxs-lookup"><span data-stu-id="c49c1-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="c49c1-116">Du må velge transaksjonstypene for purringene.</span><span class="sxs-lookup"><span data-stu-id="c49c1-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="c49c1-117">Alle åpne transaksjoner for disse typene inkluderes i beregningen.</span><span class="sxs-lookup"><span data-stu-id="c49c1-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="c49c1-118">Velg et alternativ for Purring-feltet.</span><span class="sxs-lookup"><span data-stu-id="c49c1-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="c49c1-119">Angi datoen på purringen.</span><span class="sxs-lookup"><span data-stu-id="c49c1-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="c49c1-120">Det er to alternativer for posteringsprofil: Konto – bruk posteringsprofilen som er tilordnet kundekontoen for hver rentenota.</span><span class="sxs-lookup"><span data-stu-id="c49c1-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="c49c1-121">Velg – Bruk posteringsprofilen som du velger i Posteringsprofil-feltet.</span><span class="sxs-lookup"><span data-stu-id="c49c1-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="c49c1-122">Velg en posteringsprofil hvis du har endret Bruk posteringsprofil fra til Velg.</span><span class="sxs-lookup"><span data-stu-id="c49c1-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="c49c1-123">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="c49c1-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="c49c1-124">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="c49c1-124">Click Filter.</span></span>
6. <span data-ttu-id="c49c1-125">Angi en kunde-ID i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="c49c1-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="c49c1-126">Skriv for eksempel inn USA-001.</span><span class="sxs-lookup"><span data-stu-id="c49c1-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="c49c1-127">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c49c1-127">Click OK.</span></span>
8. <span data-ttu-id="c49c1-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c49c1-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="c49c1-129">Skrive ut purringer</span><span class="sxs-lookup"><span data-stu-id="c49c1-129">Print collection letters</span></span>
1. <span data-ttu-id="c49c1-130">Gå til Kreditt og innkreving > Purring > Gjennomgå og behandle purrebrev.</span><span class="sxs-lookup"><span data-stu-id="c49c1-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="c49c1-131">Velg Opprettet i Status-feltet.</span><span class="sxs-lookup"><span data-stu-id="c49c1-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="c49c1-132">Velg Ikke skrevet ut i feltet Utskrevet.</span><span class="sxs-lookup"><span data-stu-id="c49c1-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="c49c1-133">Klikk Skriv ut.</span><span class="sxs-lookup"><span data-stu-id="c49c1-133">Click Print.</span></span>
5. <span data-ttu-id="c49c1-134">Klikk Purrenota.</span><span class="sxs-lookup"><span data-stu-id="c49c1-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="c49c1-135">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="c49c1-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="c49c1-136">Angi fristen for posteringer</span><span class="sxs-lookup"><span data-stu-id="c49c1-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="c49c1-137">Klikk OK for å skrive ut den valgte purringen.</span><span class="sxs-lookup"><span data-stu-id="c49c1-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="c49c1-138">Postere purringen</span><span class="sxs-lookup"><span data-stu-id="c49c1-138">Post the collection letter</span></span>
1. <span data-ttu-id="c49c1-139">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="c49c1-139">Click Post.</span></span>
2. <span data-ttu-id="c49c1-140">Angi posteringsdatoen for purringen.</span><span class="sxs-lookup"><span data-stu-id="c49c1-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="c49c1-141">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="c49c1-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="c49c1-142">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c49c1-142">Click OK.</span></span>
5. <span data-ttu-id="c49c1-143">Velg Postert i Status-feltet.</span><span class="sxs-lookup"><span data-stu-id="c49c1-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="c49c1-144">Velg et alternativ i feltet Utskrevet.</span><span class="sxs-lookup"><span data-stu-id="c49c1-144">In the Printed field, select an option.</span></span>


