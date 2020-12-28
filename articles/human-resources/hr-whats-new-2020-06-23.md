---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (25. juni 2020)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 23. juni 2020.
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2020
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
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 28eecb6289e5e895e860cffa29a55e773c6aadaa
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528723"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a><span data-ttu-id="ce370-103">Hva er nytt eller endret i Dynamics 365 Human Resources (23. juni 2020)</span><span class="sxs-lookup"><span data-stu-id="ce370-103">What's new or changed in Dynamics 365 Human Resources (June 23, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ce370-104">Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ce370-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="ce370-105">Endringer gjelder for Build-nummeret 8.1.3347.</span><span class="sxs-lookup"><span data-stu-id="ce370-105">Changes apply to build number 8.1.3347.</span></span> <span data-ttu-id="ce370-106">Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.</span><span class="sxs-lookup"><span data-stu-id="ce370-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a><span data-ttu-id="ce370-107">Når en registrering er utløpt for en avsluttet ansatt, fjernes permisjonstypen, saldoen og beløpet i Permisjonsregistreringsskjemaet (444867)</span><span class="sxs-lookup"><span data-stu-id="ce370-107">When an enrollment is expired for a terminated employee, the leave type, balance, and amount are all cleared in the Leave enrollment form (444867)</span></span>

<span data-ttu-id="ce370-108">Verdier i **Permisjonstype**, **Saldo** og **Beløp** beholdes nå i stedet for å fjernes når du gjør dette valget.</span><span class="sxs-lookup"><span data-stu-id="ce370-108">Values in the **Leave type**, **Balance**, and **Amount** are now maintained instead of cleared upon making this selection.</span></span>

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a><span data-ttu-id="ce370-109">Feil anslått saldo ved ny funksjon (permisjonsavsetning for ett enkelt firma eller én enkelt plan) er aktivert (456553)</span><span class="sxs-lookup"><span data-stu-id="ce370-109">Incorrect forecasted balance when new feature (Leave accrual for a single company or a single plan) is enabled (456553)</span></span>

<span data-ttu-id="ce370-110">Riktig anslått saldo vises nå når permisjonsavsetning for ett enkelt firma eller én enkelt plan er aktivert.</span><span class="sxs-lookup"><span data-stu-id="ce370-110">The correct forecasted balance now displays when the leave accrual for a single company or single plan has been enabled.</span></span>

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a><span data-ttu-id="ce370-111">Enheter med relasjoner som resulterer i dupliserte navigasjonsegenskaper (456486)</span><span class="sxs-lookup"><span data-stu-id="ce370-111">Entities with relations that result in duplicate navigation properties (456486)</span></span>

<span data-ttu-id="ce370-112">Denne versjonen retter opp et problem med navigeringsegenskapene (relasjon) for flere enheter.</span><span class="sxs-lookup"><span data-stu-id="ce370-112">This release corrects an issue with the navigation properties (relation) of multiple entities.</span></span> <span data-ttu-id="ce370-113">Dupliserte relasjoner er oppdaget.</span><span class="sxs-lookup"><span data-stu-id="ce370-113">Duplicate relations are detected.</span></span> <span data-ttu-id="ce370-114">Disse scenariene er rettet opp.</span><span class="sxs-lookup"><span data-stu-id="ce370-114">These scenarios have all been corrected.</span></span>
 
## <a name="cross-company-comments-on-performance-review-455536"></a><span data-ttu-id="ce370-115">Kommentarer på tvers av firmaer på Medarbeidersamtale (455536)</span><span class="sxs-lookup"><span data-stu-id="ce370-115">Cross-company comments on Performance review (455536)</span></span>

<span data-ttu-id="ce370-116">Kommentarer på tvers av firmaer er nå synlig på medarbeidersamtaler med denne reparasjonen.</span><span class="sxs-lookup"><span data-stu-id="ce370-116">Cross-company comments are now visible on performance reviews with this fix.</span></span> <span data-ttu-id="ce370-117">Denne endringen korrigerer visningen av anmelderkommentarer som ble angitt i forskjellige firmaer for samme medarbeidersamtale.</span><span class="sxs-lookup"><span data-stu-id="ce370-117">This change corrects the view of reviewer comments that were entered in different companies for the same performance review.</span></span>
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a><span data-ttu-id="ce370-118">Inkonsekvens i visning av kompensasjonsstyringsdata (432562)</span><span class="sxs-lookup"><span data-stu-id="ce370-118">Inconsistency in showing compensation management data (432562)</span></span>

<span data-ttu-id="ce370-119">Det vedlikeholdes nå en konsekvent visning av kompensasjonsdata i Selvbetjening for ledere.</span><span class="sxs-lookup"><span data-stu-id="ce370-119">A consistent view of compensation data is now maintained in Manager self service.</span></span> <span data-ttu-id="ce370-120">Avhengig av hvordan du navigerer til en arbeiders **Kompensasjonsdetaljer**, viser kompensasjonsdata nå konsekvent for ledere.</span><span class="sxs-lookup"><span data-stu-id="ce370-120">Depending on how you navigate to a worker's **Compensation details**, compensation data now consistently displays to managers.</span></span>
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a><span data-ttu-id="ce370-121">Kompensasjonsplanens gjeldende dato er dagens dato som standard (411994)</span><span class="sxs-lookup"><span data-stu-id="ce370-121">Fixed compensation plan's effective date defaults to today's date (411994)</span></span>

<span data-ttu-id="ce370-122">Startdatoen for kompensasjon er nå basert på startdatoen for stillingen som blir tilordnet den ansatte.</span><span class="sxs-lookup"><span data-stu-id="ce370-122">The compensation start date is now based on the start date of the position being assigned to the employee.</span></span>

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a><span data-ttu-id="ce370-123">Permisjon- og fraværsskjema Aktiver halvdagsdefinisjon deaktiveres når skjemaet åpnes (452607)</span><span class="sxs-lookup"><span data-stu-id="ce370-123">Leave and absence form Enable half day definition is disabled when form opens (452607)</span></span>

<span data-ttu-id="ce370-124">Med denne endringen blir **Aktiver halvdagsdefinisjon** aktivert til det finnes nye permisjonstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="ce370-124">With this change, the **Enable half day definition** will be enabled until new leave transactions exist.</span></span> 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a><span data-ttu-id="ce370-125">Kan ikke publisere til HcmDiscussionEntity via Excel. Feil i TotalRatingScore-felt (453899)</span><span class="sxs-lookup"><span data-stu-id="ce370-125">Unable to publish to HcmDiscussionEntity via Excel; TotalRatingScore field error (453899)</span></span>

<span data-ttu-id="ce370-126">Du kan nå oppdatere **TotalRatingScore**-feltet ved hjelp av **HCMDiscussionEntity** i Excels arbeidsbokutforming.</span><span class="sxs-lookup"><span data-stu-id="ce370-126">You can now update the **TotalRatingScore** field using **HCMDiscussionEntity** in the Excel workbook designer.</span></span>

## <a name="in-preview"></a><span data-ttu-id="ce370-127">I forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="ce370-127">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="ce370-128">Databaselogging</span><span class="sxs-lookup"><span data-stu-id="ce370-128">Database logging</span></span>

<span data-ttu-id="ce370-129">Med databaseloggføring kan du bestemme hvilke tabeller og felt som skal overvåkes.</span><span class="sxs-lookup"><span data-stu-id="ce370-129">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="ce370-130">Du kan også fastslå hvilke hendelser som skal utløse endringssporing.</span><span class="sxs-lookup"><span data-stu-id="ce370-130">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="ce370-131">Du kan bruke funksjonen for databaselogging for å se endringene over tid.</span><span class="sxs-lookup"><span data-stu-id="ce370-131">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="ce370-132">Hvis du vil ha mer informasjon, se [Konfigurere og administrere databaselogging](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="ce370-132">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="ce370-133">Obligatorisk felt</span><span class="sxs-lookup"><span data-stu-id="ce370-133">Mandatory fields</span></span> 

<span data-ttu-id="ce370-134">Du kan nå endre feltene ved hjelp av tilpasningsfunksjonene i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ce370-134">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="ce370-135">Denne funksjonen krever **Lagrede visninger**.</span><span class="sxs-lookup"><span data-stu-id="ce370-135">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="ce370-136">Human Resources-søknad i Teams</span><span class="sxs-lookup"><span data-stu-id="ce370-136">Human Resources application in Teams</span></span>

<span data-ttu-id="ce370-137">Ansatte kan se og be om fravær fra jobb i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="ce370-137">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="ce370-138">De kan kommunisere med en robot for å opprette permisjonsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="ce370-138">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="ce370-139">For mer informasjon, se [Human Resources-app i Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="ce370-139">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="ce370-140">Data Management Framework (DMF)-enheter for Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="ce370-140">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="ce370-141">Enheter for fordelsstyring frigis.</span><span class="sxs-lookup"><span data-stu-id="ce370-141">Benefits management entities are releasing.</span></span> <span data-ttu-id="ce370-142">DMF-enheter gjør det mulig å importere og eksportere data slik at du enkelt kan konfigurere fordelsbehandling.</span><span class="sxs-lookup"><span data-stu-id="ce370-142">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="ce370-143">En mal for fordelsbehandling vil være tilgjengelig for å flytte data.</span><span class="sxs-lookup"><span data-stu-id="ce370-143">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="ce370-144">Malen eksporterer og importerer data på en sekvensiell måte for å respektere dataavhengigheter.</span><span class="sxs-lookup"><span data-stu-id="ce370-144">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="ce370-145">Kjøp og selg permisjon</span><span class="sxs-lookup"><span data-stu-id="ce370-145">Buy and sell leave</span></span> 

<span data-ttu-id="ce370-146">Noen organisasjoner tilbyr en fordel som gjør det mulig for ansatte å kjøpe eller selge permisjon.</span><span class="sxs-lookup"><span data-stu-id="ce370-146">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="ce370-147">Denne prosessen behandles ofte manuelt.</span><span class="sxs-lookup"><span data-stu-id="ce370-147">This process is often managed manually.</span></span> <span data-ttu-id="ce370-148">Denne funksjonen automatiserer behandling av policyer og forespørsler for personalavdelingen.</span><span class="sxs-lookup"><span data-stu-id="ce370-148">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="ce370-149">Den strømlinjeformer permisjonsstyringsprosessen og bidrar til å eliminere feil.</span><span class="sxs-lookup"><span data-stu-id="ce370-149">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="ce370-150">Hvis du vil ha mer informasjon, kan du se:</span><span class="sxs-lookup"><span data-stu-id="ce370-150">For more information, see:</span></span>

- [<span data-ttu-id="ce370-151">Administrere policyer for kjøp og salg av permisjon</span><span class="sxs-lookup"><span data-stu-id="ce370-151">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="ce370-152">Kjøp og selg permisjon</span><span class="sxs-lookup"><span data-stu-id="ce370-152">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="ce370-153">Permisjonsavsetning for ett enkelt firma eller én enkelt plan</span><span class="sxs-lookup"><span data-stu-id="ce370-153">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="ce370-154">Kunder kan behandle avsetninger for ett enkelt firma eller en enkel permisjons- og fraværsplan.</span><span class="sxs-lookup"><span data-stu-id="ce370-154">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="ce370-155">Denne muligheten gir klarhet til avsetningsprosessen for kunder med forskjellige policyer for fraværsår eller permisjonsavsetning.</span><span class="sxs-lookup"><span data-stu-id="ce370-155">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="ce370-156">Hvis du vil ha mer informasjon, se [Avsett permisjon per firma eller per permisjonsplan](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="ce370-156">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="ce370-157">Legge til vedlegg i fraværsforespørsler</span><span class="sxs-lookup"><span data-stu-id="ce370-157">Add attachments to time off requests</span></span>

<span data-ttu-id="ce370-158">Muligheten til å legge til vedlegg i godkjente permisjonsforespørsler er viktig i det gjeldende COVID-19-miljøet.</span><span class="sxs-lookup"><span data-stu-id="ce370-158">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="ce370-159">Ansatte kan nå legge til disse vedleggene.</span><span class="sxs-lookup"><span data-stu-id="ce370-159">Employees can now add these attachments.</span></span> <span data-ttu-id="ce370-160">De har også mer innsikt i hvordan det gjøres oppdateringer for permisjonsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="ce370-160">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="ce370-161">Hvis du vil ha mer informasjon, kan du se [Legge til et vedlegg i en eksisterende forespørsel](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="ce370-161">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="ce370-162">Legge til årsakskode for avsetningsuspensjoner</span><span class="sxs-lookup"><span data-stu-id="ce370-162">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="ce370-163">Årsakskoder er lagt til i avsetningssuspensjonen.</span><span class="sxs-lookup"><span data-stu-id="ce370-163">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="ce370-164">Overføringsregler</span><span class="sxs-lookup"><span data-stu-id="ce370-164">Carry forward rules</span></span> 

<span data-ttu-id="ce370-165">Du kan angi en type overføringspermisjon for overføringssaldoer der overføringsjusteringer overføres.</span><span class="sxs-lookup"><span data-stu-id="ce370-165">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="ce370-166">Hvis en ansatt for eksempel overfører 10 dager, kan du velge en annen permisjonstype for disse 10 dagene.</span><span class="sxs-lookup"><span data-stu-id="ce370-166">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="ce370-167">Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="ce370-167">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="ce370-168">Avbryte permisjonsavsetning for angitte permisjonstyper</span><span class="sxs-lookup"><span data-stu-id="ce370-168">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="ce370-169">Du kan opprette en regel for å utsette permisjonsavsetninger for ansatte med permisjonsforespørsler som er angitt for fravær som ikke betales.</span><span class="sxs-lookup"><span data-stu-id="ce370-169">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="ce370-170">Fravær som ikke betales, kan være en type, men behøver ikke å være det.</span><span class="sxs-lookup"><span data-stu-id="ce370-170">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="ce370-171">Du kan stoppe enhver permisjon basert på en annen permisjonstype.</span><span class="sxs-lookup"><span data-stu-id="ce370-171">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="ce370-172">DMF-enhet tilgjengelig for avsetningssuspensjoner</span><span class="sxs-lookup"><span data-stu-id="ce370-172">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="ce370-173">En DMF-enhet er nå tilgjengelig for avsetningssuspensjoner.</span><span class="sxs-lookup"><span data-stu-id="ce370-173">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="ce370-174">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="ce370-174">Coming soon</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="ce370-175">Konfigurere navnet på ansattselvbetjening</span><span class="sxs-lookup"><span data-stu-id="ce370-175">Configure the name of Employee self-service</span></span>

<span data-ttu-id="ce370-176">Et nytt alternativ vil være tilgjengelig i **Personale-parametere** for å oppdatere navnet på arbeidsområdet Ansattselvbetjening til Selvbetjening.</span><span class="sxs-lookup"><span data-stu-id="ce370-176">A new option will be available in **Human Resources parameters** to update the name of the Employee self service workspace to Self service.</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="ce370-177">Sjekklisteenheter inkludert i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ce370-177">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="ce370-178">Sjekklisteenheter for pålasting, avlasting, overføringer og forretningsprosesser vil snart være tilgjengelige i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ce370-178">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon within Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce370-179">Se også</span><span class="sxs-lookup"><span data-stu-id="ce370-179">See also</span></span>

[<span data-ttu-id="ce370-180">Nyheter eller endringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="ce370-180">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="ce370-181">Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="ce370-181">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="ce370-182">Oppdatere prosess</span><span class="sxs-lookup"><span data-stu-id="ce370-182">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="ce370-183">Behandle funksjoner</span><span class="sxs-lookup"><span data-stu-id="ce370-183">Manage features</span></span>](hr-admin-manage-features.md)