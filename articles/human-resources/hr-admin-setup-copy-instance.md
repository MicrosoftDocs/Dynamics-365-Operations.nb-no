---
title: Kopier en forekomst
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010024"
---
# <a name="copy-an-instance"></a><span data-ttu-id="03e78-102">Kopier en forekomst</span><span class="sxs-lookup"><span data-stu-id="03e78-102">Copy an instance</span></span>

<span data-ttu-id="03e78-103">Du kan bruke Microsoft Dynamics Lifecycle Services (LCS) til å kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="03e78-103">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="03e78-104">Hvis du har et annet sandkassemiljø, kan du også kopiere databasen fra dette miljøet til et målrettet sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="03e78-104">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="03e78-105">Hvis du vil kopiere en forekomst, må du sikre følgende:</span><span class="sxs-lookup"><span data-stu-id="03e78-105">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="03e78-106">Forekomsten av Human Resources som du vil overskrive, må være et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="03e78-106">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="03e78-107">Miljøene du kopierer fra og til, må være i samme område.</span><span class="sxs-lookup"><span data-stu-id="03e78-107">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="03e78-108">Du kan ikke kopiere på tvers av områder.</span><span class="sxs-lookup"><span data-stu-id="03e78-108">You can't copy across regions.</span></span>

- <span data-ttu-id="03e78-109">Du må være administrator i målmiljøet, slik at du kan logge på det etter at du har kopiert forekomsten.</span><span class="sxs-lookup"><span data-stu-id="03e78-109">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="03e78-110">Når du kopierer Human Resources-databasen, kopierer du ikke elementene (apper eller data) som finnes i et Microsoft PowerApps-miljø.</span><span class="sxs-lookup"><span data-stu-id="03e78-110">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="03e78-111">Hvis du vil ha informasjon om hvordan du kopierer elementer i et PowerApps-miljø, kan du se [Kopiere et miljø](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="03e78-111">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="03e78-112">PowerApps-miljøet som du vil overskrive, må være et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="03e78-112">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="03e78-113">Du må være en global leieradministrator for å endre et PowerApps-produksjonsmiljø til et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="03e78-113">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="03e78-114">Hvis du vil ha mer informasjon om hvordan du endrer et PowerApps-miljø, kan du se [Bytte en forekomst](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="03e78-114">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="03e78-115">Virkninger av å kopiere en Human Resources-database</span><span class="sxs-lookup"><span data-stu-id="03e78-115">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="03e78-116">Følgende hendelser inntreffer når du kopierer en Human Resources-database:</span><span class="sxs-lookup"><span data-stu-id="03e78-116">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="03e78-117">Kopieringsprosessen sletter den eksisterende databasen i målmiljøet.</span><span class="sxs-lookup"><span data-stu-id="03e78-117">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="03e78-118">Når kopieringsprosessen er fullført, kan du ikke gjenopprette den eksisterende databasen.</span><span class="sxs-lookup"><span data-stu-id="03e78-118">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="03e78-119">Målmiljøet vil ikke være tilgjengelig før kopieringsprosessen er fullført.</span><span class="sxs-lookup"><span data-stu-id="03e78-119">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="03e78-120">Dokumenter i Microsoft Azure Blob-lagring kopieres ikke fra ett miljø til et annet.</span><span class="sxs-lookup"><span data-stu-id="03e78-120">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="03e78-121">Derfor vil ingen dokumenter og maler som er vedlagt, bli kopiert, og de forblir i kildemiljøet.</span><span class="sxs-lookup"><span data-stu-id="03e78-121">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="03e78-122">Alle brukere, bortsett fra administratoren og andre brukerkontoer for interne tjenester, vil bli utilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="03e78-122">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="03e78-123">Derfor kan administratorbrukeren slette eller nedtone data før andre brukere får tilgang til systemet igjen.</span><span class="sxs-lookup"><span data-stu-id="03e78-123">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="03e78-124">Administratorbrukeren må utføre nødvendige konfigurasjonsendringer, for eksempel koble til integreringsendepunkter på nytt til bestemte tjenester eller URL-adresser.</span><span class="sxs-lookup"><span data-stu-id="03e78-124">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="03e78-125">Kopiere Human Resources-databasen</span><span class="sxs-lookup"><span data-stu-id="03e78-125">Copy the Human Resources database</span></span>

<span data-ttu-id="03e78-126">Hvis du vil fullføre denne oppgaven, kopierer du først en forekomst, og deretter logger du deg på administrasjonssenteret for Microsoft Power Platform for å kopiere PowerApps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="03e78-126">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="03e78-127">Når du kopierer en forekomst, slettes databasen i målforekomsten.</span><span class="sxs-lookup"><span data-stu-id="03e78-127">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="03e78-128">Målforekomsten er ikke tilgjengelig under denne prosessen.</span><span class="sxs-lookup"><span data-stu-id="03e78-128">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="03e78-129">Logg på LCS, og velg LCS-prosjektet som inneholder forekomsten du vil kopiere.</span><span class="sxs-lookup"><span data-stu-id="03e78-129">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="03e78-130">I LCS prosjektet velger du flisen **Human Resources-appbehandling**.</span><span class="sxs-lookup"><span data-stu-id="03e78-130">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="03e78-131">Velg forekomsten som skal kopieres, og velg deretter **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="03e78-131">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="03e78-132">I oppgaveruten **Kopier en forekomst**, velger du forekomsten som skal overskrives, og deretter velger du **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="03e78-132">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="03e78-133">Vent til verdien i feltet **Kopier status** er oppdatert til **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="03e78-133">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="03e78-134">Velge forekomst som skal overskrives</span><span class="sxs-lookup"><span data-stu-id="03e78-134">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="03e78-135">Velg **Power Platform**, og logg deg på administrasjonssenteret for Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="03e78-135">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="03e78-136">Velg Power Platform</span><span class="sxs-lookup"><span data-stu-id="03e78-136">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="03e78-137">Velg PowerApps-miljøet som skal kopieres, og velg deretter **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="03e78-137">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="03e78-138">Når kopieringsprosessen er fullført, logger du på målforekomsten og aktiverer Common Data Service-integrering.</span><span class="sxs-lookup"><span data-stu-id="03e78-138">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="03e78-139">Hvis du vil ha mer informasjon og instruksjoner, kan du se [Konfigurere Common Data Service-integrering for arbeidsområder](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="03e78-139">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="03e78-140">Dataelementer og -statuser</span><span class="sxs-lookup"><span data-stu-id="03e78-140">Data elements and statuses</span></span>

<span data-ttu-id="03e78-141">Følgende dataelementer kopieres ikke når du kopierer en Human Resources-forekomst:</span><span class="sxs-lookup"><span data-stu-id="03e78-141">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="03e78-142">E-postadresser i **LogisticsElectronicAddress**-tabellen</span><span class="sxs-lookup"><span data-stu-id="03e78-142">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="03e78-143">Loggen for den satsvise jobben i tabellene **BatchJobHistory**, **BatchHistory** og **BatchConstraintHistory** tables</span><span class="sxs-lookup"><span data-stu-id="03e78-143">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="03e78-144">SMTP-passordet (Simple Mail Transfer Protocol) i **SysEmailSMTPPassword**-tabellen</span><span class="sxs-lookup"><span data-stu-id="03e78-144">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="03e78-145">SMTP-reléserveren i **SysEmailParameters**-tabellen</span><span class="sxs-lookup"><span data-stu-id="03e78-145">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="03e78-146">Innstillinger for utskriftsbehandling i tabellene **PrintMgmtSettings** og **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="03e78-146">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="03e78-147">Miljøspesifikke poster i tabellene **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** og **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="03e78-147">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="03e78-148">Dokumentvedlegg i DocuValue-tabellen.</span><span class="sxs-lookup"><span data-stu-id="03e78-148">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="03e78-149">Disse vedleggene omfatter alle Microsoft Office-maler som ble overskrevet i kildemiljøet</span><span class="sxs-lookup"><span data-stu-id="03e78-149">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="03e78-150">Tilkoblingsstrengen i **PersonnelIntegrationConfiguration**-tabellen</span><span class="sxs-lookup"><span data-stu-id="03e78-150">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="03e78-151">Noen av disse elementene kopieres ikke fordi de er miljøspesifikke.</span><span class="sxs-lookup"><span data-stu-id="03e78-151">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="03e78-152">Eksempler inkluderer postene **BatchServerConfig** og **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="03e78-152">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="03e78-153">Andre elementer blir ikke kopiert på grunn av antallet kundestøttebilletter.</span><span class="sxs-lookup"><span data-stu-id="03e78-153">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="03e78-154">Det kan for eksempel hende at dupliserte e-poster sendes fordi SMTP fortsatt er aktivert i sandkassemiljøet for godkjenning av bruker, ugyldige integrasjonsmeldinger kan bli sendt fordi de fortsatt er aktive, og brukere kan bli aktivert før administratorer kan utføre handlinger opprydding etter oppdatering.</span><span class="sxs-lookup"><span data-stu-id="03e78-154">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="03e78-155">I tillegg endres følgende statuser når du kopierer en forekomst:</span><span class="sxs-lookup"><span data-stu-id="03e78-155">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="03e78-156">Alle brukere bortsett fra administratorer settes til **Deaktivert**.</span><span class="sxs-lookup"><span data-stu-id="03e78-156">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="03e78-157">Alle satsvise jobber, bortsett fra enkelte systemjobber, settes til **Trekk tilbake**.</span><span class="sxs-lookup"><span data-stu-id="03e78-157">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="03e78-158">Miljøadministrator</span><span class="sxs-lookup"><span data-stu-id="03e78-158">Environment admin</span></span>

<span data-ttu-id="03e78-159">Alle brukerne i sandkassemålmiljøet, inkludert administratorer, erstattes av brukerne i kildemiljøet.</span><span class="sxs-lookup"><span data-stu-id="03e78-159">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="03e78-160">Før du kopierer en forekomst, må du være sikker på at du er administrator i målmiljøet.</span><span class="sxs-lookup"><span data-stu-id="03e78-160">Before you copy an instance, be sure that you're an Administrator in the target environment.</span></span> <span data-ttu-id="03e78-161">Hvis du ikke er det, vil du ikke kunne logge på målsandkassemiljøet etter at kopieringen er fullført.</span><span class="sxs-lookup"><span data-stu-id="03e78-161">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="03e78-162">Alle brukere som ikke er administrator i målsandkassemiljøet, er deaktivert for å hindre uønskede pålogginger i sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="03e78-162">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="03e78-163">Administratorer kan reaktivere brukere om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="03e78-163">Administrators can reenable users if needed.</span></span>
