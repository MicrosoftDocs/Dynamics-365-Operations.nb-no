---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (11. juni 2020)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 6/16/2020
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
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cba6e48899ec39fc4de6656f8151a42b8aa43261
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555201"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a><span data-ttu-id="f7d06-103">Hva er nytt eller endret i Dynamics 365 Human Resources (11. juni 2020)</span><span class="sxs-lookup"><span data-stu-id="f7d06-103">What's new or changed in Dynamics 365 Human Resources (June 11, 2020)</span></span>

<span data-ttu-id="f7d06-104">Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f7d06-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="f7d06-105">Endringer gjelder for Build-nummeret 8.1.3316.</span><span class="sxs-lookup"><span data-stu-id="f7d06-105">Changes apply to build number 8.1.3316.</span></span> <span data-ttu-id="f7d06-106">Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.</span><span class="sxs-lookup"><span data-stu-id="f7d06-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a><span data-ttu-id="f7d06-107">Strømlinjeformet ansattskjema fører noen ganger til at lukkeknapper for underordnet skjema (X) slutter å fungere (442369)</span><span class="sxs-lookup"><span data-stu-id="f7d06-107">Streamlined employee form sometimes causes child form close (X) buttons to stop working (442369)</span></span>

<span data-ttu-id="f7d06-108">Når skjemaet **Arbeider** ble aktivert, virker ikke lukkeknappen (**X**) av og til for underordnede skjemaer.</span><span class="sxs-lookup"><span data-stu-id="f7d06-108">When the new **Worker** form was enabled, the close (**X**) button occasionally didn't work on child forms.</span></span> <span data-ttu-id="f7d06-109">Dette problemet var forbigående.</span><span class="sxs-lookup"><span data-stu-id="f7d06-109">This problem was intermittent.</span></span> <span data-ttu-id="f7d06-110">Du kan lukke skjemaet etter at du forlater det, og deretter komme tilbake til det.</span><span class="sxs-lookup"><span data-stu-id="f7d06-110">You could close the form after leaving and coming back to it.</span></span> <span data-ttu-id="f7d06-111">Du kan for eksempel velge et menyelement til venstre og gå tilbake til **Arbeider**-skjemaet og deretter lukke det.</span><span class="sxs-lookup"><span data-stu-id="f7d06-111">For example, you could select a menu item on the left, and navigate back to the **Worker** form, and then close it.</span></span> <span data-ttu-id="f7d06-112">Denne ukens versjon retter opp dette problemet.</span><span class="sxs-lookup"><span data-stu-id="f7d06-112">This week's release fixes this problem.</span></span> 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a><span data-ttu-id="f7d06-113">Enheten Arbeiderens personlige kontaktperson eksporterer ikke personlige kontakter med en overordnet relasjonstype</span><span class="sxs-lookup"><span data-stu-id="f7d06-113">The Worker personal contact person entity doesn't export personal contacts with a parent relationship type</span></span>

<span data-ttu-id="f7d06-114">Med denne versjonen eksporterer **Arbeiderens personlige kontaktperson** alle relasjonstyper.</span><span class="sxs-lookup"><span data-stu-id="f7d06-114">With this release, the **Worker personal contact person** entity exports all relationship types.</span></span>

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a><span data-ttu-id="f7d06-115">HcmPositionWorkerAssignmentV2Entity skal være en del av Ceridian-lønnsintegrasjonspakken som standard (448506)</span><span class="sxs-lookup"><span data-stu-id="f7d06-115">The HcmPositionWorkerAssignmentV2Entity should be part of the Ceridian payroll integration package by default (448506)</span></span>

<span data-ttu-id="f7d06-116">Med denne endringen er **HcmPositionWorkerAssignmentV2Entity** inkludert i Ceridian-lønnsintegrasjonspakken.</span><span class="sxs-lookup"><span data-stu-id="f7d06-116">With this change, the **HcmPositionWorkerAssignmentV2Entity** is included in the Ceridian payroll integration package.</span></span>

## <a name="in-preview"></a><span data-ttu-id="f7d06-117">I forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="f7d06-117">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="f7d06-118">Databaselogging</span><span class="sxs-lookup"><span data-stu-id="f7d06-118">Database logging</span></span>

<span data-ttu-id="f7d06-119">Med funksjonen for databaseloggføring kan du bestemme hvilke tabeller og felt som skal overvåkes.</span><span class="sxs-lookup"><span data-stu-id="f7d06-119">The database logging feature allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="f7d06-120">Du kan også fastslå hvilke hendelser som skal utløse endringssporing.</span><span class="sxs-lookup"><span data-stu-id="f7d06-120">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="f7d06-121">Du kan bruke funksjonen for databaselogging for å se endringene over tid.</span><span class="sxs-lookup"><span data-stu-id="f7d06-121">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="f7d06-122">Hvis du vil ha mer informasjon, se [Konfigurere og administrere databaselogging](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="f7d06-122">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="f7d06-123">Human Resources-søknad i Teams</span><span class="sxs-lookup"><span data-stu-id="f7d06-123">Human Resources application in Teams</span></span>

<span data-ttu-id="f7d06-124">Ansatte kan se og be om fravær fra jobb i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="f7d06-124">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="f7d06-125">De kan kommunisere med en robot for å opprette permisjonsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="f7d06-125">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="f7d06-126">For mer informasjon, se [Human Resources-app i Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="f7d06-126">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="f7d06-127">Data Management Framework (DMF)-enheter for Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="f7d06-127">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="f7d06-128">Enheter for fordelsstyring frigis.</span><span class="sxs-lookup"><span data-stu-id="f7d06-128">Benefits management entities are releasing.</span></span> <span data-ttu-id="f7d06-129">DMF-enheter gjør det mulig å importere og eksportere data slik at du enkelt kan konfigurere fordelsbehandling.</span><span class="sxs-lookup"><span data-stu-id="f7d06-129">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="f7d06-130">En mal for fordelsbehandling vil være tilgjengelig for å flytte data.</span><span class="sxs-lookup"><span data-stu-id="f7d06-130">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="f7d06-131">Malen eksporterer og importerer data på en sekvensiell måte for å respektere dataavhengigheter.</span><span class="sxs-lookup"><span data-stu-id="f7d06-131">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="f7d06-132">Kjøp og selg permisjon</span><span class="sxs-lookup"><span data-stu-id="f7d06-132">Buy and sell leave</span></span> 

<span data-ttu-id="f7d06-133">Noen organisasjoner tilbyr en fordel som gjør det mulig for ansatte å kjøpe eller selge permisjon.</span><span class="sxs-lookup"><span data-stu-id="f7d06-133">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="f7d06-134">Denne prosessen behandles ofte manuelt.</span><span class="sxs-lookup"><span data-stu-id="f7d06-134">This process is often managed manually.</span></span> <span data-ttu-id="f7d06-135">Denne funksjonen automatiserer behandling av policyer og forespørsler for personalavdelingen.</span><span class="sxs-lookup"><span data-stu-id="f7d06-135">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="f7d06-136">Den strømlinjeformer permisjonsstyringsprosessen og bidrar til å eliminere feil.</span><span class="sxs-lookup"><span data-stu-id="f7d06-136">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="f7d06-137">Hvis du vil ha mer informasjon, kan du se:</span><span class="sxs-lookup"><span data-stu-id="f7d06-137">For more information, see:</span></span>

- [<span data-ttu-id="f7d06-138">Administrere policyer for kjøp og salg av permisjon</span><span class="sxs-lookup"><span data-stu-id="f7d06-138">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="f7d06-139">Kjøp og selg permisjon</span><span class="sxs-lookup"><span data-stu-id="f7d06-139">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="f7d06-140">Permisjonsavsetning for ett enkelt firma eller én enkelt plan</span><span class="sxs-lookup"><span data-stu-id="f7d06-140">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="f7d06-141">Kunder kan behandle avsetninger for ett enkelt firma eller en enkel permisjons- og fraværsplan.</span><span class="sxs-lookup"><span data-stu-id="f7d06-141">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="f7d06-142">Denne muligheten gir klarhet til avsetningsprosessen for kunder med forskjellige policyer for fraværsår eller permisjonsavsetning.</span><span class="sxs-lookup"><span data-stu-id="f7d06-142">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="f7d06-143">Hvis du vil ha mer informasjon, se [Avsett permisjon per firma eller per permisjonsplan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span><span class="sxs-lookup"><span data-stu-id="f7d06-143">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="f7d06-144">Legge til vedlegg i fraværsforespørsler</span><span class="sxs-lookup"><span data-stu-id="f7d06-144">Add attachments to time off requests</span></span>

<span data-ttu-id="f7d06-145">Muligheten til å legge til vedlegg i godkjente permisjonsforespørsler er viktig i det gjeldende COVID-19-miljøet.</span><span class="sxs-lookup"><span data-stu-id="f7d06-145">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="f7d06-146">Ansatte kan nå legge til disse vedleggene.</span><span class="sxs-lookup"><span data-stu-id="f7d06-146">Employees can now add these attachments.</span></span> <span data-ttu-id="f7d06-147">De har også mer innsikt i hvordan det gjøres oppdateringer for permisjonsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="f7d06-147">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="f7d06-148">Hvis du vil ha mer informasjon, kan du se [Legge til et vedlegg i en eksisterende forespørsel](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="f7d06-148">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="f7d06-149">Legge til årsakskode for avsetningsuspensjoner</span><span class="sxs-lookup"><span data-stu-id="f7d06-149">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="f7d06-150">Årsakskoder er lagt til i avsetningssuspensjonen.</span><span class="sxs-lookup"><span data-stu-id="f7d06-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="f7d06-151">Overføringsregler</span><span class="sxs-lookup"><span data-stu-id="f7d06-151">Carry forward rules</span></span> 

<span data-ttu-id="f7d06-152">Du kan angi en type overføringspermisjon for overføringssaldoer der overføringsjusteringer overføres.</span><span class="sxs-lookup"><span data-stu-id="f7d06-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="f7d06-153">Hvis en ansatt for eksempel overfører 10 dager, kan du velge en annen permisjonstype for disse 10 dagene.</span><span class="sxs-lookup"><span data-stu-id="f7d06-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="f7d06-154">Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="f7d06-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="f7d06-155">Avbryte permisjonsavsetning for angitte permisjonstyper</span><span class="sxs-lookup"><span data-stu-id="f7d06-155">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="f7d06-156">Du kan opprette en regel for å utsette permisjonsavsetninger for ansatte med permisjonsforespørsler som er angitt for fravær som ikke betales.</span><span class="sxs-lookup"><span data-stu-id="f7d06-156">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="f7d06-157">Fravær som ikke betales, kan være en type, men behøver ikke å være det.</span><span class="sxs-lookup"><span data-stu-id="f7d06-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="f7d06-158">Du kan stoppe enhver permisjon basert på en annen permisjonstype.</span><span class="sxs-lookup"><span data-stu-id="f7d06-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="f7d06-159">DMF-enhet tilgjengelig for avsetningssuspensjoner</span><span class="sxs-lookup"><span data-stu-id="f7d06-159">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="f7d06-160">En DMF-enhet er nå tilgjengelig for avsetningssuspensjoner.</span><span class="sxs-lookup"><span data-stu-id="f7d06-160">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="f7d06-161">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="f7d06-161">Coming soon</span></span>

## <a name="new-platform-capabilities"></a><span data-ttu-id="f7d06-162">Nye plattformegenskaper</span><span class="sxs-lookup"><span data-stu-id="f7d06-162">New platform capabilities</span></span> 

<span data-ttu-id="f7d06-163">Du kan gjøre felt obligatoriske ved hjelp av personalisering.</span><span class="sxs-lookup"><span data-stu-id="f7d06-163">You'll be able to make fields mandatory by using personalization.</span></span> <span data-ttu-id="f7d06-164">Denne funksjonen vil kreve at du aktiverer **Lagrede visninger**.</span><span class="sxs-lookup"><span data-stu-id="f7d06-164">This feature will require you to enable **Saved views**.</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="f7d06-165">Konfigurere navnet på ansattselvbetjening</span><span class="sxs-lookup"><span data-stu-id="f7d06-165">Configure the name of Employee self-service</span></span>

<span data-ttu-id="f7d06-166">Et nytt alternativ vil være tilgjengelig i Personale-parametere for å oppdatere navnet på arbeidsområdet Ansattselvbetjening til Selvbetjening.</span><span class="sxs-lookup"><span data-stu-id="f7d06-166">A new option will be available in Human Resources parameters to update the name of the Employee self service workspace to Self service.</span></span> 

## <a name="see-also"></a><span data-ttu-id="f7d06-167">Se også</span><span class="sxs-lookup"><span data-stu-id="f7d06-167">See also</span></span>

[<span data-ttu-id="f7d06-168">Nyheter eller endringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="f7d06-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="f7d06-169">Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="f7d06-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="f7d06-170">Oppdatere prosess</span><span class="sxs-lookup"><span data-stu-id="f7d06-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="f7d06-171">Behandle funksjoner</span><span class="sxs-lookup"><span data-stu-id="f7d06-171">Manage features</span></span>](hr-admin-manage-features.md)