---
title: Bygge egendefinerte svarsider for 4xx/5xx-statuskodefeil
description: Dette emnet beskriver hvordan du bygger egendefinerte svarsider for 4xx- og 5xx-statuskodefeil ved hjelp av redigeringsverktøyene i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4477a0a43971b5322c6acd6971cba2e79e2dc8c6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001147"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="703aa-103">Bygge egendefinerte svarsider for 4xx/5xx-statuskodefeil</span><span class="sxs-lookup"><span data-stu-id="703aa-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="703aa-104">Dette emnet beskriver hvordan du bygger egendefinerte svarsider for 4xx- og 5xx-statuskodefeil ved hjelp av redigeringsverktøyene i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="703aa-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="703aa-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="703aa-105">Overview</span></span>

<span data-ttu-id="703aa-106">Hvis en forespørsel ikke lykkes, utsteder serveren svar på HTTP-statuskodefeil.</span><span class="sxs-lookup"><span data-stu-id="703aa-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="703aa-107">Statuskoden 404 registreres og returneres hvis en side ikke blir funnet, og 500 statuskoden fanges opp og returneres hvis det oppstår en serverfeil.</span><span class="sxs-lookup"><span data-stu-id="703aa-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="703aa-108">I Dynamics 365 Commerce kan programbrukere bygge egendefinerte svarsider for statuskodefeil som vises for brukere for disse statuskodefeilsvarene.</span><span class="sxs-lookup"><span data-stu-id="703aa-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="703aa-109">Bygge en svarside for statuskodefeil</span><span class="sxs-lookup"><span data-stu-id="703aa-109">Build a status code error response page</span></span>

<span data-ttu-id="703aa-110">Følg denne fremgangsmåten for å begynne å bygge en svarside for statuskodefeil.</span><span class="sxs-lookup"><span data-stu-id="703aa-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="703aa-111">I den foretrukne webleseren logger du på Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="703aa-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="703aa-112">Velg området du vil bygge en svarside for 4xx/5xx-statuskodefeil for.</span><span class="sxs-lookup"><span data-stu-id="703aa-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="703aa-113">Bygge malen</span><span class="sxs-lookup"><span data-stu-id="703aa-113">Build the template</span></span>

<span data-ttu-id="703aa-114">Følg denne fremgangsmåten for å bygge malen for svarsiden for statuskodefeil.</span><span class="sxs-lookup"><span data-stu-id="703aa-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="703aa-115">Gå til **Maler \> Ny mal**.</span><span class="sxs-lookup"><span data-stu-id="703aa-115">Go to **Templates \> New template**.</span></span>
1. <span data-ttu-id="703aa-116">Gi den nye malen et navn.</span><span class="sxs-lookup"><span data-stu-id="703aa-116">Name the new template.</span></span>
1. <span data-ttu-id="703aa-117">Bygg malen på grunnlag av strukturen du vil at svarsiden for statuskodefeil skal ha.</span><span class="sxs-lookup"><span data-stu-id="703aa-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="703aa-118">Sjekk inn malen, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="703aa-118">Check the template in, and publish it.</span></span>

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="703aa-119">Bygge svarsiden for statuskodefeil</span><span class="sxs-lookup"><span data-stu-id="703aa-119">Build the status code error response page</span></span>

<span data-ttu-id="703aa-120">Følg denne fremgangsmåten for å bygge svarsiden for statuskodefeil.</span><span class="sxs-lookup"><span data-stu-id="703aa-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="703aa-121">Gå til **Sider \> Ny side**.</span><span class="sxs-lookup"><span data-stu-id="703aa-121">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="703aa-122">Gi navn til svarsiden for statuskodefeil, men **ikke** angi **URL**-feltet.</span><span class="sxs-lookup"><span data-stu-id="703aa-122">Name the status code error response page, but do **not** set the **URL** field.</span></span>
1. <span data-ttu-id="703aa-123">Bygg siden.</span><span class="sxs-lookup"><span data-stu-id="703aa-123">Build the page.</span></span>
1. <span data-ttu-id="703aa-124">Sjekk inn siden, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="703aa-124">Check the page in, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="703aa-125">Du kan opprette separate svarsider for statuskodefeil for 4xx- og 5xx-statuskodefeil.</span><span class="sxs-lookup"><span data-stu-id="703aa-125">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="703aa-126">Du kan også bruke den samme generelle svarsiden statuskodefeil for begge feilkategorier.</span><span class="sxs-lookup"><span data-stu-id="703aa-126">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="703aa-127">Definere en omadressering for svarsiden for statuskodefeil</span><span class="sxs-lookup"><span data-stu-id="703aa-127">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="703aa-128">Følg denne fremgangsmåten for å opprette en omadressering for svarsiden for statuskodefeil.</span><span class="sxs-lookup"><span data-stu-id="703aa-128">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="703aa-129">Gå til **URL-adresser \> Ny \> Nytt alias**, og velg svarsiden for statuskodefil som du bygde tidligere.</span><span class="sxs-lookup"><span data-stu-id="703aa-129">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="703aa-130">I feltet **Alias** angir du **default-4xx** eller **default-5xx**, avhengig av hvilken svarside for statuskodefeil du definerer en omadressering for.</span><span class="sxs-lookup"><span data-stu-id="703aa-130">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="703aa-131">Disse aliasene må publiseres.</span><span class="sxs-lookup"><span data-stu-id="703aa-131">These aliases must be published.</span></span> <span data-ttu-id="703aa-132">Hvis ikke fungerer ikke omadresseringen.</span><span class="sxs-lookup"><span data-stu-id="703aa-132">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="703aa-133">Velg **OK** for å aktivere koblingen.</span><span class="sxs-lookup"><span data-stu-id="703aa-133">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="703aa-134">Hvis du bruker én svarside for statuskodefeil for begge feilkategoriene, gjentar du denne fremgangsmåten for å koble et alias for den andre feilkategorien til den samme siden.</span><span class="sxs-lookup"><span data-stu-id="703aa-134">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="703aa-135">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="703aa-135">Additional resources</span></span>

[<span data-ttu-id="703aa-136">Arbeide med maler</span><span class="sxs-lookup"><span data-stu-id="703aa-136">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="703aa-137">Legg til en ny områdeside</span><span class="sxs-lookup"><span data-stu-id="703aa-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="703aa-138">Opprette en URL-adresse for side</span><span class="sxs-lookup"><span data-stu-id="703aa-138">Create a page URL</span></span>](create-page-url.md)
