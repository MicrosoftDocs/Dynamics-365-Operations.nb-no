---
title: Implementeringsalternativer for innholdsleveringsnettverk
description: Dette emnet gjennomgår de ulike alternativene for CDN-implementering (Content Delivery Network) som kan brukes i Microsoft Dynamics 365 Commerce-miljøer. Disse alternativene omfatter innebygde, Commerce-formidlede forekomster av Azure Front Door og kundeeide forekomster av Azure Front Door.
author: BrianShook
manager: AnnBe
ms.date: 03/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ae0769b7e19f80244186c51454444c499c5e497f
ms.sourcegitcommit: 3fe4d9a33447aa8a62d704fbbf18aeb9cb667baa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2021
ms.locfileid: "5582809"
---
# <a name="content-delivery-network-implementation-options"></a><span data-ttu-id="4cf46-104">Implementeringsalternativer for innholdsleveringsnettverk</span><span class="sxs-lookup"><span data-stu-id="4cf46-104">Content delivery network implementation options</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4cf46-105">Dette emnet gjennomgår de ulike alternativene for CDN-implementering (Content Delivery Network) som kan brukes i Microsoft Dynamics 365 Commerce-miljøer.</span><span class="sxs-lookup"><span data-stu-id="4cf46-105">This topic reviews the different options for content delivery network (CDN) implementation that can be used with Microsoft Dynamics 365 Commerce environments.</span></span> <span data-ttu-id="4cf46-106">Disse alternativene omfatter innebygde, Commerce-formidlede forekomster av Azure Front Door og kundeeide forekomster av Azure Front Door.</span><span class="sxs-lookup"><span data-stu-id="4cf46-106">These options include native, Commerce-provided instances of Azure Front Door and customer-owned instances of Azure Front Door.</span></span>

<span data-ttu-id="4cf46-107">Commerce-kunder har flere alternativer når de vurderer hvilken CDN-tjeneste som skal brukes med Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="4cf46-107">Commerce customers have several options when they are considering which CDN service to use with their Commerce environment.</span></span> <span data-ttu-id="4cf46-108">Commerce frigis med grunnleggende støtte for Azure Front Door, som dekker grunnleggende driftingskrav og egendefinerte domenekrav.</span><span class="sxs-lookup"><span data-stu-id="4cf46-108">Commerce is released with basic Azure Front Door support that covers basic hosting and custom domain requirements.</span></span> <span data-ttu-id="4cf46-109">For firmaer som vil ha mer kontroll og mer spesifikke sikkerhetsegenskaper, for eksempel webprogrambrannmur (WAF), kan det være best å bruke enten en kundeeid forekomst av Azure Front Door eller en ekstern CDN-tjeneste.</span><span class="sxs-lookup"><span data-stu-id="4cf46-109">For companies that want more control and more specific security abilities, such as a web application firewall (WAF), the best option might be to use either a customer-owned instance of Azure Front Door or an external CDN service.</span></span>

<span data-ttu-id="4cf46-110">Følgende tre CDN-implementeringsalternativer kan brukes med Commerce-miljøer:</span><span class="sxs-lookup"><span data-stu-id="4cf46-110">The following three CDN implementation options can be used with Commerce environments:</span></span>

- <span data-ttu-id="4cf46-111">Den Commerce-formidlede forekomsten av Azure Front Door</span><span class="sxs-lookup"><span data-stu-id="4cf46-111">The Commerce-provided instance of Azure Front Door</span></span>
- <span data-ttu-id="4cf46-112">En kundeeid forekomst av Azure Front Door (for økt kontroll og flere sikkerhetsfunksjoner)</span><span class="sxs-lookup"><span data-stu-id="4cf46-112">A customer-owned instance of Azure Front Door (for increased control and additional security features)</span></span>
- <span data-ttu-id="4cf46-113">En ekstern CDN-tjeneste</span><span class="sxs-lookup"><span data-stu-id="4cf46-113">An external CDN service</span></span>

<span data-ttu-id="4cf46-114">Alle de tre CDN-implementeringsalternativene leverer bare dynamisk HTML-innhold fra egendefinerte domener.</span><span class="sxs-lookup"><span data-stu-id="4cf46-114">All three CDN implementation options deliver only dynamic HTML content from custom domains.</span></span> <span data-ttu-id="4cf46-115">Commerce håndterer automatisk alle JavaScript, gjennomgripende stilark (CSS), bilder, video og annet statisk innhold via Microsoft-administrerte CDN-er.</span><span class="sxs-lookup"><span data-stu-id="4cf46-115">Commerce automatically handles all JavaScript, Cascading Style Sheets (CSS), images, video, and other static content through Microsoft-managed CDNs.</span></span> <span data-ttu-id="4cf46-116">Alternativet du velger, fastslår driftsfunksjonene, kontrollfunksjonene og ytterligere sikkerhetsfunksjoner som er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="4cf46-116">The option that you choose determines the operational capabilities, control capabilities, and additional security capabilities that are available.</span></span>

<span data-ttu-id="4cf46-117">Illustrasjonen nedenfor viser en oversikt over Commerce-arkitekturen.</span><span class="sxs-lookup"><span data-stu-id="4cf46-117">The following illustration shows an overview of the Commerce architecture.</span></span>

![Oversikt over Commerce-arkitekturen](media/Commerce_CDN-Option_ComparisonModels.png)

<span data-ttu-id="4cf46-119">Hvis du vil ha mer informasjon om hvordan du definerer en forekomst av Azure Front Door for Commerce-området, kan du se [Legg til CDN-støtte](add-cdn-support.md).</span><span class="sxs-lookup"><span data-stu-id="4cf46-119">For more information about how to set up an instance of Azure Front Door for your Commerce site, see [Add CDN Support](add-cdn-support.md).</span></span>

## <a name="use-the-commerce-provided-azure-front-door-instance"></a><span data-ttu-id="4cf46-120">Bruke den Commerce-formidlede forekomsten av Azure Front Door</span><span class="sxs-lookup"><span data-stu-id="4cf46-120">Use the Commerce-provided Azure Front Door instance</span></span>

<span data-ttu-id="4cf46-121">I tabellen nedenfor finner du en oversikt over fordeler og ulemper ved å bruke den Commerce-formidlede forekomsten av Azure Front Door til å administrere innholdsendepunkt.</span><span class="sxs-lookup"><span data-stu-id="4cf46-121">The following table lists the pros and cons of using the Commerce-provided instance of Azure Front Door to manage content endpoints.</span></span>

| <span data-ttu-id="4cf46-122">Fordeler</span><span class="sxs-lookup"><span data-stu-id="4cf46-122">Pros</span></span> | <span data-ttu-id="4cf46-123">Ulemper</span><span class="sxs-lookup"><span data-stu-id="4cf46-123">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="4cf46-124">Forekomsten er inkludert i Commerce-kostnaden.</span><span class="sxs-lookup"><span data-stu-id="4cf46-124">The instance is included in the Commerce cost.</span></span></li><li><span data-ttu-id="4cf46-125">Ettersom forekomsten administreres av Commerce-teamet, kreves det mindre vedlikehold, og det finnes trinn for delt oppsett.</span><span class="sxs-lookup"><span data-stu-id="4cf46-125">Because the instance is managed by the Commerce team, less maintenance is required, and there are shared setup steps.</span></span></li><li><span data-ttu-id="4cf46-126">Den Azure-driftede infrastrukturen er skalerbar, sikker og pålitelig.</span><span class="sxs-lookup"><span data-stu-id="4cf46-126">The Azure-hosted infrastructure is scalable, secure, and reliable.</span></span></li><li><span data-ttu-id="4cf46-127">SSL-sertifikatet (Secure Sockets Layer) krever et engangsoppsett og fornyes automatisk.</span><span class="sxs-lookup"><span data-stu-id="4cf46-127">The Secure Sockets Layer (SSL) certificate requires a one-time setup and is automatically renewed.</span></span></li><li><span data-ttu-id="4cf46-128">Forekomsten blir overvåket for feil og mangler av Commerce-teamet.</span><span class="sxs-lookup"><span data-stu-id="4cf46-128">The instance is monitored for errors and anomalies by the Commerce team.</span></span></li></ul> | <ul><li><span data-ttu-id="4cf46-129">En WAF støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="4cf46-129">A WAF isn't supported.</span></span></li><li><span data-ttu-id="4cf46-130">Det finnes ingen bestemte tilpassinger eller justeringer.</span><span class="sxs-lookup"><span data-stu-id="4cf46-130">There are no specific customizations or setting adjustments.</span></span></li><li><span data-ttu-id="4cf46-131">Forekomsten avhenger av Commerce-teamet for oppdateringer eller endringer.</span><span class="sxs-lookup"><span data-stu-id="4cf46-131">The instance depends on the Commerce team for updates or changes.</span></span></li><li><span data-ttu-id="4cf46-132">En separat forekomst av Azure Front Door kreves for apex-domener, og det kreves ekstra arbeid for å integrere apex-domener Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="4cf46-132">A separate Azure Front Door instance is required for apex domains, and extra work is required to integrate apex domains with Azure DNS.</span></span></li><li><span data-ttu-id="4cf46-133">Det er ikke angitt noe telemetri om svar per andre (RPS) eller om feilraten til kunden.</span><span class="sxs-lookup"><span data-stu-id="4cf46-133">No telemetry about responses per second (RPS) or the error rate is provided to the customer.</span></span></li></ul> |

<span data-ttu-id="4cf46-134">Illustrasjonen nedenfor viser arkitekturen i forekomsten av den Commerce-formidlede forekomsten for Azure Front Door.</span><span class="sxs-lookup"><span data-stu-id="4cf46-134">The following illustration shows the architecture of the Commerce-provided Azure Front Door instance.</span></span>

![Commerce-formidlet forekomst av Azure Front Door](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a><span data-ttu-id="4cf46-136">Bruke en kundeeid forekomst av Azure Front Door</span><span class="sxs-lookup"><span data-stu-id="4cf46-136">Use a customer-owned Azure Front Door instance</span></span>

<span data-ttu-id="4cf46-137">I tabellen nedenfor finner du en oversikt over fordeler og ulemper ved å bruke en kundeeid forekomst av Azure Front Door til å administrere innholdsendepunkt.</span><span class="sxs-lookup"><span data-stu-id="4cf46-137">The following table lists the pros and cons of using a customer-owned instance of Azure Front Door to manage content endpoints.</span></span>

| <span data-ttu-id="4cf46-138">Fordeler</span><span class="sxs-lookup"><span data-stu-id="4cf46-138">Pros</span></span> | <span data-ttu-id="4cf46-139">Ulemper</span><span class="sxs-lookup"><span data-stu-id="4cf46-139">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="4cf46-140">Oppsettet er sikkert og enkelt å administrere.</span><span class="sxs-lookup"><span data-stu-id="4cf46-140">Setup is secure and easy to manage.</span></span></li><li><span data-ttu-id="4cf46-141">Den Azure-driftede infrastrukturen er skalerbar, sikker og pålitelig.</span><span class="sxs-lookup"><span data-stu-id="4cf46-141">The Azure-hosted infrastructure is scalable, secure, and reliable.</span></span></li><li><span data-ttu-id="4cf46-142">Forekomsten tillater WAF-integrering og granulære regelkontroller for mer detaljert sikkerhet som er tilpasset spesielt for området.</span><span class="sxs-lookup"><span data-stu-id="4cf46-142">The instance allows for WAF integration and granular rule controls for finer-grade security that is tuned specifically for your site.</span></span></li><li><span data-ttu-id="4cf46-143">Forekomsten gir bedre kontroll over SSL-sertifikater (både kundeeide og Azure Front Door-administrerte) og domenekobling.</span><span class="sxs-lookup"><span data-stu-id="4cf46-143">The instance allows for finer control of SSL certificates (both customer-owned and Azure Front Door–managed) and domain linking.</span></span></li><li><span data-ttu-id="4cf46-144">Forekomsten tilbyr en apex-domeneløsning hvis den er paret direkte med Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="4cf46-144">The instance offers an apex domain solution if it's paired directly with Azure DNS.</span></span></li><li><span data-ttu-id="4cf46-145">Telemetri og varsling følger med.</span><span class="sxs-lookup"><span data-stu-id="4cf46-145">Telemetry and alerting are provided.</span></span></li><li><span data-ttu-id="4cf46-146">SSL-sertifikatet krever et engangsoppsett og fornyes automatisk.</span><span class="sxs-lookup"><span data-stu-id="4cf46-146">The SSL certificate requires a one-time setup and is automatically renewed.</span></span></li></ul> | <ul><li><span data-ttu-id="4cf46-147">Forekomsten er selvstyrt.</span><span class="sxs-lookup"><span data-stu-id="4cf46-147">The instance is self-managed.</span></span></li><li><span data-ttu-id="4cf46-148">Innledende kunnskapsoppgradering er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="4cf46-148">Initial knowledge ramp-up is required.</span></span></li></ul> |

<span data-ttu-id="4cf46-149">Illustrasjonen nedenfor viser en Commerce-infrastruktur som omfatter en kundeeid forekomst av Azure Front Door.</span><span class="sxs-lookup"><span data-stu-id="4cf46-149">The following illustration shows a Commerce infrastructure that includes a customer-owned Azure Front Door instance.</span></span>

![Commerce-infrastruktur som omfatter en kundeeid forekomst av Azure Front Door](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a><span data-ttu-id="4cf46-151">Bruke en ekstern CDN-tjeneste</span><span class="sxs-lookup"><span data-stu-id="4cf46-151">Use an external CDN service</span></span>

<span data-ttu-id="4cf46-152">I tabellen nedenfor finner du en oversikt over fordeler og ulemper ved bruk av en ekstern CDN-tjeneste for å administrere innholdsendepunkter.</span><span class="sxs-lookup"><span data-stu-id="4cf46-152">The following table lists the pros and cons of using an external CDN service to manage content endpoints.</span></span>

| <span data-ttu-id="4cf46-153">Fordeler</span><span class="sxs-lookup"><span data-stu-id="4cf46-153">Pros</span></span> | <span data-ttu-id="4cf46-154">Ulemper</span><span class="sxs-lookup"><span data-stu-id="4cf46-154">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="4cf46-155">Dette alternativet er nyttig når det eksisterende domenet allerede er vert for en ekstern CDN.</span><span class="sxs-lookup"><span data-stu-id="4cf46-155">This option is useful when the existing domain is already hosted on an external CDN.</span></span></li><li><span data-ttu-id="4cf46-156">Konkurrerende CDN-er (for eksempel Akamai) kan ha flere WAF-funksjoner.</span><span class="sxs-lookup"><span data-stu-id="4cf46-156">Competitor CDNs (for example, Akamai) might have more WAF capabilities.</span></span></li></ul> | <ul><li><span data-ttu-id="4cf46-157">En separat kontrakt og ekstra etterkalkulering kreves.</span><span class="sxs-lookup"><span data-stu-id="4cf46-157">A separate contract and additional costing are required.</span></span></li><li><span data-ttu-id="4cf46-158">SSL kan påløpe ekstra kostnader.</span><span class="sxs-lookup"><span data-stu-id="4cf46-158">SSL might incur additional costs.</span></span></li><li><span data-ttu-id="4cf46-159">Ettersom tjenesten er atskilt fra skystrukturen i Azure, må tilleggsinfrastruktur administreres.</span><span class="sxs-lookup"><span data-stu-id="4cf46-159">Because the service is separate from the Azure cloud structure, additional infrastructure must be managed.</span></span></li><li><span data-ttu-id="4cf46-160">Tjenesten kan kreve lengre tidsinvesteringer i endepunkts- og sikkerhetsoppsett.</span><span class="sxs-lookup"><span data-stu-id="4cf46-160">The service might require longer time investments in endpoint and security setup.</span></span></li><li><span data-ttu-id="4cf46-161">Tjenesten er selvstyrt.</span><span class="sxs-lookup"><span data-stu-id="4cf46-161">The service is self-managed.</span></span></li><li><span data-ttu-id="4cf46-162">Tjenesten er selvovervåket.</span><span class="sxs-lookup"><span data-stu-id="4cf46-162">The service is self-monitored.</span></span></li></ul> |

<span data-ttu-id="4cf46-163">Illustrasjonen nedenfor viser en Commerce-infrastruktur som omfatter en ekstern CDN-tjeneste.</span><span class="sxs-lookup"><span data-stu-id="4cf46-163">The following illustration shows a Commerce infrastructure that includes an external CDN service.</span></span>

![Commerce-infrastruktur som omfatter en ekstern CDN-tjeneste](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a><span data-ttu-id="4cf46-165">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4cf46-165">Additional resources</span></span>

[<span data-ttu-id="4cf46-166">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="4cf46-166">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)