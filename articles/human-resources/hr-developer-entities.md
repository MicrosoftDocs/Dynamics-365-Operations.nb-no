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
ms.openlocfilehash: 988fa0b6d39a49b973626a8a0abe83c546f42297
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530012"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="7fa8d-103">Common Data Service-enheter</span><span class="sxs-lookup"><span data-stu-id="7fa8d-103">Common Data Service entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7fa8d-104">Microsoft Dynamics 365 Human Resources bruker Common Data Service til å aktivere scenarioer for utvidbarhet og integrering.</span><span class="sxs-lookup"><span data-stu-id="7fa8d-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="7fa8d-105">Hvis du vil ha mer informasjon om Common Data Service, kan du se [Hva er Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="7fa8d-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="7fa8d-106">Følgende Human Resources-enheter er tilgjengelige i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7fa8d-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="7fa8d-107">Fordelsenheter</span><span class="sxs-lookup"><span data-stu-id="7fa8d-107">Benefit entities</span></span>

| <span data-ttu-id="7fa8d-108">Navn</span><span class="sxs-lookup"><span data-stu-id="7fa8d-108">Name</span></span> | <span data-ttu-id="7fa8d-109">Enhet</span><span class="sxs-lookup"><span data-stu-id="7fa8d-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="7fa8d-110">Fordelsberegningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="7fa8d-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="7fa8d-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="7fa8d-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="7fa8d-112">Lønnsperiode i fordelsberegningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="7fa8d-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="7fa8d-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="7fa8d-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="7fa8d-114">Beregningssats for fordeler</span><span class="sxs-lookup"><span data-stu-id="7fa8d-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="7fa8d-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="7fa8d-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="7fa8d-116">Detaljer om beregningssats for fordeler</span><span class="sxs-lookup"><span data-stu-id="7fa8d-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="7fa8d-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="7fa8d-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="7fa8d-118">Fordelsalternativ</span><span class="sxs-lookup"><span data-stu-id="7fa8d-118">Benefit Option</span></span> | <span data-ttu-id="7fa8d-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="7fa8d-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="7fa8d-120">Fordelsplan</span><span class="sxs-lookup"><span data-stu-id="7fa8d-120">Benefit Plan</span></span> | <span data-ttu-id="7fa8d-121">cdm_benefitplan (ikke aktivert for støtte for egendefinerte felt)</span><span class="sxs-lookup"><span data-stu-id="7fa8d-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="7fa8d-122">Fordelstype</span><span class="sxs-lookup"><span data-stu-id="7fa8d-122">Benefit Type</span></span> | <span data-ttu-id="7fa8d-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="7fa8d-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="7fa8d-124">Enheter for forretningsprosessoppgaver</span><span class="sxs-lookup"><span data-stu-id="7fa8d-124">Business process tasks entities</span></span>

| <span data-ttu-id="7fa8d-125">Navn</span><span class="sxs-lookup"><span data-stu-id="7fa8d-125">Name</span></span> | <span data-ttu-id="7fa8d-126">Enhet</span><span class="sxs-lookup"><span data-stu-id="7fa8d-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="7fa8d-127">Forretningsprosesskalender</span><span class="sxs-lookup"><span data-stu-id="7fa8d-127">Business Process Calendar</span></span> | <span data-ttu-id="7fa8d-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="7fa8d-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="7fa8d-129">Tilordning av forretningsprosessgruppe</span><span class="sxs-lookup"><span data-stu-id="7fa8d-129">Business Process Group Assignment</span></span> | <span data-ttu-id="7fa8d-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="7fa8d-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="7fa8d-131">Oppgavegruppe for forretningsprosessbibliotek</span><span class="sxs-lookup"><span data-stu-id="7fa8d-131">Business Process Library Task Group</span></span> | <span data-ttu-id="7fa8d-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="7fa8d-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="7fa8d-133">Forretningsprosessfase</span><span class="sxs-lookup"><span data-stu-id="7fa8d-133">Business Process Stage</span></span> | <span data-ttu-id="7fa8d-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="7fa8d-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="7fa8d-135">Topptekst for sjekklistemal</span><span class="sxs-lookup"><span data-stu-id="7fa8d-135">Checklist Template Header</span></span> | <span data-ttu-id="7fa8d-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="7fa8d-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="7fa8d-137">Oppgave for sjekklistemal</span><span class="sxs-lookup"><span data-stu-id="7fa8d-137">Checklist Template Task</span></span> | <span data-ttu-id="7fa8d-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="7fa8d-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="7fa8d-139">Kompensasjonsenheter</span><span class="sxs-lookup"><span data-stu-id="7fa8d-139">Compensation entities</span></span>

| <span data-ttu-id="7fa8d-140">Navn</span><span class="sxs-lookup"><span data-stu-id="7fa8d-140">Name</span></span> | <span data-ttu-id="7fa8d-141">Enhet</span><span class="sxs-lookup"><span data-stu-id="7fa8d-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="7fa8d-142">Fast plan for kompensasjon</span><span class="sxs-lookup"><span data-stu-id="7fa8d-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="7fa8d-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="7fa8d-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="7fa8d-144">Kompensasjonsrutenett</span><span class="sxs-lookup"><span data-stu-id="7fa8d-144">Compensation Grid</span></span> | <span data-ttu-id="7fa8d-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="7fa8d-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="7fa8d-146">Kompensasjonsnivå</span><span class="sxs-lookup"><span data-stu-id="7fa8d-146">Compensation Level</span></span> | <span data-ttu-id="7fa8d-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="7fa8d-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="7fa8d-148">Kompensasjon, lønnsfrekvens</span><span class="sxs-lookup"><span data-stu-id="7fa8d-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="7fa8d-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="7fa8d-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="7fa8d-150">Oppsett av referansepunkt for kompensasjon</span><span class="sxs-lookup"><span data-stu-id="7fa8d-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="7fa8d-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="7fa8d-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="7fa8d-152">Oppsettslinje for referansepunkt for kompensasjon</span><span class="sxs-lookup"><span data-stu-id="7fa8d-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="7fa8d-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="7fa8d-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="7fa8d-154">Kompensasjonsområde</span><span class="sxs-lookup"><span data-stu-id="7fa8d-154">Compensation Region</span></span> | <span data-ttu-id="7fa8d-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="7fa8d-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="7fa8d-156">Kompensasjonsstruktur</span><span class="sxs-lookup"><span data-stu-id="7fa8d-156">Compensation Structure</span></span> | <span data-ttu-id="7fa8d-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="7fa8d-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="7fa8d-158">Variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="7fa8d-158">Compensation Variable Plan</span></span> | <span data-ttu-id="7fa8d-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="7fa8d-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="7fa8d-160">Nivå for variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="7fa8d-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="7fa8d-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="7fa8d-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="7fa8d-162">Type variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="7fa8d-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="7fa8d-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="7fa8d-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="7fa8d-164">Fast kompensasjonshendelse</span><span class="sxs-lookup"><span data-stu-id="7fa8d-164">Fixed Compensation Event</span></span> | <span data-ttu-id="7fa8d-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="7fa8d-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="7fa8d-166">Overdragelsesregel</span><span class="sxs-lookup"><span data-stu-id="7fa8d-166">Vesting Rule</span></span> | <span data-ttu-id="7fa8d-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="7fa8d-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="7fa8d-168">Fast kompensasjon for arbeider</span><span class="sxs-lookup"><span data-stu-id="7fa8d-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="7fa8d-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="7fa8d-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="7fa8d-170">Organisasjonsenheter</span><span class="sxs-lookup"><span data-stu-id="7fa8d-170">Organization entities</span></span>

| <span data-ttu-id="7fa8d-171">Navn</span><span class="sxs-lookup"><span data-stu-id="7fa8d-171">Name</span></span> | <span data-ttu-id="7fa8d-172">Enhet</span><span class="sxs-lookup"><span data-stu-id="7fa8d-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="7fa8d-173">Avdeling</span><span class="sxs-lookup"><span data-stu-id="7fa8d-173">Department</span></span> | <span data-ttu-id="7fa8d-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="7fa8d-174">cdm_department</span></span> |
| <span data-ttu-id="7fa8d-175">Ansettelse</span><span class="sxs-lookup"><span data-stu-id="7fa8d-175">Employment</span></span> | <span data-ttu-id="7fa8d-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="7fa8d-176">cdm_employment</span></span> |
| <span data-ttu-id="7fa8d-177">Bedrift</span><span class="sxs-lookup"><span data-stu-id="7fa8d-177">Company</span></span> | <span data-ttu-id="7fa8d-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="7fa8d-178">cdm_company</span></span> |
| <span data-ttu-id="7fa8d-179">Stilling</span><span class="sxs-lookup"><span data-stu-id="7fa8d-179">Job</span></span> | <span data-ttu-id="7fa8d-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="7fa8d-180">cdm_job</span></span> |
| <span data-ttu-id="7fa8d-181">Jobbfunksjon</span><span class="sxs-lookup"><span data-stu-id="7fa8d-181">Job Function</span></span> | <span data-ttu-id="7fa8d-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="7fa8d-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="7fa8d-183">stilling</span><span class="sxs-lookup"><span data-stu-id="7fa8d-183">Job Position</span></span> | <span data-ttu-id="7fa8d-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="7fa8d-184">cdm_jobposition</span></span> |
| <span data-ttu-id="7fa8d-185">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="7fa8d-185">Position Type</span></span> | <span data-ttu-id="7fa8d-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="7fa8d-186">cdm_positiontype</span></span> |
| <span data-ttu-id="7fa8d-187">Stillingstilordning</span><span class="sxs-lookup"><span data-stu-id="7fa8d-187">Position Worker Assignment</span></span> | <span data-ttu-id="7fa8d-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="7fa8d-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="7fa8d-189">stillingsdimensjon</span><span class="sxs-lookup"><span data-stu-id="7fa8d-189">Job Position Dimension</span></span> | <span data-ttu-id="7fa8d-190">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="7fa8d-190">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="7fa8d-191">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="7fa8d-191">Job Type</span></span> | <span data-ttu-id="7fa8d-192">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="7fa8d-192">cdm_jobtype</span></span> |
| <span data-ttu-id="7fa8d-193">Språk</span><span class="sxs-lookup"><span data-stu-id="7fa8d-193">Language</span></span> | <span data-ttu-id="7fa8d-194">cdm_language</span><span class="sxs-lookup"><span data-stu-id="7fa8d-194">cdm_language</span></span> |
| <span data-ttu-id="7fa8d-195">Stillingstittel</span><span class="sxs-lookup"><span data-stu-id="7fa8d-195">Title</span></span> | <span data-ttu-id="7fa8d-196">cdm_title</span><span class="sxs-lookup"><span data-stu-id="7fa8d-196">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="7fa8d-197">Finansdimensjoner for **Stillingstype**, **Stillingstilordning** og **Ansettelse** gir enveis integrering til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7fa8d-197">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Common Data Service.</span></span> <span data-ttu-id="7fa8d-198">Finansdimensjon-oppdateringer synkroniseres for øyeblikket ikke fra Common Data Service til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7fa8d-198">Financial dimensions updates currently can't synchronize from Common Data Service to Human Resources.</span></span> 

## <a name="leave-and-absence-entities"></a><span data-ttu-id="7fa8d-199">Permisjons- og fraværsenheter</span><span class="sxs-lookup"><span data-stu-id="7fa8d-199">Leave and absence entities</span></span>

| <span data-ttu-id="7fa8d-200">Navn</span><span class="sxs-lookup"><span data-stu-id="7fa8d-200">Name</span></span> | <span data-ttu-id="7fa8d-201">Entity</span><span class="sxs-lookup"><span data-stu-id="7fa8d-201">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="7fa8d-202">Banktransaksjon for permisjon</span><span class="sxs-lookup"><span data-stu-id="7fa8d-202">Leave Bank Transaction</span></span> | <span data-ttu-id="7fa8d-203">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="7fa8d-203">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="7fa8d-204">Permisjonsregistrering</span><span class="sxs-lookup"><span data-stu-id="7fa8d-204">Leave Enrollment</span></span> | <span data-ttu-id="7fa8d-205">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="7fa8d-205">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="7fa8d-206">Permisjonsplan</span><span class="sxs-lookup"><span data-stu-id="7fa8d-206">Leave Plan</span></span> | <span data-ttu-id="7fa8d-207">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="7fa8d-207">cdm_leaveplan</span></span> |
| <span data-ttu-id="7fa8d-208">Permisjonsforespørsel</span><span class="sxs-lookup"><span data-stu-id="7fa8d-208">Leave Request</span></span> | <span data-ttu-id="7fa8d-209">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="7fa8d-209">cdm_leaverequest</span></span> |
| <span data-ttu-id="7fa8d-210">Detaljer for fraværsforespørsel</span><span class="sxs-lookup"><span data-stu-id="7fa8d-210">Leave Request Detail</span></span> | <span data-ttu-id="7fa8d-211">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="7fa8d-211">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="7fa8d-212">Permisjonstype</span><span class="sxs-lookup"><span data-stu-id="7fa8d-212">Leave Type</span></span> | <span data-ttu-id="7fa8d-213">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="7fa8d-213">cdm_leavetype</span></span> |
| <span data-ttu-id="7fa8d-214">Årsakskode for permisjonstype</span><span class="sxs-lookup"><span data-stu-id="7fa8d-214">Leave Type Reason Code</span></span> | <span data-ttu-id="7fa8d-215">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="7fa8d-215">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="7fa8d-216">Lønnsenheter</span><span class="sxs-lookup"><span data-stu-id="7fa8d-216">Payroll entities</span></span>

| <span data-ttu-id="7fa8d-217">Navn</span><span class="sxs-lookup"><span data-stu-id="7fa8d-217">Name</span></span> | <span data-ttu-id="7fa8d-218">Enhet</span><span class="sxs-lookup"><span data-stu-id="7fa8d-218">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="7fa8d-219">Lønnssyklus</span><span class="sxs-lookup"><span data-stu-id="7fa8d-219">Pay Cycle</span></span> | <span data-ttu-id="7fa8d-220">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="7fa8d-220">cdm_paycycle</span></span> |
| <span data-ttu-id="7fa8d-221">Lønnsperiode</span><span class="sxs-lookup"><span data-stu-id="7fa8d-221">Pay Period</span></span> | <span data-ttu-id="7fa8d-222">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="7fa8d-222">cdm_payperiod</span></span> |
| <span data-ttu-id="7fa8d-223">Inntektskode for lønn</span><span class="sxs-lookup"><span data-stu-id="7fa8d-223">Payroll Earning Code</span></span> | <span data-ttu-id="7fa8d-224">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="7fa8d-224">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="7fa8d-225">Bankkontobetaling</span><span class="sxs-lookup"><span data-stu-id="7fa8d-225">Bank Account Disbursement</span></span> | <span data-ttu-id="7fa8d-226">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="7fa8d-226">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="7fa8d-227">Avgiftsområde</span><span class="sxs-lookup"><span data-stu-id="7fa8d-227">Tax Region</span></span> | <span data-ttu-id="7fa8d-228">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="7fa8d-228">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="7fa8d-229">Arbeiderenheter</span><span class="sxs-lookup"><span data-stu-id="7fa8d-229">Worker entities</span></span>

| <span data-ttu-id="7fa8d-230">Navn</span><span class="sxs-lookup"><span data-stu-id="7fa8d-230">Name</span></span> | <span data-ttu-id="7fa8d-231">Enhet</span><span class="sxs-lookup"><span data-stu-id="7fa8d-231">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="7fa8d-232">Arbeider</span><span class="sxs-lookup"><span data-stu-id="7fa8d-232">Worker</span></span> | <span data-ttu-id="7fa8d-233">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="7fa8d-233">cdm_worker</span></span> |
| <span data-ttu-id="7fa8d-234">Arbeideradresse</span><span class="sxs-lookup"><span data-stu-id="7fa8d-234">Worker Address</span></span> | <span data-ttu-id="7fa8d-235">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="7fa8d-235">cdm_workeraddress</span></span> |
| <span data-ttu-id="7fa8d-236">Arbeiderens personopplysninger</span><span class="sxs-lookup"><span data-stu-id="7fa8d-236">Worker Personal Detail</span></span> | <span data-ttu-id="7fa8d-237">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="7fa8d-237">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="7fa8d-238">Personidentifikasjonsnummer for arbeider</span><span class="sxs-lookup"><span data-stu-id="7fa8d-238">Worker Person Identification Number</span></span> | <span data-ttu-id="7fa8d-239">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="7fa8d-239">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="7fa8d-240">Personidentifikasjonstype for arbeider</span><span class="sxs-lookup"><span data-stu-id="7fa8d-240">Worker Person Identification Type</span></span> | <span data-ttu-id="7fa8d-241">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="7fa8d-241">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="7fa8d-242">Arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="7fa8d-242">Work Calendar</span></span> | <span data-ttu-id="7fa8d-243">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="7fa8d-243">cdm_workcalendar</span></span> |
| <span data-ttu-id="7fa8d-244">Arbeidskalenderdag</span><span class="sxs-lookup"><span data-stu-id="7fa8d-244">Work Calendar Day</span></span> | <span data-ttu-id="7fa8d-245">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="7fa8d-245">cdm_workcalendarday</span></span> |
| <span data-ttu-id="7fa8d-246">Helligdag i arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="7fa8d-246">Work Calendar Holiday</span></span> |<span data-ttu-id="7fa8d-247">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="7fa8d-247">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="7fa8d-248">Ferielinje for arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="7fa8d-248">Work Calendar Holiday Line</span></span> | <span data-ttu-id="7fa8d-249">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="7fa8d-249">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="7fa8d-250">Tidsintervall for arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="7fa8d-250">Work Calendar Time Interval</span></span> | <span data-ttu-id="7fa8d-251">cdm_workcalendartimeinterval (ikke aktivert for støtte for egendefinerte felt)</span><span class="sxs-lookup"><span data-stu-id="7fa8d-251">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="7fa8d-252">Bankkonto for arbeider</span><span class="sxs-lookup"><span data-stu-id="7fa8d-252">Worker Bank Account</span></span> | <span data-ttu-id="7fa8d-253">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="7fa8d-253">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="7fa8d-254">Enheter for arbeideroppsett</span><span class="sxs-lookup"><span data-stu-id="7fa8d-254">Worker setup entities</span></span>

| <span data-ttu-id="7fa8d-255">Navn</span><span class="sxs-lookup"><span data-stu-id="7fa8d-255">Name</span></span> | <span data-ttu-id="7fa8d-256">Enhet</span><span class="sxs-lookup"><span data-stu-id="7fa8d-256">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="7fa8d-257">Veteranstatus</span><span class="sxs-lookup"><span data-stu-id="7fa8d-257">Veteran Status</span></span> | <span data-ttu-id="7fa8d-258">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="7fa8d-258">cdm_veteranstatus</span></span> |
| <span data-ttu-id="7fa8d-259">Etnisk opprinnelse</span><span class="sxs-lookup"><span data-stu-id="7fa8d-259">Ethnic Origin</span></span> | <span data-ttu-id="7fa8d-260">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="7fa8d-260">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="7fa8d-261">Årsakskode</span><span class="sxs-lookup"><span data-stu-id="7fa8d-261">Reason Code</span></span> | <span data-ttu-id="7fa8d-262">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="7fa8d-262">cdm_reasoncode</span></span> |
| <span data-ttu-id="7fa8d-263">Utstedende byrå for personidentifikasjon</span><span class="sxs-lookup"><span data-stu-id="7fa8d-263">Person Identification Issuing Agency</span></span> | <span data-ttu-id="7fa8d-264">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="7fa8d-264">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="7fa8d-265">Kompetanseenheter</span><span class="sxs-lookup"><span data-stu-id="7fa8d-265">Competency entities</span></span>

| <span data-ttu-id="7fa8d-266">Navn</span><span class="sxs-lookup"><span data-stu-id="7fa8d-266">Name</span></span> | <span data-ttu-id="7fa8d-267">Enhet</span><span class="sxs-lookup"><span data-stu-id="7fa8d-267">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="7fa8d-268">Kompetansetype</span><span class="sxs-lookup"><span data-stu-id="7fa8d-268">Skill Type</span></span> | <span data-ttu-id="7fa8d-269">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="7fa8d-269">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="7fa8d-270">Enhetsrelasjonsmodeller</span><span class="sxs-lookup"><span data-stu-id="7fa8d-270">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="7fa8d-271">Arbeider</span><span class="sxs-lookup"><span data-stu-id="7fa8d-271">Worker</span></span>

![Arbeider](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="7fa8d-273">Jobb og stilling</span><span class="sxs-lookup"><span data-stu-id="7fa8d-273">Job and Job Position</span></span>

![Jobb og stilling](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="7fa8d-275">Fordeler</span><span class="sxs-lookup"><span data-stu-id="7fa8d-275">Benefits</span></span>

![Fordeler](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="7fa8d-277">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="7fa8d-277">Compensation</span></span>

![Kompensasjon](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="7fa8d-279">Permisjon</span><span class="sxs-lookup"><span data-stu-id="7fa8d-279">Leave</span></span>

![Permisjon](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="7fa8d-281">Arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="7fa8d-281">Work Calendar</span></span>

![Arbeidskalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="7fa8d-283">Se også</span><span class="sxs-lookup"><span data-stu-id="7fa8d-283">See also</span></span>

[<span data-ttu-id="7fa8d-284">Velge en dataintegreringsteknologi</span><span class="sxs-lookup"><span data-stu-id="7fa8d-284">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="7fa8d-285">Konfigurere Common Data Service-integrering</span><span class="sxs-lookup"><span data-stu-id="7fa8d-285">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)
