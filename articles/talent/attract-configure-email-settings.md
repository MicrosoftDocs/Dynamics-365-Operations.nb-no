---
title: Konfigurere e-postinnstillinger i Attract
description: Dette emnet beskriver hvordan konfigurerer innstillinger for e-post som sendes av Microsoft Dynamcis 365 Talent – Attract.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c1ebfaeb2e9bc2836bb70e87afa93484c829b6cb
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833121"
---
# <a name="configure-email-settings-in-attract"></a><span data-ttu-id="95d77-103">Konfigurere e-postinnstillinger i Attract</span><span class="sxs-lookup"><span data-stu-id="95d77-103">Configure email settings in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="95d77-104">Varemerket ditt vekker tillit og hjelper deg å utvikle et forhold til kandidater selv før de søker på stillinger.</span><span class="sxs-lookup"><span data-stu-id="95d77-104">Your brand establishes trust and helps you build a relationship with candidates before they even apply for your positions.</span></span> <span data-ttu-id="95d77-105">Positive oppfatninger av varemerket tiltrekker de største talentene og øker lojaliteten til eksisterende ansatte.</span><span class="sxs-lookup"><span data-stu-id="95d77-105">Positive brand perception attracts top talent and increases the loyalty of existing employees.</span></span> <span data-ttu-id="95d77-106">Microsoft Dynamics 365 Talent: Attract lar deg konfigurere e-postmeldinger slik at de gjenspeiler firmaets varemerke.</span><span class="sxs-lookup"><span data-stu-id="95d77-106">Microsoft Dynamics 365 Talent: Attract lets you configure emails so that they reflect your company's brand.</span></span> <span data-ttu-id="95d77-107">Derfor kan du gi jobbkandidater en konsekvent opplevelse etter hvert som de går gjennom søknadsprosessen.</span><span class="sxs-lookup"><span data-stu-id="95d77-107">Therefore, you can provide a consistent experience to job candidates as they progress through the application process.</span></span>

<span data-ttu-id="95d77-108">Med Attract kan du utføre følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="95d77-108">Attract lets you perform these actions:</span></span>

- <span data-ttu-id="95d77-109">Konfigurer e-postinnstillinger slik at firmaets e-posttjenestekonto i Microsoft Exchange brukes.</span><span class="sxs-lookup"><span data-stu-id="95d77-109">Configure email settings so that your company's Microsoft Exchange email service account is used.</span></span> <span data-ttu-id="95d77-110">På denne måten vet kandidater at e-postmeldingene kommer fra firmaet.</span><span class="sxs-lookup"><span data-stu-id="95d77-110">In this way, candidates know that the emails are coming from your company.</span></span> <span data-ttu-id="95d77-111">Du kan for eksempel konfigurere innstillingene slik at kandidater mottar e-postmeldinger fra `recruiting@contoso.com` i stedet for `contoso@microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="95d77-111">For example, you can configure your settings so that candidates receive emails from `recruiting@contoso.com` instead of `contoso@microsoft.com`.</span></span>
- <span data-ttu-id="95d77-112">Opprett konsekvent varemerking for alle e-postmeldingene ved å angi en global topptekst og bunntekst for e-postmaler.</span><span class="sxs-lookup"><span data-stu-id="95d77-112">Create consistent branding for all your email communications by setting a global header and footer for email templates.</span></span> 

> [!NOTE]
> <span data-ttu-id="95d77-113">Hvis du vil konfigurere Attract slik at det bruker firmaets e-posttjenestekonto til å sende e-post, trenger du tillegget for omfattende ansettelse.</span><span class="sxs-lookup"><span data-stu-id="95d77-113">To configure Attract so that it uses your company's email service account to send email, you need the Comprehensive hiring add-on.</span></span>

## <a name="connect-an-email-service-account"></a><span data-ttu-id="95d77-114">Koble til en e-posttjenestekonto</span><span class="sxs-lookup"><span data-stu-id="95d77-114">Connect an email service account</span></span>

<span data-ttu-id="95d77-115">Når du kobler til firmaets e-posttjenestekonto, kan du skape en varemerket e-postopplevelse for jobbkandidatene.</span><span class="sxs-lookup"><span data-stu-id="95d77-115">By connecting your company's email service account, you can create a branded email experience for your job candidates.</span></span> <span data-ttu-id="95d77-116">Hvis du ikke kobler til firmakontoen, bruker Attract den standard Microsoft-varemerkede e-posttjenestekontoen.</span><span class="sxs-lookup"><span data-stu-id="95d77-116">If you don't connect your company account, Attract uses the default Microsoft-branded email service account.</span></span>

1. <span data-ttu-id="95d77-117">Velg **Innstillinger** (tannhjulsikonet i øvre høyre hjørne), og velg deretter **Administrasjonssenter**.</span><span class="sxs-lookup"><span data-stu-id="95d77-117">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="95d77-118">Velg **Koble til en firmakonto** under **E-posttjenestekontoer** i fanen **E-postinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="95d77-118">On the **Email settings** tab, under **Email service accounts**, select **Connect a company account**.</span></span>

    ![Koble til firmaets e-posttjenestekonto i Attract](./media/attract-admin-email-service-accounts.png)

    <span data-ttu-id="95d77-120">Hvis du vil ha mer informasjon om hvordan du oppretter en delt e-postkonto, kan du se [Delte postbokser i Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="95d77-120">For more information about how to create a shared email account, see [Shared mailboxes in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span></span>

3. <span data-ttu-id="95d77-121">I påloggingsvinduet for Microsoft logger du på ved å bruke firmalegitimasjonen.</span><span class="sxs-lookup"><span data-stu-id="95d77-121">In the Microsoft sign-in window, sign in by using your corporate credentials.</span></span>
4. <span data-ttu-id="95d77-122">Hvis du ikke har konfigurert en e-posttjenestekonto, eller hvis du vil legge til en ny, velger du **Legg til ny tjenestekonto**, og angi deretter e-postinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="95d77-122">If you haven't yet set up an email service account, or if you want to add a new one, select **Add new service account**, and then enter your email information.</span></span> <span data-ttu-id="95d77-123">Hvis du allerede har konfigurert e-posttjenestekontoen du vil bruke, velger du den.</span><span class="sxs-lookup"><span data-stu-id="95d77-123">If you've already set up the email service account that you want to use, select it.</span></span>

<span data-ttu-id="95d77-124">Når e-posttjenestekontoen er konfigurert, vises den under **E-posttjenestekontoer**.</span><span class="sxs-lookup"><span data-stu-id="95d77-124">When your email service account is successfully configured, you will see it listed under **Email service accounts**.</span></span>

## <a name="disconnect-an-email-service-account"></a><span data-ttu-id="95d77-125">Koble fra en e-posttjenestekonto</span><span class="sxs-lookup"><span data-stu-id="95d77-125">Disconnect an email service account</span></span>

<span data-ttu-id="95d77-126">Hvis du vil slutte å bruke firmaets domene i e-postkommunikasjon via Attract, kan du koble fra en e-posttjenestekonto.</span><span class="sxs-lookup"><span data-stu-id="95d77-126">If you want to stop using your company's domain in email communications through Attract, you can disconnect an email service account.</span></span>

1. <span data-ttu-id="95d77-127">Velg **Innstillinger** (tannhjulsikonet i øvre høyre hjørne), og velg deretter **Administrasjonssenter**.</span><span class="sxs-lookup"><span data-stu-id="95d77-127">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="95d77-128">Under **posttjenestekontoer** i fanen **E-postinnstillinger** velger du **Mer**-knappen (tre loddrette prikker) ved siden av e-posttjenestekontoen du vil koble fra.</span><span class="sxs-lookup"><span data-stu-id="95d77-128">On the **Email settings** tab, under **Email service accounts**, select the **More** button (three vertical dots) next to the email service account that you want to disconnect.</span></span>
3. <span data-ttu-id="95d77-129">Velg **Koble fra e-postkonto**.</span><span class="sxs-lookup"><span data-stu-id="95d77-129">Select **Disconnect email account**.</span></span>

    ![Koble fra firmaets e-posttjenestekonto](./media/attract-admin-disconnect-email-account.png)

4. <span data-ttu-id="95d77-131">Når du blir bedt om å bekrefte operasjonen, velger du **Koble fra**.</span><span class="sxs-lookup"><span data-stu-id="95d77-131">When you're prompted to confirm the operation, select **Disconnect**.</span></span>

    ![Bekrefte frakoblingen av firmaets e-posttjenestekonto](./media/attract-admin-email-confirm-disconnect.png)

<span data-ttu-id="95d77-133">Hvis du ikke kobler til en annen e-posttjenestekonto, bruker e-postmeldinger som sendes fra Attract, den standard Microsoft-varemerkede e-posttjenestekontoen.</span><span class="sxs-lookup"><span data-stu-id="95d77-133">If you don't connect a different email service account, emails that are sent from Attract will use the default Microsoft-branded email service account.</span></span>

## <a name="configure-email-template-settings"></a><span data-ttu-id="95d77-134">Konfigurere innstillinger for e-postmal</span><span class="sxs-lookup"><span data-stu-id="95d77-134">Configure email template settings</span></span>

<span data-ttu-id="95d77-135">Du kan laste opp et bilde av firmaets logo og annen informasjon som en varemerket topptekst for e-postmeldingene.</span><span class="sxs-lookup"><span data-stu-id="95d77-135">You can upload an image of your company's logo and other information as a branded header for your emails.</span></span> <span data-ttu-id="95d77-136">Du kan også ha koblinger til personvernpolicy og vilkår for bruk i bunntekst i e-post.</span><span class="sxs-lookup"><span data-stu-id="95d77-136">You can also provide links to your privacy policy and terms of use in email footers.</span></span>

> [!NOTE]
> <span data-ttu-id="95d77-137">Du må overholde alle gjeldende lover i landet eller området ditt samt landet eller området som styrer e-postmottakeren.</span><span class="sxs-lookup"><span data-stu-id="95d77-137">You must comply with all applicable laws of your country or region, and also the country or region that governs the email recipient.</span></span> <span data-ttu-id="95d77-138">Disse lovene omfatter forskrifter for søppelpost.</span><span class="sxs-lookup"><span data-stu-id="95d77-138">These laws include anti-spam regulations.</span></span>

1. <span data-ttu-id="95d77-139">Velg **Innstillinger** (tannhjulsikonet i øvre høyre hjørne), og velg deretter **Administrasjonssenter**.</span><span class="sxs-lookup"><span data-stu-id="95d77-139">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="95d77-140">Under **Innstillinger for e-postmal** i fanen **postinnstillinger** drar du bildet du vil bruke som topptekst i e-postmeldinger, til bildeboksen, eller du klikker i bildeboksen for å bla gjennom etter filen.</span><span class="sxs-lookup"><span data-stu-id="95d77-140">On the **Email settings** tab, under **Email template settings**, drag the image that you want to use as your email header into the image box, or click in the image box to browse for the file.</span></span> <span data-ttu-id="95d77-141">Hvis du vil erstatte et eksisterende bilde, må du først velge **Fjern** ved siden av det.</span><span class="sxs-lookup"><span data-stu-id="95d77-141">To replace an existing image, you must first select **Remove** next to it.</span></span> <span data-ttu-id="95d77-142">Bildet må være en JPEG-, JPG-, PNG- eller SVG-fil.</span><span class="sxs-lookup"><span data-stu-id="95d77-142">The image must be a JPEG, JPG, PNG, or SVG file.</span></span> <span data-ttu-id="95d77-143">Den anbefalte størrelsen for bilder er mellom 25 og 800 piksler bredt og mellom 25 og 150 piksler høyt.</span><span class="sxs-lookup"><span data-stu-id="95d77-143">The recommended size for images is between 25 and 800 pixels wide, and between 25 and 150 pixels high.</span></span> <span data-ttu-id="95d77-144">Den maksimale filstørrelsen for toppteksten er 1 megabyte (MB).</span><span class="sxs-lookup"><span data-stu-id="95d77-144">The maximum file size for the header is 1 megabyte (MB).</span></span>

    ![Legge til et bilde for firmaets topptekst i e-postmeldinger](./media/attract-admin-email-header.png)

3. <span data-ttu-id="95d77-146">Under **Din personvernerklæring for kommunikasjon** kan du oppgi en kobling til firmaets personvernpolicy.</span><span class="sxs-lookup"><span data-stu-id="95d77-146">Under **Your Privacy policy for communications**, provide a link to your company's privacy policy.</span></span> <span data-ttu-id="95d77-147">Under **Dine vilkår og betingelser for kommunikasjon** kan du angi en kobling til firmaets vilkår for bruk.</span><span class="sxs-lookup"><span data-stu-id="95d77-147">Under **Your Terms and conditions for communication**, provide a link to your company's terms of use.</span></span>

    ![Legge til koblinger i firmaets personvernpolicy og vilkår for bruk for bunnteksten i e-postmeldinger](./media/attract-admin-email-footer.png)

4. <span data-ttu-id="95d77-149">Velg **Lagre** for å lagre innstillingene for e-postmal.</span><span class="sxs-lookup"><span data-stu-id="95d77-149">Select **Save** to save your email template settings.</span></span>
