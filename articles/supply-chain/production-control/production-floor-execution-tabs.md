---
title: Utform grensesnittet for produksjonsutførelse
description: Dette emnet beskriver hvordan du utformer innholdet i brukergrensesnittet for hver konfigurasjon.
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 81c5c83128bb81523dee6ede549eece7b0d80e30
ms.sourcegitcommit: d9d1ddce6a334ade8b32b5ea3ac4c1e1a8f72715
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664278"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="ec90c-103">Utform grensesnittet for produksjonsutførelse</span><span class="sxs-lookup"><span data-stu-id="ec90c-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ec90c-104">Du kan utforme innholdet i brukergrensesnittet for hver konfigurasjon som brukes av grensesnittet for produksjonsutførelse.</span><span class="sxs-lookup"><span data-stu-id="ec90c-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="ec90c-105">Arbeidere i én arbeidscelle kan for eksempel trenge å åpne jobbinstruksjoner i produksjonen, mens det ikke er nødvendig med instruksjoner i en annen arbeidscelle.</span><span class="sxs-lookup"><span data-stu-id="ec90c-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="ec90c-106">I dette tilfellet bør det opprettes to konfigurasjoner, en med en knapp for å åpne dokumentvedlegg og en uten denne knappen.</span><span class="sxs-lookup"><span data-stu-id="ec90c-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="ec90c-107">Utform en fane</span><span class="sxs-lookup"><span data-stu-id="ec90c-107">Design a tab</span></span>

<span data-ttu-id="ec90c-108">På siden **Konfigurere produksjonsutførelse** kan du opprette og konfigurere faner ved å velge **Utform faner** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ec90c-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="ec90c-109">Hver fane er delt inn i fire deler, som vist i følgende illustrasjon.</span><span class="sxs-lookup"><span data-stu-id="ec90c-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="ec90c-110">![Faneoppsett](media/pfe-tab-layout.png "Faneoppsett")</span><span class="sxs-lookup"><span data-stu-id="ec90c-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="ec90c-111">Følgende elementer vises i illustrasjonen:</span><span class="sxs-lookup"><span data-stu-id="ec90c-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="ec90c-112">Primær verktøylinje</span><span class="sxs-lookup"><span data-stu-id="ec90c-112">Primary toolbar</span></span>
1. <span data-ttu-id="ec90c-113">Sekundær verktøylinje</span><span class="sxs-lookup"><span data-stu-id="ec90c-113">Secondary toolbar</span></span>
1. <span data-ttu-id="ec90c-114">Hovedvisning</span><span class="sxs-lookup"><span data-stu-id="ec90c-114">Main view</span></span>
1. <span data-ttu-id="ec90c-115">Detaljert visning</span><span class="sxs-lookup"><span data-stu-id="ec90c-115">Detailed view</span></span>

<span data-ttu-id="ec90c-116">Hvis du vil opprette og konfigurere en ny fane, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="ec90c-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="ec90c-117">Gå til **Produksjonskontroll &gt; Oppsett &gt; Produksjonsutførelse**.</span><span class="sxs-lookup"><span data-stu-id="ec90c-117">Go to **Production control &gt; Setup &gt; Manufacturing execution**.</span></span>

1. <span data-ttu-id="ec90c-118">Velg **Utform faner** i handlingsruten for å åpne siden **Utform faner**.</span><span class="sxs-lookup"><span data-stu-id="ec90c-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="ec90c-119">![Utform faner-siden](media/pfe-design-tabs.png "Utform faner-siden")</span><span class="sxs-lookup"><span data-stu-id="ec90c-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="ec90c-120">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ec90c-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="ec90c-121">Velg følgende innstillinger i toppteksten på siden:</span><span class="sxs-lookup"><span data-stu-id="ec90c-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="ec90c-122">**Fanenavn** – Angi et navn på fanen.</span><span class="sxs-lookup"><span data-stu-id="ec90c-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="ec90c-123">**Hovedvisning** – Velg mellom de to forhåndsdefinerte jobblistene (*Aktive jobber* eller *Alle jobber*).</span><span class="sxs-lookup"><span data-stu-id="ec90c-123">**Main view** - Select between the two pre-defined job lists (*Active jobs* or *All jobs*).</span></span>
    - <span data-ttu-id="ec90c-124">**Detaljvisning** – Velg mellom en tom verdi eller **Jobbdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="ec90c-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="ec90c-125">Hvis du velger den tomme verdien, vil det ikke være noen detaljert visning i fanen. Hvis du velger **Jobbdetaljer**, vil den detaljerte visningen inneholde en detaljert beskrivelse av jobben som er valgt i jobblisten i hovedvisningen.</span><span class="sxs-lookup"><span data-stu-id="ec90c-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="ec90c-126">Under **Primær verktøylinje** velger du hvilke knapper som skal være tilgjengelige på den primære verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="ec90c-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="ec90c-127">Kolonnen **Tilgjengelige handlinger** viser en liste over alle knappene som kan legges til.</span><span class="sxs-lookup"><span data-stu-id="ec90c-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="ec90c-128">Kolonnen **Valgte handlinger** viser en liste over alle knappene som er inkludert i den gjeldende konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="ec90c-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="ec90c-129">Bruk knappene mellom kolonnene til å flytte valgte elementer mellom kolonnene etter behov.</span><span class="sxs-lookup"><span data-stu-id="ec90c-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="ec90c-130">Bruk opp- og ned-knappene ved siden av kolonnen **Valgte handlinger** til å angi i hvilken rekkefølge knappene skal vises i, i brukergrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="ec90c-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="ec90c-131">Under **Sekundær** **verktøylinje** velger du hvilke knapper som skal være tilgjengelige på den sekundære verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="ec90c-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="ec90c-132">Kolonnen **Tilgjengelige handlinger** viser en liste over alle knappene som kan legges til.</span><span class="sxs-lookup"><span data-stu-id="ec90c-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="ec90c-133">Kolonnen **Valgte handlinger** viser en liste over alle knappene som er inkludert i den gjeldende konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="ec90c-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="ec90c-134">Bruk knappene mellom kolonnene til å flytte valgte elementer mellom kolonnene etter behov.</span><span class="sxs-lookup"><span data-stu-id="ec90c-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="ec90c-135">Bruk opp- og ned-knappene ved siden av kolonnen **Valgte handlinger** til å angi i hvilken rekkefølge knappene skal vises i, i brukergrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="ec90c-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="ec90c-136">Knytt en fane til en konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="ec90c-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="ec90c-137">Etter at du har utformet alle fanene du trenger, kan du knytte dem til en konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="ec90c-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="ec90c-138">Gå til **Produksjonskontroll &gt; Oppsett &gt; Konfigurer produksjonsutførelse**.</span><span class="sxs-lookup"><span data-stu-id="ec90c-138">Go to **Production control &gt; Setup &gt; Configure production floor execution**.</span></span>

    <span data-ttu-id="ec90c-139">![Konfigurer produksjonsutførelse](media/pfe-config-prod-floor-execution.png "Konfigurer produksjonsutførelse")</span><span class="sxs-lookup"><span data-stu-id="ec90c-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="ec90c-140">Velg **Legg til** på hurtigfanen **Fanevalg**.</span><span class="sxs-lookup"><span data-stu-id="ec90c-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="ec90c-141">Det blir lagt til en ny rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="ec90c-141">A new row is added to the grid.</span></span> <span data-ttu-id="ec90c-142">For denne nye raden velger du navnet på en fane du vil legge til i konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="ec90c-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="ec90c-143">Fortsett å legge til flere faner etter behov.</span><span class="sxs-lookup"><span data-stu-id="ec90c-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="ec90c-144">Bruk knappene **Flytt opp** og **Flytt ned** på verktøylinjen til å ordne fanene etter behov.</span><span class="sxs-lookup"><span data-stu-id="ec90c-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="ec90c-145">Fanene blir vist fra venstre mot høyre i den rekkefølgen som vises i skjermbildet ovenfor (fanen øverst vises til venstre).</span><span class="sxs-lookup"><span data-stu-id="ec90c-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>
