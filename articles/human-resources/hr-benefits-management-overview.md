---
title: Oversikt over fordelsbehandling
description: Oversikt over funksjonen Fordelsbehandling i Dynamics 365 Human Resources. Gi de ansatte utvidede fordelsalternativer med en brukervennlig Internett-opplevelse.
author: andreabichsel
manager: AnnBe
ms.date: 07/16/2020
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
ms.openlocfilehash: 1043fb18c33e5ec0cde13008b168fd317c7c7be6
ms.sourcegitcommit: 9dc5c7dd5877cc6e7cd0059d173bcd8052ba13bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/16/2020
ms.locfileid: "3599386"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="ba496-104">Oversikt over Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="ba496-104">Benefits management overview</span></span>

<span data-ttu-id="ba496-105">For å være konkurransedyktig må du tilby et stort utvalg av fordeler for å tiltrekke deg og beholde de beste ansatte.</span><span class="sxs-lookup"><span data-stu-id="ba496-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="ba496-106">I tillegg til standardfordeler som dekning av lege- og tannlegeutgifter ønsker du kanskje også å tilby utvidede tjenester, for eksempel starthjelp, rekreasjonsprogrammer og dekning av klær.</span><span class="sxs-lookup"><span data-stu-id="ba496-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="ba496-107">Med Fordelsbehandling i Microsoft Dynamics 365 Human Resources får du en fleksibel løsning som støtter en rekke ulike fordelsalternativer.</span><span class="sxs-lookup"><span data-stu-id="ba496-107">Benefits management in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="ba496-108">Human Resources inneholder også en brukervennlig ansattopplevelse som viser tilbudene dine.</span><span class="sxs-lookup"><span data-stu-id="ba496-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="ba496-109">Med forbedrede fordelsplaner kan du opprette og behandle unike fordelsplaner og støtte komplekse fordelsgradtabeller og nestede lag.</span><span class="sxs-lookup"><span data-stu-id="ba496-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="ba496-110">Du kan enkelt opprette fordelsprogrammer, bunter og automatiske registreringsregler for å få en enklere ansattopplevelse.</span><span class="sxs-lookup"><span data-stu-id="ba496-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="ba496-111">Med fleksible kredittprogrammer kan du vurdere å støtte pensjon og andre levetidshendelser.</span><span class="sxs-lookup"><span data-stu-id="ba496-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="ba496-112">Omfattende rettighetsregler sikrer at du gjør de riktige fordelene tilgjengelig for de riktige ansatte.</span><span class="sxs-lookup"><span data-stu-id="ba496-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="ba496-113">Fordelsregistrering på nettet gir en enkel opplevelse for dine ansatte.</span><span class="sxs-lookup"><span data-stu-id="ba496-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="ba496-114">Behandling av kvalifisert levetidshendelse støtter fremtidige levetidshendelser.</span><span class="sxs-lookup"><span data-stu-id="ba496-114">Qualified life event processing supports future life events.</span></span>

<span data-ttu-id="ba496-115">Hvis du vil ha tilgang til demonstrasjonsdataene, må du distribuere sandkassemiljøet på nytt.</span><span class="sxs-lookup"><span data-stu-id="ba496-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

## <a name="benefits-management-known-issues"></a><span data-ttu-id="ba496-116">Kjente problemer med Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="ba496-116">Benefits management known issues</span></span>

### <a name="flex-credit-programs"></a><span data-ttu-id="ba496-117">Fleksikredittprogrammer</span><span class="sxs-lookup"><span data-stu-id="ba496-117">Flex credit programs</span></span>

<span data-ttu-id="ba496-118">Den totale kredittverdien som er definert for et fleksibelt kredittprogram, vises ikke i skjemaet **Fordelsplaner for arbeider**.</span><span class="sxs-lookup"><span data-stu-id="ba496-118">The total credit value defined for a flex credit program doesn't display in the **Worker benefit plans** form.</span></span> <span data-ttu-id="ba496-119">Hvis du angir at et fleksibelt kredittprogram skal ha fordelingsregelen **Ingen**, får du også en feil i skjemaet **Fordelsplan for arbeider** når du velger og bekrefter planer.</span><span class="sxs-lookup"><span data-stu-id="ba496-119">Also, if you set a flex credit program to have a proration rule of **None**, you get an error in the **Worker benefit plan** form when selecting and confirming plans.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="ba496-120">Aktivere Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="ba496-120">Enable Benefits management</span></span>

<span data-ttu-id="ba496-121">Denne artikkelen beskriver hvordan du aktiverer funksjoner i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ba496-121">This article describes how to turn on features in Human Resources.</span></span> <span data-ttu-id="ba496-122">Den forteller også hvilke eksisterende funksjoner i Human Resources som Fordelsbehandling erstatter, eller som deaktiveres når du aktiverer Fordelsbehandling.</span><span class="sxs-lookup"><span data-stu-id="ba496-122">It also tells which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ba496-123">Du kan ikke deaktivere Fordelsbehandling i et **produksjonsmiljø** etter at du har aktivert det.</span><span class="sxs-lookup"><span data-stu-id="ba496-123">After you enable Benefits management in a **Production** environment, you can't disable it.</span></span> <span data-ttu-id="ba496-124">Vi anbefaler at du aktiverer og tester Fordelsbehandling i et **Sandkasse**-miljø før du aktiverer det i et **Produksjon**-miljø.</span><span class="sxs-lookup"><span data-stu-id="ba496-124">We recommend enabling and testing Benefits management in a **Sandbox** environment before enabling it in a **Production** environment.</span></span> <span data-ttu-id="ba496-125">Det er store forskjeller mellom den eldre Fordel-funksjonaliteten og den nye Fordelsbehandling-funksjonaliteten, som krever ekstra oppsett, og som bør testes før den blir satt i produksjon.</span><span class="sxs-lookup"><span data-stu-id="ba496-125">There are significant differences between the legacy Benefit functionality and new Benefits management functionality that require additional setup and should be tested prior to being placed into production.</span></span>

- [<span data-ttu-id="ba496-126">Behandle funksjoner</span><span class="sxs-lookup"><span data-stu-id="ba496-126">Manage features</span></span>](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a><span data-ttu-id="ba496-127">Konfigurere informasjon om ansatte</span><span class="sxs-lookup"><span data-stu-id="ba496-127">Configure employee information</span></span>

<span data-ttu-id="ba496-128">Før du kan registrere ansatte i fordeler, må du angi nødvendig informasjon.</span><span class="sxs-lookup"><span data-stu-id="ba496-128">Before you can enroll employees in benefits, you must provide required information.</span></span> <span data-ttu-id="ba496-129">Du må registrere en ansatt i en **fast kompensasjonsplan** på startdatoen, og du må velge en **frekvens for fordelsbetaling** i **ansettelsesdetaljene** i **Arbeider**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="ba496-129">You must enroll an employee in a **Fixed compensation plan** on their start date, and you must select a **Benefit pay frequency** in **Employment details** on the **Worker** form.</span></span>

<span data-ttu-id="ba496-130">Hvis du har en ansatt som får tilleggskompensasjon som provisjon, kan du legge til et **årlig lønnsbeløp for fordeler** fra ansattposten.</span><span class="sxs-lookup"><span data-stu-id="ba496-130">If you have an employee who receives supplemental compensation like commissions, you can add a **Benefits annual salary** amount from the employee record.</span></span> <span data-ttu-id="ba496-131">Human Resources bruker **årlig lønnsbeløp for fordeler** når de fastsetter dekningsbeløp i stedet for det årlige beløpet for fast kompensasjonen.</span><span class="sxs-lookup"><span data-stu-id="ba496-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> <span data-ttu-id="ba496-132">**Årlig lønnsbeløp for fordeler** må være gyldig per den ansattes startdato eller starte av fordelsperioden, avhengig av hva som er sist.</span><span class="sxs-lookup"><span data-stu-id="ba496-132">The **Benefits annual salary** must be valid as of the employee’s start date or the beginning of the benefit period, whichever is latest.</span></span> <span data-ttu-id="ba496-133">Hvis både fast kompensasjon og årlig lønnsbeløp for fordeler registreres for en ansatt, blir årlig lønnsbeløp for fordeler brukt til å bestemme dekningsbeløp.</span><span class="sxs-lookup"><span data-stu-id="ba496-133">If both a fixed compensation and benefits annual salary amount is recorded for an employee, the benefits annual salary will be used in determining coverage amounts.</span></span>

<span data-ttu-id="ba496-134">Når du oppretter en fordelsplan som bruker satser som er basert på kjønn eller alder, må du angi en fødselsdato og et kjønn for den ansatte for å beregne fordelskostnaden.</span><span class="sxs-lookup"><span data-stu-id="ba496-134">When you create a benefit plan that uses rates that are based on gender or age, you must enter a birth date and gender for the employee to calculate the benefit cost.</span></span>

## <a name="configure-benefits-management"></a><span data-ttu-id="ba496-135">Konfigurere fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="ba496-135">Configure Benefits management</span></span>

<span data-ttu-id="ba496-136">Før du kan opprette fordelsplaner for de ansatte, må du konfigurere alternativer for planene.</span><span class="sxs-lookup"><span data-stu-id="ba496-136">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="ba496-137">Se parametere i Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="ba496-137">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="ba496-138">Konfigurere rettighetsregler og -alternativer</span><span class="sxs-lookup"><span data-stu-id="ba496-138">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="ba496-139">Konfigurere alternativer for personlige kontaktrettigheter</span><span class="sxs-lookup"><span data-stu-id="ba496-139">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="ba496-140">Opprette dekningsalternativer</span><span class="sxs-lookup"><span data-stu-id="ba496-140">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="ba496-141">Definere betalingshyppigheter</span><span class="sxs-lookup"><span data-stu-id="ba496-141">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="ba496-142">Konfigurere hendelsestyper for levetid</span><span class="sxs-lookup"><span data-stu-id="ba496-142">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="ba496-143">Opprette plantyper</span><span class="sxs-lookup"><span data-stu-id="ba496-143">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="ba496-144">Definer årsakskoder</span><span class="sxs-lookup"><span data-stu-id="ba496-144">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="ba496-145">Definere lagkoder</span><span class="sxs-lookup"><span data-stu-id="ba496-145">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="ba496-146">Konfigurere satser</span><span class="sxs-lookup"><span data-stu-id="ba496-146">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="ba496-147">Konfigurere fradrag</span><span class="sxs-lookup"><span data-stu-id="ba496-147">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="ba496-148">Konfigurere ventedager</span><span class="sxs-lookup"><span data-stu-id="ba496-148">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="ba496-149">Konfigurere venteperioder</span><span class="sxs-lookup"><span data-stu-id="ba496-149">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="ba496-150">Definere avrundingsregler</span><span class="sxs-lookup"><span data-stu-id="ba496-150">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="ba496-151">Opprette ansettelseskategorier</span><span class="sxs-lookup"><span data-stu-id="ba496-151">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="ba496-152">Definere ansettelsestyper</span><span class="sxs-lookup"><span data-stu-id="ba496-152">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="ba496-153">Konfigurere ansattselvbetjening</span><span class="sxs-lookup"><span data-stu-id="ba496-153">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="ba496-154">Opprette fordelsplaner</span><span class="sxs-lookup"><span data-stu-id="ba496-154">Create benefit plans</span></span>

<span data-ttu-id="ba496-155">Disse artiklene viser hvordan du kan opprette fordelsplaner, inkludert bunter og fleksible kredittprogrammer.</span><span class="sxs-lookup"><span data-stu-id="ba496-155">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="ba496-156">Definere fordelsplaner</span><span class="sxs-lookup"><span data-stu-id="ba496-156">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="ba496-157">Definere fleksible kredittprogrammer</span><span class="sxs-lookup"><span data-stu-id="ba496-157">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="ba496-158">Behandle fordelsplaner</span><span class="sxs-lookup"><span data-stu-id="ba496-158">Process benefit plans</span></span>

<span data-ttu-id="ba496-159">Du må behandle noen av endringene for å aktivere dem.</span><span class="sxs-lookup"><span data-stu-id="ba496-159">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="ba496-160">Fordelsregistreringsrettighet</span><span class="sxs-lookup"><span data-stu-id="ba496-160">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="ba496-161">Behandle levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="ba496-161">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="ba496-162">Behandle endringer i levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="ba496-162">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="ba496-163">Behandle rettighet for levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="ba496-163">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="ba496-164">Behandle satsendringer</span><span class="sxs-lookup"><span data-stu-id="ba496-164">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

