---
title: Opprette et lukket spørsmål
description: Med lukkede spørsmål kan du angi alternativer for respondenten å velge blant.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0316661d8be04cc5912e88bc50b3a1c7a73bbcb
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056690"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="da2e6-103">Opprette et lukket spørsmål</span><span class="sxs-lookup"><span data-stu-id="da2e6-103">Create a closed ended question</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="da2e6-104">Med lukkede spørsmål kan du angi alternativer for respondenten å velge blant.</span><span class="sxs-lookup"><span data-stu-id="da2e6-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="da2e6-105">Du må først opprette svargruppen med svar, og deretter opprette spørsmålet som bruker svargruppen.</span><span class="sxs-lookup"><span data-stu-id="da2e6-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="da2e6-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="da2e6-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="da2e6-107">Opprette en svargruppe</span><span class="sxs-lookup"><span data-stu-id="da2e6-107">Create an answer group</span></span>
1. <span data-ttu-id="da2e6-108">Gå til Spørreskjema > Utform > Svargrupper.</span><span class="sxs-lookup"><span data-stu-id="da2e6-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="da2e6-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="da2e6-109">Click New.</span></span>
3. <span data-ttu-id="da2e6-110">Skriv inn en verdi i Svargruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="da2e6-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="da2e6-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="da2e6-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="da2e6-112">Bruk funksjonen Tilfeldig rekkefølge til å plassere svarene tilfeldig i en annen rekkefølge hver gang svargruppen brukes for et spørsmål.</span><span class="sxs-lookup"><span data-stu-id="da2e6-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="da2e6-113">Klikk Svar.</span><span class="sxs-lookup"><span data-stu-id="da2e6-113">Click Answer.</span></span>
6. <span data-ttu-id="da2e6-114">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="da2e6-114">Click New.</span></span>
    * <span data-ttu-id="da2e6-115">Sekvensnummeret styrer rekkefølgen som svar vises i, med mindre Tilfeldig rekkefølge velges for svargruppen.</span><span class="sxs-lookup"><span data-stu-id="da2e6-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="da2e6-116">Poeng kan tildeles til svarene for bruk i poengberegning for spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="da2e6-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="da2e6-117">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="da2e6-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="da2e6-118">Det riktige svaret kan merkes for å indikere at det valgte svaret er riktig.</span><span class="sxs-lookup"><span data-stu-id="da2e6-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="da2e6-119">Dette kan brukes for poengberegning for spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="da2e6-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="da2e6-120">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="da2e6-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="da2e6-121">Fortsett å opprette svaralternativer for svargruppen.</span><span class="sxs-lookup"><span data-stu-id="da2e6-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="da2e6-122">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="da2e6-122">Click New.</span></span>
10. <span data-ttu-id="da2e6-123">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="da2e6-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="da2e6-124">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="da2e6-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="da2e6-125">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="da2e6-125">Click New.</span></span>
13. <span data-ttu-id="da2e6-126">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="da2e6-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="da2e6-127">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="da2e6-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="da2e6-128">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="da2e6-128">Click New.</span></span>
16. <span data-ttu-id="da2e6-129">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="da2e6-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="da2e6-130">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="da2e6-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="da2e6-131">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="da2e6-131">Click New.</span></span>
19. <span data-ttu-id="da2e6-132">Angi et tall i Poeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="da2e6-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="da2e6-133">Skriv inn en verdi i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="da2e6-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="da2e6-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="da2e6-134">Close the page.</span></span>
22. <span data-ttu-id="da2e6-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="da2e6-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="da2e6-136">Opprette spørsmålet</span><span class="sxs-lookup"><span data-stu-id="da2e6-136">Create the question</span></span>
1. <span data-ttu-id="da2e6-137">Gå til Spørreskjema > Utform > Spørsmål.</span><span class="sxs-lookup"><span data-stu-id="da2e6-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="da2e6-138">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="da2e6-138">Click New.</span></span>
3. <span data-ttu-id="da2e6-139">Bruk Type-feltet til å gruppere relaterte spørsmål.</span><span class="sxs-lookup"><span data-stu-id="da2e6-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="da2e6-140">Du kan bruke inndatatyper for avmerkingsboks, alternativknapp eller kombinasjonsboks for lukkede spørsmål.</span><span class="sxs-lookup"><span data-stu-id="da2e6-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="da2e6-141">Velg et alternativ i Inndatatype-feltet.</span><span class="sxs-lookup"><span data-stu-id="da2e6-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="da2e6-142">Angi eller velg en verdi i Svargruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="da2e6-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="da2e6-143">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="da2e6-143">In the Text field, type a value.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]