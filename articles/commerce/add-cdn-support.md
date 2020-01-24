---
title: Legge til støtte for et innholdsleveringsnettverk (CDN)
description: Dette emnet beskriver hvordan du legger til et innholdsleveringsnettverk (CDN) i Microsoft Dynamics 365 Commerce-miljøet.
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d2d64f0de5287a764cb2e40b99a08084494bf53c
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945634"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="a76f0-103">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="a76f0-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a76f0-104">Dette emnet beskriver hvordan du legger til et innholdsleveringsnettverk (CDN) i Microsoft Dynamics 365 Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="a76f0-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="a76f0-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="a76f0-105">Overview</span></span>

<span data-ttu-id="a76f0-106">Når du definerer et e-handelsmiljø i Dynamics 365 Commerce, kan du konfigurere det slik at det fungerer med CDN-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="a76f0-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="a76f0-107">Ditt egendefinerte domene kan aktiveres under klargjøringsprosessen for ditt e-handelsmiljø.</span><span class="sxs-lookup"><span data-stu-id="a76f0-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="a76f0-108">Du kan også bruke en serviceforespørsel for å konfigurere den etter at klargjøringsprosessen er fullført.</span><span class="sxs-lookup"><span data-stu-id="a76f0-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="a76f0-109">Klargjøringsprosessen for e-handelsmiljøet genererer et vertsnavn som er knyttet til miljøet.</span><span class="sxs-lookup"><span data-stu-id="a76f0-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="a76f0-110">Dette vertsnavnet har følgende format, der *e-handel-leier-navn* er navnet på miljøet ditt:</span><span class="sxs-lookup"><span data-stu-id="a76f0-110">This host name has the following format, where *e-commerce-tenant-name* is the name of your environment:</span></span>

<span data-ttu-id="a76f0-111">&lt;e-handel-leier-navn&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="a76f0-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="a76f0-112">Vertsnavnet eller endepunktet som genereres under klargjøringsprosessen, støtter bare et SSL-sertifikat (Secure Sockets Layer) for \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="a76f0-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="a76f0-113">Den støtter ikke SSL for egendefinerte domener.</span><span class="sxs-lookup"><span data-stu-id="a76f0-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="a76f0-114">Derfor må du avslutte SSL for egendefinerte domener i CDN og videresende trafikk fra CDN til vertsnavnet eller endepunktet som Commerce genererte.</span><span class="sxs-lookup"><span data-stu-id="a76f0-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="a76f0-115">I tillegg betjenes *statistiske filer* (JavaScript- eller Cascading Style Sheets \[CSS\]-filer) fra Commerce fra endepunktet som Commerce genererte (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="a76f0-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="a76f0-116">Statistiske filer kan bare hurtigbufres hvis vertsnavnet eller endepunktet som Commerce genererte, plasseres bak CDN.</span><span class="sxs-lookup"><span data-stu-id="a76f0-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="a76f0-117">Definer SSL</span><span class="sxs-lookup"><span data-stu-id="a76f0-117">Set up SSL</span></span>

<span data-ttu-id="a76f0-118">For å sikre at SSL er konfigurert, og at statistiske filer bufres, må du konfigurere CDN slik at det er tilknyttet vertsnavnet som Commerce har generert for miljøet ditt.</span><span class="sxs-lookup"><span data-stu-id="a76f0-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="a76f0-119">Du må også bufre det følgende mønsteret bare for statistiske filer:</span><span class="sxs-lookup"><span data-stu-id="a76f0-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="a76f0-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="a76f0-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="a76f0-121">Når du har klargjort handelsmiljøet med det tilpassede domenet som er oppgitt, eller etter at du har angitt det egendefinerte domenet for miljøet ditt ved å bruke en tjenesteforespørsel, kan du peke det tilpassede domenet til vertsnavnet eller endepunktet som Commerce laget.</span><span class="sxs-lookup"><span data-stu-id="a76f0-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="a76f0-122">Som tidligere nevnt støtter det genererte vertsnavnet eller endepunktet bare et SSL-sertifikat for \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="a76f0-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="a76f0-123">Den støtter ikke SSL for egendefinerte domener.</span><span class="sxs-lookup"><span data-stu-id="a76f0-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="a76f0-124">CDN-tjenester</span><span class="sxs-lookup"><span data-stu-id="a76f0-124">CDN services</span></span>

<span data-ttu-id="a76f0-125">Alle CDN-tjenester kan brukes med et handelsmiljø.</span><span class="sxs-lookup"><span data-stu-id="a76f0-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="a76f0-126">Her er to eksempler:</span><span class="sxs-lookup"><span data-stu-id="a76f0-126">Here are two examples:</span></span>

- <span data-ttu-id="a76f0-127">**Microsoft Azure Front Door Service** – Azure CDN-løsningen.</span><span class="sxs-lookup"><span data-stu-id="a76f0-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="a76f0-128">Hvis du vil ha mer informasjon om Azure Front Door Service, se [Dokumentasjon for Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="a76f0-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="a76f0-129">**Akamai Dynamic Site Accelerator** – For mer informasjon, se [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="a76f0-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="a76f0-130">CND-oppsett</span><span class="sxs-lookup"><span data-stu-id="a76f0-130">CDN setup</span></span>

<span data-ttu-id="a76f0-131">Installasjonsprosessen for CDN består av disse generelle trinnene:</span><span class="sxs-lookup"><span data-stu-id="a76f0-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="a76f0-132">Legg til en frontvert.</span><span class="sxs-lookup"><span data-stu-id="a76f0-132">Add a front-end host.</span></span>
1. <span data-ttu-id="a76f0-133">Konfigurer et serverdelsutvalg.</span><span class="sxs-lookup"><span data-stu-id="a76f0-133">Configure a back-end pool.</span></span>
1. <span data-ttu-id="a76f0-134">Definer regler for ruting og bufring.</span><span class="sxs-lookup"><span data-stu-id="a76f0-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="a76f0-135">Legg til en frontvert</span><span class="sxs-lookup"><span data-stu-id="a76f0-135">Add a front-end host</span></span>

<span data-ttu-id="a76f0-136">Alle CDN-tjenester kan brukes, men for eksempel i dette emnet brukes Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="a76f0-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="a76f0-137">Hvis du vil ha informasjon om hvordan du konfigurerer Azure Front Door Service, se [Hurtigstart: Opprette en hovedinngang for et høyt tilgjengelig globalt webprogram](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="a76f0-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a><span data-ttu-id="a76f0-138">Konfigurere et serverdelsutvalg i Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="a76f0-138">Configure a back-end pool in Azure Front Door Service</span></span>

<span data-ttu-id="a76f0-139">Følg disse trinnene for å konfigurere et serverdelsutvalg i Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="a76f0-139">To configure a back-end pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="a76f0-140">Legg til **&lt;ecom-leier-navn&gt;.commerce.dynamics.com** til et serverdelsutvalg som en egendefinert vert som har et tomt serverdelvertshode.</span><span class="sxs-lookup"><span data-stu-id="a76f0-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a back-end pool as a custom host that has an empty back-end host header.</span></span>
1. <span data-ttu-id="a76f0-141">Under **Helsetilstand** i feltet **Bane** angir du **/keepalive**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-141">Under **Health probes**, in the **Path** field, enter **/keepalive**.</span></span>
1. <span data-ttu-id="a76f0-142">I feltet **Intervaller (sekunder)** angir du **255**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-142">In the **Intervals (seconds)** field, enter **255**.</span></span>
1. <span data-ttu-id="a76f0-143">Under **Belastningsfordeling** lar du standardverdiene være.</span><span class="sxs-lookup"><span data-stu-id="a76f0-143">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="a76f0-144">Følgende illustrasjon viser dialogboksen **Legg til et serverdelsutvalg** i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="a76f0-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service.</span></span>

![Legge til en dialogboks for serverdelsutvalg](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="a76f0-146">Definere regler i Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="a76f0-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="a76f0-147">Følg disse trinnene for å opprette en rutingsregel i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="a76f0-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="a76f0-148">Legge til en rutingsregel.</span><span class="sxs-lookup"><span data-stu-id="a76f0-148">Add a routing rule.</span></span>
1. <span data-ttu-id="a76f0-149">Angi **standard** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="a76f0-150">I feltet **Godkjent protokoll** velger du **HTTP og HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="a76f0-151">I feltet **Frontverter** angir du **dynamics-ecom-leiernavn.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="a76f0-152">Under **Mønstre som skal samsvare** angir du **/\*** i det øvre feltet.</span><span class="sxs-lookup"><span data-stu-id="a76f0-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="a76f0-153">Under **Rutedetaljer** angir du alternativet **Rutetype** til **Fremover**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="a76f0-154">I feltet **Serverdelsutvalg** velger du **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="a76f0-155">I feltet **Videresendingsprotokoll** velger du alternativet **Samsvar forespørsel**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="a76f0-156">Angi at alternativet **URL rewrite** skal være **Deaktivert**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="a76f0-157">Angi at alternativet **Bufring** skal være **Deaktivert**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="a76f0-158">Følg disse trinnene for å opprette en bufringsregel i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="a76f0-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="a76f0-159">Legg til en bufringsregel.</span><span class="sxs-lookup"><span data-stu-id="a76f0-159">Add a caching rule.</span></span>
1. <span data-ttu-id="a76f0-160">Angi **statistiske filer** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="a76f0-161">I feltet **Godkjent protokoll** velger du **HTTP og HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="a76f0-162">I feltet **Frontverter** angir du **dynamics-ecom-leiernavn.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="a76f0-163">Under **Mønstre som skal samsvare** i det øvre feltet angir du **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="a76f0-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="a76f0-164">Under **Rutedetaljer** angir du alternativet **Rutetype** til **Fremover**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="a76f0-165">I feltet **Serverdelsutvalg** velger du **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="a76f0-166">I feltet **Videresendingsprotokoll** velger du alternativet **Samsvar forespørsel**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="a76f0-167">Angi at alternativet **URL rewrite** skal være **Deaktivert**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="a76f0-168">Angi at alternativet **Bufring** skal være **Deaktivert**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="a76f0-169">Velg **Bufre hver unike URL-adresse** i **Hurtigbufring for spørringsstreng**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="a76f0-170">I feltet **Dynamisk komprimering** velger du alternativet **Aktivert**.</span><span class="sxs-lookup"><span data-stu-id="a76f0-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="a76f0-171">Følgende illustrasjon viser dialogboksen **Legg til en regel** i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="a76f0-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Dialogboksen Legg til en regel](./media/CDN_CachingRule.png)

<span data-ttu-id="a76f0-173">Når denne innledende konfigurasjonen er distribuert, må du legge til det egendefinerte domenet i konfigurasjonen for Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="a76f0-173">After this initial configuration is deployed, you must add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="a76f0-174">Hvis du vil legge til det egendefinerte domenet (for eksempel `www.fabrikam.com`), må du konfigurere et kanonisk navn (CNAME) for domenet.</span><span class="sxs-lookup"><span data-stu-id="a76f0-174">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="a76f0-175">Følgende illustrasjon viser dialogboksen **CNAME-konfigurasjon** i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="a76f0-175">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Dialogboksen CNAME-konfigurasjon](./media/CNAME_Configuration.png)

> [!NOTE]
> <span data-ttu-id="a76f0-177">Hvis domenet du skal bruke, allerede er aktivt og live, kontakter du kundestøtten for å aktivere dette domenet med Azure Front Door Service for å konfigurere en test.</span><span class="sxs-lookup"><span data-stu-id="a76f0-177">If the domain that you will use is already active and live, contact support to enable this domain with Azure Front Door Service to set up a test.</span></span>

<span data-ttu-id="a76f0-178">Du kan bruke Azure Front Door Service til å administrere sertifikatet, eller du kan bruke ditt eget sertifikat for det egendefinerte domenet.</span><span class="sxs-lookup"><span data-stu-id="a76f0-178">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="a76f0-179">Den følgende illustrasjonen viser dialogboksen for **HTTPS for egendefinert domene** i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="a76f0-179">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Dialogboksen for HTTPS for egendefinert domene](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="a76f0-181">CDN skal nå være riktig konfigurert slik at det kan brukes sammen med ditt handelsområde.</span><span class="sxs-lookup"><span data-stu-id="a76f0-181">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a76f0-182">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a76f0-182">Additional resources</span></span>

[<span data-ttu-id="a76f0-183">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="a76f0-183">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="a76f0-184">Distribuere et nytt e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="a76f0-184">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="a76f0-185">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="a76f0-185">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="a76f0-186">Knytte et nettområde til en kanal</span><span class="sxs-lookup"><span data-stu-id="a76f0-186">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="a76f0-187">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="a76f0-187">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="a76f0-188">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="a76f0-188">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="a76f0-189">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="a76f0-189">Enable location-based store detection</span></span>](enable-store-detection.md)
