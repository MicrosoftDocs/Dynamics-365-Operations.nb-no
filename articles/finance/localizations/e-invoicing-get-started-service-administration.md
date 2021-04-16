---
title: Komme i gang med tjenesteadministrasjon for elektronisk fakturering
description: Dette emnet beskriver hvordan du kommer i gang med elektronisk fakturering.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ec431cb4a3620459d905f64a80fd820a2113290f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840154"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a><span data-ttu-id="8673d-103">Komme i gang med tjenesteadministrasjon for elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="8673d-103">Get started with Electronic invoicing service administration</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="8673d-104">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="8673d-104">Prerequisites</span></span>

<span data-ttu-id="8673d-105">Før du kan fullføre trinnene i dette emnet må følgende forutsetninger være på plass:</span><span class="sxs-lookup"><span data-stu-id="8673d-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="8673d-106">Du må ha tilgang til kontoen for Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="8673d-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="8673d-107">Du må ha et LCS-prosjekt som inkluderer versjon 10.0.17 eller senere av Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8673d-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="8673d-108">I tillegg må disse appene distribueres i én av følgende Azure-geografier:</span><span class="sxs-lookup"><span data-stu-id="8673d-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="8673d-109">USA øst</span><span class="sxs-lookup"><span data-stu-id="8673d-109">East US</span></span>
    - <span data-ttu-id="8673d-110">USA vest</span><span class="sxs-lookup"><span data-stu-id="8673d-110">West US</span></span>
    - <span data-ttu-id="8673d-111">EU nord</span><span class="sxs-lookup"><span data-stu-id="8673d-111">North EU</span></span>
    - <span data-ttu-id="8673d-112">EU vest</span><span class="sxs-lookup"><span data-stu-id="8673d-112">West EU</span></span>

- <span data-ttu-id="8673d-113">Du må ha tilgang til RCS-kontoen (Regulatory Configuration Services) for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8673d-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="8673d-114">Du må aktivere globaliseringsfunksjonen for kontoen for RCS i Funksjonsbehandling.</span><span class="sxs-lookup"><span data-stu-id="8673d-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="8673d-115">Hvis du vil ha mer informasjon, kan du se [Regulatory Configuration Services (RCS) – globaliseringsfunksjoner](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="8673d-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="8673d-116">Du må opprette en Key Vault og en lagringskonto i Azure.</span><span class="sxs-lookup"><span data-stu-id="8673d-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="8673d-117">Hvis du vil ha mer informasjon, kan du se [Opprette en Azure Storage-konto og et Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="8673d-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a><span data-ttu-id="8673d-118">Installere tilleggsprogrammet for mikrotjenester i Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="8673d-118">Install the add-in for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="8673d-119">Logg på LCS-kontoen.</span><span class="sxs-lookup"><span data-stu-id="8673d-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="8673d-120">Velg flisen **Administrasjon av forhåndsvisningsfunksjoner**.</span><span class="sxs-lookup"><span data-stu-id="8673d-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="8673d-121">Velg delen **Funksjoner i offenlig forhåndsversjon** velger du **E-faktureringstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="8673d-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="8673d-122">Kontroller at alternativet **Forhåndsversjon aktivert** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8673d-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="8673d-123">Velg LCS-distribusjonsprosjektet på LCS-instrumentbordet.</span><span class="sxs-lookup"><span data-stu-id="8673d-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="8673d-124">LCS-prosjektet må kjøre.</span><span class="sxs-lookup"><span data-stu-id="8673d-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="8673d-125">I fanen **Miljøtillegg** velger du **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="8673d-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="8673d-126">Velg **E-faktureringstjenester**.</span><span class="sxs-lookup"><span data-stu-id="8673d-126">Select **e-invoicing Services**.</span></span>
9. <span data-ttu-id="8673d-127">I feltet **App-ID for AAD** angir du **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="8673d-127">In the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="8673d-128">Dettee er en fast verdi.</span><span class="sxs-lookup"><span data-stu-id="8673d-128">This is a fixed value.</span></span>
10. <span data-ttu-id="8673d-129">I feltet **AAD-leier-ID** angir du leier-IDen for kontoen for Azure-abonnementet.</span><span class="sxs-lookup"><span data-stu-id="8673d-129">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="8673d-130">Gå gjennom vilkårene og betingelsene og merk deretter av i avmeringsboksen.</span><span class="sxs-lookup"><span data-stu-id="8673d-130">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="8673d-131">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="8673d-131">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a><span data-ttu-id="8673d-132">Konfigurere parametere for RCS-integrasjon med elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="8673d-132">Set up the parameters for RCS integration with Electronic invoicing</span></span>

1. <span data-ttu-id="8673d-133">Logg på RCS-kontoen.</span><span class="sxs-lookup"><span data-stu-id="8673d-133">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="8673d-134">I delen **Relaterte koblinger** i arbeidsområdet **Elektronisk rapportering** velger du **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="8673d-134">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="8673d-135">I kategorien **E-faktureringstjeneste**, i feltet **URI for endepunkt for tjeneste**, angir du riktig tjenesteendepunkt for Azure-geografien, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="8673d-135">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="8673d-136">Datasenter Azure-geografi</span><span class="sxs-lookup"><span data-stu-id="8673d-136">Datacenter Azure geography</span></span> | <span data-ttu-id="8673d-137">URI for tjenestesluttpunkt</span><span class="sxs-lookup"><span data-stu-id="8673d-137">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="8673d-138">USA øst</span><span class="sxs-lookup"><span data-stu-id="8673d-138">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="8673d-139">USA vest</span><span class="sxs-lookup"><span data-stu-id="8673d-139">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="8673d-140">EU nord</span><span class="sxs-lookup"><span data-stu-id="8673d-140">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="8673d-141">EU vest</span><span class="sxs-lookup"><span data-stu-id="8673d-141">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="8673d-142">Kontroller at feltet **Program-ID** er satt til **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="8673d-142">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="8673d-143">Denne verdien er en fast verdi.</span><span class="sxs-lookup"><span data-stu-id="8673d-143">This value is a fixed value.</span></span>
5. <span data-ttu-id="8673d-144">I feltet **ID for LCS-miljø** angir du ID-en for LCS-miljøet.</span><span class="sxs-lookup"><span data-stu-id="8673d-144">In the **LCS Environment Id** field, enter the ID of your LCS environment.</span></span>
6. <span data-ttu-id="8673d-145">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="8673d-145">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-references"></a><span data-ttu-id="8673d-146">Opprette Key Vault-referanser</span><span class="sxs-lookup"><span data-stu-id="8673d-146">Create Key Vault references</span></span>

1. <span data-ttu-id="8673d-147">Logg på RCS-kontoen.</span><span class="sxs-lookup"><span data-stu-id="8673d-147">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="8673d-148">I arbeidsområdet **Globaliseringsfunksjon** velger du flisen **Elektronisk fakturering** i delen **Miljø**.</span><span class="sxs-lookup"><span data-stu-id="8673d-148">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="8673d-149">På siden for **Miljøkonfigurasjon**, i handlingsruten, velger du **Tjenestemiljø**, og deretter velger du **Key Vault-parametere**.</span><span class="sxs-lookup"><span data-stu-id="8673d-149">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="8673d-150">Velg **Ny** for å opprette en Key Vault-referanse.</span><span class="sxs-lookup"><span data-stu-id="8673d-150">Select **New** to create a key vault reference.</span></span>
5. <span data-ttu-id="8673d-151">I **Navn**-feltet angir du navnet på Key Vault-referansen.</span><span class="sxs-lookup"><span data-stu-id="8673d-151">In the **Name** field, enter the name of the key vault reference.</span></span> <span data-ttu-id="8673d-152">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8673d-152">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="8673d-153">Lim inn hemmeligheten fra Azure Key Vault i feltet **URI for Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="8673d-153">In the **Key Vault URI** field, paste the key vault secret from Azure Key Vault.</span></span> <span data-ttu-id="8673d-154">Hvis du vil ha mer informasjon, kan du se [Opprette en Azure Storage-konto og et Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="8673d-154">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
7. <span data-ttu-id="8673d-155">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="8673d-155">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="8673d-156">Opprette hemmelighet for lagringskonto</span><span class="sxs-lookup"><span data-stu-id="8673d-156">Create Storage account secret</span></span>

1. <span data-ttu-id="8673d-157">På siden **Miljøkonfigurasjon**, i handlingsruten, velger du **Tjenestemiljø** > **Key Vault-parametere**.</span><span class="sxs-lookup"><span data-stu-id="8673d-157">On the **Environment setups** page, on the Action Pane, select **Service environment** > **Key Vault parameters**.</span></span>
2. <span data-ttu-id="8673d-158">Velg en **Key Vault-referanse**, gå til **Sertifikater**-delen, og velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="8673d-158">Select a **Key Vault reference** and in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="8673d-159">I **Navn**-feltet angir du navnet på lagringskontohemmeligheten.</span><span class="sxs-lookup"><span data-stu-id="8673d-159">In the **Name** field, enter the name of the storage account secret.</span></span> <span data-ttu-id="8673d-160">Hvis du vil ha mer informasjon, kan du se [Opprette en Azure Storage-konto og et Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="8673d-160">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="8673d-161">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8673d-161">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="8673d-162">Velg **Hemmelighet** i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8673d-162">In the **Type** field, select **Secret**.</span></span>
6. <span data-ttu-id="8673d-163">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="8673d-163">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="8673d-164">Opprette et digitalt sertifikat og opprette et digitalt sertifikat</span><span class="sxs-lookup"><span data-stu-id="8673d-164">Create a digital certificate secret</span></span>

1. <span data-ttu-id="8673d-165">På siden **Miljøkonfigurasjon**, i handlingsruten, velger du **Tjenestemiljø**, og deretter velger du **Key Vault-parametere**.</span><span class="sxs-lookup"><span data-stu-id="8673d-165">On the **Environment setups** page, on the action Pane, select **Service environment** and then select **Key Vault parameters**.</span></span>
2. <span data-ttu-id="8673d-166">Velg en **Key Vault-referanse**, gå til **Sertifikater**-delen, og velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="8673d-166">Select a **Key Vault reference** and then in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="8673d-167">I **Navn**-feltet angir du navnet på hemmeligheten for det digitale sertifikatet.</span><span class="sxs-lookup"><span data-stu-id="8673d-167">In the **Name** field, enter the name of the digital certificate secret.</span></span> <span data-ttu-id="8673d-168">Hvis du vil ha mer informasjon, kan du se [Opprette en Azure Storage-konto og et Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="8673d-168">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="8673d-169">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8673d-169">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="8673d-170">I feltet **Type** velger du **Sertifikat**.</span><span class="sxs-lookup"><span data-stu-id="8673d-170">In the **Type** field, select **Certificate**.</span></span>
6. <span data-ttu-id="8673d-171">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="8673d-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="8673d-172">Opprette et tjenestemiljø</span><span class="sxs-lookup"><span data-stu-id="8673d-172">Create a service environment</span></span>

1. <span data-ttu-id="8673d-173">Logg på RCS-kontoen.</span><span class="sxs-lookup"><span data-stu-id="8673d-173">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="8673d-174">I arbeidsområdet **Globaliseringsfunksjon** velger du flisen **Elektronisk fakturering** i delen **Miljø**.</span><span class="sxs-lookup"><span data-stu-id="8673d-174">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="8673d-175">Velg **Tjenestemiljø** på siden **Miljøoppsett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8673d-175">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
4. <span data-ttu-id="8673d-176">Velg **Ny** for å opprette et nytt tjenestemiljø.</span><span class="sxs-lookup"><span data-stu-id="8673d-176">Select **New** to create a new service environment.</span></span>
5. <span data-ttu-id="8673d-177">I **Navn**-feltet angir du navnet på e-fakturamiljøet.</span><span class="sxs-lookup"><span data-stu-id="8673d-177">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="8673d-178">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8673d-178">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="8673d-179">I feltet **Lagring av for SAS-tokenhemmelighet** velger du navnet på lagringskontohemmeligheten som må brukes til å godkjenne tilgang til lagringskontoen.</span><span class="sxs-lookup"><span data-stu-id="8673d-179">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
7. <span data-ttu-id="8673d-180">I **Brukere**-delen velger du **Legg til** for å legge til en bruker som har tillatelse til å sende elektroniske fakturaer gjennom miljøet og også koble seg til lagringskontoen.</span><span class="sxs-lookup"><span data-stu-id="8673d-180">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
8. <span data-ttu-id="8673d-181">I **Bruker-ID**-feltet angir du aliaset til brukeren.</span><span class="sxs-lookup"><span data-stu-id="8673d-181">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="8673d-182">Angi brukerens e-postadresse i feltet **E-post**.</span><span class="sxs-lookup"><span data-stu-id="8673d-182">In the **Email** field, enter the user's email address.</span></span>
9. <span data-ttu-id="8673d-183">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="8673d-183">Select **Save**.</span></span>
10. <span data-ttu-id="8673d-184">Hvis den land/område-spesifikke fakturaen krever en sertifikatkjede for å bruke digitale signaturer, velger du **Kjede av sertifikater** og deretter, i handlingsruten, velger du **Key Vault-hemmeligheter**, og følg deretter denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="8673d-184">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>
    1. <span data-ttu-id="8673d-185">Velg **Ny** for å opprette en kjede av sertifikater.</span><span class="sxs-lookup"><span data-stu-id="8673d-185">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="8673d-186">I **Navn**-feltet angir du navnet på kjeden av sertifikater.</span><span class="sxs-lookup"><span data-stu-id="8673d-186">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="8673d-187">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8673d-187">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="8673d-188">I delen **Sertifikater** velger du **Legg til** for å legge til et sertifikat i kjeden.</span><span class="sxs-lookup"><span data-stu-id="8673d-188">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="8673d-189">Bruk knappene **Opp** eller **Ned** for å endre posisjonen til sertifikatene i kjeden.</span><span class="sxs-lookup"><span data-stu-id="8673d-189">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="8673d-190">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="8673d-190">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="8673d-191">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8673d-191">Close the page.</span></span>
11. <span data-ttu-id="8673d-192">På siden **Tjenestemiljø**, i handlingsruten, velger du **Publiser** for å publisere miljøet til skyen.</span><span class="sxs-lookup"><span data-stu-id="8673d-192">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="8673d-193">Verdien i feltet **Status** endres til **Publisert**.</span><span class="sxs-lookup"><span data-stu-id="8673d-193">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="8673d-194">Opprette et tilkoblet program</span><span class="sxs-lookup"><span data-stu-id="8673d-194">Create a connected application</span></span>

1. <span data-ttu-id="8673d-195">Velg **Tilkoblede programmer** på siden **Miljøoppsett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8673d-195">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="8673d-196">Velg **Ny** for å opprette et tilkoblet program.</span><span class="sxs-lookup"><span data-stu-id="8673d-196">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="8673d-197">I **Navn**-feltet angir du navnet på programmet som skal kobles til.</span><span class="sxs-lookup"><span data-stu-id="8673d-197">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="8673d-198">I feltet **Program** angir du URL-adressen til Finance- og Supply Chain Management-miljøet du vil koble til.</span><span class="sxs-lookup"><span data-stu-id="8673d-198">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="8673d-199">I feltet **Leietaker** angir du leietakeren i Finance- og Supply Chain Management-miljøet.</span><span class="sxs-lookup"><span data-stu-id="8673d-199">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="8673d-200">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="8673d-200">Select **Save**.</span></span>
6. <span data-ttu-id="8673d-201">Velg **Kontroller tilkobling** i handlingsruten for å teste tilkoblingen til miljøet.</span><span class="sxs-lookup"><span data-stu-id="8673d-201">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="8673d-202">Lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="8673d-202">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="8673d-203">Koble tilkoblede programmer til miljøer</span><span class="sxs-lookup"><span data-stu-id="8673d-203">Link connected applications to environments</span></span>

1. <span data-ttu-id="8673d-204">På siden **Miljøoppsett** velger du **Ny** for å tilordne et tilkoblet program til et miljø.</span><span class="sxs-lookup"><span data-stu-id="8673d-204">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="8673d-205">I feltet **Tilkoblet program** velger du det tilkoblede programmet.</span><span class="sxs-lookup"><span data-stu-id="8673d-205">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="8673d-206">Velg et tjenestemiljø i feltet **Servicemiljø**.</span><span class="sxs-lookup"><span data-stu-id="8673d-206">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="8673d-207">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="8673d-207">Select **Save**, and then close the page.</span></span>

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="8673d-208">Konfigurere integrasjon av elektronisk fakturering i Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8673d-208">Set up Electronic invoicing integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a><span data-ttu-id="8673d-209">Aktivere funksjonen for integrering av Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="8673d-209">Turn on the Electronic invoicing integration feature</span></span>

1. <span data-ttu-id="8673d-210">Logg på Finance- eller Supply Chain Management-forekomsten din.</span><span class="sxs-lookup"><span data-stu-id="8673d-210">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="8673d-211">I arbeidsområdet **Funksjonsbehandling** søker du etter funksjonen **Integrasjon av Elektronisk fakturering**.</span><span class="sxs-lookup"><span data-stu-id="8673d-211">In the **Feature management** workspace, search for the **Electronic invoicing integration** feature.</span></span> <span data-ttu-id="8673d-212">Hvis denne funksjonen ikke vises på siden, velger du **Se etter oppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="8673d-212">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="8673d-213">Velg funksjonen, og velg deretter **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="8673d-213">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="8673d-214">Konfigurer URL-adressen for endepunkt for tjeneste</span><span class="sxs-lookup"><span data-stu-id="8673d-214">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="8673d-215">Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="8673d-215">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="8673d-216">I kategorien **Innsendingstjeneste**, i feltet **URL for endepunkt for tjeneste**, angir du riktig tjenesteendepunkt for Azure-geografien, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="8673d-216">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="8673d-217">Datasenter Azure-geografi</span><span class="sxs-lookup"><span data-stu-id="8673d-217">Datacenter Azure geography</span></span> | <span data-ttu-id="8673d-218">URL for tjenestesluttpunkt</span><span class="sxs-lookup"><span data-stu-id="8673d-218">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="8673d-219">USA øst</span><span class="sxs-lookup"><span data-stu-id="8673d-219">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="8673d-220">USA vest</span><span class="sxs-lookup"><span data-stu-id="8673d-220">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="8673d-221">Europa, nord</span><span class="sxs-lookup"><span data-stu-id="8673d-221">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="8673d-222">Europa, vest</span><span class="sxs-lookup"><span data-stu-id="8673d-222">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="8673d-223">I **Miljø**-feltet angir du navnet på tjenestemiljøet som er publisert i Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="8673d-223">In the **Environment** field, enter the name of the service environment published in Electronic invoicing.</span></span>
4. <span data-ttu-id="8673d-224">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="8673d-224">Select **Save**, and then close the page.</span></span>

### <a name="enable-flighting-keys"></a><span data-ttu-id="8673d-225">Aktiver testversjoneringsnøkler</span><span class="sxs-lookup"><span data-stu-id="8673d-225">Enable Flighting keys</span></span>

<span data-ttu-id="8673d-226">Aktiver testversjoneringsnøkler for Microsoft Dynamics 365 Finance eller Microsoft Dynamics 365 Supply Chain Management, versjon 10.0.17 eller tidligere.</span><span class="sxs-lookup"><span data-stu-id="8673d-226">Enable Flight keys for  Microsoft Dynamics 365 Finance or  Microsoft Dynamics 365 Supply Chain Management versions 10.0.17 or earlier.</span></span> 
1. <span data-ttu-id="8673d-227">Utfør følgende SQL-kommando:</span><span class="sxs-lookup"><span data-stu-id="8673d-227">Execute the following SQL command:</span></span>

    <span data-ttu-id="8673d-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span><span class="sxs-lookup"><span data-stu-id="8673d-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span></span>
    
    <span data-ttu-id="8673d-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span><span class="sxs-lookup"><span data-stu-id="8673d-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span></span>

2. <span data-ttu-id="8673d-230">Utfør en IISreset-kommando for alle AOS'-er.</span><span class="sxs-lookup"><span data-stu-id="8673d-230">Perform an IISreset command for all AOS's.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
