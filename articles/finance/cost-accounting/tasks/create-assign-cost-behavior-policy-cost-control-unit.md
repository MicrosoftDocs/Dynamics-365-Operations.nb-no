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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58f888a373af33832c24518fbb5483c3de2d1a58
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208709"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="aee12-103">Opprette og tilordne en kostnadsatferdspolicy til en kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="aee12-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aee12-104">Kostnadsatferd er klassifiseringen av kostnader som faste eller variable.</span><span class="sxs-lookup"><span data-stu-id="aee12-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="aee12-105">En policy og de tilsvarende reglene må tilordnes til en kostnadskontrollenhet for at policyen skal aktiveres.</span><span class="sxs-lookup"><span data-stu-id="aee12-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="aee12-106">Bruk denne fremgangsmåten til å opprette en policy og deretter tilordne policyen til en kostnadskontrollenhet.</span><span class="sxs-lookup"><span data-stu-id="aee12-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="aee12-107">Opprette et hierarki for kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="aee12-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="aee12-108">Gå til Kostnadsregnskap > Dimensjoner > Dimensjonshierarkier.</span><span class="sxs-lookup"><span data-stu-id="aee12-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="aee12-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="aee12-109">Click New.</span></span>
3. <span data-ttu-id="aee12-110">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="aee12-110">Click Create.</span></span>
4. <span data-ttu-id="aee12-111">Skriv inn "Hierarki for kostnadsatferd" i feltet Dimensjonshierarkinavn.</span><span class="sxs-lookup"><span data-stu-id="aee12-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="aee12-112">Angi eller velg en verdi i feltet Dimensjon.</span><span class="sxs-lookup"><span data-stu-id="aee12-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="aee12-113">Velg Kostnadselementer.</span><span class="sxs-lookup"><span data-stu-id="aee12-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="aee12-114">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="aee12-114">Click Save.</span></span>
7. <span data-ttu-id="aee12-115">Klikk Vis hierarki.</span><span class="sxs-lookup"><span data-stu-id="aee12-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="aee12-116">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="aee12-116">Click New.</span></span>
9. <span data-ttu-id="aee12-117">Skriv inn en verdi i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="aee12-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="aee12-118">Angi Fast kostnad.</span><span class="sxs-lookup"><span data-stu-id="aee12-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="aee12-119">Velg "Hierarki for kostnadsatferd" i treet.</span><span class="sxs-lookup"><span data-stu-id="aee12-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="aee12-120">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="aee12-120">Click New.</span></span>
12. <span data-ttu-id="aee12-121">Skriv inn en verdi i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="aee12-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="aee12-122">Angi Variabel kostnad.</span><span class="sxs-lookup"><span data-stu-id="aee12-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="aee12-123">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="aee12-123">Click Save.</span></span>
14. <span data-ttu-id="aee12-124">Velg "Hierarki for kostnadsatferd\Fast kostnad" i treet.</span><span class="sxs-lookup"><span data-stu-id="aee12-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="aee12-125">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="aee12-125">Click New.</span></span>
16. <span data-ttu-id="aee12-126">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="aee12-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="aee12-127">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="aee12-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="aee12-128">Området for dimensjonsmedlemmene kan inneholde mellomrom, men medlemmene kan ikke overlappe.</span><span class="sxs-lookup"><span data-stu-id="aee12-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="aee12-129">Angi eller velg en verdi i feltet Til dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="aee12-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="aee12-130">Området for dimensjonsmedlemmene kan inneholde mellomrom, men medlemmene kan ikke overlappe.</span><span class="sxs-lookup"><span data-stu-id="aee12-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="aee12-131">Velg "Hierarki for kostnadsatferd\Variabel kostnad" i treet.</span><span class="sxs-lookup"><span data-stu-id="aee12-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="aee12-132">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="aee12-132">Click New.</span></span>
21. <span data-ttu-id="aee12-133">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="aee12-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="aee12-134">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="aee12-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="aee12-135">Området for dimensjonsmedlemmene kan inneholde mellomrom, men medlemmene kan ikke overlappe.</span><span class="sxs-lookup"><span data-stu-id="aee12-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="aee12-136">Angi eller velg en verdi i feltet Til dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="aee12-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="aee12-137">Området for dimensjonsmedlemmene kan inneholde mellomrom, men medlemmene kan ikke overlappe.</span><span class="sxs-lookup"><span data-stu-id="aee12-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="aee12-138">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="aee12-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="aee12-139">Opprette policyen og regler</span><span class="sxs-lookup"><span data-stu-id="aee12-139">Create the policy and rules</span></span>
1. <span data-ttu-id="aee12-140">Gå til Kostnadsregnskap > Policyer > Policyer for kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="aee12-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="aee12-141">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="aee12-141">Click New.</span></span>
3. <span data-ttu-id="aee12-142">Skriv inn en verdi i feltet Policynavn.</span><span class="sxs-lookup"><span data-stu-id="aee12-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="aee12-143">Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="aee12-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="aee12-144">Velg policyhierarkiet du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="aee12-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="aee12-145">Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="aee12-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="aee12-146">Velg Organisasjon.</span><span class="sxs-lookup"><span data-stu-id="aee12-146">Select Organization.</span></span>  
6. <span data-ttu-id="aee12-147">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="aee12-147">Click Save.</span></span>
7. <span data-ttu-id="aee12-148">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="aee12-148">Click New.</span></span>
8. <span data-ttu-id="aee12-149">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="aee12-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="aee12-150">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="aee12-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="aee12-151">Utvid hierarkiet for å velge Variabel kostnad.</span><span class="sxs-lookup"><span data-stu-id="aee12-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="aee12-152">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="aee12-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="aee12-153">Som standard er den variable prosentdelen 100 prosent.</span><span class="sxs-lookup"><span data-stu-id="aee12-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="aee12-154">Klikk Policytilordninger for kostnadskontrollenhet.</span><span class="sxs-lookup"><span data-stu-id="aee12-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="aee12-155">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="aee12-155">Click New.</span></span>
13. <span data-ttu-id="aee12-156">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="aee12-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="aee12-157">Angi en dato i feltet Gyldig fra regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="aee12-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="aee12-158">Reglene er datoeffektive, og en bruker eller systemet kan utløpe en regel hvis det opprettes en nyere versjon.</span><span class="sxs-lookup"><span data-stu-id="aee12-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="aee12-159">Angi eller velg en verdi i feltet Kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="aee12-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="aee12-160">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="aee12-160">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]