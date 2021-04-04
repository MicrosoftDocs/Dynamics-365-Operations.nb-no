---
title: Dataverse-tabeller
description: Microsoft Dynamics 365 Human Resources bruker Dataverse til å aktivere scenarioer for utvidbarhet og integrering.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
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
ms.openlocfilehash: caf8b0a5d0b24ef3619f45a6d236acae6d29c8ab
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465228"
---
# <a name="dataverse-tables"></a><span data-ttu-id="8a79c-103">Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="8a79c-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8a79c-104">Microsoft Dynamics 365 Human Resources bruker Dataverse til å aktivere scenarioer for utvidbarhet og integrering.</span><span class="sxs-lookup"><span data-stu-id="8a79c-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="8a79c-105">Human Resources-enheter tilsvarer Dataverse-tabeller.</span><span class="sxs-lookup"><span data-stu-id="8a79c-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="8a79c-106">Hvis du vil ha mer informasjon om Dataverse (tidligere Common Data Service) og terminologioppdateringer, kan du se [Hva er Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="8a79c-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="8a79c-107">Følgende Dataverse-tabeller er tilgjengelige på Human Resources-enheter.</span><span class="sxs-lookup"><span data-stu-id="8a79c-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="8a79c-108">Fordelstabeller</span><span class="sxs-lookup"><span data-stu-id="8a79c-108">Benefit tables</span></span>

| <span data-ttu-id="8a79c-109">Navn</span><span class="sxs-lookup"><span data-stu-id="8a79c-109">Name</span></span> | <span data-ttu-id="8a79c-110">Tabell</span><span class="sxs-lookup"><span data-stu-id="8a79c-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="8a79c-111">Beregningsfrekvens for fordeler</span><span class="sxs-lookup"><span data-stu-id="8a79c-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="8a79c-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="8a79c-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="8a79c-113">Lønnsperiode i fordelsberegningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="8a79c-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="8a79c-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="8a79c-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="8a79c-115">Beregningssats for fordeler</span><span class="sxs-lookup"><span data-stu-id="8a79c-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="8a79c-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="8a79c-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="8a79c-117">Detaljer om beregningssats for fordeler</span><span class="sxs-lookup"><span data-stu-id="8a79c-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="8a79c-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="8a79c-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="8a79c-119">Fordelsalternativ</span><span class="sxs-lookup"><span data-stu-id="8a79c-119">Benefit Option</span></span> | <span data-ttu-id="8a79c-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="8a79c-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="8a79c-121">Fordelsplan</span><span class="sxs-lookup"><span data-stu-id="8a79c-121">Benefit Plan</span></span> | <span data-ttu-id="8a79c-122">cdm_benefitplan (ikke aktivert for støtte for egendefinerte felt)</span><span class="sxs-lookup"><span data-stu-id="8a79c-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="8a79c-123">Fordelstype</span><span class="sxs-lookup"><span data-stu-id="8a79c-123">Benefit Type</span></span> | <span data-ttu-id="8a79c-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="8a79c-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="8a79c-125">Tabeller for forretningsprosessoppgaver</span><span class="sxs-lookup"><span data-stu-id="8a79c-125">Business process tasks tables</span></span>

| <span data-ttu-id="8a79c-126">Navn</span><span class="sxs-lookup"><span data-stu-id="8a79c-126">Name</span></span> | <span data-ttu-id="8a79c-127">Tabell</span><span class="sxs-lookup"><span data-stu-id="8a79c-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="8a79c-128">Forretningsprosesskalender</span><span class="sxs-lookup"><span data-stu-id="8a79c-128">Business Process Calendar</span></span> | <span data-ttu-id="8a79c-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="8a79c-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="8a79c-130">Tilordning av forretningsprosessgruppe</span><span class="sxs-lookup"><span data-stu-id="8a79c-130">Business Process Group Assignment</span></span> | <span data-ttu-id="8a79c-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="8a79c-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="8a79c-132">Oppgavegruppe for forretningsprosessbibliotek</span><span class="sxs-lookup"><span data-stu-id="8a79c-132">Business Process Library Task Group</span></span> | <span data-ttu-id="8a79c-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="8a79c-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="8a79c-134">Forretningsprosessfase</span><span class="sxs-lookup"><span data-stu-id="8a79c-134">Business Process Stage</span></span> | <span data-ttu-id="8a79c-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="8a79c-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="8a79c-136">Topptekst for sjekklistemal</span><span class="sxs-lookup"><span data-stu-id="8a79c-136">Checklist Template Header</span></span> | <span data-ttu-id="8a79c-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="8a79c-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="8a79c-138">Oppgave for sjekklistemal</span><span class="sxs-lookup"><span data-stu-id="8a79c-138">Checklist Template Task</span></span> | <span data-ttu-id="8a79c-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="8a79c-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="8a79c-140">Kompensasjonstabeller</span><span class="sxs-lookup"><span data-stu-id="8a79c-140">Compensation tables</span></span>

| <span data-ttu-id="8a79c-141">Navn</span><span class="sxs-lookup"><span data-stu-id="8a79c-141">Name</span></span> | <span data-ttu-id="8a79c-142">Tabell</span><span class="sxs-lookup"><span data-stu-id="8a79c-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="8a79c-143">Fast kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="8a79c-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="8a79c-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="8a79c-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="8a79c-145">Kompensasjonsrutenett</span><span class="sxs-lookup"><span data-stu-id="8a79c-145">Compensation Grid</span></span> | <span data-ttu-id="8a79c-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="8a79c-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="8a79c-147">Kompensasjonsnivå</span><span class="sxs-lookup"><span data-stu-id="8a79c-147">Compensation Level</span></span> | <span data-ttu-id="8a79c-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="8a79c-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="8a79c-149">Kompensasjon, lønnsfrekvens</span><span class="sxs-lookup"><span data-stu-id="8a79c-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="8a79c-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="8a79c-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="8a79c-151">Oppsett av referansepunkt for kompensasjon</span><span class="sxs-lookup"><span data-stu-id="8a79c-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="8a79c-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="8a79c-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="8a79c-153">Oppsettslinje for referansepunkt for kompensasjon</span><span class="sxs-lookup"><span data-stu-id="8a79c-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="8a79c-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="8a79c-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="8a79c-155">Kompensasjonsområde</span><span class="sxs-lookup"><span data-stu-id="8a79c-155">Compensation Region</span></span> | <span data-ttu-id="8a79c-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="8a79c-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="8a79c-157">Kompensasjonsstruktur</span><span class="sxs-lookup"><span data-stu-id="8a79c-157">Compensation Structure</span></span> | <span data-ttu-id="8a79c-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="8a79c-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="8a79c-159">Variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="8a79c-159">Compensation Variable Plan</span></span> | <span data-ttu-id="8a79c-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="8a79c-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="8a79c-161">Nivå for variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="8a79c-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="8a79c-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="8a79c-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="8a79c-163">Type variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="8a79c-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="8a79c-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="8a79c-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="8a79c-165">Fast kompensasjonshendelse</span><span class="sxs-lookup"><span data-stu-id="8a79c-165">Fixed Compensation Event</span></span> | <span data-ttu-id="8a79c-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="8a79c-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="8a79c-167">Overdragelsesregel</span><span class="sxs-lookup"><span data-stu-id="8a79c-167">Vesting Rule</span></span> | <span data-ttu-id="8a79c-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="8a79c-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="8a79c-169">Fast kompensasjon for arbeider</span><span class="sxs-lookup"><span data-stu-id="8a79c-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="8a79c-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="8a79c-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="8a79c-171">Organisasjonstabeller</span><span class="sxs-lookup"><span data-stu-id="8a79c-171">Organization tables</span></span>

| <span data-ttu-id="8a79c-172">Navn</span><span class="sxs-lookup"><span data-stu-id="8a79c-172">Name</span></span> | <span data-ttu-id="8a79c-173">Tabell</span><span class="sxs-lookup"><span data-stu-id="8a79c-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="8a79c-174">Avdeling</span><span class="sxs-lookup"><span data-stu-id="8a79c-174">Department</span></span> | <span data-ttu-id="8a79c-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="8a79c-175">cdm_department</span></span> |
| <span data-ttu-id="8a79c-176">Ansettelse</span><span class="sxs-lookup"><span data-stu-id="8a79c-176">Employment</span></span> | <span data-ttu-id="8a79c-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="8a79c-177">cdm_employment</span></span> |
| <span data-ttu-id="8a79c-178">Bedrift</span><span class="sxs-lookup"><span data-stu-id="8a79c-178">Company</span></span> | <span data-ttu-id="8a79c-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="8a79c-179">cdm_company</span></span> |
| <span data-ttu-id="8a79c-180">Stilling</span><span class="sxs-lookup"><span data-stu-id="8a79c-180">Job</span></span> | <span data-ttu-id="8a79c-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="8a79c-181">cdm_job</span></span> |
| <span data-ttu-id="8a79c-182">Jobbfunksjon</span><span class="sxs-lookup"><span data-stu-id="8a79c-182">Job Function</span></span> | <span data-ttu-id="8a79c-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="8a79c-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="8a79c-184">stilling</span><span class="sxs-lookup"><span data-stu-id="8a79c-184">Job Position</span></span> | <span data-ttu-id="8a79c-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="8a79c-185">cdm_jobposition</span></span> |
| <span data-ttu-id="8a79c-186">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="8a79c-186">Position Type</span></span> | <span data-ttu-id="8a79c-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="8a79c-187">cdm_positiontype</span></span> |
| <span data-ttu-id="8a79c-188">Stillingstilordning</span><span class="sxs-lookup"><span data-stu-id="8a79c-188">Position Worker Assignment</span></span> | <span data-ttu-id="8a79c-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="8a79c-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="8a79c-190">stillingsdimensjon</span><span class="sxs-lookup"><span data-stu-id="8a79c-190">Job Position Dimension</span></span> | <span data-ttu-id="8a79c-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="8a79c-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="8a79c-192">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="8a79c-192">Job Type</span></span> | <span data-ttu-id="8a79c-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="8a79c-193">cdm_jobtype</span></span> |
| <span data-ttu-id="8a79c-194">Språk</span><span class="sxs-lookup"><span data-stu-id="8a79c-194">Language</span></span> | <span data-ttu-id="8a79c-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="8a79c-195">cdm_language</span></span> |
| <span data-ttu-id="8a79c-196">Stillingstittel</span><span class="sxs-lookup"><span data-stu-id="8a79c-196">Title</span></span> | <span data-ttu-id="8a79c-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="8a79c-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="8a79c-198">Finansdimensjoner for **Stillingstype**, **Stillingstilordning** og **Ansettelse** gir enveis integrering til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8a79c-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="8a79c-199">Finansdimensjon-oppdateringer synkroniseres for øyeblikket ikke fra Dataverse til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8a79c-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="8a79c-200">Tabeller for permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="8a79c-200">Leave and absence tables</span></span>

| <span data-ttu-id="8a79c-201">Navn</span><span class="sxs-lookup"><span data-stu-id="8a79c-201">Name</span></span> | <span data-ttu-id="8a79c-202">Tabell</span><span class="sxs-lookup"><span data-stu-id="8a79c-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="8a79c-203">Banktransaksjon for permisjon</span><span class="sxs-lookup"><span data-stu-id="8a79c-203">Leave Bank Transaction</span></span> | <span data-ttu-id="8a79c-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="8a79c-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="8a79c-205">Permisjonsregistrering</span><span class="sxs-lookup"><span data-stu-id="8a79c-205">Leave Enrollment</span></span> | <span data-ttu-id="8a79c-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="8a79c-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="8a79c-207">Permisjonsplan</span><span class="sxs-lookup"><span data-stu-id="8a79c-207">Leave Plan</span></span> | <span data-ttu-id="8a79c-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="8a79c-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="8a79c-209">Permisjonsforespørsel</span><span class="sxs-lookup"><span data-stu-id="8a79c-209">Leave Request</span></span> | <span data-ttu-id="8a79c-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="8a79c-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="8a79c-211">Detaljer for fraværsforespørsel</span><span class="sxs-lookup"><span data-stu-id="8a79c-211">Leave Request Detail</span></span> | <span data-ttu-id="8a79c-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="8a79c-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="8a79c-213">Permisjonstype</span><span class="sxs-lookup"><span data-stu-id="8a79c-213">Leave Type</span></span> | <span data-ttu-id="8a79c-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="8a79c-214">cdm_leavetype</span></span> |
| <span data-ttu-id="8a79c-215">Årsakskode for permisjonstype</span><span class="sxs-lookup"><span data-stu-id="8a79c-215">Leave Type Reason Code</span></span> | <span data-ttu-id="8a79c-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="8a79c-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="8a79c-217">Lønnstabeller</span><span class="sxs-lookup"><span data-stu-id="8a79c-217">Payroll tables</span></span>

| <span data-ttu-id="8a79c-218">Navn</span><span class="sxs-lookup"><span data-stu-id="8a79c-218">Name</span></span> | <span data-ttu-id="8a79c-219">Tabell</span><span class="sxs-lookup"><span data-stu-id="8a79c-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="8a79c-220">Lønnssyklus</span><span class="sxs-lookup"><span data-stu-id="8a79c-220">Pay Cycle</span></span> | <span data-ttu-id="8a79c-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="8a79c-221">cdm_paycycle</span></span> |
| <span data-ttu-id="8a79c-222">Lønnsperiode</span><span class="sxs-lookup"><span data-stu-id="8a79c-222">Pay Period</span></span> | <span data-ttu-id="8a79c-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="8a79c-223">cdm_payperiod</span></span> |
| <span data-ttu-id="8a79c-224">Inntektskode for lønn</span><span class="sxs-lookup"><span data-stu-id="8a79c-224">Payroll Earning Code</span></span> | <span data-ttu-id="8a79c-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="8a79c-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="8a79c-226">Bankkontobetaling</span><span class="sxs-lookup"><span data-stu-id="8a79c-226">Bank Account Disbursement</span></span> | <span data-ttu-id="8a79c-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="8a79c-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="8a79c-228">Avgiftsområde</span><span class="sxs-lookup"><span data-stu-id="8a79c-228">Tax Region</span></span> | <span data-ttu-id="8a79c-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="8a79c-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="8a79c-230">Arbeidertabeller</span><span class="sxs-lookup"><span data-stu-id="8a79c-230">Worker tables</span></span>

| <span data-ttu-id="8a79c-231">Navn</span><span class="sxs-lookup"><span data-stu-id="8a79c-231">Name</span></span> | <span data-ttu-id="8a79c-232">Tabell</span><span class="sxs-lookup"><span data-stu-id="8a79c-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="8a79c-233">Worker</span><span class="sxs-lookup"><span data-stu-id="8a79c-233">Worker</span></span> | <span data-ttu-id="8a79c-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="8a79c-234">cdm_worker</span></span> |
| <span data-ttu-id="8a79c-235">Arbeideradresse</span><span class="sxs-lookup"><span data-stu-id="8a79c-235">Worker Address</span></span> | <span data-ttu-id="8a79c-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="8a79c-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="8a79c-237">Arbeiderens personopplysninger</span><span class="sxs-lookup"><span data-stu-id="8a79c-237">Worker Personal Detail</span></span> | <span data-ttu-id="8a79c-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="8a79c-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="8a79c-239">Personidentifikasjonsnummer for arbeider</span><span class="sxs-lookup"><span data-stu-id="8a79c-239">Worker Person Identification Number</span></span> | <span data-ttu-id="8a79c-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="8a79c-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="8a79c-241">Personidentifikasjonstype for arbeider</span><span class="sxs-lookup"><span data-stu-id="8a79c-241">Worker Person Identification Type</span></span> | <span data-ttu-id="8a79c-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="8a79c-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="8a79c-243">Arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="8a79c-243">Work Calendar</span></span> | <span data-ttu-id="8a79c-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="8a79c-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="8a79c-245">Arbeidskalenderdag</span><span class="sxs-lookup"><span data-stu-id="8a79c-245">Work Calendar Day</span></span> | <span data-ttu-id="8a79c-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="8a79c-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="8a79c-247">Helligdag i arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="8a79c-247">Work Calendar Holiday</span></span> |<span data-ttu-id="8a79c-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="8a79c-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="8a79c-249">Ferielinje for arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="8a79c-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="8a79c-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="8a79c-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="8a79c-251">Tidsintervall for arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="8a79c-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="8a79c-252">cdm_workcalendartimeinterval (ikke aktivert for støtte for egendefinerte felt)</span><span class="sxs-lookup"><span data-stu-id="8a79c-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="8a79c-253">Bankkonto for arbeider</span><span class="sxs-lookup"><span data-stu-id="8a79c-253">Worker Bank Account</span></span> | <span data-ttu-id="8a79c-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="8a79c-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="8a79c-255">Tabeller for arbeideroppsett</span><span class="sxs-lookup"><span data-stu-id="8a79c-255">Worker setup tables</span></span>

| <span data-ttu-id="8a79c-256">Navn</span><span class="sxs-lookup"><span data-stu-id="8a79c-256">Name</span></span> | <span data-ttu-id="8a79c-257">Tabell</span><span class="sxs-lookup"><span data-stu-id="8a79c-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="8a79c-258">Veteranstatus</span><span class="sxs-lookup"><span data-stu-id="8a79c-258">Veteran Status</span></span> | <span data-ttu-id="8a79c-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="8a79c-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="8a79c-260">Etnisk opprinnelse</span><span class="sxs-lookup"><span data-stu-id="8a79c-260">Ethnic Origin</span></span> | <span data-ttu-id="8a79c-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="8a79c-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="8a79c-262">Årsakskode</span><span class="sxs-lookup"><span data-stu-id="8a79c-262">Reason Code</span></span> | <span data-ttu-id="8a79c-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="8a79c-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="8a79c-264">Utstedende byrå for personidentifikasjon</span><span class="sxs-lookup"><span data-stu-id="8a79c-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="8a79c-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="8a79c-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="8a79c-266">Kompetansetabeller</span><span class="sxs-lookup"><span data-stu-id="8a79c-266">Competency tables</span></span>

| <span data-ttu-id="8a79c-267">Navn</span><span class="sxs-lookup"><span data-stu-id="8a79c-267">Name</span></span> | <span data-ttu-id="8a79c-268">Tabell</span><span class="sxs-lookup"><span data-stu-id="8a79c-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="8a79c-269">Kompetansetype</span><span class="sxs-lookup"><span data-stu-id="8a79c-269">Skill Type</span></span> | <span data-ttu-id="8a79c-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="8a79c-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="8a79c-271">Tabellrelasjonsmodeller</span><span class="sxs-lookup"><span data-stu-id="8a79c-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="8a79c-272">Worker</span><span class="sxs-lookup"><span data-stu-id="8a79c-272">Worker</span></span>

![Worker](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="8a79c-274">Jobb og stilling</span><span class="sxs-lookup"><span data-stu-id="8a79c-274">Job and Job Position</span></span>

![Jobb og stilling](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="8a79c-276">Fordeler</span><span class="sxs-lookup"><span data-stu-id="8a79c-276">Benefits</span></span>

![Fordeler](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="8a79c-278">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="8a79c-278">Compensation</span></span>

![Kompensasjon](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="8a79c-280">Permisjon</span><span class="sxs-lookup"><span data-stu-id="8a79c-280">Leave</span></span>

![Permisjon](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="8a79c-282">Arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="8a79c-282">Work Calendar</span></span>

![Arbeidskalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="8a79c-284">Se også</span><span class="sxs-lookup"><span data-stu-id="8a79c-284">See also</span></span>

[<span data-ttu-id="8a79c-285">Velge en dataintegreringsteknologi</span><span class="sxs-lookup"><span data-stu-id="8a79c-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="8a79c-286">Konfigurere Dataverse-integrering</span><span class="sxs-lookup"><span data-stu-id="8a79c-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="8a79c-287">Konfigurere virtuelle Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="8a79c-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="8a79c-288">Vanlige spørsmål om virtuelle tabeller for Human Resources</span><span class="sxs-lookup"><span data-stu-id="8a79c-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="8a79c-289">Hva er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="8a79c-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="8a79c-290">Terminologioppdateringer</span><span class="sxs-lookup"><span data-stu-id="8a79c-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]