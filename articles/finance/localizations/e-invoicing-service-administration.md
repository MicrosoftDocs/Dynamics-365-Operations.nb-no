---
title: Administrasjonskomponenter for Elektronisk fakturering-tillegget
description: Dette emnet inneholder informasjon om komponentene som er knyttet til administrasjon av tillegget Elektronisk fakturering.
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
ms.openlocfilehash: 70ef47dd45200a14c9d780f3c280c554d0e52ac3
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592580"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="329b3-103">Administrasjonskomponenter for Elektronisk fakturering-tillegget</span><span class="sxs-lookup"><span data-stu-id="329b3-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="329b3-104">Dette emnet inneholder informasjon om komponentene som er knyttet til administrasjon av tillegget Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="329b3-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="329b3-105">Det inneholder også informasjon om hvordan du konfigurerer tillegget for Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="329b3-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="329b3-106">Azure</span><span class="sxs-lookup"><span data-stu-id="329b3-106">Azure</span></span>

<span data-ttu-id="329b3-107">Bruk Microsoft Azure for å opprette key vault-hemmelighetene og lagringskontoen.</span><span class="sxs-lookup"><span data-stu-id="329b3-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="329b3-108">Deretter bruker du konfigurasjonen av tillegget for Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="329b3-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="329b3-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="329b3-109">Lifecycle Services</span></span>

<span data-ttu-id="329b3-110">Bruk Microsoft Dynamics Lifecycle Services (LCS) til å aktivere tillegget for mikrotjenestene på LCS-distribusjonsprosjektet.</span><span class="sxs-lookup"><span data-stu-id="329b3-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="329b3-111">Installasjonen av mikrotjenestetillegget i LCS krever minst en virtuell maskin på nivå 2.</span><span class="sxs-lookup"><span data-stu-id="329b3-111">The installation of the microservice add-on in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="329b3-112">Hvis du vil ha mer informasjon om miljøplanlegging, kan du se [Miljøplanlegging](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="329b3-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="329b3-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="329b3-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="329b3-114">Dynamics 365 Regulatory Configuration Services (RCS) er grensesnittet som brukes til å konfigurere tillegget for Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="329b3-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="329b3-115">Ressurser som miljøer og funksjoner for elektroniske fakturering opprettes, vedlikeholdes og driftes i RCS.</span><span class="sxs-lookup"><span data-stu-id="329b3-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="329b3-116">Når ressursene er klare, publiseres de i tilleggstjenesten for Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="329b3-116">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="329b3-117">For RCS-registrering kan du se [Regulatory Services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="329b3-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="329b3-118">Hvis du vil ha mer informasjon om RCS, kan du se [Regulatory Configuration Services (RCS) – globaliseringsfunksjoner](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="329b3-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="329b3-119">Integrering med Elektronisk fakturering-tillegget</span><span class="sxs-lookup"><span data-stu-id="329b3-119">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="329b3-120">Før du kan bruke RCS til å konfigurere elektroniske fakturaer, må du konfigurere RCS til å tillate kommunikasjon med tillegget for Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="329b3-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="329b3-121">Du fyller ut denne konfigurasjonen i kategorien **Tillegg for elektronisk fakturering** på siden **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="329b3-121">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="329b3-122">Tjenestesluttpunkt</span><span class="sxs-lookup"><span data-stu-id="329b3-122">Service endpoint</span></span>

<span data-ttu-id="329b3-123">Tillegget for elektronisk fakturering er tilgjengelig i flere geografiske områder for Azure-datasenteret.</span><span class="sxs-lookup"><span data-stu-id="329b3-123">The Electronic invoicing add-on is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="329b3-124">I tabellen nedenfor finner du en oversikt over tilgjengelighet per område.</span><span class="sxs-lookup"><span data-stu-id="329b3-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="329b3-125">Azure-datasentergeografi</span><span class="sxs-lookup"><span data-stu-id="329b3-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="329b3-126">USA øst</span><span class="sxs-lookup"><span data-stu-id="329b3-126">East US</span></span>                    |
| <span data-ttu-id="329b3-127">USA vest</span><span class="sxs-lookup"><span data-stu-id="329b3-127">West US</span></span>                    |
| <span data-ttu-id="329b3-128">Europa, nord</span><span class="sxs-lookup"><span data-stu-id="329b3-128">North EU</span></span>                   |
| <span data-ttu-id="329b3-129">Europa, vest</span><span class="sxs-lookup"><span data-stu-id="329b3-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="329b3-130">Tjenestemiljøer</span><span class="sxs-lookup"><span data-stu-id="329b3-130">Service environments</span></span>

<span data-ttu-id="329b3-131">Tjenestemiljøer er logiske partisjoner som opprettes for å støtte utføring av funksjonene for Elektronisk fakturering i tillegget for Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="329b3-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="329b3-132">Sikkserhetshemmelighetene og de digitale sertifikatene, og styringen (det vil si tilgangstillatelser), må konfigureres på tjenestemiljønivå.</span><span class="sxs-lookup"><span data-stu-id="329b3-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="329b3-133">Kunder kan opprette så mange tjenestemiljøer de vil.</span><span class="sxs-lookup"><span data-stu-id="329b3-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="329b3-134">Alle tjenestemiljøene som en kunde oppretter, er uavhengige av hverandre.</span><span class="sxs-lookup"><span data-stu-id="329b3-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="329b3-135">Tjenestemiljøer må opprettes og vedlikeholdes i RCS.</span><span class="sxs-lookup"><span data-stu-id="329b3-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="329b3-136">Når tjenestemiljøene er klare, må de publiseres til Elektronisk fakturering-tillegget.</span><span class="sxs-lookup"><span data-stu-id="329b3-136">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="329b3-137">Tjenesemiljøstatus</span><span class="sxs-lookup"><span data-stu-id="329b3-137">Service environment status</span></span>

<span data-ttu-id="329b3-138">Tjenestemiljøer kan administreres via status.</span><span class="sxs-lookup"><span data-stu-id="329b3-138">Service environments can be managed through status.</span></span> <span data-ttu-id="329b3-139">Mulige alternativer er:</span><span class="sxs-lookup"><span data-stu-id="329b3-139">The possible options are:</span></span>

- <span data-ttu-id="329b3-140">**Ikke publisert** – Miljøet er opprettet, men det er ennå ikke publisert.</span><span class="sxs-lookup"><span data-stu-id="329b3-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="329b3-141">**Publisert** – Miljøet er publisert i tillegget for Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="329b3-141">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="329b3-142">**Endret** – Attributtene for et publisert miljø er endret, men endringene er ikke publisert ennå.</span><span class="sxs-lookup"><span data-stu-id="329b3-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="329b3-143">Kundehemmeligheter</span><span class="sxs-lookup"><span data-stu-id="329b3-143">Customer secrets</span></span>

<span data-ttu-id="329b3-144">Tillegget Elektronisk fakturering er ansvarlig for lagring av alle forretningsdata i Azure-ressursene som firmaet ditt eier.</span><span class="sxs-lookup"><span data-stu-id="329b3-144">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="329b3-145">For å sikre at tjenesten fungerer som den skal, og at alle forretningsdataene som trengs for og genereres av tillegget Elektronisk fakturering, bare åpnes av tillegget, må du opprette to hoved-Azure-ressurser:</span><span class="sxs-lookup"><span data-stu-id="329b3-145">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="329b3-146">En Azure Storage-konto (blob-lagring) som lagrer elektroniske fakturaer</span><span class="sxs-lookup"><span data-stu-id="329b3-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="329b3-147">Et Azure Key Vault som lagrer sertifikater og URIen (Uniform Resource Identifier) for lagringskontoen</span><span class="sxs-lookup"><span data-stu-id="329b3-147">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="329b3-148">En dedikert Key Vault- og kundelagringskonto må tilordnes spesifikt for bruk med tillegget Elektroniske fakturering.</span><span class="sxs-lookup"><span data-stu-id="329b3-148">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="329b3-149">Hvis du vil ha mer informasjon, kan du se [Opprette en Azure Storage-konto og et Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="329b3-149">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="329b3-150">Brukere</span><span class="sxs-lookup"><span data-stu-id="329b3-150">Users</span></span>

<span data-ttu-id="329b3-151">Hvert tjenestemiljø må vise en liste over brukerne som kan koble seg til fra Dynamics 365 Finance og Dynamics 365 Supply Chain Management i Elektronisk fakturering-tillegget.</span><span class="sxs-lookup"><span data-stu-id="329b3-151">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="329b3-152">Publisering</span><span class="sxs-lookup"><span data-stu-id="329b3-152">Publication</span></span>

<span data-ttu-id="329b3-153">Tjenestemiljøene må de publiseres til Elektronisk fakturering-tillegget før de kan brukes.</span><span class="sxs-lookup"><span data-stu-id="329b3-153">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="329b3-154">Det er bare tilgang til publiserte miljøer fra Finance og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="329b3-154">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="329b3-155">I tillegg må et tjenestemiljø publiseres før eventuelle oppdateringer av attributtene trer i kraft på den elektroniske faktureringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="329b3-155">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="329b3-156">Tilkoblede programmer</span><span class="sxs-lookup"><span data-stu-id="329b3-156">Connected applications</span></span>

<span data-ttu-id="329b3-157">Tilkoblede programmer er forekomstene av Finance og Supply Chain Management som du kanskje vil nå gjennom RCS.</span><span class="sxs-lookup"><span data-stu-id="329b3-157">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="329b3-158">I tillegg til program-URLen og leietakeren inneholder et tilkoblet program legitimasjon som gjør at RCS kan koble seg til miljøet.</span><span class="sxs-lookup"><span data-stu-id="329b3-158">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="329b3-159">Gjennom de tilkoblede programmene kan du konfigurere deler av Elektronisk fakturering-funksjonen i Finance og Supply Chain Management for å få hele Elektronisk fakturering-funksjonen til å fungere.</span><span class="sxs-lookup"><span data-stu-id="329b3-159">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="329b3-160">Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="329b3-160">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="329b3-161">Integrering med Elektronisk fakturering-tillegg</span><span class="sxs-lookup"><span data-stu-id="329b3-161">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="329b3-162">Før du kan bruke Finance og Supply Chain Management til å utstede elektroniske fakturaer via tillegget for Elektronisk fakturering, må tillegget konfigureres slik at det er tillatt å kommunisere med tjenesten.</span><span class="sxs-lookup"><span data-stu-id="329b3-162">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="329b3-163">Integreringsfunksjon for tillegget Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="329b3-163">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="329b3-164">Hvis du vil aktivere kommunikasjon mellom Finance og Supply Chain Management og tillegget for Elektronisk fakturering, må du aktivere funksjonen for **Integrering av tillegget Elektronisk fakturering** i arbeidsområdet for **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="329b3-164">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="329b3-165">Tjenestesluttpunkt</span><span class="sxs-lookup"><span data-stu-id="329b3-165">Service endpoint</span></span>

<span data-ttu-id="329b3-166">Endepunktet for tjeneste er URL-adressen der tillegget for Elektronisk fakturering er plassert.</span><span class="sxs-lookup"><span data-stu-id="329b3-166">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="329b3-167">Før du elektroniske fakturaer kan utstedet må endepunktet for tjenesten konfigurere i Finance og Supply Chain Management, slik at det er tillatt å kommunisere med tjenesten.</span><span class="sxs-lookup"><span data-stu-id="329b3-167">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="329b3-168">For å konfigurere tjenestesluttpunktet, kan du gå til **Organisasjonsadministrasjon \> Oppsett \> parametere for elektronisk dokument**, og deretter, i fanen **Innsendingstjenester** i feltet **URL for tillegg for Elektronisk faktura**, angir du URL-en som beskrevet i tabellen som er beskrevet i delen **Tjenestesluttpunkt**.</span><span class="sxs-lookup"><span data-stu-id="329b3-168">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="329b3-169">Miljøer</span><span class="sxs-lookup"><span data-stu-id="329b3-169">Environments</span></span>

<span data-ttu-id="329b3-170">Miljønavnet som angis i Finance og Supply Chain Management, refererer til navnet på miljøet som opprettes i RCS og publiseres i tillegget til Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="329b3-170">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="329b3-171">Miljøet må konfigureres i kategorien **Innsendingstjenester** på siden **Parameter for elektronisk dokument**, slik at hver forespørsel om å utstede elektroniske fakturaer, inneholder miljøet der tillegget for Elektronisk fakturering kan fastslå hvilken elektronisk faktureringsfunksjon som må behandle forespørselen.</span><span class="sxs-lookup"><span data-stu-id="329b3-171">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="329b3-172">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="329b3-172">Additional resources</span></span>

- [<span data-ttu-id="329b3-173">Konfigurere elektroniske fakturaer i RCS</span><span class="sxs-lookup"><span data-stu-id="329b3-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="329b3-174">Utstede elektroniske fakturaer i Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="329b3-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
