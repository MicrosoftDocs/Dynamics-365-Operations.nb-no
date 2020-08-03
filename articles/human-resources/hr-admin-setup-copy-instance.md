---
title: Kopier en forekomst
description: Du kan bruke Microsoft Dynamics Lifecycle Services (LCS) til å kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkassemiljø.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b14baf49517f5d606038af20366944788b22eba2
ms.sourcegitcommit: 1ec931f8fe86bde27f6def36ea214a2a05fb22f6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/13/2020
ms.locfileid: "3554331"
---
# <a name="copy-an-instance"></a><span data-ttu-id="d8639-103">Kopier en forekomst</span><span class="sxs-lookup"><span data-stu-id="d8639-103">Copy an instance</span></span>

<span data-ttu-id="d8639-104">Du kan bruke Microsoft Dynamics Lifecycle Services (LCS) til å kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="d8639-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="d8639-105">Hvis du har et annet sandkassemiljø, kan du også kopiere databasen fra dette miljøet til et målrettet sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="d8639-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="d8639-106">Hvis du vil kopiere en forekomst, må du sikre følgende:</span><span class="sxs-lookup"><span data-stu-id="d8639-106">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="d8639-107">Forekomsten av Human Resources som du vil overskrive, må være et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="d8639-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="d8639-108">Miljøene du kopierer fra og til, må være i samme område.</span><span class="sxs-lookup"><span data-stu-id="d8639-108">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="d8639-109">Du kan ikke kopiere på tvers av områder.</span><span class="sxs-lookup"><span data-stu-id="d8639-109">You can't copy across regions.</span></span>

- <span data-ttu-id="d8639-110">Du må være administrator i målmiljøet, slik at du kan logge på det etter at du har kopiert forekomsten.</span><span class="sxs-lookup"><span data-stu-id="d8639-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="d8639-111">Når du kopierer Human Resources-databasen, kopierer du ikke elementene (apper eller data) som finnes i et Microsoft PowerApps-miljø.</span><span class="sxs-lookup"><span data-stu-id="d8639-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="d8639-112">Hvis du vil ha informasjon om hvordan du kopierer elementer i et PowerApps-miljø, kan du se [Kopiere et miljø](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="d8639-112">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="d8639-113">PowerApps-miljøet som du vil overskrive, må være et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="d8639-113">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="d8639-114">Du må være en global leieradministrator for å endre et PowerApps-produksjonsmiljø til et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="d8639-114">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="d8639-115">Hvis du vil ha mer informasjon om hvordan du endrer et PowerApps-miljø, kan du se [Bytte en forekomst](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="d8639-115">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="d8639-116">Virkninger av å kopiere en Human Resources-database</span><span class="sxs-lookup"><span data-stu-id="d8639-116">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="d8639-117">Følgende hendelser inntreffer når du kopierer en Human Resources-database:</span><span class="sxs-lookup"><span data-stu-id="d8639-117">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="d8639-118">Kopieringsprosessen sletter den eksisterende databasen i målmiljøet.</span><span class="sxs-lookup"><span data-stu-id="d8639-118">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="d8639-119">Når kopieringsprosessen er fullført, kan du ikke gjenopprette den eksisterende databasen.</span><span class="sxs-lookup"><span data-stu-id="d8639-119">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="d8639-120">Målmiljøet vil ikke være tilgjengelig før kopieringsprosessen er fullført.</span><span class="sxs-lookup"><span data-stu-id="d8639-120">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="d8639-121">Dokumenter i Microsoft Azure Blob-lagring kopieres ikke fra ett miljø til et annet.</span><span class="sxs-lookup"><span data-stu-id="d8639-121">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="d8639-122">Derfor vil ingen dokumenter og maler som er vedlagt, bli kopiert, og de forblir i kildemiljøet.</span><span class="sxs-lookup"><span data-stu-id="d8639-122">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="d8639-123">Alle brukere, bortsett fra administratoren og andre brukerkontoer for interne tjenester, vil bli utilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="d8639-123">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="d8639-124">Derfor kan administratorbrukeren slette eller nedtone data før andre brukere får tilgang til systemet igjen.</span><span class="sxs-lookup"><span data-stu-id="d8639-124">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="d8639-125">Administratorbrukeren må utføre nødvendige konfigurasjonsendringer, for eksempel koble til integreringsendepunkter på nytt til bestemte tjenester eller URL-adresser.</span><span class="sxs-lookup"><span data-stu-id="d8639-125">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="d8639-126">Kopiere Human Resources-databasen</span><span class="sxs-lookup"><span data-stu-id="d8639-126">Copy the Human Resources database</span></span>

<span data-ttu-id="d8639-127">Hvis du vil fullføre denne oppgaven, kopierer du først en forekomst, og deretter logger du deg på administrasjonssenteret for Microsoft Power Platform for å kopiere PowerApps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="d8639-127">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="d8639-128">Når du kopierer en forekomst, slettes databasen i målforekomsten.</span><span class="sxs-lookup"><span data-stu-id="d8639-128">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="d8639-129">Målforekomsten er ikke tilgjengelig under denne prosessen.</span><span class="sxs-lookup"><span data-stu-id="d8639-129">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="d8639-130">Logg på LCS, og velg LCS-prosjektet som inneholder forekomsten du vil kopiere.</span><span class="sxs-lookup"><span data-stu-id="d8639-130">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="d8639-131">I LCS prosjektet velger du flisen **Human Resources-appbehandling**.</span><span class="sxs-lookup"><span data-stu-id="d8639-131">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="d8639-132">Velg forekomsten som skal kopieres, og velg deretter **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="d8639-132">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="d8639-133">I oppgaveruten **Kopier en forekomst**, velger du forekomsten som skal overskrives, og deretter velger du **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="d8639-133">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="d8639-134">Vent til verdien i feltet **Kopier status** er oppdatert til **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="d8639-134">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="d8639-135">Velge forekomst som skal overskrives</span><span class="sxs-lookup"><span data-stu-id="d8639-135">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="d8639-136">Velg **Power Platform**, og logg deg på administrasjonssenteret for Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="d8639-136">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="d8639-137">Velg Power Platform</span><span class="sxs-lookup"><span data-stu-id="d8639-137">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="d8639-138">Velg PowerApps-miljøet som skal kopieres, og velg deretter **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="d8639-138">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="d8639-139">Når kopieringsprosessen er fullført, logger du på målforekomsten og aktiverer Common Data Service-integrering.</span><span class="sxs-lookup"><span data-stu-id="d8639-139">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="d8639-140">Hvis du vil ha mer informasjon og instruksjoner, kan du se [Konfigurere Common Data Service-integrering for arbeidsområder](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="d8639-140">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="d8639-141">Dataelementer og -statuser</span><span class="sxs-lookup"><span data-stu-id="d8639-141">Data elements and statuses</span></span>

<span data-ttu-id="d8639-142">Følgende dataelementer kopieres ikke når du kopierer en Human Resources-forekomst:</span><span class="sxs-lookup"><span data-stu-id="d8639-142">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="d8639-143">E-postadresser i **LogisticsElectronicAddress**-tabellen</span><span class="sxs-lookup"><span data-stu-id="d8639-143">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="d8639-144">Loggen for den satsvise jobben i tabellene **BatchJobHistory**, **BatchHistory** og **BatchConstraintHistory** tables</span><span class="sxs-lookup"><span data-stu-id="d8639-144">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="d8639-145">SMTP-passordet (Simple Mail Transfer Protocol) i **SysEmailSMTPPassword**-tabellen</span><span class="sxs-lookup"><span data-stu-id="d8639-145">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="d8639-146">SMTP-reléserveren i **SysEmailParameters**-tabellen</span><span class="sxs-lookup"><span data-stu-id="d8639-146">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="d8639-147">Innstillinger for utskriftsbehandling i tabellene **PrintMgmtSettings** og **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="d8639-147">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="d8639-148">Miljøspesifikke poster i tabellene **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** og **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="d8639-148">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="d8639-149">Dokumentvedlegg i DocuValue-tabellen.</span><span class="sxs-lookup"><span data-stu-id="d8639-149">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="d8639-150">Disse vedleggene omfatter alle Microsoft Office-maler som ble overskrevet i kildemiljøet</span><span class="sxs-lookup"><span data-stu-id="d8639-150">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="d8639-151">Tilkoblingsstrengen i **PersonnelIntegrationConfiguration**-tabellen</span><span class="sxs-lookup"><span data-stu-id="d8639-151">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="d8639-152">Noen av disse elementene kopieres ikke fordi de er miljøspesifikke.</span><span class="sxs-lookup"><span data-stu-id="d8639-152">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="d8639-153">Eksempler inkluderer postene **BatchServerConfig** og **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="d8639-153">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="d8639-154">Andre elementer blir ikke kopiert på grunn av antallet kundestøttebilletter.</span><span class="sxs-lookup"><span data-stu-id="d8639-154">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="d8639-155">Det kan for eksempel hende at dupliserte e-poster sendes fordi SMTP fortsatt er aktivert i sandkassemiljøet for godkjenning av bruker, ugyldige integrasjonsmeldinger kan bli sendt fordi de fortsatt er aktive, og brukere kan bli aktivert før administratorer kan utføre handlinger opprydding etter oppdatering.</span><span class="sxs-lookup"><span data-stu-id="d8639-155">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="d8639-156">I tillegg endres følgende statuser når du kopierer en forekomst:</span><span class="sxs-lookup"><span data-stu-id="d8639-156">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="d8639-157">Alle brukere bortsett fra administratorer settes til **Deaktivert**.</span><span class="sxs-lookup"><span data-stu-id="d8639-157">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="d8639-158">Alle satsvise jobber, bortsett fra enkelte systemjobber, settes til **Trekk tilbake**.</span><span class="sxs-lookup"><span data-stu-id="d8639-158">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="d8639-159">Miljøadministrator</span><span class="sxs-lookup"><span data-stu-id="d8639-159">Environment admin</span></span>

<span data-ttu-id="d8639-160">Alle brukerne i sandkassemålmiljøet, inkludert administratorer, erstattes av brukerne i kildemiljøet.</span><span class="sxs-lookup"><span data-stu-id="d8639-160">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="d8639-161">Før du kopierer en forekomst, må du være sikker på at du er administrator i kildemiljøet.</span><span class="sxs-lookup"><span data-stu-id="d8639-161">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="d8639-162">Hvis du ikke er det, vil du ikke kunne logge på målsandkassemiljøet etter at kopieringen er fullført.</span><span class="sxs-lookup"><span data-stu-id="d8639-162">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="d8639-163">Alle brukere som ikke er administrator i målsandkassemiljøet, er deaktivert for å hindre uønskede pålogginger i sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="d8639-163">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="d8639-164">Administratorer kan reaktivere brukere om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="d8639-164">Administrators can reenable users if needed.</span></span>
