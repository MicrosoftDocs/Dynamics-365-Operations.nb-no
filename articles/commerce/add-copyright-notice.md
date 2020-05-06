---
title: Legge til en opphavsrettserklæring
description: Dette emnet beskriver hvordan du legger til opphavsrettserklæring på e-handelsområdet.
author: psimolin
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a2ed52dbd19508e07fcced92a7fad831180b1d1d
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269596"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="0f17b-103">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="0f17b-103">Add a copyright notice</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0f17b-104">Dette emnet beskriver hvordan du legger til opphavsrettserklæring på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="0f17b-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0f17b-105">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="0f17b-105">Prerequisites</span></span>

<span data-ttu-id="0f17b-106">Før du kan legge til en opphavsrettserklæring på området, må du ha følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="0f17b-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="0f17b-107">En mal som inneholder et delt bunntekstfragment.</span><span class="sxs-lookup"><span data-stu-id="0f17b-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="0f17b-108">En side som bruker denne malen.</span><span class="sxs-lookup"><span data-stu-id="0f17b-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="0f17b-109">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="0f17b-109">Add a copyright notice</span></span>

<span data-ttu-id="0f17b-110">Hvis du vil legge til en opphavsrettserklæring nederst på hver side som bruker en bestemt mal, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="0f17b-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="0f17b-111">Gå til **Fragmenter**, og velg **Nytt sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="0f17b-111">Go to **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="0f17b-112">I dialogboksen velger du **Bunntekst**-modulen, og deretter gir du navn til fragmentet.</span><span class="sxs-lookup"><span data-stu-id="0f17b-112">In the dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="0f17b-113">Skriv for eksempel inn **Bunntekst-opphavsrettserklæring**.</span><span class="sxs-lookup"><span data-stu-id="0f17b-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="0f17b-114">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0f17b-114">Select **OK**.</span></span>
1. <span data-ttu-id="0f17b-115">I navigasjonsruten velger du ellipseknappen (**...**) ved siden av **Bunntekst**, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="0f17b-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="0f17b-116">I dialogboksen velger du **Bunntekstkategori**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="0f17b-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="0f17b-117">I navigasjonsruten velger du ellipseknappen ved siden av **Bunntekstkategori**, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="0f17b-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="0f17b-118">I dialogboksen velger du **Tekstblokk**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="0f17b-118">In the dialog box, select **Text block**, and then select **OK**.</span></span>
1. <span data-ttu-id="0f17b-119">I navigasjonsruten velger du **Tekstblokk**.</span><span class="sxs-lookup"><span data-stu-id="0f17b-119">In the navigation pane, select **Text block**.</span></span>
1. <span data-ttu-id="0f17b-120">Legg til melding om opphavsrett i feltet **Avsnitt** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="0f17b-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="0f17b-121">Skriv for eksempel inn **(C) Fabrikam 2019**.</span><span class="sxs-lookup"><span data-stu-id="0f17b-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="0f17b-122">Velg **Lagre**, velg **Fullfør redigering**, og velg deretter **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="0f17b-122">Select **Save**, select **Finish editing**, and then select **Publish**.</span></span>
1. <span data-ttu-id="0f17b-123">Gå til **Maler**, velg malen, og velg deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="0f17b-123">Go to **Templates**, select the template, and then select **Edit**.</span></span>
1. <span data-ttu-id="0f17b-124">Under **Sideoppsett** utvider du **Brødtekst**, og deretter utvider du **Standardside**.</span><span class="sxs-lookup"><span data-stu-id="0f17b-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="0f17b-125">Velg ellipseknappen ved siden av **Bunntekstspor**, og velg deretter **Legg til fragment**.</span><span class="sxs-lookup"><span data-stu-id="0f17b-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="0f17b-126">Velg fragmentet du opprettet tidligere, og velg deretter **Velg**.</span><span class="sxs-lookup"><span data-stu-id="0f17b-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="0f17b-127">Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="0f17b-127">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="0f17b-128">Bunnteksten som inneholder opphavsrettserklæringen, vises automatisk nederst på alle sider som bruker den valgte malen.</span><span class="sxs-lookup"><span data-stu-id="0f17b-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f17b-129">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0f17b-129">Additional resources</span></span>

[<span data-ttu-id="0f17b-130">Legge til en logo</span><span class="sxs-lookup"><span data-stu-id="0f17b-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="0f17b-131">Velge et områdetema</span><span class="sxs-lookup"><span data-stu-id="0f17b-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="0f17b-132">Arbeide med CSS-overstyringsfiler</span><span class="sxs-lookup"><span data-stu-id="0f17b-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="0f17b-133">Legge til et favorittikon</span><span class="sxs-lookup"><span data-stu-id="0f17b-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="0f17b-134">Legge til en velkomstmelding</span><span class="sxs-lookup"><span data-stu-id="0f17b-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="0f17b-135">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="0f17b-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="0f17b-136">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="0f17b-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

