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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1027a6a1ddb1057ba039382d394522d6f9538a90
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434496"
---
# <a name="service-intervals"></a><span data-ttu-id="c4fe2-103">Serviceintervaller</span><span class="sxs-lookup"><span data-stu-id="c4fe2-103">Service intervals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4fe2-104">Serviceavtaleintervallet viser hvor ofte serviceordrelinjene skal opprettes for serviceavtalelinjene når du oppretter serviceordrer automatisk.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-104">The service agreement interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders automatically.</span></span>

<span data-ttu-id="c4fe2-105">Når du oppretter serviceordrer automatisk, opprettes serviceordrelinjer i samsvar med det intervallet du har angitt for serviceavtalelinjen fra startdatoen for avtalelinjen.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-105">When you create service orders automatically, service order lines are created according to the interval that you have specified for the service agreement line from the start date of the agreement line.</span></span>

<span data-ttu-id="c4fe2-106">Hvis **Intervall**-feltet for en serviceavtalelinje på **Serviceavtaler**-siden er tomt, gjelder linjen et engangstilfelle, og brukes ikke til å opprette gjentatte serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-106">If the **Interval** field of a service agreement line in the **Service agreements** page is blank, the line is a one-time event, and it is not used to create service orders repeatedly.</span></span>

## <a name="example"></a><span data-ttu-id="c4fe2-107">Eksempel</span><span class="sxs-lookup"><span data-stu-id="c4fe2-107">Example</span></span>

<span data-ttu-id="c4fe2-108">Dette eksemplet viser hvordan et serviceintervall påvirker serviceavtalelinjer og serviceordrelinjer i en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-108">This example illustrates how a service interval will affect service agreement lines and service order lines on a service order.</span></span>

### <a name="create-a-service-agreement"></a><span data-ttu-id="c4fe2-109">Opprette en serviceavtale</span><span class="sxs-lookup"><span data-stu-id="c4fe2-109">Create a service agreement</span></span>

<span data-ttu-id="c4fe2-110">Først oppretter du en serviceavtale og setter **Kombiner serviceordrer** til **Etter serviceavtale**.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-110">First, you create a service agreement and set the **Combine service orders** option to **By service agreement**.</span></span>

1. <span data-ttu-id="c4fe2-111">Klikk på **Serviceavtaler**.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-111">Click **Service agreements**</span></span>
2. <span data-ttu-id="c4fe2-112">I **Handlingsruten** i **Serviceavtale**-kategorien i **Ny**-gruppen klikker du **Serviceavtale** for å opprette en ny serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-112">On the **Action Pane**, on the **Service agreement** tab, in the **New** group, click **Service agreement** to create a new service agreement.</span></span>
3. <span data-ttu-id="c4fe2-113">Angi en beskrivelse, velg et prosjekt i **Prosjekt-ID**-feltet, og angi en dato i **Startdato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-113">Enter a description, select a project in the **Project ID** field, and enter a date in the **Start date** field.</span></span>
4. <span data-ttu-id="c4fe2-114">I **Kombiner serviceordrer**-feltet velger du **Etter serviceavtale**.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-114">In the **Combine service orders** field, select **By service agreement**.</span></span>

<span data-ttu-id="c4fe2-115">Du har nå opprettet følgende serviceavtale:</span><span class="sxs-lookup"><span data-stu-id="c4fe2-115">You have now created the following service agreement:</span></span>

| <span data-ttu-id="c4fe2-116">Project</span><span class="sxs-lookup"><span data-stu-id="c4fe2-116">Project</span></span>      | <span data-ttu-id="c4fe2-117">Startdato</span><span class="sxs-lookup"><span data-stu-id="c4fe2-117">Start date</span></span>                                                                         |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c4fe2-118">Ditt prosjekt</span><span class="sxs-lookup"><span data-stu-id="c4fe2-118">Your project</span></span> | <span data-ttu-id="c4fe2-119">Datoen du angav for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-119">The date you specified for the project.</span></span> <span data-ttu-id="c4fe2-120">I dette eksemplet brukes gjeldende dato.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-120">In this example, the current date is used.</span></span> |

### <a name="create-a-service-agreement-line"></a><span data-ttu-id="c4fe2-121">Opprette en serviceavtalelinje</span><span class="sxs-lookup"><span data-stu-id="c4fe2-121">Create a service agreement line</span></span>

<span data-ttu-id="c4fe2-122">Deretter oppretter du en serviceavtalelinje som har transaksjonstypen **Time**.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-122">Next, you create a service agreement line that has the transaction type **Hour**.</span></span>

<span data-ttu-id="c4fe2-123">For å fullføre denne delen, må du opprette et serviceintervall på 10 dager på **Serviceintervaller**-siden.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-123">To complete this part of the example, you must create a service interval of 10 days in the **Service intervals** page.</span></span> 

1. <span data-ttu-id="c4fe2-124">Velg serviceavtalen du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-124">Select the service agreement that you just created.</span></span> 
2. <span data-ttu-id="c4fe2-125">På **Linjer**-hurtigkategorien, klikk **Legg til** for å opprette en ny linje i den nedre ruten på **Serviceavtaler**-siden.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-125">On the **Lines** FastTab, click the **Add** button to create a new line in the lower pane of the **Service agreements** page.</span></span>
3. <span data-ttu-id="c4fe2-126">Velg **Time** i **Transaksjonstype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-126">In the **Transaction type** field, select **Hour**.</span></span>
4. <span data-ttu-id="c4fe2-127">I **Arbeider**-feltet velger du arbeideren som skal levere servicen.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-127">In the **Worker** field, select the worker who will deliver the service.</span></span>
5. <span data-ttu-id="c4fe2-128">Velg 10-dagersintervallet i feltet **Serviceintervall**.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-128">In the **Service interval** field, select the 10 days interval.</span></span>

<span data-ttu-id="c4fe2-129">Du har nå opprettet en serviceavtalelinje med følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="c4fe2-129">You have now created a service agreement line with the following information:</span></span>

| <span data-ttu-id="c4fe2-130">transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="c4fe2-130">Transaction type</span></span> | <span data-ttu-id="c4fe2-131">Startdato</span><span class="sxs-lookup"><span data-stu-id="c4fe2-131">Start date</span></span>                               | <span data-ttu-id="c4fe2-132">Serviceintervall</span><span class="sxs-lookup"><span data-stu-id="c4fe2-132">Service interval</span></span> |
|------------------|------------------------------------------|------------------|
| <span data-ttu-id="c4fe2-133">Time</span><span class="sxs-lookup"><span data-stu-id="c4fe2-133">Hour</span></span>             | <span data-ttu-id="c4fe2-134">Den gjeldende datoen.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-134">The current date.</span></span>                        | <span data-ttu-id="c4fe2-135">Hver 10. dag</span><span class="sxs-lookup"><span data-stu-id="c4fe2-135">Every 10 days</span></span>    |
| <span data-ttu-id="c4fe2-136">Arbeider</span><span class="sxs-lookup"><span data-stu-id="c4fe2-136">Worker</span></span>           | <span data-ttu-id="c4fe2-137">Arbeideren som skal utføre servicen.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-137">The worker who will perform the service.</span></span> |                  |

<span data-ttu-id="c4fe2-138">Det er ikke angitt noe tidsvindu for linjen.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-138">There is no time window specified for the line.</span></span> 

### <a name="create-planned-service-orders"></a><span data-ttu-id="c4fe2-139">Opprette planlagte serviceordrer</span><span class="sxs-lookup"><span data-stu-id="c4fe2-139">Create planned service orders</span></span>

<span data-ttu-id="c4fe2-140">Du kan nå opprette planlagte serviceordrer og serviceordrelinjer for kommende måned.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-140">You can now create planned service orders and service order lines for the coming month.</span></span>

1. <span data-ttu-id="c4fe2-141">På **Serviceavtaler**-siden i **handlingsruten** i **Lever**-fanen, klikker du **Planlagte serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-141">In the **Service agreements** page, on the **Action Pane**, on the **Deliver** tab, click **Planned service orders**.</span></span>
2. <span data-ttu-id="c4fe2-142">På **Opprett serviceordrer**-siden skriver du inn gjeldende dato i **Fra dato**-feltet og en dato som er én måned fra gjeldende dato i **Til dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-142">In the **Create service orders** page, enter the current date in the **From date** field and a date that is one month from the current date in the **To date** field.</span></span>
3. <span data-ttu-id="c4fe2-143">Sett **Time**-glidebryteren til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-143">Set the **Hour** slider to **Yes**.</span></span> 
4. <span data-ttu-id="c4fe2-144">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-144">Click **OK**.</span></span>

<span data-ttu-id="c4fe2-145">Fordi det ikke finnes noen grupperinger i serviceordren (definert med alternativet **Etter serviceavtale** i feltet **Kombiner serviceordrer**), blir det opprettet én serviceordrelinje per serviceordre.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-145">Because there is no grouping on the service order (defined by the **By service agreement** option in the **Combine service orders** field), one service order line is created per service order.</span></span>

### <a name="service-orders-created"></a><span data-ttu-id="c4fe2-146">Opprettede serviceordrer</span><span class="sxs-lookup"><span data-stu-id="c4fe2-146">Service orders created</span></span>

<span data-ttu-id="c4fe2-147">Tre serviceordrelinjer er opprettet innenfor tidsrammen du angav i dialogboksen **Opprett serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-147">Three service order lines have been created within the time frame that you specified in the **Create service orders** dialog box.</span></span> <span data-ttu-id="c4fe2-148">Du kan vise serviceordrelinjene på **Serviceavtaler**-siden (**Handlingsrute** \> **Lever**-kategorien \> **Vis**-knappen).</span><span class="sxs-lookup"><span data-stu-id="c4fe2-148">You can view the service order lines in the **Service agreements** page (**Action Pane** \> **Deliver** tab \>**View** button).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4fe2-149">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="c4fe2-149">Related topics</span></span>

[<span data-ttu-id="c4fe2-150">Definere serviceintervaller</span><span class="sxs-lookup"><span data-stu-id="c4fe2-150">Set up service intervals</span></span>](set-up-service-intervals.md)  

