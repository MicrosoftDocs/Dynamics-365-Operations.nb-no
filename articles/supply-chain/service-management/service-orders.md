---
title: Serviceordrer
description: En serviceordre representerer et besøk av en servicetekniker hos en kunde på en bestemt dato.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e47c3f998b563c775da77c48edcb7b8abcba4a04
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824492"
---
# <a name="service-orders"></a><span data-ttu-id="2cf24-103">Serviceordrer</span><span class="sxs-lookup"><span data-stu-id="2cf24-103">Service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2cf24-104">En serviceordre representerer et besøk av en servicetekniker hos en kunde på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="2cf24-104">A service order represents a visit that a service technician makes to a customer site on a specific date.</span></span> <span data-ttu-id="2cf24-105">Hver serviceordre består av en eller flere serviceordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="2cf24-105">Each service order consists of one or more service order lines.</span></span> <span data-ttu-id="2cf24-106">Serviceordrelinjer representerer antall arbeidstimer som må utføres av serviceteknikere, og relaterte varer, utgifter og gebyrer.</span><span class="sxs-lookup"><span data-stu-id="2cf24-106">Service order lines represent the hours of work that must be performed by the service technician, and the related items, expenses, and fees.</span></span>

<span data-ttu-id="2cf24-107">Du kan knytte oppgaver og objekter til en serviceordrelinje.</span><span class="sxs-lookup"><span data-stu-id="2cf24-107">You can attach tasks and objects to a service order line.</span></span> <span data-ttu-id="2cf24-108">Du kan deretter gruppere serviceordrelinjer etter oppgaven eller objektet.</span><span class="sxs-lookup"><span data-stu-id="2cf24-108">You can then group service order lines by task or by object.</span></span> <span data-ttu-id="2cf24-109">Du kan også knytte varer som er oppgitt i lageret til serviceordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="2cf24-109">You can also attach items that are listed in inventory to service order lines.</span></span>

## <a name="create-service-orders"></a><span data-ttu-id="2cf24-110">Opprette serviceordrer</span><span class="sxs-lookup"><span data-stu-id="2cf24-110">Create service orders</span></span>

<span data-ttu-id="2cf24-111">Du kan opprette serviceordrer basert på en serviceavtale og linjene som er inkludert i denne avtalen.</span><span class="sxs-lookup"><span data-stu-id="2cf24-111">You can create service orders based on a service agreement and the lines that are contained in that agreement.</span></span> <span data-ttu-id="2cf24-112">Du kan imidlertid bare opprette serviceordrer som er knyttet til en serviceavtale i perioden som er angitt i avtalen.</span><span class="sxs-lookup"><span data-stu-id="2cf24-112">However, you can create service orders that are associated with a service agreement only in the period that is specified in the agreement.</span></span> <span data-ttu-id="2cf24-113">Hvis en serviceavtale er gyldig for 2011-kalenderåret, kan du for eksempel opprette serviceordrer for den avtalen fra 1. januar 2011, og 31. desember 2011.</span><span class="sxs-lookup"><span data-stu-id="2cf24-113">For example, if a service agreement is valid for the 2011 calendar year, you can create service orders for the agreement from January 1, 2011, and December 31, 2011.</span></span>

<span data-ttu-id="2cf24-114">Du kan også opprette serviceordrer enkeltvis, uten å knytte dem til en avtale.</span><span class="sxs-lookup"><span data-stu-id="2cf24-114">You can also create service orders individually, without associating them with an agreement.</span></span> <span data-ttu-id="2cf24-115">Disse serviceordrene kan brukes til å håndtere uplanlagte eller enkeltstående servicebesøk.</span><span class="sxs-lookup"><span data-stu-id="2cf24-115">These service orders can be used to handle unscheduled or one-time service visits.</span></span> <span data-ttu-id="2cf24-116">I mars måned ønsker kunden din for eksempel at service skal utføres på to maskiner i tillegg til maskinene som er angitt i serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="2cf24-116">For example, in the month of March, your customer wants service to be performed on two machines, in addition to the machines that are specified in the service agreement.</span></span> <span data-ttu-id="2cf24-117">For denne aktiviteten du oppretter serviceordrer, men knytte ikke dem til en avtale.</span><span class="sxs-lookup"><span data-stu-id="2cf24-117">For this task, you create service orders but do not associate them with an agreement.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2cf24-118">Hvis du vil opprette serviceordrer som ikke er knyttet til en serviceavtale, må du merke av for <STRONG>Tillat uten serviceavtale</STRONG> i skjemaet <STRONG>Servicestyringsparametere</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2cf24-118">To create service orders that are not associated with a service agreement, you must select the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form.</span></span></P>

<span data-ttu-id="2cf24-119">**Scenario**</span><span class="sxs-lookup"><span data-stu-id="2cf24-119">**Scenario**</span></span>

<span data-ttu-id="2cf24-120">Dette scenariet beskriver en annen situasjon der det er nyttig å opprette en serviceordre som ikke er knyttet til en serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="2cf24-120">The following scenario describes another situation where it is useful to create a service order that is not associated with a service agreement.</span></span>

<span data-ttu-id="2cf24-121">Firmaets fordelingsansvarlig mottar en telefon med forespørsel om øyeblikkelig hjelp med en heis.</span><span class="sxs-lookup"><span data-stu-id="2cf24-121">The company dispatcher receives a call requesting emergency service on an elevator.</span></span> <span data-ttu-id="2cf24-122">Det er ikke tid til å opprette en serviceavtale og et prosjekt for servicen.</span><span class="sxs-lookup"><span data-stu-id="2cf24-122">There is no time to set up a service agreement and a project for the service.</span></span> <span data-ttu-id="2cf24-123">Derfor fordelingsansvarlig oppretter en serviceordre direkte i **Serviceordrer**-skjemaet, knytter serviceordren til et eksisterende prosjekt, og oppretter serviceordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="2cf24-123">Therefore, the dispatcher creates a service order directly in the **Service orders** form, attaches the service order to an existing project, and creates the service order lines.</span></span> <span data-ttu-id="2cf24-124">Fordelingsansvarlig oppretter også en oppgave eller en objektrelasjon for en eksisterende serviceordre for å registrere arbeid som ikke er tilknyttet serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="2cf24-124">The dispatcher also creates a task or object relation for an existing service order, to record work that is not related to the service agreement.</span></span> <span data-ttu-id="2cf24-125">Hvis du vil ha mer informasjon, se [Opprette serviceordrer manuelt](create-service-orders-manually.md) og [Opprette serviceoppgaverelasjoner](create-service-task-relations.md).</span><span class="sxs-lookup"><span data-stu-id="2cf24-125">For more information, see [Create service orders manually](create-service-orders-manually.md) and [Create service task relations](create-service-task-relations.md).</span></span>

## <a name="monitor-the-progress-of-service-orders"></a><span data-ttu-id="2cf24-126">Overvåk fremdriften til serviceordren</span><span class="sxs-lookup"><span data-stu-id="2cf24-126">Monitor the progress of service orders</span></span>

<span data-ttu-id="2cf24-127">Hvis du vil overvåke fremdriften til en salgsordre gjennom ulike grupper og arbeidsprosesser, kan du sette opp et system med stadier og årsakskoder for serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="2cf24-127">To monitor the progress of a sales order through the different teams and work processes, you can set up a system of stages and reason codes for service orders.</span></span> <span data-ttu-id="2cf24-128">For hvert stadium kan du angi handlingene som er tillatt.</span><span class="sxs-lookup"><span data-stu-id="2cf24-128">For each stage, you can specify the actions that are allowed.</span></span> <span data-ttu-id="2cf24-129">Hvis du vil ha mer informasjon, kan du se [Opprette årsakskoder](create-reason-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2cf24-129">For more information, see [Create reason codes](create-reason-codes.md).</span></span>

<span data-ttu-id="2cf24-130">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="2cf24-130">**Example**</span></span>

<span data-ttu-id="2cf24-131">En serviceordre godkjennes av fordelingsansvarlig.</span><span class="sxs-lookup"><span data-stu-id="2cf24-131">A service order is approved by the dispatcher.</span></span> <span data-ttu-id="2cf24-132">Fordelingsansvarlig oppdaterer stadiet til serviceordren og angir en årsakskode som indikerer at serviceordren er frigitt til serviceteknikeren.</span><span class="sxs-lookup"><span data-stu-id="2cf24-132">The dispatcher updates the stage of the service order and specifies a reason code that indicates that the service order has been released to the service technician.</span></span> <span data-ttu-id="2cf24-133">Serviceteknikeren reiser til kundens sted og utfører servicen.</span><span class="sxs-lookup"><span data-stu-id="2cf24-133">The technician goes to the customer site and performs the service.</span></span>

## <a name="specify-item-requirements-for-service-orders"></a><span data-ttu-id="2cf24-134">Angi varebehov for serviceordrer</span><span class="sxs-lookup"><span data-stu-id="2cf24-134">Specify item requirements for service orders</span></span>

<span data-ttu-id="2cf24-135">Du kan angi lagervarer som kreves for serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="2cf24-135">You can specify the inventory items that are required for service orders.</span></span> <span data-ttu-id="2cf24-136">Serviceordren må imidlertid være tilknyttet et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="2cf24-136">However, the service order must be associated with a project.</span></span> <span data-ttu-id="2cf24-137">Varebehov for serviceordrer behandles via et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="2cf24-137">Item requirements for service orders are processed through a project.</span></span> 

<span data-ttu-id="2cf24-138">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="2cf24-138">**Example**</span></span>

<span data-ttu-id="2cf24-139">Serviceordrene som er opprettet fra serviceavtalen behandles av fordelingsansvarlig.</span><span class="sxs-lookup"><span data-stu-id="2cf24-139">The service orders that are created from the service agreement are processed by the dispatcher.</span></span> <span data-ttu-id="2cf24-140">For den første serviceordren oppdager fordelingsansvarlig at serviceteknikeren trenger en viktig reservedel som ikke finnes i lagerbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="2cf24-140">For the first service order, the dispatcher realizes that the service technician requires an important spare part that is not in the on-hand inventory.</span></span> <span data-ttu-id="2cf24-141">Derfor oppretter fordelingsansvarlig et varebehov for reservedelen direkte fra serviceordren.</span><span class="sxs-lookup"><span data-stu-id="2cf24-141">Therefore, the dispatcher creates an item requirement for the spare part directly from the service order.</span></span>

## <a name="move-and-post-lines"></a><span data-ttu-id="2cf24-142">Flytte og postere linjer</span><span class="sxs-lookup"><span data-stu-id="2cf24-142">Move and post lines</span></span>

<span data-ttu-id="2cf24-143">En servicetekniker kommer tilbake fra et servicebesøk og endrer deretter og oppdaterer serviceordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="2cf24-143">A service technician returns from a service visit, and then modifies and updates the service order lines.</span></span> <span data-ttu-id="2cf24-144">I løpet av servicebesøket utførte teknikeren en servicejobb som var planlagt for det neste servicebesøket.</span><span class="sxs-lookup"><span data-stu-id="2cf24-144">During the service visit, the technician performed a service job that was scheduled for the next service visit.</span></span> <span data-ttu-id="2cf24-145">Derfor flytter teknikeren linjene fra neste servicebesøk til gjeldende servicebesøk.</span><span class="sxs-lookup"><span data-stu-id="2cf24-145">Therefore, the technician moves the lines from the next service visit to the current service visit.</span></span> <span data-ttu-id="2cf24-146">Teknikeren posterer deretter serviceordren.</span><span class="sxs-lookup"><span data-stu-id="2cf24-146">The technician then posts the service order.</span></span> <span data-ttu-id="2cf24-147">Hvis du vil ha mer informasjon, se [Flytte serviceordrelinjer](move-service-order-lines.md).</span><span class="sxs-lookup"><span data-stu-id="2cf24-147">For more information, see [Move service order lines](move-service-order-lines.md).</span></span>

## <a name="cancel-service-orders"></a><span data-ttu-id="2cf24-148">Annuller serviceordrer</span><span class="sxs-lookup"><span data-stu-id="2cf24-148">Cancel service orders</span></span>

<span data-ttu-id="2cf24-149">En av de andre serviceordrene som ble generert for januar, foreldes fordi jobben blir annullert.</span><span class="sxs-lookup"><span data-stu-id="2cf24-149">One of the other service orders that was generated for the month of January becomes obsolete, because the job is canceled.</span></span> <span data-ttu-id="2cf24-150">Derfor annullerer servicefordelingsansvarlig serviceordren.</span><span class="sxs-lookup"><span data-stu-id="2cf24-150">Therefore, the service dispatcher cancels the service order.</span></span> <span data-ttu-id="2cf24-151">Hvis du vil ha mer informasjon, se [Annullere serviceordrer](cancel-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="2cf24-151">For more information, see [Cancel service orders](cancel-service-orders.md).</span></span>

## <a name="post-from-projects"></a><span data-ttu-id="2cf24-152">Postere fra prosjekter</span><span class="sxs-lookup"><span data-stu-id="2cf24-152">Post from projects</span></span>

<span data-ttu-id="2cf24-153">På slutten av hver uke vil fordelingsansvarlig postere alle serviceordrer som er tilknyttet et bestemt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="2cf24-153">At the end of each week, the dispatcher wants to post all service orders that are attached to a specific project.</span></span> <span data-ttu-id="2cf24-154">Derfor fordelingsansvarlig finner det relevante prosjektet i **Prosjekter**-skjemaet og posterer serviceordrene som er fullført.</span><span class="sxs-lookup"><span data-stu-id="2cf24-154">Therefore, the dispatcher locates the relevant project in the **Projects** form and posts the service orders that have been completed.</span></span> <span data-ttu-id="2cf24-155">Hvis du vil ha mer informasjon, se [Postere serviceordrer (klasseskjema)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="2cf24-155">For more information, see [Post service orders (class form)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).</span></span>

## <a name="delete-service-orders"></a><span data-ttu-id="2cf24-156">Slett serviceordrer</span><span class="sxs-lookup"><span data-stu-id="2cf24-156">Delete service orders</span></span>

<span data-ttu-id="2cf24-157">I løpet av årets andre halvdel bestemmer kunden seg for at servicebesøkene er for sjeldne.</span><span class="sxs-lookup"><span data-stu-id="2cf24-157">During the second half of the year, your customer decides that the service visits are too infrequent.</span></span> <span data-ttu-id="2cf24-158">Du må opprette en ny serie med hyppigere servicebesøk for resten av tiden som gjenstår på serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="2cf24-158">You must create a new, more frequent series of service visits for the remaining time on the service agreement.</span></span> <span data-ttu-id="2cf24-159">Derfor må du slette de eksisterende serviceordrene og opprette nye serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="2cf24-159">Therefore, you must delete the existing service orders and create new service orders.</span></span> <span data-ttu-id="2cf24-160">Hvis du vil ha mer informasjon, se [Slette serviceordrer](delete-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="2cf24-160">For more information, see [Delete service orders](delete-service-orders.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2cf24-161">Se også</span><span class="sxs-lookup"><span data-stu-id="2cf24-161">See also</span></span>

<span data-ttu-id="2cf24-162">[Serviceordrer (skjema)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="2cf24-162">[Service orders (form)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]