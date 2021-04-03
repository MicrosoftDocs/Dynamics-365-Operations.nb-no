---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (14. mai 2020)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 14. mai 2020.
author: andreabichsel
manager: tfehr
ms.date: 05/14/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f1ef15bec1d2eb7b7aaca3a413e13089b36315fd
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465300"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a><span data-ttu-id="64d00-103">Hva er nytt eller endret i Dynamics 365 Human Resources (14. mai 2020)</span><span class="sxs-lookup"><span data-stu-id="64d00-103">What's new or changed in Dynamics 365 Human Resources (May 14, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="64d00-104">Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="64d00-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="64d00-105">Endringer gjelder for Build-nummeret 8.1.3244.</span><span class="sxs-lookup"><span data-stu-id="64d00-105">Changes apply to build number 8.1.3244.</span></span> <span data-ttu-id="64d00-106">Tallene i parentes i noen overskrifter refererer til støttenumre i Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="64d00-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="64d00-107">Plattformendringer</span><span class="sxs-lookup"><span data-stu-id="64d00-107">Platform changes</span></span>

<span data-ttu-id="64d00-108">Plattformendringer er inkludert i denne ukens frigivelse.</span><span class="sxs-lookup"><span data-stu-id="64d00-108">Platform changes are included in this week's release.</span></span> <span data-ttu-id="64d00-109">Hvis du vil ha mer informasjon, kan du se [Platformoppdateringer for versjon 10.0.10 av Finance and Operations-apper (mai 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34).</span><span class="sxs-lookup"><span data-stu-id="64d00-109">For more information, see [Platform updates for version 10.0.10 of Finance and Operations apps (May 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34).</span></span> <span data-ttu-id="64d00-110">Denne versjonen inneholder feilrettinger og endringer i lagrede visninger.</span><span class="sxs-lookup"><span data-stu-id="64d00-110">This release includes bug fixes and changes to saved views.</span></span>
 
## <a name="ensure-dataverse-picklists-are-consistent-with-leave-enums-436343"></a><span data-ttu-id="64d00-111">Sørg for at plukklister i Dataverse er konsekvente med permisjonsopplistinger (436343)</span><span class="sxs-lookup"><span data-stu-id="64d00-111">Ensure Dataverse picklists are consistent with Leave enums (436343)</span></span>

<span data-ttu-id="64d00-112">Plukklister i Dataverse er konsekvente med permisjonsopplistinger.</span><span class="sxs-lookup"><span data-stu-id="64d00-112">Dataverse picklists are now consistent with Leave enums.</span></span>

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a><span data-ttu-id="64d00-113">Tillat brukere å konfigurere en arbeidsflyt for permisjonsforespørsel basert på forespørselsbeløpet (300044)</span><span class="sxs-lookup"><span data-stu-id="64d00-113">Allow users to configure leave request workflow based on the request amount (300044)</span></span>

<span data-ttu-id="64d00-114">Brukere kan konfigurere arbeidsflyter for permisjonsforespørsel basert på forespørselsbeløp.</span><span class="sxs-lookup"><span data-stu-id="64d00-114">Users can configure leave requests workflows based on request amounts.</span></span>
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a><span data-ttu-id="64d00-115">Nytt arbeiderskjema viser data på Vis-menyen når avansert sikkerhet er aktivert (403185)</span><span class="sxs-lookup"><span data-stu-id="64d00-115">New worker form exposes data through the View menu when advanced security is enabled (403185)</span></span>

<span data-ttu-id="64d00-116">Denne versjonen korrigerer hvordan visning av arbeidere på tvers av juridiske enheter fungerer når avansert tilgang er aktivert, og arbeidere i andre firmaer er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="64d00-116">This release corrects how viewing workers across legal entities functions when advanced access is enabled and workers in other companies are accessible.</span></span>

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a><span data-ttu-id="64d00-117">Tillat at det kjøres permisjonsavsetninger for én plan eller ett firma (318844)</span><span class="sxs-lookup"><span data-stu-id="64d00-117">Allow running leave accruals for a single plan or a single company (318844)</span></span>

<span data-ttu-id="64d00-118">Med denne endringen kan du kjøre avsetninger for et firma eller en plan.</span><span class="sxs-lookup"><span data-stu-id="64d00-118">With this change, you can run accruals for a company or a plan.</span></span>
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a><span data-ttu-id="64d00-119">Vis stillingens heltidsekvivalent (FTE) i skjemaet Registrerte arbeidere (414658)</span><span class="sxs-lookup"><span data-stu-id="64d00-119">Show the position's full-time equivalent (FTE) in the Enrolled workers form (414658)</span></span>

<span data-ttu-id="64d00-120">FTE-verdien fra stillingen til en arbeider bestemmer en ansatts avsetningssats når FTE-alternativet er aktivert for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="64d00-120">The FTE value from a worker's position determines a worker's accrual rate when the FTE option is enabled on the leave type.</span></span> <span data-ttu-id="64d00-121">Dette feltet er nå inkludert i skjemaet **Registrerte arbeidere** og dialogboksen **Masseregistrering**.</span><span class="sxs-lookup"><span data-stu-id="64d00-121">This field is now included in **Enrolled workers** form and the **Mass enrollment** dialog.</span></span>

## <a name="add-leave-balance-expiration-batch-job-431266"></a><span data-ttu-id="64d00-122">Legg til den satsvise jobben for utestående beløp (431266)</span><span class="sxs-lookup"><span data-stu-id="64d00-122">Add leave balance expiration batch job (431266)</span></span>

<span data-ttu-id="64d00-123">En ny satsvis jobb er nå tilgjengelig som kjører daglig.</span><span class="sxs-lookup"><span data-stu-id="64d00-123">A new batch job is now available that runs daily.</span></span> <span data-ttu-id="64d00-124">Det reduserer saldoen for gjenværende permisjon når utløpsdatoer blir gjeldende.</span><span class="sxs-lookup"><span data-stu-id="64d00-124">It decreases the remaining leave balance when expiration dates become current.</span></span>

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a><span data-ttu-id="64d00-125">Eksport av personlige kontaktpersoner for en ansatt ved hjelp av arbeiderens personlige kontaktperson, eksporterer ikke personlige kontakter med den overordnede relasjonstypen (345893)</span><span class="sxs-lookup"><span data-stu-id="64d00-125">Exporting personal contacts for an employee using the Worker personal contact person entity doesn't export personal contacts with the Parent relationship type (345893)</span></span>

<span data-ttu-id="64d00-126">Dataenheten **Arbeiderens personlige kontaktperson** (**HcmPersonalContactPersonEntity** i DMF og **PersonalContactPerson** i OData) kan ikke eksportere personlige kontakter som har relasjonstypen **Overordnet**.</span><span class="sxs-lookup"><span data-stu-id="64d00-126">The **Worker personal contact person** data entity (**HcmPersonalContactPersonEntity** in DMF and **PersonalContactPerson** in OData) couldn't export personal contacts that have a relationship type of **Parent**.</span></span> <span data-ttu-id="64d00-127">Dette problemet er løst for personlige kontakter som er opprettet etter denne endringen.</span><span class="sxs-lookup"><span data-stu-id="64d00-127">This issue is fixed for personal contacts that are created after this change.</span></span> <span data-ttu-id="64d00-128">Eksisterende personlige kontakter av typen **Overordnet** vil bli løst i en senere versjon.</span><span class="sxs-lookup"><span data-stu-id="64d00-128">Existing personal contacts of type **Parent** will be fixed in a later release.</span></span>

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a><span data-ttu-id="64d00-129">Årsakskoder vises på tvers av ulike scenarioer når de merkes som permisjon og fravær, og det strømlinjeformede ansattskjemaet er aktivert (434163)</span><span class="sxs-lookup"><span data-stu-id="64d00-129">Reason codes display across different scenarios when they're marked as Leave and absence and the streamlined employee form is enabled (434163)</span></span>

<span data-ttu-id="64d00-130">Denne endringen begrenser årsakskodene til bare permisjons- og fraværskoder når du aktiverer strømlinjeformet ansattoppføring.</span><span class="sxs-lookup"><span data-stu-id="64d00-130">This change restricts the reason codes to only Leave and absence codes when you enable streamlined employee entry.</span></span>

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a><span data-ttu-id="64d00-131">Forhåndsvisningsfunksjonen Tilordne en permisjon til ansatte i fremtiden viser feil (433555)</span><span class="sxs-lookup"><span data-stu-id="64d00-131">The preview feature Assign a leave plan to employees in the future displays error (433555)</span></span>

<span data-ttu-id="64d00-132">Denne endringen korrigerer en feil når en permisjonsplan har to permisjonstyper tilordnet, og du prøver å tilordne en ansatt.</span><span class="sxs-lookup"><span data-stu-id="64d00-132">This change corrects an error when a leave plan has two leave types assigned and you attempt to assign an employee.</span></span>

## <a name="getting-started-banner-appears-for-all-users-441731"></a><span data-ttu-id="64d00-133">Banneret Komme i gang vises for alle brukere (441731)</span><span class="sxs-lookup"><span data-stu-id="64d00-133">Getting started banner appears for all users (441731)</span></span>

<span data-ttu-id="64d00-134">Med denne endringen er banneret Komme i gang skjult for brukere som ikke er systemadministratorer eller databehandlingsadministratorer.</span><span class="sxs-lookup"><span data-stu-id="64d00-134">With this change, the Getting started banner is hidden for users that aren't System administrators or Data management administrators.</span></span> 

## <a name="the-dataverse-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a><span data-ttu-id="64d00-135">Enheten Adresse for Dataverse-arbeider fungerer annerledes når det gjelder datoer som er gyldige i Human Resources (425071)</span><span class="sxs-lookup"><span data-stu-id="64d00-135">The Dataverse Worker Address entity works differently in terms of date time effective dates in Human Resources (425071)</span></span>

<span data-ttu-id="64d00-136">Denne endringen holder adresseinformasjon justert i bestemte scenarioer, basert på datoene til adressen.</span><span class="sxs-lookup"><span data-stu-id="64d00-136">This change keeps address information aligned in certain scenarios, based on the dates of the address.</span></span>

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a><span data-ttu-id="64d00-137">Kan ikke legge til et vedlegg i en godkjent permisjonsforespørsel (425407)</span><span class="sxs-lookup"><span data-stu-id="64d00-137">Unable to add an attachment to an approved leave request (425407)</span></span>

<span data-ttu-id="64d00-138">Med denne ukes frigivelse kan du legge til vedlegg i godkjente permisjonsforespørsler uten å endre permisjonsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="64d00-138">With this week's release, you can add attachments to approved leave requests without changing the leave request.</span></span>

## <a name="in-preview"></a><span data-ttu-id="64d00-139">I forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="64d00-139">In preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="64d00-140">Avbryt permisjon</span><span class="sxs-lookup"><span data-stu-id="64d00-140">Leave suspension</span></span>

<span data-ttu-id="64d00-141">Du kan avbryte permisjon og fravær i Human Resources for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="64d00-141">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="64d00-142">Hvis du avbryter permisjon, stoppes permisjonsavsetningene for utvalgte permisjonstyper.</span><span class="sxs-lookup"><span data-stu-id="64d00-142">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="64d00-143">Hvis suspensjonen skjer etter at en avsetning er behandlet, vil avbrudd av permisjon opprette fordelt justering til den ansattes permisjonssaldo.</span><span class="sxs-lookup"><span data-stu-id="64d00-143">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="64d00-144">Hvis du vil ha mer informasjon, kan du se [Avbryt permisjon](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="64d00-144">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="64d00-145">Oppdater brukeropplevelsen for å angi at avsetning er deaktivert (429550)</span><span class="sxs-lookup"><span data-stu-id="64d00-145">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="64d00-146">Brukeropplevelsen viser nå at avsetningen er utsatt for en plan.</span><span class="sxs-lookup"><span data-stu-id="64d00-146">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a><span data-ttu-id="64d00-147">Avbryte permisjonsavsetning for angitte permisjonstyper (272447)</span><span class="sxs-lookup"><span data-stu-id="64d00-147">Suspend leave accrual for specified leave types (272447)</span></span>

<span data-ttu-id="64d00-148">I denne versjonen kan HR opprette en regel for å utsette permisjonsavsetninger for ansatte med permisjonsforespørsler som er angitt for fravær som ikke betales.</span><span class="sxs-lookup"><span data-stu-id="64d00-148">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="64d00-149">Fravær som ikke betales, kan være en type, men behøver ikke å være det.</span><span class="sxs-lookup"><span data-stu-id="64d00-149">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="64d00-150">Du kan stoppe enhver permisjon basert på en annen permisjonstype.</span><span class="sxs-lookup"><span data-stu-id="64d00-150">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a><span data-ttu-id="64d00-151">DMF-enhet tilgjengelig for avsetningssuspensjoner (429549)</span><span class="sxs-lookup"><span data-stu-id="64d00-151">DMF entity available for accrual suspensions (429549)</span></span>

<span data-ttu-id="64d00-152">En DMF-enhet er nå tilgjengelig for avsetningssuspensjoner.</span><span class="sxs-lookup"><span data-stu-id="64d00-152">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-429547"></a><span data-ttu-id="64d00-153">Legg til årsakskode for avsetningsuspensjoner (429547)</span><span class="sxs-lookup"><span data-stu-id="64d00-153">Add reason code to accrual suspensions (429547)</span></span>

<span data-ttu-id="64d00-154">Årsakskoder er lagt til i avsetningssuspensjonen.</span><span class="sxs-lookup"><span data-stu-id="64d00-154">Reason codes have been added to the accrual suspension.</span></span>

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a><span data-ttu-id="64d00-155">Begynne overgang fra Personale-parametere til permisjons- og fraværsparametere</span><span class="sxs-lookup"><span data-stu-id="64d00-155">Begin transitioning from Human Resources parameters to leave and absence parameters</span></span>

<span data-ttu-id="64d00-156">Denne versjonen begynner med å kombinere Personale-parametere med permisjons- og fraværsparametere.</span><span class="sxs-lookup"><span data-stu-id="64d00-156">This release starts to combine Human Resources parameters with Leave and absence parameters.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="64d00-157">Overføringsregler</span><span class="sxs-lookup"><span data-stu-id="64d00-157">Carry forward rules</span></span>

<span data-ttu-id="64d00-158">Du kan angi en type overføringspermisjon for overføringssaldoer der overføringsjusteringer overføres.</span><span class="sxs-lookup"><span data-stu-id="64d00-158">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="64d00-159">Hvis en ansatt for eksempel overfører 10 dager, kan du velge en annen permisjonstype for disse 10 dagene.</span><span class="sxs-lookup"><span data-stu-id="64d00-159">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="64d00-160">Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="64d00-160">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="64d00-161">Se også</span><span class="sxs-lookup"><span data-stu-id="64d00-161">See also</span></span>

[<span data-ttu-id="64d00-162">Nyheter eller endringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="64d00-162">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="64d00-163">Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="64d00-163">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="64d00-164">Oppdatere prosess</span><span class="sxs-lookup"><span data-stu-id="64d00-164">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="64d00-165">Behandle funksjoner</span><span class="sxs-lookup"><span data-stu-id="64d00-165">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]