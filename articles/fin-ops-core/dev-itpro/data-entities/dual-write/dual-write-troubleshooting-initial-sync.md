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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410087"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="b51b0-103">Feilsøke problemer under første synkronisering</span><span class="sxs-lookup"><span data-stu-id="b51b0-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b51b0-104">Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b51b0-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="b51b0-105">Det inneholder informasjon som kan hjelpe deg med å løse problemer som kan oppstå under første synkronisering.</span><span class="sxs-lookup"><span data-stu-id="b51b0-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b51b0-106">Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator.</span><span class="sxs-lookup"><span data-stu-id="b51b0-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="b51b0-107">Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="b51b0-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="b51b0-108">Se etter innledende synkroniseringsfeil i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="b51b0-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="b51b0-109">Når du har aktivert tilordningsmalene, skal statusen for tilordningene være **Kjører**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="b51b0-110">Hvis statusen er **Kjører ikke**, oppstod det feil under første synkronisering.</span><span class="sxs-lookup"><span data-stu-id="b51b0-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="b51b0-111">Hvis du vil vise feilene, velger du kategorien **Detaljer om innledende synkronisering** på siden **Dobbel skriving**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Kategorien Detaljer om innledende synkronisering](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="b51b0-113">Du kan ikke fullføre første synkronisering: 400 Ugyldig forespørsel</span><span class="sxs-lookup"><span data-stu-id="b51b0-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="b51b0-114">**Nødvendig rolle for å løse problemet:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="b51b0-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="b51b0-115">Du kan få følgende feilmelding når du prøver å kjøre tilordningen og den innledende synkroniseringen:</span><span class="sxs-lookup"><span data-stu-id="b51b0-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="b51b0-116">*Den eksterne serveren returnerte en feil: (400) Ugyldig forespørsel.), AX-eksporten oppdaget en feil*</span><span class="sxs-lookup"><span data-stu-id="b51b0-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="b51b0-117">Her er et eksempel på hele feilmeldingen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="b51b0-118">Hvis denne feilen oppstår konsekvent, og du ikke kan fullføre den første synkroniseringen, følger du denne fremgangsmåten for å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="b51b0-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="b51b0-119">Logg på den virtuelle maskinen for Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="b51b0-120">Åpne Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="b51b0-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="b51b0-121">I **Tjenester**-ruten kontrollerer du at tjenesten for rammeverk for dataimport/-eksport for Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b51b0-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="b51b0-122">Start den på nytt hvis den er stoppet, fordi den første synkroniseringen krever det.</span><span class="sxs-lookup"><span data-stu-id="b51b0-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="b51b0-123">Innledende synkroniseringsfeil: 403 forbudt</span><span class="sxs-lookup"><span data-stu-id="b51b0-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="b51b0-124">Du kan få følgende feilmelding under innledende synkronisering:</span><span class="sxs-lookup"><span data-stu-id="b51b0-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="b51b0-125">*(\[Forbudt\], Den eksterne serveren returnerte en feil: (403) Forbudt.), AX-eksporten oppdaget en feil*</span><span class="sxs-lookup"><span data-stu-id="b51b0-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="b51b0-126">Følg fremgangsmåten nedenfor for å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="b51b0-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="b51b0-127">Logg på Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="b51b0-128">På siden **Azure Active Directory-programmer** sletter du **DtAppID**-klienten, og deretter legger du den til på nytt.</span><span class="sxs-lookup"><span data-stu-id="b51b0-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Liste over Azure AD-programmer](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="b51b0-130">Egenreferanse- eller sirkelreferansefeil under innledende synkronisering</span><span class="sxs-lookup"><span data-stu-id="b51b0-130">Self-reference or circular-reference failures during initial synchronization</span></span>

<span data-ttu-id="b51b0-131">Du kan få feilmeldinger hvis noen av tilordningene dine har egenreferanser eller sirkelreferanser.</span><span class="sxs-lookup"><span data-stu-id="b51b0-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="b51b0-132">Feilene faller under følgende kategorier:</span><span class="sxs-lookup"><span data-stu-id="b51b0-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="b51b0-133">Leverandører V2 til msdyn_vendors-enhetstilordning</span><span class="sxs-lookup"><span data-stu-id="b51b0-133">Vendors V2 to msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="b51b0-134">Kunder V3 til Kontoer-enhetstilordning</span><span class="sxs-lookup"><span data-stu-id="b51b0-134">Customers V3 to Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="b51b0-135">Utbedre en feil i enhetstilordning fra Leverandører V2 til msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="b51b0-135">Resolve an error in Vendors V2 to msdyn_vendors entity mapping</span></span>

<span data-ttu-id="b51b0-136">Det kan hende du møter på følgende feil med innledende synkronisering i tilordningen **Leverandører V2** til **msdyn_vendors** hvis enhetene har eksisterende poster med verdier i feltene **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-136">You might run into the following initial sync errors on the **Vendors V2** to **msdyn_vendors** mapping if the entities have existing records with values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="b51b0-137">Dette fordi **InvoiceVendorAccountNumber** er et selvrefererende felt, og **PrimaryContactPersonId** er en sirkelreferanse i leverandørtilordningen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-137">This because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="b51b0-138">*Fant ikke GUID for feltet: <field>. Oppslaget ga ingen treff: <value>. Prøv disse URL-ene for å kontrollere at referansedataene finnes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="b51b0-138">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

<span data-ttu-id="b51b0-139">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="b51b0-139">Here are a couple of examples:</span></span>

- <span data-ttu-id="b51b0-140">*Finner ikke GUID for feltet: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Fant ikke oppslaget: 000056. Prøv denne URL-adressen for å kontrollere om referansedataene finnes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$Select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="b51b0-140">*Couldn't resolve the guid for the field: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="b51b0-141">*Finner ikke GUID for feltet: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Fant ikke oppslaget: V24-1. Prøv denne URL-adressen for å kontrollere om referansedataene finnes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span><span class="sxs-lookup"><span data-stu-id="b51b0-141">*Couldn't resolve the guid for the field: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span></span>

<span data-ttu-id="b51b0-142">Hvis du har poster med verdier i disse feltene i leverandørenheten, følger du trinnene i delen nedenfor for å fullføre den innledende synkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-142">If you have records with values in these fields in the vendor entity follow the steps in the below section to complete initial sync successfully.</span></span>

1. <span data-ttu-id="b51b0-143">I Finance and Operations-appen sletter du **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**-feltene fra tilordningen, og lagrer endringene.</span><span class="sxs-lookup"><span data-stu-id="b51b0-143">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping and save the changes.</span></span>

    1. <span data-ttu-id="b51b0-144">Gå til siden for tilordning med dobbeltskriving for **Leverandører V2 (msdyn_vendors)**, og velg **Enhetstilordninger**-fanen. I filteret til venstre velger du **Finance and Operations apps.Leverandører V2**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-144">Navigate to the dual-write mapping page for **Vendors V2 (msdyn_vendors)**, and select the **Entity mappings** tab. In the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="b51b0-145">I filteret til høyre velger du **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-145">In the right filter, select **Sales.Vendor**.</span></span>

    2. <span data-ttu-id="b51b0-146">Søk etter **primarycontactperson** for å finne kildefeltet **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-146">Search for **primarycontactperson** to find the source field **PrimaryContactPersonId**.</span></span>
    
    3. <span data-ttu-id="b51b0-147">Klikk på **Handlinger**-knappen, og velg **Slett**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-147">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![egen- eller sirkelreferanse 3](media/vend_selfref3.png)
    
    4. <span data-ttu-id="b51b0-149">Gjenta prosessen for å slette **InvoiceVendorAccountNumber**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b51b0-149">Repeat to delete the **InvoiceVendorAccountNumber** field.</span></span>
    
        ![egen- eller sirkelreferanse 4](media/vend-selfref4.png)
    
    5. <span data-ttu-id="b51b0-151">Lagre tilordningsendringene.</span><span class="sxs-lookup"><span data-stu-id="b51b0-151">Save the mapping changes.</span></span>

2. <span data-ttu-id="b51b0-152">Deaktiver sporing av endringer for **Leverandører V2**-enheten.</span><span class="sxs-lookup"><span data-stu-id="b51b0-152">Disable the change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="b51b0-153">Gå til **Datastyring \> Dataenheter**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-153">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="b51b0-154">Velg **Leverandører V2**-enheten.</span><span class="sxs-lookup"><span data-stu-id="b51b0-154">Select the **Vendors V2** entity.</span></span>
    
    3. <span data-ttu-id="b51b0-155">Klikk på **Alternativer** på menylinjen, og deretter **Endringssporing**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-155">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![egen- eller sirkelreferanse 5](media/selfref_options.png)
    
    4. <span data-ttu-id="b51b0-157">Klikk på **Deaktiver endringssporing**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-157">Click **Disable Change Tracking**.</span></span>
    
        ![egen- eller sirkelreferanse 6](media/selfref_tracking.png)

3. <span data-ttu-id="b51b0-159">Kjør den innledende synkroniseringen av **Leverandører V2 (msdyn_vendors)**-tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-159">Run the initial sync of **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="b51b0-160">Den innledende synkroniseringen skal kjøres uten feil.</span><span class="sxs-lookup"><span data-stu-id="b51b0-160">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="b51b0-161">Kjør den innledende synkroniseringen for **CDS-kontakter V2 (kontakter)**-tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-161">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="b51b0-162">Du må synkronisere denne tilordningen hvis du vil synkronisere det primære kontaktfeltet på leverandørenheten, ettersom kontaktpostene også må gjennomgå innledende synkronisering.</span><span class="sxs-lookup"><span data-stu-id="b51b0-162">You must sync this mapping if you want to sync primary contact field on vendors entity as the contacts records also need to be initial synced.</span></span>

5. <span data-ttu-id="b51b0-163">Legg til feltene **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** tilbake i **Leverandører V2 (msdyn_vendors)**-tilordningen, og lagre tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-163">Add the fields **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** back to the **Vendors V2 (msdyn_vendors)** mapping and save the mapping.</span></span>

6. <span data-ttu-id="b51b0-164">Kjør den innledende synkroniseringen på nytt for **Leverandører V2 (msdyn_vendors)**-tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-164">Run the initial sync again for the **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="b51b0-165">Alle postene synkroniseres, fordi endringssporing er deaktivert.</span><span class="sxs-lookup"><span data-stu-id="b51b0-165">All the records will be synced, because change tracking is disabled.</span></span>

7. <span data-ttu-id="b51b0-166">Aktiver sporing av endringer for **Leverandører V2**-enheten.</span><span class="sxs-lookup"><span data-stu-id="b51b0-166">Enable change tracking for the **Vendors V2** entity.</span></span>

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="b51b0-167">Utbedre en feil i enhetstilordningen Kunder V3 til Kontoer</span><span class="sxs-lookup"><span data-stu-id="b51b0-167">Resolve an error in Customers V3 to Accounts entity mapping</span></span>

<span data-ttu-id="b51b0-168">Det kan hende du møter på følgende feil med innledende synkronisering i tilordningen **Kunder V3** til **Kontoer** hvis enhetene har eksisterende poster med verdier i feltene **ContactPersonID** og **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-168">You might run into the following initial sync errors on the **Customers V3** to **Accounts** mapping if the entities have existing records with values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="b51b0-169">Dette fordi **InvoiceAccount** er et selvrefererende felt, og **ContactPersonID** er en sirkelreferanse i leverandørtilordningen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-169">This because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="b51b0-170">*Fant ikke GUID for feltet: <field>. Oppslaget ga ingen treff: <value>. Prøv disse URL-ene for å kontrollere at referansedataene finnes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="b51b0-170">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

- <span data-ttu-id="b51b0-171">*Finner ikke GUID for feltet: primarycontactid.msdyn_contactpersonid. Fant ikke oppslaget: 000056. Prøv denne URL-adressen for å kontrollere om referansedataene finnes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$Select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="b51b0-171">*Couldn't resolve the guid for the field: primarycontactid.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="b51b0-172">*Finner ikke GUID for feltet: msdyn_billingaccount.accountnumber. Fant ikke oppslaget: 1206-1. Prøv denne URL-adressen for å kontrollere om referansedataene finnes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span><span class="sxs-lookup"><span data-stu-id="b51b0-172">*Couldn't resolve the guid for the field: msdyn_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span></span>

<span data-ttu-id="b51b0-173">Hvis du har poster med verdier i disse feltene i kundeenheten, følger du trinnene i delen nedenfor for å fullføre den innledende synkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-173">If you have records with values in these fields in the customer entity follow the steps in the below section to complete initial sync successfully.</span></span> <span data-ttu-id="b51b0-174">Du kan bruke denne fremgangsmåten for alle de kunderettede enhetene, for eksempel Kontoer og Contacts.</span><span class="sxs-lookup"><span data-stu-id="b51b0-174">You can use this approach for any out-of-the-box entities such Accounts and Contacts.</span></span>

1. <span data-ttu-id="b51b0-175">I Finance and Operations-appen sletter du feltene **ContactPersonID** og **InvoiceAccount** fra **Kunder V3 (kontoer)**-tilordningen, og lagrer tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-175">In the Finance and Operations app, delete the fields **ContactPersonID** and **InvoiceAccount** from the **Customers V3 (accounts)** mapping and save the mapping.</span></span>

    1. <span data-ttu-id="b51b0-176">Gå til siden for tilordning med dobbeltskriving for **Kunder V3 (Kontoer)**, og velg **Enhetstilordninger**-fanen. I filteret til venstre velger du **Finance and Operations app.Kunder V3**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-176">Navigate to the dual-write mapping page for **Customers V3 (accounts)**, select the **Entity mappings** tab. In the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="b51b0-177">I filteret til høyre velger du **Common Data Service .Account**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-177">In the right filter, select **Common Data Service.Account**.</span></span>

    2. <span data-ttu-id="b51b0-178">Søk etter **contactperson** for å finne kildefeltet **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-178">Search for **contactperson** to find the source field **ContactPersonID**.</span></span>
    
    3. <span data-ttu-id="b51b0-179">Klikk på **Handlinger**-knappen, og velg **Slett**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-179">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![egen- eller sirkelreferanse 3](media/cust_selfref3.png)
    
    4. <span data-ttu-id="b51b0-181">Gjenta prosessen for å slette **InvoiceAccount**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b51b0-181">Repeat to delete the **InvoiceAccount** field.</span></span>
    
        ![egen- eller sirkelreferanse](media/cust_selfref4.png)
    
    5. <span data-ttu-id="b51b0-183">Lagre tilordningsendringene.</span><span class="sxs-lookup"><span data-stu-id="b51b0-183">Save the mapping changes.</span></span>

2. <span data-ttu-id="b51b0-184">Deaktiver sporing av endringer for **Kunder V3**-enheten.</span><span class="sxs-lookup"><span data-stu-id="b51b0-184">Disable the change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="b51b0-185">Gå til **Datastyring \> Dataenheter**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-185">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="b51b0-186">Velg **Kunder V3**-enheten.</span><span class="sxs-lookup"><span data-stu-id="b51b0-186">Select the **Customers V3** entity.</span></span>
    
    3. <span data-ttu-id="b51b0-187">Klikk på **Alternativer** på menylinjen, og deretter **Endringssporing**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-187">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![egen- eller sirkelreferanse 5](media/selfref_options.png)
    
    4. <span data-ttu-id="b51b0-189">Klikk på **Deaktiver endringssporing**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-189">Click **Disable Change Tracking**.</span></span>
    
        ![egen- eller sirkelreferanse 6](media/selfref_tracking.png)

3. <span data-ttu-id="b51b0-191">Kjør den innledende synkroniseringen for **Kunder V3 (Kontoer)**-tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-191">Run the initial sync for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="b51b0-192">Den innledende synkroniseringen skal kjøres uten feil.</span><span class="sxs-lookup"><span data-stu-id="b51b0-192">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="b51b0-193">Kjør den innledende synkroniseringen for **CDS-kontakter V2 (kontakter)**-tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-193">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="b51b0-194">Det finnes to tilordninger med samme navn.</span><span class="sxs-lookup"><span data-stu-id="b51b0-194">There are 2 maps with the same name.</span></span> <span data-ttu-id="b51b0-195">Velg den som har beskrivelsen **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="b51b0-195">Select the one with the description **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span> <span data-ttu-id="b51b0-196">i **Detaljer**-kategorien for tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-196">on the **Details** tab of the map.</span></span>

5. <span data-ttu-id="b51b0-197">Legg til feltene **InvoiceAccount** og **ContactPersonId** i **Kunder V3 (Kontoer)** -tilordningen igjen, og lagre tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-197">Add the fields **InvoiceAccount** and **ContactPersonId** back to the **Customers V3 (Accounts)** mapping and save the mapping.</span></span> <span data-ttu-id="b51b0-198">Nå er både **InvoiceAccount**- og **ContactPersonId**-feltene igjen en del av Live Sync-modusen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-198">Now, both the **InvoiceAccount** field and the **ContactPersonId** field are again part of live sync mode.</span></span> <span data-ttu-id="b51b0-199">I neste trinn fullfører du den innledende synkroniseringen for disse feltene.</span><span class="sxs-lookup"><span data-stu-id="b51b0-199">In the next step, you complete the initial sync for these fields.</span></span>

6. <span data-ttu-id="b51b0-200">Kjør den innledende synkroniseringen på nytt for **Kunder V3 (Kontoer)**-tilordningen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-200">Run the initial sync again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="b51b0-201">Siden endringssporing er deaktivert, synkroniseres dataene for **InvoiceAccount** og **ContactPersonId** fra Finance and Operations-appen til Common Data Service hvis du kjører synkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-201">Because change tracking is disabled, running the sync will sync the data for **InvoiceAccount** and **ContactPersonId** from the Finance and Operations app to Common Data Service.</span></span>

7. <span data-ttu-id="b51b0-202">Hvis du vil synkronisere dataene for **InvoiceAccount** og **ContactPersonId** fra Common Data Service til Finance and Operations, bruker du et dataintegrasjonsprosjekt.</span><span class="sxs-lookup"><span data-stu-id="b51b0-202">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations, you use a data integration project.</span></span>

    1. <span data-ttu-id="b51b0-203">Under Power Apps oppretter du et dataintegrasjonsprosjekt mellom **Sales.Account** og **Finance and Operations apps.Kunder V3**-enheter.</span><span class="sxs-lookup"><span data-stu-id="b51b0-203">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="b51b0-204">Dataretningen må være fra Common Data Service til Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-204">The data direction must be from Common Data Service to the Finance and Operations app.</span></span>  <span data-ttu-id="b51b0-205">Fordi **InvoiceAccount** er et nytt attributt med dobbeltskriving, kan det hende du bør hoppe over innledende synkronisering for dette attributtet.</span><span class="sxs-lookup"><span data-stu-id="b51b0-205">Because **InvoiceAccount** is a new attribute in dual-write, you may want to skip initial sync for this attribute.</span></span> <span data-ttu-id="b51b0-206">Hvis du vil ha mer informasjon, se [Integrere data i Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="b51b0-206">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="b51b0-207">Bildet nedenfor viser et prosjekt som oppdaterer **CustomerAccount** og **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-207">The following image shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![egen- eller sirkelreferanse](media/cust_selfref6.png)

    2. <span data-ttu-id="b51b0-209">Legg til firmakriteriene i filteret på Common Data Service-siden, ettersom bare postene som samsvarer med filterkriteriene, blir oppdatert i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-209">Add the company criteria in the filter on Common Data Service side, because only the records that match filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="b51b0-210">Klikk på filterikonet for å legge til et filter.</span><span class="sxs-lookup"><span data-stu-id="b51b0-210">To add a filter, click the filter icon.</span></span> <span data-ttu-id="b51b0-211">I **Rediger spørring**-dialogen kan du legge til en filterspørring som for eksempel **_msdyn_company_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="b51b0-211">In the **Edit query** dialog, you can add a filter query like **_msdyn_company_value eq '\<guid\>'**.</span></span> <span data-ttu-id="b51b0-212">Hvis filterikonet ikke finnes, oppretter du en støtteforespørsel for å be dataintegreringsgruppen aktivere filterfunksjonen i leieren din.</span><span class="sxs-lookup"><span data-stu-id="b51b0-212">If the filter icon is not present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span> <span data-ttu-id="b51b0-213">Hvis du ikke angir en filterspørring for **_msdyn_company_value**, blir alle postene synkronisert.</span><span class="sxs-lookup"><span data-stu-id="b51b0-213">If you do not enter a filter query for **_msdyn_company_value**, then all the records are synced.</span></span>

        ![egen- eller sirkelreferanse](media/cust_selfref7.png)

        <span data-ttu-id="b51b0-215">Dette fullfører den første synkroniseringen av postene.</span><span class="sxs-lookup"><span data-stu-id="b51b0-215">This completes the initial sync of the records.</span></span>

8. <span data-ttu-id="b51b0-216">Aktiver sporing av endringer for **Kunder V3**-enheten i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="b51b0-216">Enable change tracking for the **Customers V3** entity in the Finance and Operations app.</span></span>

