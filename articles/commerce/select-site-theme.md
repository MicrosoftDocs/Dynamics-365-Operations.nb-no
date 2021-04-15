---
title: Velge et områdetema
description: Dette emnet beskriver hvordan du angir eller endrer områdets tema i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e11e2ffafa29dfe4ad7a4a8e4d14e9d7c74c31f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794073"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="90495-103">Velge et områdetema</span><span class="sxs-lookup"><span data-stu-id="90495-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="90495-104">Dette emnet beskriver hvordan du angir eller endrer områdets tema i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="90495-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="90495-105">Området og stilen for et oppsett (for eksempel skrifter, størrelser og farger) defineres av temaet du velger, og gjelder for området.</span><span class="sxs-lookup"><span data-stu-id="90495-105">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="90495-106">Et tema opprettes og distribueres av en utvikler i firmaet.</span><span class="sxs-lookup"><span data-stu-id="90495-106">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="90495-107">Hvis du vil ha en oversikt over temaer, se [Temaoversikt](e-commerce-extensibility/theming.md).</span><span class="sxs-lookup"><span data-stu-id="90495-107">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="90495-108">Hvis du vil ha mer informasjon om hvordan du oppretter og distribuerer temaer, kan du se [Opprette et nytt tema](e-commerce-extensibility/create-theme.md).</span><span class="sxs-lookup"><span data-stu-id="90495-108">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="90495-109">Når du oppretter et område for første gang, bruker det som standard et tema kalt **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="90495-109">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="90495-110">Dette standardtemaet leveres som en del av Commerce-modulbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="90495-110">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="90495-111">Når du har distribuert flere temaer for området, kan du konfigurere området slik at det bruker en av dem i stedet.</span><span class="sxs-lookup"><span data-stu-id="90495-111">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="90495-112">Velge områdetema</span><span class="sxs-lookup"><span data-stu-id="90495-112">Select the site theme</span></span>

<span data-ttu-id="90495-113">Følg denne fremgangsmåten for å velge temaet som skal brukes på området.</span><span class="sxs-lookup"><span data-stu-id="90495-113">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="90495-114">Gå til området i redigeringsmiljøet for området.</span><span class="sxs-lookup"><span data-stu-id="90495-114">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="90495-115">Gå til **Områdebehandling** \> **Utvidelsesmulighet**.</span><span class="sxs-lookup"><span data-stu-id="90495-115">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="90495-116">Under **Tema** velger du et tema på rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="90495-116">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="90495-117">Hvis du vil bruke det valgte temaet på området, velger du **Lagre og publiser**.</span><span class="sxs-lookup"><span data-stu-id="90495-117">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="90495-118">Temaet du velger, publiseres på området så snart du velger **Lagre og publiser** på siden **Utvidelse**.</span><span class="sxs-lookup"><span data-stu-id="90495-118">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="90495-119">Hvis du vil forhåndsvise et tema på området før du bruker det, kan du bruke utviklings- eller sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="90495-119">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="90495-120">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="90495-120">Additional resources</span></span>

[<span data-ttu-id="90495-121">Legge til en logo</span><span class="sxs-lookup"><span data-stu-id="90495-121">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="90495-122">Arbeide med CSS-overstyringsfiler</span><span class="sxs-lookup"><span data-stu-id="90495-122">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="90495-123">Legge til et favorittikon</span><span class="sxs-lookup"><span data-stu-id="90495-123">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="90495-124">Legge til en velkomstmelding</span><span class="sxs-lookup"><span data-stu-id="90495-124">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="90495-125">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="90495-125">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="90495-126">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="90495-126">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="90495-127">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="90495-127">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="90495-128">Temaoversikt</span><span class="sxs-lookup"><span data-stu-id="90495-128">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="90495-129">Opprett et nytt tema</span><span class="sxs-lookup"><span data-stu-id="90495-129">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
