---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (16. september 2020)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 16. september 2020.
author: jcart1106
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0fe3ac2393e66a00e070d8cb6862c29625d39b53
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057170"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a><span data-ttu-id="0fffd-103">Hva er nytt eller endret i Dynamics 365 Human Resources (16. september 2020)</span><span class="sxs-lookup"><span data-stu-id="0fffd-103">What's new or changed in Dynamics 365 Human Resources (September 16, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0fffd-104">Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0fffd-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0fffd-105">Endringer gjelder for Build-nummeret 8.1.3557.</span><span class="sxs-lookup"><span data-stu-id="0fffd-105">Changes apply to build number 8.1.3557.</span></span> <span data-ttu-id="0fffd-106">Tallene i parentes ved siden av noen funksjoner refererer til støttenumre i Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="0fffd-106">The numbers in parentheses next to some features refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="included-in-this-release"></a><span data-ttu-id="0fffd-107">Inkludert i denne versjonen</span><span class="sxs-lookup"><span data-stu-id="0fffd-107">Included in this release</span></span>

-  [<span data-ttu-id="0fffd-108">Lagrede visninger – generell tilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="0fffd-108">Saved views - general availability</span></span>](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br><span data-ttu-id="0fffd-109">- Hvis du vil ha mer informasjon se [Lagrede visninger](../fin-ops-core/fin-ops/get-started/saved-views.md).</span><span class="sxs-lookup"><span data-stu-id="0fffd-109">- For more information, see [Saved views](../fin-ops-core/fin-ops/get-started/saved-views.md).</span></span> 

- <span data-ttu-id="0fffd-110">Skjemaet **Stillingshandlinger** har et oppdatert dimensjonsrutenett og en ny dialog (469495).</span><span class="sxs-lookup"><span data-stu-id="0fffd-110">The **Position actions** form has an updated dimensions grid and new dialogue (469495).</span></span>

- <span data-ttu-id="0fffd-111">Hvis du setter **Begrens tilgang til arbeiderinformasjon** til Ja i **Avansert tilgang** i **Delte parametere for personaladministrasjon**, viser fordelsskjemaer nå bare de riktige arbeiderne (393384).</span><span class="sxs-lookup"><span data-stu-id="0fffd-111">If you set **Restrict access to worker information** to yes in **Advanced access** in **Human Resources Shared parameters**, benefits forms now show only the appropriate workers (393384).</span></span>

- <span data-ttu-id="0fffd-112">Nye alternativer for kalendergenerering i **WorkCalendar**-enheten (477055):</span><span class="sxs-lookup"><span data-stu-id="0fffd-112">New calendar generation options in the **WorkCalendar** entity (477055):</span></span><br><span data-ttu-id="0fffd-113">- Standard sluttidspunkt</span><span class="sxs-lookup"><span data-stu-id="0fffd-113">- Default ending time</span></span><br><span data-ttu-id="0fffd-114">-    Standard starttidspunkt</span><span class="sxs-lookup"><span data-stu-id="0fffd-114">-    Default starting time</span></span><br><span data-ttu-id="0fffd-115">-  Er fredag arbeidsdag</span><span class="sxs-lookup"><span data-stu-id="0fffd-115">-  Is Friday working day</span></span><br><span data-ttu-id="0fffd-116">-  Er mandag arbeidsdag</span><span class="sxs-lookup"><span data-stu-id="0fffd-116">-  Is Monday working day</span></span><br><span data-ttu-id="0fffd-117">-  Er lørdag arbeidsdag</span><span class="sxs-lookup"><span data-stu-id="0fffd-117">-  Is Saturday working day</span></span><br><span data-ttu-id="0fffd-118">- Er søndag arbeidsdag</span><span class="sxs-lookup"><span data-stu-id="0fffd-118">- Is Sunday working day</span></span><br><span data-ttu-id="0fffd-119">- Er torsdag arbeidsdag</span><span class="sxs-lookup"><span data-stu-id="0fffd-119">- Is Thursday working day</span></span><br><span data-ttu-id="0fffd-120">- Er tirsdag arbeidsdag</span><span class="sxs-lookup"><span data-stu-id="0fffd-120">- Is Tuesday working day</span></span><br><span data-ttu-id="0fffd-121">- Er onsdag arbeidsdag</span><span class="sxs-lookup"><span data-stu-id="0fffd-121">- Is Wednesday working day</span></span><br><span data-ttu-id="0fffd-122">- ID for helligdag i arbeidskalender</span><span class="sxs-lookup"><span data-stu-id="0fffd-122">- Work calendar holiday ID</span></span>

- <span data-ttu-id="0fffd-123">Enheten **LeaveBankTransactionV1** inneholder nå årsakskoden (477823).</span><span class="sxs-lookup"><span data-stu-id="0fffd-123">The **LeaveBankTransactionV1** entity now includes the reason code (477823).</span></span>

- <span data-ttu-id="0fffd-124">Du kan nå lagre oppgaveopptak (492923).</span><span class="sxs-lookup"><span data-stu-id="0fffd-124">You can now save task recordings (492923).</span></span>

- <span data-ttu-id="0fffd-125">Data er nå publisert fra **HCMWorkerContactEntity** (427620).</span><span class="sxs-lookup"><span data-stu-id="0fffd-125">Data is now published successfully from **HCMWorkerContactEntity** (427620).</span></span>

- <span data-ttu-id="0fffd-126">Hurtigfanen **Kompensasjon** vises nå for arbeidertypen oppdragstakeren i skjemaet **Arbeiderhandlinger** (482494).</span><span class="sxs-lookup"><span data-stu-id="0fffd-126">The **Compensation** fast tab now displays for the contractor worker type in the **Worker actions** form (482494).</span></span>

- <span data-ttu-id="0fffd-127">Feltene **Nivå** og **Plan** er nå obligatoriske hvis du angir **Fast kompensasjon**.</span><span class="sxs-lookup"><span data-stu-id="0fffd-127">The **Level** and **Plan** fields are now mandatory if you set **Fixed compensation**.</span></span> <span data-ttu-id="0fffd-128">En feilmelding vises hvis du lar disse feltene stå tomme (482497).</span><span class="sxs-lookup"><span data-stu-id="0fffd-128">An error message displays if you leave these fields blank (482497).</span></span>

- <span data-ttu-id="0fffd-129">Feltet **Plantype** i **Fordeler** er nå en rullegardinliste (488768).</span><span class="sxs-lookup"><span data-stu-id="0fffd-129">The **Plan type** field in **Benefits** is now a dropdown list (488768).</span></span>

- <span data-ttu-id="0fffd-130">Systemadministratorer mottar nå et varsel hvis et egendefinert felt slettes fra Human Resources (481408).</span><span class="sxs-lookup"><span data-stu-id="0fffd-130">System administrators now receive a notification if a custom field is deleted from Human Resources (481408).</span></span>

- <span data-ttu-id="0fffd-131">Under avslutningsprosessen for den ansatte fungerer Human Resources som forventet og endrer ikke det valgte firmaet etter å ha blitt låst (479877).</span><span class="sxs-lookup"><span data-stu-id="0fffd-131">During the terminate employee process, Human Resources behaves as expected and doesn't change the selected company after appearing to lock (479877).</span></span> 

- <span data-ttu-id="0fffd-132">Ledere kan ikke lenger legge til en tallkolonne via egen tilpasning (485317).</span><span class="sxs-lookup"><span data-stu-id="0fffd-132">Managers can no longer add a number column through personalization (485317).</span></span>

- <span data-ttu-id="0fffd-133">Ledere kan ikke lenger fjerne dataområdefilteret fra ID-numre som utløper (485321).</span><span class="sxs-lookup"><span data-stu-id="0fffd-133">Managers can no longer remove the data range filter from identification numbers expiring (485321).</span></span>

- <span data-ttu-id="0fffd-134">Når feltet **Rapporterer til** er tomt, vises stillingsdetaljene fremdeles ved peking over plasseringen (433328).</span><span class="sxs-lookup"><span data-stu-id="0fffd-134">When the **Reports to** field is empty, position details still display when hovering over the position (433328).</span></span>

- <span data-ttu-id="0fffd-135">Ansatte kan nå vise fordelsplaninformasjon i Ansattselvbetjening (481676).</span><span class="sxs-lookup"><span data-stu-id="0fffd-135">Employees can now view benefit plan information in Employee self service (481676).</span></span>

- <span data-ttu-id="0fffd-136">Ansatte kan nå se alle registrerte kurs (429048).</span><span class="sxs-lookup"><span data-stu-id="0fffd-136">Employees can now see all registered courses (429048).</span></span>

- <span data-ttu-id="0fffd-137">Nå kan du begrense visningsalternativene for siden **Profesjonelle sertifikater**.</span><span class="sxs-lookup"><span data-stu-id="0fffd-137">You can now restrict viewing options for the **Professional certificates** page.</span></span> <span data-ttu-id="0fffd-138">Du kan begrense visningsalternativene til den gjeldende juridiske enheten, etter arbeiderstatus og etter arbeidertype (451501).</span><span class="sxs-lookup"><span data-stu-id="0fffd-138">You can restrict viewing options to the current legal entity, by worker status, and by worker type (451501).</span></span> 


## <a name="in-preview"></a><span data-ttu-id="0fffd-139">I forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="0fffd-139">In Preview</span></span>

### <a name="human-resources-app-in-teams"></a><span data-ttu-id="0fffd-140">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="0fffd-140">Human Resources app in Teams</span></span>

<span data-ttu-id="0fffd-141">Ansatte kan se og be om fravær fra jobb i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="0fffd-141">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="0fffd-142">De kan kommunisere med en robot for å opprette permisjonsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="0fffd-142">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="0fffd-143">Hvis du vil ha mer informasjon, kan du se:</span><span class="sxs-lookup"><span data-stu-id="0fffd-143">For more information, see:</span></span>

- <span data-ttu-id="0fffd-144">[Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) i Dynamics 365-planen for lanseringsbølge 1 i 2020</span><span class="sxs-lookup"><span data-stu-id="0fffd-144">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="0fffd-145">[Human Resources-app i Teams](./hr-admin-teams-leave-app.md) i Human Resources-dokumentasjon</span><span class="sxs-lookup"><span data-stu-id="0fffd-145">[Human Resources app in Teams](./hr-admin-teams-leave-app.md) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="0fffd-146">Human Resources-app i Teams-evalueringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="0fffd-146">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="0fffd-147">**Varslinger**: Innsendere og godkjennere av fritidsforespørsler vil bli varslet i Human Resources-appen i Teams.</span><span class="sxs-lookup"><span data-stu-id="0fffd-147">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="0fffd-148">Godkjennere kan godkjenne eller avslå forespørsler om fritid.</span><span class="sxs-lookup"><span data-stu-id="0fffd-148">Approvers can approve or deny time-off requests.</span></span> <span data-ttu-id="0fffd-149">Innsendere vil bli varslet hvis forespørselen ble godkjent eller avvist.</span><span class="sxs-lookup"><span data-stu-id="0fffd-149">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="0fffd-150">Hvis du vil ha mer informasjon, kan du se:</span><span class="sxs-lookup"><span data-stu-id="0fffd-150">For more information, see:</span></span>
   - <span data-ttu-id="0fffd-151">[Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) i Dynamics 365-planen for lanseringsbølge 2 i 2020</span><span class="sxs-lookup"><span data-stu-id="0fffd-151">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="0fffd-152">[Aktivere varslinger for Human Resources-appen i Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) i Human Resources-dokumentasjon</span><span class="sxs-lookup"><span data-stu-id="0fffd-152">[Enable notifications for the Human Resources app in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="0fffd-153">[Aktivere eller deaktivere Teams-varslinger for enkeltstående brukere](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) i Human Resources-dokumentasjonen</span><span class="sxs-lookup"><span data-stu-id="0fffd-153">[Turn Teams notifications on or off for individual users](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="0fffd-154">[Teams-varslinger](./hr-teams-leave-app.md#respond-to-teams-notifications) i Human Resources-dokumentasjonen</span><span class="sxs-lookup"><span data-stu-id="0fffd-154">[Teams notifications](./hr-teams-leave-app.md#respond-to-teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="0fffd-155">[Vise permisjonskalenderen for Teams](./hr-teams-leave-app.md#view-your-teams-leave-calendar) i Human Resources-dokumentasjonen</span><span class="sxs-lookup"><span data-stu-id="0fffd-155">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="0fffd-156">**Fritidskalender for leder**: Ledere kan se godkjent og ventende fritid for direkte underordnede i en kalendervisning.</span><span class="sxs-lookup"><span data-stu-id="0fffd-156">**Manager time-off calendar**: Managers can see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="0fffd-157">Denne visningen gir en enkel forståelse av når teammedlemmene er borte fra arbeid.</span><span class="sxs-lookup"><span data-stu-id="0fffd-157">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="0fffd-158">Hvis du vil ha mer informasjon, kan du se:</span><span class="sxs-lookup"><span data-stu-id="0fffd-158">For more information, see:</span></span>
   - <span data-ttu-id="0fffd-159">[Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) i Dynamics 365-planen for lanseringsbølge 2 i 2020</span><span class="sxs-lookup"><span data-stu-id="0fffd-159">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="0fffd-160">[Vise permisjonskalenderen for Teams](./hr-teams-leave-app.md#view-your-teams-leave-calendar) i Human Resources-dokumentasjonen</span><span class="sxs-lookup"><span data-stu-id="0fffd-160">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="0fffd-161">Konfigurasjonsalternativ for å plassere listen Arbeidselementer som er tilordnet til meg (477004)</span><span class="sxs-lookup"><span data-stu-id="0fffd-161">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="0fffd-162">Et nytt alternativ er nå tilgjengelig for å plassere listen **Arbeidselementer som er tilordnet til meg** i høyre kolonne på instrumentbordet.</span><span class="sxs-lookup"><span data-stu-id="0fffd-162">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="0fffd-163">Med denne endringen vises alle arbeidselementer og gjøremålslister i samme område.</span><span class="sxs-lookup"><span data-stu-id="0fffd-163">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="0fffd-164">Aktiver denne funksjonaliteten ved å aktivere **Forhåndsvisning – forbedringer av arbeidsflytsopplevelse** i Funksjonsbehandling.</span><span class="sxs-lookup"><span data-stu-id="0fffd-164">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="0fffd-165">Hvis du vil ha mer informasjon om å aktivere forhåndsversjonsfunksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="0fffd-165">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="0fffd-166">Denne funksjonen fremmer også arbeidsflytalternativene som vises i personalhandlingsskjemaene.</span><span class="sxs-lookup"><span data-stu-id="0fffd-166">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="0fffd-167">Arbeidsflytalternativer vises også over hurtigkategorien for handlingen for rask tilgang.</span><span class="sxs-lookup"><span data-stu-id="0fffd-167">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="0fffd-168">Hvis du vil ha mer informasjon, kan du se:</span><span class="sxs-lookup"><span data-stu-id="0fffd-168">For more information, see:</span></span> 

- <span data-ttu-id="0fffd-169">[Forbedringer i arbeidsflyten for organisasjons- og personalstyring](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) i Dynamics 365 2020-frigivelsesbølge 2-planen</span><span class="sxs-lookup"><span data-stu-id="0fffd-169">[Organization and personnel management workflow experience enhancements](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![Arbeidselementer som er tilordnet til meg](./media/hr-workflow-work-items-assigned-to-me.png)

![Hurtigtilgang til arbeidsflytelementer](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a><span data-ttu-id="0fffd-172">Kalender for permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="0fffd-172">Leave and absence calendar</span></span>

<span data-ttu-id="0fffd-173">Denne versjonen inneholder flere kalenderalternativer for permisjons- og fraværskalendere.</span><span class="sxs-lookup"><span data-stu-id="0fffd-173">This release includes additional calendar options for leave and absence calendars.</span></span> <span data-ttu-id="0fffd-174">Hvis du vil ha mer informasjon, kan du se [Vise team- og firmakalendere](./hr-employee-self-service-calendar.md).</span><span class="sxs-lookup"><span data-stu-id="0fffd-174">For more information, see [View team and company calendars](./hr-employee-self-service-calendar.md).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="0fffd-175">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="0fffd-175">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="0fffd-176">Sjekklisteenheter inkludert i Dataverse</span><span class="sxs-lookup"><span data-stu-id="0fffd-176">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="0fffd-177">Sjekklisteenheter for pålasting, avlasting, overføringer og forretningsprosesser vil snart være tilgjengelige i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="0fffd-177">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="0fffd-178">Årsakskoder for fordelsstyring</span><span class="sxs-lookup"><span data-stu-id="0fffd-178">Benefits management reason codes</span></span>

<span data-ttu-id="0fffd-179">Årsakskoder for fordelsstyring kombineres snart med eksisterende årsakskoder i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0fffd-179">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="0fffd-180">Hvis du har opprettet årsakskoder i fordelsstyringen som er over 15 tegn, må du endre navnet på årsakskoden i skjemaet **Årsakskoder** for Fordelsbehandling slik at det består av 15 tegn eller mindre.</span><span class="sxs-lookup"><span data-stu-id="0fffd-180">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="0fffd-181">Når du har oppdatert navnet, vises årsakskoden under det eksisterende årsakskodeskjemaet i Personaladministrasjon.</span><span class="sxs-lookup"><span data-stu-id="0fffd-181">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="0fffd-182">Denne endringen vil være tilgjengelig i fremtiden, og vil ikke påvirke eksisterende funksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="0fffd-182">This change will be available in the future and won't affect existing functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="0fffd-183">Se også</span><span class="sxs-lookup"><span data-stu-id="0fffd-183">See also</span></span>

[<span data-ttu-id="0fffd-184">Nyheter eller endringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="0fffd-184">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="0fffd-185">Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="0fffd-185">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="0fffd-186">Oppdatere prosess</span><span class="sxs-lookup"><span data-stu-id="0fffd-186">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="0fffd-187">Behandle funksjoner</span><span class="sxs-lookup"><span data-stu-id="0fffd-187">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
