---
title: Handlingssøk
description: Denne artikkelen beskriver funksjonen for handlingssøk. Handlingssøk hjelper deg med å finne og kjøre handlinger på en side.
author: jasongre
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d01247aa356625cb759306e5ead2afd3cdeb840f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191322"
---
# <a name="action-search"></a><span data-ttu-id="4ddfa-104">Handlingssøk</span><span class="sxs-lookup"><span data-stu-id="4ddfa-104">Action search</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ddfa-105">Denne artikkelen beskriver funksjonen for handlingssøk.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-105">This article describes the action search functionality.</span></span> <span data-ttu-id="4ddfa-106">Handlingssøk hjelper deg med å finne og kjøre handlinger på en side.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-106">Action search will help you find and run actions on a page.</span></span>

## <a name="introduction"></a><span data-ttu-id="4ddfa-107">Innledning</span><span class="sxs-lookup"><span data-stu-id="4ddfa-107">Introduction</span></span>

<span data-ttu-id="4ddfa-108">Sidene viser hovedsakelig kommandoer i handlingsruter, både standard handlingsruten som vises øverst på en side, og verktøylinjene som vises i ulike deler av siden.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-108">Pages primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="4ddfa-109">I tidligere versjoner gir en funksjon for nøkkeltips deg rask tilgang til alle knapper i en handlingsrute ved å trykke Alt-tasten og deretter en serie med bokstaver.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span>

<span data-ttu-id="4ddfa-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span><span class="sxs-lookup"><span data-stu-id="4ddfa-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span></span>

<span data-ttu-id="4ddfa-111">Nøkkeltips er ikke lenger tilgjengelige, men er erstattet med handlingssøkfunksjonen.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-111">Key Tips are no longer available but have been replaced by the action search feature.</span></span> <span data-ttu-id="4ddfa-112">Denne nye funksjonen lar deg raskt søke etter og kjøre en knapp fra en hvilken som helst synlig handlingsrute.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-112">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="4ddfa-113">Bruke handlingssøk</span><span class="sxs-lookup"><span data-stu-id="4ddfa-113">Using action search</span></span>

<span data-ttu-id="4ddfa-114">Når du skal bruke handlingssøkfunksjonen, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-114">To use the action search feature, follow these steps.</span></span>

1. <span data-ttu-id="4ddfa-115">I handlingsruten klikker du i feltet for **handlingssøk**.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-115">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="4ddfa-116">(Feltet for **handlingssøk** inneholder et forstørrelsesglassikon.)</span><span class="sxs-lookup"><span data-stu-id="4ddfa-116">(The **action search** field contains a magnifying glass icon.)</span></span>
2. <span data-ttu-id="4ddfa-117">Skriv inn hele eller deler av navnet på knappen du vil kjøre.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-117">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="4ddfa-118">Du kan også søke ved hjelp av ord fra knappens "bane".</span><span class="sxs-lookup"><span data-stu-id="4ddfa-118">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="4ddfa-119">(Hvis du vil ha mer informasjon, se den neste delen av denne artikkelen.) En knapp vises vanligvis øverst i resultatlisten etter at du har skrevet inn to til fire tegn.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-119">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3. <span data-ttu-id="4ddfa-120">Finn og kjør knappen i resultatlisten (ved hjelp av musen eller tastaturet).</span><span class="sxs-lookup"><span data-stu-id="4ddfa-120">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="4ddfa-121">Når knappen er kjørt, returnerer fokuset til den siste posisjonen på siden, slik at du kan fortsette å arbeide.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-121">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span>

<span data-ttu-id="4ddfa-122">[![handling-søk-felt](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="4ddfa-122">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="4ddfa-123">Du kan også starte handlingssøket ved å trykke Ctrl +/ eller Alt + Q.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-123">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="4ddfa-124">Trykk hurtigtasten på nytt for å returnere fokuset til den siste posisjonen på siden.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-124">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="4ddfa-125">Forstå resultatlisten</span><span class="sxs-lookup"><span data-stu-id="4ddfa-125">Understanding the results list</span></span>

<span data-ttu-id="4ddfa-126">Du må ofte vite både plasseringen og konteksten til en knapp for å fullt ut forstå formålet med denne knappen.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-126">Often, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="4ddfa-127">Derfor vises tilleggsinformasjon for hvert element i listen over resultater, som forklarer nøyaktig hvilke knapper som vises i listen.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-127">Therefore, additional information is shown for each item in the results list, to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="4ddfa-128">Spesielt vises "banen" for knappen.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-128">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="4ddfa-129">Denne banen kan inkludere etikettene for følgende grensesnittelementer, etter behov:</span><span class="sxs-lookup"><span data-stu-id="4ddfa-129">This path might include the labels of the following UI elements, as relevant:</span></span>

- <span data-ttu-id="4ddfa-130">Handlingsrutekategori</span><span class="sxs-lookup"><span data-stu-id="4ddfa-130">Action Pane tab</span></span>
- <span data-ttu-id="4ddfa-131">Knappegruppe</span><span class="sxs-lookup"><span data-stu-id="4ddfa-131">Button group</span></span>
- <span data-ttu-id="4ddfa-132">Menyknapp (hvis knappen er i en menyknapp)</span><span class="sxs-lookup"><span data-stu-id="4ddfa-132">Menu button (if the button is inside a menu button)</span></span>
- <span data-ttu-id="4ddfa-133">Menyskillelinje (hvis knappen er i en navngitt gruppe i en menyknapp)</span><span class="sxs-lookup"><span data-stu-id="4ddfa-133">Menu separator (if the button is inside a named group inside a menu button)</span></span>
- <span data-ttu-id="4ddfa-134">Gruppen eller kategorien på siden (for eksempel navnet på en hurtigfane)</span><span class="sxs-lookup"><span data-stu-id="4ddfa-134">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="4ddfa-135">Du tastet for eksempel **tot** i feltet for **handlingssøk**, og undersøker nå resultatlisten.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-135">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="4ddfa-136">Den første oppføringen, for en knapp som heter **Totaler**, er uthevet.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-136">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="4ddfa-137">En knapp i banen til **Salgsordre** &gt; **Vis** vises også.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-137">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="4ddfa-138">**Salgsordre**-delen av banen korresponderer til **Salgsordre**-kategorien på handlingspanelet, og **Vis**-delen av banen korresponderer til **Vis**-gruppen for denne kategorien. Tilsvarende vil banen for **Total rabatt**-knappen (**Selg** &gt; **Beregne**) informere deg at denne knappen er lokalisert i **Kalkuler**-gruppen i kategorien **Selg** i handlingspanelet.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-138">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="4ddfa-139">Derfor kan denne informasjonen hjelpe deg med å forstå nøyaktig hvilken knapp som vil utløses av handlingssøk (hvis du velger denne knappen i resultatlisten).</span><span class="sxs-lookup"><span data-stu-id="4ddfa-139">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span>

<span data-ttu-id="4ddfa-140">[![handling-søk-felt-med-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="4ddfa-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span>

<span data-ttu-id="4ddfa-141">I det forrige eksemplet viste handlingssøk resultatene fra standardhandlingsruten øverst på en side.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-141">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="4ddfa-142">Handlingssøk viser imidlertid også resultater fra synlige verktøylinjer som er plassert andre steder på siden.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-142">However, action search also shows results from visible toolbars that are located in other places on the page.</span></span> <span data-ttu-id="4ddfa-143">Du søker for eksempel etter knappen **Lagerbeholdning** som er plassert i hurtigfanen **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-143">For example, you're searching for the **On-hand inventory** button that is located on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="4ddfa-144">I dette tilfellet informerer knappebanen i resultatlisten (**Salgsordrelinjer** &gt; **Beholdning** &gt; **Vis**) deg om at denne knappen er plassert under overskriften **Vis** på **Beholdning**-menyknappen i hurtigfanen **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-144">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is located under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span>

<span data-ttu-id="4ddfa-145">[![lager-beholdning](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="4ddfa-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="4ddfa-146">Handlingssøk kontra navigasjonssøk</span><span class="sxs-lookup"><span data-stu-id="4ddfa-146">Action search vs. Navigation search</span></span>

<span data-ttu-id="4ddfa-147">Mens handlingssøk skal søke etter og kjøre handlinger på en side, er det en egen søkemekanisme for å finne og navigere til sider.</span><span class="sxs-lookup"><span data-stu-id="4ddfa-147">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages.</span></span> <span data-ttu-id="4ddfa-148">Hvis du vil ha mer informasjon om denne funksjonen, kan du se artikkelen [Navigasjonssøk](navigation-search.md).</span><span class="sxs-lookup"><span data-stu-id="4ddfa-148">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>
