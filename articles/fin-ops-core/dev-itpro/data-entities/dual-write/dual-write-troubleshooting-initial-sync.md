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
ms.openlocfilehash: 4d0ca1fb4b7a4964194516544686b6bb7d26e76c
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997332"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="b185f-103">Feilsøke problemer under første synkronisering</span><span class="sxs-lookup"><span data-stu-id="b185f-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b185f-104">Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b185f-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="b185f-105">Det inneholder informasjon som kan hjelpe deg med å løse problemer som kan oppstå under første synkronisering.</span><span class="sxs-lookup"><span data-stu-id="b185f-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b185f-106">Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator.</span><span class="sxs-lookup"><span data-stu-id="b185f-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="b185f-107">Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="b185f-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="b185f-108">Se etter innledende synkroniseringsfeil i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="b185f-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="b185f-109">Når du har aktivert tilordningsmalene, skal statusen for tilordningene være **Kjører**.</span><span class="sxs-lookup"><span data-stu-id="b185f-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="b185f-110">Hvis statusen er **Kjører ikke** , oppstod det feil under første synkronisering.</span><span class="sxs-lookup"><span data-stu-id="b185f-110">If the status is **Not running** , errors occurred during initial synchronization.</span></span> <span data-ttu-id="b185f-111">Hvis du vil vise feilene, velger du kategorien **Detaljer om innledende synkronisering** på siden **Dobbel skriving**.</span><span class="sxs-lookup"><span data-stu-id="b185f-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Feil i kategorien Detaljer om innledende synkronisering](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="b185f-113">Du kan ikke fullføre første synkronisering: 400 Ugyldig forespørsel</span><span class="sxs-lookup"><span data-stu-id="b185f-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="b185f-114">**Nødvendig rolle for å løse problemet:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="b185f-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="b185f-115">Du kan få følgende feilmelding når du prøver å kjøre tilordningen og den innledende synkroniseringen:</span><span class="sxs-lookup"><span data-stu-id="b185f-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="b185f-116">*(\[Ugyldig forespørsel\], Den eksterne serveren returnerte en feil: (400) Ugyldig forespørsel.), AX-eksporten oppdaget en feil*</span><span class="sxs-lookup"><span data-stu-id="b185f-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="b185f-117">Her er et eksempel på hele feilmeldingen.</span><span class="sxs-lookup"><span data-stu-id="b185f-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="b185f-118">Hvis denne feilen oppstår konsekvent, og du ikke kan fullføre den første synkroniseringen, følger du denne fremgangsmåten for å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="b185f-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="b185f-119">Logg på den virtuelle maskinen for Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="b185f-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="b185f-120">Åpne Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="b185f-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="b185f-121">I **Tjenester** -ruten kontrollerer du at tjenesten for rammeverk for dataimport/-eksport for Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b185f-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="b185f-122">Start den på nytt hvis den er stoppet, fordi den første synkroniseringen krever det.</span><span class="sxs-lookup"><span data-stu-id="b185f-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="b185f-123">Innledende synkroniseringsfeil: 403 forbudt</span><span class="sxs-lookup"><span data-stu-id="b185f-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="b185f-124">Du kan få følgende feilmelding under innledende synkronisering:</span><span class="sxs-lookup"><span data-stu-id="b185f-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="b185f-125">*(\[Forbudt\], Den eksterne serveren returnerte en feil: (403) Forbudt.), AX-eksporten oppdaget en feil*</span><span class="sxs-lookup"><span data-stu-id="b185f-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="b185f-126">Følg fremgangsmåten nedenfor for å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="b185f-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="b185f-127">Logg på Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="b185f-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="b185f-128">På siden **Azure Active Directory-programmer** sletter du **DtAppID** -klienten, og deretter legger du den til på nytt.</span><span class="sxs-lookup"><span data-stu-id="b185f-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![DtAppID-klient i listen over Azure AD-programmer](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="b185f-130">Egenreferanse- eller sirkelreferansefeil under innledende synkronisering</span><span class="sxs-lookup"><span data-stu-id="b185f-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="b185f-131">Du kan få feilmeldinger hvis noen av tilordningene dine har egenreferanser eller sirkelreferanser.</span><span class="sxs-lookup"><span data-stu-id="b185f-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="b185f-132">Feilene faller under følgende kategorier:</span><span class="sxs-lookup"><span data-stu-id="b185f-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="b185f-133">Feil i enhetstilordning Leverandører V2 til msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="b185f-133">Errors in the Vendors V2–to–msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="b185f-134">Feil i enhetstilordningen Kunder V3 til Kontoer</span><span class="sxs-lookup"><span data-stu-id="b185f-134">Errors in the Customers V3–to–Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="b185f-135">Løs feil i enhetstilordning Leverandører V2 til msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="b185f-135">Resolve errors in the Vendors V2–to–msdyn_vendors entity mapping</span></span>

<span data-ttu-id="b185f-136">Det kan hende du møter på feil med innledende synkronisering for tilordningen **Leverandører V2** til **msdyn\_vendors** hvis enhetene har eksisterende poster med verdier i feltene **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="b185f-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the entities have existing records where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="b185f-137">Disse feilene skjer fordi **InvoiceVendorAccountNumber** er et selvrefererende felt, og **PrimaryContactPersonId** er en sirkelreferanse i leverandørtilordningen.</span><span class="sxs-lookup"><span data-stu-id="b185f-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="b185f-138">Feilmeldingene du mottar, vil ha følgende form.</span><span class="sxs-lookup"><span data-stu-id="b185f-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="b185f-139">*Fant ikke GUID for feltet: \<field\>. Oppslaget ga ingen treff: \<value\>. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="b185f-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="b185f-140">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="b185f-140">Here are some examples:</span></span>

- <span data-ttu-id="b185f-141">*Fant ikke GUID for feltet: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Oppslaget ga ingen treff: 000056. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="b185f-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="b185f-142">*Fant ikke GUID for feltet: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Oppslaget ga ingen treff: V24-1. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="b185f-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="b185f-143">Hvis noen poster i leverandørenheten har verdier i feltene **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** , følger du disse trinnene for å fullføre den innledende synkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="b185f-143">If any records in the vendor entity have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="b185f-144">I Finance and Operations-appen sletter du **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** -feltene fra tilordningen, og deretter lagrer du endringene.</span><span class="sxs-lookup"><span data-stu-id="b185f-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="b185f-145">På siden for tilordning med dobbeltskriving for **Leverandører V2 (msdyn\_vendors)** , i kategorien **Enhetstilordninger** i filteret til venstre velger du **Finance and Operations-apper.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="b185f-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)** , on the **Entity mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="b185f-146">I filteret til høyre velger du **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="b185f-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="b185f-147">Søk etter **primarycontactperson** for å finne kildefeltet **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="b185f-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source field.</span></span>
    3. <span data-ttu-id="b185f-148">Velg **Handlinger** , og velg deretter **Slett**.</span><span class="sxs-lookup"><span data-stu-id="b185f-148">Select **Actions** , and then select **Delete**.</span></span>

        ![Slette PrimaryContactPersonId-feltet](media/vend_selfref3.png)

    4. <span data-ttu-id="b185f-150">Gjenta disse trinnene for å slette **InvoiceVendorAccountNumber** -feltet.</span><span class="sxs-lookup"><span data-stu-id="b185f-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** field.</span></span>

        ![Slette InvoiceVendorAccountNumber-feltet](media/vend-selfref4.png)

    5. <span data-ttu-id="b185f-152">Lagre endringene i tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b185f-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="b185f-153">Deaktiver sporing av endringer for **Leverandører V2** -enheten.</span><span class="sxs-lookup"><span data-stu-id="b185f-153">Turn off change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="b185f-154">I **Dataadministrasjon** -arbeidsområdet velger du flisen **Dataenheter**.</span><span class="sxs-lookup"><span data-stu-id="b185f-154">In the **Data management** workspace, select the **Data entities** tile.</span></span>
    2. <span data-ttu-id="b185f-155">Velg **Leverandører V2** -enheten.</span><span class="sxs-lookup"><span data-stu-id="b185f-155">Select the **Vendors V2** entity.</span></span>
    3. <span data-ttu-id="b185f-156">I handlingsruten velger du **Alternativer** , og deretter velger du **Endringssporing**.</span><span class="sxs-lookup"><span data-stu-id="b185f-156">On the Action Pane, select **Options** , and then select **Change tracking**.</span></span>

        ![Velge alternativet Endringssporing](media/selfref_options.png)

    4. <span data-ttu-id="b185f-158">Velg **Deaktiver endringssporing**.</span><span class="sxs-lookup"><span data-stu-id="b185f-158">Select **Disable Change Tracking**.</span></span>

        ![Velge Deaktiver endringssporing](media/selfref_tracking.png)

3. <span data-ttu-id="b185f-160">Kjør den innledende synkroniseringen for tilordningen **Leverandører V2 (msdyn\_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="b185f-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="b185f-161">Den innledende synkroniseringen skal kjøres uten feil.</span><span class="sxs-lookup"><span data-stu-id="b185f-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="b185f-162">Kjør den innledende synkroniseringen for **CDS-kontakter V2 (kontakter)** -tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b185f-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="b185f-163">Du må synkronisere denne tilordningen hvis du vil synkronisere det primære kontaktfeltet på leverandørenheten, ettersom innledende synkronisering også må utføres for kontaktpostene.</span><span class="sxs-lookup"><span data-stu-id="b185f-163">You must sync this mapping if you want to sync the primary contact field on the vendors entity, because initial synchronization must also be done for the contact records.</span></span>
5. <span data-ttu-id="b185f-164">Legg til feltene **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** tilbake i **Leverandører V2 (msdyn\_vendors)** -tilordningen, og lagre deretter tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b185f-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="b185f-165">Kjør den innledende synkroniseringen igjen for tilordningen **Leverandører V2 (msdyn\_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="b185f-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="b185f-166">Siden endringssporing er slått av, synkroniseres alle postene.</span><span class="sxs-lookup"><span data-stu-id="b185f-166">Because change tracking is turned off, all the records will be synced.</span></span>
7. <span data-ttu-id="b185f-167">Slå sporingsendring på igjen for **Leverandører V2** -enheten.</span><span class="sxs-lookup"><span data-stu-id="b185f-167">Turn change tracking back on for the **Vendors V2** entity.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="b185f-168">Utbedre feil i enhetstilordningen Kunder V3 til Kontoer</span><span class="sxs-lookup"><span data-stu-id="b185f-168">Resolve errors in the Customers V3–to–Accounts entity mapping</span></span>

<span data-ttu-id="b185f-169">Det kan hende du møter på feil med innledende synkronisering for tilordningen **Kunder V3** til **Kontoer** hvis enhetene har eksisterende poster med verdier i feltene **ContactPersonID** og **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="b185f-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the entities have existing records where there are values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="b185f-170">Disse feilene skjer fordi **InvoiceAccount** er et selvrefererende felt, og **ContactPersonID** er en sirkelreferanse i leverandørtilordningen.</span><span class="sxs-lookup"><span data-stu-id="b185f-170">These errors occur because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="b185f-171">Feilmeldingene du mottar, vil ha følgende form.</span><span class="sxs-lookup"><span data-stu-id="b185f-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="b185f-172">*Fant ikke GUID for feltet: \<field\>. Oppslaget ga ingen treff: \<value\>. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="b185f-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="b185f-173">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="b185f-173">Here are some examples:</span></span>

- <span data-ttu-id="b185f-174">*Fant ikke GUID for feltet: primarycontactid.msdyn\_contactpersonid. Oppslaget ga ingen treff: 000056. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="b185f-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="b185f-175">*Fant ikke GUID for feltet: msdyn\_billingaccount.accountnumber. Oppslaget ga ingen treff: 1206-1. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="b185f-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="b185f-176">Hvis noen poster i kundeenheten har verdier i feltene **ContactPersonID** og **InvoiceAccount** , følger du disse trinnene for å fullføre den innledende synkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="b185f-176">If any records in the customer entity have values in the **ContactPersonID** and **InvoiceAccount** fields, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="b185f-177">Du kan bruke denne fremgangsmåten for alle de kunderettede enhetene, for eksempel **Kontoer** og **Kontakter**.</span><span class="sxs-lookup"><span data-stu-id="b185f-177">You can use this approach for any out-of-box entities, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="b185f-178">I Finance and Operations-appen sletter du feltene **ContactPersonID** og **InvoiceAccount** fra **Kunder V3 (kontoer)** -tilordningen, og deretter lagrer du tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b185f-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** fields from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="b185f-179">På siden for tilordning med dobbeltskriving for **Kunder V3 (Kontoer)** , i kategorien **Enhetstilordninger** -fanen, i filteret til venstre, velger du **Finance and Operations-app.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="b185f-179">On the dual-write mapping page for **Customers V3 (accounts)** , on the **Entity mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="b185f-180">I filteret til høyre velger du **Common Data Service .Account**.</span><span class="sxs-lookup"><span data-stu-id="b185f-180">In the right filter, select **Common Data Service.Account**.</span></span>
    2. <span data-ttu-id="b185f-181">Søk etter **contactperson** for å finne kildefeltet **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="b185f-181">Search for **contactperson** to find the **ContactPersonID** source field.</span></span>
    3. <span data-ttu-id="b185f-182">Velg **Handlinger** , og velg deretter **Slett**.</span><span class="sxs-lookup"><span data-stu-id="b185f-182">Select **Actions** , and then select **Delete**.</span></span>

        ![Slette ContactPersonID-feltet](media/cust_selfref3.png)

    4. <span data-ttu-id="b185f-184">Gjenta disse trinnene for å slette feltet **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="b185f-184">Repeat these steps to delete the **InvoiceAccount** field.</span></span>

        ![Slette InvoiceAccount-feltet](media/cust_selfref4.png)

    5. <span data-ttu-id="b185f-186">Lagre endringene i tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b185f-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="b185f-187">Deaktiver sporing av endringer for **Kunder V3** -enheten.</span><span class="sxs-lookup"><span data-stu-id="b185f-187">Turn off change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="b185f-188">I **Dataadministrasjon** -arbeidsområdet velger du flisen **Dataenheter**.</span><span class="sxs-lookup"><span data-stu-id="b185f-188">In the **Data management** workspace, select the **Data entities** tile.</span></span>
    2. <span data-ttu-id="b185f-189">Velg **Kunder V3** -enheten.</span><span class="sxs-lookup"><span data-stu-id="b185f-189">Select the **Customers V3** entity.</span></span>
    3. <span data-ttu-id="b185f-190">I handlingsruten velger du **Alternativer** , og deretter velger du **Endringssporing**.</span><span class="sxs-lookup"><span data-stu-id="b185f-190">On the Action Pane, select **Options** , and then select **Change tracking**.</span></span>

        ![Velge alternativet Endringssporing](media/selfref_options.png)

    4. <span data-ttu-id="b185f-192">Velg **Deaktiver endringssporing**.</span><span class="sxs-lookup"><span data-stu-id="b185f-192">Select **Disable Change Tracking**.</span></span>

        ![Velge Deaktiver endringssporing](media/selfref_tracking.png)

3. <span data-ttu-id="b185f-194">Kjør den innledende synkroniseringen på nytt for **Kunder V3 (Kontoer)** -tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b185f-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="b185f-195">Den innledende synkroniseringen skal kjøres uten feil.</span><span class="sxs-lookup"><span data-stu-id="b185f-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="b185f-196">Kjør den innledende synkroniseringen for **CDS-kontakter V2 (kontakter)** -tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b185f-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b185f-197">Det er to tilordninger med samme navn.</span><span class="sxs-lookup"><span data-stu-id="b185f-197">There are two maps that have the same name.</span></span> <span data-ttu-id="b185f-198">Sørg for å velge tilordningen med følgende beskrivelse i fanen **Detaljer** : **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Krever ny pakke \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="b185f-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="b185f-199">Legg til feltene **InvoiceAccount** og **ContactPersonId** i **Kunder V3 (Kontoer)** -tilordningen igjen, og lagre deretter tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b185f-199">Add the **InvoiceAccount** and **ContactPersonId** fields back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="b185f-200">Både **InvoiceAccount** - og **ContactPersonId** -feltene er nå en del av modus for direkte synkronisering igjen.</span><span class="sxs-lookup"><span data-stu-id="b185f-200">Both the **InvoiceAccount** field and the **ContactPersonId** field are now part of live synchronization mode again.</span></span> <span data-ttu-id="b185f-201">I neste trinn skal du utføre den innledende synkroniseringen for disse feltene.</span><span class="sxs-lookup"><span data-stu-id="b185f-201">In the next step, you will do the initial synchronization for these fields.</span></span>
6. <span data-ttu-id="b185f-202">Kjør den innledende synkroniseringen på nytt for **Kunder V3 (Kontoer)** -tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b185f-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="b185f-203">Siden endringssporing er slått av, synkroniseres dataene for **InvoiceAccount** og **ContactPersonId** fra Finance and Operations-appen til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b185f-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Common Data Service.</span></span>
7. <span data-ttu-id="b185f-204">Hvis du vil synkronisere dataene for **InvoiceAccount** og **ContactPersonId** fra Common Data Service til Finance and Operations-appen, må du bruke et dataintegrasjonsprosjekt.</span><span class="sxs-lookup"><span data-stu-id="b185f-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="b185f-205">Under Power Apps oppretter du et dataintegrasjonsprosjekt mellom **Sales.Account** og **Finance and Operations apps.Kunder V3** -enheter.</span><span class="sxs-lookup"><span data-stu-id="b185f-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="b185f-206">Dataretningen må være fra Common Data Service til Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="b185f-206">The data direction must be from Common Data Service to the Finance and Operations app.</span></span> <span data-ttu-id="b185f-207">Fordi **InvoiceAccount** er et nytt attributt med dobbeltskriving, kan det hende du bør hoppe over innledende synkronisering for dette attributtet.</span><span class="sxs-lookup"><span data-stu-id="b185f-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="b185f-208">Hvis du vil ha mer informasjon, se [Integrere data i Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="b185f-208">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="b185f-209">Illustrasjonen nedenfor viser et prosjekt som oppdaterer **CustomerAccount** og **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="b185f-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![Dataintegrasjonsprosjekt for å oppdatere CustomerAccount og ContactPersonId](media/cust_selfref6.png)

    2. <span data-ttu-id="b185f-211">Legg til firmakriteriene i filteret på Common Data Service-siden, slik at bare postene som samsvarer med filterkriteriene, blir oppdatert i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="b185f-211">Add the company criteria in the filter on the Common Data Service side, so that only records that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="b185f-212">Velg filterknappen for å legge til et filter.</span><span class="sxs-lookup"><span data-stu-id="b185f-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="b185f-213">Deretter, i dialogboksen **Rediger spørring** , kan du legge til en filterspørring som for eksempel **\_msdyn\_company\_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="b185f-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="b185f-214">[MERK] Hvis filterknappen ikke finnes, oppretter du en støtteforespørsel for å be dataintegreringsgruppen aktivere filterfunksjonen i leieren din.</span><span class="sxs-lookup"><span data-stu-id="b185f-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="b185f-215">Hvis du ikke angir en filterspørring for **\_msdyn\_company\_value** , blir alle postene synkronisert.</span><span class="sxs-lookup"><span data-stu-id="b185f-215">If you don't enter a filter query for **\_msdyn\_company\_value** , all the records will be synced.</span></span>

        ![Legge til en filterspørring](media/cust_selfref7.png)

    <span data-ttu-id="b185f-217">Den innledende synkroniseringen av oppføringene er nå fullført.</span><span class="sxs-lookup"><span data-stu-id="b185f-217">The initial synchronization of the records is now completed.</span></span>

8. <span data-ttu-id="b185f-218">I Finance and Operations-appen aktiverer du endringssporing igjen for **Kunder V3** -enheten.</span><span class="sxs-lookup"><span data-stu-id="b185f-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** entity.</span></span>
