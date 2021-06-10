---
title: Oppgrader til parten og den globale adressebokmodellen
description: Dette emnet beskriver hvordan du oppgraderer data for dobbel skriving til partsmodellen og den globale adressebokmodellen.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 90ddbe704ab21d62752b581a813601e8986c2103
ms.sourcegitcommit: 180548e3c10459776cf199989d3753e0c1555912
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6112679"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="8d427-103">Oppgrader til parten og den globale adressebokmodellen</span><span class="sxs-lookup"><span data-stu-id="8d427-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8d427-104">Med [Microsoft Azure Data Factory-malen](https://aka.ms/dual-write-gab-adf) kan du oppgradere eksisterende **Konto**, **Kontakt** og **Leverandør**-tabelldata i dobbel skriving til partsmodellen og den globale adressebokmodellen.</span><span class="sxs-lookup"><span data-stu-id="8d427-104">The [Microsoft Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="8d427-105">Malen avstemmer dataene fra både Finance and Operations-apper og Customer Engagement-apper.</span><span class="sxs-lookup"><span data-stu-id="8d427-105">The template reconciles the data from both finance and operations apps and customer engagement applications.</span></span> <span data-ttu-id="8d427-106">På slutten av prosessen vil **Part**- og **Kontakt**-felter for **Part**-oppføringer opprettes og knyttes til **Konto**, **Kontakt** og **Leverandør**-oppføringer i Customer Engagement-programmer.</span><span class="sxs-lookup"><span data-stu-id="8d427-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="8d427-107">En .csv-fil (`FONewParty.csv`) genereres for å opprette nye **Part**-oppføringer i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="8d427-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the finance and operations app.</span></span> <span data-ttu-id="8d427-108">I dette emnet finner du instruksjoner om hvordan du kan bruke Data Factory-malen og oppgradere dataene.</span><span class="sxs-lookup"><span data-stu-id="8d427-108">This topic provides instructions about how to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="8d427-109">Hvis du ikke har noen tilpasninger, kan du bruke malen som den er.</span><span class="sxs-lookup"><span data-stu-id="8d427-109">If you don’t have any customizations, you can use the template as is.</span></span> <span data-ttu-id="8d427-110">Hvis du har tilpasninger for **Konto**, **Kontakt** og **Leverandør**, må du endre malen ved å følge instruksjonene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="8d427-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="8d427-111">Malen oppgraderer bare **Part**-dataene.</span><span class="sxs-lookup"><span data-stu-id="8d427-111">The template only upgrades the **Party** data.</span></span> <span data-ttu-id="8d427-112">I en fremtidig versjon blir postadresser og elektroniske adresser inkludert.</span><span class="sxs-lookup"><span data-stu-id="8d427-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8d427-113">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="8d427-113">Prerequisites</span></span>

<span data-ttu-id="8d427-114">Følgende forutsetninger kreves for å oppgradere til parten og den globale adressebokmodellen:</span><span class="sxs-lookup"><span data-stu-id="8d427-114">The following prerequisites are required to upgrade to the party and global address book model:</span></span>

+ [<span data-ttu-id="8d427-115">Azure-abonnement</span><span class="sxs-lookup"><span data-stu-id="8d427-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="8d427-116">Tilgang til malen</span><span class="sxs-lookup"><span data-stu-id="8d427-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="8d427-117">Du må være en eksisterende kunde med dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="8d427-117">You must be an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="8d427-118">Forberede for oppgraderingen</span><span class="sxs-lookup"><span data-stu-id="8d427-118">Prepare for the upgrade</span></span>
<span data-ttu-id="8d427-119">Følgende aktiviteter er nødvendige for å forberede for oppgraderingen:</span><span class="sxs-lookup"><span data-stu-id="8d427-119">The following activities are needed to prepare for the upgrade:</span></span>

+ <span data-ttu-id="8d427-120">**Fullstendig synkronisert**: Begge miljøene er i en fullstending synkronisert tilstand for **Konto (kunde)**, **Kontakt** og **Leverandør**.</span><span class="sxs-lookup"><span data-stu-id="8d427-120">**Fully synced**: Both environments are in a fully synced state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="8d427-121">**Integrasjonsnøkler**: Tabellene **Konto (kunde)**, **Kontakt** og **Leverandør** i Customer Engagement-apper bruker de medfølgende integrasjonsnøklene.</span><span class="sxs-lookup"><span data-stu-id="8d427-121">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="8d427-122">Hvis du har tilpasset integrasjonsnøklene, må du tilpasse malen.</span><span class="sxs-lookup"><span data-stu-id="8d427-122">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="8d427-123">**Partsnummer**: Alle oppføringer av typen **Konto (kunde)**, **Kontakt** og **Leverandør** som skal oppgraderes, har et **partsnummer**.</span><span class="sxs-lookup"><span data-stu-id="8d427-123">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="8d427-124">Oppføringer uten et **partsnummer** blir ignorert.</span><span class="sxs-lookup"><span data-stu-id="8d427-124">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="8d427-125">Hvis du vil oppgradere disse oppføringer, legger du til et **partsnummer** før du starter oppgraderingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="8d427-125">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="8d427-126">**Systembrudd**: Under oppgraderingsprosessen må du koble fra både Finance and Operations- og Customer Engagement-miljøer.</span><span class="sxs-lookup"><span data-stu-id="8d427-126">**System outage**: During the upgrade process, you will have to take both the finance and operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="8d427-127">**Øyeblikksbilde**: Ta øyeblikksbilder både av Finance and Operations- og Customer Engagement-appene.</span><span class="sxs-lookup"><span data-stu-id="8d427-127">**Snapshot**: Take snapshots of both the finance and operations apps and customer engagement apps.</span></span> <span data-ttu-id="8d427-128">Bruk øyeblikksbildene til å gjenopprette den forrige tilstanden hvis du ønsker det.</span><span class="sxs-lookup"><span data-stu-id="8d427-128">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="8d427-129">Distribusjon</span><span class="sxs-lookup"><span data-stu-id="8d427-129">Deployment</span></span>

1. <span data-ttu-id="8d427-130">Last ned malen fra [Dynamics-365-FastTrack-Implementering-Ressurser](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="8d427-130">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="8d427-131">Logg på [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="8d427-131">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="8d427-132">Opprett en [ressursgruppe](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="8d427-132">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="8d427-133">Opprett en [lagringskonto](/azure/storage/common/storage-account-create?tabs=azure-portal) i ressursgruppen som du opprettet.</span><span class="sxs-lookup"><span data-stu-id="8d427-133">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="8d427-134">Opprett en [datafabrikk](/azure/data-factory/quickstart-create-data-factory-portal) i ressursgruppen som du opprettet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="8d427-134">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="8d427-135">Åpne datafabrikken og velg flisen **Forfatter og overvåking**.</span><span class="sxs-lookup"><span data-stu-id="8d427-135">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="8d427-136">På **Administrer**-fanen velger du **ARM-mal**.</span><span class="sxs-lookup"><span data-stu-id="8d427-136">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="8d427-137">Velg **Importer ARM-mal** for å importere **partsmalen**.</span><span class="sxs-lookup"><span data-stu-id="8d427-137">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="8d427-138">Importer malen til datafabrikken.</span><span class="sxs-lookup"><span data-stu-id="8d427-138">Import the template into the data factory.</span></span> <span data-ttu-id="8d427-139">Angi følgende verdier for **Prosjektdetalj** og **Forekomstdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="8d427-139">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="8d427-140">Felt</span><span class="sxs-lookup"><span data-stu-id="8d427-140">Field</span></span> | <span data-ttu-id="8d427-141">Verdi</span><span class="sxs-lookup"><span data-stu-id="8d427-141">Value</span></span>
    ---|---
    <span data-ttu-id="8d427-142">Abonnement</span><span class="sxs-lookup"><span data-stu-id="8d427-142">Subscription</span></span> | <span data-ttu-id="8d427-143">Azure-abonnement</span><span class="sxs-lookup"><span data-stu-id="8d427-143">Azure subscription</span></span>
    <span data-ttu-id="8d427-144">Ressursgruppe</span><span class="sxs-lookup"><span data-stu-id="8d427-144">Resource group</span></span> | <span data-ttu-id="8d427-145">Oppgi den samme ressursen som lagringskontoen opprettes under.</span><span class="sxs-lookup"><span data-stu-id="8d427-145">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="8d427-146">Område</span><span class="sxs-lookup"><span data-stu-id="8d427-146">Region</span></span> | <span data-ttu-id="8d427-147">Angi område.</span><span class="sxs-lookup"><span data-stu-id="8d427-147">Specify region.</span></span>
    <span data-ttu-id="8d427-148">Fabrikknavn</span><span class="sxs-lookup"><span data-stu-id="8d427-148">Factory Name</span></span> | <span data-ttu-id="8d427-149">Angi fabrikknavnet.</span><span class="sxs-lookup"><span data-stu-id="8d427-149">Specify factory name.</span></span>
    <span data-ttu-id="8d427-150">FO Linked Service_service Principal Key</span><span class="sxs-lookup"><span data-stu-id="8d427-150">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="8d427-151">Angi nøkkkelen til programmet.</span><span class="sxs-lookup"><span data-stu-id="8d427-151">Specify the application's key.</span></span>
    <span data-ttu-id="8d427-152">Azure Blob Storage_connection String</span><span class="sxs-lookup"><span data-stu-id="8d427-152">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="8d427-153">Tilkoblingsstreng for Azure Blob Storage</span><span class="sxs-lookup"><span data-stu-id="8d427-153">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="8d427-154">Dynamics Crm Linked Service_password</span><span class="sxs-lookup"><span data-stu-id="8d427-154">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="8d427-155">Passordet for brukerkontoen du har oppgitt som brukernavnet.</span><span class="sxs-lookup"><span data-stu-id="8d427-155">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="8d427-156">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="8d427-156">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="8d427-157">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="8d427-157">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="8d427-158">Angi leierinformasjonen (domenenavn eller leier-ID) som appen ligger under.</span><span class="sxs-lookup"><span data-stu-id="8d427-158">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="8d427-159">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="8d427-159">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="8d427-160">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="8d427-160">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="8d427-161">Angi klient-ID-en til programmet.</span><span class="sxs-lookup"><span data-stu-id="8d427-161">Specify the application's client ID.</span></span>
    <span data-ttu-id="8d427-162">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="8d427-162">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="8d427-163">Brukernavnet for å koble til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8d427-163">The username to connect to Dynamics 365.</span></span>

    <span data-ttu-id="8d427-164">Hvis du vil ha mer informasjon, kan du se ett av følgende emner:</span><span class="sxs-lookup"><span data-stu-id="8d427-164">For additional information, refer to the following topics:</span></span> 
    
    - [<span data-ttu-id="8d427-165">Forfremme en Resource Manager-mal for hvert miljø manuelt</span><span class="sxs-lookup"><span data-stu-id="8d427-165">Manually promote a Resource Manager template for each environment</span></span>](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [<span data-ttu-id="8d427-166">Tilkoblede tjenesteegenskaper</span><span class="sxs-lookup"><span data-stu-id="8d427-166">Linked service properties</span></span>](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [<span data-ttu-id="8d427-167">Kopiere data ved hjelp av Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="8d427-167">Copy data using Azure Data Factory</span></span>](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. <span data-ttu-id="8d427-168">Etter distribusjonen validerer du datasettene, dataflyten og den tilkoblede tjenesten til datafabrikken.</span><span class="sxs-lookup"><span data-stu-id="8d427-168">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Datasett, dataflyt og tilknyttet tjeneste](media/data-factory-validate.png)

11. <span data-ttu-id="8d427-170">Naviger til **Administrer**.</span><span class="sxs-lookup"><span data-stu-id="8d427-170">Navigate to **Manage**.</span></span> <span data-ttu-id="8d427-171">Under **Tilkoblinger** velger du **Tilknyttet tjeneste**.</span><span class="sxs-lookup"><span data-stu-id="8d427-171">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="8d427-172">Velg **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="8d427-172">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="8d427-173">I skjemaet **Rediger tilknyttet tjeneste (Dynamics CRM)** angir du følgende verdier.</span><span class="sxs-lookup"><span data-stu-id="8d427-173">In the **Edit linked service (Dynamics CRM)** form, enter the following values.</span></span>

    <span data-ttu-id="8d427-174">Felt</span><span class="sxs-lookup"><span data-stu-id="8d427-174">Field</span></span> | <span data-ttu-id="8d427-175">Verdi</span><span class="sxs-lookup"><span data-stu-id="8d427-175">Value</span></span>
    ---|---
    <span data-ttu-id="8d427-176">Navn</span><span class="sxs-lookup"><span data-stu-id="8d427-176">Name</span></span> | <span data-ttu-id="8d427-177">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="8d427-177">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="8d427-178">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="8d427-178">Description</span></span> | <span data-ttu-id="8d427-179">Tilknyttede tjenester for tilkobling til CRM-forekomsten for å hente data for enheter</span><span class="sxs-lookup"><span data-stu-id="8d427-179">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="8d427-180">Tilkobling via integrasjonskjøretid</span><span class="sxs-lookup"><span data-stu-id="8d427-180">Connect via integration runtime</span></span> | <span data-ttu-id="8d427-181">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8d427-181">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="8d427-182">Distribusjonstype</span><span class="sxs-lookup"><span data-stu-id="8d427-182">Deployment type</span></span> | <span data-ttu-id="8d427-183">Tilkoblet</span><span class="sxs-lookup"><span data-stu-id="8d427-183">Online</span></span>
    <span data-ttu-id="8d427-184">Tjeneste-URI</span><span class="sxs-lookup"><span data-stu-id="8d427-184">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="8d427-185">Godkjenningstype</span><span class="sxs-lookup"><span data-stu-id="8d427-185">Authentication type</span></span> | <span data-ttu-id="8d427-186">Office365</span><span class="sxs-lookup"><span data-stu-id="8d427-186">Office365</span></span>
    <span data-ttu-id="8d427-187">Brukernavn</span><span class="sxs-lookup"><span data-stu-id="8d427-187">User name</span></span> |
    <span data-ttu-id="8d427-188">Passord eller Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="8d427-188">Password or Azure Key Vault</span></span> | <span data-ttu-id="8d427-189">Passord</span><span class="sxs-lookup"><span data-stu-id="8d427-189">Password</span></span>
    <span data-ttu-id="8d427-190">Passord</span><span class="sxs-lookup"><span data-stu-id="8d427-190">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="8d427-191">Kjør malen</span><span class="sxs-lookup"><span data-stu-id="8d427-191">Run the template</span></span>

1. <span data-ttu-id="8d427-192">Stopp følgende dobbel skriving-tilordninger for **Konto**, **Kontakt** og **Leverandør** ved å bruke Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="8d427-192">Stop the following **Account**, **Contact**, and **Vendor** dual-write maps using the Finance and Operations app.</span></span>

    + <span data-ttu-id="8d427-193">Kunder V3 (kontoer)</span><span class="sxs-lookup"><span data-stu-id="8d427-193">Customers V3(accounts)</span></span>
    + <span data-ttu-id="8d427-194">Kunder V3 (kontakter)</span><span class="sxs-lookup"><span data-stu-id="8d427-194">Customers V3(contacts)</span></span>
    + <span data-ttu-id="8d427-195">CDS-kontakter V2 (kontakter)</span><span class="sxs-lookup"><span data-stu-id="8d427-195">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="8d427-196">CDS-kontakter V2 (kontakter)</span><span class="sxs-lookup"><span data-stu-id="8d427-196">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="8d427-197">Leverandør V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="8d427-197">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="8d427-198">Kontroller at kartene er fjernet fra `msdy_dualwriteruntimeconfig`-tabellen i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8d427-198">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="8d427-199">Installer [Løsninger for part med dobbel skriving og global adressebok](https://aka.ms/dual-write-gab) fra AppSource.</span><span class="sxs-lookup"><span data-stu-id="8d427-199">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="8d427-200">Hvis tabellene nedenfor i Finance and Operations-appen inneholder data, kjører du **Innledende synkronisering** for dem.</span><span class="sxs-lookup"><span data-stu-id="8d427-200">In the finance and operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="8d427-201">Hilsener</span><span class="sxs-lookup"><span data-stu-id="8d427-201">Salutations</span></span>
    + <span data-ttu-id="8d427-202">Typer personlige tegn</span><span class="sxs-lookup"><span data-stu-id="8d427-202">Personal character types</span></span>
    + <span data-ttu-id="8d427-203">Avsluttende hilsen</span><span class="sxs-lookup"><span data-stu-id="8d427-203">Complimentary closing</span></span>
    + <span data-ttu-id="8d427-204">Kontaktpersontitler</span><span class="sxs-lookup"><span data-stu-id="8d427-204">Contact person titles</span></span>
    + <span data-ttu-id="8d427-205">Roller for beslutningstaking</span><span class="sxs-lookup"><span data-stu-id="8d427-205">Decision making roles</span></span>
    + <span data-ttu-id="8d427-206">Fordelsnivåer</span><span class="sxs-lookup"><span data-stu-id="8d427-206">Loyalty levels</span></span>

5. <span data-ttu-id="8d427-207">I Customer Engagement-appen deaktiverer du følgende trinn for plugin-moduler.</span><span class="sxs-lookup"><span data-stu-id="8d427-207">In the customer engagement app, disable the following plug-in steps.</span></span>

    + <span data-ttu-id="8d427-208">Kontooppdatering</span><span class="sxs-lookup"><span data-stu-id="8d427-208">Account Update</span></span>
         + <span data-ttu-id="8d427-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Oppdatering av konto</span><span class="sxs-lookup"><span data-stu-id="8d427-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="8d427-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Oppdatering av konto</span><span class="sxs-lookup"><span data-stu-id="8d427-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="8d427-211">Kontaktoppdatering</span><span class="sxs-lookup"><span data-stu-id="8d427-211">Contact Update</span></span>
         + <span data-ttu-id="8d427-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Oppdatering av kontakt</span><span class="sxs-lookup"><span data-stu-id="8d427-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="8d427-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Oppdatering av kontakt</span><span class="sxs-lookup"><span data-stu-id="8d427-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="8d427-214">msdyn_party-oppdatering</span><span class="sxs-lookup"><span data-stu-id="8d427-214">msdyn_party Update</span></span>
         + <span data-ttu-id="8d427-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Oppdatering av msdyn_party</span><span class="sxs-lookup"><span data-stu-id="8d427-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="8d427-216">msdyn_vendor-oppdatering</span><span class="sxs-lookup"><span data-stu-id="8d427-216">msdyn_vendor Update</span></span>
         + <span data-ttu-id="8d427-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Oppdatering av msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="8d427-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="8d427-218">I Customer Engagement-appen deaktiverer du følgende arbeidsflyter:</span><span class="sxs-lookup"><span data-stu-id="8d427-218">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="8d427-219">Opprette leverandører i tabellen Kontoer</span><span class="sxs-lookup"><span data-stu-id="8d427-219">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="8d427-220">Opprette leverandører i tabellen Kontoer</span><span class="sxs-lookup"><span data-stu-id="8d427-220">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="8d427-221">Opprette leverandører av typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="8d427-221">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="8d427-222">Opprette leverandører av typen Person i tabellen Leverandører</span><span class="sxs-lookup"><span data-stu-id="8d427-222">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="8d427-223">Oppdatere leverandører i tabellen Kontoer</span><span class="sxs-lookup"><span data-stu-id="8d427-223">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="8d427-224">Oppdatere leverandører i tabellen Leverandører</span><span class="sxs-lookup"><span data-stu-id="8d427-224">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="8d427-225">Oppdatere leverandører av typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="8d427-225">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="8d427-226">Oppdatere leverandører av typen Person i tabellen Leverandører</span><span class="sxs-lookup"><span data-stu-id="8d427-226">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="8d427-227">I datafabrikken kjører du malen ved å velge **Utløs nå**, som vist på følgende bilde.</span><span class="sxs-lookup"><span data-stu-id="8d427-227">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="8d427-228">Det kan ta noen timer å fullføre denne prosessen basert på datavolumet.</span><span class="sxs-lookup"><span data-stu-id="8d427-228">This process might take a few hours to complete based on the data volume.</span></span>

    ![Utløserkjøring](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="8d427-230">Hvis du har tilpasninger for **Konto**, **Kontakt** og **Leverandør**, må du endre malen.</span><span class="sxs-lookup"><span data-stu-id="8d427-230">If you have customizations for **Account**, **Contact**, and **Vendor**, then you need to modify the template.</span></span>

8. <span data-ttu-id="8d427-231">Importer de nye **partsoppføringene** i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="8d427-231">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="8d427-232">Last ned `FONewParty.csv`-filen fra Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="8d427-232">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="8d427-233">Banen er `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="8d427-233">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="8d427-234">Konverter `FONewParty.csv`-filen til en Excel-fil, og importer Excel-filen til Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="8d427-234">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the finance and operations app.</span></span> <span data-ttu-id="8d427-235">Hvis CSV-import fungerer for deg, kan du importere CSV-filen direkte.</span><span class="sxs-lookup"><span data-stu-id="8d427-235">If the csv import works for you, you can import the csv file directly.</span></span> <span data-ttu-id="8d427-236">Importen kan ta noen timer å kjøre, avhengig av datavolumet.</span><span class="sxs-lookup"><span data-stu-id="8d427-236">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="8d427-237">Hvis du vil ha mer informasjon, se [Oversikt over dataimport- og -eksportjobber](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="8d427-237">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Importer Datavers-partsoppføringene](media/data-factory-import-party.png)

9. <span data-ttu-id="8d427-239">I Customer Engagement-appen aktiverer du følgende trinn for plugin-moduler:</span><span class="sxs-lookup"><span data-stu-id="8d427-239">In the customer engagement apps, enable the following plug-in steps:</span></span>

    + <span data-ttu-id="8d427-240">Kontooppdatering</span><span class="sxs-lookup"><span data-stu-id="8d427-240">Account Update</span></span>
         + <span data-ttu-id="8d427-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Oppdatering av konto</span><span class="sxs-lookup"><span data-stu-id="8d427-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="8d427-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Oppdatering av konto</span><span class="sxs-lookup"><span data-stu-id="8d427-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="8d427-243">Kontaktoppdatering</span><span class="sxs-lookup"><span data-stu-id="8d427-243">Contact Update</span></span>
         + <span data-ttu-id="8d427-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Oppdatering av kontakt</span><span class="sxs-lookup"><span data-stu-id="8d427-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="8d427-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Oppdatering av kontakt</span><span class="sxs-lookup"><span data-stu-id="8d427-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="8d427-246">msdyn_party-oppdatering</span><span class="sxs-lookup"><span data-stu-id="8d427-246">msdyn_party Update</span></span>
         + <span data-ttu-id="8d427-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Oppdatering av msdyn_party</span><span class="sxs-lookup"><span data-stu-id="8d427-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="8d427-248">msdyn_vendor-oppdatering</span><span class="sxs-lookup"><span data-stu-id="8d427-248">msdyn_vendor Update</span></span>
         + <span data-ttu-id="8d427-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Oppdatering av msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="8d427-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="8d427-250">I Customer Engagement-appene aktiverer du følgende arbeidsflyter hvis du deaktiverte dem i de forrige trinnene:</span><span class="sxs-lookup"><span data-stu-id="8d427-250">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="8d427-251">Opprette leverandører i tabellen Kontoer</span><span class="sxs-lookup"><span data-stu-id="8d427-251">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="8d427-252">Opprette leverandører i tabellen Kontoer</span><span class="sxs-lookup"><span data-stu-id="8d427-252">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="8d427-253">Opprette leverandører av typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="8d427-253">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="8d427-254">Opprette leverandører av typen Person i tabellen Leverandører</span><span class="sxs-lookup"><span data-stu-id="8d427-254">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="8d427-255">Oppdatere leverandører i tabellen Kontoer</span><span class="sxs-lookup"><span data-stu-id="8d427-255">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="8d427-256">Oppdatere leverandører i tabellen Leverandører</span><span class="sxs-lookup"><span data-stu-id="8d427-256">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="8d427-257">Oppdatere leverandører av typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="8d427-257">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="8d427-258">Oppdatere leverandører av typen Person i tabellen Leverandører</span><span class="sxs-lookup"><span data-stu-id="8d427-258">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="8d427-259">Kjør de **partsrelaterte** kartene ved å følge instruksjonene i [Part og global adressebok](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="8d427-259">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="8d427-260">Feilsøking</span><span class="sxs-lookup"><span data-stu-id="8d427-260">Troubleshooting</span></span>

1. <span data-ttu-id="8d427-261">Hvis prosessen mislykkes, kjører du datafabrikken på nytt fra den mislykkede aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="8d427-261">If the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="8d427-262">Enkelte filer genereres av datafabrikken som du kan bruke til datavalideringsformål.</span><span class="sxs-lookup"><span data-stu-id="8d427-262">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="8d427-263">Datafabrikken kjøres basert på csv-filer som er kommadelt.</span><span class="sxs-lookup"><span data-stu-id="8d427-263">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="8d427-264">Hvis det er en feltverdi som har komma, kan det påvirke resultatene.</span><span class="sxs-lookup"><span data-stu-id="8d427-264">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="8d427-265">Du må fjerne kommaene.</span><span class="sxs-lookup"><span data-stu-id="8d427-265">You need to remove the commas.</span></span>
4. <span data-ttu-id="8d427-266">Kategorien **Overvåking** inneholder informasjon om alle trinn og data som behandles.</span><span class="sxs-lookup"><span data-stu-id="8d427-266">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="8d427-267">Velg et bestemt trinn for å feilsøke det.</span><span class="sxs-lookup"><span data-stu-id="8d427-267">Select a specific step to debug it.</span></span>

    ![Kategorien Overvåking](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="8d427-269">Finn ut mer om malen</span><span class="sxs-lookup"><span data-stu-id="8d427-269">Learn more about the template</span></span>

<span data-ttu-id="8d427-270">Du finner mer informasjon om malen i [Kommentarer for Viktig-filen for Azure Data Factory-malen](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="8d427-270">You can find additional information about the template in [Comments for Azure Data Factory template readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span></span>
