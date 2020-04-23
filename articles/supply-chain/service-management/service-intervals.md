---
title: Serviceintervaller
description: Serviceintervallet viser hvor ofte serviceordrelinjene skal opprettes for serviceavtalelinjene når du oppretter serviceordrer.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5766d8ce1fa382f3f014e160d311b2dfab2bf774
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216281"
---
# <a name="service-intervals"></a><span data-ttu-id="e4681-103">Serviceintervaller</span><span class="sxs-lookup"><span data-stu-id="e4681-103">Service intervals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4681-104">Serviceavtaleintervallet viser hvor ofte serviceordrelinjene skal opprettes for serviceavtalelinjene når du oppretter serviceordrer automatisk.</span><span class="sxs-lookup"><span data-stu-id="e4681-104">The service agreement interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders automatically.</span></span>

<span data-ttu-id="e4681-105">Når du oppretter serviceordrer automatisk, opprettes serviceordrelinjer i samsvar med det intervallet du har angitt for serviceavtalelinjen fra startdatoen for avtalelinjen.</span><span class="sxs-lookup"><span data-stu-id="e4681-105">When you create service orders automatically, service order lines are created according to the interval that you have specified for the service agreement line from the start date of the agreement line.</span></span>

<span data-ttu-id="e4681-106">Hvis **Intervall**-feltet for en serviceavtalelinje på **Serviceavtaler**-siden er tomt, gjelder linjen et engangstilfelle, og brukes ikke til å opprette gjentatte serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="e4681-106">If the **Interval** field of a service agreement line in the **Service agreements** page is blank, the line is a one-time event, and it is not used to create service orders repeatedly.</span></span>

## <a name="example"></a><span data-ttu-id="e4681-107">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e4681-107">Example</span></span>

<span data-ttu-id="e4681-108">Dette eksemplet viser hvordan et serviceintervall påvirker serviceavtalelinjer og serviceordrelinjer i en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="e4681-108">This example illustrates how a service interval will affect service agreement lines and service order lines on a service order.</span></span>

### <a name="create-a-service-agreement"></a><span data-ttu-id="e4681-109">Opprette en serviceavtale</span><span class="sxs-lookup"><span data-stu-id="e4681-109">Create a service agreement</span></span>

<span data-ttu-id="e4681-110">Først oppretter du en serviceavtale og setter **Kombiner serviceordrer** til **Etter serviceavtale**.</span><span class="sxs-lookup"><span data-stu-id="e4681-110">First, you create a service agreement and set the **Combine service orders** option to **By service agreement**.</span></span>

1. <span data-ttu-id="e4681-111">Klikk på **Serviceavtaler**.</span><span class="sxs-lookup"><span data-stu-id="e4681-111">Click **Service agreements**</span></span>
2. <span data-ttu-id="e4681-112">I **Handlingsruten** i **Serviceavtale**-kategorien i **Ny**-gruppen klikker du **Serviceavtale** for å opprette en ny serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="e4681-112">On the **Action Pane**, on the **Service agreement** tab, in the **New** group, click **Service agreement** to create a new service agreement.</span></span>
3. <span data-ttu-id="e4681-113">Angi en beskrivelse, velg et prosjekt i **Prosjekt-ID**-feltet, og angi en dato i **Startdato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e4681-113">Enter a description, select a project in the **Project ID** field, and enter a date in the **Start date** field.</span></span>
4. <span data-ttu-id="e4681-114">I **Kombiner serviceordrer**-feltet velger du **Etter serviceavtale**.</span><span class="sxs-lookup"><span data-stu-id="e4681-114">In the **Combine service orders** field, select **By service agreement**.</span></span>

<span data-ttu-id="e4681-115">Du har nå opprettet følgende serviceavtale:</span><span class="sxs-lookup"><span data-stu-id="e4681-115">You have now created the following service agreement:</span></span>

| <span data-ttu-id="e4681-116">Project</span><span class="sxs-lookup"><span data-stu-id="e4681-116">Project</span></span>      | <span data-ttu-id="e4681-117">Startdato</span><span class="sxs-lookup"><span data-stu-id="e4681-117">Start date</span></span>                                                                         |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e4681-118">Ditt prosjekt</span><span class="sxs-lookup"><span data-stu-id="e4681-118">Your project</span></span> | <span data-ttu-id="e4681-119">Datoen du angav for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="e4681-119">The date you specified for the project.</span></span> <span data-ttu-id="e4681-120">I dette eksemplet brukes gjeldende dato.</span><span class="sxs-lookup"><span data-stu-id="e4681-120">In this example, the current date is used.</span></span> |

### <a name="create-a-service-agreement-line"></a><span data-ttu-id="e4681-121">Opprette en serviceavtalelinje</span><span class="sxs-lookup"><span data-stu-id="e4681-121">Create a service agreement line</span></span>

<span data-ttu-id="e4681-122">Deretter oppretter du en serviceavtalelinje som har transaksjonstypen **Time**.</span><span class="sxs-lookup"><span data-stu-id="e4681-122">Next, you create a service agreement line that has the transaction type **Hour**.</span></span>

<span data-ttu-id="e4681-123">For å fullføre denne delen, må du opprette et serviceintervall på 10 dager på **Serviceintervaller**-siden.</span><span class="sxs-lookup"><span data-stu-id="e4681-123">To complete this part of the example, you must create a service interval of 10 days in the **Service intervals** page.</span></span> 

1. <span data-ttu-id="e4681-124">Velg serviceavtalen du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="e4681-124">Select the service agreement that you just created.</span></span> 
2. <span data-ttu-id="e4681-125">På **Linjer**-hurtigkategorien, klikk **Legg til** for å opprette en ny linje i den nedre ruten på **Serviceavtaler**-siden.</span><span class="sxs-lookup"><span data-stu-id="e4681-125">On the **Lines** FastTab, click the **Add** button to create a new line in the lower pane of the **Service agreements** page.</span></span>
3. <span data-ttu-id="e4681-126">Velg **Time** i **Transaksjonstype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e4681-126">In the **Transaction type** field, select **Hour**.</span></span>
4. <span data-ttu-id="e4681-127">I **Arbeider**-feltet velger du arbeideren som skal levere servicen.</span><span class="sxs-lookup"><span data-stu-id="e4681-127">In the **Worker** field, select the worker who will deliver the service.</span></span>
5. <span data-ttu-id="e4681-128">Velg 10-dagersintervallet i feltet **Serviceintervall**.</span><span class="sxs-lookup"><span data-stu-id="e4681-128">In the **Service interval** field, select the 10 days interval.</span></span>

<span data-ttu-id="e4681-129">Du har nå opprettet en serviceavtalelinje med følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="e4681-129">You have now created a service agreement line with the following information:</span></span>

| <span data-ttu-id="e4681-130">transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="e4681-130">Transaction type</span></span> | <span data-ttu-id="e4681-131">Startdato</span><span class="sxs-lookup"><span data-stu-id="e4681-131">Start date</span></span>                               | <span data-ttu-id="e4681-132">Serviceintervall</span><span class="sxs-lookup"><span data-stu-id="e4681-132">Service interval</span></span> |
|------------------|------------------------------------------|------------------|
| <span data-ttu-id="e4681-133">Time</span><span class="sxs-lookup"><span data-stu-id="e4681-133">Hour</span></span>             | <span data-ttu-id="e4681-134">Den gjeldende datoen.</span><span class="sxs-lookup"><span data-stu-id="e4681-134">The current date.</span></span>                        | <span data-ttu-id="e4681-135">Hver 10. dag</span><span class="sxs-lookup"><span data-stu-id="e4681-135">Every 10 days</span></span>    |
| <span data-ttu-id="e4681-136">Arbeider</span><span class="sxs-lookup"><span data-stu-id="e4681-136">Worker</span></span>           | <span data-ttu-id="e4681-137">Arbeideren som skal utføre servicen.</span><span class="sxs-lookup"><span data-stu-id="e4681-137">The worker who will perform the service.</span></span> |                  |

<span data-ttu-id="e4681-138">Det er ikke angitt noe tidsvindu for linjen.</span><span class="sxs-lookup"><span data-stu-id="e4681-138">There is no time window specified for the line.</span></span> 

### <a name="create-planned-service-orders"></a><span data-ttu-id="e4681-139">Opprette planlagte serviceordrer</span><span class="sxs-lookup"><span data-stu-id="e4681-139">Create planned service orders</span></span>

<span data-ttu-id="e4681-140">Du kan nå opprette planlagte serviceordrer og serviceordrelinjer for kommende måned.</span><span class="sxs-lookup"><span data-stu-id="e4681-140">You can now create planned service orders and service order lines for the coming month.</span></span>

1. <span data-ttu-id="e4681-141">På **Serviceavtaler**-siden i **handlingsruten** i **Lever**-fanen, klikker du **Planlagte serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="e4681-141">In the **Service agreements** page, on the **Action Pane**, on the **Deliver** tab, click **Planned service orders**.</span></span>
2. <span data-ttu-id="e4681-142">På **Opprett serviceordrer**-siden skriver du inn gjeldende dato i **Fra dato**-feltet og en dato som er én måned fra gjeldende dato i **Til dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e4681-142">In the **Create service orders** page, enter the current date in the **From date** field and a date that is one month from the current date in the **To date** field.</span></span>
3. <span data-ttu-id="e4681-143">Sett **Time**-glidebryteren til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e4681-143">Set the **Hour** slider to **Yes**.</span></span> 
4. <span data-ttu-id="e4681-144">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4681-144">Click **OK**.</span></span>

<span data-ttu-id="e4681-145">Fordi det ikke finnes noen grupperinger i serviceordren (definert med alternativet **Etter serviceavtale** i feltet **Kombiner serviceordrer**), blir det opprettet én serviceordrelinje per serviceordre.</span><span class="sxs-lookup"><span data-stu-id="e4681-145">Because there is no grouping on the service order (defined by the **By service agreement** option in the **Combine service orders** field), one service order line is created per service order.</span></span>

### <a name="service-orders-created"></a><span data-ttu-id="e4681-146">Opprettede serviceordrer</span><span class="sxs-lookup"><span data-stu-id="e4681-146">Service orders created</span></span>

<span data-ttu-id="e4681-147">Tre serviceordrelinjer er opprettet innenfor tidsrammen du angav i dialogboksen **Opprett serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="e4681-147">Three service order lines have been created within the time frame that you specified in the **Create service orders** dialog box.</span></span> <span data-ttu-id="e4681-148">Du kan vise serviceordrelinjene på **Serviceavtaler**-siden (**Handlingsrute** \> **Lever**-kategorien \> **Vis**-knappen).</span><span class="sxs-lookup"><span data-stu-id="e4681-148">You can view the service order lines in the **Service agreements** page (**Action Pane** \> **Deliver** tab \>**View** button).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4681-149">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="e4681-149">Related topics</span></span>

[<span data-ttu-id="e4681-150">Definere serviceintervaller</span><span class="sxs-lookup"><span data-stu-id="e4681-150">Set up service intervals</span></span>](set-up-service-intervals.md)  

