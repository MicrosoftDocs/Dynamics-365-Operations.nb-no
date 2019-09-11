---
title: Brukssted for vare
description: Dette emnet beskriver hvordan du får oversikt over hvor en vare brukes i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: 84ab803aedf5b803b6c5f39ff1907726335cb45d
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918332"
---
# <a name="item-where-used"></a><span data-ttu-id="c07c4-103">Brukssted for vare</span><span class="sxs-lookup"><span data-stu-id="c07c4-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="c07c4-104">Du kan foreta en beregning for en bestemt vare for å få en oversikt over hvor i Aktivastyring varen er brukt.</span><span class="sxs-lookup"><span data-stu-id="c07c4-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="c07c4-105">Resultatene viser konteksten som varen ble brukt i, i løpet av varens levetid.</span><span class="sxs-lookup"><span data-stu-id="c07c4-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="c07c4-106">Siden **Vare der brukt** kan åpnes fra hovedmenyen for Aktivastyring, og kan også nås fra følgende sider:</span><span class="sxs-lookup"><span data-stu-id="c07c4-106">The **Item where used** page can be opened from the main Asset management menu, and it can also be accessed from the following pages:</span></span>

[<span data-ttu-id="c07c4-107">Stykkliste for aktiva</span><span class="sxs-lookup"><span data-stu-id="c07c4-107">Asset BOM</span></span>](../objects/object-BOM.md)

[<span data-ttu-id="c07c4-108">Reservedeler på aktivatypestandarder</span><span class="sxs-lookup"><span data-stu-id="c07c4-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md)

[<span data-ttu-id="c07c4-109">Vareprognose i prognose for vedlikeholdsjobbtypestandarder</span><span class="sxs-lookup"><span data-stu-id="c07c4-109">Item forecast on Maintenance job type defaults forecast</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

[<span data-ttu-id="c07c4-110">Prognose for vedlikehold av arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="c07c4-110">Work order maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

[<span data-ttu-id="c07c4-111">Innkjøpsrekvisisjon for arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="c07c4-111">Work order purchase requisition</span></span>](../work-orders/procurement.md)

[<span data-ttu-id="c07c4-112">Innkjøp for arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="c07c4-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="c07c4-113">Gjøre en beregning for vare-der-brukt</span><span class="sxs-lookup"><span data-stu-id="c07c4-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="c07c4-114">Klikk på **Aktivastyring** > **Forespørsler** > **Vare der brukt**, eller velg **Vare der brukt**-knappen på en av sidene som er nevnt ovenfor.</span><span class="sxs-lookup"><span data-stu-id="c07c4-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="c07c4-115">I dialogboksen **Vare der brukt** velger du varen du vil gjøre beregningen for, i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c07c4-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="c07c4-116">Du kan bruke **Nivå**-feltet til å angi hvor detaljert varelinjene skal være når det gjelder arbeidssted.</span><span class="sxs-lookup"><span data-stu-id="c07c4-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> <span data-ttu-id="c07c4-117">Hvis du for eksempel setter inn tallet 1 i feltet, og du har en flernivås arbeidsstedsstruktur, vises alle varelinjene for et arbeidssted på øverste nivå.</span><span class="sxs-lookup"><span data-stu-id="c07c4-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="c07c4-118">Derfor kan relasjon/antall på en linje tilføyes fra arbeidssteder på et lavere nivå.</span><span class="sxs-lookup"><span data-stu-id="c07c4-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="c07c4-119">Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle varelinjene på alle arbeidsstedsnivåene de er relatert til.</span><span class="sxs-lookup"><span data-stu-id="c07c4-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="c07c4-120">I **Inkluder**-delen velger du Ja på veksleknappene som du vil ta med i beregningen.</span><span class="sxs-lookup"><span data-stu-id="c07c4-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="c07c4-121">Klikk på **OK** for å starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="c07c4-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="c07c4-122">I kategorien **Vare der brukt** > **Grupper etter...**-handlingsrutegruppene velger du de relevante knappene for å vise det nødvendige detaljnivået for beregningen.</span><span class="sxs-lookup"><span data-stu-id="c07c4-122">On the **Item where used** tab > **Group by...** action pane groups, select the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="c07c4-123">De valgte handlingsrutegruppeknappene er uthevet.</span><span class="sxs-lookup"><span data-stu-id="c07c4-123">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="c07c4-124">Klikk på en knapp for å aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="c07c4-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="c07c4-125">Hvis du vil vise dimensjoner knyttet til varen, klikker du på **Visningsdimensjoner** og velger dimensjonene som skal vises.</span><span class="sxs-lookup"><span data-stu-id="c07c4-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

<span data-ttu-id="c07c4-126">I figuren nedenfor ser du et eksempel på en beregning for vare-der-brukt for varenummer 1000.</span><span class="sxs-lookup"><span data-stu-id="c07c4-126">In the figure below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![Figur 1](media/12-controlling-and-reporting.png)

