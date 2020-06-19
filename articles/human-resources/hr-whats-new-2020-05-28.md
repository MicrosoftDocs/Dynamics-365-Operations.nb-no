---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (28. mai 2020)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2020
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c386025843edef83d229a42d3f2314678fadae20
ms.sourcegitcommit: beddfba095c23b3265f0004f5124c4e9dc6404cc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411936"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a><span data-ttu-id="80659-103">Hva er nytt eller endret i Dynamics 365 Human Resources (28. mai 2020)</span><span class="sxs-lookup"><span data-stu-id="80659-103">What's new or changed in Dynamics 365 Human Resources (May 28, 2020)</span></span>

<span data-ttu-id="80659-104">Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="80659-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="80659-105">Endringer gjelder for Build-nummeret 8.1.3287.</span><span class="sxs-lookup"><span data-stu-id="80659-105">Changes apply to build number 8.1.3287.</span></span> <span data-ttu-id="80659-106">Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.</span><span class="sxs-lookup"><span data-stu-id="80659-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a><span data-ttu-id="80659-107">LeaveRequest-enheten fungerer ikke når du aktiverer flere typer per permisjonsplan (447498)</span><span class="sxs-lookup"><span data-stu-id="80659-107">LeaveRequest entity doesn't work when you enable multiple types per leave plan (447498)</span></span>

<span data-ttu-id="80659-108">Med denne endringen er **LeaveEnrollmentV2Entity** nå tilgjengelig for å rette opp feilen som oppstår når du aktiverer flere permisjonstyper.</span><span class="sxs-lookup"><span data-stu-id="80659-108">With this change, the **LeaveEnrollmentV2Entity** is now available to correct the error that occurs when you enable multiple leave types.</span></span>

## <a name="batch-contention-reduction-feature-preview-446619"></a><span data-ttu-id="80659-109">Funksjon for reduksjon av partikonflikt (forhåndsversjon) (446619)</span><span class="sxs-lookup"><span data-stu-id="80659-109">Batch contention reduction feature (preview) (446619)</span></span>

<span data-ttu-id="80659-110">Når du aktiverer denne funksjonen, kan du forvente en reduksjon i blokkering av tabeller for partirammeverk mens du velger oppgaver og ferdigstiller jobber.</span><span class="sxs-lookup"><span data-stu-id="80659-110">When you enable this feature, you can expect a reduction in blocking on batch framework tables while selecting tasks and finishing jobs.</span></span>

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a><span data-ttu-id="80659-111">UpdateConflict ved lagring av arbeider forhindrer redigering av en post i Personer (427915)</span><span class="sxs-lookup"><span data-stu-id="80659-111">UpdateConflict while saving worker prevents editing a record in People (427915)</span></span>

<span data-ttu-id="80659-112">Denne endringen korrigerer en feil når du legger til en ny arbeider, oppdaterer adresseinformasjon og endrer språkpreferansen.</span><span class="sxs-lookup"><span data-stu-id="80659-112">This change corrects an error when adding a new worker, updating address information, and changing language preference.</span></span> <span data-ttu-id="80659-113">I dette unike scenariet ble det vist en feilmelding om at posten ikke kunne oppdateres.</span><span class="sxs-lookup"><span data-stu-id="80659-113">In this unique scenario, an error displayed indicating the record couldn't be updated.</span></span> 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a><span data-ttu-id="80659-114">Kan ikke legge til et vedlegg i en godkjent permisjonsforespørsel for ny innsending (425407)</span><span class="sxs-lookup"><span data-stu-id="80659-114">Unable to add an attachment to an approved leave request to resubmit (425407)</span></span>

<span data-ttu-id="80659-115">Denne endringen tillater nå vedlegg i godkjente permisjonsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="80659-115">This change now allows attachments to approved leave requests.</span></span>

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a><span data-ttu-id="80659-116">Brukeren kan angi kompensasjon for en ansatt i et annet skjema for juridisk enhet (409529)</span><span class="sxs-lookup"><span data-stu-id="80659-116">User can enter compensation for an employee in a different legal entity form (409529)</span></span>

<span data-ttu-id="80659-117">Denne endringen deaktiverer kompensasjonsalternativer for å hindre utilsiktet registrering av kompensasjonsposter for feil juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="80659-117">This change disables compensation options to prevent inadvertent entry of compensation records for the wrong legal entity.</span></span>

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a><span data-ttu-id="80659-118">Feil når du overfører en ansatt, og tilordningsdatoen for arbeiderstillingen kommer før stillingsvarigheten (429402)</span><span class="sxs-lookup"><span data-stu-id="80659-118">Error when you transfer an employee and the Worker position assignment date is before the position duration (429402)</span></span>

<span data-ttu-id="80659-119">Feilmeldinger ved overføring av en ansatt i dette scenariet har blitt oppdatert for å forbedre beskrivelsen av endringene som kreves for å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="80659-119">Error messages when transferring an employee in this scenario have been updated to better describe the changes needed to correct the problem.</span></span>

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a><span data-ttu-id="80659-120">Vedleggsfunksjoner i registrering av selvbetjente fordeler for ansatte</span><span class="sxs-lookup"><span data-stu-id="80659-120">Attachments capabilities in Employee self service benefits enrollment</span></span>
 
<span data-ttu-id="80659-121">Nå kan du legge til vedlegg under prosessen for fordelsregistrering for hver plan som den ansatte registrerer seg i.</span><span class="sxs-lookup"><span data-stu-id="80659-121">Now you can add attachments during the benefits enrollment process for each plan that the employee's enrolling in.</span></span> <span data-ttu-id="80659-122">Du kan deretter vise vedleggene i **Fordeler registrert av arbeider**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="80659-122">You can then view the attachments within the **Worker enrolled benefit** form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="80659-123">I forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="80659-123">In preview</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="80659-124">Human Resources-søknad i Teams</span><span class="sxs-lookup"><span data-stu-id="80659-124">Human Resources application in Teams</span></span>

<span data-ttu-id="80659-125">Ansatte kan se og be om fravær fra jobb i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="80659-125">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="80659-126">De kan kommunisere med en robot for å opprette permisjonsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="80659-126">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="80659-127">For mer informasjon, se [Human Resources-app i Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="80659-127">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="leave-suspension"></a><span data-ttu-id="80659-128">Avbryt permisjon</span><span class="sxs-lookup"><span data-stu-id="80659-128">Leave suspension</span></span>

<span data-ttu-id="80659-129">Du kan avbryte permisjon og fravær i Human Resources for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="80659-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="80659-130">Hvis du avbryter permisjon, stoppes permisjonsavsetningene for utvalgte permisjonstyper.</span><span class="sxs-lookup"><span data-stu-id="80659-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="80659-131">Hvis suspensjonen skjer etter at en avsetning er behandlet, vil avbrudd av permisjon opprette fordelt justering til den ansattes permisjonssaldo.</span><span class="sxs-lookup"><span data-stu-id="80659-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="80659-132">Hvis du vil ha mer informasjon, kan du se [Avbryt permisjon](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="80659-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="80659-133">Oppdater brukeropplevelsen for å angi at avsetning er deaktivert (429550)</span><span class="sxs-lookup"><span data-stu-id="80659-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="80659-134">Brukeropplevelsen viser nå at avsetningen er utsatt for en plan.</span><span class="sxs-lookup"><span data-stu-id="80659-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="80659-135">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="80659-135">Coming soon</span></span>

## <a name="database-logging-in-preview-in-june"></a><span data-ttu-id="80659-136">Database-loggføring (forhåndsversjon i juni)</span><span class="sxs-lookup"><span data-stu-id="80659-136">Database logging (in preview in June)</span></span>

<span data-ttu-id="80659-137">Med funksjonen for databaseloggføring kan du bestemme hvilke tabeller og felt som skal overvåkes.</span><span class="sxs-lookup"><span data-stu-id="80659-137">The database logging feature allows you to determine which table and fields should be monitored.</span></span> <span data-ttu-id="80659-138">Du kan også fastslå hvilke hendelser som skal utløse endringssporing.</span><span class="sxs-lookup"><span data-stu-id="80659-138">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="80659-139">Forespørselsfunksjoner er tilgjengelige for å se disse endringene over tid.</span><span class="sxs-lookup"><span data-stu-id="80659-139">Inquiry capabilities are available to see these changes over time.</span></span>

## <a name="buy-and-sell-leave-in-preview-june-1"></a><span data-ttu-id="80659-140">Kjøp og salg av permisjon (forhåndsversjon 1. juni)</span><span class="sxs-lookup"><span data-stu-id="80659-140">Buy and sell leave (in preview June 1)</span></span>

<span data-ttu-id="80659-141">Noen organisasjoner tilbyr en fordel som gjør det mulig for ansatte å kjøpe eller selge permisjon.</span><span class="sxs-lookup"><span data-stu-id="80659-141">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="80659-142">Denne prosessen behandles ofte manuelt.</span><span class="sxs-lookup"><span data-stu-id="80659-142">This process is often managed manually.</span></span> <span data-ttu-id="80659-143">Denne funksjonen gir en mer automatisert måte å administrere policyer og forespørsler for HR-avdelingen på, og den bidrar til å eliminere feil samtidig som du effektiviserer permisjonsstyringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="80659-143">This feature provides a more automated way to manage policies and requests for the HR department, and it helps eliminate mistakes while streamlining the leave management process.</span></span>

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="80659-144">Data Management Framework (DMF)-enheter for Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="80659-144">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="80659-145">Enheter for fordelsstyring frigis.</span><span class="sxs-lookup"><span data-stu-id="80659-145">Benefits management entities are releasing.</span></span> <span data-ttu-id="80659-146">DMF-enheter gjør det mulig å importere og eksportere data slik at du enkelt kan konfigurere fordelsbehandling.</span><span class="sxs-lookup"><span data-stu-id="80659-146">DMF entities allow importing and exporting data to easily configure benefits management.</span></span> <span data-ttu-id="80659-147">En mal for fordelsbehandling vil også være tilgjengelig for å flytte data.</span><span class="sxs-lookup"><span data-stu-id="80659-147">A Benefits management template will also be available to move data.</span></span> <span data-ttu-id="80659-148">Malen eksporterer og importerer data på en sekvensiell måte for å respektere dataavhengigheter.</span><span class="sxs-lookup"><span data-stu-id="80659-148">The template exports and imports the data in a sequential manner to respect data dependencies.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a><span data-ttu-id="80659-149">Legg til årsakskode for avsetningsuspensjoner (1. juni)</span><span class="sxs-lookup"><span data-stu-id="80659-149">Add reason code to accrual suspensions (June 1)</span></span>

<span data-ttu-id="80659-150">Årsakskoder er lagt til i avsetningssuspensjonen.</span><span class="sxs-lookup"><span data-stu-id="80659-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules-june-1"></a><span data-ttu-id="80659-151">Overføringsregler (1. juni)</span><span class="sxs-lookup"><span data-stu-id="80659-151">Carry forward rules (June 1)</span></span>

<span data-ttu-id="80659-152">Du kan angi en type overføringspermisjon for overføringssaldoer der overføringsjusteringer overføres.</span><span class="sxs-lookup"><span data-stu-id="80659-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="80659-153">Hvis en ansatt for eksempel overfører 10 dager, kan du velge en annen permisjonstype for disse 10 dagene.</span><span class="sxs-lookup"><span data-stu-id="80659-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="80659-154">Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="80659-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a><span data-ttu-id="80659-155">Avbryte permisjonsavsetning for angitte permisjonstyper (1. juni)</span><span class="sxs-lookup"><span data-stu-id="80659-155">Suspend leave accrual for specified leave types (June 1)</span></span>

<span data-ttu-id="80659-156">I denne versjonen kan HR opprette en regel for å utsette permisjonsavsetninger for ansatte med permisjonsforespørsler som er angitt for fravær som ikke betales.</span><span class="sxs-lookup"><span data-stu-id="80659-156">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="80659-157">Fravær som ikke betales, kan være en type, men behøver ikke å være det.</span><span class="sxs-lookup"><span data-stu-id="80659-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="80659-158">Du kan stoppe enhver permisjon basert på en annen permisjonstype.</span><span class="sxs-lookup"><span data-stu-id="80659-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a><span data-ttu-id="80659-159">DMF-enhet tilgjengelig for avsetningssuspensjoner (1. juni)</span><span class="sxs-lookup"><span data-stu-id="80659-159">DMF entity available for accrual suspensions (June 1)</span></span>

<span data-ttu-id="80659-160">En DMF-enhet er nå tilgjengelig for avsetningssuspensjoner.</span><span class="sxs-lookup"><span data-stu-id="80659-160">A DMF entity is now available for accrual suspensions.</span></span>