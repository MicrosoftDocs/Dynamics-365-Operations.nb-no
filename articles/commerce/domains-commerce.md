---
title: Domener i Dynamics 365 Commerce
description: Dette emnet beskriver hvordan domener behandles i Microsoft Dynamics 365 Commerce.
author: BrShoo
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: d855f2164e4ee0f0cdb220787eb96217523137e3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010253"
---
# <a name="domains-in-dynamics-365-commerce"></a><span data-ttu-id="b3208-103">Domener i Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b3208-103">Domains in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b3208-104">Dette emnet beskriver hvordan domener behandles i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b3208-104">This topic describes how domains are handled in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b3208-105">Domener er webadresser som brukes til å navigere til Dynamics 365 Commerce-områder i en nettleser.</span><span class="sxs-lookup"><span data-stu-id="b3208-105">Domains are web addresses used to navigate to Dynamics 365 Commerce sites in a web browser.</span></span> <span data-ttu-id="b3208-106">Du styrer administrasjonen av domenet med en valgt DNS-leverandør (Domain Name Server).</span><span class="sxs-lookup"><span data-stu-id="b3208-106">You control management of your domain with a chosen Domain Name Server (DNS) provider.</span></span> <span data-ttu-id="b3208-107">Det refereres til domener i hele områdebyggeren i Dynamics 365 Commerce for å koordinere hvordan et område skal åpnes når det er publisert.</span><span class="sxs-lookup"><span data-stu-id="b3208-107">Domains are referenced throughout Dynamics 365 Commerce site builder to coordinate how a site will be accessed when published.</span></span> <span data-ttu-id="b3208-108">Dette emnet omtaler hvordan domener behandles og refereres til i løpet av livssyklusen til utvikling og lansering på handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="b3208-108">This topic reviews how domains are handled and referenced throughout the lifecycle of the Commerce site development and launch.</span></span>

## <a name="provisioning-and-supported-host-names"></a><span data-ttu-id="b3208-109">Klargjøring av og støttede vertsnavn</span><span class="sxs-lookup"><span data-stu-id="b3208-109">Provisioning and supported host names</span></span>

<span data-ttu-id="b3208-110">Når du klargjør et e-handelsmiljø i [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), brukes boksen **Støttede vertsnavn** i vinduet Klargjøring av e-handel til å angi domener som skal knyttes til det distribuerte handelsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="b3208-110">When provisioning an e-commerce environment in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), the **Supported host names** box on the e-commerce provisioning screen is used to enter domains that will be associated with the deployed Commerce environment.</span></span> <span data-ttu-id="b3208-111">Disse domenene vil være DNS-navn (Domain Name Server) for kunden, der nettsteder for e-handel vil være driftet.</span><span class="sxs-lookup"><span data-stu-id="b3208-111">These domains will be the customer-facing Domain Name Server (DNS) names where e-commerce websites will be hosted.</span></span> <span data-ttu-id="b3208-112">Hvis du går til et domene på dette stadiet, blir ikke trafikken omdirigert for domenet til Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b3208-112">Entering a domain at this stage does not start diverting traffic for the domain to Dynamics 365 Commerce.</span></span> <span data-ttu-id="b3208-113">Trafikk for et domene blir bare rutet til handelsendepunktet når DNS CNAME-posten oppdateres til å bruke handelsendepunktet med domenet.</span><span class="sxs-lookup"><span data-stu-id="b3208-113">Traffic for a domain will only be routed to the Commerce endpoint when the DNS CNAME record is updated to use the Commerce endpoint with the domain.</span></span>

> [!NOTE]
> <span data-ttu-id="b3208-114">Du kan skrive inn flere domener i boksen **Støttede vertsnavn** ved å skille dem med semikolon.</span><span class="sxs-lookup"><span data-stu-id="b3208-114">Multiple domains can be entered into the **Supported host names** box by separating them with semi-colons.</span></span>

<span data-ttu-id="b3208-115">Illustrasjonen nedenfor viser LCS for e-handelsklargjøring med boksen **Støttede vertsnavn** uthevet.</span><span class="sxs-lookup"><span data-stu-id="b3208-115">The following illustration shows the LCS e-commerce provisioning screen with the **Supported host names** box highlighted.</span></span> 

![LCS for e-handelsklargjøring med boksen **Støttede vertsnavn** uthevet](./media/Domains_ProvisioningeCommerceScreen.png)

<span data-ttu-id="b3208-117">Du kan opprette en serviceforespørsel for å legge til flere domener i et miljø hvis klargjøring allerede har skjedd.</span><span class="sxs-lookup"><span data-stu-id="b3208-117">You can create a service request to add additional domains to an environment if provisioning has already occurred.</span></span> <span data-ttu-id="b3208-118">Hvis du vil opprette en serviceforespørsel i LCS, kan du i miljøet gå til **Kundestøtte \> Kundestøtteproblemer** og velge **Send en hendelse**.</span><span class="sxs-lookup"><span data-stu-id="b3208-118">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

## <a name="commerce-generated-urls"></a><span data-ttu-id="b3208-119">Commerce-genererte URL-adresser</span><span class="sxs-lookup"><span data-stu-id="b3208-119">Commerce-generated URLs</span></span>

<span data-ttu-id="b3208-120">Når du klargjør et Dynamics 365 Commerce-e-handelsmiljø, vil Commerce generere en URL-adresse som skal virke i miljøet.</span><span class="sxs-lookup"><span data-stu-id="b3208-120">When provisioning a Dynamics 365 Commerce e-commerce environment, Commerce will generate a URL that will be the working address for the environment.</span></span> <span data-ttu-id="b3208-121">Det refereres til denne URL-adressen i områdekoblingen for e-handel som vises i LCS etter at miljøet er klargjort.</span><span class="sxs-lookup"><span data-stu-id="b3208-121">This URL is referenced in the e-commerce site link shown in LCS after the environment is provisioned.</span></span> <span data-ttu-id="b3208-122">En Commerce-generert URL-adresse er i formatet `https://<e-commerce tenant name>.commerce.dynamics.com`, der navnet på e-handelsleieren er navnet som er angitt i LCS for Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="b3208-122">A Commerce-generated URL is in the format `https://<e-commerce tenant name>.commerce.dynamics.com`, where the e-commerce tenant name is the name entered in LCS for the Commerce environment.</span></span>

<span data-ttu-id="b3208-123">Du kan også bruke vertsnavn for produksjonsområde i et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="b3208-123">You can use production site host names in a sandbox environment as well.</span></span> <span data-ttu-id="b3208-124">Dette alternativet er ideelt når du skal kopiere et område fra et sandkassemiljø til produksjon.</span><span class="sxs-lookup"><span data-stu-id="b3208-124">This option is ideal when you will be copying a site from a sandbox environment to production.</span></span>

## <a name="site-setup"></a><span data-ttu-id="b3208-125">Weboppsett</span><span class="sxs-lookup"><span data-stu-id="b3208-125">Site setup</span></span>

<span data-ttu-id="b3208-126">Når e-handelsmiljøet er klargjort, må du sette opp området i områdebygger for Commerce for å knytte området til den fungerende URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="b3208-126">After your e-commerce environment is provisioned, you must set up your site in Commerce site builder to associate your site to the working URL.</span></span>

<span data-ttu-id="b3208-127">Når du konfigurerer et område i områdebyggeren for første gang, vises dialogboksen **Konfigurer området**.</span><span class="sxs-lookup"><span data-stu-id="b3208-127">When you first set up a site in site builder, the **Setup your Site** dialog box will appear.</span></span>

<span data-ttu-id="b3208-128">Følgende illustrasjon viser dialogboksen **Konfigurer området** for et område kalt "standard" når du åpner området for første gang i områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="b3208-128">The following illustration shows the **Setup your Site** dialog box for a site named "default" when you access the site for the first time in site builder.</span></span>

![**Dialogboksen Konfigurer område**](./media/Domains_SetupyoursiteScreen.png)

<span data-ttu-id="b3208-130">Ved hjelp av boksen **Velg et domene** kan du knytte et av de støttede vertsnavnene som er oppgitt for området i LCS, til området i områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="b3208-130">The **Select a domain** box allows you to associate one of the supported host names provided for your site in LCS to your site in site builder.</span></span>

<span data-ttu-id="b3208-131">Boksen **Bane** kan stå tom, eller du kan legge til en ekstra banestreng som vil bli gjenspeilet i den fungerende URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="b3208-131">The **Path** box can be left blank, or an additional path string can be added that will be reflected in your working URL.</span></span> <span data-ttu-id="b3208-132">Hvis du lar boksen **Bane** være tom, knyttes den grunnleggende Commerce-genererte URL-adressen til området som er definert i områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="b3208-132">Leaving the **Path** box blank associates the base Commerce-generated URL with the site being set up in site builder.</span></span> <span data-ttu-id="b3208-133">Baner må være unike for hvert område-/domenepar.</span><span class="sxs-lookup"><span data-stu-id="b3208-133">Paths must be unique for each site/domain pair.</span></span> <span data-ttu-id="b3208-134">Innenfor området og domenet som er valgt, kan bare ett område i miljøet bruke den tomme banen eller være knyttet til en unik banestreng.</span><span class="sxs-lookup"><span data-stu-id="b3208-134">Within the site and domain selected, only one site in the environment can use the blank path or be associated with a unique path string.</span></span> <span data-ttu-id="b3208-135">Alle strenger som legges til i feltet **Bane** under områdekonfigurasjonen, blir en delbane av den grunnleggende Commerce-genererte URL-adressen som brukes til å få tilgang til området i en nettleser.</span><span class="sxs-lookup"><span data-stu-id="b3208-135">Any string added to the **Path** field during site setup will become a subpath of the base Commerce-generated URL used to access the site in a web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="b3208-136">Banen er også kjent som **samsvarsbanen** når du legger til en kanal i konfigurasjonsdelen **Områdeinnstillinger \> Kanaler** for områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="b3208-136">The path is also known as the **Match path** when adding a channel in the **Site Settings \> Channels** configuration section of site builder.</span></span>

<span data-ttu-id="b3208-137">Hvis du for eksempel har et område i områdebyggeren som heter Fabrikam i en e-handelsleier med navnet XYZ, og hvis du konfigurerer området med en tom bane, vil du få tilgang til det publiserte områdeinnholdet i en nettleser ved å gå til den grunnleggende Commerce-genererte URL-adressen:</span><span class="sxs-lookup"><span data-stu-id="b3208-137">For example, if you have a site in site builder called "fabrikam" in an e-commerce tenant named "xyz," and if you set up the site with a blank path, then you would access the published site content in a web browser by going directly to the base Commerce-generated URL:</span></span>

`https://xyz.commerce.dynamics.com`

<span data-ttu-id="b3208-138">Hvis du har lagt til banen Fabrikam under installasjonen av det samme området, får du tilgang til det publiserte områdeinnholdet i en nettleser ved hjelp av følgende URL-adresse:</span><span class="sxs-lookup"><span data-stu-id="b3208-138">Alternately, if you had added a path of "fabrikam" during this same site's setup, you would access the published site content in a web browser using the following URL:</span></span>

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a><span data-ttu-id="b3208-139">Sider og URL-adresser</span><span class="sxs-lookup"><span data-stu-id="b3208-139">Pages and URLs</span></span>

<span data-ttu-id="b3208-140">Når området er satt opp med en bane, vil alle URL-adresser som er tilknyttet sidene i områdebyggeren, bygge videre på den fungerende URL-adressen (den Commerce-genererte URL-adressen eller den Commerce-genererte URL-adressen pluss banen) for området.</span><span class="sxs-lookup"><span data-stu-id="b3208-140">After your site is set up with a path, all URLs associated with pages in site builder will build on the working URL (the Commerce-generated URL, or the Commerce-generated URL plus the path) for the site.</span></span> <span data-ttu-id="b3208-141">Oppretter en ny URL-adresse i områdebyggeren (**URL-adresser /> + Ny**) ved å velge en side fra listen i dialogboksen **Ny URL-adresse**, og angivelse av URL-adressebanen for den siden knytter denne URL-adressen til den valgte siden.</span><span class="sxs-lookup"><span data-stu-id="b3208-141">Creating a new URL in site builder (**URLS /> +New**) by selecting a page from the list in the **New URL** dialog box and entering the URL path for that page will associate that URL with the selected page.</span></span> <span data-ttu-id="b3208-142">Verdien i URL-adressebanen føyes deretter til områdets fungerende URL-adresse for å få tilgang til siden, og den er merket som `./<URL path>` i URL-adresselisten på siden **URL-adresser** i områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="b3208-142">The URL path value then appends to the site's working URL to access the page, and is labeled as `./<URL path>` in the URL list of the **URLs** page in site builder.</span></span>

<span data-ttu-id="b3208-143">Den følgende illustrasjonen viser dialogboksen **Ny URL-adresse** i områdebyggeren med eksempel på uthevet URL-adressebane.</span><span class="sxs-lookup"><span data-stu-id="b3208-143">The following illustration shows the **New URL** dialog box in site builder with an example URL path highlighted.</span></span> 

![Dialogboksen **Ny URL-adresse** i områdebyggeren](./media/Domains_PageSetup2a.png)

<span data-ttu-id="b3208-145">Den følgende illustrasjonen viser siden **URL-adresser** i områdebyggeren med eksempel på uthevet URL-adresse i listen.</span><span class="sxs-lookup"><span data-stu-id="b3208-145">The following illustration shows the **URLs** page in site builder with an example URL highlighted in the list.</span></span>

![Kjør brukerflyt-alternativet policyflyt](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a><span data-ttu-id="b3208-147">Domener i områdebyggeren</span><span class="sxs-lookup"><span data-stu-id="b3208-147">Domains in site builder</span></span>

<span data-ttu-id="b3208-148">Verdiene for de støttede vertsnavnene er tilgjengelige for å knyttes til et domene ved konfigurasjon av et område.</span><span class="sxs-lookup"><span data-stu-id="b3208-148">The supported host names values are available to be associated as a domain when setting up a site.</span></span> <span data-ttu-id="b3208-149">Når du velger en vertsnavnverdi som domene, vil du se det valgte domenet som det refereres til i hele områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="b3208-149">When selecting a supported host name value as the domain, you will see the chosen domain referenced throughout site builder.</span></span> <span data-ttu-id="b3208-150">Dette domenet er bare en referanse i Commerce-miljøet. Direktetrafikk for det domenet vil ikke videresendes til Dynamics 365 Commerce ennå.</span><span class="sxs-lookup"><span data-stu-id="b3208-150">This domain is only a reference within the Commerce environment, live traffic for that domain will not yet be forwarded to Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b3208-151">Hvis du har to områder som er konfigurert med to forskjellige domener, kan du legge til attributtet **?domain=** i den fungerende URL-adressen for å få tilgang til det publiserte områdeinnholdet i en nettleser.</span><span class="sxs-lookup"><span data-stu-id="b3208-151">When working with sites in site builder, if you have two sites set up with two different domains, you can append the **?domain=** attribute to your working URL to access the published site content in a browser.</span></span>

<span data-ttu-id="b3208-152">Miljøet xyz er for eksempel klargjort, og to områder er opprettet og tilknyttet i områdebyggeren: ett med domenet `www.fabrikam.com` og det andre med domenet `www.constoso.com`.</span><span class="sxs-lookup"><span data-stu-id="b3208-152">For example, environment "xyz" has been provisioned, and two sites have been created and associated in site builder: one with the domain `www.fabrikam.com` and the other with the domain `www.constoso.com`.</span></span> <span data-ttu-id="b3208-153">Hvert område ble konfigurert med en tom bane.</span><span class="sxs-lookup"><span data-stu-id="b3208-153">Each site was set up using a blank path.</span></span> <span data-ttu-id="b3208-154">Du kan deretter få tilgang til disse to områdene i en nettleser på følgende måte ved hjelp av attributtet **?domain=**:</span><span class="sxs-lookup"><span data-stu-id="b3208-154">These two sites could then be accessed in a web browser as follows using the **?domain=** attribute:</span></span>
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

<span data-ttu-id="b3208-155">Når en domenespørrestreng ikke er angitt i et miljø med flere domener som er oppgitt, bruker Commerce det første domenet du oppgav.</span><span class="sxs-lookup"><span data-stu-id="b3208-155">When a domain query string is not given in an environment with multiple domains provided, Commerce uses the first domain you provided.</span></span> <span data-ttu-id="b3208-156">Hvis banen Fabrikam for eksempel først ble oppgitt under konfigurasjon av området, kan URL-adressen `https://xyz.commerce.dynamics.com` brukes til å få tilgang til det publiserte områdets innholdsområde for `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="b3208-156">For example, if the path "fabrikam" was provided first during site setup, the URL `https://xyz.commerce.dynamics.com` could be used to access the published site content site for `www.fabrikam.com`.</span></span>

## <a name="traffic-forwarding-in-production"></a><span data-ttu-id="b3208-157">Viderekobling av trafikk i produksjon</span><span class="sxs-lookup"><span data-stu-id="b3208-157">Traffic forwarding in production</span></span>

<span data-ttu-id="b3208-158">Du kan simulere flere domener ved hjelp av parametere for domenespørringsstreng på endepunktet commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="b3208-158">You can simulate multiple domains using domain query string parameters on the commerce.dynamics.com endpoint itself.</span></span> <span data-ttu-id="b3208-159">Men når du må gå i gang med produksjon, må du videresende trafikken for det egendefinerte domenet til endepunktet `<e-commerce tenant name>.commerce.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="b3208-159">But when you need to go live in production, you must forward the traffic for your custom domain to the `<e-commerce tenant name>.commerce.dynamics.com` endpoint.</span></span>

<span data-ttu-id="b3208-160">Endepunktet `<e-commerce tenant name>.commerce.dynamics.com` støtter ikke egendefinerte SSL-er (Secure Sockets Layers), så du må konfigurere tilpassede domener ved hjelp av Front Door Service eller et innholdsleveringsnettverk (CDN).</span><span class="sxs-lookup"><span data-stu-id="b3208-160">The `<e-commerce tenant name>.commerce.dynamics.com` endpoint does not support custom domain Secure Sockets Layers (SSLs), so you must set up custom domains using a front door service or content delivery network (CDN).</span></span> 

<span data-ttu-id="b3208-161">Hvis du vil konfigurere tilpassede domener ved hjelp av Front Door Service eller CDN, har du to alternativer:</span><span class="sxs-lookup"><span data-stu-id="b3208-161">To set up custom domains using a front door service or CDN, you have two options:</span></span>

- <span data-ttu-id="b3208-162">Konfigurer Front Door Service, for eksempel i Azure, til å håndtere fronttrafikk og koble til Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="b3208-162">Set up a front door service like Azure Front Door to handle front-end traffic and connect to your Commerce environment.</span></span> <span data-ttu-id="b3208-163">Dette gir bedre kontroll over behandling av domene- og sertifikatadministrasjon og mer detaljerte sikkerhetspolicyer.</span><span class="sxs-lookup"><span data-stu-id="b3208-163">This provides greater control over domain and certificate management and more granular security policies.</span></span>
- <span data-ttu-id="b3208-164">Bruk den Commerce-støttede forekomsten av Front Door Service i Azure.</span><span class="sxs-lookup"><span data-stu-id="b3208-164">Use the Commerce-supplied Azure Front Door instance.</span></span> <span data-ttu-id="b3208-165">Dette krever koordineringshandling med Dynamics 365 Commerce-teamet for domenekontroll og henting av SSL-sertifikater for produksjonsdomenet.</span><span class="sxs-lookup"><span data-stu-id="b3208-165">This requires coordinating action with the Dynamics 365 Commerce team for domain verification and obtaining SSL certificates for your production domain.</span></span>

<span data-ttu-id="b3208-166">Hvis du vil ha informasjon om hvordan du setter opp en CDN-tjeneste direkte, kan du se [Legge til støtte for et innholdsleveringsnettverk (CDN)](add-cdn-support.md).</span><span class="sxs-lookup"><span data-stu-id="b3208-166">For information about how to set up a CDN service directly, see [Add support for a content delivery network (CDN)](add-cdn-support.md).</span></span>

<span data-ttu-id="b3208-167">Hvis du vil bruke den Commerce-støttede forekomsten av Front Door Service i Azure, må du opprette en serviceforespørsel for installasjon av CDN fra jobbintroduksjonsteamet til Commerce.</span><span class="sxs-lookup"><span data-stu-id="b3208-167">To use the Commerce-supplied Azure Front Door instance, you must create a service request for CDN setup assistance from the Commerce onboarding team.</span></span> 

- <span data-ttu-id="b3208-168">Du må angi firmanavn, produksjonsdomene, miljø-ID og navn på e-handelsleieren for produksjonen.</span><span class="sxs-lookup"><span data-stu-id="b3208-168">You will need to provide your company name, the production domain, environment ID, and production e-commerce tenant name.</span></span> 
- <span data-ttu-id="b3208-169">Du må bekrefte om dette er et eksisterende domene (brukes for et aktivt område) eller et nytt domene.</span><span class="sxs-lookup"><span data-stu-id="b3208-169">You will need to confirm if this is an existing domain (used for a currently active site) or a new domain.</span></span> 
- <span data-ttu-id="b3208-170">For et nytt domene kan domenekontrolleren og SSL-sertifikatet oppnås i ett trinn.</span><span class="sxs-lookup"><span data-stu-id="b3208-170">For a new domain, the domain verification and SSL certificate can be achieved in a single step.</span></span> 
- <span data-ttu-id="b3208-171">For et domene som betjener et eksisterende nettsted, finnes det en trinnvis prosess som kreves for å etablere domeneverifisering og SSL-sertifikatet.</span><span class="sxs-lookup"><span data-stu-id="b3208-171">For a domain serving an existing website, there is a multistep process required to establish the domain verification and SSL certificate.</span></span> <span data-ttu-id="b3208-172">Denne prosessen har en servicenivåavtale på 7 virkedager før et domene blir aktivt, fordi den inneholder flere sekvensielle trinn.</span><span class="sxs-lookup"><span data-stu-id="b3208-172">This process has a 7-working-day service level agreement (SLA) for a domain to go live, because it includes multiple sequential steps.</span></span>

<span data-ttu-id="b3208-173">Hvis du vil opprette en serviceforespørsel i LCS, kan du i miljøet gå til **Kundestøtte \> Kundestøtteproblemer** og velge **Send en hendelse**.</span><span class="sxs-lookup"><span data-stu-id="b3208-173">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

> [!NOTE]
> <span data-ttu-id="b3208-174">Egendefinerte domener med SSL støttes bare i produksjonsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="b3208-174">Custom domains with SSL are only supported on production environments.</span></span> <span data-ttu-id="b3208-175">For ikke-produktive miljøer, for eksempel sandkasse og brukergodkjenningstesting (UAT), bruker du den Commerce-genererte URL-adressen til å få tilgang til publisert innhold i en nettleser.</span><span class="sxs-lookup"><span data-stu-id="b3208-175">For non-production environments such as sandbox and user acceptance testing (UAT), use the Commerce-generated URL to access published content in a web browser.</span></span>

## <a name="ssl-certificate-process"></a><span data-ttu-id="b3208-176">SSL-sertifikatprosess</span><span class="sxs-lookup"><span data-stu-id="b3208-176">SSL certificate process</span></span>

<span data-ttu-id="b3208-177">Når en serviceforespørsel arkiveres, vil Commerce-teamet koordinere følgende trinn med deg.</span><span class="sxs-lookup"><span data-stu-id="b3208-177">When a service request is filed, the Commerce team will coordinate the following steps with you.</span></span>

<span data-ttu-id="b3208-178">For nye domener:</span><span class="sxs-lookup"><span data-stu-id="b3208-178">For new domains:</span></span>
- <span data-ttu-id="b3208-179">Commerce-teamet konfigurerer forekomsten av Azure Front Door (Commerce-driftet).</span><span class="sxs-lookup"><span data-stu-id="b3208-179">The Commerce team will set up the Azure Front Door instance (Commerce-hosted).</span></span>
- <span data-ttu-id="b3208-180">Commerce-teamet vil deretter gi CNAME-posten tilgang til å henvise til ditt egendefinerte domene.</span><span class="sxs-lookup"><span data-stu-id="b3208-180">The Commerce team will then provide the CNAME record to point your custom domain.</span></span>
- <span data-ttu-id="b3208-181">Etter at CNAME-posten er oppdatert, vil den Commerce-driftede forekomsten av Azure Front Door kontrollere domeneeierskapet og få SSL-sertifikatet.</span><span class="sxs-lookup"><span data-stu-id="b3208-181">After the CNAME record is updated, the Commerce-hosted Azure Front Door instance will be able to verify the domain ownership and get the SSL certificate.</span></span>

<span data-ttu-id="b3208-182">For eksisterende/aktive domener:</span><span class="sxs-lookup"><span data-stu-id="b3208-182">For existing/active domains:</span></span>
- <span data-ttu-id="b3208-183">Commerce-teamet instruerer deg om å legge til en CNAME-post for `afdverify.<custom-domain>` som du oppgir til DNS-leverandøren for domenet.</span><span class="sxs-lookup"><span data-stu-id="b3208-183">The Commerce team will instruct you to add an `afdverify.<custom-domain>` CNAME record to provide to your domain DNS provider.</span></span>
- <span data-ttu-id="b3208-184">Når den er fullført, legger Commerce-teamet til domenet i forekomsten av Azure Front Door og formidler ekstra DNS TXT-poster som skal legges til i DNS for domenet.</span><span class="sxs-lookup"><span data-stu-id="b3208-184">When complete, the Commerce team will add the domain to the Azure Front Door instance and provide additional DNS TXT records to be added to the DNS for the domain.</span></span>
- <span data-ttu-id="b3208-185">Når TXT-postene er fullført, fullfører Commerce-teamet oppdateringene for Azure Front Door for domenet som skal konfigurere SSL-sertifikatet.</span><span class="sxs-lookup"><span data-stu-id="b3208-185">After the TXT records are completed, the Commerce team will complete the Azure Front Door updates for the domain that will set up the SSL certificate.</span></span>

## <a name="apex-domains"></a><span data-ttu-id="b3208-186">Apex-domener</span><span class="sxs-lookup"><span data-stu-id="b3208-186">Apex domains</span></span>

<span data-ttu-id="b3208-187">Den Commerce-støttede forekomsten av Azure Front Door støtter ikke Apex-domener (rotdomener som ikke inneholder underdomener).</span><span class="sxs-lookup"><span data-stu-id="b3208-187">The Commerce-supplied Azure Front Door instance does not support apex domains (root domains that do not contain subdomains).</span></span> <span data-ttu-id="b3208-188">Apex-domener krever at en IP-adresse løses, og den Commerce-støttede forekomsten av Azure Front Door finnes bare med virtuelle endepunkter.</span><span class="sxs-lookup"><span data-stu-id="b3208-188">Apex domains require an IP address to resolve, and the Commerce Azure Front Door instance exists with virtual endpoints only.</span></span> <span data-ttu-id="b3208-189">Hvis du vil bruke et Apex-domene, har du to alternativer:</span><span class="sxs-lookup"><span data-stu-id="b3208-189">To use an apex domain, you have two options:</span></span>

- <span data-ttu-id="b3208-190">**Alternativ 1** – Bruk DNS-leverandøren til å omadressere Apex-domenet til et www-domene.</span><span class="sxs-lookup"><span data-stu-id="b3208-190">**Option 1** - Use your DNS provider to redirect the apex domain to a "www" domain.</span></span> <span data-ttu-id="b3208-191">Fabrikam.com omadresserer for eksempel til `www.fabrikam.com`, der `www.fabrikam.com` er CNAME-posten som peker til den Commerce-driftede forekomsten av Azure Front Door.</span><span class="sxs-lookup"><span data-stu-id="b3208-191">For example, fabrikam.com redirects to `www.fabrikam.com` where `www.fabrikam.com` is the CNAME record that points to the Commerce-hosted Azure Front Door instance.</span></span>

- <span data-ttu-id="b3208-192">**Alternativ 2** – Konfigurer en forekomst av CDN/Front Door som du kan bruke til å drifte Apex-domenet.</span><span class="sxs-lookup"><span data-stu-id="b3208-192">**Option 2** - Set up a CDN/front door instance on your own to host the apex domain.</span></span>

> [!NOTE]
> <span data-ttu-id="b3208-193">Hvis du bruker Azure Front Door, må du også konfigurere Azure DNS i det samme abonnementet.</span><span class="sxs-lookup"><span data-stu-id="b3208-193">If you are using Azure Front Door, you must also set up an Azure DNS in the same subscription.</span></span> <span data-ttu-id="b3208-194">Apex-domenet som er driftet på Azure DNS, kan peke til din forekomst av Azure Front Door som en aliaspost.</span><span class="sxs-lookup"><span data-stu-id="b3208-194">The apex domain hosted on Azure DNS can point to your Azure Front Door as an alias record.</span></span> <span data-ttu-id="b3208-195">Dette er den eneste løsningen, ettersom Apex-domener alltid må peke til en IP-adresse.</span><span class="sxs-lookup"><span data-stu-id="b3208-195">This is the only work around, as apex domains must always point to an IP address.</span></span>

  ## <a name="additional-resources"></a><span data-ttu-id="b3208-196">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b3208-196">Additional resources</span></span>

  [<span data-ttu-id="b3208-197">Distribuere en ny e-handelsleier</span><span class="sxs-lookup"><span data-stu-id="b3208-197">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

  [<span data-ttu-id="b3208-198">Definere en kanal for nettbutikk</span><span class="sxs-lookup"><span data-stu-id="b3208-198">Set up an online store channel</span></span>](online-stores.md)

  [<span data-ttu-id="b3208-199">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="b3208-199">Create an e-commerce site</span></span>](create-ecommerce-site.md)

  [<span data-ttu-id="b3208-200">Knytte et Dynamics 365 Commerce-nettsted til en nettkanal</span><span class="sxs-lookup"><span data-stu-id="b3208-200">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

  [<span data-ttu-id="b3208-201">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="b3208-201">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

  [<span data-ttu-id="b3208-202">Laste opp masseomdirigeringer for URL-adresse</span><span class="sxs-lookup"><span data-stu-id="b3208-202">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

  [<span data-ttu-id="b3208-203">Konfigurere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="b3208-203">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

  [<span data-ttu-id="b3208-204">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="b3208-204">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

  [<span data-ttu-id="b3208-205">Konfigurere flere B2C-leiere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="b3208-205">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

  [<span data-ttu-id="b3208-206">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="b3208-206">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

  [<span data-ttu-id="b3208-207">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="b3208-207">Enable location-based store detection</span></span>](enable-store-detection.md)
