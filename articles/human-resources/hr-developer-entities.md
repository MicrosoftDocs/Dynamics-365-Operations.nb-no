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
ms.openlocfilehash: c8e0288da16829c04a9b97c0a52caa8bd27cddf8
ms.sourcegitcommit: fde8045ea49d0cf26d5e7ac5a0da5c0d3d69d5bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/26/2020
ms.locfileid: "3166504"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="89863-103">Common Data Service-enheter</span><span class="sxs-lookup"><span data-stu-id="89863-103">Common Data Service entities</span></span>

<span data-ttu-id="89863-104">Microsoft Dynamics 365 Human Resources bruker Common Data Service til å aktivere scenarioer for utvidbarhet og integrering.</span><span class="sxs-lookup"><span data-stu-id="89863-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="89863-105">Hvis du vil ha mer informasjon om Common Data Service, kan du se [Hva er Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="89863-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="89863-106">Følgende Human Resources-enheter er tilgjengelige i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="89863-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="89863-107">Fordelsenheter</span><span class="sxs-lookup"><span data-stu-id="89863-107">Benefit entities</span></span>

| <span data-ttu-id="89863-108">Navn</span><span class="sxs-lookup"><span data-stu-id="89863-108">Name</span></span> | <span data-ttu-id="89863-109">Enhet</span><span class="sxs-lookup"><span data-stu-id="89863-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="89863-110">Fordelsberegningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="89863-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="89863-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="89863-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="89863-112">Lønnsperiode i fordelsberegningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="89863-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="89863-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="89863-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="89863-114">Beregningssats for fordeler</span><span class="sxs-lookup"><span data-stu-id="89863-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="89863-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="89863-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="89863-116">Detaljer om beregningssats for fordeler</span><span class="sxs-lookup"><span data-stu-id="89863-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="89863-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="89863-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="89863-118">Fordelsalternativ</span><span class="sxs-lookup"><span data-stu-id="89863-118">Benefit Option</span></span> | <span data-ttu-id="89863-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="89863-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="89863-120">Fordelsplan</span><span class="sxs-lookup"><span data-stu-id="89863-120">Benefit Plan</span></span> | <span data-ttu-id="89863-121">cdm_benefitplan (ikke aktivert for støtte for egendefinerte felt)</span><span class="sxs-lookup"><span data-stu-id="89863-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="89863-122">Fordelstype</span><span class="sxs-lookup"><span data-stu-id="89863-122">Benefit Type</span></span> | <span data-ttu-id="89863-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="89863-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="89863-124">Enheter for forretningsprosessoppgaver</span><span class="sxs-lookup"><span data-stu-id="89863-124">Business process tasks entities</span></span>

| <span data-ttu-id="89863-125">Navn</span><span class="sxs-lookup"><span data-stu-id="89863-125">Name</span></span> | <span data-ttu-id="89863-126">Enhet</span><span class="sxs-lookup"><span data-stu-id="89863-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="89863-127">Forretningsprosesskalender</span><span class="sxs-lookup"><span data-stu-id="89863-127">Business Process Calendar</span></span> | <span data-ttu-id="89863-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="89863-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="89863-129">Tilordning av forretningsprosessgruppe</span><span class="sxs-lookup"><span data-stu-id="89863-129">Business Process Group Assignment</span></span> | <span data-ttu-id="89863-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="89863-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="89863-131">Oppgavegruppe for forretningsprosessbibliotek</span><span class="sxs-lookup"><span data-stu-id="89863-131">Business Process Library Task Group</span></span> | <span data-ttu-id="89863-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="89863-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="89863-133">Forretningsprosessfase</span><span class="sxs-lookup"><span data-stu-id="89863-133">Business Process Stage</span></span> | <span data-ttu-id="89863-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="89863-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="89863-135">Topptekst for sjekklistemal</span><span class="sxs-lookup"><span data-stu-id="89863-135">Checklist Template Header</span></span> | <span data-ttu-id="89863-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="89863-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="89863-137">Oppgave for sjekklistemal</span><span class="sxs-lookup"><span data-stu-id="89863-137">Checklist Template Task</span></span> | <span data-ttu-id="89863-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="89863-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="89863-139">Kompensasjonsenheter</span><span class="sxs-lookup"><span data-stu-id="89863-139">Compensation entities</span></span>

| <span data-ttu-id="89863-140">Navn</span><span class="sxs-lookup"><span data-stu-id="89863-140">Name</span></span> | <span data-ttu-id="89863-141">Enhet</span><span class="sxs-lookup"><span data-stu-id="89863-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="89863-142">Fast plan for kompensasjon</span><span class="sxs-lookup"><span data-stu-id="89863-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="89863-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="89863-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="89863-144">Kompensasjonsrutenett</span><span class="sxs-lookup"><span data-stu-id="89863-144">Compensation Grid</span></span> | <span data-ttu-id="89863-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="89863-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="89863-146">Kompensasjonsnivå</span><span class="sxs-lookup"><span data-stu-id="89863-146">Compensation Level</span></span> | <span data-ttu-id="89863-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="89863-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="89863-148">Kompensasjon, lønnsfrekvens</span><span class="sxs-lookup"><span data-stu-id="89863-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="89863-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="89863-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="89863-150">Oppsett av referansepunkt for kompensasjon</span><span class="sxs-lookup"><span data-stu-id="89863-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="89863-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="89863-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="89863-152">Oppsettslinje for referansepunkt for kompensasjon</span><span class="sxs-lookup"><span data-stu-id="89863-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="89863-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="89863-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="89863-154">Kompensasjonsområde</span><span class="sxs-lookup"><span data-stu-id="89863-154">Compensation Region</span></span> | <span data-ttu-id="89863-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="89863-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="89863-156">Kompensasjonsstruktur</span><span class="sxs-lookup"><span data-stu-id="89863-156">Compensation Structure</span></span> | <span data-ttu-id="89863-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="89863-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="89863-158">Variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="89863-158">Compensation Variable Plan</span></span> | <span data-ttu-id="89863-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="89863-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="89863-160">Nivå for variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="89863-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="89863-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="89863-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="89863-162">Type variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="89863-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="89863-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="89863-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="89863-164">Fast kompensasjonshendelse</span><span class="sxs-lookup"><span data-stu-id="89863-164">Fixed Compensation Event</span></span> | <span data-ttu-id="89863-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="89863-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="89863-166">Overdragelsesregel</span><span class="sxs-lookup"><span data-stu-id="89863-166">Vesting Rule</span></span> | <span data-ttu-id="89863-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="89863-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="89863-168">Fast kompensasjon for arbeider</span><span class="sxs-lookup"><span data-stu-id="89863-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="89863-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="89863-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="89863-170">Organisasjonsenheter</span><span class="sxs-lookup"><span data-stu-id="89863-170">Organization entities</span></span>

| <span data-ttu-id="89863-171">Navn</span><span class="sxs-lookup"><span data-stu-id="89863-171">Name</span></span> | <span data-ttu-id="89863-172">Enhet</span><span class="sxs-lookup"><span data-stu-id="89863-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="89863-173">Avdeling</span><span class="sxs-lookup"><span data-stu-id="89863-173">Department</span></span> | <span data-ttu-id="89863-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="89863-174">cdm_department</span></span> |
| <span data-ttu-id="89863-175">Ansettelse</span><span class="sxs-lookup"><span data-stu-id="89863-175">Employment</span></span> | <span data-ttu-id="89863-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="89863-176">cdm_employment</span></span> |
| <span data-ttu-id="89863-177">Bedrift</span><span class="sxs-lookup"><span data-stu-id="89863-177">Company</span></span> | <span data-ttu-id="89863-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="89863-178">cdm_company</span></span> |
| <span data-ttu-id="89863-179">Stilling</span><span class="sxs-lookup"><span data-stu-id="89863-179">Job</span></span> | <span data-ttu-id="89863-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="89863-180">cdm_job</span></span> |
| <span data-ttu-id="89863-181">Jobbfunksjon</span><span class="sxs-lookup"><span data-stu-id="89863-181">Job Function</span></span> | <span data-ttu-id="89863-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="89863-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="89863-183">stilling</span><span class="sxs-lookup"><span data-stu-id="89863-183">Job Position</span></span> | <span data-ttu-id="89863-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="89863-184">cdm_jobposition</span></span> |
| <span data-ttu-id="89863-185">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="89863-185">Position Type</span></span> | <span data-ttu-id="89863-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="89863-186">cdm_positiontype</span></span> |
| <span data-ttu-id="89863-187">Stillingstilordning</span><span class="sxs-lookup"><span data-stu-id="89863-187">Position Worker Assignment</span></span> | <span data-ttu-id="89863-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="89863-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="89863-189">stillingsdimensjon</span><span class="sxs-lookup"><span data-stu-id="89863-189">Job Position Dimension</span></span> | <span data-ttu-id="89863-190">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="89863-190">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="89863-191">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="89863-191">Job Type</span></span> | <span data-ttu-id="89863-192">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="89863-192">cdm_jobtype</span></span> |
| <span data-ttu-id="89863-193">Språk</span><span class="sxs-lookup"><span data-stu-id="89863-193">Language</span></span> | <span data-ttu-id="89863-194">cdm_language</span><span class="sxs-lookup"><span data-stu-id="89863-194">cdm_language</span></span> |
| <span data-ttu-id="89863-195">Stillingstittel</span><span class="sxs-lookup"><span data-stu-id="89863-195">Title</span></span> | <span data-ttu-id="89863-196">cdm_title</span><span class="sxs-lookup"><span data-stu-id="89863-196">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="89863-197">Finansdimensjoner for **Stillingstype**, **Stillingstilordning** og **Ansettelse** gir enveis integrering til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="89863-197">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Common Data Service.</span></span> <span data-ttu-id="89863-198">Finansdimensjon-oppdateringer synkroniseres for øyeblikket ikke fra Common Data Service til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="89863-198">Financial dimensions updates currently can't synchronize from Common Data Service to Human Resources.</span></span> 

## <a name="leave-and-absence-entities"></a><span data-ttu-id="89863-199">Permisjons- og fraværsenheter</span><span class="sxs-lookup"><span data-stu-id="89863-199">Leave and absence entities</span></span>

| <span data-ttu-id="89863-200">Navn</span><span class="sxs-lookup"><span data-stu-id="89863-200">Name</span></span> | <span data-ttu-id="89863-201">Entity</span><span class="sxs-lookup"><span data-stu-id="89863-201">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="89863-202">Banktransaksjon for permisjon</span><span class="sxs-lookup"><span data-stu-id="89863-202">Leave Bank Transaction</span></span> | <span data-ttu-id="89863-203">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="89863-203">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="89863-204">Permisjonsregistrering</span><span class="sxs-lookup"><span data-stu-id="89863-204">Leave Enrollment</span></span> | <span data-ttu-id="89863-205">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="89863-205">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="89863-206">Permisjonsplan</span><span class="sxs-lookup"><span data-stu-id="89863-206">Leave Plan</span></span> | <span data-ttu-id="89863-207">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="89863-207">cdm_leaveplan</span></span> |
| <span data-ttu-id="89863-208">Permisjonsforespørsel</span><span class="sxs-lookup"><span data-stu-id="89863-208">Leave Request</span></span> | <span data-ttu-id="89863-209">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="89863-209">cdm_leaverequest</span></span> |
| <span data-ttu-id="89863-210">Detaljer for fraværsforespørsel</span><span class="sxs-lookup"><span data-stu-id="89863-210">Leave Request Detail</span></span> | <span data-ttu-id="89863-211">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="89863-211">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="89863-212">Permisjonstype</span><span class="sxs-lookup"><span data-stu-id="89863-212">Leave Type</span></span> | <span data-ttu-id="89863-213">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="89863-213">cdm_leavetype</span></span> |
| <span data-ttu-id="89863-214">Årsakskode for permisjonstype</span><span class="sxs-lookup"><span data-stu-id="89863-214">Leave Type Reason Code</span></span> | <span data-ttu-id="89863-215">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="89863-215">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="89863-216">Lønnsenheter</span><span class="sxs-lookup"><span data-stu-id="89863-216">Payroll entities</span></span>

| <span data-ttu-id="89863-217">Navn</span><span class="sxs-lookup"><span data-stu-id="89863-217">Name</span></span> | <span data-ttu-id="89863-218">Enhet</span><span class="sxs-lookup"><span data-stu-id="89863-218">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="89863-219">Lønnssyklus</span><span class="sxs-lookup"><span data-stu-id="89863-219">Pay Cycle</span></span> | <span data-ttu-id="89863-220">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="89863-220">cdm_paycycle</span></span> |
| <span data-ttu-id="89863-221">Lønnsperiode</span><span class="sxs-lookup"><span data-stu-id="89863-221">Pay Period</span></span> | <span data-ttu-id="89863-222">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="89863-222">cdm_payperiod</span></span> |
| <span data-ttu-id="89863-223">Inntektskode for lønn</span><span class="sxs-lookup"><span data-stu-id="89863-223">Payroll Earning Code</span></span> | <span data-ttu-id="89863-224">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="89863-224">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="89863-225">Bankkontobetaling</span><span class="sxs-lookup"><span data-stu-id="89863-225">Bank Account Disbursement</span></span> | <span data-ttu-id="89863-226">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="89863-226">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="89863-227">Avgiftsområde</span><span class="sxs-lookup"><span data-stu-id="89863-227">Tax Region</span></span> | <span data-ttu-id="89863-228">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="89863-228">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="89863-229">Arbeiderenheter</span><span class="sxs-lookup"><span data-stu-id="89863-229">Worker entities</span></span>

| <span data-ttu-id="89863-230">Navn</span><span class="sxs-lookup"><span data-stu-id="89863-230">Name</span></span> | <span data-ttu-id="89863-231">Enhet</span><span class="sxs-lookup"><span data-stu-id="89863-231">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="89863-232">Arbeider</span><span class="sxs-lookup"><span data-stu-id="89863-232">Worker</span></span> | <span data-ttu-id="89863-233">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="89863-233">cdm_worker</span></span> |
| <span data-ttu-id="89863-234">Arbeideradresse</span><span class="sxs-lookup"><span data-stu-id="89863-234">Worker Address</span></span> | <span data-ttu-id="89863-235">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="89863-235">cdm_workeraddress</span></span> |
| <span data-ttu-id="89863-236">Arbeiderens personopplysninger</span><span class="sxs-lookup"><span data-stu-id="89863-236">Worker Personal Detail</span></span> | <span data-ttu-id="89863-237">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="89863-237">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="89863-238">Personidentifikasjonsnummer for arbeider</span><span class="sxs-lookup"><span data-stu-id="89863-238">Worker Person Identification Number</span></span> | <span data-ttu-id="89863-239">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="89863-239">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="89863-240">Personidentifikasjonstype for arbeider</span><span class="sxs-lookup"><span data-stu-id="89863-240">Worker Person Identification Type</span></span> | <span data-ttu-id="89863-241">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="89863-241">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="89863-242">Arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="89863-242">Work Calendar</span></span> | <span data-ttu-id="89863-243">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="89863-243">cdm_workcalendar</span></span> |
| <span data-ttu-id="89863-244">Arbeidskalenderdag</span><span class="sxs-lookup"><span data-stu-id="89863-244">Work Calendar Day</span></span> | <span data-ttu-id="89863-245">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="89863-245">cdm_workcalendarday</span></span> |
| <span data-ttu-id="89863-246">Helligdag i arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="89863-246">Work Calendar Holiday</span></span> |<span data-ttu-id="89863-247">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="89863-247">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="89863-248">Ferielinje for arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="89863-248">Work Calendar Holiday Line</span></span> | <span data-ttu-id="89863-249">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="89863-249">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="89863-250">Tidsintervall for arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="89863-250">Work Calendar Time Interval</span></span> | <span data-ttu-id="89863-251">cdm_workcalendartimeinterval (ikke aktivert for støtte for egendefinerte felt)</span><span class="sxs-lookup"><span data-stu-id="89863-251">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="89863-252">Bankkonto for arbeider</span><span class="sxs-lookup"><span data-stu-id="89863-252">Worker Bank Account</span></span> | <span data-ttu-id="89863-253">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="89863-253">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="89863-254">Enheter for arbeideroppsett</span><span class="sxs-lookup"><span data-stu-id="89863-254">Worker setup entities</span></span>

| <span data-ttu-id="89863-255">Navn</span><span class="sxs-lookup"><span data-stu-id="89863-255">Name</span></span> | <span data-ttu-id="89863-256">Enhet</span><span class="sxs-lookup"><span data-stu-id="89863-256">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="89863-257">Veteranstatus</span><span class="sxs-lookup"><span data-stu-id="89863-257">Veteran Status</span></span> | <span data-ttu-id="89863-258">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="89863-258">cdm_veteranstatus</span></span> |
| <span data-ttu-id="89863-259">Etnisk opprinnelse</span><span class="sxs-lookup"><span data-stu-id="89863-259">Ethnic Origin</span></span> | <span data-ttu-id="89863-260">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="89863-260">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="89863-261">Årsakskode</span><span class="sxs-lookup"><span data-stu-id="89863-261">Reason Code</span></span> | <span data-ttu-id="89863-262">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="89863-262">cdm_reasoncode</span></span> |
| <span data-ttu-id="89863-263">Utstedende byrå for personidentifikasjon</span><span class="sxs-lookup"><span data-stu-id="89863-263">Person Identification Issuing Agency</span></span> | <span data-ttu-id="89863-264">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="89863-264">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="89863-265">Kompetanseenheter</span><span class="sxs-lookup"><span data-stu-id="89863-265">Competency entities</span></span>

| <span data-ttu-id="89863-266">Navn</span><span class="sxs-lookup"><span data-stu-id="89863-266">Name</span></span> | <span data-ttu-id="89863-267">Enhet</span><span class="sxs-lookup"><span data-stu-id="89863-267">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="89863-268">Kompetansetype</span><span class="sxs-lookup"><span data-stu-id="89863-268">Skill Type</span></span> | <span data-ttu-id="89863-269">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="89863-269">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="89863-270">Enhetsrelasjonsmodeller</span><span class="sxs-lookup"><span data-stu-id="89863-270">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="89863-271">Arbeider</span><span class="sxs-lookup"><span data-stu-id="89863-271">Worker</span></span>

![Arbeider](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="89863-273">Jobb og stilling</span><span class="sxs-lookup"><span data-stu-id="89863-273">Job and Job Position</span></span>

![Jobb og stilling](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="89863-275">Fordeler</span><span class="sxs-lookup"><span data-stu-id="89863-275">Benefits</span></span>

![Fordeler](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="89863-277">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="89863-277">Compensation</span></span>

![Kompensasjon](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="89863-279">Permisjon</span><span class="sxs-lookup"><span data-stu-id="89863-279">Leave</span></span>

![Permisjon](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="89863-281">Arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="89863-281">Work Calendar</span></span>

![Arbeidskalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="89863-283">Se også</span><span class="sxs-lookup"><span data-stu-id="89863-283">See also</span></span>

[<span data-ttu-id="89863-284">Velge en dataintegreringsteknologi</span><span class="sxs-lookup"><span data-stu-id="89863-284">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="89863-285">Konfigurere Common Data Service-integrering</span><span class="sxs-lookup"><span data-stu-id="89863-285">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)
