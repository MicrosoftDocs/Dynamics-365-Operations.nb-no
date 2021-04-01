---
title: Kostnader for vedlikeholdsplan
description: Dette emnet beskriver kostnader for vedlikeholdsplan i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9686efb228e123671ba93a37480d2daac8d038a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252972"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="cb67f-103">Kostnader for vedlikeholdsplan</span><span class="sxs-lookup"><span data-stu-id="cb67f-103">Maintenance schedule cost</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="cb67f-104">I Aktivastyring kan du beregne budsjettkostnader på vedlikeholdsplanlinjer.</span><span class="sxs-lookup"><span data-stu-id="cb67f-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="cb67f-105">Dette er nyttig hvis du vil ha en oversikt over forventede kostnader, for eksempel kostnader knyttet til planlagte forebyggende vedlikeholdsjobber for neste år.</span><span class="sxs-lookup"><span data-stu-id="cb67f-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="cb67f-106">Beregningene er basert på eksisterende vedlikeholdsplanlinjer av typen Vedlikeholdsplaner, Vedlikeholdsrunder og Vedlikeholdsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="cb67f-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="cb67f-107">Klikk på **Aktivastyring** > **Forespørsler** > **Aktiva** > **Kostnader for vedlikeholdsplan**.</span><span class="sxs-lookup"><span data-stu-id="cb67f-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="cb67f-108">I dialogboksen **Kostnader for vedlikeholdsplan** kan du velge et **finansdimensjonssett** hvis du vil se kostnader gruppert i finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="cb67f-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="cb67f-109">Finansdimensjonssett blir definert i **Finans** > **Kontoplan** > **Dimensjoner** > **Finansdimensjonssett**.</span><span class="sxs-lookup"><span data-stu-id="cb67f-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="cb67f-110">Du kan bruke **Nivå**-feltet til å angi hvor detaljert vedlikeholdsplanlinjene skal være når det gjelder arbeidssted.</span><span class="sxs-lookup"><span data-stu-id="cb67f-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="cb67f-111">Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle vedlikeholdsplanlinjene for et arbeidssted på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå.</span><span class="sxs-lookup"><span data-stu-id="cb67f-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="cb67f-112">Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle vedlikeholdsplanlinjene på alle arbeidsstedsnivåene de er relatert til.</span><span class="sxs-lookup"><span data-stu-id="cb67f-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="cb67f-113">Hvis du vil gjøre en beregning for bestemte aktiva , klikker du på **Filter** i hurtigfanen **Poster som skal inkluderes**, og velger de relevante aktivaene.</span><span class="sxs-lookup"><span data-stu-id="cb67f-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="cb67f-114">Hvis det er nødvendig, kan du også angi en **Forventet startdato** for kostberegningen, eller velge en annen **Status** for kostberegningen.</span><span class="sxs-lookup"><span data-stu-id="cb67f-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="cb67f-115">Klikk på **OK** for å starte kostberegningen.</span><span class="sxs-lookup"><span data-stu-id="cb67f-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="cb67f-116">I fanen **Kostnader for vedlikeholdsplan** > i **Grupper etter...**-handlingsrutegruppene klikker du på de relevante knappene for å vise det nødvendige detaljnivået for kostnadsberegningen.</span><span class="sxs-lookup"><span data-stu-id="cb67f-116">On the **Maintenance schedule cost** tab > in the **Group by...** Action Pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="cb67f-117">De valgte handlingsrutegruppeknappene er uthevet.</span><span class="sxs-lookup"><span data-stu-id="cb67f-117">The selected Action Pane group buttons are highlighted.</span></span> <span data-ttu-id="cb67f-118">Klikk på en knapp for å aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="cb67f-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="cb67f-119">Klikk på knappen **Beregn kostnad** hvis du vil foreta en ny kostberegning.</span><span class="sxs-lookup"><span data-stu-id="cb67f-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>

<span data-ttu-id="cb67f-120">Illustrasjonen nedenfor viser resultatet av en beregning av kostnader for vedlikeholdsplan.</span><span class="sxs-lookup"><span data-stu-id="cb67f-120">The illustration below shows the results of a maintenance schedule cost calculation.</span></span>

![Figur 1](media/17-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]