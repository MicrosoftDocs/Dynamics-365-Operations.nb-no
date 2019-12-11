---
title: Distribuere en ny e-handelsleier
description: Dette emnet beskriver hvordan du distribuerer en ny e-handelsleier ved å bruke Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c2632632b9b21dd3a88e9a4df0e65cfd28e579d2
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697457"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="27744-103">Distribuere en ny e-handelsleier</span><span class="sxs-lookup"><span data-stu-id="27744-103">Deploy a new e-Commerce tenant</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="27744-104">Dette emnet beskriver hvordan du distribuerer et nytt e-handelsområde ved å bruke Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="27744-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="27744-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="27744-105">Overview</span></span>
    
<span data-ttu-id="27744-106">Microsoft Dynamics Lifecycle Services (LCS) er et skybasert samarbeidsområde som partnere og kunder kan bruke til å administrere sine prosjekter og miljøer, vise nyeste informasjon om Microsoft Dynamics-produkter og -funksjoner og opprette, spore og bla gjennom kundestøttehendelser.</span><span class="sxs-lookup"><span data-stu-id="27744-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="27744-107">Funksjoner for e-handelsadministrasjon er integrert i LCS.</span><span class="sxs-lookup"><span data-stu-id="27744-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="27744-108">Hvis du vil vite mer om LCS, se [Brukerveiledning for Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="27744-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="27744-109">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="27744-109">Get started</span></span>

<span data-ttu-id="27744-110">Før du kan initialisere e-handel, må du initialisere et prosjekt, et miljø og en Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="27744-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="27744-111">Hvis du vil utføre initialiseringen i LCS, må du ha tillatelse til rollen Prosjekteier eller rollen Miljøadministrator.</span><span class="sxs-lookup"><span data-stu-id="27744-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="27744-112">Produksjons- og sandkassemiljøtopologiene støttes.</span><span class="sxs-lookup"><span data-stu-id="27744-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="27744-113">Hvis du vil ha mer informasjon om miljøene, se [Miljøplanlegging](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="27744-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="27744-114">Hvis du vil ha mer informasjon om RCSU, se [Initialisere Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="27744-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="27744-115">Initialisere e-handel</span><span class="sxs-lookup"><span data-stu-id="27744-115">Initialize e-Commerce</span></span>

<span data-ttu-id="27744-116">Bruk denne fremgangsmåten for å initialisere e-handel-funksjonen i et eksisterende miljø.</span><span class="sxs-lookup"><span data-stu-id="27744-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="27744-117">Før du begynner må du kontrollere at du har følgende nødvendige informasjon:</span><span class="sxs-lookup"><span data-stu-id="27744-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="27744-118">RCSU som blir brukt.</span><span class="sxs-lookup"><span data-stu-id="27744-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="27744-119">Microsoft Azure Active Directory-sikkerhetsgruppen som skal brukes til systemansvarlige i e-handel.</span><span class="sxs-lookup"><span data-stu-id="27744-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="27744-120">Microsoft Azure Active Directory-sikkerhetsgruppen som skal brukes for vurderings- og omtalemoderatorer.</span><span class="sxs-lookup"><span data-stu-id="27744-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="27744-121">Domenene som skal knyttes til miljøet.</span><span class="sxs-lookup"><span data-stu-id="27744-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="27744-122">I tillegg kan du samle inn følgende valgfrie opplysninger:</span><span class="sxs-lookup"><span data-stu-id="27744-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="27744-123">Azure AD-forretning-til-forbruker-informasjon (B2C):</span><span class="sxs-lookup"><span data-stu-id="27744-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="27744-124">Navn på leietaker.</span><span class="sxs-lookup"><span data-stu-id="27744-124">Tenant Name.</span></span>
    - <span data-ttu-id="27744-125">Klient-ID.</span><span class="sxs-lookup"><span data-stu-id="27744-125">Client ID.</span></span>
    - <span data-ttu-id="27744-126">Egendefinert domene for pålogging.</span><span class="sxs-lookup"><span data-stu-id="27744-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="27744-127">Svar-URL.</span><span class="sxs-lookup"><span data-stu-id="27744-127">Reply URL.</span></span>
    - <span data-ttu-id="27744-128">Policy-ID for registrering/pålogging.</span><span class="sxs-lookup"><span data-stu-id="27744-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="27744-129">Policy-ID for tilbakestilling av passord.</span><span class="sxs-lookup"><span data-stu-id="27744-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="27744-130">Policy-ID for redigering av profil.</span><span class="sxs-lookup"><span data-stu-id="27744-130">Edit Profile Policy ID.</span></span>

[!NOTE]
<span data-ttu-id="27744-131">Denne informasjonen kan legges til senere, via en serviceforespørsel.</span><span class="sxs-lookup"><span data-stu-id="27744-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="27744-132">Når du har samlet inn den nødvendige informasjonen, følger du denne fremgangsmåten for å initialisere e-handel.</span><span class="sxs-lookup"><span data-stu-id="27744-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="27744-133">Logg på [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="27744-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="27744-134">Åpne prosjektet som inneholder miljøet der du vil initialisere e-handel.</span><span class="sxs-lookup"><span data-stu-id="27744-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="27744-135">Velg miljøet i delen **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="27744-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="27744-136">Under **Miljøfunksjoner** velger du koblingen **Detaljhandelsstyring**.</span><span class="sxs-lookup"><span data-stu-id="27744-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="27744-137">Velg **Oppsett** i kategorien **e-handel**.</span><span class="sxs-lookup"><span data-stu-id="27744-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="27744-138">Det vises en dialogboks der du må skrive inn informasjonen som kreves for klargjøring.</span><span class="sxs-lookup"><span data-stu-id="27744-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="27744-139">Fyll inn nødvendig informasjon, og gå deretter til neste side.</span><span class="sxs-lookup"><span data-stu-id="27744-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="27744-140">På neste side fyller du ut nødvendig informasjon, og deretter sender du inn skjemaet.</span><span class="sxs-lookup"><span data-stu-id="27744-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="27744-141">Du kommer tilbake til kategorien **e-handel**, der du skal se at initialiseringen er startet.</span><span class="sxs-lookup"><span data-stu-id="27744-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="27744-142">Hvis du vil vise initialiseringsegenskaper, kan du velge **Oppdater** eller gå tilbake til **e-handel**.</span><span class="sxs-lookup"><span data-stu-id="27744-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="27744-143">Når e-handel startes fra LCS, klargjør systemet flere komponenter som kreves for e-handel, og knytter dem til miljøet.</span><span class="sxs-lookup"><span data-stu-id="27744-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="27744-144">Når klargjøringen er fullført, oppdateres kategorien **e-handel** på siden **Detaljhandelsstyring** for å gjenspeile klargjøringen.</span><span class="sxs-lookup"><span data-stu-id="27744-144">After provisioning is completed, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="27744-145">Siden viser de siste tilpasningsdistribusjonene og statusen til eventuelle andre pågående distribusjoner.</span><span class="sxs-lookup"><span data-stu-id="27744-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="27744-146">Den inneholder også koblinger til webområdet for e-handel og områdeadministrasjonsverktøyet for e-handel (redigeringsverktøyet).</span><span class="sxs-lookup"><span data-stu-id="27744-146">It also includes links to the e-Commerce site and the e-Commerce site management tool (the authoring tool).</span></span>

## <a name="access-the-authoring-environment"></a><span data-ttu-id="27744-147">Få tilgang til redigeirngsmiljøet</span><span class="sxs-lookup"><span data-stu-id="27744-147">Access the authoring environment</span></span>

<span data-ttu-id="27744-148">Du får tilgang til redigeringsmiljøet ved å gå til kategorien **e-handel** på siden **Detaljhandelsstyring**.</span><span class="sxs-lookup"><span data-stu-id="27744-148">To access the authoring environment, go to the **e-Commerce** tab on the **Retail management** page.</span></span> <span data-ttu-id="27744-149">Der finner du koblinger til e-handelsområdet og områdebehandlingsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="27744-149">There, you will find links to your e-Commerce site and the site management tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="27744-150">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="27744-150">Additional resources</span></span>

[<span data-ttu-id="27744-151">Oversikt over nettbutikk</span><span class="sxs-lookup"><span data-stu-id="27744-151">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="27744-152">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="27744-152">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="27744-153">Knytte et nettområde til en kanal</span><span class="sxs-lookup"><span data-stu-id="27744-153">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="27744-154">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="27744-154">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="27744-155">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="27744-155">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="27744-156">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="27744-156">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="27744-157">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="27744-157">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
