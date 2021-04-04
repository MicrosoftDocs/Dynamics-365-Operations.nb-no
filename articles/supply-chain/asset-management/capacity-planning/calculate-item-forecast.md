---
title: Beregn vareprognose
description: Dette emnet forklarer hvordan du beregner vareprognose i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1cea3b6cfd42348285985122ae905f8ea9f3facb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260040"
---
# <a name="calculate-item-forecast"></a><span data-ttu-id="6fefc-103">Beregn vareprognose</span><span class="sxs-lookup"><span data-stu-id="6fefc-103">Calculate item forecast</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6fefc-104">På samme måte som du kan foreta beregninger av kapasitetsbelastning, som beskrevet i den forrige delen, kan du også foreta beregninger av vareprognoser:</span><span class="sxs-lookup"><span data-stu-id="6fefc-104">Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on:</span></span>

- <span data-ttu-id="6fefc-105">linjer for vedlikeholdsplan</span><span class="sxs-lookup"><span data-stu-id="6fefc-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="6fefc-106">arbeidsordrer som ennå ikke er planlagt</span><span class="sxs-lookup"><span data-stu-id="6fefc-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="6fefc-107">planlagte arbeidsordrer</span><span class="sxs-lookup"><span data-stu-id="6fefc-107">scheduled work orders</span></span>

<span data-ttu-id="6fefc-108">Dette er nyttig hvis du vil ha en oversikt over forventet vareforbruk (reservedeler i tillegg til andre varer som er nødvendige for å fullføre arbeidsordrer) for en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="6fefc-108">This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period.</span></span> <span data-ttu-id="6fefc-109">Beregning av vareprognose kan utføres for alle aktiva eller valgte aktiva.</span><span class="sxs-lookup"><span data-stu-id="6fefc-109">Calculation of item forecast can be done on all assets or selected assets.</span></span> <span data-ttu-id="6fefc-110">Du kan også foreta en beregning av en aktivitet for vedlikeholdsnedetid (**Alle aktiviteter for vedlikeholdsnedetid** eller **Aktive aktiviteter for vedlikeholdsnedetid**), eller en arbeidsordrepulje (**Alle arbeidsordrepuljer** eller **Aktive arbeidsordrepuljer**).</span><span class="sxs-lookup"><span data-stu-id="6fefc-110">You can also make a calculation on a maintenance downtime activity (**All maintenance downtime activities** or **Active maintenance downtime activities**), or on a work order pool (**All work order pools** or **Active work order pools**).</span></span>

1. <span data-ttu-id="6fefc-111">Klikk på **Aktivastyring** > **Forespørsler** > **Vareprognose** eller **Aktivastyring** > **Felles** > **Arbeidsordrepuljer** > **Alle arbeidsordrepuljer** / **Aktive arbeidsordrepuljer** > velg arbeidsordrepulje i listen > **Vareprognose**-knappen, eller **Aktivastyring** > **Felles** > **Aktiviteter for vedlikeholdsnedetid** > **Alle aktiviteter for vedlikeholdsnedetid** / **Aktive aktiviteter for vedlikeholdsnedetid** > velg aktiviteter for vedlikeholdsnedetid i listen > **Vareprognose**-knappen.</span><span class="sxs-lookup"><span data-stu-id="6fefc-111">Click **Asset management** > **Inquiries** > **Item forecast**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance downtime activity in the list > **Item forecast** button.</span></span>

2. <span data-ttu-id="6fefc-112">I dialogboksen **Beregn vareprognose** velger du en periode for beregningen i feltene **Start dato/klokkeslett** og **Sluttdato/-klokkeslett**.</span><span class="sxs-lookup"><span data-stu-id="6fefc-112">In the **Calculate item forecast** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="6fefc-113">Velg "Ja" på veksleknappen **Inkluder vedlikeholdsplan** hvis du vil inkludere vedlikeholdsplanlinjer i prognoseberegningen.</span><span class="sxs-lookup"><span data-stu-id="6fefc-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the forecast calculation.</span></span>

4. <span data-ttu-id="6fefc-114">Velg "Ja" på veksleknappen **Inkluder arbeidsordre** hvis du vil inkludere arbeidsordrejobber i prognoseberegningen.</span><span class="sxs-lookup"><span data-stu-id="6fefc-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the forecast calculation.</span></span>

5. <span data-ttu-id="6fefc-115">Du kan bruke **Nivå**-feltet til å angi hvor detaljert prognoselinjene skal være når det gjelder arbeidssted.</span><span class="sxs-lookup"><span data-stu-id="6fefc-115">You can use the **Level** field to indicate how detailed you want the item forecast lines to be regarding functional locations.</span></span> 

      <span data-ttu-id="6fefc-116">Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle vedlikeholdsplanlinjene og arbeidsordrene for et arbeidssted på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå.</span><span class="sxs-lookup"><span data-stu-id="6fefc-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
  
      <span data-ttu-id="6fefc-117">Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle vedlikeholdsplanlinjene og alle arbeidsordrene på alle arbeidsstedsnivåene de er relatert til.</span><span class="sxs-lookup"><span data-stu-id="6fefc-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="6fefc-118">Klikk på **OK** for å starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="6fefc-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="6fefc-119">I **Grupper etter...**-gruppene klikker du de relevante knappene for å vise det nødvendige detaljnivået for beregningen.</span><span class="sxs-lookup"><span data-stu-id="6fefc-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="6fefc-120">I skjermbildet nedenfor er de valgte **Grupper etter**-knappene uthevet med blått.</span><span class="sxs-lookup"><span data-stu-id="6fefc-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="6fefc-121">Klikk på en knapp for å aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="6fefc-121">Click on a button to activate or deactivate it.</span></span>

8. <span data-ttu-id="6fefc-122">Klikk på **Vis dimensjoner**-knappen hvis du vil se produkt-, lagrings- eller sporingsdimensjonene som er knyttet til varene.</span><span class="sxs-lookup"><span data-stu-id="6fefc-122">Click the **Display dimensions** button if you want to see the product, storage, or tracking dimensions related to the items.</span></span> <span data-ttu-id="6fefc-123">Merk av i de aktuelle avmerkingsboksene, og klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="6fefc-123">Select the relevant check boxes, and click **OK**.</span></span>

![Figur 1](media/02-capacity-planning.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]