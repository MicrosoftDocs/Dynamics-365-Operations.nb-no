---
title: Legge til en velkomstmelding
description: Dette emnet beskriver hvordan du legger til en velkomstmelding for nettstedet ditt for Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e61f43eca7d1343d020e1c01b5b1140f07b63c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797389"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="b6682-103">Legge til en velkomstmelding</span><span class="sxs-lookup"><span data-stu-id="b6682-103">Add a welcome message</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b6682-104">Dette emnet beskriver hvordan du legger til en velkomstmelding for nettstedet ditt for Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b6682-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

<span data-ttu-id="b6682-105">En velkomstmelding på webområdet for e-handel kan informere besøkende om pågående salg, områdeoppdateringer eller tilgjengelighet for sesongsamlinger.</span><span class="sxs-lookup"><span data-stu-id="b6682-105">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="b6682-106">Velkomstmeldingen angis ved hjelp av varselmodulen.</span><span class="sxs-lookup"><span data-stu-id="b6682-106">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="b6682-107">Varselmodulen skal legges til i sporet for **Feilmeldinger/Informasjonsmeldinger** i topptekstfragmentet.</span><span class="sxs-lookup"><span data-stu-id="b6682-107">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="b6682-108">Ved hjelp av varselmodulen kan du angi teksten som vises, tekstfargen og justeringen.</span><span class="sxs-lookup"><span data-stu-id="b6682-108">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="b6682-109">Du kan også angi om gjester på området kan ignorere meldingen.</span><span class="sxs-lookup"><span data-stu-id="b6682-109">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="b6682-110">Når en velkomstmelding blir lagt til i et delt topptekstfragment, vises den på hver side som bruker malen der det delte topptekstfragmentet brukes.</span><span class="sxs-lookup"><span data-stu-id="b6682-110">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="b6682-111">Følg denne fremgangsmåten for å legge til en velkomstmelding på området.</span><span class="sxs-lookup"><span data-stu-id="b6682-111">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="b6682-112">Gå til området i Commerce-områdebygger.</span><span class="sxs-lookup"><span data-stu-id="b6682-112">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="b6682-113">Velg **Fragmenter**.</span><span class="sxs-lookup"><span data-stu-id="b6682-113">Select **Fragments**.</span></span>
1. <span data-ttu-id="b6682-114">Velg topptekstfragmentet du vil legge til meldingen i.</span><span class="sxs-lookup"><span data-stu-id="b6682-114">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="b6682-115">Utvid **Feilmeldinger/Informasjonsmeldinger** i disposisjonstreet.</span><span class="sxs-lookup"><span data-stu-id="b6682-115">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="b6682-116">Velg varselmodulen, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6682-116">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="b6682-117">Hvis det ennå ikke finnes en varselmodul, velger du først ellipseknappen (**...**) ved siden **Feilmeldinger/Informasjonsmeldinger**, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="b6682-117">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="b6682-118">I egenskapsruten til høyre, i kategorien **Data**, velger du **Legg til datakilde**, og deretter velger du **Innhold**.</span><span class="sxs-lookup"><span data-stu-id="b6682-118">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="b6682-119">I feltet **Inndatatekst** skriver du inn teksten i velkomstmeldingen.</span><span class="sxs-lookup"><span data-stu-id="b6682-119">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="b6682-120">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn topptekstfragmentet, og velg deretter **Publiser** for å publisere det.</span><span class="sxs-lookup"><span data-stu-id="b6682-120">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="b6682-121">Velkomstmeldingen vil nå vises øverst på alle områdesider som bruker det valgte topptekstfragmentet.</span><span class="sxs-lookup"><span data-stu-id="b6682-121">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6682-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b6682-122">Additional resources</span></span>

[<span data-ttu-id="b6682-123">Legge til en logo</span><span class="sxs-lookup"><span data-stu-id="b6682-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="b6682-124">Velge et områdetema</span><span class="sxs-lookup"><span data-stu-id="b6682-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="b6682-125">Arbeide med CSS-overstyringsfiler</span><span class="sxs-lookup"><span data-stu-id="b6682-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="b6682-126">Legge til et favorittikon</span><span class="sxs-lookup"><span data-stu-id="b6682-126">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="b6682-127">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="b6682-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="b6682-128">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="b6682-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="b6682-129">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="b6682-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
