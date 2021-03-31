---
title: Bygge egendefinerte svarsider for 4xx/5xx-statuskodefeil
description: Dette emnet beskriver hvordan du bygger egendefinerte svarsider for 4xx- og 5xx-statuskodefeil ved hjelp av redigeringsverktøyene i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ee2f74581ded6020d075377f931c465d7c89f9e5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211111"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="0384f-103">Bygge egendefinerte svarsider for 4xx/5xx-statuskodefeil</span><span class="sxs-lookup"><span data-stu-id="0384f-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0384f-104">Dette emnet beskriver hvordan du bygger egendefinerte svarsider for 4xx- og 5xx-statuskodefeil ved hjelp av redigeringsverktøyene i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0384f-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0384f-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="0384f-105">Overview</span></span>

<span data-ttu-id="0384f-106">Hvis en forespørsel ikke lykkes, utsteder serveren svar på HTTP-statuskodefeil.</span><span class="sxs-lookup"><span data-stu-id="0384f-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="0384f-107">Statuskoden 404 registreres og returneres hvis en side ikke blir funnet, og 500 statuskoden fanges opp og returneres hvis det oppstår en serverfeil.</span><span class="sxs-lookup"><span data-stu-id="0384f-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="0384f-108">I Dynamics 365 Commerce kan programbrukere bygge egendefinerte svarsider for statuskodefeil som vises for brukere for disse statuskodefeilsvarene.</span><span class="sxs-lookup"><span data-stu-id="0384f-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="0384f-109">Bygge en svarside for statuskodefeil</span><span class="sxs-lookup"><span data-stu-id="0384f-109">Build a status code error response page</span></span>

<span data-ttu-id="0384f-110">Følg denne fremgangsmåten for å begynne å bygge en svarside for statuskodefeil.</span><span class="sxs-lookup"><span data-stu-id="0384f-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="0384f-111">I den foretrukne webleseren logger du på Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0384f-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="0384f-112">Velg området du vil bygge en svarside for 4xx/5xx-statuskodefeil for.</span><span class="sxs-lookup"><span data-stu-id="0384f-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="0384f-113">Bygge malen</span><span class="sxs-lookup"><span data-stu-id="0384f-113">Build the template</span></span>

<span data-ttu-id="0384f-114">Følg denne fremgangsmåten for å bygge malen for svarsiden for statuskodefeil.</span><span class="sxs-lookup"><span data-stu-id="0384f-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="0384f-115">Gå til **Maler**.</span><span class="sxs-lookup"><span data-stu-id="0384f-115">Go to **Templates**.</span></span>
1. <span data-ttu-id="0384f-116">Velg **Ny** for å opprette en sidemal.</span><span class="sxs-lookup"><span data-stu-id="0384f-116">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="0384f-117">I dialogboksen **Ny mal**, under **Malnavn**, angir du et navn for den nye malen, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="0384f-117">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="0384f-118">Bygg malen på grunnlag av strukturen du vil at svarsiden for statuskodefeil skal ha.</span><span class="sxs-lookup"><span data-stu-id="0384f-118">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="0384f-119">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="0384f-119">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="0384f-120">Bygge svarsiden for statuskodefeil</span><span class="sxs-lookup"><span data-stu-id="0384f-120">Build the status code error response page</span></span>

<span data-ttu-id="0384f-121">Følg denne fremgangsmåten for å bygge svarsiden for statuskodefeil.</span><span class="sxs-lookup"><span data-stu-id="0384f-121">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="0384f-122">Gå til **Sider**.</span><span class="sxs-lookup"><span data-stu-id="0384f-122">Go to **Pages**.</span></span>
1. <span data-ttu-id="0384f-123">Velg **Ny** for å opprette en side.</span><span class="sxs-lookup"><span data-stu-id="0384f-123">Select **New** to create a page.</span></span>
1. <span data-ttu-id="0384f-124">Velg en mal i dialogboksen **Velg en mal**, og skriv deretter inn et navn for svarsiden for statuskodefeil under **Sidenavn**.</span><span class="sxs-lookup"><span data-stu-id="0384f-124">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="0384f-125">La feltet **URL-adresse for side** være tomt.</span><span class="sxs-lookup"><span data-stu-id="0384f-125">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="0384f-126">Bygg siden.</span><span class="sxs-lookup"><span data-stu-id="0384f-126">Build the page.</span></span>
1. <span data-ttu-id="0384f-127">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="0384f-127">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="0384f-128">Du kan opprette separate svarsider for statuskodefeil for 4xx- og 5xx-statuskodefeil.</span><span class="sxs-lookup"><span data-stu-id="0384f-128">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="0384f-129">Du kan også bruke den samme generelle svarsiden statuskodefeil for begge feilkategorier.</span><span class="sxs-lookup"><span data-stu-id="0384f-129">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="0384f-130">Definere en omadressering for svarsiden for statuskodefeil</span><span class="sxs-lookup"><span data-stu-id="0384f-130">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="0384f-131">Følg denne fremgangsmåten for å opprette en omadressering for svarsiden for statuskodefeil.</span><span class="sxs-lookup"><span data-stu-id="0384f-131">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="0384f-132">Gå til **URL-adresser \> Ny \> Nytt alias**, og velg svarsiden for statuskodefil som du bygde tidligere.</span><span class="sxs-lookup"><span data-stu-id="0384f-132">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="0384f-133">I feltet **Alias** angir du **default-4xx** eller **default-5xx**, avhengig av hvilken svarside for statuskodefeil du definerer en omadressering for.</span><span class="sxs-lookup"><span data-stu-id="0384f-133">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="0384f-134">Disse aliasene må publiseres.</span><span class="sxs-lookup"><span data-stu-id="0384f-134">These aliases must be published.</span></span> <span data-ttu-id="0384f-135">Hvis ikke fungerer ikke omadresseringen.</span><span class="sxs-lookup"><span data-stu-id="0384f-135">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="0384f-136">Velg **OK** for å aktivere koblingen.</span><span class="sxs-lookup"><span data-stu-id="0384f-136">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="0384f-137">Hvis du bruker én svarside for statuskodefeil for begge feilkategoriene, gjentar du denne fremgangsmåten for å koble et alias for den andre feilkategorien til den samme siden.</span><span class="sxs-lookup"><span data-stu-id="0384f-137">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0384f-138">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0384f-138">Additional resources</span></span>

[<span data-ttu-id="0384f-139">Arbeide med maler</span><span class="sxs-lookup"><span data-stu-id="0384f-139">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="0384f-140">Legg til en ny områdeside</span><span class="sxs-lookup"><span data-stu-id="0384f-140">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="0384f-141">Opprette en URL-adresse for side</span><span class="sxs-lookup"><span data-stu-id="0384f-141">Create a page URL</span></span>](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]