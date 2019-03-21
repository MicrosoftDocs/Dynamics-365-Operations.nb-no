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
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6b490a696dc0a00c47e56f57373f330d0e53dde
ms.sourcegitcommit: 479b8cda7e411830bf1f579fab3692c980dcf850
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "782965"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-5-2019"></a><span data-ttu-id="5c4b9-103">Hva er nytt eller endret i Dynamics 365 for Talent (5. mars 2019)?</span><span class="sxs-lookup"><span data-stu-id="5c4b9-103">What's new or changed in Dynamics 365 for Talent (March 5, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5c4b9-104">Dette emnet beskriver funksjoner som enten er nye eller endret i Talent</span><span class="sxs-lookup"><span data-stu-id="5c4b9-104">This topic describes features that are either new or changed in Talent</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="5c4b9-105">Endringer i Attract</span><span class="sxs-lookup"><span data-stu-id="5c4b9-105">Changes in Attract</span></span>

### <a name="extending-option-sets-in-attract"></a><span data-ttu-id="5c4b9-106">Utvide alternativsett i Attract</span><span class="sxs-lookup"><span data-stu-id="5c4b9-106">Extending option sets in Attract</span></span>

<span data-ttu-id="5c4b9-107">I Attract finnes det flere felt som er alternativsett i Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="5c4b9-107">In Attract, there are multiple fields that are option sets within the Common Data Service (CDS).</span></span> <span data-ttu-id="5c4b9-108">Nye funksjoner er lansert for å utvide alternativsettene og begynner med **Avslag**-årsaksfeltet, **Ansettelsestype**-feltet og **Ansiennitetstype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-108">New capabilities have been introduced to extend the option sets, beginning with the **Rejection** reason field, **Employment type** field, and **Seniority type** field.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5c4b9-109">Jobbposteringen til LinkedIn-funksjonaliteten krever bruk av feltene **Ansettelsestype** og **Ansiennitetstype** på siden **Jobbdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-109">The job posting to LinkedIn functionality requires the use of the **Employment type** and **Seniority type** fields on the **Job details** page.</span></span> <span data-ttu-id="5c4b9-110">Standardverdiene i disse feltene støttes av LinkedIn og vises når jobben posteres.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-110">The default values in these fields are supported by LinkedIn and are displayed when the job is posted.</span></span> <span data-ttu-id="5c4b9-111">Hvis du posterer jobber i LinkedIn og endrer de eksisterende alternativsettverdiene for disse feltene, vil jobben fortsatt posteres, men LinkedIn vil ikke vise de egendefinerte **Ansettelsestype**- og **Ansiennitetstype**-verdiene.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-111">If you are posting jobs to LinkedIn and you modify the existing option set values for these fields, the job will still post, but LinkedIn will not display the custom **Employment type** and **Seniority type** values.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="5c4b9-112">Endringer i jobbintroduksjon</span><span class="sxs-lookup"><span data-stu-id="5c4b9-112">Changes in Onboarding</span></span>

### <a name="private-preview-for-onboard-teams"></a><span data-ttu-id="5c4b9-113">Privat forhåndsvisning for jobbintroduksjonsteam</span><span class="sxs-lookup"><span data-stu-id="5c4b9-113">Private preview for Onboard teams</span></span>
<span data-ttu-id="5c4b9-114">Du kan nå enkelt dele og samarbeide om maler på tvers av hele organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-114">You can now easily share and collaborate on templates across your entire organization.</span></span> <span data-ttu-id="5c4b9-115">Hvis du vil ha mer informasjon, se [Dele gode fremgangsmåter i hele organisasjonen ved hjelp av jobbintroduksjonsteam](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span><span class="sxs-lookup"><span data-stu-id="5c4b9-115">For more information, see [Share best practices across your organization using Onboard Teams](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span></span>

### <a name="private-preview-for-assignee-placeholders"></a><span data-ttu-id="5c4b9-116">Privat forhåndsvisning for tilordnetplassholdere</span><span class="sxs-lookup"><span data-stu-id="5c4b9-116">Private preview for assignee placeholders</span></span>
<span data-ttu-id="5c4b9-117">Du kan berike malene ved å tilordne aktiviteter til roller i stedet for enkeltpersoner.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-117">You can enrich your templates by assigning activities to roles instead of individuals.</span></span> <span data-ttu-id="5c4b9-118">Roller tilordnes deretter til enkeltpersoner ved oppretting av veiledningen.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-118">Roles are then assigned to individuals at the time of guide creation.</span></span> <span data-ttu-id="5c4b9-119">Hvis du vil ha mer informasjon, se [Strømlinjeforme veiledningsadministrasjon ved å tilordne aktiviteter til roller](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span><span class="sxs-lookup"><span data-stu-id="5c4b9-119">For more information, see [Streamline guide administration by assigning activities to roles](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="5c4b9-120">Endringer i Core HR</span><span class="sxs-lookup"><span data-stu-id="5c4b9-120">Changes in Core HR</span></span>
<span data-ttu-id="5c4b9-121">**Build 8.1.2178**</span><span class="sxs-lookup"><span data-stu-id="5c4b9-121">**Build 8.1.2178**</span></span>

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a><span data-ttu-id="5c4b9-122">Konfigurere arbeidsflyt til å automatisk godkjenne eller følge arbeidsflyten når en HR- eller linjeleder sender eller oppdaterer fraværsforespørsler</span><span class="sxs-lookup"><span data-stu-id="5c4b9-122">Configure workflow to auto-approve or follow workflow when an HR or line manager submits or updates time off requests</span></span>
<span data-ttu-id="5c4b9-123">Nye arbeidsflytbetingelser er lagt til for å tillate automatisk godkjenning av fraværsforespørsler hvis de sendes av en ansatts leder eller HR.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-123">New workflow conditions have been added to allow for leave requests to be automatically approved if submitted by an employee’s manager or by HR.</span></span> <span data-ttu-id="5c4b9-124">Én måte å oppnå denne automatiske godkjenningen i en arbeidsflyt på, er å aktivere en automatisk handling i arbeidsflyten for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-124">One way to achieve this auto-approval on a workflow is to enable an automatic action on the workflow approval.</span></span>

<span data-ttu-id="5c4b9-125">Betingelsene som er lagt til, inkluderer:</span><span class="sxs-lookup"><span data-stu-id="5c4b9-125">The conditions that have been added include:</span></span>

- <span data-ttu-id="5c4b9-126">Sendt av – Brukes til å evaluere systembruker-IDen til brukeren som sendte forespørselen til arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-126">Submitted by - Used to evaluate the system user ID of the user who submitted the request to workflow.</span></span>
- <span data-ttu-id="5c4b9-127">Sendt på vegne av – Brukes til å evaluere hvis fraværsforespørselen ble sendt på vegne av arbeideren som er knyttet til forespørselen.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-127">Submitted on behalf of - Used to evaluate if the leave request was submitted on behalf of the worker associated to the request.</span></span>
- <span data-ttu-id="5c4b9-128">Sendt av personal – Brukes til å evaluere hvis systembrukeren som sendte forespørselen til arbeidsflyt, har en HR-rolle.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-128">Submitted by human resources - Used to evaluate if the system user who submitted the request to workflow is in a Human Resources role.</span></span>
- <span data-ttu-id="5c4b9-129">Sendt av leder – Brukes til å evaluere hvis brukeren som sendte fraværsforespørselen til arbeidsflyten, er en linjehierarkileder for arbeideren som er knyttet til forespørselen.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-129">Submitted by manager - Used to evaluate if the user who submitted the leave request to workflow is a line hierarchy manager of the worker associated to the request.</span></span>

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a><span data-ttu-id="5c4b9-130">Aktivere fast kompensasjon for ansatte for fremtidige stillingstilordninger</span><span class="sxs-lookup"><span data-stu-id="5c4b9-130">Enable employee fixed compensation for future position assignments</span></span>
<span data-ttu-id="5c4b9-131">Det er vanlig for ansatte å delta i en organisasjon med en fremtidig startdato.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-131">It is typical for employees to join an organization with a future start date.</span></span> <span data-ttu-id="5c4b9-132">Med denne endringen er det mulig å definere fast kompensasjon for ansatte med fremtidige stillingstilordninger.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-132">This change enables defining fixed compensation for employees with future position assignments.</span></span>

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a><span data-ttu-id="5c4b9-133">Lønnsfeltene for stillingen er tomme når plasseringen redigeres</span><span class="sxs-lookup"><span data-stu-id="5c4b9-133">Position Payroll fields are blank when editing the position</span></span>
<span data-ttu-id="5c4b9-134">Med denne endringen, når du ber om endringer i eksisterende stillinger, vil lønnsfeltene nå som standard gå til gjeldende verdier.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-134">With this change, when requesting changes to existing positions, the payroll fields will now default to the current values.</span></span>

### <a name="other-miscellaneous-bug-fixes"></a><span data-ttu-id="5c4b9-135">Andre feilrettinger</span><span class="sxs-lookup"><span data-stu-id="5c4b9-135">Other miscellaneous bug fixes</span></span>
<span data-ttu-id="5c4b9-136">Andre mindre feilrettinger er inkludert i denne utgivelsen.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-136">Other minor bug fixes are included with this release.</span></span>

### <a name="upgrade-to-cds-for-apps"></a><span data-ttu-id="5c4b9-137">Oppgradering til CDS for Apps</span><span class="sxs-lookup"><span data-stu-id="5c4b9-137">Upgrade to CDS for Apps</span></span>
<span data-ttu-id="5c4b9-138">Tidsfrister for å oppgradere til CD for Apps nærmer deg raskt.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-138">Deadlines to upgrade to CDS for Apps are quickly approaching.</span></span> <span data-ttu-id="5c4b9-139">Logg på PowerApps-administrasjonssenteret for å bestemme om databasen må oppgraderes.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-139">Sign in to the PowerApps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="5c4b9-140">Hvis du vil ha mer informasjon om tidsfrister og de nødvendige trinnene for å oppgradere, kan du se [Oppgradere til Common Data Service for Apps](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).</span><span class="sxs-lookup"><span data-stu-id="5c4b9-140">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service for Apps](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="5c4b9-141">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="5c4b9-141">Coming soon</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="5c4b9-142">Avansert kompensasjonssikkerhet (fast og variabel)</span><span class="sxs-lookup"><span data-stu-id="5c4b9-142">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="5c4b9-143">I mange organisasjoner har kompensasjons- og fordelsansvarlige bare tilgang til bestemte kompensasjonsposter, for eksempel poster for ledere eller regionsbaserte ansatte.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-143">In many organizations, compensation and benefits managers can only access certain compensation records, such as records for executives or regional-based employees.</span></span> <span data-ttu-id="5c4b9-144">Med denne endringen kan du administrere og vedlikeholde kompensasjonsplanene for ulike ansattgrupper i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-144">With this change, you can manage and maintain the compensation plans for different employee populations in the organization.</span></span> <span data-ttu-id="5c4b9-145">Faste og variable planer kan tilordnes til sikkerhetsroller, som bestemmer tilgangen til planene og ansattdataene som er knyttet til dem, for eksempel lønns- eller bonusposter.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-145">Fixed and variable plans can be assigned security roles, which will determine the access to the plans and the employee data related to the plans, such as salary or bonus records.</span></span> <span data-ttu-id="5c4b9-146">Bare rollene som har den rette tilgangen, vil kunne behandle kompensasjon for disse ansatte.</span><span class="sxs-lookup"><span data-stu-id="5c4b9-146">Only the roles with the given access will be able to process compensation for those employees.</span></span>

###  <a name="platform-update-24"></a><span data-ttu-id="5c4b9-147">Plattform update 24</span><span class="sxs-lookup"><span data-stu-id="5c4b9-147">Platform update 24</span></span>
<span data-ttu-id="5c4b9-148">Hvis du vil ha mer informasjon om Plattformoppdatering 24, kan du se [Hva er nytt eller endret i Finance and Operations Plattformoppdatering 24 (mars 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="5c4b9-148">For additional details about Platform update 24, see [What's new or changed in Finance and Operations platform update 24 (March 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span></span>
