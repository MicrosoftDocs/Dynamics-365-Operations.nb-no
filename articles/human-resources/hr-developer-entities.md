---
title: Dataverse-tabeller
description: Microsoft Dynamics 365 Human Resources bruker Dataverse til å aktivere scenarioer for utvidbarhet og integrering.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8ddb74a2f0b6265c5be3c13a009211455ea862da
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893406"
---
# <a name="dataverse-tables"></a><span data-ttu-id="31239-103">Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="31239-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="31239-104">Microsoft Dynamics 365 Human Resources bruker Dataverse til å aktivere scenarioer for utvidbarhet og integrering.</span><span class="sxs-lookup"><span data-stu-id="31239-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="31239-105">Human Resources-enheter tilsvarer Dataverse-tabeller.</span><span class="sxs-lookup"><span data-stu-id="31239-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="31239-106">Hvis du vil ha mer informasjon om Dataverse (tidligere Common Data Service) og terminologioppdateringer, kan du se [Hva er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="31239-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="31239-107">Følgende Dataverse-tabeller er tilgjengelige på Human Resources-enheter.</span><span class="sxs-lookup"><span data-stu-id="31239-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="31239-108">Fordelstabeller</span><span class="sxs-lookup"><span data-stu-id="31239-108">Benefit tables</span></span>

| <span data-ttu-id="31239-109">Navn</span><span class="sxs-lookup"><span data-stu-id="31239-109">Name</span></span> | <span data-ttu-id="31239-110">Tabell</span><span class="sxs-lookup"><span data-stu-id="31239-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="31239-111">Beregningsfrekvens for fordeler</span><span class="sxs-lookup"><span data-stu-id="31239-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="31239-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="31239-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="31239-113">Lønnsperiode i fordelsberegningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="31239-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="31239-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="31239-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="31239-115">Beregningssats for fordeler</span><span class="sxs-lookup"><span data-stu-id="31239-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="31239-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="31239-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="31239-117">Detaljer om beregningssats for fordeler</span><span class="sxs-lookup"><span data-stu-id="31239-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="31239-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="31239-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="31239-119">Fordelsalternativ</span><span class="sxs-lookup"><span data-stu-id="31239-119">Benefit Option</span></span> | <span data-ttu-id="31239-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="31239-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="31239-121">Fordelsplan</span><span class="sxs-lookup"><span data-stu-id="31239-121">Benefit Plan</span></span> | <span data-ttu-id="31239-122">cdm_benefitplan (ikke aktivert for støtte for egendefinerte felt)</span><span class="sxs-lookup"><span data-stu-id="31239-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="31239-123">Fordelstype</span><span class="sxs-lookup"><span data-stu-id="31239-123">Benefit Type</span></span> | <span data-ttu-id="31239-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="31239-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="31239-125">Tabeller for forretningsprosessoppgaver</span><span class="sxs-lookup"><span data-stu-id="31239-125">Business process tasks tables</span></span>

| <span data-ttu-id="31239-126">Navn</span><span class="sxs-lookup"><span data-stu-id="31239-126">Name</span></span> | <span data-ttu-id="31239-127">Tabell</span><span class="sxs-lookup"><span data-stu-id="31239-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="31239-128">Forretningsprosesskalender</span><span class="sxs-lookup"><span data-stu-id="31239-128">Business Process Calendar</span></span> | <span data-ttu-id="31239-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="31239-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="31239-130">Tilordning av forretningsprosessgruppe</span><span class="sxs-lookup"><span data-stu-id="31239-130">Business Process Group Assignment</span></span> | <span data-ttu-id="31239-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="31239-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="31239-132">Oppgavegruppe for forretningsprosessbibliotek</span><span class="sxs-lookup"><span data-stu-id="31239-132">Business Process Library Task Group</span></span> | <span data-ttu-id="31239-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="31239-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="31239-134">Forretningsprosessfase</span><span class="sxs-lookup"><span data-stu-id="31239-134">Business Process Stage</span></span> | <span data-ttu-id="31239-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="31239-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="31239-136">Topptekst for sjekklistemal</span><span class="sxs-lookup"><span data-stu-id="31239-136">Checklist Template Header</span></span> | <span data-ttu-id="31239-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="31239-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="31239-138">Oppgave for sjekklistemal</span><span class="sxs-lookup"><span data-stu-id="31239-138">Checklist Template Task</span></span> | <span data-ttu-id="31239-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="31239-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="31239-140">Kompensasjonstabeller</span><span class="sxs-lookup"><span data-stu-id="31239-140">Compensation tables</span></span>

| <span data-ttu-id="31239-141">Navn</span><span class="sxs-lookup"><span data-stu-id="31239-141">Name</span></span> | <span data-ttu-id="31239-142">Tabell</span><span class="sxs-lookup"><span data-stu-id="31239-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="31239-143">Fast kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="31239-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="31239-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="31239-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="31239-145">Kompensasjonsrutenett</span><span class="sxs-lookup"><span data-stu-id="31239-145">Compensation Grid</span></span> | <span data-ttu-id="31239-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="31239-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="31239-147">Kompensasjonsnivå</span><span class="sxs-lookup"><span data-stu-id="31239-147">Compensation Level</span></span> | <span data-ttu-id="31239-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="31239-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="31239-149">Kompensasjon, lønnsfrekvens</span><span class="sxs-lookup"><span data-stu-id="31239-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="31239-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="31239-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="31239-151">Oppsett av referansepunkt for kompensasjon</span><span class="sxs-lookup"><span data-stu-id="31239-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="31239-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="31239-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="31239-153">Oppsettslinje for referansepunkt for kompensasjon</span><span class="sxs-lookup"><span data-stu-id="31239-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="31239-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="31239-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="31239-155">Kompensasjonsområde</span><span class="sxs-lookup"><span data-stu-id="31239-155">Compensation Region</span></span> | <span data-ttu-id="31239-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="31239-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="31239-157">Kompensasjonsstruktur</span><span class="sxs-lookup"><span data-stu-id="31239-157">Compensation Structure</span></span> | <span data-ttu-id="31239-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="31239-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="31239-159">Variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="31239-159">Compensation Variable Plan</span></span> | <span data-ttu-id="31239-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="31239-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="31239-161">Nivå for variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="31239-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="31239-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="31239-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="31239-163">Type variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="31239-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="31239-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="31239-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="31239-165">Fast kompensasjonshendelse</span><span class="sxs-lookup"><span data-stu-id="31239-165">Fixed Compensation Event</span></span> | <span data-ttu-id="31239-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="31239-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="31239-167">Overdragelsesregel</span><span class="sxs-lookup"><span data-stu-id="31239-167">Vesting Rule</span></span> | <span data-ttu-id="31239-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="31239-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="31239-169">Fast kompensasjon for arbeider</span><span class="sxs-lookup"><span data-stu-id="31239-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="31239-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="31239-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="31239-171">Organisasjonstabeller</span><span class="sxs-lookup"><span data-stu-id="31239-171">Organization tables</span></span>

| <span data-ttu-id="31239-172">Navn</span><span class="sxs-lookup"><span data-stu-id="31239-172">Name</span></span> | <span data-ttu-id="31239-173">Tabell</span><span class="sxs-lookup"><span data-stu-id="31239-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="31239-174">Avdeling</span><span class="sxs-lookup"><span data-stu-id="31239-174">Department</span></span> | <span data-ttu-id="31239-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="31239-175">cdm_department</span></span> |
| <span data-ttu-id="31239-176">Ansettelse</span><span class="sxs-lookup"><span data-stu-id="31239-176">Employment</span></span> | <span data-ttu-id="31239-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="31239-177">cdm_employment</span></span> |
| <span data-ttu-id="31239-178">Bedrift</span><span class="sxs-lookup"><span data-stu-id="31239-178">Company</span></span> | <span data-ttu-id="31239-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="31239-179">cdm_company</span></span> |
| <span data-ttu-id="31239-180">Stilling</span><span class="sxs-lookup"><span data-stu-id="31239-180">Job</span></span> | <span data-ttu-id="31239-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="31239-181">cdm_job</span></span> |
| <span data-ttu-id="31239-182">Jobbfunksjon</span><span class="sxs-lookup"><span data-stu-id="31239-182">Job Function</span></span> | <span data-ttu-id="31239-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="31239-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="31239-184">stilling</span><span class="sxs-lookup"><span data-stu-id="31239-184">Job Position</span></span> | <span data-ttu-id="31239-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="31239-185">cdm_jobposition</span></span> |
| <span data-ttu-id="31239-186">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="31239-186">Position Type</span></span> | <span data-ttu-id="31239-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="31239-187">cdm_positiontype</span></span> |
| <span data-ttu-id="31239-188">Stillingstilordning</span><span class="sxs-lookup"><span data-stu-id="31239-188">Position Worker Assignment</span></span> | <span data-ttu-id="31239-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="31239-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="31239-190">stillingsdimensjon</span><span class="sxs-lookup"><span data-stu-id="31239-190">Job Position Dimension</span></span> | <span data-ttu-id="31239-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="31239-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="31239-192">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="31239-192">Job Type</span></span> | <span data-ttu-id="31239-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="31239-193">cdm_jobtype</span></span> |
| <span data-ttu-id="31239-194">Språk</span><span class="sxs-lookup"><span data-stu-id="31239-194">Language</span></span> | <span data-ttu-id="31239-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="31239-195">cdm_language</span></span> |
| <span data-ttu-id="31239-196">Stillingstittel</span><span class="sxs-lookup"><span data-stu-id="31239-196">Title</span></span> | <span data-ttu-id="31239-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="31239-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="31239-198">Finansdimensjoner for **Stillingstype**, **Stillingstilordning** og **Ansettelse** gir enveis integrering til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="31239-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="31239-199">Finansdimensjon-oppdateringer synkroniseres for øyeblikket ikke fra Dataverse til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="31239-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="31239-200">Tabeller for permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="31239-200">Leave and absence tables</span></span>

| <span data-ttu-id="31239-201">Navn</span><span class="sxs-lookup"><span data-stu-id="31239-201">Name</span></span> | <span data-ttu-id="31239-202">Tabell</span><span class="sxs-lookup"><span data-stu-id="31239-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="31239-203">Banktransaksjon for permisjon</span><span class="sxs-lookup"><span data-stu-id="31239-203">Leave Bank Transaction</span></span> | <span data-ttu-id="31239-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="31239-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="31239-205">Permisjonsregistrering</span><span class="sxs-lookup"><span data-stu-id="31239-205">Leave Enrollment</span></span> | <span data-ttu-id="31239-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="31239-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="31239-207">Permisjonsplan</span><span class="sxs-lookup"><span data-stu-id="31239-207">Leave Plan</span></span> | <span data-ttu-id="31239-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="31239-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="31239-209">Permisjonsforespørsel</span><span class="sxs-lookup"><span data-stu-id="31239-209">Leave Request</span></span> | <span data-ttu-id="31239-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="31239-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="31239-211">Detaljer for fraværsforespørsel</span><span class="sxs-lookup"><span data-stu-id="31239-211">Leave Request Detail</span></span> | <span data-ttu-id="31239-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="31239-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="31239-213">Permisjonstype</span><span class="sxs-lookup"><span data-stu-id="31239-213">Leave Type</span></span> | <span data-ttu-id="31239-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="31239-214">cdm_leavetype</span></span> |
| <span data-ttu-id="31239-215">Årsakskode for permisjonstype</span><span class="sxs-lookup"><span data-stu-id="31239-215">Leave Type Reason Code</span></span> | <span data-ttu-id="31239-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="31239-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="31239-217">Lønnstabeller</span><span class="sxs-lookup"><span data-stu-id="31239-217">Payroll tables</span></span>

| <span data-ttu-id="31239-218">Navn</span><span class="sxs-lookup"><span data-stu-id="31239-218">Name</span></span> | <span data-ttu-id="31239-219">Tabell</span><span class="sxs-lookup"><span data-stu-id="31239-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="31239-220">Lønnssyklus</span><span class="sxs-lookup"><span data-stu-id="31239-220">Pay Cycle</span></span> | <span data-ttu-id="31239-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="31239-221">cdm_paycycle</span></span> |
| <span data-ttu-id="31239-222">Lønnsperiode</span><span class="sxs-lookup"><span data-stu-id="31239-222">Pay Period</span></span> | <span data-ttu-id="31239-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="31239-223">cdm_payperiod</span></span> |
| <span data-ttu-id="31239-224">Inntektskode for lønn</span><span class="sxs-lookup"><span data-stu-id="31239-224">Payroll Earning Code</span></span> | <span data-ttu-id="31239-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="31239-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="31239-226">Bankkontobetaling</span><span class="sxs-lookup"><span data-stu-id="31239-226">Bank Account Disbursement</span></span> | <span data-ttu-id="31239-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="31239-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="31239-228">Avgiftsområde</span><span class="sxs-lookup"><span data-stu-id="31239-228">Tax Region</span></span> | <span data-ttu-id="31239-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="31239-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="31239-230">Arbeidertabeller</span><span class="sxs-lookup"><span data-stu-id="31239-230">Worker tables</span></span>

| <span data-ttu-id="31239-231">Navn</span><span class="sxs-lookup"><span data-stu-id="31239-231">Name</span></span> | <span data-ttu-id="31239-232">Tabell</span><span class="sxs-lookup"><span data-stu-id="31239-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="31239-233">Worker</span><span class="sxs-lookup"><span data-stu-id="31239-233">Worker</span></span> | <span data-ttu-id="31239-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="31239-234">cdm_worker</span></span> |
| <span data-ttu-id="31239-235">Arbeideradresse</span><span class="sxs-lookup"><span data-stu-id="31239-235">Worker Address</span></span> | <span data-ttu-id="31239-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="31239-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="31239-237">Arbeiderens personopplysninger</span><span class="sxs-lookup"><span data-stu-id="31239-237">Worker Personal Detail</span></span> | <span data-ttu-id="31239-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="31239-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="31239-239">Personidentifikasjonsnummer for arbeider</span><span class="sxs-lookup"><span data-stu-id="31239-239">Worker Person Identification Number</span></span> | <span data-ttu-id="31239-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="31239-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="31239-241">Personidentifikasjonstype for arbeider</span><span class="sxs-lookup"><span data-stu-id="31239-241">Worker Person Identification Type</span></span> | <span data-ttu-id="31239-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="31239-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="31239-243">Arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="31239-243">Work Calendar</span></span> | <span data-ttu-id="31239-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="31239-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="31239-245">Arbeidskalenderdag</span><span class="sxs-lookup"><span data-stu-id="31239-245">Work Calendar Day</span></span> | <span data-ttu-id="31239-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="31239-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="31239-247">Helligdag i arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="31239-247">Work Calendar Holiday</span></span> |<span data-ttu-id="31239-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="31239-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="31239-249">Ferielinje for arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="31239-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="31239-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="31239-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="31239-251">Tidsintervall for arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="31239-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="31239-252">cdm_workcalendartimeinterval (ikke aktivert for støtte for egendefinerte felt)</span><span class="sxs-lookup"><span data-stu-id="31239-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="31239-253">Bankkonto for arbeider</span><span class="sxs-lookup"><span data-stu-id="31239-253">Worker Bank Account</span></span> | <span data-ttu-id="31239-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="31239-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="31239-255">Tabeller for arbeideroppsett</span><span class="sxs-lookup"><span data-stu-id="31239-255">Worker setup tables</span></span>

| <span data-ttu-id="31239-256">Navn</span><span class="sxs-lookup"><span data-stu-id="31239-256">Name</span></span> | <span data-ttu-id="31239-257">Tabell</span><span class="sxs-lookup"><span data-stu-id="31239-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="31239-258">Veteranstatus</span><span class="sxs-lookup"><span data-stu-id="31239-258">Veteran Status</span></span> | <span data-ttu-id="31239-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="31239-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="31239-260">Etnisk opprinnelse</span><span class="sxs-lookup"><span data-stu-id="31239-260">Ethnic Origin</span></span> | <span data-ttu-id="31239-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="31239-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="31239-262">Årsakskode</span><span class="sxs-lookup"><span data-stu-id="31239-262">Reason Code</span></span> | <span data-ttu-id="31239-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="31239-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="31239-264">Utstedende byrå for personidentifikasjon</span><span class="sxs-lookup"><span data-stu-id="31239-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="31239-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="31239-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="31239-266">Kompetansetabeller</span><span class="sxs-lookup"><span data-stu-id="31239-266">Competency tables</span></span>

| <span data-ttu-id="31239-267">Navn</span><span class="sxs-lookup"><span data-stu-id="31239-267">Name</span></span> | <span data-ttu-id="31239-268">Tabell</span><span class="sxs-lookup"><span data-stu-id="31239-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="31239-269">Kompetansetype</span><span class="sxs-lookup"><span data-stu-id="31239-269">Skill Type</span></span> | <span data-ttu-id="31239-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="31239-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="31239-271">Tabellrelasjonsmodeller</span><span class="sxs-lookup"><span data-stu-id="31239-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="31239-272">Worker</span><span class="sxs-lookup"><span data-stu-id="31239-272">Worker</span></span>

![Worker](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="31239-274">Jobb og stilling</span><span class="sxs-lookup"><span data-stu-id="31239-274">Job and Job Position</span></span>

![Jobb og stilling](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="31239-276">Fordeler</span><span class="sxs-lookup"><span data-stu-id="31239-276">Benefits</span></span>

![Fordeler](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="31239-278">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="31239-278">Compensation</span></span>

![Kompensasjon](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="31239-280">Permisjon</span><span class="sxs-lookup"><span data-stu-id="31239-280">Leave</span></span>

![Permisjon](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="31239-282">Arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="31239-282">Work Calendar</span></span>

![Arbeidskalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="31239-284">Se også</span><span class="sxs-lookup"><span data-stu-id="31239-284">See also</span></span>

[<span data-ttu-id="31239-285">Velge en dataintegreringsteknologi</span><span class="sxs-lookup"><span data-stu-id="31239-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="31239-286">Konfigurere Dataverse-integrering</span><span class="sxs-lookup"><span data-stu-id="31239-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="31239-287">Konfigurere virtuelle Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="31239-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="31239-288">Vanlige spørsmål om virtuelle tabeller for Human Resources</span><span class="sxs-lookup"><span data-stu-id="31239-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="31239-289">Hva er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="31239-289">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="31239-290">Terminologioppdateringer</span><span class="sxs-lookup"><span data-stu-id="31239-290">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]