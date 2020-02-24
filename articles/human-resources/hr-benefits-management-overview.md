---
title: Oversikt over Fordelsbehandling
description: Oversikt over forhåndsversjonen av funksjonen Fordelsbehandling i Dynamics 365 Human Resources. Gi de ansatte utvidede fordelsalternativer med en brukervennlig Internett-opplevelse.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029469"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="a3c5e-104">Oversikt over Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="a3c5e-104">Benefits management overview</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="a3c5e-105">For å være konkurransedyktig må du tilby et stort utvalg av fordeler for å tiltrekke deg og beholde de beste ansatte.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="a3c5e-106">I tillegg til standardfordeler som dekning av lege- og tannlegeutgifter ønsker du kanskje også å tilby utvidede tjenester, for eksempel starthjelp, rekreasjonsprogrammer og dekning av klær.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="a3c5e-107">Med forhåndsversjonen av funksjonen Fordelsbehandling i Microsoft Dynamics 365 Human Resources får du en fleksibel løsning som støtter en rekke ulike fordelsalternativer.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-107">The Benefits management preview feature in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="a3c5e-108">Human Resources inneholder også en brukervennlig ansattopplevelse som viser tilbudene dine.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="a3c5e-109">Med forbedrede fordelsplaner kan du opprette og behandle unike fordelsplaner og støtte komplekse fordelsgradtabeller og nestede lag.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="a3c5e-110">Du kan enkelt opprette fordelsprogrammer, bunter og automatiske registreringsregler for å få en enklere ansattopplevelse.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="a3c5e-111">Med fleksible kredittprogrammer kan du vurdere å støtte pensjon og andre levetidshendelser.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="a3c5e-112">Omfattende rettighetsregler sikrer at du gjør de riktige fordelene tilgjengelig for de riktige ansatte.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="a3c5e-113">Fordelsregistrering på nettet gir en enkel opplevelse for dine ansatte.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="a3c5e-114">Kvalifisert levetidsbehandling er integrert med selvbetjening for ansatte, og støtter også fremtidige livshendelser.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-114">Qualified life event processing integrates with Employee self service, and also supports future life events.</span></span>

<span data-ttu-id="a3c5e-115">Hvis du vil ha tilgang til demonstrasjonsdataene, må du distribuere sandkassemiljøet på nytt.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

<span data-ttu-id="a3c5e-116">Du kan gi direkte tilbakemelding eller rapport problemer til: D365BenefitsPreview@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-116">You can provide direct feedback or report issues to:  D365BenefitsPreview@microsoft.com.</span></span>

## <a name="benefits-management-known-issues"></a><span data-ttu-id="a3c5e-117">Kjente problemer med Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="a3c5e-117">Benefits management known issues</span></span>

### <a name="eligibility-processing"></a><span data-ttu-id="a3c5e-118">Rettighetsbehandling</span><span class="sxs-lookup"><span data-stu-id="a3c5e-118">Eligibility processing</span></span>

<span data-ttu-id="a3c5e-119">Ved pågående rettighet for fordeler som bruker et dekningsbeløp av typen 1–5 ganger lønn, prosent av lønn og flatt beløp, må du angi datoen for **Fordelsdetaljer** til **Medarbeiderens startdato** i **Ansettelseshistorikk**.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-119">When running eligibility for benefits that use a 1-5X Salary, % of Salary, and Flat Amount coverage amount, you must set the **Benefit details** date to the **Employee start date** in **Employment history**.</span></span> <span data-ttu-id="a3c5e-120">Du må også ta med **Arbeidstimer**, **Betalingsfrekvens** og **Årlig lønnsbeløp for fordeler**.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-120">You must also include **Hours worked**, **Payment frequency**, and **Annual benefits salary amount**.</span></span> <span data-ttu-id="a3c5e-121">Hvis arbeideren har fast kompensasjon, angir du **Arbeidstimer** og **Betalingsfrekvens**.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-121">If the worker has fixed compensation, enter **Hours worked** and **Payment frequency**.</span></span> <span data-ttu-id="a3c5e-122">Det årlige lønnsbeløpet blir beregnet.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-122">The annual salary amount will calculate.</span></span> <span data-ttu-id="a3c5e-123">Hvis den ansatte har fast lønn, trenger du ikke angi **Arbeidstimer**.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-123">If the employee is salaried, you don't need to enter **Hours worked**.</span></span> <span data-ttu-id="a3c5e-124">Det anbefales at du angir fast kompensasjon først når du oppretter nye arbeidere.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-124">We recommend that when creating new workers, enter fixed compensation first.</span></span> <span data-ttu-id="a3c5e-125">Du kan oppdatere posten med fordelsdetaljer ved å gå til **Arbeider > Arbeiderlogg > Ansettelsesdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-125">To update the benefit details record, navigate to **Worker > Worker history > Employment details**.</span></span> <span data-ttu-id="a3c5e-126">Juster datoen til arbeiderens startdato.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-126">Adjust the date to the worker's start date.</span></span>

### <a name="employee-self-service"></a><span data-ttu-id="a3c5e-127">Ansattselvbetjening</span><span class="sxs-lookup"><span data-stu-id="a3c5e-127">Employee self-service</span></span>

<span data-ttu-id="a3c5e-128">Den ansattes beløp beregnes ikke ved oppdatering av dekningsbeløpet for livsforsikring.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-128">Employee amount doesn't calculate when updating the coverage amount for life insurance.</span></span> <span data-ttu-id="a3c5e-129">Når en ansatt for eksempel blir tilbudt en livsforsikringsplan, kan de velge opptil $50 000 i dekning med en kost på $0,36 per $1000 dekning.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-129">For example, when an employee is offered a life insurance plan, they can select up to $50,000 in coverage at a cost of $.36 per $1,000 of coverage.</span></span>  <span data-ttu-id="a3c5e-130">Når den ansatte oppdaterer dekningsbeløpet, forblir den ansattes tilknyttede kostpris null.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-130">When the employee updates the coverage amount, the employee’s associated cost remains at zero.</span></span>

<span data-ttu-id="a3c5e-131">For en fordelsplan som bare tillater ett valg av denne plantypen, får brukeren en feilmelding hvis de prøver å frafalle en plan etter å ha valgt en plan.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-131">For a benefit plan that only allows a single selection of that plan type, the user receives an error if they attempt to waive a plan after selecting a plan.</span></span> <span data-ttu-id="a3c5e-132">En bruker velger for eksempel en medisinsk plan og setter den inn i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-132">For example, a user selects a medical plan and places it in their cart.</span></span> <span data-ttu-id="a3c5e-133">Brukeren velger deretter **Frafall** for en annen medisinsk plan.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-133">The user then selects **Waive** for another medical plan.</span></span> <span data-ttu-id="a3c5e-134">Brukeren vil motta en feil.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-134">The user will receive an error.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="a3c5e-135">Aktivere Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="a3c5e-135">Enable Benefits management</span></span>

<span data-ttu-id="a3c5e-136">Fordelsbehandling er en forhåndsversjon av en funksjon og er bare tilgjengelig i **sandkassemiljøer**.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-136">Benefits management is a preview feature, and is only available in **Sandbox** environments.</span></span> <span data-ttu-id="a3c5e-137">Disse artiklene beskriver hvordan du aktiverer forhåndsversjoner av funksjoner i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-137">These articles describe how to turn on preview features in Human Resources.</span></span> <span data-ttu-id="a3c5e-138">De forteller også hvilke eksisterende funksjoner i Human Resources som Fordelsbehandling erstatter, eller som deaktiveres når du aktiverer Fordelsbehandling.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-138">They also tell which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

- [<span data-ttu-id="a3c5e-139">Behandle funksjoner</span><span class="sxs-lookup"><span data-stu-id="a3c5e-139">Manage features</span></span>](hr-admin-manage-features.md)
- [<span data-ttu-id="a3c5e-140">Forhåndsversjon av funksjon: Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="a3c5e-140">Preview feature: Benefits management</span></span>](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a><span data-ttu-id="a3c5e-141">Konfigurere Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="a3c5e-141">Configure Benefits management</span></span>

<span data-ttu-id="a3c5e-142">Før du kan opprette fordelsplaner for de ansatte, må du konfigurere alternativer for planene.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-142">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="a3c5e-143">Se parametere i Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="a3c5e-143">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="a3c5e-144">Konfigurere rettighetsregler og -alternativer</span><span class="sxs-lookup"><span data-stu-id="a3c5e-144">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="a3c5e-145">Konfigurere alternativer for personlige kontaktrettigheter</span><span class="sxs-lookup"><span data-stu-id="a3c5e-145">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="a3c5e-146">Opprette dekningsalternativer</span><span class="sxs-lookup"><span data-stu-id="a3c5e-146">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="a3c5e-147">Definere betalingsfrekvenser</span><span class="sxs-lookup"><span data-stu-id="a3c5e-147">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="a3c5e-148">Konfigurere levetidshendelsestyper</span><span class="sxs-lookup"><span data-stu-id="a3c5e-148">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="a3c5e-149">Opprette plantyper</span><span class="sxs-lookup"><span data-stu-id="a3c5e-149">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="a3c5e-150">Definer årsakskoder</span><span class="sxs-lookup"><span data-stu-id="a3c5e-150">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="a3c5e-151">Definer lagkoder</span><span class="sxs-lookup"><span data-stu-id="a3c5e-151">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="a3c5e-152">Konfigurere satser</span><span class="sxs-lookup"><span data-stu-id="a3c5e-152">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="a3c5e-153">Konfigurere fradrag</span><span class="sxs-lookup"><span data-stu-id="a3c5e-153">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="a3c5e-154">Konfigurere ventedager</span><span class="sxs-lookup"><span data-stu-id="a3c5e-154">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="a3c5e-155">Konfigurere venteperioder</span><span class="sxs-lookup"><span data-stu-id="a3c5e-155">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="a3c5e-156">Definere avrundingsregler</span><span class="sxs-lookup"><span data-stu-id="a3c5e-156">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="a3c5e-157">Opprett ansettelseskategorier</span><span class="sxs-lookup"><span data-stu-id="a3c5e-157">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="a3c5e-158">Definere ansettelsestyper</span><span class="sxs-lookup"><span data-stu-id="a3c5e-158">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="a3c5e-159">Konfigurere ansattselvbetjening</span><span class="sxs-lookup"><span data-stu-id="a3c5e-159">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="a3c5e-160">Opprette fordelsplaner</span><span class="sxs-lookup"><span data-stu-id="a3c5e-160">Create benefit plans</span></span>

<span data-ttu-id="a3c5e-161">Disse artiklene viser hvordan du kan opprette fordelsplaner, inkludert bunter og fleksible kredittprogrammer.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-161">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="a3c5e-162">Definere fordelsplaner</span><span class="sxs-lookup"><span data-stu-id="a3c5e-162">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="a3c5e-163">Opprette fordelsplaner for ansatte</span><span class="sxs-lookup"><span data-stu-id="a3c5e-163">Create worker benefit plans</span></span>](hr-benefits-plans-worker.md)
- [<span data-ttu-id="a3c5e-164">Definere fleksible kredittprogrammer</span><span class="sxs-lookup"><span data-stu-id="a3c5e-164">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)
- [<span data-ttu-id="a3c5e-165">Konfigurere fremtidige levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="a3c5e-165">Configure future life events</span></span>](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="a3c5e-166">Behandle fordelsplaner</span><span class="sxs-lookup"><span data-stu-id="a3c5e-166">Process benefit plans</span></span>

<span data-ttu-id="a3c5e-167">Du må behandle noen av endringene for å aktivere dem.</span><span class="sxs-lookup"><span data-stu-id="a3c5e-167">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="a3c5e-168">Fordelsregistreringsrettighet</span><span class="sxs-lookup"><span data-stu-id="a3c5e-168">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="a3c5e-169">Behandle levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="a3c5e-169">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="a3c5e-170">Behandle endringer i levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="a3c5e-170">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="a3c5e-171">Behandle rettighet for levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="a3c5e-171">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="a3c5e-172">Behandle satsendringer</span><span class="sxs-lookup"><span data-stu-id="a3c5e-172">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

