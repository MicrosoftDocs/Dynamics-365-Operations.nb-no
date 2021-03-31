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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2ea04854636fdd0c2b3223bb19d5f06a19836151
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206373"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="11074-103">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="11074-103">Add a copyright notice</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="11074-104">Dette emnet beskriver hvordan du legger til opphavsrettserklæring på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="11074-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="11074-105">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="11074-105">Prerequisites</span></span>

<span data-ttu-id="11074-106">Før du kan legge til en opphavsrettserklæring på området, må du ha følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="11074-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="11074-107">En mal som inneholder et delt bunntekstfragment.</span><span class="sxs-lookup"><span data-stu-id="11074-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="11074-108">En side som bruker denne malen.</span><span class="sxs-lookup"><span data-stu-id="11074-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="11074-109">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="11074-109">Add a copyright notice</span></span>

<span data-ttu-id="11074-110">Hvis du vil legge til en opphavsrettserklæring nederst på hver side som bruker en bestemt mal, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="11074-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="11074-111">Gå til **Fragmenter**, og velg deretter **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="11074-111">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="11074-112">I dialogboksen **Nytt fragment** velger du **Bunntekst**-modulen, og gir fragmentet et navn.</span><span class="sxs-lookup"><span data-stu-id="11074-112">In the **New fragment** dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="11074-113">Skriv for eksempel inn **Bunntekst-opphavsrettserklæring**.</span><span class="sxs-lookup"><span data-stu-id="11074-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="11074-114">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="11074-114">Select **OK**.</span></span>
1. <span data-ttu-id="11074-115">I navigasjonsruten velger du ellipseknappen (**...**) ved siden av **Bunntekst**, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="11074-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="11074-116">I dialogboksen velger du **Bunntekstkategori**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="11074-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="11074-117">I navigasjonsruten velger du ellipseknappen ved siden av **Bunntekstkategori**, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="11074-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="11074-118">I dialogboksen velger du **Tekstblokk**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="11074-118">In the dialog box, select **Text block**, and then select **OK**.</span></span>
1. <span data-ttu-id="11074-119">I navigasjonsruten velger du **Tekstblokk**.</span><span class="sxs-lookup"><span data-stu-id="11074-119">In the navigation pane, select **Text block**.</span></span>
1. <span data-ttu-id="11074-120">Legg til melding om opphavsrett i feltet **Avsnitt** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="11074-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="11074-121">Skriv for eksempel inn **(C) Fabrikam 2019**.</span><span class="sxs-lookup"><span data-stu-id="11074-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="11074-122">Velg **Lagre**, velg **Fullfør redigering**, og velg deretter **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="11074-122">Select **Save**, select **Finish editing**, and then select **Publish**.</span></span>
1. <span data-ttu-id="11074-123">Gå til **Maler**, velg malen, og velg deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="11074-123">Go to **Templates**, select the template, and then select **Edit**.</span></span>
1. <span data-ttu-id="11074-124">Under **Sideoppsett** utvider du **Brødtekst**, og deretter utvider du **Standardside**.</span><span class="sxs-lookup"><span data-stu-id="11074-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="11074-125">Velg ellipseknappen ved siden av **Bunntekstspor**, og velg deretter **Legg til fragment**.</span><span class="sxs-lookup"><span data-stu-id="11074-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="11074-126">Velg fragmentet du opprettet tidligere, og velg deretter **Velg**.</span><span class="sxs-lookup"><span data-stu-id="11074-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="11074-127">Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="11074-127">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="11074-128">Bunnteksten som inneholder opphavsrettserklæringen, vises automatisk nederst på alle sider som bruker den valgte malen.</span><span class="sxs-lookup"><span data-stu-id="11074-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="11074-129">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="11074-129">Additional resources</span></span>

[<span data-ttu-id="11074-130">Legge til en logo</span><span class="sxs-lookup"><span data-stu-id="11074-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="11074-131">Velge et områdetema</span><span class="sxs-lookup"><span data-stu-id="11074-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="11074-132">Arbeide med CSS-overstyringsfiler</span><span class="sxs-lookup"><span data-stu-id="11074-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="11074-133">Legge til et favorittikon</span><span class="sxs-lookup"><span data-stu-id="11074-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="11074-134">Legge til en velkomstmelding</span><span class="sxs-lookup"><span data-stu-id="11074-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="11074-135">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="11074-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="11074-136">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="11074-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]