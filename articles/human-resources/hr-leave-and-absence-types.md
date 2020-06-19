---
title: Konfigurere permisjons- og fraværstyper
description: Definer permisjonstyper som de ansatte kan ta i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1802938f54a1d78e6ea60572a76177a037192ae0
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428599"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="88289-103">Konfigurere permisjons- og fraværstyper</span><span class="sxs-lookup"><span data-stu-id="88289-103">Configure leave and absence types</span></span>

<span data-ttu-id="88289-104">Permisjonstyper i Dynamics 365 Human Resources definerer de ulike typene fravær som ansatte kan rapportere.</span><span class="sxs-lookup"><span data-stu-id="88289-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="88289-105">Du kan skreddersy permisjonstyper i henhold til behovene i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="88289-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="88289-106">Eksempler på permisjonstyper omfatter:</span><span class="sxs-lookup"><span data-stu-id="88289-106">Examples of leave types include:</span></span>

- <span data-ttu-id="88289-107">Betalt avspasering (PTO)</span><span class="sxs-lookup"><span data-stu-id="88289-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="88289-108">Fravær uten lønn</span><span class="sxs-lookup"><span data-stu-id="88289-108">Unpaid leave</span></span>
- <span data-ttu-id="88289-109">Betalt ferie</span><span class="sxs-lookup"><span data-stu-id="88289-109">Paid vacation</span></span>
- <span data-ttu-id="88289-110">Sykepermisjon</span><span class="sxs-lookup"><span data-stu-id="88289-110">Sick leave</span></span>
- <span data-ttu-id="88289-111">Sykepermisjon</span><span class="sxs-lookup"><span data-stu-id="88289-111">Medical leave</span></span>
- <span data-ttu-id="88289-112">Familiepermisjon</span><span class="sxs-lookup"><span data-stu-id="88289-112">Family leave</span></span>
- <span data-ttu-id="88289-113">Kortsiktig uførhet</span><span class="sxs-lookup"><span data-stu-id="88289-113">Short-term disability</span></span>
- <span data-ttu-id="88289-114">Eksamenspermisjon</span><span class="sxs-lookup"><span data-stu-id="88289-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="88289-115">Legge til en permisjonstype</span><span class="sxs-lookup"><span data-stu-id="88289-115">Add a leave type</span></span>

1. <span data-ttu-id="88289-116">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="88289-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="88289-117">Under **Oppsett**velger du **Permisjons- og fraværstyper**.</span><span class="sxs-lookup"><span data-stu-id="88289-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="88289-118">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="88289-118">Select **New**.</span></span>

4. <span data-ttu-id="88289-119">Angi et navn for permisjonstypen under **Type**, velg en arbeidsflyt fra **Arbeidsflyt-ID**, og angi en beskrivelse under **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="88289-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="88289-120">I **Generelt** velger du **Ingen**, **Planlagt** eller **Ikke planlagt** fra rullegardinlisten **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="88289-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="88289-121">Velg en inntektskode fra rullegardinlisten **Inntektskode**.</span><span class="sxs-lookup"><span data-stu-id="88289-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="88289-122">Under **Årsakskode kreves** må du velge om du vil kreve en årsakskode.</span><span class="sxs-lookup"><span data-stu-id="88289-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="88289-123">Hvis du vil kreve årsakskoder, kan det hende at du må legge dem til.</span><span class="sxs-lookup"><span data-stu-id="88289-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="88289-124">Under **Årsakskoder** velger du **Legg til**, velger en årsakskode og merker av for **Aktivert** ved siden av den.</span><span class="sxs-lookup"><span data-stu-id="88289-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="88289-125">Under **Begrens tilgang til valgte roller** velger du om du vil begrense tilgangen.</span><span class="sxs-lookup"><span data-stu-id="88289-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="88289-126">Deretter velger du sikkerhetsrollene under **Sikkerhetsroller for denne permisjonstypen**.</span><span class="sxs-lookup"><span data-stu-id="88289-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="88289-127">Sikkerhetsrollene er definert i arbeidsflyten du valgte under **Arbeidsflyt-ID** tidligere i denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="88289-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="88289-128">Under **Suspensjonsforbindelser** velger du om du vil at denne permisjonstypen skal suspendere en annen permisjonstype eller bli deaktivert av en annen permisjonstype.</span><span class="sxs-lookup"><span data-stu-id="88289-128">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="88289-129">Når en fraværsforespørsel sendes for permisjonstypen "avbrudd", opprettes det automatisk et permisjonstidspunkt for den avbrutte permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="88289-129">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="88289-130">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="88289-130">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="88289-131">Konfigurer regler for permisjonstyper</span><span class="sxs-lookup"><span data-stu-id="88289-131">Configure leave type rules</span></span>

1. <span data-ttu-id="88289-132">Angi avrundingsalternativer for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="88289-132">Set rounding options for the leave type.</span></span> <span data-ttu-id="88289-133">Alternativene omfatter **Ingen**, **Opp**, **Ned** og **Nærmest**.</span><span class="sxs-lookup"><span data-stu-id="88289-133">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="88289-134">Du kan også angi avrundingspresisjonen for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="88289-134">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="88289-135">Angi **Helligdagskorrigering** for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="88289-135">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="88289-136">Når du velger dette alternativet, bruker Human Resources antallet helligdager som faller på en arbeidsdag, for å bestemme hvordan det skal avsettes avspasering for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="88289-136">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="88289-137">Hvis for eksempel første juledag faller på en mandag, vil Human Resources trekke én dag fra permisjonstypen ved behandling av avsetninger.</span><span class="sxs-lookup"><span data-stu-id="88289-137">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="88289-138">Du angir helligdager i arbeidstidskalenderen.</span><span class="sxs-lookup"><span data-stu-id="88289-138">You set holidays in the working time calendar.</span></span> <span data-ttu-id="88289-139">Hvis du vil ha mer informasjon, kan du se [Opprette en driftstidskalender](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="88289-139">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="88289-140">Angi **Permisjonstypen overføring** som permisjonstype.</span><span class="sxs-lookup"><span data-stu-id="88289-140">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="88289-141">Når du velger dette alternativet, blir alle overføringssaldoer overført til den angitte permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="88289-141">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="88289-142">Permisjonstypen for overføring må også være inkludert i permisjons- og fraværsplanen.</span><span class="sxs-lookup"><span data-stu-id="88289-142">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="88289-143">Definer **Utløpsregler** for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="88289-143">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="88289-144">Når du konfigurerer dette alternativet, kan du velge dager eller måneder som enhet, og angi varigheten for utløpstiden.</span><span class="sxs-lookup"><span data-stu-id="88289-144">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="88289-145">Du kan også angi gjeldende dato for utløpsregelen.</span><span class="sxs-lookup"><span data-stu-id="88289-145">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="88289-146">Eventuelle permisjonssaldoer som finnes på utløpstidspunktet, trekkes fra permisjonstypen, og gjenspeiles i permisjonssaldoen.</span><span class="sxs-lookup"><span data-stu-id="88289-146">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
 
## <a name="see-also"></a><span data-ttu-id="88289-147">Se også</span><span class="sxs-lookup"><span data-stu-id="88289-147">See also</span></span>

- [<span data-ttu-id="88289-148">Oversikt over permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="88289-148">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="88289-149">Opprette en permisjons- og fraværsplan</span><span class="sxs-lookup"><span data-stu-id="88289-149">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="88289-150">Opprette en arbeidstidskalender</span><span class="sxs-lookup"><span data-stu-id="88289-150">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="88289-151">Suspender permisjon</span><span class="sxs-lookup"><span data-stu-id="88289-151">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)

