---
title: Komme i gang med tjenesteadministrasjon for tillegget for Elektronisk fakturering
description: Dette emnet beskriver hvordan du kommer i gang med tillegget Elektronisk fakturering.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
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
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104418"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="59972-103">Komme i gang med tjenesteadministrasjon for tillegget for Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="59972-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="59972-104">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="59972-104">Prerequisites</span></span>

<span data-ttu-id="59972-105">Før du kan fullføre trinnene i dette emnet må følgende forutsetninger være på plass:</span><span class="sxs-lookup"><span data-stu-id="59972-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="59972-106">Du må ha tilgang til kontoen for Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="59972-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="59972-107">Du må ha et LCS-prosjekt som inkluderer versjon 10.0.13 eller senere av Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="59972-107">You must have an LCS project that includes version 10.0.13 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="59972-108">I tillegg må disse appene distribueres i én av følgende Azure-geografier:</span><span class="sxs-lookup"><span data-stu-id="59972-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="59972-109">USA øst</span><span class="sxs-lookup"><span data-stu-id="59972-109">East US</span></span>
    - <span data-ttu-id="59972-110">USA vest</span><span class="sxs-lookup"><span data-stu-id="59972-110">West US</span></span>
    - <span data-ttu-id="59972-111">EU nord</span><span class="sxs-lookup"><span data-stu-id="59972-111">North EU</span></span>
    - <span data-ttu-id="59972-112">EU vest</span><span class="sxs-lookup"><span data-stu-id="59972-112">West EU</span></span>

- <span data-ttu-id="59972-113">Du må ha tilgang til RCS-kontoen (Regulatory Configuration Services) for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="59972-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="59972-114">Du må aktivere globaliseringsfunksjonen for kontoen for RCS i Funksjonsbehandling.</span><span class="sxs-lookup"><span data-stu-id="59972-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="59972-115">Hvis du vil ha mer informasjon, kan du se [Regulatory Configuration Services (RCS) – globaliseringsfunksjoner](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="59972-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="59972-116">Du må opprette en Key Vault og en lagringskonto i Azure.</span><span class="sxs-lookup"><span data-stu-id="59972-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="59972-117">Hvis du vil ha mer informasjon, kan du se [Opprette en Azure Storage-konto og et Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="59972-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="59972-118">Installere tillegget for mikrotjenester i Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="59972-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="59972-119">Logg på LCS-kontoen.</span><span class="sxs-lookup"><span data-stu-id="59972-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="59972-120">Velg flisen **Administrasjon av forhåndsvisningsfunksjoner**.</span><span class="sxs-lookup"><span data-stu-id="59972-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="59972-121">Velg delen **Funksjoner i offenlig forhåndsversjon** velger du **E-faktureringstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="59972-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="59972-122">Kontroller at alternativet **Forhåndsversjon aktivert** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="59972-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="59972-123">Konfigurere parametere for RCS-integrasjon med Elektronisk fakturering-tillegget</span><span class="sxs-lookup"><span data-stu-id="59972-123">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="59972-124">Logg på RCS-kontoen.</span><span class="sxs-lookup"><span data-stu-id="59972-124">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="59972-125">I delen **Relaterte koblinger** i arbeidsområdet **Elektronisk rapportering** velger du **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="59972-125">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="59972-126">I kategorien **E-faktureringstjeneste**, i feltet **URI for endepunkt for tjeneste**, angir du riktig tjenesteendepunkt for Azure-geografien, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="59972-126">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="59972-127">Datasenter Azure-geografi</span><span class="sxs-lookup"><span data-stu-id="59972-127">Datacenter Azure geography</span></span> | <span data-ttu-id="59972-128">URI for tjenestesluttpunkt</span><span class="sxs-lookup"><span data-stu-id="59972-128">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="59972-129">USA øst</span><span class="sxs-lookup"><span data-stu-id="59972-129">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="59972-130">USA vest</span><span class="sxs-lookup"><span data-stu-id="59972-130">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="59972-131">EU nord</span><span class="sxs-lookup"><span data-stu-id="59972-131">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="59972-132">EU vest</span><span class="sxs-lookup"><span data-stu-id="59972-132">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="59972-133">Kontroller at feltet **Program-ID** er satt til **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="59972-133">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="59972-134">Denne verdien er en fast verdi.</span><span class="sxs-lookup"><span data-stu-id="59972-134">This value is a fixed value.</span></span>
5. <span data-ttu-id="59972-135">I feltet **ID for LCS-miljø** angir du IDen for LCS-abonnementskontoen.</span><span class="sxs-lookup"><span data-stu-id="59972-135">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="59972-136">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="59972-136">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="59972-137">Opprette Key Vault-hemmelighet</span><span class="sxs-lookup"><span data-stu-id="59972-137">Create Key Vault secret</span></span>

1. <span data-ttu-id="59972-138">Logg på RCS-kontoen.</span><span class="sxs-lookup"><span data-stu-id="59972-138">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="59972-139">I **Globaliseringsfunksjon**-arbeidsområdet i delen **Miljø** velger du flisen **E-fakturering**.</span><span class="sxs-lookup"><span data-stu-id="59972-139">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="59972-140">På siden for **Miljøkonfigurasjon**, i handlingsruten, velger du **Tjenestemiljø**, og deretter velger du **Key Vault-parametere**.</span><span class="sxs-lookup"><span data-stu-id="59972-140">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="59972-141">Velg **Ny** for å opprette en Key Vault-nøkkel.</span><span class="sxs-lookup"><span data-stu-id="59972-141">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="59972-142">I **Navn**-feltet angir du navnet på Key Vault-hemmeligheten.</span><span class="sxs-lookup"><span data-stu-id="59972-142">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="59972-143">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="59972-143">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="59972-144">Lim inn hemmeligheten fra Azure Key Vault i feltet **URI for Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="59972-144">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="59972-145">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="59972-145">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="59972-146">Opprette hemmelighet for lagringskonto</span><span class="sxs-lookup"><span data-stu-id="59972-146">Create Storage account secret</span></span>

1. <span data-ttu-id="59972-147">Velg **Legg til** på siden **Nøkkelhvelvparametere** i delen **Sertifikater**.</span><span class="sxs-lookup"><span data-stu-id="59972-147">On **Key vault parameters** page, in the **Certificates** section, select **Add**.</span></span>
2. <span data-ttu-id="59972-148">I **Navn**-feltet angir du navnet på lagringskontohemmeligheten.</span><span class="sxs-lookup"><span data-stu-id="59972-148">In the **Name** field, enter the same of the storage account secret.</span></span> <span data-ttu-id="59972-149">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="59972-149">In the **Description** field, enter a description.</span></span>
3. <span data-ttu-id="59972-150">I feltet **Type** velger du **Sertifikat**.</span><span class="sxs-lookup"><span data-stu-id="59972-150">In the **Type** field, select **Certificate**.</span></span>
4. <span data-ttu-id="59972-151">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="59972-151">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="59972-152">Opprette et miljø for tillegget Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="59972-152">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="59972-153">Logg på RCS-kontoen.</span><span class="sxs-lookup"><span data-stu-id="59972-153">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="59972-154">I **Globaliseringsfunksjon**-arbeidsområdet i delen **Miljø** velger du flisen **E-fakturering**.</span><span class="sxs-lookup"><span data-stu-id="59972-154">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="59972-155">Opprette et tjenestemiljø</span><span class="sxs-lookup"><span data-stu-id="59972-155">Create a service environment</span></span>

1. <span data-ttu-id="59972-156">Velg **Tjenestemiljø** på siden **Miljøoppsett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="59972-156">On the **Environment setups** page, on the action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="59972-157">Velg **Ny** for å opprette et nytt tjenestemiljø.</span><span class="sxs-lookup"><span data-stu-id="59972-157">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="59972-158">I **Navn**-feltet angir du navnet på e-fakturamiljøet.</span><span class="sxs-lookup"><span data-stu-id="59972-158">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="59972-159">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="59972-159">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="59972-160">I feltet **Lagring av for SAS-tokenhemmelighet** velger du navnet på sertifikatet som må brukes til å godkjenne tilgang til lagringskontoen.</span><span class="sxs-lookup"><span data-stu-id="59972-160">In the **Storage SAS token secret** field, select the name of the certificate that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="59972-161">I **Brukere**-delen velger du **Legg til** for å legge til en bruker som har tillatelse til å sende elektroniske fakturaer gjennom miljøet og også koble seg til lagringskontoen.</span><span class="sxs-lookup"><span data-stu-id="59972-161">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="59972-162">I **Bruker-ID**-feltet angir du aliaset til brukeren.</span><span class="sxs-lookup"><span data-stu-id="59972-162">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="59972-163">Angi brukerens e-postadresse i feltet **E-post**.</span><span class="sxs-lookup"><span data-stu-id="59972-163">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="59972-164">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="59972-164">Select **Save**.</span></span>
8. <span data-ttu-id="59972-165">Hvis den land/område-spesifikke fakturaen krever en sertifikatkjede for å bruke digitale signaturer, velger du **Kjede av sertifikater** og deretter, i handlingsruten, velger du **Key Vault-hemmeligheter**, og følg deretter denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="59972-165">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="59972-166">Velg **Ny** for å opprette en kjede av sertifikater.</span><span class="sxs-lookup"><span data-stu-id="59972-166">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="59972-167">I **Navn**-feltet angir du navnet på kjeden av sertifikater.</span><span class="sxs-lookup"><span data-stu-id="59972-167">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="59972-168">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="59972-168">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="59972-169">I delen **Sertifikater** velger du **Legg til** for å legge til et sertifikat i kjeden.</span><span class="sxs-lookup"><span data-stu-id="59972-169">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="59972-170">Bruk knappene **Opp** eller **Ned** for å endre posisjonen til sertifikatene i kjeden.</span><span class="sxs-lookup"><span data-stu-id="59972-170">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="59972-171">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="59972-171">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="59972-172">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="59972-172">Close the page.</span></span>
9. <span data-ttu-id="59972-173">På siden **Tjenestemiljø**, i handlingsruten, velger du **Publiser** for å publisere miljøet til skyen.</span><span class="sxs-lookup"><span data-stu-id="59972-173">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="59972-174">Verdien i feltet **Status** endres til **Publisert**.</span><span class="sxs-lookup"><span data-stu-id="59972-174">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="59972-175">Opprette et tilkoblet program</span><span class="sxs-lookup"><span data-stu-id="59972-175">Create a connected application</span></span>

1. <span data-ttu-id="59972-176">Velg **Tilkoblede programmer** på siden **Miljøoppsett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="59972-176">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="59972-177">Velg **Ny** for å opprette et tilkoblet program.</span><span class="sxs-lookup"><span data-stu-id="59972-177">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="59972-178">I **Navn**-feltet angir du navnet på programmet som skal kobles til.</span><span class="sxs-lookup"><span data-stu-id="59972-178">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="59972-179">I feltet **Program** angir du URL-adressen til Finance- og Supply Chain Management-miljøet du vil koble til.</span><span class="sxs-lookup"><span data-stu-id="59972-179">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="59972-180">I feltet **Leietaker** angir du leietakeren i Finance- og Supply Chain Management-miljøet.</span><span class="sxs-lookup"><span data-stu-id="59972-180">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="59972-181">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="59972-181">Select **Save**.</span></span>
6. <span data-ttu-id="59972-182">Velg **Kontroller tilkobling** i handlingsruten for å teste tilkoblingen til miljøet.</span><span class="sxs-lookup"><span data-stu-id="59972-182">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="59972-183">Lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="59972-183">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="59972-184">Koble tilkoblede programmer til miljøer</span><span class="sxs-lookup"><span data-stu-id="59972-184">Link connected applications to environments</span></span>

1. <span data-ttu-id="59972-185">På siden **Miljøoppsett** velger du **Ny** for å tilordne et tilkoblet program til et miljø.</span><span class="sxs-lookup"><span data-stu-id="59972-185">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="59972-186">I feltet **Tilkoblet program** velger du det tilkoblede programmet.</span><span class="sxs-lookup"><span data-stu-id="59972-186">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="59972-187">Velg et tjenestemiljø i feltet **Servicemiljø**.</span><span class="sxs-lookup"><span data-stu-id="59972-187">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="59972-188">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="59972-188">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="59972-189">Konfigurere integrasjonen av tillegget Elektronisk fakturering i Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="59972-189">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="59972-190">Aktivere funksjonen for integrering av tillegget Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="59972-190">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="59972-191">Logg på Finance- eller Supply Chain Management-forekomsten din.</span><span class="sxs-lookup"><span data-stu-id="59972-191">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="59972-192">I arbeidsområdet **Funksjonsbehandling** søker du etter funksjonen **Integrasjon av tillegget Elektronisk fakturering**.</span><span class="sxs-lookup"><span data-stu-id="59972-192">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="59972-193">Hvis denne funksjonen ikke vises på siden, velger du **Se etter oppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="59972-193">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="59972-194">Velg funksjonen, og velg deretter **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="59972-194">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="59972-195">Konfigurer URL-adressen for endepunkt for tjeneste</span><span class="sxs-lookup"><span data-stu-id="59972-195">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="59972-196">Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="59972-196">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="59972-197">I kategorien **Innsendingstjeneste**, i feltet **URL for endepunkt for tjeneste**, angir du riktig tjenesteendepunkt for Azure-geografien, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="59972-197">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="59972-198">Datasenter Azure-geografi</span><span class="sxs-lookup"><span data-stu-id="59972-198">Datacenter Azure geography</span></span> | <span data-ttu-id="59972-199">URL for tjenestesluttpunkt</span><span class="sxs-lookup"><span data-stu-id="59972-199">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="59972-200">USA øst</span><span class="sxs-lookup"><span data-stu-id="59972-200">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="59972-201">USA vest</span><span class="sxs-lookup"><span data-stu-id="59972-201">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="59972-202">EU nord</span><span class="sxs-lookup"><span data-stu-id="59972-202">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="59972-203">EU vest</span><span class="sxs-lookup"><span data-stu-id="59972-203">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="59972-204">I **Miljø**-feltet angir du navnet på miljøet for tillegget Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="59972-204">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="59972-205">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="59972-205">Select **Save**, and then close the page.</span></span>
