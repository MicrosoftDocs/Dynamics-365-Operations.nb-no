---
title: Arbeidsområde for lastplanlegging
description: Dette emnet beskriver hvordan du arbeider med arbeidsområde for lastplanlegging.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 429a8bac5491a342ecbc8b67c59c71715a4b0889
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646421"
---
# <a name="load-building-workbench"></a><span data-ttu-id="d5994-103">Arbeidsområde for lastplanlegging</span><span class="sxs-lookup"><span data-stu-id="d5994-103">Load building workbench</span></span>

<span data-ttu-id="d5994-104">Med arbeidsområde for lastplanlegging kan du bruke lastplanleggingsstrategier når du oppretter belastninger.</span><span class="sxs-lookup"><span data-stu-id="d5994-104">The load building workbench lets you apply load building strategies when you create loads.</span></span>

## <a name="create-a-load-building-strategy"></a><span data-ttu-id="d5994-105">Opprett en lastplanleggingsstrategi</span><span class="sxs-lookup"><span data-stu-id="d5994-105">Create a load building strategy</span></span>

<span data-ttu-id="d5994-106">Du bruker lastplanleggingsstrategier til å bygge belastninger automatisk.</span><span class="sxs-lookup"><span data-stu-id="d5994-106">You use load building strategies to automatically build loads.</span></span> <span data-ttu-id="d5994-107">Denne funksjonen kan være nyttig i følgende situasjoner:</span><span class="sxs-lookup"><span data-stu-id="d5994-107">This capability can be beneficial in the following situations:</span></span>

- <span data-ttu-id="d5994-108">Hvis du ofte sender et bestemt sett med produkter, vil laststrategier hjelpe deg med å spare tid, fordi du ikke trenger å bygge den samme belastningen hver gang.</span><span class="sxs-lookup"><span data-stu-id="d5994-108">If you regularly ship a specific set of products, load strategies help save time, because you don't have to build the same load every time.</span></span>
- <span data-ttu-id="d5994-109">Hvis du vil unngå halvfulle belastninger for å maksimere effektiviteten, kan laststrategier bidra til å fylle hver belastning så mye som mulig.</span><span class="sxs-lookup"><span data-stu-id="d5994-109">If you want to avoid half-full loads to maximize efficiency, load strategies can help fill each load as much as possible.</span></span>

<span data-ttu-id="d5994-110">En laststrategiklasse som heter `TMSLoadBuildingVolumeStrategy` gir en laststrategi som heter *Volumbasert laststrategi*.</span><span class="sxs-lookup"><span data-stu-id="d5994-110">A load building strategy class that is named `TMSLoadBuildingVolumeStrategy` provides a load building strategy that is named *Volume-based load building strategy*.</span></span> <span data-ttu-id="d5994-111">Med denne strategien kan du bruke de maksimale verdiene som er angitt for høyde og vekt i lastmalen, eller du kan overstyre innstillingene ved å angi nye verdier.</span><span class="sxs-lookup"><span data-stu-id="d5994-111">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="d5994-112">Denne strategien er den eneste strategien som er inkludert.</span><span class="sxs-lookup"><span data-stu-id="d5994-112">This strategy is the only strategy that is included out of the box.</span></span> <span data-ttu-id="d5994-113">(Du kan imidlertid ha noen egendefinerte strategier.)</span><span class="sxs-lookup"><span data-stu-id="d5994-113">(However, you might have some custom strategies.)</span></span>

<span data-ttu-id="d5994-114">Hvis du vil bruke den bruksklare strategien *Volumbasert strategi for lastplanlegging*, velger du den i feltet **Strategi for lastplanlegging** på siden **Arbeidsområde for lastplanlegging** (**Transportstyring &gt; Planlegging &gt; Arbeidsområde for lastplanlegging)**.</span><span class="sxs-lookup"><span data-stu-id="d5994-114">To use the out-of-box *Volume-based load building strategy* strategy, select it in the **Load building strategy** field on the **Load building workbench** page (**Transportation management &gt; Planning &gt; Load building workbench**).</span></span>

<span data-ttu-id="d5994-115">Følg denne fremgangsmåten for å opprette en strategi for lastplanlegging.</span><span class="sxs-lookup"><span data-stu-id="d5994-115">To create a load building strategy, follow these steps.</span></span>

1. <span data-ttu-id="d5994-116">Gå til **Transportstyring &gt; Oppsett &gt; Lastplanlegging &gt; Strategier for lastplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="d5994-116">Go to **Transportation management &gt; Setup &gt; Load building &gt; Load building strategies**.</span></span>
1. <span data-ttu-id="d5994-117">I handlingsruten velger du **Generer klasseliste** for å kontrollere at du har siste versjon av alle tilgjengelige klasser.</span><span class="sxs-lookup"><span data-stu-id="d5994-117">On the Action Pane, select **Generate class list** to make sure that you have the latest versions of all available classes.</span></span>
1. <span data-ttu-id="d5994-118">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d5994-118">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d5994-119">Angi et unikt navn for strategien, velg klassen til strategien for lastplanlegging for den, og angi en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d5994-119">Enter a unique name for the strategy, select the load building strategy class for it, and enter a description.</span></span>
1. <span data-ttu-id="d5994-120">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d5994-120">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="d5994-121">Velg **Parametere** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d5994-121">On the Action Pane, select **Parameters**.</span></span>
1. <span data-ttu-id="d5994-122">På siden **Parametere for strategi for lastplanlegging** velger du **Volumkapasitet** i listen, og deretter angir du i feltet **Verdi** prosentandelen av lastens totale volumkapasitet som skal tas i bruk for den nye strategien for lastplanlegging.</span><span class="sxs-lookup"><span data-stu-id="d5994-122">On the **Load building strategy parameters** page, select **Volume capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total volume capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="d5994-123">Velg **Vektkapasitet** i listen, og angi deretter i feltet **Verdi** prosentandelen av lastens totale vektkapasitet som skal tas i bruk for den nye strategien for lastplanlegging.</span><span class="sxs-lookup"><span data-stu-id="d5994-123">Select **Weight capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total weight capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="d5994-124">Lukk siden **Parametere for strategi for lastplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="d5994-124">Close the **Load building strategy parameters** page.</span></span>
1. <span data-ttu-id="d5994-125">Lukk siden **Strategier for lastplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="d5994-125">Close the **Load building strategies** page.</span></span>

<span data-ttu-id="d5994-126">Nå kan du tilordne en strategi for lastplanlegging til en mal for lastplanlegging.</span><span class="sxs-lookup"><span data-stu-id="d5994-126">You can now assign the load building strategy to a load building template.</span></span> <span data-ttu-id="d5994-127">Du kan også bruke den direkte i arbeidsområdet for lastplanlegging.</span><span class="sxs-lookup"><span data-stu-id="d5994-127">Alternatively, you can use it directly in the load planning workbench.</span></span>

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a><span data-ttu-id="d5994-128">Bruk en strategi for lastplanlegging i arbeidsområdet for lastplanlegging</span><span class="sxs-lookup"><span data-stu-id="d5994-128">Use a load building strategy in the load building workbench</span></span>

1. <span data-ttu-id="d5994-129">Gå til **Transportstyring &gt; Planlegging &gt; Arbeidsområde for lastplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="d5994-129">Go to **Transportation management &gt; Planning &gt; Load building workbench**.</span></span>
1. <span data-ttu-id="d5994-130">Følg ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="d5994-130">Follow one of these steps:</span></span>

    - <span data-ttu-id="d5994-131">Velg en strategi i feltet **Strategi for lastplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="d5994-131">Select a strategy in the **Load building strategy** field.</span></span>
    - <span data-ttu-id="d5994-132">Hvis du har definert en lastplanleggingsmal og tilordnet strategien for lastplanlegging til den, velger du **Bruk mal** i handlingsruten i fanen **Administrer maler**.</span><span class="sxs-lookup"><span data-stu-id="d5994-132">If you've defined a load building template and assigned the load building strategy to it, on the Action Pane, on the **Manage templates** tab, select **Apply template**.</span></span> <span data-ttu-id="d5994-133">Deretter velger du en mal i feltet **Navn på lastplanleggingsmal** i rullegardinfeltet **Bruk lastplanleggingsmal**.</span><span class="sxs-lookup"><span data-stu-id="d5994-133">Then, in the **Apply load building template** drop-down dialog box, select a template in the **Load building template name** field.</span></span>

1. <span data-ttu-id="d5994-134">Velg én eller flere [lastmaler](load-template.md) i hurtigfanen **Lastmalsekvens**.</span><span class="sxs-lookup"><span data-stu-id="d5994-134">On the **Load templates sequence** FastTab, select one or more [load templates](load-template.md).</span></span> <span data-ttu-id="d5994-135">Arbeidsområdet vil forsøke å tilpasse belastningen inn i disse beholderne, i rekkefølgen som er angitt her.</span><span class="sxs-lookup"><span data-stu-id="d5994-135">The workbench will try to fit the load into these types of containers, in the sequence that is specified here.</span></span> <span data-ttu-id="d5994-136">Vanligvis bør du plassere de minste beholderne øverst på listen for å sikre at den minste mulige beholderen velges først.</span><span class="sxs-lookup"><span data-stu-id="d5994-136">Typically, you should put the smallest containers at the top of the list to ensure that the smallest possible container is selected first.</span></span>
1. <span data-ttu-id="d5994-137">Klikk på **Foreslå laster** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d5994-137">On the Action Pane, select **Propose loads**.</span></span>
1. <span data-ttu-id="d5994-138">Se gjennom de foreslåtte lastene og foreslåtte lastlinjene.</span><span class="sxs-lookup"><span data-stu-id="d5994-138">Review the proposed loads and proposed load lines.</span></span>
1. <span data-ttu-id="d5994-139">Velg **Opprett laster** i handlingsruten for å opprette laster som er basert på kildedokumentlinjene på hurtigfanen **Foreslåtte belastningslinjer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d5994-139">On the Action Pane, select **Create loads** to create loads that are based on the source document lines on the **Proposed load lines** FastTab.</span></span>
1. <span data-ttu-id="d5994-140">Lukk siden **Arbeidsområde for lastplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="d5994-140">Close the **Load building workbench** page.</span></span>
