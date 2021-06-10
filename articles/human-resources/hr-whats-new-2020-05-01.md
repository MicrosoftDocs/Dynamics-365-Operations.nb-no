---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (1. mai 2020)
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 1. mai 2020.
author: andreabichsel
ms.date: 05/01/2020
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
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e8ceea10b3157fee410e5db6e1d8c9a0366e30e2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6050975"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a><span data-ttu-id="32633-103">Hva er nytt eller endret i Dynamics 365 Human Resources (1. mai 2020)</span><span class="sxs-lookup"><span data-stu-id="32633-103">What's new or changed in Dynamics 365 Human Resources (May 1, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="32633-104">Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="32633-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="32633-105">Endringer gjelder for Build-nummeret 8.1.3196.</span><span class="sxs-lookup"><span data-stu-id="32633-105">Changes apply to build number 8.1.3196.</span></span> <span data-ttu-id="32633-106">Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.</span><span class="sxs-lookup"><span data-stu-id="32633-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a><span data-ttu-id="32633-107">Nye ytelsesstyringsenheter er tilgjengelige i Data Management Framework (DMF)</span><span class="sxs-lookup"><span data-stu-id="32633-107">New Performance Management entities available in Data Management Framework (DMF)</span></span>

<span data-ttu-id="32633-108">Følgende enheter er nå tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="32633-108">The following entities are now available.</span></span> <span data-ttu-id="32633-109">Hvis du ikke ser disse enhetene oppført i enhetslisten, bruker du alternativet **Oppdater enheter** i **Rammeverkparametere > Enhetsinnstillinger > Oppdater enhetsliste**.</span><span class="sxs-lookup"><span data-stu-id="32633-109">If you don't see these entities listed in the entities list, use the **Refresh entities** option in **Framework Parameters > Entity settings > Refresh entity list**.</span></span>

- <span data-ttu-id="32633-110">**Diskusjonskompetanse**</span><span class="sxs-lookup"><span data-stu-id="32633-110">**Discussion Competency**</span></span>
- <span data-ttu-id="32633-111">**Diskusjonsmål**</span><span class="sxs-lookup"><span data-stu-id="32633-111">**Discussion Goals**</span></span>
- <span data-ttu-id="32633-112">**Diskusjonsmål**</span><span class="sxs-lookup"><span data-stu-id="32633-112">**Discussion Measurement**</span></span>
- <span data-ttu-id="32633-113">**Diskusjonsemne**</span><span class="sxs-lookup"><span data-stu-id="32633-113">**Discussion Topic**</span></span>
- <span data-ttu-id="32633-114">**Ytelsesjournal**</span><span class="sxs-lookup"><span data-stu-id="32633-114">**Performance Journal**</span></span>
- <span data-ttu-id="32633-115">**Mål**</span><span class="sxs-lookup"><span data-stu-id="32633-115">**Measurement**</span></span>
- <span data-ttu-id="32633-116">**Mål**</span><span class="sxs-lookup"><span data-stu-id="32633-116">**Goal Measurement**</span></span>

<span data-ttu-id="32633-117">I tillegg ble **totalt resultat** og **gjennomsnittsresultat** lagt til i **Diskusjon**-enheten.</span><span class="sxs-lookup"><span data-stu-id="32633-117">In addition, **Total score** and **Average score** were added to the **Discussion** entity.</span></span>

## <a name="increase-length-of-leave-request-comments-275641"></a><span data-ttu-id="32633-118">Øke lengden på permisjonsforespørselskommentarer (275641)</span><span class="sxs-lookup"><span data-stu-id="32633-118">Increase length of leave request comments (275641)</span></span>

<span data-ttu-id="32633-119">Kommentarer om permisjonsforespørsler tillater nå mer enn 100 tegn.</span><span class="sxs-lookup"><span data-stu-id="32633-119">Comments on leave requests now allow more than 100 characters.</span></span>

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a><span data-ttu-id="32633-120">Endelige kommentarer om gjennomganger vises ikke når lederen eller den ansatte blir logget på et annet firma (431688)</span><span class="sxs-lookup"><span data-stu-id="32633-120">Final comments on reviews don't appear when the manager or employee is signed into a different company (431688)</span></span>

<span data-ttu-id="32633-121">Alle kommentarer vises nå ved visning av gjennomganger.</span><span class="sxs-lookup"><span data-stu-id="32633-121">All comments will now appear when viewing reviews.</span></span>

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a><span data-ttu-id="32633-122">Brukerdefinerte koblinger støttes ikke for skjema for ny arbeider (390374)</span><span class="sxs-lookup"><span data-stu-id="32633-122">User-defined links aren't supported on new Worker form (390374)</span></span>

<span data-ttu-id="32633-123">Brukerdefinerte koblinger er nå aktivert i det strømlinjeformede **Arbeider**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="32633-123">User-defined links are now enabled on the streamlined **Worker** form.</span></span>

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a><span data-ttu-id="32633-124">HcmRatingLevelEntity forårsaker OData-API-krasj (439476)</span><span class="sxs-lookup"><span data-stu-id="32633-124">HcmRatingLevelEntity causes OData API crash (439476)</span></span>

<span data-ttu-id="32633-125">Denne endringen korrigerer API-krasjet.</span><span class="sxs-lookup"><span data-stu-id="32633-125">This change corrects the API crash.</span></span> <span data-ttu-id="32633-126">Det dupliserte navnet forårsaket denne feilen.</span><span class="sxs-lookup"><span data-stu-id="32633-126">A duplicate name cased this error.</span></span>

## <a name="in-preview"></a><span data-ttu-id="32633-127">I forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="32633-127">In preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="32633-128">Avbryt permisjon</span><span class="sxs-lookup"><span data-stu-id="32633-128">Leave suspension</span></span>

<span data-ttu-id="32633-129">Du kan avbryte permisjon og fravær i Human Resources for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="32633-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="32633-130">Hvis du avbryter permisjon, stoppes permisjonsavsetningene for utvalgte permisjonstyper.</span><span class="sxs-lookup"><span data-stu-id="32633-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="32633-131">Hvis suspensjonen skjer etter at en avsetning er behandlet, vil avbrudd av permisjon opprette fordelt justering til den ansattes permisjonssaldo.</span><span class="sxs-lookup"><span data-stu-id="32633-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="32633-132">Hvis du vil ha mer informasjon, kan du se [Avbryt permisjon](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="32633-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="32633-133">Oppdater brukeropplevelsen for å angi at avsetning er deaktivert (429550)</span><span class="sxs-lookup"><span data-stu-id="32633-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="32633-134">Brukeropplevelsen viser nå at avsetningen er utsatt for en plan.</span><span class="sxs-lookup"><span data-stu-id="32633-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a><span data-ttu-id="32633-135">Avbryte permisjonsavsetning for angitte permisjonstyper (272447)</span><span class="sxs-lookup"><span data-stu-id="32633-135">Suspend leave accrual for specified leave types (272447)</span></span>

<span data-ttu-id="32633-136">I denne versjonen kan HR opprette en regel for å utsette permisjonsavsetninger for ansatte med permisjonsforespørsler som er angitt for fravær som ikke betales.</span><span class="sxs-lookup"><span data-stu-id="32633-136">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="32633-137">Fravær som ikke betales, kan være en type, men behøver ikke å være det.</span><span class="sxs-lookup"><span data-stu-id="32633-137">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="32633-138">Du kan stoppe enhver permisjon basert på en annen permisjonstype.</span><span class="sxs-lookup"><span data-stu-id="32633-138">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a><span data-ttu-id="32633-139">DMF-enhet tilgjengelig for avsetningssuspensjoner (429549)</span><span class="sxs-lookup"><span data-stu-id="32633-139">DMF entity available for accrual suspensions (429549)</span></span>

<span data-ttu-id="32633-140">En DMF-enhet er nå tilgjengelig for avsetningssuspensjoner.</span><span class="sxs-lookup"><span data-stu-id="32633-140">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-429547"></a><span data-ttu-id="32633-141">Legg til årsakskode for avsetningsuspensjoner (429547)</span><span class="sxs-lookup"><span data-stu-id="32633-141">Add reason code to accrual suspensions (429547)</span></span>

<span data-ttu-id="32633-142">Årsakskoder er lagt til i avsetningssuspensjonen.</span><span class="sxs-lookup"><span data-stu-id="32633-142">Reason codes have been added to the accrual suspension.</span></span>

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a><span data-ttu-id="32633-143">Begynne overgang fra Personale-parametere til permisjons- og fraværsparametere</span><span class="sxs-lookup"><span data-stu-id="32633-143">Begin transitioning from Human Resources parameters to leave and absence parameters</span></span>

<span data-ttu-id="32633-144">Denne versjonen begynner med å kombinere Personale-parametere med permisjons- og fraværsparametere.</span><span class="sxs-lookup"><span data-stu-id="32633-144">This release starts to combine Human Resources parameters with Leave and absence parameters.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="32633-145">Overføringsregler</span><span class="sxs-lookup"><span data-stu-id="32633-145">Carry forward rules</span></span>

<span data-ttu-id="32633-146">Du kan angi en type overføringspermisjon for overføringssaldoer der overføringsjusteringer overføres.</span><span class="sxs-lookup"><span data-stu-id="32633-146">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="32633-147">Hvis en ansatt for eksempel overfører 10 dager, kan du velge en annen permisjonstype for disse 10 dagene.</span><span class="sxs-lookup"><span data-stu-id="32633-147">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="32633-148">Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="32633-148">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="32633-149">Kjente problemer</span><span class="sxs-lookup"><span data-stu-id="32633-149">Known issues</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="32633-150">SharePoint-forhåndsvisning fungerer ikke i enkelte miljøer</span><span class="sxs-lookup"><span data-stu-id="32633-150">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="32633-151">Hvis dokumentforhåndsvisning for dokumenter lagret i SharePoint, ikke fungerer, kan du prøve følgende:</span><span class="sxs-lookup"><span data-stu-id="32633-151">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="32633-152">Kontroller at brukerkontoen for administratorer har en e-post tilknyttet brukeroppføringen.</span><span class="sxs-lookup"><span data-stu-id="32633-152">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="32633-153">Du kan vise denne informasjonen på **Bruker**-siden.</span><span class="sxs-lookup"><span data-stu-id="32633-153">You can view this information in the **User** page.</span></span> <span data-ttu-id="32633-154">Hvis e-post ikke er konfigurert, må du legge til e-postmeldingen og leverandøren med Excel-tillegget OData.</span><span class="sxs-lookup"><span data-stu-id="32633-154">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="32633-155">Som standard finnes ikke e-postadressen i Excel-utformingen.</span><span class="sxs-lookup"><span data-stu-id="32633-155">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="32633-156">Du må redigere Excel-utformingen, legge til alle felt, bruke og oppdatere.</span><span class="sxs-lookup"><span data-stu-id="32633-156">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="32633-157">Når du har fullført disse trinnene, kan du oppdatere administratorkontoen.</span><span class="sxs-lookup"><span data-stu-id="32633-157">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="32633-158">Når administratorkontoen har en tilknyttet e-postkonto, logger du på Human Resources med administratorlegitimasjon.</span><span class="sxs-lookup"><span data-stu-id="32633-158">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="32633-159">Få tilgang til et vedlegg i SharePoint for å starte forhåndsvisning av dokument.</span><span class="sxs-lookup"><span data-stu-id="32633-159">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="32633-160">Logg på med en annen brukerkonto som har tilgang til vedlegg, og bekreft at forhåndsvisningen fungerer som forventet.</span><span class="sxs-lookup"><span data-stu-id="32633-160">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="32633-161">Se også</span><span class="sxs-lookup"><span data-stu-id="32633-161">See also</span></span>

[<span data-ttu-id="32633-162">Nyheter eller endringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="32633-162">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="32633-163">Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="32633-163">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="32633-164">Oppdatere prosess</span><span class="sxs-lookup"><span data-stu-id="32633-164">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="32633-165">Behandle funksjoner</span><span class="sxs-lookup"><span data-stu-id="32633-165">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]