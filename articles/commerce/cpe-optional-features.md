---
title: Konfigurere valgfrie funksjoner for et miljø for forhåndsvisning av Dynamics 365 Commerce
description: Dette emnet forklarer hvordan du konfigurerer valgfrie funksjoner for et Microsoft Dynamics 365 Commerce-forhåndsvisningsmiljø.
author: psimolin
manager: annbe
ms.date: 12/10/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 43b23b9ef881b2ab2f3d005d4ba761848a7fa4ed
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024735"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="abec7-103">Konfigurere valgfrie funksjoner for et miljø for forhåndsvisning av Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="abec7-103">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="abec7-104">Dette emnet forklarer hvordan du konfigurerer valgfrie funksjoner for et Microsoft Dynamics 365 Commerce-forhåndsvisningsmiljø.</span><span class="sxs-lookup"><span data-stu-id="abec7-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="abec7-105">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="abec7-105">Prerequisites</span></span>

<span data-ttu-id="abec7-106">Hvis du vil evaluere de transaksjonelle e-postfunksjonene, må følgende forutsetninger oppfylles:</span><span class="sxs-lookup"><span data-stu-id="abec7-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="abec7-107">Du har en e-postserver tilgjengelig (\[SMTP\]-server), som kan brukes fra Microsoft Azure-abonnementet der du klargjorde forhåndsvisningsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="abec7-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the preview environment.</span></span>
- <span data-ttu-id="abec7-108">Du har serverens fullstendig kvaliserte domenenavn (FQDN)/IP-adresse, SMTP-portnummer og godkjenningsinformasjon tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="abec7-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="abec7-109">Hvis du vil evaluere funksjoner for digital aktivastyring ved inntak av nye omnikanalbilder, må du ha navnet på leierenaktiva for innholdsstyringssystemet (CMS) tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="abec7-109">If you want to evaluate Digital Asset Management features by ingesting new omni-channel images, you must have the name of your content management system (CMS) tenant available.</span></span> <span data-ttu-id="abec7-110">Du finner instruksjoner for å finne dette navnet senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="abec7-110">Instructions for finding this name are provided later in this topic.</span></span> <span data-ttu-id="abec7-111">> > > (Sp: hvor er instruksjonene?)</span><span class="sxs-lookup"><span data-stu-id="abec7-111">>>>(Q: where are the instructions?)</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="abec7-112">Konfigurere bildeserveren</span><span class="sxs-lookup"><span data-stu-id="abec7-112">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="abec7-113">Finne primær URL-adresse for media</span><span class="sxs-lookup"><span data-stu-id="abec7-113">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="abec7-114">Før du kan fullføre denne prosedyren, må du fullføre trinnene i [Konfigurere området i handel](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span><span class="sxs-lookup"><span data-stu-id="abec7-114">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="abec7-115">Logg på verktøyet for administrasjon av e-handel-området ved hjelp av URL-adressen du noterte da du startet e-handel under klargjøring (se [Initialisere e-handel](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="abec7-115">Sign in to the Commerce site management tool by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="abec7-116">Åpne **Fabrikam**-området.</span><span class="sxs-lookup"><span data-stu-id="abec7-116">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="abec7-117">Velg **Aktiva** på menyen til venstre.</span><span class="sxs-lookup"><span data-stu-id="abec7-117">On the menu on the left, select **Assets**.</span></span>
1. <span data-ttu-id="abec7-118">Velg et hvilket som helst enkeltbilde.</span><span class="sxs-lookup"><span data-stu-id="abec7-118">Select any single image asset.</span></span>
1. <span data-ttu-id="abec7-119">I egenskapsinspektøren til høyre finner du egenskapen **Offentlig URL**.</span><span class="sxs-lookup"><span data-stu-id="abec7-119">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="abec7-120">Verdien er en URL.</span><span class="sxs-lookup"><span data-stu-id="abec7-120">The value is a URL.</span></span> <span data-ttu-id="abec7-121">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="abec7-121">Here is an example:</span></span>

    <span data-ttu-id="abec7-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="abec7-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="abec7-123">Erstatt den siste identifikatoren i URL-adressen (**MA1nQC** i forrige eksempel) med strengen **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="abec7-123">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="abec7-124">Slik ser eksempel-URL-en ut etter at denne endringen er gjort:</span><span class="sxs-lookup"><span data-stu-id="abec7-124">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="abec7-125">Denne URL-adressen er primær URL-adresse for media.</span><span class="sxs-lookup"><span data-stu-id="abec7-125">This URL is your media base URL.</span></span> <span data-ttu-id="abec7-126">Noter den.</span><span class="sxs-lookup"><span data-stu-id="abec7-126">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="abec7-127">Oppdatere primær URL-adresse for media</span><span class="sxs-lookup"><span data-stu-id="abec7-127">Update the media base URL</span></span>

1. <span data-ttu-id="abec7-128">Logg på Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="abec7-128">Sign in to Dynamics 365 Retail.</span></span>
1. <span data-ttu-id="abec7-129">Bruk menyen til venstre og gå til **Moduler \> Detaljhandel \> Kanaloppsett \> Kanalprofiler**.</span><span class="sxs-lookup"><span data-stu-id="abec7-129">Use the menu on the left to go to **Modules \> Retail \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="abec7-130">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="abec7-130">Select **Edit**.</span></span>
1. <span data-ttu-id="abec7-131">Fra **Profilegenskaper** erstatter du egenskapsverdien for **Primær URL-adresse for medieserver** med den primære URL-adressen for media du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="abec7-131">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="abec7-132">Velg den andre kanalen fra listen til venstre, under **Standard**-kanal.</span><span class="sxs-lookup"><span data-stu-id="abec7-132">In the list on the left, under the **Default** channel, select the other channel.</span></span>
1. <span data-ttu-id="abec7-133">Klikk **Legg til** under **Profilegenskaper**.</span><span class="sxs-lookup"><span data-stu-id="abec7-133">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="abec7-134">For egenskapen som ble lagt til, velger du **Primær URL-adresse for medieserver** som egenskapsnøkkel.</span><span class="sxs-lookup"><span data-stu-id="abec7-134">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="abec7-135">Som egenskapsverdi angir du primær URL-adresse for media som du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="abec7-135">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="abec7-136">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="abec7-136">Select **Save**.</span></span>

## <a name="configure-the-email-server"></a><span data-ttu-id="abec7-137">Konfigurere e-postserveren</span><span class="sxs-lookup"><span data-stu-id="abec7-137">Configure the email server</span></span>

> [!NOTE]
> <span data-ttu-id="abec7-138">SMTP-serveren eller e-posttjenesten du angir her, må være tilgjengelig fra Azure-abonnementet du bruker for miljøet.</span><span class="sxs-lookup"><span data-stu-id="abec7-138">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="abec7-139">Logg på Retail.</span><span class="sxs-lookup"><span data-stu-id="abec7-139">Sign in to Retail.</span></span>
1. <span data-ttu-id="abec7-140">Bruk menyen til venstre, og gå til **Moduler \> Systemadministrasjon \> Oppsett \> E-post \> E-postparametere**.</span><span class="sxs-lookup"><span data-stu-id="abec7-140">Use the menu on the left to go to **Modules \> System administration \> Setup \> Email \> Email parameters**.</span></span>
1. <span data-ttu-id="abec7-141">I kategorien **SMTP-innstillinger** i feltet **Server for utgående e-post** angir du FQDN eller IP-adressen til SMTP-serveren eller e-posttjenesten.</span><span class="sxs-lookup"><span data-stu-id="abec7-141">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="abec7-142">I feltet **SMTP-portnummer** angir du portnummeret.</span><span class="sxs-lookup"><span data-stu-id="abec7-142">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="abec7-143">(Hvis du ikke bruker Secure Sockets Layer \[SSL\], er standard portnummer **25**.)</span><span class="sxs-lookup"><span data-stu-id="abec7-143">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="abec7-144">Hvis godkjenning kreves, angir du verdier i feltene **Brukernavn** og **Passord**.</span><span class="sxs-lookup"><span data-stu-id="abec7-144">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="abec7-145">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="abec7-145">Select **Save**.</span></span>
1. <span data-ttu-id="abec7-146">Velg **Oppdater**.</span><span class="sxs-lookup"><span data-stu-id="abec7-146">Select **Refresh**.</span></span>
1. <span data-ttu-id="abec7-147">Velg **SMTP** i **E-postleverandør**-feltet i kategorien **Test e-post**.</span><span class="sxs-lookup"><span data-stu-id="abec7-147">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="abec7-148">I feltet **Send til** angir du e-postadressen der du vil at test-e-posten skal leveres.</span><span class="sxs-lookup"><span data-stu-id="abec7-148">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="abec7-149">Velg **Send e-posttest**.</span><span class="sxs-lookup"><span data-stu-id="abec7-149">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="abec7-150">Konfigurere e-postmaler</span><span class="sxs-lookup"><span data-stu-id="abec7-150">Configure email templates</span></span>

<span data-ttu-id="abec7-151">E-postmalen for hver transaksjonshendelse du vil sende e-postmeldinger for, må oppdateres med en gyldig e-postadresse for avsender.</span><span class="sxs-lookup"><span data-stu-id="abec7-151">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="abec7-152">Logg på Retail.</span><span class="sxs-lookup"><span data-stu-id="abec7-152">Sign in to Retail.</span></span>
1. <span data-ttu-id="abec7-153">Bruk menyen til venstre, og gå til **Moduler \> Organisasjonsstyring \> Oppsett \> Maler for e-post til organisasjon**.</span><span class="sxs-lookup"><span data-stu-id="abec7-153">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="abec7-154">Velg **Vis liste**.</span><span class="sxs-lookup"><span data-stu-id="abec7-154">Select **Show list**.</span></span>
1. <span data-ttu-id="abec7-155">Følg disse trinnene for hver mal i listen:</span><span class="sxs-lookup"><span data-stu-id="abec7-155">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="abec7-156">Angi senderens e-postadresse i feltet **Avsenders e-postadresse**.</span><span class="sxs-lookup"><span data-stu-id="abec7-156">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="abec7-157">Valgfritt: I feltet **Sendernavn** angir du navnet som skal brukes som sendernavn.</span><span class="sxs-lookup"><span data-stu-id="abec7-157">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="abec7-158">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="abec7-158">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="abec7-159">Tilpasse e-postmaler</span><span class="sxs-lookup"><span data-stu-id="abec7-159">Customize email templates</span></span>

<span data-ttu-id="abec7-160">Det kan være lurt å tilpasse e-postmalene slik at de bruker forskjellige bilder.</span><span class="sxs-lookup"><span data-stu-id="abec7-160">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="abec7-161">Eller kanskje du vil oppdatere koblingene i malene slik at de går til forhåndsvisningsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="abec7-161">Or you might want to update the links in the templates so that they go to your preview environment.</span></span> <span data-ttu-id="abec7-162">Trinnene nedenfor forklarer hvordan du laster ned standardmaler, tilpasser dem og oppdaterer malene i systemet.</span><span class="sxs-lookup"><span data-stu-id="abec7-162">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="abec7-163">Bruk en webleser og last ned [Microsoft Dynamics 365 Commerce forhåndsvisning av standard e-postmaler .zip-fil](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) til den lokale datamaskinen.</span><span class="sxs-lookup"><span data-stu-id="abec7-163">In a web browser, download the [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="abec7-164">Denne filen inneholder følgende HTML-dokumenter:</span><span class="sxs-lookup"><span data-stu-id="abec7-164">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="abec7-165">Ordrebekreftelsesmal</span><span class="sxs-lookup"><span data-stu-id="abec7-165">Order confirmation template</span></span>
    - <span data-ttu-id="abec7-166">Utsted gavekort-mal</span><span class="sxs-lookup"><span data-stu-id="abec7-166">Issue gift card template</span></span>
    - <span data-ttu-id="abec7-167">Ny ordre-mal</span><span class="sxs-lookup"><span data-stu-id="abec7-167">New order template</span></span>
    - <span data-ttu-id="abec7-168">Pakke bestilt-mal</span><span class="sxs-lookup"><span data-stu-id="abec7-168">Pack order template</span></span>
    - <span data-ttu-id="abec7-169">Hent ordre-mal</span><span class="sxs-lookup"><span data-stu-id="abec7-169">Pick order template</span></span>

1. <span data-ttu-id="abec7-170">Tilpass malene ved hjelp av et tekst- eller HTML-redigeringsprogram.</span><span class="sxs-lookup"><span data-stu-id="abec7-170">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="abec7-171">Se listen over [støttede tokener](#supported-tokens-in-the-email-template) senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="abec7-171">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="abec7-172">Logg på Retail.</span><span class="sxs-lookup"><span data-stu-id="abec7-172">Sign in to Retail.</span></span>
1. <span data-ttu-id="abec7-173">Bruk menyen til venstre, og gå til **Moduler \> Organisasjonsstyring \> Oppsett \> Maler for e-post til organisasjon**.</span><span class="sxs-lookup"><span data-stu-id="abec7-173">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="abec7-174">Utvid listen til venstre for å se alle malene.</span><span class="sxs-lookup"><span data-stu-id="abec7-174">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="abec7-175">Følg denne fremgangsmåten for hver mal du vil tilpasse:</span><span class="sxs-lookup"><span data-stu-id="abec7-175">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="abec7-176">Velg malen fra listen.</span><span class="sxs-lookup"><span data-stu-id="abec7-176">Select the template in the list.</span></span>
    1. <span data-ttu-id="abec7-177">Under **Innhold i e-postmelding** velger du riktig språkversjonen fra listen.</span><span class="sxs-lookup"><span data-stu-id="abec7-177">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="abec7-178">(Standardspråket er **en-us**.)</span><span class="sxs-lookup"><span data-stu-id="abec7-178">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="abec7-179">Velg **Rediger** under **Innhold i e-postmelding**.</span><span class="sxs-lookup"><span data-stu-id="abec7-179">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="abec7-180">Ruten **Last opp e-postmal** vises.</span><span class="sxs-lookup"><span data-stu-id="abec7-180">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="abec7-181">Velg **Bla gjennom**, og finn HTML-filen med det tilpassede innholdet.</span><span class="sxs-lookup"><span data-stu-id="abec7-181">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="abec7-182">Velg **Last opp**.</span><span class="sxs-lookup"><span data-stu-id="abec7-182">Select **Upload**.</span></span> <span data-ttu-id="abec7-183">Malen lastes opp til systemet, og en forhåndsvisning vises.</span><span class="sxs-lookup"><span data-stu-id="abec7-183">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="abec7-184">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="abec7-184">Select **OK**.</span></span>
    1. <span data-ttu-id="abec7-185">Valgfritt: Tilpass egenskapen **Emne** for malen.</span><span class="sxs-lookup"><span data-stu-id="abec7-185">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="abec7-186">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="abec7-186">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="abec7-187">Støttede tokener i e-postmalen</span><span class="sxs-lookup"><span data-stu-id="abec7-187">Supported tokens in the email template</span></span>

<span data-ttu-id="abec7-188">Når e-posten gjengis, ersattes disse tokenene med de faktiske verdiene som gjelder for kunden og kundens ordre.</span><span class="sxs-lookup"><span data-stu-id="abec7-188">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="abec7-189">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="abec7-189">Sales order</span></span>

<span data-ttu-id="abec7-190">Følgende tokener gjelder for den overordnede salgsordren.</span><span class="sxs-lookup"><span data-stu-id="abec7-190">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="abec7-191">Navnet på tokenet</span><span class="sxs-lookup"><span data-stu-id="abec7-191">Name of the token</span></span> | <span data-ttu-id="abec7-192">Token </span><span class="sxs-lookup"><span data-stu-id="abec7-192">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="abec7-193">Ordrenummer</span><span class="sxs-lookup"><span data-stu-id="abec7-193">Order number</span></span>      | <span data-ttu-id="abec7-194">%salesid%</span><span class="sxs-lookup"><span data-stu-id="abec7-194">%salesid%</span></span> |
| <span data-ttu-id="abec7-195">Kundens navn</span><span class="sxs-lookup"><span data-stu-id="abec7-195">Customer's name</span></span>   | <span data-ttu-id="abec7-196">%customername%</span><span class="sxs-lookup"><span data-stu-id="abec7-196">%customername%</span></span> |
| <span data-ttu-id="abec7-197">Leveringsadresse</span><span class="sxs-lookup"><span data-stu-id="abec7-197">Delivery address</span></span>  | <span data-ttu-id="abec7-198">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="abec7-198">%deliveryaddress%</span></span> |
| <span data-ttu-id="abec7-199">Faktureringsadresse</span><span class="sxs-lookup"><span data-stu-id="abec7-199">Billing address</span></span>   | <span data-ttu-id="abec7-200">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="abec7-200">%customeraddress%</span></span> |
| <span data-ttu-id="abec7-201">Bestillingsdato</span><span class="sxs-lookup"><span data-stu-id="abec7-201">Order date</span></span>        | <span data-ttu-id="abec7-202">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="abec7-202">%shipdate%</span></span> |
| <span data-ttu-id="abec7-203">Leveringsmåte</span><span class="sxs-lookup"><span data-stu-id="abec7-203">Delivery mode</span></span>     | <span data-ttu-id="abec7-204">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="abec7-204">%modeofdelivery%</span></span> |
| <span data-ttu-id="abec7-205">Rabatt</span><span class="sxs-lookup"><span data-stu-id="abec7-205">Discount</span></span>          | <span data-ttu-id="abec7-206">%discount%</span><span class="sxs-lookup"><span data-stu-id="abec7-206">%discount%</span></span> |
| <span data-ttu-id="abec7-207">Merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="abec7-207">Sales tax</span></span>         | <span data-ttu-id="abec7-208">%tax%</span><span class="sxs-lookup"><span data-stu-id="abec7-208">%tax%</span></span> |
| <span data-ttu-id="abec7-209">Ordretotal</span><span class="sxs-lookup"><span data-stu-id="abec7-209">Order total</span></span>       | <span data-ttu-id="abec7-210">%total%</span><span class="sxs-lookup"><span data-stu-id="abec7-210">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="abec7-211">Salgslinje</span><span class="sxs-lookup"><span data-stu-id="abec7-211">Sales line</span></span>

<span data-ttu-id="abec7-212">Følgende tokener erstattes med verdier for hvert produkt i ordren.</span><span class="sxs-lookup"><span data-stu-id="abec7-212">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="abec7-213">Sett inn tokenet **Produktliste - start** i begynnelsen av HTML-blokken som gjentas for hvert produkt, og sett inn tokenet **Produktliste - slutt** på slutten av blokken.</span><span class="sxs-lookup"><span data-stu-id="abec7-213">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="abec7-214">Navnet på tokenet</span><span class="sxs-lookup"><span data-stu-id="abec7-214">Name of the token</span></span>      | <span data-ttu-id="abec7-215">Token </span><span class="sxs-lookup"><span data-stu-id="abec7-215">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="abec7-216">Produktliste – start</span><span class="sxs-lookup"><span data-stu-id="abec7-216">Product list - start</span></span>   | <span data-ttu-id="abec7-217">\<!--%tablebegin.salesline% --\></span><span class="sxs-lookup"><span data-stu-id="abec7-217">\<!--%tablebegin.salesline% --\></span></span> |
| <span data-ttu-id="abec7-218">Produktliste – slutt</span><span class="sxs-lookup"><span data-stu-id="abec7-218">Product list - end</span></span>     | <span data-ttu-id="abec7-219">\<!--%tableend.salesline%--\></span><span class="sxs-lookup"><span data-stu-id="abec7-219">\<!--%tableend.salesline%--\></span></span> |
| <span data-ttu-id="abec7-220">Produktnavn</span><span class="sxs-lookup"><span data-stu-id="abec7-220">Product name</span></span>           | <span data-ttu-id="abec7-221">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="abec7-221">%lineproductname%</span></span> |
| <span data-ttu-id="abec7-222">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="abec7-222">Description</span></span>            | <span data-ttu-id="abec7-223">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="abec7-223">%lineproductdescription%</span></span> |
| <span data-ttu-id="abec7-224">Antall</span><span class="sxs-lookup"><span data-stu-id="abec7-224">Quantity</span></span>               | <span data-ttu-id="abec7-225">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="abec7-225">%linequantity%</span></span> |
| <span data-ttu-id="abec7-226">Linjeenhetspris</span><span class="sxs-lookup"><span data-stu-id="abec7-226">Line unit price</span></span>        | <span data-ttu-id="abec7-227">%lineprice% (kontroller)</span><span class="sxs-lookup"><span data-stu-id="abec7-227">%lineprice% (verify)</span></span> |
| <span data-ttu-id="abec7-228">linjevaresum</span><span class="sxs-lookup"><span data-stu-id="abec7-228">line item total</span></span>        | <span data-ttu-id="abec7-229">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="abec7-229">%linenetamount%</span></span> |
| <span data-ttu-id="abec7-230">linjerabatt</span><span class="sxs-lookup"><span data-stu-id="abec7-230">line discount</span></span>          | <span data-ttu-id="abec7-231">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="abec7-231">%linediscount%</span></span> |
| <span data-ttu-id="abec7-232">Forsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="abec7-232">Ship date</span></span>              | <span data-ttu-id="abec7-233">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="abec7-233">%lineshipdate%</span></span> |
| <span data-ttu-id="abec7-234">Innkjøpsmetode</span><span class="sxs-lookup"><span data-stu-id="abec7-234">Procurement method</span></span>     | <span data-ttu-id="abec7-235">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="abec7-235">%linedeliverymode%</span></span> |
| <span data-ttu-id="abec7-236">leveringsadresse</span><span class="sxs-lookup"><span data-stu-id="abec7-236">delivery address</span></span>       | <span data-ttu-id="abec7-237">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="abec7-237">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="abec7-238">Salgsenhet for linjen</span><span class="sxs-lookup"><span data-stu-id="abec7-238">Sales unit of the line</span></span> | <span data-ttu-id="abec7-239">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="abec7-239">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="abec7-240">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="abec7-240">Additional resources</span></span>

[<span data-ttu-id="abec7-241">Oversikt over miljø for forhåndsvisning av Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="abec7-241">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="abec7-242">Klargjøre et miljø for forhåndsvisning av Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="abec7-242">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="abec7-243">Konfigurere et miljø for forhåndsvisning av Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="abec7-243">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="abec7-244">Vanlige spørsmål om miljø for forhåndsvisning av Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="abec7-244">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="abec7-245">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="abec7-245">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="abec7-246">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="abec7-246">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="abec7-247">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="abec7-247">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="abec7-248">Dynamics 365 Commerce-webområde</span><span class="sxs-lookup"><span data-stu-id="abec7-248">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
