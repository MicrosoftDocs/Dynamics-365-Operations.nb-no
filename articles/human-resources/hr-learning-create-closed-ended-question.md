---
title: Opprette et lukket spørsmål
description: Med lukkede spørsmål kan du angi alternativer for respondenten å velge blant.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 65d77806498c3a710c00865ad27716f50796cdf5
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2021
ms.locfileid: "5114962"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="bacca-103">Opprette et lukket spørsmål</span><span class="sxs-lookup"><span data-stu-id="bacca-103">Create a closed ended question</span></span>



<span data-ttu-id="bacca-104">Med lukkede spørsmål kan du angi alternativer for respondenten å velge blant.</span><span class="sxs-lookup"><span data-stu-id="bacca-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="bacca-105">Du må først opprette svargruppen med svar, og deretter opprette spørsmålet som bruker svargruppen.</span><span class="sxs-lookup"><span data-stu-id="bacca-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="bacca-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="bacca-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="bacca-107">Opprette en svargruppe</span><span class="sxs-lookup"><span data-stu-id="bacca-107">Create an answer group</span></span>
1. <span data-ttu-id="bacca-108">Gå til Spørreskjema > Utform > Svargrupper.</span><span class="sxs-lookup"><span data-stu-id="bacca-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="bacca-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="bacca-109">Click New.</span></span>
3. <span data-ttu-id="bacca-110">Skriv inn en verdi i Svargruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="bacca-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="bacca-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="bacca-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="bacca-112">Bruk funksjonen Tilfeldig rekkefølge til å plassere svarene tilfeldig i en annen rekkefølge hver gang svargruppen brukes for et spørsmål.</span><span class="sxs-lookup"><span data-stu-id="bacca-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="bacca-113">Klikk Svar.</span><span class="sxs-lookup"><span data-stu-id="bacca-113">Click Answer.</span></span>
6. <span data-ttu-id="bacca-114">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="bacca-114">Click New.</span></span>
    * <span data-ttu-id="bacca-115">Sekvensnummeret styrer rekkefølgen som svar vises i, med mindre Tilfeldig rekkefølge velges for svargruppen.</span><span class="sxs-lookup"><span data-stu-id="bacca-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="bacca-116">Poeng kan tildeles til svarene for bruk i poengberegning for spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="bacca-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="bacca-117">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="bacca-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="bacca-118">Det riktige svaret kan merkes for å indikere at det valgte svaret er riktig.</span><span class="sxs-lookup"><span data-stu-id="bacca-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="bacca-119">Dette kan brukes for poengberegning for spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="bacca-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="bacca-120">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="bacca-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="bacca-121">Fortsett å opprette svaralternativer for svargruppen.</span><span class="sxs-lookup"><span data-stu-id="bacca-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="bacca-122">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="bacca-122">Click New.</span></span>
10. <span data-ttu-id="bacca-123">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="bacca-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="bacca-124">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="bacca-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="bacca-125">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="bacca-125">Click New.</span></span>
13. <span data-ttu-id="bacca-126">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="bacca-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="bacca-127">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="bacca-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="bacca-128">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="bacca-128">Click New.</span></span>
16. <span data-ttu-id="bacca-129">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="bacca-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="bacca-130">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="bacca-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="bacca-131">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="bacca-131">Click New.</span></span>
19. <span data-ttu-id="bacca-132">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="bacca-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="bacca-133">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="bacca-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="bacca-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="bacca-134">Close the page.</span></span>
22. <span data-ttu-id="bacca-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="bacca-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="bacca-136">Opprette spørsmålet</span><span class="sxs-lookup"><span data-stu-id="bacca-136">Create the question</span></span>
1. <span data-ttu-id="bacca-137">Gå til Spørreskjema > Utform > Spørsmål.</span><span class="sxs-lookup"><span data-stu-id="bacca-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="bacca-138">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="bacca-138">Click New.</span></span>
3. <span data-ttu-id="bacca-139">Bruk Type-feltet til å gruppere relaterte spørsmål.</span><span class="sxs-lookup"><span data-stu-id="bacca-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="bacca-140">Du kan bruke inndatatyper for avmerkingsboks, alternativknapp eller kombinasjonsboks for lukkede spørsmål.</span><span class="sxs-lookup"><span data-stu-id="bacca-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="bacca-141">Velg et alternativ i Inndatatype-feltet.</span><span class="sxs-lookup"><span data-stu-id="bacca-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="bacca-142">Angi eller velg en verdi i Svargruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="bacca-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="bacca-143">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="bacca-143">In the Text field, type a value.</span></span>

