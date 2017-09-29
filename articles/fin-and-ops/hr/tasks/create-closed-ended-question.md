--- 
title: "Opprette et lukket spørsmål"
description: "Med lukkede spørsmål kan du angi alternativer for respondenten å velge blant."
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 59f1af68e4b1198894a7cdab291021de9f3cf8a9
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="2310c-103">Opprette et lukket spørsmål</span><span class="sxs-lookup"><span data-stu-id="2310c-103">Create a closed ended question</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2310c-104">Med lukkede spørsmål kan du angi alternativer for respondenten å velge blant.</span><span class="sxs-lookup"><span data-stu-id="2310c-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="2310c-105">Du må først opprette svargruppen med svar, og deretter opprette spørsmålet som bruker svargruppen.</span><span class="sxs-lookup"><span data-stu-id="2310c-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="2310c-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="2310c-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="2310c-107">Opprette en svargruppe</span><span class="sxs-lookup"><span data-stu-id="2310c-107">Create an answer group</span></span>
1. <span data-ttu-id="2310c-108">Gå til Spørreskjema > Utform > Svargrupper.</span><span class="sxs-lookup"><span data-stu-id="2310c-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="2310c-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2310c-109">Click New.</span></span>
3. <span data-ttu-id="2310c-110">Skriv inn en verdi i Svargruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="2310c-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="2310c-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="2310c-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="2310c-112">Bruk funksjonen Tilfeldig rekkefølge til å plassere svarene tilfeldig i en annen rekkefølge hver gang svargruppen brukes for et spørsmål.</span><span class="sxs-lookup"><span data-stu-id="2310c-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="2310c-113">Klikk Svar.</span><span class="sxs-lookup"><span data-stu-id="2310c-113">Click Answer.</span></span>
6. <span data-ttu-id="2310c-114">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2310c-114">Click New.</span></span>
    * <span data-ttu-id="2310c-115">Sekvensnummeret styrer rekkefølgen som svar vises i, med mindre Tilfeldig rekkefølge velges for svargruppen.</span><span class="sxs-lookup"><span data-stu-id="2310c-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="2310c-116">Poeng kan tildeles til svarene for bruk i poengberegning for spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="2310c-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="2310c-117">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="2310c-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="2310c-118">Det riktige svaret kan merkes for å indikere at det valgte svaret er riktig.</span><span class="sxs-lookup"><span data-stu-id="2310c-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="2310c-119">Dette kan brukes for poengberegning for spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="2310c-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="2310c-120">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="2310c-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="2310c-121">Fortsett å opprette svaralternativer for svargruppen.</span><span class="sxs-lookup"><span data-stu-id="2310c-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="2310c-122">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2310c-122">Click New.</span></span>
10. <span data-ttu-id="2310c-123">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="2310c-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="2310c-124">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="2310c-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="2310c-125">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2310c-125">Click New.</span></span>
13. <span data-ttu-id="2310c-126">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="2310c-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="2310c-127">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="2310c-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="2310c-128">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2310c-128">Click New.</span></span>
16. <span data-ttu-id="2310c-129">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="2310c-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="2310c-130">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="2310c-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="2310c-131">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2310c-131">Click New.</span></span>
19. <span data-ttu-id="2310c-132">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="2310c-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="2310c-133">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="2310c-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="2310c-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2310c-134">Close the page.</span></span>
22. <span data-ttu-id="2310c-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2310c-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="2310c-136">Opprette spørsmålet</span><span class="sxs-lookup"><span data-stu-id="2310c-136">Create the question</span></span>
1. <span data-ttu-id="2310c-137">Gå til Spørreskjema > Utform > Spørsmål.</span><span class="sxs-lookup"><span data-stu-id="2310c-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="2310c-138">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2310c-138">Click New.</span></span>
3. <span data-ttu-id="2310c-139">Bruk Type-feltet til å gruppere relaterte spørsmål.</span><span class="sxs-lookup"><span data-stu-id="2310c-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="2310c-140">Du kan bruke inndatatyper for avmerkingsboks, alternativknapp eller kombinasjonsboks for lukkede spørsmål.</span><span class="sxs-lookup"><span data-stu-id="2310c-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="2310c-141">Velg et alternativ i Inndatatype-feltet.</span><span class="sxs-lookup"><span data-stu-id="2310c-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="2310c-142">Angi eller velg en verdi i Svargruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="2310c-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="2310c-143">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="2310c-143">In the Text field, type a value.</span></span>


