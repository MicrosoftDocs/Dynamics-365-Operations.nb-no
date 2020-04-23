---
title: Beregn kapasitetsbelastning
description: Dette emnet forklarer hvordan du beregner kapasitetsbelastning i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
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
ms.openlocfilehash: 2ddce7d3076d44b969cfb4c52462f92ed7f6db1d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216488"
---
# <a name="calculate-capacity-load"></a><span data-ttu-id="7fcc7-103">Beregn kapasitetsbelastning</span><span class="sxs-lookup"><span data-stu-id="7fcc7-103">Calculate capacity load</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="7fcc7-104">I Aktivastyring kan du beregne kapasitetsbelastning på:</span><span class="sxs-lookup"><span data-stu-id="7fcc7-104">In Asset Management, you can calculate capacity load on:</span></span>

- <span data-ttu-id="7fcc7-105">linjer for vedlikeholdsplan</span><span class="sxs-lookup"><span data-stu-id="7fcc7-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="7fcc7-106">arbeidsordrer som ennå ikke er planlagt</span><span class="sxs-lookup"><span data-stu-id="7fcc7-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="7fcc7-107">planlagte arbeidsordrer</span><span class="sxs-lookup"><span data-stu-id="7fcc7-107">scheduled work orders</span></span>

<span data-ttu-id="7fcc7-108">Dette er nyttig hvis du vil ha en oversikt over forventet kapasitetsbelastning for en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-108">This is useful if you want to get an overview of expected capacity load for a specific period.</span></span> <span data-ttu-id="7fcc7-109">Beregning av kapasitetsbelastning kan utføres for alle aktiva eller valgte aktiva.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-109">Calculation of capacity load can be done on all assets or selected assets.</span></span> <span data-ttu-id="7fcc7-110">Du kan også foreta en beregning av aktiviteter for vedlikeholdsnedetid eller arbeidsordrepuljer.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-110">You can also make a calculation on maintenance downtime activities or work order pools.</span></span>

1. <span data-ttu-id="7fcc7-111">Klikk **Aktivastyring** > **Forespørsler** > **Kapasitetsbelastning** eller **Aktivastyring** > **Felles** > **Arbeidsordrepuljer** > **Alle arbeidsordrepuljer** / **Aktive arbeidsordrepuljer** > velg arbeidsordrepulje i listen > **Kapasitetsbelastning**-knappen, eller **Aktivastyring** > **Felles** > **Aktiviteter for vedlikeholdsnedetid** > **Alle aktiviteter for vedlikeholdsnedetid** / **Aktive aktiviteter for vedlikeholdsnedetid** > velg vedlikeholdsaktivitet i listen > **Kapasitetsbelastning**-knappen.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-111">Click **Asset management** > **Inquiries** > **Capacity load**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance activity in the list > **Capacity load** button.</span></span>

2. <span data-ttu-id="7fcc7-112">I dialogboksen **Beregn kapasitetsbelastning** velger du en periode for beregningen i feltene **Start dato/klokkeslett** og **Sluttdato/-klokkeslett**.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-112">In the **Calculate capacity load** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="7fcc7-113">Velg "Ja" på veksleknappen **Inkluder vedlikeholdsplan** hvis du vil inkludere vedlikeholdsplanlinjer i beregningen.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the calculation.</span></span>

4. <span data-ttu-id="7fcc7-114">Velg "Ja" på veksleknappen **Inkluder arbeidsordre** hvis du vil inkludere arbeidsordrejobber i beregningen.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the calculation.</span></span>

5. <span data-ttu-id="7fcc7-115">Du kan bruke **Nivå**-feltet til å angi hvor detaljerte kapasitetsbelastningslinjene skal være når det gjelder arbeidssted.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-115">You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="7fcc7-116">Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle vedlikeholdsplanlinjene og arbeidsordrene for et arbeidssted på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="7fcc7-117">Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle vedlikeholdsplanlinjene og alle arbeidsordrene på alle arbeidsstedsnivåene de er relatert til.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="7fcc7-118">Klikk på **OK** for å starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="7fcc7-119">I **Grupper etter...**-gruppene klikker du de relevante knappene for å vise det nødvendige detaljnivået for beregningen.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="7fcc7-120">I skjermbildet nedenfor er de valgte **Grupper etter**-knappene uthevet med blått.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="7fcc7-121">Klikk på en knapp for å aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-121">Click on a button to activate or deactivate it.</span></span>

    ![Figur 1](media/01-capacity-planning.png)

>[!NOTE]
><span data-ttu-id="7fcc7-123">Hvis du bare vil fokusere på kapasitetsplanlegging i forbindelse med planlagte arbeidsordrer, kan du se [Beregne kapasitetsbelastning på planlagte arbeidsordrer](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span><span class="sxs-lookup"><span data-stu-id="7fcc7-123">If you want to focus only on capacity planning regarding scheduled work orders, see [Calculate capacity load on scheduled work orders](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span></span>

