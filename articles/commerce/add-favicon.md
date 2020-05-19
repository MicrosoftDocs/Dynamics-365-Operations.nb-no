---
title: Legge til et favorittikon
description: Dette emnet forklarer hvordan du legger til et favorittikon på området.
author: bicyclingfool
manager: annbe
ms.date: 04/27/2020
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2d95e8b799c3b89418657342868e0ec7e94a86f9
ms.sourcegitcommit: ce79fb570e299a26a644e29da7ceb5a57a1374e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2020
ms.locfileid: "3295086"
---
# <a name="add-a-favicon"></a><span data-ttu-id="09b09-103">Legge til et favorittikon</span><span class="sxs-lookup"><span data-stu-id="09b09-103">Add a favicon</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="09b09-104">Dette emnet forklarer hvordan du legger til et favorittikon på området.</span><span class="sxs-lookup"><span data-stu-id="09b09-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="09b09-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="09b09-105">Overview</span></span>

<span data-ttu-id="09b09-106">Et favorittikon er en liten grafikkfil som vises i en webleserkategori, i adressefeltet, i leserloggen og i bokmerker eller favoritter, blant andre steder.</span><span class="sxs-lookup"><span data-stu-id="09b09-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="09b09-107">Vi anbefaler at du legger til et favorittikon på området, fordi det representerer og forsterker et merke, og bidrar til å identifisere området fra andre områder som kundene besøker.</span><span class="sxs-lookup"><span data-stu-id="09b09-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="09b09-108">Selv om du kan legge til flere favorittikoner av forskjellige størrelser og filtyper på området, viser dette emnet hvordan du legger til ett enkelt favorittikon.</span><span class="sxs-lookup"><span data-stu-id="09b09-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="09b09-109">Den samme prosessen og lokasjonen brukes imidlertid til å legge til flere favorittikoner.</span><span class="sxs-lookup"><span data-stu-id="09b09-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="09b09-110">Laste opp et favorittikon til aktivasamlingen på området</span><span class="sxs-lookup"><span data-stu-id="09b09-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="09b09-111">Følg denne fremgangsmåten for å laste opp et favorittikon til områdets aktivasamling.</span><span class="sxs-lookup"><span data-stu-id="09b09-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="09b09-112">Velg **Mediebibliotek** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="09b09-112">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="09b09-113">Velg **Last opp \> Last opp medieelementer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="09b09-113">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="09b09-114">I filutforskervinduet blar du til favorittikonfilen du vil laste opp, velger den og velger deretter **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="09b09-114">In the File Explorer window, browse to the favicon image file that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="09b09-115">I dialogboksen **Last opp medieelement** angir du nødvendig tittel og alt-tekst.</span><span class="sxs-lookup"><span data-stu-id="09b09-115">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="09b09-116">Hvis du vil publisere bilder like etter opplastingen, merker du av for **Publiser medieelementer etter opplasting**.</span><span class="sxs-lookup"><span data-stu-id="09b09-116">If you want to publish the image immediately after upload, select the **Publish media items after upload** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="09b09-117">Hvis du ikke merker av for **Publiser medieelementer etter opplasting**, må du gå tilbake til siden **Medieelementer** og manuelt publisere favorittikonet senere.</span><span class="sxs-lookup"><span data-stu-id="09b09-117">If you don't select the **Publish media items after upload** check box, you must return to **Media items** page and manually publish the favicon later.</span></span>

1. <span data-ttu-id="09b09-118">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="09b09-118">Select **OK**.</span></span>
1. <span data-ttu-id="09b09-119">I egenskapsruten til høyre kopierer du den offentlige URL-adressen til favorittikonet.</span><span class="sxs-lookup"><span data-stu-id="09b09-119">In the property pane on the right, copy the public URL of the favicon.</span></span> <span data-ttu-id="09b09-120">Du skal bruke denne URL-adressen senere.</span><span class="sxs-lookup"><span data-stu-id="09b09-120">You will use this URL later.</span></span>

## <a name="create-the-html-for-your-favicon"></a><span data-ttu-id="09b09-121">Opprette HTML for favorittikonet ditt</span><span class="sxs-lookup"><span data-stu-id="09b09-121">Create the HTML for your favicon</span></span>

<span data-ttu-id="09b09-122">Hvis du vil opprette HTML-koden for favorittikonet, bruker du følgende HTML-streng.</span><span class="sxs-lookup"><span data-stu-id="09b09-122">To create the HTML for the favicon, use the following HTML string.</span></span> <span data-ttu-id="09b09-123">For **href**-attributtet erstatter du **Public\_URL\_for\_your\_favicon** med den offentlige URL-adressen du kopierte tidligere.</span><span class="sxs-lookup"><span data-stu-id="09b09-123">For the **href** attribute, replace **Public\_URL\_for\_your\_favicon** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-page-fragment-that-contains-a-metatag-for-your-favicon"></a><span data-ttu-id="09b09-124">Opprette et sidefragment som inneholder en metakode for favorittikon</span><span class="sxs-lookup"><span data-stu-id="09b09-124">Create a page fragment that contains a metatag for your favicon</span></span>

<span data-ttu-id="09b09-125">For å opprette et sidefragment som inneholder en metakode for favorittikon, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="09b09-125">To create a page fragment that contains a metatag for your favicon, follow these steps.</span></span>

1. <span data-ttu-id="09b09-126">Gå til **Sidefragmenter**, og velg **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="09b09-126">Go to **Page fragments**, and select **New**.</span></span>
1. <span data-ttu-id="09b09-127">I dialogboksen **Nytt sidefragment** velger du **Metakoder** som modulen som sidefragmentet er basert på.</span><span class="sxs-lookup"><span data-stu-id="09b09-127">In the **New Page Fragment** dialog box, select **Metatags** as the module that the page fragment is based on.</span></span>
1. <span data-ttu-id="09b09-128">Angi et navn på sideoppsettet, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="09b09-128">Enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="09b09-129">Velg det underordnede **Standard metakoder** i fragmenthierarkitreet.</span><span class="sxs-lookup"><span data-stu-id="09b09-129">In the fragment hierarchy tree, select the **Default metatags** child.</span></span>
1. <span data-ttu-id="09b09-130">I ruten til høyre under **Metakoder** velger du **Legg til**, og deretter skriver du inn HTML-strengen du opprettet tidligere for favorittikonet.</span><span class="sxs-lookup"><span data-stu-id="09b09-130">In the right pane, under **Meta Tags**, select **Add**, and then enter the HTML string that you created earlier for the favicon.</span></span> 
1. <span data-ttu-id="09b09-131">Velg **Fullfør redigering**, og velg deretter **Publiser** for å publisere sidefragmentet.</span><span class="sxs-lookup"><span data-stu-id="09b09-131">Select **Finish editing**, and then select **Publish** to publish the page fragment.</span></span>

## <a name="add-the-metatag-page-fragment-to-the-html-head-section-of-your-pages"></a><span data-ttu-id="09b09-132">Legge til metakodesidefragmentet i HTML-hodedelen på sidene</span><span class="sxs-lookup"><span data-stu-id="09b09-132">Add the metatag page fragment to the HTML head section of your pages</span></span>

<span data-ttu-id="09b09-133">For å legge til metakodesidefragmentet i HTML-**hode**-delen på sidene følger du trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="09b09-133">To add the metatag page fragment to the HTML **head** section of your pages, follow these steps.</span></span>

1. <span data-ttu-id="09b09-134">Gå til **Maler**, og åpne malen for sidene du vil legge til favorittikonet ditt, og velg deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="09b09-134">Go to **Templates**, open the template for the pages that you want to add your favicon to, and then select **Edit**.</span></span>
1. <span data-ttu-id="09b09-135">I malhierarkitreet velger du ellipser (**...**)-knappen til høyre for **HTML-hode**-beholderen, og deretter velger du **Legg til sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="09b09-135">In the template hierarchy tree, select the ellipsis (**...**) button to the right of the **HTML head** container, and then select **Add page fragment**.</span></span>
1. <span data-ttu-id="09b09-136">I dialogboksen **Velg sidefragment** velger du metakodesidefragmentet du opprettet tidligere, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="09b09-136">In the **Select Page Fragment** dialog box, select the metatag page fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="09b09-137">Velg **Fullfør redigering**, og velg deretter **Publiser** for å publisere malen.</span><span class="sxs-lookup"><span data-stu-id="09b09-137">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>

> [!NOTE]
> <span data-ttu-id="09b09-138">Hvis området bruker mer enn én mal, må du legge til metakodesidefragmentet i alle.</span><span class="sxs-lookup"><span data-stu-id="09b09-138">If your site uses more than one template, you must add the metatags page fragment to all of them.</span></span>

<span data-ttu-id="09b09-139">Når du forhåndsviser sider som er basert på malen som du la til metakodesidefragmentet i, kan du nå se favorittikonet i leserkategorien.</span><span class="sxs-lookup"><span data-stu-id="09b09-139">When you preview pages that are based on the template that you added the metatags page fragment to, you should now see the favicon on the browser tab.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="09b09-140">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="09b09-140">Additional resources</span></span>

[<span data-ttu-id="09b09-141">Legge til en logo</span><span class="sxs-lookup"><span data-stu-id="09b09-141">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="09b09-142">Velge et områdetema</span><span class="sxs-lookup"><span data-stu-id="09b09-142">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="09b09-143">Arbeide med CSS-overstyringsfiler</span><span class="sxs-lookup"><span data-stu-id="09b09-143">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="09b09-144">Legge til en velkomstmelding</span><span class="sxs-lookup"><span data-stu-id="09b09-144">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="09b09-145">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="09b09-145">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="09b09-146">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="09b09-146">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="09b09-147">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="09b09-147">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

