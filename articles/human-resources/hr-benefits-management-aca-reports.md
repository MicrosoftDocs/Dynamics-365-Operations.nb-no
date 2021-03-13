---
title: Generere rapporter om Affordable Care Act i fordelsbehandling
description: Dette emnet beskriver hvordan fordelsbehandling hjelper deg med å spore informasjon som er rapportert på skjema 1095-B og skjema 1095-C for employer mandate Affordable Care Act (ACA).
author: andreabichsel
manager: tfehr
ms.date: 12/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 2e4b250f4a059719067a9e19bbf3ce4aecc9bb1f
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113748"
---
# <a name="generate-aca-reports-in-benefits-management"></a><span data-ttu-id="dcc6b-103">Generere ACA-rapporter i fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="dcc6b-103">Generate ACA reports in Benefits management</span></span>

<span data-ttu-id="dcc6b-104">Fordelsbehandling hjelper deg med å spore informasjon som er rapportert på skjema 1095-B og skjema 1095-C for employer mandate Affordable Care Act (ACA).</span><span class="sxs-lookup"><span data-stu-id="dcc6b-104">Benefits management helps you track information that is reported on Form 1095-B and Form 1095-C for the Affordable Care Act (ACA) employer mandate.</span></span> <span data-ttu-id="dcc6b-105">I likhet med ACA-rapporteringsfunksjonene på det gamle arbeidsområdet **Fordeler**, gjelder denne funksjonaliteten bare for juridiske enheter i USA.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-105">Like the ACA reporting capability in the old **Benefits** workspace, this functionality applies only to legal entities in the United States.</span></span>

<span data-ttu-id="dcc6b-106">Hvis du vil bruke denne funksjonen, må du først aktivere **Avansert fordelsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-106">To use this functionality, you must first turn on **Advanced Benefits Management**.</span></span> <span data-ttu-id="dcc6b-107">Hvis du vil ha mer informasjon, inkludert viktige opplysninger om fordelsbehandling, kan du se [Aktivere eller deaktivere fordelsbehandling](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span><span class="sxs-lookup"><span data-stu-id="dcc6b-107">For more information, including important caveats about Benefits management, see [Enable or disable Benefits management](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dcc6b-108">Du kan bare bruke ACA-rapportering fra arbeidsområdet for **Fordelsbehandling** eller det gamle arbeidsområdet **Fordeler**, ikke fra begge.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-108">You can use ACA reporting only from either the **Benefits management** workspace or the old **Benefits** workspace, not from both.</span></span> <span data-ttu-id="dcc6b-109">Hvis du for eksempel byttet til Fordelsbehandling, er ACA-rapportering bare tilgjengelig fra arbeidsområdet for **Fordelsbehandling**, ikke fra det gamle **Fordeler**-arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-109">For example, if you switched to Benefits management, ACA reporting is available only from the **Benefits management** workspace, not from the old **Benefits** workspace.</span></span>
>
> <span data-ttu-id="dcc6b-110">Hvis du bytter til Fordelsbehandling midt i et registreringsår, må du konfigurere ansattdata på riktig måte for hele året i Fordelsbehandling.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-110">If you switch to Benefits management in the middle of an enrollment year, you must correctly configure employee data for the whole year in Benefits management.</span></span> <span data-ttu-id="dcc6b-111">På denne måten sikrer du at du vil motta nøyaktig rapporteringsinformasjon for hele året.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-111">In this way, you ensure that you will receive accurate reporting information for the whole year.</span></span>

## <a name="getting-started"></a><span data-ttu-id="dcc6b-112">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="dcc6b-112">Getting started</span></span>

<span data-ttu-id="dcc6b-113">Hvis du vil spore informasjon for 1095-skjemaer, må du først opprette én eller flere Affordable Care-dekningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-113">To track information for 1095 forms, first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="dcc6b-114">Disse gruppene angir følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="dcc6b-114">These groups indicate the following information:</span></span>

- <span data-ttu-id="dcc6b-115">Tilbudet om dekning som ble gitt til en ansatt</span><span class="sxs-lookup"><span data-stu-id="dcc6b-115">The offer of coverage that was provided to an employee</span></span>
- <span data-ttu-id="dcc6b-116">Den ansattes del av den månedlige bonusen med lavest kostnad, hvis kostnaden er over den føderale fattigdomsgrensen</span><span class="sxs-lookup"><span data-stu-id="dcc6b-116">The employee's share of the lowest-cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="dcc6b-117">Safe Harbor som brukes av arbeidsgiveren, dersom det er aktuelt</span><span class="sxs-lookup"><span data-stu-id="dcc6b-117">The safe harbor that is used by the employer, if applicable</span></span>

<span data-ttu-id="dcc6b-118">Affordable Care-dekningsgrupper hjelper deg med å administrere denne informasjonen for flere ansattposter som har de samme betingelsene.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-118">Affordable Care coverage groups help you manage this information for multiple employee records that have the same conditions.</span></span> <span data-ttu-id="dcc6b-119">Du kan lett tilordne grupper til én eller flere ansatte.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-119">You can easily assign groups to one or more employees.</span></span>

### <a name="create-or-edit-an-affordable-care-coverage-group"></a><span data-ttu-id="dcc6b-120">Opprette eller redigere en Affordable Care-dekningsgruppe</span><span class="sxs-lookup"><span data-stu-id="dcc6b-120">Create or edit an Affordable Care coverage group</span></span>

1. <span data-ttu-id="dcc6b-121">I arbeidsområdet **Fordelsbehandling** velger du **Affordable Care-dekningsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-121">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>

    ![Velge Affordable Care-dekningsgruppe](./media/hr-benefits-management-aca-coverage-group.png)

2. <span data-ttu-id="dcc6b-123">Velg **Ny** for å opprette en ny Affordable Care-dekningsgruppe eller **Rediger** for å endre en eksisterende gruppe.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-123">Select **New** to create a new Affordable Care coverage group or **Edit** to change an existing group.</span></span>

    ![Velge Ny eller Rediger](./media/hr-benefits-management-aca-new.png)

3. <span data-ttu-id="dcc6b-125">Angi følgende felt.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-125">Set the following fields.</span></span>

    | <span data-ttu-id="dcc6b-126">Felt</span><span class="sxs-lookup"><span data-stu-id="dcc6b-126">Field</span></span> | <span data-ttu-id="dcc6b-127">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="dcc6b-127">Description</span></span> |
    |---|---|
    | <span data-ttu-id="dcc6b-128">Navn</span><span class="sxs-lookup"><span data-stu-id="dcc6b-128">Name</span></span> | <span data-ttu-id="dcc6b-129">Angi et navn for gruppen.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-129">Enter a name for the group.</span></span> |
    | <span data-ttu-id="dcc6b-130">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="dcc6b-130">Description</span></span> | <span data-ttu-id="dcc6b-131">Angi en beskrivelse av gruppen.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-131">Enter a description of the group.</span></span> |
    | <span data-ttu-id="dcc6b-132">Tilbud om dekning</span><span class="sxs-lookup"><span data-stu-id="dcc6b-132">Offer of coverage</span></span> | <span data-ttu-id="dcc6b-133">Dekningen som tilbys ansatte, deres ektefelle eller partner og deres avhengige.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-133">The coverage that is offered to employees, their spouse or partner, and their dependents.</span></span> |
    | <span data-ttu-id="dcc6b-134">Ansattdel av kostnad</span><span class="sxs-lookup"><span data-stu-id="dcc6b-134">Employee share of cost</span></span> | <span data-ttu-id="dcc6b-135">Beløpet som den ansatte er ansvarlig for.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-135">The amount that the employee is responsible for.</span></span> |
    | <span data-ttu-id="dcc6b-136">Gjeldende avsnitt, 4980H safe harbor</span><span class="sxs-lookup"><span data-stu-id="dcc6b-136">Applicable section 4980H safe harbor</span></span> | <span data-ttu-id="dcc6b-137">4980H safe harbor-kode eller kode for overgangslettelse.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-137">The 4980H safe harbor or transition relief code.</span></span> |
    | <span data-ttu-id="dcc6b-138">Startmåned for plan</span><span class="sxs-lookup"><span data-stu-id="dcc6b-138">Plan start month</span></span> | <span data-ttu-id="dcc6b-139">Velg kalendermåneden når fordelsplanåret starter.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-139">Select the calendar month when your benefit plan year begins.</span></span> |
    | <span data-ttu-id="dcc6b-140">Gruppe gyldig fra</span><span class="sxs-lookup"><span data-stu-id="dcc6b-140">Group valid from</span></span> | <span data-ttu-id="dcc6b-141">Den første datoen denne posten er gyldig.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-141">The first date when this record is valid.</span></span> |
    | <span data-ttu-id="dcc6b-142">Gruppe gyldig til og med</span><span class="sxs-lookup"><span data-stu-id="dcc6b-142">Group valid through</span></span> | <span data-ttu-id="dcc6b-143">Den siste datoen denne posten er gyldig.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-143">The last date when this record is valid.</span></span> <span data-ttu-id="dcc6b-144">Hvis det ikke er noen utløpsdato, angir du **Aldri**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-144">If there is no expiration date, enter **Never**.</span></span> |

    ![Opprette en dekningsgruppe](./media/hr-benefits-management-aca-new-group.png)

4. <span data-ttu-id="dcc6b-146">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-146">Select **Save**.</span></span>

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a><span data-ttu-id="dcc6b-147">Tilordne flere ansatte til en Affordable Care-dekningsgruppe</span><span class="sxs-lookup"><span data-stu-id="dcc6b-147">Assign multiple employees to an Affordable Care coverage group</span></span>

1. <span data-ttu-id="dcc6b-148">I arbeidsområdet **Fordelsbehandling** velger du **Affordable Care-dekningsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-148">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>
2. <span data-ttu-id="dcc6b-149">Velg gruppen du vil tilordne ansatte til.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-149">Select the group to assign employees to.</span></span>
3. <span data-ttu-id="dcc6b-150">Velg **Massetilordning**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-150">Select **Mass assignment**.</span></span>

    ![Velge Massetilordning](./media/hr-benefits-management-aca-mass-assignment.png)

4. <span data-ttu-id="dcc6b-152">Velg ansatte i listen, og velg **Tilordne**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-152">Select employees in the list, and then select **Assign**.</span></span>

    ![Tilordne valgte ansatte til en gruppe](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a><span data-ttu-id="dcc6b-154">Vedlikeholde flere versjoner av dekningalternativer</span><span class="sxs-lookup"><span data-stu-id="dcc6b-154">Maintain multiple versions of coverage options</span></span>

<span data-ttu-id="dcc6b-155">Du kan vedlikeholde flere versjoner av en hvilken som helst dekningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-155">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="dcc6b-156">Når noe endres i organisasjonen eller fordelene som tilbys, kan du holde gruppens informasjon oppdatert uten å måtte opprette en ny gruppe og tilordne ansatte til den på nytt.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-156">When something changes in your organization or the benefits that are offered, you can keep the group's information up to date without having to create a new group and reassign employees to it.</span></span>

<span data-ttu-id="dcc6b-157">Når du har opprettet Affordable Care-dekningsgrupper, kan du massetilordne ansatte til dem.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-157">After you've created Affordable Care coverage groups, you can mass-assign employees to them.</span></span> <span data-ttu-id="dcc6b-158">Du kan også tilordne ansatte individuelt til grupper, og angi om ACA-informasjon skal spores og rapporteres.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-158">You can also individually assign employees to groups, and indicate whether ACA information is tracked and reported.</span></span>

<span data-ttu-id="dcc6b-159">Hvis du ikke trenger å spore og rapportere ACA-informasjon for en ansatt, kan du sette alternativet **Rapportdekning** til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-159">If you don't have to track and report ACA information for an employee, you can set the **Report coverage** option to **No**.</span></span> <span data-ttu-id="dcc6b-160">Du kan for eksempel ha deltidsansatte som ikke trenger ACA-rapportering.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-160">For example, you might have part-time employees who don't require ACA reporting.</span></span>

### <a name="override-default-values-for-an-employee"></a><span data-ttu-id="dcc6b-161">Overstyre standardverdier for en ansatt</span><span class="sxs-lookup"><span data-stu-id="dcc6b-161">Override default values for an employee</span></span>

<span data-ttu-id="dcc6b-162">For ansatte som er tilordnet en Affordable Care-dekningsgruppe, kan du endre følgende alternativer for måneder som krever ulike verdier:</span><span class="sxs-lookup"><span data-stu-id="dcc6b-162">For employees who are assigned to an Affordable Care coverage group, you can change the following options for any months that require different values:</span></span>

- <span data-ttu-id="dcc6b-163">Tilbud om dekning</span><span class="sxs-lookup"><span data-stu-id="dcc6b-163">Offer of coverage</span></span>
- <span data-ttu-id="dcc6b-164">Ansattdel av kostnad</span><span class="sxs-lookup"><span data-stu-id="dcc6b-164">Employee share of cost</span></span>
- <span data-ttu-id="dcc6b-165">Gjeldende avsnitt, 4980H safe harbor</span><span class="sxs-lookup"><span data-stu-id="dcc6b-165">Applicable section 4980H safe harbor</span></span>

> [!NOTE]
> <span data-ttu-id="dcc6b-166">For 2020 ACA-rapporter må du rapportere både jobb- og hjemmepostnumre på skjema 1095-C.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-166">For 2020 ACA reports, you must report both work and home ZIP Codes on Form 1095-C.</span></span> <span data-ttu-id="dcc6b-167">Verdier fylles ut automatisk basert på gjeldende aktive lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-167">Values are automatically filled in, based on current active locations.</span></span> <span data-ttu-id="dcc6b-168">Hvis en av lokasjonene var forskjellig i løpet av året, må du overstyre verdien.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-168">If either location was different during any part of the year, you must override the value.</span></span> <span data-ttu-id="dcc6b-169">**Postnummer**-feltet (linje 17) for 1095-C-rapporten fylles bare ut hvis koden **Tilbud om dekning** inneholder **1L** til og med **1Q** følgende måte:</span><span class="sxs-lookup"><span data-stu-id="dcc6b-169">The **ZIP Code** field (line 17) of the 1095-C report is filled in only if the **Offer of coverage** code contains **1L** through **1Q**, as follows:</span></span>
>
> - <span data-ttu-id="dcc6b-170">**1L, 1M eller 1N:** Postnummer for primær bosted</span><span class="sxs-lookup"><span data-stu-id="dcc6b-170">**1L, 1M, or 1N:** The primary residence ZIP Code</span></span>
> - <span data-ttu-id="dcc6b-171">**1O, 1P, 1Q:** Postnummer for det primære arbeidsstedet</span><span class="sxs-lookup"><span data-stu-id="dcc6b-171">**1O, 1P, 1Q:** The primary work ZIP Code</span></span>

<span data-ttu-id="dcc6b-172">Følg denne fremgangsmåten for å angi unntak for verdier til en Affordable Care-dekningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-172">To enter exceptions for any values of an Affordable Care coverage group, follow these steps.</span></span>

1. <span data-ttu-id="dcc6b-173">I arbeidsområdet **Personaladministrasjon** velger du **Koblinger** og deretter **Arbeidere**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-173">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>
2. <span data-ttu-id="dcc6b-174">Velg ansatt i listen.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-174">Select the employee in the list.</span></span>
3. <span data-ttu-id="dcc6b-175">I kategorien **Ansettelse** i delen **Mer informasjon** velger du **Affordable Care-dekning**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-175">On the **Employment** tab, in the **More information** section, select **Affordable Care coverage**.</span></span>

    ![Endre alternativer for én ansatt](./media/hr-benefits-management-aca-change-single-employee.png)

4. <span data-ttu-id="dcc6b-177">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-177">Select **Edit**.</span></span>
5. <span data-ttu-id="dcc6b-178">For hver måned som krever endringer, merker du av for **Overstyr standard**, og deretter endrer du de andre verdiene etter behov.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-178">For each month that requires changes, select the **Override default** check box, and then change the other values as required.</span></span>

    ![Overstyre standardverdier](./media/hr-benefits-management-aca-override-default.png)

6. <span data-ttu-id="dcc6b-180">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-180">Select **Save**.</span></span>

## <a name="report-health-care-coverage"></a><span data-ttu-id="dcc6b-181">Rapportere helsedekning</span><span class="sxs-lookup"><span data-stu-id="dcc6b-181">Report health care coverage</span></span>

<span data-ttu-id="dcc6b-182">Du må spore alle arbeidsgiver-sponsede, selvforsikret helsedekning for heltids- og deltidsansatte.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-182">You must track any employer-sponsored, self-insured health care coverage for full-time and part-time employees.</span></span> <span data-ttu-id="dcc6b-183">Inkluder hver ansatt sammen med deres avhengige på 1095-C-rapporten for månedene de ble dekket.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-183">Include each employee, together with their dependents, on the 1095-C report for the months when they were covered.</span></span>

<span data-ttu-id="dcc6b-184">Følg denne fremgangsmåten for å angi om en fordelsplan må rapporteres.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-184">To indicate whether a benefit plan must be reported, follow these steps.</span></span>

1. <span data-ttu-id="dcc6b-185">I arbeidsområdet **Fordelsbehandling**, velger du **Fordelsplaner**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-185">In the **Benefits management** workspace, select **Benefit plans**.</span></span>
2. <span data-ttu-id="dcc6b-186">Velg fordelsplanen som skal rapporteres.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-186">Select the benefit plan to report.</span></span>
3. <span data-ttu-id="dcc6b-187">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-187">Select **Edit**.</span></span>
4. <span data-ttu-id="dcc6b-188">Sett alternativet **Rapportert under Affordable Care Act** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-188">Set the **Reported under the Affordable Care Act** option to **Yes**.</span></span>

    ![Rapportere helsedekning](./media/hr-benefits-management-aca-report-coverage.png)

5. <span data-ttu-id="dcc6b-190">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-190">Select **Save**.</span></span>

<span data-ttu-id="dcc6b-191">Hvis en ansatt velger helsedekning for en avhengig, bestemmes avhengiges dekningsperiode av datoen da den avhengige ble registrert eller fjernet.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-191">If an employee chooses health care coverage for a dependent, the dependent's coverage period is determined by the date when the dependent was enrolled or removed.</span></span> <span data-ttu-id="dcc6b-192">Dekningsdatoer for avhengige beregnes automatisk basert på perioden da den avhengige var kvalifisert og aktiv i en plan i løpet av registreringsåret.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-192">Coverage dates for dependents are automatically calculated based on the period when the dependent was eligible and active in a plan during the enrollment year.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="dcc6b-193">Generere 1095-B- og 1095-C-skjemaer</span><span class="sxs-lookup"><span data-stu-id="dcc6b-193">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="dcc6b-194">Du kan også generere ACA 1095-B- og 1095-C-skjemaer, og distribuer dem deretter til alle ansatte.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-194">You can generate ACA 1095-B and 1095-C forms, and then distribute them to each of your employees.</span></span> <span data-ttu-id="dcc6b-195">Du kan også generere skjema 1095-C elektronisk og de tilsvarende overføringsfilene for 1094-C som skal sendes til Internal Revenue Service (IRS).</span><span class="sxs-lookup"><span data-stu-id="dcc6b-195">You can also electronically generate Form 1095-C and the corresponding 1094-C transmittal files to send to the Internal Revenue Service (IRS).</span></span>

1. <span data-ttu-id="dcc6b-196">I arbeidsområdet **Fordelsbehandling** velger du **ACA 1095-B-skjema** eller **ACA 1095-C-skjema**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-196">In the **Benefits management** workspace, select **ACA 1095-B form** or **ACA 1095-C form**.</span></span>
2. <span data-ttu-id="dcc6b-197">Endre parameterne etter behov, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-197">Change the parameters as required, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dcc6b-198">Hvis du skriver ut 1095-C-skjemaer for mer enn 500 ansatte, får du mer enn én PDF-fil.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-198">If you're printing 1095-C forms for more than 500 employees, you will receive more than one PDF file.</span></span> <span data-ttu-id="dcc6b-199">Vi anbefaler at du øker verdien til feltet **Maksimum filstørrelse** på siden **Parametere for dokumentstyring** til **150**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-199">We recommend that you increase the value of the **Maximum file size in megabytes** field on the **Document management parameters** page to **150**.</span></span> <span data-ttu-id="dcc6b-200">(Du kan åpne den siden raskt ved å bruke søkefeltet i navigasjonsfeltet.)</span><span class="sxs-lookup"><span data-stu-id="dcc6b-200">(To quickly open that page, you can use the search field on the navigation bar.)</span></span>
    >
    > ![Endre maksimumsfilstørrelse](./media/hr-benefits-management-aca-maximum-file-size.png)

3. <span data-ttu-id="dcc6b-202">Hvis du vil kontrollere statusen til rapportene og vise dem, bruker du søkefeltet på navigasjonslinjen til å åpne siden **Elektroniske rapporteringsjobber**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-202">To check the status of your reports and view them, use the search field on the navigation bar to open the **Electronic reporting jobs** page.</span></span>

    ![Søke etter siden Elektroniske rapporteringsjobber](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. <span data-ttu-id="dcc6b-204">Velg rapporten som skal vises, og velg deretter **Vis filer**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-204">Select the report to view, and then select **Show files**.</span></span>

    ![Viser filer](./media/hr-benefits-management-aca-show-files.png)

5. <span data-ttu-id="dcc6b-206">Velg **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-206">Select **Open**.</span></span>

    ![Åpne en fil](./media/hr-benefits-management-aca-open-file.png)

6. <span data-ttu-id="dcc6b-208">Åpne zip-filen i varslingsfeltet som vises nederst i webleservinduet, og velg deretter rapporten.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-208">From the Notification bar that appears at the bottom of the browser window, open the zip file, and then select the report.</span></span> <span data-ttu-id="dcc6b-209">Du kan vise eller skrive ut PDF-filen.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-209">You can view or print the PDF file.</span></span>

    ![Eksempel 1095-C-skjema](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a><span data-ttu-id="dcc6b-211">Vise ACA-dekningsinformasjon</span><span class="sxs-lookup"><span data-stu-id="dcc6b-211">View ACA coverage information</span></span>

<span data-ttu-id="dcc6b-212">Siden **Affordable Care-dekning for arbeidere** viser følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="dcc6b-212">The **Worker Affordable Care coverage** page shows the following information:</span></span>

- <span data-ttu-id="dcc6b-213">Ansatte som er tilordnet hver dekningsgruppe</span><span class="sxs-lookup"><span data-stu-id="dcc6b-213">Employees who are assigned to each coverage group</span></span>
- <span data-ttu-id="dcc6b-214">Ansatte som ikke må inkluderes i en rapport</span><span class="sxs-lookup"><span data-stu-id="dcc6b-214">Employees who don't have to be included on a report</span></span>
- <span data-ttu-id="dcc6b-215">Ikke tilordnede ansatte</span><span class="sxs-lookup"><span data-stu-id="dcc6b-215">Unassigned employees</span></span>

<span data-ttu-id="dcc6b-216">Følg disse trinnene for å vise informasjonen.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-216">To view this information, follow these steps.</span></span>

1. <span data-ttu-id="dcc6b-217">I arbeidsområdet **Fordelsbehandling** velger du **Affordable Care-dekning for arbeidere**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-217">In the **Benefits management** workspace, select **Worker Affordable Care coverage**.</span></span>
2. <span data-ttu-id="dcc6b-218">Velg en gruppe i feltet **Gruppenavn**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-218">In the **Group name** field, select a group.</span></span>

    ![Vise ACA-dekning](./media/hr-benefits-management-aca-view-coverage.png)

<span data-ttu-id="dcc6b-220">Hvis noen av standardverdiene fra Affordable Care-dekningsgruppen har blitt overstyrt, vises en stjerne ved siden av verdien som ble endret.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-220">If any default values from the Affordable Care coverage group have been overridden, an asterisk appears next to the value that was changed.</span></span> <span data-ttu-id="dcc6b-221">Hvis verdiene for alle tolv månedene er de samme, og ikke har blitt overstyrt, vises verdien i **Alle 12 måneder**-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-221">If the values for all 12 months are the same and haven't been overridden, the value appears in the **All 12 months** column.</span></span>

<span data-ttu-id="dcc6b-222">Du kan vise ansatte som er merket som ikke ACA-rapporterbare, og som ikke vil kreve et skjema 1095-C.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-222">You can view employees who are marked as not ACA-reportable, and who won't require a Form 1095-C.</span></span> <span data-ttu-id="dcc6b-223">Velg **Ikke ACA-rapporterbar** i feltet **Filtrer etter**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-223">In the **Filter by** field, select **Not ACA reportable**.</span></span>

<span data-ttu-id="dcc6b-224">Du kan vise ansatte som ikke er tilordnet en gruppe, eller som er tilordnet til en utløpt gruppe.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-224">You can view employees who aren't assigned to a group, or who are assigned to an expired group.</span></span> <span data-ttu-id="dcc6b-225">Velg **Ikke tilordnet eller utløpt gruppe** i **Filtrer etter**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-225">In the **Filter by** field, select **Unassigned or expired group**.</span></span>

### <a name="export-to-excel"></a><span data-ttu-id="dcc6b-226">Eksporter til Excel</span><span class="sxs-lookup"><span data-stu-id="dcc6b-226">Export to Excel</span></span>

<span data-ttu-id="dcc6b-227">Følg denne fremgangsmåten for å eksportere hvilke som helst av listene til Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-227">To export any of the lists to Microsoft Excel, follow these steps.</span></span>

1. <span data-ttu-id="dcc6b-228">Velg knappen **Åpne i Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-228">Select the **Open in Microsoft Office** button.</span></span>
2. <span data-ttu-id="dcc6b-229">Velg valget for **HCM Human Resources midlertidig tabell for intern bruk**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-229">Select **HCM Human Resources temporary table for internal use**.</span></span>
3. <span data-ttu-id="dcc6b-230">Velg **Last ned**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-230">Select **Download**.</span></span>

### <a name="view-aca-reportable-dependents"></a><span data-ttu-id="dcc6b-231">Vise ACA-rapporterbare avhengige</span><span class="sxs-lookup"><span data-stu-id="dcc6b-231">View ACA-reportable dependents</span></span>

<span data-ttu-id="dcc6b-232">Hvis du må rapportere dekkede personer fordi du gir selvforsikret dekning, kan du vise avhengige som dekkes av fordelsplaner, som er merket som **ACA-rapporterbar**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-232">If you must report covered individuals because you provide self-insured coverage, you can view dependents who are covered under benefit plans that are marked as **ACA reportable**.</span></span> <span data-ttu-id="dcc6b-233">Velg **Vis avhengig dekning** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-233">On the Action Pane, select **View Dependent coverage**.</span></span>

![Vise avhengig dekning](./media/hr-benefits-management-aca-view-dependent-coverage.png)

<span data-ttu-id="dcc6b-235">Dekningsinformasjon for de ansattes avhengige vises.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-235">Coverage information for the employee's dependents is shown.</span></span>

![Avhengig dekning](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> <span data-ttu-id="dcc6b-237">Siden viser bare fordelsplaner som er merket som **ACA-rapporterbare**.</span><span class="sxs-lookup"><span data-stu-id="dcc6b-237">The page shows only benefits plans that are marked as **ACA reportable**.</span></span>
