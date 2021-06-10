---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (25. februar 2020)?
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 25. februar 2020.
author: andreabichsel
ms.date: 02/25/2020
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
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d9ff9b524a5812bd309fc33d6aa4ba4a92d687b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051191"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a><span data-ttu-id="af86c-103">Hva er nytt eller endret i Dynamics 365 Human Resources (25. februar 2020)?</span><span class="sxs-lookup"><span data-stu-id="af86c-103">What's new or changed in Dynamics 365 Human Resources (February 25, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="af86c-104">Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="af86c-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="af86c-105">Endringer gjelder for Build-nummeret 8.1.2927.</span><span class="sxs-lookup"><span data-stu-id="af86c-105">Changes apply to build number 8.1.2927.</span></span> <span data-ttu-id="af86c-106">Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.</span><span class="sxs-lookup"><span data-stu-id="af86c-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a><span data-ttu-id="af86c-107">Aktivere Saksbehandling-navigering og enhet for rammeverk for databehandling (DMF) (414754)</span><span class="sxs-lookup"><span data-stu-id="af86c-107">Enable Case Management navigation and data management framework (DMF) entity (414754)</span></span>

<span data-ttu-id="af86c-108">Denne forhåndsvisningsfunksjonen muliggjør ytterligere navigering til saksbehandlingstilfeller.</span><span class="sxs-lookup"><span data-stu-id="af86c-108">This preview feature enables additional navigation to case management cases.</span></span> <span data-ttu-id="af86c-109">Du kan aktivere denne forhåndsvisningsfunksjonen i arbeidsområdet **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="af86c-109">You can enable this preview feature in the **Feature Management** workspace.</span></span> <span data-ttu-id="af86c-110">Disse menypunktene vises i **Samsvar**-arbeidsområdet for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="af86c-110">These menu items appear in the **Compliance** workspace of Dynamics 365 Human Resources.</span></span> <span data-ttu-id="af86c-111">Med denne endringen kan Human Resources ha tilgang til følgende:</span><span class="sxs-lookup"><span data-stu-id="af86c-111">With this change, Human Resources can access:</span></span>

- <span data-ttu-id="af86c-112">Alle saker</span><span class="sxs-lookup"><span data-stu-id="af86c-112">All cases</span></span>
- <span data-ttu-id="af86c-113">Mine saker</span><span class="sxs-lookup"><span data-stu-id="af86c-113">My cases</span></span>
- <span data-ttu-id="af86c-114">Mine åpne tilfeller</span><span class="sxs-lookup"><span data-stu-id="af86c-114">My open cases</span></span>
- <span data-ttu-id="af86c-115">Mine forfalte tilfeller</span><span class="sxs-lookup"><span data-stu-id="af86c-115">My overdue cases</span></span>
- <span data-ttu-id="af86c-116">Saker tilordnet til meg via arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="af86c-116">Cases assigned to me through workflow</span></span>

<span data-ttu-id="af86c-117">Sammen med disse nye visningene i saker kan DMF-enheten **Saksdetalj** også være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="af86c-117">Along with these new views into cases, the **Case detail** DMF entity is also available.</span></span>

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a><span data-ttu-id="af86c-118">Aktivere relasjonsdefinisjoner i den globale adresseboken (414762)</span><span class="sxs-lookup"><span data-stu-id="af86c-118">Enable Relationship definitions in global address bBook (414762)</span></span>

<span data-ttu-id="af86c-119">Relasjoner er nå aktivert i den globale adresseboken.</span><span class="sxs-lookup"><span data-stu-id="af86c-119">Relationships are now enabled in the global address book.</span></span> <span data-ttu-id="af86c-120">Før frigivelsen denne uken, viste **Relasjon**-faktaboksen alle systemdefinerte relasjoner.</span><span class="sxs-lookup"><span data-stu-id="af86c-120">Prior to this week's release, the **Relationship** fact box displayed any system-defined relationships.</span></span> <span data-ttu-id="af86c-121">Nå kan du definere disse relasjonene i den globale adresse bok-siden.</span><span class="sxs-lookup"><span data-stu-id="af86c-121">Now you can define those relationships within the global address book page.</span></span>

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a><span data-ttu-id="af86c-122">En stilling kan fjernes når det finnes aktive kompensasjonsposter for stillingen (414568)</span><span class="sxs-lookup"><span data-stu-id="af86c-122">A position can be removed when active compensation records exist for the position (414568)</span></span>

<span data-ttu-id="af86c-123">Med denne endringen vises det en advarsel når du prøver å slette en stilling, og en arbeider har en aktiv kompensasjonspost for den samme stillingen.</span><span class="sxs-lookup"><span data-stu-id="af86c-123">With this change, a warning appears when you attempt to delete a position and a worker has an active compensation record for that same position.</span></span> <span data-ttu-id="af86c-124">Når dette skjer, må du oppdatere den faste kompensasjonsposten for den ansatte før du fjerner stillingen.</span><span class="sxs-lookup"><span data-stu-id="af86c-124">When this happens, you must update the employee fixed compensation record before removing the position.</span></span>

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a><span data-ttu-id="af86c-125">Medarbeidersamtale-arbeidsflyt legger iblant til godkjenninger fra personer som ikke er en del av prosessen (414171)</span><span class="sxs-lookup"><span data-stu-id="af86c-125">Performance review workflow occasionally adds sign-offs from people who are not part of the process (414171)</span></span>

<span data-ttu-id="af86c-126">Denne endringen løser et problem der flere godkjenningsdeltakere legges til i medarbeidersamtalen.</span><span class="sxs-lookup"><span data-stu-id="af86c-126">This change corrects an issue where additional sign-off participants are added to the performance review.</span></span>

## <a name="worker-position-assignment-not-created-in-dataverse-when-selected-on-the-new-worker-dialog-413479"></a><span data-ttu-id="af86c-127">Tilordninger for arbeiderstilling opprettes ikke i Dataverse når valgt i dialogboksen Ny arbeider (413479)</span><span class="sxs-lookup"><span data-stu-id="af86c-127">Worker position assignment not created in Dataverse when selected on the New Worker dialog (413479)</span></span>

<span data-ttu-id="af86c-128">Denne endringen korrigerer et problem når du ansetter en ny arbeider og tilordner den nyansatte gjennom dialogboksen **Ny arbeider**.</span><span class="sxs-lookup"><span data-stu-id="af86c-128">This change corrects an issue when hiring a new worker and assigning the new hire to a position through the **New worker** dialog.</span></span> <span data-ttu-id="af86c-129">Nå vil stillingstilordningen gjenspeiles i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="af86c-129">Now the position assignment is reflected in Dataverse.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="af86c-130">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="af86c-130">Coming soon</span></span>

### <a name="updated-dataverse-solution"></a><span data-ttu-id="af86c-131">Oppdatert Dataverse-løsning</span><span class="sxs-lookup"><span data-stu-id="af86c-131">Updated Dataverse solution</span></span>

<span data-ttu-id="af86c-132">En ny Dataverse-løsning vil snart være tilgjengelig med følgende endringer:</span><span class="sxs-lookup"><span data-stu-id="af86c-132">A new Dataverse solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="af86c-133">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="af86c-133">Description</span></span> | <span data-ttu-id="af86c-134">Vekslepenger</span><span class="sxs-lookup"><span data-stu-id="af86c-134">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="af86c-135">Endringer i enheten **Jobb/stilling**</span><span class="sxs-lookup"><span data-stu-id="af86c-135">**Job/Position** entity changes</span></span> | <span data-ttu-id="af86c-136">**Kompensasjonsområde** lagt til</span><span class="sxs-lookup"><span data-stu-id="af86c-136">**Compensation region** added</span></span></br><span data-ttu-id="af86c-137">**Finansdimensjoner** lagt til</span><span class="sxs-lookup"><span data-stu-id="af86c-137">**Financial dimensions** added</span></span> |
| <span data-ttu-id="af86c-138">Endringer i **Arbeider**-enheten</span><span class="sxs-lookup"><span data-stu-id="af86c-138">**Worker** entity changes</span></span> | <span data-ttu-id="af86c-139">**Navnerekkefølge** lagt til</span><span class="sxs-lookup"><span data-stu-id="af86c-139">**Name sequence** added</span></span></br><span data-ttu-id="af86c-140">**Arbeider hjemmefra** lagt til</span><span class="sxs-lookup"><span data-stu-id="af86c-140">**Works from home** added</span></span></br><span data-ttu-id="af86c-141">**Språk** lagt til</span><span class="sxs-lookup"><span data-stu-id="af86c-141">**Language** added</span></span></br><span data-ttu-id="af86c-142">**Ansiennitetsdato** lagt til</span><span class="sxs-lookup"><span data-stu-id="af86c-142">**Seniority date** added</span></span></br><span data-ttu-id="af86c-143">**Jubileumsdato** lagt til</span><span class="sxs-lookup"><span data-stu-id="af86c-143">**Anniversary date** added</span></span></br><span data-ttu-id="af86c-144">**Opprinnelig ansettelsesdato** lagt til</span><span class="sxs-lookup"><span data-stu-id="af86c-144">**Original hire date** added</span></span> |
| <span data-ttu-id="af86c-145">Endringer i **Ansettelse**-enheten</span><span class="sxs-lookup"><span data-stu-id="af86c-145">**Employment** entity changes</span></span> | <span data-ttu-id="af86c-146">**Finansdimensjoner** lagt til</span><span class="sxs-lookup"><span data-stu-id="af86c-146">**Financial dimensions** added</span></span></br><span data-ttu-id="af86c-147">**Avslutningsårsak** lagt til</span><span class="sxs-lookup"><span data-stu-id="af86c-147">**Termination reason** added</span></span></br><span data-ttu-id="af86c-148">**Avslutningsdato** endret navn fra **Overgangsdato**</span><span class="sxs-lookup"><span data-stu-id="af86c-148">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="af86c-149">**Prøvedato** lagt til</span><span class="sxs-lookup"><span data-stu-id="af86c-149">**Probation date** added</span></span> |
| <span data-ttu-id="af86c-150">Endringer i **Arbeideradresse**-enheten</span><span class="sxs-lookup"><span data-stu-id="af86c-150">**Worker address** entity changes</span></span> | <span data-ttu-id="af86c-151">**Gateadresse** lagt til</span><span class="sxs-lookup"><span data-stu-id="af86c-151">**Street address** added</span></span></br><span data-ttu-id="af86c-152">**Adresselinje 1**, **Adresselinje 2** og **Adresselinje 3** merket for avskriving</span><span class="sxs-lookup"><span data-stu-id="af86c-152">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="af86c-153">Nye enheter for oppsett av variabel kompensasjon</span><span class="sxs-lookup"><span data-stu-id="af86c-153">New variable compensation setup entities</span></span> | <span data-ttu-id="af86c-154">**Type variabel kompensasjonsplan**</span><span class="sxs-lookup"><span data-stu-id="af86c-154">**Compensation variable plan type**</span></span></br><span data-ttu-id="af86c-155">**Variabel plan for kompensasjon**</span><span class="sxs-lookup"><span data-stu-id="af86c-155">**Compensation variable plan**</span></span></br><span data-ttu-id="af86c-156">**Overdragelsesregler**</span><span class="sxs-lookup"><span data-stu-id="af86c-156">**Vesting rules**</span></span></br><span data-ttu-id="af86c-157">**Nivå for variabel kompensasjonsplan**</span><span class="sxs-lookup"><span data-stu-id="af86c-157">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="af86c-158">Ny enhet, **Ansettelse i arbeiderkalender**</span><span class="sxs-lookup"><span data-stu-id="af86c-158">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="af86c-159">**Arbeidskalenderenhet** lagt til</span><span class="sxs-lookup"><span data-stu-id="af86c-159">**Work calendar entity** added</span></span> |
| <span data-ttu-id="af86c-160">Ny enhet, **Lønnstillingsdetaljer**</span><span class="sxs-lookup"><span data-stu-id="af86c-160">New **Payroll position detail** entity</span></span> | <span data-ttu-id="af86c-161">**Lønnsstillingsdetaljer** lagt til</span><span class="sxs-lookup"><span data-stu-id="af86c-161">**Payroll position detail** added</span></span> |
| <span data-ttu-id="af86c-162">Ny **Tittel**-enhet</span><span class="sxs-lookup"><span data-stu-id="af86c-162">New **Title** entity</span></span> | <span data-ttu-id="af86c-163">**Tittel** lagt til.</span><span class="sxs-lookup"><span data-stu-id="af86c-163">**Title** added.</span></span> <span data-ttu-id="af86c-164">Den nye **Tittel**-enheten blir tatt med i synkroniseringsprosessen mellom Human Resources og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="af86c-164">The new **Title** entity will be included in the sync process between Human Resources and Dataverse.</span></span> <span data-ttu-id="af86c-165">Det blir i utgangspunktet ikke referert fra enhetene **Stilling** eller **Jobb**.</span><span class="sxs-lookup"><span data-stu-id="af86c-165">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

<span data-ttu-id="af86c-166">De neste ukene vil disse enhetsendringene være tilgjengelige i alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="af86c-166">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="af86c-167">Slik installerer du den nyeste Dataverse-løsningen for Human Resources manuelt:</span><span class="sxs-lookup"><span data-stu-id="af86c-167">To manually install the latest Dataverse solution for Human Resources:</span></span>

1.  <span data-ttu-id="af86c-168">Gå til [Power Platform-administrasjonssenteret](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="af86c-168">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="af86c-169">Velg **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="af86c-169">Select **Environments**.</span></span>

3.  <span data-ttu-id="af86c-170">Finn miljøet du vil oppgradere.</span><span class="sxs-lookup"><span data-stu-id="af86c-170">Find the environment you want to upgrade.</span></span> <span data-ttu-id="af86c-171">Miljøet må samsvare med **miljønavn** i **Common Data Service**-informasjonsdelen i **Om**-skjemaet i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="af86c-171">This should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="af86c-172">Velg miljøet for å vise miljødetaljer.</span><span class="sxs-lookup"><span data-stu-id="af86c-172">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="af86c-173">Velg **Administrer løsninger** på handlingslinjen øverst.</span><span class="sxs-lookup"><span data-stu-id="af86c-173">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="af86c-174">Et nytt leservindu åpner og navigerer til **Administrasjonssenter for Dynamics 365** i konteksten til miljøet ditt.</span><span class="sxs-lookup"><span data-stu-id="af86c-174">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="af86c-175">I **Løsning**-listen velger du **Dynamics 365 Human Resources Anker**.</span><span class="sxs-lookup"><span data-stu-id="af86c-175">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="af86c-176">Velg **Oppgrader** hvis du vil bruke den nyeste løsningen.</span><span class="sxs-lookup"><span data-stu-id="af86c-176">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="af86c-177">I forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="af86c-177">In preview</span></span>

<span data-ttu-id="af86c-178">Følgende forhåndsversjonsfunksjoner er tilgjengelige fra 3. februar 2020:</span><span class="sxs-lookup"><span data-stu-id="af86c-178">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="af86c-179">**Forhåndsversjonsfunksjoner for permisjon og fravær** – For mer informasjon, se [Forhåndsversjonsfunksjoner for permisjon og fravær](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span><span class="sxs-lookup"><span data-stu-id="af86c-179">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="af86c-180">**Forhåndsversjonsfunksjonen Fordelsbehandling** – For mer informasjon, inkludert kjente problemer, se [Oversikt over Fordelsbehandling](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="af86c-180">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="af86c-181">Se også</span><span class="sxs-lookup"><span data-stu-id="af86c-181">See also</span></span>

[<span data-ttu-id="af86c-182">Nyheter eller endringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="af86c-182">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="af86c-183">Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="af86c-183">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="af86c-184">Oppdatere prosess</span><span class="sxs-lookup"><span data-stu-id="af86c-184">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="af86c-185">Behandle funksjoner</span><span class="sxs-lookup"><span data-stu-id="af86c-185">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]