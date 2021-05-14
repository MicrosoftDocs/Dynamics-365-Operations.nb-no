---
title: Distribuere en ny e-handelsleier
description: Dette emnet beskriver hvordan du distribuerer et nytt Dynamics 365 Commerce-e-handelsområde ved å bruke Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b228babfd32a4191eeed2a6d924a8b99f1a5311
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936712"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="68170-103">Distribuere en ny e-handelsleier</span><span class="sxs-lookup"><span data-stu-id="68170-103">Deploy a new e-commerce tenant</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="68170-104">Dette emnet beskriver hvordan du distribuerer et nytt Dynamics 365 Commerce-e-handelsområde ved å bruke Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="68170-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="68170-105">Microsoft Dynamics Lifecycle Services (LCS) er et skybasert samarbeidsområde som partnere og kunder kan bruke til å administrere sine prosjekter og miljøer, vise nyeste informasjon om Microsoft Dynamics-produkter og -funksjoner og opprette, spore og bla gjennom kundestøttehendelser.</span><span class="sxs-lookup"><span data-stu-id="68170-105">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="68170-106">Funksjoner for e-handelsadministrasjon er integrert i LCS.</span><span class="sxs-lookup"><span data-stu-id="68170-106">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="68170-107">Hvis du vil vite mer om LCS, se [Brukerveiledning for Lifecycle Services](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="68170-107">To learn more about LCS, see the [Lifecycle Services User Guide](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="68170-108">Kom i gang</span><span class="sxs-lookup"><span data-stu-id="68170-108">Get started</span></span>

<span data-ttu-id="68170-109">Før du kan initialisere e-handel, må du initialisere et prosjekt, et miljø og en Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="68170-109">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="68170-110">Hvis du vil utføre initialiseringen i LCS, må du ha tillatelse til rollen Prosjekteier eller rollen Miljøadministrator.</span><span class="sxs-lookup"><span data-stu-id="68170-110">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="68170-111">Produksjons- og sandkassemiljøtopologiene støttes.</span><span class="sxs-lookup"><span data-stu-id="68170-111">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="68170-112">Hvis du vil ha mer informasjon om miljøene, se [Miljøplanlegging](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="68170-112">For more information about environments, see [Environment planning](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="68170-113">Hvis du vil ha mer informasjon om RCSU, se [Initialisere Retail Cloud Scale Unit](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="68170-113">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="68170-114">Initialisere e-handel</span><span class="sxs-lookup"><span data-stu-id="68170-114">Initialize e-commerce</span></span>

<span data-ttu-id="68170-115">Bruk denne fremgangsmåten for å initialisere e-handel-funksjonen i et eksisterende miljø.</span><span class="sxs-lookup"><span data-stu-id="68170-115">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="68170-116">Før du begynner må du kontrollere at du har følgende nødvendige informasjon:</span><span class="sxs-lookup"><span data-stu-id="68170-116">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="68170-117">RCSU som blir brukt.</span><span class="sxs-lookup"><span data-stu-id="68170-117">The RCSU that will be used.</span></span>
- <span data-ttu-id="68170-118">Microsoft Azure Active Directory-sikkerhetsgruppen som skal brukes til systemansvarlige i e-handel.</span><span class="sxs-lookup"><span data-stu-id="68170-118">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="68170-119">Microsoft Azure Active Directory-sikkerhetsgruppen som skal brukes for vurderings- og omtalemoderatorer.</span><span class="sxs-lookup"><span data-stu-id="68170-119">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="68170-120">Domenene som skal knyttes til miljøet.</span><span class="sxs-lookup"><span data-stu-id="68170-120">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="68170-121">I tillegg kan du samle inn følgende valgfrie opplysninger:</span><span class="sxs-lookup"><span data-stu-id="68170-121">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="68170-122">Azure AD-forretning-til-forbruker-informasjon (B2C):</span><span class="sxs-lookup"><span data-stu-id="68170-122">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="68170-123">Navn på leietaker.</span><span class="sxs-lookup"><span data-stu-id="68170-123">Tenant Name.</span></span>
    - <span data-ttu-id="68170-124">Klient-ID.</span><span class="sxs-lookup"><span data-stu-id="68170-124">Client ID.</span></span>
    - <span data-ttu-id="68170-125">Egendefinert domene for pålogging.</span><span class="sxs-lookup"><span data-stu-id="68170-125">Login Custom Domain.</span></span>
    - <span data-ttu-id="68170-126">Svar-URL.</span><span class="sxs-lookup"><span data-stu-id="68170-126">Reply URL.</span></span>
    - <span data-ttu-id="68170-127">Policy-ID for registrering/pålogging.</span><span class="sxs-lookup"><span data-stu-id="68170-127">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="68170-128">Policy-ID for tilbakestilling av passord.</span><span class="sxs-lookup"><span data-stu-id="68170-128">Reset password Policy ID.</span></span>
    - <span data-ttu-id="68170-129">Policy-ID for redigering av profil.</span><span class="sxs-lookup"><span data-stu-id="68170-129">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="68170-130">Denne informasjonen kan legges til senere, via en serviceforespørsel.</span><span class="sxs-lookup"><span data-stu-id="68170-130">This information can be added later, through a service request.</span></span>

<span data-ttu-id="68170-131">Når du har samlet inn den nødvendige informasjonen, følger du denne fremgangsmåten for å initialisere e-handel.</span><span class="sxs-lookup"><span data-stu-id="68170-131">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="68170-132">Logg på [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="68170-132">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="68170-133">Åpne prosjektet som inneholder miljøet der du vil initialisere e-handel.</span><span class="sxs-lookup"><span data-stu-id="68170-133">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="68170-134">Velg miljøet i delen **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="68170-134">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="68170-135">Under **Miljøfunksjoner** velger du koblingen **Detaljhandelsstyring**.</span><span class="sxs-lookup"><span data-stu-id="68170-135">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="68170-136">Velg **Oppsett** i kategorien **e-handel**.</span><span class="sxs-lookup"><span data-stu-id="68170-136">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="68170-137">Det vises en dialogboks der du må skrive inn informasjonen som kreves for klargjøring.</span><span class="sxs-lookup"><span data-stu-id="68170-137">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="68170-138">Fyll inn nødvendig informasjon, og gå deretter til neste side.</span><span class="sxs-lookup"><span data-stu-id="68170-138">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="68170-139">På neste side fyller du ut nødvendig informasjon, og deretter sender du inn skjemaet.</span><span class="sxs-lookup"><span data-stu-id="68170-139">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="68170-140">Du kommer tilbake til kategorien **e-handel**, der du skal se at initialiseringen er startet.</span><span class="sxs-lookup"><span data-stu-id="68170-140">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="68170-141">Hvis du vil vise initialiseringsegenskaper, kan du velge **Oppdater** eller gå tilbake til **e-handel**.</span><span class="sxs-lookup"><span data-stu-id="68170-141">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="68170-142">Når e-handel startes fra LCS, klargjør systemet flere komponenter som kreves for e-handel, og knytter dem til miljøet.</span><span class="sxs-lookup"><span data-stu-id="68170-142">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="68170-143">Når klargjøringen er fullført, oppdateres kategorien **e-handel** på siden **Detaljhandelsstyring** for å gjenspeile klargjøringen.</span><span class="sxs-lookup"><span data-stu-id="68170-143">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="68170-144">Siden viser de siste tilpasningsdistribusjonene og statusen til eventuelle andre pågående distribusjoner.</span><span class="sxs-lookup"><span data-stu-id="68170-144">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="68170-145">Den inneholder også koblinger til e-handelsområdet og Commerce-områdebyggeren der områder redigeres.</span><span class="sxs-lookup"><span data-stu-id="68170-145">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="68170-146">Tilgang til Commerce-områdebygger</span><span class="sxs-lookup"><span data-stu-id="68170-146">Access Commerce site builder</span></span>

<span data-ttu-id="68170-147">Hvis du vil ha tilgang til Commerce-områdebygger, går du til **e-handel**-fanen på **Administrasjon av detaljhandel**-siden i LCS og velger **Verktøy for administrasjon av e-handelsområdet**-koblingen.</span><span class="sxs-lookup"><span data-stu-id="68170-147">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="68170-148">Målsiden for områdebygger viser en leiernivåvisning.</span><span class="sxs-lookup"><span data-stu-id="68170-148">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="68170-149">Fra denne siden kan du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="68170-149">From this page, you can:</span></span>

- <span data-ttu-id="68170-150">Endre innstillinger på leiernivå.</span><span class="sxs-lookup"><span data-stu-id="68170-150">Modify tenant-level settings.</span></span>
- <span data-ttu-id="68170-151">Navigere til et område du har opprettet og har tillatelse til å vise.</span><span class="sxs-lookup"><span data-stu-id="68170-151">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="68170-152">Få tilgang til Gjennomgå-funksjoner, som endring og rapportering.</span><span class="sxs-lookup"><span data-stu-id="68170-152">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="68170-153">Opprette et nytt område.</span><span class="sxs-lookup"><span data-stu-id="68170-153">Create a new site.</span></span> <span data-ttu-id="68170-154">Hvis du vil ha mer informasjon om hvordan du oppretter et nytt område, kan du se [Opprette et e-handelsområde](create-ecommerce-site.md) .</span><span class="sxs-lookup"><span data-stu-id="68170-154">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="68170-155">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="68170-155">Additional resources</span></span>

[<span data-ttu-id="68170-156">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="68170-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="68170-157">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="68170-157">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="68170-158">Knytte et Dynamics 365 Commerce-nettsted til en nettkanal</span><span class="sxs-lookup"><span data-stu-id="68170-158">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="68170-159">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="68170-159">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="68170-160">Laste opp masseomdirigeringer for URL-adresse</span><span class="sxs-lookup"><span data-stu-id="68170-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="68170-161">Konfigurere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="68170-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="68170-162">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="68170-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="68170-163">Konfigurere flere B2C-leiere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="68170-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="68170-164">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="68170-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="68170-165">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="68170-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]