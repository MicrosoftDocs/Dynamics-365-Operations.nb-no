---
title: Administrasjonskomponenter for elektronisk fakturering
description: Dette emnet inneholder informasjon om komponentene som er knyttet til administrasjon av Elektronisk fakturering.
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
ms.openlocfilehash: 2e859875e124796e49000cd5ea94cfb75ecd768a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840034"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="d2d6d-103">Administrasjonskomponenter for elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="d2d6d-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d2d6d-104">Dette emnet inneholder informasjon om komponentene som er knyttet til administrasjon av Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="d2d6d-105">Det inneholder også informasjon om hvordan du konfigurerer Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="d2d6d-106">Azure</span><span class="sxs-lookup"><span data-stu-id="d2d6d-106">Azure</span></span>

<span data-ttu-id="d2d6d-107">Bruk Microsoft Azure for å opprette key vault-hemmelighetene og lagringskontoen.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="d2d6d-108">Deretter bruker du konfigurasjonen av Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="d2d6d-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="d2d6d-109">Lifecycle Services</span></span>

<span data-ttu-id="d2d6d-110">Bruk Microsoft Dynamics Lifecycle Services (LCS) til å aktivere mikrotjenestene på LCS-distribusjonsprosjektet.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="d2d6d-111">Installasjonen av mikrotjenesten i LCS krever minst en virtuell maskin på nivå 2.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="d2d6d-112">Hvis du vil ha mer informasjon om miljøplanlegging, kan du se [Miljøplanlegging](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="d2d6d-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="d2d6d-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="d2d6d-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="d2d6d-114">Dynamics 365 Regulatory Configuration Services (RCS) er grensesnittet som brukes til å konfigurere Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="d2d6d-115">Ressurser som miljøer og funksjoner for elektroniske fakturering opprettes, vedlikeholdes og driftes i RCS.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="d2d6d-116">Når ressursene er klare, publiseres de i tjenesten for Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="d2d6d-117">For RCS-registrering kan du se [Regulatory Services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="d2d6d-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="d2d6d-118">Hvis du vil ha mer informasjon om RCS, kan du se [Regulatory Configuration Services (RCS) – globaliseringsfunksjoner](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="d2d6d-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="d2d6d-119">Integrering med Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="d2d6d-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="d2d6d-120">Før du kan bruke RCS til å konfigurere elektroniske fakturaer, må du konfigurere RCS til å tillate kommunikasjon med Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="d2d6d-121">Du fyller ut denne konfigurasjonen i kategorien **Elektronisk fakturering** på siden **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="d2d6d-122">Tjenestesluttpunkt</span><span class="sxs-lookup"><span data-stu-id="d2d6d-122">Service endpoint</span></span>

<span data-ttu-id="d2d6d-123">Elektronisk fakturering er tilgjengelig i flere geografiske områder for Azure-datasenteret.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="d2d6d-124">I tabellen nedenfor finner du en oversikt over tilgjengelighet per område.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="d2d6d-125">Azure-datasentergeografi</span><span class="sxs-lookup"><span data-stu-id="d2d6d-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="d2d6d-126">USA øst</span><span class="sxs-lookup"><span data-stu-id="d2d6d-126">East US</span></span>                    |
| <span data-ttu-id="d2d6d-127">USA vest</span><span class="sxs-lookup"><span data-stu-id="d2d6d-127">West US</span></span>                    |
| <span data-ttu-id="d2d6d-128">Europa, nord</span><span class="sxs-lookup"><span data-stu-id="d2d6d-128">North EU</span></span>                   |
| <span data-ttu-id="d2d6d-129">Europa, vest</span><span class="sxs-lookup"><span data-stu-id="d2d6d-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="d2d6d-130">Tjenestemiljøer</span><span class="sxs-lookup"><span data-stu-id="d2d6d-130">Service environments</span></span>

<span data-ttu-id="d2d6d-131">Tjenestemiljøer er logiske partisjoner som opprettes for å støtte utføring av funksjonene for elektronisk fakturering i Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="d2d6d-132">Sikkserhetshemmelighetene og de digitale sertifikatene, og styringen (det vil si tilgangstillatelser), må konfigureres på tjenestemiljønivå.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="d2d6d-133">Kunder kan opprette så mange tjenestemiljøer de vil.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="d2d6d-134">Alle tjenestemiljøene som en kunde oppretter, er uavhengige av hverandre.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="d2d6d-135">Tjenestemiljøer må opprettes og vedlikeholdes i RCS.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="d2d6d-136">Når tjenestemiljøene er klare, må de publiseres til Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="d2d6d-137">Tjenesemiljøstatus</span><span class="sxs-lookup"><span data-stu-id="d2d6d-137">Service environment status</span></span>

<span data-ttu-id="d2d6d-138">Tjenestemiljøer kan administreres via status.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-138">Service environments can be managed through status.</span></span> <span data-ttu-id="d2d6d-139">Mulige alternativer er:</span><span class="sxs-lookup"><span data-stu-id="d2d6d-139">The possible options are:</span></span>

- <span data-ttu-id="d2d6d-140">**Ikke publisert** – Miljøet er opprettet, men det er ennå ikke publisert.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="d2d6d-141">**Publisert** – Miljøet er publisert i Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="d2d6d-142">**Endret** – Attributtene for et publisert miljø er endret, men endringene er ikke publisert ennå.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="d2d6d-143">Kundehemmeligheter</span><span class="sxs-lookup"><span data-stu-id="d2d6d-143">Customer secrets</span></span>

<span data-ttu-id="d2d6d-144">Tjenesten Elektronisk fakturering er ansvarlig for lagring av alle forretningsdata i Azure-ressursene som firmaet ditt eier.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="d2d6d-145">For å sikre at tjenesten fungerer som den skal, og at det blir gitt tilgang til alle forretningsdataene som trengs for og genereres av Elektronisk fakturering, på riktig måte, må du opprette to hoved-Azure-ressurser:</span><span class="sxs-lookup"><span data-stu-id="d2d6d-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="d2d6d-146">En Azure Storage-konto (blob-lagring) som lagrer elektroniske fakturaer</span><span class="sxs-lookup"><span data-stu-id="d2d6d-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="d2d6d-147">Et Azure Key Vault som lagrer sertifikater og URIen (Uniform Resource Identifier) for lagringskontoen</span><span class="sxs-lookup"><span data-stu-id="d2d6d-147">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="d2d6d-148">En dedikert Key Vault- og kundelagringskonto må tilordnes spesifikt for bruk med Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-148">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing .</span></span>

<span data-ttu-id="d2d6d-149">Hvis du vil ha mer informasjon, kan du se [Opprette en Azure Storage-konto og et Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="d2d6d-149">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="d2d6d-150">Brukere</span><span class="sxs-lookup"><span data-stu-id="d2d6d-150">Users</span></span>

<span data-ttu-id="d2d6d-151">Hvert tjenestemiljø må vise en liste over brukerne som kan koble seg til fra Dynamics 365 Finance og Dynamics 365 Supply Chain Management i Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-151">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="d2d6d-152">Publisering</span><span class="sxs-lookup"><span data-stu-id="d2d6d-152">Publication</span></span>

<span data-ttu-id="d2d6d-153">Tjenestemiljøene må de publiseres til Elektronisk fakturering før de kan brukes.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-153">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="d2d6d-154">Det er bare tilgang til publiserte miljøer fra Finance og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-154">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="d2d6d-155">I tillegg må et tjenestemiljø publiseres før eventuelle oppdateringer av attributtene trer i kraft på den elektroniske faktureringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-155">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="d2d6d-156">Tilkoblede programmer</span><span class="sxs-lookup"><span data-stu-id="d2d6d-156">Connected applications</span></span>

<span data-ttu-id="d2d6d-157">Tilkoblede programmer er forekomstene av Finance og Supply Chain Management som du kanskje vil nå gjennom RCS.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-157">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="d2d6d-158">I tillegg til program-URLen og leietakeren inneholder et tilkoblet program legitimasjon som gjør at RCS kan koble seg til miljøet.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-158">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="d2d6d-159">Gjennom de tilkoblede programmene kan du konfigurere deler av Elektronisk fakturering-funksjonen i Finance og Supply Chain Management for å få hele Elektronisk fakturering-funksjonen til å fungere.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-159">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="d2d6d-160">Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d2d6d-160">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="d2d6d-161">Integrering med Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="d2d6d-161">Integration with Electronic invoicing</span></span>

<span data-ttu-id="d2d6d-162">Før du kan bruke Finance og Supply Chain Management til å utstede elektroniske fakturaer via Elektronisk fakturering, må det konfigureres slik at det er tillatt å kommunisere med tjenesten.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-162">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="d2d6d-163">Integreringsfunksjon for Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="d2d6d-163">Electronic invoicing integration feature</span></span>

<span data-ttu-id="d2d6d-164">Hvis du vil aktivere kommunikasjon mellom Finance og Supply Chain Management og Elektronisk fakturering, må du aktivere funksjonen for **Integrering av Elektronisk fakturering** i arbeidsområdet for **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-164">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="d2d6d-165">Tjenestesluttpunkt</span><span class="sxs-lookup"><span data-stu-id="d2d6d-165">Service endpoint</span></span>

<span data-ttu-id="d2d6d-166">Endepunktet for tjeneste er URL-adressen der Elektronisk fakturering er plassert.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-166">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="d2d6d-167">Før du elektroniske fakturaer kan utstedet må endepunktet for tjenesten konfigurere i Finance og Supply Chain Management, slik at det er tillatt å kommunisere med tjenesten.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-167">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="d2d6d-168">For å konfigurere tjenestesluttpunktet, kan du gå til **Organisasjonsadministrasjon \> Oppsett \> parametere for elektronisk dokument**, og deretter, i fanen **Innsendingstjenester** i feltet **URL for Elektronisk faktura**, angir du URL-en som beskrevet i tabellen som er beskrevet i delen **Tjenestesluttpunkt**.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-168">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="d2d6d-169">Miljøer</span><span class="sxs-lookup"><span data-stu-id="d2d6d-169">Environments</span></span>

<span data-ttu-id="d2d6d-170">Miljønavnet som angis i Finance og Supply Chain Management, refererer til navnet på miljøet som opprettes i RCS og publiseres i Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-170">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="d2d6d-171">Miljøet må konfigureres i kategorien **Innsendingstjenester** på siden **Parameter for elektronisk dokument**, slik at hver forespørsel om å utstede elektroniske fakturaer, inneholder miljøet der Elektronisk fakturering kan fastslå hvilken elektronisk faktureringsfunksjon som må behandle forespørselen.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-171">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d2d6d-172">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d2d6d-172">Additional resources</span></span>

- [<span data-ttu-id="d2d6d-173">Konfigurere elektroniske fakturaer i RCS</span><span class="sxs-lookup"><span data-stu-id="d2d6d-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="d2d6d-174">Utstede elektroniske fakturaer i Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d2d6d-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
