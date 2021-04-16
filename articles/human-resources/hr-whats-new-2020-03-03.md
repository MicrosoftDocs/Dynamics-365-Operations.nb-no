---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (3. mars 2020)?
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 3. mars 2020.
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 793f47526ef828a281750c34da9d763c94971943
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790458"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-3-2020"></a><span data-ttu-id="97ba3-103">Hva er nytt eller endret i Dynamics 365 Human Resources (3. mars 2020)?</span><span class="sxs-lookup"><span data-stu-id="97ba3-103">What's new or changed in Dynamics 365 Human Resources (March 3, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="97ba3-104">Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="97ba3-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="97ba3-105">Endringer gjelder for Build-nummeret 8.1.2955.</span><span class="sxs-lookup"><span data-stu-id="97ba3-105">Changes apply to build number 8.1.2955.</span></span> <span data-ttu-id="97ba3-106">Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.</span><span class="sxs-lookup"><span data-stu-id="97ba3-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a><span data-ttu-id="97ba3-107">Dataverse-løsningen er nå tilgjengelig med følgende endringer:</span><span class="sxs-lookup"><span data-stu-id="97ba3-107">Dataverse solution is now available with the following changes:</span></span>

<span data-ttu-id="97ba3-108">En ny Dataverse-løsning vil snart være tilgjengelig med følgende endringer:</span><span class="sxs-lookup"><span data-stu-id="97ba3-108">A new Dataverse solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="97ba3-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="97ba3-109">Description</span></span> | <span data-ttu-id="97ba3-110">Vekslepenger</span><span class="sxs-lookup"><span data-stu-id="97ba3-110">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="97ba3-111">Endringer i enheten **Jobb/stilling**</span><span class="sxs-lookup"><span data-stu-id="97ba3-111">**Job/Position** entity changes</span></span> | <span data-ttu-id="97ba3-112">**Kompensasjonsområde** lagt til</span><span class="sxs-lookup"><span data-stu-id="97ba3-112">**Compensation region** added</span></span></br><span data-ttu-id="97ba3-113">**Finansdimensjoner** lagt til</span><span class="sxs-lookup"><span data-stu-id="97ba3-113">**Financial dimensions** added</span></span> |
| <span data-ttu-id="97ba3-114">Endringer i **Arbeider**-enheten</span><span class="sxs-lookup"><span data-stu-id="97ba3-114">**Worker** entity changes</span></span> | <span data-ttu-id="97ba3-115">**Navnerekkefølge** lagt til</span><span class="sxs-lookup"><span data-stu-id="97ba3-115">**Name sequence** added</span></span></br><span data-ttu-id="97ba3-116">**Arbeider hjemmefra** lagt til</span><span class="sxs-lookup"><span data-stu-id="97ba3-116">**Works from home** added</span></span></br><span data-ttu-id="97ba3-117">**Språk** lagt til</span><span class="sxs-lookup"><span data-stu-id="97ba3-117">**Language** added</span></span></br><span data-ttu-id="97ba3-118">**Ansiennitetsdato** lagt til</span><span class="sxs-lookup"><span data-stu-id="97ba3-118">**Seniority date** added</span></span></br><span data-ttu-id="97ba3-119">**Jubileumsdato** lagt til</span><span class="sxs-lookup"><span data-stu-id="97ba3-119">**Anniversary date** added</span></span></br><span data-ttu-id="97ba3-120">**Opprinnelig ansettelsesdato** lagt til</span><span class="sxs-lookup"><span data-stu-id="97ba3-120">**Original hire date** added</span></span> |
| <span data-ttu-id="97ba3-121">Endringer i **Ansettelse**-enheten</span><span class="sxs-lookup"><span data-stu-id="97ba3-121">**Employment** entity changes</span></span> | <span data-ttu-id="97ba3-122">**Finansdimensjoner** lagt til</span><span class="sxs-lookup"><span data-stu-id="97ba3-122">**Financial dimensions** added</span></span></br><span data-ttu-id="97ba3-123">**Avslutningsårsak** lagt til</span><span class="sxs-lookup"><span data-stu-id="97ba3-123">**Termination reason** added</span></span></br><span data-ttu-id="97ba3-124">**Avslutningsdato** endret navn fra **Overgangsdato**</span><span class="sxs-lookup"><span data-stu-id="97ba3-124">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="97ba3-125">**Prøvedato** lagt til</span><span class="sxs-lookup"><span data-stu-id="97ba3-125">**Probation date** added</span></span> |
| <span data-ttu-id="97ba3-126">Endringer i **Arbeideradresse**-enheten</span><span class="sxs-lookup"><span data-stu-id="97ba3-126">**Worker address** entity changes</span></span> | <span data-ttu-id="97ba3-127">**Gateadresse** lagt til</span><span class="sxs-lookup"><span data-stu-id="97ba3-127">**Street address** added</span></span></br><span data-ttu-id="97ba3-128">**Adresselinje 1**, **Adresselinje 2** og **Adresselinje 3** merket for avskriving</span><span class="sxs-lookup"><span data-stu-id="97ba3-128">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="97ba3-129">Nye enheter for oppsett av variabel kompensasjon</span><span class="sxs-lookup"><span data-stu-id="97ba3-129">New variable compensation setup entities</span></span> | <span data-ttu-id="97ba3-130">**Type variabel kompensasjonsplan**</span><span class="sxs-lookup"><span data-stu-id="97ba3-130">**Compensation variable plan type**</span></span></br><span data-ttu-id="97ba3-131">**Variabel plan for kompensasjon**</span><span class="sxs-lookup"><span data-stu-id="97ba3-131">**Compensation variable plan**</span></span></br><span data-ttu-id="97ba3-132">**Overdragelsesregler**</span><span class="sxs-lookup"><span data-stu-id="97ba3-132">**Vesting rules**</span></span></br><span data-ttu-id="97ba3-133">**Nivå for variabel kompensasjonsplan**</span><span class="sxs-lookup"><span data-stu-id="97ba3-133">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="97ba3-134">Ny enhet, **Ansettelse i arbeiderkalender**</span><span class="sxs-lookup"><span data-stu-id="97ba3-134">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="97ba3-135">**Arbeidskalenderenhet** lagt til</span><span class="sxs-lookup"><span data-stu-id="97ba3-135">**Work calendar entity** added</span></span> |
| <span data-ttu-id="97ba3-136">Ny enhet, **Lønnstillingsdetaljer**</span><span class="sxs-lookup"><span data-stu-id="97ba3-136">New **Payroll position detail** entity</span></span> | <span data-ttu-id="97ba3-137">**Lønnsstillingsdetaljer** lagt til</span><span class="sxs-lookup"><span data-stu-id="97ba3-137">**Payroll position detail** added</span></span> |
| <span data-ttu-id="97ba3-138">Ny **Tittel**-enhet</span><span class="sxs-lookup"><span data-stu-id="97ba3-138">New **Title** entity</span></span> | <span data-ttu-id="97ba3-139">**Tittel** lagt til.</span><span class="sxs-lookup"><span data-stu-id="97ba3-139">**Title** added.</span></span> <span data-ttu-id="97ba3-140">Den nye **Tittel**-enheten blir tatt med i synkroniseringsprosessen mellom Human Resources og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="97ba3-140">The new **Title** entity will be included in the sync process between Human Resources and Dataverse.</span></span> <span data-ttu-id="97ba3-141">Det blir i utgangspunktet ikke referert fra enhetene **Stilling** eller **Jobb**.</span><span class="sxs-lookup"><span data-stu-id="97ba3-141">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

<span data-ttu-id="97ba3-142">De neste ukene vil disse enhetsendringene være tilgjengelige i alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="97ba3-142">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="97ba3-143">Slik installerer du den nyeste Dataverse-løsningen for Human Resources manuelt:</span><span class="sxs-lookup"><span data-stu-id="97ba3-143">To manually install the latest Dataverse solution for Human Resources:</span></span>

1.  <span data-ttu-id="97ba3-144">Gå til [Power Platform-administrasjonssenteret](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="97ba3-144">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="97ba3-145">Velg **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="97ba3-145">Select **Environments**.</span></span>

3.  <span data-ttu-id="97ba3-146">Finn miljøet du vil oppgradere.</span><span class="sxs-lookup"><span data-stu-id="97ba3-146">Find the environment you want to upgrade.</span></span> <span data-ttu-id="97ba3-147">Miljøet må samsvare med **miljønavn** i **Common Data Service**-informasjonsdelen i **Om**-skjemaet i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="97ba3-147">The environment should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="97ba3-148">Velg miljøet for å vise miljødetaljer.</span><span class="sxs-lookup"><span data-stu-id="97ba3-148">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="97ba3-149">Velg **Administrer løsninger** på handlingslinjen øverst.</span><span class="sxs-lookup"><span data-stu-id="97ba3-149">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="97ba3-150">Et nytt leservindu åpner og navigerer til **Administrasjonssenter for Dynamics 365** i konteksten til miljøet ditt.</span><span class="sxs-lookup"><span data-stu-id="97ba3-150">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="97ba3-151">I **Løsning**-listen velger du **Dynamics 365 Human Resources Anker**.</span><span class="sxs-lookup"><span data-stu-id="97ba3-151">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="97ba3-152">Velg **Oppgrader** hvis du vil bruke den nyeste løsningen.</span><span class="sxs-lookup"><span data-stu-id="97ba3-152">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="import-issues-with-the-leave-enrollment-data-entity-406082"></a><span data-ttu-id="97ba3-153">Importproblemer med Permisjonsregistrering-dataenheten (406082)</span><span class="sxs-lookup"><span data-stu-id="97ba3-153">Import issues with the Leave enrollment data entity (406082)</span></span>

<span data-ttu-id="97ba3-154">Du kan nå registrere en ansatt i en ny permisjonsplan av samme type, så lenge den nye registreringsdatoen er senere enn den utløpte registreringsdatoen for den tidligere planen.</span><span class="sxs-lookup"><span data-stu-id="97ba3-154">You can now enroll an employee in a new leave plan of the same type, as long as the new enrollment date is later than the expired enrollment date of the previous plan.</span></span>

## <a name="issue-with-exporting-contribution-rates-in-the-401k-payrollworkerenrolledbenefitdetail-entity-in-dmf-420700"></a><span data-ttu-id="97ba3-155">Problem med eksportering av bidragssatser i 401k payrollWorkerEnrolledBenefitDetail-enheten i DMF (420700)</span><span class="sxs-lookup"><span data-stu-id="97ba3-155">Issue with exporting contribution rates in the 401k payrollWorkerEnrolledBenefitDetail entity in DMF (420700)</span></span>

<span data-ttu-id="97ba3-156">Denne endringen korrigerer eksportfunksjonaliteten for **payrollWorkerEnrolledBenefitDetail**-enheten for å gjenspeile de gjeldende verdiene for arbeidsgivers bidrag.</span><span class="sxs-lookup"><span data-stu-id="97ba3-156">This change corrects the export functionality for the **payrollWorkerEnrolledBenefitDetail** entity to reflect the current values for employer contribution.</span></span>

## <a name="searching-in-the-streamlined-worker-form-causes-message-saying-person-field-must-be-filled-in-402525"></a><span data-ttu-id="97ba3-157">Hvis du søker i det strømlinjeformede Arbeider-skjemaet, kan det vises en melding om at Person-feltet fylles ut (402525)</span><span class="sxs-lookup"><span data-stu-id="97ba3-157">Searching in the streamlined Worker form causes message saying Person field must be filled in (402525)</span></span>

<span data-ttu-id="97ba3-158">Når du søker etter en ansatt, vil du ikke lenger få melding om at du må fylle ut **Person**-feltet.</span><span class="sxs-lookup"><span data-stu-id="97ba3-158">When you search for an employee, you'll no longer receive a message saying you must fill in the **Person** field.</span></span>

## <a name="note-field-value-doesnt-render-on-the-add-more-skills-form-380134"></a><span data-ttu-id="97ba3-159">Merknad-feltverdi gjengis ikke i skjemaet Legg til flere kompetanser (380134)</span><span class="sxs-lookup"><span data-stu-id="97ba3-159">Note field value doesn't render on the Add more skills form (380134)</span></span>

<span data-ttu-id="97ba3-160">Denne endringen retter opp et problem når du tilpasser skjemaet **Legg til flere kompetanser** i ansattselvbetjeningen.</span><span class="sxs-lookup"><span data-stu-id="97ba3-160">This change corrects an issue when you personalize the **Add more skills** form in Employee self service.</span></span>

## <a name="multiple-fixed-compensation-plans-dont-expire-when-transferring-employees-389466"></a><span data-ttu-id="97ba3-161">Flere faste kompensasjonsplaner utløper ikke når ansatte overføres (389466)</span><span class="sxs-lookup"><span data-stu-id="97ba3-161">Multiple fixed compensation plans don't expire when transferring employees (389466)</span></span>

<span data-ttu-id="97ba3-162">Med denne endringen vil alle aktive faste kompensasjonsposter for den gamle stillingen utløpe på overgangsdatoen.</span><span class="sxs-lookup"><span data-stu-id="97ba3-162">With this change, all active fixed compensation records for the old position will expire on the transition date.</span></span>

## <a name="in-preview"></a><span data-ttu-id="97ba3-163">I forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="97ba3-163">In preview</span></span>

<span data-ttu-id="97ba3-164">Følgende forhåndsversjonsfunksjoner er tilgjengelige fra 3. februar 2020:</span><span class="sxs-lookup"><span data-stu-id="97ba3-164">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="97ba3-165">**Forhåndsversjonsfunksjoner for permisjon og fravær** – For mer informasjon, se [Forhåndsversjonsfunksjoner for permisjon og fravær](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span><span class="sxs-lookup"><span data-stu-id="97ba3-165">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="97ba3-166">**Forhåndsversjonsfunksjonen Fordelsbehandling** – For mer informasjon, inkludert kjente problemer, se [Oversikt over Fordelsbehandling](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="97ba3-166">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="97ba3-167">Se også</span><span class="sxs-lookup"><span data-stu-id="97ba3-167">See also</span></span>

[<span data-ttu-id="97ba3-168">Nyheter eller endringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="97ba3-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="97ba3-169">Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="97ba3-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="97ba3-170">Oppdatere prosess</span><span class="sxs-lookup"><span data-stu-id="97ba3-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="97ba3-171">Behandle funksjoner</span><span class="sxs-lookup"><span data-stu-id="97ba3-171">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]