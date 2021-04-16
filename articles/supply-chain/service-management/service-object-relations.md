---
title: Serviceobjektrelasjoner
description: Du kan opprette serviceobjektrelasjoner mellom et serviceobjekt og en serviceavtale eller en serviceordre.
author: ShylaThompson
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1984e4c2d57a03ad27c1f6d417209b806f7d6be6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835852"
---
# <a name="service-object-relations"></a><span data-ttu-id="4f80a-103">Serviceobjektrelasjoner</span><span class="sxs-lookup"><span data-stu-id="4f80a-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f80a-104">Du kan opprette serviceobjektrelasjoner mellom et serviceobjekt og en serviceavtale eller en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="4f80a-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="4f80a-105">Når du oppretter en relasjon, knytter du serviceobjektet til serviceavtalen eller serviceordren.</span><span class="sxs-lookup"><span data-stu-id="4f80a-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="4f80a-106">Når relasjonen er opprettet, kan du knytte serviceobjektet til en hvilken som helst linje i serviceavtalen eller serviceordren.</span><span class="sxs-lookup"><span data-stu-id="4f80a-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="4f80a-107">Stykklistemaler</span><span class="sxs-lookup"><span data-stu-id="4f80a-107">Template BOMs</span></span>

<span data-ttu-id="4f80a-108">Du kan også angi en stykklistemal for objektrelasjonen.</span><span class="sxs-lookup"><span data-stu-id="4f80a-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="4f80a-109">Stykklistemalen er en stykkliste for objektet som du utfører service på.</span><span class="sxs-lookup"><span data-stu-id="4f80a-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="4f80a-110">Hvis du bytter en del som en del av serviceobjektet under et servicebesøk, kan du registrere denne endringene i servicestykklisten ved hjelp av Serviceobjekter-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="4f80a-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="4f80a-111">Eksempel</span><span class="sxs-lookup"><span data-stu-id="4f80a-111">Example</span></span>

<span data-ttu-id="4f80a-112">Du oppretter en serviceavtale om å utføre service på to heiser i kundens bygg.</span><span class="sxs-lookup"><span data-stu-id="4f80a-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="4f80a-113">Serviceavtalen har identifikatoren ID SAL-001.</span><span class="sxs-lookup"><span data-stu-id="4f80a-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="4f80a-114">Heisene er definert som objekter i Serviceobjekter-skjemaet med numrene EL-S/1000 og EL-L/1000.</span><span class="sxs-lookup"><span data-stu-id="4f80a-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="4f80a-115">Du knytter serviceobjektene EL-S/1000 og EL-L/1000 til serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="4f80a-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="4f80a-116">Du vil registrere endringer i stykklisten (SL) for serviceobjektet når du setter inn reservedeler i objektet, så du knytter en servicestykkliste til serviceobjektrelasjonen, som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="4f80a-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="4f80a-117">Serviceobjekt</span><span class="sxs-lookup"><span data-stu-id="4f80a-117">Service object</span></span> | <span data-ttu-id="4f80a-118">Relasjon – Serviceavtale</span><span class="sxs-lookup"><span data-stu-id="4f80a-118">Relation – Service agreement</span></span> | <span data-ttu-id="4f80a-119">Servicestykkliste</span><span class="sxs-lookup"><span data-stu-id="4f80a-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="4f80a-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="4f80a-120">EL-S/1000</span></span>      | <span data-ttu-id="4f80a-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="4f80a-121">ID SAL-001</span></span>                   | <span data-ttu-id="4f80a-122">SL-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="4f80a-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="4f80a-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="4f80a-123">EL-L/1000</span></span>      | <span data-ttu-id="4f80a-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="4f80a-124">ID SAL-001</span></span>                   | <span data-ttu-id="4f80a-125">SL-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="4f80a-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="4f80a-126">Fordi det finnes serviceobjektrelasjoner for avtalen, kan du nå opprette serviceavtalelinjer med disse objektene, som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="4f80a-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="4f80a-127">transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="4f80a-127">Transaction type</span></span> | <span data-ttu-id="4f80a-128">Kategori</span><span class="sxs-lookup"><span data-stu-id="4f80a-128">Category</span></span>           | <span data-ttu-id="4f80a-129">Serviceobjekt</span><span class="sxs-lookup"><span data-stu-id="4f80a-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="4f80a-130">Time</span><span class="sxs-lookup"><span data-stu-id="4f80a-130">Hour</span></span>             | <span data-ttu-id="4f80a-131">Inspeksjon</span><span class="sxs-lookup"><span data-stu-id="4f80a-131">Inspection</span></span>         | <span data-ttu-id="4f80a-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="4f80a-132">EL-S/1000</span></span>      |
| <span data-ttu-id="4f80a-133">Time</span><span class="sxs-lookup"><span data-stu-id="4f80a-133">Hour</span></span>             | <span data-ttu-id="4f80a-134">Rengjøring av girkasse</span><span class="sxs-lookup"><span data-stu-id="4f80a-134">Gear box cleaning</span></span>  | <span data-ttu-id="4f80a-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="4f80a-135">EL-S/1000</span></span>      |
| <span data-ttu-id="4f80a-136">Vare</span><span class="sxs-lookup"><span data-stu-id="4f80a-136">Item</span></span>             | <span data-ttu-id="4f80a-137">Rengjøringsmaterialer</span><span class="sxs-lookup"><span data-stu-id="4f80a-137">Cleaning materials</span></span> | <span data-ttu-id="4f80a-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="4f80a-138">EL-S/1000</span></span>      |
| <span data-ttu-id="4f80a-139">Time</span><span class="sxs-lookup"><span data-stu-id="4f80a-139">Hour</span></span>             | <span data-ttu-id="4f80a-140">Inspeksjon</span><span class="sxs-lookup"><span data-stu-id="4f80a-140">Inspection</span></span>         | <span data-ttu-id="4f80a-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="4f80a-141">EL-L/1000</span></span>      |
| <span data-ttu-id="4f80a-142">Time</span><span class="sxs-lookup"><span data-stu-id="4f80a-142">Hour</span></span>             | <span data-ttu-id="4f80a-143">Rengjøring av girkasse</span><span class="sxs-lookup"><span data-stu-id="4f80a-143">Gearbox cleaning</span></span>   | <span data-ttu-id="4f80a-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="4f80a-144">EL-L/1000</span></span>      |
| <span data-ttu-id="4f80a-145">Vare</span><span class="sxs-lookup"><span data-stu-id="4f80a-145">Item</span></span>             | <span data-ttu-id="4f80a-146">Rengjøringsmaterialer</span><span class="sxs-lookup"><span data-stu-id="4f80a-146">Cleaning materials</span></span> | <span data-ttu-id="4f80a-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="4f80a-147">EL-L/1000</span></span>      |

<span data-ttu-id="4f80a-148">På et servicebesøk må du bytte girkasse i heisen EL-S/1000.</span><span class="sxs-lookup"><span data-stu-id="4f80a-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="4f80a-149">Når du skal bytte en del i objektet, kan du åpne stykklistedesigneren ved hjelp av serviceobjektrelasjonen som du definerte for gjeldende serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="4f80a-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="4f80a-150">Åpne stykklistedesigneren ved hjelp av en serviceobjektrelasjon</span><span class="sxs-lookup"><span data-stu-id="4f80a-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="4f80a-151">Serviceavtaler</span><span class="sxs-lookup"><span data-stu-id="4f80a-151">Service agreements</span></span>
2. <span data-ttu-id="4f80a-152">Dobbeltklikk en serviceavtale, eller klikk Serviceavtale for å opprette en serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="4f80a-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="4f80a-153">Klikk på fanen Oppsett.</span><span class="sxs-lookup"><span data-stu-id="4f80a-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="4f80a-154">Klikk på Serviceobjekter hvis du vil knytte en stykklistemal til serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="4f80a-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="4f80a-155">I Serviceobjekter-skjemaet klikker du Utforming for å åpne skjemaet Utforming for å endre stykklistemalen.</span><span class="sxs-lookup"><span data-stu-id="4f80a-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="4f80a-156">Automatisk opprettede serviceordrer</span><span class="sxs-lookup"><span data-stu-id="4f80a-156">Automatically created service orders</span></span>

<span data-ttu-id="4f80a-157">Hvis du oppretter serviceordrer for serviceavtalen automatisk, opprettes også serviceobjektrelasjonene i avtalen, i serviceordrene.</span><span class="sxs-lookup"><span data-stu-id="4f80a-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]