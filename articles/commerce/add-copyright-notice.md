---
title: Legge til en opphavsrettserklæring
description: Dette emnet beskriver hvordan du legger til opphavsrettserklæring på e-handelsområdet.
author: psimolin
manager: AnnBe
ms.date: 10/16/2020
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
ms.openlocfilehash: 838047cac694c65047332e146a7c43ee2ae0f401
ms.sourcegitcommit: 1a12b42cc17f004a981c716aed3da6cf538475a5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4414771"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="6c3fe-103">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="6c3fe-103">Add a copyright notice</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6c3fe-104">Dette emnet beskriver hvordan du legger til opphavsrettserklæring på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6c3fe-105">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="6c3fe-105">Prerequisites</span></span>

<span data-ttu-id="6c3fe-106">Før du kan legge til en opphavsrettserklæring på området, må du ha følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="6c3fe-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="6c3fe-107">En mal som inneholder et delt bunntekstfragment.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="6c3fe-108">En side som bruker denne malen.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="6c3fe-109">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="6c3fe-109">Add a copyright notice</span></span>

<span data-ttu-id="6c3fe-110">Hvis du vil legge til en opphavsrettserklæring nederst på hver side som bruker en bestemt mal, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="6c3fe-111">Gå til **Fragmenter**, og velg deretter **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-111">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="6c3fe-112">I dialogboksen **Nytt fragment** velger du **Bunntekst**-modulen, og gir fragmentet et navn.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-112">In the **New fragment** dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="6c3fe-113">Skriv for eksempel inn **Bunntekst-opphavsrettserklæring**.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="6c3fe-114">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-114">Select **OK**.</span></span>
1. <span data-ttu-id="6c3fe-115">I navigasjonsruten velger du ellipseknappen (**...**) ved siden av **Bunntekst**, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="6c3fe-116">I dialogboksen velger du **Bunntekstkategori**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="6c3fe-117">I navigasjonsruten velger du ellipseknappen ved siden av **Bunntekstkategori**, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="6c3fe-118">I dialogboksen velger du **Tekstblokk**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-118">In the dialog box, select **Text block**, and then select **OK**.</span></span>
1. <span data-ttu-id="6c3fe-119">I navigasjonsruten velger du **Tekstblokk**.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-119">In the navigation pane, select **Text block**.</span></span>
1. <span data-ttu-id="6c3fe-120">Legg til melding om opphavsrett i feltet **Avsnitt** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="6c3fe-121">Skriv for eksempel inn **(C) Fabrikam 2019**.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="6c3fe-122">Velg **Lagre**, velg **Fullfør redigering**, og velg deretter **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-122">Select **Save**, select **Finish editing**, and then select **Publish**.</span></span>
1. <span data-ttu-id="6c3fe-123">Gå til **Maler**, velg malen, og velg deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-123">Go to **Templates**, select the template, and then select **Edit**.</span></span>
1. <span data-ttu-id="6c3fe-124">Under **Sideoppsett** utvider du **Brødtekst**, og deretter utvider du **Standardside**.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="6c3fe-125">Velg ellipseknappen ved siden av **Bunntekstspor**, og velg deretter **Legg til fragment**.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="6c3fe-126">Velg fragmentet du opprettet tidligere, og velg deretter **Velg**.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="6c3fe-127">Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-127">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="6c3fe-128">Bunnteksten som inneholder opphavsrettserklæringen, vises automatisk nederst på alle sider som bruker den valgte malen.</span><span class="sxs-lookup"><span data-stu-id="6c3fe-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c3fe-129">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6c3fe-129">Additional resources</span></span>

[<span data-ttu-id="6c3fe-130">Legge til en logo</span><span class="sxs-lookup"><span data-stu-id="6c3fe-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="6c3fe-131">Velge et områdetema</span><span class="sxs-lookup"><span data-stu-id="6c3fe-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="6c3fe-132">Arbeide med CSS-overstyringsfiler</span><span class="sxs-lookup"><span data-stu-id="6c3fe-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="6c3fe-133">Legge til et favorittikon</span><span class="sxs-lookup"><span data-stu-id="6c3fe-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="6c3fe-134">Legge til en velkomstmelding</span><span class="sxs-lookup"><span data-stu-id="6c3fe-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="6c3fe-135">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="6c3fe-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="6c3fe-136">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="6c3fe-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

