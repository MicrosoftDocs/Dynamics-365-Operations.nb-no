---
title: Konfigurere parametere for Human Resources
description: Dette emnet forklarer hvordan du konfigurerer firmaspesifikke parametere i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cd66cb4f5ac02407250e15ae134b36f5ccd4d290
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889938"
---
# <a name="configure-human-resources-parameters"></a><span data-ttu-id="0aff2-103">Konfigurere parametere for Human Resources</span><span class="sxs-lookup"><span data-stu-id="0aff2-103">Configure Human resources parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0aff2-104">Innstillingene for noen Human Resources-parametere deles mellom firmaer, mens innstillingene for andre parametere er firmaspesifikke.</span><span class="sxs-lookup"><span data-stu-id="0aff2-104">The settings of some Human resources parameters are shared across companies, while the settings of other parameters are company-specific.</span></span> <span data-ttu-id="0aff2-105">Dette emnet forklarer hvordan du konfigurerer firmaspesifikke parametere i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0aff2-105">This topic explains how to set up company-specific Human resources parameters.</span></span>

<span data-ttu-id="0aff2-106">To sider brukes til å angi Human Resources-parametere.</span><span class="sxs-lookup"><span data-stu-id="0aff2-106">Two pages are used to set Human resources parameters.</span></span> <span data-ttu-id="0aff2-107">For parametere som deles på tvers av firmaer, bruker du siden **Delte parametere for personaladministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="0aff2-107">For parameters that are shared across companies, you use the **Human resources shared parameters** page.</span></span> <span data-ttu-id="0aff2-108">For parameterne som er firmaspesifikke (altså innstillingene gjelder ett enkelt firma), bruker du siden **Personalparametere**.</span><span class="sxs-lookup"><span data-stu-id="0aff2-108">For parameters that are company-specific (in other words, the settings apply to a single company), you use the **Human resource parameters** page.</span></span>

![Gå til Human Resources-parametere](./media/hr-employee-self-service-human-resources-parameters.png)

<span data-ttu-id="0aff2-110">På siden **Personalparametere** er innstillingene delt inn i seks kategorier:</span><span class="sxs-lookup"><span data-stu-id="0aff2-110">On the **Human resources parameters** page, the settings are divided among six tabs:</span></span>

- <span data-ttu-id="0aff2-111">**Generelt**</span><span class="sxs-lookup"><span data-stu-id="0aff2-111">**General**</span></span>
- <span data-ttu-id="0aff2-112">**Rekruttering** (denne fanen er ikke inkludert i Dynamics 365 Human Resources)</span><span class="sxs-lookup"><span data-stu-id="0aff2-112">**Recruitment** (this tab isn't included in Dynamics 365 Human Resources)</span></span>
- <span data-ttu-id="0aff2-113">**Kompensasjon**</span><span class="sxs-lookup"><span data-stu-id="0aff2-113">**Compensation**</span></span>
- <span data-ttu-id="0aff2-114">**Nummerserier**</span><span class="sxs-lookup"><span data-stu-id="0aff2-114">**Number sequences**</span></span>
- <span data-ttu-id="0aff2-115">**FMLA**</span><span class="sxs-lookup"><span data-stu-id="0aff2-115">**FMLA**</span></span>
- <span data-ttu-id="0aff2-116">**Ansattselvbetjening**</span><span class="sxs-lookup"><span data-stu-id="0aff2-116">**Employee self service**</span></span>
- <span data-ttu-id="0aff2-117">**Lederselvbetjening**</span><span class="sxs-lookup"><span data-stu-id="0aff2-117">**Manager self service**</span></span>
- <span data-ttu-id="0aff2-118">**Fordelsbehandling**</span><span class="sxs-lookup"><span data-stu-id="0aff2-118">**Benefits management**</span></span>
- <span data-ttu-id="0aff2-119">**Permisjon og fravær**</span><span class="sxs-lookup"><span data-stu-id="0aff2-119">**Leave and absence**</span></span>
- <span data-ttu-id="0aff2-120">**Betalingsmåter**</span><span class="sxs-lookup"><span data-stu-id="0aff2-120">**Payment methods**</span></span>

<span data-ttu-id="0aff2-121">Hver kategori inneholder informasjon som gjelder ett enkelt firma.</span><span class="sxs-lookup"><span data-stu-id="0aff2-121">Each tab contains information that pertains to a single company.</span></span>

## <a name="general"></a><span data-ttu-id="0aff2-122">Generelt</span><span class="sxs-lookup"><span data-stu-id="0aff2-122">General</span></span>

<span data-ttu-id="0aff2-123">Innstillingene i kategorien **Generelt** definerer utseendet til informasjon om fravær, skade og sykdom og nye ansettelser.</span><span class="sxs-lookup"><span data-stu-id="0aff2-123">The settings on the **General** tab define the appearance of information about absence, injury and illness, and new hires.</span></span> <span data-ttu-id="0aff2-124">Innstillingene i denne kategorien definerer også noen standardoppføringer som vises når du arbeider.</span><span class="sxs-lookup"><span data-stu-id="0aff2-124">The settings on this tab also define some default entries that appear as you work.</span></span> <span data-ttu-id="0aff2-125">I denne fanen kan du spesifikt gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="0aff2-125">Specifically, this tab lets you:</span></span>

- <span data-ttu-id="0aff2-126">Velg en farge som skal brukes på åpne fraværstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="0aff2-126">Select a color to apply to open absence transactions</span></span>
- <span data-ttu-id="0aff2-127">Angi stilarket som skal brukes for rapporter</span><span class="sxs-lookup"><span data-stu-id="0aff2-127">Specify the style sheet to use for reports</span></span>
- <span data-ttu-id="0aff2-128">Aktivere integrering mellom kurs og fraværsregistrering</span><span class="sxs-lookup"><span data-stu-id="0aff2-128">Enable the integration between training courses and absence registration</span></span>
- <span data-ttu-id="0aff2-129">Velg fraværskoden som skal brukes til å kontrollere denne integreringen.</span><span class="sxs-lookup"><span data-stu-id="0aff2-129">Select the absence code that is used to control this integration.</span></span>
- <span data-ttu-id="0aff2-130">Angi hvor lenge hendelsene i tilfelle tilfeller av sykdom skal holdes under åpenhet og på grunn av sykdom.</span><span class="sxs-lookup"><span data-stu-id="0aff2-130">Indicate how long to keep injury and illness case incidents.</span></span>
- <span data-ttu-id="0aff2-131">Angi standard identifikasjonsnummer som vises når en ny arbeider blir ansatt.</span><span class="sxs-lookup"><span data-stu-id="0aff2-131">Specify the default identification number shown when a new worker is hired.</span></span>

![Fanen Generelt](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a><span data-ttu-id="0aff2-133">Rekruttering</span><span class="sxs-lookup"><span data-stu-id="0aff2-133">Recruitment</span></span>

<span data-ttu-id="0aff2-134">Innstillingene i fanen **Rekruttering** definerer dokumenttypene som brukes til korrespondanse, som automatisk sendes til søkere.</span><span class="sxs-lookup"><span data-stu-id="0aff2-134">The settings on the **Recruitment** tab define the document types used for correspondence automatically sent to applicants.</span></span> <span data-ttu-id="0aff2-135">Du kan også angi rekrutteringsprosjektet som brukes til uanførte søknader.</span><span class="sxs-lookup"><span data-stu-id="0aff2-135">You can also indicate the recruitment project used for unsolicited applications.</span></span>

<span data-ttu-id="0aff2-136">Perioden som er definert for aldersfordeling for rekrutteringsprosjekt bestemmer rekrutteringsprosjektene som er inkludert i flisen **Aldersfordelingsprosjekter** i arbeidsområdet **Rekrutteringsstyring**.</span><span class="sxs-lookup"><span data-stu-id="0aff2-136">The period defined for recruitment project aging determines the recruitment projects included on the **Aging projects** tile in the **Recruitment management** workspace.</span></span> <span data-ttu-id="0aff2-137">Perioden som er definert for advarselen for tidsfrist for søknad, brukes til å vise rekrutteringsprosjekter som nærmer seg sin søknadsfrist på flisen **Søknadsfristen nærmer seg** i arbeidsområdet **Rekruttering**.</span><span class="sxs-lookup"><span data-stu-id="0aff2-137">The period defined for the application deadline warning is used to display recruitment projects that are approaching their application deadline on the **Application deadline approaching** tile in the **Recruitment** workspace.</span></span>

<span data-ttu-id="0aff2-138">Hvis du vil ha mer informasjon om rekruttering, kan du se [Rekruttere jobbkandidater](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="0aff2-138">For more information about recruiting, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="compensation"></a><span data-ttu-id="0aff2-139">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="0aff2-139">Compensation</span></span>

<span data-ttu-id="0aff2-140">Innstillingene i fanen **Kompensasjon** i Dynamics 365 Finance definerer om brukere må bekrefte at de vil lagre informasjon for en fast eller variabel kompensasjonsplan.</span><span class="sxs-lookup"><span data-stu-id="0aff2-140">In Dynamics 365 Finance, the settings on the **Compensation** tab define whether users must confirm that they want to save information for a fixed or variable compensation plan.</span></span> <span data-ttu-id="0aff2-141">Hvis du merker av for **Aktiver lagring av validering**, mottar brukere en melding som spør om de vil lagre posten når de lukker en kompensasjonsrelatert side.</span><span class="sxs-lookup"><span data-stu-id="0aff2-141">If you select **Enable save validation**, when users close a compensation-related page, they receive a message that asks whether they want to save the record.</span></span> <span data-ttu-id="0aff2-142">Noen av sidene i Kompensasjonsstyring lar ikke brukere slette informasjon.</span><span class="sxs-lookup"><span data-stu-id="0aff2-142">Some pages in Compensation management don't let users delete information.</span></span> <span data-ttu-id="0aff2-143">Ved å be brukere bekrefte at de vil lagre informasjon, kan du kunne begrense mengden av informasjon som lagres, men som ikke kan slettes senere.</span><span class="sxs-lookup"><span data-stu-id="0aff2-143">By prompting users to verify that they want to save information, you might be able to limit the amount of information that is saved but can't be deleted later.</span></span> <span data-ttu-id="0aff2-144">Hvis du fjerner merket for **Aktiver lagring av validering**, lagres poster umiddelbart, muligens før brukeren er klar.</span><span class="sxs-lookup"><span data-stu-id="0aff2-144">If you clear **Enable save validation**, records save immediately, possibly before the user is ready.</span></span> <span data-ttu-id="0aff2-145">Hvis du bruker Ytelsesstyring, kan du bruke fanen **Kompensasjon** til å velge en vurderingsmodell i stedet for å bruke modellen som er tilordnet til kompensasjonsplaner ved vurdering av ytelse.</span><span class="sxs-lookup"><span data-stu-id="0aff2-145">If you're using Performance management, the **Compensation** tab also lets you select a rating model to use instead of the model assigned to compensation plans when rating performance.</span></span>

<span data-ttu-id="0aff2-146">I Human Resources kan du bruke fanen **Kompensasjon** til å velge å begrense tilgang til kompensasjonsplaner og angi en standardvaluta.</span><span class="sxs-lookup"><span data-stu-id="0aff2-146">In Human Resources, you can use the **Compensation** tab to choose to restrict access to compensation plans and to set a default currency.</span></span>

<span data-ttu-id="0aff2-147">Hvis du vil ha mer informasjon om kompensasjon, kan du se [Oversikt over kompensasjonsplaner](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0aff2-147">For more information about compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Kategorien Kompensasjon](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a><span data-ttu-id="0aff2-149">Nummerserier</span><span class="sxs-lookup"><span data-stu-id="0aff2-149">Number sequences</span></span>

<span data-ttu-id="0aff2-150">Innstillingene i fanen **Nummerserie** bestemmer seriene som brukes til automatisk å tilordne ID-er til varer i Human Resources, for eksempel:</span><span class="sxs-lookup"><span data-stu-id="0aff2-150">The settings on the **Number sequence** tab determine the sequences used to automatically assign IDs to items in Human Resources, such as:</span></span>

- <span data-ttu-id="0aff2-151">Søknader</span><span class="sxs-lookup"><span data-stu-id="0aff2-151">Applications</span></span>
- <span data-ttu-id="0aff2-152">Fraværsregistreringer</span><span class="sxs-lookup"><span data-stu-id="0aff2-152">Absence registrations</span></span>
- <span data-ttu-id="0aff2-153">Resultater av kompensasjonsprosess</span><span class="sxs-lookup"><span data-stu-id="0aff2-153">Compensation process results</span></span>
- <span data-ttu-id="0aff2-154">Saksnumre</span><span class="sxs-lookup"><span data-stu-id="0aff2-154">Case numbers</span></span>
- <span data-ttu-id="0aff2-155">Kurs</span><span class="sxs-lookup"><span data-stu-id="0aff2-155">Courses</span></span>
- <span data-ttu-id="0aff2-156">Kursagendaer</span><span class="sxs-lookup"><span data-stu-id="0aff2-156">Course agendas</span></span>

<span data-ttu-id="0aff2-157">Hvis du vil beholde nummerseriereferanser og -koder, kan du bruke listen **Nummerserier** (velg **Organisasjonsstyring > Nummerserier > Nummerserier**).</span><span class="sxs-lookup"><span data-stu-id="0aff2-157">To maintain number sequence references and codes, use the **Number sequences** list page (select **Organization administration > Number sequences > Number sequences**).</span></span>

<span data-ttu-id="0aff2-158">Hvis du vil ha mer informasjon, kan du se [Oversikt over nummerserier](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="0aff2-158">For more information, see [Number sequences overview](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

> [!NOTE]
> <span data-ttu-id="0aff2-159">Antall timer arbeidet kan ikke overskride 1250, og lengden på ansettelse kan ikke overskride 12 måneder.</span><span class="sxs-lookup"><span data-stu-id="0aff2-159">The number of hours that are worked can't exceed 1,250, and the length of employment can't exceed 12 months.</span></span> <span data-ttu-id="0aff2-160">Disse maksimumsverdier er i overensstemmelse med gjeldende lovgivning i USA.</span><span class="sxs-lookup"><span data-stu-id="0aff2-160">These maximum values are in accordance with federal law in the United States.</span></span>

![Fanen Nummerserier](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a><span data-ttu-id="0aff2-162">FMLA</span><span class="sxs-lookup"><span data-stu-id="0aff2-162">FMLA</span></span>

<span data-ttu-id="0aff2-163">I fanen FMLA definerer du FMLA-rettighetskravene og FMLA-rettighetstimene.</span><span class="sxs-lookup"><span data-stu-id="0aff2-163">On the FMLA tab, you set FMLA eligibility requirements and FMLA entitlement hours.</span></span> <span data-ttu-id="0aff2-164">Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværsparametere](hr-leave-and-absence-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0aff2-164">For more information, see [Configure leave and absence parameters](hr-leave-and-absence-parameters.md).</span></span>

![FMLA-fane](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a><span data-ttu-id="0aff2-166">Ansattselvbetjening</span><span class="sxs-lookup"><span data-stu-id="0aff2-166">Employee self service</span></span>

<span data-ttu-id="0aff2-167">Innstillingene i fanen **Selvbetjening for ansatte** påvirker hvordan Selvbetjening for ansatte vises for ansatte.</span><span class="sxs-lookup"><span data-stu-id="0aff2-167">The settings on the **Employee self service** tab affect how Employee self service appears to employees.</span></span> <span data-ttu-id="0aff2-168">I denne fanen kan du:</span><span class="sxs-lookup"><span data-stu-id="0aff2-168">On this tab, you can:</span></span>

- <span data-ttu-id="0aff2-169">Angi et navn for arbeidsområdet Selvbetjening for ansatte</span><span class="sxs-lookup"><span data-stu-id="0aff2-169">Enter a name for the Employee self service workspace</span></span>
- <span data-ttu-id="0aff2-170">Velge hvilken informasjon en leder kan legge inn for ansatte</span><span class="sxs-lookup"><span data-stu-id="0aff2-170">Select which information a manager can enter for employees</span></span>
- <span data-ttu-id="0aff2-171">Legge til nyttige koblinger for ansatte</span><span class="sxs-lookup"><span data-stu-id="0aff2-171">Add useful links for employees</span></span>
- <span data-ttu-id="0aff2-172">Hindre at ansatte legger til eller redigerer kontaktdetaljer for virksomhet.</span><span class="sxs-lookup"><span data-stu-id="0aff2-172">Restrict employees from adding or editing business contact details.</span></span> <span data-ttu-id="0aff2-173">Hvis du vil ha mer informasjon, kan du se [Begrense redigering av personlige opplysninger](hr-employee-self-service-restrict-editing.md).</span><span class="sxs-lookup"><span data-stu-id="0aff2-173">For more information, see [Restrict editing of personal information](hr-employee-self-service-restrict-editing.md).</span></span>

<span data-ttu-id="0aff2-174">Hvis du vil ha mer informasjon om hvordan du konfigurerer Selvbetjening for ansatte, kan du se [Oversikt over selvbetjening for ansatte og ledere](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0aff2-174">For more information about setting up Employee self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Fanen Selvbetjening for ansatte](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a><span data-ttu-id="0aff2-176">Lederselvbetjening</span><span class="sxs-lookup"><span data-stu-id="0aff2-176">Manager self service</span></span>

<span data-ttu-id="0aff2-177">Innstillingene i fanen **Selvbetjening for leder** påvirker hva ledere ser i Selvbetjening for leder.</span><span class="sxs-lookup"><span data-stu-id="0aff2-177">The settings on the **Manager self service** tab affect what managers see in Manager self service.</span></span> <span data-ttu-id="0aff2-178">I denne fanen kan du konfigurere følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="0aff2-178">On this tab, you can configure the following options:</span></span>

- <span data-ttu-id="0aff2-179">Området for utløpsposter</span><span class="sxs-lookup"><span data-stu-id="0aff2-179">The range for expiring records</span></span>
- <span data-ttu-id="0aff2-180">Informasjon som ledere kan vise i utløpsposter</span><span class="sxs-lookup"><span data-stu-id="0aff2-180">Information managers can view in expiring records</span></span>
- <span data-ttu-id="0aff2-181">Om ledere kan vise åpne stillinger for utvidede rapporter</span><span class="sxs-lookup"><span data-stu-id="0aff2-181">Whether managers can view open positions for extended reports</span></span>
- <span data-ttu-id="0aff2-182">Visninger av eksisterende arbeidere</span><span class="sxs-lookup"><span data-stu-id="0aff2-182">Views of exiting workers</span></span>
- <span data-ttu-id="0aff2-183">Nyttige koblinger for ledere</span><span class="sxs-lookup"><span data-stu-id="0aff2-183">Useful links for managers</span></span>

<span data-ttu-id="0aff2-184">Hvis du vil ha mer informasjon om hvordan du konfigurerer Selvbetjening for leder, kan du se [Oversikt over selvbetjening for ansatte og ledere](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0aff2-184">For more information about setting up Manager self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Fanen Selvbetjening for leder](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a><span data-ttu-id="0aff2-186">Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="0aff2-186">Benefits management</span></span>

<span data-ttu-id="0aff2-187">I fanen Fordelsstyring kan du konfigurere e-postalternativer for Fordelsstyring.</span><span class="sxs-lookup"><span data-stu-id="0aff2-187">On the Benefits management tab, you can configure email options for Benefits management.</span></span> <span data-ttu-id="0aff2-188">Hvis du vil ha informasjon om hvordan du konfigurerer og bruker Fordelsbehandling, kan du se [Oversikt over fordelsbehandling](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0aff2-188">For information about setting up and using Benefits management, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

![Fanen Fordelsbehandling](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a><span data-ttu-id="0aff2-190">Permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="0aff2-190">Leave and absence</span></span>

<span data-ttu-id="0aff2-191">Hvis du vil ha informasjon om hvordan du konfigurerer og bruker Permisjon og fravær, kan du se [Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0aff2-191">For information about setting up and using Leave and absence, see [Leave and absence overview](hr-leave-and-absence-overview.md).</span></span>

## <a name="payment-methods"></a><span data-ttu-id="0aff2-192">Betalingsmåter</span><span class="sxs-lookup"><span data-stu-id="0aff2-192">Payment methods</span></span>

<span data-ttu-id="0aff2-193">I fanen **Betalingsmåter** kan du velge betalingsmåtene som støttes av organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="0aff2-193">On the **Payment methods** tab, you can select the payment methods supported by your organization.</span></span> <span data-ttu-id="0aff2-194">Hvis du vil ha mer informasjon om hvordan du konfigurerer kompensasjon, kan du se [Oversikt over kompensasjonsplaner](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0aff2-194">For more information about configuring compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Fanen Betalingsmåter](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]