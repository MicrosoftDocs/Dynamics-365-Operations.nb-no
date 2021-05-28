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
ms.openlocfilehash: 84f5e949f0c81f840c8a9086d05bbcfc576e42aa
ms.sourcegitcommit: b67665ed689c55df1a67d1a7840947c3977d600c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6017012"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="d82a8-103">Tillegg for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="d82a8-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="d82a8-104">Tillegget for lagersynlighet er en uavhengig og høyt skalerbar mikrotjeneste som aktiverer beholdningssporing i sanntid, og gir dermed en global visning av lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="d82a8-105">All informasjon som er relatert til lagerbeholdningen, eksporteres til tjenesten via i SQL-integrasjon med minimal forsinkelse.</span><span class="sxs-lookup"><span data-stu-id="d82a8-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="d82a8-106">Eksterne systemer får tilgang til tjenesten via RESTful-API-er for spørring om lagerbeholdningsinformasjon for gitte sett med dimensjoner, og dermed hente en liste over tilgjengelige lagerbeholdninger.</span><span class="sxs-lookup"><span data-stu-id="d82a8-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="d82a8-107">Lagersynlighet er en mikrotjeneste som er bygd på Microsoft Dataverse, som betyr at du kan utvide den ved å bygge Power Apps og bruke Power BI til å oppgi egendefinert funksjonalitet som dekker dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="d82a8-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="d82a8-108">Det er også mulig å oppgradere indeksen for å utføre lagerspørringer.</span><span class="sxs-lookup"><span data-stu-id="d82a8-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="d82a8-109">Lagersynlighet inneholder konfigurasjonsalternativer som gjør at den kan integreres med flere tredjepartssystemer.</span><span class="sxs-lookup"><span data-stu-id="d82a8-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="d82a8-110">Den støtter den standardiserte lagerdimensjonen, egendefinert utvidelse og standardisert beregnet antall som kan konfigureres.</span><span class="sxs-lookup"><span data-stu-id="d82a8-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="d82a8-111">Dette emnet beskriver hvordan du installerer og konfigurerer tillegget for lagersynlighet for Dynamics 365 Supply Chain Management, og hvordan du bruker app-programmeringsgrensesnittet (API).</span><span class="sxs-lookup"><span data-stu-id="d82a8-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="d82a8-112">Installer tillegget for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="d82a8-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="d82a8-113">Du må installere tillegget for lagersynlighet ved hjelp av Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="d82a8-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="d82a8-114">LCS er en samarbeidsportal som gir et miljø og et sett med jevnlig oppdaterte tjenester som hjelper deg med å administrere applivssyklusen til Dynamics 365 Finance and Operations-appene dine.</span><span class="sxs-lookup"><span data-stu-id="d82a8-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="d82a8-115">Hvis du vil ha mer informasjon, se [Lifecycle Services-ressurser](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span><span class="sxs-lookup"><span data-stu-id="d82a8-115">For more information, see [Lifecycle Services resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span></span>

### <a name="inventory-visibility-add-in-prerequisites"></a><span data-ttu-id="d82a8-116">Forutsetninger for tillegg for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="d82a8-116">Inventory Visibility Add-in prerequisites</span></span>

<span data-ttu-id="d82a8-117">Før du kan installere tillegget for lagersynlighet, må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="d82a8-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="d82a8-118">Hent et LCS-implementeringsprosjekt med minst ett miljø som er distribuert.</span><span class="sxs-lookup"><span data-stu-id="d82a8-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="d82a8-119">Sørg for at forutsetningene for å definere tillegg som er oppført i [Tilleggsoversikt](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md), er fullført.</span><span class="sxs-lookup"><span data-stu-id="d82a8-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="d82a8-120">Lagersynlighet krever ikke kobling til dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="d82a8-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="d82a8-121">Kontakt lagersynlighetsteamet på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for å få følgende tre obligatoriske filer:</span><span class="sxs-lookup"><span data-stu-id="d82a8-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>
  - `Inventory Visibility Dataverse Solution.zip`
  - `Inventory Visibility Configuration Trigger.zip`
  - <span data-ttu-id="d82a8-122">`Inventory Visibility Integration.zip` (hvis versjonen av Supply Chain Management du kjører, er eldre enn versjon 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="d82a8-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>
- <span data-ttu-id="d82a8-123">Du kan eventuelt kontakte lagersynlighetsteamet på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for å få Package Deployer-pakker:</span><span class="sxs-lookup"><span data-stu-id="d82a8-123">Alternatively, contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package deployer packages.</span></span> <span data-ttu-id="d82a8-124">Disse pakkene kan brukes av et offisielt Package Deployer-verktøy.</span><span class="sxs-lookup"><span data-stu-id="d82a8-124">These packages can be used by an official package deployer tool.</span></span>
  - `InventoryServiceBase.PackageDeployer.zip`
  - <span data-ttu-id="d82a8-125">`InventoryServiceApplication.PackageDeployer.zip` (denne pakken inneholder alle endringene i `InventoryServiceBase`-pakken pluss ekstra grensesnittprogramkomponenter)</span><span class="sxs-lookup"><span data-stu-id="d82a8-125">`InventoryServiceApplication.PackageDeployer.zip` (this package contains all of the changes in the `InventoryServiceBase` package, plus additional UI application components)</span></span>
- <span data-ttu-id="d82a8-126">Følg instruksjonene gitt i [Hurtigstart: Registrere en app med Microsoft-identitetsplattformen](/azure/active-directory/develop/quickstart-register-app) for å registrere en app og legge til en klienthemmelighet for AAD under Azure-abonnementet ditt.</span><span class="sxs-lookup"><span data-stu-id="d82a8-126">Follow the instructions given in [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register an application and add a client secret to AAD under your azure subscription.</span></span>
  - [<span data-ttu-id="d82a8-127">Registrere en app</span><span class="sxs-lookup"><span data-stu-id="d82a8-127">Register an application</span></span>](/azure/active-directory/develop/quickstart-register-app)
  - [<span data-ttu-id="d82a8-128">Legge til en klienthemmelighet</span><span class="sxs-lookup"><span data-stu-id="d82a8-128">Add a client secret</span></span>](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
  - <span data-ttu-id="d82a8-129">**App-ID (klient)**, **Klienthemmelighet** og **Leier-ID** vil bli brukt i trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="d82a8-129">The **Application(Client) Id**, **Client Secret**, and **Tenant ID** will be used in the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="d82a8-130">Landene og områdene som støttes for øyeblikket, omfatter Canada, USA og Den europeiske union (EU).</span><span class="sxs-lookup"><span data-stu-id="d82a8-130">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="d82a8-131">Hvis du har spørsmål om disse forutsetningene, kan du ta kontakt med produktteamet for lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-131">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="d82a8-132">Konfigurere Dataverse</span><span class="sxs-lookup"><span data-stu-id="d82a8-132">Set up Dataverse</span></span>

<span data-ttu-id="d82a8-133">Hvis du vil konfigurere Dataverse for bruk med lagersynlighet, må du først klargjøre forhåndskravene og deretter bestemme om du vil konfigurere Dataverse ved hjelp av enten Package Deployer-verktøyet eller ved å importere løsningene manuelt (du trenger ikke å gjøre begge deler).</span><span class="sxs-lookup"><span data-stu-id="d82a8-133">To set up Dataverse for use with Inventory Visibility, you must first prepare the prerequisites and then decide whether to set up Dataverse using either the package deployer tool or by manually importing the solutions (you don't have to do both).</span></span> <span data-ttu-id="d82a8-134">Deretter installerer du tillegget for lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-134">Then install the Inventory Visibility Add-in.</span></span> <span data-ttu-id="d82a8-135">Følgende underdeler beskriver hvordan du fullfører hver av disse oppgavene.</span><span class="sxs-lookup"><span data-stu-id="d82a8-135">The following subsections describe how to complete each of these tasks.</span></span>

#### <a name="prepare-dataverse-prerequisites"></a><span data-ttu-id="d82a8-136">Forutsetninger for Dataverse-klargjøring</span><span class="sxs-lookup"><span data-stu-id="d82a8-136">Prepare Dataverse prerequisites</span></span>

<span data-ttu-id="d82a8-137">Før du begynner å definere Dataverse legger du til et serviceprinsipp i leietakeren ved å gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="d82a8-137">Before you start to set up Dataverse, add a service principle to your tenant by doing the following:</span></span>

1. <span data-ttu-id="d82a8-138">Installer Azure AD PowerShell-modul v2 som beskrevet i [Installer Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="d82a8-138">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>

1. <span data-ttu-id="d82a8-139">Kjør følgende PowerShell-kommando:</span><span class="sxs-lookup"><span data-stu-id="d82a8-139">Run the following PowerShell command:</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)
    
    New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
    ```

#### <a name="set-up-dataverse-using-the-package-deployer-tool"></a><span data-ttu-id="d82a8-140">Konfigurere Dataverse ved hjelp av Package Deployer-verktøyet</span><span class="sxs-lookup"><span data-stu-id="d82a8-140">Set up Dataverse using the package deployer tool</span></span>

<span data-ttu-id="d82a8-141">Når du har forutsetningene på plass, bruker du fremgangsmåten nedenfor hvis du foretrekker å konfigurere Dataverse ved hjelp av Package Deployer-verktøyet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-141">After you have the prerequisites in place, use the following procedure if you prefer to set up Dataverse using the package deployer tool.</span></span> <span data-ttu-id="d82a8-142">Se den neste delen hvis du vil ha mer informasjon om hvordan du importerer løsningene manuelt i stedet (ikke gjør begge deler).</span><span class="sxs-lookup"><span data-stu-id="d82a8-142">See the next section for details about how to import the solutions manually instead (don't do both).</span></span>

1. <span data-ttu-id="d82a8-143">Installer utviklerverktøy som beskrevet i [Nedlastingsverktøy fra NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).</span><span class="sxs-lookup"><span data-stu-id="d82a8-143">Install developer tools as described in [Download tools from NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).</span></span>

1. <span data-ttu-id="d82a8-144">Basert på forretningskravene velger du `InventoryServiceBase`- eller `InventoryServiceApplication`-pakken.</span><span class="sxs-lookup"><span data-stu-id="d82a8-144">Based on your business requirements, choose the `InventoryServiceBase` or `InventoryServiceApplication` package.</span></span>

1. <span data-ttu-id="d82a8-145">Importer løsningene:</span><span class="sxs-lookup"><span data-stu-id="d82a8-145">Import the solutions:</span></span>
    1. <span data-ttu-id="d82a8-146">For `InventoryServiceBase`-pakken:</span><span class="sxs-lookup"><span data-stu-id="d82a8-146">For the `InventoryServiceBase` package:</span></span>
        - <span data-ttu-id="d82a8-147">Pakke ut `InventoryServiceBase.PackageDeployer.zip`</span><span class="sxs-lookup"><span data-stu-id="d82a8-147">Unzip `InventoryServiceBase.PackageDeployer.zip`</span></span>
        - <span data-ttu-id="d82a8-148">Finn mappen `InventoryServiceBase`, filen `[Content_Types].xml`, filen `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll`, filen `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` og filen `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`.</span><span class="sxs-lookup"><span data-stu-id="d82a8-148">Find folder `InventoryServiceBase`, file `[Content_Types].xml`, file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll`, file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`, and file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`.</span></span> 
        - <span data-ttu-id="d82a8-149">Kopier hver av disse mappene og filene til `.\Tools\PackageDeployment`-katalogen, som ble opprettet da du installerte utviklerverktøyene.</span><span class="sxs-lookup"><span data-stu-id="d82a8-149">Copy each of these folders and files to the `.\Tools\PackageDeployment` directory, which was created when you installed the developer tools.</span></span>
    1. <span data-ttu-id="d82a8-150">For `InventoryServiceApplication`-pakken:</span><span class="sxs-lookup"><span data-stu-id="d82a8-150">For the `InventoryServiceApplication` package:</span></span>
        - <span data-ttu-id="d82a8-151">Pakke ut `InventoryServiceApplication.PackageDeployer.zip`</span><span class="sxs-lookup"><span data-stu-id="d82a8-151">Unzip `InventoryServiceApplication.PackageDeployer.zip`</span></span>
        - <span data-ttu-id="d82a8-152">Finn mappen `InventoryServiceApplication`, filen `[Content_Types].xml`, filen `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`, filen `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` og filen `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.</span><span class="sxs-lookup"><span data-stu-id="d82a8-152">Find folder `InventoryServiceApplication`, file `[Content_Types].xml`, file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`, file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`, and file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.</span></span>
        - <span data-ttu-id="d82a8-153">Kopier hver av disse mappene og filene til `.\Tools\PackageDeployment`-katalogen, som ble opprettet da du installerte utviklerverktøyene.</span><span class="sxs-lookup"><span data-stu-id="d82a8-153">Copy each of these folders and files to the `.\Tools\PackageDeployment` directory, which was created when you installed the developer tools.</span></span>
    1. <span data-ttu-id="d82a8-154">Kjør `.\Tools\PackageDeployment\PackageDeployer.exe`.</span><span class="sxs-lookup"><span data-stu-id="d82a8-154">Execute `.\Tools\PackageDeployment\PackageDeployer.exe`.</span></span> <span data-ttu-id="d82a8-155">Følg instruksjonene på skjermen for å importere løsningene.</span><span class="sxs-lookup"><span data-stu-id="d82a8-155">Follow the instructions on your screen to import the solutions.</span></span>

1. <span data-ttu-id="d82a8-156">Tilordne sikkerhetsroller til programbrukeren.</span><span class="sxs-lookup"><span data-stu-id="d82a8-156">Assign security roles to the application user.</span></span>
    1. <span data-ttu-id="d82a8-157">Åpne URL-adressen for Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-157">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="d82a8-158">Gå til **Avansert innstilling \> System \> Sikkerhet \> Brukere**, og finn brukeren med navnet **# InventoryVisibility**.</span><span class="sxs-lookup"><span data-stu-id="d82a8-158">Go to **Advanced Setting \> System \> Security \> Users**, and find user the named **# InventoryVisibility**.</span></span>
    1. <span data-ttu-id="d82a8-159">Velg **Tilordne rolle**, og velg deretter **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="d82a8-159">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="d82a8-160">Hvis det finnes en rolle kalt **Common Data Service-bruker**, velger du den også.</span><span class="sxs-lookup"><span data-stu-id="d82a8-160">If there is a role that is named **Common Data Service User**, select it as well.</span></span>

#### <a name="set-up-dataverse-manually-by-importing-solutions"></a><span data-ttu-id="d82a8-161">Konfigurere Dataverse manuelt ved å importere løsninger</span><span class="sxs-lookup"><span data-stu-id="d82a8-161">Set up Dataverse manually by importing solutions</span></span>

<span data-ttu-id="d82a8-162">Når du har forutsetningene på plass, bruker du fremgangsmåten nedenfor hvis du foretrekker å konfigurere Dataverse ved å importere løsninger manuelt.</span><span class="sxs-lookup"><span data-stu-id="d82a8-162">After you have the prerequisites in place, use the following procedure if you prefer to set up Dataverse by manually importing solutions.</span></span> <span data-ttu-id="d82a8-163">Se den forrige delen hvis du vil ha mer informasjon om hvordan du bruker Package Deployer-verktøyet i stedet (ikke gjør begge deler).</span><span class="sxs-lookup"><span data-stu-id="d82a8-163">See the previous section for details about how to use the package deployer tool instead (don't do both).</span></span>

1. <span data-ttu-id="d82a8-164">Opprett en applikasjonsbruker for lagersynlighet i Dataverse:</span><span class="sxs-lookup"><span data-stu-id="d82a8-164">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="d82a8-165">Åpne URL-adressen for Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-165">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="d82a8-166">Gå til **Avansert innstilling \> System \> Sikkerhet \> Brukere** og opporett en appbruker.</span><span class="sxs-lookup"><span data-stu-id="d82a8-166">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="d82a8-167">Bruk Vis-menyen til å endre sidevisningen til **Appbrukere**.</span><span class="sxs-lookup"><span data-stu-id="d82a8-167">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="d82a8-168">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d82a8-168">Select **New**.</span></span> <span data-ttu-id="d82a8-169">Sett app-ID-en til *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="d82a8-169">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="d82a8-170">(Objekt-ID-en lastes automatisk når du lagrer endringene.) Du kan tilpasse navnet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-170">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="d82a8-171">Du kan for eksempel endre til *Lagersynlighet*.</span><span class="sxs-lookup"><span data-stu-id="d82a8-171">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="d82a8-172">Når du er ferdig, velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="d82a8-172">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="d82a8-173">Velg **Tilordne rolle**, og velg deretter **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="d82a8-173">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="d82a8-174">Hvis det finnes en rolle kalt **Common Data Service-bruker**, velger du den også.</span><span class="sxs-lookup"><span data-stu-id="d82a8-174">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="d82a8-175">Hvis du vil ha mer informasjon, kan du se [Opprette en appbruker](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="d82a8-175">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="d82a8-176">Hvis standardspråket for Dataverse ikke er **engelsk**:</span><span class="sxs-lookup"><span data-stu-id="d82a8-176">If the default language of your Dataverse is not **English**:</span></span>

    1. <span data-ttu-id="d82a8-177">Gå til **Avanserte innstillinger \> Administrasjon \> Språk**,</span><span class="sxs-lookup"><span data-stu-id="d82a8-177">Go to **Advanced Setting \> Administration \> Languages**,</span></span>
    1. <span data-ttu-id="d82a8-178">Velg **Engelsk (språkkode=1033)**, og velg **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="d82a8-178">Select **English (LanguageCode=1033)** and select **Apply**.</span></span>

1. <span data-ttu-id="d82a8-179">Importer `Inventory Visibility Dataverse Solution.zip`-filen, som inkluderer relaterte enheter for konfigurasjon av Dataverse og Power Apps:</span><span class="sxs-lookup"><span data-stu-id="d82a8-179">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="d82a8-180">Gå til siden **Løsninger**.</span><span class="sxs-lookup"><span data-stu-id="d82a8-180">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="d82a8-181">Velg **Import**.</span><span class="sxs-lookup"><span data-stu-id="d82a8-181">Select **Import**.</span></span>

1. <span data-ttu-id="d82a8-182">Importer utløserflyten for konfigurasjonsoppgradering:</span><span class="sxs-lookup"><span data-stu-id="d82a8-182">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="d82a8-183">Gå til Microsoft Flow-siden.</span><span class="sxs-lookup"><span data-stu-id="d82a8-183">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="d82a8-184">Sørg for at det finnes en tilkobling med navnet *Dataverse (eldre)*.</span><span class="sxs-lookup"><span data-stu-id="d82a8-184">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="d82a8-185">(Hvis den ikke finnes, kan du opprette den.)</span><span class="sxs-lookup"><span data-stu-id="d82a8-185">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="d82a8-186">Importer `Inventory Visibility Configuration Trigger.zip`-filen.</span><span class="sxs-lookup"><span data-stu-id="d82a8-186">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="d82a8-187">Når den er importert, vises utløseren under **Mine flyter**.</span><span class="sxs-lookup"><span data-stu-id="d82a8-187">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="d82a8-188">Initialiser følgende fire variabler basert på miljøinformasjon:</span><span class="sxs-lookup"><span data-stu-id="d82a8-188">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="d82a8-189">Leier-ID for Azure</span><span class="sxs-lookup"><span data-stu-id="d82a8-189">Azure Tenant ID</span></span>
        - <span data-ttu-id="d82a8-190">Appklient-ID for Azure</span><span class="sxs-lookup"><span data-stu-id="d82a8-190">Azure Application Client ID</span></span>
        - <span data-ttu-id="d82a8-191">Appklienthemmelighet for Azure</span><span class="sxs-lookup"><span data-stu-id="d82a8-191">Azure Application Client Secret</span></span>
        - <span data-ttu-id="d82a8-192">Endepunkt for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="d82a8-192">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="d82a8-193">Hvis du vil ha mer informasjon om denne variabelen, kan du se delen [Konfigurere integrering av lagersynlighet](#setup-inventory-visibility-integration) senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-193">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="d82a8-194">![Konfigurasjonsutløser](media/configuration-trigger.png "Konfigurasjonsutløser")</span><span class="sxs-lookup"><span data-stu-id="d82a8-194">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="d82a8-195">Velg **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="d82a8-195">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="d82a8-196">Installer tillegget</span><span class="sxs-lookup"><span data-stu-id="d82a8-196">Install the add-in</span></span>

<span data-ttu-id="d82a8-197">Hvis du vil installere tillegget for lagersynlighet, må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="d82a8-197">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="d82a8-198">Logg på [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index)-portalen.</span><span class="sxs-lookup"><span data-stu-id="d82a8-198">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="d82a8-199">På hjemmesiden velger du prosjektet der miljøet er distribuert.</span><span class="sxs-lookup"><span data-stu-id="d82a8-199">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="d82a8-200">På prosjektsiden velger du miljøet du vil installere tillegget i.</span><span class="sxs-lookup"><span data-stu-id="d82a8-200">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="d82a8-201">På miljøsiden ruller du ned til du ser delen delen **Miljøtillegg** i delen **Power Platform-integrering**, der du også finner navnet på Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-201">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="d82a8-202">I delen **Miljøtillegg** velger du **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="d82a8-202">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="d82a8-203">![Miljøsiden i LCS](media/inventory-visibility-environment.png "Miljøsiden i LCS")</span><span class="sxs-lookup"><span data-stu-id="d82a8-203">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="d82a8-204">Velg koblingen **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="d82a8-204">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="d82a8-205">En liste over tilgjengelige tillegg åpnes.</span><span class="sxs-lookup"><span data-stu-id="d82a8-205">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="d82a8-206">Velg **Lagersynlighet** i listen.</span><span class="sxs-lookup"><span data-stu-id="d82a8-206">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="d82a8-207">Angi verdier for følgende felter i miljøet:</span><span class="sxs-lookup"><span data-stu-id="d82a8-207">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="d82a8-208">**ID for AAD-app (klient)**</span><span class="sxs-lookup"><span data-stu-id="d82a8-208">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="d82a8-209">**Leier-ID for AAD**</span><span class="sxs-lookup"><span data-stu-id="d82a8-209">**AAD tenant ID**</span></span>

    <span data-ttu-id="d82a8-210">![Legg til i konfigurasjon-side](media/inventory-visibility-setup.png "Legg til i konfigurasjon-side")</span><span class="sxs-lookup"><span data-stu-id="d82a8-210">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="d82a8-211">Godta vilkåret og betingelsen ved å merke av for **Vilkår og betingelser**.</span><span class="sxs-lookup"><span data-stu-id="d82a8-211">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="d82a8-212">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="d82a8-212">Select **Install**.</span></span> <span data-ttu-id="d82a8-213">Statusen for tillegget vil vises som **Installerer**.</span><span class="sxs-lookup"><span data-stu-id="d82a8-213">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="d82a8-214">Når du er ferdig, oppdaterer du siden for å se status endre til **Installert**.</span><span class="sxs-lookup"><span data-stu-id="d82a8-214">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="d82a8-215">Avinstallere tillegget</span><span class="sxs-lookup"><span data-stu-id="d82a8-215">Uninstall the add-in</span></span>

<span data-ttu-id="d82a8-216">Velg **Avinstaller** tillegget for å avinstallere tillegget.</span><span class="sxs-lookup"><span data-stu-id="d82a8-216">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="d82a8-217">Når du oppdaterer LCS, fjernes tillegget for lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-217">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="d82a8-218">Avinstallasjonsprosessen fjerner registreringen av tillegget, og starter også en jobb for å rydde opp i alle forretningsdataene som er lagret i tjenesten.</span><span class="sxs-lookup"><span data-stu-id="d82a8-218">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="d82a8-219">Bruke lagerbeholdningsdata fra Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d82a8-219">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="d82a8-220">Distribuere integreringspakken for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="d82a8-220">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="d82a8-221">Hvis du kjører Supply Chain Management versjon 10.0.17 eller tidligere, kan du kontakte kundestøttegruppen for lagersynlighet på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for å hente pakkefilen.</span><span class="sxs-lookup"><span data-stu-id="d82a8-221">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="d82a8-222">Deretter distribuerer du pakken i LCS.</span><span class="sxs-lookup"><span data-stu-id="d82a8-222">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="d82a8-223">Hvis det oppstår en versjonsfeil under distribusjon, må du importere X++-prosjektet til utviklingsmiljøet manuelt.</span><span class="sxs-lookup"><span data-stu-id="d82a8-223">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="d82a8-224">Opprett deretter den distribuerbare pakken i utviklingsmiljøet, og distribuer den i produksjonsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-224">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="d82a8-225">Koden er inkludert i Supply Chain Management versjon 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="d82a8-225">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="d82a8-226">Hvis du kjører den versjonen eller senere, er det ikke nødvendig å distribuere påkrevd distribusjon.</span><span class="sxs-lookup"><span data-stu-id="d82a8-226">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="d82a8-227">Sørg for at følgende funksjoner er aktivert i miljøet i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d82a8-227">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="d82a8-228">(De er som standard aktiverte.)</span><span class="sxs-lookup"><span data-stu-id="d82a8-228">(By default, they are turned on.)</span></span>

| <span data-ttu-id="d82a8-229">Funksjonsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="d82a8-229">Feature description</span></span> | <span data-ttu-id="d82a8-230">Kodeversjon</span><span class="sxs-lookup"><span data-stu-id="d82a8-230">Code version</span></span> | <span data-ttu-id="d82a8-231">Veksle klasse</span><span class="sxs-lookup"><span data-stu-id="d82a8-231">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="d82a8-232">Aktivere eller deaktivere bruk av lagerdimensjoner i InventSum-tabell</span><span class="sxs-lookup"><span data-stu-id="d82a8-232">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="d82a8-233">10.0.11</span><span class="sxs-lookup"><span data-stu-id="d82a8-233">10.0.11</span></span> | <span data-ttu-id="d82a8-234">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="d82a8-234">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="d82a8-235">Aktivere eller deaktivere bruk av lagerdimensjoner i InventSumDelta-tabell</span><span class="sxs-lookup"><span data-stu-id="d82a8-235">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="d82a8-236">10.0.12</span><span class="sxs-lookup"><span data-stu-id="d82a8-236">10.0.12</span></span> | <span data-ttu-id="d82a8-237">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="d82a8-237">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="d82a8-238">Definer integrering av lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="d82a8-238">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="d82a8-239">I Supply Chain Management åpner du arbeidsområdet **[Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og aktiverer funksjonen **Integrering av lagersynlighet**.</span><span class="sxs-lookup"><span data-stu-id="d82a8-239">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="d82a8-240">Gå til **Lagerstyring \> Konfigurere \> Parametere for integrering av lagersynlighet**, og angi URL-adressen for miljøet der du kjører Lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-240">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="d82a8-241">Finn LCS-miljøets Azure-område, og skriv deretter inn URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="d82a8-241">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="d82a8-242">URL-adressen har følgende skjema:</span><span class="sxs-lookup"><span data-stu-id="d82a8-242">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="d82a8-243">Hvis du for eksempel er i Europa, vil miljøet ditt ha en av følgende URL-adresser:</span><span class="sxs-lookup"><span data-stu-id="d82a8-243">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="d82a8-244">Følgende områder er for øyeblikket tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="d82a8-244">The following regions are currently available.</span></span>

    | <span data-ttu-id="d82a8-245">Azure-område</span><span class="sxs-lookup"><span data-stu-id="d82a8-245">Azure region</span></span> | <span data-ttu-id="d82a8-246">Kortnavn for område</span><span class="sxs-lookup"><span data-stu-id="d82a8-246">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="d82a8-247">Australia øst</span><span class="sxs-lookup"><span data-stu-id="d82a8-247">Australia east</span></span> | <span data-ttu-id="d82a8-248">eau</span><span class="sxs-lookup"><span data-stu-id="d82a8-248">eau</span></span> |
    | <span data-ttu-id="d82a8-249">Australia, sørøst</span><span class="sxs-lookup"><span data-stu-id="d82a8-249">Australia southeast</span></span> | <span data-ttu-id="d82a8-250">seau</span><span class="sxs-lookup"><span data-stu-id="d82a8-250">seau</span></span> |
    | <span data-ttu-id="d82a8-251">Midt-Canada</span><span class="sxs-lookup"><span data-stu-id="d82a8-251">Canada central</span></span> | <span data-ttu-id="d82a8-252">cca</span><span class="sxs-lookup"><span data-stu-id="d82a8-252">cca</span></span> |
    | <span data-ttu-id="d82a8-253">Canada, øst</span><span class="sxs-lookup"><span data-stu-id="d82a8-253">Canada east</span></span> | <span data-ttu-id="d82a8-254">eca</span><span class="sxs-lookup"><span data-stu-id="d82a8-254">eca</span></span> |
    | <span data-ttu-id="d82a8-255">Europa nord</span><span class="sxs-lookup"><span data-stu-id="d82a8-255">North Europe</span></span> | <span data-ttu-id="d82a8-256">neu</span><span class="sxs-lookup"><span data-stu-id="d82a8-256">neu</span></span> |
    | <span data-ttu-id="d82a8-257">Europa vest</span><span class="sxs-lookup"><span data-stu-id="d82a8-257">West Europe</span></span> | <span data-ttu-id="d82a8-258">weu</span><span class="sxs-lookup"><span data-stu-id="d82a8-258">weu</span></span> |
    | <span data-ttu-id="d82a8-259">USA øst</span><span class="sxs-lookup"><span data-stu-id="d82a8-259">East US</span></span> | <span data-ttu-id="d82a8-260">eus</span><span class="sxs-lookup"><span data-stu-id="d82a8-260">eus</span></span> |
    | <span data-ttu-id="d82a8-261">USA vest</span><span class="sxs-lookup"><span data-stu-id="d82a8-261">West US</span></span> | <span data-ttu-id="d82a8-262">wus</span><span class="sxs-lookup"><span data-stu-id="d82a8-262">wus</span></span> |

1. <span data-ttu-id="d82a8-263">Gå til **Lagerstyring \> Periodisk \> Integrering av lagersynlighet** og aktiver jobben.</span><span class="sxs-lookup"><span data-stu-id="d82a8-263">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="d82a8-264">Alle lagerendringshendelser fra Supply Chain Management posteres nå til Lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-264">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="d82a8-265">Den offentlige API-en for tillegget for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="d82a8-265">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="d82a8-266">Den offentlige REST-API-en i tillegget for lagersynlighet viser flere spesifikke endepunkter for integrering.</span><span class="sxs-lookup"><span data-stu-id="d82a8-266">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="d82a8-267">Det støtter tre hovedtyper for samhandling:</span><span class="sxs-lookup"><span data-stu-id="d82a8-267">It supports three main interaction types:</span></span>

- <span data-ttu-id="d82a8-268">Postering av beholdningsendringer i tillegget fra et eksternt system</span><span class="sxs-lookup"><span data-stu-id="d82a8-268">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="d82a8-269">Spørring etter gjeldende antall i beholdningen fra et eksternt system</span><span class="sxs-lookup"><span data-stu-id="d82a8-269">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="d82a8-270">Automatisk synkronisering med beholdningen for Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d82a8-270">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="d82a8-271">Automatisk synkronisering er ikke en del av den offentlige API-en.</span><span class="sxs-lookup"><span data-stu-id="d82a8-271">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="d82a8-272">I stedet håndteres den i bakgrunnen for miljøer der tillegget for lagersynlighet er aktivert.</span><span class="sxs-lookup"><span data-stu-id="d82a8-272">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="d82a8-273">Godkjenning</span><span class="sxs-lookup"><span data-stu-id="d82a8-273">Authentication</span></span>

<span data-ttu-id="d82a8-274">Platformsikkerhetstokenet brukes til å kalle inn tillegget for lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-274">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="d82a8-275">Derfor må du generere et *Azure Active Directory-token (Azure AD)* ved hjelp av Azure AD-appen.</span><span class="sxs-lookup"><span data-stu-id="d82a8-275">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="d82a8-276">Du må deretter bruke Azure AD-tokenet til å få *tilgangstokenet* fra sikkerhetstjenesten.</span><span class="sxs-lookup"><span data-stu-id="d82a8-276">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="d82a8-277">Hent et token for sikkerhetstjeneste ved å gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="d82a8-277">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="d82a8-278">Logg på Azure-portalen, og bruk det til å finne `clientId` og `clientSecret` for Supply Chain Management-appen.</span><span class="sxs-lookup"><span data-stu-id="d82a8-278">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="d82a8-279">Hent et Azure Active Directory-token (`aadToken`) ved å sende en HTTP-forespørsel med følgende egenskaper:</span><span class="sxs-lookup"><span data-stu-id="d82a8-279">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="d82a8-280">**URL-adresse** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="d82a8-280">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="d82a8-281">**Metode** - `GET`</span><span class="sxs-lookup"><span data-stu-id="d82a8-281">**Method** - `GET`</span></span>
    - <span data-ttu-id="d82a8-282">**Meldingstekst (skjemadata)**:</span><span class="sxs-lookup"><span data-stu-id="d82a8-282">**Body content (form data)**:</span></span>

        | <span data-ttu-id="d82a8-283">nøkkel</span><span class="sxs-lookup"><span data-stu-id="d82a8-283">key</span></span> | <span data-ttu-id="d82a8-284">verdi</span><span class="sxs-lookup"><span data-stu-id="d82a8-284">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="d82a8-285">client_id</span><span class="sxs-lookup"><span data-stu-id="d82a8-285">client_id</span></span> | <span data-ttu-id="d82a8-286">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="d82a8-286">${aadAppId}</span></span> |
        | <span data-ttu-id="d82a8-287">client_secret</span><span class="sxs-lookup"><span data-stu-id="d82a8-287">client_secret</span></span> | <span data-ttu-id="d82a8-288">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="d82a8-288">${aadAppSecret}</span></span> |
        | <span data-ttu-id="d82a8-289">grant_type</span><span class="sxs-lookup"><span data-stu-id="d82a8-289">grant_type</span></span> | <span data-ttu-id="d82a8-290">client_credentials</span><span class="sxs-lookup"><span data-stu-id="d82a8-290">client_credentials</span></span> |
        | <span data-ttu-id="d82a8-291">resource</span><span class="sxs-lookup"><span data-stu-id="d82a8-291">resource</span></span> | <span data-ttu-id="d82a8-292">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="d82a8-292">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="d82a8-293">Du skal motta et `aadToken` som svar, som ligner på følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="d82a8-293">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="d82a8-294">Formuler en JSON-forespørsel som ligner på følgende:</span><span class="sxs-lookup"><span data-stu-id="d82a8-294">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="d82a8-295">Der:</span><span class="sxs-lookup"><span data-stu-id="d82a8-295">Where:</span></span>
    - <span data-ttu-id="d82a8-296">Verdien for `client_assertion` må være `aadToken` du mottok i forrige trinn.</span><span class="sxs-lookup"><span data-stu-id="d82a8-296">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="d82a8-297">Verdien for `context` må være miljø-ID-en der du vil implementere tillegget.</span><span class="sxs-lookup"><span data-stu-id="d82a8-297">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="d82a8-298">Angi alle andre verdier som vist i eksemplet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-298">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="d82a8-299">Send en HTTP-forespørsel med følgende egenskaper:</span><span class="sxs-lookup"><span data-stu-id="d82a8-299">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="d82a8-300">**URL-adresse** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="d82a8-300">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="d82a8-301">**Metode** - `POST`</span><span class="sxs-lookup"><span data-stu-id="d82a8-301">**Method** - `POST`</span></span>
    - <span data-ttu-id="d82a8-302">**HTTP-hode** - Ta med API-versjonen (nøkkelen er `Api-Version` og verdien er `1.0`)</span><span class="sxs-lookup"><span data-stu-id="d82a8-302">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="d82a8-303">**Meldingstekst** - Ta med JSON-forespørselen du opprettet i forrige trinn.</span><span class="sxs-lookup"><span data-stu-id="d82a8-303">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="d82a8-304">Du får et `access_token` som svar.</span><span class="sxs-lookup"><span data-stu-id="d82a8-304">You will get an `access_token` in response.</span></span> <span data-ttu-id="d82a8-305">Dette er det du trenger som bærertoken for å kalle opp lagersynlighets-API-en.</span><span class="sxs-lookup"><span data-stu-id="d82a8-305">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="d82a8-306">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="d82a8-306">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a><span data-ttu-id="d82a8-307">Eksempelforespørsel</span><span class="sxs-lookup"><span data-stu-id="d82a8-307">Sample Request</span></span>

<span data-ttu-id="d82a8-308">For din referanse har du her et eksempel på en http-forespørsel. Du kan bruke alle verktøy eller kodingsspråk til å sende denne forespørselen, for eksempel ``Postman``.</span><span class="sxs-lookup"><span data-stu-id="d82a8-308">For your reference, here is a sample http request, you can use any tools or coding language to send this request, such as  ``Postman``.</span></span>

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

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="d82a8-309">Konfigurer API-en for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="d82a8-309">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="d82a8-310">Før du bruker tjenesten, må du fullføre konfigurasjonene som er beskrevet i følgende underavsnitt.</span><span class="sxs-lookup"><span data-stu-id="d82a8-310">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="d82a8-311">Konfigurasjonen kan variere avhengig av detaljene i miljøet ditt.</span><span class="sxs-lookup"><span data-stu-id="d82a8-311">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="d82a8-312">Den inneholder hovedsakelig fire deler:</span><span class="sxs-lookup"><span data-stu-id="d82a8-312">It primarily includes four parts:</span></span>

- [<span data-ttu-id="d82a8-313">Partisjonering</span><span class="sxs-lookup"><span data-stu-id="d82a8-313">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="d82a8-314">Dimensjonskonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="d82a8-314">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="d82a8-315">Indeksering</span><span class="sxs-lookup"><span data-stu-id="d82a8-315">Indexing</span></span>](#indexing)
- [<span data-ttu-id="d82a8-316">Egendefinert mål</span><span class="sxs-lookup"><span data-stu-id="d82a8-316">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="d82a8-317">Partisjonering</span><span class="sxs-lookup"><span data-stu-id="d82a8-317">Partitioning</span></span>

<span data-ttu-id="d82a8-318">Partisjonering kan påvirke ytelsen betydelig for API-en for lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-318">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="d82a8-319">Det er en god idé å definere et oppsett som tillater små grupperinger av data, samtidig som du tillater meningsfulle dataspørringer samtidig.</span><span class="sxs-lookup"><span data-stu-id="d82a8-319">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="d82a8-320">`organizationId` (`dataAreaId` i Supply Chain Management) vil alltid være en del av partisjonen, og standard lagersynlighet er satt til partisjonering per dimensjon som *Område + sted*.</span><span class="sxs-lookup"><span data-stu-id="d82a8-320">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="d82a8-321">Dette betyr at tjenesten alltid må spørres med disse dimensjonene som er definert i filtrene.</span><span class="sxs-lookup"><span data-stu-id="d82a8-321">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="d82a8-322">*Område* og *Sted* er to generelle standarddimensjoner i lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-322">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="d82a8-323">I Supply Chain Management kalles disse dimensjonene *Område* (`InventSiteId`) og *Lager* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="d82a8-323">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="d82a8-324">Dimensjonskonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="d82a8-324">Dimension configurations</span></span>

<span data-ttu-id="d82a8-325">Lagersynlighet inneholder en liste over generelle standarddimensjoner for å aktivere systemintegrasjon med flere kilder.</span><span class="sxs-lookup"><span data-stu-id="d82a8-325">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="d82a8-326">Tabellen nedenfor viser hvilke lagerdimensjoner som skal være standard dimensjonsnavn i lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-326">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="d82a8-327">Dimensjonstype</span><span class="sxs-lookup"><span data-stu-id="d82a8-327">Dimension type</span></span> | <span data-ttu-id="d82a8-328">Dimensjonsnavn</span><span class="sxs-lookup"><span data-stu-id="d82a8-328">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="d82a8-329">Produkt</span><span class="sxs-lookup"><span data-stu-id="d82a8-329">Product</span></span> | `ColorId` |
| <span data-ttu-id="d82a8-330">Produkt</span><span class="sxs-lookup"><span data-stu-id="d82a8-330">Product</span></span> | `SizeId` |
| <span data-ttu-id="d82a8-331">Produkt</span><span class="sxs-lookup"><span data-stu-id="d82a8-331">Product</span></span> | `StyleId` |
| <span data-ttu-id="d82a8-332">Produkt</span><span class="sxs-lookup"><span data-stu-id="d82a8-332">Product</span></span> | `ConfigId` |
| <span data-ttu-id="d82a8-333">Sporing</span><span class="sxs-lookup"><span data-stu-id="d82a8-333">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="d82a8-334">Sporing</span><span class="sxs-lookup"><span data-stu-id="d82a8-334">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="d82a8-335">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="d82a8-335">Location</span></span> | `LocationId` |
| <span data-ttu-id="d82a8-336">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="d82a8-336">Location</span></span> | `SiteId` |
| <span data-ttu-id="d82a8-337">Lagerstatus</span><span class="sxs-lookup"><span data-stu-id="d82a8-337">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="d82a8-338">Lagerspesifikk</span><span class="sxs-lookup"><span data-stu-id="d82a8-338">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="d82a8-339">Lagerspesifikk</span><span class="sxs-lookup"><span data-stu-id="d82a8-339">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="d82a8-340">Lagerspesifikk</span><span class="sxs-lookup"><span data-stu-id="d82a8-340">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="d82a8-341">Dimensjonstypen som er oppført i den forrige tabellen, er bare for referanse.</span><span class="sxs-lookup"><span data-stu-id="d82a8-341">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="d82a8-342">Du trenger ikke definere dimensjonstypen i Lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-342">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="d82a8-343">Hvis det finnes en egendefinert dimensjon som må flyte til en standardverdi når det brukes av lagersynlighet, kan du konfigurere navnet **Egendefinert dimensjon** i Lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-343">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="d82a8-344">Eksterne systemer har tilgang til lagersynlighet via RESTful-API-er som gir deg beholdningsinformasjon om gitte dimensjoner som det skal spørres om.</span><span class="sxs-lookup"><span data-stu-id="d82a8-344">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="d82a8-345">Ved integreringen kan du bruke Lagersynlighet til å konfigurere den *eksterne kanaldatakilden* og kildedimensjonen til *måldimensjonene* i Lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-345">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="d82a8-346">Måldimensjonene må være ett av følgende:</span><span class="sxs-lookup"><span data-stu-id="d82a8-346">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="d82a8-347">Standarddimensjoner i Lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="d82a8-347">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="d82a8-348">Egendefinerte dimensjoner</span><span class="sxs-lookup"><span data-stu-id="d82a8-348">Custom dimensions</span></span>

<span data-ttu-id="d82a8-349">Formålet med dimensjonskonfigurasjon er å standardisere integreringen med flere systemer for spørringen på dimensjoner og posteringshendelsen med dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="d82a8-349">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="d82a8-350">Indeksering</span><span class="sxs-lookup"><span data-stu-id="d82a8-350">Indexing</span></span>

<span data-ttu-id="d82a8-351">Vanligvis vil ikke lagerbeholdningsspørringen bare være på det høyeste totale nivået, men du vil kanskje se resultater som er aggregert basert på lagerdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="d82a8-351">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="d82a8-352">Lagersynlighet gir fleksibilitet ved å la deg definere indeksene som er basert på dimensjonen eller kombinasjonen av dimensjonene.</span><span class="sxs-lookup"><span data-stu-id="d82a8-352">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="d82a8-353">For øyeblikket kan du bare konfigurere indekser til maksimalt fem.</span><span class="sxs-lookup"><span data-stu-id="d82a8-353">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="d82a8-354">Du må nøye vurdere hvilken dimensjon eller dimensjonskombinasjon du vil bruke før implementeringen for å sikre at den oppfyller dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="d82a8-354">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="d82a8-355">Hvis du for eksempel vil spørre etter produkter som følger:</span><span class="sxs-lookup"><span data-stu-id="d82a8-355">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="d82a8-356">Forespør den aggregerte produktbeholdningen etter dimensjonene *Farge* og *Størrelse*.</span><span class="sxs-lookup"><span data-stu-id="d82a8-356">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="d82a8-357">I noen tilfeller vil du bare spørre om produktet totalt.</span><span class="sxs-lookup"><span data-stu-id="d82a8-357">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="d82a8-358">Du har to indekser definert som følgende:</span><span class="sxs-lookup"><span data-stu-id="d82a8-358">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="d82a8-359">Den tomme parentesen samles, basert på produkt-ID-en i partisjonen.</span><span class="sxs-lookup"><span data-stu-id="d82a8-359">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="d82a8-360">Indekseringen definerer hvordan du kan gruppere resultatene basert på `groupBy`-spørringsinnstillingen.</span><span class="sxs-lookup"><span data-stu-id="d82a8-360">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="d82a8-361">I dette tilfellet hvis du ikke definerer noen `groupBy`-verdier, får du totaler etter `productid`.</span><span class="sxs-lookup"><span data-stu-id="d82a8-361">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="d82a8-362">Hvis du definerer `groupBy` som `groupBy=ColorId&groupBy=SizeId`, vil du ellers få flere linjer returnert, basert på de ulike kombinasjonene mellom farger og størrelser i systemet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-362">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="d82a8-363">Du kan legge spørringskriteriene i brødteksten for forespørselen.</span><span class="sxs-lookup"><span data-stu-id="d82a8-363">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="d82a8-364">Her er en eksempelspørring på produktet med farge- og størrelseskombinasjon.</span><span class="sxs-lookup"><span data-stu-id="d82a8-364">Here is a sample query on the product with color and size combination.</span></span>

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

<span data-ttu-id="d82a8-365">For `filters`-feltet støtter for øyeblikket bare `ProductId` flere verdier.</span><span class="sxs-lookup"><span data-stu-id="d82a8-365">For the `filters` field, currently only `ProductId` supports multiple values.</span></span> <span data-ttu-id="d82a8-366">Hvis `ProductId` er en tom matrise, vil alle produkter bli spurt etter.</span><span class="sxs-lookup"><span data-stu-id="d82a8-366">If the `ProductId` is an empty array, all products will be queried.</span></span>

#### <a name="custom-measurement"></a><span data-ttu-id="d82a8-367">Egendefinert mål</span><span class="sxs-lookup"><span data-stu-id="d82a8-367">Custom measurement</span></span>

<span data-ttu-id="d82a8-368">Standard målantall er koblet til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d82a8-368">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="d82a8-369">Det kan imidlertid være at du vil ha et antall som består av en kombinasjon av standardmålene.</span><span class="sxs-lookup"><span data-stu-id="d82a8-369">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="d82a8-370">Hvis du vil gjøre dette, kan du ha en konfigurasjon av egendefinert antall, som vil bli lagt til i utdataene i lagerbeholdningsspørringene.</span><span class="sxs-lookup"><span data-stu-id="d82a8-370">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="d82a8-371">Ved hjelp av funksjonaliteten kan du bare definere et sett med mål som skal legges til, eller et sett med mål som skal trekkes fra, for å kunne lage det egendefinerte målet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-371">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="d82a8-372">Med følgende spørringsvilkår vil du for eksempel konfigurere det egendefinerte målantallet som `MyCustomAvailableforReservation` som skal brukes av forbrukssystemet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-372">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="d82a8-373">Forbrukssystem</span><span class="sxs-lookup"><span data-stu-id="d82a8-373">Consumption system</span></span> | <span data-ttu-id="d82a8-374">Beregnede mål</span><span class="sxs-lookup"><span data-stu-id="d82a8-374">Calculated measurers</span></span> | <span data-ttu-id="d82a8-375">Datakilde</span><span class="sxs-lookup"><span data-stu-id="d82a8-375">Data source</span></span> | <span data-ttu-id="d82a8-376">Modifikator</span><span class="sxs-lookup"><span data-stu-id="d82a8-376">Modifier</span></span> | <span data-ttu-id="d82a8-377">Beregningstype for modifikator</span><span class="sxs-lookup"><span data-stu-id="d82a8-377">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="d82a8-378">Tillegg</span><span class="sxs-lookup"><span data-stu-id="d82a8-378">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="d82a8-379">Tillegg</span><span class="sxs-lookup"><span data-stu-id="d82a8-379">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="d82a8-380">Subtraksjon</span><span class="sxs-lookup"><span data-stu-id="d82a8-380">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="d82a8-381">Tillegg</span><span class="sxs-lookup"><span data-stu-id="d82a8-381">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="d82a8-382">Subtraksjon</span><span class="sxs-lookup"><span data-stu-id="d82a8-382">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="d82a8-383">Tillegg</span><span class="sxs-lookup"><span data-stu-id="d82a8-383">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="d82a8-384">Tillegg</span><span class="sxs-lookup"><span data-stu-id="d82a8-384">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="d82a8-385">Subtraksjon</span><span class="sxs-lookup"><span data-stu-id="d82a8-385">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="d82a8-386">Subtraksjon</span><span class="sxs-lookup"><span data-stu-id="d82a8-386">Subtraction</span></span> |

<span data-ttu-id="d82a8-387">Med dette vil spørringen på det egendefinerte målantallet returnere følgende utdata.</span><span class="sxs-lookup"><span data-stu-id="d82a8-387">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="d82a8-388">`MyCustomAvailableforReservation`-utdataene er basert på beregningsinnstillingen i de egendefinerte målene som:</span><span class="sxs-lookup"><span data-stu-id="d82a8-388">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="d82a8-389">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="d82a8-389">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="d82a8-390">Postere lagerendringer</span><span class="sxs-lookup"><span data-stu-id="d82a8-390">Posting on-hand changes</span></span>

<span data-ttu-id="d82a8-391">Den nøyaktige URL-adressen som hendelsen vil bli postert til, avhenger av det geografiske området.</span><span class="sxs-lookup"><span data-stu-id="d82a8-391">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="d82a8-392">Den tar følgende form:</span><span class="sxs-lookup"><span data-stu-id="d82a8-392">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="d82a8-393">Når den er godkjent, kan denne URL-adressen brukes sammen med HTTP `POST`-metoden til å sende lagerbeholdningshendelser til tjenesten.</span><span class="sxs-lookup"><span data-stu-id="d82a8-393">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="d82a8-394">En spesiell topptekst brukes til å kommunisere med Dynamics 365-tjenester via HTTP-forespørsler, og angir miljø-ID-en til Supply Chain Management-forkomten dataene er koblet til.</span><span class="sxs-lookup"><span data-stu-id="d82a8-394">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="d82a8-395">For eksempel:</span><span class="sxs-lookup"><span data-stu-id="d82a8-395">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="d82a8-396">Postere spørringer om lagerendringer eksempel 1</span><span class="sxs-lookup"><span data-stu-id="d82a8-396">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="d82a8-397">I dette eksemplet vises det et scenario der du kan definere dimensjonskonfigurasjonen i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="d82a8-397">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="d82a8-398">Bruk følgende spørring til å konfigurere dimensjonstilordningen i Power Apps:</span><span class="sxs-lookup"><span data-stu-id="d82a8-398">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="d82a8-399">Nå kan du angi `dimensionDataSource` og bruke egendefinerte dimensjoner i spørringene.</span><span class="sxs-lookup"><span data-stu-id="d82a8-399">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="d82a8-400">Systemet konverterer automatisk egendefinerte dimensjoner til basisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="d82a8-400">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="d82a8-401">Postere spørringer om lagerendringer eksempel 2</span><span class="sxs-lookup"><span data-stu-id="d82a8-401">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="d82a8-402">Dette eksemplet viser et scenario der ingen tilordninger er definert for dimensjonskonfigurasjonen i Power Apps, slik at posteringen også bør bruke basisdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="d82a8-402">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="d82a8-403">Alle dimensjoner må være basisdimensjoner når `dimensionDataSource`-feltet er null, tomt eller mellomrom.</span><span class="sxs-lookup"><span data-stu-id="d82a8-403">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="d82a8-404">Feltegenskaper for JSON-dokument</span><span class="sxs-lookup"><span data-stu-id="d82a8-404">JSON document field properties</span></span>

<span data-ttu-id="d82a8-405">Feltene fra JSON-spørringseksemplene som ble angitt tidligere, har egenskapene som er oppført i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="d82a8-405">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="d82a8-406">Felt-ID</span><span class="sxs-lookup"><span data-stu-id="d82a8-406">Field ID</span></span> | <span data-ttu-id="d82a8-407">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d82a8-407">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="d82a8-408">En unik ID for den bestemte endringshendelsen.</span><span class="sxs-lookup"><span data-stu-id="d82a8-408">A unique ID for the specific change event.</span></span> <span data-ttu-id="d82a8-409">Denne ID-en brukes til å sikre at hvis kommunikasjon med tjenesten mislykkes under posteringen, vil sendingen av hendelsen ikke resultere i at samme hendelse telles to ganger i systemet.</span><span class="sxs-lookup"><span data-stu-id="d82a8-409">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="d82a8-410">Identifikatoren til organisasjonen som er koblet til hendelsen.</span><span class="sxs-lookup"><span data-stu-id="d82a8-410">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="d82a8-411">Dette tilordner til ID-er til Supply Chain Management-organisasjoner eller dataområder.</span><span class="sxs-lookup"><span data-stu-id="d82a8-411">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="d82a8-412">Identifikatoren til produktet det gjelder.</span><span class="sxs-lookup"><span data-stu-id="d82a8-412">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="d82a8-413">Antallet som lagerbeholdningen må endres med.</span><span class="sxs-lookup"><span data-stu-id="d82a8-413">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="d82a8-414">Hvis for eksempel ti nye bagels er lagt til i en hylle, vil denne verdien være 10.</span><span class="sxs-lookup"><span data-stu-id="d82a8-414">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="d82a8-415">Hvis tre bagels deretter ble fjernet fra hyllen eller solgt, ville denne verdien være –3.</span><span class="sxs-lookup"><span data-stu-id="d82a8-415">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="d82a8-416">Datakilden for dimensjonene som brukes i posteringsendringshendelsen og -spørringen.</span><span class="sxs-lookup"><span data-stu-id="d82a8-416">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="d82a8-417">Hvis du angir datakilden, kan du bruke de egendefinerte dimensjonene fra den angitte datakilden.</span><span class="sxs-lookup"><span data-stu-id="d82a8-417">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="d82a8-418">Med dimensjonskonfigurasjonen kan Lagersynlighet tilordne de egendefinerte dimensjonene til de generelle standarddimensjonene.</span><span class="sxs-lookup"><span data-stu-id="d82a8-418">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="d82a8-419">Hvis `dimensionDataSource` ikke er angitt, kan du bare bruke de generelle standarddimensjonene i spørringene.</span><span class="sxs-lookup"><span data-stu-id="d82a8-419">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="d82a8-420">En dynamisk samling med nøkkel/verdi-par.</span><span class="sxs-lookup"><span data-stu-id="d82a8-420">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="d82a8-421">Disse vil tilordnes noen av dimensjonene i Supply Chain Management, men du kan også legge til egendefinerte dimensjoner (som *Kilde*) som kan angi om hendelsen kommer fra Supply Chain Management eller et eksternt system.</span><span class="sxs-lookup"><span data-stu-id="d82a8-421">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="d82a8-422">Spørring om aktuell lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="d82a8-422">Querying current on-hand</span></span>

<span data-ttu-id="d82a8-423">Endepunktet for spørringer av gjeldende lagerbeholdning vil ha en lignende URL-adresse:</span><span class="sxs-lookup"><span data-stu-id="d82a8-423">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="d82a8-424">Det blir spurt med HTTP `POST`-metoden.</span><span class="sxs-lookup"><span data-stu-id="d82a8-424">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="d82a8-425">Gjeldende beholdningsspørring, eksempel 1</span><span class="sxs-lookup"><span data-stu-id="d82a8-425">Current on-hand query example 1</span></span>

<span data-ttu-id="d82a8-426">I dette eksemplet vises det et scenario der du allerede har fullført dimensjonskonfigurasjonen i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="d82a8-426">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="d82a8-427">Bruk følgende spørring til å konfigurere dimensjonstilordningen i Power Apps:</span><span class="sxs-lookup"><span data-stu-id="d82a8-427">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="d82a8-428">Nå kan du angi `dimensionDataSource` og bruke egendefinerte dimensjoner i spørringene.</span><span class="sxs-lookup"><span data-stu-id="d82a8-428">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="d82a8-429">Systemet konverterer automatisk egendefinerte dimensjoner til basisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="d82a8-429">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="d82a8-430">Du kan angi `DimensionDataSource` i `filters` og angi egendefinerte dimensjoner i både `filters` og `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="d82a8-430">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="d82a8-431">Systemet konverterer automatisk egendefinerte dimensjoner til basisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="d82a8-431">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="d82a8-432">Gjeldende beholdningsspørring, eksempel 2</span><span class="sxs-lookup"><span data-stu-id="d82a8-432">Current on-hand query example 2</span></span>

<span data-ttu-id="d82a8-433">Dette eksemplet viser et scenario der ingen tilordninger er definert for dimensjonskonfigurasjonen i Power Apps, slik at posteringen også bør bruke basisdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="d82a8-433">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="d82a8-434">Alle dimensjoner må være basisdimensjoner når `dimensionDataSource`-feltet, under `filters`, er null, tomt eller mellomrom.</span><span class="sxs-lookup"><span data-stu-id="d82a8-434">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="d82a8-435">Eksempel på returresultat</span><span class="sxs-lookup"><span data-stu-id="d82a8-435">Example return result</span></span>

<span data-ttu-id="d82a8-436">Spørringene som vises i eksemplene ovenfor, kan returnere et resultat som dette.</span><span class="sxs-lookup"><span data-stu-id="d82a8-436">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="d82a8-437">Legg merke til at antall-feltene er strukturert som en ordliste for mål og tilknyttede verdier.</span><span class="sxs-lookup"><span data-stu-id="d82a8-437">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
