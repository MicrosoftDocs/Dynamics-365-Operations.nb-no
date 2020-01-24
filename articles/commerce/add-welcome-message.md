---
title: Legge til en velkomstmelding
description: Dette emnet beskriver hvordan du legger til en velkomstmelding i Microsoft Dynamics 365 Commerce-webområdet.
author: psimolin
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4e9deeeaf491b77700ba0833e429f05d376a4392
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914522"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="f4507-103">Legge til en velkomstmelding</span><span class="sxs-lookup"><span data-stu-id="f4507-103">Add a welcome message</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f4507-104">Dette emnet beskriver hvordan du legger til en velkomstmelding i Microsoft Dynamics 365 Commerce-webområdet.</span><span class="sxs-lookup"><span data-stu-id="f4507-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="f4507-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="f4507-105">Overview</span></span>

<span data-ttu-id="f4507-106">En velkomstmelding på webområdet for e-handel kan informere besøkende om pågående salg, områdeoppdateringer eller tilgjengelighet for sesongsamlinger.</span><span class="sxs-lookup"><span data-stu-id="f4507-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="f4507-107">Velkomstmeldingen angis ved hjelp av varselmodulen.</span><span class="sxs-lookup"><span data-stu-id="f4507-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="f4507-108">Varselmodulen skal legges til i sporet for **Feilmeldinger/Informasjonsmeldinger** i topptekstfragmentet.</span><span class="sxs-lookup"><span data-stu-id="f4507-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="f4507-109">Ved hjelp av varselmodulen kan du angi teksten som vises, tekstfargen og justeringen.</span><span class="sxs-lookup"><span data-stu-id="f4507-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="f4507-110">Du kan også angi om gjester på området kan ignorere meldingen.</span><span class="sxs-lookup"><span data-stu-id="f4507-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="f4507-111">Når en velkomstmelding blir lagt til i et delt topptekstfragment, vises den på hver side som bruker malen der det delte topptekstfragmentet brukes.</span><span class="sxs-lookup"><span data-stu-id="f4507-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="f4507-112">Følg denne fremgangsmåten for å legge til en velkomstmelding på området.</span><span class="sxs-lookup"><span data-stu-id="f4507-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="f4507-113">I Dynamics 365 Commerce går du til området ditt.</span><span class="sxs-lookup"><span data-stu-id="f4507-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="f4507-114">Velg **Fragmenter**.</span><span class="sxs-lookup"><span data-stu-id="f4507-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="f4507-115">Velg topptekstfragmentet du vil legge til meldingen i.</span><span class="sxs-lookup"><span data-stu-id="f4507-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="f4507-116">Utvid **Feilmeldinger/Informasjonsmeldinger** i disposisjonstreet.</span><span class="sxs-lookup"><span data-stu-id="f4507-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="f4507-117">Velg varselmodulen.</span><span class="sxs-lookup"><span data-stu-id="f4507-117">Select the alert module.</span></span>

    <span data-ttu-id="f4507-118">Hvis det ennå ikke finnes en varselmodul, velger du ellipseknappen (**...**) ved siden **Feilmeldinger/Informasjonsmeldinger**, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="f4507-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="f4507-119">Velg varselmodulen, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4507-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="f4507-120">I egenskapsruten til høyre, i kategorien **Data**, velger du **Legg til datakilde**, og deretter velger du **Innhold**.</span><span class="sxs-lookup"><span data-stu-id="f4507-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="f4507-121">I feltet **Inndatatekst** skriver du inn teksten i velkomstmeldingen.</span><span class="sxs-lookup"><span data-stu-id="f4507-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="f4507-122">Lagre topptekstfragmentet, sjekk det inn, og publiser det.</span><span class="sxs-lookup"><span data-stu-id="f4507-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="f4507-123">Velkomstmeldingen vil nå vises øverst på alle områdesider som bruker det valgte topptekstfragmentet.</span><span class="sxs-lookup"><span data-stu-id="f4507-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4507-124">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f4507-124">Additional resources</span></span>

[<span data-ttu-id="f4507-125">Legge til en logo</span><span class="sxs-lookup"><span data-stu-id="f4507-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="f4507-126">Velge et områdetema</span><span class="sxs-lookup"><span data-stu-id="f4507-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="f4507-127">Arbeide med CSS-overstyringsfiler</span><span class="sxs-lookup"><span data-stu-id="f4507-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="f4507-128">Legge til et favorittikon</span><span class="sxs-lookup"><span data-stu-id="f4507-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="f4507-129">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="f4507-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="f4507-130">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="f4507-130">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="f4507-131">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="f4507-131">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

