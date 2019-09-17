---
title: Hva er nytt eller endret i Dynamics 365 for Talent (6. mai 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c541bac532e878c8493a60d95c05c9104d4b96e1
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741550"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-6-2019"></a><span data-ttu-id="91979-103">Hva er nytt eller endret i Dynamics 365 for Talent (6. mai 2019)</span><span class="sxs-lookup"><span data-stu-id="91979-103">What's new or changed in Dynamics 365 for Talent (May 6, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="91979-104">Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="91979-104">This topic describes features that are either new or changed in Dynamics 365 for Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="91979-105">Endringer i Attract</span><span class="sxs-lookup"><span data-stu-id="91979-105">Changes in Attract</span></span>

### <a name="select-optional-documents-upon-offer-creation"></a><span data-ttu-id="91979-106">Velg valgfrie dokumenter ved tilbudsoppretting</span><span class="sxs-lookup"><span data-stu-id="91979-106">Select optional documents upon offer creation</span></span>

<span data-ttu-id="91979-107">Når du velger en tilbudspakkemal, blir du nå bedt om å velge de aktuelle, valgfrie dokumentene fra denne pakkemalen.</span><span class="sxs-lookup"><span data-stu-id="91979-107">When you select an offer package template, Attract now prompts you to select the applicable, optional documents from that package template.</span></span> <span data-ttu-id="91979-108">Du kan legge til andre valgfrie dokumenter mens du klargjør tilbudet.</span><span class="sxs-lookup"><span data-stu-id="91979-108">You can add other optional documents while preparing the offer.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="91979-109">Endringer i Onboard</span><span class="sxs-lookup"><span data-stu-id="91979-109">Changes in Onboard</span></span>

<span data-ttu-id="91979-110">Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="91979-110">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="91979-111">Endringer i Core HR</span><span class="sxs-lookup"><span data-stu-id="91979-111">Changes in Core HR</span></span>

<span data-ttu-id="91979-112">Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2282.</span><span class="sxs-lookup"><span data-stu-id="91979-112">Changes described in this section apply to build number 8.1.2282.</span></span> <span data-ttu-id="91979-113">Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="91979-113">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="platform-update-26"></a><span data-ttu-id="91979-114">Plattform update 26</span><span class="sxs-lookup"><span data-stu-id="91979-114">Platform update 26</span></span>

<span data-ttu-id="91979-115">Hvis du vil ha mer informasjon om Platform update 26, kan du se [Forhåndsvisningsfunksjoner i Dynamics 365 for Finance and Operations Platform Update 26 (mai 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26).</span><span class="sxs-lookup"><span data-stu-id="91979-115">For additional details about Platform update 26, see [Preview features in Dynamics 365 for Finance and Operations platform update 26 (May 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26).</span></span> 

### <a name="common-data-service-entity-support-for-custom-fields"></a><span data-ttu-id="91979-116">Common Data Service-enhetsstøtte for egendefinerte felt</span><span class="sxs-lookup"><span data-stu-id="91979-116">Common Data Service entity support for custom fields</span></span>

<span data-ttu-id="91979-117">I denne ukens versjon støtter nå følgende enheter egendefinerte felt: Beregningsfrekvens for fordeler, Beregningssats for fordeler, Fordelstype, Arbeidskalender, Arbeidskalenderferie, Lønnssyklus og Arbeideridentifikasjonstyper.</span><span class="sxs-lookup"><span data-stu-id="91979-117">In this week's release, the following entities now support custom fields: Benefit calc frequency, Benefit calc rate, Benefit type, Work calendar, Work calendar holiday, Pay cycle, and Worker identification types.</span></span>

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a><span data-ttu-id="91979-118">Avslutning av masseregistrering og endring av nivågrunnlaget til Ansiennitetsdato oppdaterer ikke den første avsetningssatsen (318526)</span><span class="sxs-lookup"><span data-stu-id="91979-118">Leave mass enrollment, changing the tier basis to "Seniority date" doesn't refresh the initial accrual rate (318526)</span></span>

<span data-ttu-id="91979-119">Når du masseregistrerer ansatte og endrer nivågrunnlaget, gjenspeiler nå den første avsetningen nivågrunnlaget du valgte.</span><span class="sxs-lookup"><span data-stu-id="91979-119">When you mass enroll employees and change the tier basis, the initial accrual now reflects the tier basis that you selected.</span></span>

### <a name="workflow-showing-duplicate-place-holders-313636"></a><span data-ttu-id="91979-120">Arbeidsflyt som viser dupliserte plassholdere (313636)</span><span class="sxs-lookup"><span data-stu-id="91979-120">Workflow showing duplicate place holders (313636)</span></span>

<span data-ttu-id="91979-121">Endringer i denne versjonen fjerner dupliserte plassholdere når arbeidsflytvarslinger sendes.</span><span class="sxs-lookup"><span data-stu-id="91979-121">Changes in this release eliminate duplication of placeholders when workflow notifications are sent.</span></span>

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a><span data-ttu-id="91979-122">Dimensjonsfelt blir ikke oppdatert når du bruker Åpne i Excel (176261)</span><span class="sxs-lookup"><span data-stu-id="91979-122">Dimension fields aren't updated when using "Open in Excel" (176261)</span></span>

<span data-ttu-id="91979-123">Med denne versjonen kan du nå oppdatere finansdimensjonen ved hjelp av **Åpne i Excel** fra **Arbeider**-siden.</span><span class="sxs-lookup"><span data-stu-id="91979-123">With this release, you can now update financial dimension using **Open in Excel** from the **Worker** page.</span></span> 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a><span data-ttu-id="91979-124">Arbeideradresse opprettet i Common Data Service synkroniseres ikke med Talent (317555)</span><span class="sxs-lookup"><span data-stu-id="91979-124">Worker address created in Common Data Service isn't synced to Talent (317555)</span></span>

<span data-ttu-id="91979-125">Med denne endringen blir adresser som er opprettet i Common Data Service, oppdatert i Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="91979-125">With this change, addresses created in Common Data Service are updated in Talent Core HR.</span></span>


## <a name="in-preview"></a><span data-ttu-id="91979-126">I forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="91979-126">In preview</span></span>

### <a name="new-page-to-validate-position-hierarchy-data"></a><span data-ttu-id="91979-127">Ny side for å validere stillingshierarkidata</span><span class="sxs-lookup"><span data-stu-id="91979-127">New page to validate position hierarchy data</span></span>

<span data-ttu-id="91979-128">Personale (HR) og administratorer kan nå validere lederhierarkiet for eventuelle sirkelreferanser som kan ha blitt importert ved en feiltakelse.</span><span class="sxs-lookup"><span data-stu-id="91979-128">Human resources (HR) and administrators can now validate the managerial hierarchy for any circular references that might have inadvertently been imported.</span></span> <span data-ttu-id="91979-129">Du kan få tilgang til den nye siden fra **Organisasjonsstyring > Koblinger > Stillinger > Validering av stillingshierarki**.</span><span class="sxs-lookup"><span data-stu-id="91979-129">You can access this new page from **Organizational administration > Links > Positions > Position hierarchy validation**.</span></span>

### <a name="specify-reason-codes-on-leave-types"></a><span data-ttu-id="91979-130">Angi årsakskoder for permisjonstyper</span><span class="sxs-lookup"><span data-stu-id="91979-130">Specify reason codes on leave types</span></span>

<span data-ttu-id="91979-131">Organisasjoner må kanskje ha tilleggsinformasjon om fraværsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="91979-131">Organizations might require additional information about time-off requests.</span></span> <span data-ttu-id="91979-132">Du kan nå angi årsakskoder for fraværstyper og la de ansatte velge en årsakskode i fraværsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="91979-132">You can now specify reason codes for leave types and let employees select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a><span data-ttu-id="91979-133">Kreve årsakskoder for bestemte fraværstyper i forespørsler om fravær</span><span class="sxs-lookup"><span data-stu-id="91979-133">Require reason codes for specific leave types on time-off requests</span></span>

<span data-ttu-id="91979-134">Organisasjoner kan kreve årsakskoder for bestemte fraværstyper når ansatte sender fraværsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="91979-134">Organizations might require reason codes for specific leave types when employees submit time-off requests.</span></span> <span data-ttu-id="91979-135">Dette kravet kan finnes på grunn av firmapolicy eller forskriftsmessige krav.</span><span class="sxs-lookup"><span data-stu-id="91979-135">This requirement might exist because of company policy or regulatory requirements.</span></span> <span data-ttu-id="91979-136">Du kan nå angi hvilke permisjonstyper som krever en årsakskode, og du kan kreve at ansatte angir en årsakskode for fraværstypen i forespørsler om fravær.</span><span class="sxs-lookup"><span data-stu-id="91979-136">You can now specify which leave types require a reason code, and you can require that employees provide a reason code for the leave type on their time-off requests.</span></span>

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a><span data-ttu-id="91979-137">Angi en transaksjonsliste for permisjon og fravær for HR</span><span class="sxs-lookup"><span data-stu-id="91979-137">Provide a leave and absence transaction list for HR</span></span>

<span data-ttu-id="91979-138">Muligheten for å spore ansattes fravær og forstå hvordan fravær beregnes, hjelper ikke bare HR med å svare på ansattspørsmål, men sørger også for nøyaktige fraværstildelinger for ansatte.</span><span class="sxs-lookup"><span data-stu-id="91979-138">The ability to track employee time off and understand how time off is calculated not only helps HR answer employee questions, but also helps ensure accurate time-off awards for employees.</span></span> <span data-ttu-id="91979-139">HR har nå en ny oversikt over transaksjonene (tildelinger, avsetninger, justeringer og forespørsler), slik at HR-ansatte kan vise årsakene bak saldoer.</span><span class="sxs-lookup"><span data-stu-id="91979-139">HR now has a new view into the transactions (grants, accruals, adjustments, and requests), so that HR staff can view the reasons behind balances.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="91979-140">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="91979-140">Coming soon</span></span>

### <a name="indicate-instance-type-when-provisioning-talent"></a><span data-ttu-id="91979-141">Angi forekomsttype ved klargjøring av Talent</span><span class="sxs-lookup"><span data-stu-id="91979-141">Indicate instance type when provisioning Talent</span></span>

<span data-ttu-id="91979-142">Når du klargjør en ny forekomst av Talent, vil du kunne angi om forekomsttypen er **Produksjon** eller **Sandkasse**, slik at du kan teste nye funksjoner tidlig.</span><span class="sxs-lookup"><span data-stu-id="91979-142">When provisioning a new instance of Talent, you will be able to indicate whether the instance type is **Production** or **Sandbox**, allowing for early testing of new features.</span></span> <span data-ttu-id="91979-143">Alle eksisterende Talent-forekomster vil bli oppdatert til produksjonsforekomsttypen.</span><span class="sxs-lookup"><span data-stu-id="91979-143">All existing Talent instances will be updated to the Production instance type.</span></span> <span data-ttu-id="91979-144">Hvis du vil at en av de eksisterende forekomstene skal oppdateres til forekomsttypen sandkasse, kan du kontakte kundestøtte for å starte endringsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="91979-144">If you want one of your existing instances to be updated to the Sandbox instance type, please contact Support to initiate the change request.</span></span>
