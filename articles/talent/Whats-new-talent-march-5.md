---
title: Hva er nytt eller endret i Dynamics 365 for Talent (5. mars 2019)?
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
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
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fe24846ab98a75d474df045a62a72bfc41c64866
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741896"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-5-2019"></a><span data-ttu-id="90ab6-103">Hva er nytt eller endret i Dynamics 365 for Talent (5. mars 2019)?</span><span class="sxs-lookup"><span data-stu-id="90ab6-103">What's new or changed in Dynamics 365 for Talent (March 5, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="90ab6-104">Dette emnet beskriver funksjoner som enten er nye eller endret i Talent</span><span class="sxs-lookup"><span data-stu-id="90ab6-104">This topic describes features that are either new or changed in Talent</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="90ab6-105">Endringer i Attract</span><span class="sxs-lookup"><span data-stu-id="90ab6-105">Changes in Attract</span></span>

### <a name="extending-option-sets-in-attract"></a><span data-ttu-id="90ab6-106">Utvide alternativsett i Attract</span><span class="sxs-lookup"><span data-stu-id="90ab6-106">Extending option sets in Attract</span></span>

<span data-ttu-id="90ab6-107">I Attract finnes det flere felt som er alternativsett i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="90ab6-107">In Attract, there are multiple fields that are option sets within the Common Data Service.</span></span> <span data-ttu-id="90ab6-108">Nye funksjoner er lansert for å utvide alternativsettene og begynner med **Avslag**-årsaksfeltet, **Ansettelsestype**-feltet og **Ansiennitetstype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="90ab6-108">New capabilities have been introduced to extend the option sets, beginning with the **Rejection** reason field, **Employment type** field, and **Seniority type** field.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="90ab6-109">Jobbposteringen til LinkedIn-funksjonaliteten krever bruk av feltene **Ansettelsestype** og **Ansiennitetstype** på siden **Jobbdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="90ab6-109">The job posting to LinkedIn functionality requires the use of the **Employment type** and **Seniority type** fields on the **Job details** page.</span></span> <span data-ttu-id="90ab6-110">Standardverdiene i disse feltene støttes av LinkedIn og vises når jobben posteres.</span><span class="sxs-lookup"><span data-stu-id="90ab6-110">The default values in these fields are supported by LinkedIn and are displayed when the job is posted.</span></span> <span data-ttu-id="90ab6-111">Hvis du posterer jobber i LinkedIn og endrer de eksisterende alternativsettverdiene for disse feltene, vil jobben fortsatt posteres, men LinkedIn vil ikke vise de egendefinerte **Ansettelsestype**- og **Ansiennitetstype**-verdiene.</span><span class="sxs-lookup"><span data-stu-id="90ab6-111">If you are posting jobs to LinkedIn and you modify the existing option set values for these fields, the job will still post, but LinkedIn will not display the custom **Employment type** and **Seniority type** values.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="90ab6-112">Endringer i jobbintroduksjon</span><span class="sxs-lookup"><span data-stu-id="90ab6-112">Changes in Onboarding</span></span>

### <a name="private-preview-for-onboard-teams"></a><span data-ttu-id="90ab6-113">Privat forhåndsvisning for jobbintroduksjonsteam</span><span class="sxs-lookup"><span data-stu-id="90ab6-113">Private preview for Onboard teams</span></span>
<span data-ttu-id="90ab6-114">Du kan nå enkelt dele og samarbeide om maler på tvers av hele organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="90ab6-114">You can now easily share and collaborate on templates across your entire organization.</span></span> <span data-ttu-id="90ab6-115">Hvis du vil ha mer informasjon, se [Dele gode fremgangsmåter i hele organisasjonen ved hjelp av jobbintroduksjonsteam](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span><span class="sxs-lookup"><span data-stu-id="90ab6-115">For more information, see [Share best practices across your organization using Onboard Teams](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span></span>

### <a name="private-preview-for-assignee-placeholders"></a><span data-ttu-id="90ab6-116">Privat forhåndsvisning for tilordnetplassholdere</span><span class="sxs-lookup"><span data-stu-id="90ab6-116">Private preview for assignee placeholders</span></span>
<span data-ttu-id="90ab6-117">Du kan berike malene ved å tilordne aktiviteter til roller i stedet for enkeltpersoner.</span><span class="sxs-lookup"><span data-stu-id="90ab6-117">You can enrich your templates by assigning activities to roles instead of individuals.</span></span> <span data-ttu-id="90ab6-118">Roller tilordnes deretter til enkeltpersoner ved oppretting av veiledningen.</span><span class="sxs-lookup"><span data-stu-id="90ab6-118">Roles are then assigned to individuals at the time of guide creation.</span></span> <span data-ttu-id="90ab6-119">Hvis du vil ha mer informasjon, se [Strømlinjeforme veiledningsadministrasjon ved å tilordne aktiviteter til roller](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span><span class="sxs-lookup"><span data-stu-id="90ab6-119">For more information, see [Streamline guide administration by assigning activities to roles](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="90ab6-120">Endringer i Core HR</span><span class="sxs-lookup"><span data-stu-id="90ab6-120">Changes in Core HR</span></span>
<span data-ttu-id="90ab6-121">**Build 8.1.2178**</span><span class="sxs-lookup"><span data-stu-id="90ab6-121">**Build 8.1.2178**</span></span>

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a><span data-ttu-id="90ab6-122">Konfigurere arbeidsflyt til å automatisk godkjenne eller følge arbeidsflyten når en HR- eller linjeleder sender eller oppdaterer fraværsforespørsler</span><span class="sxs-lookup"><span data-stu-id="90ab6-122">Configure workflow to auto-approve or follow workflow when an HR or line manager submits or updates time off requests</span></span>
<span data-ttu-id="90ab6-123">Nye arbeidsflytbetingelser er lagt til for å tillate automatisk godkjenning av fraværsforespørsler hvis de sendes av en ansatts leder eller HR.</span><span class="sxs-lookup"><span data-stu-id="90ab6-123">New workflow conditions have been added to allow for leave requests to be automatically approved if submitted by an employee’s manager or by HR.</span></span> <span data-ttu-id="90ab6-124">Én måte å oppnå denne automatiske godkjenningen i en arbeidsflyt på, er å aktivere en automatisk handling i arbeidsflyten for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="90ab6-124">One way to achieve this auto-approval on a workflow is to enable an automatic action on the workflow approval.</span></span>

<span data-ttu-id="90ab6-125">Betingelsene som er lagt til, inkluderer:</span><span class="sxs-lookup"><span data-stu-id="90ab6-125">The conditions that have been added include:</span></span>

- <span data-ttu-id="90ab6-126">Sendt av – Brukes til å evaluere systembruker-IDen til brukeren som sendte forespørselen til arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="90ab6-126">Submitted by - Used to evaluate the system user ID of the user who submitted the request to workflow.</span></span>
- <span data-ttu-id="90ab6-127">Sendt på vegne av – Brukes til å evaluere hvis fraværsforespørselen ble sendt på vegne av arbeideren som er knyttet til forespørselen.</span><span class="sxs-lookup"><span data-stu-id="90ab6-127">Submitted on behalf of - Used to evaluate if the leave request was submitted on behalf of the worker associated to the request.</span></span>
- <span data-ttu-id="90ab6-128">Sendt av personal – Brukes til å evaluere hvis systembrukeren som sendte forespørselen til arbeidsflyt, har en HR-rolle.</span><span class="sxs-lookup"><span data-stu-id="90ab6-128">Submitted by human resources - Used to evaluate if the system user who submitted the request to workflow is in a Human Resources role.</span></span>
- <span data-ttu-id="90ab6-129">Sendt av leder – Brukes til å evaluere hvis brukeren som sendte fraværsforespørselen til arbeidsflyten, er en linjehierarkileder for arbeideren som er knyttet til forespørselen.</span><span class="sxs-lookup"><span data-stu-id="90ab6-129">Submitted by manager - Used to evaluate if the user who submitted the leave request to workflow is a line hierarchy manager of the worker associated to the request.</span></span>

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a><span data-ttu-id="90ab6-130">Aktivere fast kompensasjon for ansatte for fremtidige stillingstilordninger</span><span class="sxs-lookup"><span data-stu-id="90ab6-130">Enable employee fixed compensation for future position assignments</span></span>
<span data-ttu-id="90ab6-131">Det er vanlig for ansatte å delta i en organisasjon med en fremtidig startdato.</span><span class="sxs-lookup"><span data-stu-id="90ab6-131">It is typical for employees to join an organization with a future start date.</span></span> <span data-ttu-id="90ab6-132">Med denne endringen er det mulig å definere fast kompensasjon for ansatte med fremtidige stillingstilordninger.</span><span class="sxs-lookup"><span data-stu-id="90ab6-132">This change enables defining fixed compensation for employees with future position assignments.</span></span>

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a><span data-ttu-id="90ab6-133">Lønnsfeltene for stillingen er tomme når plasseringen redigeres</span><span class="sxs-lookup"><span data-stu-id="90ab6-133">Position Payroll fields are blank when editing the position</span></span>
<span data-ttu-id="90ab6-134">Med denne endringen, når du ber om endringer i eksisterende stillinger, vil lønnsfeltene nå som standard gå til gjeldende verdier.</span><span class="sxs-lookup"><span data-stu-id="90ab6-134">With this change, when requesting changes to existing positions, the payroll fields will now default to the current values.</span></span>

### <a name="other-miscellaneous-bug-fixes"></a><span data-ttu-id="90ab6-135">Andre feilrettinger</span><span class="sxs-lookup"><span data-stu-id="90ab6-135">Other miscellaneous bug fixes</span></span>
<span data-ttu-id="90ab6-136">Andre mindre feilrettinger er inkludert i denne utgivelsen.</span><span class="sxs-lookup"><span data-stu-id="90ab6-136">Other minor bug fixes are included with this release.</span></span>

### <a name="upgrade-to-common-data-service"></a><span data-ttu-id="90ab6-137">Oppgradere til Common Data Service</span><span class="sxs-lookup"><span data-stu-id="90ab6-137">Upgrade to Common Data Service</span></span>
<span data-ttu-id="90ab6-138">Tidsfrister for å oppgradere til Common Data Service nærmer deg raskt.</span><span class="sxs-lookup"><span data-stu-id="90ab6-138">Deadlines to upgrade to Common Data Service are quickly approaching.</span></span> <span data-ttu-id="90ab6-139">Logg på PowerApps-administrasjonssenteret for å bestemme om databasen må oppgraderes.</span><span class="sxs-lookup"><span data-stu-id="90ab6-139">Sign in to the PowerApps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="90ab6-140">Hvis du vil ha mer informasjon om tidsfrister og de nødvendige trinnene for å oppgradere, kan du se [Oppgradere til Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span><span class="sxs-lookup"><span data-stu-id="90ab6-140">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="90ab6-141">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="90ab6-141">Coming soon</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="90ab6-142">Avansert kompensasjonssikkerhet (fast og variabel)</span><span class="sxs-lookup"><span data-stu-id="90ab6-142">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="90ab6-143">I mange organisasjoner har kompensasjons- og fordelsansvarlige bare tilgang til bestemte kompensasjonsposter, for eksempel poster for ledere eller regionsbaserte ansatte.</span><span class="sxs-lookup"><span data-stu-id="90ab6-143">In many organizations, compensation and benefits managers can only access certain compensation records, such as records for executives or regional-based employees.</span></span> <span data-ttu-id="90ab6-144">Med denne endringen kan du administrere og vedlikeholde kompensasjonsplanene for ulike ansattgrupper i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="90ab6-144">With this change, you can manage and maintain the compensation plans for different employee populations in the organization.</span></span> <span data-ttu-id="90ab6-145">Faste og variable planer kan tilordnes til sikkerhetsroller, som bestemmer tilgangen til planene og ansattdataene som er knyttet til dem, for eksempel lønns- eller bonusposter.</span><span class="sxs-lookup"><span data-stu-id="90ab6-145">Fixed and variable plans can be assigned security roles, which will determine the access to the plans and the employee data related to the plans, such as salary or bonus records.</span></span> <span data-ttu-id="90ab6-146">Bare rollene som har den rette tilgangen, vil kunne behandle kompensasjon for disse ansatte.</span><span class="sxs-lookup"><span data-stu-id="90ab6-146">Only the roles with the given access will be able to process compensation for those employees.</span></span>

###  <a name="platform-update-24"></a><span data-ttu-id="90ab6-147">Plattform update 24</span><span class="sxs-lookup"><span data-stu-id="90ab6-147">Platform update 24</span></span>
<span data-ttu-id="90ab6-148">Hvis du vil ha mer informasjon om Plattformoppdatering 24, kan du se [Hva er nytt eller endret i Finance and Operations Plattformoppdatering 24 (mars 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="90ab6-148">For additional details about Platform update 24, see [What's new or changed in Finance and Operations platform update 24 (March 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span></span>
