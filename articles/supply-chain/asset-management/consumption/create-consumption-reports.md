---
title: Opprette forbruksrapporter
description: Dette emnet forklarer hvordan du oppretter forbruksrapporter i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eecfb101af9a91f515aab221181c54d53e358a68
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652431"
---
# <a name="create-consumption-reports"></a><span data-ttu-id="65d1a-103">Opprette forbruksrapporter</span><span class="sxs-lookup"><span data-stu-id="65d1a-103">Create consumption reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="65d1a-104">Når du har opprettet og postert forbruksregistreringer på arbeidsordrer i Aktivastyring, er to rapporter tilgjengelige for visning av forbruksdetaljer.</span><span class="sxs-lookup"><span data-stu-id="65d1a-104">When you've created and posted consumption registrations on work orders in Asset Management, two reports are available to display consumption details.</span></span>


## <a name="asset-consumption-report"></a><span data-ttu-id="65d1a-105">Forbruksrapport for aktivum</span><span class="sxs-lookup"><span data-stu-id="65d1a-105">Asset consumption report</span></span>

<span data-ttu-id="65d1a-106">Når du har bokført forbruk på arbeidsordrer, kan du skrive ut en forbruksrapport for aktivum.</span><span class="sxs-lookup"><span data-stu-id="65d1a-106">When you have posted consumption on work orders, you can print an asset consumption report.</span></span> <span data-ttu-id="65d1a-107">Rapporten viser timer, timekostnader, varekostnader og utgifter som er bokført for aktiva.</span><span class="sxs-lookup"><span data-stu-id="65d1a-107">The report displays hours, hour costs, item costs, and expenses posted on assets.</span></span>

1. <span data-ttu-id="65d1a-108">Klikk **Aktivastyring** > **Rapporter** > **Aktiva** > **Aktivumforbruk**.</span><span class="sxs-lookup"><span data-stu-id="65d1a-108">Click **Asset management** > **Reports** > **Assets** > **Asset consumption**.</span></span>

2. <span data-ttu-id="65d1a-109">I dialogboksen **Aktivumforbruk** velger du parameterne og detaljnivået du vil se, ved å velge **Ja** på de aktuelle veksleknappene og sette inn et arbeidsstedsnivå i **Vis**-delen.</span><span class="sxs-lookup"><span data-stu-id="65d1a-109">In the **Asset consumption** dialog, select the parameters and detail level you want to see by selecting **Yes** on the relevant toggle buttons, and inserting a functional location level in the **Show** section.</span></span>
    - <span data-ttu-id="65d1a-110">Du kan bruke **Nivåer**-feltet til å angi hvor detaljert anleggsmiddellinjene skal være når det gjelder arbeidssteder.</span><span class="sxs-lookup"><span data-stu-id="65d1a-110">You can use the **Levels** field to indicate how detailed you want the asset lines to be regarding functional locations.</span></span> 
    
        <span data-ttu-id="65d1a-111">Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle aktiva for et arbeidssted på øverste nivå, og derfor kan det hende at en linje blir lagt til fra arbeidssteder plassert på et lavere nivå.</span><span class="sxs-lookup"><span data-stu-id="65d1a-111">For example, if you enter the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location will be shown on the top level, and therefore a line may be added up from functional locations located at a lower level.</span></span> 
        
        <span data-ttu-id="65d1a-112">Hvis du setter inn tallet 0 i **Nivåer**-feltet, vil du se et detaljert resultat som viser alle aktiva på alle arbeidsstedsnivåene de er relatert til.</span><span class="sxs-lookup"><span data-stu-id="65d1a-112">If you enter the number "0" in the **Levels** field, you will see a detailed result showing all assets on all the functional location levels to which they are related.</span></span> 
        
    - <span data-ttu-id="65d1a-113">Velg **Ja** på veksleknappen **Sum på alle underordnede aktiva** for å vise summer for hvert underaktivum i rapporten.</span><span class="sxs-lookup"><span data-stu-id="65d1a-113">Select **Yes** on the **Sum on all sub assets** toggle button to see sums for each sub asset in the report.</span></span>

3. <span data-ttu-id="65d1a-114">Velg et datointervall i **Datoer**-delen.</span><span class="sxs-lookup"><span data-stu-id="65d1a-114">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="65d1a-115">I hurtigfanen **Mål** velger du om du vil vise rapporten på skjermen, skrive den ut eller lagre den som en fil eller e-post.</span><span class="sxs-lookup"><span data-stu-id="65d1a-115">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="65d1a-116">Hvis det er nødvendig, kan du velge å vise bestemte anleggsmidler i rapporten.</span><span class="sxs-lookup"><span data-stu-id="65d1a-116">If required, you can select specific assets to be displayed in the report.</span></span> <span data-ttu-id="65d1a-117">I hurtigfanen **Poster som skal inkluderes** klikker du **Filtrer** og legger til anleggsmidlene du vil ha med i rapporten.</span><span class="sxs-lookup"><span data-stu-id="65d1a-117">On the **Records to include** FastTab, click **Filter**, and add the assets you want to include in the report.</span></span>

6. <span data-ttu-id="65d1a-118">Klikk på **OK** for å generere rapporten.</span><span class="sxs-lookup"><span data-stu-id="65d1a-118">Click **OK** to generate the report.</span></span>


## <a name="work-order-consumption-report"></a><span data-ttu-id="65d1a-119">Forbruksrapport for arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="65d1a-119">Work order consumption report</span></span>

<span data-ttu-id="65d1a-120">Når du har bokført forbruk på arbeidsordrer, kan du skrive ut en forbruksrapport for arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="65d1a-120">When you have posted consumption on work orders, you can print a work order consumption report.</span></span> <span data-ttu-id="65d1a-121">Rapporten viser timer, timekostnader, varekostnader og utgifter som er bokført for arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="65d1a-121">The report displays hours, hour costs, item costs, and expenses posted on work orders.</span></span>

1. <span data-ttu-id="65d1a-122">Klikk på **Aktivastyring** > **Rapporter** > **Arbeidsordrer** > **Arbeidsordreforbruk**.</span><span class="sxs-lookup"><span data-stu-id="65d1a-122">Click **Asset management** > **Reports** > **Work orders** > **Work order consumption**.</span></span>

2. <span data-ttu-id="65d1a-123">I dialogboksen **Arbeidsordreforbruk** velger du parameterne du vil ta med i rapporten, ved å velge **Ja** på de aktuelle veksleknappene i **Vis**-delen.</span><span class="sxs-lookup"><span data-stu-id="65d1a-123">In the **Work order consumption** dialog, select the parameters you want to include in the report by selecting **Yes** on the relevant toggle buttons in the **Show** section.</span></span>

3. <span data-ttu-id="65d1a-124">Velg et datointervall i **Datoer**-delen.</span><span class="sxs-lookup"><span data-stu-id="65d1a-124">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="65d1a-125">I hurtigfanen **Mål** velger du om du vil vise rapporten på skjermen, skrive den ut eller lagre den som en fil eller e-post.</span><span class="sxs-lookup"><span data-stu-id="65d1a-125">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="65d1a-126">Hvis det er nødvendig, kan du velge å vise bestemte arbeidsordrer i rapporten.</span><span class="sxs-lookup"><span data-stu-id="65d1a-126">If required, you can select specific work orders to be displayed in the report.</span></span> <span data-ttu-id="65d1a-127">I hurtigfanen **Poster som skal inkluderes** klikker du **Filtrer** og legger til arbeidsordrene du vil ha med i rapporten.</span><span class="sxs-lookup"><span data-stu-id="65d1a-127">On the **Records to include** FastTab, click **Filter**, and add the work orders you want to include in the report.</span></span>

6. <span data-ttu-id="65d1a-128">Klikk på **OK** for å generere rapporten.</span><span class="sxs-lookup"><span data-stu-id="65d1a-128">Click **OK** to generate the report.</span></span>


>[!NOTE]
><span data-ttu-id="65d1a-129">Du kan også generere en [arbeidsordrerapport](../work-orders/work-order-report.md), som inneholder flere arbeidsordredetaljer.</span><span class="sxs-lookup"><span data-stu-id="65d1a-129">You can also generate a [work order report](../work-orders/work-order-report.md), which contains more work order details.</span></span>

