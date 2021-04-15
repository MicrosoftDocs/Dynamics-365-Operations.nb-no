---
title: Laste opp og betjene statiske filer
description: Dette emnet beskriver hvordan du laster opp en statisk fil til områdebyggeren for Microsoft Dynamics 365 Commerce, og hvordan du oppretter en egendefinert nettadresse og et filnavn som kan brukes til å be om denne filen.
author: StuHarg
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d5f092042b3dda65b041ab2f25f7319dd8e158d1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801391"
---
# <a name="upload-and-serve-static-files"></a><span data-ttu-id="d45e6-103">Laste opp og betjene statiske filer</span><span class="sxs-lookup"><span data-stu-id="d45e6-103">Upload and serve static files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d45e6-104">Dette emnet beskriver hvordan du laster opp en statisk fil til områdebyggeren for Microsoft Dynamics 365 Commerce, og hvordan du oppretter en egendefinert nettadresse og et filnavn som kan brukes til å be om denne filen.</span><span class="sxs-lookup"><span data-stu-id="d45e6-104">This topic describes how to upload a static file into Microsoft Dynamics 365 Commerce site builder, and how to create a custom URL and file name that can be used to request that file.</span></span>

<span data-ttu-id="d45e6-105">Noen tredjepartskontakter krever at en fil blir lagret og betjent fra e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="d45e6-105">Some third-party connectors require that a file be hosted and served from the e-commerce site.</span></span> <span data-ttu-id="d45e6-106">Disse koblingene forventer at filen blir returnert ved forespørsler til en bestemt URL-bane for tilbakeringing og et filnavn.</span><span class="sxs-lookup"><span data-stu-id="d45e6-106">These connectors expect that the file will be returned by requests to a specific callback URL path and file name.</span></span> <span data-ttu-id="d45e6-107">Dette emnet beskriver derfor hvordan du laster opp og betjener en statisk fil med en brukerdefinert URL-adresse og et filnavn på et Dynamics 365 Commerce-e-handelsområde.</span><span class="sxs-lookup"><span data-stu-id="d45e6-107">Therefore, this topic explains how to upload and serve a static file that has a user-definable URL and file name on a Dynamics 365 Commerce e-commerce site.</span></span>

## <a name="create-a-site-url-that-returns-a-static-file"></a><span data-ttu-id="d45e6-108">Opprett en URL-adresse for område som returnerer en statisk fil</span><span class="sxs-lookup"><span data-stu-id="d45e6-108">Create a site URL that returns a static file</span></span>

<span data-ttu-id="d45e6-109">Følg denne fremgangsmåten for å opprette en URL-adresse for område som returnerer en statisk fil i Commerce-områdebygger.</span><span class="sxs-lookup"><span data-stu-id="d45e6-109">To create a site URL that returns a static file in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d45e6-110">Gå til mediebiblioteket for området, og last opp filen som skal betjenes av forespørsler til URL-adressen du vil definere.</span><span class="sxs-lookup"><span data-stu-id="d45e6-110">Go to your site's Media library, and upload the file that should be served by requests to the URL that you will define.</span></span> <span data-ttu-id="d45e6-111">Hvis du allerede har lastet opp filen, kan du hoppe over dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="d45e6-111">If you've already uploaded the file, you can skip this step.</span></span>
1. <span data-ttu-id="d45e6-112">Gå til **URL-adresser** for området.</span><span class="sxs-lookup"><span data-stu-id="d45e6-112">Go to **URLs** for your site.</span></span>
1. <span data-ttu-id="d45e6-113">Velg **Ny \> Ny URL-adresse**.</span><span class="sxs-lookup"><span data-stu-id="d45e6-113">Select **New \> New URL**.</span></span>
1. <span data-ttu-id="d45e6-114">Velg **Mediebibliotekressurs** i dialogboksen **Ny URL-adresse**.</span><span class="sxs-lookup"><span data-stu-id="d45e6-114">In the **New URL** dialog box, select **Media library asset**.</span></span>
1. <span data-ttu-id="d45e6-115">I feltet **URL-bane** angir du URL-banen.</span><span class="sxs-lookup"><span data-stu-id="d45e6-115">In the **URL path** field, enter the URL path.</span></span> <span data-ttu-id="d45e6-116">Inkluder filnavnet i banen.</span><span class="sxs-lookup"><span data-stu-id="d45e6-116">Include the file name in the path.</span></span>
1. <span data-ttu-id="d45e6-117">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="d45e6-117">Select **Next**.</span></span> <span data-ttu-id="d45e6-118">Mediebiblioteket åpnes, og alle medieressursene for **dokumenttypen** som er lastet opp, vises.</span><span class="sxs-lookup"><span data-stu-id="d45e6-118">The Media library is opened and shows all media assets of the **document** type that have been uploaded.</span></span>
1. <span data-ttu-id="d45e6-119">Velg filen som skal betjenes for forespørsler til URL-adressen du definerte i trinn 5.</span><span class="sxs-lookup"><span data-stu-id="d45e6-119">Select the file that should be served for requests to the URL that you defined in step 5.</span></span>
1. <span data-ttu-id="d45e6-120">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="d45e6-120">Select **Save**.</span></span>

<span data-ttu-id="d45e6-121">På dette tidspunktet er URL-adressen du opprettet, i utkasttilstand.</span><span class="sxs-lookup"><span data-stu-id="d45e6-121">At this point, the URL that you created is in a draft state.</span></span> <span data-ttu-id="d45e6-122">Filen som URL-adressen peker til, returneres ikke før du publiserer URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="d45e6-122">The file that the URL points to won't be returned until you publish the URL.</span></span> <span data-ttu-id="d45e6-123">Før du publiserer URL-adressen, kan du validere at den returnerer de riktige dataene.</span><span class="sxs-lookup"><span data-stu-id="d45e6-123">Before you publish the URL, you can validate that it returns the correct data.</span></span>

## <a name="validate-and-publish-a-url"></a><span data-ttu-id="d45e6-124">Validere og publiser en URL</span><span class="sxs-lookup"><span data-stu-id="d45e6-124">Validate and publish a URL</span></span>

<span data-ttu-id="d45e6-125">Hvis du vil validere en URL før du publiserer, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="d45e6-125">To validate an URL before you publish it, follow these steps.</span></span>

1. <span data-ttu-id="d45e6-126">Gå til **URL-adresser** for området, og velg URL-adressen du vil forhåndsvise.</span><span class="sxs-lookup"><span data-stu-id="d45e6-126">Go to **URLs** for your site, and select the URL to preview.</span></span>
2. <span data-ttu-id="d45e6-127">I egenskaperruten til høyre, under **Rediger**-knappen velger du den riktige URL-koblingen.</span><span class="sxs-lookup"><span data-stu-id="d45e6-127">In the properties pane on the right, below the **Edit** button, select the correct URL link.</span></span> <span data-ttu-id="d45e6-128">Et nytt nettleservindu åpnes, og du får en 404-feilmelding.</span><span class="sxs-lookup"><span data-stu-id="d45e6-128">A new browser window is opened, and you should receive a 404 error.</span></span>
3. <span data-ttu-id="d45e6-129">Legg til **?preview=inprogress**-spørringsstrengen til URL-adressen (for eksempel `https://yoursite.com/callback.html?preview=inprogress`), og last inn siden på nytt.</span><span class="sxs-lookup"><span data-stu-id="d45e6-129">Append the **?preview=inprogress** query string to the URL (for example, `https://yoursite.com/callback.html?preview=inprogress`), and reload the page.</span></span> <span data-ttu-id="d45e6-130">Filen du lastet opp til mediebiblioteket, skal returneres i svaret.</span><span class="sxs-lookup"><span data-stu-id="d45e6-130">The file that you uploaded to the Media library should be returned in the response.</span></span>

<span data-ttu-id="d45e6-131">Når du har validert URL-adressen, kan du publisere den.</span><span class="sxs-lookup"><span data-stu-id="d45e6-131">After you've validated the URL, you can publish it.</span></span>

1. <span data-ttu-id="d45e6-132">Gå til **URL-adresser** for området, og velg URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="d45e6-132">Go to **URLs** for your site, and select the URL.</span></span>
2. <span data-ttu-id="d45e6-133">Velg **Publiser** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="d45e6-133">Select **Publish** on the command bar.</span></span>

## <a name="update-the-file-that-a-url-points-to"></a><span data-ttu-id="d45e6-134">Oppdater filen som en URL-adresse peker til</span><span class="sxs-lookup"><span data-stu-id="d45e6-134">Update the file that a URL points to</span></span>

<span data-ttu-id="d45e6-135">Når en URL-adresse er publisert, kan du oppdatere den slik at den peker til en annen fil.</span><span class="sxs-lookup"><span data-stu-id="d45e6-135">After a URL is published, you can update it so that it points to a different file.</span></span> <span data-ttu-id="d45e6-136">Du kan også oppdatere URL-adressen slik at den peker mot en annen ressurstype, som beskrevet i neste del.</span><span class="sxs-lookup"><span data-stu-id="d45e6-136">Alternatively, you can update the URL so that it points to a different the type of resource, as described in the next section.</span></span> <span data-ttu-id="d45e6-137">Du kan for eksempel peke URL-adressen til en intern side eller en omadressering.</span><span class="sxs-lookup"><span data-stu-id="d45e6-137">For example, you can point the URL to an internal page or a redirect.</span></span>

<span data-ttu-id="d45e6-138">Følg denne fremgangsmåten for å oppdatere filen som en URL-adresse peker til.</span><span class="sxs-lookup"><span data-stu-id="d45e6-138">To update the file that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="d45e6-139">Gå til **URL-adresser** for området, og velg URL-adressen du vil oppdatere.</span><span class="sxs-lookup"><span data-stu-id="d45e6-139">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="d45e6-140">Velg **Rediger** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="d45e6-140">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="d45e6-141">Under **URL-tilordning** velger du **Trinn 2**-boksen og deretter velger du et nytt dokument fra mediebiblioteket.</span><span class="sxs-lookup"><span data-stu-id="d45e6-141">Under **URL assignment**, select the **Step 2** box, and then select a new document from the Media library.</span></span>
1. <span data-ttu-id="d45e6-142">Velg **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="d45e6-142">Select **Apply**.</span></span>

## <a name="update-the-asset-type-that-a-url-points-to"></a><span data-ttu-id="d45e6-143">Oppdater ressurstypen som en URL-adresse peker til</span><span class="sxs-lookup"><span data-stu-id="d45e6-143">Update the asset type that a URL points to</span></span>

<span data-ttu-id="d45e6-144">Du kan også oppdatere en URL-adresse slik at den peker på en annen aktivumtype (ressurs), for eksempel en intern side eller en omadressering.</span><span class="sxs-lookup"><span data-stu-id="d45e6-144">You can also update a URL so that it points to a different type of asset (resource), such as an internal page or a redirect.</span></span>

<span data-ttu-id="d45e6-145">Følg denne aktivumtypen for å oppdatere filen som en URL-adresse peker til.</span><span class="sxs-lookup"><span data-stu-id="d45e6-145">To update the asset type that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="d45e6-146">Gå til **URL-adresser** for området, og velg URL-adressen du vil oppdatere.</span><span class="sxs-lookup"><span data-stu-id="d45e6-146">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="d45e6-147">Velg **Rediger** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="d45e6-147">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="d45e6-148">Under **URL-tilordning** under **Trinn 1** velger du en annen aktivumtype.</span><span class="sxs-lookup"><span data-stu-id="d45e6-148">Under **URL assignment**, under **Step 1**, select a different asset type.</span></span>
1. <span data-ttu-id="d45e6-149">Velg **Trinn 2**-boksen, og velg deretter den nye ressursen.</span><span class="sxs-lookup"><span data-stu-id="d45e6-149">Select the **Step 2** box, and then select the new asset.</span></span>
1. <span data-ttu-id="d45e6-150">Velg **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="d45e6-150">Select **Apply**.</span></span>

## <a name="change-the-url-path"></a><span data-ttu-id="d45e6-151">Endre URL-banen</span><span class="sxs-lookup"><span data-stu-id="d45e6-151">Change the URL path</span></span>

<span data-ttu-id="d45e6-152">Når en URL-adresse er opprettet, kan ikke banen endres.</span><span class="sxs-lookup"><span data-stu-id="d45e6-152">After a URL is created, its path can't be changed.</span></span> <span data-ttu-id="d45e6-153">Hvis du må endre URL-banen som betjener en fil eller en annen ressurstype, må du opprette en ny URL-adresse, tilordne den til den eksisterende filen eller en annen ressurs, og deretter oppheve publiseringen og slette den gamle URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="d45e6-153">If you must change the URL path that serves a file or any other type of resource, you have to create a new URL, map it to the existing file or other resource, and then unpublish and delete the old URL.</span></span>

<span data-ttu-id="d45e6-154">Hvis du vil endre URL-banen, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="d45e6-154">To change the URL path, follow these steps.</span></span>

1. <span data-ttu-id="d45e6-155">Hvis du vil opprette en ny URL-adresse og tilordne den til den eksisterende filen eller en annen ressurs, følger du instruksjonene i delen [Opprett en URL-adressen for område som returnerer en statisk fil](#create-a-site-url-that-returns-a-static-file) tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="d45e6-155">To create a new URL and map it to the existing file or another resource, follow the instructions in the [Create a site URL that returns a static file](#create-a-site-url-that-returns-a-static-file) section earlier in this topic.</span></span>
1. <span data-ttu-id="d45e6-156">Velg den nye URL-adressen, og velg **Publiser** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="d45e6-156">Select the new URL, and select **Publish** on the command bar.</span></span> <span data-ttu-id="d45e6-157">Den nye URL-adressen publiseres.</span><span class="sxs-lookup"><span data-stu-id="d45e6-157">The new URL is published.</span></span>
1. <span data-ttu-id="d45e6-158">Hvis du vil oppheve publiseringen av den gamle URL-adressen, merker du den og velger **Opphev publisering** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="d45e6-158">To unpublish the old URL, select it, and then select **Unpublish** on the command bar.</span></span> <span data-ttu-id="d45e6-159">Du kan nå slette den gamle URL-adressen hvis du vil det.</span><span class="sxs-lookup"><span data-stu-id="d45e6-159">You can now delete the old URL if you want.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d45e6-160">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d45e6-160">Additional resources</span></span>

[<span data-ttu-id="d45e6-161">Oversikt over behandling av digitale aktiva</span><span class="sxs-lookup"><span data-stu-id="d45e6-161">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="d45e6-162">Laste opp bilder</span><span class="sxs-lookup"><span data-stu-id="d45e6-162">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="d45e6-163">Laste opp videoer</span><span class="sxs-lookup"><span data-stu-id="d45e6-163">Upload videos</span></span>](dam-upload-video.md)

[<span data-ttu-id="d45e6-164">Laste opp andre filer enn bilder og videoer</span><span class="sxs-lookup"><span data-stu-id="d45e6-164">Upload files other than images and videos</span></span>](dam-upload-files.md)

[<span data-ttu-id="d45e6-165">Beskjære bilder</span><span class="sxs-lookup"><span data-stu-id="d45e6-165">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="d45e6-166">Tilpasse bildefokuspunkter</span><span class="sxs-lookup"><span data-stu-id="d45e6-166">Customize image focal points</span></span>](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]