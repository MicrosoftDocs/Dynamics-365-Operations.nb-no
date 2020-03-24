---
title: Oppdatere prosess
description: Microsoft Dynamics 365 Human Resources er ekte programvare som tjeneste (SaaS) som gir kontinuerlige, berøringsfrie serviceoppdateringer for program- og plattformendringer.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 267682f4497bacf70f93840a948d0e525dfa4aa1
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092207"
---
# <a name="update-process"></a><span data-ttu-id="45825-103">Oppdatere prosess</span><span class="sxs-lookup"><span data-stu-id="45825-103">Update process</span></span>

<span data-ttu-id="45825-104">Microsoft Dynamics 365 Human Resources er ekte programvare som tjeneste (SaaS) som gir kontinuerlige, berøringsfrie serviceoppdateringer.</span><span class="sxs-lookup"><span data-stu-id="45825-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="45825-105">Disse oppdateringene inneholder både program- og plattformendringer som ofte gir kritiske forbedringer av tjenesten, inkludert forskriftsmessige oppdateringer.</span><span class="sxs-lookup"><span data-stu-id="45825-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="45825-106">Oppdateringspolicy</span><span class="sxs-lookup"><span data-stu-id="45825-106">Update policy</span></span>

<span data-ttu-id="45825-107">Oppdateringer utgis regelmessig for alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="45825-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="45825-108">Human Resources støttes i henhold til [Microsoft Lifecycle-policyen](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), som gir konsekvente og forutsigbare retningslinjer for tilgjengelighet av produktstøtte.</span><span class="sxs-lookup"><span data-stu-id="45825-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="45825-109">Lanseringsfrekvens</span><span class="sxs-lookup"><span data-stu-id="45825-109">Release cadence</span></span>

<span data-ttu-id="45825-110">Human Resources-oppdateringer brukes for alle miljøer automatisk.</span><span class="sxs-lookup"><span data-stu-id="45825-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="45825-111">Human Resources har to typer lanseringer:</span><span class="sxs-lookup"><span data-stu-id="45825-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="45825-112">**Serviceoppdateringer**: ukentlige oppdateringer som inneholder feilrettinger og nye funksjoner.</span><span class="sxs-lookup"><span data-stu-id="45825-112">**Service updates**: Weekly updates that include bug fixes and new features.</span></span> <span data-ttu-id="45825-113">Serviceoppdateringer omfatter også aktuelle plattformoppdateringer når de frigis.</span><span class="sxs-lookup"><span data-stu-id="45825-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="45825-114">For en oversikt over når plattformoppdateringer frigis, se [Tabell 3: Plattformutgaver](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span><span class="sxs-lookup"><span data-stu-id="45825-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="45825-115">Ukentlige oppdateringer frigir vanligvis på onsdager.</span><span class="sxs-lookup"><span data-stu-id="45825-115">Weekly updates usually release on Wednesdays.</span></span> <span data-ttu-id="45825-116">Hvis du vil ha mer informasjon om ukentlige oppdateringer, kan du se [Hva er nytt eller endret i Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).</span><span class="sxs-lookup"><span data-stu-id="45825-116">For more information about weekly updates, see [What's new or changed in Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).</span></span>

    <span data-ttu-id="45825-117">Alle støttede datasentre oppdateres ukentlig med mindre annet er angitt.</span><span class="sxs-lookup"><span data-stu-id="45825-117">All supported data centers update weekly, unless otherwise noted.</span></span> <span data-ttu-id="45825-118">Ukentlige oppdateringer begynner vanligvis på onsdager og fullføres søndager.</span><span class="sxs-lookup"><span data-stu-id="45825-118">Weekly updates typically begin on Wednesday and complete by Sunday.</span></span> <span data-ttu-id="45825-119">USA, Australia, Europa, Storbritannia, Asia og Canada er inkludert i ukentlige oppdateringer.</span><span class="sxs-lookup"><span data-stu-id="45825-119">US, Australia, Europe, UK, Asia, and Canada regions are included in weekly updates.</span></span> 

- <span data-ttu-id="45825-120">**Common Data Service-løsningsoppdateringer**: Disse oppdateringene inntreffer omtrent hver sjette uke etter behov.</span><span class="sxs-lookup"><span data-stu-id="45825-120">**Common Data Service solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="45825-121">De inneholder nye enheter og endringer i eksisterende enheter i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="45825-121">They include new entities and changes to existing entities in Common Data Service.</span></span> <span data-ttu-id="45825-122">Disse oppdateringene utgis i de samme regionene som de ukentlige oppdateringene, og de tar omtrent seks uker på å replisere gjennom alle datasentre.</span><span class="sxs-lookup"><span data-stu-id="45825-122">These updates release to the same regions as the weekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="45825-123">Løsningsoppdateringer kan være rettet inn mot ukentlige serviceoppdateringer.</span><span class="sxs-lookup"><span data-stu-id="45825-123">Solution updates may or may not align with weekly service updates.</span></span>

<span data-ttu-id="45825-124">Følgende tabell viser et eksempel på en tidsplan:</span><span class="sxs-lookup"><span data-stu-id="45825-124">The following table shows a sample schedule:</span></span>

| <span data-ttu-id="45825-125">Uke</span><span class="sxs-lookup"><span data-stu-id="45825-125">Week</span></span> | <span data-ttu-id="45825-126">Oppdateringstype</span><span class="sxs-lookup"><span data-stu-id="45825-126">Update type</span></span> |
| --- | --- |
| <span data-ttu-id="45825-127">1</span><span class="sxs-lookup"><span data-stu-id="45825-127">1</span></span> | <span data-ttu-id="45825-128">Serviceoppdatering (alle områder)</span><span class="sxs-lookup"><span data-stu-id="45825-128">Service update (all regions)</span></span> |
| <span data-ttu-id="45825-129">2</span><span class="sxs-lookup"><span data-stu-id="45825-129">2</span></span> | <span data-ttu-id="45825-130">Serviceoppdatering (alle områder) + løsningsoppdatering (områder i uke 1)</span><span class="sxs-lookup"><span data-stu-id="45825-130">Service update (all regions) + Solution update (Week 1 regions)</span></span> |
| <span data-ttu-id="45825-131">3</span><span class="sxs-lookup"><span data-stu-id="45825-131">3</span></span> | <span data-ttu-id="45825-132">Serviceoppdatering (alle områder) + løsningsoppdatering (områder i uke 2)</span><span class="sxs-lookup"><span data-stu-id="45825-132">Service update (all regions) + Solution update (Week 2 regions)</span></span> |
| <span data-ttu-id="45825-133">4</span><span class="sxs-lookup"><span data-stu-id="45825-133">4</span></span> | <span data-ttu-id="45825-134">Serviceoppdatering (alle områder) + løsningsoppdatering (områder i uke 3)</span><span class="sxs-lookup"><span data-stu-id="45825-134">Service update (all regions) + Solution update (Week 3 regions)</span></span> |
| <span data-ttu-id="45825-135">5</span><span class="sxs-lookup"><span data-stu-id="45825-135">5</span></span> | <span data-ttu-id="45825-136">Serviceoppdatering (alle områder) + løsningsoppdatering (områder i uke 4)</span><span class="sxs-lookup"><span data-stu-id="45825-136">Service update (all regions) + Solution update (Week 4 regions)</span></span> |
| <span data-ttu-id="45825-137">6</span><span class="sxs-lookup"><span data-stu-id="45825-137">6</span></span> | <span data-ttu-id="45825-138">Serviceoppdatering (alle områder) + løsningsoppdatering (områder i uke 5)</span><span class="sxs-lookup"><span data-stu-id="45825-138">Service update (all regions) + Solution update (Week 5 regions)</span></span> |
| <span data-ttu-id="45825-139">7</span><span class="sxs-lookup"><span data-stu-id="45825-139">7</span></span> | <span data-ttu-id="45825-140">Serviceoppdatering (alle områder) + løsningsoppdatering (områder i uke 6)</span><span class="sxs-lookup"><span data-stu-id="45825-140">Service update (all regions) + Solution update (Week 6 regions)</span></span> |
| <span data-ttu-id="45825-141">8</span><span class="sxs-lookup"><span data-stu-id="45825-141">8</span></span> | <span data-ttu-id="45825-142">Serviceoppdatering (alle områder)</span><span class="sxs-lookup"><span data-stu-id="45825-142">Service update (all regions)</span></span> |

> [!NOTE]
> <span data-ttu-id="45825-143">Løsningsoppdateringer er tilgjengelige på alle datasentrene når de er frigitt.</span><span class="sxs-lookup"><span data-stu-id="45825-143">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="45825-144">Hvis du ikke vil vente på at oppdateringene skal replikeres automatisk, kan du bruke disse oppdateringene manuelt på alle miljøer i alle datasentre.</span><span class="sxs-lookup"><span data-stu-id="45825-144">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="45825-145">Når det er nødvendig, tilbyr Human Resources også følgende typer korrigeringer:</span><span class="sxs-lookup"><span data-stu-id="45825-145">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="45825-146">**Revisjon (hurti reparasjon**): feilrettinger som kan forekomme sammen med eller utenfor en ukentlig serviceoppdatering</span><span class="sxs-lookup"><span data-stu-id="45825-146">**Revision (hotfix)**: bug fixes that can occur either with or apart from a weekly service update release</span></span>

- <span data-ttu-id="45825-147">**Nødreparasjon**: proaktive og reaktive hurtigreparasjoner som er frittstående av natur, kan inkludere endringer bare i konfigurasjon eller kodeendringer for å løse problemer på områder direkte, og kan forekomme i stedet for en ukentlig serviceoppdatering</span><span class="sxs-lookup"><span data-stu-id="45825-147">**Emergency fix**: proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a weekly service update release</span></span>

<span data-ttu-id="45825-148">Versjoner er gjennomgått, testet og godkjent i et internt miljø.</span><span class="sxs-lookup"><span data-stu-id="45825-148">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="45825-149">Etter at buildene er godkjent, distribueres de deretter til produksjon.</span><span class="sxs-lookup"><span data-stu-id="45825-149">After builds are signed off, they're then deployed to production.</span></span>

## <a name="exceptions-in-2019"></a><span data-ttu-id="45825-150">Unntak i 2019</span><span class="sxs-lookup"><span data-stu-id="45825-150">Exceptions in 2019</span></span>

<span data-ttu-id="45825-151">Følgende datoer er unntak fra den vanlige utgivelsesplanen:</span><span class="sxs-lookup"><span data-stu-id="45825-151">The following dates are exceptions to the regular release schedule:</span></span>

| <span data-ttu-id="45825-152">Dato</span><span class="sxs-lookup"><span data-stu-id="45825-152">Date</span></span> | <span data-ttu-id="45825-153">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="45825-153">Description</span></span> |
| --- | --- |
| <span data-ttu-id="45825-154">Uken fra 25. november</span><span class="sxs-lookup"><span data-stu-id="45825-154">Week of November 25</span></span> | <span data-ttu-id="45825-155">Ingen oppdateringer</span><span class="sxs-lookup"><span data-stu-id="45825-155">No updates</span></span> |
| <span data-ttu-id="45825-156">Uken fra 16. desember</span><span class="sxs-lookup"><span data-stu-id="45825-156">Week of December 16</span></span> | <span data-ttu-id="45825-157">Bare mindre oppdateringer</span><span class="sxs-lookup"><span data-stu-id="45825-157">Minor updates only</span></span> |
| <span data-ttu-id="45825-158">Uken fra 23. desember</span><span class="sxs-lookup"><span data-stu-id="45825-158">Week of December 23</span></span> | <span data-ttu-id="45825-159">Ingen oppdateringer</span><span class="sxs-lookup"><span data-stu-id="45825-159">No updates</span></span> |
| <span data-ttu-id="45825-160">Uken fra 30. desember</span><span class="sxs-lookup"><span data-stu-id="45825-160">Week of December 30</span></span> | <span data-ttu-id="45825-161">Ingen oppdateringer</span><span class="sxs-lookup"><span data-stu-id="45825-161">No updates</span></span> |

## <a name="communications"></a><span data-ttu-id="45825-162">Kommunikasjoner</span><span class="sxs-lookup"><span data-stu-id="45825-162">Communications</span></span>

<span data-ttu-id="45825-163">Du kan finne ut hva vi arbeider med for Human Resources, og hva vi har utgitt på følgende steder:</span><span class="sxs-lookup"><span data-stu-id="45825-163">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="45825-164">Dynamics 365 Human Resources-veikart</span><span class="sxs-lookup"><span data-stu-id="45825-164">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/talent/)

- [<span data-ttu-id="45825-165">Lanseringsplaner for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="45825-165">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="45825-166">Hva er nytt eller endret i Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="45825-166">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="45825-167">[Problemsøk i Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (bare for feil relatert til plattform)</span><span class="sxs-lookup"><span data-stu-id="45825-167">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="45825-168">Human Resources-blogg</span><span class="sxs-lookup"><span data-stu-id="45825-168">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="45825-169">Human Resources Yammer-samfunn</span><span class="sxs-lookup"><span data-stu-id="45825-169">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="45825-170">Forhåndsversjoner av funksjoner i et sandkassemiljø</span><span class="sxs-lookup"><span data-stu-id="45825-170">Preview features in a sandbox environment</span></span>

<span data-ttu-id="45825-171">Du kan validere forhåndsversjoner av funksjoner i et sandkassemiljø før du aktiverer dem i produksjonsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="45825-171">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="45825-172">Hvis du vil ha mer informasjon om hvordan du aktiverer funksjoner, kan du se [Oversikt over funksjonsbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="45825-172">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="45825-173">Alle nye funksjoner blir forhåndsvist i minst 30 dager, og vanligvis 30-60 dager.</span><span class="sxs-lookup"><span data-stu-id="45825-173">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="45825-174">Større funksjoner er vanligvis tilgjengelig i oktober og april i hvert år etter forhåndsvisningsperioden.</span><span class="sxs-lookup"><span data-stu-id="45825-174">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="45825-175">Så snart du ser nye funksjoner i arbeidsområdet for funksjonsbehandling, kan du aktivere dem.</span><span class="sxs-lookup"><span data-stu-id="45825-175">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="45825-176">Det kan hende at noen funksjoner er aktivert som standard.</span><span class="sxs-lookup"><span data-stu-id="45825-176">Some features may be on by default.</span></span>

<span data-ttu-id="45825-177">Noen ganger vil en integrert funksjon være aktivert som standard og kan ikke deaktiveres (for eksempel arbeidsområdet Funksjonsbehandling).</span><span class="sxs-lookup"><span data-stu-id="45825-177">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="45825-178">Når en funksjon er generelt tilgjengelig, kan den aktiveres eller deaktiveres i produksjonsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="45825-178">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="45825-179">Arbeidsområdet for funksjonsbehandling angir når en forhåndsvisningsfunksjon blir obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="45825-179">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="45825-180">Denne datoen er vanligvis 1. oktober eller 1. april for å justeres med de halvårlige frigivelsesplanene.</span><span class="sxs-lookup"><span data-stu-id="45825-180">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="45825-181">De kan ikke deaktivere obligatoriske funksjoner.</span><span class="sxs-lookup"><span data-stu-id="45825-181">You can't turn off mandatory features.</span></span> <span data-ttu-id="45825-182">Før den blir obligatorisk, kan du slå en funksjon på og av i alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="45825-182">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="45825-183">Vi anbefaler på det sterkeste forhåndsversjoner av funksjoner i et sandkasse- eller prøvemiljø.</span><span class="sxs-lookup"><span data-stu-id="45825-183">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="45825-184">Det er best å opprette en kopi av gjeldende produksjonsmiljø eller database i et sandkassemiljø, slik at du får den komplette opplevelsen av de nye funksjonene med dataene dine.</span><span class="sxs-lookup"><span data-stu-id="45825-184">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="45825-185">Hvis du vil ha mer informasjon om hvordan du klargjør et sandkassemiljø, kan du se [Klargjøre et Human Resources-prosjekt](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="45825-185">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="45825-186">Hvis du vil fjerne et testmiljø, kan du se [Fjerne en forekomst](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="45825-186">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="45825-187">Rapportere feil</span><span class="sxs-lookup"><span data-stu-id="45825-187">Report bugs</span></span>

<span data-ttu-id="45825-188">Når du tester forhåndsversjoner av funksjoner eller prøver nye funksjoner, kan det hende at du finner elementer som ikke fungerer som forventet.</span><span class="sxs-lookup"><span data-stu-id="45825-188">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="45825-189">Vi ber deg om å rapportere alle feil gjennom [Microsoft Dynamics 365-støtte](https://dynamics.microsoft.com/support/).</span><span class="sxs-lookup"><span data-stu-id="45825-189">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="45825-190">Se også</span><span class="sxs-lookup"><span data-stu-id="45825-190">See also</span></span>

- [<span data-ttu-id="45825-191">Lanseringsplaner for Dynamics 365 og Power Platform</span><span class="sxs-lookup"><span data-stu-id="45825-191">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)
- [<span data-ttu-id="45825-192">Hva er nytt eller endret i Dynamics 365 Human Resource</span><span class="sxs-lookup"><span data-stu-id="45825-192">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="45825-193">Policy for programvarelivssyklus</span><span class="sxs-lookup"><span data-stu-id="45825-193">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

