---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (13. april 2020)?
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 13. april 2020.
author: andreabichsel
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2a43b55c075102056ed7c752b72a85f2c9012d46
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051047"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a><span data-ttu-id="c475e-103">Hva er nytt eller endret i Dynamics 365 Human Resources (13. april 2020)?</span><span class="sxs-lookup"><span data-stu-id="c475e-103">What's new or changed in Dynamics 365 Human Resources (April 13, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c475e-104">Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c475e-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c475e-105">Endringer gjelder for Build-nummeret 8.1.3136.</span><span class="sxs-lookup"><span data-stu-id="c475e-105">Changes apply to build number 8.1.3136.</span></span> <span data-ttu-id="c475e-106">Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.</span><span class="sxs-lookup"><span data-stu-id="c475e-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="c475e-107">Ny produksjonslanseringsfrekvens</span><span class="sxs-lookup"><span data-stu-id="c475e-107">New production release cadence</span></span>

<span data-ttu-id="c475e-108">Med denne ukens lansering vil lanseringsfrekvensen for Human Resources skifte fra en ukentlig oppdatering til en oppdatering annenhver uke.</span><span class="sxs-lookup"><span data-stu-id="c475e-108">With this week's release, the release cadence for Human Resources shifts from a weekly update to a biweekly update.</span></span> <span data-ttu-id="c475e-109">For å sikre innretting etter sikre distribusjonspraksiser og opprettholde høye standarder for stabilitet og pålitelighet i tjenesten, vil prosessen med å distribuere serviceoppdateringer til alle områder er nå en to-ukes distribusjon.</span><span class="sxs-lookup"><span data-stu-id="c475e-109">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions is now a two-week rollout.</span></span> <span data-ttu-id="c475e-110">Flere tester og skjermer er på plass for å bekrefte vellykket distribusjon på hvert trinn i prosessen.</span><span class="sxs-lookup"><span data-stu-id="c475e-110">Additional testing and monitors are in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="c475e-111">Hvis du vil ha mer informasjon om lanseringsfrekvensen, kan du se [Oppdateringsprosess](hr-admin-setup-update-process.md).</span><span class="sxs-lookup"><span data-stu-id="c475e-111">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a><span data-ttu-id="c475e-112">Avrundingspresisjonsfelt kan ikke redigeres når en avrundingstype er angitt (435616)</span><span class="sxs-lookup"><span data-stu-id="c475e-112">Rounding precision field isn't editable after specifying a Rounding type (435616)</span></span>

<span data-ttu-id="c475e-113">Med denne endringen er feltet **Avrundingspresisjon** nå tilgjengelig etter at du har oppdatert feltet **Avrundingstype**.</span><span class="sxs-lookup"><span data-stu-id="c475e-113">With this change, the **Rounding precision** field is now available after you update the **Rounding type** field.</span></span>

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a><span data-ttu-id="c475e-114">Kan ikke redigere sluttdatoen for permisjonsregistrering når permisjonsplanen ikke har avsetningsperioder (413628)</span><span class="sxs-lookup"><span data-stu-id="c475e-114">Can't edit leave enrollment end date when the leave plan doesn't have accrual periods (413628)</span></span>

<span data-ttu-id="c475e-115">Du kan nå redigere sluttdatoen for registrering uten å få feil meldingen "Feltet Datogrunnlag for avsetning må være fylt ut".</span><span class="sxs-lookup"><span data-stu-id="c475e-115">You can now edit the enrollment end date without getting the error "Field Accrual date basis must be filled in."</span></span>

## <a name="employment-entity-doesnt-sync-to-dataverse-430834"></a><span data-ttu-id="c475e-116">Ansettelsesenhet synkroniseres ikke til Dataverse (430834)</span><span class="sxs-lookup"><span data-stu-id="c475e-116">Employment entity doesn't sync to Dataverse (430834)</span></span>

<span data-ttu-id="c475e-117">Denne endringen løser et problem der ansettelsesdataene ikke ble synkronisert til Dataverse etter å ha lagt til finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="c475e-117">This change corrects an issue where the employment data wasn't syncing to Dataverse after adding financial dimensions.</span></span> 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a><span data-ttu-id="c475e-118">Fjern flere overordnede for enheten Tidsintervall for arbeidskalender (431775)</span><span class="sxs-lookup"><span data-stu-id="c475e-118">Remove multi-parenting for Work Calendar Time Interval entity (431775)</span></span>

<span data-ttu-id="c475e-119">Denne endringen fjerner flere overordnede for enheten **Tidsintervall for arbeidskalender**.</span><span class="sxs-lookup"><span data-stu-id="c475e-119">This change removes multi-parenting for the **Work Calendar Time Interval** entity.</span></span>

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a><span data-ttu-id="c475e-120">Filter med CAST-funksjon fungerer ikke på OData-kall til enheten Stillingstilordning (431699)</span><span class="sxs-lookup"><span data-stu-id="c475e-120">Filter with CAST function doesn't work on OData call Position Worker Assignment entity (431699)</span></span>

<span data-ttu-id="c475e-121">Denne oppdateringen inneholder en endring for å tillate filter med CAST-funksjonen i OData for enheten **Stillingstilordning**.</span><span class="sxs-lookup"><span data-stu-id="c475e-121">This update includes a change to allow  filter with CAST function within OData for the **Position Worker Assignment** entity.</span></span>

## <a name="in-preview"></a><span data-ttu-id="c475e-122">I forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="c475e-122">In Preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="c475e-123">Avbryt permisjon</span><span class="sxs-lookup"><span data-stu-id="c475e-123">Leave suspension</span></span>

<span data-ttu-id="c475e-124">Du kan avbryte permisjon og fravær i Human Resources for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="c475e-124">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="c475e-125">Hvis du avbryter permisjon, stoppes permisjonsavsetningene for utvalgte permisjonstyper.</span><span class="sxs-lookup"><span data-stu-id="c475e-125">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="c475e-126">Hvis suspensjonen skjer etter at en avsetning er behandlet, vil avbrudd av permisjon opprette fordelt justering til den ansattes permisjonssaldo.</span><span class="sxs-lookup"><span data-stu-id="c475e-126">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="c475e-127">Hvis du vil ha mer informasjon, kan du se [Avbryt permisjon](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="c475e-127">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="c475e-128">Overføringsregler</span><span class="sxs-lookup"><span data-stu-id="c475e-128">Carry forward rules</span></span>

<span data-ttu-id="c475e-129">Du kan angi en type overføringspermisjon for overføringssaldoer der overføringsjusteringer overføres.</span><span class="sxs-lookup"><span data-stu-id="c475e-129">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="c475e-130">Hvis en ansatt for eksempel overfører 10 dager, kan du velge en annen permisjonstype for disse 10 dagene.</span><span class="sxs-lookup"><span data-stu-id="c475e-130">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="c475e-131">Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="c475e-131">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="c475e-132">Kjente problemer</span><span class="sxs-lookup"><span data-stu-id="c475e-132">Known issues</span></span>

## <a name="employment-details-entity"></a><span data-ttu-id="c475e-133">Enheten Ansettelsesdetaljer</span><span class="sxs-lookup"><span data-stu-id="c475e-133">Employment Details entity</span></span>

<span data-ttu-id="c475e-134">Enheten **Ansettelsesdetalj** er oppdatert med følgende felt:</span><span class="sxs-lookup"><span data-stu-id="c475e-134">The **Employment Detail** entity has been updated with the following fields:</span></span>

- <span data-ttu-id="c475e-135">**Lønnsfrekvens**</span><span class="sxs-lookup"><span data-stu-id="c475e-135">**PayFrequency**</span></span>
- <span data-ttu-id="c475e-136">**ID for ansettelseskategori**</span><span class="sxs-lookup"><span data-stu-id="c475e-136">**Employment Category ID**</span></span>
- <span data-ttu-id="c475e-137">**Ansettelsestype**</span><span class="sxs-lookup"><span data-stu-id="c475e-137">**Employment Type**</span></span>
- <span data-ttu-id="c475e-138">**ID for ansettelsestype**</span><span class="sxs-lookup"><span data-stu-id="c475e-138">**EmploymentType ID**</span></span>
- <span data-ttu-id="c475e-139">**Ansettelsesstatus for fordel**</span><span class="sxs-lookup"><span data-stu-id="c475e-139">**Benefit Employment Status**</span></span>

<span data-ttu-id="c475e-140">Oppsettsdataene for disse feltene er avhengig av fordelsadministrasjonen som aktiveres i arbeidsområdet **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="c475e-140">The setup data for these fields rely on benefits management being enabled in the **Feature management** workspace.</span></span> <span data-ttu-id="c475e-141">Ikke fyll ut eller oppdater disse feltene i enheten **Ansettlesesdetalj** fordi dette vil føre til feil under importen.</span><span class="sxs-lookup"><span data-stu-id="c475e-141">Don't populate or update these fields in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="c475e-142">SharePoint-forhåndsvisning fungerer ikke i enkelte miljøer</span><span class="sxs-lookup"><span data-stu-id="c475e-142">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="c475e-143">Hvis dokumentforhåndsvisning for dokumenter lagret i SharePoint, ikke fungerer, kan du prøve følgende:</span><span class="sxs-lookup"><span data-stu-id="c475e-143">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="c475e-144">Kontroller at brukerkontoen for administratorer har en e-post tilknyttet brukeroppføringen.</span><span class="sxs-lookup"><span data-stu-id="c475e-144">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="c475e-145">Du kan vise denne informasjonen på **Bruker**-siden.</span><span class="sxs-lookup"><span data-stu-id="c475e-145">You can view this information in the **User** page.</span></span> <span data-ttu-id="c475e-146">Hvis e-post ikke er konfigurert, må du legge til e-postmeldingen og leverandøren med Excel-tillegget OData.</span><span class="sxs-lookup"><span data-stu-id="c475e-146">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="c475e-147">Som standard finnes ikke e-postadressen i Excel-utformingen.</span><span class="sxs-lookup"><span data-stu-id="c475e-147">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="c475e-148">Du må redigere Excel-utformingen, legge til alle felt, bruke og oppdatere.</span><span class="sxs-lookup"><span data-stu-id="c475e-148">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="c475e-149">Når du har fullført disse trinnene, kan du oppdatere administratorkontoen.</span><span class="sxs-lookup"><span data-stu-id="c475e-149">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="c475e-150">Når administratorkontoen har en tilknyttet e-postkonto, logger du på Human Resources med administratorlegitimasjon.</span><span class="sxs-lookup"><span data-stu-id="c475e-150">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="c475e-151">Få tilgang til et vedlegg i SharePoint for å starte forhåndsvisning av dokument.</span><span class="sxs-lookup"><span data-stu-id="c475e-151">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="c475e-152">Logg på med en annen brukerkonto som har tilgang til vedlegg, og bekreft at forhåndsvisningen fungerer som forventet.</span><span class="sxs-lookup"><span data-stu-id="c475e-152">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="c475e-153">Se også</span><span class="sxs-lookup"><span data-stu-id="c475e-153">See also</span></span>

[<span data-ttu-id="c475e-154">Nyheter eller endringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="c475e-154">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="c475e-155">Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="c475e-155">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="c475e-156">Oppdatere prosess</span><span class="sxs-lookup"><span data-stu-id="c475e-156">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="c475e-157">Behandle funksjoner</span><span class="sxs-lookup"><span data-stu-id="c475e-157">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]