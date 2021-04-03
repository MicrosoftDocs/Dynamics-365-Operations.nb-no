---
title: Konfigurere permisjons- og fraværstyper
description: Definer permisjonstyper som de ansatte kan ta i Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: f1c3ced43b1f5693c5d5466fd97a20beb358fa20
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463340"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="70452-103">Konfigurere permisjons- og fraværstyper</span><span class="sxs-lookup"><span data-stu-id="70452-103">Configure leave and absence types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="70452-104">Permisjonstyper i Dynamics 365 Human Resources definerer de ulike typene fravær som ansatte kan rapportere.</span><span class="sxs-lookup"><span data-stu-id="70452-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="70452-105">Du kan skreddersy permisjonstyper i henhold til behovene i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="70452-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="70452-106">Eksempler på permisjonstyper omfatter:</span><span class="sxs-lookup"><span data-stu-id="70452-106">Examples of leave types include:</span></span>

- <span data-ttu-id="70452-107">Betalt avspasering (PTO)</span><span class="sxs-lookup"><span data-stu-id="70452-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="70452-108">Fravær uten lønn</span><span class="sxs-lookup"><span data-stu-id="70452-108">Unpaid leave</span></span>
- <span data-ttu-id="70452-109">Betalt ferie</span><span class="sxs-lookup"><span data-stu-id="70452-109">Paid vacation</span></span>
- <span data-ttu-id="70452-110">Sykepermisjon</span><span class="sxs-lookup"><span data-stu-id="70452-110">Sick leave</span></span>
- <span data-ttu-id="70452-111">Sykepermisjon</span><span class="sxs-lookup"><span data-stu-id="70452-111">Medical leave</span></span>
- <span data-ttu-id="70452-112">Familiepermisjon</span><span class="sxs-lookup"><span data-stu-id="70452-112">Family leave</span></span>
- <span data-ttu-id="70452-113">Kortsiktig uførhet</span><span class="sxs-lookup"><span data-stu-id="70452-113">Short-term disability</span></span>
- <span data-ttu-id="70452-114">Eksamenspermisjon</span><span class="sxs-lookup"><span data-stu-id="70452-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="70452-115">Legge til en permisjonstype</span><span class="sxs-lookup"><span data-stu-id="70452-115">Add a leave type</span></span>

1. <span data-ttu-id="70452-116">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="70452-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="70452-117">Under **Oppsett** velger du **Permisjons- og fraværstyper**.</span><span class="sxs-lookup"><span data-stu-id="70452-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="70452-118">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="70452-118">Select **New**.</span></span>

4. <span data-ttu-id="70452-119">Angi et navn for permisjonstypen under **Type**, velg en arbeidsflyt fra **Arbeidsflyt-ID**, og angi en beskrivelse under **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="70452-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="70452-120">I **Generelt** velger du **Ingen**, **Planlagt** eller **Ikke planlagt** fra rullegardinlisten **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="70452-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="70452-121">Velg en inntektskode fra rullegardinlisten **Inntektskode**.</span><span class="sxs-lookup"><span data-stu-id="70452-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="70452-122">Under **Årsakskode kreves** må du velge om du vil kreve en årsakskode.</span><span class="sxs-lookup"><span data-stu-id="70452-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="70452-123">Hvis du vil kreve årsakskoder, kan det hende at du må legge dem til.</span><span class="sxs-lookup"><span data-stu-id="70452-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="70452-124">Under **Årsakskoder** velger du **Legg til**, velger en årsakskode og merker av for **Aktivert** ved siden av den.</span><span class="sxs-lookup"><span data-stu-id="70452-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="70452-125">Under **Begrens tilgang til valgte roller** velger du om du vil begrense tilgangen.</span><span class="sxs-lookup"><span data-stu-id="70452-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="70452-126">Deretter velger du sikkerhetsrollene under **Sikkerhetsroller for denne permisjonstypen**.</span><span class="sxs-lookup"><span data-stu-id="70452-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="70452-127">Sikkerhetsrollene er definert i arbeidsflyten du valgte under **Arbeidsflyt-ID** tidligere i denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="70452-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="70452-128">Under **Kalenderfarge** velger du hvilken farge som skal vises på permisjons- og fraværskalendere for denne permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="70452-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="70452-129">Under **Suspensjonsforbindelser** velger du om du vil at denne permisjonstypen skal suspendere en annen permisjonstype eller bli deaktivert av en annen permisjonstype.</span><span class="sxs-lookup"><span data-stu-id="70452-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="70452-130">Når en fraværsforespørsel sendes for permisjonstypen "avbrudd", opprettes det automatisk et permisjonstidspunkt for den avbrutte permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="70452-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="70452-131">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="70452-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="70452-132">Konfigurer regler for permisjonstyper</span><span class="sxs-lookup"><span data-stu-id="70452-132">Configure leave type rules</span></span>

1. <span data-ttu-id="70452-133">Angi avrundingsalternativer for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="70452-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="70452-134">Alternativene omfatter **Ingen**, **Opp**, **Ned** og **Nærmest**.</span><span class="sxs-lookup"><span data-stu-id="70452-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="70452-135">Du kan også angi avrundingspresisjonen for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="70452-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="70452-136">Angi **Helligdagskorrigering** for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="70452-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="70452-137">Når du velger dette alternativet, bruker Human Resources antallet helligdager som faller på en arbeidsdag, for å bestemme hvordan det skal avsettes avspasering for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="70452-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="70452-138">Hvis for eksempel første juledag faller på en mandag, vil Human Resources trekke én dag fra permisjonstypen ved behandling av avsetninger.</span><span class="sxs-lookup"><span data-stu-id="70452-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="70452-139">Du angir helligdager i arbeidstidskalenderen.</span><span class="sxs-lookup"><span data-stu-id="70452-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="70452-140">Hvis du vil ha mer informasjon, kan du se [Opprette en driftstidskalender](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="70452-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="70452-141">Angi **Permisjonstypen overføring** som permisjonstype.</span><span class="sxs-lookup"><span data-stu-id="70452-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="70452-142">Når du velger dette alternativet, blir alle overføringssaldoer overført til den angitte permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="70452-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="70452-143">Permisjonstypen for overføring må også være inkludert i permisjons- og fraværsplanen.</span><span class="sxs-lookup"><span data-stu-id="70452-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="70452-144">Definer **Utløpsregler** for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="70452-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="70452-145">Når du konfigurerer dette alternativet, kan du velge dager eller måneder som enhet, og angi varigheten for utløpstiden.</span><span class="sxs-lookup"><span data-stu-id="70452-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="70452-146">Du kan også angi gjeldende dato for utløpsregelen.</span><span class="sxs-lookup"><span data-stu-id="70452-146">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="70452-147">Gyldighetsdatoen brukes til å avgjøre når den satsvise jobben som behandler permisjonsutløpet, eller datoen når regelen trer i kraft.</span><span class="sxs-lookup"><span data-stu-id="70452-147">The effective date is used to determine when to start running the batch job that processes the leave expiration, or the date when the rule takes effect.</span></span> <span data-ttu-id="70452-148">Selve utløpet vil alltid skje på startdatoen for permisjonsplanen når den satsvise jobben er satt til behandling.</span><span class="sxs-lookup"><span data-stu-id="70452-148">The expiration itself will always happen on the leave plan start date once the batch job is set to process.</span></span> <span data-ttu-id="70452-149">Startdatoen for planen kan for eksempel være 1.1.2020, men regelen vil ikke bli opprettet før 1.6.2020.</span><span class="sxs-lookup"><span data-stu-id="70452-149">For example, the plan start date may be 1/1/2020, but the rule wasn't created until 6/1/2020.</span></span> <span data-ttu-id="70452-150">Hvis du setter gyldighetsdatoen til 1.6.2020, behandles regelen ved neste års grense, nemlig 1.1.2021.</span><span class="sxs-lookup"><span data-stu-id="70452-150">By setting the effective date to 6/1/2020, the rule will be processed on the next year boundary, so 1/1/2021.</span></span> <span data-ttu-id="70452-151">Eventuelle permisjonssaldoer som finnes på utløpstidspunktet, trekkes fra permisjonstypen, og gjenspeiles i permisjonssaldoen.</span><span class="sxs-lookup"><span data-stu-id="70452-151">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
## <a name="see-also"></a><span data-ttu-id="70452-152">Se også</span><span class="sxs-lookup"><span data-stu-id="70452-152">See also</span></span>

- [<span data-ttu-id="70452-153">Oversikt over permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="70452-153">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="70452-154">Opprette en permisjons- og fraværsplan</span><span class="sxs-lookup"><span data-stu-id="70452-154">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="70452-155">Opprette en arbeidstidskalender</span><span class="sxs-lookup"><span data-stu-id="70452-155">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="70452-156">Suspender permisjon</span><span class="sxs-lookup"><span data-stu-id="70452-156">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
