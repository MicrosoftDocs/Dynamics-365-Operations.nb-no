---
title: Distribuere en ny e-handelsleier
description: Dette emnet beskriver hvordan du distribuerer et nytt Dynamics 365 Commerce-e-handelsområde ved å bruke Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 157dc8225e5bbf9338a1b5a79a2880e8a8c4bf10
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517288"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="e6c85-103">Distribuere en ny e-handelsleier</span><span class="sxs-lookup"><span data-stu-id="e6c85-103">Deploy a new e-commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e6c85-104">Dette emnet beskriver hvordan du distribuerer et nytt Dynamics 365 Commerce-e-handelsområde ved å bruke Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="e6c85-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="e6c85-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="e6c85-105">Overview</span></span>

<span data-ttu-id="e6c85-106">Microsoft Dynamics Lifecycle Services (LCS) er et skybasert samarbeidsområde som partnere og kunder kan bruke til å administrere sine prosjekter og miljøer, vise nyeste informasjon om Microsoft Dynamics-produkter og -funksjoner og opprette, spore og bla gjennom kundestøttehendelser.</span><span class="sxs-lookup"><span data-stu-id="e6c85-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="e6c85-107">Funksjoner for e-handelsadministrasjon er integrert i LCS.</span><span class="sxs-lookup"><span data-stu-id="e6c85-107">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="e6c85-108">Hvis du vil vite mer om LCS, se [Brukerveiledning for Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="e6c85-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="e6c85-109">Kom i gang</span><span class="sxs-lookup"><span data-stu-id="e6c85-109">Get started</span></span>

<span data-ttu-id="e6c85-110">Før du kan initialisere e-handel, må du initialisere et prosjekt, et miljø og en Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="e6c85-110">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="e6c85-111">Hvis du vil utføre initialiseringen i LCS, må du ha tillatelse til rollen Prosjekteier eller rollen Miljøadministrator.</span><span class="sxs-lookup"><span data-stu-id="e6c85-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="e6c85-112">Produksjons- og sandkassemiljøtopologiene støttes.</span><span class="sxs-lookup"><span data-stu-id="e6c85-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="e6c85-113">Hvis du vil ha mer informasjon om miljøene, se [Miljøplanlegging](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="e6c85-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="e6c85-114">Hvis du vil ha mer informasjon om RCSU, se [Initialisere Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="e6c85-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="e6c85-115">Initialisere e-handel</span><span class="sxs-lookup"><span data-stu-id="e6c85-115">Initialize e-commerce</span></span>

<span data-ttu-id="e6c85-116">Bruk denne fremgangsmåten for å initialisere e-handel-funksjonen i et eksisterende miljø.</span><span class="sxs-lookup"><span data-stu-id="e6c85-116">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="e6c85-117">Før du begynner må du kontrollere at du har følgende nødvendige informasjon:</span><span class="sxs-lookup"><span data-stu-id="e6c85-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="e6c85-118">RCSU som blir brukt.</span><span class="sxs-lookup"><span data-stu-id="e6c85-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="e6c85-119">Microsoft Azure Active Directory-sikkerhetsgruppen som skal brukes til systemansvarlige i e-handel.</span><span class="sxs-lookup"><span data-stu-id="e6c85-119">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="e6c85-120">Microsoft Azure Active Directory-sikkerhetsgruppen som skal brukes for vurderings- og omtalemoderatorer.</span><span class="sxs-lookup"><span data-stu-id="e6c85-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="e6c85-121">Domenene som skal knyttes til miljøet.</span><span class="sxs-lookup"><span data-stu-id="e6c85-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="e6c85-122">I tillegg kan du samle inn følgende valgfrie opplysninger:</span><span class="sxs-lookup"><span data-stu-id="e6c85-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="e6c85-123">Azure AD-forretning-til-forbruker-informasjon (B2C):</span><span class="sxs-lookup"><span data-stu-id="e6c85-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="e6c85-124">Navn på leietaker.</span><span class="sxs-lookup"><span data-stu-id="e6c85-124">Tenant Name.</span></span>
    - <span data-ttu-id="e6c85-125">Klient-ID.</span><span class="sxs-lookup"><span data-stu-id="e6c85-125">Client ID.</span></span>
    - <span data-ttu-id="e6c85-126">Egendefinert domene for pålogging.</span><span class="sxs-lookup"><span data-stu-id="e6c85-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="e6c85-127">Svar-URL.</span><span class="sxs-lookup"><span data-stu-id="e6c85-127">Reply URL.</span></span>
    - <span data-ttu-id="e6c85-128">Policy-ID for registrering/pålogging.</span><span class="sxs-lookup"><span data-stu-id="e6c85-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="e6c85-129">Policy-ID for tilbakestilling av passord.</span><span class="sxs-lookup"><span data-stu-id="e6c85-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="e6c85-130">Policy-ID for redigering av profil.</span><span class="sxs-lookup"><span data-stu-id="e6c85-130">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="e6c85-131">Denne informasjonen kan legges til senere, via en serviceforespørsel.</span><span class="sxs-lookup"><span data-stu-id="e6c85-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="e6c85-132">Når du har samlet inn den nødvendige informasjonen, følger du denne fremgangsmåten for å initialisere e-handel.</span><span class="sxs-lookup"><span data-stu-id="e6c85-132">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="e6c85-133">Logg på [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="e6c85-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="e6c85-134">Åpne prosjektet som inneholder miljøet der du vil initialisere e-handel.</span><span class="sxs-lookup"><span data-stu-id="e6c85-134">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="e6c85-135">Velg miljøet i delen **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="e6c85-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="e6c85-136">Under **Miljøfunksjoner** velger du koblingen **Detaljhandelsstyring**.</span><span class="sxs-lookup"><span data-stu-id="e6c85-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="e6c85-137">Velg **Oppsett** i kategorien **e-handel**.</span><span class="sxs-lookup"><span data-stu-id="e6c85-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="e6c85-138">Det vises en dialogboks der du må skrive inn informasjonen som kreves for klargjøring.</span><span class="sxs-lookup"><span data-stu-id="e6c85-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="e6c85-139">Fyll inn nødvendig informasjon, og gå deretter til neste side.</span><span class="sxs-lookup"><span data-stu-id="e6c85-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="e6c85-140">På neste side fyller du ut nødvendig informasjon, og deretter sender du inn skjemaet.</span><span class="sxs-lookup"><span data-stu-id="e6c85-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="e6c85-141">Du kommer tilbake til kategorien **e-handel**, der du skal se at initialiseringen er startet.</span><span class="sxs-lookup"><span data-stu-id="e6c85-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="e6c85-142">Hvis du vil vise initialiseringsegenskaper, kan du velge **Oppdater** eller gå tilbake til **e-handel**.</span><span class="sxs-lookup"><span data-stu-id="e6c85-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="e6c85-143">Når e-handel startes fra LCS, klargjør systemet flere komponenter som kreves for e-handel, og knytter dem til miljøet.</span><span class="sxs-lookup"><span data-stu-id="e6c85-143">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="e6c85-144">Når klargjøringen er fullført, oppdateres kategorien **e-handel** på siden **Detaljhandelsstyring** for å gjenspeile klargjøringen.</span><span class="sxs-lookup"><span data-stu-id="e6c85-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="e6c85-145">Siden viser de siste tilpasningsdistribusjonene og statusen til eventuelle andre pågående distribusjoner.</span><span class="sxs-lookup"><span data-stu-id="e6c85-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="e6c85-146">Den inneholder også koblinger til e-handelsområdet og Commerce-områdebyggeren der områder redigeres.</span><span class="sxs-lookup"><span data-stu-id="e6c85-146">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="e6c85-147">Tilgang til Commerce-områdebygger</span><span class="sxs-lookup"><span data-stu-id="e6c85-147">Access Commerce site builder</span></span>

<span data-ttu-id="e6c85-148">Hvis du vil ha tilgang til Commerce-områdebygger, går du til **e-handel**-fanen på **Administrasjon av detaljhandel**-siden i LCS og velger **Verktøy for administrasjon av e-handelsområdet**-koblingen.</span><span class="sxs-lookup"><span data-stu-id="e6c85-148">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="e6c85-149">Målsiden for områdebygger viser en leiernivåvisning.</span><span class="sxs-lookup"><span data-stu-id="e6c85-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="e6c85-150">Fra denne siden kan du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="e6c85-150">From this page, you can:</span></span>

- <span data-ttu-id="e6c85-151">Endre innstillinger på leiernivå.</span><span class="sxs-lookup"><span data-stu-id="e6c85-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="e6c85-152">Navigere til et område du har opprettet og har tillatelse til å vise.</span><span class="sxs-lookup"><span data-stu-id="e6c85-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="e6c85-153">Få tilgang til Gjennomgå-funksjoner, som endring og rapportering.</span><span class="sxs-lookup"><span data-stu-id="e6c85-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="e6c85-154">Opprette et nytt område.</span><span class="sxs-lookup"><span data-stu-id="e6c85-154">Create a new site.</span></span> <span data-ttu-id="e6c85-155">Hvis du vil ha mer informasjon om hvordan du oppretter et nytt område, kan du se [Opprette et e-handelsområde](create-ecommerce-site.md) .</span><span class="sxs-lookup"><span data-stu-id="e6c85-155">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="e6c85-156">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e6c85-156">Additional resources</span></span>

[<span data-ttu-id="e6c85-157">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="e6c85-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="e6c85-158">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="e6c85-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="e6c85-159">Knytte et Dynamics 365 Commerce-nettsted til en nettkanal</span><span class="sxs-lookup"><span data-stu-id="e6c85-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="e6c85-160">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="e6c85-160">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="e6c85-161">Laste opp masseomdirigeringer for URL-adresse</span><span class="sxs-lookup"><span data-stu-id="e6c85-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="e6c85-162">Konfigurere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="e6c85-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="e6c85-163">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="e6c85-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="e6c85-164">Konfigurere flere B2C-leiere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="e6c85-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="e6c85-165">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="e6c85-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="e6c85-166">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="e6c85-166">Enable location-based store detection</span></span>](enable-store-detection.md)
