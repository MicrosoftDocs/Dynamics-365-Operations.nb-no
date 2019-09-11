---
title: Servicenivå og -beskrivelse
description: Dette emnet beskriver servicenivå og -beskrivelse i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e645c25208f55b1032bc7f7c181c72db7a2f265
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874653"
---
# <a name="service-level-and-description"></a><span data-ttu-id="a98c0-103">Servicenivå og -beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a98c0-103">Service level and description</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="a98c0-104">Når du oppretter en arbeidsordre, vil du kanskje definere servicenivåene og legge til en generell beskrivelse for den.</span><span class="sxs-lookup"><span data-stu-id="a98c0-104">When you create a work order, you might want to define the service levels for it and add a general description to it.</span></span> <span data-ttu-id="a98c0-105">Du kan opprette servicenivåer for arbeidsordrer på siden **Servicenivåer for arbeidsordrer** og beskrivelser på siden **Arbeidsordrebeskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="a98c0-105">You can create work order service levels on the **Work order service levels** page and descriptions on the **Work order description** page.</span></span>

## <a name="create-a-service-level"></a><span data-ttu-id="a98c0-106">Opprette et servicenivå</span><span class="sxs-lookup"><span data-stu-id="a98c0-106">Create a service level</span></span>

1. <span data-ttu-id="a98c0-107">Velg **Aktivastyring** \> **Oppsett** \> **Arbeidsordrer** \> **Servicenivå**.</span><span class="sxs-lookup"><span data-stu-id="a98c0-107">Select **Asset management** \> **Setup** \> **Work orders** \> **Service level**.</span></span>
2. <span data-ttu-id="a98c0-108">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a98c0-108">Select **New**.</span></span>
3. <span data-ttu-id="a98c0-109">I **Servicenivå**-feltet angir du servicenivået (for eksempel et tall).</span><span class="sxs-lookup"><span data-stu-id="a98c0-109">In the **Service level** field, enter the service level (for example, a number).</span></span>
4. <span data-ttu-id="a98c0-110">Angi et navn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a98c0-110">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="a98c0-111">I hurtigfanen **Arbeidsordrer** kan du definere forventede start- og sluttdatoer og -klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="a98c0-111">On the **Work orders** FastTab, you can define expected start and end dates and times.</span></span> <span data-ttu-id="a98c0-112">Feltene i denne hurtigfanen definerer perioden som arbeidsordrer skal startes og avsluttes i.</span><span class="sxs-lookup"><span data-stu-id="a98c0-112">The fields on this FastTab define the period that work orders should be started and ended during.</span></span> <span data-ttu-id="a98c0-113">De brukes for arbeidsordrer som opprettes manuelt, og arbeidsordrer som opprettes basert på vedlikeholdsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="a98c0-113">They are used for work orders that are manually created and work orders that are created based on maintenance requests.</span></span> 

5. <span data-ttu-id="a98c0-114">I feltet **Startdag** angir du et antall dager for å definere perioden som arbeidsordren skal starte i.</span><span class="sxs-lookup"><span data-stu-id="a98c0-114">In the **Start day** field, enter a number of days to define the period that the work order should start during.</span></span> <span data-ttu-id="a98c0-115">Antallet dager beregnes fra opprettelsesdatoen for arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="a98c0-115">The number of days is calculated from the creation date of the work order.</span></span> <span data-ttu-id="a98c0-116">Hvis for eksempel arbeidsordren skal starte når den opprettes, skriver du inn **0**.</span><span class="sxs-lookup"><span data-stu-id="a98c0-116">For example, if the work order should start when it's created, enter **0**.</span></span> <span data-ttu-id="a98c0-117">Hvis arbeidsordren skal starte innen én uke etter den opprettes, skriver du inn **7**.</span><span class="sxs-lookup"><span data-stu-id="a98c0-117">If the work order should start within one week after it's created, enter **7**.</span></span>
6. <span data-ttu-id="a98c0-118">Hvis du vil angi et starttidspunkt for arbeidsordren, i tillegg til en startdato, setter du alternativet **Angi starttidspunkt** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a98c0-118">To set a start time for the work order, in addition to a start date, set the **Set start time** option to **Yes**.</span></span> <span data-ttu-id="a98c0-119">Deretter angir du starttidspunktet i **Starttidspunkt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a98c0-119">Then enter the start time in the **Start time** field.</span></span> <span data-ttu-id="a98c0-120">Hvis du setter alternativet til **Nei**, brukes gjeldende tidspunkt på dagen.</span><span class="sxs-lookup"><span data-stu-id="a98c0-120">If you set the option to **No**, the current time of day is used.</span></span>
7. <span data-ttu-id="a98c0-121">I feltet **Sluttdag** angir du et antall dager for å definere perioden som arbeidsordren skal avsluttes i.</span><span class="sxs-lookup"><span data-stu-id="a98c0-121">In the **End day** field, enter a number of days to define the period that the work order should end during.</span></span> <span data-ttu-id="a98c0-122">Antallet dager beregnes fra startdatoen for arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="a98c0-122">The number of days is calculated from the start date of the work order.</span></span> <span data-ttu-id="a98c0-123">Hvis for eksempel arbeidsordren skal slutte innen én uke fra startdatoen, skriver du inn **7**.</span><span class="sxs-lookup"><span data-stu-id="a98c0-123">For example, if the work order should end within one week of its start date, enter **7**.</span></span>
8. <span data-ttu-id="a98c0-124">Hvis du vil angi et sluttidspunkt for arbeidsordren, i tillegg til en sluttdato, setter du alternativet **Angi sluttidspunkt** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a98c0-124">To set an end time for the work order, in addition to an end date, set the **Set end time** option to **Yes**.</span></span> <span data-ttu-id="a98c0-125">Deretter angir du sluttidspunktet i **Sluttidspunkt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a98c0-125">Then enter the end time in the **End time** field.</span></span> <span data-ttu-id="a98c0-126">Hvis du setter alternativet til **Nei**, brukes gjeldende tidspunkt på dagen.</span><span class="sxs-lookup"><span data-stu-id="a98c0-126">If you set the option to **No**, the current time of day is used.</span></span>
9. <span data-ttu-id="a98c0-127">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a98c0-127">Select **Save**.</span></span>

![Figur 1](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a><span data-ttu-id="a98c0-129">Opprett en beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a98c0-129">Create a description</span></span>

1. <span data-ttu-id="a98c0-130">Velg **Aktivastyring** \> **Oppsett** \> **Arbeidsordrer** \> **Beskrivelser**.</span><span class="sxs-lookup"><span data-stu-id="a98c0-130">Select **Asset management** \> **Setup** \> **Work orders** \> **Descriptions**.</span></span>
2. <span data-ttu-id="a98c0-131">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a98c0-131">Select **New**.</span></span>
3. <span data-ttu-id="a98c0-132">Angi beskrivelsen i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a98c0-132">In the **Description** field, enter the description.</span></span>
4. <span data-ttu-id="a98c0-133">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a98c0-133">Select **Save**.</span></span>
