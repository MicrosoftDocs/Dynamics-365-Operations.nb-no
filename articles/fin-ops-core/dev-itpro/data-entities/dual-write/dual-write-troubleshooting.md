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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: c3352afd93dfc7c37a8af9dabaf85b7a1debad30
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997260"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="287ad-103">Generell feilsøking</span><span class="sxs-lookup"><span data-stu-id="287ad-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="287ad-104">Dette emnet inneholder generell feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="287ad-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="287ad-105">Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator.</span><span class="sxs-lookup"><span data-stu-id="287ad-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="287ad-106">Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="287ad-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="287ad-107">Når du prøver å installere dobbel skriving-pakken ved hjelp av Package Deployer-verktøyet, vises ingen tilgjengelige løsninger</span><span class="sxs-lookup"><span data-stu-id="287ad-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="287ad-108">Noen versjoner av Package Deployer-verktøyet er ikke kompatible med løsningspakken for dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="287ad-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="287ad-109">Hvis du vil installere pakken, må du bruke [versjon 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) eller senere av Package Deployer-verktøyet.</span><span class="sxs-lookup"><span data-stu-id="287ad-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="287ad-110">Når du har installert Package Deployer-verktøyet, installerer du løsningspakken ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="287ad-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="287ad-111">Last ned den nyeste løsningspakkefilen fra Yammer.com.</span><span class="sxs-lookup"><span data-stu-id="287ad-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="287ad-112">Når zip-filen for pakken er lastet ned, høyreklikker du den og velger **Egenskaper**.</span><span class="sxs-lookup"><span data-stu-id="287ad-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="287ad-113">Merk av for **Fjern blokkering** , og velg deretter **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="287ad-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="287ad-114">Hvis du ikke ser avmerkingsboksen **Fjern blokkering,** er blokkeringen av zip-filen allerede fjernet, og du kan hoppe over dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="287ad-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Dialogboksen Egenskaper](media/unblock_option.png)

2. <span data-ttu-id="287ad-116">Pakk ut zip-filen for pakken, og kopier alle filene i mappen **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**.</span><span class="sxs-lookup"><span data-stu-id="287ad-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Innholdet i mappen Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. <span data-ttu-id="287ad-118">Lim inn alle de kopierte filene i **Verktøy** -mappen i Package Deployer-verktøyet.</span><span class="sxs-lookup"><span data-stu-id="287ad-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="287ad-119">Kjør **PackageDeployer.exe** for å velge Common Data Service-miljøet og installere løsningene.</span><span class="sxs-lookup"><span data-stu-id="287ad-119">Run **PackageDeployer.exe** to select the Common Data Service environment and install the solutions.</span></span>

    ![Innhold i Verktøy-mappen](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a><span data-ttu-id="287ad-121">Aktivere og vise plugin-sporingsloggen Common Data Service for å vise feildetaljer</span><span class="sxs-lookup"><span data-stu-id="287ad-121">Enable and view the plug-in trace log in Common Data Service to view error details</span></span>

<span data-ttu-id="287ad-122">**Nødvendig rolle for å aktivere sporingsloggen og vise feil** : Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="287ad-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="287ad-123">Følg denne fremgangsmåten for å aktivere sporingsloggen.</span><span class="sxs-lookup"><span data-stu-id="287ad-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="287ad-124">Logg inn på den modelldrevne appe i Dynamics 365, åpne **Innstillinger** -siden, og velg deretter **Administrasjon** under **System**.</span><span class="sxs-lookup"><span data-stu-id="287ad-124">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **System** , select **Administration**.</span></span>
2. <span data-ttu-id="287ad-125">Velg **Systeminnstillinger** på siden **Administrasjon**.</span><span class="sxs-lookup"><span data-stu-id="287ad-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="287ad-126">I kategorien **Tilpassing** , i feltet **Sporing av plugin-modul og egendefinert arbeidsflytaktivitet** , velger du **Alle** for å aktivere plugin-sporingsloggen.</span><span class="sxs-lookup"><span data-stu-id="287ad-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="287ad-127">Hvis du bare vil logge sporingslogger når det oppstår unntak, kan du velge **Unntak** i stedet.</span><span class="sxs-lookup"><span data-stu-id="287ad-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="287ad-128">Følg denne fremgangsmåten for å se sporingsloggen.</span><span class="sxs-lookup"><span data-stu-id="287ad-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="287ad-129">Logg inn på den modelldrevne appe i Dynamics 365, åpne **Innstillinger** -siden, og velg deretter **Sporingslogg for plugin-modul** under **Tilpassing**.</span><span class="sxs-lookup"><span data-stu-id="287ad-129">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **Customization** , select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="287ad-130">Finn sporingsloggene der **Typenavn** -feltet er satt til **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span><span class="sxs-lookup"><span data-stu-id="287ad-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span></span>
3. <span data-ttu-id="287ad-131">Dobbeltklikk et element for å vise hele loggen, og se deretter gjennom **Meldingsblokk** -teksten i hurtigfanen **Utførelse**.</span><span class="sxs-lookup"><span data-stu-id="287ad-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="287ad-132">Aktivere feilsøkingsmodus for å feilsøke problemer med direkte synkronisering i Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="287ad-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="287ad-133">**Nødvendig rolle for å vise feilene:** Systemadministrator – dobbel skriving-feil som kommer fra Common Data Service, kan vises i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="287ad-133">**Required role to view the errors:** System admin Dual-write errors that originate in Common Data Service can appear in the Finance and Operations app.</span></span> <span data-ttu-id="287ad-134">I noen tilfeller er ikke hele teksten i feilmeldingen tilgjengelig fordi meldingen er for lang eller inneholder personlig identifiserende informasjon (PII).</span><span class="sxs-lookup"><span data-stu-id="287ad-134">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="287ad-135">Du kan aktivere detaljert logging for feil ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="287ad-135">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="287ad-136">Alle prosjektkonfigurasjoner i Finance and Operations-apper har en **IsDebugMode** -egenskap i **DualWriteProjectConfiguration** -enheten.</span><span class="sxs-lookup"><span data-stu-id="287ad-136">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="287ad-137">Åpne **DualWriteProjectConfiguration** -enheten ved hjelp av Excel-tillegget.</span><span class="sxs-lookup"><span data-stu-id="287ad-137">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="287ad-138">En enkel måte å åpne enheten på er å aktivere **Utforming** -modus i Excel-tillegget og deretter legge til **DualWriteProjectConfigurationEntity** i regnearket.</span><span class="sxs-lookup"><span data-stu-id="287ad-138">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="287ad-139">Hvis du vil ha mer informasjon, kan du se [Åpne enhetsdata i Excel og oppdatere dataene ved hjelp av Excel-tillegget](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="287ad-139">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="287ad-140">Sett egenskapen **IsDebugMode** til **Ja** for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="287ad-140">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="287ad-141">Kjør scenariet som genererer feil.</span><span class="sxs-lookup"><span data-stu-id="287ad-141">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="287ad-142">De detaljerte loggene er tilgjengelige i tabellen DualWriteErrorLog.</span><span class="sxs-lookup"><span data-stu-id="287ad-142">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="287ad-143">Hvis du vil slå opp data i tabelleseren, bruker du følgende URL-adresse (erstatt **XXX** etter behov):</span><span class="sxs-lookup"><span data-stu-id="287ad-143">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="287ad-144">Kontrollere synkroniseringsfeil på den virtuelle maskinen for Finance and Operations-appen</span><span class="sxs-lookup"><span data-stu-id="287ad-144">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="287ad-145">**Nødvendig rolle for å vise feilene:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="287ad-145">**Required role to view the errors:** System administrator</span></span>

1. <span data-ttu-id="287ad-146">Logg på Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="287ad-146">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="287ad-147">Åpne LCS-prosjektet du har valgt til å utføre testing av dobbel skriving for.</span><span class="sxs-lookup"><span data-stu-id="287ad-147">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="287ad-148">Velg flisen **Skybaserte miljøer**.</span><span class="sxs-lookup"><span data-stu-id="287ad-148">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="287ad-149">Bruk Eksternt skrivebord for å logge på den virtuelle maskinen for Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="287ad-149">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="287ad-150">Bruk den lokale kontoen som vises i LCS.</span><span class="sxs-lookup"><span data-stu-id="287ad-150">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="287ad-151">Åpne hendelseslisten.</span><span class="sxs-lookup"><span data-stu-id="287ad-151">Open Event viewer.</span></span>
6. <span data-ttu-id="287ad-152">Velg **Program- og tjenestelogger \> Microsoft \> Dynamics \> AX-DualWriteSync \> Drift**.</span><span class="sxs-lookup"><span data-stu-id="287ad-152">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="287ad-153">Se gjennom listen over nylige feil.</span><span class="sxs-lookup"><span data-stu-id="287ad-153">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="287ad-154">Koble fra og koble til et annet Common Data Service-miljø fra en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="287ad-154">Unlink and link another Common Data Service environment from a Finance and Operations app</span></span>

<span data-ttu-id="287ad-155">**Nødvendig rolle for å koble fra miljøet:** Systemansvarlig for enten Finance and Operations-app eller Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="287ad-155">**Required role to unlink the environment:** System administrator for either Finance and Operations app or Common Data Service.</span></span>

1. <span data-ttu-id="287ad-156">Logg på Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="287ad-156">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="287ad-157">Gå til **Arbeidsområder \> Databehandling** , og velg flisen **Dobbel skriving**.</span><span class="sxs-lookup"><span data-stu-id="287ad-157">Go to **Workspaces \> Data management** , and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="287ad-158">Velg alle kjørende tilordninger, og klikk på **Stopp**.</span><span class="sxs-lookup"><span data-stu-id="287ad-158">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="287ad-159">Klikk **Koble fra miljø**.</span><span class="sxs-lookup"><span data-stu-id="287ad-159">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="287ad-160">Velg **Ja** for å bekrefte operasjonen.</span><span class="sxs-lookup"><span data-stu-id="287ad-160">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="287ad-161">Du kan nå koble til et nytt miljø.</span><span class="sxs-lookup"><span data-stu-id="287ad-161">You can now link a new environment.</span></span>

## <a name="unable-to-view-the-sales-order-line-information-form"></a><span data-ttu-id="287ad-162">Kan ikke vise informasjonsskjemaet for salgsordrelinjen</span><span class="sxs-lookup"><span data-stu-id="287ad-162">Unable to view the sales order line Information form</span></span> 

<span data-ttu-id="287ad-163">Når du oppretter en salgsordre i Dynamics 365 Sales, kan du bli omdirigert til ordrelinjeskjemaet for Dynamics 365 Project Operations hvis du klikker på **+ Legg til produkter**.</span><span class="sxs-lookup"><span data-stu-id="287ad-163">When you create a sales order in Dynamics 365 Sales, clicking on **+ Add products** might redirect you to the Dynamics 365 Project Operations order line form.</span></span> <span data-ttu-id="287ad-164">Det finnes ingen måter fra dette skjemaet å vise **Informasjon** -skjemaet for salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="287ad-164">There is no way from that form to view the sales order line **Information** form.</span></span> <span data-ttu-id="287ad-165">Alternativet for **Informasjon** vises ikke i rullegardinlisten under **Ny ordrelinje**.</span><span class="sxs-lookup"><span data-stu-id="287ad-165">The option for **Information** does not appear in the dropdown below **New Order Line**.</span></span> <span data-ttu-id="287ad-166">Dette skjer fordi Project Operations er installert i ditt miljø.</span><span class="sxs-lookup"><span data-stu-id="287ad-166">This happens because Project Operations has been installed in your environment.</span></span>

<span data-ttu-id="287ad-167">Følg denne fremgangsmåten for å reaktivere alternativet for **Informasjon** -skjema:</span><span class="sxs-lookup"><span data-stu-id="287ad-167">To re-enable the **Information** form option, follow these steps:</span></span>
1. <span data-ttu-id="287ad-168">Gå til **Ordrelinje** -enheten.</span><span class="sxs-lookup"><span data-stu-id="287ad-168">Navigate to the **Order Line** entity.</span></span>
2. <span data-ttu-id="287ad-169">Finn **Informasjon** -skjemaet under skjemaer-noden.</span><span class="sxs-lookup"><span data-stu-id="287ad-169">Find the **Information** form under the forms node.</span></span> 
3. <span data-ttu-id="287ad-170">Velg **Informasjon** -skjemaet, og klikk deretter **Aktiver sikkerhetsroller**.</span><span class="sxs-lookup"><span data-stu-id="287ad-170">Select the **Information** form and click **Enable security roles**.</span></span> 
4. <span data-ttu-id="287ad-171">Endre sikkerhetsinnstillingen til **Vis til alle**.</span><span class="sxs-lookup"><span data-stu-id="287ad-171">Change the security setting to **Display to everyone**.</span></span>
