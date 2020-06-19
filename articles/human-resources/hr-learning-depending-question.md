---
title: Gjøre et spørsmål avhengig av svaret på det forrige spørsmålet
description: Med betingede spørsmål kan du angi hvilket oppfølgingsspørsmål som skal vises til respondenten, avhengig av svaret på det forrige spørsmålet.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4295b49336ec7ac3cff4deba675bc63511be48de
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429549"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="a3897-103">Gjøre et spørsmål avhengig av svaret på det forrige spørsmålet</span><span class="sxs-lookup"><span data-stu-id="a3897-103">Make a question dependent on the answer of the previous question</span></span>



<span data-ttu-id="a3897-104">Med betingede spørsmål kan du angi hvilket oppfølgingsspørsmål som skal vises til respondenten, avhengig av svaret på det forrige spørsmålet.</span><span class="sxs-lookup"><span data-stu-id="a3897-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="a3897-105">Hvis du for eksempel spør Foretrekker du kaffe eller te, kan et logisk oppfølgingsspørsmål bestemmes avhengig av om respondenten velger kaffe eller te som et svar.</span><span class="sxs-lookup"><span data-stu-id="a3897-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="a3897-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="a3897-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="a3897-107">Søk etter det eksisterende spørreskjemaet</span><span class="sxs-lookup"><span data-stu-id="a3897-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="a3897-108">Gå til Spørreskjema > Utform > Spørreskjemaer.</span><span class="sxs-lookup"><span data-stu-id="a3897-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="a3897-109">Velg spørreskjemaet WorkFH i listen.</span><span class="sxs-lookup"><span data-stu-id="a3897-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="a3897-110">Legg til alle spørsmålene og underspørsmålene i spørreskjemaet</span><span class="sxs-lookup"><span data-stu-id="a3897-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="a3897-111">Klikk Spørsmål.</span><span class="sxs-lookup"><span data-stu-id="a3897-111">Click Questions.</span></span>
2. <span data-ttu-id="a3897-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="a3897-112">Click New.</span></span>
3. <span data-ttu-id="a3897-113">Velg spørsmål nummer 00016 i Spørsmål-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3897-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="a3897-114">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="a3897-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a3897-115">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="a3897-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a3897-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="a3897-116">Click Save.</span></span>
7. <span data-ttu-id="a3897-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a3897-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="a3897-118">Angi sekvensen for spørreskjemaet til Betinget og gjør spørsmålet avhengig av det aktuelle spørsmålet</span><span class="sxs-lookup"><span data-stu-id="a3897-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="a3897-119">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="a3897-119">Click Edit.</span></span>
2. <span data-ttu-id="a3897-120">Utvid Oppsett-delen.</span><span class="sxs-lookup"><span data-stu-id="a3897-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="a3897-121">Velg Betinget i Spørsmålsrekkefølge-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3897-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="a3897-122">Klikk Betinget spørsmål.</span><span class="sxs-lookup"><span data-stu-id="a3897-122">Click Conditional question.</span></span>
5. <span data-ttu-id="a3897-123">Velg Spørsmål\Forklar hvorfor du besvarte det forrige spørsmålet slik du gjorde i treet.</span><span class="sxs-lookup"><span data-stu-id="a3897-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="a3897-124">Velg spørsmål 00009 i Hovedspørsmål-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3897-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="a3897-125">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="a3897-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="a3897-126">Angi svarsekvens-ID-en for svaralternativet som du vil gjøre spørsmålet avhengig av, i Svar-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3897-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="a3897-127">Angi for eksempel 1 for det første svaralternativet.</span><span class="sxs-lookup"><span data-stu-id="a3897-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="a3897-128">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="a3897-128">Click Save.</span></span>
10. <span data-ttu-id="a3897-129">I treet velger du Spørsmål\Jeg betales rettferdig for arbeidet jeg gjør.</span><span class="sxs-lookup"><span data-stu-id="a3897-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="a3897-130">Legg merke til at spørsmålstreet er oppdatert for å vise avhengigheten.</span><span class="sxs-lookup"><span data-stu-id="a3897-130">Note that the question tree updated to show the dependency.</span></span>  

