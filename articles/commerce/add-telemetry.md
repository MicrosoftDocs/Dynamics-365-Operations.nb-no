---
title: Legge til skript kode i områdes ID-er for å støtte telemetri
description: Dette emnet beskriver hvordan du kan legge til skriptkode på klientsiden på områdesidene dine for å støtte innsamling av telemetri på klientsiden.
author: bicyclingfool
manager: annbe
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 79d0e11946f3c6f4704d3a726d33de0378eb53bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914545"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="4b613-103">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="4b613-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="4b613-104">Dette emnet beskriver hvordan du kan legge til skriptkode på klientsiden på områdesidene dine for å støtte innsamling av telemetri på klientsiden.</span><span class="sxs-lookup"><span data-stu-id="4b613-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="4b613-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="4b613-105">Overview</span></span>

<span data-ttu-id="4b613-106">Web Analytics er et viktig verktøy når du vil forstå hvordan kundene samhandler med området og tar avgjørelser som vil bidra til å optimalisere opplevelsen for maksimal konvertering.</span><span class="sxs-lookup"><span data-stu-id="4b613-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="4b613-107">Mange Web Analytics-pakker er tilgjengelige for å hjelpe deg med å oppnå disse målene, for eksempel Google Analytics, Clicky, Moz Analytics og KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="4b613-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="4b613-108">De fleste Web Analytics-pakker krever at du legger til skriptkode på klientsiden i **\<hode\>**-elementet på HTMLen for alle sidene på området.</span><span class="sxs-lookup"><span data-stu-id="4b613-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="4b613-109">Instruksjonene i dette emnet gjelder også for annen tilpasset funksjonalitet på klientsiden som Microsoft Dynamics 365 Commerce ikke tilbyr.</span><span class="sxs-lookup"><span data-stu-id="4b613-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="4b613-110">Opprette et gjenbrukbart fragment for skriptkoden</span><span class="sxs-lookup"><span data-stu-id="4b613-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="4b613-111">Når du har opprettet et fragment for skriptkoden, kan det brukes på nytt på alle sider på området.</span><span class="sxs-lookup"><span data-stu-id="4b613-111">After you create a fragment for your script code, it can be reused across all pages on your site.</span></span>

1. <span data-ttu-id="4b613-112">Gå til **Fragmenter \> Nytt sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="4b613-112">Go to **Fragments \> New page fragment**.</span></span>
2. <span data-ttu-id="4b613-113">Velg **Eksternt skript**, skriv inn et navn på fragmentet, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b613-113">Select **External Script**, enter a name for the fragment, and then select **OK**.</span></span>
3. <span data-ttu-id="4b613-114">I fragmenthierarkiet velger du den underordnede **skriptinnsetting**-modulen for fragmentet som du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="4b613-114">In the fragment hierarchy, select the **script injector** module child of the fragment that you just created.</span></span>
4. <span data-ttu-id="4b613-115">I egenskapsruten til høyre legger du til skriptet på klientsiden, og deretter angir du andre konfigurasjonsalternativer etter behov.</span><span class="sxs-lookup"><span data-stu-id="4b613-115">In the property pane on the right, add your client-side script, and set other configuration options as you require.</span></span>

## <a name="add-the-fragment-to-templates"></a><span data-ttu-id="4b613-116">Legge til fragmentet i maler</span><span class="sxs-lookup"><span data-stu-id="4b613-116">Add the fragment to templates</span></span>

1. <span data-ttu-id="4b613-117">Gå til **Maler**, og åpne malen for sidene du vil legge til skriptkoden i.</span><span class="sxs-lookup"><span data-stu-id="4b613-117">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
2. <span data-ttu-id="4b613-118">I venstre rute utvider du malhierarkiet slik at det viser **HTML-hode**-sporet.</span><span class="sxs-lookup"><span data-stu-id="4b613-118">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
3. <span data-ttu-id="4b613-119">Velg ellipseknappen (**...**) for **HTML-hode**-sporet, og velg deretter **Legg til fragment**.</span><span class="sxs-lookup"><span data-stu-id="4b613-119">Select the ellipsis button (**...**) for the **HTML Head** slot, and then select **Add fragment**.</span></span>
4. <span data-ttu-id="4b613-120">Velg fragmentet du opprettet for skriptkoden.</span><span class="sxs-lookup"><span data-stu-id="4b613-120">Select the fragment that you created for your script code.</span></span>
5. <span data-ttu-id="4b613-121">Lagre malen, og sjekk den inn.</span><span class="sxs-lookup"><span data-stu-id="4b613-121">Save the template, and check it in.</span></span>

> [!NOTE]
> <span data-ttu-id="4b613-122">Når du er ferdig, må du publisere fragmentet og malen.</span><span class="sxs-lookup"><span data-stu-id="4b613-122">After you've finished, you must publish the fragment and the master template.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="4b613-123">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4b613-123">Additional resources</span></span>

[<span data-ttu-id="4b613-124">Legge til en logo</span><span class="sxs-lookup"><span data-stu-id="4b613-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="4b613-125">Velge et områdetema</span><span class="sxs-lookup"><span data-stu-id="4b613-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="4b613-126">Arbeide med CSS-overstyringsfiler</span><span class="sxs-lookup"><span data-stu-id="4b613-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="4b613-127">Legge til et favorittikon</span><span class="sxs-lookup"><span data-stu-id="4b613-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="4b613-128">Legge til en velkomstmelding</span><span class="sxs-lookup"><span data-stu-id="4b613-128">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="4b613-129">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="4b613-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="4b613-130">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="4b613-130">Add languages to your site</span></span>](add-languages-to-site.md)

