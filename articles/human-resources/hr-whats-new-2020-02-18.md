---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (18. februar 2020)?
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 18. februar 2020.
author: andreabichsel
ms.date: 02/18/2020
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
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6c28d0dc76195cc0aedc132f348a229af0421c43
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790434"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a><span data-ttu-id="5770d-103">Hva er nytt eller endret i Dynamics 365 Human Resources (18. februar 2020)?</span><span class="sxs-lookup"><span data-stu-id="5770d-103">What's new or changed in Dynamics 365 Human Resources (February 18, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5770d-104">Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5770d-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="5770d-105">Endringer gjelder for Build-nummeret 8.1.2903.</span><span class="sxs-lookup"><span data-stu-id="5770d-105">Changes apply to build number 8.1.2903.</span></span> <span data-ttu-id="5770d-106">Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.</span><span class="sxs-lookup"><span data-stu-id="5770d-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="5770d-107">Plattform update 32</span><span class="sxs-lookup"><span data-stu-id="5770d-107">Platform update 32</span></span> 

<span data-ttu-id="5770d-108">Platform Update 32 er nå tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="5770d-108">Platform update 32 is now available.</span></span> <span data-ttu-id="5770d-109">Hvis du vil ha mer informasjon, se [Hva er nytt eller endret i Platform Update 32 for Finance and Operations (februar 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span><span class="sxs-lookup"><span data-stu-id="5770d-109">For more information, see [What's new or changed in Platform update 32 for Finance and Operations (February 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span></span>

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a><span data-ttu-id="5770d-110">Søkeverdier huskes ved endring av visningsalternativer i strømlinjeformet ansatt-skjemaet (383833)</span><span class="sxs-lookup"><span data-stu-id="5770d-110">Search values are remembered when changing view options in streamlined employee form (383833)</span></span>

<span data-ttu-id="5770d-111">Det nye **Arbeider**-skjemaet husker nå søkeverdier når du endrer visningsalternativene og bruker endringer.</span><span class="sxs-lookup"><span data-stu-id="5770d-111">The new **Worker** form now remembers  search values when you change the view options and apply changes.</span></span>

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a><span data-ttu-id="5770d-112">Sammendragsfliser for kompensasjonsstyring i forhåndsvisningsfunksjonen omadresser til feil format (401861)</span><span class="sxs-lookup"><span data-stu-id="5770d-112">Compensation management summary tiles in preview feature redirect to wrong form (401861)</span></span>

<span data-ttu-id="5770d-113">Faste og variable kompensasjonsstyringsfliser viser nå de riktige postene i det nye **Arbeider**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="5770d-113">Fixed and variable compensation management tiles now display the correct records in the new **Worker** form.</span></span> <span data-ttu-id="5770d-114">Gjelder bare den forhåndsvisningsfunksjonen for strømlinjeformede ansatte.</span><span class="sxs-lookup"><span data-stu-id="5770d-114">Applies only to the streamlined employee form preview feature.</span></span> <span data-ttu-id="5770d-115">Du kan aktivere denne forhåndsvisningsfunksjonen **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="5770d-115">You can enable this preview feature in **Feature management**.</span></span> <span data-ttu-id="5770d-116">Hvis du vil ha mer informasjon, kan du se [Behandle funksjoner](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="5770d-116">For more information, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="empty-status-field-for-some-leave-request-records-in-dataverse-414915"></a><span data-ttu-id="5770d-117">Tomt Status-felt for enkelte oen permisjonsforespørselsposter i Dataverse (414915)</span><span class="sxs-lookup"><span data-stu-id="5770d-117">Empty Status field for some leave request records in Dataverse (414915)</span></span>

<span data-ttu-id="5770d-118">Denne endringen løser et problem i Dataverse når **Status**-feltet i en permisjonsforespørsel er angitt til **Gjennomgang**.</span><span class="sxs-lookup"><span data-stu-id="5770d-118">This change corrects an issue in Dataverse when the **Status** field in a leave request is set to **Review**.</span></span> <span data-ttu-id="5770d-119">Dataverse gjenspeiler nå statusen.</span><span class="sxs-lookup"><span data-stu-id="5770d-119">Dataverse now reflects the status.</span></span>

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a><span data-ttu-id="5770d-120">Kompetansegapanalyse er bare mulig for tilordnet jobb (411390)</span><span class="sxs-lookup"><span data-stu-id="5770d-120">Skill gap analysis only possible for assigned job (411390)</span></span>

<span data-ttu-id="5770d-121">Du kan nå foreta en kompetansegapanalyse på en hvilken som helst jobb som er definert i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5770d-121">You can now do a skill gap analysis on any job defined in Human Resources.</span></span>

## <a name="system-currency-doesnt-sync-from-dataverse-to-human-resources-in-new-environments-418011"></a><span data-ttu-id="5770d-122">Systemvaluta synkroniseres ikke fra Dataverse til Human Resources i nye miljøer (418011)</span><span class="sxs-lookup"><span data-stu-id="5770d-122">System currency doesn't sync from Dataverse to Human Resources in new environments (418011)</span></span>

<span data-ttu-id="5770d-123">Systemvalutaen i Dataverse kan nå synkroniseres til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5770d-123">The system currency in Dataverse can now sync to Human Resources.</span></span>

## <a name="in-preview"></a><span data-ttu-id="5770d-124">I forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="5770d-124">In preview</span></span>

- [<span data-ttu-id="5770d-125">Forhåndsversjonsfunksjoner for permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="5770d-125">Leave and absence preview features</span></span>](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [<span data-ttu-id="5770d-126">Forhåndsvisningsfunksjoner for ordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="5770d-126">Benefits management preview features</span></span>](hr-benefits-management-overview.md)

## <a name="coming-soon"></a><span data-ttu-id="5770d-127">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="5770d-127">Coming soon</span></span>

### <a name="updated-dataverse-solution"></a><span data-ttu-id="5770d-128">Oppdatert Dataverse-løsning</span><span class="sxs-lookup"><span data-stu-id="5770d-128">Updated Dataverse solution</span></span>

<span data-ttu-id="5770d-129">En ny Dataverse-løsning vil snart være tilgjengelig med følgende endringer:</span><span class="sxs-lookup"><span data-stu-id="5770d-129">A new Dataverse solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="5770d-130">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5770d-130">Description</span></span> | <span data-ttu-id="5770d-131">Vekslepenger</span><span class="sxs-lookup"><span data-stu-id="5770d-131">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="5770d-132">Endringer i enheten **Jobb/stilling**</span><span class="sxs-lookup"><span data-stu-id="5770d-132">**Job/Position** entity changes</span></span> | <span data-ttu-id="5770d-133">**Kompensasjonsområde** lagt til</span><span class="sxs-lookup"><span data-stu-id="5770d-133">**Compensation region** added</span></span></br><span data-ttu-id="5770d-134">**Finansdimensjoner** lagt til</span><span class="sxs-lookup"><span data-stu-id="5770d-134">**Financial dimensions** added</span></span> |
| <span data-ttu-id="5770d-135">Endringer i **Arbeider**-enheten</span><span class="sxs-lookup"><span data-stu-id="5770d-135">**Worker** entity changes</span></span> | <span data-ttu-id="5770d-136">**Navnerekkefølge** lagt til</span><span class="sxs-lookup"><span data-stu-id="5770d-136">**Name sequence** added</span></span></br><span data-ttu-id="5770d-137">**Arbeider hjemmefra** lagt til</span><span class="sxs-lookup"><span data-stu-id="5770d-137">**Works from home** added</span></span></br><span data-ttu-id="5770d-138">**Språk** lagt til</span><span class="sxs-lookup"><span data-stu-id="5770d-138">**Language** added</span></span></br><span data-ttu-id="5770d-139">**Ansiennitetsdato** lagt til</span><span class="sxs-lookup"><span data-stu-id="5770d-139">**Seniority date** added</span></span></br><span data-ttu-id="5770d-140">**Jubileumsdato** lagt til</span><span class="sxs-lookup"><span data-stu-id="5770d-140">**Anniversary date** added</span></span></br><span data-ttu-id="5770d-141">**Opprinnelig ansettelsesdato** lagt til</span><span class="sxs-lookup"><span data-stu-id="5770d-141">**Original hire date** added</span></span> |
| <span data-ttu-id="5770d-142">Endringer i **Ansettelse**-enheten</span><span class="sxs-lookup"><span data-stu-id="5770d-142">**Employment** entity changes</span></span> | <span data-ttu-id="5770d-143">**Finansdimensjoner** lagt til</span><span class="sxs-lookup"><span data-stu-id="5770d-143">**Financial dimensions** added</span></span></br><span data-ttu-id="5770d-144">**Avslutningsårsak** lagt til</span><span class="sxs-lookup"><span data-stu-id="5770d-144">**Termination reason** added</span></span></br><span data-ttu-id="5770d-145">**Avslutningsdato** endret navn fra **Overgangsdato**</span><span class="sxs-lookup"><span data-stu-id="5770d-145">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="5770d-146">**Prøvedato** lagt til</span><span class="sxs-lookup"><span data-stu-id="5770d-146">**Probation date** added</span></span> |
| <span data-ttu-id="5770d-147">Endringer i **Arbeideradresse**-enheten</span><span class="sxs-lookup"><span data-stu-id="5770d-147">**Worker address** entity changes</span></span> | <span data-ttu-id="5770d-148">**Gateadresse** lagt til</span><span class="sxs-lookup"><span data-stu-id="5770d-148">**Street address** added</span></span></br><span data-ttu-id="5770d-149">**Adresselinje 1**, **Adresselinje 2** og **Adresselinje 3** merket for avskriving</span><span class="sxs-lookup"><span data-stu-id="5770d-149">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="5770d-150">Nye enheter for oppsett av variabel kompensasjon</span><span class="sxs-lookup"><span data-stu-id="5770d-150">New variable compensation setup entities</span></span> | <span data-ttu-id="5770d-151">**Type variabel kompensasjonsplan**</span><span class="sxs-lookup"><span data-stu-id="5770d-151">**Compensation variable plan type**</span></span></br><span data-ttu-id="5770d-152">**Variabel plan for kompensasjon**</span><span class="sxs-lookup"><span data-stu-id="5770d-152">**Compensation variable plan**</span></span></br><span data-ttu-id="5770d-153">**Overdragelsesregler**</span><span class="sxs-lookup"><span data-stu-id="5770d-153">**Vesting rules**</span></span></br><span data-ttu-id="5770d-154">**Nivå for variabel kompensasjonsplan**</span><span class="sxs-lookup"><span data-stu-id="5770d-154">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="5770d-155">Ny enhet, **Ansettelse i arbeiderkalender**</span><span class="sxs-lookup"><span data-stu-id="5770d-155">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="5770d-156">**Arbeidskalenderenhet** lagt til</span><span class="sxs-lookup"><span data-stu-id="5770d-156">**Work calendar entity** added</span></span> |
| <span data-ttu-id="5770d-157">Ny enhet, **Lønnstillingsdetaljer**</span><span class="sxs-lookup"><span data-stu-id="5770d-157">New **Payroll position detail** entity</span></span> | <span data-ttu-id="5770d-158">**Lønnsstillingsdetaljer** lagt til</span><span class="sxs-lookup"><span data-stu-id="5770d-158">**Payroll position detail** added</span></span> |
| <span data-ttu-id="5770d-159">Ny **Tittel**-enhet</span><span class="sxs-lookup"><span data-stu-id="5770d-159">New **Title** entity</span></span> | <span data-ttu-id="5770d-160">**Tittel** lagt til.</span><span class="sxs-lookup"><span data-stu-id="5770d-160">**Title** added.</span></span> <span data-ttu-id="5770d-161">Den nye **Tittel**-enheten blir tatt med i synkroniseringsprosessen mellom Human Resources og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5770d-161">The new **Title** entity will be included in the sync process between Human Resources and Dataverse.</span></span> <span data-ttu-id="5770d-162">Det blir i utgangspunktet ikke referert fra enhetene **Stilling** eller **Jobb**.</span><span class="sxs-lookup"><span data-stu-id="5770d-162">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

## <a name="see-also"></a><span data-ttu-id="5770d-163">Se også</span><span class="sxs-lookup"><span data-stu-id="5770d-163">See also</span></span>

[<span data-ttu-id="5770d-164">Nyheter eller endringer i Personale?</span><span class="sxs-lookup"><span data-stu-id="5770d-164">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="5770d-165">Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="5770d-165">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="5770d-166">Oppdatere prosess</span><span class="sxs-lookup"><span data-stu-id="5770d-166">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="5770d-167">Behandle funksjoner</span><span class="sxs-lookup"><span data-stu-id="5770d-167">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]