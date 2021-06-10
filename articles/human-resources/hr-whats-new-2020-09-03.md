---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (03. september 2020)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 3. september 2020.
author: andreabichsel
ms.date: 09/03/2020
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
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8c8ad853b8d1f8383b23f2ac4341a5f37a904795
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054458"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a><span data-ttu-id="47693-103">Hva er nytt eller endret i Dynamics 365 Human Resources (3. september 2020)</span><span class="sxs-lookup"><span data-stu-id="47693-103">What's new or changed in Dynamics 365 Human Resources (September 3, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="47693-104">Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="47693-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="47693-105">Endringer gjelder for Build-nummeret 8.1.3504.</span><span class="sxs-lookup"><span data-stu-id="47693-105">Changes apply to build number 8.1.3504.</span></span> <span data-ttu-id="47693-106">Tallene i parentes i noen overskrifter refererer til støttenumre i Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="47693-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

<span data-ttu-id="47693-107">Hvis du vil ha mer informasjon om kommende funksjoner i Human Resources, kan du se [Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).</span><span class="sxs-lookup"><span data-stu-id="47693-107">For more information about upcoming features in Human Resources, see [Overview of Dynamics 365 Human Resources 2019 release wave 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).</span></span> <span data-ttu-id="47693-108">Hvis du vil ha mer informasjon om oppdateringsprosessen for Human Resources, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).</span><span class="sxs-lookup"><span data-stu-id="47693-108">For more information about the update process for Human Resources, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="in-this-release"></a><span data-ttu-id="47693-109">I denne versjonen</span><span class="sxs-lookup"><span data-stu-id="47693-109">In this release</span></span>

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a><span data-ttu-id="47693-110">Nytt standard rutenett for finansdimensjoner og dialogmønster i hele Human Resources (469495)</span><span class="sxs-lookup"><span data-stu-id="47693-110">New default financial dimensions grid and dialog pattern throughout Human Resources (469495)</span></span>

<span data-ttu-id="47693-111">Det nye mønsteret for finansdimensjoner er nå tilgjengelig i følgende områder:</span><span class="sxs-lookup"><span data-stu-id="47693-111">The new pattern for financial dimensions is now available in the following areas:</span></span>

- <span data-ttu-id="47693-112">Stillingshandlinger (Skjema: **HcmPositionActionDetail**)</span><span class="sxs-lookup"><span data-stu-id="47693-112">Position actions  (Form: **HcmPositionActionDetail**)</span></span>
- <span data-ttu-id="47693-113">Inntektskoder for lønn (Skjema: **PayrollEarningCode**)</span><span class="sxs-lookup"><span data-stu-id="47693-113">Payroll earning codes  (Form: **PayrollEarningCode**)</span></span>

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a><span data-ttu-id="47693-114">Oppføringer vises ikke i firmaets permisjonskalender hvis forbedringer i permisjons- og fraværskalenderen ikke er aktivert (484406)</span><span class="sxs-lookup"><span data-stu-id="47693-114">Entries don't appear in company leave calendar if Leave and absence calendar enhancements aren't enabled (484406)</span></span>

<span data-ttu-id="47693-115">Denne versjonen retter opp et problem der permisjonsoppføringer ikke vises i firmaets permisjonskalender.</span><span class="sxs-lookup"><span data-stu-id="47693-115">This release corrects an issue where leave entries aren't displayed in the company leave calendar.</span></span> <span data-ttu-id="47693-116">Dette problemet oppstår bare når alternativet **Forbedringer til permisjons- og fraværskalender** ikke er aktivert i Funksjonsbehandling.</span><span class="sxs-lookup"><span data-stu-id="47693-116">This issue only occurs when the Feature management option **Leave and absence calendar enhancements** isn't enabled.</span></span>

### <a name="benefitplanemployeeentity-issue-467597"></a><span data-ttu-id="47693-117">BenefitPlanEmployeeEntity-problem (467597)</span><span class="sxs-lookup"><span data-stu-id="47693-117">BenefitPlanEmployeeEntity issue (467597)</span></span>

<span data-ttu-id="47693-118">Denne versjonen retter opp et problem med enheten **BenefitsPlanEmployee**.</span><span class="sxs-lookup"><span data-stu-id="47693-118">This release corrects an issue with the **BenefitsPlanEmployee** entity.</span></span> <span data-ttu-id="47693-119">Ved import av arbeiderregistreringer angis **Dekningskode** og **Kode for plantype** er nå riktig angitt.</span><span class="sxs-lookup"><span data-stu-id="47693-119">When importing worker enrollments, the **Coverage code** and the **Plan type code** are now set correctly.</span></span> <span data-ttu-id="47693-120">Dette problemet førte til at ansattes fordelsplaner ble vist feil i skjemaene **Fordelsplaner for arbeider** og **Åpen registrering** i Ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="47693-120">This issue caused employee benefit plans to display incorrectly in the **Worker benefits plan** and **Open enrollment** forms in Employee self service.</span></span>

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a><span data-ttu-id="47693-121">Elektronisk filutskrift av 1094-C mangler bokstav i XML (435190)</span><span class="sxs-lookup"><span data-stu-id="47693-121">Electronic file 1094-C output missing letter in XML (435190)</span></span>

<span data-ttu-id="47693-122">Denne endringen retter opp et problem der utdatafilen 1094-C mangler et nødvendig tegn under sending til IRS.</span><span class="sxs-lookup"><span data-stu-id="47693-122">This change corrects an issue with the 1094-C output file missing a character needed when submitting to the IRS.</span></span>

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a><span data-ttu-id="47693-123">Variabel kompensasjonstabell for ansatt tilordnet til skjema for fast kompensasjon (476117)</span><span class="sxs-lookup"><span data-stu-id="47693-123">Employee variable compensation table mapped to fixed compensation form (476117)</span></span>

<span data-ttu-id="47693-124">Denne endringen justerer de faste kompensasjonsfeltene med skjemaet for fast kompensasjon.</span><span class="sxs-lookup"><span data-stu-id="47693-124">This change aligns the fixed compensation fields with the fixed compensation form.</span></span> <span data-ttu-id="47693-125">Feltene for variabel kompensasjon er nå bare tilgjengelige med skjemaet for variabel kompensasjon.</span><span class="sxs-lookup"><span data-stu-id="47693-125">Variable compensation fields are now only available with the variable compensation form.</span></span>

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a><span data-ttu-id="47693-126">Permisjonsforespørsler tillatt før registrering hvis permisjonstypen har en negativ minimumssaldo (469917)</span><span class="sxs-lookup"><span data-stu-id="47693-126">Leave requests allowed before enrollment if that leave type has a negative minimum balance (469917)</span></span>

<span data-ttu-id="47693-127">Denne endringen hindrer at du angir permisjonsforespørsler før de registreres i planen, selv om registreringen har en negativ minimumssaldo.</span><span class="sxs-lookup"><span data-stu-id="47693-127">This change prohibits entering leave requests before being enrolled in the plan, even if the enrollment has a negative minimum balance.</span></span> <span data-ttu-id="47693-128">Du kan bare angi eller sende forespørsler når planen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="47693-128">You can only enter or submit requests when the plan is active.</span></span>

### <a name="document-templates-dont-download-457279"></a><span data-ttu-id="47693-129">Dokumentmaler blir ikke lastet ned (457279)</span><span class="sxs-lookup"><span data-stu-id="47693-129">Document templates don't download (457279)</span></span>

<span data-ttu-id="47693-130">Med denne endringen kan du nå laste ned alle dokumentmaler.</span><span class="sxs-lookup"><span data-stu-id="47693-130">With this change, you can now download all document templates.</span></span> 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a><span data-ttu-id="47693-131">Data vises som kolonneoverskrifter i stedet for rader for feltet Lønnssats i kompensasjonsplanrapporten (476077)</span><span class="sxs-lookup"><span data-stu-id="47693-131">Data displays as column headers instead of rows for the Pay rate field in the compensation plan report (476077)</span></span>

<span data-ttu-id="47693-132">Analyserapporten viser nå den riktige informasjonen for **Lønnssats**.</span><span class="sxs-lookup"><span data-stu-id="47693-132">The analytics report now displays the correct information for **Pay rate**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="47693-133">I forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="47693-133">In preview</span></span>

### <a name="human-resources-application-in-teams"></a><span data-ttu-id="47693-134">Human Resources-søknad i Teams</span><span class="sxs-lookup"><span data-stu-id="47693-134">Human Resources application in Teams</span></span>

<span data-ttu-id="47693-135">Ansatte kan se og be om fravær fra jobb i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="47693-135">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="47693-136">De kan kommunisere med en robot for å opprette permisjonsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="47693-136">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="47693-137">Hvis du vil ha mer informasjon, kan du se:</span><span class="sxs-lookup"><span data-stu-id="47693-137">For more information, see:</span></span>

- <span data-ttu-id="47693-138">[Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) i Dynamics 365-planen for lanseringsbølge 1 i 2020</span><span class="sxs-lookup"><span data-stu-id="47693-138">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="47693-139">[Human Resources-app i Teams](./hr-admin-teams-leave-app.md) i Human Resources-dokumentasjon</span><span class="sxs-lookup"><span data-stu-id="47693-139">[Human Resources app in Teams](./hr-admin-teams-leave-app.md) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="47693-140">Human Resources-app i Teams-evalueringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="47693-140">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="47693-141">**Varslinger**: Innsendere og godkjennere av fritidsforespørsler vil bli varslet i Human Resources-appen i Teams.</span><span class="sxs-lookup"><span data-stu-id="47693-141">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="47693-142">Godkjennere vil kunne godkjenne eller avslå forespørsler om fritid.</span><span class="sxs-lookup"><span data-stu-id="47693-142">Approvers will be able to approve or deny time-off requests.</span></span> <span data-ttu-id="47693-143">Innsendere vil bli varslet hvis forespørselen ble godkjent eller avvist.</span><span class="sxs-lookup"><span data-stu-id="47693-143">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="47693-144">Hvis du vil ha mer informasjon, kan du se:</span><span class="sxs-lookup"><span data-stu-id="47693-144">For more information, see:</span></span>
   - <span data-ttu-id="47693-145">[Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) i Dynamics 365-planen for lanseringsbølge 2 i 2020</span><span class="sxs-lookup"><span data-stu-id="47693-145">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="47693-146">[Aktivere varslinger for Human Resources-appen i Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) i Human Resources-dokumentasjon</span><span class="sxs-lookup"><span data-stu-id="47693-146">[Enable notifications for the Human Resources app in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="47693-147">[Aktivere eller deaktivere Teams-varslinger for enkeltstående brukere](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) i Human Resources-dokumentasjonen</span><span class="sxs-lookup"><span data-stu-id="47693-147">[Turn Teams notifications on or off for individual users](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="47693-148">[Teams-varslinger](./hr-teams-leave-app.md#respond-to-teams-notifications) i Human Resources-dokumentasjonen</span><span class="sxs-lookup"><span data-stu-id="47693-148">[Teams notifications](./hr-teams-leave-app.md#respond-to-teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="47693-149">[Vise permisjonskalenderen for Teams](./hr-teams-leave-app.md#view-your-teams-leave-calendar) i Human Resources-dokumentasjonen</span><span class="sxs-lookup"><span data-stu-id="47693-149">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="47693-150">**Fritidskalender for leder**: Ledere kan se godkjent og ventende fritid for direkte underordnede i en kalendervisning.</span><span class="sxs-lookup"><span data-stu-id="47693-150">**Manager time-off calendar**: Managers will be able to see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="47693-151">Denne visningen gir en enkel forståelse av når teammedlemmene er borte fra arbeid.</span><span class="sxs-lookup"><span data-stu-id="47693-151">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="47693-152">Hvis du vil ha mer informasjon, kan du se:</span><span class="sxs-lookup"><span data-stu-id="47693-152">For more information, see:</span></span>
   - <span data-ttu-id="47693-153">[Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) i Dynamics 365-planen for lanseringsbølge 2 i 2020</span><span class="sxs-lookup"><span data-stu-id="47693-153">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="47693-154">[Vise permisjonskalenderen for Teams](./hr-teams-leave-app.md#view-your-teams-leave-calendar) i Human Resources-dokumentasjonen</span><span class="sxs-lookup"><span data-stu-id="47693-154">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="47693-155">Konfigurasjonsalternativ for å plassere listen Arbeidselementer som er tilordnet til meg (477004)</span><span class="sxs-lookup"><span data-stu-id="47693-155">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="47693-156">Et nytt alternativ er nå tilgjengelig for å plassere listen **Arbeidselementer som er tilordnet til meg** i høyre kolonne på instrumentbordet.</span><span class="sxs-lookup"><span data-stu-id="47693-156">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="47693-157">Med denne endringen vises alle arbeidselementer og gjøremålslister i samme område.</span><span class="sxs-lookup"><span data-stu-id="47693-157">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="47693-158">Aktiver denne funksjonaliteten ved å aktivere **Forhåndsvisning – forbedringer av arbeidsflytsopplevelse** i Funksjonsbehandling.</span><span class="sxs-lookup"><span data-stu-id="47693-158">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="47693-159">Hvis du vil ha mer informasjon om å aktivere forhåndsversjonsfunksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="47693-159">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="47693-160">Denne funksjonen fremmer også arbeidsflytalternativene som vises i personalhandlingsskjemaene.</span><span class="sxs-lookup"><span data-stu-id="47693-160">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="47693-161">Arbeidsflytalternativer vises også over hurtigkategorien for handlingen for rask tilgang.</span><span class="sxs-lookup"><span data-stu-id="47693-161">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="47693-162">Hvis du vil ha mer informasjon, kan du se:</span><span class="sxs-lookup"><span data-stu-id="47693-162">For more information, see:</span></span> 

- <span data-ttu-id="47693-163">[Forbedringer i arbeidsflyten for organisasjons- og personalstyring](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) i Dynamics 365 2020-frigivelsesbølge 2-planen</span><span class="sxs-lookup"><span data-stu-id="47693-163">[Organization and personnel management workflow experience enhancements](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![Arbeidselementer som er tilordnet til meg](./media/hr-workflow-work-items-assigned-to-me.png)

![Hurtigtilgang til arbeidsflytelementer](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a><span data-ttu-id="47693-166">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="47693-166">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="47693-167">Sjekklisteenheter inkludert i Dataverse</span><span class="sxs-lookup"><span data-stu-id="47693-167">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="47693-168">Sjekklisteenheter for pålasting, avlasting, overføringer og forretningsprosesser vil snart være tilgjengelige i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="47693-168">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="47693-169">Årsakskoder for fordelsstyring</span><span class="sxs-lookup"><span data-stu-id="47693-169">Benefits management reason codes</span></span>

<span data-ttu-id="47693-170">Årsakskoder for fordelsstyring kombineres snart med eksisterende årsakskoder i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="47693-170">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="47693-171">Hvis du har opprettet årsakskoder i fordelsstyringen som er over 15 tegn, må du endre navnet på årsakskoden i skjemaet **Årsakskoder** for Fordelsbehandling slik at det består av 15 tegn eller mindre.</span><span class="sxs-lookup"><span data-stu-id="47693-171">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="47693-172">Når du har oppdatert navnet, vises årsakskoden under det eksisterende årsakskodeskjemaet i Personaladministrasjon.</span><span class="sxs-lookup"><span data-stu-id="47693-172">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="47693-173">Denne endringen vil være tilgjengelig i fremtiden, og vil ikke påvirke eksisterende funksjoner.</span><span class="sxs-lookup"><span data-stu-id="47693-173">This change will be available in the future and won't affect existing functionally.</span></span>

## <a name="see-also"></a><span data-ttu-id="47693-174">Se også</span><span class="sxs-lookup"><span data-stu-id="47693-174">See also</span></span>

[<span data-ttu-id="47693-175">Nyheter eller endringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="47693-175">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="47693-176">Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="47693-176">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="47693-177">Oppdatere prosess</span><span class="sxs-lookup"><span data-stu-id="47693-177">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="47693-178">Behandle funksjoner</span><span class="sxs-lookup"><span data-stu-id="47693-178">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
