---
title: Common Data Service-enheter
description: Microsoft Dynamics 365 Human Resources bruker Common Data Service til å aktivere scenarioer for utvidbarhet og integrering.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 6879a45dd1fcc1ba718747aaaf0d7936c2eac49f
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087352"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="eaddf-103">Common Data Service-enheter</span><span class="sxs-lookup"><span data-stu-id="eaddf-103">Common Data Service entities</span></span>

<span data-ttu-id="eaddf-104">Microsoft Dynamics 365 Human Resources bruker Common Data Service til å aktivere scenarioer for utvidbarhet og integrering.</span><span class="sxs-lookup"><span data-stu-id="eaddf-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="eaddf-105">Hvis du vil ha mer informasjon om Common Data Service, kan du se [Hva er Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="eaddf-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="eaddf-106">Følgende Human Resources-enheter er tilgjengelige i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="eaddf-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="eaddf-107">Fordelsenheter</span><span class="sxs-lookup"><span data-stu-id="eaddf-107">Benefit entities</span></span>

| <span data-ttu-id="eaddf-108">Navn</span><span class="sxs-lookup"><span data-stu-id="eaddf-108">Name</span></span> | <span data-ttu-id="eaddf-109">Enhet</span><span class="sxs-lookup"><span data-stu-id="eaddf-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="eaddf-110">Fordelsberegningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="eaddf-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="eaddf-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="eaddf-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="eaddf-112">Lønnsperiode i fordelsberegningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="eaddf-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="eaddf-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="eaddf-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="eaddf-114">Beregningssats for fordeler</span><span class="sxs-lookup"><span data-stu-id="eaddf-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="eaddf-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="eaddf-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="eaddf-116">Detaljer om beregningssats for fordeler</span><span class="sxs-lookup"><span data-stu-id="eaddf-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="eaddf-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="eaddf-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="eaddf-118">Fordelsalternativ</span><span class="sxs-lookup"><span data-stu-id="eaddf-118">Benefit Option</span></span> | <span data-ttu-id="eaddf-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="eaddf-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="eaddf-120">Fordelsplan</span><span class="sxs-lookup"><span data-stu-id="eaddf-120">Benefit Plan</span></span> | <span data-ttu-id="eaddf-121">cdm_benefitplan (ikke aktivert for støtte for egendefinerte felt)</span><span class="sxs-lookup"><span data-stu-id="eaddf-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="eaddf-122">Fordelstype</span><span class="sxs-lookup"><span data-stu-id="eaddf-122">Benefit Type</span></span> | <span data-ttu-id="eaddf-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="eaddf-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="eaddf-124">Enheter for forretningsprosessoppgaver</span><span class="sxs-lookup"><span data-stu-id="eaddf-124">Business process tasks entities</span></span>

| <span data-ttu-id="eaddf-125">Navn</span><span class="sxs-lookup"><span data-stu-id="eaddf-125">Name</span></span> | <span data-ttu-id="eaddf-126">Enhet</span><span class="sxs-lookup"><span data-stu-id="eaddf-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="eaddf-127">Forretningsprosesskalender</span><span class="sxs-lookup"><span data-stu-id="eaddf-127">Business Process Calendar</span></span> | <span data-ttu-id="eaddf-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="eaddf-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="eaddf-129">Tilordning av forretningsprosessgruppe</span><span class="sxs-lookup"><span data-stu-id="eaddf-129">Business Process Group Assignment</span></span> | <span data-ttu-id="eaddf-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="eaddf-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="eaddf-131">Oppgavegruppe for forretningsprosessbibliotek</span><span class="sxs-lookup"><span data-stu-id="eaddf-131">Business Process Library Task Group</span></span> | <span data-ttu-id="eaddf-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="eaddf-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="eaddf-133">Forretningsprosessfase</span><span class="sxs-lookup"><span data-stu-id="eaddf-133">Business Process Stage</span></span> | <span data-ttu-id="eaddf-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="eaddf-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="eaddf-135">Topptekst for sjekklistemal</span><span class="sxs-lookup"><span data-stu-id="eaddf-135">Checklist Template Header</span></span> | <span data-ttu-id="eaddf-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="eaddf-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="eaddf-137">Oppgave for sjekklistemal</span><span class="sxs-lookup"><span data-stu-id="eaddf-137">Checklist Template Task</span></span> | <span data-ttu-id="eaddf-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="eaddf-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="eaddf-139">Kompensasjonsenheter</span><span class="sxs-lookup"><span data-stu-id="eaddf-139">Compensation entities</span></span>

| <span data-ttu-id="eaddf-140">Navn</span><span class="sxs-lookup"><span data-stu-id="eaddf-140">Name</span></span> | <span data-ttu-id="eaddf-141">Enhet</span><span class="sxs-lookup"><span data-stu-id="eaddf-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="eaddf-142">Fast plan for kompensasjon</span><span class="sxs-lookup"><span data-stu-id="eaddf-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="eaddf-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="eaddf-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="eaddf-144">Kompensasjonsrutenett</span><span class="sxs-lookup"><span data-stu-id="eaddf-144">Compensation Grid</span></span> | <span data-ttu-id="eaddf-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="eaddf-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="eaddf-146">Kompensasjonsnivå</span><span class="sxs-lookup"><span data-stu-id="eaddf-146">Compensation Level</span></span> | <span data-ttu-id="eaddf-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="eaddf-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="eaddf-148">Kompensasjon, lønnsfrekvens</span><span class="sxs-lookup"><span data-stu-id="eaddf-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="eaddf-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="eaddf-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="eaddf-150">Oppsett av referansepunkt for kompensasjon</span><span class="sxs-lookup"><span data-stu-id="eaddf-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="eaddf-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="eaddf-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="eaddf-152">Oppsettslinje for referansepunkt for kompensasjon</span><span class="sxs-lookup"><span data-stu-id="eaddf-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="eaddf-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="eaddf-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="eaddf-154">Kompensasjonsområde</span><span class="sxs-lookup"><span data-stu-id="eaddf-154">Compensation Region</span></span> | <span data-ttu-id="eaddf-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="eaddf-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="eaddf-156">Kompensasjonsstruktur</span><span class="sxs-lookup"><span data-stu-id="eaddf-156">Compensation Structure</span></span> | <span data-ttu-id="eaddf-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="eaddf-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="eaddf-158">Variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="eaddf-158">Compensation Variable Plan</span></span> | <span data-ttu-id="eaddf-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="eaddf-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="eaddf-160">Nivå for variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="eaddf-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="eaddf-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="eaddf-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="eaddf-162">Type variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="eaddf-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="eaddf-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="eaddf-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="eaddf-164">Fast kompensasjonshendelse</span><span class="sxs-lookup"><span data-stu-id="eaddf-164">Fixed Compensation Event</span></span> | <span data-ttu-id="eaddf-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="eaddf-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="eaddf-166">Overdragelsesregel</span><span class="sxs-lookup"><span data-stu-id="eaddf-166">Vesting Rule</span></span> | <span data-ttu-id="eaddf-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="eaddf-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="eaddf-168">Fast kompensasjon for arbeider</span><span class="sxs-lookup"><span data-stu-id="eaddf-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="eaddf-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="eaddf-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="eaddf-170">Organisasjonsenheter</span><span class="sxs-lookup"><span data-stu-id="eaddf-170">Organization entities</span></span>

| <span data-ttu-id="eaddf-171">Navn</span><span class="sxs-lookup"><span data-stu-id="eaddf-171">Name</span></span> | <span data-ttu-id="eaddf-172">Enhet</span><span class="sxs-lookup"><span data-stu-id="eaddf-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="eaddf-173">Avdeling</span><span class="sxs-lookup"><span data-stu-id="eaddf-173">Department</span></span> | <span data-ttu-id="eaddf-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="eaddf-174">cdm_department</span></span> |
| <span data-ttu-id="eaddf-175">Ansettelse</span><span class="sxs-lookup"><span data-stu-id="eaddf-175">Employment</span></span> | <span data-ttu-id="eaddf-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="eaddf-176">cdm_employment</span></span> |
| <span data-ttu-id="eaddf-177">Bedrift</span><span class="sxs-lookup"><span data-stu-id="eaddf-177">Company</span></span> | <span data-ttu-id="eaddf-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="eaddf-178">cdm_company</span></span> |
| <span data-ttu-id="eaddf-179">Stilling</span><span class="sxs-lookup"><span data-stu-id="eaddf-179">Job</span></span> | <span data-ttu-id="eaddf-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="eaddf-180">cdm_job</span></span> |
| <span data-ttu-id="eaddf-181">Jobbfunksjon</span><span class="sxs-lookup"><span data-stu-id="eaddf-181">Job Function</span></span> | <span data-ttu-id="eaddf-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="eaddf-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="eaddf-183">stilling</span><span class="sxs-lookup"><span data-stu-id="eaddf-183">Job Position</span></span> | <span data-ttu-id="eaddf-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="eaddf-184">cdm_jobposition</span></span> |
| <span data-ttu-id="eaddf-185">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="eaddf-185">Position Type</span></span> | <span data-ttu-id="eaddf-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="eaddf-186">cdm_positiontype</span></span> |
| <span data-ttu-id="eaddf-187">Stillingstilordning</span><span class="sxs-lookup"><span data-stu-id="eaddf-187">Position Worker Assignment</span></span> | <span data-ttu-id="eaddf-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="eaddf-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="eaddf-189">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="eaddf-189">Job Type</span></span> | <span data-ttu-id="eaddf-190">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="eaddf-190">cdm_jobtype</span></span> |
| <span data-ttu-id="eaddf-191">Språk</span><span class="sxs-lookup"><span data-stu-id="eaddf-191">Language</span></span> | <span data-ttu-id="eaddf-192">cdm_language</span><span class="sxs-lookup"><span data-stu-id="eaddf-192">cdm_language</span></span> |

## <a name="leave-and-absence-entities"></a><span data-ttu-id="eaddf-193">Permisjons- og fraværsenheter</span><span class="sxs-lookup"><span data-stu-id="eaddf-193">Leave and absence entities</span></span>

| <span data-ttu-id="eaddf-194">Navn</span><span class="sxs-lookup"><span data-stu-id="eaddf-194">Name</span></span> | <span data-ttu-id="eaddf-195">Enhet</span><span class="sxs-lookup"><span data-stu-id="eaddf-195">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="eaddf-196">Permisjonsbanktransaksjon</span><span class="sxs-lookup"><span data-stu-id="eaddf-196">Leave Bank Transaction</span></span> | <span data-ttu-id="eaddf-197">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="eaddf-197">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="eaddf-198">Permisjonsregistrering</span><span class="sxs-lookup"><span data-stu-id="eaddf-198">Leave Enrollment</span></span> | <span data-ttu-id="eaddf-199">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="eaddf-199">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="eaddf-200">Permisjonsplan</span><span class="sxs-lookup"><span data-stu-id="eaddf-200">Leave Plan</span></span> | <span data-ttu-id="eaddf-201">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="eaddf-201">cdm_leaveplan</span></span> |
| <span data-ttu-id="eaddf-202">Permisjonsforespørsel</span><span class="sxs-lookup"><span data-stu-id="eaddf-202">Leave Request</span></span> | <span data-ttu-id="eaddf-203">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="eaddf-203">cdm_leaverequest</span></span> |
| <span data-ttu-id="eaddf-204">Detaljer for fraværsforespørsel</span><span class="sxs-lookup"><span data-stu-id="eaddf-204">Leave Request Detail</span></span> | <span data-ttu-id="eaddf-205">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="eaddf-205">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="eaddf-206">Permisjonstype</span><span class="sxs-lookup"><span data-stu-id="eaddf-206">Leave Type</span></span> | <span data-ttu-id="eaddf-207">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="eaddf-207">cdm_leavetype</span></span> |
| <span data-ttu-id="eaddf-208">Årsakskode for permisjonstype</span><span class="sxs-lookup"><span data-stu-id="eaddf-208">Leave Type Reason Code</span></span> | <span data-ttu-id="eaddf-209">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="eaddf-209">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="eaddf-210">Lønnsenheter</span><span class="sxs-lookup"><span data-stu-id="eaddf-210">Payroll entities</span></span>

| <span data-ttu-id="eaddf-211">Navn</span><span class="sxs-lookup"><span data-stu-id="eaddf-211">Name</span></span> | <span data-ttu-id="eaddf-212">Enhet</span><span class="sxs-lookup"><span data-stu-id="eaddf-212">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="eaddf-213">Lønnssyklus</span><span class="sxs-lookup"><span data-stu-id="eaddf-213">Pay Cycle</span></span> | <span data-ttu-id="eaddf-214">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="eaddf-214">cdm_paycycle</span></span> |
| <span data-ttu-id="eaddf-215">Lønnsperiode</span><span class="sxs-lookup"><span data-stu-id="eaddf-215">Pay Period</span></span> | <span data-ttu-id="eaddf-216">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="eaddf-216">cdm_payperiod</span></span> |
| <span data-ttu-id="eaddf-217">Inntektskode for lønn</span><span class="sxs-lookup"><span data-stu-id="eaddf-217">Payroll Earning Code</span></span> | <span data-ttu-id="eaddf-218">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="eaddf-218">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="eaddf-219">Bankkontobetaling</span><span class="sxs-lookup"><span data-stu-id="eaddf-219">Bank Account Disbursement</span></span> | <span data-ttu-id="eaddf-220">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="eaddf-220">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="eaddf-221">Avgiftsområde</span><span class="sxs-lookup"><span data-stu-id="eaddf-221">Tax Region</span></span> | <span data-ttu-id="eaddf-222">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="eaddf-222">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="eaddf-223">Arbeiderenheter</span><span class="sxs-lookup"><span data-stu-id="eaddf-223">Worker entities</span></span>

| <span data-ttu-id="eaddf-224">Navn</span><span class="sxs-lookup"><span data-stu-id="eaddf-224">Name</span></span> | <span data-ttu-id="eaddf-225">Enhet</span><span class="sxs-lookup"><span data-stu-id="eaddf-225">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="eaddf-226">Arbeider</span><span class="sxs-lookup"><span data-stu-id="eaddf-226">Worker</span></span> | <span data-ttu-id="eaddf-227">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="eaddf-227">cdm_worker</span></span> |
| <span data-ttu-id="eaddf-228">Arbeideradresse</span><span class="sxs-lookup"><span data-stu-id="eaddf-228">Worker Address</span></span> | <span data-ttu-id="eaddf-229">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="eaddf-229">cdm_workeraddress</span></span> |
| <span data-ttu-id="eaddf-230">Arbeiderens personopplysninger</span><span class="sxs-lookup"><span data-stu-id="eaddf-230">Worker Personal Detail</span></span> | <span data-ttu-id="eaddf-231">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="eaddf-231">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="eaddf-232">Personidentifikasjonsnummer for arbeider</span><span class="sxs-lookup"><span data-stu-id="eaddf-232">Worker Person Identification Number</span></span> | <span data-ttu-id="eaddf-233">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="eaddf-233">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="eaddf-234">Personidentifikasjonstype for arbeider</span><span class="sxs-lookup"><span data-stu-id="eaddf-234">Worker Person Identification Type</span></span> | <span data-ttu-id="eaddf-235">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="eaddf-235">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="eaddf-236">Arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="eaddf-236">Work Calendar</span></span> | <span data-ttu-id="eaddf-237">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="eaddf-237">cdm_workcalendar</span></span> |
| <span data-ttu-id="eaddf-238">Arbeidskalenderdag</span><span class="sxs-lookup"><span data-stu-id="eaddf-238">Work Calendar Day</span></span> | <span data-ttu-id="eaddf-239">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="eaddf-239">cdm_workcalendarday</span></span> |
| <span data-ttu-id="eaddf-240">Helligdag i arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="eaddf-240">Work Calendar Holiday</span></span> |<span data-ttu-id="eaddf-241">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="eaddf-241">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="eaddf-242">Ferielinje for arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="eaddf-242">Work Calendar Holiday Line</span></span> | <span data-ttu-id="eaddf-243">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="eaddf-243">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="eaddf-244">Tidsintervall for arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="eaddf-244">Work Calendar Time Interval</span></span> | <span data-ttu-id="eaddf-245">cdm_workcalendartimeinterval (ikke aktivert for støtte for egendefinerte felt)</span><span class="sxs-lookup"><span data-stu-id="eaddf-245">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="eaddf-246">Bankkonto for arbeider</span><span class="sxs-lookup"><span data-stu-id="eaddf-246">Worker Bank Account</span></span> | <span data-ttu-id="eaddf-247">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="eaddf-247">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="eaddf-248">Enheter for arbeideroppsett</span><span class="sxs-lookup"><span data-stu-id="eaddf-248">Worker setup entities</span></span>

| <span data-ttu-id="eaddf-249">Navn</span><span class="sxs-lookup"><span data-stu-id="eaddf-249">Name</span></span> | <span data-ttu-id="eaddf-250">Enhet</span><span class="sxs-lookup"><span data-stu-id="eaddf-250">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="eaddf-251">Veteranstatus</span><span class="sxs-lookup"><span data-stu-id="eaddf-251">Veteran Status</span></span> | <span data-ttu-id="eaddf-252">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="eaddf-252">cdm_veteranstatus</span></span> |
| <span data-ttu-id="eaddf-253">Etnisk opprinnelse</span><span class="sxs-lookup"><span data-stu-id="eaddf-253">Ethnic Origin</span></span> | <span data-ttu-id="eaddf-254">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="eaddf-254">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="eaddf-255">Årsakskode</span><span class="sxs-lookup"><span data-stu-id="eaddf-255">Reason Code</span></span> | <span data-ttu-id="eaddf-256">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="eaddf-256">cdm_reasoncode</span></span> |
| <span data-ttu-id="eaddf-257">Utstedende byrå for personidentifikasjon</span><span class="sxs-lookup"><span data-stu-id="eaddf-257">Person Identification Issuing Agency</span></span> | <span data-ttu-id="eaddf-258">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="eaddf-258">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="eaddf-259">Kompetanseenheter</span><span class="sxs-lookup"><span data-stu-id="eaddf-259">Competency entities</span></span>

| <span data-ttu-id="eaddf-260">Navn</span><span class="sxs-lookup"><span data-stu-id="eaddf-260">Name</span></span> | <span data-ttu-id="eaddf-261">Enhet</span><span class="sxs-lookup"><span data-stu-id="eaddf-261">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="eaddf-262">Kompetansetype</span><span class="sxs-lookup"><span data-stu-id="eaddf-262">Skill Type</span></span> | <span data-ttu-id="eaddf-263">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="eaddf-263">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="eaddf-264">Enhetsrelasjonsmodeller</span><span class="sxs-lookup"><span data-stu-id="eaddf-264">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="eaddf-265">Arbeider</span><span class="sxs-lookup"><span data-stu-id="eaddf-265">Worker</span></span>

![Arbeider](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="eaddf-267">Jobb og stilling</span><span class="sxs-lookup"><span data-stu-id="eaddf-267">Job and Job Position</span></span>

![Jobb og stilling](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="eaddf-269">Fordeler</span><span class="sxs-lookup"><span data-stu-id="eaddf-269">Benefits</span></span>

![Fordeler](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="eaddf-271">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="eaddf-271">Compensation</span></span>

![Kompensasjon](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="eaddf-273">Permisjon</span><span class="sxs-lookup"><span data-stu-id="eaddf-273">Leave</span></span>

![Permisjon](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="eaddf-275">Arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="eaddf-275">Work Calendar</span></span>

![Arbeidskalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="eaddf-277">Se også</span><span class="sxs-lookup"><span data-stu-id="eaddf-277">See also</span></span>

[<span data-ttu-id="eaddf-278">Velge en dataintegreringsteknologi</span><span class="sxs-lookup"><span data-stu-id="eaddf-278">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="eaddf-279">Konfigurere Common Data Service-integrering</span><span class="sxs-lookup"><span data-stu-id="eaddf-279">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)