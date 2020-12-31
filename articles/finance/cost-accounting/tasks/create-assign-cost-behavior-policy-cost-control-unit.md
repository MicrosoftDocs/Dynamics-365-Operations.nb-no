---
title: Opprette og tilordne en kostnadsatferdspolicy til en kostnadskontrollenhet
description: Kostnadsatferd er klassifiseringen av kostnader som faste eller variable.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cfdff9b1af9183d21e988dd53559e749eed077eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446329"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="57e52-103">Opprette og tilordne en kostnadsatferdspolicy til en kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="57e52-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="57e52-104">Kostnadsatferd er klassifiseringen av kostnader som faste eller variable.</span><span class="sxs-lookup"><span data-stu-id="57e52-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="57e52-105">En policy og de tilsvarende reglene må tilordnes til en kostnadskontrollenhet for at policyen skal aktiveres.</span><span class="sxs-lookup"><span data-stu-id="57e52-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="57e52-106">Bruk denne fremgangsmåten til å opprette en policy og deretter tilordne policyen til en kostnadskontrollenhet.</span><span class="sxs-lookup"><span data-stu-id="57e52-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="57e52-107">Opprette et hierarki for kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="57e52-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="57e52-108">Gå til Kostnadsregnskap > Dimensjoner > Dimensjonshierarkier.</span><span class="sxs-lookup"><span data-stu-id="57e52-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="57e52-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="57e52-109">Click New.</span></span>
3. <span data-ttu-id="57e52-110">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="57e52-110">Click Create.</span></span>
4. <span data-ttu-id="57e52-111">Skriv inn "Hierarki for kostnadsatferd" i feltet Dimensjonshierarkinavn.</span><span class="sxs-lookup"><span data-stu-id="57e52-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="57e52-112">Angi eller velg en verdi i feltet Dimensjon.</span><span class="sxs-lookup"><span data-stu-id="57e52-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="57e52-113">Velg Kostnadselementer.</span><span class="sxs-lookup"><span data-stu-id="57e52-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="57e52-114">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="57e52-114">Click Save.</span></span>
7. <span data-ttu-id="57e52-115">Klikk Vis hierarki.</span><span class="sxs-lookup"><span data-stu-id="57e52-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="57e52-116">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="57e52-116">Click New.</span></span>
9. <span data-ttu-id="57e52-117">Skriv inn en verdi i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="57e52-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="57e52-118">Angi Fast kostnad.</span><span class="sxs-lookup"><span data-stu-id="57e52-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="57e52-119">Velg "Hierarki for kostnadsatferd" i treet.</span><span class="sxs-lookup"><span data-stu-id="57e52-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="57e52-120">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="57e52-120">Click New.</span></span>
12. <span data-ttu-id="57e52-121">Skriv inn en verdi i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="57e52-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="57e52-122">Angi Variabel kostnad.</span><span class="sxs-lookup"><span data-stu-id="57e52-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="57e52-123">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="57e52-123">Click Save.</span></span>
14. <span data-ttu-id="57e52-124">Velg "Hierarki for kostnadsatferd\Fast kostnad" i treet.</span><span class="sxs-lookup"><span data-stu-id="57e52-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="57e52-125">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="57e52-125">Click New.</span></span>
16. <span data-ttu-id="57e52-126">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="57e52-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="57e52-127">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="57e52-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="57e52-128">Området for dimensjonsmedlemmene kan inneholde mellomrom, men medlemmene kan ikke overlappe.</span><span class="sxs-lookup"><span data-stu-id="57e52-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="57e52-129">Angi eller velg en verdi i feltet Til dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="57e52-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="57e52-130">Området for dimensjonsmedlemmene kan inneholde mellomrom, men medlemmene kan ikke overlappe.</span><span class="sxs-lookup"><span data-stu-id="57e52-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="57e52-131">Velg "Hierarki for kostnadsatferd\Variabel kostnad" i treet.</span><span class="sxs-lookup"><span data-stu-id="57e52-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="57e52-132">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="57e52-132">Click New.</span></span>
21. <span data-ttu-id="57e52-133">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="57e52-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="57e52-134">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="57e52-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="57e52-135">Området for dimensjonsmedlemmene kan inneholde mellomrom, men medlemmene kan ikke overlappe.</span><span class="sxs-lookup"><span data-stu-id="57e52-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="57e52-136">Angi eller velg en verdi i feltet Til dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="57e52-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="57e52-137">Området for dimensjonsmedlemmene kan inneholde mellomrom, men medlemmene kan ikke overlappe.</span><span class="sxs-lookup"><span data-stu-id="57e52-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="57e52-138">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="57e52-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="57e52-139">Opprette policyen og regler</span><span class="sxs-lookup"><span data-stu-id="57e52-139">Create the policy and rules</span></span>
1. <span data-ttu-id="57e52-140">Gå til Kostnadsregnskap > Policyer > Policyer for kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="57e52-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="57e52-141">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="57e52-141">Click New.</span></span>
3. <span data-ttu-id="57e52-142">Skriv inn en verdi i feltet Policynavn.</span><span class="sxs-lookup"><span data-stu-id="57e52-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="57e52-143">Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="57e52-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="57e52-144">Velg policyhierarkiet du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="57e52-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="57e52-145">Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="57e52-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="57e52-146">Velg Organisasjon.</span><span class="sxs-lookup"><span data-stu-id="57e52-146">Select Organization.</span></span>  
6. <span data-ttu-id="57e52-147">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="57e52-147">Click Save.</span></span>
7. <span data-ttu-id="57e52-148">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="57e52-148">Click New.</span></span>
8. <span data-ttu-id="57e52-149">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="57e52-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="57e52-150">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="57e52-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="57e52-151">Utvid hierarkiet for å velge Variabel kostnad.</span><span class="sxs-lookup"><span data-stu-id="57e52-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="57e52-152">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="57e52-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="57e52-153">Som standard er den variable prosentdelen 100 prosent.</span><span class="sxs-lookup"><span data-stu-id="57e52-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="57e52-154">Klikk Policytilordninger for kostnadskontrollenhet.</span><span class="sxs-lookup"><span data-stu-id="57e52-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="57e52-155">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="57e52-155">Click New.</span></span>
13. <span data-ttu-id="57e52-156">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="57e52-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="57e52-157">Angi en dato i feltet Gyldig fra regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="57e52-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="57e52-158">Reglene er datoeffektive, og en bruker eller systemet kan utløpe en regel hvis det opprettes en nyere versjon.</span><span class="sxs-lookup"><span data-stu-id="57e52-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="57e52-159">Angi eller velg en verdi i feltet Kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="57e52-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="57e52-160">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="57e52-160">Click Save.</span></span>

