---
title: Legge til støtte for et innholdsleveringsnettverk (CDN)
description: Dette emnet beskriver hvordan du legger til et innholdsleveringsnettverk (CDN) i Microsoft Dynamics 365 Commerce-miljøet.
author: brianshook
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d653b072eca134c765a5db5659b228648fc13c4a
ms.sourcegitcommit: 3fe4d9a33447aa8a62d704fbbf18aeb9cb667baa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2021
ms.locfileid: "5582725"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="84471-103">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="84471-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="84471-104">Dette emnet beskriver hvordan du legger til et innholdsleveringsnettverk (CDN) i Microsoft Dynamics 365 Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="84471-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="84471-105">Når du definerer et e-handelsmiljø i Dynamics 365 Commerce, kan du konfigurere det slik at det fungerer med CDN-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="84471-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="84471-106">Ditt egendefinerte domene kan aktiveres under klargjøringsprosessen for ditt e-handelsmiljø.</span><span class="sxs-lookup"><span data-stu-id="84471-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="84471-107">Du kan også bruke en serviceforespørsel for å konfigurere den etter at klargjøringsprosessen er fullført.</span><span class="sxs-lookup"><span data-stu-id="84471-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="84471-108">Klargjøringsprosessen for e-handelsmiljøet genererer et vertsnavn som er knyttet til miljøet.</span><span class="sxs-lookup"><span data-stu-id="84471-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="84471-109">Dette vertsnavnet har følgende format, der \<*e-commerce-tenant-name*\> er navnet på miljøet ditt:</span><span class="sxs-lookup"><span data-stu-id="84471-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="84471-110">&lt;e-handel-leier-navn&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="84471-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="84471-111">Vertsnavnet eller endepunktet som genereres under klargjøringsprosessen, støtter bare et SSL-sertifikat (Secure Sockets Layer) for \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="84471-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="84471-112">Den støtter ikke SSL for egendefinerte domener.</span><span class="sxs-lookup"><span data-stu-id="84471-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="84471-113">Derfor må du avslutte SSL for egendefinerte domener i CDN og videresende trafikk fra CDN til vertsnavnet eller endepunktet som Commerce genererte.</span><span class="sxs-lookup"><span data-stu-id="84471-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="84471-114">I tillegg betjenes *statistiske filer* (JavaScript- eller Cascading Style Sheets \[CSS\]-filer) fra Commerce fra endepunktet som Commerce genererte (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="84471-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="84471-115">Statistiske filer kan bare hurtigbufres hvis vertsnavnet eller endepunktet som Commerce genererte, plasseres bak CDN.</span><span class="sxs-lookup"><span data-stu-id="84471-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="84471-116">Definer SSL</span><span class="sxs-lookup"><span data-stu-id="84471-116">Set up SSL</span></span>

<span data-ttu-id="84471-117">For å sikre at SSL er konfigurert, og at statistiske filer bufres, må du konfigurere CDN slik at det er tilknyttet vertsnavnet som Commerce har generert for miljøet ditt.</span><span class="sxs-lookup"><span data-stu-id="84471-117">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="84471-118">Du må også bufre det følgende mønsteret bare for statistiske filer:</span><span class="sxs-lookup"><span data-stu-id="84471-118">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="84471-119">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="84471-119">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="84471-120">Når du har klargjort handelsmiljøet med det tilpassede domenet som er oppgitt, eller etter at du har angitt det egendefinerte domenet for miljøet ditt ved å bruke en tjenesteforespørsel, kan du peke det tilpassede domenet til vertsnavnet eller endepunktet som Commerce laget.</span><span class="sxs-lookup"><span data-stu-id="84471-120">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="84471-121">Som tidligere nevnt støtter det genererte vertsnavnet eller endepunktet bare et SSL-sertifikat for \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="84471-121">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="84471-122">Den støtter ikke SSL for egendefinerte domener.</span><span class="sxs-lookup"><span data-stu-id="84471-122">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="84471-123">CDN-tjenester</span><span class="sxs-lookup"><span data-stu-id="84471-123">CDN services</span></span>

<span data-ttu-id="84471-124">Alle CDN-tjenester kan brukes med et handelsmiljø.</span><span class="sxs-lookup"><span data-stu-id="84471-124">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="84471-125">Her er to eksempler:</span><span class="sxs-lookup"><span data-stu-id="84471-125">Here are two examples:</span></span>

- <span data-ttu-id="84471-126">**Microsoft Azure Front Door Service** – Azure CDN-løsningen.</span><span class="sxs-lookup"><span data-stu-id="84471-126">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="84471-127">Hvis du vil ha mer informasjon om Azure Front Door Service, se [Dokumentasjon for Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="84471-127">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="84471-128">**Akamai Dynamic Site Accelerator** – For mer informasjon, se [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="84471-128">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="84471-129">CND-oppsett</span><span class="sxs-lookup"><span data-stu-id="84471-129">CDN setup</span></span>

<span data-ttu-id="84471-130">Installasjonsprosessen for CDN består av disse generelle trinnene:</span><span class="sxs-lookup"><span data-stu-id="84471-130">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="84471-131">Legg til en frontvert.</span><span class="sxs-lookup"><span data-stu-id="84471-131">Add a front-end host.</span></span>
1. <span data-ttu-id="84471-132">Konfigurer et serverdelsutvalg.</span><span class="sxs-lookup"><span data-stu-id="84471-132">Configure a backend pool.</span></span>
1. <span data-ttu-id="84471-133">Definer regler for ruting og bufring.</span><span class="sxs-lookup"><span data-stu-id="84471-133">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="84471-134">Legg til en frontvert</span><span class="sxs-lookup"><span data-stu-id="84471-134">Add a front-end host</span></span>

<span data-ttu-id="84471-135">Alle CDN-tjenester kan brukes, men for eksempel i dette emnet brukes Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="84471-135">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="84471-136">Hvis du vil ha informasjon om hvordan du konfigurerer Azure Front Door Service, se [Hurtigstart: Opprette en hovedinngang for et høyt tilgjengelig globalt webprogram](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="84471-136">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="84471-137">Konfigurere et serverdelsutvalg i Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="84471-137">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="84471-138">Følg disse trinnene for å konfigurere et serverdelsutvalg i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="84471-138">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="84471-139">Legg til **&lt;ecom-leier-navn&gt;.commerce.dynamics.com** til et serverdelsutvalg som en egendefinert vert som har et tomt serverdelvertshode.</span><span class="sxs-lookup"><span data-stu-id="84471-139">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="84471-140">Under **Belastningsfordeling** lar du standardverdiene være.</span><span class="sxs-lookup"><span data-stu-id="84471-140">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="84471-141">Følgende illustrasjon viser dialogboksen **Legg til en serverdel** i Azure Front Door Service, der vertsnavnet for serverdelen er angitt.</span><span class="sxs-lookup"><span data-stu-id="84471-141">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Legge til en dialogboks for serverdelsutvalg](./media/CDN_BackendPool.png)

<span data-ttu-id="84471-143">Følgende illustrasjon viser dialogboksen **Legg til et serverdelutvalg** i Azure Front Door Service med standardverdier for belastningsfordeling.</span><span class="sxs-lookup"><span data-stu-id="84471-143">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Legge til en dialogboks for serverdelsutvalg (fortsettelse)](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="84471-145">Definere regler i Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="84471-145">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="84471-146">Følg disse trinnene for å opprette en rutingsregel i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="84471-146">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="84471-147">Legge til en rutingsregel.</span><span class="sxs-lookup"><span data-stu-id="84471-147">Add a routing rule.</span></span>
1. <span data-ttu-id="84471-148">Angi **standard** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="84471-148">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="84471-149">I feltet **Godkjent protokoll** velger du **HTTP og HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="84471-149">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="84471-150">I feltet **Frontverter** angir du **dynamics-ecom-leiernavn.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="84471-150">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="84471-151">Under **Mønstre som skal samsvare** angir du **/\*** i det øvre feltet.</span><span class="sxs-lookup"><span data-stu-id="84471-151">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="84471-152">Under **Rutedetaljer** angir du alternativet **Rutetype** til **Fremover**.</span><span class="sxs-lookup"><span data-stu-id="84471-152">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="84471-153">I feltet **Serverdelsutvalg** velger du **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="84471-153">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="84471-154">I feltet **Videresendingsprotokoll** velger du alternativet **Samsvar forespørsel**.</span><span class="sxs-lookup"><span data-stu-id="84471-154">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="84471-155">Angi at alternativet **URL rewrite** skal være **Deaktivert**.</span><span class="sxs-lookup"><span data-stu-id="84471-155">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="84471-156">Angi at alternativet **Bufring** skal være **Deaktivert**.</span><span class="sxs-lookup"><span data-stu-id="84471-156">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="84471-157">Følg disse trinnene for å opprette en bufringsregel i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="84471-157">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="84471-158">Legg til en bufringsregel.</span><span class="sxs-lookup"><span data-stu-id="84471-158">Add a caching rule.</span></span>
1. <span data-ttu-id="84471-159">Angi **statistiske filer** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="84471-159">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="84471-160">I feltet **Godkjent protokoll** velger du **HTTP og HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="84471-160">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="84471-161">I feltet **Frontverter** angir du **dynamics-ecom-leiernavn.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="84471-161">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="84471-162">Under **Mønstre som skal samsvare** i det øvre feltet angir du **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="84471-162">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="84471-163">Under **Rutedetaljer** angir du alternativet **Rutetype** til **Fremover**.</span><span class="sxs-lookup"><span data-stu-id="84471-163">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="84471-164">I feltet **Serverdelsutvalg** velger du **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="84471-164">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="84471-165">I feltet **Videresendingsprotokoll** velger du alternativet **Samsvar forespørsel**.</span><span class="sxs-lookup"><span data-stu-id="84471-165">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="84471-166">Angi at alternativet **URL rewrite** skal være **Deaktivert**.</span><span class="sxs-lookup"><span data-stu-id="84471-166">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="84471-167">Angi at alternativet **Bufring** skal være **Deaktivert**.</span><span class="sxs-lookup"><span data-stu-id="84471-167">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="84471-168">Velg **Bufre hver unike URL-adresse** i **Hurtigbufring for spørringsstreng**.</span><span class="sxs-lookup"><span data-stu-id="84471-168">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="84471-169">I feltet **Dynamisk komprimering** velger du alternativet **Aktivert**.</span><span class="sxs-lookup"><span data-stu-id="84471-169">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="84471-170">Følgende illustrasjon viser dialogboksen **Legg til en regel** i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="84471-170">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Dialogboksen Legg til en regel](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="84471-172">Hvis domenet du skal bruke, allerede er aktivt og direkte, oppretter du en støtteforespørsel fra **Støtte**-flisen i [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) for å få hjelp til de neste trinnene.</span><span class="sxs-lookup"><span data-stu-id="84471-172">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="84471-173">Hvis du vil ha mer informasjon, kan du se [Få støtte for Finance and Operations-apper eller Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="84471-173">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="84471-174">Hvis domenet er nytt og det ikke er et direkte domene som allerede finnes, kan du legge til det egendefinerte domenet i konfigurasjonen for Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="84471-174">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="84471-175">Dette vil gjøre det mulig for nettrafikk å dirigere til nettstedet ditt via Azure Front Door-forekomsten.</span><span class="sxs-lookup"><span data-stu-id="84471-175">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="84471-176">Hvis du vil legge til det egendefinerte domenet (for eksempel `www.fabrikam.com`), må du konfigurere et kanonisk navn (CNAME) for domenet.</span><span class="sxs-lookup"><span data-stu-id="84471-176">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="84471-177">Følgende illustrasjon viser dialogboksen **CNAME-konfigurasjon** i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="84471-177">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Dialogboksen CNAME-konfigurasjon](./media/CNAME_Configuration.png)

<span data-ttu-id="84471-179">Du kan bruke Azure Front Door Service til å administrere sertifikatet, eller du kan bruke ditt eget sertifikat for det egendefinerte domenet.</span><span class="sxs-lookup"><span data-stu-id="84471-179">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="84471-180">Den følgende illustrasjonen viser dialogboksen for **HTTPS for egendefinert domene** i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="84471-180">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Dialogboksen for HTTPS for egendefinert domene](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="84471-182">Hvis du vil ha detaljerte instruksjoner om hvordan du legger til et tilpasset domene i Azure Front Door, kan du se [Legge til et egendefinert domene i Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="84471-182">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="84471-183">CDN skal nå være riktig konfigurert slik at det kan brukes sammen med ditt handelsområde.</span><span class="sxs-lookup"><span data-stu-id="84471-183">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="84471-184">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="84471-184">Additional resources</span></span>

[<span data-ttu-id="84471-185">Implementeringsalternativer for innholdsleveringsnettverk</span><span class="sxs-lookup"><span data-stu-id="84471-185">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
