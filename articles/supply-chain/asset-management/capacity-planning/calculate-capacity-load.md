---
title: Beregn kapasitetsbelastning
description: Dette emnet forklarer hvordan du beregner kapasitetsbelastning i Aktivastyring.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ba4b9ef43e27f689e1f10d2ee8f10f6ea4bf43ed
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821735"
---
# <a name="calculate-capacity-load"></a><span data-ttu-id="c02e5-103">Beregn kapasitetsbelastning</span><span class="sxs-lookup"><span data-stu-id="c02e5-103">Calculate capacity load</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="c02e5-104">I Aktivastyring kan du beregne kapasitetsbelastning på:</span><span class="sxs-lookup"><span data-stu-id="c02e5-104">In Asset Management, you can calculate capacity load on:</span></span>

- <span data-ttu-id="c02e5-105">linjer for vedlikeholdsplan</span><span class="sxs-lookup"><span data-stu-id="c02e5-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="c02e5-106">arbeidsordrer som ennå ikke er planlagt</span><span class="sxs-lookup"><span data-stu-id="c02e5-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="c02e5-107">planlagte arbeidsordrer</span><span class="sxs-lookup"><span data-stu-id="c02e5-107">scheduled work orders</span></span>

<span data-ttu-id="c02e5-108">Dette er nyttig hvis du vil ha en oversikt over forventet kapasitetsbelastning for en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="c02e5-108">This is useful if you want to get an overview of expected capacity load for a specific period.</span></span> <span data-ttu-id="c02e5-109">Beregning av kapasitetsbelastning kan utføres for alle aktiva eller valgte aktiva.</span><span class="sxs-lookup"><span data-stu-id="c02e5-109">Calculation of capacity load can be done on all assets or selected assets.</span></span> <span data-ttu-id="c02e5-110">Du kan også foreta en beregning av aktiviteter for vedlikeholdsnedetid eller arbeidsordrepuljer.</span><span class="sxs-lookup"><span data-stu-id="c02e5-110">You can also make a calculation on maintenance downtime activities or work order pools.</span></span>

1. <span data-ttu-id="c02e5-111">Klikk på **Aktivastyring** > **Forespørsler** > **Kapasitetsbelastning** eller **Aktivastyring** > **Felles** > **Arbeidsordrepuljer** > **Alle arbeidsordrepuljer** / **Aktive arbeidsordrepuljer** > velg arbeidsordrepulje i listen > **Kapasitetsbelastning**-knappen, eller **Aktivastyring** > **Felles** > **Aktiviteter for vedlikeholdsnedetid** > **Alle aktiviteter for vedlikeholdsnedetid** / **Aktive aktiviteter for vedlikeholdsnedetid** > velg vedlikeholdsaktivitet i listen > **Kapasitetsbelastning**-knappen.</span><span class="sxs-lookup"><span data-stu-id="c02e5-111">Click **Asset management** > **Inquiries** > **Capacity load**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance activity in the list > **Capacity load** button.</span></span>

2. <span data-ttu-id="c02e5-112">I dialogboksen **Beregn kapasitetsbelastning** velger du en periode for beregningen i feltene **Start dato/klokkeslett** og **Sluttdato/-klokkeslett**.</span><span class="sxs-lookup"><span data-stu-id="c02e5-112">In the **Calculate capacity load** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="c02e5-113">Velg "Ja" på veksleknappen **Inkluder vedlikeholdsplan** hvis du vil inkludere vedlikeholdsplanlinjer i beregningen.</span><span class="sxs-lookup"><span data-stu-id="c02e5-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the calculation.</span></span>

4. <span data-ttu-id="c02e5-114">Velg "Ja" på veksleknappen **Inkluder arbeidsordre** hvis du vil inkludere arbeidsordrejobber i beregningen.</span><span class="sxs-lookup"><span data-stu-id="c02e5-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the calculation.</span></span>

5. <span data-ttu-id="c02e5-115">Du kan bruke **Nivå**-feltet til å angi hvor detaljerte kapasitetsbelastningslinjene skal være når det gjelder arbeidssted.</span><span class="sxs-lookup"><span data-stu-id="c02e5-115">You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="c02e5-116">Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle vedlikeholdsplanlinjene og arbeidsordrene for et arbeidssted på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå.</span><span class="sxs-lookup"><span data-stu-id="c02e5-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="c02e5-117">Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle vedlikeholdsplanlinjene og alle arbeidsordrene på alle arbeidsstedsnivåene de er relatert til.</span><span class="sxs-lookup"><span data-stu-id="c02e5-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="c02e5-118">Klikk på **OK** for å starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="c02e5-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="c02e5-119">I **Grupper etter...**-gruppene klikker du de relevante knappene for å vise det nødvendige detaljnivået for beregningen.</span><span class="sxs-lookup"><span data-stu-id="c02e5-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="c02e5-120">I skjermbildet nedenfor er de valgte **Grupper etter**-knappene uthevet med blått.</span><span class="sxs-lookup"><span data-stu-id="c02e5-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="c02e5-121">Klikk på en knapp for å aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="c02e5-121">Click on a button to activate or deactivate it.</span></span>

    ![Figur 1](media/01-capacity-planning.png)

>[!NOTE]
><span data-ttu-id="c02e5-123">Hvis du bare vil fokusere på kapasitetsplanlegging i forbindelse med planlagte arbeidsordrer, kan du se [Beregne kapasitetsbelastning på planlagte arbeidsordrer](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span><span class="sxs-lookup"><span data-stu-id="c02e5-123">If you want to focus only on capacity planning regarding scheduled work orders, see [Calculate capacity load on scheduled work orders](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]