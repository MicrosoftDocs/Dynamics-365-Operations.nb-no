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
ms.openlocfilehash: d09c7be5de75511b10d7a69d4b8ac12917b0dbe8
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910431"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="9dd08-103">Tillegg for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="9dd08-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="9dd08-104">Tillegget for lagersynlighet er en uavhengig og høyt skalerbar mikrotjeneste som aktiverer beholdningssporing i sanntid, og gir dermed en global visning av lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="9dd08-105">All informasjon som er relatert til lagerbeholdningen, eksporteres til tjenesten via i SQL-integrasjon med minimal forsinkelse.</span><span class="sxs-lookup"><span data-stu-id="9dd08-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="9dd08-106">Eksterne systemer får tilgang til tjenesten via RESTful-API-er for spørring om lagerbeholdningsinformasjon for gitte sett med dimensjoner, og dermed hente en liste over tilgjengelige lagerbeholdninger.</span><span class="sxs-lookup"><span data-stu-id="9dd08-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="9dd08-107">Lagersynlighet er en mikrotjeneste som er bygd på Microsoft Dataverse, som betyr at du kan utvide den ved å bygge Power Apps og bruke Power BI til å oppgi egendefinert funksjonalitet som dekker dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="9dd08-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="9dd08-108">Det er også mulig å oppgradere indeksen for å utføre lagerspørringer.</span><span class="sxs-lookup"><span data-stu-id="9dd08-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="9dd08-109">Lagersynlighet inneholder konfigurasjonsalternativer som gjør at den kan integreres med flere tredjepartssystemer.</span><span class="sxs-lookup"><span data-stu-id="9dd08-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="9dd08-110">Den støtter den standardiserte lagerdimensjonen, egendefinert utvidelse og standardisert beregnet antall som kan konfigureres.</span><span class="sxs-lookup"><span data-stu-id="9dd08-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="9dd08-111">Dette emnet beskriver hvordan du installerer og konfigurerer tillegget for lagersynlighet for Dynamics 365 Supply Chain Management, og hvordan du bruker app-programmeringsgrensesnittet (API).</span><span class="sxs-lookup"><span data-stu-id="9dd08-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="9dd08-112">Installer tillegget for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="9dd08-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="9dd08-113">Du må installere tillegget for lagersynlighet ved hjelp av Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9dd08-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="9dd08-114">LCS er en samarbeidsportal som gir et miljø og et sett med jevnlig oppdaterte tjenester som hjelper deg med å administrere applivssyklusen til Dynamics 365 Finance and Operations-appene dine.</span><span class="sxs-lookup"><span data-stu-id="9dd08-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="9dd08-115">Hvis du vil ha mer informasjon, se [Lifecycle Services-ressurser](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span><span class="sxs-lookup"><span data-stu-id="9dd08-115">For more information, see [Lifecycle Services resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="9dd08-116">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="9dd08-116">Prerequisites</span></span>

<span data-ttu-id="9dd08-117">Før du kan installere tillegget for lagersynlighet, må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="9dd08-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="9dd08-118">Hent et LCS-implementeringsprosjekt med minst ett miljø som er distribuert.</span><span class="sxs-lookup"><span data-stu-id="9dd08-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="9dd08-119">Sørg for at forutsetningene for å definere tillegg som er oppført i [Tilleggsoversikt](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md), er fullført.</span><span class="sxs-lookup"><span data-stu-id="9dd08-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="9dd08-120">Lagersynlighet krever ikke kobling til dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="9dd08-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="9dd08-121">Kontakt lagersynlighetsteamet på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for å få følgende tre obligatoriske filer:</span><span class="sxs-lookup"><span data-stu-id="9dd08-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>
    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="9dd08-122">`Inventory Visibility Integration.zip` (hvis versjonen av Supply Chain Management du kjører, er eldre enn versjon 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="9dd08-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>
- <span data-ttu-id="9dd08-123">Følg instruksjonene gitt i [Hurtigstart: Registrere en app med Microsoft-identitetsplattformen](/azure/active-directory/develop/quickstart-register-app) for å registrere en app og legge til en klienthemmelighet for AAD under Azure-abonnementet ditt.</span><span class="sxs-lookup"><span data-stu-id="9dd08-123">Follow the instructions given in [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register an application and add a client secret to AAD under your azure subscription.</span></span>
    - [<span data-ttu-id="9dd08-124">Registrere en app</span><span class="sxs-lookup"><span data-stu-id="9dd08-124">Register an application</span></span>](/azure/active-directory/develop/quickstart-register-app)
    - [<span data-ttu-id="9dd08-125">Legge til en klienthemmelighet</span><span class="sxs-lookup"><span data-stu-id="9dd08-125">Add a client secret</span></span>](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
    - <span data-ttu-id="9dd08-126">**App-ID (klient)**, **Klienthemmelighet** og **Leier-ID** vil bli brukt i trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="9dd08-126">The **Application(Client) Id**, **Client Secret** and **Tenant ID** will be used in the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="9dd08-127">Landene og områdene som støttes for øyeblikket, omfatter Canada, USA og Den europeiske union (EU).</span><span class="sxs-lookup"><span data-stu-id="9dd08-127">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="9dd08-128">Hvis du har spørsmål om disse forutsetningene, kan du ta kontakt med produktteamet for lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-128">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="9dd08-129">Konfigurere Dataverse</span><span class="sxs-lookup"><span data-stu-id="9dd08-129">Set up Dataverse</span></span>

<span data-ttu-id="9dd08-130">Gjør følgende for å konfigurere Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9dd08-130">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="9dd08-131">Legg til et serviceprinsipp i leieren:</span><span class="sxs-lookup"><span data-stu-id="9dd08-131">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="9dd08-132">Installer Azure AD PowerShell-modul v2 som beskrevet i [Installer Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="9dd08-132">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="9dd08-133">Kjør følgende PowerShell-kommando.</span><span class="sxs-lookup"><span data-stu-id="9dd08-133">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="9dd08-134">Opprett en applikasjonsbruker for lagersynlighet i Dataverse:</span><span class="sxs-lookup"><span data-stu-id="9dd08-134">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="9dd08-135">Åpne URL-adressen for Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-135">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="9dd08-136">Gå til **Avansert innstilling \> System \> Sikkerhet \> Brukere** og opporett en appbruker.</span><span class="sxs-lookup"><span data-stu-id="9dd08-136">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="9dd08-137">Bruk Vis-menyen til å endre sidevisningen til **Appbrukere**.</span><span class="sxs-lookup"><span data-stu-id="9dd08-137">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="9dd08-138">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9dd08-138">Select **New**.</span></span> <span data-ttu-id="9dd08-139">Sett app-ID-en til *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="9dd08-139">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="9dd08-140">(Objekt-ID-en lastes automatisk når du lagrer endringene.) Du kan tilpasse navnet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-140">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="9dd08-141">Du kan for eksempel endre til *Lagersynlighet*.</span><span class="sxs-lookup"><span data-stu-id="9dd08-141">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="9dd08-142">Når du er ferdig, velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9dd08-142">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="9dd08-143">Velg **Tilordne rolle**, og velg deretter **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="9dd08-143">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="9dd08-144">Hvis det finnes en rolle kalt **Common Data Service-bruker**, velger du den også.</span><span class="sxs-lookup"><span data-stu-id="9dd08-144">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="9dd08-145">Hvis du vil ha mer informasjon, kan du se [Opprette en appbruker](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="9dd08-145">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="9dd08-146">Hvis standardspråket for Dataverse ikke er **engelsk**:</span><span class="sxs-lookup"><span data-stu-id="9dd08-146">If the default language of your Dataverse is not **English**:</span></span>

    1. <span data-ttu-id="9dd08-147">Gå til **Avanserte innstillinger \> Administrasjon \> Språk**,</span><span class="sxs-lookup"><span data-stu-id="9dd08-147">Go to **Advanced Setting \> Administration \> Languages**,</span></span>
    1. <span data-ttu-id="9dd08-148">Velg **Engelsk (språkkode=1033)**, og velg **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="9dd08-148">Select **English (LanguageCode=1033)** and select **Apply**.</span></span>

1. <span data-ttu-id="9dd08-149">Importer `Inventory Visibility Dataverse Solution.zip`-filen, som inkluderer relaterte enheter for konfigurasjon av Dataverse og Power Apps:</span><span class="sxs-lookup"><span data-stu-id="9dd08-149">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="9dd08-150">Gå til siden **Løsninger**.</span><span class="sxs-lookup"><span data-stu-id="9dd08-150">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="9dd08-151">Velg **Import**.</span><span class="sxs-lookup"><span data-stu-id="9dd08-151">Select **Import**.</span></span>

1. <span data-ttu-id="9dd08-152">Importer utløserflyten for konfigurasjonsoppgradering:</span><span class="sxs-lookup"><span data-stu-id="9dd08-152">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="9dd08-153">Gå til Microsoft Flow-siden.</span><span class="sxs-lookup"><span data-stu-id="9dd08-153">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="9dd08-154">Sørg for at det finnes en tilkobling med navnet *Dataverse (eldre)*.</span><span class="sxs-lookup"><span data-stu-id="9dd08-154">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="9dd08-155">(Hvis den ikke finnes, kan du opprette den.)</span><span class="sxs-lookup"><span data-stu-id="9dd08-155">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="9dd08-156">Importer `Inventory Visibility Configuration Trigger.zip`-filen.</span><span class="sxs-lookup"><span data-stu-id="9dd08-156">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="9dd08-157">Når den er importert, vises utløseren under **Mine flyter**.</span><span class="sxs-lookup"><span data-stu-id="9dd08-157">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="9dd08-158">Initialiser følgende fire variabler basert på miljøinformasjon:</span><span class="sxs-lookup"><span data-stu-id="9dd08-158">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="9dd08-159">Leier-ID for Azure</span><span class="sxs-lookup"><span data-stu-id="9dd08-159">Azure Tenant ID</span></span>
        - <span data-ttu-id="9dd08-160">Appklient-ID for Azure</span><span class="sxs-lookup"><span data-stu-id="9dd08-160">Azure Application Client ID</span></span>
        - <span data-ttu-id="9dd08-161">Appklienthemmelighet for Azure</span><span class="sxs-lookup"><span data-stu-id="9dd08-161">Azure Application Client Secret</span></span>
        - <span data-ttu-id="9dd08-162">Endepunkt for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="9dd08-162">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="9dd08-163">Hvis du vil ha mer informasjon om denne variabelen, kan du se delen [Konfigurere integrering av lagersynlighet](#setup-inventory-visibility-integration) senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-163">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="9dd08-164">![Konfigurasjonsutløser](media/configuration-trigger.png "Konfigurasjonsutløser")</span><span class="sxs-lookup"><span data-stu-id="9dd08-164">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="9dd08-165">Velg **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="9dd08-165">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="9dd08-166">Installer tillegget</span><span class="sxs-lookup"><span data-stu-id="9dd08-166">Install the add-in</span></span>

<span data-ttu-id="9dd08-167">Hvis du vil installere tillegget for lagersynlighet, må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="9dd08-167">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="9dd08-168">Logg på [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index)-portalen.</span><span class="sxs-lookup"><span data-stu-id="9dd08-168">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="9dd08-169">På hjemmesiden velger du prosjektet der miljøet er distribuert.</span><span class="sxs-lookup"><span data-stu-id="9dd08-169">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="9dd08-170">På prosjektsiden velger du miljøet du vil installere tillegget i.</span><span class="sxs-lookup"><span data-stu-id="9dd08-170">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="9dd08-171">På miljøsiden ruller du ned til du ser delen delen **Miljøtillegg** i delen **Power Platform-integrering**, der du også finner navnet på Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-171">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="9dd08-172">I delen **Miljøtillegg** velger du **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="9dd08-172">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="9dd08-173">![Miljøsiden i LCS](media/inventory-visibility-environment.png "Miljøsiden i LCS")</span><span class="sxs-lookup"><span data-stu-id="9dd08-173">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="9dd08-174">Velg koblingen **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="9dd08-174">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="9dd08-175">En liste over tilgjengelige tillegg åpnes.</span><span class="sxs-lookup"><span data-stu-id="9dd08-175">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="9dd08-176">Velg **Lagersynlighet** i listen.</span><span class="sxs-lookup"><span data-stu-id="9dd08-176">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="9dd08-177">Angi verdier for følgende felter i miljøet:</span><span class="sxs-lookup"><span data-stu-id="9dd08-177">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="9dd08-178">**ID for AAD-app (klient)**</span><span class="sxs-lookup"><span data-stu-id="9dd08-178">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="9dd08-179">**Leier-ID for AAD**</span><span class="sxs-lookup"><span data-stu-id="9dd08-179">**AAD tenant ID**</span></span>

    <span data-ttu-id="9dd08-180">![Legg til i konfigurasjon-side](media/inventory-visibility-setup.png "Legg til i konfigurasjon-side")</span><span class="sxs-lookup"><span data-stu-id="9dd08-180">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="9dd08-181">Godta vilkåret og betingelsen ved å merke av for **Vilkår og betingelser**.</span><span class="sxs-lookup"><span data-stu-id="9dd08-181">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="9dd08-182">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="9dd08-182">Select **Install**.</span></span> <span data-ttu-id="9dd08-183">Statusen for tillegget vil vises som **Installerer**.</span><span class="sxs-lookup"><span data-stu-id="9dd08-183">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="9dd08-184">Når du er ferdig, oppdaterer du siden for å se status endre til **Installert**.</span><span class="sxs-lookup"><span data-stu-id="9dd08-184">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="9dd08-185">Avinstallere tillegget</span><span class="sxs-lookup"><span data-stu-id="9dd08-185">Uninstall the add-in</span></span>

<span data-ttu-id="9dd08-186">Velg **Avinstaller** tillegget for å avinstallere tillegget.</span><span class="sxs-lookup"><span data-stu-id="9dd08-186">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="9dd08-187">Når du oppdaterer LCS, fjernes tillegget for lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-187">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="9dd08-188">Avinstallasjonsprosessen fjerner registreringen av tillegget, og starter også en jobb for å rydde opp i alle forretningsdataene som er lagret i tjenesten.</span><span class="sxs-lookup"><span data-stu-id="9dd08-188">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="9dd08-189">Bruke lagerbeholdningsdata fra Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9dd08-189">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="9dd08-190">Distribuere integreringspakken for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="9dd08-190">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="9dd08-191">Hvis du kjører Supply Chain Management versjon 10.0.17 eller tidligere, kan du kontakte kundestøttegruppen for lagersynlighet på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for å hente pakkefilen.</span><span class="sxs-lookup"><span data-stu-id="9dd08-191">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="9dd08-192">Deretter distribuerer du pakken i LCS.</span><span class="sxs-lookup"><span data-stu-id="9dd08-192">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="9dd08-193">Hvis det oppstår en versjonsfeil under distribusjon, må du importere X++-prosjektet til utviklingsmiljøet manuelt.</span><span class="sxs-lookup"><span data-stu-id="9dd08-193">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="9dd08-194">Opprett deretter den distribuerbare pakken i utviklingsmiljøet, og distribuer den i produksjonsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-194">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="9dd08-195">Koden er inkludert i Supply Chain Management versjon 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="9dd08-195">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="9dd08-196">Hvis du kjører den versjonen eller senere, er det ikke nødvendig å distribuere påkrevd distribusjon.</span><span class="sxs-lookup"><span data-stu-id="9dd08-196">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="9dd08-197">Sørg for at følgende funksjoner er aktivert i miljøet i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9dd08-197">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="9dd08-198">(De er som standard aktiverte.)</span><span class="sxs-lookup"><span data-stu-id="9dd08-198">(By default, they are turned on.)</span></span>

| <span data-ttu-id="9dd08-199">Funksjonsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="9dd08-199">Feature description</span></span> | <span data-ttu-id="9dd08-200">Kodeversjon</span><span class="sxs-lookup"><span data-stu-id="9dd08-200">Code version</span></span> | <span data-ttu-id="9dd08-201">Veksle klasse</span><span class="sxs-lookup"><span data-stu-id="9dd08-201">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="9dd08-202">Aktivere eller deaktivere bruk av lagerdimensjoner i InventSum-tabell</span><span class="sxs-lookup"><span data-stu-id="9dd08-202">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="9dd08-203">10.0.11</span><span class="sxs-lookup"><span data-stu-id="9dd08-203">10.0.11</span></span> | <span data-ttu-id="9dd08-204">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="9dd08-204">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="9dd08-205">Aktivere eller deaktivere bruk av lagerdimensjoner i InventSumDelta-tabell</span><span class="sxs-lookup"><span data-stu-id="9dd08-205">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="9dd08-206">10.0.12</span><span class="sxs-lookup"><span data-stu-id="9dd08-206">10.0.12</span></span> | <span data-ttu-id="9dd08-207">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="9dd08-207">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="9dd08-208">Definer integrering av lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="9dd08-208">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="9dd08-209">I Supply Chain Management åpner du arbeidsområdet **[Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og aktiverer funksjonen **Integrering av lagersynlighet**.</span><span class="sxs-lookup"><span data-stu-id="9dd08-209">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="9dd08-210">Gå til **Lagerstyring \> Konfigurere \> Parametere for integrering av lagersynlighet**, og angi URL-adressen for miljøet der du kjører Lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-210">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="9dd08-211">Finn LCS-miljøets Azure-område, og skriv deretter inn URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="9dd08-211">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="9dd08-212">URL-adressen har følgende skjema:</span><span class="sxs-lookup"><span data-stu-id="9dd08-212">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="9dd08-213">Hvis du for eksempel er i Europa, vil miljøet ditt ha en av følgende URL-adresser:</span><span class="sxs-lookup"><span data-stu-id="9dd08-213">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="9dd08-214">Følgende områder er for øyeblikket tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="9dd08-214">The following regions are currently available.</span></span>

    | <span data-ttu-id="9dd08-215">Azure-område</span><span class="sxs-lookup"><span data-stu-id="9dd08-215">Azure region</span></span> | <span data-ttu-id="9dd08-216">Kortnavn for område</span><span class="sxs-lookup"><span data-stu-id="9dd08-216">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="9dd08-217">Australia øst</span><span class="sxs-lookup"><span data-stu-id="9dd08-217">Australia east</span></span> | <span data-ttu-id="9dd08-218">eau</span><span class="sxs-lookup"><span data-stu-id="9dd08-218">eau</span></span> |
    | <span data-ttu-id="9dd08-219">Australia, sørøst</span><span class="sxs-lookup"><span data-stu-id="9dd08-219">Australia southeast</span></span> | <span data-ttu-id="9dd08-220">seau</span><span class="sxs-lookup"><span data-stu-id="9dd08-220">seau</span></span> |
    | <span data-ttu-id="9dd08-221">Midt-Canada</span><span class="sxs-lookup"><span data-stu-id="9dd08-221">Canada central</span></span> | <span data-ttu-id="9dd08-222">cca</span><span class="sxs-lookup"><span data-stu-id="9dd08-222">cca</span></span> |
    | <span data-ttu-id="9dd08-223">Canada, øst</span><span class="sxs-lookup"><span data-stu-id="9dd08-223">Canada east</span></span> | <span data-ttu-id="9dd08-224">eca</span><span class="sxs-lookup"><span data-stu-id="9dd08-224">eca</span></span> |
    | <span data-ttu-id="9dd08-225">Europa nord</span><span class="sxs-lookup"><span data-stu-id="9dd08-225">North Europe</span></span> | <span data-ttu-id="9dd08-226">neu</span><span class="sxs-lookup"><span data-stu-id="9dd08-226">neu</span></span> |
    | <span data-ttu-id="9dd08-227">Europa vest</span><span class="sxs-lookup"><span data-stu-id="9dd08-227">West Europe</span></span> | <span data-ttu-id="9dd08-228">weu</span><span class="sxs-lookup"><span data-stu-id="9dd08-228">weu</span></span> |
    | <span data-ttu-id="9dd08-229">USA øst</span><span class="sxs-lookup"><span data-stu-id="9dd08-229">East US</span></span> | <span data-ttu-id="9dd08-230">eus</span><span class="sxs-lookup"><span data-stu-id="9dd08-230">eus</span></span> |
    | <span data-ttu-id="9dd08-231">USA vest</span><span class="sxs-lookup"><span data-stu-id="9dd08-231">West US</span></span> | <span data-ttu-id="9dd08-232">wus</span><span class="sxs-lookup"><span data-stu-id="9dd08-232">wus</span></span> |

1. <span data-ttu-id="9dd08-233">Gå til **Lagerstyring \> Periodisk \> Integrering av lagersynlighet** og aktiver jobben.</span><span class="sxs-lookup"><span data-stu-id="9dd08-233">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="9dd08-234">Alle lagerendringshendelser fra Supply Chain Management posteres nå til Lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-234">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="9dd08-235">Den offentlige API-en for tillegget for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="9dd08-235">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="9dd08-236">Den offentlige REST-API-en i tillegget for lagersynlighet viser flere spesifikke endepunkter for integrering.</span><span class="sxs-lookup"><span data-stu-id="9dd08-236">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="9dd08-237">Det støtter tre hovedtyper for samhandling:</span><span class="sxs-lookup"><span data-stu-id="9dd08-237">It supports three main interaction types:</span></span>

- <span data-ttu-id="9dd08-238">Postering av beholdningsendringer i tillegget fra et eksternt system</span><span class="sxs-lookup"><span data-stu-id="9dd08-238">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="9dd08-239">Spørring etter gjeldende antall i beholdningen fra et eksternt system</span><span class="sxs-lookup"><span data-stu-id="9dd08-239">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="9dd08-240">Automatisk synkronisering med beholdningen for Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9dd08-240">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="9dd08-241">Automatisk synkronisering er ikke en del av den offentlige API-en.</span><span class="sxs-lookup"><span data-stu-id="9dd08-241">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="9dd08-242">I stedet håndteres den i bakgrunnen for miljøer der tillegget for lagersynlighet er aktivert.</span><span class="sxs-lookup"><span data-stu-id="9dd08-242">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="9dd08-243">Godkjenning</span><span class="sxs-lookup"><span data-stu-id="9dd08-243">Authentication</span></span>

<span data-ttu-id="9dd08-244">Platformsikkerhetstokenet brukes til å kalle inn tillegget for lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-244">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="9dd08-245">Derfor må du generere et *Azure Active Directory-token (Azure AD)* ved hjelp av Azure AD-appen.</span><span class="sxs-lookup"><span data-stu-id="9dd08-245">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="9dd08-246">Du må deretter bruke Azure AD-tokenet til å få *tilgangstokenet* fra sikkerhetstjenesten.</span><span class="sxs-lookup"><span data-stu-id="9dd08-246">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="9dd08-247">Hent et token for sikkerhetstjeneste ved å gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="9dd08-247">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="9dd08-248">Logg på Azure-portalen, og bruk det til å finne `clientId` og `clientSecret` for Supply Chain Management-appen.</span><span class="sxs-lookup"><span data-stu-id="9dd08-248">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="9dd08-249">Hent et Azure Active Directory-token (`aadToken`) ved å sende en HTTP-forespørsel med følgende egenskaper:</span><span class="sxs-lookup"><span data-stu-id="9dd08-249">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="9dd08-250">**URL-adresse** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="9dd08-250">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="9dd08-251">**Metode** - `GET`</span><span class="sxs-lookup"><span data-stu-id="9dd08-251">**Method** - `GET`</span></span>
    - <span data-ttu-id="9dd08-252">**Meldingstekst (skjemadata)**:</span><span class="sxs-lookup"><span data-stu-id="9dd08-252">**Body content (form data)**:</span></span>

        | <span data-ttu-id="9dd08-253">nøkkel</span><span class="sxs-lookup"><span data-stu-id="9dd08-253">key</span></span> | <span data-ttu-id="9dd08-254">verdi</span><span class="sxs-lookup"><span data-stu-id="9dd08-254">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="9dd08-255">client_id</span><span class="sxs-lookup"><span data-stu-id="9dd08-255">client_id</span></span> | <span data-ttu-id="9dd08-256">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="9dd08-256">${aadAppId}</span></span> |
        | <span data-ttu-id="9dd08-257">client_secret</span><span class="sxs-lookup"><span data-stu-id="9dd08-257">client_secret</span></span> | <span data-ttu-id="9dd08-258">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="9dd08-258">${aadAppSecret}</span></span> |
        | <span data-ttu-id="9dd08-259">grant_type</span><span class="sxs-lookup"><span data-stu-id="9dd08-259">grant_type</span></span> | <span data-ttu-id="9dd08-260">client_credentials</span><span class="sxs-lookup"><span data-stu-id="9dd08-260">client_credentials</span></span> |
        | <span data-ttu-id="9dd08-261">resource</span><span class="sxs-lookup"><span data-stu-id="9dd08-261">resource</span></span> | <span data-ttu-id="9dd08-262">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="9dd08-262">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="9dd08-263">Du skal motta et `aadToken` som svar, som ligner på følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="9dd08-263">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="9dd08-264">Formuler en JSON-forespørsel som ligner på følgende:</span><span class="sxs-lookup"><span data-stu-id="9dd08-264">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="9dd08-265">Der:</span><span class="sxs-lookup"><span data-stu-id="9dd08-265">Where:</span></span>
    - <span data-ttu-id="9dd08-266">Verdien for `client_assertion` må være `aadToken` du mottok i forrige trinn.</span><span class="sxs-lookup"><span data-stu-id="9dd08-266">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="9dd08-267">Verdien for `context` må være miljø-ID-en der du vil implementere tillegget.</span><span class="sxs-lookup"><span data-stu-id="9dd08-267">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="9dd08-268">Angi alle andre verdier som vist i eksemplet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-268">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="9dd08-269">Send en HTTP-forespørsel med følgende egenskaper:</span><span class="sxs-lookup"><span data-stu-id="9dd08-269">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="9dd08-270">**URL-adresse** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="9dd08-270">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="9dd08-271">**Metode** - `POST`</span><span class="sxs-lookup"><span data-stu-id="9dd08-271">**Method** - `POST`</span></span>
    - <span data-ttu-id="9dd08-272">**HTTP-hode** - Ta med API-versjonen (nøkkelen er `Api-Version` og verdien er `1.0`)</span><span class="sxs-lookup"><span data-stu-id="9dd08-272">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="9dd08-273">**Meldingstekst** - Ta med JSON-forespørselen du opprettet i forrige trinn.</span><span class="sxs-lookup"><span data-stu-id="9dd08-273">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="9dd08-274">Du får et `access_token` som svar.</span><span class="sxs-lookup"><span data-stu-id="9dd08-274">You will get an `access_token` in response.</span></span> <span data-ttu-id="9dd08-275">Dette er det du trenger som bærertoken for å kalle opp lagersynlighets-API-en.</span><span class="sxs-lookup"><span data-stu-id="9dd08-275">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="9dd08-276">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="9dd08-276">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a><span data-ttu-id="9dd08-277">Eksempelforespørsel</span><span class="sxs-lookup"><span data-stu-id="9dd08-277">Sample Request</span></span>

<span data-ttu-id="9dd08-278">For din referanse har du her et eksempel på en http-forespørsel. Du kan bruke alle verktøy eller kodingsspråk til å sende denne forespørselen, for eksempel ``Postman``.</span><span class="sxs-lookup"><span data-stu-id="9dd08-278">For your reference, here is a sample http request, you can use any tools or coding language to send this request, such as  ``Postman``.</span></span>

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="9dd08-279">Konfigurer API-en for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="9dd08-279">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="9dd08-280">Før du bruker tjenesten, må du fullføre konfigurasjonene som er beskrevet i følgende underavsnitt.</span><span class="sxs-lookup"><span data-stu-id="9dd08-280">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="9dd08-281">Konfigurasjonen kan variere avhengig av detaljene i miljøet ditt.</span><span class="sxs-lookup"><span data-stu-id="9dd08-281">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="9dd08-282">Den inneholder hovedsakelig fire deler:</span><span class="sxs-lookup"><span data-stu-id="9dd08-282">It primarily includes four parts:</span></span>

- [<span data-ttu-id="9dd08-283">Partisjonering</span><span class="sxs-lookup"><span data-stu-id="9dd08-283">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="9dd08-284">Dimensjonskonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="9dd08-284">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="9dd08-285">Indeksering</span><span class="sxs-lookup"><span data-stu-id="9dd08-285">Indexing</span></span>](#indexing)
- [<span data-ttu-id="9dd08-286">Egendefinert mål</span><span class="sxs-lookup"><span data-stu-id="9dd08-286">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="9dd08-287">Partisjonering</span><span class="sxs-lookup"><span data-stu-id="9dd08-287">Partitioning</span></span>

<span data-ttu-id="9dd08-288">Partisjonering kan påvirke ytelsen betydelig for API-en for lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-288">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="9dd08-289">Det er en god idé å definere et oppsett som tillater små grupperinger av data, samtidig som du tillater meningsfulle dataspørringer samtidig.</span><span class="sxs-lookup"><span data-stu-id="9dd08-289">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="9dd08-290">`organizationId` (`dataAreaId` i Supply Chain Management) vil alltid være en del av partisjonen, og standard lagersynlighet er satt til partisjonering per dimensjon som *Område + sted*.</span><span class="sxs-lookup"><span data-stu-id="9dd08-290">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="9dd08-291">Dette betyr at tjenesten alltid må spørres med disse dimensjonene som er definert i filtrene.</span><span class="sxs-lookup"><span data-stu-id="9dd08-291">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="9dd08-292">*Område* og *Sted* er to generelle standarddimensjoner i lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-292">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="9dd08-293">I Supply Chain Management kalles disse dimensjonene *Område* (`InventSiteId`) og *Lager* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="9dd08-293">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="9dd08-294">Dimensjonskonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="9dd08-294">Dimension configurations</span></span>

<span data-ttu-id="9dd08-295">Lagersynlighet inneholder en liste over generelle standarddimensjoner for å aktivere systemintegrasjon med flere kilder.</span><span class="sxs-lookup"><span data-stu-id="9dd08-295">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="9dd08-296">Tabellen nedenfor viser hvilke lagerdimensjoner som skal være standard dimensjonsnavn i lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-296">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="9dd08-297">Dimensjonstype</span><span class="sxs-lookup"><span data-stu-id="9dd08-297">Dimension type</span></span> | <span data-ttu-id="9dd08-298">Dimensjonsnavn</span><span class="sxs-lookup"><span data-stu-id="9dd08-298">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="9dd08-299">Produkt</span><span class="sxs-lookup"><span data-stu-id="9dd08-299">Product</span></span> | `ColorId` |
| <span data-ttu-id="9dd08-300">Produkt</span><span class="sxs-lookup"><span data-stu-id="9dd08-300">Product</span></span> | `SizeId` |
| <span data-ttu-id="9dd08-301">Produkt</span><span class="sxs-lookup"><span data-stu-id="9dd08-301">Product</span></span> | `StyleId` |
| <span data-ttu-id="9dd08-302">Produkt</span><span class="sxs-lookup"><span data-stu-id="9dd08-302">Product</span></span> | `ConfigId` |
| <span data-ttu-id="9dd08-303">Sporing</span><span class="sxs-lookup"><span data-stu-id="9dd08-303">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="9dd08-304">Sporing</span><span class="sxs-lookup"><span data-stu-id="9dd08-304">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="9dd08-305">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="9dd08-305">Location</span></span> | `LocationId` |
| <span data-ttu-id="9dd08-306">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="9dd08-306">Location</span></span> | `SiteId` |
| <span data-ttu-id="9dd08-307">Lagerstatus</span><span class="sxs-lookup"><span data-stu-id="9dd08-307">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="9dd08-308">Lagerspesifikk</span><span class="sxs-lookup"><span data-stu-id="9dd08-308">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="9dd08-309">Lagerspesifikk</span><span class="sxs-lookup"><span data-stu-id="9dd08-309">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="9dd08-310">Lagerspesifikk</span><span class="sxs-lookup"><span data-stu-id="9dd08-310">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="9dd08-311">Dimensjonstypen som er oppført i den forrige tabellen, er bare for referanse.</span><span class="sxs-lookup"><span data-stu-id="9dd08-311">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="9dd08-312">Du trenger ikke definere dimensjonstypen i Lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-312">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="9dd08-313">Hvis det finnes en egendefinert dimensjon som må flyte til en standardverdi når det brukes av lagersynlighet, kan du konfigurere navnet **Egendefinert dimensjon** i Lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-313">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="9dd08-314">Eksterne systemer har tilgang til lagersynlighet via RESTful-API-er som gir deg beholdningsinformasjon om gitte dimensjoner som det skal spørres om.</span><span class="sxs-lookup"><span data-stu-id="9dd08-314">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="9dd08-315">Ved integreringen kan du bruke Lagersynlighet til å konfigurere den *eksterne kanaldatakilden* og kildedimensjonen til *måldimensjonene* i Lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-315">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="9dd08-316">Måldimensjonene må være ett av følgende:</span><span class="sxs-lookup"><span data-stu-id="9dd08-316">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="9dd08-317">Standarddimensjoner i Lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="9dd08-317">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="9dd08-318">Egendefinerte dimensjoner</span><span class="sxs-lookup"><span data-stu-id="9dd08-318">Custom dimensions</span></span>

<span data-ttu-id="9dd08-319">Formålet med dimensjonskonfigurasjon er å standardisere integreringen med flere systemer for spørringen på dimensjoner og posteringshendelsen med dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="9dd08-319">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="9dd08-320">Indeksering</span><span class="sxs-lookup"><span data-stu-id="9dd08-320">Indexing</span></span>

<span data-ttu-id="9dd08-321">Vanligvis vil ikke lagerbeholdningsspørringen bare være på det høyeste totale nivået, men du vil kanskje se resultater som er aggregert basert på lagerdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="9dd08-321">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="9dd08-322">Lagersynlighet gir fleksibilitet ved å la deg definere indeksene som er basert på dimensjonen eller kombinasjonen av dimensjonene.</span><span class="sxs-lookup"><span data-stu-id="9dd08-322">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="9dd08-323">For øyeblikket kan du bare konfigurere indekser til maksimalt fem.</span><span class="sxs-lookup"><span data-stu-id="9dd08-323">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="9dd08-324">Du må nøye vurdere hvilken dimensjon eller dimensjonskombinasjon du vil bruke før implementeringen for å sikre at den oppfyller dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="9dd08-324">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="9dd08-325">Hvis du for eksempel vil spørre etter produkter som følger:</span><span class="sxs-lookup"><span data-stu-id="9dd08-325">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="9dd08-326">Forespør den aggregerte produktbeholdningen etter dimensjonene *Farge* og *Størrelse*.</span><span class="sxs-lookup"><span data-stu-id="9dd08-326">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="9dd08-327">I noen tilfeller vil du bare spørre om produktet totalt.</span><span class="sxs-lookup"><span data-stu-id="9dd08-327">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="9dd08-328">Du har to indekser definert som følgende:</span><span class="sxs-lookup"><span data-stu-id="9dd08-328">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="9dd08-329">Den tomme parentesen samles, basert på produkt-ID-en i partisjonen.</span><span class="sxs-lookup"><span data-stu-id="9dd08-329">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="9dd08-330">Indekseringen definerer hvordan du kan gruppere resultatene basert på `groupBy`-spørringsinnstillingen.</span><span class="sxs-lookup"><span data-stu-id="9dd08-330">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="9dd08-331">I dette tilfellet hvis du ikke definerer noen `groupBy`-verdier, får du totaler etter `productid`.</span><span class="sxs-lookup"><span data-stu-id="9dd08-331">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="9dd08-332">Hvis du definerer `groupBy` som `groupBy=ColorId&groupBy=SizeId`, vil du ellers få flere linjer returnert, basert på de ulike kombinasjonene mellom farger og størrelser i systemet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-332">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="9dd08-333">Du kan legge spørringskriteriene i brødteksten for forespørselen.</span><span class="sxs-lookup"><span data-stu-id="9dd08-333">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="9dd08-334">Her er en eksempelspørring på produktet med farge- og størrelseskombinasjon.</span><span class="sxs-lookup"><span data-stu-id="9dd08-334">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
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

<span data-ttu-id="9dd08-335">For `filters`-feltet støtter for øyeblikket bare `ProductId` flere verdier.</span><span class="sxs-lookup"><span data-stu-id="9dd08-335">For the `filters` field, currently only `ProductId` supports multiple values.</span></span> <span data-ttu-id="9dd08-336">Hvis `ProductId` er en tom matrise, vil alle produkter bli spurt etter.</span><span class="sxs-lookup"><span data-stu-id="9dd08-336">If the `ProductId` is an empty array, all products will be queried.</span></span>

#### <a name="custom-measurement"></a><span data-ttu-id="9dd08-337">Egendefinert mål</span><span class="sxs-lookup"><span data-stu-id="9dd08-337">Custom measurement</span></span>

<span data-ttu-id="9dd08-338">Standard målantall er koblet til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9dd08-338">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="9dd08-339">Det kan imidlertid være at du vil ha et antall som består av en kombinasjon av standardmålene.</span><span class="sxs-lookup"><span data-stu-id="9dd08-339">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="9dd08-340">Hvis du vil gjøre dette, kan du ha en konfigurasjon av egendefinert antall, som vil bli lagt til i utdataene i lagerbeholdningsspørringene.</span><span class="sxs-lookup"><span data-stu-id="9dd08-340">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="9dd08-341">Ved hjelp av funksjonaliteten kan du bare definere et sett med mål som skal legges til, eller et sett med mål som skal trekkes fra, for å kunne lage det egendefinerte målet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-341">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="9dd08-342">Med følgende spørringsvilkår vil du for eksempel konfigurere det egendefinerte målantallet som `MyCustomAvailableforReservation` som skal brukes av forbrukssystemet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-342">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="9dd08-343">Forbrukssystem</span><span class="sxs-lookup"><span data-stu-id="9dd08-343">Consumption system</span></span> | <span data-ttu-id="9dd08-344">Beregnede mål</span><span class="sxs-lookup"><span data-stu-id="9dd08-344">Calculated measurers</span></span> | <span data-ttu-id="9dd08-345">Datakilde</span><span class="sxs-lookup"><span data-stu-id="9dd08-345">Data source</span></span> | <span data-ttu-id="9dd08-346">Modifikator</span><span class="sxs-lookup"><span data-stu-id="9dd08-346">Modifier</span></span> | <span data-ttu-id="9dd08-347">Beregningstype for modifikator</span><span class="sxs-lookup"><span data-stu-id="9dd08-347">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="9dd08-348">Tillegg</span><span class="sxs-lookup"><span data-stu-id="9dd08-348">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="9dd08-349">Tillegg</span><span class="sxs-lookup"><span data-stu-id="9dd08-349">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="9dd08-350">Subtraksjon</span><span class="sxs-lookup"><span data-stu-id="9dd08-350">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="9dd08-351">Tillegg</span><span class="sxs-lookup"><span data-stu-id="9dd08-351">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="9dd08-352">Subtraksjon</span><span class="sxs-lookup"><span data-stu-id="9dd08-352">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="9dd08-353">Tillegg</span><span class="sxs-lookup"><span data-stu-id="9dd08-353">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="9dd08-354">Tillegg</span><span class="sxs-lookup"><span data-stu-id="9dd08-354">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="9dd08-355">Subtraksjon</span><span class="sxs-lookup"><span data-stu-id="9dd08-355">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="9dd08-356">Subtraksjon</span><span class="sxs-lookup"><span data-stu-id="9dd08-356">Subtraction</span></span> |

<span data-ttu-id="9dd08-357">Med dette vil spørringen på det egendefinerte målantallet returnere følgende utdata.</span><span class="sxs-lookup"><span data-stu-id="9dd08-357">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="9dd08-358">`MyCustomAvailableforReservation`-utdataene er basert på beregningsinnstillingen i de egendefinerte målene som:</span><span class="sxs-lookup"><span data-stu-id="9dd08-358">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="9dd08-359">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="9dd08-359">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="9dd08-360">Postere lagerendringer</span><span class="sxs-lookup"><span data-stu-id="9dd08-360">Posting on-hand changes</span></span>

<span data-ttu-id="9dd08-361">Den nøyaktige URL-adressen som hendelsen vil bli postert til, avhenger av det geografiske området.</span><span class="sxs-lookup"><span data-stu-id="9dd08-361">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="9dd08-362">Den tar følgende form:</span><span class="sxs-lookup"><span data-stu-id="9dd08-362">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="9dd08-363">Når den er godkjent, kan denne URL-adressen brukes sammen med HTTP `POST`-metoden til å sende lagerbeholdningshendelser til tjenesten.</span><span class="sxs-lookup"><span data-stu-id="9dd08-363">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="9dd08-364">En spesiell topptekst brukes til å kommunisere med Dynamics 365-tjenester via HTTP-forespørsler, og angir miljø-ID-en til Supply Chain Management-forkomten dataene er koblet til.</span><span class="sxs-lookup"><span data-stu-id="9dd08-364">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="9dd08-365">For eksempel:</span><span class="sxs-lookup"><span data-stu-id="9dd08-365">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="9dd08-366">Postere spørringer om lagerendringer eksempel 1</span><span class="sxs-lookup"><span data-stu-id="9dd08-366">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="9dd08-367">I dette eksemplet vises det et scenario der du kan definere dimensjonskonfigurasjonen i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="9dd08-367">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="9dd08-368">Bruk følgende spørring til å konfigurere dimensjonstilordningen i Power Apps:</span><span class="sxs-lookup"><span data-stu-id="9dd08-368">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="9dd08-369">Nå kan du angi `dimensionDataSource` og bruke egendefinerte dimensjoner i spørringene.</span><span class="sxs-lookup"><span data-stu-id="9dd08-369">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="9dd08-370">Systemet konverterer automatisk egendefinerte dimensjoner til basisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="9dd08-370">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="9dd08-371">Postere spørringer om lagerendringer eksempel 2</span><span class="sxs-lookup"><span data-stu-id="9dd08-371">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="9dd08-372">Dette eksemplet viser et scenario der ingen tilordninger er definert for dimensjonskonfigurasjonen i Power Apps, slik at posteringen også bør bruke basisdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="9dd08-372">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="9dd08-373">Alle dimensjoner må være basisdimensjoner når `dimensionDataSource`-feltet er null, tomt eller mellomrom.</span><span class="sxs-lookup"><span data-stu-id="9dd08-373">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="9dd08-374">Feltegenskaper for JSON-dokument</span><span class="sxs-lookup"><span data-stu-id="9dd08-374">JSON document field properties</span></span>

<span data-ttu-id="9dd08-375">Feltene fra JSON-spørringseksemplene som ble angitt tidligere, har egenskapene som er oppført i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="9dd08-375">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="9dd08-376">Felt-ID</span><span class="sxs-lookup"><span data-stu-id="9dd08-376">Field ID</span></span> | <span data-ttu-id="9dd08-377">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9dd08-377">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="9dd08-378">En unik ID for den bestemte endringshendelsen.</span><span class="sxs-lookup"><span data-stu-id="9dd08-378">A unique ID for the specific change event.</span></span> <span data-ttu-id="9dd08-379">Denne ID-en brukes til å sikre at hvis kommunikasjon med tjenesten mislykkes under posteringen, vil sendingen av hendelsen ikke resultere i at samme hendelse telles to ganger i systemet.</span><span class="sxs-lookup"><span data-stu-id="9dd08-379">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="9dd08-380">Identifikatoren til organisasjonen som er koblet til hendelsen.</span><span class="sxs-lookup"><span data-stu-id="9dd08-380">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="9dd08-381">Dette tilordner til ID-er til Supply Chain Management-organisasjoner eller dataområder.</span><span class="sxs-lookup"><span data-stu-id="9dd08-381">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="9dd08-382">Identifikatoren til produktet det gjelder.</span><span class="sxs-lookup"><span data-stu-id="9dd08-382">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="9dd08-383">Antallet som lagerbeholdningen må endres med.</span><span class="sxs-lookup"><span data-stu-id="9dd08-383">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="9dd08-384">Hvis for eksempel ti nye bagels er lagt til i en hylle, vil denne verdien være 10.</span><span class="sxs-lookup"><span data-stu-id="9dd08-384">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="9dd08-385">Hvis tre bagels deretter ble fjernet fra hyllen eller solgt, ville denne verdien være –3.</span><span class="sxs-lookup"><span data-stu-id="9dd08-385">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="9dd08-386">Datakilden for dimensjonene som brukes i posteringsendringshendelsen og -spørringen.</span><span class="sxs-lookup"><span data-stu-id="9dd08-386">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="9dd08-387">Hvis du angir datakilden, kan du bruke de egendefinerte dimensjonene fra den angitte datakilden.</span><span class="sxs-lookup"><span data-stu-id="9dd08-387">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="9dd08-388">Med dimensjonskonfigurasjonen kan Lagersynlighet tilordne de egendefinerte dimensjonene til de generelle standarddimensjonene.</span><span class="sxs-lookup"><span data-stu-id="9dd08-388">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="9dd08-389">Hvis `dimensionDataSource` ikke er angitt, kan du bare bruke de generelle standarddimensjonene i spørringene.</span><span class="sxs-lookup"><span data-stu-id="9dd08-389">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="9dd08-390">En dynamisk samling med nøkkel/verdi-par.</span><span class="sxs-lookup"><span data-stu-id="9dd08-390">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="9dd08-391">Disse vil tilordnes noen av dimensjonene i Supply Chain Management, men du kan også legge til egendefinerte dimensjoner (som *Kilde*) som kan angi om hendelsen kommer fra Supply Chain Management eller et eksternt system.</span><span class="sxs-lookup"><span data-stu-id="9dd08-391">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="9dd08-392">Spørring om aktuell lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="9dd08-392">Querying current on-hand</span></span>

<span data-ttu-id="9dd08-393">Endepunktet for spørringer av gjeldende lagerbeholdning vil ha en lignende URL-adresse:</span><span class="sxs-lookup"><span data-stu-id="9dd08-393">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="9dd08-394">Det blir spurt med HTTP `POST`-metoden.</span><span class="sxs-lookup"><span data-stu-id="9dd08-394">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="9dd08-395">Gjeldende beholdningsspørring, eksempel 1</span><span class="sxs-lookup"><span data-stu-id="9dd08-395">Current on-hand query example 1</span></span>

<span data-ttu-id="9dd08-396">I dette eksemplet vises det et scenario der du allerede har fullført dimensjonskonfigurasjonen i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="9dd08-396">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="9dd08-397">Bruk følgende spørring til å konfigurere dimensjonstilordningen i Power Apps:</span><span class="sxs-lookup"><span data-stu-id="9dd08-397">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="9dd08-398">Nå kan du angi `dimensionDataSource` og bruke egendefinerte dimensjoner i spørringene.</span><span class="sxs-lookup"><span data-stu-id="9dd08-398">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="9dd08-399">Systemet konverterer automatisk egendefinerte dimensjoner til basisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="9dd08-399">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="9dd08-400">Du kan angi `DimensionDataSource` i `filters` og angi egendefinerte dimensjoner i både `filters` og `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="9dd08-400">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="9dd08-401">Systemet konverterer automatisk egendefinerte dimensjoner til basisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="9dd08-401">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="9dd08-402">Gjeldende beholdningsspørring, eksempel 2</span><span class="sxs-lookup"><span data-stu-id="9dd08-402">Current on-hand query example 2</span></span>

<span data-ttu-id="9dd08-403">Dette eksemplet viser et scenario der ingen tilordninger er definert for dimensjonskonfigurasjonen i Power Apps, slik at posteringen også bør bruke basisdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="9dd08-403">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="9dd08-404">Alle dimensjoner må være basisdimensjoner når `dimensionDataSource`-feltet, under `filters`, er null, tomt eller mellomrom.</span><span class="sxs-lookup"><span data-stu-id="9dd08-404">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="9dd08-405">Eksempel på returresultat</span><span class="sxs-lookup"><span data-stu-id="9dd08-405">Example return result</span></span>

<span data-ttu-id="9dd08-406">Spørringene som vises i eksemplene ovenfor, kan returnere et resultat som dette.</span><span class="sxs-lookup"><span data-stu-id="9dd08-406">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="9dd08-407">Legg merke til at antall-feltene er strukturert som en ordliste for mål og tilknyttede verdier.</span><span class="sxs-lookup"><span data-stu-id="9dd08-407">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]