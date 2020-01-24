---
title: Legge til en opphavsrettserklæring
description: Dette emnet beskriver hvordan du legger til opphavsrettserklæring på e-handelsområdet.
author: psimolin
manager: AnnBe
ms.date: 12/12/2019
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
ms.openlocfilehash: 58c2949057ef777f706d12cee2dd3341d1a3b7e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914583"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="f239c-103">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="f239c-103">Add a copyright notice</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f239c-104">Dette emnet beskriver hvordan du legger til opphavsrettserklæring på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="f239c-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f239c-105">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="f239c-105">Prerequisites</span></span>

<span data-ttu-id="f239c-106">Før du kan legge til en opphavsrettserklæring på området, må du ha følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="f239c-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="f239c-107">En mal som inneholder et delt bunntekstfragment.</span><span class="sxs-lookup"><span data-stu-id="f239c-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="f239c-108">En side som bruker denne malen.</span><span class="sxs-lookup"><span data-stu-id="f239c-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="f239c-109">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="f239c-109">Add a copyright notice</span></span>

<span data-ttu-id="f239c-110">Hvis du vil legge til en opphavsrettserklæring nederst på hver side som bruker en bestemt mal, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="f239c-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="f239c-111">Gå til **Fragmenter**, og velg **Nytt sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="f239c-111">Go to **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="f239c-112">I dialogboksen velger du **Bunntekst**-modulen, og deretter gir du navn til fragmentet.</span><span class="sxs-lookup"><span data-stu-id="f239c-112">In the dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="f239c-113">Skriv for eksempel inn **Bunntekst-opphavsrettserklæring**.</span><span class="sxs-lookup"><span data-stu-id="f239c-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="f239c-114">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f239c-114">Select **OK**.</span></span>
1. <span data-ttu-id="f239c-115">I navigasjonsruten velger du ellipseknappen (**...**) ved siden av **Bunntekst**, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="f239c-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="f239c-116">I dialogboksen velger du **Bunntekstkategori**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="f239c-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="f239c-117">I navigasjonsruten velger du ellipseknappen ved siden av **Bunntekstkategori**, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="f239c-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="f239c-118">I dialoigboksen velger du **Innholdsrikt blokkelement**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f239c-118">In the dialog box, select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="f239c-119">I navigasjonsruten velger du **Innholdsrikt blokkelement**.</span><span class="sxs-lookup"><span data-stu-id="f239c-119">In the navigation pane, select **Content rich block item**.</span></span>
1. <span data-ttu-id="f239c-120">Legg til melding om opphavsrett i feltet **Avsnitt** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="f239c-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="f239c-121">Skriv for eksempel inn **(C) Fabrikam 2019**.</span><span class="sxs-lookup"><span data-stu-id="f239c-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="f239c-122">Velg **Lagre**, velg **Sjekk inn**, og velg deretter **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="f239c-122">Select **Save**, select **Check In**, and then select **Publish**.</span></span>
1. <span data-ttu-id="f239c-123">Gå til **Maler**, velg malen, og velg deretter **Sjekk ut**.</span><span class="sxs-lookup"><span data-stu-id="f239c-123">Go to **Templates**, select the template, and then select **Check Out**.</span></span>
1. <span data-ttu-id="f239c-124">Under **Sideoppsett** utvider du **Brødtekst**, og deretter utvider du **Standardside**.</span><span class="sxs-lookup"><span data-stu-id="f239c-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="f239c-125">Velg ellipseknappen ved siden av **Bunntekstspor**, og velg deretter **Legg til fragment**.</span><span class="sxs-lookup"><span data-stu-id="f239c-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="f239c-126">Velg fragmentet du opprettet tidligere, og velg deretter **Velg**.</span><span class="sxs-lookup"><span data-stu-id="f239c-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="f239c-127">Sjekk inn malen, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="f239c-127">Check in the template, and publish it.</span></span>

<span data-ttu-id="f239c-128">Bunnteksten som inneholder opphavsrettserklæringen, vises automatisk nederst på alle sider som bruker den valgte malen.</span><span class="sxs-lookup"><span data-stu-id="f239c-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f239c-129">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f239c-129">Additional resources</span></span>

[<span data-ttu-id="f239c-130">Legge til en logo</span><span class="sxs-lookup"><span data-stu-id="f239c-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="f239c-131">Velge et områdetema</span><span class="sxs-lookup"><span data-stu-id="f239c-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="f239c-132">Arbeide med CSS-overstyringsfiler</span><span class="sxs-lookup"><span data-stu-id="f239c-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="f239c-133">Legge til et favorittikon</span><span class="sxs-lookup"><span data-stu-id="f239c-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="f239c-134">Legge til en velkomstmelding</span><span class="sxs-lookup"><span data-stu-id="f239c-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="f239c-135">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="f239c-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="f239c-136">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="f239c-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

