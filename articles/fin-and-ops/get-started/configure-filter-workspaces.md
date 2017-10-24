---
title: "Konfigurere og filtrere arbeidsområder"
description: "Denne artikkelen gir en oversikt over hvordan du konfigurerer og filtrerer arbeidsområder."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17491
ms.assetid: 541e6012-4680-4684-8494-e9b5ca4684ee
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 754cd81a4550318de7003d847fafb2bcc7414b32
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="configure-and-filter-workspaces"></a><span data-ttu-id="abff8-103">Konfigurere og filtrere arbeidsområder</span><span class="sxs-lookup"><span data-stu-id="abff8-103">Configure and filter workspaces</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="abff8-104">Denne artikkelen gir en oversikt over hvordan du konfigurerer og filtrerer arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="abff8-104">This article provides an overview about how to configure and filter workspaces.</span></span>

<a name="configuring-a-workspace"></a><span data-ttu-id="abff8-105">Konfigurere et arbeidsområde</span><span class="sxs-lookup"><span data-stu-id="abff8-105">Configuring a workspace</span></span>
-----------------------

<span data-ttu-id="abff8-106">Du kan endre utseendet og virkemåten til noen arbeidsområder ved å oppdatere innstillinger som gjelder hele arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="abff8-106">You can change the appearance and behavior of some workspaces by updating settings that apply to the whole workspace.</span></span> <span data-ttu-id="abff8-107">Når du kan konfigurere et arbeidsområde, inneholder handlingsruten en knapp som angir at du kan klikke den for å gjøre endringer i konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="abff8-107">When a workspace can be configured, the Action Pane includes a button that instructs you to click it to make configuration changes.</span></span> <span data-ttu-id="abff8-108">I illustrasjonen nedenfor heter for eksempel knappen **Konfigurer mitt arbeidsområde**.</span><span class="sxs-lookup"><span data-stu-id="abff8-108">For example, in the following illustration, the button is named **Configure my workspace**.</span></span> 

<span data-ttu-id="abff8-109">[![konfigurere-og-filtrere-arbeidsområder](./media/configure-and-filter-workspaces.png)](./media/configure-and-filter-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="abff8-109">[![configure-and-filter-workspaces](./media/configure-and-filter-workspaces.png)](./media/configure-and-filter-workspaces.png)</span></span>   

<span data-ttu-id="abff8-110">Når du klikker knappen, vises en dialogboks. Der kan du endre de forhåndsdefinerte innstillingene for arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="abff8-110">When you click the button, a dialog appears, where you can modify the predefined settings for the workspace.</span></span> <span data-ttu-id="abff8-111">De bestemte innstillingene du ser i denne dialogboksen, varierer etter hvert arbeidsområde og er avhengig av bestemte kontroller og forretningsdata som er tilgjengelige i arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="abff8-111">The specific settings that you see in this dialog vary by workspace, and depend on the specific controls and business data that are available in the workspace.</span></span> 

<span data-ttu-id="abff8-112">[![konfigurere-mitt-arbeidsområde](./media/configure-my-workspace.png)](./media/configure-my-workspace.png)</span><span class="sxs-lookup"><span data-stu-id="abff8-112">[![configure-my-workspace](./media/configure-my-workspace.png)](./media/configure-my-workspace.png)</span></span>

## <a name="filtering-a-workspace"></a><span data-ttu-id="abff8-113">Filtrere et arbeidsområde</span><span class="sxs-lookup"><span data-stu-id="abff8-113">Filtering a workspace</span></span>
<span data-ttu-id="abff8-114">Mange arbeidsområder lar deg filtrere innholdet som vises i filene.</span><span class="sxs-lookup"><span data-stu-id="abff8-114">Many workspaces let you filter the content that appears in them.</span></span> <span data-ttu-id="abff8-115">Kontrollene som er tilgjengelige, kan la deg filtrere innholdet i arbeidsområdet eller bare innholdet i en bestemt del av arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="abff8-115">The controls that are available might let you filter all the content in the workspace or only the content in a specific section of the workspace.</span></span> <span data-ttu-id="abff8-116">Filtrene på arbeidsområder kan være oppslag, kombinasjonsbokser, felt for frihåndstekst eller andre kontrolltyper.</span><span class="sxs-lookup"><span data-stu-id="abff8-116">The filters on workspaces can be lookups, combo boxes, free-form text fields, or other types of controls.</span></span> <span data-ttu-id="abff8-117">Alle typer filter har imidlertid samme effekt, som beskrevet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="abff8-117">However, every type of filter has the same effects, as described in the following sections.</span></span>

### <a name="workspace-wide-filters"></a><span data-ttu-id="abff8-118">Filtre for hele arbeidsområdet</span><span class="sxs-lookup"><span data-stu-id="abff8-118">Workspace-wide filters</span></span>

<span data-ttu-id="abff8-119">Du kan filtrere hele arbeidsområdet ved å bruke et filter for hele arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="abff8-119">You can filter the whole workspace by using a workspace-wide filter.</span></span> <span data-ttu-id="abff8-120">Et filter for hele arbeidsområdet vises i øvre venstre hjørne på arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="abff8-120">A workspace-wide filter appears in the upper-left corner of the workspace.</span></span> <span data-ttu-id="abff8-121">Når du velger en bestemt verdi i rullegardinlisten, blir innholdet i arbeidsområdet filtrert basert på dette valget.</span><span class="sxs-lookup"><span data-stu-id="abff8-121">When you select a specific value in the drop-down list, the contents of the workspace are filtered based on that selection.</span></span> 

<span data-ttu-id="abff8-122">[![arbeidsområde-filtrere](./media/workspace-filter.png)](./media/workspace-filter.png)</span><span class="sxs-lookup"><span data-stu-id="abff8-122">[![workspace-filter](./media/workspace-filter.png)](./media/workspace-filter.png)</span></span> 

<span data-ttu-id="abff8-123">Når du klikker for å åpne filteret, vises flere alternativer.</span><span class="sxs-lookup"><span data-stu-id="abff8-123">When you click to open the filter, you're presented with several options.</span></span> 

<span data-ttu-id="abff8-124">[![arbeidsområde-filter-utvidet](./media/workspace-filter-expanded.png)](./media/workspace-filter-expanded.png)</span><span class="sxs-lookup"><span data-stu-id="abff8-124">[![workspace-filter-expanded](./media/workspace-filter-expanded.png)](./media/workspace-filter-expanded.png)</span></span> 

<span data-ttu-id="abff8-125">Velg et alternativ for å filtrere arbeidsområdet basert på dette alternativet.</span><span class="sxs-lookup"><span data-stu-id="abff8-125">Select an option to filter the workspace based on that option.</span></span>

### <a name="workspace-section-filters"></a><span data-ttu-id="abff8-126">Filtre i arbeidsområdedel</span><span class="sxs-lookup"><span data-stu-id="abff8-126">Workspace section filters</span></span>

<span data-ttu-id="abff8-127">Hvis enkelte deler av arbeidsområdet har filtre, kan du filtrere hver del separat.</span><span class="sxs-lookup"><span data-stu-id="abff8-127">If individual sections of the workspace have filters, you can filter each section separately.</span></span> <span data-ttu-id="abff8-128">I illustrasjonen nedenfor, er filteret (feltet som inneholder teksten "Filter") et eksempel på et filter for frihåndstekst.</span><span class="sxs-lookup"><span data-stu-id="abff8-128">In the following illustration, the filter (the field that contains the text "Filter") is an example of a free-form text field filter.</span></span> 

<span data-ttu-id="abff8-129">[![arbeidsområde-del-filtre](./media/workspace-section-filters.png)](./media/workspace-section-filters.png)</span><span class="sxs-lookup"><span data-stu-id="abff8-129">[![workspace-section-filters](./media/workspace-section-filters.png)](./media/workspace-section-filters.png)</span></span> 

<span data-ttu-id="abff8-130">Som med et filter for hele arbeidsområdet velger eller angir du en verdi i feltet for å filtrere innholdet i delen.</span><span class="sxs-lookup"><span data-stu-id="abff8-130">As with a workspace-wide filter, select or enter a value in the field to filter the contents of the section.</span></span>




