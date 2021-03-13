---
title: Administrasjonskomponenter for Elektronisk fakturering-tillegget
description: Dette emnet inneholder informasjon om komponentene som er knyttet til administrasjon av tillegget Elektronisk fakturering.
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
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104420"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="eae3c-103">Administrasjonskomponenter for Elektronisk fakturering-tillegget</span><span class="sxs-lookup"><span data-stu-id="eae3c-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="eae3c-104">Dette emnet inneholder informasjon om komponentene som er knyttet til administrasjon av tillegget Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="eae3c-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="eae3c-105">Det inneholder også informasjon om hvordan du konfigurerer tillegget for Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="eae3c-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="eae3c-106">Azure</span><span class="sxs-lookup"><span data-stu-id="eae3c-106">Azure</span></span>

<span data-ttu-id="eae3c-107">Bruk Microsoft Azure for å opprette key vault-hemmelighetene og lagringskontoen.</span><span class="sxs-lookup"><span data-stu-id="eae3c-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="eae3c-108">Deretter bruker du konfigurasjonen av tillegget for Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="eae3c-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="eae3c-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="eae3c-109">Lifecycle Services</span></span>

<span data-ttu-id="eae3c-110">Bruk Microsoft Dynamics Lifecycle Services (LCS) til å aktivere tillegget for mikrotjenestene på LCS-distribusjonsprosjektet.</span><span class="sxs-lookup"><span data-stu-id="eae3c-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

<span data-ttu-id="eae3c-111">I LCS velger du flisen **Administrasjon av forhåndsvisningsfunksjoner**, og deretter aktiverer du funksjonen **E-faktureringstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="eae3c-111">In LCS, select the **Preview feature management** tile, and then turn on the **e-Invoicing Service** feature.</span></span>

## <a name="regulatory-configuration-services"></a><span data-ttu-id="eae3c-112">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="eae3c-112">Regulatory Configuration Services</span></span>

<span data-ttu-id="eae3c-113">Dynamics 365 Regulatory Configuration Services (RCS) er grensesnittet som brukes til å konfigurere tillegget for Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="eae3c-113">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="eae3c-114">Ressurser som miljøer og funksjoner for elektroniske fakturering opprettes, vedlikeholdes og driftes i RCS.</span><span class="sxs-lookup"><span data-stu-id="eae3c-114">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="eae3c-115">Når ressursene er klare, publiseres de i tilleggstjenesten for Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="eae3c-115">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="eae3c-116">Hvis du vil ha mer informasjon om RCS, kan du se [Regulatory Configuration Services (RCS) – globaliseringsfunksjoner](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="eae3c-116">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="eae3c-117">Integrering med Elektronisk fakturering-tillegget</span><span class="sxs-lookup"><span data-stu-id="eae3c-117">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="eae3c-118">Før du kan bruke RCS til å konfigurere elektroniske fakturaer, må du konfigurere RCS til å tillate kommunikasjon med tillegget for Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="eae3c-118">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="eae3c-119">Du fyller ut denne konfigurasjonen i kategorien **Tillegg for elektronisk fakturering** på siden **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="eae3c-119">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="eae3c-120">Tjenestesluttpunkt</span><span class="sxs-lookup"><span data-stu-id="eae3c-120">Service endpoint</span></span>

<span data-ttu-id="eae3c-121">URL-adressen til tillegget for Elektronisk fakturering kan variere i henhold til den geografiske plasseringen til Azure-datasenteret.</span><span class="sxs-lookup"><span data-stu-id="eae3c-121">The URL of the Electronic invoicing add-on endpoint can vary according to the Azure datacenter geography.</span></span> <span data-ttu-id="eae3c-122">I tabellen nedenfor finner du en oversikt over tilgjengelighet per område:</span><span class="sxs-lookup"><span data-stu-id="eae3c-122">The following table lists the availability per region:</span></span>

| <span data-ttu-id="eae3c-123">Azure-datasentergeografi</span><span class="sxs-lookup"><span data-stu-id="eae3c-123">Azure datacenter geography</span></span> | <span data-ttu-id="eae3c-124">URL for tjenestesluttpunkt</span><span class="sxs-lookup"><span data-stu-id="eae3c-124">Service endpoint URL</span></span>                                                       |
|----------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="eae3c-125">USA øst</span><span class="sxs-lookup"><span data-stu-id="eae3c-125">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="eae3c-126">USA vest</span><span class="sxs-lookup"><span data-stu-id="eae3c-126">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="eae3c-127">Europa, nord</span><span class="sxs-lookup"><span data-stu-id="eae3c-127">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="eae3c-128">Europa, vest</span><span class="sxs-lookup"><span data-stu-id="eae3c-128">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a><span data-ttu-id="eae3c-129">App-ID</span><span class="sxs-lookup"><span data-stu-id="eae3c-129">Application ID</span></span>

<span data-ttu-id="eae3c-130">Program-IDen er IDen for programmet for Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="eae3c-130">The application ID is the ID of the Electronic invoicing add-on application.</span></span> <span data-ttu-id="eae3c-131">I dette tilfellet er verdien fast: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="eae3c-131">In this case, the value is fixed: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

#### <a name="lcs-environment-id"></a><span data-ttu-id="eae3c-132">LCS-miljø-ID</span><span class="sxs-lookup"><span data-stu-id="eae3c-132">LCS environment ID</span></span>

<span data-ttu-id="eae3c-133">LCS-miljø-IDen er IDen for organisasjonens LCS-abonnement.</span><span class="sxs-lookup"><span data-stu-id="eae3c-133">The LCS environment ID is the ID of your organization's LCS subscription.</span></span>

### <a name="service-environments"></a><span data-ttu-id="eae3c-134">Tjenestemiljøer</span><span class="sxs-lookup"><span data-stu-id="eae3c-134">Service environments</span></span>

<span data-ttu-id="eae3c-135">Tjenestemiljøer er logiske partisjoner som opprettes for å støtte utføring av funksjonene for Elektronisk fakturering i tillegget for Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="eae3c-135">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="eae3c-136">Sikkserhetshemmelighetene og de digitale sertifikatene, og styringen (det vil si tilgangstillatelser), må konfigureres på tjenestemiljønivå.</span><span class="sxs-lookup"><span data-stu-id="eae3c-136">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="eae3c-137">Kunder kan opprette så mange tjenestemiljøer de vil.</span><span class="sxs-lookup"><span data-stu-id="eae3c-137">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="eae3c-138">Alle tjenestemiljøene som en kunde oppretter, er uavhengige av hverandre.</span><span class="sxs-lookup"><span data-stu-id="eae3c-138">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="eae3c-139">Tjenestemiljøer må opprettes og vedlikeholdes i RCS.</span><span class="sxs-lookup"><span data-stu-id="eae3c-139">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="eae3c-140">Når tjenestemiljøene er klare, må de publiseres til Elektronisk fakturering-tillegget.</span><span class="sxs-lookup"><span data-stu-id="eae3c-140">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="eae3c-141">Tjenesemiljøstatus</span><span class="sxs-lookup"><span data-stu-id="eae3c-141">Service environment status</span></span>

<span data-ttu-id="eae3c-142">Tjenestemiljøer kan administreres via status.</span><span class="sxs-lookup"><span data-stu-id="eae3c-142">Service environments can be managed through status.</span></span> <span data-ttu-id="eae3c-143">Mulige alternativer er:</span><span class="sxs-lookup"><span data-stu-id="eae3c-143">The possible options are:</span></span>

- <span data-ttu-id="eae3c-144">**Ikke publisert** – Miljøet er opprettet, men det er ennå ikke publisert.</span><span class="sxs-lookup"><span data-stu-id="eae3c-144">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="eae3c-145">**Publisert** – Miljøet er publisert i tillegget for Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="eae3c-145">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="eae3c-146">**Endret** – Attributtene for et publisert miljø er endret, men endringene er ikke publisert ennå.</span><span class="sxs-lookup"><span data-stu-id="eae3c-146">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="eae3c-147">Kundehemmeligheter</span><span class="sxs-lookup"><span data-stu-id="eae3c-147">Customer secrets</span></span>

<span data-ttu-id="eae3c-148">Tillegget Elektronisk fakturering er ansvarlig for lagring av alle forretningsdata i Azure-ressursene som firmaet ditt eier.</span><span class="sxs-lookup"><span data-stu-id="eae3c-148">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="eae3c-149">For å sikre at tjenesten fungerer som den skal, og at alle forretningsdataene som trengs for og genereres av tillegget Elektronisk fakturering, bare åpnes av tillegget, må du opprette to hoved-Azure-ressurser:</span><span class="sxs-lookup"><span data-stu-id="eae3c-149">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="eae3c-150">En Azure Storage-konto (blob-lagring) som lagrer elektroniske fakturaer</span><span class="sxs-lookup"><span data-stu-id="eae3c-150">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="eae3c-151">Et Azure Key Vault som lagrer sertifikater og URIen (Uniform Resource Identifier) for lagringskontoen</span><span class="sxs-lookup"><span data-stu-id="eae3c-151">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="eae3c-152">En dedikert Key Vault- og kundelagringskonto må tilordnes spesifikt for bruk med tillegget Elektroniske fakturering.</span><span class="sxs-lookup"><span data-stu-id="eae3c-152">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="eae3c-153">Hvis du vil ha mer informasjon, kan du se [Opprette en Azure Storage-konto og et Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="eae3c-153">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="eae3c-154">Brukere</span><span class="sxs-lookup"><span data-stu-id="eae3c-154">Users</span></span>

<span data-ttu-id="eae3c-155">Hvert tjenestemiljø må vise en liste over brukerne som kan koble seg til fra Dynamics 365 Finance og Dynamics 365 Supply Chain Management i Elektronisk fakturering-tillegget.</span><span class="sxs-lookup"><span data-stu-id="eae3c-155">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="eae3c-156">Publisering</span><span class="sxs-lookup"><span data-stu-id="eae3c-156">Publication</span></span>

<span data-ttu-id="eae3c-157">Tjenestemiljøene må de publiseres til Elektronisk fakturering-tillegget før de kan brukes.</span><span class="sxs-lookup"><span data-stu-id="eae3c-157">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="eae3c-158">Det er bare tilgang til publiserte miljøer fra Finance og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="eae3c-158">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="eae3c-159">I tillegg må et tjenestemiljø publiseres før eventuelle oppdateringer av attributtene trer i kraft på den elektroniske faktureringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="eae3c-159">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="eae3c-160">Tilkoblede programmer</span><span class="sxs-lookup"><span data-stu-id="eae3c-160">Connected applications</span></span>

<span data-ttu-id="eae3c-161">Tilkoblede programmer er forekomstene av Finance og Supply Chain Management som du kanskje vil nå gjennom RCS.</span><span class="sxs-lookup"><span data-stu-id="eae3c-161">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="eae3c-162">I tillegg til program-URLen og leietakeren inneholder et tilkoblet program legitimasjon som gjør at RCS kan koble seg til miljøet.</span><span class="sxs-lookup"><span data-stu-id="eae3c-162">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="eae3c-163">Gjennom de tilkoblede programmene kan du konfigurere deler av Elektronisk fakturering-funksjonen i Finance og Supply Chain Management for å få hele Elektronisk fakturering-funksjonen til å fungere.</span><span class="sxs-lookup"><span data-stu-id="eae3c-163">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="eae3c-164">Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="eae3c-164">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="eae3c-165">Integrering med Elektronisk fakturering-tillegg</span><span class="sxs-lookup"><span data-stu-id="eae3c-165">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="eae3c-166">Før du kan bruke Finance og Supply Chain Management til å utstede elektroniske fakturaer via tillegget for Elektronisk fakturering, må tillegget konfigureres slik at det er tillatt å kommunisere med tjenesten.</span><span class="sxs-lookup"><span data-stu-id="eae3c-166">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="eae3c-167">Integreringsfunksjon for tillegget Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="eae3c-167">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="eae3c-168">Hvis du vil aktivere kommunikasjon mellom Finance og Supply Chain Management og tillegget for Elektronisk fakturering, må du aktivere funksjonen for **Integrering av tillegget Elektronisk fakturering** i arbeidsområdet for **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="eae3c-168">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="eae3c-169">Tjenestesluttpunkt</span><span class="sxs-lookup"><span data-stu-id="eae3c-169">Service endpoint</span></span>

<span data-ttu-id="eae3c-170">Endepunktet for tjeneste er URL-adressen der tillegget for Elektronisk fakturering er plassert.</span><span class="sxs-lookup"><span data-stu-id="eae3c-170">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="eae3c-171">Før du elektroniske fakturaer kan utstedet må endepunktet for tjenesten konfigurere i Finance og Supply Chain Management, slik at det er tillatt å kommunisere med tjenesten.</span><span class="sxs-lookup"><span data-stu-id="eae3c-171">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="eae3c-172">For å konfigurere tjenestesluttpunktet, kan du gå til **Organisasjonsadministrasjon \> Oppsett \> parametere for elektronisk dokument**, og deretter, i fanen **Innsendingstjenester** i feltet **URL for tillegg for Elektronisk faktura**, angir du URL-en som beskrevet i tabellen som er beskrevet i delen **Tjenestesluttpunkt**.</span><span class="sxs-lookup"><span data-stu-id="eae3c-172">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="eae3c-173">Miljøer</span><span class="sxs-lookup"><span data-stu-id="eae3c-173">Environments</span></span>

<span data-ttu-id="eae3c-174">Miljønavnet som angis i Finance og Supply Chain Management, refererer til navnet på miljøet som opprettes i RCS og publiseres i tillegget til Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="eae3c-174">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="eae3c-175">Miljøet må konfigureres i kategorien **Innsendingstjenester** på siden **Parameter for elektronisk dokument**, slik at hver forespørsel om å utstede elektroniske fakturaer, inneholder miljøet der tillegget for Elektronisk fakturering kan fastslå hvilken elektronisk faktureringsfunksjon som må behandle forespørselen.</span><span class="sxs-lookup"><span data-stu-id="eae3c-175">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eae3c-176">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="eae3c-176">Additional resources</span></span>

- [<span data-ttu-id="eae3c-177">Konfigurere elektroniske fakturaer i RCS</span><span class="sxs-lookup"><span data-stu-id="eae3c-177">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="eae3c-178">Utstede elektroniske fakturaer i Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="eae3c-178">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)
