---
title: Generell feilsøking
description: Dette emnet inneholder generell feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f7ee0b5aa4e72614205e129acd986376b33efc70
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172697"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="94fe1-103">Generell feilsøking</span><span class="sxs-lookup"><span data-stu-id="94fe1-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="94fe1-104">Dette emnet inneholder generell feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="94fe1-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94fe1-105">Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator.</span><span class="sxs-lookup"><span data-stu-id="94fe1-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="94fe1-106">Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="94fe1-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="94fe1-107">Når du prøver å installere dobbel skriving-pakken ved hjelp av Package Deployer-verktøyet, vises ingen tilgjengelige løsninger</span><span class="sxs-lookup"><span data-stu-id="94fe1-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="94fe1-108">Noen versjoner av Package Deployer-verktøyet er ikke kompatible med løsningspakken for dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="94fe1-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="94fe1-109">Hvis du vil installere pakken, må du bruke [versjon 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) eller senere av Package Deployer-verktøyet.</span><span class="sxs-lookup"><span data-stu-id="94fe1-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="94fe1-110">Når du har installert Package Deployer-verktøyet, installerer du løsningspakken ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="94fe1-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="94fe1-111">Last ned den nyeste løsningspakkefilen fra Yammer.com.</span><span class="sxs-lookup"><span data-stu-id="94fe1-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="94fe1-112">Når zip-filen for pakken er lastet ned, høyreklikker du den og velger **Egenskaper**.</span><span class="sxs-lookup"><span data-stu-id="94fe1-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="94fe1-113">Merk av for **Fjern blokkering**, og velg deretter **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="94fe1-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="94fe1-114">Hvis du ikke ser avmerkingsboksen **Fjern blokkering,** er blokkeringen av zip-filen allerede fjernet, og du kan hoppe over dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="94fe1-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Dialogboksen Egenskaper](media/unblock_option.png)

2. <span data-ttu-id="94fe1-116">Pakk ut zip-filen for pakken, og kopier alle filene i mappen **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**.</span><span class="sxs-lookup"><span data-stu-id="94fe1-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Innholdet i mappen Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. <span data-ttu-id="94fe1-118">Lim inn alle de kopierte filene i **Verktøy**-mappen i Package Deployer-verktøyet.</span><span class="sxs-lookup"><span data-stu-id="94fe1-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="94fe1-119">Kjør **PackageDeployer.exe** for å velge Common Data Service-miljøet og installere løsningene.</span><span class="sxs-lookup"><span data-stu-id="94fe1-119">Run **PackageDeployer.exe** to select the Common Data Service environment and install the solutions.</span></span>

    ![Innhold i Verktøy-mappen](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a><span data-ttu-id="94fe1-121">Aktivere og vise plugin-sporingsloggen Common Data Service for å vise feildetaljer</span><span class="sxs-lookup"><span data-stu-id="94fe1-121">Enable and view the plug-in trace log in Common Data Service to view error details</span></span>

<span data-ttu-id="94fe1-122">**Nødvendig rolle for å aktivere sporingsloggen og vise feil**: Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="94fe1-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="94fe1-123">Følg denne fremgangsmåten for å aktivere sporingsloggen.</span><span class="sxs-lookup"><span data-stu-id="94fe1-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="94fe1-124">Logg inn på Finance and Operations-appen, åpne **Innstillinger**-siden, og velg deretter **Administrasjon** under **System**.</span><span class="sxs-lookup"><span data-stu-id="94fe1-124">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="94fe1-125">Velg **Systeminnstillinger** på siden **Administrasjon**.</span><span class="sxs-lookup"><span data-stu-id="94fe1-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="94fe1-126">I kategorien **Tilpassing**, i feltet **Sporing av plugin-modul og egendefinert arbeidsflytaktivitet**, velger du **Alle** for å aktivere plugin-sporingsloggen.</span><span class="sxs-lookup"><span data-stu-id="94fe1-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="94fe1-127">Hvis du bare vil logge sporingslogger når det oppstår unntak, kan du velge **Unntak** i stedet.</span><span class="sxs-lookup"><span data-stu-id="94fe1-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="94fe1-128">Følg denne fremgangsmåten for å se sporingsloggen.</span><span class="sxs-lookup"><span data-stu-id="94fe1-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="94fe1-129">Logg inn på Finance and Operations-appen, åpne **Innstillinger**-siden, og velg deretter **Sporingslogg for plugin-modul** under **Tilpassing**.</span><span class="sxs-lookup"><span data-stu-id="94fe1-129">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="94fe1-130">Finn sporingsloggene der **Typenavn**-feltet er satt til **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span><span class="sxs-lookup"><span data-stu-id="94fe1-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span></span>
3. <span data-ttu-id="94fe1-131">Dobbeltklikk et element for å vise hele loggen, og se deretter gjennom **Meldingsblokk**-teksten i hurtigfanen **Utførelse**.</span><span class="sxs-lookup"><span data-stu-id="94fe1-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="94fe1-132">Aktivere feilsøkingsmodus for å feilsøke problemer med direkte synkronisering i Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="94fe1-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="94fe1-133">**Nødvendig rolle for å vise feilene:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="94fe1-133">**Required role to view the errors:** System admin</span></span>

<span data-ttu-id="94fe1-134">Dobbel skriving-feil som kommer fra Common Data Service, kan vises i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="94fe1-134">Dual-write errors that originate in Common Data Service can appear in the Finance and Operations app.</span></span> <span data-ttu-id="94fe1-135">I noen tilfeller er ikke hele teksten i feilmeldingen tilgjengelig fordi meldingen er for lang eller inneholder personlig identifiserende informasjon (PII).</span><span class="sxs-lookup"><span data-stu-id="94fe1-135">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="94fe1-136">Du kan aktivere detaljert logging for feil ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="94fe1-136">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="94fe1-137">Alle prosjektkonfigurasjoner i Finance and Operations-apper har en **IsDebugMode**-egenskap i **DualWriteProjectConfiguration**-enheten.</span><span class="sxs-lookup"><span data-stu-id="94fe1-137">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="94fe1-138">Åpne **DualWriteProjectConfiguration**-enheten ved hjelp av Excel-tillegget.</span><span class="sxs-lookup"><span data-stu-id="94fe1-138">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="94fe1-139">En enkel måte å åpne enheten på er å aktivere **Utforming**-modus i Excel-tillegget og deretter legge til **DualWriteProjectConfigurationEntity** i regnearket.</span><span class="sxs-lookup"><span data-stu-id="94fe1-139">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="94fe1-140">Hvis du vil ha mer informasjon, kan du se [Åpne enhetsdata i Excel og oppdatere dataene ved hjelp av Excel-tillegget](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="94fe1-140">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="94fe1-141">Sett egenskapen **IsDebugMode** til **Ja** for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="94fe1-141">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="94fe1-142">Kjør scenariet som genererer feil.</span><span class="sxs-lookup"><span data-stu-id="94fe1-142">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="94fe1-143">De detaljerte loggene er tilgjengelige i tabellen DualWriteErrorLog.</span><span class="sxs-lookup"><span data-stu-id="94fe1-143">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="94fe1-144">Hvis du vil slå opp data i tabelleseren, bruker du følgende URL-adresse (erstatt **XXX** etter behov):</span><span class="sxs-lookup"><span data-stu-id="94fe1-144">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="94fe1-145">Kontrollere synkroniseringsfeil på den virtuelle maskinen for Finance and Operations-appen</span><span class="sxs-lookup"><span data-stu-id="94fe1-145">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="94fe1-146">**Nødvendig rolle for å vise feilene:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="94fe1-146">**Required role to view the errors:** System admin</span></span>

1. <span data-ttu-id="94fe1-147">Logg på Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="94fe1-147">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="94fe1-148">Åpne LCS-prosjektet du har valgt til å utføre testing av dobbel skriving for.</span><span class="sxs-lookup"><span data-stu-id="94fe1-148">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="94fe1-149">Velg flisen **Skybaserte miljøer**.</span><span class="sxs-lookup"><span data-stu-id="94fe1-149">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="94fe1-150">Bruk Eksternt skrivebord for å logge på den virtuelle maskinen for Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="94fe1-150">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="94fe1-151">Bruk den lokale kontoen som vises i LCS.</span><span class="sxs-lookup"><span data-stu-id="94fe1-151">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="94fe1-152">Åpne hendelseslisten.</span><span class="sxs-lookup"><span data-stu-id="94fe1-152">Open Event viewer.</span></span>
6. <span data-ttu-id="94fe1-153">Velg **Program- og tjenestelogger \> Microsoft \> Dynamics \> AX-DualWriteSync \> Drift**.</span><span class="sxs-lookup"><span data-stu-id="94fe1-153">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="94fe1-154">Se gjennom listen over nylige feil.</span><span class="sxs-lookup"><span data-stu-id="94fe1-154">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="94fe1-155">Koble fra og koble til et annet Common Data Service-miljø fra en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="94fe1-155">Unlink and link another Common Data Service environment from a Finance and Operations app</span></span>

<span data-ttu-id="94fe1-156">**Nødvendig legitimasjon for å koble fra miljøet:** Azure AD-leieradministrator</span><span class="sxs-lookup"><span data-stu-id="94fe1-156">**Required credentials to unlink the environment:** Azure AD tenant admin</span></span>

1. <span data-ttu-id="94fe1-157">Logg på Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="94fe1-157">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="94fe1-158">Gå til **Arbeidsområder \> Databehandling**, og velg flisen **Dobbel skriving**.</span><span class="sxs-lookup"><span data-stu-id="94fe1-158">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="94fe1-159">Velg alle kjørende tilordninger, og klikk på **Stopp**.</span><span class="sxs-lookup"><span data-stu-id="94fe1-159">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="94fe1-160">Klikk **Koble fra miljø**.</span><span class="sxs-lookup"><span data-stu-id="94fe1-160">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="94fe1-161">Velg **Ja** for å bekrefte operasjonen.</span><span class="sxs-lookup"><span data-stu-id="94fe1-161">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="94fe1-162">Du kan nå koble til et nytt miljø.</span><span class="sxs-lookup"><span data-stu-id="94fe1-162">You can now link a new environment.</span></span>
