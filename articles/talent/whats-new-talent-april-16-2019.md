---
title: Hva er nytt eller endret i Dynamics 365 Talent (16. april 2019)?
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a37436eb15ee4c561d5d0c15c90e37815cb80860
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897931"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-16-2019"></a><span data-ttu-id="bd2a6-103">Hva er nytt eller endret i Dynamics 365 Talent (16. april 2019)?</span><span class="sxs-lookup"><span data-stu-id="bd2a6-103">What's new or changed in Dynamics 365 Talent (April 16, 2019)</span></span>

<span data-ttu-id="bd2a6-104">Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="bd2a6-105">Endringer i Attract</span><span class="sxs-lookup"><span data-stu-id="bd2a6-105">Changes in Attract</span></span>

### <a name="process-auditing"></a><span data-ttu-id="bd2a6-106">Prosessovervåking</span><span class="sxs-lookup"><span data-stu-id="bd2a6-106">Process auditing</span></span>

<span data-ttu-id="bd2a6-107">Du kan nå spore endringer som gjøres i kandidater, ledige stillinger og stillingssøknader.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-107">You can now track the changes made to candidates, job openings, and job applications.</span></span> <span data-ttu-id="bd2a6-108">Hvis du vil ha mer informasjon, kan du se [Spore endringer i rekrutteringsdata](process-auditing.md).</span><span class="sxs-lookup"><span data-stu-id="bd2a6-108">For more information, see [Track changes in recruiting data](process-auditing.md).</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="bd2a6-109">Endringer i Onboard</span><span class="sxs-lookup"><span data-stu-id="bd2a6-109">Changes in Onboard</span></span>

<span data-ttu-id="bd2a6-110">Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-110">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="bd2a6-111">Endringer i Core HR</span><span class="sxs-lookup"><span data-stu-id="bd2a6-111">Changes in Core HR</span></span>

<span data-ttu-id="bd2a6-112">Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2239.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-112">Changes described in this section apply to build number 8.1.2239.</span></span> <span data-ttu-id="bd2a6-113">Tall i parentes refererer til støttenumre i Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="bd2a6-113">Numbers in parentheses refer to support numbers in Lifecycle Services (LCS).</span></span>

### <a name="compensation-region-compensation-level-benefit-option-and-skill-type-entities-in-common-data-service-updated-to-include-customer-field-support"></a><span data-ttu-id="bd2a6-114">Enhetene Kompensasjonsområde, Kompensasjonsnivå, Fordelsalternativ og Kompetansetype i Common Data Service er oppdatert for å inkludere støtte for kundefelt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-114">Compensation region, Compensation level, Benefit option and Skill type entities in Common Data Service updated to include customer field support</span></span>

<span data-ttu-id="bd2a6-115">I denne versjonen har disse Common Data Service-enhetene blitt oppdatert slik at de inkluderer muligheten for å inkludere egendefinert felt som legges til via Talent: (Core HR).</span><span class="sxs-lookup"><span data-stu-id="bd2a6-115">With this release, these Common Data Service entities have been updated to include the ability to include custom field added through Talent: Core HR.</span></span>

### <a name="new-common-data-service-entity-support-for-compensation-vesting-rules-compensation-variable-plan-variable-compensation"></a><span data-ttu-id="bd2a6-116">Støtte for ny Common Data Service-enhet: Kompensasjon, overdragelsesregler, Variabel plan for kompensasjon, Variabel kompensasjon</span><span class="sxs-lookup"><span data-stu-id="bd2a6-116">New Common Data Service entity support for: Compensation vesting rules, Compensation variable plan, Variable compensation</span></span>

<span data-ttu-id="bd2a6-117">I denne versjonen er enhetene Kompensasjon, overdragelsesregler, Variabel plan for kompensasjon og Variabel kompensasjon lagt til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-117">With this release, Compensation vesting rules, Compensation variable plan, and Variable compensation entities have been added to Common Data Service.</span></span> <span data-ttu-id="bd2a6-118">Disse enhetene støtter også egendefinerte felt som legges til via Talent: (Core HR).</span><span class="sxs-lookup"><span data-stu-id="bd2a6-118">These entities also support custom fields added through Talent: Core HR.</span></span>

### <a name="powerbi-refresh-issues-314342"></a><span data-ttu-id="bd2a6-119">PowerBI-oppdateringsproblemer (314342)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-119">PowerBI refresh issues (314342)</span></span>

<span data-ttu-id="bd2a6-120">Denne endringen løser et problem med PowerBI-rapporter slik at de oppdateres riktig.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-120">This change corrects an issue with PowerBI reports refreshing correctly.</span></span>

### <a name="unable-to-click-directly-through-on-transition-tasks-in-employee-self-service-303309"></a><span data-ttu-id="bd2a6-121">Kan ikke klikke direkte gjennom på overgangsoppgaver i ansattselvbetjening (303309)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-121">Unable to click directly through on transition tasks in employee self-service (303309)</span></span>

<span data-ttu-id="bd2a6-122">Denne endringen gjør at brukere med ansattrollen kan velge og oppdatere overgangsoppgaver fra gjøremålslisten i Talent.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-122">This change enables users with the employee role to select and update transition tasks from the Talent to-do list.</span></span>

### <a name="performance-feedback-email-message-updated-309615"></a><span data-ttu-id="bd2a6-123">E-postmelding med tilbakemelding om resultat er oppdatert (309615)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-123">Performance feedback email message updated (309615)</span></span>

<span data-ttu-id="bd2a6-124">Med denne endringen vises en bekreftelsesmelding når tilbakemeldingen er sendt inn.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-124">With this change, a confirmation message displays when feedback is successfully submitted.</span></span>

### <a name="missing-tables-in-word-template-308048"></a><span data-ttu-id="bd2a6-125">Manglende tabeller i Word-mal (308048)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-125">Missing tables in Word template (308048)</span></span>

<span data-ttu-id="bd2a6-126">Med denne endringen vil bare kompetansen for den valgte medarbeideren vises i Word-dokumentet når du oppretter en Word-mal med ansatt- og kompetanseinformasjon.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-126">With this change, when creating a Word template with employee and skill information, only the skills for the selected employee appear in the Word document.</span></span>

### <a name="when-applying-an-offboarding-checklist-an-error-is-displayed-299877"></a><span data-ttu-id="bd2a6-127">Når du bruker en sjekkliste for jobbavslutning, vises en feil.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-127">When applying an offboarding checklist an error is displayed.</span></span> <span data-ttu-id="bd2a6-128">(299877)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-128">(299877)</span></span>

<span data-ttu-id="bd2a6-129">Denne endringen løser et problem når det brukes en sjekkliste for jobbavslutning direkte fra arbeiderskjemaet.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-129">This change corrects an issue when applying an offboarding checklist directly from the worker form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="bd2a6-130">I forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="bd2a6-130">In preview</span></span>

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a><span data-ttu-id="bd2a6-131">Tillate angivelse av årsakskoder for permisjonstyper</span><span class="sxs-lookup"><span data-stu-id="bd2a6-131">Allow reason codes to be specified on leave types</span></span>

<span data-ttu-id="bd2a6-132">Organisasjoner må kanskje ha tilleggsinformasjon om fraværsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-132">Organizations might need additional information about time-off requests.</span></span> <span data-ttu-id="bd2a6-133">Du kan nå angi årsakskoder for fraværstyper og gi de ansatte mulighet til å velge en årsakskode i fraværsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-133">You can now specify reason codes for leave types and enable employees to select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a><span data-ttu-id="bd2a6-134">Kreve årsakskoder for bestemte fraværstyper i forespørsler om fravær</span><span class="sxs-lookup"><span data-stu-id="bd2a6-134">Require reason codes for certain leave types on time-off requests</span></span>

<span data-ttu-id="bd2a6-135">Organisasjoner kan kreve årsakskoder for bestemte fraværstyper når ansatte sender fraværsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-135">Organizations might require reason codes for specific leave types when employees submit time off.</span></span> <span data-ttu-id="bd2a6-136">Dette kan være på grunn av firmapolicy eller lovbestemte krav.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-136">This might be due to company policy or regulatory requirements.</span></span> <span data-ttu-id="bd2a6-137">Du kan nå angi hvilke permisjonstyper som krever en årsakskode, og du kan kreve at ansatte må angi en årsakskode for fraværstypen i forespørsler om fravær.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-137">You can now specify which leave types require a reason code, and you can require employees to provide a reason code for the leave type on their time-off requests.</span></span>

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a><span data-ttu-id="bd2a6-138">Angi transaksjonsliste for permisjon og fravær for HR</span><span class="sxs-lookup"><span data-stu-id="bd2a6-138">Provide leave and absence transaction list for HR</span></span>

<span data-ttu-id="bd2a6-139">Sporing av ansattes fravær og forståelse av hvordan fravær beregnes, hjelper ikke bare HR med å svare på ansattspørsmål, men sørger også for nøyaktige fraværstildelinger for ansatte.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-139">Tracking employee time off and understanding how time off is calculated not only helps HR answer employee questions, but also ensures accurate time-off awards for employees.</span></span> <span data-ttu-id="bd2a6-140">HR har nå en ny oversikt over transaksjonene (tildelinger, avsetninger, justeringer og forespørsler), slik at det er mulig å vise årsakene bak saldoer.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-140">HR now has a new view into the transactions (grants, accruals, adjustments, and requests) to see the reasons behind balances.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="bd2a6-141">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="bd2a6-141">Coming soon</span></span>

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a><span data-ttu-id="bd2a6-142">Forbedringer av brukergrensesnittet for kontroll av dupliserte ansatte</span><span class="sxs-lookup"><span data-stu-id="bd2a6-142">Improvements to the user interface for duplicate employee check</span></span>

<span data-ttu-id="bd2a6-143">Med denne endringen oppdages duplikater når du angir navnefelt, og statusen viser hvor mange duplikater som ble funnet.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-143">With this change, duplicates are detected as you enter name fields, and a status displays the number of duplicates found.</span></span> <span data-ttu-id="bd2a6-144">Du kan velge den angitte lenken for å åpne en ny side for å vurdere om du vil bruke resultatet som ble funnet.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-144">You can select the provided link to open a new page to evaluate whether to use the detected match.</span></span> <span data-ttu-id="bd2a6-145">For å unngå å forstyrre dataregistreringen åpnes duplikatskjemaet ikke automatisk.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-145">To avoid interrupting data entry, the duplicates form doesn't automatically open.</span></span>

### <a name="email-support-for-alerts"></a><span data-ttu-id="bd2a6-146">E-poststøtte for varsler</span><span class="sxs-lookup"><span data-stu-id="bd2a6-146">Email support for alerts</span></span>

<span data-ttu-id="bd2a6-147">Med platform update 25 for Finance and Operations kan brukere opprette varslingsregler som automatisk leverer e-postmeldinger til kontakter når de utløses av en hendelse.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-147">With Platform update 25 for Finance and Operations, users can create alert rules that automatically send email notifications to contacts when triggered by an event.</span></span>


