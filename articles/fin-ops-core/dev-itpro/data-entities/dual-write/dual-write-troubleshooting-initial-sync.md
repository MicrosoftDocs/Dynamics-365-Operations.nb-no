---
title: Feilsøke problemer under første synkronisering
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer som kan oppstå under første synkronisering.
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
ms.openlocfilehash: a2f0e0cbf0f8710dc020a48506775fa28df9c2d2
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744643"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="5a8b1-103">Feilsøke problemer under første synkronisering</span><span class="sxs-lookup"><span data-stu-id="5a8b1-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5a8b1-104">Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="5a8b1-105">Det inneholder informasjon som kan hjelpe deg med å løse problemer som kan oppstå under første synkronisering.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5a8b1-106">Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="5a8b1-107">Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="5a8b1-108">Se etter innledende synkroniseringsfeil i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="5a8b1-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="5a8b1-109">Når du har aktivert tilordningsmalene, skal statusen for tilordningene være **Kjører**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="5a8b1-110">Hvis statusen er **Kjører ikke**, oppstod det feil under første synkronisering.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="5a8b1-111">Hvis du vil vise feilene, velger du fanen **Detaljer om innledende synkronisering** på siden **Dobbel skriving**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Feil i fanen Detaljer om innledende synkronisering](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="5a8b1-113">Du kan ikke fullføre første synkronisering: 400 Ugyldig forespørsel</span><span class="sxs-lookup"><span data-stu-id="5a8b1-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="5a8b1-114">**Nødvendig rolle for å løse problemet:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="5a8b1-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="5a8b1-115">Du kan få følgende feilmelding når du prøver å kjøre tilordningen og den innledende synkroniseringen:</span><span class="sxs-lookup"><span data-stu-id="5a8b1-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="5a8b1-116">*(\[Ugyldig forespørsel\], Den eksterne serveren returnerte en feil: (400) Ugyldig forespørsel.), AX-eksporten oppdaget en feil*</span><span class="sxs-lookup"><span data-stu-id="5a8b1-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="5a8b1-117">Her er et eksempel på hele feilmeldingen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="5a8b1-118">Hvis denne feilen oppstår konsekvent, og du ikke kan fullføre den første synkroniseringen, følger du denne fremgangsmåten for å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="5a8b1-119">Logg på den virtuelle maskinen for Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="5a8b1-120">Åpne Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="5a8b1-121">I **Tjenester**-ruten kontrollerer du at tjenesten for rammeverk for dataimport/-eksport for Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="5a8b1-122">Start den på nytt hvis den er stoppet, fordi den første synkroniseringen krever det.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="5a8b1-123">Innledende synkroniseringsfeil: 403 forbudt</span><span class="sxs-lookup"><span data-stu-id="5a8b1-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="5a8b1-124">Du kan få følgende feilmelding under innledende synkronisering:</span><span class="sxs-lookup"><span data-stu-id="5a8b1-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="5a8b1-125">*(\[Forbudt\], Den eksterne serveren returnerte en feil: (403) Forbudt.), AX-eksporten oppdaget en feil*</span><span class="sxs-lookup"><span data-stu-id="5a8b1-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="5a8b1-126">Følg fremgangsmåten nedenfor for å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="5a8b1-127">Logg på Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="5a8b1-128">På siden **Azure Active Directory-programmer** sletter du **DtAppID**-klienten, og deretter legger du den til på nytt.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![DtAppID-klient i listen over Azure AD-programmer](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="5a8b1-130">Egenreferanse- eller sirkelreferansefeil under innledende synkronisering</span><span class="sxs-lookup"><span data-stu-id="5a8b1-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="5a8b1-131">Du kan få feilmeldinger hvis noen av tilordningene dine har egenreferanser eller sirkelreferanser.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="5a8b1-132">Feilene faller under følgende kategorier:</span><span class="sxs-lookup"><span data-stu-id="5a8b1-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="5a8b1-133">Feil i tabelltilordning Leverandører V2 til msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="5a8b1-133">Errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="5a8b1-134">Feil i tabelltilordningen Kunder V3 til Kontoer</span><span class="sxs-lookup"><span data-stu-id="5a8b1-134">Errors in the Customers V3–to–Accounts table mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="5a8b1-135">Løs feil i tabelltilordningen Leverandører V2 til msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="5a8b1-135">Resolve errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>

<span data-ttu-id="5a8b1-136">Det kan hende at det oppstår feil med innledende synkronisering for tilordningen **Leverandører V2** til **msdyn\_vendors** hvis tabellene har eksisterende rader med verdier i feltene **PrimaryContactPersonId** og kolonnen **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the tables have existing rows where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns.</span></span> <span data-ttu-id="5a8b1-137">Disse feilene skjer fordi **InvoiceVendorAccountNumber** er en selvrefererende kolonne, og **PrimaryContactPersonId** er en sirkelreferanse i leverandørtilordningen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing column, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="5a8b1-138">Feilmeldingene du mottar, vil ha følgende form.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="5a8b1-139">*Fant ikke GUID for feltet: \<field\>. Oppslaget ga ingen treff: \<value\>. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="5a8b1-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="5a8b1-140">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="5a8b1-140">Here are some examples:</span></span>

- <span data-ttu-id="5a8b1-141">*Fant ikke GUID for feltet: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Oppslaget ga ingen treff: 000056. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="5a8b1-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="5a8b1-142">*Fant ikke GUID for feltet: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Oppslaget ga ingen treff: V24-1. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="5a8b1-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="5a8b1-143">Hvis rader i leverandørtabellen har verdier i kolonnene **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**, følger du disse trinnene for å fullføre den innledende synkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-143">If any rows in the vendor table have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="5a8b1-144">I Finance and Operations-appen sletter du kolonnene **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** fra tilordningen, og deretter lagrer du tilordningen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="5a8b1-145">På siden for tilordning med dobbeltskriving for **Leverandører V2 (msdyn\_vendors)**, i fanen **Tabelltilordninger** i filteret til venstre velger du **Finance and Operations-apper.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="5a8b1-146">I filteret til høyre velger du **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="5a8b1-147">Søk etter **primarycontactperson** for å finne kildekolonnen **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source column.</span></span>
    3. <span data-ttu-id="5a8b1-148">Velg **Handlinger**, og velg deretter **Slett**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-148">Select **Actions**, and then select **Delete**.</span></span>

        ![Slette kolonnen PrimaryContactPersonId](media/vend_selfref3.png)

    4. <span data-ttu-id="5a8b1-150">Gjenta disse trinnene for å slette kolonnen **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** column.</span></span>

        ![Slette kolonnen InvoiceVendorAccountNumber](media/vend-selfref4.png)

    5. <span data-ttu-id="5a8b1-152">Lagre endringene i tilordningen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="5a8b1-153">Deaktiver sporing av endringer for **Leverandører V2**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-153">Turn off change tracking for the **Vendors V2** table.</span></span>

    1. <span data-ttu-id="5a8b1-154">I arbeidsområdet **Dataadministrasjon** velger du flisen **Datatabeller**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-154">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="5a8b1-155">Velg **Leverandører V2**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-155">Select the **Vendors V2** table.</span></span>
    3. <span data-ttu-id="5a8b1-156">I handlingsruten velger du **Alternativer**, og deretter velger du **Endringssporing**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-156">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Velge alternativet Endringssporing](media/selfref_options.png)

    4. <span data-ttu-id="5a8b1-158">Velg **Deaktiver endringssporing**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-158">Select **Disable Change Tracking**.</span></span>

        ![Velge Deaktiver endringssporing](media/selfref_tracking.png)

3. <span data-ttu-id="5a8b1-160">Kjør den innledende synkroniseringen for tilordningen **Leverandører V2 (msdyn\_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="5a8b1-161">Den innledende synkroniseringen skal kjøres uten feil.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="5a8b1-162">Kjør den innledende synkroniseringen for **CDS-kontakter V2 (kontakter)**-tilordningen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="5a8b1-163">Du må synkronisere denne tilordningen hvis du vil synkronisere den primære kontaktkolonnen i leverandørtabellen, siden innledende synkronisering også må utføres for kontaktradene.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-163">You must sync this mapping if you want to sync the primary contact column on the vendors table, because initial synchronization must also be done for the contact rows.</span></span>
5. <span data-ttu-id="5a8b1-164">Legg kolonnene **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** tilbake i tilordningen **Leverandører V2 (msdyn\_vendors)**, og lagre deretter tilordningen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="5a8b1-165">Kjør den innledende synkroniseringen igjen for tilordningen **Leverandører V2 (msdyn\_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="5a8b1-166">Siden endringssporing er deaktivert, synkroniseres alle radene.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-166">Because change tracking is turned off, all the rows will be synced.</span></span>
7. <span data-ttu-id="5a8b1-167">Aktiver sporingsendring på nytt for **Leverandører V2**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-167">Turn change tracking back on for the **Vendors V2** table.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="5a8b1-168">Utbedre feil i tabelltilordningen Kunder V3 til Kontoer</span><span class="sxs-lookup"><span data-stu-id="5a8b1-168">Resolve errors in the Customers V3–to–Accounts table mapping</span></span>

<span data-ttu-id="5a8b1-169">Det kan hende at det oppstår feil med innledende synkronisering for tilordningen **Kunder V3** til **Kontoer** hvis tabellene har eksisterende rader med verdier i kolonnene **ContactPersonID** og **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the tables have existing rows where there are values in the **ContactPersonID** and **InvoiceAccount** columns.</span></span> <span data-ttu-id="5a8b1-170">Disse feilene skjer fordi **InvoiceAccount** er en selvrefererende kolonne, og **ContactPersonID** er en sirkelreferanse i leverandørtilordningen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-170">These errors occur because **InvoiceAccount** is a self-referencing column, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="5a8b1-171">Feilmeldingene du mottar, vil ha følgende form.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="5a8b1-172">*Fant ikke GUID for feltet: \<field\>. Oppslaget ga ingen treff: \<value\>. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="5a8b1-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="5a8b1-173">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="5a8b1-173">Here are some examples:</span></span>

- <span data-ttu-id="5a8b1-174">*Fant ikke GUID for feltet: primarycontactid.msdyn\_contactpersonid. Oppslaget ga ingen treff: 000056. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="5a8b1-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="5a8b1-175">*Fant ikke GUID for feltet: msdyn\_billingaccount.accountnumber. Oppslaget ga ingen treff: 1206-1. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="5a8b1-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="5a8b1-176">Hvis noen rader i kundetabellen har verdier i kolonnene **ContactPersonID** og **InvoiceAccount**, følger du disse trinnene for å fullføre den innledende synkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-176">If any rows in the customer table have values in the **ContactPersonID** and **InvoiceAccount** columns, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="5a8b1-177">Du kan bruke denne fremgangsmåten for alle de kunderettede tabellene, for eksempel **Kontoer** og **Kontakter**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-177">You can use this approach for any out-of-box tables, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="5a8b1-178">I Finance and Operations-appen sletter du kolonnene **ContactPersonID** og **InvoiceAccount** fra tilordningen **Kunder V3 (kontoer)**, og deretter lagrer du tilordningen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** columns from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="5a8b1-179">I filteret til venstre i fanen **Tabelltilordninger** på siden for tilordning med dobbeltskriving for **Kunder V3 (kontoer)** velger du **Finance and Operations-app.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-179">On the dual-write mapping page for **Customers V3 (accounts)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="5a8b1-180">I filteret til høyre velger du **Dataverse .Account**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-180">In the right filter, select **Dataverse.Account**.</span></span>
    2. <span data-ttu-id="5a8b1-181">Søk etter **contactperson** for å finne kildekolonnen **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-181">Search for **contactperson** to find the **ContactPersonID** source column.</span></span>
    3. <span data-ttu-id="5a8b1-182">Velg **Handlinger**, og velg deretter **Slett**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-182">Select **Actions**, and then select **Delete**.</span></span>

        ![Slette kolonnen ContactPersonID](media/cust_selfref3.png)

    4. <span data-ttu-id="5a8b1-184">Gjenta disse trinnene for å slette kolonnen **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-184">Repeat these steps to delete the **InvoiceAccount** column.</span></span>

        ![Slette kolonnen InvoiceAccount](media/cust_selfref4.png)

    5. <span data-ttu-id="5a8b1-186">Lagre endringene i tilordningen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="5a8b1-187">Deaktiver sporing av endringer for **Kunder V3**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-187">Turn off change tracking for the **Customers V3** table.</span></span>

    1. <span data-ttu-id="5a8b1-188">I arbeidsområdet **Dataadministrasjon** velger du flisen **Datatabeller**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-188">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="5a8b1-189">Velg **Kunder V3**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-189">Select the **Customers V3** table.</span></span>
    3. <span data-ttu-id="5a8b1-190">I handlingsruten velger du **Alternativer**, og deretter velger du **Endringssporing**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-190">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Velge alternativet Endringssporing](media/selfref_options.png)

    4. <span data-ttu-id="5a8b1-192">Velg **Deaktiver endringssporing**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-192">Select **Disable Change Tracking**.</span></span>

        ![Velge Deaktiver endringssporing](media/selfref_tracking.png)

3. <span data-ttu-id="5a8b1-194">Kjør den innledende synkroniseringen på nytt for **Kunder V3 (Kontoer)**-tilordningen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="5a8b1-195">Den innledende synkroniseringen skal kjøres uten feil.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="5a8b1-196">Kjør den innledende synkroniseringen for **CDS-kontakter V2 (kontakter)**-tilordningen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5a8b1-197">Det er to tilordninger med samme navn.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-197">There are two maps that have the same name.</span></span> <span data-ttu-id="5a8b1-198">Sørg for å velge tilordningen med følgende beskrivelse i fanen **Detaljer**: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Krever ny pakke \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="5a8b1-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="5a8b1-199">Legg kolonnene **InvoiceAccount** og **ContactPersonId** tilbake i tilordningen **Kunder V3 (Kontoer)** igjen, og lagre deretter tilordningen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-199">Add the **InvoiceAccount** and **ContactPersonId** columns back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="5a8b1-200">Både kolonnen **InvoiceAccount** og kolonnen **ContactPersonId** er nå en del av modus for direkte synkronisering igjen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-200">Both the **InvoiceAccount** column and the **ContactPersonId** column are now part of live synchronization mode again.</span></span> <span data-ttu-id="5a8b1-201">I neste trinn skal du utføre den innledende synkroniseringen for disse kolonnene.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-201">In the next step, you will do the initial synchronization for these columns.</span></span>
6. <span data-ttu-id="5a8b1-202">Kjør den innledende synkroniseringen på nytt for **Kunder V3 (Kontoer)**-tilordningen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="5a8b1-203">Siden endringssporing er slått av, synkroniseres dataene for **InvoiceAccount** og **ContactPersonId** fra Finance and Operations-appen til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Dataverse.</span></span>
7. <span data-ttu-id="5a8b1-204">Hvis du vil synkronisere dataene for **InvoiceAccount** og **ContactPersonId** fra Dataverse til Finance and Operations-appen, må du bruke et dataintegrasjonsprosjekt.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Dataverse to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="5a8b1-205">Under Power Apps oppretter du et dataintegrasjonsprosjekt mellom **Sales.Account** og **Finance and Operations apps.Kunder V3**-tabeller.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** tables.</span></span> <span data-ttu-id="5a8b1-206">Dataretningen må være fra Dataverse til Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-206">The data direction must be from Dataverse to the Finance and Operations app.</span></span> <span data-ttu-id="5a8b1-207">Fordi **InvoiceAccount** er et nytt attributt med dobbeltskriving, kan det hende du bør hoppe over innledende synkronisering for dette attributtet.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="5a8b1-208">Hvis du vil ha mer informasjon, se [Integrere data i Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="5a8b1-208">For more information, see [Integrate data into Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="5a8b1-209">Illustrasjonen nedenfor viser et prosjekt som oppdaterer **CustomerAccount** og **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![Dataintegrasjonsprosjekt for å oppdatere CustomerAccount og ContactPersonId](media/cust_selfref6.png)

    2. <span data-ttu-id="5a8b1-211">Legg til firmakriteriene i filteret på Dataverse-siden, slik at bare radene som samsvarer med filterkriteriene, blir oppdatert i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-211">Add the company criteria in the filter on the Dataverse side, so that only rows that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="5a8b1-212">Velg filterknappen for å legge til et filter.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="5a8b1-213">Deretter, i dialogboksen **Rediger spørring**, kan du legge til en filterspørring som for eksempel **\_msdyn\_company\_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="5a8b1-214">[MERK] Hvis filterknappen ikke finnes, oppretter du en støtteforespørsel for å be dataintegreringsgruppen aktivere filterfunksjonen i leieren din.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="5a8b1-215">Hvis du ikke angir en filterspørring for **\_msdyn\_company\_value**, blir alle radene synkronisert.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-215">If you don't enter a filter query for **\_msdyn\_company\_value**, all the rows will be synced.</span></span>

        ![Legge til en filterspørring](media/cust_selfref7.png)

    <span data-ttu-id="5a8b1-217">Den innledende synkroniseringen av radene er nå fullført.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-217">The initial synchronization of the rows is now completed.</span></span>

8. <span data-ttu-id="5a8b1-218">I Finance and Operations-appen aktiverer du endringssporing på nytt for **Kunder V3**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="5a8b1-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** table.</span></span>
