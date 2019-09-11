---
title: Opprette arbeidsordrer
description: Dette emnet forklarer hvordan du oppretter arbeidsordrer i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b23ed3251b2f6cf4f34b423ce2f85301d6ab31a1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875814"
---
# <a name="creating-work-orders"></a><span data-ttu-id="34a7b-103">Opprette arbeidsordrer</span><span class="sxs-lookup"><span data-stu-id="34a7b-103">Creating work orders</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="34a7b-104">Når du har planlagt forebyggende vedlikeholdsjobber, er neste trinn å opprette arbeidsordrer for jobbene.</span><span class="sxs-lookup"><span data-stu-id="34a7b-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="34a7b-105">Dette gjøres i en av vedlikeholdsplanene.</span><span class="sxs-lookup"><span data-stu-id="34a7b-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="34a7b-106">De planlagte jobbene i en vedlikeholdsplan kan ha forskjellige referansetyper:</span><span class="sxs-lookup"><span data-stu-id="34a7b-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="34a7b-107">Referansetype</span><span class="sxs-lookup"><span data-stu-id="34a7b-107">Reference type</span></span> | <span data-ttu-id="34a7b-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="34a7b-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34a7b-109">Vedlikeholdsplaner</span><span class="sxs-lookup"><span data-stu-id="34a7b-109">Maintenance plans</span></span>     | <span data-ttu-id="34a7b-110">Forebyggende vedlikeholdsjobber basert på vedlikeholdsplantypene "tid" eller "teller".</span><span class="sxs-lookup"><span data-stu-id="34a7b-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="34a7b-111">Vedlikeholdsrunder</span><span class="sxs-lookup"><span data-stu-id="34a7b-111">Maintenance rounds</span></span>    | <span data-ttu-id="34a7b-112">Forebyggende vedlikeholdsjobber som inneholder flere anleggsmidler som krever en lignende type vedlikehold.</span><span class="sxs-lookup"><span data-stu-id="34a7b-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="34a7b-113">Forespørsel om vedlikehold</span><span class="sxs-lookup"><span data-stu-id="34a7b-113">Maintenance request</span></span>   | <span data-ttu-id="34a7b-114">Manuelt opprettet forespørsel om vedlikehold eller reparasjon av et anleggsmiddel, som kan konverteres til en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="34a7b-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="34a7b-115">Klikk **Aktivastyring** > **Felles** > **Alle vedlikeholdsplaner** eller **Åpne vedlikeholdsplanlinjer** eller **Åpne vedlikeholdsplanpuljer**.</span><span class="sxs-lookup"><span data-stu-id="34a7b-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="34a7b-116">Velg de planlagte vedlikeholdsjobbene du vil opprette en arbeidsordre for, og klikk på **Arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="34a7b-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="34a7b-117">Det totale antallet prognosetimer for de valgte linjene vises i feltet **Vedlikeholdsprognosetimer**.</span><span class="sxs-lookup"><span data-stu-id="34a7b-117">The total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="34a7b-118">I **Parametere**-delen velger du hvor mange arbeidsordrer som skal opprettes.</span><span class="sxs-lookup"><span data-stu-id="34a7b-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="34a7b-119">Du kan opprette én arbeidsordre per vedlikeholdsplanlinje, eller en rekke arbeidsordrer, basert på valgene i delen **Én arbeidsordre per**.</span><span class="sxs-lookup"><span data-stu-id="34a7b-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="34a7b-120">Velg en **Arbeidsordretype** som skal brukes på alle arbeidsordrene du oppretter.</span><span class="sxs-lookup"><span data-stu-id="34a7b-120">Select a **Work order type** that will be used on all the work orders you create.</span></span>

5. <span data-ttu-id="34a7b-121">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="34a7b-121">Click **OK**.</span></span> <span data-ttu-id="34a7b-122">Én eller flere arbeidsordrer opprettes.</span><span class="sxs-lookup"><span data-stu-id="34a7b-122">One or more work orders are created.</span></span>

![Figur 1](media/18-preventive-maintenance.png)

