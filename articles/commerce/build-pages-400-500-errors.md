---
title: Bygge egendefinerte svarsider for 4xx/5xx-statuskodefeil
description: Dette emnet beskriver hvordan du bygger egendefinerte svarsider for 4xx- og 5xx-statuskodefeil ved hjelp av redigeringsverktøyene i Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b35b3c07b1edd41e6a3763c0001529e125e4636
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799659"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="78199-103">Bygge egendefinerte svarsider for 4xx/5xx-statuskodefeil</span><span class="sxs-lookup"><span data-stu-id="78199-103">Build custom response pages for 4xx/5xx status code errors</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="78199-104">Dette emnet beskriver hvordan du bygger egendefinerte svarsider for 4xx- og 5xx-statuskodefeil ved hjelp av redigeringsverktøyene i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="78199-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="78199-105">Hvis en forespørsel ikke lykkes, utsteder serveren svar på HTTP-statuskodefeil.</span><span class="sxs-lookup"><span data-stu-id="78199-105">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="78199-106">Statuskoden 404 registreres og returneres hvis en side ikke blir funnet, og 500 statuskoden fanges opp og returneres hvis det oppstår en serverfeil.</span><span class="sxs-lookup"><span data-stu-id="78199-106">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="78199-107">I Dynamics 365 Commerce kan programbrukere bygge egendefinerte svarsider for statuskodefeil som vises for brukere for disse statuskodefeilsvarene.</span><span class="sxs-lookup"><span data-stu-id="78199-107">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="78199-108">Bygge en svarside for statuskodefeil</span><span class="sxs-lookup"><span data-stu-id="78199-108">Build a status code error response page</span></span>

<span data-ttu-id="78199-109">Følg denne fremgangsmåten for å begynne å bygge en svarside for statuskodefeil.</span><span class="sxs-lookup"><span data-stu-id="78199-109">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="78199-110">I den foretrukne webleseren logger du på Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="78199-110">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="78199-111">Velg området du vil bygge en svarside for 4xx/5xx-statuskodefeil for.</span><span class="sxs-lookup"><span data-stu-id="78199-111">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="78199-112">Bygge malen</span><span class="sxs-lookup"><span data-stu-id="78199-112">Build the template</span></span>

<span data-ttu-id="78199-113">Følg denne fremgangsmåten for å bygge malen for svarsiden for statuskodefeil.</span><span class="sxs-lookup"><span data-stu-id="78199-113">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="78199-114">Gå til **Maler**.</span><span class="sxs-lookup"><span data-stu-id="78199-114">Go to **Templates**.</span></span>
1. <span data-ttu-id="78199-115">Velg **Ny** for å opprette en sidemal.</span><span class="sxs-lookup"><span data-stu-id="78199-115">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="78199-116">I dialogboksen **Ny mal**, under **Malnavn**, angir du et navn for den nye malen, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="78199-116">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="78199-117">Bygg malen på grunnlag av strukturen du vil at svarsiden for statuskodefeil skal ha.</span><span class="sxs-lookup"><span data-stu-id="78199-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="78199-118">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="78199-118">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="78199-119">Bygge svarsiden for statuskodefeil</span><span class="sxs-lookup"><span data-stu-id="78199-119">Build the status code error response page</span></span>

<span data-ttu-id="78199-120">Følg denne fremgangsmåten for å bygge svarsiden for statuskodefeil.</span><span class="sxs-lookup"><span data-stu-id="78199-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="78199-121">Gå til **Sider**.</span><span class="sxs-lookup"><span data-stu-id="78199-121">Go to **Pages**.</span></span>
1. <span data-ttu-id="78199-122">Velg **Ny** for å opprette en side.</span><span class="sxs-lookup"><span data-stu-id="78199-122">Select **New** to create a page.</span></span>
1. <span data-ttu-id="78199-123">Velg en mal i dialogboksen **Velg en mal**, og skriv deretter inn et navn for svarsiden for statuskodefeil under **Sidenavn**.</span><span class="sxs-lookup"><span data-stu-id="78199-123">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="78199-124">La feltet **URL-adresse for side** være tomt.</span><span class="sxs-lookup"><span data-stu-id="78199-124">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="78199-125">Bygg siden.</span><span class="sxs-lookup"><span data-stu-id="78199-125">Build the page.</span></span>
1. <span data-ttu-id="78199-126">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="78199-126">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="78199-127">Du kan opprette separate svarsider for statuskodefeil for 4xx- og 5xx-statuskodefeil.</span><span class="sxs-lookup"><span data-stu-id="78199-127">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="78199-128">Du kan også bruke den samme generelle svarsiden statuskodefeil for begge feilkategorier.</span><span class="sxs-lookup"><span data-stu-id="78199-128">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="78199-129">Definere en omadressering for svarsiden for statuskodefeil</span><span class="sxs-lookup"><span data-stu-id="78199-129">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="78199-130">Følg denne fremgangsmåten for å opprette en omadressering for svarsiden for statuskodefeil.</span><span class="sxs-lookup"><span data-stu-id="78199-130">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="78199-131">Gå til **URL-adresser \> Ny \> Nytt alias**, og velg svarsiden for statuskodefil som du bygde tidligere.</span><span class="sxs-lookup"><span data-stu-id="78199-131">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="78199-132">I feltet **Alias** angir du **default-4xx** eller **default-5xx**, avhengig av hvilken svarside for statuskodefeil du definerer en omadressering for.</span><span class="sxs-lookup"><span data-stu-id="78199-132">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="78199-133">Disse aliasene må publiseres.</span><span class="sxs-lookup"><span data-stu-id="78199-133">These aliases must be published.</span></span> <span data-ttu-id="78199-134">Hvis ikke fungerer ikke omadresseringen.</span><span class="sxs-lookup"><span data-stu-id="78199-134">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="78199-135">Velg **OK** for å aktivere koblingen.</span><span class="sxs-lookup"><span data-stu-id="78199-135">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="78199-136">Hvis du bruker én svarside for statuskodefeil for begge feilkategoriene, gjentar du denne fremgangsmåten for å koble et alias for den andre feilkategorien til den samme siden.</span><span class="sxs-lookup"><span data-stu-id="78199-136">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="78199-137">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="78199-137">Additional resources</span></span>

[<span data-ttu-id="78199-138">Arbeide med maler</span><span class="sxs-lookup"><span data-stu-id="78199-138">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="78199-139">Legg til en ny områdeside</span><span class="sxs-lookup"><span data-stu-id="78199-139">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="78199-140">Opprette en URL-adresse for side</span><span class="sxs-lookup"><span data-stu-id="78199-140">Create a page URL</span></span>](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
