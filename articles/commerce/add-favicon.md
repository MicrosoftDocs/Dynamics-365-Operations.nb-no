---
title: Legge til et favorittikon
description: Dette emnet forklarer hvordan du legger til et favorittikon på området.
author: bicyclingfool
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f249348fac526fc7814045b1b1b71c898430c0f2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980437"
---
# <a name="add-a-favicon"></a><span data-ttu-id="0fbf5-103">Legge til et favorittikon</span><span class="sxs-lookup"><span data-stu-id="0fbf5-103">Add a favicon</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0fbf5-104">Dette emnet forklarer hvordan du legger til et favorittikon på området.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="0fbf5-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="0fbf5-105">Overview</span></span>

<span data-ttu-id="0fbf5-106">Et favorittikon er en liten grafikkfil som vises i en webleserkategori, i adressefeltet, i leserloggen og i bokmerker eller favoritter, blant andre steder.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="0fbf5-107">Vi anbefaler at du legger til et favorittikon på området, fordi det representerer og forsterker et merke, og bidrar til å identifisere området fra andre områder som kundene besøker.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="0fbf5-108">Selv om du kan legge til flere favorittikoner av forskjellige størrelser og filtyper på området, viser dette emnet hvordan du legger til ett enkelt favorittikon.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="0fbf5-109">Den samme prosessen og lokasjonen brukes imidlertid til å legge til flere favorittikoner.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="0fbf5-110">Laste opp et favorittikon til aktivasamlingen på området</span><span class="sxs-lookup"><span data-stu-id="0fbf5-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="0fbf5-111">Følg denne fremgangsmåten for å laste opp et favorittikon til områdets aktivasamling.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="0fbf5-112">Velg **Mediebibliotek** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-112">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="0fbf5-113">Velg **Last opp \> Last opp medieelementer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-113">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="0fbf5-114">I filutforskervinduet blar du til favorittikonfilen du vil laste opp, velger den og velger deretter **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-114">In the File Explorer window, browse to the favicon image file that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="0fbf5-115">I dialogboksen **Last opp medieelement** angir du nødvendig tittel og alt-tekst.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-115">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="0fbf5-116">Hvis du vil publisere bilder like etter opplastingen, merker du av for **Publiser medieelementer etter opplasting**.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-116">If you want to publish the image immediately after upload, select the **Publish media items after upload** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0fbf5-117">Hvis du ikke merker av for **Publiser medieelementer etter opplasting**, må du gå tilbake til siden **Medieelementer** og manuelt publisere favorittikonet senere.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-117">If you don't select the **Publish media items after upload** check box, you must return to **Media items** page and manually publish the favicon later.</span></span>

1. <span data-ttu-id="0fbf5-118">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-118">Select **OK**.</span></span>
1. <span data-ttu-id="0fbf5-119">I egenskapsruten til høyre kopierer du den offentlige URL-adressen til favorittikonet.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-119">In the property pane on the right, copy the public URL of the favicon.</span></span> <span data-ttu-id="0fbf5-120">Du skal bruke denne URL-adressen senere.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-120">You will use this URL later.</span></span>

## <a name="create-the-html-for-your-favicon"></a><span data-ttu-id="0fbf5-121">Opprette HTML for favorittikonet ditt</span><span class="sxs-lookup"><span data-stu-id="0fbf5-121">Create the HTML for your favicon</span></span>

<span data-ttu-id="0fbf5-122">Hvis du vil opprette HTML-koden for favorittikonet, bruker du følgende HTML-streng.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-122">To create the HTML for the favicon, use the following HTML string.</span></span> <span data-ttu-id="0fbf5-123">For **href**-attributtet erstatter du **Public\_URL\_for\_your\_favicon** med den offentlige URL-adressen du kopierte tidligere.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-123">For the **href** attribute, replace **Public\_URL\_for\_your\_favicon** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a><span data-ttu-id="0fbf5-124">Opprette et fragment som inneholder en metakode for favorittikon</span><span class="sxs-lookup"><span data-stu-id="0fbf5-124">Create a fragment that contains a metatag for your favicon</span></span>

<span data-ttu-id="0fbf5-125">For å opprette et fragment som inneholder en metakode for favorittikon, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-125">To create a fragment that contains a metatag for your favicon, follow these steps.</span></span>

1. <span data-ttu-id="0fbf5-126">Gå til **Fragmenter**, og velg **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-126">Go to **Fragments**, and select **New**.</span></span>
1. <span data-ttu-id="0fbf5-127">I dialogboksen **Nytt fragment** velger du **Metakoder** som modulen som fragmentet er basert på.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-127">In the **New fragment** dialog box, select **Metatags** as the module that the fragment is based on.</span></span>
1. <span data-ttu-id="0fbf5-128">Angi et navn på fragmentet, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-128">Enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="0fbf5-129">Velg det underordnede **Standard metakoder** i fragmenthierarkitreet.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-129">In the fragment hierarchy tree, select the **Default metatags** child.</span></span>
1. <span data-ttu-id="0fbf5-130">I ruten til høyre under **Metakoder** velger du **Legg til**, og deretter skriver du inn HTML-strengen du opprettet tidligere for favorittikonet.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-130">In the right pane, under **Meta Tags**, select **Add**, and then enter the HTML string that you created earlier for the favicon.</span></span> 
1. <span data-ttu-id="0fbf5-131">Velg **Fullfør redigering**, og velg deretter **Publiser** for å publisere fragmentet.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-131">Select **Finish editing**, and then select **Publish** to publish the fragment.</span></span>

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a><span data-ttu-id="0fbf5-132">Legge til metakodefragmentet i HTML-hodedelen på sidene</span><span class="sxs-lookup"><span data-stu-id="0fbf5-132">Add the metatag fragment to the HTML head section of your pages</span></span>

<span data-ttu-id="0fbf5-133">For å legge til metakodefragmentet i delen HTML-**hode** på sidene følger du trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-133">To add the metatag fragment to the HTML **head** section of your pages, follow these steps.</span></span>

1. <span data-ttu-id="0fbf5-134">Gå til **Maler**, og åpne malen for sidene du vil legge til favorittikonet ditt, og velg deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-134">Go to **Templates**, open the template for the pages that you want to add your favicon to, and then select **Edit**.</span></span>
1. <span data-ttu-id="0fbf5-135">I malhierarkitreet velger du ellipser (**...**)-knappen til høyre for **HTML-hode**-beholderen, og deretter velger du **Legg til fragment**.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-135">In the template hierarchy tree, select the ellipsis (**...**) button to the right of the **HTML head** container, and then select **Add fragment**.</span></span>
1. <span data-ttu-id="0fbf5-136">I dialogboksen **Velg fragment** velger du metakodefragmentet du opprettet tidligere, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-136">In the **Select fragment** dialog box, select the metatag fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="0fbf5-137">Velg **Fullfør redigering**, og velg deretter **Publiser** for å publisere malen.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-137">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>

> [!NOTE]
> <span data-ttu-id="0fbf5-138">Hvis området bruker mer enn én mal, må du legge til metakodefragmentet i alle.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-138">If your site uses more than one template, you must add the metatags fragment to all of them.</span></span>

<span data-ttu-id="0fbf5-139">Når du forhåndsviser sider som er basert på malen som du la til metakodefragmentet i, kan du nå se favorittikonet i leserkategorien.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-139">When you preview pages that are based on the template that you added the metatags fragment to, you should now see the favicon on the browser tab.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0fbf5-140">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0fbf5-140">Additional resources</span></span>

[<span data-ttu-id="0fbf5-141">Legge til en logo</span><span class="sxs-lookup"><span data-stu-id="0fbf5-141">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="0fbf5-142">Velge et områdetema</span><span class="sxs-lookup"><span data-stu-id="0fbf5-142">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="0fbf5-143">Arbeide med CSS-overstyringsfiler</span><span class="sxs-lookup"><span data-stu-id="0fbf5-143">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="0fbf5-144">Legge til en velkomstmelding</span><span class="sxs-lookup"><span data-stu-id="0fbf5-144">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="0fbf5-145">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="0fbf5-145">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="0fbf5-146">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="0fbf5-146">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="0fbf5-147">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="0fbf5-147">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

