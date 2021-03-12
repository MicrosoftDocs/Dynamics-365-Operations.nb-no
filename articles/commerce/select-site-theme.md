---
title: Velge et områdetema
description: Dette emnet beskriver hvordan du angir eller endrer områdets tema i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: 66fcff9fa18d3c98e022ef91d15903fbba8b6b61
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982416"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="d1d30-103">Velge et områdetema</span><span class="sxs-lookup"><span data-stu-id="d1d30-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d1d30-104">Dette emnet beskriver hvordan du angir eller endrer områdets tema i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d1d30-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d1d30-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="d1d30-105">Overview</span></span>

<span data-ttu-id="d1d30-106">Området og stilen for et oppsett (for eksempel skrifter, størrelser og farger) defineres av temaet du velger, og gjelder for området.</span><span class="sxs-lookup"><span data-stu-id="d1d30-106">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="d1d30-107">Et tema opprettes og distribueres av en utvikler i firmaet.</span><span class="sxs-lookup"><span data-stu-id="d1d30-107">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="d1d30-108">Hvis du vil ha en oversikt over temaer, se [Temaoversikt](e-commerce-extensibility/theming.md).</span><span class="sxs-lookup"><span data-stu-id="d1d30-108">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="d1d30-109">Hvis du vil ha mer informasjon om hvordan du oppretter og distribuerer temaer, kan du se [Opprette et nytt tema](e-commerce-extensibility/create-theme.md).</span><span class="sxs-lookup"><span data-stu-id="d1d30-109">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="d1d30-110">Når du oppretter et område for første gang, bruker det som standard et tema kalt **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="d1d30-110">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="d1d30-111">Dette standardtemaet leveres som en del av Commerce-modulbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="d1d30-111">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="d1d30-112">Når du har distribuert flere temaer for området, kan du konfigurere området slik at det bruker en av dem i stedet.</span><span class="sxs-lookup"><span data-stu-id="d1d30-112">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="d1d30-113">Velge områdetema</span><span class="sxs-lookup"><span data-stu-id="d1d30-113">Select the site theme</span></span>

<span data-ttu-id="d1d30-114">Følg denne fremgangsmåten for å velge temaet som skal brukes på området.</span><span class="sxs-lookup"><span data-stu-id="d1d30-114">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="d1d30-115">Gå til området i redigeringsmiljøet for området.</span><span class="sxs-lookup"><span data-stu-id="d1d30-115">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="d1d30-116">Gå til **Områdebehandling** \> **Utvidelsesmulighet**.</span><span class="sxs-lookup"><span data-stu-id="d1d30-116">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="d1d30-117">Under **Tema** velger du et tema på rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="d1d30-117">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="d1d30-118">Hvis du vil bruke det valgte temaet på området, velger du **Lagre og publiser**.</span><span class="sxs-lookup"><span data-stu-id="d1d30-118">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="d1d30-119">Temaet du velger, publiseres på området så snart du velger **Lagre og publiser** på siden **Utvidelse**.</span><span class="sxs-lookup"><span data-stu-id="d1d30-119">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="d1d30-120">Hvis du vil forhåndsvise et tema på området før du bruker det, kan du bruke utviklings- eller sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="d1d30-120">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d1d30-121">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d1d30-121">Additional resources</span></span>

[<span data-ttu-id="d1d30-122">Legge til en logo</span><span class="sxs-lookup"><span data-stu-id="d1d30-122">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="d1d30-123">Arbeide med CSS-overstyringsfiler</span><span class="sxs-lookup"><span data-stu-id="d1d30-123">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="d1d30-124">Legge til et favorittikon</span><span class="sxs-lookup"><span data-stu-id="d1d30-124">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="d1d30-125">Legge til en velkomstmelding</span><span class="sxs-lookup"><span data-stu-id="d1d30-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="d1d30-126">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="d1d30-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="d1d30-127">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="d1d30-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="d1d30-128">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="d1d30-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="d1d30-129">Temaoversikt</span><span class="sxs-lookup"><span data-stu-id="d1d30-129">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="d1d30-130">Opprett et nytt tema</span><span class="sxs-lookup"><span data-stu-id="d1d30-130">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)

