---
title: Oppdatere prosess
description: Microsoft Dynamics 365 Human Resources er ekte programvare som tjeneste (SaaS) som gir kontinuerlige, berøringsfrie serviceoppdateringer for program- og plattformendringer.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: be9be5509f933ecbda5bf6d040027a7bac8b666d
ms.sourcegitcommit: 5472005274f2f94fba82dda90de128f39d8b8390
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759965"
---
# <a name="update-process"></a><span data-ttu-id="2a8af-103">Oppdatere prosess</span><span class="sxs-lookup"><span data-stu-id="2a8af-103">Update process</span></span>

<span data-ttu-id="2a8af-104">Microsoft Dynamics 365 Human Resources er ekte programvare som tjeneste (SaaS) som gir kontinuerlige, berøringsfrie serviceoppdateringer.</span><span class="sxs-lookup"><span data-stu-id="2a8af-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="2a8af-105">Disse oppdateringene inneholder både program- og plattformendringer som ofte gir kritiske forbedringer av tjenesten, inkludert forskriftsmessige oppdateringer.</span><span class="sxs-lookup"><span data-stu-id="2a8af-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="2a8af-106">Oppdateringspolicy</span><span class="sxs-lookup"><span data-stu-id="2a8af-106">Update policy</span></span>

<span data-ttu-id="2a8af-107">Oppdateringer utgis regelmessig for alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="2a8af-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="2a8af-108">Human Resources støttes i henhold til [Microsoft Lifecycle-policyen](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), som gir konsekvente og forutsigbare retningslinjer for tilgjengelighet av produktstøtte.</span><span class="sxs-lookup"><span data-stu-id="2a8af-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="2a8af-109">Lanseringsfrekvens</span><span class="sxs-lookup"><span data-stu-id="2a8af-109">Release cadence</span></span> 

<span data-ttu-id="2a8af-110">Human Resources-oppdateringer brukes for alle miljøer automatisk.</span><span class="sxs-lookup"><span data-stu-id="2a8af-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="2a8af-111">Human Resources har to typer lanseringer:</span><span class="sxs-lookup"><span data-stu-id="2a8af-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="2a8af-112">**Serviceoppdateringer**: Oppdateringer skjer annenhver uke som inneholder feilrettinger og nye funksjoner.</span><span class="sxs-lookup"><span data-stu-id="2a8af-112">**Service updates**: Updates occur every two weeks that include bug fixes and new features.</span></span> <span data-ttu-id="2a8af-113">Serviceoppdateringer omfatter også aktuelle plattformoppdateringer når de frigis.</span><span class="sxs-lookup"><span data-stu-id="2a8af-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="2a8af-114">For en oversikt over når plattformoppdateringer frigis, se [Tabell 3: Plattformutgaver](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span><span class="sxs-lookup"><span data-stu-id="2a8af-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="2a8af-115">oppdateringer annenhver uke har en trinnvis, global distribusjon på tvers av områder.</span><span class="sxs-lookup"><span data-stu-id="2a8af-115">Biweekly updates have a staged global rollout across regions.</span></span> <span data-ttu-id="2a8af-116">Hvis du vil ha mer informasjon om oppdateringer annenhver uke, kan du se [Hva er nytt eller endret i Dynamics 365 Human Resources](hr-admin-whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="2a8af-116">For more information about biweekly updates, see [What's new or changed in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span></span>

    <span data-ttu-id="2a8af-117">Alle støttede datasentre oppdateres annenhver uke med mindre annet er angitt.</span><span class="sxs-lookup"><span data-stu-id="2a8af-117">All supported data centers update every two weeks, unless otherwise noted.</span></span> <span data-ttu-id="2a8af-118">USA, Australia, Europa, Storbritannia, Asia og Canada er inkludert i oppdateringer annenhver uke.</span><span class="sxs-lookup"><span data-stu-id="2a8af-118">US, Australia, Europe, UK, Asia, and Canada regions are included in biweekly updates.</span></span> 

- <span data-ttu-id="2a8af-119">**Common Data Service-løsningsoppdateringer**: Disse oppdateringene inntreffer omtrent hver sjette uke etter behov.</span><span class="sxs-lookup"><span data-stu-id="2a8af-119">**Common Data Service solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="2a8af-120">De inneholder nye enheter og endringer i eksisterende enheter i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="2a8af-120">They include new entities and changes to existing entities in Common Data Service.</span></span> <span data-ttu-id="2a8af-121">Disse oppdateringene utgis i de samme regionene som oppdateringene annenhver uke, og de tar omtrent seks uker på å replisere gjennom alle datasentre.</span><span class="sxs-lookup"><span data-stu-id="2a8af-121">These updates release to the same regions as the biweekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="2a8af-122">Løsningsoppdateringer kan være rettet inn mot serviceoppdateringer annenhver uke.</span><span class="sxs-lookup"><span data-stu-id="2a8af-122">Solution updates may or may not align with biweekly service updates.</span></span>

> [!NOTE]
> <span data-ttu-id="2a8af-123">Løsningsoppdateringer er tilgjengelige på alle datasentrene når de er frigitt.</span><span class="sxs-lookup"><span data-stu-id="2a8af-123">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="2a8af-124">Hvis du ikke vil vente på at oppdateringene skal replikeres automatisk, kan du bruke disse oppdateringene manuelt på alle miljøer i alle datasentre.</span><span class="sxs-lookup"><span data-stu-id="2a8af-124">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="2a8af-125">Når det er nødvendig, tilbyr Human Resources også følgende typer korrigeringer:</span><span class="sxs-lookup"><span data-stu-id="2a8af-125">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="2a8af-126">**Revisjon (hurtigreparasjon**): Feilrettinger som kan forekomme sammen med eller utenfor en serviceoppdatering annenhver uke</span><span class="sxs-lookup"><span data-stu-id="2a8af-126">**Revision (hotfix)**: Bug fixes that can occur either with or apart from a biweekly service update release</span></span>

- <span data-ttu-id="2a8af-127">**Nødreparasjon**: Proaktive og reaktive hurtigreparasjoner som er frittstående av natur, kan inkludere endringer bare i konfigurasjon eller kodeendringer for å løse problemer på områder direkte, og kan forekomme i stedet for en serviceoppdatering annenhver uke</span><span class="sxs-lookup"><span data-stu-id="2a8af-127">**Emergency fix**: Proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a biweekly service update release</span></span>

<span data-ttu-id="2a8af-128">Versjoner er gjennomgått, testet og godkjent i et internt miljø.</span><span class="sxs-lookup"><span data-stu-id="2a8af-128">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="2a8af-129">Etter at buildene er godkjent, distribueres de deretter til produksjon.</span><span class="sxs-lookup"><span data-stu-id="2a8af-129">After builds are signed off, they're then deployed to production.</span></span>

## <a name="release-cadence-exceptions-in-2020"></a><span data-ttu-id="2a8af-130">Unntak fra lanseringsfrekvens i 2020</span><span class="sxs-lookup"><span data-stu-id="2a8af-130">Release cadence exceptions in 2020</span></span>

<span data-ttu-id="2a8af-131">Hvis du vil ha en konto for helligdager, er utgivelsesplanen for november og desember 2020 som følger:</span><span class="sxs-lookup"><span data-stu-id="2a8af-131">To account for holidays, the release schedule for November and December 2020 is as follows:</span></span>

- <span data-ttu-id="2a8af-132">Novemberutgivelse: 2–13. november</span><span class="sxs-lookup"><span data-stu-id="2a8af-132">November release: November 2 - November 13</span></span>
- <span data-ttu-id="2a8af-133">Desemberutgivelse: 30. november til 11. desember</span><span class="sxs-lookup"><span data-stu-id="2a8af-133">December release: November 30 - December 11</span></span>
 
<span data-ttu-id="2a8af-134">Lanseringsfrekvensen på to uker vil fortsette som vanlig den 11. januar 2021.</span><span class="sxs-lookup"><span data-stu-id="2a8af-134">The two-week release cadence will resume as usual on January 11, 2021.</span></span>

## <a name="communications"></a><span data-ttu-id="2a8af-135">Kommunikasjoner</span><span class="sxs-lookup"><span data-stu-id="2a8af-135">Communications</span></span>

<span data-ttu-id="2a8af-136">Du kan finne ut hva vi arbeider med for Human Resources, og hva vi har utgitt på følgende steder:</span><span class="sxs-lookup"><span data-stu-id="2a8af-136">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="2a8af-137">Dynamics 365 Human Resources-veikart</span><span class="sxs-lookup"><span data-stu-id="2a8af-137">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/human-resources/)

- [<span data-ttu-id="2a8af-138">Lanseringsplaner for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="2a8af-138">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="2a8af-139">Hva er nytt eller endret i Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="2a8af-139">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="2a8af-140">[Problemsøk i Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (bare for feil relatert til plattform)</span><span class="sxs-lookup"><span data-stu-id="2a8af-140">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="2a8af-141">Human Resources-blogg</span><span class="sxs-lookup"><span data-stu-id="2a8af-141">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="2a8af-142">Human Resources Yammer-samfunn</span><span class="sxs-lookup"><span data-stu-id="2a8af-142">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="2a8af-143">Forhåndsversjoner av funksjoner i et sandkassemiljø</span><span class="sxs-lookup"><span data-stu-id="2a8af-143">Preview features in a sandbox environment</span></span>

<span data-ttu-id="2a8af-144">Du kan validere forhåndsversjoner av funksjoner i et sandkassemiljø før du aktiverer dem i produksjonsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="2a8af-144">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="2a8af-145">Hvis du vil ha mer informasjon om hvordan du aktiverer funksjoner, kan du se [Oversikt over funksjonsbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="2a8af-145">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="2a8af-146">Alle nye funksjoner blir forhåndsvist i minst 30 dager, og vanligvis 30-60 dager.</span><span class="sxs-lookup"><span data-stu-id="2a8af-146">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="2a8af-147">Større funksjoner er vanligvis tilgjengelig i oktober og april i hvert år etter forhåndsvisningsperioden.</span><span class="sxs-lookup"><span data-stu-id="2a8af-147">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="2a8af-148">Så snart du ser nye funksjoner i arbeidsområdet for funksjonsbehandling, kan du aktivere dem.</span><span class="sxs-lookup"><span data-stu-id="2a8af-148">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="2a8af-149">Det kan hende at noen funksjoner er aktivert som standard.</span><span class="sxs-lookup"><span data-stu-id="2a8af-149">Some features may be on by default.</span></span>

<span data-ttu-id="2a8af-150">Noen ganger vil en integrert funksjon være aktivert som standard og kan ikke deaktiveres (for eksempel arbeidsområdet Funksjonsbehandling).</span><span class="sxs-lookup"><span data-stu-id="2a8af-150">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="2a8af-151">Når en funksjon er generelt tilgjengelig, kan den aktiveres eller deaktiveres i produksjonsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="2a8af-151">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="2a8af-152">Arbeidsområdet for funksjonsbehandling angir når en forhåndsvisningsfunksjon blir obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="2a8af-152">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="2a8af-153">Denne datoen er vanligvis 1. oktober eller 1. april for å justeres med de halvårlige frigivelsesplanene.</span><span class="sxs-lookup"><span data-stu-id="2a8af-153">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="2a8af-154">De kan ikke deaktivere obligatoriske funksjoner.</span><span class="sxs-lookup"><span data-stu-id="2a8af-154">You can't turn off mandatory features.</span></span> <span data-ttu-id="2a8af-155">Før den blir obligatorisk, kan du slå en funksjon på og av i alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="2a8af-155">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="2a8af-156">Vi anbefaler på det sterkeste forhåndsversjoner av funksjoner i et sandkasse- eller prøvemiljø.</span><span class="sxs-lookup"><span data-stu-id="2a8af-156">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="2a8af-157">Det er best å opprette en kopi av gjeldende produksjonsmiljø eller database i et sandkassemiljø, slik at du får den komplette opplevelsen av de nye funksjonene med dataene dine.</span><span class="sxs-lookup"><span data-stu-id="2a8af-157">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="2a8af-158">Hvis du vil ha mer informasjon om hvordan du klargjør et sandkassemiljø, kan du se [Klargjøre et Human Resources-prosjekt](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="2a8af-158">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="2a8af-159">Hvis du vil fjerne et testmiljø, kan du se [Fjerne en forekomst](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="2a8af-159">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="2a8af-160">Rapportere feil</span><span class="sxs-lookup"><span data-stu-id="2a8af-160">Report bugs</span></span>

<span data-ttu-id="2a8af-161">Når du tester forhåndsversjoner av funksjoner eller prøver nye funksjoner, kan det hende at du finner elementer som ikke fungerer som forventet.</span><span class="sxs-lookup"><span data-stu-id="2a8af-161">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="2a8af-162">Vi ber deg om å rapportere alle feil gjennom [Microsoft Dynamics 365-støtte](https://dynamics.microsoft.com/support/).</span><span class="sxs-lookup"><span data-stu-id="2a8af-162">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="2a8af-163">Se også</span><span class="sxs-lookup"><span data-stu-id="2a8af-163">See also</span></span>

[<span data-ttu-id="2a8af-164">Lanseringsplaner for Dynamics 365 og Power Platform</span><span class="sxs-lookup"><span data-stu-id="2a8af-164">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)</br>
[<span data-ttu-id="2a8af-165">Hva er nytt eller endret i Dynamics 365 Human Resource</span><span class="sxs-lookup"><span data-stu-id="2a8af-165">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="2a8af-166">Policy for programvarelivssyklus</span><span class="sxs-lookup"><span data-stu-id="2a8af-166">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

