---
title: Klargjøre et Commerce-forhåndsvisningsmiljø
description: Dette emnet forklarer hvordan du klargjør et Microsoft Dynamics 365 Commerce-forhåndsvisningsmiljø.
author: psimolin
manager: annbe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934754"
---
# <a name="provision-a-commerce-preview-environment"></a><span data-ttu-id="e95b8-103">Klargjøre et Commerce-forhåndsvisningsmiljø</span><span class="sxs-lookup"><span data-stu-id="e95b8-103">Provision a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e95b8-104">Dette emnet forklarer hvordan du klargjør et Microsoft Dynamics 365 Commerce-forhåndsvisningsmiljø.</span><span class="sxs-lookup"><span data-stu-id="e95b8-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="e95b8-105">Før du begynner anbefaler vi at du minst skumleser hele emnet for å få en pekepinn på hva prosessen medfører og hva dette emnet inneholder.</span><span class="sxs-lookup"><span data-stu-id="e95b8-105">Before you begin, we recommend that you at least skim through this whole topic to get an idea of what the process entails and what this topic contains.</span></span>

> [!NOTE]
> <span data-ttu-id="e95b8-106">Hvis du ikke har fått tilgang til Dynamics 365 Commerce-forhåndsvisningen, kan du be om forhåndsvisningstilgang fra [nettstedet for e-handel](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="e95b8-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="e95b8-107">Oversikt</span><span class="sxs-lookup"><span data-stu-id="e95b8-107">Overview</span></span>

<span data-ttu-id="e95b8-108">For å kunne klargjøre Commerce Preview-miljøet må du opprette et prosjekt som har et bestemt produktnavn og type.</span><span class="sxs-lookup"><span data-stu-id="e95b8-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="e95b8-109">Miljøet og Retail Cloud Scale Unit (RCSU) har også bestemte parametere du må bruke når du skal klargjøre e-handel senere.</span><span class="sxs-lookup"><span data-stu-id="e95b8-109">The environment and Retail Cloud Scale Unit (RCSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="e95b8-110">Instruksjonene i dette emnet beskriver alle nødvendige trinn du må fullføre, og parameterne du må bruke.</span><span class="sxs-lookup"><span data-stu-id="e95b8-110">The instructions in this topic describe all the required steps that you must complete and the parameters that you must use.</span></span>

<span data-ttu-id="e95b8-111">Når klargjøringen av Commerce-forhåndsvisningsmiljøet er fullført, er det noen få trinn du må ta i etterkant for å klargjøre det.</span><span class="sxs-lookup"><span data-stu-id="e95b8-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="e95b8-112">Noen trinn er valgfrie, avhengig av hvilke aspekter av systemet du vil evaluere.</span><span class="sxs-lookup"><span data-stu-id="e95b8-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="e95b8-113">Du kan alltid fullføre de valgfrie trinnene senere.</span><span class="sxs-lookup"><span data-stu-id="e95b8-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="e95b8-114">Hvis du vil ha informasjon om hvordan du konfigurerer Commerce-forhåndsvisningsmiljøet etter klargjøring, kan du se [Konfigurere et Commerce-forhåndsvisningsmiljø](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="e95b8-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="e95b8-115">Hvis du vil ha informasjon om hvordan du konfigurerer valgfrie funksjoner for Commerce-forhåndsvisningsmiljøet, kan du se [Konfigurere valgfrie funksjoner for et Commerce-forhåndsvisningsmiljø](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="e95b8-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="e95b8-116">Hvis du har spørsmål om klargjøringstrinnene eller du får problemer, kan du fortelle Microsoft i [Yammer-gruppen for Microsoft Dynamics 365 Commerce-forhåndsvisningen](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="e95b8-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e95b8-117">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="e95b8-117">Prerequisites</span></span>

<span data-ttu-id="e95b8-118">Følgende forutsetninger må være på plass før du kan klargjøre Commerce-forhåndsvisningsmiljøet:</span><span class="sxs-lookup"><span data-stu-id="e95b8-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="e95b8-119">Du har tilgang til Microsoft Dynamics Lifecycle Services-portalen (LCS).</span><span class="sxs-lookup"><span data-stu-id="e95b8-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="e95b8-120">Du er godtatt i Dynamics 365 Commerce-forhåndsvisningsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="e95b8-120">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="e95b8-121">Du har de nødvendige tillatelsene til å opprette et prosjekt for **Potensielt førsalg** eller **Overfør, opprett løsninger og finn ut mer om**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-121">You have the required permissions to create a project for **Prospective presales** or **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="e95b8-122">Du er medlem av **Miljøadministrator**- eller **Prosjekteier**-rollen i prosjektet der du skal klargjøre miljøet.</span><span class="sxs-lookup"><span data-stu-id="e95b8-122">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="e95b8-123">Du har administratortilgang til Microsoft Azure-abonnementet eller kontakt med en abonnementsadministrator som kan utføre de to trinnene som krever administratortillatelser på dine vegne.</span><span class="sxs-lookup"><span data-stu-id="e95b8-123">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="e95b8-124">Du har Azure Active Directory (Azure AD) tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="e95b8-124">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="e95b8-125">Du har opprettet en Azure AD-sikkerhetsgruppe som skal brukes som systemadministratorgruppe for e-handel, og du har ID-en tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="e95b8-125">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="e95b8-126">Du har opprettet en Azure AD-sikkerhetsgruppe som skal brukes som moderatorgruppe for vurderinger og omtaler, og du har ID-en tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="e95b8-126">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="e95b8-127">(Denne sikkerhetsgruppen kan være den samme som systemadministrasjonsgruppen for e-handel.)</span><span class="sxs-lookup"><span data-stu-id="e95b8-127">(This security group can be the same as the e-Commerce system admin group.)</span></span>

### <a name="find-your-azure-ad-tenant-id"></a><span data-ttu-id="e95b8-128">Finn din Azure AD-leier-ID</span><span class="sxs-lookup"><span data-stu-id="e95b8-128">Find your Azure AD tenant ID</span></span>

<span data-ttu-id="e95b8-129">Azure AD-leier-IDen er en globalt unik identifikator (GUID) som ligner på dette eksemplet: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-129">Your Azure AD tenant ID is a globally unique identifier (GUID) that resembles this example: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a><span data-ttu-id="e95b8-130">Finn din Azure AD-leier-ID ved hjelp av Azure-portalen</span><span class="sxs-lookup"><span data-stu-id="e95b8-130">Find your Azure AD tenant ID by using the Azure portal</span></span>

1. <span data-ttu-id="e95b8-131">Logg på [Azure-portalen](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="e95b8-131">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="e95b8-132">Kontroller at du har valgt riktig katalog.</span><span class="sxs-lookup"><span data-stu-id="e95b8-132">Make sure that the correct directory is selected.</span></span>
1. <span data-ttu-id="e95b8-133">Velg **Azure Active Directory** på menyen til venstre.</span><span class="sxs-lookup"><span data-stu-id="e95b8-133">On the menu on the left, select **Azure Active Directory**.</span></span>
1. <span data-ttu-id="e95b8-134">Velg **Egenskaper** under **Behandle**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-134">Under **Manage**, select **Properties**.</span></span> <span data-ttu-id="e95b8-135">Azure AD-leier-IDen vises under **Katalog-ID**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-135">Your Azure AD tenant ID appears under **Directory ID**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a><span data-ttu-id="e95b8-136">Finn din Azure AD-leier-ID ved å bruke OpenID Connect-metadata</span><span class="sxs-lookup"><span data-stu-id="e95b8-136">Find your Azure AD tenant ID by using OpenID Connect metadata</span></span>

<span data-ttu-id="e95b8-137">Opprett en OpenID-URL ved å erstatte **\{YOUR\_DOMAIN\}** med domenet ditt, for eksempel `microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="e95b8-137">Create an OpenID URL by replacing **\{YOUR\_DOMAIN\}** with your domain, such as `microsoft.com`.</span></span> <span data-ttu-id="e95b8-138">For eksempel vil `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` bli `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span><span class="sxs-lookup"><span data-stu-id="e95b8-138">For example, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` will become `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span></span>

1. <span data-ttu-id="e95b8-139">Gå til OpenID-URLen som inneholder domenet ditt.</span><span class="sxs-lookup"><span data-stu-id="e95b8-139">Go to the OpenID URL that contains your domain.</span></span>

    <span data-ttu-id="e95b8-140">Du kan finne din Azure AD-leier-ID i flere egenskapsverdier.</span><span class="sxs-lookup"><span data-stu-id="e95b8-140">You can find you Azure AD tenant ID in multiple property values.</span></span>

1. <span data-ttu-id="e95b8-141">Søk etter **authorization\_endpoint**, og pakk ut GUID-en som vises umiddelbart etter `login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="e95b8-141">Find **authorization\_endpoint**, and extract the GUID that appears immediately after `login.microsoftonline.com/`.</span></span>

### <a name="find-your-azure-ad-security-group-id"></a><span data-ttu-id="e95b8-142">Finne Azure AD-sikkerhetsgruppe-IDen</span><span class="sxs-lookup"><span data-stu-id="e95b8-142">Find your Azure AD security group ID</span></span>

<span data-ttu-id="e95b8-143">IDen for Azure AD-sikkerhetsgruppen er en GUID som ligner på dette eksemplet: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-143">The ID of your Azure AD security group is a GUID that resembles this example: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span></span>

<span data-ttu-id="e95b8-144">Denne fremgangsmåten forutsetter at du er medlem av gruppen du prøver å finne IDen for.</span><span class="sxs-lookup"><span data-stu-id="e95b8-144">This procedure assumes that you're a member of the group that you're trying to find the ID for.</span></span>

1. <span data-ttu-id="e95b8-145">Åpne [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span><span class="sxs-lookup"><span data-stu-id="e95b8-145">Open the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span></span>
1. <span data-ttu-id="e95b8-146">Klikk **Logg på med Microsoft**, og logg på med legitimasjonen din.</span><span class="sxs-lookup"><span data-stu-id="e95b8-146">Select **Sign In with Microsoft**, and sign in by using your credentials.</span></span>
1. <span data-ttu-id="e95b8-147">Velg **Vis flere eksempler**til venstre.</span><span class="sxs-lookup"><span data-stu-id="e95b8-147">On the left, select **show more samples**.</span></span>
1. <span data-ttu-id="e95b8-148">Aktiver **Grupper** i høyre rute.</span><span class="sxs-lookup"><span data-stu-id="e95b8-148">In the right pane, enable **Groups**.</span></span>
1. <span data-ttu-id="e95b8-149">Lukk høyre rute.</span><span class="sxs-lookup"><span data-stu-id="e95b8-149">Close the right pane.</span></span>
1. <span data-ttu-id="e95b8-150">Klikk **alle grupper jeg tilhører**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-150">Select **all groups I belong to**.</span></span>
1. <span data-ttu-id="e95b8-151">Finn gruppen din i feltet **Forhåndsvis svar**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-151">In the **Response Preview** field, find your group.</span></span> <span data-ttu-id="e95b8-152">Sikkerhetsgruppe-IDen vises under egenskapen **ID**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-152">The security group ID appears under the **id** property.</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="e95b8-153">Klargjøre Commerce-forhåndsvisningsmiljøet</span><span class="sxs-lookup"><span data-stu-id="e95b8-153">Provision your Commerce preview environment</span></span>

<span data-ttu-id="e95b8-154">Disse prosedyrene forklarer hvordan du klargjør et Commerce-forhåndsvisningsmiljø.</span><span class="sxs-lookup"><span data-stu-id="e95b8-154">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="e95b8-155">Når du har fullført dem, vil forhåndsvisningsmiljøet for Commerce være klart for konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="e95b8-155">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="e95b8-156">Alle aktivitetene som beskrives her, skjer i LCS-portalen.</span><span class="sxs-lookup"><span data-stu-id="e95b8-156">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e95b8-157">Forhåndsvisningstilgang er knyttet til LCS-kontoen og organisasjonen du angav i forhåndsvisningsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="e95b8-157">Preview access is tied to the LCS account and organization that you specified in your preview application.</span></span> <span data-ttu-id="e95b8-158">Du må bruke samme konto for å klargjøre Commerce-forhåndsvisningsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="e95b8-158">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="e95b8-159">Hvis du må bruke en annen LCS-konto eller leier for Commerceforhåndsvisningsmiljøet, må du oppgi disse detaljene til Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e95b8-159">If you must use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="e95b8-160">Hvis du vil ha kontaktinformasjon, kan du se delen [Støtte for Commerce-forhåndsvisningsmiljøet](#commerce-preview-environment-support) senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="e95b8-160">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="grant-access-to-e-commerce-applications"></a><span data-ttu-id="e95b8-161">Gi tilgang til e-handelsprogrammer</span><span class="sxs-lookup"><span data-stu-id="e95b8-161">Grant access to e-Commerce applications</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e95b8-162">Personen som logger på, må være en Azure AD-leieradministrator som har Azure AD-leier-IDen.</span><span class="sxs-lookup"><span data-stu-id="e95b8-162">The person who signs in must be an Azure AD tenant admin who has the Azure AD tenant ID.</span></span> <span data-ttu-id="e95b8-163">Hvis dette trinnet ikke er fullført, vil de gjenstående klargjøringstrinnene mislykkes.</span><span class="sxs-lookup"><span data-stu-id="e95b8-163">If this step isn't successfully completed, the remaining provisioning steps will fail.</span></span>

<span data-ttu-id="e95b8-164">Følg denne fremgangsmåten for å autorisere e-handelsprogrammene til å få tilgang til Azure-abonnementet ditt.</span><span class="sxs-lookup"><span data-stu-id="e95b8-164">To authorize e-Commerce applications to access your Azure subscription, follow these steps.</span></span>

1. <span data-ttu-id="e95b8-165">Sett sammen en URL-adresse i følgende format:</span><span class="sxs-lookup"><span data-stu-id="e95b8-165">Assemble a URL in the following format:</span></span>

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. <span data-ttu-id="e95b8-166">Kopier og lim inn URLen i nettleseren eller tekstredigeringsprogrammet, og erstatt **\{AAD\_TENANT\_ID\}** med din Azure AD-leier-ID.</span><span class="sxs-lookup"><span data-stu-id="e95b8-166">Copy and paste the URL into your browser or text editor, and replace **\{AAD\_TENANT\_ID\}** with your Azure AD tenant ID.</span></span> <span data-ttu-id="e95b8-167">Åpne deretter URLen.</span><span class="sxs-lookup"><span data-stu-id="e95b8-167">Then open the URL.</span></span>
1. <span data-ttu-id="e95b8-168">I dialogboksen for pålogging til Azure AD logger du deg på og bekrefter at du vil gi **Dynamics 365 Commerce (forhåndsvisning)** tilgang til abonnementet.</span><span class="sxs-lookup"><span data-stu-id="e95b8-168">In the Azure AD sign-in dialog box, sign in, and confirm that you want to grant **Dynamics 365 Commerce (Preview)** access to your subscription.</span></span> <span data-ttu-id="e95b8-169">Du blir sendt til en side som angir om operasjonen var vellykket.</span><span class="sxs-lookup"><span data-stu-id="e95b8-169">You're redirected to a page that indicates whether the operation was successful.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="e95b8-170">Kontroller at forhåndsvisningsfunksjonene er tilgjengelige og aktivert i LCS</span><span class="sxs-lookup"><span data-stu-id="e95b8-170">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="e95b8-171">Gjør følgende for å kontrollere at forhåndsvisningsfunksjonene er tilgjengelige og aktivert i LCS.</span><span class="sxs-lookup"><span data-stu-id="e95b8-171">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="e95b8-172">Logg på [LCS-portalen](https://lcs.dynamics.com) ved hjelp av samme LCS-konto du brukte til å be om tilgang til forhåndsvisningen.</span><span class="sxs-lookup"><span data-stu-id="e95b8-172">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="e95b8-173">På LCS-startsiden ruller du helt til høyre og klikker på flisen **Administrasjon av forhåndsvisningsfunksjoner**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-173">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Fanen Forhåndsversjonsstyring](./media/preview1.png)

1. <span data-ttu-id="e95b8-175">Bla ned til **Private forhåndsvisningsfunksjoner**, og kontroller at følgende funksjoner er tilgjengelige og aktivert:</span><span class="sxs-lookup"><span data-stu-id="e95b8-175">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="e95b8-176">E-handelsevaluering</span><span class="sxs-lookup"><span data-stu-id="e95b8-176">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="e95b8-177">Programmiljøer for Commerce-forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="e95b8-177">Commerce Preview Program Environments</span></span>

    ![Private forhåndsvisningsfunksjoner](./media/preview2.png)

1. <span data-ttu-id="e95b8-179">Hvis disse funksjonene ikke vises i listen, kontakter du Microsoft og angir e-postadresse for arbeid, LCS-konto og leierinformasjon.</span><span class="sxs-lookup"><span data-stu-id="e95b8-179">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="e95b8-180">Hvis du vil ha kontaktinformasjon, kan du se delen [Støtte for Commerce-forhåndsvisningsmiljøet](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="e95b8-180">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="e95b8-181">Opprett nytt prosjekt</span><span class="sxs-lookup"><span data-stu-id="e95b8-181">Create a new project</span></span>

<span data-ttu-id="e95b8-182">Hvis du vil opprette et nytt prosjekt i LCS, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="e95b8-182">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="e95b8-183">På LCS-startsiden velger du plusstegnet (**+**) for å opprette et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="e95b8-183">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="e95b8-184">I den høyre ruten følger du ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="e95b8-184">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="e95b8-185">Hvis du er en partner, velger du **Overfør, opprett løsninger og finn ut mer om**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-185">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="e95b8-186">Hvis du er kunde, velger du **Potensielt førsalg**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-186">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="e95b8-187">Angi navn, beskrivelse og bransje.</span><span class="sxs-lookup"><span data-stu-id="e95b8-187">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="e95b8-188">I **Produktnavn**-feltet velger du **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-188">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="e95b8-189">I **Produktversjon**-feltet velger du **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-189">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="e95b8-190">I **Metodologi**-feltet velger du **Implementeringsmetodologi for Dynamics Retail**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-190">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="e95b8-191">Valgfritt: Du kan importere roller og brukere fra et eksisterende prosjekt.</span><span class="sxs-lookup"><span data-stu-id="e95b8-191">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="e95b8-192">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-192">Select **Create**.</span></span> <span data-ttu-id="e95b8-193">Prosjektvisningen vises.</span><span class="sxs-lookup"><span data-stu-id="e95b8-193">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="e95b8-194">Legge til Azure-koblingen</span><span class="sxs-lookup"><span data-stu-id="e95b8-194">Add the Azure Connector</span></span>

<span data-ttu-id="e95b8-195">Hvis du vil legge til Azure-koblingen i LCS-prosjektet, følger du fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="e95b8-195">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="e95b8-196">Følg ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="e95b8-196">Follow one of these steps:</span></span>

    - <span data-ttu-id="e95b8-197">Hvis du er en partner, velger du **Prosjektinnstillinger**-flisen helt til høyre.</span><span class="sxs-lookup"><span data-stu-id="e95b8-197">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="e95b8-198">Hvis du er en kunde, velger du **Prosjektinnstillinger** fra den øverste menyen.</span><span class="sxs-lookup"><span data-stu-id="e95b8-198">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="e95b8-199">Velg **Azure-koblinger**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-199">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="e95b8-200">Klikk **Legg til** for å legge til Azure-koblingen.</span><span class="sxs-lookup"><span data-stu-id="e95b8-200">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="e95b8-201">Skriv inn et navn.</span><span class="sxs-lookup"><span data-stu-id="e95b8-201">Enter a name.</span></span>
1. <span data-ttu-id="e95b8-202">Angi ID for Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="e95b8-202">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="e95b8-203">Aktiver alternativet **Konfigurer til å bruke ARM (Azure Resource Manager)**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-203">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="e95b8-204">Kontroller at verdien for **AAD-leierdomene (eller ID) for Azure-abonnement** er riktig.</span><span class="sxs-lookup"><span data-stu-id="e95b8-204">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="e95b8-205">Kontakt om nødvendig Azure-abonnementsadministratoren.</span><span class="sxs-lookup"><span data-stu-id="e95b8-205">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="e95b8-206">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-206">Select **Next**.</span></span>
1. <span data-ttu-id="e95b8-207">Følg instruksjonene på siden for å gi de nødvendige programmene tilgang til abonnementet.</span><span class="sxs-lookup"><span data-stu-id="e95b8-207">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="e95b8-208">Kontakt om nødvendig Azure-abonnementsadministratoren.</span><span class="sxs-lookup"><span data-stu-id="e95b8-208">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="e95b8-209">Logg på [Azure-portalen](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="e95b8-209">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="e95b8-210">Kontroller at riktig katalog er valgt, og velg deretter **Abonnementer** på menyen til venstre.</span><span class="sxs-lookup"><span data-stu-id="e95b8-210">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="e95b8-211">Finn det riktige abonnementet fra listen, og velg det.</span><span class="sxs-lookup"><span data-stu-id="e95b8-211">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="e95b8-212">Bruk søkefunksjonaliteten etter behov.</span><span class="sxs-lookup"><span data-stu-id="e95b8-212">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="e95b8-213">Velg **Tilgangskontroll (IAM)** på menyen.</span><span class="sxs-lookup"><span data-stu-id="e95b8-213">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="e95b8-214">Klikk **Legg til** under **Legg til rolletilordning** på høyre side.</span><span class="sxs-lookup"><span data-stu-id="e95b8-214">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="e95b8-215">**Legg til rolletilordning**-ruten åpnes.</span><span class="sxs-lookup"><span data-stu-id="e95b8-215">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="e95b8-216">I **Rolle**-feltet velger du **Bidragsyter**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-216">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="e95b8-217">I feltet **Tilordne tilgang til** beholder du standardverdien, **Azure AD-bruker, -gruppe eller -tjenestekontohaver.**</span><span class="sxs-lookup"><span data-stu-id="e95b8-217">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="e95b8-218">Under **Velg** angir du **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-218">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="e95b8-219">Velg **Dynamics-distribusjonstjenester \[wsfed-aktivert\]** fra listen.</span><span class="sxs-lookup"><span data-stu-id="e95b8-219">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="e95b8-220">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-220">Select **Save**.</span></span>

1. <span data-ttu-id="e95b8-221">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-221">Select **Next**.</span></span>
1. <span data-ttu-id="e95b8-222">Følg instruksjonene på siden for å gi de nødvendige programmene tilgang til abonnementet.</span><span class="sxs-lookup"><span data-stu-id="e95b8-222">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="e95b8-223">Kontakt om nødvendig Azure-abonnementsadministratoren.</span><span class="sxs-lookup"><span data-stu-id="e95b8-223">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="e95b8-224">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-224">Select **Next**.</span></span>
1. <span data-ttu-id="e95b8-225">I **Azure-område**-feltet velger du **USA øst**, **USA øst 2**, **USA vest** eller **USA vest 2**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-225">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="e95b8-226">Velg **Koble til**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-226">Select **Connect**.</span></span> <span data-ttu-id="e95b8-227">Din Azure-kobling skal vises i listen.</span><span class="sxs-lookup"><span data-stu-id="e95b8-227">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="e95b8-228">Importere miljøer for e-handelsforhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="e95b8-228">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="e95b8-229">Følg denne fremgangsmåten for å importere miljøer for e-handelsforhåndsvisning til prosjektet ditt.</span><span class="sxs-lookup"><span data-stu-id="e95b8-229">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="e95b8-230">Åpne startsiden for prosjektet ved å velge prosjektnavnet øverst.</span><span class="sxs-lookup"><span data-stu-id="e95b8-230">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="e95b8-231">Følg ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="e95b8-231">Follow one of these steps:</span></span>

    - <span data-ttu-id="e95b8-232">Hvis du er en partner, velger du **Aktivabibliotek**-flisen helt til høyre.</span><span class="sxs-lookup"><span data-stu-id="e95b8-232">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="e95b8-233">Hvis du er en kunde, velger du **Aktivabibliotek** fra den øverste menyen.</span><span class="sxs-lookup"><span data-stu-id="e95b8-233">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="e95b8-234">Velg **Distribuerbar programvarepakke** fra listen til venstre.</span><span class="sxs-lookup"><span data-stu-id="e95b8-234">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="e95b8-235">Velg **Import**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-235">Select **Import**.</span></span>
1. <span data-ttu-id="e95b8-236">Velg **Miljøer for e-handelsforhåndsvisning** fra listen over aktiva under **Delt aktivabibliotek**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-236">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="e95b8-237">Velg **Plukk**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-237">Select **Pick**.</span></span> <span data-ttu-id="e95b8-238">Du kommer tilbake til aktivabiblioteket, og du skal se utvidelsen i listen.</span><span class="sxs-lookup"><span data-stu-id="e95b8-238">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="e95b8-239">Illustrasjonen nedenfor viser handlingene som må utføres på LCS-siden **Aktivabibliotek**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-239">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![Importere miljøer for e-handelsforhåndsvisning](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="e95b8-241">Distribuere miljøet</span><span class="sxs-lookup"><span data-stu-id="e95b8-241">Deploy the environment</span></span>

<span data-ttu-id="e95b8-242">Gjør følgende for å distribuere miljøet.</span><span class="sxs-lookup"><span data-stu-id="e95b8-242">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="e95b8-243">Det kan hende du ikke trenger å fullføre trinn 6, 7 og/eller 8 fordi sider som har et enkelt alternativ, hoppes over.</span><span class="sxs-lookup"><span data-stu-id="e95b8-243">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="e95b8-244">Når du er i **Miljøparametere**-visningen, bekrefter du at teksten **Dynamics 365 Commerce (forhåndsvisning) - demo (10.0.6 med Platform update 30)** vises rett over **Miljønavn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e95b8-244">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce (Preview) - Demo (10.0.6 with Platform update 30)** appears directly above the **Environment name** field.</span></span> <span data-ttu-id="e95b8-245">Se illustrasjonen som vises etter trinn 8.</span><span class="sxs-lookup"><span data-stu-id="e95b8-245">See the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="e95b8-246">Fra den øverste menyen velger du **Skybaserte miljøer**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-246">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="e95b8-247">Klikk **Legg til** for å legge til et miljø.</span><span class="sxs-lookup"><span data-stu-id="e95b8-247">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="e95b8-248">I **Produktversjon**-feltet velger du **10.0.6**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-248">In the **Application version** field, select **10.0.6**.</span></span>
1. <span data-ttu-id="e95b8-249">Velg **Platform update 30** for **Plattformversjon**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-249">In the **Platform version** field, select **Platform Update 30**.</span></span>

    ![Velge program- og plattformversjoner](./media/project1.png)

1. <span data-ttu-id="e95b8-251">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-251">Select **Next**.</span></span>
1. <span data-ttu-id="e95b8-252">Velg **Demo** som miljøtopologien.</span><span class="sxs-lookup"><span data-stu-id="e95b8-252">Select **Demo** as the environment topology.</span></span>

    ![Velge miljøtopologien 1](./media/project2.png)

1. <span data-ttu-id="e95b8-254">Velg **Dynamics 365 Commerce (forhåndsvisning) - demo** som miljøtopologien.</span><span class="sxs-lookup"><span data-stu-id="e95b8-254">Select **Dynamics 365 Commerce (Preview) - Demo** as the environment topology.</span></span> <span data-ttu-id="e95b8-255">Hvis du konfigurerte en enkelt Azure-kobling tidligere, vil den bli brukt for dette miljøet.</span><span class="sxs-lookup"><span data-stu-id="e95b8-255">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="e95b8-256">Hvis du konfigurerte flere Azure-koblinger, kan du velge hvilken kontakt som skal brukes: **USA øst**, **USA øst 2**, **USA vest** eller **USA vest 2**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-256">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="e95b8-257">(For den beste ende-til-ende-ytelsen anbefaler vi at du velger **USA vest 2**.)</span><span class="sxs-lookup"><span data-stu-id="e95b8-257">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![Velge miljøtopologien 2](./media/project3.png)

1. <span data-ttu-id="e95b8-259">På **Distribusjonsmiljø**-siden angir du et miljønavn.</span><span class="sxs-lookup"><span data-stu-id="e95b8-259">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="e95b8-260">La Avanserte innstillinger stå som de er.</span><span class="sxs-lookup"><span data-stu-id="e95b8-260">Leave the advanced settings as they are.</span></span>

    ![Distribusjonsmiljø-siden](./media/project4.png)

1. <span data-ttu-id="e95b8-262">Juster VM-størrelsen etter behov.</span><span class="sxs-lookup"><span data-stu-id="e95b8-262">Adjust the VM size as required.</span></span> <span data-ttu-id="e95b8-263">(Vi anbefaler VM-lagerenhet \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="e95b8-263">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="e95b8-264">Se gjennom vilkårene for prising og lisensiering, og merk deretter av i avmerkingsboksen for å angi at du godtar dem.</span><span class="sxs-lookup"><span data-stu-id="e95b8-264">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="e95b8-265">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-265">Select **Next**.</span></span>
1. <span data-ttu-id="e95b8-266">Klikk **Distribuer**på bekreftelsessiden for distribusjon når du har bekreftet at detaljene er riktige.</span><span class="sxs-lookup"><span data-stu-id="e95b8-266">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="e95b8-267">Du kommer tilbake til visningen **Skybaserte miljøer**, og miljøet skal vises i listen.</span><span class="sxs-lookup"><span data-stu-id="e95b8-267">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="e95b8-268">Det forespurte miljøet vil vises som en kø og deretter distribueres.</span><span class="sxs-lookup"><span data-stu-id="e95b8-268">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="e95b8-269">Miljøarbeidsflytene vil ta litt tid å fullføre.</span><span class="sxs-lookup"><span data-stu-id="e95b8-269">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="e95b8-270">Kom derfor tilbake etter ca seks til ni timer.</span><span class="sxs-lookup"><span data-stu-id="e95b8-270">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="e95b8-271">Før du fortsetter må du kontrollere at miljøstatusen er **Distribuert**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-271">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-rcsu"></a><span data-ttu-id="e95b8-272">Initialiser RCSU</span><span class="sxs-lookup"><span data-stu-id="e95b8-272">Initialize RCSU</span></span>

<span data-ttu-id="e95b8-273">Hvis du vil initialisere en RCSU-adresse, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="e95b8-273">To initialize RCSU, follow these steps.</span></span>

1. <span data-ttu-id="e95b8-274">Velg miljøet ditt fra listen i visningen **Skybaserte miljøer**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-274">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="e95b8-275">Klikk **Detaljerte opplysninger** i miljøvisningen til høyre.</span><span class="sxs-lookup"><span data-stu-id="e95b8-275">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="e95b8-276">Detaljerte opplysninger for miljø vises.</span><span class="sxs-lookup"><span data-stu-id="e95b8-276">The environment details view appears.</span></span>
1. <span data-ttu-id="e95b8-277">Klikk **Behandle** under **Miljøfunksjoner**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-277">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="e95b8-278">Velg **Initialiser** i kategorien **Detaljhandel**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-278">On the **Retail** tab, select **Initialize**.</span></span> <span data-ttu-id="e95b8-279">Visningen av parametere for RCSU-initialisering vises.</span><span class="sxs-lookup"><span data-stu-id="e95b8-279">The RCSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="e95b8-280">I **Område**-feltet velger du **USA øst**, **USA øst 2**, **USA vest** eller **USA vest 2**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-280">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="e95b8-281">I **Versjon**-feltet velger du **Angi en versjon** i listen, og deretter angir du **9.16.19262.5** i feltet som vises.</span><span class="sxs-lookup"><span data-stu-id="e95b8-281">In the **Version** field, select **Specify a version** in the list, and then specify **9.16.19262.5** in the field that appears.</span></span> <span data-ttu-id="e95b8-282">Pass på at du angir nøyaktig hvilken versjon som er angitt her.</span><span class="sxs-lookup"><span data-stu-id="e95b8-282">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="e95b8-283">Ellers må du oppdatere RCSU til korrekt versjon senere.</span><span class="sxs-lookup"><span data-stu-id="e95b8-283">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="e95b8-284">Aktiver alternativet **Bruk utvidelse**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-284">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="e95b8-285">Velg **Miljøer for e-handelsforhåndsvisning** fra listen over utvidelser.</span><span class="sxs-lookup"><span data-stu-id="e95b8-285">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="e95b8-286">Velg **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-286">Select **Initialize**.</span></span>
1. <span data-ttu-id="e95b8-287">Klikk **Ja**på bekreftelsessiden for distribusjon når du har bekreftet at detaljene er riktige.</span><span class="sxs-lookup"><span data-stu-id="e95b8-287">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="e95b8-288">Du returneres til visningen **Detaljhandelsstyring**, der kategorien **Detaljhandel** er valgt.</span><span class="sxs-lookup"><span data-stu-id="e95b8-288">You're returned to the **Retail management** view, where the **Retail** tab is selected.</span></span> <span data-ttu-id="e95b8-289">RCSU-en din er lagt i kø for klargjøring.</span><span class="sxs-lookup"><span data-stu-id="e95b8-289">Your RCSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="e95b8-290">Før du fortsetter må du kontrollere at miljøstatusen til RCSU er **Vellykket**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-290">Before you continue, make sure that the status of your RCSU is **Success**.</span></span> <span data-ttu-id="e95b8-291">Initialiseringen tar omtrent to til fem timer.</span><span class="sxs-lookup"><span data-stu-id="e95b8-291">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="e95b8-292">Initialisere e-handel</span><span class="sxs-lookup"><span data-stu-id="e95b8-292">Initialize e-Commerce</span></span>

<span data-ttu-id="e95b8-293">Hvis du vil initialisere e-handel, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="e95b8-293">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="e95b8-294">I kategorien **E-handel (forhåndsvisning)** ser du gjennom samtykket for forhåndsvisning, og velger deretter **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-294">On the **e-Commerce (Preview)** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="e95b8-295">Angi et navn i feltet **Navn på e-handelsleier**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-295">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="e95b8-296">Vær imidlertid oppmerksom på at dette navnet vil vises i noen av URL-adressene som peker til e-handelsforekomsten.</span><span class="sxs-lookup"><span data-stu-id="e95b8-296">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="e95b8-297">I feltet **Retail Cloud Scale Unit-navn** velger du RCSU-en i listen.</span><span class="sxs-lookup"><span data-stu-id="e95b8-297">In the **Retail cloud scale unit name** field, select your RCSU in the list.</span></span> <span data-ttu-id="e95b8-298">(Listen bør bare ha ett alternativ.)</span><span class="sxs-lookup"><span data-stu-id="e95b8-298">(The list should have only one option.)</span></span>

    <span data-ttu-id="e95b8-299">Feltet **Geografi for e-handel** angis automatisk, og verdien kan ikke endres.</span><span class="sxs-lookup"><span data-stu-id="e95b8-299">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="e95b8-300">Klikk **Neste** for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="e95b8-300">Select **Next** to continue.</span></span>
1. <span data-ttu-id="e95b8-301">I feltet **Støttede vertsnavn** angir du et gyldig domene, for eksempel `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="e95b8-301">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="e95b8-302">I feltet **AAD sikkerhetsgruppe for systemadministrasjon** angir du de første bokstavene i navnet på sikkerhetsgruppen du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="e95b8-302">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="e95b8-303">Velg forstørrelsesglass-ikonet for å vise søkeresultatene.</span><span class="sxs-lookup"><span data-stu-id="e95b8-303">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="e95b8-304">Velg en sikkerhetsgruppe fra listen.</span><span class="sxs-lookup"><span data-stu-id="e95b8-304">Select a security group from the list.</span></span>
2.  <span data-ttu-id="e95b8-305">I feltet **Moderator for AAD-sikkerhetsgruppe for vurderinger og omtaler** angir du de første bokstavene i navnet på sikkerhetsgruppen du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="e95b8-305">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="e95b8-306">Velg forstørrelsesglass-ikonet for å vise søkeresultatene.</span><span class="sxs-lookup"><span data-stu-id="e95b8-306">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="e95b8-307">Velg en sikkerhetsgruppe fra listen.</span><span class="sxs-lookup"><span data-stu-id="e95b8-307">Select a security group from the list.</span></span>
1. <span data-ttu-id="e95b8-308">La alternativet **Aktiver tjenesten for vurderinger og omtale** være aktivert.</span><span class="sxs-lookup"><span data-stu-id="e95b8-308">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="e95b8-309">Hvis du allerede har fullført trinnet Microsoft Azure Active Directory (Azure AD)-samtykke, som beskrevet i delen "Gi tilgang til e-handelsprogrammer", merker du av i avmerkingsboksen for å bekrefte ditt samtykke.</span><span class="sxs-lookup"><span data-stu-id="e95b8-309">If you have already completed the Microsoft Azure Active Directory (Azure AD) consent step as described in the "Grant access to e-Commerce applications" section, select the check box to confirm your consent.</span></span> <span data-ttu-id="e95b8-310">Hvis du ennå ikke har fullført dette trinnet, må du gjøre det før du fortsetter med initialiseringen.</span><span class="sxs-lookup"><span data-stu-id="e95b8-310">If you have not yet completed this step, you need to do that before proceeding with the initialization.</span></span> <span data-ttu-id="e95b8-311">Merk koblingen i teksten ved siden av avmerkingsboksen for å åpne dialogboksen for samtykke, og fullfør trinnet.</span><span class="sxs-lookup"><span data-stu-id="e95b8-311">Select the link within the text next to the check box to open the consent dialog box and complete the step.</span></span>
1. <span data-ttu-id="e95b8-312">Velg **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-312">Select **Initialize**.</span></span> <span data-ttu-id="e95b8-313">Du returneres til visningen **Detaljhandelsstyring**, der kategorien **E-handel (forhåndsvisning)** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="e95b8-313">You're returned to the **Retail management** view, where the **e-Commerce (Preview)** tab is selected.</span></span> <span data-ttu-id="e95b8-314">Initialiseringen av e-handel har startet.</span><span class="sxs-lookup"><span data-stu-id="e95b8-314">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="e95b8-315">Før du fortsetter må du vente til initialiseringsstatusen for e-handel er **Initialisering vellykket**.</span><span class="sxs-lookup"><span data-stu-id="e95b8-315">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="e95b8-316">Under **Koblinger** ned til høyre noterer du URL-adressene for følgende koblinger:</span><span class="sxs-lookup"><span data-stu-id="e95b8-316">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="e95b8-317">**E-handelsområde** – koblingen til roten for e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="e95b8-317">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="e95b8-318">**Verktøy for administrasjon av e-handel-området** – koblingen til verktøyet for områdeadministrasjon.</span><span class="sxs-lookup"><span data-stu-id="e95b8-318">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="e95b8-319">Støtte for Commerce-forhåndsvisningsmiljø</span><span class="sxs-lookup"><span data-stu-id="e95b8-319">Commerce preview environment support</span></span>

<span data-ttu-id="e95b8-320">Hvis det oppstår problemer under utføring av klargjøringstrinnene, kan du gå til [Yammer-gruppen for Microsoft Dynamics 365 Commerce forhåndsvisning](https://aka.ms/Dynamics365CommercePreviewYammer) for å få hjelp.</span><span class="sxs-lookup"><span data-stu-id="e95b8-320">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="e95b8-321">Hvis du får problemer når du prøver å få tilgang til Yammer-gruppen, kan du kontakte Microsoft via e-post på <Dynamics365Commerce@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="e95b8-321">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="e95b8-322">Denne e-postadressen overvåkes ikke aktivt.</span><span class="sxs-lookup"><span data-stu-id="e95b8-322">This email address isn't actively monitored.</span></span> <span data-ttu-id="e95b8-323">Forvent derfor en forsinkelse i svaret.</span><span class="sxs-lookup"><span data-stu-id="e95b8-323">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e95b8-324">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="e95b8-324">Next steps</span></span>

<span data-ttu-id="e95b8-325">Hvis du vil fortsette prosessen for å klargjøre og konfigurere Commerce-forhåndsvisningsmiljøet, kan du se [Konfigurere et Commerce-forhåndsvisningsmiljø](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="e95b8-325">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e95b8-326">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e95b8-326">Additional resources</span></span>

[<span data-ttu-id="e95b8-327">Oversikt over Commerce-forhåndsvisningsmiljø</span><span class="sxs-lookup"><span data-stu-id="e95b8-327">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="e95b8-328">Konfigurere et Commerce-forhåndsvisningsmiljø</span><span class="sxs-lookup"><span data-stu-id="e95b8-328">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="e95b8-329">Konfigurere valgfrie funksjoner for et Commerce-forhåndsvisningsmiljø</span><span class="sxs-lookup"><span data-stu-id="e95b8-329">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="e95b8-330">Vanlige spørsmål for Commerce-forhåndsvisningsmiljø</span><span class="sxs-lookup"><span data-stu-id="e95b8-330">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="e95b8-331">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="e95b8-331">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="e95b8-332">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="e95b8-332">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="e95b8-333">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="e95b8-333">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="e95b8-334">Dynamics 365 Commerce-webområde</span><span class="sxs-lookup"><span data-stu-id="e95b8-334">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="e95b8-335">Hjelperessurser for Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="e95b8-335">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
