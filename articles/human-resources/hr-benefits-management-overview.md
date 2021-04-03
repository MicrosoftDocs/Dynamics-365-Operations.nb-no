---
title: Oversikt over fordelsbehandling
description: Oversikt over funksjonen Fordelsbehandling i Dynamics 365 Human Resources. Gi de ansatte utvidede fordelsalternativer med en brukervennlig Internett-opplevelse.
author: andreabichsel
manager: tfehr
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba6623102431eb45bf5d0c96b6583615663d1081
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464332"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="5b25b-104">Oversikt over Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="5b25b-104">Benefits management overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5b25b-105">For å være konkurransedyktig må du tilby et stort utvalg av fordeler for å tiltrekke deg og beholde de beste ansatte.</span><span class="sxs-lookup"><span data-stu-id="5b25b-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="5b25b-106">I tillegg til standardfordeler som dekning av lege- og tannlegeutgifter ønsker du kanskje også å tilby utvidede tjenester, for eksempel starthjelp, rekreasjonsprogrammer og dekning av klær.</span><span class="sxs-lookup"><span data-stu-id="5b25b-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="5b25b-107">Med Fordelsbehandling i Microsoft Dynamics 365 Human Resources får du en fleksibel løsning som støtter en rekke ulike fordelsalternativer.</span><span class="sxs-lookup"><span data-stu-id="5b25b-107">Benefits management in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="5b25b-108">Human Resources inneholder også en brukervennlig ansattopplevelse som viser tilbudene dine.</span><span class="sxs-lookup"><span data-stu-id="5b25b-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="5b25b-109">Med forbedrede fordelsplaner kan du opprette og behandle unike fordelsplaner og støtte komplekse fordelsgradtabeller og nestede lag.</span><span class="sxs-lookup"><span data-stu-id="5b25b-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="5b25b-110">Du kan enkelt opprette fordelsprogrammer, bunter og automatiske registreringsregler for å få en enklere ansattopplevelse.</span><span class="sxs-lookup"><span data-stu-id="5b25b-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="5b25b-111">Med fleksible kredittprogrammer kan du vurdere å støtte pensjon og andre levetidshendelser.</span><span class="sxs-lookup"><span data-stu-id="5b25b-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="5b25b-112">Omfattende rettighetsregler sikrer at du gjør de riktige fordelene tilgjengelig for de riktige ansatte.</span><span class="sxs-lookup"><span data-stu-id="5b25b-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="5b25b-113">Fordelsregistrering på nettet gir en enkel opplevelse for dine ansatte.</span><span class="sxs-lookup"><span data-stu-id="5b25b-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="5b25b-114">Behandling av kvalifisert levetidshendelse støtter fremtidige levetidshendelser.</span><span class="sxs-lookup"><span data-stu-id="5b25b-114">Qualified life event processing supports future life events.</span></span>

<span data-ttu-id="5b25b-115">Hvis du vil ha tilgang til demonstrasjonsdataene, må du distribuere sandkassemiljøet på nytt.</span><span class="sxs-lookup"><span data-stu-id="5b25b-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="5b25b-116">Aktivere Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="5b25b-116">Enable Benefits management</span></span>

<span data-ttu-id="5b25b-117">Dette emnet beskriver hvordan du aktiverer funksjoner i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5b25b-117">This topic describes how to turn on features in Human Resources.</span></span> <span data-ttu-id="5b25b-118">Den forteller også hvilke eksisterende funksjoner i Human Resources som Fordelsbehandling erstatter, eller som deaktiveres når du aktiverer Fordelsbehandling.</span><span class="sxs-lookup"><span data-stu-id="5b25b-118">It also tells which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b25b-119">Du kan ikke deaktivere Fordelsbehandling i et **produksjonsmiljø** etter at du har aktivert det.</span><span class="sxs-lookup"><span data-stu-id="5b25b-119">After you enable Benefits management in a **Production** environment, you can't disable it.</span></span> <span data-ttu-id="5b25b-120">Det anbefales at du aktiverer og tester Fordelsbehandling i et **Sandkasse**-miljø før du aktiverer det i et **Produksjon**-miljø.</span><span class="sxs-lookup"><span data-stu-id="5b25b-120">We recommend enabling and testing Benefits management in a **Sandbox** environment before enabling it in a **Production** environment.</span></span> <span data-ttu-id="5b25b-121">Det er store forskjeller mellom den eldre Fordel-funksjonaliteten og den nye Fordelsbehandling-funksjonaliteten, som krever ekstra oppsett, og som bør testes før den blir satt i produksjon.</span><span class="sxs-lookup"><span data-stu-id="5b25b-121">There are significant differences between the legacy Benefit functionality and new Benefits management functionality that require additional setup and should be tested prior to being placed into production.</span></span>

- [<span data-ttu-id="5b25b-122">Behandle funksjoner</span><span class="sxs-lookup"><span data-stu-id="5b25b-122">Manage features</span></span>](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a><span data-ttu-id="5b25b-123">Konfigurere informasjon om ansatte</span><span class="sxs-lookup"><span data-stu-id="5b25b-123">Configure employee information</span></span>

<span data-ttu-id="5b25b-124">Før du kan registrere ansatte i fordeler, må du angi nødvendig informasjon.</span><span class="sxs-lookup"><span data-stu-id="5b25b-124">Before you can enroll employees in benefits, you must provide required information.</span></span> <span data-ttu-id="5b25b-125">Du må registrere en ansatt i en **fast kompensasjonsplan** på startdatoen, og du må velge en **frekvens for fordelsbetaling** i **ansettelsesdetaljene** i **Arbeider**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="5b25b-125">You must enroll an employee in a **Fixed compensation plan** on their start date, and you must select a **Benefit pay frequency** in **Employment details** on the **Worker** form.</span></span>

<span data-ttu-id="5b25b-126">Hvis du har en ansatt som får tilleggskompensasjon som provisjon, kan du legge til et **årlig lønnsbeløp for fordeler** fra ansattposten.</span><span class="sxs-lookup"><span data-stu-id="5b25b-126">If you have an employee who receives supplemental compensation like commissions, you can add a **Benefits annual salary** amount from the employee record.</span></span> <span data-ttu-id="5b25b-127">Human Resources bruker **årlig lønnsbeløp for fordeler** når de fastsetter dekningsbeløp i stedet for det årlige beløpet for fast kompensasjonen.</span><span class="sxs-lookup"><span data-stu-id="5b25b-127">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> <span data-ttu-id="5b25b-128">**Årlig lønnsbeløp for fordeler** må være gyldig per den ansattes startdato eller starte av fordelsperioden, avhengig av hva som er sist.</span><span class="sxs-lookup"><span data-stu-id="5b25b-128">The **Benefits annual salary** must be valid as of the employee’s start date or the beginning of the benefit period, whichever is latest.</span></span> <span data-ttu-id="5b25b-129">Hvis både fast kompensasjon og årlig lønnsbeløp for fordeler registreres for en ansatt, blir årlig lønnsbeløp for fordeler brukt til å bestemme dekningsbeløp.</span><span class="sxs-lookup"><span data-stu-id="5b25b-129">If both a fixed compensation and benefits annual salary amount is recorded for an employee, the benefits annual salary will be used in determining coverage amounts.</span></span>

<span data-ttu-id="5b25b-130">Når du oppretter en fordelsplan som bruker satser som er basert på kjønn eller alder, må du angi en fødselsdato og et kjønn for den ansatte for å beregne fordelskostnaden.</span><span class="sxs-lookup"><span data-stu-id="5b25b-130">When you create a benefit plan that uses rates that are based on gender or age, you must enter a birth date and gender for the employee to calculate the benefit cost.</span></span>

## <a name="configure-benefits-management"></a><span data-ttu-id="5b25b-131">Konfigurere fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="5b25b-131">Configure Benefits management</span></span>

<span data-ttu-id="5b25b-132">Før du kan opprette fordelsplaner for de ansatte, må du konfigurere alternativer for planene.</span><span class="sxs-lookup"><span data-stu-id="5b25b-132">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="5b25b-133">Se parametere i Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="5b25b-133">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="5b25b-134">Konfigurere rettighetsregler og -alternativer</span><span class="sxs-lookup"><span data-stu-id="5b25b-134">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="5b25b-135">Konfigurere alternativer for personlige kontaktrettigheter</span><span class="sxs-lookup"><span data-stu-id="5b25b-135">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="5b25b-136">Opprette dekningsalternativer</span><span class="sxs-lookup"><span data-stu-id="5b25b-136">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="5b25b-137">Definere betalingshyppigheter</span><span class="sxs-lookup"><span data-stu-id="5b25b-137">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="5b25b-138">Konfigurere hendelsestyper for levetid</span><span class="sxs-lookup"><span data-stu-id="5b25b-138">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="5b25b-139">Opprette plantyper</span><span class="sxs-lookup"><span data-stu-id="5b25b-139">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="5b25b-140">Definer årsakskoder</span><span class="sxs-lookup"><span data-stu-id="5b25b-140">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="5b25b-141">Definere lagkoder</span><span class="sxs-lookup"><span data-stu-id="5b25b-141">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="5b25b-142">Konfigurere satser</span><span class="sxs-lookup"><span data-stu-id="5b25b-142">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="5b25b-143">Konfigurere fradrag</span><span class="sxs-lookup"><span data-stu-id="5b25b-143">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="5b25b-144">Konfigurere ventedager</span><span class="sxs-lookup"><span data-stu-id="5b25b-144">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="5b25b-145">Konfigurere venteperioder</span><span class="sxs-lookup"><span data-stu-id="5b25b-145">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="5b25b-146">Definere avrundingsregler</span><span class="sxs-lookup"><span data-stu-id="5b25b-146">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="5b25b-147">Opprette ansettelseskategorier</span><span class="sxs-lookup"><span data-stu-id="5b25b-147">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="5b25b-148">Definere ansettelsestyper</span><span class="sxs-lookup"><span data-stu-id="5b25b-148">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="5b25b-149">Konfigurere ansattselvbetjening</span><span class="sxs-lookup"><span data-stu-id="5b25b-149">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="5b25b-150">Opprette fordelsplaner</span><span class="sxs-lookup"><span data-stu-id="5b25b-150">Create benefit plans</span></span>

<span data-ttu-id="5b25b-151">Disse artiklene viser hvordan du kan opprette fordelsplaner, inkludert bunter og fleksible kredittprogrammer.</span><span class="sxs-lookup"><span data-stu-id="5b25b-151">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="5b25b-152">Definere fordelsplaner</span><span class="sxs-lookup"><span data-stu-id="5b25b-152">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="5b25b-153">Definere fleksible kredittprogrammer</span><span class="sxs-lookup"><span data-stu-id="5b25b-153">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="5b25b-154">Behandle fordelsplaner</span><span class="sxs-lookup"><span data-stu-id="5b25b-154">Process benefit plans</span></span>

<span data-ttu-id="5b25b-155">Du må behandle noen av endringene for å aktivere dem.</span><span class="sxs-lookup"><span data-stu-id="5b25b-155">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="5b25b-156">Fordelsregistreringsrettighet</span><span class="sxs-lookup"><span data-stu-id="5b25b-156">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="5b25b-157">Behandle levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="5b25b-157">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="5b25b-158">Behandle endringer i levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="5b25b-158">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="5b25b-159">Behandle rettighet for levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="5b25b-159">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="5b25b-160">Behandle satsendringer</span><span class="sxs-lookup"><span data-stu-id="5b25b-160">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]