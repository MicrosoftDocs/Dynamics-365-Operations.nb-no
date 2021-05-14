---
title: Oppgrader til parten og den globale adressebokmodellen
description: Dette emnet beskriver hvordan du oppgraderer data for dobbel skriving til partsmodellen og den globale adressebokmodellen.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 32128d48bfac195530d70b60e67cfd4921fc001e
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941089"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="445df-103">Oppgrader til parten og den globale adressebokmodellen</span><span class="sxs-lookup"><span data-stu-id="445df-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="445df-104">Med [Azure Data Factory-malen](https://aka.ms/dual-write-gab-adf) kan du oppgradere eksisterende **Konto**, **Kontakt** og **Leverandør**-tabelldata i dobbel skriving til partsmodellen og den globale adressebokmodellen.</span><span class="sxs-lookup"><span data-stu-id="445df-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="445df-105">Malen avstemmer dataene fra både Finance and Operations-apper og Customer Engagement-programmer.</span><span class="sxs-lookup"><span data-stu-id="445df-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="445df-106">På slutten av prosessen vil **Part**- og **Kontakt**-felter for **Part**-oppføringer opprettes og knyttes til **Konto**, **Kontakt** og **Leverandør**-oppføringer i Customer Engagement-programmer.</span><span class="sxs-lookup"><span data-stu-id="445df-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="445df-107">En .csv-fil (`FONewParty.csv`) genereres for å opprette nye **Part**-oppføringer i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="445df-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="445df-108">I dette emnet finner du instruksjoner om hvordan du kan bruke Data Factory-malen og oppgradere dataene.</span><span class="sxs-lookup"><span data-stu-id="445df-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="445df-109">Hvis du ikke har noen tilpasninger, kan du bruke malen som den er.</span><span class="sxs-lookup"><span data-stu-id="445df-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="445df-110">Hvis du har tilpasninger for **Konto**, **Kontakt** og **Leverandør**, må du endre malen ved å følge instruksjonene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="445df-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="445df-111">Malen gjør det enklere å oppgradere bare **Part**-dataene.</span><span class="sxs-lookup"><span data-stu-id="445df-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="445df-112">I en fremtidig versjon blir postadresser og elektroniske adresser inkludert.</span><span class="sxs-lookup"><span data-stu-id="445df-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="445df-113">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="445df-113">Prerequisites</span></span>

<span data-ttu-id="445df-114">Disse forutsetningene kreves:</span><span class="sxs-lookup"><span data-stu-id="445df-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="445df-115">Azure-abonnement</span><span class="sxs-lookup"><span data-stu-id="445df-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="445df-116">Tilgang til malen</span><span class="sxs-lookup"><span data-stu-id="445df-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="445df-117">Du er en eksisterende kunde med dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="445df-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="445df-118">Forberede for oppgraderingen</span><span class="sxs-lookup"><span data-stu-id="445df-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="445df-119">**Fullstendig synkronisert**: Begge miljøene er fullstending synkronisert for **Konto (kunde)**, **Kontakt** og **Leverandør**.</span><span class="sxs-lookup"><span data-stu-id="445df-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="445df-120">**Integrasjonsnøkler**: Tabellene **Konto (kunde)**, **Kontakt** og **Leverandør** i Customer Engagement-apper bruker de medfølgende integrasjonsnøklene.</span><span class="sxs-lookup"><span data-stu-id="445df-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="445df-121">Hvis du har tilpasset integrasjonsnøklene, må du tilpasse malen.</span><span class="sxs-lookup"><span data-stu-id="445df-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="445df-122">**Partsnummer**: Alle oppføringer av typen **Konto (kunde)**, **Kontakt** og **Leverandør** som skal oppgraderes, har et **partsnummer**.</span><span class="sxs-lookup"><span data-stu-id="445df-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="445df-123">Oppføringer uten et **partsnummer** blir ignorert.</span><span class="sxs-lookup"><span data-stu-id="445df-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="445df-124">Hvis du vil oppgradere disse oppføringer, legger du til et **partsnummer** før du starter oppgraderingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="445df-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="445df-125">**Systembrudd**: Under oppgraderingsprosessen må du koble fra både Finance and Operations- og Customer Engagement-miljøer.</span><span class="sxs-lookup"><span data-stu-id="445df-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="445df-126">**Øyeblikksbilde**: Ta øyeblikksbilder både av Finance and Operations- og Customer Engagement-appene.</span><span class="sxs-lookup"><span data-stu-id="445df-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="445df-127">Bruk øyeblikksbildene til å gjenopprette den forrige tilstanden hvis du ønsker det.</span><span class="sxs-lookup"><span data-stu-id="445df-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="445df-128">Distribusjon</span><span class="sxs-lookup"><span data-stu-id="445df-128">Deployment</span></span>

1. <span data-ttu-id="445df-129">Last ned malen fra [Dynamics-365-FastTrack-Implementering-Ressurser](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="445df-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="445df-130">Logg på [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="445df-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="445df-131">Opprett en [ressursgruppe](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="445df-131">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="445df-132">Opprett en [lagringskonto](/azure/storage/common/storage-account-create?tabs=azure-portal) i ressursgruppen som du opprettet.</span><span class="sxs-lookup"><span data-stu-id="445df-132">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="445df-133">Opprett en [datafabrikk](/azure/data-factory/quickstart-create-data-factory-portal) i ressursgruppen som du opprettet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="445df-133">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="445df-134">Åpne datafabrikken og velg flisen **Forfatter og overvåking**.</span><span class="sxs-lookup"><span data-stu-id="445df-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="445df-135">På **Administrer**-fanen velger du **ARM-mal**.</span><span class="sxs-lookup"><span data-stu-id="445df-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="445df-136">Velg **Importer ARM-mal** for å importere **partsmalen**.</span><span class="sxs-lookup"><span data-stu-id="445df-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="445df-137">Importer malen til datafabrikken.</span><span class="sxs-lookup"><span data-stu-id="445df-137">Import the template into the data factory.</span></span> <span data-ttu-id="445df-138">Angi følgende verdier for **Prosjektdetalj** og **Forekomstdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="445df-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="445df-139">Felt</span><span class="sxs-lookup"><span data-stu-id="445df-139">Field</span></span> | <span data-ttu-id="445df-140">Verdi</span><span class="sxs-lookup"><span data-stu-id="445df-140">Value</span></span>
    ---|---
    <span data-ttu-id="445df-141">Abonnement</span><span class="sxs-lookup"><span data-stu-id="445df-141">Subscription</span></span> | <span data-ttu-id="445df-142">Azure-abonnement</span><span class="sxs-lookup"><span data-stu-id="445df-142">Azure subscription</span></span>
    <span data-ttu-id="445df-143">Ressursgruppe</span><span class="sxs-lookup"><span data-stu-id="445df-143">Resource group</span></span> | <span data-ttu-id="445df-144">Oppgi den samme ressursen som lagringskontoen opprettes under.</span><span class="sxs-lookup"><span data-stu-id="445df-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="445df-145">Område</span><span class="sxs-lookup"><span data-stu-id="445df-145">Region</span></span> | <span data-ttu-id="445df-146">Angi område.</span><span class="sxs-lookup"><span data-stu-id="445df-146">Specify region.</span></span>
    <span data-ttu-id="445df-147">Fabrikknavn</span><span class="sxs-lookup"><span data-stu-id="445df-147">Factory Name</span></span> | <span data-ttu-id="445df-148">Angi fabrikknavnet.</span><span class="sxs-lookup"><span data-stu-id="445df-148">Specify factory name.</span></span>
    <span data-ttu-id="445df-149">FO Linked Service_service Principal Key</span><span class="sxs-lookup"><span data-stu-id="445df-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="445df-150">Angi nøkkkelen til programmet.</span><span class="sxs-lookup"><span data-stu-id="445df-150">Specify the application's key.</span></span>
    <span data-ttu-id="445df-151">Azure Blob Storage_connection String</span><span class="sxs-lookup"><span data-stu-id="445df-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="445df-152">Tilkoblingsstreng for Azure Blob Storage</span><span class="sxs-lookup"><span data-stu-id="445df-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="445df-153">Dynamics Crm Linked Service_password</span><span class="sxs-lookup"><span data-stu-id="445df-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="445df-154">Passordet for brukerkontoen du har oppgitt som brukernavnet.</span><span class="sxs-lookup"><span data-stu-id="445df-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="445df-155">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="445df-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="445df-156">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="445df-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="445df-157">Angi leierinformasjonen (domenenavn eller leier-ID) som appen ligger under.</span><span class="sxs-lookup"><span data-stu-id="445df-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="445df-158">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="445df-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="445df-159">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="445df-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="445df-160">Angi klient-ID-en til programmet.</span><span class="sxs-lookup"><span data-stu-id="445df-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="445df-161">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="445df-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="445df-162">Brukernavnet for å koble til Dynamics.</span><span class="sxs-lookup"><span data-stu-id="445df-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="445df-163">Hvis du vil ha mer informasjon, kan du se [Forfremme en Resource Manager-mal for hvert miljø manuelt](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Tilkoblede tjenesteegenskaper](/azure/data-factory/connector-dynamics-ax#linked-service-properties) og [Kopiere data ved å bruke Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="445df-163">For more information, see [Manually promote a Resource Manager template for each environment](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="445df-164">Etter distribusjonen validerer du datasettene, dataflyten og den tilkoblede tjenesten til datafabrikken.</span><span class="sxs-lookup"><span data-stu-id="445df-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Datasett, dataflyt og tilknyttet tjeneste](media/data-factory-validate.png)

11. <span data-ttu-id="445df-166">Naviger til **Administrer**.</span><span class="sxs-lookup"><span data-stu-id="445df-166">Navigate to **Manage**.</span></span> <span data-ttu-id="445df-167">Under **Tilkoblinger** velger du **Tilknyttet tjeneste**.</span><span class="sxs-lookup"><span data-stu-id="445df-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="445df-168">Velg **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="445df-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="445df-169">I skjemaet **Rediger tilknyttet tjeneste (Dynamics CRM)** angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="445df-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="445df-170">Felt</span><span class="sxs-lookup"><span data-stu-id="445df-170">Field</span></span> | <span data-ttu-id="445df-171">Verdi</span><span class="sxs-lookup"><span data-stu-id="445df-171">Value</span></span>
    ---|---
    <span data-ttu-id="445df-172">Navn</span><span class="sxs-lookup"><span data-stu-id="445df-172">Name</span></span> | <span data-ttu-id="445df-173">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="445df-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="445df-174">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="445df-174">Description</span></span> | <span data-ttu-id="445df-175">Tilknyttede tjenester for tilkobling til CRM-forekomsten for å hente data for enheter</span><span class="sxs-lookup"><span data-stu-id="445df-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="445df-176">Tilkobling via integrasjonskjøretid</span><span class="sxs-lookup"><span data-stu-id="445df-176">Connect via integration runtime</span></span> | <span data-ttu-id="445df-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="445df-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="445df-178">Distribusjonstype</span><span class="sxs-lookup"><span data-stu-id="445df-178">Deployment type</span></span> | <span data-ttu-id="445df-179">Tilkoblet</span><span class="sxs-lookup"><span data-stu-id="445df-179">Online</span></span>
    <span data-ttu-id="445df-180">Tjeneste-URI</span><span class="sxs-lookup"><span data-stu-id="445df-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="445df-181">Godkjenningstype</span><span class="sxs-lookup"><span data-stu-id="445df-181">Authentication type</span></span> | <span data-ttu-id="445df-182">Office365</span><span class="sxs-lookup"><span data-stu-id="445df-182">Office365</span></span>
    <span data-ttu-id="445df-183">Brukernavn</span><span class="sxs-lookup"><span data-stu-id="445df-183">User name</span></span> |
    <span data-ttu-id="445df-184">Passord eller Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="445df-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="445df-185">Passord</span><span class="sxs-lookup"><span data-stu-id="445df-185">Password</span></span>
    <span data-ttu-id="445df-186">Passord</span><span class="sxs-lookup"><span data-stu-id="445df-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="445df-187">Kjør malen</span><span class="sxs-lookup"><span data-stu-id="445df-187">Run the template</span></span>

1. <span data-ttu-id="445df-188">Stopp dobbel skriving for **Konto**, **Kontakt** og **Leverandør** ved å bruke Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="445df-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="445df-189">Kunder V3 (kontoer)</span><span class="sxs-lookup"><span data-stu-id="445df-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="445df-190">Kunder V3 (kontakter)</span><span class="sxs-lookup"><span data-stu-id="445df-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="445df-191">CDS-kontakter V2 (kontakter)</span><span class="sxs-lookup"><span data-stu-id="445df-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="445df-192">CDS-kontakter V2 (kontakter)</span><span class="sxs-lookup"><span data-stu-id="445df-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="445df-193">Leverandør V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="445df-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="445df-194">Kontroller at kartene er fjernet fra `msdy_dualwriteruntimeconfig`-tabellen i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="445df-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="445df-195">Installer [Løsninger for part med dobbel skriving og global adressebok](https://aka.ms/dual-write-gab) fra AppSource.</span><span class="sxs-lookup"><span data-stu-id="445df-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="445df-196">Hvis tabellene nedenfor i Finance and Operations-appen inneholder data, kjører du deretter **innledende synkronisering** for dem.</span><span class="sxs-lookup"><span data-stu-id="445df-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="445df-197">Hilsener</span><span class="sxs-lookup"><span data-stu-id="445df-197">Salutations</span></span>
    + <span data-ttu-id="445df-198">Typer personlige tegn</span><span class="sxs-lookup"><span data-stu-id="445df-198">Personal character types</span></span>
    + <span data-ttu-id="445df-199">Avsluttende hilsen</span><span class="sxs-lookup"><span data-stu-id="445df-199">Complimentary closing</span></span>
    + <span data-ttu-id="445df-200">Kontaktpersontitler</span><span class="sxs-lookup"><span data-stu-id="445df-200">Contact person titles</span></span>
    + <span data-ttu-id="445df-201">Roller for beslutningstaking</span><span class="sxs-lookup"><span data-stu-id="445df-201">Decision making roles</span></span>
    + <span data-ttu-id="445df-202">Fordelsnivåer</span><span class="sxs-lookup"><span data-stu-id="445df-202">Loyalty levels</span></span>

5. <span data-ttu-id="445df-203">I Customer Engagement-appen deaktiverer du følgende trinn for plugin-moduler.</span><span class="sxs-lookup"><span data-stu-id="445df-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="445df-204">Kontooppdatering</span><span class="sxs-lookup"><span data-stu-id="445df-204">Account Update</span></span>
         + <span data-ttu-id="445df-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Oppdatering av konto</span><span class="sxs-lookup"><span data-stu-id="445df-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="445df-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Oppdatering av konto</span><span class="sxs-lookup"><span data-stu-id="445df-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="445df-207">Kontaktoppdatering</span><span class="sxs-lookup"><span data-stu-id="445df-207">Contact Update</span></span>
         + <span data-ttu-id="445df-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Oppdatering av kontakt</span><span class="sxs-lookup"><span data-stu-id="445df-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="445df-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Oppdatering av kontakt</span><span class="sxs-lookup"><span data-stu-id="445df-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="445df-210">msdyn_party-oppdatering</span><span class="sxs-lookup"><span data-stu-id="445df-210">msdyn_party Update</span></span>
         + <span data-ttu-id="445df-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Oppdatering av msdyn_party</span><span class="sxs-lookup"><span data-stu-id="445df-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="445df-212">msdyn_vendor-oppdatering</span><span class="sxs-lookup"><span data-stu-id="445df-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="445df-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Oppdatering av msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="445df-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="445df-214">I Customer Engagement-appen deaktiverer du følgende arbeidsflyter:</span><span class="sxs-lookup"><span data-stu-id="445df-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="445df-215">Opprette leverandører i tabellen Kontoer</span><span class="sxs-lookup"><span data-stu-id="445df-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="445df-216">Opprette leverandører i tabellen Kontoer</span><span class="sxs-lookup"><span data-stu-id="445df-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="445df-217">Opprette leverandører av typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="445df-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="445df-218">Opprette leverandører av typen Person i tabellen Leverandører</span><span class="sxs-lookup"><span data-stu-id="445df-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="445df-219">Oppdatere leverandører i tabellen Kontoer</span><span class="sxs-lookup"><span data-stu-id="445df-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="445df-220">Oppdatere leverandører i tabellen Leverandører</span><span class="sxs-lookup"><span data-stu-id="445df-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="445df-221">Oppdatere leverandører av typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="445df-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="445df-222">Oppdatere leverandører av typen Person i tabellen Leverandører</span><span class="sxs-lookup"><span data-stu-id="445df-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="445df-223">I datafabrikken kjører du malen ved å velge **Utløs nå**, som vist på følgende bilde.</span><span class="sxs-lookup"><span data-stu-id="445df-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="445df-224">Det kan ta noen timer å fullføre denne prosessen basert på datavolumet.</span><span class="sxs-lookup"><span data-stu-id="445df-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![Utløserkjøring](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="445df-226">Hvis du har tilpasninger for **Konto**, **Kontakt** og **Leverandør**, må du endre malen.</span><span class="sxs-lookup"><span data-stu-id="445df-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="445df-227">Importer de nye **partsoppføringene** i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="445df-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="445df-228">Last ned `FONewParty.csv`-filen fra Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="445df-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="445df-229">Banen er `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="445df-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="445df-230">Konverter `FONewParty.csv`-filen til en Excel-fil, og importer Excel-filen til Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="445df-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="445df-231">Hvis CSV-import fungerer for deg, kan du importere CSV-filen direkte.</span><span class="sxs-lookup"><span data-stu-id="445df-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="445df-232">Importen kan ta noen timer å kjøre, avhengig av datavolumet.</span><span class="sxs-lookup"><span data-stu-id="445df-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="445df-233">Hvis du vil ha mer informasjon, se [Oversikt over dataimport- og -eksportjobber](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="445df-233">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Importer Datavers-partsoppføringene](media/data-factory-import-party.png)

9. <span data-ttu-id="445df-235">I Customer Engagement-appen aktiverer du følgende trinn for plugin-moduler:</span><span class="sxs-lookup"><span data-stu-id="445df-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="445df-236">Kontooppdatering</span><span class="sxs-lookup"><span data-stu-id="445df-236">Account Update</span></span>
         + <span data-ttu-id="445df-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Oppdatering av konto</span><span class="sxs-lookup"><span data-stu-id="445df-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="445df-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Oppdatering av konto</span><span class="sxs-lookup"><span data-stu-id="445df-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="445df-239">Kontaktoppdatering</span><span class="sxs-lookup"><span data-stu-id="445df-239">Contact Update</span></span>
         + <span data-ttu-id="445df-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Oppdatering av kontakt</span><span class="sxs-lookup"><span data-stu-id="445df-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="445df-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Oppdatering av kontakt</span><span class="sxs-lookup"><span data-stu-id="445df-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="445df-242">msdyn_party-oppdatering</span><span class="sxs-lookup"><span data-stu-id="445df-242">msdyn_party Update</span></span>
         + <span data-ttu-id="445df-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Oppdatering av msdyn_party</span><span class="sxs-lookup"><span data-stu-id="445df-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="445df-244">msdyn_vendor-oppdatering</span><span class="sxs-lookup"><span data-stu-id="445df-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="445df-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Oppdatering av msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="445df-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="445df-246">I Customer Engagement-appene aktiverer du følgende arbeidsflyter hvis du deaktiverte dem i de forrige trinnene:</span><span class="sxs-lookup"><span data-stu-id="445df-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="445df-247">Opprette leverandører i tabellen Kontoer</span><span class="sxs-lookup"><span data-stu-id="445df-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="445df-248">Opprette leverandører i tabellen Kontoer</span><span class="sxs-lookup"><span data-stu-id="445df-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="445df-249">Opprette leverandører av typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="445df-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="445df-250">Opprette leverandører av typen Person i tabellen Leverandører</span><span class="sxs-lookup"><span data-stu-id="445df-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="445df-251">Oppdatere leverandører i tabellen Kontoer</span><span class="sxs-lookup"><span data-stu-id="445df-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="445df-252">Oppdatere leverandører i tabellen Leverandører</span><span class="sxs-lookup"><span data-stu-id="445df-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="445df-253">Oppdatere leverandører av typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="445df-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="445df-254">Oppdatere leverandører av typen Person i tabellen Leverandører</span><span class="sxs-lookup"><span data-stu-id="445df-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="445df-255">Kjør de **partsrelaterte** kartene ved å følge instruksjonene i [Part og global adressebok](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="445df-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="445df-256">Feilsøking</span><span class="sxs-lookup"><span data-stu-id="445df-256">Troubleshooting</span></span>

1. <span data-ttu-id="445df-257">Hvis prosessen mislykkes, kjører du datafabrikken på nytt fra den mislykkede aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="445df-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="445df-258">Enkelte filer genereres av datafabrikken som du kan bruke til datavalideringsformål.</span><span class="sxs-lookup"><span data-stu-id="445df-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="445df-259">Datafabrikken kjøres basert på csv-filer som er kommadelt.</span><span class="sxs-lookup"><span data-stu-id="445df-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="445df-260">Hvis det er en feltverdi som har komma, kan det påvirke resultatene.</span><span class="sxs-lookup"><span data-stu-id="445df-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="445df-261">Du må fjerne kommaene.</span><span class="sxs-lookup"><span data-stu-id="445df-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="445df-262">Kategorien **Overvåking** inneholder informasjon om alle trinn og data som behandles.</span><span class="sxs-lookup"><span data-stu-id="445df-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="445df-263">Velg et bestemt trinn for å feilsøke det.</span><span class="sxs-lookup"><span data-stu-id="445df-263">Select a specific step to debug it.</span></span>

    ![Kategorien Overvåking](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="445df-265">Finn ut mer om malen</span><span class="sxs-lookup"><span data-stu-id="445df-265">Learn more about the template</span></span>

<span data-ttu-id="445df-266">Du kan finne kommentarer til malen i [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md)-filen.</span><span class="sxs-lookup"><span data-stu-id="445df-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>