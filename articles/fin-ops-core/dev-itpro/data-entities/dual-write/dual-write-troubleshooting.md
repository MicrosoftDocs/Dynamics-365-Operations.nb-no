---
title: Generell feilsøking
description: Dette emnet inneholder generell feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 4b97fffce6d1c3ea143e0d8445769e794d0c46a4
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566106"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="be49d-103">Generell feilsøking</span><span class="sxs-lookup"><span data-stu-id="be49d-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="be49d-104">Dette emnet inneholder generell feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="be49d-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be49d-105">Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator.</span><span class="sxs-lookup"><span data-stu-id="be49d-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="be49d-106">Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="be49d-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="be49d-107">Når du prøver å installere dobbel skriving-pakken ved hjelp av Package Deployer-verktøyet, vises ingen tilgjengelige løsninger</span><span class="sxs-lookup"><span data-stu-id="be49d-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="be49d-108">Noen versjoner av Package Deployer-verktøyet er ikke kompatible med løsningspakken for dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="be49d-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="be49d-109">Hvis du vil installere pakken, må du bruke [versjon 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) eller senere av Package Deployer-verktøyet.</span><span class="sxs-lookup"><span data-stu-id="be49d-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="be49d-110">Når du har installert Package Deployer-verktøyet, installerer du løsningspakken ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="be49d-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="be49d-111">Last ned den nyeste løsningspakkefilen fra Yammer.com.</span><span class="sxs-lookup"><span data-stu-id="be49d-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="be49d-112">Når zip-filen for pakken er lastet ned, høyreklikker du den og velger **Egenskaper**.</span><span class="sxs-lookup"><span data-stu-id="be49d-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="be49d-113">Merk av for **Fjern blokkering**, og velg deretter **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="be49d-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="be49d-114">Hvis du ikke ser avmerkingsboksen **Fjern blokkering,** er blokkeringen av zip-filen allerede fjernet, og du kan hoppe over dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="be49d-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Dialogboksen Egenskaper](media/unblock_option.png)

2. <span data-ttu-id="be49d-116">Pakk ut zip-filen for pakken, og kopier alle filene i mappen **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**.</span><span class="sxs-lookup"><span data-stu-id="be49d-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Innholdet i mappen Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. <span data-ttu-id="be49d-118">Lim inn alle de kopierte filene i **Verktøy**-mappen i Package Deployer-verktøyet.</span><span class="sxs-lookup"><span data-stu-id="be49d-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="be49d-119">Kjør **PackageDeployer.exe** for å velge Dataverse-miljøet og installere løsningene.</span><span class="sxs-lookup"><span data-stu-id="be49d-119">Run **PackageDeployer.exe** to select the Dataverse environment and install the solutions.</span></span>

    ![Innhold i Verktøy-mappen](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a><span data-ttu-id="be49d-121">Aktivere og vise plugin-sporingsloggen i Dataverse for å vise feildetaljer</span><span class="sxs-lookup"><span data-stu-id="be49d-121">Enable and view the plug-in trace log in Dataverse to view error details</span></span>

<span data-ttu-id="be49d-122">**Nødvendig rolle for å aktivere sporingsloggen og vise feil**: Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="be49d-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="be49d-123">Følg denne fremgangsmåten for å aktivere sporingsloggen.</span><span class="sxs-lookup"><span data-stu-id="be49d-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="be49d-124">Logg inn på den modelldrevne appe i Dynamics 365, åpne **Innstillinger**-siden, og velg deretter **Administrasjon** under **System**.</span><span class="sxs-lookup"><span data-stu-id="be49d-124">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="be49d-125">Velg **Systeminnstillinger** på siden **Administrasjon**.</span><span class="sxs-lookup"><span data-stu-id="be49d-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="be49d-126">I kolonnen **Sporing av plugin-modul og egendefinert arbeidsflytaktivitet** i **Tilpassing**-fanen velger du **Alle** for å aktivere plugin-sporingsloggen.</span><span class="sxs-lookup"><span data-stu-id="be49d-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** column, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="be49d-127">Hvis du bare vil logge sporingslogger når det oppstår unntak, kan du velge **Unntak** i stedet.</span><span class="sxs-lookup"><span data-stu-id="be49d-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="be49d-128">Følg denne fremgangsmåten for å se sporingsloggen.</span><span class="sxs-lookup"><span data-stu-id="be49d-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="be49d-129">Logg inn på den modelldrevne appe i Dynamics 365, åpne **Innstillinger**-siden, og velg deretter **Sporingslogg for plugin-modul** under **Tilpassing**.</span><span class="sxs-lookup"><span data-stu-id="be49d-129">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="be49d-130">Finn sporingsloggene der **Typenavn**-kolonnen er satt til **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span><span class="sxs-lookup"><span data-stu-id="be49d-130">Find the trace logs where the **Type Name** column is set to **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span></span>
3. <span data-ttu-id="be49d-131">Dobbeltklikk et element for å vise hele loggen, og se deretter gjennom **Meldingsblokk**-teksten i hurtigfanen **Utførelse**.</span><span class="sxs-lookup"><span data-stu-id="be49d-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="be49d-132">Aktivere feilsøkingsmodus for å feilsøke problemer med direkte synkronisering i Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="be49d-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="be49d-133">**Nødvendig rolle for å vise feilene:** Systemadministrator – dobbel skriving-feil som kommer fra Dataverse, kan vises i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="be49d-133">**Required role to view the errors:** System admin Dual-write errors that originate in Dataverse can appear in the Finance and Operations app.</span></span> <span data-ttu-id="be49d-134">I noen tilfeller er ikke hele teksten i feilmeldingen tilgjengelig fordi meldingen er for lang eller inneholder personlig identifiserende informasjon (PII).</span><span class="sxs-lookup"><span data-stu-id="be49d-134">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="be49d-135">Du kan aktivere detaljert logging for feil ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="be49d-135">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="be49d-136">Alle prosjektkonfigurasjoner i Finance and Operations-apper har en **IsDebugMode**-egenskap i **DualWriteProjectConfiguration**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="be49d-136">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** table.</span></span> <span data-ttu-id="be49d-137">Åpne **DualWriteProjectConfiguration**-tabellen ved hjelp av Excel-tillegget.</span><span class="sxs-lookup"><span data-stu-id="be49d-137">Open the **DualWriteProjectConfiguration** table by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="be49d-138">En enkel måte å åpne tabellen på er å aktivere **Utforming**-modus i Excel-tillegget og deretter legge til **DualWriteProjectConfigurationEntity** i regnearket.</span><span class="sxs-lookup"><span data-stu-id="be49d-138">An easy way to open the table is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="be49d-139">Hvis du vil ha mer informasjon, kan du se [Åpne tabelldata i Excel og oppdatere dataene ved hjelp av Excel-tillegget](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="be49d-139">For more information, see [Open table data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="be49d-140">Sett egenskapen **IsDebugMode** til **Ja** for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="be49d-140">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="be49d-141">Kjør scenariet som genererer feil.</span><span class="sxs-lookup"><span data-stu-id="be49d-141">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="be49d-142">De detaljerte loggene er tilgjengelige i tabellen DualWriteErrorLog.</span><span class="sxs-lookup"><span data-stu-id="be49d-142">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="be49d-143">Hvis du vil slå opp data i tabelleseren, bruker du følgende URL-adresse (erstatt **XXX** etter behov):</span><span class="sxs-lookup"><span data-stu-id="be49d-143">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="be49d-144">Kontrollere synkroniseringsfeil på den virtuelle maskinen for Finance and Operations-appen</span><span class="sxs-lookup"><span data-stu-id="be49d-144">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="be49d-145">**Nødvendig rolle for å vise feilene:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="be49d-145">**Required role to view the errors:** System administrator</span></span>

1. <span data-ttu-id="be49d-146">Logg på Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="be49d-146">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="be49d-147">Åpne LCS-prosjektet du har valgt til å utføre testing av dobbel skriving for.</span><span class="sxs-lookup"><span data-stu-id="be49d-147">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="be49d-148">Velg flisen **Skybaserte miljøer**.</span><span class="sxs-lookup"><span data-stu-id="be49d-148">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="be49d-149">Bruk Eksternt skrivebord for å logge på den virtuelle maskinen for Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="be49d-149">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="be49d-150">Bruk den lokale kontoen som vises i LCS.</span><span class="sxs-lookup"><span data-stu-id="be49d-150">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="be49d-151">Åpne hendelseslisten.</span><span class="sxs-lookup"><span data-stu-id="be49d-151">Open Event viewer.</span></span>
6. <span data-ttu-id="be49d-152">Velg **Program- og tjenestelogger \> Microsoft \> Dynamics \> AX-DualWriteSync \> Drift**.</span><span class="sxs-lookup"><span data-stu-id="be49d-152">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="be49d-153">Se gjennom listen over nylige feil.</span><span class="sxs-lookup"><span data-stu-id="be49d-153">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="be49d-154">Koble fra og koble til et annet Dataverse-miljø fra en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="be49d-154">Unlink and link another Dataverse environment from a Finance and Operations app</span></span>

<span data-ttu-id="be49d-155">**Nødvendig rolle for å koble fra miljøet:** Systemansvarlig for enten Finance and Operations-app eller Dataverse.</span><span class="sxs-lookup"><span data-stu-id="be49d-155">**Required role to unlink the environment:** System administrator for either Finance and Operations app or Dataverse.</span></span>

1. <span data-ttu-id="be49d-156">Logg på Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="be49d-156">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="be49d-157">Gå til **Arbeidsområder \> Databehandling**, og velg flisen **Dobbel skriving**.</span><span class="sxs-lookup"><span data-stu-id="be49d-157">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="be49d-158">Velg alle kjørende tilordninger, og klikk på **Stopp**.</span><span class="sxs-lookup"><span data-stu-id="be49d-158">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="be49d-159">Klikk på **Koble fra miljø**.</span><span class="sxs-lookup"><span data-stu-id="be49d-159">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="be49d-160">Velg **Ja** for å bekrefte operasjonen.</span><span class="sxs-lookup"><span data-stu-id="be49d-160">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="be49d-161">Du kan nå koble til et nytt miljø.</span><span class="sxs-lookup"><span data-stu-id="be49d-161">You can now link a new environment.</span></span>

## <a name="unable-to-view-the-sales-order-line-information-form"></a><span data-ttu-id="be49d-162">Kan ikke vise informasjonsskjemaet for salgsordrelinjen</span><span class="sxs-lookup"><span data-stu-id="be49d-162">Unable to view the sales order line Information form</span></span> 

<span data-ttu-id="be49d-163">Når du oppretter en salgsordre i Dynamics 365 Sales, kan du bli omdirigert til ordrelinjeskjemaet for Dynamics 365 Project Operations hvis du klikker på **+ Legg til produkter**.</span><span class="sxs-lookup"><span data-stu-id="be49d-163">When you create a sales order in Dynamics 365 Sales, clicking on **+ Add products** might redirect you to the Dynamics 365 Project Operations order line form.</span></span> <span data-ttu-id="be49d-164">Det finnes ingen måter fra dette skjemaet å vise **Informasjon**-skjemaet for salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="be49d-164">There is no way from that form to view the sales order line **Information** form.</span></span> <span data-ttu-id="be49d-165">Alternativet for **Informasjon** vises ikke i rullegardinlisten under **Ny ordrelinje**.</span><span class="sxs-lookup"><span data-stu-id="be49d-165">The option for **Information** does not appear in the dropdown below **New Order Line**.</span></span> <span data-ttu-id="be49d-166">Dette skjer fordi Project Operations er installert i ditt miljø.</span><span class="sxs-lookup"><span data-stu-id="be49d-166">This happens because Project Operations has been installed in your environment.</span></span>

<span data-ttu-id="be49d-167">Følg denne fremgangsmåten for å reaktivere alternativet for **Informasjon**-skjema:</span><span class="sxs-lookup"><span data-stu-id="be49d-167">To re-enable the **Information** form option, follow these steps:</span></span>
1. <span data-ttu-id="be49d-168">Gå til **Ordrelinje**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="be49d-168">Navigate to the **Order Line** table.</span></span>
2. <span data-ttu-id="be49d-169">Finn **Informasjon**-skjemaet under skjemaer-noden.</span><span class="sxs-lookup"><span data-stu-id="be49d-169">Find the **Information** form under the forms node.</span></span> 
3. <span data-ttu-id="be49d-170">Velg **Informasjon**-skjemaet, og klikk deretter **Aktiver sikkerhetsroller**.</span><span class="sxs-lookup"><span data-stu-id="be49d-170">Select the **Information** form and click **Enable security roles**.</span></span> 
4. <span data-ttu-id="be49d-171">Endre sikkerhetsinnstillingen til **Vis til alle**.</span><span class="sxs-lookup"><span data-stu-id="be49d-171">Change the security setting to **Display to everyone**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]