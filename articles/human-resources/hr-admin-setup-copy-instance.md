---
title: Kopier en forekomst
description: Du kan bruke Microsoft Dynamics Lifecycle Services (LCS) til å kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkassemiljø.
author: andreabichsel
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6cb8050980b9b54480d09a59379430cd229ff141
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801101"
---
# <a name="copy-an-instance"></a><span data-ttu-id="0047b-103">Kopier en forekomst</span><span class="sxs-lookup"><span data-stu-id="0047b-103">Copy an instance</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0047b-104">Du kan bruke Microsoft Dynamics Lifecycle Services (LCS) til å kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="0047b-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="0047b-105">Hvis du har et annet sandkassemiljø, kan du også kopiere databasen fra dette miljøet til et målrettet sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="0047b-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="0047b-106">Hvis du vil kopiere en forekomst, må du tenke på følgende tips:</span><span class="sxs-lookup"><span data-stu-id="0047b-106">To copy an instance, keep the following tips in mind:</span></span>

- <span data-ttu-id="0047b-107">Forekomsten av Human Resources som du vil overskrive, må være et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="0047b-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="0047b-108">Miljøene du kopierer fra og til, må være i samme område.</span><span class="sxs-lookup"><span data-stu-id="0047b-108">The environments you're copying from and to must be in the same region.</span></span> <span data-ttu-id="0047b-109">Du kan ikke kopiere på tvers av områder.</span><span class="sxs-lookup"><span data-stu-id="0047b-109">You can't copy across regions.</span></span>

- <span data-ttu-id="0047b-110">Du må være administrator i målmiljøet, slik at du kan logge på det etter at du har kopiert forekomsten.</span><span class="sxs-lookup"><span data-stu-id="0047b-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="0047b-111">Når du kopierer Human Resources-databasen, kopierer du ikke elementene (apper eller data) som finnes i et Microsoft Power Apps-miljø.</span><span class="sxs-lookup"><span data-stu-id="0047b-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft Power Apps environment.</span></span> <span data-ttu-id="0047b-112">Hvis du vil ha informasjon om hvordan du kopierer elementer i et Power Apps-miljø, kan du se [Kopiere et miljø](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="0047b-112">For information about how to copy elements in a Power Apps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="0047b-113">Power Apps-miljøet som du vil overskrive, må være et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="0047b-113">The Power Apps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="0047b-114">Du må være en global leieradministrator for å endre et Power Apps-produksjonsmiljø til et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="0047b-114">You must be a global tenant admin to change a Power Apps production environment to a sandbox environment.</span></span> <span data-ttu-id="0047b-115">Hvis du vil ha mer informasjon om hvordan du endrer et Power Apps-miljø, kan du se [Bytte en forekomst](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="0047b-115">For more information about changing a Power Apps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

- <span data-ttu-id="0047b-116">Hvis du kopierer en forekomst inn i sandkassemiljøet og vil integrere sandkassemiljøet i Dataverse, må du bruke egendefinerte felt på nytt i Dataverse-tabeller.</span><span class="sxs-lookup"><span data-stu-id="0047b-116">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span> <span data-ttu-id="0047b-117">Se [Bruke egendefinerte felt i Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span><span class="sxs-lookup"><span data-stu-id="0047b-117">See [Apply custom fields to Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="0047b-118">Virkninger av å kopiere en Human Resources-database</span><span class="sxs-lookup"><span data-stu-id="0047b-118">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="0047b-119">Følgende hendelser inntreffer når du kopierer en Human Resources-database:</span><span class="sxs-lookup"><span data-stu-id="0047b-119">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="0047b-120">Kopieringsprosessen sletter den eksisterende databasen i målmiljøet.</span><span class="sxs-lookup"><span data-stu-id="0047b-120">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="0047b-121">Når kopieringsprosessen er fullført, kan du ikke gjenopprette den eksisterende databasen.</span><span class="sxs-lookup"><span data-stu-id="0047b-121">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="0047b-122">Målmiljøet vil ikke være tilgjengelig før kopieringsprosessen er fullført.</span><span class="sxs-lookup"><span data-stu-id="0047b-122">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="0047b-123">Dokumenter i Microsoft Azure Blob-lagring kopieres ikke fra ett miljø til et annet.</span><span class="sxs-lookup"><span data-stu-id="0047b-123">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="0047b-124">Derfor vil ingen dokumenter og maler som er vedlagt, bli kopiert, og de forblir i kildemiljøet.</span><span class="sxs-lookup"><span data-stu-id="0047b-124">As a result, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="0047b-125">Alle brukere, bortsett fra administratoren og andre brukerkontoer for interne tjenester, vil bli utilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="0047b-125">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="0047b-126">Administratorbrukeren kan slette eller nedtone data før andre brukere får tilgang til systemet igjen.</span><span class="sxs-lookup"><span data-stu-id="0047b-126">The Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="0047b-127">Administratorbrukeren må utføre nødvendige konfigurasjonsendringer, for eksempel koble til integreringsendepunkter på nytt til bestemte tjenester eller URL-adresser.</span><span class="sxs-lookup"><span data-stu-id="0047b-127">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="0047b-128">Kopiere Human Resources-databasen</span><span class="sxs-lookup"><span data-stu-id="0047b-128">Copy the Human Resources database</span></span>

<span data-ttu-id="0047b-129">Hvis du vil fullføre denne oppgaven, kopierer du først en forekomst, og deretter logger du deg på administrasjonssenteret for Microsoft Power Platform for å kopiere Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="0047b-129">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your Power Apps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="0047b-130">Når du kopierer en forekomst, slettes databasen i målforekomsten.</span><span class="sxs-lookup"><span data-stu-id="0047b-130">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="0047b-131">Målforekomsten er ikke tilgjengelig under denne prosessen.</span><span class="sxs-lookup"><span data-stu-id="0047b-131">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="0047b-132">Logg på LCS, og velg LCS-prosjektet som inneholder forekomsten du vil kopiere.</span><span class="sxs-lookup"><span data-stu-id="0047b-132">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="0047b-133">I LCS prosjektet velger du flisen **Human Resources-appbehandling**.</span><span class="sxs-lookup"><span data-stu-id="0047b-133">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="0047b-134">Velg forekomsten som skal kopieres, og velg deretter **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="0047b-134">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="0047b-135">I oppgaveruten **Kopier en forekomst**, velger du forekomsten som skal overskrives, og deretter velger du **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="0047b-135">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="0047b-136">Vent til verdien i feltet **Kopier status** er oppdatert til **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="0047b-136">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="0047b-137">Velge forekomst som skal overskrives</span><span class="sxs-lookup"><span data-stu-id="0047b-137">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="0047b-138">Velg **Power Platform**, og logg deg på administrasjonssenteret for Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="0047b-138">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="0047b-139">Velg Power Platform</span><span class="sxs-lookup"><span data-stu-id="0047b-139">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="0047b-140">Velg Power Apps-miljøet som skal kopieres, og velg deretter **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="0047b-140">Select the Power Apps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="0047b-141">Når kopieringsprosessen er fullført, logger du på målforekomsten og aktiverer Dataverse-integrering.</span><span class="sxs-lookup"><span data-stu-id="0047b-141">When the copy process is completed, sign in to the target instance, and enable Dataverse integration.</span></span> <span data-ttu-id="0047b-142">Hvis du vil ha mer informasjon og instruksjoner, kan du se [Konfigurere Dataverse-integrering for arbeidsområder](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="0047b-142">For more information and instructions, see [Configure Dataverse integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="0047b-143">Dataelementer og -statuser</span><span class="sxs-lookup"><span data-stu-id="0047b-143">Data elements and statuses</span></span>

<span data-ttu-id="0047b-144">Følgende dataelementer kopieres ikke når du kopierer en Human Resources-forekomst:</span><span class="sxs-lookup"><span data-stu-id="0047b-144">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="0047b-145">E-postadresser i **LogisticsElectronicAddress**-tabellen</span><span class="sxs-lookup"><span data-stu-id="0047b-145">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="0047b-146">Loggen for den satsvise jobben i tabellene **BatchJobHistory**, **BatchHistory** og **BatchConstraintHistory** tables</span><span class="sxs-lookup"><span data-stu-id="0047b-146">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="0047b-147">SMTP-passordet (Simple Mail Transfer Protocol) i **SysEmailSMTPPassword**-tabellen</span><span class="sxs-lookup"><span data-stu-id="0047b-147">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="0047b-148">SMTP-reléserveren i **SysEmailParameters**-tabellen</span><span class="sxs-lookup"><span data-stu-id="0047b-148">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="0047b-149">Innstillinger for utskriftsbehandling i tabellene **PrintMgmtSettings** og **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="0047b-149">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="0047b-150">Miljøspesifikke poster i tabellene **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** og **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="0047b-150">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="0047b-151">Dokumentvedlegg i DocuValue-tabellen.</span><span class="sxs-lookup"><span data-stu-id="0047b-151">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="0047b-152">Disse vedleggene omfatter alle Microsoft Office-maler som ble overskrevet i kildemiljøet</span><span class="sxs-lookup"><span data-stu-id="0047b-152">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="0047b-153">Tilkoblingsstrengen i **PersonnelIntegrationConfiguration**-tabellen</span><span class="sxs-lookup"><span data-stu-id="0047b-153">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="0047b-154">Noen av disse elementene kopieres ikke fordi de er miljøspesifikke.</span><span class="sxs-lookup"><span data-stu-id="0047b-154">Some of these elements aren't copied because they're environment-specific.</span></span> <span data-ttu-id="0047b-155">Eksempler inkluderer postene **BatchServerConfig** og **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="0047b-155">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="0047b-156">Andre elementer blir ikke kopiert på grunn av antallet kundestøttebilletter.</span><span class="sxs-lookup"><span data-stu-id="0047b-156">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="0047b-157">For eksempel:</span><span class="sxs-lookup"><span data-stu-id="0047b-157">For example:</span></span>

- <span data-ttu-id="0047b-158">Det kan hende at det sendes dupliserte e-postmeldinger fordi SMTP fortsatt er aktivert i miljøet for testing av brukeraksept (sandkasse).</span><span class="sxs-lookup"><span data-stu-id="0047b-158">Duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment.</span></span>

- <span data-ttu-id="0047b-159">Det kan hende at ugyldige integrasjonsmeldinger sendes fordi de satsvise jobbene fortsatt er aktive.</span><span class="sxs-lookup"><span data-stu-id="0047b-159">Invalid integration messages might be sent because batch jobs are still enabled.</span></span>

- <span data-ttu-id="0047b-160">Brukere kan være aktivert før administratorer kan utføre oppryddingshandlinger etter oppdatering.</span><span class="sxs-lookup"><span data-stu-id="0047b-160">Users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="0047b-161">I tillegg endres følgende statuser når du kopierer en forekomst:</span><span class="sxs-lookup"><span data-stu-id="0047b-161">Also, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="0047b-162">Alle brukere bortsett fra administratorer settes til **Deaktivert**.</span><span class="sxs-lookup"><span data-stu-id="0047b-162">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="0047b-163">Alle satsvise jobber, bortsett fra enkelte systemjobber, settes til **Trekk tilbake**.</span><span class="sxs-lookup"><span data-stu-id="0047b-163">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="0047b-164">Miljøadministrator</span><span class="sxs-lookup"><span data-stu-id="0047b-164">Environment admin</span></span>

<span data-ttu-id="0047b-165">Alle brukerne i sandkassemålmiljøet, inkludert administratorer, erstattes av brukerne i kildemiljøet.</span><span class="sxs-lookup"><span data-stu-id="0047b-165">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="0047b-166">Før du kopierer en forekomst, må du være sikker på at du er administrator i kildemiljøet.</span><span class="sxs-lookup"><span data-stu-id="0047b-166">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="0047b-167">Hvis du ikke er det, vil du ikke kunne logge på målsandkassemiljøet etter at kopieringen er fullført.</span><span class="sxs-lookup"><span data-stu-id="0047b-167">If you aren't, you can't sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="0047b-168">Alle brukere som ikke er administrator i målsandkassemiljøet, er deaktivert for å hindre uønskede pålogginger i sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="0047b-168">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="0047b-169">Administratorer kan reaktivere brukere om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="0047b-169">Administrators can reenable users if needed.</span></span>

## <a name="apply-custom-fields-to-dataverse"></a><span data-ttu-id="0047b-170">Bruke egendefinerte felt i Dataverse</span><span class="sxs-lookup"><span data-stu-id="0047b-170">Apply custom fields to Dataverse</span></span>

<span data-ttu-id="0047b-171">Hvis du kopierer en forekomst inn i sandkassemiljøet og vil integrere sandkassemiljøet i Dataverse, må du bruke egendefinerte felt på nytt i Dataverse-tabeller.</span><span class="sxs-lookup"><span data-stu-id="0047b-171">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span>

<span data-ttu-id="0047b-172">For hvert egendefinerte felt som vises på Dataverse-tabeller, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="0047b-172">For each custom field that's exposed on Dataverse tables, do the following steps:</span></span>

1. <span data-ttu-id="0047b-173">Gå til det egendefinerte feltet og velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="0047b-173">Go to the custom field and select **Edit**.</span></span>

2. <span data-ttu-id="0047b-174">Fjern merket i **Aktivert**-feltet for hver cdm_\*-enhet som det egendefinerte feltet er aktivert på.</span><span class="sxs-lookup"><span data-stu-id="0047b-174">Unselect the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

3. <span data-ttu-id="0047b-175">Velg **Bruk endringer**.</span><span class="sxs-lookup"><span data-stu-id="0047b-175">Select **Apply Changes**.</span></span>

4. <span data-ttu-id="0047b-176">Velg **Rediger** på nytt.</span><span class="sxs-lookup"><span data-stu-id="0047b-176">Select **Edit** again.</span></span>

5. <span data-ttu-id="0047b-177">Velg feltet **Aktivert** for hver cdm_\*-enhet som det egendefinerte feltet er aktivert på.</span><span class="sxs-lookup"><span data-stu-id="0047b-177">Select the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

6. <span data-ttu-id="0047b-178">Velg **Bruk endringer** på nytt.</span><span class="sxs-lookup"><span data-stu-id="0047b-178">Select **Apply Changes** again.</span></span>

<span data-ttu-id="0047b-179">Prosessen med å fjerne valg, aktivere endringer, velge på nytt og bruke endringer på nytt ber skjemaet om å oppdatere i Dataverse for å inkludere de egendefinerte feltene.</span><span class="sxs-lookup"><span data-stu-id="0047b-179">The process of unselecting, applying changes, reselecting, and reapplying changes prompts the schema to update in Dataverse to include the custom fields.</span></span>

<span data-ttu-id="0047b-180">Hvis du vil ha mer informasjon om egendefinerte felt, kan du se [Opprette og arbeide med egendefinerte felt](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span><span class="sxs-lookup"><span data-stu-id="0047b-180">For more information about custom fields, see [Create and work with custom fields](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span></span>

## <a name="see-also"></a><span data-ttu-id="0047b-181">Se også</span><span class="sxs-lookup"><span data-stu-id="0047b-181">See also</span></span>

[<span data-ttu-id="0047b-182">Klargjøre Human Resources</span><span class="sxs-lookup"><span data-stu-id="0047b-182">Provision Human Resources</span></span>](hr-admin-setup-provision.md)</br>
[<span data-ttu-id="0047b-183">Fjerne en forekomst</span><span class="sxs-lookup"><span data-stu-id="0047b-183">Remove an instance</span></span>](hr-admin-setup-remove-instance.md)</br>
[<span data-ttu-id="0047b-184">Oppdatere prosess</span><span class="sxs-lookup"><span data-stu-id="0047b-184">Update process</span></span>](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]