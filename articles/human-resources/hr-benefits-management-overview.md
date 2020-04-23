---
title: Oversikt over fordelsbehandling
description: Oversikt over funksjonen Fordelsbehandling i Dynamics 365 Human Resources. Gi de ansatte utvidede fordelsalternativer med en brukervennlig Internett-opplevelse.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: 91a4425b4f020f90843bb3b0b280b7ee28463670
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230160"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="d4b25-104">Oversikt over Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="d4b25-104">Benefits management overview</span></span>

<span data-ttu-id="d4b25-105">For å være konkurransedyktig må du tilby et stort utvalg av fordeler for å tiltrekke deg og beholde de beste ansatte.</span><span class="sxs-lookup"><span data-stu-id="d4b25-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="d4b25-106">I tillegg til standardfordeler som dekning av lege- og tannlegeutgifter ønsker du kanskje også å tilby utvidede tjenester, for eksempel starthjelp, rekreasjonsprogrammer og dekning av klær.</span><span class="sxs-lookup"><span data-stu-id="d4b25-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="d4b25-107">Med Fordelsbehandling i Microsoft Dynamics 365 Human Resources får du en fleksibel løsning som støtter en rekke ulike fordelsalternativer.</span><span class="sxs-lookup"><span data-stu-id="d4b25-107">Benefits management in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="d4b25-108">Human Resources inneholder også en brukervennlig ansattopplevelse som viser tilbudene dine.</span><span class="sxs-lookup"><span data-stu-id="d4b25-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="d4b25-109">Med forbedrede fordelsplaner kan du opprette og behandle unike fordelsplaner og støtte komplekse fordelsgradtabeller og nestede lag.</span><span class="sxs-lookup"><span data-stu-id="d4b25-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="d4b25-110">Du kan enkelt opprette fordelsprogrammer, bunter og automatiske registreringsregler for å få en enklere ansattopplevelse.</span><span class="sxs-lookup"><span data-stu-id="d4b25-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="d4b25-111">Med fleksible kredittprogrammer kan du vurdere å støtte pensjon og andre levetidshendelser.</span><span class="sxs-lookup"><span data-stu-id="d4b25-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="d4b25-112">Omfattende rettighetsregler sikrer at du gjør de riktige fordelene tilgjengelig for de riktige ansatte.</span><span class="sxs-lookup"><span data-stu-id="d4b25-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="d4b25-113">Fordelsregistrering på nettet gir en enkel opplevelse for dine ansatte.</span><span class="sxs-lookup"><span data-stu-id="d4b25-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="d4b25-114">Behandling av kvalifisert levetidshendelse støtter fremtidige levetidshendelser.</span><span class="sxs-lookup"><span data-stu-id="d4b25-114">Qualified life event processing supports future life events.</span></span>

<span data-ttu-id="d4b25-115">Hvis du vil ha tilgang til demonstrasjonsdataene, må du distribuere sandkassemiljøet på nytt.</span><span class="sxs-lookup"><span data-stu-id="d4b25-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

## <a name="benefits-management-known-issues"></a><span data-ttu-id="d4b25-116">Kjente problemer med Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="d4b25-116">Benefits management known issues</span></span>

### <a name="flex-credit-programs"></a><span data-ttu-id="d4b25-117">Fleksikredittprogrammer</span><span class="sxs-lookup"><span data-stu-id="d4b25-117">Flex credit programs</span></span>

<span data-ttu-id="d4b25-118">Den totale kredittverdien som er definert for et fleksibelt kredittprogram, vises ikke i skjemaet **Fordelsplaner for arbeider**.</span><span class="sxs-lookup"><span data-stu-id="d4b25-118">The total credit value defined for a flex credit program doesn't display in the **Worker benefit plans** form.</span></span> <span data-ttu-id="d4b25-119">Hvis du angir at et fleksibelt kredittprogram skal ha fordelingsregelen **Ingen**, får du også en feil i skjemaet **Fordelsplan for arbeider** når du velger og bekrefter planer.</span><span class="sxs-lookup"><span data-stu-id="d4b25-119">Also, if you set a flex credit program to have a proration rule of **None**, you get an error in the **Worker benefit plan** form when selecting and confirming plans.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="d4b25-120">Aktivere Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="d4b25-120">Enable Benefits management</span></span>

<span data-ttu-id="d4b25-121">Denne artikkelen beskriver hvordan du aktiverer funksjoner i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d4b25-121">This article describes how to turn on features in Human Resources.</span></span> <span data-ttu-id="d4b25-122">Den forteller også hvilke eksisterende funksjoner i Human Resources som Fordelsbehandling erstatter, eller som deaktiveres når du aktiverer Fordelsbehandling.</span><span class="sxs-lookup"><span data-stu-id="d4b25-122">It also tells which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4b25-123">Du kan ikke deaktivere Fordelsbehandling i et **produksjonsmiljø** etter at du har aktivert det.</span><span class="sxs-lookup"><span data-stu-id="d4b25-123">After you enable Benefits management in a **Production** environment, you can't disable it.</span></span> <span data-ttu-id="d4b25-124">Vi anbefaler at du aktiverer og tester Fordelsbehandling i et **Sandkasse**-miljø før du aktiverer det i et **Produksjon**-miljø.</span><span class="sxs-lookup"><span data-stu-id="d4b25-124">We recommend enabling and testing Benefits management in a **Sandbox** environment before enabling it in a **Production** environment.</span></span> <span data-ttu-id="d4b25-125">Det er store forskjeller mellom den eldre Fordel-funksjonaliteten og den nye Fordelsbehandling-funksjonaliteten, som krever ekstra oppsett, og som bør testes før den blir satt i produksjon.</span><span class="sxs-lookup"><span data-stu-id="d4b25-125">There are significant differences between the legacy Benefit functionality and new Benefits management functionality that require additional setup and should be tested prior to being placed into production.</span></span>

- [<span data-ttu-id="d4b25-126">Behandle funksjoner</span><span class="sxs-lookup"><span data-stu-id="d4b25-126">Manage features</span></span>](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a><span data-ttu-id="d4b25-127">Konfigurere informasjon om ansatte</span><span class="sxs-lookup"><span data-stu-id="d4b25-127">Configure employee information</span></span>

<span data-ttu-id="d4b25-128">Før du kan registrere ansatte i fordeler, må du angi nødvendig informasjon.</span><span class="sxs-lookup"><span data-stu-id="d4b25-128">Before you can enroll employees in benefits, you must provide required information.</span></span> <span data-ttu-id="d4b25-129">Du må registrere en ansatt i en **fast kompensasjonsplan** på startdatoen, og du må velge en **frekvens for fordelsbetaling** i **ansettelsesdetaljene** i **Arbeider**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="d4b25-129">You must enroll an employee in a **Fixed compensation plan** on their start date, and you must select a **Benefit pay frequency** in **Employment details** on the **Worker** form.</span></span>

<span data-ttu-id="d4b25-130">Når du oppretter en fordelsplan som bruker satser som er basert på kjønn eller alder, må du angi en fødselsdato og et kjønn for den ansatte for å beregne fordelskostnaden.</span><span class="sxs-lookup"><span data-stu-id="d4b25-130">When you create a benefit plan that uses rates that are based on gender or age, you must enter a birth date and gender for the employee to calculate the benefit cost.</span></span>

## <a name="configure-benefits-management"></a><span data-ttu-id="d4b25-131">Konfigurere fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="d4b25-131">Configure Benefits management</span></span>

<span data-ttu-id="d4b25-132">Før du kan opprette fordelsplaner for de ansatte, må du konfigurere alternativer for planene.</span><span class="sxs-lookup"><span data-stu-id="d4b25-132">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="d4b25-133">Se parametere i Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="d4b25-133">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="d4b25-134">Konfigurere rettighetsregler og -alternativer</span><span class="sxs-lookup"><span data-stu-id="d4b25-134">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="d4b25-135">Konfigurere alternativer for personlige kontaktrettigheter</span><span class="sxs-lookup"><span data-stu-id="d4b25-135">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="d4b25-136">Opprette dekningsalternativer</span><span class="sxs-lookup"><span data-stu-id="d4b25-136">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="d4b25-137">Definere betalingshyppigheter</span><span class="sxs-lookup"><span data-stu-id="d4b25-137">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="d4b25-138">Konfigurere hendelsestyper for levetid</span><span class="sxs-lookup"><span data-stu-id="d4b25-138">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="d4b25-139">Opprette plantyper</span><span class="sxs-lookup"><span data-stu-id="d4b25-139">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="d4b25-140">Definer årsakskoder</span><span class="sxs-lookup"><span data-stu-id="d4b25-140">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="d4b25-141">Definere lagkoder</span><span class="sxs-lookup"><span data-stu-id="d4b25-141">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="d4b25-142">Konfigurere satser</span><span class="sxs-lookup"><span data-stu-id="d4b25-142">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="d4b25-143">Konfigurere fradrag</span><span class="sxs-lookup"><span data-stu-id="d4b25-143">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="d4b25-144">Konfigurere ventedager</span><span class="sxs-lookup"><span data-stu-id="d4b25-144">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="d4b25-145">Konfigurere venteperioder</span><span class="sxs-lookup"><span data-stu-id="d4b25-145">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="d4b25-146">Definere avrundingsregler</span><span class="sxs-lookup"><span data-stu-id="d4b25-146">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="d4b25-147">Opprette ansettelseskategorier</span><span class="sxs-lookup"><span data-stu-id="d4b25-147">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="d4b25-148">Definere ansettelsestyper</span><span class="sxs-lookup"><span data-stu-id="d4b25-148">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="d4b25-149">Konfigurere ansattselvbetjening</span><span class="sxs-lookup"><span data-stu-id="d4b25-149">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="d4b25-150">Opprette fordelsplaner</span><span class="sxs-lookup"><span data-stu-id="d4b25-150">Create benefit plans</span></span>

<span data-ttu-id="d4b25-151">Disse artiklene viser hvordan du kan opprette fordelsplaner, inkludert bunter og fleksible kredittprogrammer.</span><span class="sxs-lookup"><span data-stu-id="d4b25-151">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="d4b25-152">Definere fordelsplaner</span><span class="sxs-lookup"><span data-stu-id="d4b25-152">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="d4b25-153">Definere fleksible kredittprogrammer</span><span class="sxs-lookup"><span data-stu-id="d4b25-153">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="d4b25-154">Behandle fordelsplaner</span><span class="sxs-lookup"><span data-stu-id="d4b25-154">Process benefit plans</span></span>

<span data-ttu-id="d4b25-155">Du må behandle noen av endringene for å aktivere dem.</span><span class="sxs-lookup"><span data-stu-id="d4b25-155">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="d4b25-156">Fordelsregistreringsrettighet</span><span class="sxs-lookup"><span data-stu-id="d4b25-156">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="d4b25-157">Behandle levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="d4b25-157">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="d4b25-158">Behandle endringer i levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="d4b25-158">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="d4b25-159">Behandle rettighet for levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="d4b25-159">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="d4b25-160">Behandle satsendringer</span><span class="sxs-lookup"><span data-stu-id="d4b25-160">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

