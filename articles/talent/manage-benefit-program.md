---
title: Definere og administrere et fordelsprogram
description: "Personale inneholder et sett med verktøy som kan brukes til å definere og vedlikeholde fordeler, fradrag og arbeideres kompensasjonsplaner som en organisasjon tilbyr eller behandler for sine arbeidere. Denne artikkelen inneholder informasjon om hvordan du definerer og behandler fordeler."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fc325b519299098a4f8257c013bce0842237f9ea
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---

# <a name="define-and-manage-a-benefits-program"></a><span data-ttu-id="0cae7-104">Definere og administrere et fordelsprogram</span><span class="sxs-lookup"><span data-stu-id="0cae7-104">Define and manage a benefits program</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0cae7-105">Personale inneholder et sett med verktøy som kan brukes til å definere og vedlikeholde fordeler, fradrag og arbeideres kompensasjonsplaner som en organisasjon tilbyr eller behandler for sine arbeidere.</span><span class="sxs-lookup"><span data-stu-id="0cae7-105">Human resources provides a set of tools that can be used to set up and maintain benefits, deductions, and workers' compensation plans that an organization offers or processes for its workers.</span></span> <span data-ttu-id="0cae7-106">Dette emnert inneholder informasjon om hvordan du definerer og behandler fordeler.</span><span class="sxs-lookup"><span data-stu-id="0cae7-106">This topic provides information about how to set up and manage benefits.</span></span>

<a name="benefit-setup"></a><span data-ttu-id="0cae7-107">Fordelsoppsett</span><span class="sxs-lookup"><span data-stu-id="0cae7-107">Benefit setup</span></span>
-------------

<span data-ttu-id="0cae7-108">Før arbeidere kan registreres i fordeler, må du opprette elementene i hver enkelt fordel.</span><span class="sxs-lookup"><span data-stu-id="0cae7-108">Before workers can be enrolled in benefits, you must create the elements of each benefit.</span></span> <span data-ttu-id="0cae7-109">Disse elementene kombinerer lignende fordelsplaner og definer standardinnstillinger, for eksempel fradragssatser og regnskapsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="0cae7-109">These elements combine similar benefit plans and define default settings, such as deduction rates and accounting details.</span></span> <span data-ttu-id="0cae7-110">Mange av disse innstillingene kan justeres når arbeidere senere registreres i fordelsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="0cae7-110">Many of these settings can be adjusted when workers are later enrolled in the benefit.</span></span> <span data-ttu-id="0cae7-111">En organisasjon kan tilby flere registreringsalternativer for hver fordelsplanen, eller en arbeider kan avstå fra registrering i planen.</span><span class="sxs-lookup"><span data-stu-id="0cae7-111">For each benefit plan, an organization can offer several enrollment options, or a worker can waive enrollment in the plan.</span></span> 

<span data-ttu-id="0cae7-112">[![Prosessflyt for fordel](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span><span class="sxs-lookup"><span data-stu-id="0cae7-112">[![Benefit process flow](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span></span>

## <a name="benefit-elements"></a><span data-ttu-id="0cae7-113">Fordelselementer</span><span class="sxs-lookup"><span data-stu-id="0cae7-113">Benefit elements</span></span>
<span data-ttu-id="0cae7-114">Før du begynner å opprette fordeler og registrer arbeidere i dem, må du definere elementene som utgjør en fordel: type, plan og alternativer.</span><span class="sxs-lookup"><span data-stu-id="0cae7-114">Before you begin to create to create benefits and enroll workers in them, you must define the elements that make up a benefit: the type, plan, and options.</span></span>

-   <span data-ttu-id="0cae7-115">**Type** – En samling av planer for en bestemt fordel, for eksempel en medisinsk fordel eller en parkeringsfordel.</span><span class="sxs-lookup"><span data-stu-id="0cae7-115">**Type** – A collection of plans for a specific benefit, such as medical or parking.</span></span>
-   <span data-ttu-id="0cae7-116">**Plan** – En bestemt fordel som leveres på kontrakt av en leverandør.</span><span class="sxs-lookup"><span data-stu-id="0cae7-116">**Plan** – A specific benefit that is contracted from a provider.</span></span>
-   <span data-ttu-id="0cae7-117">**Alternativ** – Dekningsgraden, for eksempel bare den ansatte eller den ansatte og ektefelle/partner.</span><span class="sxs-lookup"><span data-stu-id="0cae7-117">**Option** – The coverage level, such as employee only, or employee and spouse/partner.</span></span>

<span data-ttu-id="0cae7-118">For hver type fordeler, for eksempel syn eller tannlege, kan en organisasjon tilby én eller flere planer til arbeidere.</span><span class="sxs-lookup"><span data-stu-id="0cae7-118">For each type of benefit, such as vision or dental, an organization can offer one or more plans to its workers.</span></span> <span data-ttu-id="0cae7-119">Organisasjonen kan tilby forskjellige alternativer for hver plan.</span><span class="sxs-lookup"><span data-stu-id="0cae7-119">For each plan, the organization can offer different options.</span></span> <span data-ttu-id="0cae7-120">Arbeidere kan for eksempel kjøpe tilleggsdekning for livsforsikring på én, to eller tre ganger sin årlige lønnen.</span><span class="sxs-lookup"><span data-stu-id="0cae7-120">For example, workers can buy additional term life insurance coverage at one, two, or three times their yearly salary.</span></span> <span data-ttu-id="0cae7-121">Hver kombinasjon av en plan og alternativene blir en fordel som arbeidere kan registrere seg for.</span><span class="sxs-lookup"><span data-stu-id="0cae7-121">Each combination of a plan and options becomes a benefit that workers can enroll in.</span></span> 

<span data-ttu-id="0cae7-122">[![bilde av fordel](./media/benefit-pic.png)](./media/benefit-pic.png)</span><span class="sxs-lookup"><span data-stu-id="0cae7-122">[![benefit pic](./media/benefit-pic.png)](./media/benefit-pic.png)</span></span>

## <a name="eligibility"></a><span data-ttu-id="0cae7-123">Rettighet</span><span class="sxs-lookup"><span data-stu-id="0cae7-123">Eligibility</span></span>
<span data-ttu-id="0cae7-124">Mange faktorer avgjør arbeideres kvalifikasjon for ulike typer fordeler som en arbeidsgiver tilbyr.</span><span class="sxs-lookup"><span data-stu-id="0cae7-124">Many factors determine worker eligibility for the various types of benefits that an employer offers.</span></span> <span data-ttu-id="0cae7-125">Når du oppretter en fordel i Microsoft Talent, kan du angi type rettighet som gjelder for denne fordelen.</span><span class="sxs-lookup"><span data-stu-id="0cae7-125">When you create a benefit in Microsoft Talent, you can set the type of eligibility that applies to that benefit.</span></span> 

<span data-ttu-id="0cae7-126">Du kan gjøre en fordel tilgjengelig for alle arbeidere.</span><span class="sxs-lookup"><span data-stu-id="0cae7-126">You can make a benefit available to all workers.</span></span> <span data-ttu-id="0cae7-127">Enkelte selskaper tilbyr for eksempel parkeringskort til alle ansatte som en fordelsskatt.</span><span class="sxs-lookup"><span data-stu-id="0cae7-127">For example, some companies offer parking passes to all employees as a fringe benefit.</span></span> <span data-ttu-id="0cae7-128">Når du oppretter denne fordelen, setter du kvalifikasjonen til **Alle arbeidere er kvalifiserte**.</span><span class="sxs-lookup"><span data-stu-id="0cae7-128">When you create this benefit, you set the eligibility to **All workers are eligible**.</span></span> 

<span data-ttu-id="0cae7-129">For andre fordeler, for eksempel utlegg og avgiftslettelser, gjelder ikke berettiget.</span><span class="sxs-lookup"><span data-stu-id="0cae7-129">For other benefits, such as garnishments and tax levies, eligibility doesn't apply.</span></span> <span data-ttu-id="0cae7-130">Når du oppretter disse typer av fordeler, setter du berettigelsen til **Omgå berettigelsesprosess**.</span><span class="sxs-lookup"><span data-stu-id="0cae7-130">Whey you create these types of benefits, you set the eligibility to **Bypass eligibility process**.</span></span> 

<span data-ttu-id="0cae7-131">Fordelsrettigheter kan til slutt være regelbasert.</span><span class="sxs-lookup"><span data-stu-id="0cae7-131">Finally, benefit eligibility can be rule-based.</span></span> <span data-ttu-id="0cae7-132">Et selskap kan for eksempel tilby to typer livsforsikringsfordel til ansatte.</span><span class="sxs-lookup"><span data-stu-id="0cae7-132">For example, a company offers two types of life insurance benefit to employees.</span></span> <span data-ttu-id="0cae7-133">Ansatte i ledelsen er kvalifisert for én livsforsikringsplan, mens alle andre heltidsansatte er kvalifisert for den andre livsforsikringsplanen.</span><span class="sxs-lookup"><span data-stu-id="0cae7-133">Executive employees are eligible for one life insurance plan, whereas all other full-time employees are eligible for the other life insurance plan.</span></span> <span data-ttu-id="0cae7-134">I Talent kan du opprette en fordelsrettighetsregel for å søke etter alle ansatte i ledelsen, og en annen regel til å finne alle andre heltidsansatte og deretter bruke disse reglene til den aktuelle fordelen.</span><span class="sxs-lookup"><span data-stu-id="0cae7-134">In Talent, you can create a benefit eligibility rule to find all executive employees and another rule to find all other full-time employees, and then apply those rules to the appropriate benefit.</span></span>

## <a name="enrollment"></a><span data-ttu-id="0cae7-135">Registrering</span><span class="sxs-lookup"><span data-stu-id="0cae7-135">Enrollment</span></span>
<span data-ttu-id="0cae7-136">Når du har opprettet fordelene som organisasjonen tilbyr, og fastslått rettigheten, kan du registrere arbeiderne i fordeler.</span><span class="sxs-lookup"><span data-stu-id="0cae7-136">After you've created the benefits that your organization offers and determined eligibility, you can enroll your workers in benefits.</span></span> <span data-ttu-id="0cae7-137">Du kan registrere én enkelt arbeider i fordeler eller du kan registrere mange arbeidere i én eller flere fordeler i én enkelt prosess.</span><span class="sxs-lookup"><span data-stu-id="0cae7-137">You can enroll a single worker in benefits, or you can enroll many workers in one or more benefits during a single process.</span></span> 

<span data-ttu-id="0cae7-138">Noen ganger stopper en organisasjon å tilby bestemte fordeler.</span><span class="sxs-lookup"><span data-stu-id="0cae7-138">Sometimes, an organization stops offering certain benefits.</span></span> <span data-ttu-id="0cae7-139">I dette tilfellet må du oppdatere fordelen og arbeidere som er registrert.</span><span class="sxs-lookup"><span data-stu-id="0cae7-139">In this case, you must update the benefit and the workers who are enrolled in.</span></span> <span data-ttu-id="0cae7-140">Utløpsdato for massefordeler lar deg samtidig endre utløpsdatoen både for en fordel og registreringene av arbeidere for denne fordelen.</span><span class="sxs-lookup"><span data-stu-id="0cae7-140">Mass benefit expiration lets you change the expiration date of both a benefit and the worker enrollments for that benefit at the same time.</span></span> <span data-ttu-id="0cae7-141">Du kan også velge flere arbeidere som er registrert i en fordel, og endre sluttdatoen for dekningen deres.</span><span class="sxs-lookup"><span data-stu-id="0cae7-141">You can also select multiple workers who are enrolled in a benefit and change the ending date of their coverage.</span></span> 

<span data-ttu-id="0cae7-142">På samme måte kan du med masseutvidelse av fordel utvide utløpsdatoen for både en fordel og arbeiderregistreringene for denne fordelen hvis du vil tilby en fordel lenger enn opprinnelig planlagt.</span><span class="sxs-lookup"><span data-stu-id="0cae7-142">Similarly, mass benefit extension lets you extend the expiration date of both a benefit and the worker enrollments for that benefit if you decide to offer a benefit longer than you originally planned.</span></span>

<a name="additional-resources"></a><span data-ttu-id="0cae7-143">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0cae7-143">Additional resources</span></span>
--------

[<span data-ttu-id="0cae7-144">Policyer for fordelsrettigheter</span><span class="sxs-lookup"><span data-stu-id="0cae7-144">Benefit eligibility policies</span></span>](benefit-eligibility-policies.md)




