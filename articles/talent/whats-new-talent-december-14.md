---
title: Hva er nytt eller endret i Dynamics 365 for Talent Core HR (14. desember 2018)?
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7d2866923efd7f115ad5290f35ed4fcac5e47573
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "305558"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a><span data-ttu-id="c909b-103">Hva er nytt eller endret i Dynamics 365 for Talent Core HR (14. desember 2018)?</span><span class="sxs-lookup"><span data-stu-id="c909b-103">What's new or changed in Dynamics 365 for Talent Core HR (December 14, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c909b-104">**Build 8.1.2085**</span><span class="sxs-lookup"><span data-stu-id="c909b-104">**Build 8.1.2085**</span></span>

<span data-ttu-id="c909b-105">Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.</span><span class="sxs-lookup"><span data-stu-id="c909b-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="c909b-106">Endringer</span><span class="sxs-lookup"><span data-stu-id="c909b-106">Changes</span></span>

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a><span data-ttu-id="c909b-107">USA - ACA (lov om Affordable Care)-støtte for skatteåret 2018 1095-B- og 1095-C-skjemaer</span><span class="sxs-lookup"><span data-stu-id="c909b-107">US - ACA (Affordable Care Act) support for tax year 2018 1095-B and 1095-C forms</span></span>

<span data-ttu-id="c909b-108">Hvert år må aktuelle store arbeidsgivere angi alle fulltidsansatte med 1095-C.</span><span class="sxs-lookup"><span data-stu-id="c909b-108">Each year, Applicable Large Employers (ALEs) must provide each full-time employees with a 1095-C.</span></span> <span data-ttu-id="c909b-109">Hvis arbeidsgiveren også gir selvforsikret dekning, må de angi 1095-C (hvis de er en større arbeidsgiver) og 1095-B (hvis de er en mindre arbeidsgiver) for ansatte, fulltid eller deltid, som dekkes av en av de tilbudte helseplanene.</span><span class="sxs-lookup"><span data-stu-id="c909b-109">In addition, if the employer provides self-insured coverage they must provide the 1095-C (if they are an ALE) and a 1095-B (if they are a small employer) to any employee, full-time or part-time, covered under one of their offered health plans.</span></span> <span data-ttu-id="c909b-110">Denne funksjonen gir utskrivbare skjemaer for både 1095-C og 1095-B.</span><span class="sxs-lookup"><span data-stu-id="c909b-110">This feature provides printable forms for both the 1095-C and 1095-B.</span></span>

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a><span data-ttu-id="c909b-111">Under import ignoreres SubmittedByPersonId-feltet i HcmPerfJournalEntity</span><span class="sxs-lookup"><span data-stu-id="c909b-111">During import SubmittedByPersonId field on HcmPerfJournalEntity is ignored</span></span>

<span data-ttu-id="c909b-112">Ved import/eksport av ytelsesjournalposter ignoreres **Sendt av**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c909b-112">When importing/exporting performance journal entries, the **Submitted by** field is ignored.</span></span> <span data-ttu-id="c909b-113">Med denne endringen gjenspeiler verdien **importert/eksportert** verdien i tabellen under eksporten. Ved import oppdateres systemet med verdien som er angitt i importfilen.</span><span class="sxs-lookup"><span data-stu-id="c909b-113">With this change, the value **imported/exported** will reflect the value in the table during the export, when importing the system will be updated with the value supplied in the import file.</span></span>

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a><span data-ttu-id="c909b-114">Analyse-kategorien i arbeidsområdet Permisjon og fravær viser feilen OpenConnectionError for ikke-systemadministratorroller</span><span class="sxs-lookup"><span data-stu-id="c909b-114">Analytics tab on 'Leave and absence' workspace displays "OpenConnectionError" error for non-system Admin roles</span></span>

<span data-ttu-id="c909b-115">Med denne oppdateringen utstedes det ikke feil når du åpner **Analyse**-kategorien i **Permisjon og fravær**-arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="c909b-115">With this update, no errors will be issued when opening the **Analytics** tab on the **Leave and Absence** workspace.</span></span>

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="c909b-116">Neddrilling i Ansattselvbetjening, Stillingshierarki fra flis kan ikke hente overordnet node</span><span class="sxs-lookup"><span data-stu-id="c909b-116">Employee self-service, Position Hierarchy drill-down from tile fails to get parent node</span></span>

<span data-ttu-id="c909b-117">En endring er gjort for å rette feilen «Henting av den overordnede noden mislyktes» når stillingshierarkiet er tilpasset for å vises i et eksisterende arbeidsområde og en stilling er valgt i hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="c909b-117">A change has been made to correct the error "Getting the parent node failed" when the position hierarchy has been personalized to appear on an existing workspace and a position is selected in the hierarchy.</span></span>  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a><span data-ttu-id="c909b-118">Må være systemadministrator for å kunne se kategorien Lønn på Stilling-siden</span><span class="sxs-lookup"><span data-stu-id="c909b-118">Must be System Admin to see the Payroll tab in the Position page</span></span>

<span data-ttu-id="c909b-119">En endring er gjort for å inkludere de riktige sikkerhetselementene i den eksisterende rettigheten: Vedlikehold lønnsdetaljer for arbeider og stilling.</span><span class="sxs-lookup"><span data-stu-id="c909b-119">A change has been made to include the correct security elements in the existing privilege: "Maintain payroll worker and position detail".</span></span> <span data-ttu-id="c909b-120">Med denne endringen får lønnsadministratoren som standard tilgang til lønnsfeltene på Stilling-siden.</span><span class="sxs-lookup"><span data-stu-id="c909b-120">With this change, by default, the Payroll Administrator will have access to the Payroll fields on the Position page.</span></span>

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a><span data-ttu-id="c909b-121">Feil når du sender prestasjonsvurdering til leder og plassholderen %Reviews.PerfPeriod% brukes i sendeinstruksjonene</span><span class="sxs-lookup"><span data-stu-id="c909b-121">Error when submitting performance review to manager and the %Reviews.PerfPeriod% placeholder is used in the Submission instructions</span></span>

<span data-ttu-id="c909b-122">Det er gjort en endring som retter opp feilen Nullreferanse når du bruker plassholderen %Reviews.PerfPeriod% i sendeinstruksjonene.</span><span class="sxs-lookup"><span data-stu-id="c909b-122">A change has been made that corrects the "Null Reference" error when using the %Reviews.PerfPeriod% placeholder in the Submission instructions.</span></span>

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a><span data-ttu-id="c909b-123">Workforce Power BI-rapporten viser feil når arbeiderens ansiennitetsdato er en skuddårsdag.</span><span class="sxs-lookup"><span data-stu-id="c909b-123">Workforce Power BI report shows error when worker seniority date is a leap day</span></span>

<span data-ttu-id="c909b-124">Med denne endringen støttes nå skuddårsdager i Power BI.</span><span class="sxs-lookup"><span data-stu-id="c909b-124">With this change, leap days are now supported in Power BI.</span></span>

### <a name="integration-between-core-hr-and-attract"></a><span data-ttu-id="c909b-125">Integrasjon mellom Core HR og Attract</span><span class="sxs-lookup"><span data-stu-id="c909b-125">Integration between Core HR and Attract</span></span>

<span data-ttu-id="c909b-126">En endring er gjort for å oppdatere integreringen mellom Core HR og Attract knyttet til kandidater som skal ansettes.</span><span class="sxs-lookup"><span data-stu-id="c909b-126">A change has been made to update the integration between Core HR and Attract related to candidates to hire.</span></span> <span data-ttu-id="c909b-127">For at kandidater som skal ansettes, skal vises i **Personaladministrasjon**-arbeidsområdet brukes følgende CDS for Apps (CDS 2.0)-enheter:</span><span class="sxs-lookup"><span data-stu-id="c909b-127">For candidates to hire to be visible in the **Personnel Management** workspace, the following CDS for Apps (CDS 2.0) entities are used:</span></span>

<span data-ttu-id="c909b-128">Stillingssøknad</span><span class="sxs-lookup"><span data-stu-id="c909b-128">Job Application</span></span>
- <span data-ttu-id="c909b-129">Statusårsak må settes til Tilbud godtatt</span><span class="sxs-lookup"><span data-stu-id="c909b-129">Status Reason needs to be set to Offer Accepted</span></span>
-   <span data-ttu-id="c909b-130">Angir kandidat og ledig stilling</span><span class="sxs-lookup"><span data-stu-id="c909b-130">Provides Candidate and Job Opening</span></span>

<span data-ttu-id="c909b-131">Kandidat</span><span class="sxs-lookup"><span data-stu-id="c909b-131">Candidate</span></span>
-   <span data-ttu-id="c909b-132">Angir kandidatinformasjon</span><span class="sxs-lookup"><span data-stu-id="c909b-132">Provides Candidate information</span></span>

<span data-ttu-id="c909b-133">Ledig stilling</span><span class="sxs-lookup"><span data-stu-id="c909b-133">Job Opening</span></span>
-   <span data-ttu-id="c909b-134">Angir ID for ledig stilling og deltakere for ledig stilling</span><span class="sxs-lookup"><span data-stu-id="c909b-134">Provides Job Opening ID and Job Opening Participants</span></span>

<span data-ttu-id="c909b-135">Deltakere for ledig stilling</span><span class="sxs-lookup"><span data-stu-id="c909b-135">Job Opening Participants</span></span>
-   <span data-ttu-id="c909b-136">Angir ansettelsesansvarlig</span><span class="sxs-lookup"><span data-stu-id="c909b-136">Provides Hiring Manager</span></span>

<span data-ttu-id="c909b-137">Når en kandidat legges til personaladministrasjon, kan kandidaten nå også forkastes ved hjelp av et nytt alternativ på kandidatkortet.</span><span class="sxs-lookup"><span data-stu-id="c909b-137">When a candidate is added to Personnel Management, the candidate can now also be dismissed using a new option available on the candidate card.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="c909b-138">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="c909b-138">Coming soon</span></span>

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a><span data-ttu-id="c909b-139">Permisjon og fravær: Saldoer for fremtidig permisjon og permisjonsprognoser</span><span class="sxs-lookup"><span data-stu-id="c909b-139">Leave and absence: Future leave and forecasting leave balances</span></span>

<span data-ttu-id="c909b-140">Med endringene som gjøres for å la ansatte planlegge avspasering og be om fremtidige fraværsforespørsler uten å påvirke gjeldende avspaseringssaldoer, endres også måten avspaseringssaldoer vises på.</span><span class="sxs-lookup"><span data-stu-id="c909b-140">With the changes being made to allow for employees to forecast time off and request future time off requests without impacting their current time off balances, the way the time off balances are displayed is also changing.</span></span> 

<span data-ttu-id="c909b-141">Tilgjengelig saldo som vises nå, er hvor mye avspasering som er tilgjengelig for forespørsler, inkludert avsetninger til og med i dag og alle godkjente permisjonsforespørsler til sluttidspunktet.</span><span class="sxs-lookup"><span data-stu-id="c909b-141">The available balance currently displayed is the amount of time off available for requests including accruals through today and all approved leave requests to the end of time.</span></span> 

<span data-ttu-id="c909b-142">Når muligheten for prognostisering gis ut, endres den viste saldoen til gjeldende avspaseringssaldo, inkludert avsetninger til og med i dag og forespørsler til og med i dag.</span><span class="sxs-lookup"><span data-stu-id="c909b-142">When the ability to forecast is released, the balance displayed changes to  be the current balance of time off including accruals through today and requests through today.</span></span> <span data-ttu-id="c909b-143">Ansatte og ledere vil se disse oppdaterte saldoene i ansatt- og lederselvbetjening på **Fridager**-kortet og i vinduet for **avspaseringssaldoer**.</span><span class="sxs-lookup"><span data-stu-id="c909b-143">Employees and managers will see these updated balances in employee and manager self-service on the **Time off** card and in the **Time off balances** window.</span></span> <span data-ttu-id="c909b-144">Personalledere vil se disse oppdaterte saldoene i **Personer**-arbeidsområdet og i vinduet **Tilordnede permisjonsplaner** for ansatte.</span><span class="sxs-lookup"><span data-stu-id="c909b-144">HR managers will see these updated balances in the **People** workspace and in the employee’s **Assigned leave plans** window.</span></span>

## <a name="known-issue"></a><span data-ttu-id="c909b-145">Kjent problem</span><span class="sxs-lookup"><span data-stu-id="c909b-145">Known issue</span></span>

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a><span data-ttu-id="c909b-146">Tilordningsfeil i integrasjonen med Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c909b-146">Mapping errors in the integration with Finance and Operations</span></span>

<span data-ttu-id="c909b-147">Følgende problemer er identifisert i gjeldende mal for integrering av Talent med Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c909b-147">The following issues have been identified in the current template for integrating Talent with Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="c909b-148">En ny mal blir snart publisert og skal brukes på alle nye integrasjonsprosjekter som opprettes.</span><span class="sxs-lookup"><span data-stu-id="c909b-148">A new template will be published soon and will be applied to all new integration projects that are created.</span></span> <span data-ttu-id="c909b-149">For eksisterende integrasjonsprosjekter kan oppgavetilordningene oppdateres.</span><span class="sxs-lookup"><span data-stu-id="c909b-149">For existing integration projects, the task mappings can be updated.</span></span> <span data-ttu-id="c909b-150">Se følgende tabell for oppdaterte tilordninger.</span><span class="sxs-lookup"><span data-stu-id="c909b-150">Refer to the following table for updated mappings.</span></span> 

>[!NOTE]
> <span data-ttu-id="c909b-151">Den overordnede jobbtilordningsoppgaven for jobbstillinger til stillinger kan ikke integrere data.</span><span class="sxs-lookup"><span data-stu-id="c909b-151">The Job Positions to Positions Parent Job Assignment task does not integrate data.</span></span> <span data-ttu-id="c909b-152">Dette er et problem som undersøkes nå.</span><span class="sxs-lookup"><span data-stu-id="c909b-152">This is an issue that is currently being researched.</span></span> <span data-ttu-id="c909b-153">Det finnes ingen løsning i gjeldende tilordning.</span><span class="sxs-lookup"><span data-stu-id="c909b-153">There is no workaround in the current mapping.</span></span> 

<span data-ttu-id="c909b-154">Avdelinger til driftsenhet-oppgaven må ha følgende tilordninger oppdatert.</span><span class="sxs-lookup"><span data-stu-id="c909b-154">The Departments to Operating unit task needs the following mappings updated.</span></span>

| <span data-ttu-id="c909b-155">Eksisterende kildefelt</span><span class="sxs-lookup"><span data-stu-id="c909b-155">Existing source field</span></span>          | <span data-ttu-id="c909b-156">Nytt kildefelt</span><span class="sxs-lookup"><span data-stu-id="c909b-156">New source field</span></span> |
| -------------------------------|------------------|
| <span data-ttu-id="c909b-157">cdm_description (beskrivelse)</span><span class="sxs-lookup"><span data-stu-id="c909b-157">cdm_description (Description)</span></span>  | <span data-ttu-id="c909b-158">cdm_name (navn)</span><span class="sxs-lookup"><span data-stu-id="c909b-158">cdm_name (Name)</span></span>  |

<span data-ttu-id="c909b-159">En ekstra tilordning må også legges til.</span><span class="sxs-lookup"><span data-stu-id="c909b-159">An additional mapping also needs to be added.</span></span> <span data-ttu-id="c909b-160">Velg det siste **Ingen**-feltet for å legge til følgende tilordning.</span><span class="sxs-lookup"><span data-stu-id="c909b-160">Select the last **None** field to add the following mapping.</span></span>

| <span data-ttu-id="c909b-161">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="c909b-161">Source field</span></span>                   | <span data-ttu-id="c909b-162">Målfelt</span><span class="sxs-lookup"><span data-stu-id="c909b-162">Destination field</span></span>    |
| -------------------------------|----------------------|
| <span data-ttu-id="c909b-163">cdm_description (beskrivelse)</span><span class="sxs-lookup"><span data-stu-id="c909b-163">cdm_description (Description)</span></span>  | <span data-ttu-id="c909b-164">NAMEALIAS (NAMEALIAS)</span><span class="sxs-lookup"><span data-stu-id="c909b-164">NAMEALIAS (NAMEALIAS)</span></span>|

<span data-ttu-id="c909b-165">De oppdaterte tilordningene skal se ut som følgende bilde.</span><span class="sxs-lookup"><span data-stu-id="c909b-165">The updated mappings should look like the following image.</span></span>

![Avdelinger til driftsenhet-oppgaven](./media/DepartmentMapping.png)


<span data-ttu-id="c909b-167">Jobber til jobbdetaljer-oppgaven må ha følgende tilordninger oppdatert.</span><span class="sxs-lookup"><span data-stu-id="c909b-167">The Jobs to Job Detail task needs the following mappings updated.</span></span>

| <span data-ttu-id="c909b-168">Eksisterende kildefelt</span><span class="sxs-lookup"><span data-stu-id="c909b-168">Existing source field</span></span>          | <span data-ttu-id="c909b-169">Nytt kildefelt</span><span class="sxs-lookup"><span data-stu-id="c909b-169">New source field</span></span>                   |
| -------------------------------|------------------------------------|
| <span data-ttu-id="c909b-170">cdm_name (navn)</span><span class="sxs-lookup"><span data-stu-id="c909b-170">cdm_name (Name)</span></span>                | <span data-ttu-id="c909b-171">cdm_description (beskrivelse)</span><span class="sxs-lookup"><span data-stu-id="c909b-171">cdm_description (Description)</span></span>      |
| <span data-ttu-id="c909b-172">cdm_name (beskrivelse)</span><span class="sxs-lookup"><span data-stu-id="c909b-172">cdm_name (Description)</span></span>         | <span data-ttu-id="c909b-173">cdm_jobdescription(jobbeskrivelse)</span><span class="sxs-lookup"><span data-stu-id="c909b-173">cdm_jobdescription(Job Description)</span></span>|


<span data-ttu-id="c909b-174">De oppdaterte tilordningene skal se ut som bildet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="c909b-174">The updated mappings should look like the image below.</span></span>

![Jobber til jobbdetaljer-oppgaven](./media/JobMapping.png)

<span data-ttu-id="c909b-176">Arbeidere til arbeid-oppgaven må ha følgende tilordninger oppdatert.</span><span class="sxs-lookup"><span data-stu-id="c909b-176">The Workers to Work task needs the following mappings updated.</span></span>

| <span data-ttu-id="c909b-177">Eksisterende kildefelt</span><span class="sxs-lookup"><span data-stu-id="c909b-177">Existing source field</span></span>                 | <span data-ttu-id="c909b-178">Nytt kildefelt</span><span class="sxs-lookup"><span data-stu-id="c909b-178">New source field</span></span>                               |
| --------------------------------------|------------------------------------------------|
| <span data-ttu-id="c909b-179">cdm_emailaddress1 (e-postadresse 1)</span><span class="sxs-lookup"><span data-stu-id="c909b-179">cdm_emailaddress1 (Email Address 1)</span></span>   | <span data-ttu-id="c909b-180">cdm_primaryemailaddress (primær e-postadresse)</span><span class="sxs-lookup"><span data-stu-id="c909b-180">cdm_primaryemailaddress (Primary Email Address</span></span> |
| <span data-ttu-id="c909b-181">cdm_telephone1 (telefon 1)</span><span class="sxs-lookup"><span data-stu-id="c909b-181">cdm_telephone1 (Telephone 1)</span></span>          | <span data-ttu-id="c909b-182">cdm_primarytelephone (hovedtelefon)</span><span class="sxs-lookup"><span data-stu-id="c909b-182">cdm_primarytelephone (Primary Telephone)</span></span>       |

<span data-ttu-id="c909b-183">Endringen av Kjønn-feltet må også oppdateres.</span><span class="sxs-lookup"><span data-stu-id="c909b-183">The Gender field transform also needs to be updated.</span></span> <span data-ttu-id="c909b-184">Velg tilordningstypen **fn** (funksjon) for kjønn og oppdater følgende verditilordninger.</span><span class="sxs-lookup"><span data-stu-id="c909b-184">Select the **fn** (function) map type for Gender and update the following value mappings.</span></span>

| <span data-ttu-id="c909b-185">CDS-verdi</span><span class="sxs-lookup"><span data-stu-id="c909b-185">CDS value</span></span>                   | <span data-ttu-id="c909b-186">Finance and Operations-verdi</span><span class="sxs-lookup"><span data-stu-id="c909b-186">Finance and Operations value</span></span>                     |
| ----------------------------|--------------------------------------------------|
| <span data-ttu-id="c909b-187">75440000</span><span class="sxs-lookup"><span data-stu-id="c909b-187">75440000</span></span>                    | <span data-ttu-id="c909b-188">Mann</span><span class="sxs-lookup"><span data-stu-id="c909b-188">Male</span></span>                                             |
| <span data-ttu-id="c909b-189">75440001</span><span class="sxs-lookup"><span data-stu-id="c909b-189">75440001</span></span>                    | <span data-ttu-id="c909b-190">Kvinne</span><span class="sxs-lookup"><span data-stu-id="c909b-190">Female</span></span>                                           |
| <span data-ttu-id="c909b-191">75440002</span><span class="sxs-lookup"><span data-stu-id="c909b-191">75440002</span></span>                    | <span data-ttu-id="c909b-192">Ingen</span><span class="sxs-lookup"><span data-stu-id="c909b-192">None</span></span>                                             | 
| <span data-ttu-id="c909b-193">75440003</span><span class="sxs-lookup"><span data-stu-id="c909b-193">75440003</span></span>                    | <span data-ttu-id="c909b-194">Ikke-spesifikt</span><span class="sxs-lookup"><span data-stu-id="c909b-194">NonSpecific</span></span>                                      |

<span data-ttu-id="c909b-195">De oppdaterte tilordningene skal se ut som følgende bilder.</span><span class="sxs-lookup"><span data-stu-id="c909b-195">The updated mappings should look like the following images.</span></span>

![Arbeidere til arbeider-oppgaven](./media/WorkerMapping.png)

![Endring av Kjønn-feltet](./media/WorkerTransform.png)
