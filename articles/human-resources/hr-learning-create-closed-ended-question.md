---
title: Opprette et lukket spørsmål
description: Med lukkede spørsmål kan du angi alternativer for respondenten å velge blant.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2eb53290d39fef0bf439a199dfd774138823ec2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419958"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="4b8d9-103">Opprette et lukket spørsmål</span><span class="sxs-lookup"><span data-stu-id="4b8d9-103">Create a closed ended question</span></span>



<span data-ttu-id="4b8d9-104">Med lukkede spørsmål kan du angi alternativer for respondenten å velge blant.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="4b8d9-105">Du må først opprette svargruppen med svar, og deretter opprette spørsmålet som bruker svargruppen.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="4b8d9-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="4b8d9-107">Opprette en svargruppe</span><span class="sxs-lookup"><span data-stu-id="4b8d9-107">Create an answer group</span></span>
1. <span data-ttu-id="4b8d9-108">Gå til Spørreskjema > Utform > Svargrupper.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="4b8d9-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-109">Click New.</span></span>
3. <span data-ttu-id="4b8d9-110">Skriv inn en verdi i Svargruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="4b8d9-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4b8d9-112">Bruk funksjonen Tilfeldig rekkefølge til å plassere svarene tilfeldig i en annen rekkefølge hver gang svargruppen brukes for et spørsmål.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="4b8d9-113">Klikk Svar.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-113">Click Answer.</span></span>
6. <span data-ttu-id="4b8d9-114">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-114">Click New.</span></span>
    * <span data-ttu-id="4b8d9-115">Sekvensnummeret styrer rekkefølgen som svar vises i, med mindre Tilfeldig rekkefølge velges for svargruppen.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="4b8d9-116">Poeng kan tildeles til svarene for bruk i poengberegning for spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="4b8d9-117">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="4b8d9-118">Det riktige svaret kan merkes for å indikere at det valgte svaret er riktig.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="4b8d9-119">Dette kan brukes for poengberegning for spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="4b8d9-120">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="4b8d9-121">Fortsett å opprette svaralternativer for svargruppen.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="4b8d9-122">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-122">Click New.</span></span>
10. <span data-ttu-id="4b8d9-123">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="4b8d9-124">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="4b8d9-125">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-125">Click New.</span></span>
13. <span data-ttu-id="4b8d9-126">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="4b8d9-127">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="4b8d9-128">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-128">Click New.</span></span>
16. <span data-ttu-id="4b8d9-129">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="4b8d9-130">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="4b8d9-131">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-131">Click New.</span></span>
19. <span data-ttu-id="4b8d9-132">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="4b8d9-133">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="4b8d9-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-134">Close the page.</span></span>
22. <span data-ttu-id="4b8d9-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="4b8d9-136">Opprette spørsmålet</span><span class="sxs-lookup"><span data-stu-id="4b8d9-136">Create the question</span></span>
1. <span data-ttu-id="4b8d9-137">Gå til Spørreskjema > Utform > Spørsmål.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="4b8d9-138">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-138">Click New.</span></span>
3. <span data-ttu-id="4b8d9-139">Bruk Type-feltet til å gruppere relaterte spørsmål.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="4b8d9-140">Du kan bruke inndatatyper for avmerkingsboks, alternativknapp eller kombinasjonsboks for lukkede spørsmål.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="4b8d9-141">Velg et alternativ i Inndatatype-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="4b8d9-142">Angi eller velg en verdi i Svargruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="4b8d9-143">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b8d9-143">In the Text field, type a value.</span></span>

