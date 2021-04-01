---
title: Vedlikeholdsplan
description: Dette emnet beskriver vedlikeholdsplan i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 89938a4c5fd9a520c6582215a438670f73085228
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252948"
---
# <a name="maintenance-schedule"></a><span data-ttu-id="57237-103">Vedlikeholdsplan</span><span class="sxs-lookup"><span data-stu-id="57237-103">Maintenance schedule</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="57237-104">Vedlikeholdsplanen inneholder en liste over alle forventede forebyggende vedlikeholdsplaner, vedlikeholdsforespørsler og vedlikeholdsrunder som skal utføres. Noen planleggingslinjer kan ha blitt konvertert til arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="57237-104">The maintenance schedule contains a list of all the expected preventive maintenance plans, maintenance requests, and maintenance rounds to be carried out. Some schedule lines may have been converted to work orders.</span></span>

<span data-ttu-id="57237-105">De fire visningene for vedlikeholdsplaner er litt forskjellige, avhengig av hvilke vedlikeholdsplanlinjer du vil se.</span><span class="sxs-lookup"><span data-stu-id="57237-105">The four maintenance schedule views are slightly different, depending on which maintenance schedule lines you want to see.</span></span>

| <span data-ttu-id="57237-106">Menyelement</span><span class="sxs-lookup"><span data-stu-id="57237-106">Menu item</span></span>                  | <span data-ttu-id="57237-107">Beskrivelse av innhold</span><span class="sxs-lookup"><span data-stu-id="57237-107">Description of contents</span></span>                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57237-108">Alle vedlikeholdsplaner</span><span class="sxs-lookup"><span data-stu-id="57237-108">All maintenance schedule</span></span>       | <span data-ttu-id="57237-109">Alle vedlikeholdsplanlinjene vises.</span><span class="sxs-lookup"><span data-stu-id="57237-109">All maintenance schedule lines are shown.</span></span>     |
| <span data-ttu-id="57237-110">Min aktivumplan</span><span class="sxs-lookup"><span data-stu-id="57237-110">My asset schedule</span></span>        | <span data-ttu-id="57237-111">Alle vedlikeholdsplanlinjer som inneholder aktiva som finnes på arbeidssteder du er tilknyttet som arbeider (oppsett i [Vedlikeholdspersoner og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md)), vises i denne listen.</span><span class="sxs-lookup"><span data-stu-id="57237-111">All maintenance schedule lines containing assets installed on functional locations to which you are related as a worker (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)) are shown in this list.</span></span> |
| <span data-ttu-id="57237-112">Åpne linjer for vedlikeholdsplan</span><span class="sxs-lookup"><span data-stu-id="57237-112">Open maintenance schedule lines</span></span> | <span data-ttu-id="57237-113">Vedlikeholdsplanlinjer med statusen Opprettet – betyr at de ennå ikke er konvertert til en arbeidsordre eller forkastet – vises i denne listen.</span><span class="sxs-lookup"><span data-stu-id="57237-113">Maintenance schedule lines with status "Created" - meaning they have not yet been converted to a work order or discarded - are shown in this list.</span></span>                                            |
| <span data-ttu-id="57237-114">Åpne vedlikeholdsplansamlinger</span><span class="sxs-lookup"><span data-stu-id="57237-114">Open maintenance schedule pools</span></span> | <span data-ttu-id="57237-115">Vedlikeholdsplanlinjer relatert til en arbeidsordrepulje vises i denne listen.</span><span class="sxs-lookup"><span data-stu-id="57237-115">Maintenance schedule lines related to a work order pool are shown in this list.</span></span>                                                                                                                  |

>[!NOTE]
><span data-ttu-id="57237-116">Hvis en vedlikeholdsplanlinje er inkludert i flere arbeidsordrepuljer (se [Arbeidsordrepuljer](../work-orders/work-order-pools.md)), vises én post for hver pulje i **Åpne vedlikeholdsplanpuljer**.</span><span class="sxs-lookup"><span data-stu-id="57237-116">If a maintenance schedule line is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="57237-117">Dette gjøres for å optimalisere filtreringsalternativene i arbeidsordrepuljer.</span><span class="sxs-lookup"><span data-stu-id="57237-117">This is done to optimize filtering options on work order pools.</span></span>

<span data-ttu-id="57237-118">Slik åpner du en vedlikeholdsplan:</span><span class="sxs-lookup"><span data-stu-id="57237-118">To open a maintenance schedule:</span></span>

1. <span data-ttu-id="57237-119">Klikk på **Aktivastyring** > **Felles** > **Vedlikeholdsplan** > **Alle vedlikeholdsplaner** eller **Åpne vedlikeholdsplanlinjer** eller **Åpne vedlikeholdsplanpuljer**.</span><span class="sxs-lookup"><span data-stu-id="57237-119">Click **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="57237-120">Hvis du vil oppdatere vedlikeholdsplanen, klikker du på **Vedlikeholdsplan** eller **Vedlikeholdsrunder**.</span><span class="sxs-lookup"><span data-stu-id="57237-120">To update the maintenance schedule, click **Maintenance plan** or **Maintenance rounds**.</span></span> 

3. <span data-ttu-id="57237-121">Du kan redigere en vedlikeholdsplanlinje ved å merke den og klikke på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="57237-121">You can edit a maintenance schedule line by selecting it and clicking **Edit**.</span></span> <span data-ttu-id="57237-122">Du kan for eksempel enkelt oppdatere servicenivået eller arbeideren som er ansvarlig for jobben.</span><span class="sxs-lookup"><span data-stu-id="57237-122">For example, you can easily update the service level or the worker responsible for the job.</span></span> <span data-ttu-id="57237-123">Du kan bare redigere vedlikeholdsplanlinjer som ennå ikke er koblet til en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="57237-123">You can only edit maintenance schedule lines that have not yet been connected to a work order.</span></span>

4. <span data-ttu-id="57237-124">Du kan slette en vedlikeholdsplanlinje ved å velge den på listesiden og klikke på **Slett**.</span><span class="sxs-lookup"><span data-stu-id="57237-124">You can delete a maintenance schedule line by selecting it in the list page and clicking **Delete**.</span></span>

5. <span data-ttu-id="57237-125">Du kan forkaste en vedlikeholdsplanlinje ved å velge den på listesiden og klikke på **Forkast**.</span><span class="sxs-lookup"><span data-stu-id="57237-125">You can discard a maintenance schedule line by selecting it in the list page and clicking **Discard**.</span></span> <span data-ttu-id="57237-126">Denne funksjonen er nyttig hvis for eksempel et aktivum har en vedlikeholdsplan for 2 000 km og en vedlikeholdsplan for 10 000 km.</span><span class="sxs-lookup"><span data-stu-id="57237-126">This function is useful if, for example, an asset has a 2,000 km maintenance plan and a 10,000 km maintenance plan.</span></span> <span data-ttu-id="57237-127">Da vil du kanskje forkaste linjen som er opprettet fra 2 000 km-vedlikeholdsplanen når den sammenfaller med 10 000 km, 20 000 km, 30 000 km og så videre.</span><span class="sxs-lookup"><span data-stu-id="57237-127">Then, you may want to discard the line created from the 2,000 km maintenance plan when it coincides with 10,000 km, 20,000 km, 30,000 km, and so on.</span></span> <span data-ttu-id="57237-128">Hvis du forkaster en vedlikeholdsplanlinje knyttet til en vedlikeholdsplan, vil denne linjen aldri vises igjen når denne vedlikeholdsplanen planlegges.</span><span class="sxs-lookup"><span data-stu-id="57237-128">If you discard a maintenance schedule line related to a maintenance plan, that line will never again appear when that maintenance plan is scheduled.</span></span>

6. <span data-ttu-id="57237-129">Du kan velge en rekke vedlikeholdsplanlinjer i **Alle vedlikeholdsplaner** og klikke på **Arbeidsordrepulje** hvis du vil at alle valgte linjer skal tas med i samme arbeidsordrepulje.</span><span class="sxs-lookup"><span data-stu-id="57237-129">You can select a number of maintenance schedule lines in **All maintenance schedule** and click **Work order pool**, if you want all selected lines to be included in the same work order pool.</span></span>

7. <span data-ttu-id="57237-130">Du kan velge en rekke vedlikeholdsplanlinjer i **Alle vedlikeholdsplaner** eller **Åpne vedlikeholdsplanlinjer** eller **Åpne vedlikeholdsplanpuljer** og klikke på **Juster plan** hvis du vil foreta de samme justeringene på flere linjer.</span><span class="sxs-lookup"><span data-stu-id="57237-130">You can select a number of maintenance schedule lines in **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** and click **Adjust schedule** if you want to make the same adjustments on several lines.</span></span> <span data-ttu-id="57237-131">Du kan endre forventet start- og sluttdato, servicenivå og ansvarlig vedlikeholdspersongruppe eller ansvarlig vedlikeholdsperson knyttet til de valgte vedlikeholdsplanlinjene.</span><span class="sxs-lookup"><span data-stu-id="57237-131">You can change expected start and end dates, service level, and the responsible maintenance worker group or responsible maintenance worker related to the selected maintenance schedule lines.</span></span>

- <span data-ttu-id="57237-132">Når en vedlikeholdsplanlinje er knyttet til en arbeidsordre, vises ID-en for arbeidsordren i **Arbeidsordre**-feltet.</span><span class="sxs-lookup"><span data-stu-id="57237-132">When a maintenance schedule line has been related to a work order, the work order ID will be displayed in the **Work order** field.</span></span>  
- <span data-ttu-id="57237-133">I **Alle aktiva**-detaljvisningen > **Vedlikeholdsplaner for aktivum**-hurtigfanen kan du velge vedlikeholdsplaner for aktivumet.</span><span class="sxs-lookup"><span data-stu-id="57237-133">In **All assets** details view > **Asset maintenance plans** FastTab, you can select maintenance plans for the asset.</span></span> <span data-ttu-id="57237-134">Hvis du senere sletter en vedlikeholdsplanlinje knyttet til et aktivum i **Alle aktiva**, sletter du også automatisk alle vedlikeholdsplanlinjer med statusen "Opprettet" som er opprettet basert på denne vedlikeholdsplanen.</span><span class="sxs-lookup"><span data-stu-id="57237-134">Later, if you delete a maintenance plan line related to an asset in **All assets**, you also automatically delete all maintenance schedule lines with status "Created" that have been created based on that maintenance plan.</span></span> <span data-ttu-id="57237-135">Se også [Opprette et aktivum](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="57237-135">See also [Create an asset](../objects/create-an-object.md).</span></span>

<span data-ttu-id="57237-136">Illustrasjonen nedenfor viser listesiden **Alle vedlikeholdsplaner**.</span><span class="sxs-lookup"><span data-stu-id="57237-136">The illustration below shows the **All maintenance schedule** list page.</span></span>

![Figur 1](media/16-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]