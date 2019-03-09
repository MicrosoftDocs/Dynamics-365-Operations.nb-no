---
title: Vedlikeholde rute for en produktmodell
description: Kjører du denne prosedyren krever det at en eksisterende produktmodellkonfigurasjon finnes.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e793466e021671501570aed06959d684d5e9c15
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "317160"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="59780-103">Vedlikeholde rute for en produktmodell</span><span class="sxs-lookup"><span data-stu-id="59780-103">Maintain route for a product model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="59780-104">Kjører du denne prosedyren krever det at en eksisterende produktmodellkonfigurasjon finnes.</span><span class="sxs-lookup"><span data-stu-id="59780-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="59780-105">Denne fremgangsmåten bruker modellen for High-end-høyttaler i demofirmaet USMF til å lede deg gjennom prosessen.</span><span class="sxs-lookup"><span data-stu-id="59780-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="59780-106">Legge til en ruteoperasjon</span><span class="sxs-lookup"><span data-stu-id="59780-106">Add a route operation</span></span>
1. <span data-ttu-id="59780-107">Klikk Definisjon av produktvariantmodell.</span><span class="sxs-lookup"><span data-stu-id="59780-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="59780-108">Klikk Produktkonfigurasjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="59780-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="59780-109">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="59780-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="59780-110">Velg High-end-høyttalermodellen for denne øvelsen.</span><span class="sxs-lookup"><span data-stu-id="59780-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="59780-111">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="59780-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="59780-112">Utvid delen Ruteoperasjoner.</span><span class="sxs-lookup"><span data-stu-id="59780-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="59780-113">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="59780-113">Click Add.</span></span>
7. <span data-ttu-id="59780-114">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="59780-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="59780-115">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="59780-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="59780-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="59780-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="59780-117">Angi detaljer om ruteoperasjon</span><span class="sxs-lookup"><span data-stu-id="59780-117">Enter route operation details</span></span>
1. <span data-ttu-id="59780-118">Klikk Detaljer om ruteoperasjon.</span><span class="sxs-lookup"><span data-stu-id="59780-118">Click Route operation details.</span></span>
2. <span data-ttu-id="59780-119">Angi eller velg en verdi i feltet Operasjon.</span><span class="sxs-lookup"><span data-stu-id="59780-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="59780-120">I Oper.</span><span class="sxs-lookup"><span data-stu-id="59780-120">In the Oper.</span></span> <span data-ttu-id="59780-121">Nr.</span><span class="sxs-lookup"><span data-stu-id="59780-121">No.</span></span> <span data-ttu-id="59780-122">angir du et nummer.</span><span class="sxs-lookup"><span data-stu-id="59780-122">field, enter a number.</span></span>
    * <span data-ttu-id="59780-123">Operasjonsnumre fastsetter rutesekvensen.</span><span class="sxs-lookup"><span data-stu-id="59780-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="59780-124">Hver egenskap for en ruteoperasjon kan få en statisk verdi eller tilordnes til et attributt.</span><span class="sxs-lookup"><span data-stu-id="59780-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="59780-125">Tilordning til et attributt fører til at verdien blir definert som en del av konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="59780-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="59780-126">Angi eller velg en verdi i Rutegruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="59780-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="59780-127">Rutegruppen bestemmer grunnleggende virkemåte for etterkalkulering, forbruk og oppsett.</span><span class="sxs-lookup"><span data-stu-id="59780-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="59780-128">Klikk kategorien Oppsett.</span><span class="sxs-lookup"><span data-stu-id="59780-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="59780-129">Klikk kategorien Tider.</span><span class="sxs-lookup"><span data-stu-id="59780-129">Click the Times tab.</span></span>
7. <span data-ttu-id="59780-130">I feltet Prosessantall angir du et nummer.</span><span class="sxs-lookup"><span data-stu-id="59780-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="59780-131">Bestem hvor mange som skal bli behandlet i løpet av én operasjon.</span><span class="sxs-lookup"><span data-stu-id="59780-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="59780-132">Angi et tall i feltet Timer/tid.</span><span class="sxs-lookup"><span data-stu-id="59780-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="59780-133">Angi tidsforholdet.</span><span class="sxs-lookup"><span data-stu-id="59780-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="59780-134">Merk av for Sett.</span><span class="sxs-lookup"><span data-stu-id="59780-134">Select the Set check box.</span></span>
10. <span data-ttu-id="59780-135">Angi et tall i feltet Kjøretid.</span><span class="sxs-lookup"><span data-stu-id="59780-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="59780-136">Bestem behandlingstiden for antallet som du har angitt.</span><span class="sxs-lookup"><span data-stu-id="59780-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="59780-137">Klikk kategorien Ressursbehov.</span><span class="sxs-lookup"><span data-stu-id="59780-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="59780-138">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="59780-138">Click Add.</span></span>
13. <span data-ttu-id="59780-139">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="59780-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="59780-140">Velg et alternativ i feltet Behovstype.</span><span class="sxs-lookup"><span data-stu-id="59780-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="59780-141">Bestem om du vil angi bestemte ressurser eller egenskaper som de må inneha.</span><span class="sxs-lookup"><span data-stu-id="59780-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="59780-142">Angi eller velg en verdi i feltet Behov.</span><span class="sxs-lookup"><span data-stu-id="59780-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="59780-143">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="59780-143">Click OK.</span></span>

