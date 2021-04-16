---
title: Konfigurere valgfrie funksjoner for et evalueringsmiljø for Dynamics 365 Commerce
description: Dette emnet forklarer hvordan du konfigurerer valgfrie funksjoner for et evalueringsmiljø for Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6bc968c2659380bb8c92292ee19e3a7ec8a20a2b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795913"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="56fa8-103">Konfigurere valgfrie funksjoner for et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="56fa8-103">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="56fa8-104">Dette emnet forklarer hvordan du konfigurerer valgfrie funksjoner for et evalueringsmiljø for Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="56fa8-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="56fa8-105">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="56fa8-105">Prerequisites</span></span>

<span data-ttu-id="56fa8-106">Hvis du vil evaluere de transaksjonelle e-postfunksjonene, må følgende forutsetninger oppfylles:</span><span class="sxs-lookup"><span data-stu-id="56fa8-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="56fa8-107">Du har en e-postserver tilgjengelig (\[SMTP\]-server), som kan brukes fra Microsoft Azure-abonnementet der du klargjorde evalueringsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="56fa8-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the evaluation environment.</span></span>
- <span data-ttu-id="56fa8-108">Du har serverens fullstendig kvaliserte domenenavn (FQDN)/IP-adresse, SMTP-portnummer og godkjenningsinformasjon tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="56fa8-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="56fa8-109">Konfigurere bildeserveren</span><span class="sxs-lookup"><span data-stu-id="56fa8-109">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="56fa8-110">Finne primær URL-adresse for media</span><span class="sxs-lookup"><span data-stu-id="56fa8-110">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="56fa8-111">Før du kan fullføre denne prosedyren, må du fullføre trinnene i [Konfigurere området i handel](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span><span class="sxs-lookup"><span data-stu-id="56fa8-111">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="56fa8-112">Logg på Commerce-områdebyggeren ved hjelp av URL-adressen du noterte da du startet e-handel under klargjøring (se [Initialisere e-handel](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="56fa8-112">Sign in to the Commerce site builder by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="56fa8-113">Åpne **Fabrikam**-området.</span><span class="sxs-lookup"><span data-stu-id="56fa8-113">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="56fa8-114">Velg **Mediebibliotek** på menyen til venstre.</span><span class="sxs-lookup"><span data-stu-id="56fa8-114">On the menu on the left, select **Media Library**.</span></span>
1. <span data-ttu-id="56fa8-115">Velg et hvilket som helst enkeltbilde.</span><span class="sxs-lookup"><span data-stu-id="56fa8-115">Select any single image asset.</span></span>
1. <span data-ttu-id="56fa8-116">I egenskapsinspektøren til høyre finner du egenskapen **Offentlig URL**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-116">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="56fa8-117">Verdien er en URL.</span><span class="sxs-lookup"><span data-stu-id="56fa8-117">The value is a URL.</span></span> <span data-ttu-id="56fa8-118">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="56fa8-118">Here is an example:</span></span>

    <span data-ttu-id="56fa8-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="56fa8-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="56fa8-120">Erstatt den siste identifikatoren i URL-adressen (**MA1nQC** i forrige eksempel) med strengen **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-120">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="56fa8-121">Slik ser eksempel-URL-en ut etter at denne endringen er gjort:</span><span class="sxs-lookup"><span data-stu-id="56fa8-121">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="56fa8-122">Denne URL-adressen er primær URL-adresse for media.</span><span class="sxs-lookup"><span data-stu-id="56fa8-122">This URL is your media base URL.</span></span> <span data-ttu-id="56fa8-123">Noter den.</span><span class="sxs-lookup"><span data-stu-id="56fa8-123">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="56fa8-124">Oppdatere primær URL-adresse for media</span><span class="sxs-lookup"><span data-stu-id="56fa8-124">Update the media base URL</span></span>

1. <span data-ttu-id="56fa8-125">Logg på Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="56fa8-125">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="56fa8-126">Bruk menyen til venstre og gå til **Moduler \> Retail og Commerce \> Kanaloppsett \> Kanalprofiler**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-126">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="56fa8-127">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-127">Select **Edit**.</span></span>
1. <span data-ttu-id="56fa8-128">Fra **Profilegenskaper** erstatter du egenskapsverdien for **Primær URL-adresse for medieserver** med den primære URL-adressen for media du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="56fa8-128">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="56fa8-129">Velg kanalen med navnet **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-129">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="56fa8-130">Klikk **Legg til** under **Profilegenskaper**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-130">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="56fa8-131">For egenskapen som ble lagt til, velger du **Primær URL-adresse for medieserver** som egenskapsnøkkel.</span><span class="sxs-lookup"><span data-stu-id="56fa8-131">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="56fa8-132">Som egenskapsverdi angir du primær URL-adresse for media som du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="56fa8-132">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="56fa8-133">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-133">Select **Save**.</span></span>

## <a name="configure-and-test-the-email-server"></a><span data-ttu-id="56fa8-134">Konfigurere og teste e-postserveren</span><span class="sxs-lookup"><span data-stu-id="56fa8-134">Configure and test the email server</span></span>

> [!NOTE]
> <span data-ttu-id="56fa8-135">SMTP-serveren eller e-posttjenesten du angir her, må være tilgjengelig fra Azure-abonnementet du bruker for miljøet.</span><span class="sxs-lookup"><span data-stu-id="56fa8-135">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="56fa8-136">Logg på Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="56fa8-136">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="56fa8-137">Bruk menyen til venstre for å gå til **Moduler \> Detaljhandel \> Hovedkvarteroppsett \> Parametere \> E-postparametere**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-137">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Email parameters**.</span></span>
1. <span data-ttu-id="56fa8-138">I kategorien **SMTP-innstillinger** i feltet **Server for utgående e-post** angir du FQDN eller IP-adressen til SMTP-serveren eller e-posttjenesten.</span><span class="sxs-lookup"><span data-stu-id="56fa8-138">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="56fa8-139">I feltet **SMTP-portnummer** angir du portnummeret.</span><span class="sxs-lookup"><span data-stu-id="56fa8-139">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="56fa8-140">(Hvis du ikke bruker Secure Sockets Layer \[SSL\], er standard portnummer **25**.)</span><span class="sxs-lookup"><span data-stu-id="56fa8-140">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="56fa8-141">Hvis godkjenning kreves, angir du verdier i feltene **Brukernavn** og **Passord**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-141">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="56fa8-142">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-142">Select **Save**.</span></span>
1. <span data-ttu-id="56fa8-143">Velg **Oppdater**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-143">Select **Refresh**.</span></span>
1. <span data-ttu-id="56fa8-144">Velg **SMTP** i **E-postleverandør**-feltet i kategorien **Test e-post**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-144">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="56fa8-145">I feltet **Send til** angir du e-postadressen der du vil at test-e-posten skal leveres.</span><span class="sxs-lookup"><span data-stu-id="56fa8-145">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="56fa8-146">Velg **Send e-posttest**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-146">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="56fa8-147">Konfigurere e-postmaler</span><span class="sxs-lookup"><span data-stu-id="56fa8-147">Configure email templates</span></span>

<span data-ttu-id="56fa8-148">E-postmalen for hver transaksjonshendelse du vil sende e-postmeldinger for, må oppdateres med en gyldig e-postadresse for avsender.</span><span class="sxs-lookup"><span data-stu-id="56fa8-148">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="56fa8-149">Logg på Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="56fa8-149">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="56fa8-150">Bruk menyen til venstre for å gå til **Moduler \> Detaljhandel \> Hovedkvarteroppsett \> Parametere \> Maler for e-post til organisasjon**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-150">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="56fa8-151">Velg **Vis liste**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-151">Select **Show list**.</span></span>
1. <span data-ttu-id="56fa8-152">Følg disse trinnene for hver mal i listen:</span><span class="sxs-lookup"><span data-stu-id="56fa8-152">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="56fa8-153">Angi senderens e-postadresse i feltet **Avsenders e-postadresse**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-153">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="56fa8-154">Valgfritt: I feltet **Sendernavn** angir du navnet som skal brukes som sendernavn.</span><span class="sxs-lookup"><span data-stu-id="56fa8-154">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="56fa8-155">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-155">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="56fa8-156">Tilpasse e-postmaler</span><span class="sxs-lookup"><span data-stu-id="56fa8-156">Customize email templates</span></span>

<span data-ttu-id="56fa8-157">Det kan være lurt å tilpasse e-postmalene slik at de bruker forskjellige bilder.</span><span class="sxs-lookup"><span data-stu-id="56fa8-157">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="56fa8-158">Eller kanskje du vil oppdatere koblingene i malene slik at de går til evalueringsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="56fa8-158">Or you might want to update the links in the templates so that they go to your evaluation environment.</span></span> <span data-ttu-id="56fa8-159">Trinnene nedenfor forklarer hvordan du laster ned standardmaler, tilpasser dem og oppdaterer malene i systemet.</span><span class="sxs-lookup"><span data-stu-id="56fa8-159">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="56fa8-160">Bruk en webleser og last ned ZIP-filen [Microsoft Dynamics 365 Commerce Evaluering av standard e-postmaler](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) til den lokale datamaskinen.</span><span class="sxs-lookup"><span data-stu-id="56fa8-160">In a web browser, download the [Microsoft Dynamics 365 Commerce Evaluation default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="56fa8-161">Denne filen inneholder følgende HTML-dokumenter:</span><span class="sxs-lookup"><span data-stu-id="56fa8-161">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="56fa8-162">Ordrebekreftelsesmal</span><span class="sxs-lookup"><span data-stu-id="56fa8-162">Order confirmation template</span></span>
    - <span data-ttu-id="56fa8-163">Utsted gavekort-mal</span><span class="sxs-lookup"><span data-stu-id="56fa8-163">Issue gift card template</span></span>
    - <span data-ttu-id="56fa8-164">Ny ordre-mal</span><span class="sxs-lookup"><span data-stu-id="56fa8-164">New order template</span></span>
    - <span data-ttu-id="56fa8-165">Pakke bestilt-mal</span><span class="sxs-lookup"><span data-stu-id="56fa8-165">Pack order template</span></span>
    - <span data-ttu-id="56fa8-166">Hent ordre-mal</span><span class="sxs-lookup"><span data-stu-id="56fa8-166">Pick order template</span></span>

1. <span data-ttu-id="56fa8-167">Tilpass malene ved hjelp av et tekst- eller HTML-redigeringsprogram.</span><span class="sxs-lookup"><span data-stu-id="56fa8-167">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="56fa8-168">Se listen over [støttede tokener](#supported-tokens-in-the-email-template) senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="56fa8-168">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="56fa8-169">Logg på Commerce.</span><span class="sxs-lookup"><span data-stu-id="56fa8-169">Sign in to Commerce.</span></span>
1. <span data-ttu-id="56fa8-170">Bruk menyen til venstre, og gå til **Moduler \> Organisasjonsstyring \> Oppsett \> Maler for e-post til organisasjon**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-170">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="56fa8-171">Utvid listen til venstre for å se alle malene.</span><span class="sxs-lookup"><span data-stu-id="56fa8-171">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="56fa8-172">Følg denne fremgangsmåten for hver mal du vil tilpasse:</span><span class="sxs-lookup"><span data-stu-id="56fa8-172">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="56fa8-173">Velg malen fra listen.</span><span class="sxs-lookup"><span data-stu-id="56fa8-173">Select the template in the list.</span></span>
    1. <span data-ttu-id="56fa8-174">Under **Innhold i e-postmelding** velger du riktig språkversjonen fra listen.</span><span class="sxs-lookup"><span data-stu-id="56fa8-174">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="56fa8-175">(Standardspråket er **en-us**.)</span><span class="sxs-lookup"><span data-stu-id="56fa8-175">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="56fa8-176">Velg **Rediger** under **Innhold i e-postmelding**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-176">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="56fa8-177">Ruten **Last opp e-postmal** vises.</span><span class="sxs-lookup"><span data-stu-id="56fa8-177">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="56fa8-178">Velg **Bla gjennom**, og finn HTML-filen med det tilpassede innholdet.</span><span class="sxs-lookup"><span data-stu-id="56fa8-178">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="56fa8-179">Velg **Last opp**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-179">Select **Upload**.</span></span> <span data-ttu-id="56fa8-180">Malen lastes opp til systemet, og en forhåndsvisning vises.</span><span class="sxs-lookup"><span data-stu-id="56fa8-180">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="56fa8-181">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-181">Select **OK**.</span></span>
    1. <span data-ttu-id="56fa8-182">Valgfritt: Tilpass egenskapen **Emne** for malen.</span><span class="sxs-lookup"><span data-stu-id="56fa8-182">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="56fa8-183">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="56fa8-183">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="56fa8-184">Støttede tokener i e-postmalen</span><span class="sxs-lookup"><span data-stu-id="56fa8-184">Supported tokens in the email template</span></span>

<span data-ttu-id="56fa8-185">Når e-posten gjengis, ersattes disse tokenene med de faktiske verdiene som gjelder for kunden og kundens ordre.</span><span class="sxs-lookup"><span data-stu-id="56fa8-185">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="56fa8-186">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="56fa8-186">Sales order</span></span>

<span data-ttu-id="56fa8-187">Følgende tokener gjelder for den overordnede salgsordren.</span><span class="sxs-lookup"><span data-stu-id="56fa8-187">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="56fa8-188">Navnet på tokenet</span><span class="sxs-lookup"><span data-stu-id="56fa8-188">Name of the token</span></span> | <span data-ttu-id="56fa8-189">Token</span><span class="sxs-lookup"><span data-stu-id="56fa8-189">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="56fa8-190">Ordrenummer</span><span class="sxs-lookup"><span data-stu-id="56fa8-190">Order number</span></span>      | <span data-ttu-id="56fa8-191">%salesid%</span><span class="sxs-lookup"><span data-stu-id="56fa8-191">%salesid%</span></span> |
| <span data-ttu-id="56fa8-192">Kundens navn</span><span class="sxs-lookup"><span data-stu-id="56fa8-192">Customer's name</span></span>   | <span data-ttu-id="56fa8-193">%customername%</span><span class="sxs-lookup"><span data-stu-id="56fa8-193">%customername%</span></span> |
| <span data-ttu-id="56fa8-194">Leveringsadresse</span><span class="sxs-lookup"><span data-stu-id="56fa8-194">Delivery address</span></span>  | <span data-ttu-id="56fa8-195">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="56fa8-195">%deliveryaddress%</span></span> |
| <span data-ttu-id="56fa8-196">Faktureringsadresse</span><span class="sxs-lookup"><span data-stu-id="56fa8-196">Billing address</span></span>   | <span data-ttu-id="56fa8-197">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="56fa8-197">%customeraddress%</span></span> |
| <span data-ttu-id="56fa8-198">Bestillingsdato</span><span class="sxs-lookup"><span data-stu-id="56fa8-198">Order date</span></span>        | <span data-ttu-id="56fa8-199">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="56fa8-199">%shipdate%</span></span> |
| <span data-ttu-id="56fa8-200">Leveringsmåte</span><span class="sxs-lookup"><span data-stu-id="56fa8-200">Delivery mode</span></span>     | <span data-ttu-id="56fa8-201">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="56fa8-201">%modeofdelivery%</span></span> |
| <span data-ttu-id="56fa8-202">Rabatt</span><span class="sxs-lookup"><span data-stu-id="56fa8-202">Discount</span></span>          | <span data-ttu-id="56fa8-203">%discount%</span><span class="sxs-lookup"><span data-stu-id="56fa8-203">%discount%</span></span> |
| <span data-ttu-id="56fa8-204">Merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="56fa8-204">Sales tax</span></span>         | <span data-ttu-id="56fa8-205">%tax%</span><span class="sxs-lookup"><span data-stu-id="56fa8-205">%tax%</span></span> |
| <span data-ttu-id="56fa8-206">Ordretotal</span><span class="sxs-lookup"><span data-stu-id="56fa8-206">Order total</span></span>       | <span data-ttu-id="56fa8-207">%total%</span><span class="sxs-lookup"><span data-stu-id="56fa8-207">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="56fa8-208">Salgslinje</span><span class="sxs-lookup"><span data-stu-id="56fa8-208">Sales line</span></span>

<span data-ttu-id="56fa8-209">Følgende tokener erstattes med verdier for hvert produkt i ordren.</span><span class="sxs-lookup"><span data-stu-id="56fa8-209">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="56fa8-210">Sett inn tokenet **Produktliste - start** i begynnelsen av HTML-blokken som gjentas for hvert produkt, og sett inn tokenet **Produktliste - slutt** på slutten av blokken.</span><span class="sxs-lookup"><span data-stu-id="56fa8-210">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="56fa8-211">Navnet på tokenet</span><span class="sxs-lookup"><span data-stu-id="56fa8-211">Name of the token</span></span>      | <span data-ttu-id="56fa8-212">Token</span><span class="sxs-lookup"><span data-stu-id="56fa8-212">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="56fa8-213">Produktliste – start</span><span class="sxs-lookup"><span data-stu-id="56fa8-213">Product list - start</span></span>   | \<!--%tablebegin.salesline% --\> |
| <span data-ttu-id="56fa8-214">Produktliste – slutt</span><span class="sxs-lookup"><span data-stu-id="56fa8-214">Product list - end</span></span>     | \<!--%tableend.salesline%--\> |
| <span data-ttu-id="56fa8-215">Produktnavn</span><span class="sxs-lookup"><span data-stu-id="56fa8-215">Product name</span></span>           | <span data-ttu-id="56fa8-216">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="56fa8-216">%lineproductname%</span></span> |
| <span data-ttu-id="56fa8-217">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="56fa8-217">Description</span></span>            | <span data-ttu-id="56fa8-218">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="56fa8-218">%lineproductdescription%</span></span> |
| <span data-ttu-id="56fa8-219">Antall</span><span class="sxs-lookup"><span data-stu-id="56fa8-219">Quantity</span></span>               | <span data-ttu-id="56fa8-220">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="56fa8-220">%linequantity%</span></span> |
| <span data-ttu-id="56fa8-221">Linjeenhetspris</span><span class="sxs-lookup"><span data-stu-id="56fa8-221">Line unit price</span></span>        | <span data-ttu-id="56fa8-222">%lineprice% (verifiser)</span><span class="sxs-lookup"><span data-stu-id="56fa8-222">%lineprice% (verify)</span></span> |
| <span data-ttu-id="56fa8-223">linjevaresum</span><span class="sxs-lookup"><span data-stu-id="56fa8-223">line item total</span></span>        | <span data-ttu-id="56fa8-224">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="56fa8-224">%linenetamount%</span></span> |
| <span data-ttu-id="56fa8-225">linjerabatt</span><span class="sxs-lookup"><span data-stu-id="56fa8-225">line discount</span></span>          | <span data-ttu-id="56fa8-226">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="56fa8-226">%linediscount%</span></span> |
| <span data-ttu-id="56fa8-227">Forsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="56fa8-227">Ship date</span></span>              | <span data-ttu-id="56fa8-228">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="56fa8-228">%lineshipdate%</span></span> |
| <span data-ttu-id="56fa8-229">Innkjøpsmetode</span><span class="sxs-lookup"><span data-stu-id="56fa8-229">Procurement method</span></span>     | <span data-ttu-id="56fa8-230">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="56fa8-230">%linedeliverymode%</span></span> |
| <span data-ttu-id="56fa8-231">leveringsadresse</span><span class="sxs-lookup"><span data-stu-id="56fa8-231">delivery address</span></span>       | <span data-ttu-id="56fa8-232">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="56fa8-232">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="56fa8-233">Salgsenhet for linjen</span><span class="sxs-lookup"><span data-stu-id="56fa8-233">Sales unit of the line</span></span> | <span data-ttu-id="56fa8-234">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="56fa8-234">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="56fa8-235">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="56fa8-235">Additional resources</span></span>

[<span data-ttu-id="56fa8-236">Oversikt over Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="56fa8-236">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="56fa8-237">Klargjøre et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="56fa8-237">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="56fa8-238">Konfigurere et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="56fa8-238">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="56fa8-239">Konfigurere BOPIS i et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="56fa8-239">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="56fa8-240">Vanlige spørsmål om Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="56fa8-240">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="56fa8-241">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="56fa8-241">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="56fa8-242">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="56fa8-242">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="56fa8-243">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="56fa8-243">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="56fa8-244">Dynamics 365 Commerce-webområde</span><span class="sxs-lookup"><span data-stu-id="56fa8-244">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]