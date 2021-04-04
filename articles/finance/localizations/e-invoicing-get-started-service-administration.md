---
title: Komme i gang med tjenesteadministrasjon for tillegget for Elektronisk fakturering
description: Dette emnet beskriver hvordan du kommer i gang med tillegget Elektronisk fakturering.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592532"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="1ec34-103">Komme i gang med tjenesteadministrasjon for tillegget for Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="1ec34-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="1ec34-104">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="1ec34-104">Prerequisites</span></span>

<span data-ttu-id="1ec34-105">Før du kan fullføre trinnene i dette emnet må følgende forutsetninger være på plass:</span><span class="sxs-lookup"><span data-stu-id="1ec34-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="1ec34-106">Du må ha tilgang til kontoen for Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="1ec34-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="1ec34-107">Du må ha et LCS-prosjekt som inkluderer versjon 10.0.17 eller senere av Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1ec34-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1ec34-108">I tillegg må disse appene distribueres i én av følgende Azure-geografier:</span><span class="sxs-lookup"><span data-stu-id="1ec34-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="1ec34-109">USA øst</span><span class="sxs-lookup"><span data-stu-id="1ec34-109">East US</span></span>
    - <span data-ttu-id="1ec34-110">USA vest</span><span class="sxs-lookup"><span data-stu-id="1ec34-110">West US</span></span>
    - <span data-ttu-id="1ec34-111">EU nord</span><span class="sxs-lookup"><span data-stu-id="1ec34-111">North EU</span></span>
    - <span data-ttu-id="1ec34-112">EU vest</span><span class="sxs-lookup"><span data-stu-id="1ec34-112">West EU</span></span>

- <span data-ttu-id="1ec34-113">Du må ha tilgang til RCS-kontoen (Regulatory Configuration Services) for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1ec34-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="1ec34-114">Du må aktivere globaliseringsfunksjonen for kontoen for RCS i Funksjonsbehandling.</span><span class="sxs-lookup"><span data-stu-id="1ec34-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="1ec34-115">Hvis du vil ha mer informasjon, kan du se [Regulatory Configuration Services (RCS) – globaliseringsfunksjoner](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="1ec34-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="1ec34-116">Du må opprette en Key Vault og en lagringskonto i Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec34-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="1ec34-117">Hvis du vil ha mer informasjon, kan du se [Opprette en Azure Storage-konto og et Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="1ec34-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="1ec34-118">Installere tillegget for mikrotjenester i Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="1ec34-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="1ec34-119">Logg på LCS-kontoen.</span><span class="sxs-lookup"><span data-stu-id="1ec34-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="1ec34-120">Velg flisen **Administrasjon av forhåndsvisningsfunksjoner**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="1ec34-121">Velg delen **Funksjoner i offenlig forhåndsversjon** velger du **E-faktureringstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="1ec34-122">Kontroller at alternativet **Forhåndsversjon aktivert** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="1ec34-123">Velg LCS-distribusjonsprosjektet på LCS-instrumentbordet.</span><span class="sxs-lookup"><span data-stu-id="1ec34-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="1ec34-124">LCS-prosjektet må kjøre.</span><span class="sxs-lookup"><span data-stu-id="1ec34-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="1ec34-125">I fanen **Miljøtillegg** velger du **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="1ec34-126">Velg **e-faktureringstjenester**, og i feltet **ID for AAD-program** angir du **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-126">Select **e-invoicing Services** and in the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="1ec34-127">Dettee er en fast verdi.</span><span class="sxs-lookup"><span data-stu-id="1ec34-127">This is a fixed value.</span></span>
10. <span data-ttu-id="1ec34-128">I feltet **AAD-leier-ID** angir du leier-IDen for kontoen for Azure-abonnementet.</span><span class="sxs-lookup"><span data-stu-id="1ec34-128">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="1ec34-129">Gå gjennom vilkårene og betingelsene og merk deretter av i avmeringsboksen.</span><span class="sxs-lookup"><span data-stu-id="1ec34-129">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="1ec34-130">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-130">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="1ec34-131">Konfigurere parametere for RCS-integrasjon med Elektronisk fakturering-tillegget</span><span class="sxs-lookup"><span data-stu-id="1ec34-131">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="1ec34-132">Logg på RCS-kontoen.</span><span class="sxs-lookup"><span data-stu-id="1ec34-132">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="1ec34-133">I delen **Relaterte koblinger** i arbeidsområdet **Elektronisk rapportering** velger du **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-133">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="1ec34-134">I kategorien **E-faktureringstjeneste**, i feltet **URI for endepunkt for tjeneste**, angir du riktig tjenesteendepunkt for Azure-geografien, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="1ec34-134">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="1ec34-135">Datasenter Azure-geografi</span><span class="sxs-lookup"><span data-stu-id="1ec34-135">Datacenter Azure geography</span></span> | <span data-ttu-id="1ec34-136">URI for tjenestesluttpunkt</span><span class="sxs-lookup"><span data-stu-id="1ec34-136">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="1ec34-137">USA øst</span><span class="sxs-lookup"><span data-stu-id="1ec34-137">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1ec34-138">USA vest</span><span class="sxs-lookup"><span data-stu-id="1ec34-138">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1ec34-139">EU nord</span><span class="sxs-lookup"><span data-stu-id="1ec34-139">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1ec34-140">EU vest</span><span class="sxs-lookup"><span data-stu-id="1ec34-140">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="1ec34-141">Kontroller at feltet **Program-ID** er satt til **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-141">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="1ec34-142">Denne verdien er en fast verdi.</span><span class="sxs-lookup"><span data-stu-id="1ec34-142">This value is a fixed value.</span></span>
5. <span data-ttu-id="1ec34-143">I feltet **ID for LCS-miljø** angir du IDen for LCS-abonnementskontoen.</span><span class="sxs-lookup"><span data-stu-id="1ec34-143">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="1ec34-144">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="1ec34-144">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="1ec34-145">Opprette Key Vault-hemmelighet</span><span class="sxs-lookup"><span data-stu-id="1ec34-145">Create Key Vault secret</span></span>

1. <span data-ttu-id="1ec34-146">Logg på RCS-kontoen.</span><span class="sxs-lookup"><span data-stu-id="1ec34-146">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="1ec34-147">I arbeidsområdet **Globaliseringsfunksjon** velger du tittelen **Tillegg for elektronisk fakturering** i delen **Miljø**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-147">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>
3. <span data-ttu-id="1ec34-148">På siden for **Miljøkonfigurasjon**, i handlingsruten, velger du **Tjenestemiljø**, og deretter velger du **Key Vault-parametere**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-148">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="1ec34-149">Velg **Ny** for å opprette en Key Vault-nøkkel.</span><span class="sxs-lookup"><span data-stu-id="1ec34-149">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="1ec34-150">I **Navn**-feltet angir du navnet på Key Vault-hemmeligheten.</span><span class="sxs-lookup"><span data-stu-id="1ec34-150">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="1ec34-151">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1ec34-151">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="1ec34-152">Lim inn hemmeligheten fra Azure Key Vault i feltet **URI for Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-152">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="1ec34-153">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-153">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="1ec34-154">Opprette hemmelighet for lagringskonto</span><span class="sxs-lookup"><span data-stu-id="1ec34-154">Create Storage account secret</span></span>

1. <span data-ttu-id="1ec34-155">Gå til **Systemadministrasjon** > **Oppsett** > **Key Vault-parametere**, og velg en Key Vault-hemmelighet.</span><span class="sxs-lookup"><span data-stu-id="1ec34-155">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="1ec34-156">Velg **Legg til** i delen **Sertifikater**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-156">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="1ec34-157">I feltet **Navn** angir du navnet på lagringskontonavnet og en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-157">In the **Name** field, enter the name of the storage account secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="1ec34-158">I feltet **Type** velger du **Sertifikat**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-158">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="1ec34-159">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="1ec34-159">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="1ec34-160">Opprette et digitalt sertifikat og opprette et digitalt sertifikat</span><span class="sxs-lookup"><span data-stu-id="1ec34-160">Create a digital certificate secret</span></span>

1. <span data-ttu-id="1ec34-161">Gå til **Systemadministrasjon** > **Oppsett** > **Key Vault-parametere**, og velg en Key Vault-hemmelighet.</span><span class="sxs-lookup"><span data-stu-id="1ec34-161">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="1ec34-162">Velg **Legg til** i delen **Sertifikater**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-162">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="1ec34-163">I feltet **Navn** angir du navnet på den digitale sertifikathemmeligheten, og i feltet **Beskrivelse** angir du en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="1ec34-163">In the **Name** field, enter the name of the digital certificate secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="1ec34-164">I feltet **Type** velger du **Sertifikat**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-164">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="1ec34-165">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="1ec34-165">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="1ec34-166">Opprette et miljø for tillegget Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="1ec34-166">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="1ec34-167">Logg på RCS-kontoen.</span><span class="sxs-lookup"><span data-stu-id="1ec34-167">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="1ec34-168">I arbeidsområdet **Globaliseringsfunksjon** velger du tittelen **Tillegg for elektronisk fakturering** i delen **Miljø**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-168">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="1ec34-169">Opprette et tjenestemiljø</span><span class="sxs-lookup"><span data-stu-id="1ec34-169">Create a service environment</span></span>

1. <span data-ttu-id="1ec34-170">Velg **Tjenestemiljø** på siden **Miljøoppsett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="1ec34-170">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="1ec34-171">Velg **Ny** for å opprette et nytt tjenestemiljø.</span><span class="sxs-lookup"><span data-stu-id="1ec34-171">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="1ec34-172">I **Navn**-feltet angir du navnet på e-fakturamiljøet.</span><span class="sxs-lookup"><span data-stu-id="1ec34-172">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="1ec34-173">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1ec34-173">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="1ec34-174">I feltet **Lagring av for SAS-tokenhemmelighet** velger du navnet på lagringskontohemmeligheten som må brukes til å godkjenne tilgang til lagringskontoen.</span><span class="sxs-lookup"><span data-stu-id="1ec34-174">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="1ec34-175">I **Brukere**-delen velger du **Legg til** for å legge til en bruker som har tillatelse til å sende elektroniske fakturaer gjennom miljøet og også koble seg til lagringskontoen.</span><span class="sxs-lookup"><span data-stu-id="1ec34-175">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="1ec34-176">I **Bruker-ID**-feltet angir du aliaset til brukeren.</span><span class="sxs-lookup"><span data-stu-id="1ec34-176">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="1ec34-177">Angi brukerens e-postadresse i feltet **E-post**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-177">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="1ec34-178">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-178">Select **Save**.</span></span>
8. <span data-ttu-id="1ec34-179">Hvis den land/område-spesifikke fakturaen krever en sertifikatkjede for å bruke digitale signaturer, velger du **Kjede av sertifikater** og deretter, i handlingsruten, velger du **Key Vault-hemmeligheter**, og følg deretter denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="1ec34-179">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="1ec34-180">Velg **Ny** for å opprette en kjede av sertifikater.</span><span class="sxs-lookup"><span data-stu-id="1ec34-180">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="1ec34-181">I **Navn**-feltet angir du navnet på kjeden av sertifikater.</span><span class="sxs-lookup"><span data-stu-id="1ec34-181">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="1ec34-182">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1ec34-182">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="1ec34-183">I delen **Sertifikater** velger du **Legg til** for å legge til et sertifikat i kjeden.</span><span class="sxs-lookup"><span data-stu-id="1ec34-183">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="1ec34-184">Bruk knappene **Opp** eller **Ned** for å endre posisjonen til sertifikatene i kjeden.</span><span class="sxs-lookup"><span data-stu-id="1ec34-184">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="1ec34-185">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="1ec34-185">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="1ec34-186">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1ec34-186">Close the page.</span></span>
9. <span data-ttu-id="1ec34-187">På siden **Tjenestemiljø**, i handlingsruten, velger du **Publiser** for å publisere miljøet til skyen.</span><span class="sxs-lookup"><span data-stu-id="1ec34-187">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="1ec34-188">Verdien i feltet **Status** endres til **Publisert**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-188">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="1ec34-189">Opprette et tilkoblet program</span><span class="sxs-lookup"><span data-stu-id="1ec34-189">Create a connected application</span></span>

1. <span data-ttu-id="1ec34-190">Velg **Tilkoblede programmer** på siden **Miljøoppsett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="1ec34-190">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="1ec34-191">Velg **Ny** for å opprette et tilkoblet program.</span><span class="sxs-lookup"><span data-stu-id="1ec34-191">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="1ec34-192">I **Navn**-feltet angir du navnet på programmet som skal kobles til.</span><span class="sxs-lookup"><span data-stu-id="1ec34-192">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="1ec34-193">I feltet **Program** angir du URL-adressen til Finance- og Supply Chain Management-miljøet du vil koble til.</span><span class="sxs-lookup"><span data-stu-id="1ec34-193">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="1ec34-194">I feltet **Leietaker** angir du leietakeren i Finance- og Supply Chain Management-miljøet.</span><span class="sxs-lookup"><span data-stu-id="1ec34-194">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="1ec34-195">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-195">Select **Save**.</span></span>
6. <span data-ttu-id="1ec34-196">Velg **Kontroller tilkobling** i handlingsruten for å teste tilkoblingen til miljøet.</span><span class="sxs-lookup"><span data-stu-id="1ec34-196">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="1ec34-197">Lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="1ec34-197">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="1ec34-198">Koble tilkoblede programmer til miljøer</span><span class="sxs-lookup"><span data-stu-id="1ec34-198">Link connected applications to environments</span></span>

1. <span data-ttu-id="1ec34-199">På siden **Miljøoppsett** velger du **Ny** for å tilordne et tilkoblet program til et miljø.</span><span class="sxs-lookup"><span data-stu-id="1ec34-199">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="1ec34-200">I feltet **Tilkoblet program** velger du det tilkoblede programmet.</span><span class="sxs-lookup"><span data-stu-id="1ec34-200">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="1ec34-201">Velg et tjenestemiljø i feltet **Servicemiljø**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-201">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="1ec34-202">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="1ec34-202">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="1ec34-203">Konfigurere integrasjonen av tillegget Elektronisk fakturering i Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1ec34-203">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="1ec34-204">Aktivere funksjonen for integrering av tillegget Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="1ec34-204">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="1ec34-205">Logg på Finance- eller Supply Chain Management-forekomsten din.</span><span class="sxs-lookup"><span data-stu-id="1ec34-205">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="1ec34-206">I arbeidsområdet **Funksjonsbehandling** søker du etter funksjonen **Integrasjon av tillegget Elektronisk fakturering**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-206">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="1ec34-207">Hvis denne funksjonen ikke vises på siden, velger du **Se etter oppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-207">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="1ec34-208">Velg funksjonen, og velg deretter **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-208">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="1ec34-209">Konfigurer URL-adressen for endepunkt for tjeneste</span><span class="sxs-lookup"><span data-stu-id="1ec34-209">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="1ec34-210">Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="1ec34-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="1ec34-211">I kategorien **Innsendingstjeneste**, i feltet **URL for endepunkt for tjeneste**, angir du riktig tjenesteendepunkt for Azure-geografien, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="1ec34-211">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="1ec34-212">Datasenter Azure-geografi</span><span class="sxs-lookup"><span data-stu-id="1ec34-212">Datacenter Azure geography</span></span> | <span data-ttu-id="1ec34-213">URL for tjenestesluttpunkt</span><span class="sxs-lookup"><span data-stu-id="1ec34-213">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="1ec34-214">USA øst</span><span class="sxs-lookup"><span data-stu-id="1ec34-214">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1ec34-215">USA vest</span><span class="sxs-lookup"><span data-stu-id="1ec34-215">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1ec34-216">EU nord</span><span class="sxs-lookup"><span data-stu-id="1ec34-216">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1ec34-217">EU vest</span><span class="sxs-lookup"><span data-stu-id="1ec34-217">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="1ec34-218">I **Miljø**-feltet angir du navnet på miljøet for tillegget Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="1ec34-218">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="1ec34-219">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="1ec34-219">Select **Save**, and then close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
