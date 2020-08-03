---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (08. juli 2020)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 7/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8fe7bc33407bd5781d565f854c0f096766da5fc9
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555394"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a><span data-ttu-id="93599-103">Hva er nytt eller endret i Dynamics 365 Human Resources (8. juli 2020)</span><span class="sxs-lookup"><span data-stu-id="93599-103">What's new or changed in Dynamics 365 Human Resources (July 8, 2020)</span></span>

<span data-ttu-id="93599-104">Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="93599-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="93599-105">Endringer gjelder for Build-nummeret 8.1.3382.</span><span class="sxs-lookup"><span data-stu-id="93599-105">Changes apply to build number 8.1.3382.</span></span> <span data-ttu-id="93599-106">Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.</span><span class="sxs-lookup"><span data-stu-id="93599-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="database-logging"></a><span data-ttu-id="93599-107">Databaselogging</span><span class="sxs-lookup"><span data-stu-id="93599-107">Database logging</span></span>

<span data-ttu-id="93599-108">Med databaseloggføring kan du bestemme hvilke tabeller og felt som skal overvåkes.</span><span class="sxs-lookup"><span data-stu-id="93599-108">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="93599-109">Du kan også fastslå hvilke hendelser som skal utløse endringssporing.</span><span class="sxs-lookup"><span data-stu-id="93599-109">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="93599-110">Du kan bruke funksjonen for databaselogging for å se endringene over tid.</span><span class="sxs-lookup"><span data-stu-id="93599-110">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="93599-111">Hvis du vil ha mer informasjon, se [Konfigurere og administrere databaselogging](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="93599-111">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="93599-112">Konfigurere navnet på ansattselvbetjening</span><span class="sxs-lookup"><span data-stu-id="93599-112">Configure the name of Employee self service</span></span>

<span data-ttu-id="93599-113">I **Parametere for Personale** kan du nå endre navnet på **Ansattselvbetjening**-arbeidsområdet til **Selvbetjening**.</span><span class="sxs-lookup"><span data-stu-id="93599-113">In **Human Resources parameters**, you can now change the name of the **Employee self service** workspace to **Self service**.</span></span> <span data-ttu-id="93599-114">Hvis du vil ha mer informasjon, se [Endre navn på arbeidsområde for selvbetjening for ansatte](hr-employee-self-service-workspace-name.md)</span><span class="sxs-lookup"><span data-stu-id="93599-114">For more information, see [Change Employee self service workspace name](hr-employee-self-service-workspace-name.md)</span></span>

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a><span data-ttu-id="93599-115">Fordelsstyring åpner registreringstilgang utenfor perioden</span><span class="sxs-lookup"><span data-stu-id="93599-115">Benefits management open enrollment access outside of period</span></span>

<span data-ttu-id="93599-116">Denne versjonen retter opp en feil der ansatte kan få tilgang til fordeler ved å åpne registrering utenfor registreringsperioden eller uten en levetidshendelse.</span><span class="sxs-lookup"><span data-stu-id="93599-116">This release fixes a bug where employees could access benefits open enrollment outside of the enrollment period or without a life event.</span></span> <span data-ttu-id="93599-117">Hvis du trenger demonstrasjon av åpen registrering i Ansattselvbetjening, må du derfor justere datoene for åpen registrering til i dag (eller tidligere) for å gjøre den tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="93599-117">As a result, if you need to demo open enrollment in Employee self service, you must adjust the open enrollment dates to today (or earlier) to make it accessible.</span></span> <span data-ttu-id="93599-118">Du kan endre denne innstillingen under **Fordelsbehandling > Regler og alternativperioder**.</span><span class="sxs-lookup"><span data-stu-id="93599-118">You can change this setting under **Benefits management > Rules and options periods**.</span></span>

## <a name="email-employee-enrollment-confirmation"></a><span data-ttu-id="93599-119">E-postbekreftelse på ansattregistrering</span><span class="sxs-lookup"><span data-stu-id="93599-119">Email employee enrollment confirmation</span></span>

<span data-ttu-id="93599-120">Du kan nå sende e-postmeldinger til ansatte etter at de har fullført sine fordelsvalg.</span><span class="sxs-lookup"><span data-stu-id="93599-120">You can now send emails to employees after they complete their benefits selection.</span></span> <span data-ttu-id="93599-121">Du kan enten sende en standardmelding eller bruke en organisasjonse-postmal.</span><span class="sxs-lookup"><span data-stu-id="93599-121">You can either send a default message or use an organization email template.</span></span> <span data-ttu-id="93599-122">Disse innstillingene er under **Personalparametere > Fordelsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="93599-122">These settings are under **Human resource parameters > Benefits management**.</span></span>

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a><span data-ttu-id="93599-123">Avbrutt permisjon vises fortsatt i kommende fridager i Personer-arbeidsområdet (441358)</span><span class="sxs-lookup"><span data-stu-id="93599-123">Canceled leave still appears in upcoming time off on People workspace (441358)</span></span>

<span data-ttu-id="93599-124">Avbrutt permisjon vises ikke lenger i kommende fritid på permisjonskortene i **Personer**-arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="93599-124">Canceled leave no longer displays as upcoming time off on the leave cards in the **People** workspace.</span></span>

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a><span data-ttu-id="93599-125">Kan ikke bruke egenskapen for avdelingsenhet i PositionV2-enheten (456486)</span><span class="sxs-lookup"><span data-stu-id="93599-125">Unable to use the department entity property in the PositionV2 entity (456486)</span></span>

<span data-ttu-id="93599-126">Du kan nå legge til en avdeling uten å opprette en duplikat relasjon.</span><span class="sxs-lookup"><span data-stu-id="93599-126">You can now add a department without creating a duplicate relation.</span></span>

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a><span data-ttu-id="93599-127">PayrollWorkerEnrolledBenefitDetailEntity bør bare bruke beregnet felt for pensjonsplaner (459779)</span><span class="sxs-lookup"><span data-stu-id="93599-127">PayrollWorkerEnrolledBenefitDetailEntity should only use calculated field for retirement plans (459779)</span></span>

<span data-ttu-id="93599-128">Når du eksporterer **PayrollWorkerEnrolledBenefitDetailEntity**-enheten, bestemmer eksporten om den skal bruke et beregnet felt basert på en rentetabell eller bruke **ContributionAmountCur**-feltet i backing-tabellen.</span><span class="sxs-lookup"><span data-stu-id="93599-128">When exporting the **PayrollWorkerEnrolledBenefitDetailEntity** entity, the export determines whether it should use a calculated field based on a rate table or use the **ContributionAmountCur** field on the backing table.</span></span> <span data-ttu-id="93599-129">Logikken som brukes av dataenheten, bruker pristabellen i situasjoner der programmet vanligvis ikke gjør det.</span><span class="sxs-lookup"><span data-stu-id="93599-129">The logic used by the data entity uses the rate table in situations where the application normally doesn't.</span></span> <span data-ttu-id="93599-130">Denne logikken gjør at enheten eksporterer for å returnere en nullverdi for denne kolonnen, fordi det ikke er noen pristabell for beregning, og produktet tillater ikke at kunden angir en.</span><span class="sxs-lookup"><span data-stu-id="93599-130">This logic causes the entity exports to return a zero value for this column, because there's no calculation rate table and the product doesn't allow the customer to specify one.</span></span>
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a><span data-ttu-id="93599-131">Forvirrende oversettelser i tsjekkisk språk i Personaladministrasjon og Ansattselvbetjening (400276)</span><span class="sxs-lookup"><span data-stu-id="93599-131">Confusing translations in Czech language in Personnel management and Employee self service (400276)</span></span>

<span data-ttu-id="93599-132">Denne versjonen korrigerer oversettelsene for **Firmakatalog**, **Neste registrerte kurs**, **Jobb** og **Stilling**.</span><span class="sxs-lookup"><span data-stu-id="93599-132">This release corrects the translations for **Company directory**, **Next registered course**, **Job**, and **Position**.</span></span>
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a><span data-ttu-id="93599-133">WorkCalendarEmployment-tabellen har ikke de opprettede og endrede systemfeltene aktivert (460171)</span><span class="sxs-lookup"><span data-stu-id="93599-133">The WorkCalendarEmployment table doesn't have the created and modified system fields enabled (460171)</span></span>

<span data-ttu-id="93599-134">Opprettede og endrede systemfelt er nå aktivert i tabellen **WorkCalendarEmployment** i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="93599-134">Created and modified system fields are now enabled on the **WorkCalendarEmployment** table in Human Resources.</span></span>
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a><span data-ttu-id="93599-135">Nullreferanseunntak for ansettelse og tillegging av informasjon for fremtidige ansatte (455475)</span><span class="sxs-lookup"><span data-stu-id="93599-135">Null reference exception for Hire and add details for future employee (455475)</span></span>

<span data-ttu-id="93599-136">Denne versjonen korrigerer en feil (nullreferanse) i strømlinjeformet ansattregistrering når du ansetter en person ved hjelp av alternativet for **Ansett og legg til detaljer**.</span><span class="sxs-lookup"><span data-stu-id="93599-136">This release corrects an error (null reference) in streamlined employee entry when you hire an employee using the option to **Hire and add details**.</span></span>

## <a name="changes-made-in-the-common-data-service-worker-entity-dont-reflect-in-human-resources-455652"></a><span data-ttu-id="93599-137">Endringer som er gjort i arbeiderenheten i Common Data Service, gjenspeiles ikke i Human Resources (455652)</span><span class="sxs-lookup"><span data-stu-id="93599-137">Changes made in the Common Data Service Worker entity don't reflect in Human Resources (455652)</span></span>

<span data-ttu-id="93599-138">Endringer som er gjort i følgende felt i **Arbeider**-enheten i Common Data Service, vises nå i Human Resources:</span><span class="sxs-lookup"><span data-stu-id="93599-138">Changes made to the following fields in the **Worker** entity in Common Data Service will now show up in Human Resources:</span></span>

- <span data-ttu-id="93599-139">**Fungerer hjemmefra**</span><span class="sxs-lookup"><span data-stu-id="93599-139">**Works from home**</span></span>
- <span data-ttu-id="93599-140">**Ansiennitetsdato**</span><span class="sxs-lookup"><span data-stu-id="93599-140">**Seniority date**</span></span>
- <span data-ttu-id="93599-141">**Jubileumsdato**</span><span class="sxs-lookup"><span data-stu-id="93599-141">**Anniversary date**</span></span>
- <span data-ttu-id="93599-142">**Opprinnelig ansettelsesdato**</span><span class="sxs-lookup"><span data-stu-id="93599-142">**Original hire date**</span></span>

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a><span data-ttu-id="93599-143">Riktig kompensasjonsnivå går ikke til standarden basert på jobben som er tilordnet til stillingen (394136)</span><span class="sxs-lookup"><span data-stu-id="93599-143">Correct compensation level doesn't default based on the job assigned to the position (394136)</span></span>

<span data-ttu-id="93599-144">Med denne endringen går det riktige kompensasjonsnivået til standarden basert på **Gyldig dato**-poster for **Stillingsdetaljer** og **Startdatoen** for **Kompensasjonsplantilordningen**.</span><span class="sxs-lookup"><span data-stu-id="93599-144">With this change, the correct compensation level defaults based on the **Date effective** records for the **Position details** and the **Start date** of the **Compensation plan assignment**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="93599-145">I forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="93599-145">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="93599-146">Obligatorisk felt</span><span class="sxs-lookup"><span data-stu-id="93599-146">Mandatory fields</span></span> 

<span data-ttu-id="93599-147">Du kan nå endre feltene ved hjelp av tilpasningsfunksjonene i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="93599-147">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="93599-148">Denne funksjonen krever **Lagrede visninger**.</span><span class="sxs-lookup"><span data-stu-id="93599-148">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="93599-149">Human Resources-søknad i Teams</span><span class="sxs-lookup"><span data-stu-id="93599-149">Human Resources application in Teams</span></span>

<span data-ttu-id="93599-150">Ansatte kan se og be om fravær fra jobb i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="93599-150">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="93599-151">De kan kommunisere med en robot for å opprette permisjonsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="93599-151">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="93599-152">For mer informasjon, se [Human Resources-app i Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="93599-152">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="93599-153">Data Management Framework (DMF)-enheter for Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="93599-153">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="93599-154">Enheter for fordelsstyring frigis.</span><span class="sxs-lookup"><span data-stu-id="93599-154">Benefits management entities are releasing.</span></span> <span data-ttu-id="93599-155">DMF-enheter gjør det mulig å importere og eksportere data slik at du enkelt kan konfigurere fordelsbehandling.</span><span class="sxs-lookup"><span data-stu-id="93599-155">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="93599-156">En mal for fordelsbehandling vil være tilgjengelig for å flytte data.</span><span class="sxs-lookup"><span data-stu-id="93599-156">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="93599-157">Malen eksporterer og importerer data på en sekvensiell måte for å respektere dataavhengigheter.</span><span class="sxs-lookup"><span data-stu-id="93599-157">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="93599-158">Kjøp og selg permisjon</span><span class="sxs-lookup"><span data-stu-id="93599-158">Buy and sell leave</span></span> 

<span data-ttu-id="93599-159">Noen organisasjoner tilbyr en fordel som gjør det mulig for ansatte å kjøpe eller selge permisjon.</span><span class="sxs-lookup"><span data-stu-id="93599-159">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="93599-160">Denne prosessen behandles ofte manuelt.</span><span class="sxs-lookup"><span data-stu-id="93599-160">This process is often managed manually.</span></span> <span data-ttu-id="93599-161">Denne funksjonen automatiserer behandling av policyer og forespørsler for personalavdelingen.</span><span class="sxs-lookup"><span data-stu-id="93599-161">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="93599-162">Den strømlinjeformer permisjonsstyringsprosessen og bidrar til å eliminere feil.</span><span class="sxs-lookup"><span data-stu-id="93599-162">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="93599-163">Hvis du vil ha mer informasjon, kan du se:</span><span class="sxs-lookup"><span data-stu-id="93599-163">For more information, see:</span></span>

- [<span data-ttu-id="93599-164">Administrere policyer for kjøp og salg av permisjon</span><span class="sxs-lookup"><span data-stu-id="93599-164">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="93599-165">Kjøp og selg permisjon</span><span class="sxs-lookup"><span data-stu-id="93599-165">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="93599-166">Permisjonsavsetning for ett enkelt firma eller én enkelt plan</span><span class="sxs-lookup"><span data-stu-id="93599-166">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="93599-167">Kunder kan behandle avsetninger for ett enkelt firma eller en enkel permisjons- og fraværsplan.</span><span class="sxs-lookup"><span data-stu-id="93599-167">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="93599-168">Denne muligheten gir klarhet for avsetningsprosessen for kunder med forskjellige policyer for fraværsår eller permisjonsavsetning.</span><span class="sxs-lookup"><span data-stu-id="93599-168">This ability provides clarity for the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="93599-169">Hvis du vil ha mer informasjon, se [Avsett permisjon per firma eller per permisjonsplan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span><span class="sxs-lookup"><span data-stu-id="93599-169">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="93599-170">Legge til vedlegg i fraværsforespørsler</span><span class="sxs-lookup"><span data-stu-id="93599-170">Add attachments to time-off requests</span></span>

<span data-ttu-id="93599-171">Muligheten til å legge til vedlegg i godkjente permisjonsforespørsler er viktig i det gjeldende COVID-19-miljøet.</span><span class="sxs-lookup"><span data-stu-id="93599-171">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="93599-172">Ansatte kan nå legge til disse vedleggene.</span><span class="sxs-lookup"><span data-stu-id="93599-172">Employees can now add these attachments.</span></span> <span data-ttu-id="93599-173">De har også mer innsikt i hvordan det gjøres oppdateringer for permisjonsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="93599-173">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="93599-174">Hvis du vil ha mer informasjon, kan du se [Legge til et vedlegg i en eksisterende forespørsel](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="93599-174">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="93599-175">Legge til årsakskode for avsetningsuspensjoner</span><span class="sxs-lookup"><span data-stu-id="93599-175">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="93599-176">Årsakskoder er lagt til i avsetningssuspensjonen.</span><span class="sxs-lookup"><span data-stu-id="93599-176">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="93599-177">Overføringsregler</span><span class="sxs-lookup"><span data-stu-id="93599-177">Carry forward rules</span></span> 

<span data-ttu-id="93599-178">Du kan angi en type overføringspermisjon for overføringssaldoer der overføringsjusteringer overføres.</span><span class="sxs-lookup"><span data-stu-id="93599-178">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="93599-179">Hvis en ansatt for eksempel overfører 10 dager, kan du velge en annen permisjonstype for disse 10 dagene.</span><span class="sxs-lookup"><span data-stu-id="93599-179">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="93599-180">Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="93599-180">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="93599-181">Avbryte permisjonsavsetning for angitte permisjonstyper</span><span class="sxs-lookup"><span data-stu-id="93599-181">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="93599-182">Du kan opprette en regel for å utsette permisjonsavsetninger for ansatte med permisjonsforespørsler som er angitt for fravær som ikke betales.</span><span class="sxs-lookup"><span data-stu-id="93599-182">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="93599-183">Fravær som ikke betales, kan være en type, men behøver ikke å være det.</span><span class="sxs-lookup"><span data-stu-id="93599-183">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="93599-184">Du kan stoppe enhver permisjon basert på en annen permisjonstype.</span><span class="sxs-lookup"><span data-stu-id="93599-184">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="93599-185">DMF-enhet tilgjengelig for avsetningssuspensjoner</span><span class="sxs-lookup"><span data-stu-id="93599-185">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="93599-186">En DMF-enhet er nå tilgjengelig for avsetningssuspensjoner.</span><span class="sxs-lookup"><span data-stu-id="93599-186">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="93599-187">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="93599-187">Coming soon</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="93599-188">Sjekklisteenheter inkludert i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="93599-188">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="93599-189">Sjekklisteenheter for pålasting, avlasting, overføringer og forretningsprosesser vil snart være tilgjengelige i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="93599-189">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="93599-190">Se også</span><span class="sxs-lookup"><span data-stu-id="93599-190">See also</span></span>

[<span data-ttu-id="93599-191">Nyheter eller endringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="93599-191">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="93599-192">Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="93599-192">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="93599-193">Oppdatere prosess</span><span class="sxs-lookup"><span data-stu-id="93599-193">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="93599-194">Behandle funksjoner</span><span class="sxs-lookup"><span data-stu-id="93599-194">Manage features</span></span>](hr-admin-manage-features.md)
