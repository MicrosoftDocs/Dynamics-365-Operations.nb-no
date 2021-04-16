---
title: Klargjøring av Microsoft Teams fra Dynamics 365 Commerce
description: Dette emnet beskriver hvordan du klargjør Microsoft Teams ved hjelp av organisasjonsdata fra Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 96382c072e03506294d72899072a358091bda8ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842722"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a><span data-ttu-id="a08f8-103">Klargjøring av Microsoft Teams fra Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a08f8-103">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="a08f8-104">Dette emnet beskriver hvordan du klargjør Microsoft Teams ved hjelp av organisasjonsdata fra Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a08f8-104">This topic describes how to provision Microsoft Teams by using organizational data from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a08f8-105">Dynamics 365 Commerce tilbyr en enkel måte å klargjøre Teams på hvis du ikke har konfigurert team for detaljhandelsbutikker der ennå.</span><span class="sxs-lookup"><span data-stu-id="a08f8-105">Dynamics 365 Commerce offers an easy way to provision Teams if you haven't yet set up teams for your retail stores there.</span></span> <span data-ttu-id="a08f8-106">Ved å dra nytte av veldefinert informasjon fra Commerce som du vil bruke i Teams, kan du hjelpe butikkansatte med å komme i gang i Teams.</span><span class="sxs-lookup"><span data-stu-id="a08f8-106">By taking advantage of well-defined information from Commerce that you want to use in Teams, you can help your store employees get started in Teams.</span></span> <span data-ttu-id="a08f8-107">Denne informasjonen omfatter organisasjonshierarkiet, butikknavnene, ansattinformasjonen og Azure Active Directory-kontoene (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="a08f8-107">This information includes the organizational hierarchy, store names, employee information, and Azure Active Directory (Azure AD) accounts.</span></span> 

<span data-ttu-id="a08f8-108">Prosessen med å klargjøre Teams har to hovedtrinn:</span><span class="sxs-lookup"><span data-stu-id="a08f8-108">The process of provisioning Teams has two main steps:</span></span>

1. <span data-ttu-id="a08f8-109">I Teams oppretter du et team for hver detaljhandelsbutikk, og legger til butikkarbeidere som medlemmer av det aktuelle teamet.</span><span class="sxs-lookup"><span data-stu-id="a08f8-109">In Teams, create a team for each retail store, and add store workers as members of the appropriate team.</span></span> <span data-ttu-id="a08f8-110">Hvis en ansatt er knyttet til mer enn én detaljhandelsbutikk, vil teammedlemskapet gjenspeile dette faktumet.</span><span class="sxs-lookup"><span data-stu-id="a08f8-110">If an employee is associated with more than one retail store, team membership will reflect that fact.</span></span> <span data-ttu-id="a08f8-111">Et kommunikasjonsteam som inneholder regionale ledere som medlemmer, vil bli opprettet for å bidra til å publisere oppgaver fra Teams.</span><span class="sxs-lookup"><span data-stu-id="a08f8-111">A communications team that includes regional managers as members will be created to help publish tasks from Teams.</span></span>
1. <span data-ttu-id="a08f8-112">Last opp organisasjonshierarkiet fra Commerce til Teams.</span><span class="sxs-lookup"><span data-stu-id="a08f8-112">Upload your organizational hierarchy from Commerce to Teams.</span></span>

## <a name="provision-teams-in-commerce-headquarters"></a><span data-ttu-id="a08f8-113">Klargjør Teams i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="a08f8-113">Provision Teams in Commerce headquarters</span></span>

<span data-ttu-id="a08f8-114">Før du klargjør Microsoft Teams, må du fullføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="a08f8-114">Before you provision Microsoft Teams, complete these tasks:</span></span>

- <span data-ttu-id="a08f8-115">Bekreft at alle regionsjefene har blitt kommunikasjonsansvarlige.</span><span class="sxs-lookup"><span data-stu-id="a08f8-115">Confirm that all regional managers have been made communications managers.</span></span>
- <span data-ttu-id="a08f8-116">Bekreft at Azure-kontoen for hver butikksjef og arbeider er knyttet til lederens eller arbeiderens arbeiderpost i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="a08f8-116">Confirm that the Azure account of every store manager and worker has been associated with that manager's or worker's worker record in Commerce headquarters.</span></span>

<span data-ttu-id="a08f8-117">Følg denne fremgangsmåten for å klargjøre Teams i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="a08f8-117">To provision Teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a08f8-118">Gå til **Retail og Commerce \> Kanaloppsett \> Konfigurasjon av Microsoft Teams-integrering**.</span><span class="sxs-lookup"><span data-stu-id="a08f8-118">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="a08f8-119">I handlingsruten velger du **Klargjør Teams**.</span><span class="sxs-lookup"><span data-stu-id="a08f8-119">On the Action Pane, select **Provision teams**.</span></span> <span data-ttu-id="a08f8-120">En satsvis jobb med navnet **Teams-klargjøring** opprettes.</span><span class="sxs-lookup"><span data-stu-id="a08f8-120">A batch job that is named **Teams provision** is created.</span></span>
1. <span data-ttu-id="a08f8-121">Gå til **Systemadministrasjon \> Forespørsler \> Satsvise jobber**, og finn den nyeste jobben som har beskrivelsen **Teams-klargjøring**.</span><span class="sxs-lookup"><span data-stu-id="a08f8-121">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="a08f8-122">Vent til denne jobben er fullført.</span><span class="sxs-lookup"><span data-stu-id="a08f8-122">Wait until this job has finished running.</span></span>

> [!TIP]
> <span data-ttu-id="a08f8-123">Hvis ingen av dine regionsjefer, butikksjefer og butikkarbeidere er tilknyttet en Teams-lisens, kan du få følgende feilmelding: "Kan ikke hente aktuelle SKU-kategorier for brukeren".</span><span class="sxs-lookup"><span data-stu-id="a08f8-123">If none of your regional managers, store managers, and store workers have been associated with a Teams license, you might receive the following error message: "Failed to retrieve appliable Sku categories for the user."</span></span> <span data-ttu-id="a08f8-124">Hvis du vil rette på problemet, velger du **Synkroniser team og medlemmer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a08f8-124">To correct the issue, select **Sync teams and members** on the Action Pane.</span></span>

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a><span data-ttu-id="a08f8-125">Valider Teams-klargjøring i Teams-administrasjonssenteret</span><span class="sxs-lookup"><span data-stu-id="a08f8-125">Validate Teams provisioning in the Teams admin center</span></span>

<span data-ttu-id="a08f8-126">Når du skal validere Microsoft Teams-klargjøring i Microsoft Teams-administrasjonssenteret, følger du fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a08f8-126">To validate Microsoft Teams provisioning in the Microsoft Teams admin center, follow these steps.</span></span>
    
1. <span data-ttu-id="a08f8-127">Gå til [Teams-administrasjonssenteret](https://admin.teams.microsoft.com/), og logg deg på som administrator for e-handel-leieren.</span><span class="sxs-lookup"><span data-stu-id="a08f8-127">Go to the [Teams admin center](https://admin.teams.microsoft.com/), and sign in as the administrator of your e-commerce tenant.</span></span>
1. <span data-ttu-id="a08f8-128">I den venstre navigasjonsruten velger du **Team** for å utvide det, og deretter velger du **Administrer team**.</span><span class="sxs-lookup"><span data-stu-id="a08f8-128">In the left navigation pane, select **Teams** to expand it, and then select **Manage teams**.</span></span>
1. <span data-ttu-id="a08f8-129">Bekreft at ett team er opprettet for hver Commerce-detaljhandelsbutikk.</span><span class="sxs-lookup"><span data-stu-id="a08f8-129">Confirm that one team has been created for each Commerce retail store.</span></span>
1. <span data-ttu-id="a08f8-130">Velg et team, og bekreft at butikkarbeidere er lagt til som medlemmer av det.</span><span class="sxs-lookup"><span data-stu-id="a08f8-130">Select a team, and confirm that store workers have been added to it as members.</span></span>
1. <span data-ttu-id="a08f8-131">Velg **Brukere** i den venstre navigasjonsruten, og bekreft at alle butikkansatte i alle butikker er lagt til som brukere.</span><span class="sxs-lookup"><span data-stu-id="a08f8-131">In the left navigation pane, select **Users**, and confirm that all store employees in all stores have been added as users.</span></span>

<span data-ttu-id="a08f8-132">Illustrasjonen nedenfor viser et eksempel på siden **Administrer team** i Teams-administrasjonssenteret.</span><span class="sxs-lookup"><span data-stu-id="a08f8-132">The following illustration shows an example of the **Manage teams** page in the Teams admin center.</span></span>

![Eksempel på siden Administrer team i Teams-administrasjonsenteret](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a><span data-ttu-id="a08f8-134">Last opp et Commerce-organisasjonshierarki i Teams</span><span class="sxs-lookup"><span data-stu-id="a08f8-134">Upload a Commerce organizational hierarchy to Teams</span></span>
    
<span data-ttu-id="a08f8-135">Commerce-organisasjonshierarkiet kan brukes i Microsoft Teams til å publisere oppgaver i alle eller utvalgte butikker som bruker den samme hierarkistrukturen.</span><span class="sxs-lookup"><span data-stu-id="a08f8-135">The Commerce organizational hierarchy can be used in Microsoft Teams to publish tasks to all or selected stores that use the same hierarchy structure.</span></span>

<span data-ttu-id="a08f8-136">Hvis du vil laste opp et Commerce-organisasjonshierarki i Teams, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="a08f8-136">To upload a Commerce organizational hierarchy to Teams, follow these steps.</span></span>
    
1. <span data-ttu-id="a08f8-137">I Commerce Headquarters, går du til **Retail og Commerce \> Kanaloppsett \> Konfigurasjon av Microsoft Teams-integrering**.</span><span class="sxs-lookup"><span data-stu-id="a08f8-137">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="a08f8-138">Velg **Last ned målrettingshierarki**, og velg deretter **Detaljhandelsbutikker etter region** for å laste ned en fil med kommaseparerte verdier (CSV-fil) med organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="a08f8-138">Select **Download targeting hierarchy**, and then select **Retail Stores by Region** to download a comma-separated values (CSV) file of the organizational hierarchy.</span></span>
1. <span data-ttu-id="a08f8-139">Installer Microsoft Teams PowerShell-modulen ved å følge trinnene i [Installer Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="a08f8-139">Install the Microsoft Teams PowerShell module by following the steps in [Install Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span></span>
1. <span data-ttu-id="a08f8-140">Når du blir spurt i Teams PowerShell-vinduet, logger du deg på med administratorkontoen for Azure AD-leieren.</span><span class="sxs-lookup"><span data-stu-id="a08f8-140">When you're prompted in the Teams PowerShell window, sign in by using the administrator account for your Azure AD tenant.</span></span>
1. <span data-ttu-id="a08f8-141">Følg trinnene i [Konfigurer målrettingshierarkiet for teamet](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) for å laste opp CSV-filen for målrettingshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="a08f8-141">Follow the steps in [Set up your team targeting hierarchy](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) to upload the CSV file for the targeting hierarchy.</span></span>

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a><span data-ttu-id="a08f8-142">Kontroller at organisasjonshierarkiet ble lastet opp til Teams</span><span class="sxs-lookup"><span data-stu-id="a08f8-142">Verify that the organizational hierarchy was uploaded to Teams</span></span>

<span data-ttu-id="a08f8-143">Følg trinnene nedenfor for å kontroller at organisasjonshierarkiet ble lastet opp til Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="a08f8-143">To verify that the organizational hierarchy was uploaded to Microsoft Teams, follow these steps.</span></span>

1. <span data-ttu-id="a08f8-144">Logg deg på Teams som en kommunikasjonsleder.</span><span class="sxs-lookup"><span data-stu-id="a08f8-144">Sign in to Teams as a communications manager.</span></span>
1. <span data-ttu-id="a08f8-145">Velg **Oppgaver etter planlegger** i den venstre navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="a08f8-145">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="a08f8-146">På fanen **Publiserte lister** oppretter du en ny liste som har en testoppgave.</span><span class="sxs-lookup"><span data-stu-id="a08f8-146">On the **Published lists** tab, create a new list that has a dummy task.</span></span>
1. <span data-ttu-id="a08f8-147">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="a08f8-147">Select **Publish**.</span></span> <span data-ttu-id="a08f8-148">Organisasjonshierarkiet skal vises i dialogboksen **Velg hvem det skal publiseres til**, som vist i eksemplet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a08f8-148">The organizational hierarchy should appear in the **Select who to publish to** dialog box, as shown in the example in the following illustration.</span></span>

![Eksempel på et organisasjonshierarki i dialogboksen Velg hvem det skal publiseres til](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a><span data-ttu-id="a08f8-150">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a08f8-150">Additional resources</span></span>

[<span data-ttu-id="a08f8-151">Oversikt over Dynamics 365 Commerce- og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="a08f8-151">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="a08f8-152">Aktiver Dynamics 365 Commerce- og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="a08f8-152">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="a08f8-153">Synkroniser oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="a08f8-153">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="a08f8-154">Behandle brukerroller i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a08f8-154">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="a08f8-155">Tilordne butikker og grupper hvis det finnes eksisterende grupper i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a08f8-155">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="a08f8-156">Vanlige spørsmål om Dynamics 365 Commerce- og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="a08f8-156">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
