---
title: Administrasjonskomponenter for elektronisk fakturering
description: Dette emnet inneholder informasjon om komponentene som er knyttet til administrasjon av Elektronisk fakturering.
author: gionoder
ms.date: 04/29/2021
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
ms.openlocfilehash: 3ac4a03d75898680b5655421f3024dc6f666464c
ms.sourcegitcommit: 54d3ec0c006bfa9d2b849590205be08551c4e0f0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/30/2021
ms.locfileid: "5963197"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="448d8-103">Administrasjonskomponenter for elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="448d8-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="448d8-104">Dette emnet inneholder informasjon om komponentene som er knyttet til administrasjon av Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="448d8-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="448d8-105">Det inneholder også informasjon om hvordan du konfigurerer Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="448d8-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="448d8-106">Azure</span><span class="sxs-lookup"><span data-stu-id="448d8-106">Azure</span></span>

<span data-ttu-id="448d8-107">Bruk Microsoft Azure for å opprette key vault-hemmelighetene og lagringskontoen.</span><span class="sxs-lookup"><span data-stu-id="448d8-107">Use Microsoft Azure to create the secrets for the Key Vault and storage account.</span></span> <span data-ttu-id="448d8-108">Deretter bruker du konfigurasjonen av Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="448d8-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="448d8-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="448d8-109">Lifecycle Services</span></span>

<span data-ttu-id="448d8-110">Bruk Microsoft Dynamics Lifecycle Services (LCS) til å aktivere mikrotjenestene på LCS-distribusjonsprosjektet.</span><span class="sxs-lookup"><span data-stu-id="448d8-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="448d8-111">Installasjonen av mikrotjenesten i LCS krever minst en virtuell maskin på nivå 2.</span><span class="sxs-lookup"><span data-stu-id="448d8-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="448d8-112">Hvis du vil ha mer informasjon om miljøplanlegging, kan du se [Miljøplanlegging](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="448d8-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="448d8-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="448d8-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="448d8-114">Dynamics 365 Regulatory Configuration Services (RCS) er grensesnittet som brukes til å konfigurere Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="448d8-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="448d8-115">Ressurser som miljøer og funksjoner for elektroniske fakturering opprettes, vedlikeholdes og driftes i RCS.</span><span class="sxs-lookup"><span data-stu-id="448d8-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="448d8-116">Når ressursene er klare, publiseres de i tjenesten for Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="448d8-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="448d8-117">For RCS-registrering kan du se [Regulatory Services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="448d8-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="448d8-118">Hvis du vil ha mer informasjon om RCS, kan du se [Regulatory Configuration Services (RCS) – globaliseringsfunksjoner](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="448d8-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="448d8-119">Integrering med Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="448d8-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="448d8-120">Før du kan bruke RCS til å konfigurere elektroniske fakturaer, må du konfigurere RCS til å tillate kommunikasjon med Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="448d8-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="448d8-121">Du fyller ut denne konfigurasjonen i kategorien **Elektronisk fakturering** på siden **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="448d8-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="448d8-122">Tjenestesluttpunkt</span><span class="sxs-lookup"><span data-stu-id="448d8-122">Service endpoint</span></span>

<span data-ttu-id="448d8-123">Elektronisk fakturering er tilgjengelig i flere geografiske områder for Azure-datasenteret.</span><span class="sxs-lookup"><span data-stu-id="448d8-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="448d8-124">I tabellen nedenfor finner du en oversikt over tilgjengelighet per område.</span><span class="sxs-lookup"><span data-stu-id="448d8-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="448d8-125">Azure-datasentergeografi</span><span class="sxs-lookup"><span data-stu-id="448d8-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="448d8-126">USA øst</span><span class="sxs-lookup"><span data-stu-id="448d8-126">East US</span></span>                    |
| <span data-ttu-id="448d8-127">USA vest</span><span class="sxs-lookup"><span data-stu-id="448d8-127">West US</span></span>                    |
| <span data-ttu-id="448d8-128">Europa, nord</span><span class="sxs-lookup"><span data-stu-id="448d8-128">North EU</span></span>                   |
| <span data-ttu-id="448d8-129">Europa, vest</span><span class="sxs-lookup"><span data-stu-id="448d8-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="448d8-130">Tjenestemiljøer</span><span class="sxs-lookup"><span data-stu-id="448d8-130">Service environments</span></span>

<span data-ttu-id="448d8-131">Tjenestemiljøer er logiske partisjoner som opprettes for å støtte utføring av funksjonene for elektronisk fakturering i Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="448d8-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="448d8-132">Sikkserhetshemmelighetene og de digitale sertifikatene, og styringen (det vil si tilgangstillatelser), må konfigureres på tjenestemiljønivå.</span><span class="sxs-lookup"><span data-stu-id="448d8-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="448d8-133">Kunder kan opprette så mange tjenestemiljøer de vil.</span><span class="sxs-lookup"><span data-stu-id="448d8-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="448d8-134">Alle tjenestemiljøene som en kunde oppretter, er uavhengige av hverandre.</span><span class="sxs-lookup"><span data-stu-id="448d8-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="448d8-135">Tjenestemiljøer må opprettes og vedlikeholdes i RCS.</span><span class="sxs-lookup"><span data-stu-id="448d8-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="448d8-136">Når tjenestemiljøene er klare, må de publiseres til Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="448d8-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="448d8-137">Tjenesemiljøstatus</span><span class="sxs-lookup"><span data-stu-id="448d8-137">Service environment status</span></span>

<span data-ttu-id="448d8-138">Tjenestemiljøer kan administreres via status.</span><span class="sxs-lookup"><span data-stu-id="448d8-138">Service environments can be managed through status.</span></span> <span data-ttu-id="448d8-139">Mulige alternativer er:</span><span class="sxs-lookup"><span data-stu-id="448d8-139">The possible options are:</span></span>

- <span data-ttu-id="448d8-140">**Ikke publisert** – Miljøet er opprettet, men det er ennå ikke publisert.</span><span class="sxs-lookup"><span data-stu-id="448d8-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="448d8-141">**Publisert** – Miljøet er publisert i Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="448d8-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="448d8-142">**Endret** – Attributtene for et publisert miljø er endret, men endringene er ikke publisert ennå.</span><span class="sxs-lookup"><span data-stu-id="448d8-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="448d8-143">Kundehemmeligheter</span><span class="sxs-lookup"><span data-stu-id="448d8-143">Customer secrets</span></span>

<span data-ttu-id="448d8-144">Tjenesten Elektronisk fakturering er ansvarlig for lagring av alle forretningsdata i Azure-ressursene som firmaet ditt eier.</span><span class="sxs-lookup"><span data-stu-id="448d8-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="448d8-145">For å sikre at tjenesten fungerer som den skal, og at det blir gitt tilgang til alle forretningsdataene som trengs for og genereres av Elektronisk fakturering, på riktig måte, må du opprette to hoved-Azure-ressurser:</span><span class="sxs-lookup"><span data-stu-id="448d8-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="448d8-146">En Azure Storage-konto (blob-lagring) som lagrer elektroniske fakturaer</span><span class="sxs-lookup"><span data-stu-id="448d8-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="448d8-147">Et Azure Key Vault som lagrer sertifikater og URIen (Uniform Resource Identifier) for lagringskontoen</span><span class="sxs-lookup"><span data-stu-id="448d8-147">An Azure Key Vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>


<span data-ttu-id="448d8-148">En dedikert Key Vault- og kundelagringskonto må tilordnes spesifikt for bruk med Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="448d8-148">A dedicated Key Vault and customer storage account must be allocated specifically for use with Electronic Invoicing.</span></span> <span data-ttu-id="448d8-149">Hvis du vil ha mer informasjon, kan du se [Opprette en Azure Storage-konto og et Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="448d8-149">For more information, see [Create an Azure storage account and a Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

<span data-ttu-id="448d8-150">Hvis du vil overvåke Key Vault-tilstanden og motta varsler, konfigurerer du Azure Monitor for key vault.</span><span class="sxs-lookup"><span data-stu-id="448d8-150">To monitor the health of your Key Vault and receive alerts, configure the Azure Monitor for key Vault.</span></span> <span data-ttu-id="448d8-151">Ved å aktivere Key Vault-logging kan du overvåke hvordan, når og hvem som har tilgang til dine Key Vaults.</span><span class="sxs-lookup"><span data-stu-id="448d8-151">By enabling Key Vault logging, you can monitor how, when, and by whom your Key Vaults are accessed.</span></span> <span data-ttu-id="448d8-152">Hvis du vil ha mer informasjon, kan du se [Overvåking og varsling for Azure Key Vault](/azure/key-vault/general/alert) og [Hvordan du aktiverer Key Vault-logging](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span><span class="sxs-lookup"><span data-stu-id="448d8-152">For more information, see [Monitoring and alerting for Azure Key Vault](/azure/key-vault/general/alert) and [How to enable Key Vault logging](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span></span>

<span data-ttu-id="448d8-153">Det er en god fremgangsmåte å rotere hemmeligheter med jevne mellomrom.</span><span class="sxs-lookup"><span data-stu-id="448d8-153">As a best practice, periodically rotate the secrets.</span></span> <span data-ttu-id="448d8-154">Hvis du vil ha mer informasjon, kan du se i [Hemmelighetsdokumentasjon](/azure/key-vault/secrets/).</span><span class="sxs-lookup"><span data-stu-id="448d8-154">For more information, see [Secrets documentation](/azure/key-vault/secrets/).</span></span>

#### <a name="users"></a><span data-ttu-id="448d8-155">Brukere</span><span class="sxs-lookup"><span data-stu-id="448d8-155">Users</span></span>

<span data-ttu-id="448d8-156">Hvert tjenestemiljø må vise en liste over brukerne som kan koble seg til fra Dynamics 365 Finance og Dynamics 365 Supply Chain Management i Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="448d8-156">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="448d8-157">Publisering</span><span class="sxs-lookup"><span data-stu-id="448d8-157">Publication</span></span>

<span data-ttu-id="448d8-158">Tjenestemiljøene må de publiseres til Elektronisk fakturering før de kan brukes.</span><span class="sxs-lookup"><span data-stu-id="448d8-158">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="448d8-159">Det er bare tilgang til publiserte miljøer fra Finance og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="448d8-159">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="448d8-160">I tillegg må et tjenestemiljø publiseres før eventuelle oppdateringer av attributtene trer i kraft på den elektroniske faktureringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="448d8-160">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="448d8-161">Tilkoblede programmer</span><span class="sxs-lookup"><span data-stu-id="448d8-161">Connected applications</span></span>

<span data-ttu-id="448d8-162">Tilkoblede programmer er forekomstene av Finance og Supply Chain Management som du kanskje vil nå gjennom RCS.</span><span class="sxs-lookup"><span data-stu-id="448d8-162">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="448d8-163">I tillegg til program-URLen og leietakeren inneholder et tilkoblet program legitimasjon som gjør at RCS kan koble seg til miljøet.</span><span class="sxs-lookup"><span data-stu-id="448d8-163">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="448d8-164">Gjennom de tilkoblede programmene kan du konfigurere deler av Elektronisk fakturering-funksjonen i Finance og Supply Chain Management for å få hele Elektronisk fakturering-funksjonen til å fungere.</span><span class="sxs-lookup"><span data-stu-id="448d8-164">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="448d8-165">Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="448d8-165">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="448d8-166">Integrering med Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="448d8-166">Integration with Electronic invoicing</span></span>

<span data-ttu-id="448d8-167">Før du kan bruke Finance og Supply Chain Management til å utstede elektroniske fakturaer via Elektronisk fakturering, må det konfigureres slik at det er tillatt å kommunisere med tjenesten.</span><span class="sxs-lookup"><span data-stu-id="448d8-167">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="448d8-168">Integreringsfunksjon for Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="448d8-168">Electronic invoicing integration feature</span></span>

<span data-ttu-id="448d8-169">Hvis du vil aktivere kommunikasjon mellom Finance og Supply Chain Management og Elektronisk fakturering, må du aktivere funksjonen for **Integrering av Elektronisk fakturering** i arbeidsområdet for **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="448d8-169">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="448d8-170">Tjenestesluttpunkt</span><span class="sxs-lookup"><span data-stu-id="448d8-170">Service endpoint</span></span>

<span data-ttu-id="448d8-171">Endepunktet for tjeneste er URL-adressen der Elektronisk fakturering er plassert.</span><span class="sxs-lookup"><span data-stu-id="448d8-171">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="448d8-172">Før du elektroniske fakturaer kan utstedet må endepunktet for tjenesten konfigurere i Finance og Supply Chain Management, slik at det er tillatt å kommunisere med tjenesten.</span><span class="sxs-lookup"><span data-stu-id="448d8-172">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="448d8-173">For å konfigurere tjenestesluttpunktet, kan du gå til **Organisasjonsadministrasjon \> Oppsett \> parametere for elektronisk dokument**, og deretter, i fanen **Innsendingstjenester** i feltet **URL for Elektronisk faktura**, angir du URL-en som beskrevet i tabellen som er beskrevet i delen **Tjenestesluttpunkt**.</span><span class="sxs-lookup"><span data-stu-id="448d8-173">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="448d8-174">Miljøer</span><span class="sxs-lookup"><span data-stu-id="448d8-174">Environments</span></span>

<span data-ttu-id="448d8-175">Miljønavnet som angis i Finance og Supply Chain Management, refererer til navnet på miljøet som opprettes i RCS og publiseres i Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="448d8-175">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="448d8-176">Miljøet må konfigureres i kategorien **Innsendingstjenester** på siden **Parameter for elektronisk dokument**, slik at hver forespørsel om å utstede elektroniske fakturaer, inneholder miljøet der Elektronisk fakturering kan fastslå hvilken elektronisk faktureringsfunksjon som må behandle forespørselen.</span><span class="sxs-lookup"><span data-stu-id="448d8-176">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="448d8-177">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="448d8-177">Additional resources</span></span>

- [<span data-ttu-id="448d8-178">Konfigurere elektroniske fakturaer i RCS</span><span class="sxs-lookup"><span data-stu-id="448d8-178">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="448d8-179">Utstede elektroniske fakturaer i Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="448d8-179">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
