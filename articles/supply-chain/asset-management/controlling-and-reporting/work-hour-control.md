---
title: Arbeidstidskontroll
description: Dette emnet beskriver arbeidstidskontroll i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4ba1c9548ac7ad54a459f42fd9f8f20c6936f14c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216376"
---
# <a name="work-hour-control"></a><span data-ttu-id="c3b70-103">Arbeidstidskontroll</span><span class="sxs-lookup"><span data-stu-id="c3b70-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c3b70-104">I Aktivastyring kan du beregne timer for å få en oversikt over faktiske timer sammenlignet med budsjetterte timer for aktiva, arbeidssteder eller arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="c3b70-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="c3b70-105">Faktiske timer er basert på posterte transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="c3b70-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="c3b70-106">Arbeidstidskontroll for aktiva, arbeidssteder og arbeidsordrer</span><span class="sxs-lookup"><span data-stu-id="c3b70-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="c3b70-107">Beregningene for aktiva, arbeidssteder og arbeidsordrer er nesten identiske.</span><span class="sxs-lookup"><span data-stu-id="c3b70-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="c3b70-108">Den eneste forskjellen er at for anleggsmidler og arbeidssteder kan du også inkludere underordnede aktiva og underordnede arbeidssteder i beregningen.</span><span class="sxs-lookup"><span data-stu-id="c3b70-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="c3b70-109">Datoen er transaksjonsdatoen da registreringen ble registrert.</span><span class="sxs-lookup"><span data-stu-id="c3b70-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="c3b70-110">Klikk på **Aktivastyring** > **Forespørsler** > **Aktiva** > **Timekontroll for aktivum** eller **Timekontroll for arbeidssted**, eller **Aktivastyring** > **Forespørsler** > **Arbeidsordrer** > **Timekontroll for arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="c3b70-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="c3b70-111">I dialogboksen **Timekontroll for aktivum**, .</span><span class="sxs-lookup"><span data-stu-id="c3b70-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="c3b70-112">I dialogboksen **Timekontroll for aktivum** / **Timekontroll for arbeidssted** / **Timekontroll for arbeidsordre** velger du en periode som skal beregnes, i feltene **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="c3b70-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="c3b70-113">Hvis det er nødvendig, velger du et **finansdimensjonssett** som skal tas med i beregningen.</span><span class="sxs-lookup"><span data-stu-id="c3b70-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="c3b70-114">Velg "Ja" på veksleknappen **Hopp over null** hvis du ikke vil vise resultater med null timer.</span><span class="sxs-lookup"><span data-stu-id="c3b70-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="c3b70-115">Du kan bruke **Nivå**-feltet til å angi hvor detaljert timekontrollinjene skal være når det gjelder arbeidssted.</span><span class="sxs-lookup"><span data-stu-id="c3b70-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="c3b70-116">Hvis du for eksempel setter inn tallet 1 i feltet, og du har et arbeidsstedshierarki med flere nivåer, vises alle timekontrollinjer for et arbeidssted på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå.</span><span class="sxs-lookup"><span data-stu-id="c3b70-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="c3b70-117">Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle timekontrollinjene på alle arbeidsstedsnivåene de er relatert til.</span><span class="sxs-lookup"><span data-stu-id="c3b70-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="c3b70-118">Velg Ja på veksleknappen **Inkluder underordnede aktiva** for å vise kostnader knyttet til underordnede aktiva som separate linjer.</span><span class="sxs-lookup"><span data-stu-id="c3b70-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="c3b70-119">Hvis du vil begrense søket, kan du velge bestemte anleggsmidler/arbeidssteder/arbeidsordrer i hurtigfanen **Poster som skal inkluderes**.</span><span class="sxs-lookup"><span data-stu-id="c3b70-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="c3b70-120">Klikk på **OK** for å starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="c3b70-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="c3b70-121">På siden **Timekontroll for aktivum** klikker du på knappen **Grupper etter** for å vise det nødvendige detaljnivået for beregningen.</span><span class="sxs-lookup"><span data-stu-id="c3b70-121">On the **Asset hour control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="c3b70-122">De valgte **Grupper etter**-knappen er uthevet.</span><span class="sxs-lookup"><span data-stu-id="c3b70-122">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="c3b70-123">Klikk på en knapp for å aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="c3b70-123">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="c3b70-124">Eksempel</span><span class="sxs-lookup"><span data-stu-id="c3b70-124">Example</span></span>

<span data-ttu-id="c3b70-125">Skjermbildet nedenfor viser et eksempel på beregning av **timekontroll for aktivum**.</span><span class="sxs-lookup"><span data-stu-id="c3b70-125">The screenshot below shows an example of an **Asset hour control** calculation.</span></span>

- <span data-ttu-id="c3b70-126">Feltet **Opprinnelig budsjett** viser budsjetterte timer fra arbeidsordreprognosen.</span><span class="sxs-lookup"><span data-stu-id="c3b70-126">The **Original budget** field shows budget hours from the work order forecast.</span></span> 
- <span data-ttu-id="c3b70-127">Feltet **Faktiske timer** viser posterte timer på arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="c3b70-127">The **Actual hours** field shows posted hours on work orders.</span></span> 
- <span data-ttu-id="c3b70-128">Feltet **Igangsatte timer** viser totalt antall timer som firmaet har forpliktet seg til i forhold til arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="c3b70-128">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>

![Eksempel på beregning av timekontroll for aktivum](media/04-controlling-and-reporting.png)

<span data-ttu-id="c3b70-130">En annen måte å gjøre en timeberegning på er å velge flere aktiva i **Alle aktiva** eller **Aktive aktiva**.</span><span class="sxs-lookup"><span data-stu-id="c3b70-130">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="c3b70-131">Deretter klikker du på knappen **Timekontroll** i hurtigfanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="c3b70-131">Then you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="c3b70-132">De valgte anleggsmidlene settes automatisk inn i **Aktivum**-feltet i hurtigfanen **Poster som skal inkluderes**.</span><span class="sxs-lookup"><span data-stu-id="c3b70-132">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="c3b70-133">Klikk på **OK** i dialogboksen **Timekontroll for aktivum**, og beregningen for de valgte anleggsmidlene vises.</span><span class="sxs-lookup"><span data-stu-id="c3b70-133">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="c3b70-134">Den samme fremgangsmåten kan brukes for arbeidssteder i **Alle arbeidssteder** eller **Aktive arbeidssteder**, og for arbeidsordrer i **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="c3b70-134">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


