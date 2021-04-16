---
title: Tillegg for lagersynlighet
description: Dette emnet beskriver hvordan du installerer og konfigurerer tillegget for lagersynlighet for Dynamics 365 Supply Chain Management.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: e294ada8dd3e764987aa363adb2614416986575b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821135"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="ed9c3-103">Tillegg for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="ed9c3-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="ed9c3-104">Tillegget for lagersynlighet er en uavhengig og høyt skalerbar mikrotjeneste som aktiverer beholdningssporing i sanntid, og gir dermed en global visning av lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="ed9c3-105">All informasjon som er relatert til lagerbeholdningen, eksporteres til tjenesten via i SQL-integrasjon med minimal forsinkelse.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="ed9c3-106">Eksterne systemer får tilgang til tjenesten via RESTful-API-er for spørring om lagerbeholdningsinformasjon for gitte sett med dimensjoner, og dermed hente en liste over tilgjengelige lagerbeholdninger.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="ed9c3-107">Lagersynlighet er en mikrotjeneste som er bygd på Microsoft Dataverse, som betyr at du kan utvide den ved å bygge Power Apps og bruke Power BI til å oppgi egendefinert funksjonalitet som dekker dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="ed9c3-108">Det er også mulig å oppgradere indeksen for å utføre lagerspørringer.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="ed9c3-109">Lagersynlighet inneholder konfigurasjonsalternativer som gjør at den kan integreres med flere tredjepartssystemer.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="ed9c3-110">Den støtter den standardiserte lagerdimensjonen, egendefinert utvidelse og standardisert beregnet antall som kan konfigureres.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="ed9c3-111">Dette emnet beskriver hvordan du installerer og konfigurerer tillegget for lagersynlighet for Dynamics 365 Supply Chain Management, og hvordan du bruker app-programmeringsgrensesnittet (API).</span><span class="sxs-lookup"><span data-stu-id="ed9c3-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="ed9c3-112">Installer tillegget for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="ed9c3-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="ed9c3-113">Du må installere tillegget for lagersynlighet ved hjelp av Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ed9c3-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="ed9c3-114">LCS er en samarbeidsportal som gir et miljø og et sett med jevnlig oppdaterte tjenester som hjelper deg med å administrere applivssyklusen til Dynamics 365 Finance and Operations-appene dine.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="ed9c3-115">Hvis du vil ha mer informasjon, se [Lifecycle Services-ressurser](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="ed9c3-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ed9c3-116">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="ed9c3-116">Prerequisites</span></span>

<span data-ttu-id="ed9c3-117">Før du kan installere tillegget for lagersynlighet, må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="ed9c3-118">Hent et LCS-implementeringsprosjekt med minst ett miljø som er distribuert.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="ed9c3-119">Sørg for at forutsetningene for å definere tillegg som er oppført i [Tilleggsoversikt](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md), er fullført.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="ed9c3-120">Lagersynlighet krever ikke kobling til dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="ed9c3-121">Kontakt lagersynlighetsteamet på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for å få følgende tre obligatoriske filer:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>

    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="ed9c3-122">`Inventory Visibility Integration.zip` (hvis versjonen av Supply Chain Management du kjører, er eldre enn versjon 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="ed9c3-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>

> [!NOTE]
> <span data-ttu-id="ed9c3-123">Landene og områdene som støttes for øyeblikket, omfatter Canada, USA og Den europeiske union (EU).</span><span class="sxs-lookup"><span data-stu-id="ed9c3-123">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="ed9c3-124">Hvis du har spørsmål om disse forutsetningene, kan du ta kontakt med produktteamet for lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-124">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="ed9c3-125">Konfigurere Dataverse</span><span class="sxs-lookup"><span data-stu-id="ed9c3-125">Set up Dataverse</span></span>

<span data-ttu-id="ed9c3-126">Gjør følgende for å konfigurere Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-126">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="ed9c3-127">Legg til et serviceprinsipp i leieren:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-127">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="ed9c3-128">Installer Azure AD PowerShell-modul v2 som beskrevet i [Installer Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="ed9c3-128">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="ed9c3-129">Kjør følgende PowerShell-kommando.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-129">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="ed9c3-130">Opprett en applikasjonsbruker for lagersynlighet i Dataverse:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-130">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="ed9c3-131">Åpne URL-adressen for Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-131">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="ed9c3-132">Gå til **Avansert innstilling \> System \> Sikkerhet \> Brukere** og opporett en appbruker.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-132">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="ed9c3-133">Bruk Vis-menyen til å endre sidevisningen til **Appbrukere**.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-133">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="ed9c3-134">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-134">Select **New**.</span></span> <span data-ttu-id="ed9c3-135">Sett app-ID-en til *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-135">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="ed9c3-136">(Objekt-ID-en lastes automatisk når du lagrer endringene.) Du kan tilpasse navnet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-136">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="ed9c3-137">Du kan for eksempel endre til *Lagersynlighet*.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-137">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="ed9c3-138">Når du er ferdig, velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-138">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="ed9c3-139">Velg **Tilordne rolle**, og velg deretter **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-139">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="ed9c3-140">Hvis det finnes en rolle kalt **Common Data Service-bruker**, velger du den også.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-140">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="ed9c3-141">Hvis du vil ha mer informasjon, kan du se [Opprette en appbruker](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="ed9c3-141">For more information, see [Create an application user](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="ed9c3-142">Importer `Inventory Visibility Dataverse Solution.zip`-filen, som inkluderer relaterte enheter for konfigurasjon av Dataverse og Power Apps:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-142">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="ed9c3-143">Gå til siden **Løsninger**.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-143">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="ed9c3-144">Velg **Import**.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-144">Select **Import**.</span></span>

1. <span data-ttu-id="ed9c3-145">Importer utløserflyten for konfigurasjonsoppgradering:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-145">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="ed9c3-146">Gå til Microsoft Flow-siden.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-146">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="ed9c3-147">Sørg for at det finnes en tilkobling med navnet *Dataverse (eldre)*.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-147">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="ed9c3-148">(Hvis den ikke finnes, kan du opprette den.)</span><span class="sxs-lookup"><span data-stu-id="ed9c3-148">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="ed9c3-149">Importer `Inventory Visibility Configuration Trigger.zip`-filen.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-149">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="ed9c3-150">Når den er importert, vises utløseren under **Mine flyter**.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-150">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="ed9c3-151">Initialiser følgende fire variabler basert på miljøinformasjon:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-151">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="ed9c3-152">Leier-ID for Azure</span><span class="sxs-lookup"><span data-stu-id="ed9c3-152">Azure Tenant ID</span></span>
        - <span data-ttu-id="ed9c3-153">Appklient-ID for Azure</span><span class="sxs-lookup"><span data-stu-id="ed9c3-153">Azure Application Client ID</span></span>
        - <span data-ttu-id="ed9c3-154">Appklienthemmelighet for Azure</span><span class="sxs-lookup"><span data-stu-id="ed9c3-154">Azure Application Client Secret</span></span>
        - <span data-ttu-id="ed9c3-155">Endepunkt for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="ed9c3-155">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="ed9c3-156">Hvis du vil ha mer informasjon om denne variabelen, kan du se delen [Konfigurere integrering av lagersynlighet](#setup-inventory-visibility-integration) senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-156">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="ed9c3-157">![Konfigurasjonsutløser](media/configuration-trigger.png "Konfigurasjonsutløser")</span><span class="sxs-lookup"><span data-stu-id="ed9c3-157">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="ed9c3-158">Velg **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-158">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="ed9c3-159">Installer tillegget</span><span class="sxs-lookup"><span data-stu-id="ed9c3-159">Install the add-in</span></span>

<span data-ttu-id="ed9c3-160">Hvis du vil installere tillegget for lagersynlighet, må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-160">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="ed9c3-161">Logg på [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index)-portalen.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-161">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="ed9c3-162">På hjemmesiden velger du prosjektet der miljøet er distribuert.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-162">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="ed9c3-163">På prosjektsiden velger du miljøet du vil installere tillegget i.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-163">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="ed9c3-164">På miljøsiden ruller du ned til du ser delen delen **Miljøtillegg** i delen **Power Platform-integrering**, der du også finner navnet på Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-164">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="ed9c3-165">I delen **Miljøtillegg** velger du **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-165">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="ed9c3-166">![Miljøsiden i LCS](media/inventory-visibility-environment.png "Miljøsiden i LCS")</span><span class="sxs-lookup"><span data-stu-id="ed9c3-166">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="ed9c3-167">Velg koblingen **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-167">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="ed9c3-168">En liste over tilgjengelige tillegg åpnes.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-168">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="ed9c3-169">Velg **Lagersynlighet** i listen.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-169">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="ed9c3-170">Angi verdier for følgende felter i miljøet:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-170">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="ed9c3-171">**ID for AAD-app (klient)**</span><span class="sxs-lookup"><span data-stu-id="ed9c3-171">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="ed9c3-172">**Leier-ID for AAD**</span><span class="sxs-lookup"><span data-stu-id="ed9c3-172">**AAD tenant ID**</span></span>

    <span data-ttu-id="ed9c3-173">![Legg til i konfigurasjon-side](media/inventory-visibility-setup.png "Legg til i konfigurasjon-side")</span><span class="sxs-lookup"><span data-stu-id="ed9c3-173">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="ed9c3-174">Godta vilkåret og betingelsen ved å merke av for **Vilkår og betingelser**.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-174">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="ed9c3-175">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-175">Select **Install**.</span></span> <span data-ttu-id="ed9c3-176">Statusen for tillegget vil vises som **Installerer**.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-176">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="ed9c3-177">Når du er ferdig, oppdaterer du siden for å se status endre til **Installert**.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-177">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="ed9c3-178">Avinstallere tillegget</span><span class="sxs-lookup"><span data-stu-id="ed9c3-178">Uninstall the add-in</span></span>

<span data-ttu-id="ed9c3-179">Velg **Avinstaller** tillegget for å avinstallere tillegget.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-179">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="ed9c3-180">Når du oppdaterer LCS, fjernes tillegget for lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-180">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="ed9c3-181">Avinstallasjonsprosessen fjerner registreringen av tillegget, og starter også en jobb for å rydde opp i alle forretningsdataene som er lagret i tjenesten.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-181">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="ed9c3-182">Bruke lagerbeholdningsdata fra Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ed9c3-182">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="ed9c3-183">Distribuere integreringspakken for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="ed9c3-183">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="ed9c3-184">Hvis du kjører Supply Chain Management versjon 10.0.17 eller tidligere, kan du kontakte kundestøttegruppen for lagersynlighet på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for å hente pakkefilen.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-184">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="ed9c3-185">Deretter distribuerer du pakken i LCS.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-185">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="ed9c3-186">Hvis det oppstår en versjonsfeil under distribusjon, må du importere X++-prosjektet til utviklingsmiljøet manuelt.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-186">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="ed9c3-187">Opprett deretter den distribuerbare pakken i utviklingsmiljøet, og distribuer den i produksjonsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-187">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="ed9c3-188">Koden er inkludert i Supply Chain Management versjon 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-188">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="ed9c3-189">Hvis du kjører den versjonen eller senere, er det ikke nødvendig å distribuere påkrevd distribusjon.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-189">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="ed9c3-190">Sørg for at følgende funksjoner er aktivert i miljøet i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-190">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="ed9c3-191">(De er som standard aktiverte.)</span><span class="sxs-lookup"><span data-stu-id="ed9c3-191">(By default, they are turned on.)</span></span>

| <span data-ttu-id="ed9c3-192">Funksjonsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="ed9c3-192">Feature description</span></span> | <span data-ttu-id="ed9c3-193">Kodeversjon</span><span class="sxs-lookup"><span data-stu-id="ed9c3-193">Code version</span></span> | <span data-ttu-id="ed9c3-194">Veksle klasse</span><span class="sxs-lookup"><span data-stu-id="ed9c3-194">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="ed9c3-195">Aktivere eller deaktivere bruk av lagerdimensjoner i InventSum-tabell</span><span class="sxs-lookup"><span data-stu-id="ed9c3-195">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="ed9c3-196">10.0.11</span><span class="sxs-lookup"><span data-stu-id="ed9c3-196">10.0.11</span></span> | <span data-ttu-id="ed9c3-197">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="ed9c3-197">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="ed9c3-198">Aktivere eller deaktivere bruk av lagerdimensjoner i InventSumDelta-tabell</span><span class="sxs-lookup"><span data-stu-id="ed9c3-198">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="ed9c3-199">10.0.12</span><span class="sxs-lookup"><span data-stu-id="ed9c3-199">10.0.12</span></span> | <span data-ttu-id="ed9c3-200">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="ed9c3-200">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="ed9c3-201">Definer integrering av lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="ed9c3-201">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="ed9c3-202">I Supply Chain Management åpner du arbeidsområdet **[Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og aktiverer funksjonen **Integrering av lagersynlighet**.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-202">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="ed9c3-203">Gå til **Lagerstyring \> Konfigurere \> Parametere for integrering av lagersynlighet**, og angi URL-adressen for miljøet der du kjører Lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-203">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="ed9c3-204">Finn LCS-miljøets Azure-område, og skriv deretter inn URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-204">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="ed9c3-205">URL-adressen har følgende skjema:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-205">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="ed9c3-206">Hvis du for eksempel er i Europa, vil miljøet ditt ha en av følgende URL-adresser:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-206">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com/`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="ed9c3-207">Følgende områder er for øyeblikket tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-207">The following regions are currently available.</span></span>

    | <span data-ttu-id="ed9c3-208">Azure-område</span><span class="sxs-lookup"><span data-stu-id="ed9c3-208">Azure region</span></span> | <span data-ttu-id="ed9c3-209">Kortnavn for område</span><span class="sxs-lookup"><span data-stu-id="ed9c3-209">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="ed9c3-210">Australia øst</span><span class="sxs-lookup"><span data-stu-id="ed9c3-210">Australia east</span></span> | <span data-ttu-id="ed9c3-211">eau</span><span class="sxs-lookup"><span data-stu-id="ed9c3-211">eau</span></span> |
    | <span data-ttu-id="ed9c3-212">Australia, sørøst</span><span class="sxs-lookup"><span data-stu-id="ed9c3-212">Australia southeast</span></span> | <span data-ttu-id="ed9c3-213">seau</span><span class="sxs-lookup"><span data-stu-id="ed9c3-213">seau</span></span> |
    | <span data-ttu-id="ed9c3-214">Midt-Canada</span><span class="sxs-lookup"><span data-stu-id="ed9c3-214">Canada central</span></span> | <span data-ttu-id="ed9c3-215">cca</span><span class="sxs-lookup"><span data-stu-id="ed9c3-215">cca</span></span> |
    | <span data-ttu-id="ed9c3-216">Canada, øst</span><span class="sxs-lookup"><span data-stu-id="ed9c3-216">Canada east</span></span> | <span data-ttu-id="ed9c3-217">eca</span><span class="sxs-lookup"><span data-stu-id="ed9c3-217">eca</span></span> |
    | <span data-ttu-id="ed9c3-218">Europa nord</span><span class="sxs-lookup"><span data-stu-id="ed9c3-218">North Europe</span></span> | <span data-ttu-id="ed9c3-219">neu</span><span class="sxs-lookup"><span data-stu-id="ed9c3-219">neu</span></span> |
    | <span data-ttu-id="ed9c3-220">Europa vest</span><span class="sxs-lookup"><span data-stu-id="ed9c3-220">West Europe</span></span> | <span data-ttu-id="ed9c3-221">weu</span><span class="sxs-lookup"><span data-stu-id="ed9c3-221">weu</span></span> |
    | <span data-ttu-id="ed9c3-222">USA øst</span><span class="sxs-lookup"><span data-stu-id="ed9c3-222">East US</span></span> | <span data-ttu-id="ed9c3-223">eus</span><span class="sxs-lookup"><span data-stu-id="ed9c3-223">eus</span></span> |
    | <span data-ttu-id="ed9c3-224">USA vest</span><span class="sxs-lookup"><span data-stu-id="ed9c3-224">West US</span></span> | <span data-ttu-id="ed9c3-225">wus</span><span class="sxs-lookup"><span data-stu-id="ed9c3-225">wus</span></span> |

1. <span data-ttu-id="ed9c3-226">Gå til **Lagerstyring \> Periodisk \> Integrering av lagersynlighet** og aktiver jobben.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-226">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="ed9c3-227">Alle lagerendringshendelser fra Supply Chain Management posteres nå til Lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-227">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="ed9c3-228">Den offentlige API-en for tillegget for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="ed9c3-228">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="ed9c3-229">Den offentlige REST-API-en i tillegget for lagersynlighet viser flere spesifikke endepunkter for integrering.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-229">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="ed9c3-230">Det støtter tre hovedtyper for samhandling:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-230">It supports three main interaction types:</span></span>

- <span data-ttu-id="ed9c3-231">Postering av beholdningsendringer i tillegget fra et eksternt system</span><span class="sxs-lookup"><span data-stu-id="ed9c3-231">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="ed9c3-232">Spørring etter gjeldende antall i beholdningen fra et eksternt system</span><span class="sxs-lookup"><span data-stu-id="ed9c3-232">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="ed9c3-233">Automatisk synkronisering med beholdningen for Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ed9c3-233">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="ed9c3-234">Automatisk synkronisering er ikke en del av den offentlige API-en.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-234">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="ed9c3-235">I stedet håndteres den i bakgrunnen for miljøer der tillegget for lagersynlighet er aktivert.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-235">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="ed9c3-236">Godkjenning</span><span class="sxs-lookup"><span data-stu-id="ed9c3-236">Authentication</span></span>

<span data-ttu-id="ed9c3-237">Platformsikkerhetstokenet brukes til å kalle inn tillegget for lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-237">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="ed9c3-238">Derfor må du generere et *Azure Active Directory-token (Azure AD)* ved hjelp av Azure AD-appen.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-238">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="ed9c3-239">Du må deretter bruke Azure AD-tokenet til å få *tilgangstokenet* fra sikkerhetstjenesten.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-239">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="ed9c3-240">Hent et token for sikkerhetstjeneste ved å gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-240">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="ed9c3-241">Logg på Azure-portalen, og bruk det til å finne `clientId` og `clientSecret` for Supply Chain Management-appen.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-241">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="ed9c3-242">Hent et Azure Active Directory-token (`aadToken`) ved å sende en HTTP-forespørsel med følgende egenskaper:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-242">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="ed9c3-243">**URL-adresse** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="ed9c3-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="ed9c3-244">**Metode** - `GET`</span><span class="sxs-lookup"><span data-stu-id="ed9c3-244">**Method** - `GET`</span></span>
    - <span data-ttu-id="ed9c3-245">**Meldingstekst (skjemadata)**:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-245">**Body content (form data)**:</span></span>

        | <span data-ttu-id="ed9c3-246">nøkkel</span><span class="sxs-lookup"><span data-stu-id="ed9c3-246">key</span></span> | <span data-ttu-id="ed9c3-247">verdi</span><span class="sxs-lookup"><span data-stu-id="ed9c3-247">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="ed9c3-248">client_id</span><span class="sxs-lookup"><span data-stu-id="ed9c3-248">client_id</span></span> | <span data-ttu-id="ed9c3-249">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="ed9c3-249">${aadAppId}</span></span> |
        | <span data-ttu-id="ed9c3-250">client_secret</span><span class="sxs-lookup"><span data-stu-id="ed9c3-250">client_secret</span></span> | <span data-ttu-id="ed9c3-251">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="ed9c3-251">${aadAppSecret}</span></span> |
        | <span data-ttu-id="ed9c3-252">grant_type</span><span class="sxs-lookup"><span data-stu-id="ed9c3-252">grant_type</span></span> | <span data-ttu-id="ed9c3-253">client_credentials</span><span class="sxs-lookup"><span data-stu-id="ed9c3-253">client_credentials</span></span> |
        | <span data-ttu-id="ed9c3-254">resource</span><span class="sxs-lookup"><span data-stu-id="ed9c3-254">resource</span></span> | <span data-ttu-id="ed9c3-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="ed9c3-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="ed9c3-256">Du skal motta et `aadToken` som svar, som ligner på følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-256">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
    "token_type": "Bearer",
    "expires_in": "3599",
    "ext_expires_in": "3599",
    "expires_on": "1610466645",
    "not_before": "1610462745",
    "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
    "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="ed9c3-257">Formuler en JSON-forespørsel som ligner på følgende:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-257">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="ed9c3-258">Der:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-258">Where:</span></span>
    - <span data-ttu-id="ed9c3-259">Verdien for `client_assertion` må være `aadToken` du mottok i forrige trinn.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-259">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="ed9c3-260">Verdien for `context` må være miljø-ID-en der du vil implementere tillegget.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-260">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="ed9c3-261">Angi alle andre verdier som vist i eksemplet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-261">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="ed9c3-262">Send en HTTP-forespørsel med følgende egenskaper:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-262">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="ed9c3-263">**URL-adresse** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="ed9c3-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="ed9c3-264">**Metode** - `POST`</span><span class="sxs-lookup"><span data-stu-id="ed9c3-264">**Method** - `POST`</span></span>
    - <span data-ttu-id="ed9c3-265">**HTTP-hode** - Ta med API-versjonen (nøkkelen er `Api-Version` og verdien er `1.0`)</span><span class="sxs-lookup"><span data-stu-id="ed9c3-265">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="ed9c3-266">**Meldingstekst** - Ta med JSON-forespørselen du opprettet i forrige trinn.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-266">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="ed9c3-267">Du får et `access_token` som svar.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-267">You will get an `access_token` in response.</span></span> <span data-ttu-id="ed9c3-268">Dette er det du trenger som bærertoken for å kalle opp lagersynlighets-API-en.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-268">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="ed9c3-269">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-269">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="ed9c3-270">Konfigurer API-en for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="ed9c3-270">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="ed9c3-271">Før du bruker tjenesten, må du fullføre konfigurasjonene som er beskrevet i følgende underavsnitt.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-271">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="ed9c3-272">Konfigurasjonen kan variere avhengig av detaljene i miljøet ditt.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-272">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="ed9c3-273">Den inneholder hovedsakelig fire deler:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-273">It primarily includes four parts:</span></span>

- [<span data-ttu-id="ed9c3-274">Partisjonering</span><span class="sxs-lookup"><span data-stu-id="ed9c3-274">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="ed9c3-275">Dimensjonskonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="ed9c3-275">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="ed9c3-276">Indeksering</span><span class="sxs-lookup"><span data-stu-id="ed9c3-276">Indexing</span></span>](#indexing)
- [<span data-ttu-id="ed9c3-277">Egendefinert mål</span><span class="sxs-lookup"><span data-stu-id="ed9c3-277">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="ed9c3-278">Partisjonering</span><span class="sxs-lookup"><span data-stu-id="ed9c3-278">Partitioning</span></span>

<span data-ttu-id="ed9c3-279">Partisjonering kan påvirke ytelsen betydelig for API-en for lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-279">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="ed9c3-280">Det er en god idé å definere et oppsett som tillater små grupperinger av data, samtidig som du tillater meningsfulle dataspørringer samtidig.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-280">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="ed9c3-281">`organizationId` (`dataAreaId` i Supply Chain Management) vil alltid være en del av partisjonen, og standard lagersynlighet er satt til partisjonering per dimensjon som *Område + sted*.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-281">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="ed9c3-282">Dette betyr at tjenesten alltid må spørres med disse dimensjonene som er definert i filtrene.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-282">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="ed9c3-283">*Område* og *Sted* er to generelle standarddimensjoner i lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-283">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="ed9c3-284">I Supply Chain Management kalles disse dimensjonene *Område* (`InventSiteId`) og *Lager* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="ed9c3-284">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="ed9c3-285">Dimensjonskonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="ed9c3-285">Dimension configurations</span></span>

<span data-ttu-id="ed9c3-286">Lagersynlighet inneholder en liste over generelle standarddimensjoner for å aktivere systemintegrasjon med flere kilder.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-286">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="ed9c3-287">Tabellen nedenfor viser hvilke lagerdimensjoner som skal være standard dimensjonsnavn i lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-287">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="ed9c3-288">Dimensjonstype</span><span class="sxs-lookup"><span data-stu-id="ed9c3-288">Dimension type</span></span> | <span data-ttu-id="ed9c3-289">Dimensjonsnavn</span><span class="sxs-lookup"><span data-stu-id="ed9c3-289">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="ed9c3-290">Produkt</span><span class="sxs-lookup"><span data-stu-id="ed9c3-290">Product</span></span> | `ColorId` |
| <span data-ttu-id="ed9c3-291">Produkt</span><span class="sxs-lookup"><span data-stu-id="ed9c3-291">Product</span></span> | `SizeId` |
| <span data-ttu-id="ed9c3-292">Produkt</span><span class="sxs-lookup"><span data-stu-id="ed9c3-292">Product</span></span> | `StyleId` |
| <span data-ttu-id="ed9c3-293">Produkt</span><span class="sxs-lookup"><span data-stu-id="ed9c3-293">Product</span></span> | `ConfigId` |
| <span data-ttu-id="ed9c3-294">Sporing</span><span class="sxs-lookup"><span data-stu-id="ed9c3-294">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="ed9c3-295">Sporing</span><span class="sxs-lookup"><span data-stu-id="ed9c3-295">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="ed9c3-296">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="ed9c3-296">Location</span></span> | `LocationId` |
| <span data-ttu-id="ed9c3-297">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="ed9c3-297">Location</span></span> | `SiteId` |
| <span data-ttu-id="ed9c3-298">Lagerstatus</span><span class="sxs-lookup"><span data-stu-id="ed9c3-298">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="ed9c3-299">Lagerspesifikk</span><span class="sxs-lookup"><span data-stu-id="ed9c3-299">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="ed9c3-300">Lagerspesifikk</span><span class="sxs-lookup"><span data-stu-id="ed9c3-300">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="ed9c3-301">Lagerspesifikk</span><span class="sxs-lookup"><span data-stu-id="ed9c3-301">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="ed9c3-302">Dimensjonstypen som er oppført i den forrige tabellen, er bare for referanse.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-302">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="ed9c3-303">Du trenger ikke definere dimensjonstypen i Lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-303">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="ed9c3-304">Hvis det finnes en egendefinert dimensjon som må flyte til en standardverdi når det brukes av lagersynlighet, kan du konfigurere navnet **Egendefinert dimensjon** i Lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-304">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="ed9c3-305">Eksterne systemer har tilgang til lagersynlighet via RESTful-API-er som gir deg beholdningsinformasjon om gitte dimensjoner som det skal spørres om.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-305">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="ed9c3-306">Ved integreringen kan du bruke Lagersynlighet til å konfigurere den *eksterne kanaldatakilden* og kildedimensjonen til *måldimensjonene* i Lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-306">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="ed9c3-307">Måldimensjonene må være ett av følgende:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-307">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="ed9c3-308">Standarddimensjoner i Lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="ed9c3-308">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="ed9c3-309">Egendefinerte dimensjoner</span><span class="sxs-lookup"><span data-stu-id="ed9c3-309">Custom dimensions</span></span>

<span data-ttu-id="ed9c3-310">Formålet med dimensjonskonfigurasjon er å standardisere integreringen med flere systemer for spørringen på dimensjoner og posteringshendelsen med dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-310">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="ed9c3-311">Indeksering</span><span class="sxs-lookup"><span data-stu-id="ed9c3-311">Indexing</span></span>

<span data-ttu-id="ed9c3-312">Vanligvis vil ikke lagerbeholdningsspørringen bare være på det høyeste totale nivået, men du vil kanskje se resultater som er aggregert basert på lagerdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-312">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="ed9c3-313">Lagersynlighet gir fleksibilitet ved å la deg definere indeksene som er basert på dimensjonen eller kombinasjonen av dimensjonene.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-313">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="ed9c3-314">For øyeblikket kan du bare konfigurere indekser til maksimalt fem.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-314">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="ed9c3-315">Du må nøye vurdere hvilken dimensjon eller dimensjonskombinasjon du vil bruke før implementeringen for å sikre at den oppfyller dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-315">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="ed9c3-316">Hvis du for eksempel vil spørre etter produkter som følger:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-316">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="ed9c3-317">Forespør den aggregerte produktbeholdningen etter dimensjonene *Farge* og *Størrelse*.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-317">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="ed9c3-318">I noen tilfeller vil du bare spørre om produktet totalt.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-318">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="ed9c3-319">Du har to indekser definert som følgende:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-319">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="ed9c3-320">Den tomme parentesen samles, basert på produkt-ID-en i partisjonen.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-320">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="ed9c3-321">Indekseringen definerer hvordan du kan gruppere resultatene basert på `groupBy`-spørringsinnstillingen.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-321">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="ed9c3-322">I dette tilfellet hvis du ikke definerer noen `groupBy`-verdier, får du totaler etter `productid`.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-322">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="ed9c3-323">Hvis du definerer `groupBy` som `groupBy=ColorId&groupBy=SizeId`, vil du ellers få flere linjer returnert, basert på de ulike kombinasjonene mellom farger og størrelser i systemet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-323">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="ed9c3-324">Du kan legge spørringskriteriene i brødteksten for forespørselen.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-324">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="ed9c3-325">Her er en eksempelspørring på produktet med farge- og størrelseskombinasjon.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-325">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a><span data-ttu-id="ed9c3-326">Egendefinert mål</span><span class="sxs-lookup"><span data-stu-id="ed9c3-326">Custom measurement</span></span>

<span data-ttu-id="ed9c3-327">Standard målantall er koblet til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-327">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="ed9c3-328">Det kan imidlertid være at du vil ha et antall som består av en kombinasjon av standardmålene.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-328">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="ed9c3-329">Hvis du vil gjøre dette, kan du ha en konfigurasjon av egendefinert antall, som vil bli lagt til i utdataene i lagerbeholdningsspørringene.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-329">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="ed9c3-330">Ved hjelp av funksjonaliteten kan du bare definere et sett med mål som skal legges til, eller et sett med mål som skal trekkes fra, for å kunne lage det egendefinerte målet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-330">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="ed9c3-331">Med følgende spørringsvilkår vil du for eksempel konfigurere det egendefinerte målantallet som `MyCustomAvailableforReservation` som skal brukes av forbrukssystemet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-331">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="ed9c3-332">Forbrukssystem</span><span class="sxs-lookup"><span data-stu-id="ed9c3-332">Consumption system</span></span> | <span data-ttu-id="ed9c3-333">Beregnede mål</span><span class="sxs-lookup"><span data-stu-id="ed9c3-333">Calculated measurers</span></span> | <span data-ttu-id="ed9c3-334">Datakilde</span><span class="sxs-lookup"><span data-stu-id="ed9c3-334">Data source</span></span> | <span data-ttu-id="ed9c3-335">Modifikator</span><span class="sxs-lookup"><span data-stu-id="ed9c3-335">Modifier</span></span> | <span data-ttu-id="ed9c3-336">Beregningstype for modifikator</span><span class="sxs-lookup"><span data-stu-id="ed9c3-336">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="ed9c3-337">Tillegg</span><span class="sxs-lookup"><span data-stu-id="ed9c3-337">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="ed9c3-338">Tillegg</span><span class="sxs-lookup"><span data-stu-id="ed9c3-338">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="ed9c3-339">Subtraksjon</span><span class="sxs-lookup"><span data-stu-id="ed9c3-339">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="ed9c3-340">Tillegg</span><span class="sxs-lookup"><span data-stu-id="ed9c3-340">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="ed9c3-341">Subtraksjon</span><span class="sxs-lookup"><span data-stu-id="ed9c3-341">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="ed9c3-342">Tillegg</span><span class="sxs-lookup"><span data-stu-id="ed9c3-342">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="ed9c3-343">Tillegg</span><span class="sxs-lookup"><span data-stu-id="ed9c3-343">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="ed9c3-344">Subtraksjon</span><span class="sxs-lookup"><span data-stu-id="ed9c3-344">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="ed9c3-345">Subtraksjon</span><span class="sxs-lookup"><span data-stu-id="ed9c3-345">Subtraction</span></span> |

<span data-ttu-id="ed9c3-346">Med dette vil spørringen på det egendefinerte målantallet returnere følgende utdata.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-346">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="ed9c3-347">`MyCustomAvailableforReservation`-utdataene er basert på beregningsinnstillingen i de egendefinerte målene som:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-347">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="ed9c3-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="ed9c3-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="ed9c3-349">Postere lagerendringer</span><span class="sxs-lookup"><span data-stu-id="ed9c3-349">Posting on-hand changes</span></span>

<span data-ttu-id="ed9c3-350">Den nøyaktige URL-adressen som hendelsen vil bli postert til, avhenger av det geografiske området.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-350">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="ed9c3-351">Den tar følgende form:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-351">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="ed9c3-352">Når den er godkjent, kan denne URL-adressen brukes sammen med HTTP `POST`-metoden til å sende lagerbeholdningshendelser til tjenesten.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-352">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="ed9c3-353">En spesiell topptekst brukes til å kommunisere med Dynamics 365-tjenester via HTTP-forespørsler, og angir miljø-ID-en til Supply Chain Management-forkomten dataene er koblet til.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-353">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="ed9c3-354">For eksempel:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-354">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="ed9c3-355">Postere spørringer om lagerendringer eksempel 1</span><span class="sxs-lookup"><span data-stu-id="ed9c3-355">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="ed9c3-356">I dette eksemplet vises det et scenario der du kan definere dimensjonskonfigurasjonen i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-356">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="ed9c3-357">Bruk følgende spørring til å konfigurere dimensjonstilordningen i Power Apps:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-357">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="ed9c3-358">Nå kan du angi `dimensionDataSource` og bruke egendefinerte dimensjoner i spørringene.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-358">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="ed9c3-359">Systemet konverterer automatisk egendefinerte dimensjoner til basisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-359">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="ed9c3-360">Postere spørringer om lagerendringer eksempel 2</span><span class="sxs-lookup"><span data-stu-id="ed9c3-360">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="ed9c3-361">Dette eksemplet viser et scenario der ingen tilordninger er definert for dimensjonskonfigurasjonen i Power Apps, slik at posteringen også bør bruke basisdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-361">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="ed9c3-362">Alle dimensjoner må være basisdimensjoner når `dimensionDataSource`-feltet er null, tomt eller mellomrom.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-362">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="ed9c3-363">Feltegenskaper for JSON-dokument</span><span class="sxs-lookup"><span data-stu-id="ed9c3-363">JSON document field properties</span></span>

<span data-ttu-id="ed9c3-364">Feltene fra JSON-spørringseksemplene som ble angitt tidligere, har egenskapene som er oppført i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-364">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="ed9c3-365">Felt-ID</span><span class="sxs-lookup"><span data-stu-id="ed9c3-365">Field ID</span></span> | <span data-ttu-id="ed9c3-366">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ed9c3-366">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="ed9c3-367">En unik ID for den bestemte endringshendelsen.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-367">A unique ID for the specific change event.</span></span> <span data-ttu-id="ed9c3-368">Denne ID-en brukes til å sikre at hvis kommunikasjon med tjenesten mislykkes under posteringen, vil sendingen av hendelsen ikke resultere i at samme hendelse telles to ganger i systemet.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-368">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="ed9c3-369">Identifikatoren til organisasjonen som er koblet til hendelsen.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-369">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="ed9c3-370">Dette tilordner til ID-er til Supply Chain Management-organisasjoner eller dataområder.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-370">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="ed9c3-371">Identifikatoren til produktet det gjelder.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-371">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="ed9c3-372">Antallet som lagerbeholdningen må endres med.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-372">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="ed9c3-373">Hvis for eksempel ti nye bagels er lagt til i en hylle, vil denne verdien være 10.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-373">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="ed9c3-374">Hvis tre bagels deretter ble fjernet fra hyllen eller solgt, ville denne verdien være –3.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-374">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="ed9c3-375">Datakilden for dimensjonene som brukes i posteringsendringshendelsen og -spørringen.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-375">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="ed9c3-376">Hvis du angir datakilden, kan du bruke de egendefinerte dimensjonene fra den angitte datakilden.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-376">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="ed9c3-377">Med dimensjonskonfigurasjonen kan Lagersynlighet tilordne de egendefinerte dimensjonene til de generelle standarddimensjonene.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-377">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="ed9c3-378">Hvis `dimensionDataSource` ikke er angitt, kan du bare bruke de generelle standarddimensjonene i spørringene.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-378">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="ed9c3-379">En dynamisk samling med nøkkel/verdi-par.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-379">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="ed9c3-380">Disse vil tilordnes noen av dimensjonene i Supply Chain Management, men du kan også legge til egendefinerte dimensjoner (som *Kilde*) som kan angi om hendelsen kommer fra Supply Chain Management eller et eksternt system.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-380">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="ed9c3-381">Spørring om aktuell lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="ed9c3-381">Querying current on-hand</span></span>

<span data-ttu-id="ed9c3-382">Endepunktet for spørringer av gjeldende lagerbeholdning vil ha en lignende URL-adresse:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-382">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="ed9c3-383">Det blir spurt med HTTP `POST`-metoden.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-383">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="ed9c3-384">Gjeldende beholdningsspørring, eksempel 1</span><span class="sxs-lookup"><span data-stu-id="ed9c3-384">Current on-hand query example 1</span></span>

<span data-ttu-id="ed9c3-385">I dette eksemplet vises det et scenario der du allerede har fullført dimensjonskonfigurasjonen i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-385">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="ed9c3-386">Bruk følgende spørring til å konfigurere dimensjonstilordningen i Power Apps:</span><span class="sxs-lookup"><span data-stu-id="ed9c3-386">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="ed9c3-387">Nå kan du angi `dimensionDataSource` og bruke egendefinerte dimensjoner i spørringene.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-387">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="ed9c3-388">Systemet konverterer automatisk egendefinerte dimensjoner til basisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-388">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="ed9c3-389">Du kan angi `DimensionDataSource` i `filters` og angi egendefinerte dimensjoner i både `filters` og `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-389">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="ed9c3-390">Systemet konverterer automatisk egendefinerte dimensjoner til basisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-390">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="ed9c3-391">Gjeldende beholdningsspørring, eksempel 2</span><span class="sxs-lookup"><span data-stu-id="ed9c3-391">Current on-hand query example 2</span></span>

<span data-ttu-id="ed9c3-392">Dette eksemplet viser et scenario der ingen tilordninger er definert for dimensjonskonfigurasjonen i Power Apps, slik at posteringen også bør bruke basisdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-392">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="ed9c3-393">Alle dimensjoner må være basisdimensjoner når `dimensionDataSource`-feltet, under `filters`, er null, tomt eller mellomrom.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-393">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="ed9c3-394">Eksempel på returresultat</span><span class="sxs-lookup"><span data-stu-id="ed9c3-394">Example return result</span></span>

<span data-ttu-id="ed9c3-395">Spørringene som vises i eksemplene ovenfor, kan returnere et resultat som dette.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-395">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="ed9c3-396">Legg merke til at antall-feltene er strukturert som en ordliste for mål og tilknyttede verdier.</span><span class="sxs-lookup"><span data-stu-id="ed9c3-396">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
