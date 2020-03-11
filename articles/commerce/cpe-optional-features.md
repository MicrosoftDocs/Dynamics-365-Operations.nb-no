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
ms.openlocfilehash: 4b17f8e9b0d8a9a62714d0073561e66642b2eaf9
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057746"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="7ee20-103">Konfigurere valgfrie funksjoner for et miljø for forhåndsvisning av Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7ee20-103">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7ee20-104">Dette emnet forklarer hvordan du konfigurerer valgfrie funksjoner for et Microsoft Dynamics 365 Commerce-forhåndsvisningsmiljø.</span><span class="sxs-lookup"><span data-stu-id="7ee20-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7ee20-105">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="7ee20-105">Prerequisites</span></span>

<span data-ttu-id="7ee20-106">Hvis du vil evaluere de transaksjonelle e-postfunksjonene, må følgende forutsetninger oppfylles:</span><span class="sxs-lookup"><span data-stu-id="7ee20-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="7ee20-107">Du har en e-postserver tilgjengelig (\[SMTP\]-server), som kan brukes fra Microsoft Azure-abonnementet der du klargjorde forhåndsvisningsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="7ee20-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the preview environment.</span></span>
- <span data-ttu-id="7ee20-108">Du har serverens fullstendig kvaliserte domenenavn (FQDN)/IP-adresse, SMTP-portnummer og godkjenningsinformasjon tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="7ee20-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="7ee20-109">Hvis du vil evaluere funksjoner for digital aktivastyring ved inntak av nye omnikanalbilder, må du ha navnet på leierenaktiva for innholdsstyringssystemet (CMS) tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="7ee20-109">If you want to evaluate Digital Asset Management features by ingesting new omni-channel images, you must have the name of your content management system (CMS) tenant available.</span></span> <span data-ttu-id="7ee20-110">Du finner instruksjoner for å finne dette navnet senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="7ee20-110">Instructions for finding this name are provided later in this topic.</span></span> <span data-ttu-id="7ee20-111">> > > (Sp: hvor er instruksjonene?)</span><span class="sxs-lookup"><span data-stu-id="7ee20-111">>>>(Q: where are the instructions?)</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="7ee20-112">Konfigurere bildeserveren</span><span class="sxs-lookup"><span data-stu-id="7ee20-112">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="7ee20-113">Finne primær URL-adresse for media</span><span class="sxs-lookup"><span data-stu-id="7ee20-113">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="7ee20-114">Før du kan fullføre denne prosedyren, må du fullføre trinnene i [Konfigurere området i handel](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span><span class="sxs-lookup"><span data-stu-id="7ee20-114">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="7ee20-115">Logg på verktøyet for administrasjon av e-handel-området ved hjelp av URL-adressen du noterte da du startet e-handel under klargjøring (se [Initialisere e-handel](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="7ee20-115">Sign in to the Commerce site management tool by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="7ee20-116">Åpne **Fabrikam**-området.</span><span class="sxs-lookup"><span data-stu-id="7ee20-116">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="7ee20-117">Velg **Aktiva** på menyen til venstre.</span><span class="sxs-lookup"><span data-stu-id="7ee20-117">On the menu on the left, select **Assets**.</span></span>
1. <span data-ttu-id="7ee20-118">Velg et hvilket som helst enkeltbilde.</span><span class="sxs-lookup"><span data-stu-id="7ee20-118">Select any single image asset.</span></span>
1. <span data-ttu-id="7ee20-119">I egenskapsinspektøren til høyre finner du egenskapen **Offentlig URL**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-119">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="7ee20-120">Verdien er en URL.</span><span class="sxs-lookup"><span data-stu-id="7ee20-120">The value is a URL.</span></span> <span data-ttu-id="7ee20-121">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="7ee20-121">Here is an example:</span></span>

    <span data-ttu-id="7ee20-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="7ee20-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="7ee20-123">Erstatt den siste identifikatoren i URL-adressen (**MA1nQC** i forrige eksempel) med strengen **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-123">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="7ee20-124">Slik ser eksempel-URL-en ut etter at denne endringen er gjort:</span><span class="sxs-lookup"><span data-stu-id="7ee20-124">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="7ee20-125">Denne URL-adressen er primær URL-adresse for media.</span><span class="sxs-lookup"><span data-stu-id="7ee20-125">This URL is your media base URL.</span></span> <span data-ttu-id="7ee20-126">Noter den.</span><span class="sxs-lookup"><span data-stu-id="7ee20-126">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="7ee20-127">Oppdatere primær URL-adresse for media</span><span class="sxs-lookup"><span data-stu-id="7ee20-127">Update the media base URL</span></span>

1. <span data-ttu-id="7ee20-128">Logg på Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7ee20-128">Sign in to Dynamics 365 Commerce.</span></span>
1. <span data-ttu-id="7ee20-129">Bruk menyen til venstre og gå til **Moduler \> Retail og Commerce \> Kanaloppsett \> Kanalprofiler**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-129">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="7ee20-130">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-130">Select **Edit**.</span></span>
1. <span data-ttu-id="7ee20-131">Fra **Profilegenskaper** erstatter du egenskapsverdien for **Primær URL-adresse for medieserver** med den primære URL-adressen for media du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="7ee20-131">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="7ee20-132">Velg den andre kanalen fra listen til venstre, under **Standard**-kanal.</span><span class="sxs-lookup"><span data-stu-id="7ee20-132">In the list on the left, under the **Default** channel, select the other channel.</span></span>
1. <span data-ttu-id="7ee20-133">Klikk **Legg til** under **Profilegenskaper**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-133">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="7ee20-134">For egenskapen som ble lagt til, velger du **Primær URL-adresse for medieserver** som egenskapsnøkkel.</span><span class="sxs-lookup"><span data-stu-id="7ee20-134">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="7ee20-135">Som egenskapsverdi angir du primær URL-adresse for media som du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="7ee20-135">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="7ee20-136">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-136">Select **Save**.</span></span>

## <a name="configure-the-email-server"></a><span data-ttu-id="7ee20-137">Konfigurere e-postserveren</span><span class="sxs-lookup"><span data-stu-id="7ee20-137">Configure the email server</span></span>

> [!NOTE]
> <span data-ttu-id="7ee20-138">SMTP-serveren eller e-posttjenesten du angir her, må være tilgjengelig fra Azure-abonnementet du bruker for miljøet.</span><span class="sxs-lookup"><span data-stu-id="7ee20-138">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="7ee20-139">Logg på Commerce.</span><span class="sxs-lookup"><span data-stu-id="7ee20-139">Sign in to Commerce.</span></span>
1. <span data-ttu-id="7ee20-140">Bruk menyen til venstre, og gå til **Moduler \> Systemadministrasjon \> Oppsett \> E-post \> E-postparametere**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-140">Use the menu on the left to go to **Modules \> System administration \> Setup \> Email \> Email parameters**.</span></span>
1. <span data-ttu-id="7ee20-141">I kategorien **SMTP-innstillinger** i feltet **Server for utgående e-post** angir du FQDN eller IP-adressen til SMTP-serveren eller e-posttjenesten.</span><span class="sxs-lookup"><span data-stu-id="7ee20-141">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="7ee20-142">I feltet **SMTP-portnummer** angir du portnummeret.</span><span class="sxs-lookup"><span data-stu-id="7ee20-142">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="7ee20-143">(Hvis du ikke bruker Secure Sockets Layer \[SSL\], er standard portnummer **25**.)</span><span class="sxs-lookup"><span data-stu-id="7ee20-143">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="7ee20-144">Hvis godkjenning kreves, angir du verdier i feltene **Brukernavn** og **Passord**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-144">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="7ee20-145">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-145">Select **Save**.</span></span>
1. <span data-ttu-id="7ee20-146">Velg **Oppdater**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-146">Select **Refresh**.</span></span>
1. <span data-ttu-id="7ee20-147">Velg **SMTP** i **E-postleverandør**-feltet i kategorien **Test e-post**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-147">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="7ee20-148">I feltet **Send til** angir du e-postadressen der du vil at test-e-posten skal leveres.</span><span class="sxs-lookup"><span data-stu-id="7ee20-148">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="7ee20-149">Velg **Send e-posttest**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-149">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="7ee20-150">Konfigurere e-postmaler</span><span class="sxs-lookup"><span data-stu-id="7ee20-150">Configure email templates</span></span>

<span data-ttu-id="7ee20-151">E-postmalen for hver transaksjonshendelse du vil sende e-postmeldinger for, må oppdateres med en gyldig e-postadresse for avsender.</span><span class="sxs-lookup"><span data-stu-id="7ee20-151">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="7ee20-152">Logg på Commerce.</span><span class="sxs-lookup"><span data-stu-id="7ee20-152">Sign in to Commerce.</span></span>
1. <span data-ttu-id="7ee20-153">Bruk menyen til venstre, og gå til **Moduler \> Organisasjonsstyring \> Oppsett \> Maler for e-post til organisasjon**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-153">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="7ee20-154">Velg **Vis liste**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-154">Select **Show list**.</span></span>
1. <span data-ttu-id="7ee20-155">Følg disse trinnene for hver mal i listen:</span><span class="sxs-lookup"><span data-stu-id="7ee20-155">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="7ee20-156">Angi senderens e-postadresse i feltet **Avsenders e-postadresse**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-156">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="7ee20-157">Valgfritt: I feltet **Sendernavn** angir du navnet som skal brukes som sendernavn.</span><span class="sxs-lookup"><span data-stu-id="7ee20-157">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="7ee20-158">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-158">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="7ee20-159">Tilpasse e-postmaler</span><span class="sxs-lookup"><span data-stu-id="7ee20-159">Customize email templates</span></span>

<span data-ttu-id="7ee20-160">Det kan være lurt å tilpasse e-postmalene slik at de bruker forskjellige bilder.</span><span class="sxs-lookup"><span data-stu-id="7ee20-160">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="7ee20-161">Eller kanskje du vil oppdatere koblingene i malene slik at de går til forhåndsvisningsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="7ee20-161">Or you might want to update the links in the templates so that they go to your preview environment.</span></span> <span data-ttu-id="7ee20-162">Trinnene nedenfor forklarer hvordan du laster ned standardmaler, tilpasser dem og oppdaterer malene i systemet.</span><span class="sxs-lookup"><span data-stu-id="7ee20-162">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="7ee20-163">Bruk en webleser og last ned [Microsoft Dynamics 365 Commerce forhåndsvisning av standard e-postmaler .zip-fil](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) til den lokale datamaskinen.</span><span class="sxs-lookup"><span data-stu-id="7ee20-163">In a web browser, download the [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="7ee20-164">Denne filen inneholder følgende HTML-dokumenter:</span><span class="sxs-lookup"><span data-stu-id="7ee20-164">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="7ee20-165">Ordrebekreftelsesmal</span><span class="sxs-lookup"><span data-stu-id="7ee20-165">Order confirmation template</span></span>
    - <span data-ttu-id="7ee20-166">Utsted gavekort-mal</span><span class="sxs-lookup"><span data-stu-id="7ee20-166">Issue gift card template</span></span>
    - <span data-ttu-id="7ee20-167">Ny ordre-mal</span><span class="sxs-lookup"><span data-stu-id="7ee20-167">New order template</span></span>
    - <span data-ttu-id="7ee20-168">Pakke bestilt-mal</span><span class="sxs-lookup"><span data-stu-id="7ee20-168">Pack order template</span></span>
    - <span data-ttu-id="7ee20-169">Hent ordre-mal</span><span class="sxs-lookup"><span data-stu-id="7ee20-169">Pick order template</span></span>

1. <span data-ttu-id="7ee20-170">Tilpass malene ved hjelp av et tekst- eller HTML-redigeringsprogram.</span><span class="sxs-lookup"><span data-stu-id="7ee20-170">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="7ee20-171">Se listen over [støttede tokener](#supported-tokens-in-the-email-template) senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="7ee20-171">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="7ee20-172">Logg på Commerce.</span><span class="sxs-lookup"><span data-stu-id="7ee20-172">Sign in to Commerce.</span></span>
1. <span data-ttu-id="7ee20-173">Bruk menyen til venstre, og gå til **Moduler \> Organisasjonsstyring \> Oppsett \> Maler for e-post til organisasjon**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-173">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="7ee20-174">Utvid listen til venstre for å se alle malene.</span><span class="sxs-lookup"><span data-stu-id="7ee20-174">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="7ee20-175">Følg denne fremgangsmåten for hver mal du vil tilpasse:</span><span class="sxs-lookup"><span data-stu-id="7ee20-175">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="7ee20-176">Velg malen fra listen.</span><span class="sxs-lookup"><span data-stu-id="7ee20-176">Select the template in the list.</span></span>
    1. <span data-ttu-id="7ee20-177">Under **Innhold i e-postmelding** velger du riktig språkversjonen fra listen.</span><span class="sxs-lookup"><span data-stu-id="7ee20-177">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="7ee20-178">(Standardspråket er **en-us**.)</span><span class="sxs-lookup"><span data-stu-id="7ee20-178">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="7ee20-179">Velg **Rediger** under **Innhold i e-postmelding**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-179">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="7ee20-180">Ruten **Last opp e-postmal** vises.</span><span class="sxs-lookup"><span data-stu-id="7ee20-180">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="7ee20-181">Velg **Bla gjennom**, og finn HTML-filen med det tilpassede innholdet.</span><span class="sxs-lookup"><span data-stu-id="7ee20-181">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="7ee20-182">Velg **Last opp**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-182">Select **Upload**.</span></span> <span data-ttu-id="7ee20-183">Malen lastes opp til systemet, og en forhåndsvisning vises.</span><span class="sxs-lookup"><span data-stu-id="7ee20-183">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="7ee20-184">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-184">Select **OK**.</span></span>
    1. <span data-ttu-id="7ee20-185">Valgfritt: Tilpass egenskapen **Emne** for malen.</span><span class="sxs-lookup"><span data-stu-id="7ee20-185">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="7ee20-186">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="7ee20-186">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="7ee20-187">Støttede tokener i e-postmalen</span><span class="sxs-lookup"><span data-stu-id="7ee20-187">Supported tokens in the email template</span></span>

<span data-ttu-id="7ee20-188">Når e-posten gjengis, ersattes disse tokenene med de faktiske verdiene som gjelder for kunden og kundens ordre.</span><span class="sxs-lookup"><span data-stu-id="7ee20-188">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="7ee20-189">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="7ee20-189">Sales order</span></span>

<span data-ttu-id="7ee20-190">Følgende tokener gjelder for den overordnede salgsordren.</span><span class="sxs-lookup"><span data-stu-id="7ee20-190">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="7ee20-191">Navnet på tokenet</span><span class="sxs-lookup"><span data-stu-id="7ee20-191">Name of the token</span></span> | <span data-ttu-id="7ee20-192">Token </span><span class="sxs-lookup"><span data-stu-id="7ee20-192">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="7ee20-193">Ordrenummer</span><span class="sxs-lookup"><span data-stu-id="7ee20-193">Order number</span></span>      | <span data-ttu-id="7ee20-194">%salesid%</span><span class="sxs-lookup"><span data-stu-id="7ee20-194">%salesid%</span></span> |
| <span data-ttu-id="7ee20-195">Kundens navn</span><span class="sxs-lookup"><span data-stu-id="7ee20-195">Customer's name</span></span>   | <span data-ttu-id="7ee20-196">%customername%</span><span class="sxs-lookup"><span data-stu-id="7ee20-196">%customername%</span></span> |
| <span data-ttu-id="7ee20-197">Leveringsadresse</span><span class="sxs-lookup"><span data-stu-id="7ee20-197">Delivery address</span></span>  | <span data-ttu-id="7ee20-198">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="7ee20-198">%deliveryaddress%</span></span> |
| <span data-ttu-id="7ee20-199">Faktureringsadresse</span><span class="sxs-lookup"><span data-stu-id="7ee20-199">Billing address</span></span>   | <span data-ttu-id="7ee20-200">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="7ee20-200">%customeraddress%</span></span> |
| <span data-ttu-id="7ee20-201">Bestillingsdato</span><span class="sxs-lookup"><span data-stu-id="7ee20-201">Order date</span></span>        | <span data-ttu-id="7ee20-202">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="7ee20-202">%shipdate%</span></span> |
| <span data-ttu-id="7ee20-203">Leveringsmåte</span><span class="sxs-lookup"><span data-stu-id="7ee20-203">Delivery mode</span></span>     | <span data-ttu-id="7ee20-204">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="7ee20-204">%modeofdelivery%</span></span> |
| <span data-ttu-id="7ee20-205">Rabatt</span><span class="sxs-lookup"><span data-stu-id="7ee20-205">Discount</span></span>          | <span data-ttu-id="7ee20-206">%discount%</span><span class="sxs-lookup"><span data-stu-id="7ee20-206">%discount%</span></span> |
| <span data-ttu-id="7ee20-207">Merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="7ee20-207">Sales tax</span></span>         | <span data-ttu-id="7ee20-208">%tax%</span><span class="sxs-lookup"><span data-stu-id="7ee20-208">%tax%</span></span> |
| <span data-ttu-id="7ee20-209">Ordretotal</span><span class="sxs-lookup"><span data-stu-id="7ee20-209">Order total</span></span>       | <span data-ttu-id="7ee20-210">%total%</span><span class="sxs-lookup"><span data-stu-id="7ee20-210">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="7ee20-211">Salgslinje</span><span class="sxs-lookup"><span data-stu-id="7ee20-211">Sales line</span></span>

<span data-ttu-id="7ee20-212">Følgende tokener erstattes med verdier for hvert produkt i ordren.</span><span class="sxs-lookup"><span data-stu-id="7ee20-212">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="7ee20-213">Sett inn tokenet **Produktliste - start** i begynnelsen av HTML-blokken som gjentas for hvert produkt, og sett inn tokenet **Produktliste - slutt** på slutten av blokken.</span><span class="sxs-lookup"><span data-stu-id="7ee20-213">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="7ee20-214">Navnet på tokenet</span><span class="sxs-lookup"><span data-stu-id="7ee20-214">Name of the token</span></span>      | <span data-ttu-id="7ee20-215">Token </span><span class="sxs-lookup"><span data-stu-id="7ee20-215">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="7ee20-216">Produktliste – start</span><span class="sxs-lookup"><span data-stu-id="7ee20-216">Product list - start</span></span>   | <span data-ttu-id="7ee20-217">\<!--%tablebegin.salesline% --\></span><span class="sxs-lookup"><span data-stu-id="7ee20-217">\<!--%tablebegin.salesline% --\></span></span> |
| <span data-ttu-id="7ee20-218">Produktliste – slutt</span><span class="sxs-lookup"><span data-stu-id="7ee20-218">Product list - end</span></span>     | <span data-ttu-id="7ee20-219">\<!--%tableend.salesline%--\></span><span class="sxs-lookup"><span data-stu-id="7ee20-219">\<!--%tableend.salesline%--\></span></span> |
| <span data-ttu-id="7ee20-220">Produktnavn</span><span class="sxs-lookup"><span data-stu-id="7ee20-220">Product name</span></span>           | <span data-ttu-id="7ee20-221">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="7ee20-221">%lineproductname%</span></span> |
| <span data-ttu-id="7ee20-222">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="7ee20-222">Description</span></span>            | <span data-ttu-id="7ee20-223">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="7ee20-223">%lineproductdescription%</span></span> |
| <span data-ttu-id="7ee20-224">Antall</span><span class="sxs-lookup"><span data-stu-id="7ee20-224">Quantity</span></span>               | <span data-ttu-id="7ee20-225">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="7ee20-225">%linequantity%</span></span> |
| <span data-ttu-id="7ee20-226">Linjeenhetspris</span><span class="sxs-lookup"><span data-stu-id="7ee20-226">Line unit price</span></span>        | <span data-ttu-id="7ee20-227">%lineprice% (kontroller)</span><span class="sxs-lookup"><span data-stu-id="7ee20-227">%lineprice% (verify)</span></span> |
| <span data-ttu-id="7ee20-228">linjevaresum</span><span class="sxs-lookup"><span data-stu-id="7ee20-228">line item total</span></span>        | <span data-ttu-id="7ee20-229">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="7ee20-229">%linenetamount%</span></span> |
| <span data-ttu-id="7ee20-230">linjerabatt</span><span class="sxs-lookup"><span data-stu-id="7ee20-230">line discount</span></span>          | <span data-ttu-id="7ee20-231">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="7ee20-231">%linediscount%</span></span> |
| <span data-ttu-id="7ee20-232">Forsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="7ee20-232">Ship date</span></span>              | <span data-ttu-id="7ee20-233">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="7ee20-233">%lineshipdate%</span></span> |
| <span data-ttu-id="7ee20-234">Innkjøpsmetode</span><span class="sxs-lookup"><span data-stu-id="7ee20-234">Procurement method</span></span>     | <span data-ttu-id="7ee20-235">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="7ee20-235">%linedeliverymode%</span></span> |
| <span data-ttu-id="7ee20-236">leveringsadresse</span><span class="sxs-lookup"><span data-stu-id="7ee20-236">delivery address</span></span>       | <span data-ttu-id="7ee20-237">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="7ee20-237">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="7ee20-238">Salgsenhet for linjen</span><span class="sxs-lookup"><span data-stu-id="7ee20-238">Sales unit of the line</span></span> | <span data-ttu-id="7ee20-239">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="7ee20-239">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="7ee20-240">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="7ee20-240">Additional resources</span></span>

[<span data-ttu-id="7ee20-241">Oversikt over miljø for forhåndsvisning av Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7ee20-241">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="7ee20-242">Klargjøre et miljø for forhåndsvisning av Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7ee20-242">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="7ee20-243">Konfigurere et miljø for forhåndsvisning av Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7ee20-243">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="7ee20-244">Vanlige spørsmål om miljø for forhåndsvisning av Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7ee20-244">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="7ee20-245">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="7ee20-245">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="7ee20-246">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="7ee20-246">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="7ee20-247">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="7ee20-247">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="7ee20-248">Dynamics 365 Commerce-webområde</span><span class="sxs-lookup"><span data-stu-id="7ee20-248">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
