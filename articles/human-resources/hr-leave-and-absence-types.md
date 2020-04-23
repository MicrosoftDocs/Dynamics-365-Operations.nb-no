---
title: Konfigurere permisjons- og fraværstyper
description: Definer permisjonstyper som de ansatte kan ta i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df6e34fe6a23e6f0a8307a035752a35a15a3431c
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198056"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="23d4a-103">Konfigurere permisjons- og fraværstyper</span><span class="sxs-lookup"><span data-stu-id="23d4a-103">Configure leave and absence types</span></span>

<span data-ttu-id="23d4a-104">Permisjonstyper i Dynamics 365 Human Resources definerer de ulike typene fravær som ansatte kan rapportere.</span><span class="sxs-lookup"><span data-stu-id="23d4a-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="23d4a-105">Du kan skreddersy permisjonstyper i henhold til behovene i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="23d4a-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="23d4a-106">Eksempler på permisjonstyper omfatter:</span><span class="sxs-lookup"><span data-stu-id="23d4a-106">Examples of leave types include:</span></span>

- <span data-ttu-id="23d4a-107">Betalt avspasering (PTO)</span><span class="sxs-lookup"><span data-stu-id="23d4a-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="23d4a-108">Fravær uten lønn</span><span class="sxs-lookup"><span data-stu-id="23d4a-108">Unpaid leave</span></span>
- <span data-ttu-id="23d4a-109">Betalt ferie</span><span class="sxs-lookup"><span data-stu-id="23d4a-109">Paid vacation</span></span>
- <span data-ttu-id="23d4a-110">Sykepermisjon</span><span class="sxs-lookup"><span data-stu-id="23d4a-110">Sick leave</span></span>
- <span data-ttu-id="23d4a-111">Sykepermisjon</span><span class="sxs-lookup"><span data-stu-id="23d4a-111">Medical leave</span></span>
- <span data-ttu-id="23d4a-112">Familiepermisjon</span><span class="sxs-lookup"><span data-stu-id="23d4a-112">Family leave</span></span>
- <span data-ttu-id="23d4a-113">Kortsiktig uførhet</span><span class="sxs-lookup"><span data-stu-id="23d4a-113">Short-term disability</span></span>
- <span data-ttu-id="23d4a-114">Eksamenspermisjon</span><span class="sxs-lookup"><span data-stu-id="23d4a-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="23d4a-115">Legge til en permisjonstype</span><span class="sxs-lookup"><span data-stu-id="23d4a-115">Add a leave type</span></span>

1. <span data-ttu-id="23d4a-116">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="23d4a-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="23d4a-117">Under **Oppsett**velger du **Permisjons- og fraværstyper**.</span><span class="sxs-lookup"><span data-stu-id="23d4a-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="23d4a-118">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="23d4a-118">Select **New**.</span></span>

4. <span data-ttu-id="23d4a-119">Angi et navn for permisjonstypen under **Type**, velg en arbeidsflyt fra **Arbeidsflyt-ID**, og angi en beskrivelse under **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="23d4a-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="23d4a-120">I **Generelt** velger du **Ingen**, **Planlagt** eller **Ikke planlagt** fra rullegardinlisten **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="23d4a-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="23d4a-121">Velg en inntektskode fra rullegardinlisten **Inntektskode**.</span><span class="sxs-lookup"><span data-stu-id="23d4a-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="23d4a-122">Under **Årsakskode kreves** må du velge om du vil kreve en årsakskode.</span><span class="sxs-lookup"><span data-stu-id="23d4a-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="23d4a-123">Hvis du vil kreve årsakskoder, kan det hende at du må legge dem til.</span><span class="sxs-lookup"><span data-stu-id="23d4a-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="23d4a-124">Under **Årsakskoder** velger du **Legg til**, velger en årsakskode og merker av for **Aktivert** ved siden av den.</span><span class="sxs-lookup"><span data-stu-id="23d4a-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="23d4a-125">Under **Begrens tilgang til valgte roller** velger du om du vil begrense tilgangen.</span><span class="sxs-lookup"><span data-stu-id="23d4a-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="23d4a-126">Deretter velger du sikkerhetsrollene under **Sikkerhetsroller for denne permisjonstypen**.</span><span class="sxs-lookup"><span data-stu-id="23d4a-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="23d4a-127">Sikkerhetsrollene er definert i arbeidsflyten du valgte under **Arbeidsflyt-ID** tidligere i denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="23d4a-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="23d4a-128">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="23d4a-128">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="23d4a-129">Konfigurer regler for permisjonstyper</span><span class="sxs-lookup"><span data-stu-id="23d4a-129">Configure leave type rules</span></span>

1. <span data-ttu-id="23d4a-130">Angi avrundingsalternativer for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="23d4a-130">Set rounding options for the leave type.</span></span> <span data-ttu-id="23d4a-131">Alternativene omfatter **Ingen**, **Opp**, **Ned** og **Nærmest**.</span><span class="sxs-lookup"><span data-stu-id="23d4a-131">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="23d4a-132">Du kan også angi avrundingspresisjonen for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="23d4a-132">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="23d4a-133">Angi **Helligdagskorrigering** for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="23d4a-133">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="23d4a-134">Når du velger dette alternativet, bruker Human Resources antallet helligdager som faller på en arbeidsdag, for å bestemme hvordan det skal avsettes avspasering for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="23d4a-134">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="23d4a-135">Hvis for eksempel første juledag faller på en mandag, vil Human Resources trekke én dag fra permisjonstypen ved behandling av avsetninger.</span><span class="sxs-lookup"><span data-stu-id="23d4a-135">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="23d4a-136">Du angir helligdager i arbeidstidskalenderen.</span><span class="sxs-lookup"><span data-stu-id="23d4a-136">You set holidays in the working time calendar.</span></span> <span data-ttu-id="23d4a-137">Hvis du vil ha mer informasjon, kan du se [Opprette en driftstidskalender](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="23d4a-137">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
## <a name="configure-preview-features"></a><span data-ttu-id="23d4a-138">Konfigurere forhåndsversjonsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="23d4a-138">Configure preview features</span></span>

<span data-ttu-id="23d4a-139">Hvis du har aktivert forhåndsversjonsfunksjoner for permisjon og fravær, må du konfigurere innstillinger for dem også.</span><span class="sxs-lookup"><span data-stu-id="23d4a-139">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="23d4a-140">Velg permisjonstypen for overføringssaldoer som skal overføres.</span><span class="sxs-lookup"><span data-stu-id="23d4a-140">Choose the leave type for carry forward balances to be transferred to.</span></span> <span data-ttu-id="23d4a-141">Du kan også opprette en ny permisjonstype for overføring.</span><span class="sxs-lookup"><span data-stu-id="23d4a-141">You can also create a new leave type for carry forward.</span></span> 

## <a name="see-also"></a><span data-ttu-id="23d4a-142">Se også</span><span class="sxs-lookup"><span data-stu-id="23d4a-142">See also</span></span>

- [<span data-ttu-id="23d4a-143">Oversikt over permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="23d4a-143">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="23d4a-144">Opprette en permisjons- og fraværsplan</span><span class="sxs-lookup"><span data-stu-id="23d4a-144">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="23d4a-145">Opprette en driftstidskalender</span><span class="sxs-lookup"><span data-stu-id="23d4a-145">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
