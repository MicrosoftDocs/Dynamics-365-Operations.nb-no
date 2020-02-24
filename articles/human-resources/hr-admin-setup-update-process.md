---
title: Oppdateringsprosess
description: ''
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
ms.openlocfilehash: 1817e072805bafbf0d5a9eb2698ef75abc75ad68
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031096"
---
# <a name="update-process"></a><span data-ttu-id="fe271-102">Oppdateringsprosess</span><span class="sxs-lookup"><span data-stu-id="fe271-102">Update process</span></span>

<span data-ttu-id="fe271-103">Microsoft Dynamics 365 Human Resources er ekte programvare som tjeneste (SaaS) som gir kontinuerlige, berøringsfrie serviceoppdateringer.</span><span class="sxs-lookup"><span data-stu-id="fe271-103">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="fe271-104">Disse oppdateringene inneholder både program- og plattformendringer som ofte gir kritiske forbedringer av tjenesten, inkludert forskriftsmessige oppdateringer.</span><span class="sxs-lookup"><span data-stu-id="fe271-104">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="fe271-105">Oppdateringspolicy</span><span class="sxs-lookup"><span data-stu-id="fe271-105">Update policy</span></span>

<span data-ttu-id="fe271-106">Oppdateringer utgis regelmessig for alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="fe271-106">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="fe271-107">Human Resources støttes i henhold til [Microsoft Lifecycle-policyen](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), som gir konsekvente og forutsigbare retningslinjer for tilgjengelighet av produktstøtte.</span><span class="sxs-lookup"><span data-stu-id="fe271-107">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="fe271-108">Lanseringsfrekvens</span><span class="sxs-lookup"><span data-stu-id="fe271-108">Release cadence</span></span>

<span data-ttu-id="fe271-109">Human Resources-oppdateringer brukes for alle miljøer automatisk.</span><span class="sxs-lookup"><span data-stu-id="fe271-109">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="fe271-110">Human Resources har to typer lanseringer:</span><span class="sxs-lookup"><span data-stu-id="fe271-110">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="fe271-111">**Serviceoppdateringer**: ukentlige oppdateringer som inneholder feilrettinger og nye funksjoner.</span><span class="sxs-lookup"><span data-stu-id="fe271-111">**Service updates**: Weekly updates that include bug fixes and new features.</span></span> <span data-ttu-id="fe271-112">Serviceoppdateringer omfatter også aktuelle plattformoppdateringer når de frigis.</span><span class="sxs-lookup"><span data-stu-id="fe271-112">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="fe271-113">For en oversikt over når plattformoppdateringer frigis, se [Tabell 3: Plattformutgaver](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span><span class="sxs-lookup"><span data-stu-id="fe271-113">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="fe271-114">Ukentlige oppdateringer frigir vanligvis på onsdager.</span><span class="sxs-lookup"><span data-stu-id="fe271-114">Weekly updates usually release on Wednesdays.</span></span> <span data-ttu-id="fe271-115">Hvis du vil ha mer informasjon om ukentlige oppdateringer, kan du se [Hva er nytt eller endret i Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).</span><span class="sxs-lookup"><span data-stu-id="fe271-115">For more information about weekly updates, see [What's new or changed in Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).</span></span>

    <span data-ttu-id="fe271-116">Alle støttede datasentre oppdateres ukentlig med mindre annet er angitt.</span><span class="sxs-lookup"><span data-stu-id="fe271-116">All supported data centers update weekly, unless otherwise noted.</span></span> <span data-ttu-id="fe271-117">Ukentlige oppdateringer begynner vanligvis på onsdager og fullføres søndager.</span><span class="sxs-lookup"><span data-stu-id="fe271-117">Weekly updates typically begin on Wednesday and complete by Sunday.</span></span> <span data-ttu-id="fe271-118">USA, Australia, Europa, Storbritannia, Asia og Canada er inkludert i ukentlige oppdateringer.</span><span class="sxs-lookup"><span data-stu-id="fe271-118">US, Australia, Europe, UK, Asia, and Canada regions are included in weekly updates.</span></span> 

- <span data-ttu-id="fe271-119">**Common Data Service-løsningsoppdateringer**: Disse oppdateringene inntreffer omtrent hver sjette uke etter behov.</span><span class="sxs-lookup"><span data-stu-id="fe271-119">**Common Data Service solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="fe271-120">De inneholder nye enheter og endringer i eksisterende enheter i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="fe271-120">They include new entities and changes to existing entities in Common Data Service.</span></span> <span data-ttu-id="fe271-121">Disse oppdateringene utgis i de samme regionene som de ukentlige oppdateringene, og de tar omtrent seks uker på å replisere gjennom alle datasentre.</span><span class="sxs-lookup"><span data-stu-id="fe271-121">These updates release to the same regions as the weekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="fe271-122">Løsningsoppdateringer kan være rettet inn mot ukentlige serviceoppdateringer.</span><span class="sxs-lookup"><span data-stu-id="fe271-122">Solution updates may or may not align with weekly service updates.</span></span>

<span data-ttu-id="fe271-123">Følgende tabell viser et eksempel på en tidsplan:</span><span class="sxs-lookup"><span data-stu-id="fe271-123">The following table shows a sample schedule:</span></span>

| <span data-ttu-id="fe271-124">Uke</span><span class="sxs-lookup"><span data-stu-id="fe271-124">Week</span></span> | <span data-ttu-id="fe271-125">Oppdateringstype</span><span class="sxs-lookup"><span data-stu-id="fe271-125">Update type</span></span> |
| --- | --- |
| <span data-ttu-id="fe271-126">1</span><span class="sxs-lookup"><span data-stu-id="fe271-126">1</span></span> | <span data-ttu-id="fe271-127">Serviceoppdatering (alle områder)</span><span class="sxs-lookup"><span data-stu-id="fe271-127">Service update (all regions)</span></span> |
| <span data-ttu-id="fe271-128">2</span><span class="sxs-lookup"><span data-stu-id="fe271-128">2</span></span> | <span data-ttu-id="fe271-129">Serviceoppdatering (alle områder) + løsningsoppdatering (områder i uke 1)</span><span class="sxs-lookup"><span data-stu-id="fe271-129">Service update (all regions) + Solution update (Week 1 regions)</span></span> |
| <span data-ttu-id="fe271-130">3</span><span class="sxs-lookup"><span data-stu-id="fe271-130">3</span></span> | <span data-ttu-id="fe271-131">Serviceoppdatering (alle områder) + løsningsoppdatering (områder i uke 2)</span><span class="sxs-lookup"><span data-stu-id="fe271-131">Service update (all regions) + Solution update (Week 2 regions)</span></span> |
| <span data-ttu-id="fe271-132">4</span><span class="sxs-lookup"><span data-stu-id="fe271-132">4</span></span> | <span data-ttu-id="fe271-133">Serviceoppdatering (alle områder) + løsningsoppdatering (områder i uke 3)</span><span class="sxs-lookup"><span data-stu-id="fe271-133">Service update (all regions) + Solution update (Week 3 regions)</span></span> |
| <span data-ttu-id="fe271-134">5</span><span class="sxs-lookup"><span data-stu-id="fe271-134">5</span></span> | <span data-ttu-id="fe271-135">Serviceoppdatering (alle områder) + løsningsoppdatering (områder i uke 4)</span><span class="sxs-lookup"><span data-stu-id="fe271-135">Service update (all regions) + Solution update (Week 4 regions)</span></span> |
| <span data-ttu-id="fe271-136">6</span><span class="sxs-lookup"><span data-stu-id="fe271-136">6</span></span> | <span data-ttu-id="fe271-137">Serviceoppdatering (alle områder) + løsningsoppdatering (områder i uke 5)</span><span class="sxs-lookup"><span data-stu-id="fe271-137">Service update (all regions) + Solution update (Week 5 regions)</span></span> |
| <span data-ttu-id="fe271-138">7</span><span class="sxs-lookup"><span data-stu-id="fe271-138">7</span></span> | <span data-ttu-id="fe271-139">Serviceoppdatering (alle områder) + løsningsoppdatering (områder i uke 6)</span><span class="sxs-lookup"><span data-stu-id="fe271-139">Service update (all regions) + Solution update (Week 6 regions)</span></span> |
| <span data-ttu-id="fe271-140">8</span><span class="sxs-lookup"><span data-stu-id="fe271-140">8</span></span> | <span data-ttu-id="fe271-141">Serviceoppdatering (alle områder)</span><span class="sxs-lookup"><span data-stu-id="fe271-141">Service update (all regions)</span></span> |

> [!NOTE]
> <span data-ttu-id="fe271-142">Løsningsoppdateringer er tilgjengelige på alle datasentrene når de er frigitt.</span><span class="sxs-lookup"><span data-stu-id="fe271-142">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="fe271-143">Hvis du ikke vil vente på at oppdateringene skal replikeres automatisk, kan du bruke disse oppdateringene manuelt på alle miljøer i alle datasentre.</span><span class="sxs-lookup"><span data-stu-id="fe271-143">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="fe271-144">Når det er nødvendig, tilbyr Human Resources også følgende typer korrigeringer:</span><span class="sxs-lookup"><span data-stu-id="fe271-144">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="fe271-145">**Revisjon (hurti reparasjon**): feilrettinger som kan forekomme sammen med eller utenfor en ukentlig serviceoppdatering</span><span class="sxs-lookup"><span data-stu-id="fe271-145">**Revision (hotfix)**: bug fixes that can occur either with or apart from a weekly service update release</span></span>

- <span data-ttu-id="fe271-146">**Nødreparasjon**: proaktive og reaktive hurtigreparasjoner som er frittstående av natur, kan inkludere endringer bare i konfigurasjon eller kodeendringer for å løse problemer på områder direkte, og kan forekomme i stedet for en ukentlig serviceoppdatering</span><span class="sxs-lookup"><span data-stu-id="fe271-146">**Emergency fix**: proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a weekly service update release</span></span>

<span data-ttu-id="fe271-147">Versjoner er gjennomgått, testet og godkjent i et internt miljø.</span><span class="sxs-lookup"><span data-stu-id="fe271-147">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="fe271-148">Etter at buildene er godkjent, distribueres de deretter til produksjon.</span><span class="sxs-lookup"><span data-stu-id="fe271-148">After builds are signed off, they're then deployed to production.</span></span>

## <a name="exceptions-in-2019"></a><span data-ttu-id="fe271-149">Unntak i 2019</span><span class="sxs-lookup"><span data-stu-id="fe271-149">Exceptions in 2019</span></span>

<span data-ttu-id="fe271-150">Følgende datoer er unntak fra den vanlige utgivelsesplanen:</span><span class="sxs-lookup"><span data-stu-id="fe271-150">The following dates are exceptions to the regular release schedule:</span></span>

| <span data-ttu-id="fe271-151">Dato</span><span class="sxs-lookup"><span data-stu-id="fe271-151">Date</span></span> | <span data-ttu-id="fe271-152">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fe271-152">Description</span></span> |
| --- | --- |
| <span data-ttu-id="fe271-153">Uken fra 25. november</span><span class="sxs-lookup"><span data-stu-id="fe271-153">Week of November 25</span></span> | <span data-ttu-id="fe271-154">Ingen oppdateringer</span><span class="sxs-lookup"><span data-stu-id="fe271-154">No updates</span></span> |
| <span data-ttu-id="fe271-155">Uken fra 16. desember</span><span class="sxs-lookup"><span data-stu-id="fe271-155">Week of December 16</span></span> | <span data-ttu-id="fe271-156">Bare mindre oppdateringer</span><span class="sxs-lookup"><span data-stu-id="fe271-156">Minor updates only</span></span> |
| <span data-ttu-id="fe271-157">Uken fra 23. desember</span><span class="sxs-lookup"><span data-stu-id="fe271-157">Week of December 23</span></span> | <span data-ttu-id="fe271-158">Ingen oppdateringer</span><span class="sxs-lookup"><span data-stu-id="fe271-158">No updates</span></span> |
| <span data-ttu-id="fe271-159">Uken fra 30. desember</span><span class="sxs-lookup"><span data-stu-id="fe271-159">Week of December 30</span></span> | <span data-ttu-id="fe271-160">Ingen oppdateringer</span><span class="sxs-lookup"><span data-stu-id="fe271-160">No updates</span></span> |

## <a name="communications"></a><span data-ttu-id="fe271-161">Kommunikasjoner</span><span class="sxs-lookup"><span data-stu-id="fe271-161">Communications</span></span>

<span data-ttu-id="fe271-162">Du kan finne ut hva vi arbeider med for Human Resources, og hva vi har utgitt på følgende steder:</span><span class="sxs-lookup"><span data-stu-id="fe271-162">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="fe271-163">Dynamics 365 Human Resources-veikart</span><span class="sxs-lookup"><span data-stu-id="fe271-163">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/talent/)

- [<span data-ttu-id="fe271-164">Lanseringsplaner for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="fe271-164">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="fe271-165">Hva er nytt eller endret i Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="fe271-165">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="fe271-166">[Problemsøk i Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (bare for feil relatert til plattform)</span><span class="sxs-lookup"><span data-stu-id="fe271-166">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="fe271-167">Human Resources-blogg</span><span class="sxs-lookup"><span data-stu-id="fe271-167">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="fe271-168">Human Resources Yammer-samfunn</span><span class="sxs-lookup"><span data-stu-id="fe271-168">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="fe271-169">Forhåndsversjoner av funksjoner i et sandkassemiljø</span><span class="sxs-lookup"><span data-stu-id="fe271-169">Preview features in a sandbox environment</span></span>

<span data-ttu-id="fe271-170">Du kan validere forhåndsversjoner av funksjoner i et sandkassemiljø før du aktiverer dem i produksjonsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="fe271-170">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="fe271-171">Hvis du vil ha mer informasjon om hvordan du aktiverer funksjoner, kan du se [Oversikt over funksjonsbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="fe271-171">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="fe271-172">Alle nye funksjoner blir forhåndsvist i minst 30 dager, og vanligvis 30-60 dager.</span><span class="sxs-lookup"><span data-stu-id="fe271-172">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="fe271-173">Større funksjoner er vanligvis tilgjengelig i oktober og april i hvert år etter forhåndsvisningsperioden.</span><span class="sxs-lookup"><span data-stu-id="fe271-173">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="fe271-174">Så snart du ser nye funksjoner i arbeidsområdet for funksjonsbehandling, kan du aktivere dem.</span><span class="sxs-lookup"><span data-stu-id="fe271-174">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="fe271-175">Det kan hende at noen funksjoner er aktivert som standard.</span><span class="sxs-lookup"><span data-stu-id="fe271-175">Some features may be on by default.</span></span>

<span data-ttu-id="fe271-176">Noen ganger vil en integrert funksjon være aktivert som standard og kan ikke deaktiveres (for eksempel arbeidsområdet Funksjonsbehandling).</span><span class="sxs-lookup"><span data-stu-id="fe271-176">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="fe271-177">Når en funksjon er generelt tilgjengelig, kan den aktiveres eller deaktiveres i produksjonsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="fe271-177">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="fe271-178">Arbeidsområdet for funksjonsbehandling angir når en forhåndsvisningsfunksjon blir obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="fe271-178">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="fe271-179">Denne datoen er vanligvis 1. oktober eller 1. april for å justeres med de halvårlige frigivelsesplanene.</span><span class="sxs-lookup"><span data-stu-id="fe271-179">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="fe271-180">De kan ikke deaktivere obligatoriske funksjoner.</span><span class="sxs-lookup"><span data-stu-id="fe271-180">You can't turn off mandatory features.</span></span> <span data-ttu-id="fe271-181">Før den blir obligatorisk, kan du slå en funksjon på og av i alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="fe271-181">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="fe271-182">Vi anbefaler på det sterkeste forhåndsversjoner av funksjoner i et sandkasse- eller prøvemiljø.</span><span class="sxs-lookup"><span data-stu-id="fe271-182">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="fe271-183">Det er best å opprette en kopi av gjeldende produksjonsmiljø eller database i et sandkassemiljø, slik at du får den komplette opplevelsen av de nye funksjonene med dataene dine.</span><span class="sxs-lookup"><span data-stu-id="fe271-183">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="fe271-184">Hvis du vil ha mer informasjon om hvordan du klargjør et sandkassemiljø, kan du se [Klargjøre et Human Resources-prosjekt](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="fe271-184">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="fe271-185">Hvis du vil fjerne et testmiljø, kan du se [Fjerne en forekomst](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="fe271-185">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="fe271-186">Rapportere feil</span><span class="sxs-lookup"><span data-stu-id="fe271-186">Report bugs</span></span>

<span data-ttu-id="fe271-187">Når du tester forhåndsversjoner av funksjoner eller prøver nye funksjoner, kan det hende at du finner elementer som ikke fungerer som forventet.</span><span class="sxs-lookup"><span data-stu-id="fe271-187">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="fe271-188">Vi ber deg om å rapportere alle feil gjennom [Microsoft Dynamics 365-støtte](https://dynamics.microsoft.com/support/).</span><span class="sxs-lookup"><span data-stu-id="fe271-188">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="fe271-189">Se også</span><span class="sxs-lookup"><span data-stu-id="fe271-189">See also</span></span>

- [<span data-ttu-id="fe271-190">Lanseringsplaner for Dynamics 365 og Power Platform</span><span class="sxs-lookup"><span data-stu-id="fe271-190">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)
- [<span data-ttu-id="fe271-191">Hva er nytt eller endret i Dynamics 365 Human Resource</span><span class="sxs-lookup"><span data-stu-id="fe271-191">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="fe271-192">Policy for programvarelivssyklus</span><span class="sxs-lookup"><span data-stu-id="fe271-192">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

