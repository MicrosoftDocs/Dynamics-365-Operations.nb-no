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
ms.openlocfilehash: e316cda9b9c5361c0a2837e7ed6c050e76cc39b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793615"
---
# <a name="dataverse-tables"></a><span data-ttu-id="be6ca-103">Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="be6ca-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="be6ca-104">Microsoft Dynamics 365 Human Resources bruker Dataverse til å aktivere scenarioer for utvidbarhet og integrering.</span><span class="sxs-lookup"><span data-stu-id="be6ca-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="be6ca-105">Human Resources-enheter tilsvarer Dataverse-tabeller.</span><span class="sxs-lookup"><span data-stu-id="be6ca-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="be6ca-106">Hvis du vil ha mer informasjon om Dataverse (tidligere Common Data Service) og terminologioppdateringer, kan du se [Hva er Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="be6ca-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="be6ca-107">Følgende Dataverse-tabeller er tilgjengelige på Human Resources-enheter.</span><span class="sxs-lookup"><span data-stu-id="be6ca-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="be6ca-108">Fordelstabeller</span><span class="sxs-lookup"><span data-stu-id="be6ca-108">Benefit tables</span></span>

| <span data-ttu-id="be6ca-109">Navn</span><span class="sxs-lookup"><span data-stu-id="be6ca-109">Name</span></span> | <span data-ttu-id="be6ca-110">Tabell</span><span class="sxs-lookup"><span data-stu-id="be6ca-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="be6ca-111">Beregningsfrekvens for fordeler</span><span class="sxs-lookup"><span data-stu-id="be6ca-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="be6ca-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="be6ca-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="be6ca-113">Lønnsperiode i fordelsberegningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="be6ca-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="be6ca-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="be6ca-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="be6ca-115">Beregningssats for fordeler</span><span class="sxs-lookup"><span data-stu-id="be6ca-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="be6ca-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="be6ca-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="be6ca-117">Detaljer om beregningssats for fordeler</span><span class="sxs-lookup"><span data-stu-id="be6ca-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="be6ca-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="be6ca-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="be6ca-119">Fordelsalternativ</span><span class="sxs-lookup"><span data-stu-id="be6ca-119">Benefit Option</span></span> | <span data-ttu-id="be6ca-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="be6ca-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="be6ca-121">Fordelsplan</span><span class="sxs-lookup"><span data-stu-id="be6ca-121">Benefit Plan</span></span> | <span data-ttu-id="be6ca-122">cdm_benefitplan (ikke aktivert for støtte for egendefinerte felt)</span><span class="sxs-lookup"><span data-stu-id="be6ca-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="be6ca-123">Fordelstype</span><span class="sxs-lookup"><span data-stu-id="be6ca-123">Benefit Type</span></span> | <span data-ttu-id="be6ca-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="be6ca-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="be6ca-125">Tabeller for forretningsprosessoppgaver</span><span class="sxs-lookup"><span data-stu-id="be6ca-125">Business process tasks tables</span></span>

| <span data-ttu-id="be6ca-126">Navn</span><span class="sxs-lookup"><span data-stu-id="be6ca-126">Name</span></span> | <span data-ttu-id="be6ca-127">Tabell</span><span class="sxs-lookup"><span data-stu-id="be6ca-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="be6ca-128">Forretningsprosesskalender</span><span class="sxs-lookup"><span data-stu-id="be6ca-128">Business Process Calendar</span></span> | <span data-ttu-id="be6ca-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="be6ca-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="be6ca-130">Tilordning av forretningsprosessgruppe</span><span class="sxs-lookup"><span data-stu-id="be6ca-130">Business Process Group Assignment</span></span> | <span data-ttu-id="be6ca-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="be6ca-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="be6ca-132">Oppgavegruppe for forretningsprosessbibliotek</span><span class="sxs-lookup"><span data-stu-id="be6ca-132">Business Process Library Task Group</span></span> | <span data-ttu-id="be6ca-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="be6ca-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="be6ca-134">Forretningsprosessfase</span><span class="sxs-lookup"><span data-stu-id="be6ca-134">Business Process Stage</span></span> | <span data-ttu-id="be6ca-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="be6ca-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="be6ca-136">Topptekst for sjekklistemal</span><span class="sxs-lookup"><span data-stu-id="be6ca-136">Checklist Template Header</span></span> | <span data-ttu-id="be6ca-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="be6ca-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="be6ca-138">Oppgave for sjekklistemal</span><span class="sxs-lookup"><span data-stu-id="be6ca-138">Checklist Template Task</span></span> | <span data-ttu-id="be6ca-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="be6ca-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="be6ca-140">Kompensasjonstabeller</span><span class="sxs-lookup"><span data-stu-id="be6ca-140">Compensation tables</span></span>

| <span data-ttu-id="be6ca-141">Navn</span><span class="sxs-lookup"><span data-stu-id="be6ca-141">Name</span></span> | <span data-ttu-id="be6ca-142">Tabell</span><span class="sxs-lookup"><span data-stu-id="be6ca-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="be6ca-143">Fast kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="be6ca-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="be6ca-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="be6ca-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="be6ca-145">Kompensasjonsrutenett</span><span class="sxs-lookup"><span data-stu-id="be6ca-145">Compensation Grid</span></span> | <span data-ttu-id="be6ca-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="be6ca-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="be6ca-147">Kompensasjonsnivå</span><span class="sxs-lookup"><span data-stu-id="be6ca-147">Compensation Level</span></span> | <span data-ttu-id="be6ca-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="be6ca-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="be6ca-149">Kompensasjon, lønnsfrekvens</span><span class="sxs-lookup"><span data-stu-id="be6ca-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="be6ca-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="be6ca-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="be6ca-151">Oppsett av referansepunkt for kompensasjon</span><span class="sxs-lookup"><span data-stu-id="be6ca-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="be6ca-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="be6ca-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="be6ca-153">Oppsettslinje for referansepunkt for kompensasjon</span><span class="sxs-lookup"><span data-stu-id="be6ca-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="be6ca-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="be6ca-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="be6ca-155">Kompensasjonsområde</span><span class="sxs-lookup"><span data-stu-id="be6ca-155">Compensation Region</span></span> | <span data-ttu-id="be6ca-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="be6ca-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="be6ca-157">Kompensasjonsstruktur</span><span class="sxs-lookup"><span data-stu-id="be6ca-157">Compensation Structure</span></span> | <span data-ttu-id="be6ca-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="be6ca-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="be6ca-159">Variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="be6ca-159">Compensation Variable Plan</span></span> | <span data-ttu-id="be6ca-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="be6ca-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="be6ca-161">Nivå for variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="be6ca-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="be6ca-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="be6ca-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="be6ca-163">Type variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="be6ca-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="be6ca-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="be6ca-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="be6ca-165">Fast kompensasjonshendelse</span><span class="sxs-lookup"><span data-stu-id="be6ca-165">Fixed Compensation Event</span></span> | <span data-ttu-id="be6ca-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="be6ca-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="be6ca-167">Overdragelsesregel</span><span class="sxs-lookup"><span data-stu-id="be6ca-167">Vesting Rule</span></span> | <span data-ttu-id="be6ca-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="be6ca-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="be6ca-169">Fast kompensasjon for arbeider</span><span class="sxs-lookup"><span data-stu-id="be6ca-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="be6ca-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="be6ca-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="be6ca-171">Organisasjonstabeller</span><span class="sxs-lookup"><span data-stu-id="be6ca-171">Organization tables</span></span>

| <span data-ttu-id="be6ca-172">Navn</span><span class="sxs-lookup"><span data-stu-id="be6ca-172">Name</span></span> | <span data-ttu-id="be6ca-173">Tabell</span><span class="sxs-lookup"><span data-stu-id="be6ca-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="be6ca-174">Avdeling</span><span class="sxs-lookup"><span data-stu-id="be6ca-174">Department</span></span> | <span data-ttu-id="be6ca-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="be6ca-175">cdm_department</span></span> |
| <span data-ttu-id="be6ca-176">Ansettelse</span><span class="sxs-lookup"><span data-stu-id="be6ca-176">Employment</span></span> | <span data-ttu-id="be6ca-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="be6ca-177">cdm_employment</span></span> |
| <span data-ttu-id="be6ca-178">Bedrift</span><span class="sxs-lookup"><span data-stu-id="be6ca-178">Company</span></span> | <span data-ttu-id="be6ca-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="be6ca-179">cdm_company</span></span> |
| <span data-ttu-id="be6ca-180">Stilling</span><span class="sxs-lookup"><span data-stu-id="be6ca-180">Job</span></span> | <span data-ttu-id="be6ca-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="be6ca-181">cdm_job</span></span> |
| <span data-ttu-id="be6ca-182">Jobbfunksjon</span><span class="sxs-lookup"><span data-stu-id="be6ca-182">Job Function</span></span> | <span data-ttu-id="be6ca-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="be6ca-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="be6ca-184">stilling</span><span class="sxs-lookup"><span data-stu-id="be6ca-184">Job Position</span></span> | <span data-ttu-id="be6ca-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="be6ca-185">cdm_jobposition</span></span> |
| <span data-ttu-id="be6ca-186">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="be6ca-186">Position Type</span></span> | <span data-ttu-id="be6ca-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="be6ca-187">cdm_positiontype</span></span> |
| <span data-ttu-id="be6ca-188">Stillingstilordning</span><span class="sxs-lookup"><span data-stu-id="be6ca-188">Position Worker Assignment</span></span> | <span data-ttu-id="be6ca-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="be6ca-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="be6ca-190">stillingsdimensjon</span><span class="sxs-lookup"><span data-stu-id="be6ca-190">Job Position Dimension</span></span> | <span data-ttu-id="be6ca-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="be6ca-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="be6ca-192">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="be6ca-192">Job Type</span></span> | <span data-ttu-id="be6ca-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="be6ca-193">cdm_jobtype</span></span> |
| <span data-ttu-id="be6ca-194">Språk</span><span class="sxs-lookup"><span data-stu-id="be6ca-194">Language</span></span> | <span data-ttu-id="be6ca-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="be6ca-195">cdm_language</span></span> |
| <span data-ttu-id="be6ca-196">Stillingstittel</span><span class="sxs-lookup"><span data-stu-id="be6ca-196">Title</span></span> | <span data-ttu-id="be6ca-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="be6ca-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="be6ca-198">Finansdimensjoner for **Stillingstype**, **Stillingstilordning** og **Ansettelse** gir enveis integrering til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="be6ca-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="be6ca-199">Finansdimensjon-oppdateringer synkroniseres for øyeblikket ikke fra Dataverse til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="be6ca-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="be6ca-200">Tabeller for permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="be6ca-200">Leave and absence tables</span></span>

| <span data-ttu-id="be6ca-201">Navn</span><span class="sxs-lookup"><span data-stu-id="be6ca-201">Name</span></span> | <span data-ttu-id="be6ca-202">Tabell</span><span class="sxs-lookup"><span data-stu-id="be6ca-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="be6ca-203">Banktransaksjon for permisjon</span><span class="sxs-lookup"><span data-stu-id="be6ca-203">Leave Bank Transaction</span></span> | <span data-ttu-id="be6ca-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="be6ca-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="be6ca-205">Permisjonsregistrering</span><span class="sxs-lookup"><span data-stu-id="be6ca-205">Leave Enrollment</span></span> | <span data-ttu-id="be6ca-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="be6ca-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="be6ca-207">Permisjonsplan</span><span class="sxs-lookup"><span data-stu-id="be6ca-207">Leave Plan</span></span> | <span data-ttu-id="be6ca-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="be6ca-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="be6ca-209">Permisjonsforespørsel</span><span class="sxs-lookup"><span data-stu-id="be6ca-209">Leave Request</span></span> | <span data-ttu-id="be6ca-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="be6ca-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="be6ca-211">Detaljer for fraværsforespørsel</span><span class="sxs-lookup"><span data-stu-id="be6ca-211">Leave Request Detail</span></span> | <span data-ttu-id="be6ca-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="be6ca-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="be6ca-213">Permisjonstype</span><span class="sxs-lookup"><span data-stu-id="be6ca-213">Leave Type</span></span> | <span data-ttu-id="be6ca-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="be6ca-214">cdm_leavetype</span></span> |
| <span data-ttu-id="be6ca-215">Årsakskode for permisjonstype</span><span class="sxs-lookup"><span data-stu-id="be6ca-215">Leave Type Reason Code</span></span> | <span data-ttu-id="be6ca-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="be6ca-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="be6ca-217">Lønnstabeller</span><span class="sxs-lookup"><span data-stu-id="be6ca-217">Payroll tables</span></span>

| <span data-ttu-id="be6ca-218">Navn</span><span class="sxs-lookup"><span data-stu-id="be6ca-218">Name</span></span> | <span data-ttu-id="be6ca-219">Tabell</span><span class="sxs-lookup"><span data-stu-id="be6ca-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="be6ca-220">Lønnssyklus</span><span class="sxs-lookup"><span data-stu-id="be6ca-220">Pay Cycle</span></span> | <span data-ttu-id="be6ca-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="be6ca-221">cdm_paycycle</span></span> |
| <span data-ttu-id="be6ca-222">Lønnsperiode</span><span class="sxs-lookup"><span data-stu-id="be6ca-222">Pay Period</span></span> | <span data-ttu-id="be6ca-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="be6ca-223">cdm_payperiod</span></span> |
| <span data-ttu-id="be6ca-224">Inntektskode for lønn</span><span class="sxs-lookup"><span data-stu-id="be6ca-224">Payroll Earning Code</span></span> | <span data-ttu-id="be6ca-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="be6ca-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="be6ca-226">Bankkontobetaling</span><span class="sxs-lookup"><span data-stu-id="be6ca-226">Bank Account Disbursement</span></span> | <span data-ttu-id="be6ca-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="be6ca-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="be6ca-228">Avgiftsområde</span><span class="sxs-lookup"><span data-stu-id="be6ca-228">Tax Region</span></span> | <span data-ttu-id="be6ca-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="be6ca-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="be6ca-230">Arbeidertabeller</span><span class="sxs-lookup"><span data-stu-id="be6ca-230">Worker tables</span></span>

| <span data-ttu-id="be6ca-231">Navn</span><span class="sxs-lookup"><span data-stu-id="be6ca-231">Name</span></span> | <span data-ttu-id="be6ca-232">Tabell</span><span class="sxs-lookup"><span data-stu-id="be6ca-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="be6ca-233">Worker</span><span class="sxs-lookup"><span data-stu-id="be6ca-233">Worker</span></span> | <span data-ttu-id="be6ca-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="be6ca-234">cdm_worker</span></span> |
| <span data-ttu-id="be6ca-235">Arbeideradresse</span><span class="sxs-lookup"><span data-stu-id="be6ca-235">Worker Address</span></span> | <span data-ttu-id="be6ca-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="be6ca-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="be6ca-237">Arbeiderens personopplysninger</span><span class="sxs-lookup"><span data-stu-id="be6ca-237">Worker Personal Detail</span></span> | <span data-ttu-id="be6ca-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="be6ca-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="be6ca-239">Personidentifikasjonsnummer for arbeider</span><span class="sxs-lookup"><span data-stu-id="be6ca-239">Worker Person Identification Number</span></span> | <span data-ttu-id="be6ca-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="be6ca-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="be6ca-241">Personidentifikasjonstype for arbeider</span><span class="sxs-lookup"><span data-stu-id="be6ca-241">Worker Person Identification Type</span></span> | <span data-ttu-id="be6ca-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="be6ca-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="be6ca-243">Arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="be6ca-243">Work Calendar</span></span> | <span data-ttu-id="be6ca-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="be6ca-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="be6ca-245">Arbeidskalenderdag</span><span class="sxs-lookup"><span data-stu-id="be6ca-245">Work Calendar Day</span></span> | <span data-ttu-id="be6ca-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="be6ca-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="be6ca-247">Helligdag i arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="be6ca-247">Work Calendar Holiday</span></span> |<span data-ttu-id="be6ca-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="be6ca-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="be6ca-249">Ferielinje for arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="be6ca-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="be6ca-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="be6ca-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="be6ca-251">Tidsintervall for arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="be6ca-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="be6ca-252">cdm_workcalendartimeinterval (ikke aktivert for støtte for egendefinerte felt)</span><span class="sxs-lookup"><span data-stu-id="be6ca-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="be6ca-253">Bankkonto for arbeider</span><span class="sxs-lookup"><span data-stu-id="be6ca-253">Worker Bank Account</span></span> | <span data-ttu-id="be6ca-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="be6ca-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="be6ca-255">Tabeller for arbeideroppsett</span><span class="sxs-lookup"><span data-stu-id="be6ca-255">Worker setup tables</span></span>

| <span data-ttu-id="be6ca-256">Navn</span><span class="sxs-lookup"><span data-stu-id="be6ca-256">Name</span></span> | <span data-ttu-id="be6ca-257">Tabell</span><span class="sxs-lookup"><span data-stu-id="be6ca-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="be6ca-258">Veteranstatus</span><span class="sxs-lookup"><span data-stu-id="be6ca-258">Veteran Status</span></span> | <span data-ttu-id="be6ca-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="be6ca-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="be6ca-260">Etnisk opprinnelse</span><span class="sxs-lookup"><span data-stu-id="be6ca-260">Ethnic Origin</span></span> | <span data-ttu-id="be6ca-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="be6ca-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="be6ca-262">Årsakskode</span><span class="sxs-lookup"><span data-stu-id="be6ca-262">Reason Code</span></span> | <span data-ttu-id="be6ca-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="be6ca-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="be6ca-264">Utstedende byrå for personidentifikasjon</span><span class="sxs-lookup"><span data-stu-id="be6ca-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="be6ca-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="be6ca-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="be6ca-266">Kompetansetabeller</span><span class="sxs-lookup"><span data-stu-id="be6ca-266">Competency tables</span></span>

| <span data-ttu-id="be6ca-267">Navn</span><span class="sxs-lookup"><span data-stu-id="be6ca-267">Name</span></span> | <span data-ttu-id="be6ca-268">Tabell</span><span class="sxs-lookup"><span data-stu-id="be6ca-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="be6ca-269">Kompetansetype</span><span class="sxs-lookup"><span data-stu-id="be6ca-269">Skill Type</span></span> | <span data-ttu-id="be6ca-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="be6ca-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="be6ca-271">Tabellrelasjonsmodeller</span><span class="sxs-lookup"><span data-stu-id="be6ca-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="be6ca-272">Worker</span><span class="sxs-lookup"><span data-stu-id="be6ca-272">Worker</span></span>

![Worker](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="be6ca-274">Jobb og stilling</span><span class="sxs-lookup"><span data-stu-id="be6ca-274">Job and Job Position</span></span>

![Jobb og stilling](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="be6ca-276">Fordeler</span><span class="sxs-lookup"><span data-stu-id="be6ca-276">Benefits</span></span>

![Fordeler](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="be6ca-278">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="be6ca-278">Compensation</span></span>

![Kompensasjon](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="be6ca-280">Permisjon</span><span class="sxs-lookup"><span data-stu-id="be6ca-280">Leave</span></span>

![Permisjon](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="be6ca-282">Arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="be6ca-282">Work Calendar</span></span>

![Arbeidskalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="be6ca-284">Se også</span><span class="sxs-lookup"><span data-stu-id="be6ca-284">See also</span></span>

[<span data-ttu-id="be6ca-285">Velge en dataintegreringsteknologi</span><span class="sxs-lookup"><span data-stu-id="be6ca-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="be6ca-286">Konfigurere Dataverse-integrering</span><span class="sxs-lookup"><span data-stu-id="be6ca-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="be6ca-287">Konfigurere virtuelle Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="be6ca-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="be6ca-288">Vanlige spørsmål om virtuelle tabeller for Human Resources</span><span class="sxs-lookup"><span data-stu-id="be6ca-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="be6ca-289">Hva er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="be6ca-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="be6ca-290">Terminologioppdateringer</span><span class="sxs-lookup"><span data-stu-id="be6ca-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]