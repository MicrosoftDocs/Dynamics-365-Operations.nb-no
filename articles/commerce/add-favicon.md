---
title: Legge til et favorittikon
description: Dette emnet forklarer hvordan du legger til et favorittikon på området.
author: bicyclingfool
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 58cb6c592351a96876532ef53d5d477ff93fafa1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696997"
---
# <a name="add-a-favicon"></a><span data-ttu-id="660f4-103">Legge til et favorittikon</span><span class="sxs-lookup"><span data-stu-id="660f4-103">Add a favicon</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="660f4-104">Dette emnet forklarer hvordan du legger til et favorittikon på området.</span><span class="sxs-lookup"><span data-stu-id="660f4-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="660f4-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="660f4-105">Overview</span></span>

<span data-ttu-id="660f4-106">Et favorittikon er en liten grafikkfil som vises i en webleserkategori, i adressefeltet, i leserloggen og i bokmerker eller favoritter, blant andre steder.</span><span class="sxs-lookup"><span data-stu-id="660f4-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="660f4-107">Vi anbefaler at du legger til et favorittikon på området, fordi det representerer og forsterker et merke, og bidrar til å identifisere området fra andre områder som kundene besøker.</span><span class="sxs-lookup"><span data-stu-id="660f4-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="660f4-108">Selv om du kan legge til flere favorittikoner av forskjellige størrelser og filtyper på området, viser dette emnet hvordan du legger til ett enkelt favorittikon.</span><span class="sxs-lookup"><span data-stu-id="660f4-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="660f4-109">Den samme prosessen og lokasjonen brukes imidlertid til å legge til flere favorittikoner.</span><span class="sxs-lookup"><span data-stu-id="660f4-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="660f4-110">Laste opp et favorittikon til aktivasamlingen på området</span><span class="sxs-lookup"><span data-stu-id="660f4-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="660f4-111">Følg denne fremgangsmåten for å laste opp et favorittikon til områdets aktivasamling.</span><span class="sxs-lookup"><span data-stu-id="660f4-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="660f4-112">Gå til **Aktiva \> Last opp \> Last opp aktiva**.</span><span class="sxs-lookup"><span data-stu-id="660f4-112">Go to **Assets \> Upload \> Upload assets**.</span></span>
1. <span data-ttu-id="660f4-113">Finn og velg favorittikon på det lokale filsystemet.</span><span class="sxs-lookup"><span data-stu-id="660f4-113">Find and select the favicon on your local file system.</span></span>
1. <span data-ttu-id="660f4-114">Skriv inn en tittel, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="660f4-114">Enter a title, and then select **OK**.</span></span> 
1. <span data-ttu-id="660f4-115">I egenskapsruten til høyre kopierer du den offentlige URL-adressen til favorittikonet.</span><span class="sxs-lookup"><span data-stu-id="660f4-115">In the property pane on the right, copy the public URL of the favicon.</span></span>

> [!NOTE]
> <span data-ttu-id="660f4-116">Hvis du ikke velger alternativet **Publiser aktiva etter opplasting**, må du gå tilbake til siden **Aktiva** og manuelt publisere favorittikonet senere.</span><span class="sxs-lookup"><span data-stu-id="660f4-116">If you don't select the **Publish assets after upload** option, you must return to **Assets** page and manually publish the favicon later.</span></span>

## <a name="create-the-html-for-the-favicon"></a><span data-ttu-id="660f4-117">Opprette HTML for favorittikonet</span><span class="sxs-lookup"><span data-stu-id="660f4-117">Create the HTML for the favicon</span></span>

<span data-ttu-id="660f4-118">Hvis du vil opprette HTML-koden for favorittikonet, bruker du følgende HTML-kodesnutt.</span><span class="sxs-lookup"><span data-stu-id="660f4-118">To create the HTML for the favicon, use the following HTML snippet.</span></span> <span data-ttu-id="660f4-119">For **href**-attributtet erstatter du **"Public\_URL\_for\_your\_favicon"** " med den offentlige URL-adressen du kopierte tidligere.</span><span class="sxs-lookup"><span data-stu-id="660f4-119">For the **href** attribute, replace **"Public\_URL\_for\_your\_favicon"** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a><span data-ttu-id="660f4-120">Legge HTML-koden til favorittikonet i \<hode\>-elementet på sidene</span><span class="sxs-lookup"><span data-stu-id="660f4-120">Add the HTML for the favicon to the \<head\> element of your pages</span></span>

<span data-ttu-id="660f4-121">Hvis du vil legge til et favorittikon på området, bruker du den samme fremgangsmåte som brukes til å legge til en hvilken som helst type HTML eller skript i elementet **\<hode\>** på områdesidene.</span><span class="sxs-lookup"><span data-stu-id="660f4-121">To add a favicon to your site, use the same procedure that is used to add any type of HTML or script to the **\<head\>** element of your site pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="660f4-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="660f4-122">Additional resources</span></span>

[<span data-ttu-id="660f4-123">Legge til en logo</span><span class="sxs-lookup"><span data-stu-id="660f4-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="660f4-124">Velge et områdetema</span><span class="sxs-lookup"><span data-stu-id="660f4-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="660f4-125">Legge til en velkomstmelding</span><span class="sxs-lookup"><span data-stu-id="660f4-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="660f4-126">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="660f4-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="660f4-127">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="660f4-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="660f4-128">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="660f4-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

