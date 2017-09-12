--- 
title: Opprette og tilordne en kostnadsdistribusjonspolicy til en kostnadskontrollenhet
description: "Kostnadsfordelingsregler brukes til å distribuere kostnader som er økonomisk opptelt i et kollektivt kostsenter."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fbd44816fc2f2569dd477fc21f59418a575bb835
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="f4e26-103">Opprette og tilordne en kostnadsdistribusjonspolicy til en kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="f4e26-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4e26-104">Kostnadsfordelingsregler brukes til å distribuere kostnader som er økonomisk opptelt i et kollektivt kostsenter.</span><span class="sxs-lookup"><span data-stu-id="f4e26-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="f4e26-105">Regnskapsføreren sørger for at kostnaden fordeles til kostsentrene, basert på den valgte fordelingen grunnleggende.</span><span class="sxs-lookup"><span data-stu-id="f4e26-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="f4e26-106">En policy og de tilsvarende reglene er tilordnet en kontrollenhet for kost.</span><span class="sxs-lookup"><span data-stu-id="f4e26-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="f4e26-107">Denne håndboken oppgaven bruker et eksempel for å vise hvordan du oppretter en policy for distribusjon av kostnadene og de tilsvarende.</span><span class="sxs-lookup"><span data-stu-id="f4e26-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="f4e26-108">Opprette en policy</span><span class="sxs-lookup"><span data-stu-id="f4e26-108">Create a policy</span></span>
1. <span data-ttu-id="f4e26-109">Gå til Kostnadsregnskap > Policyer > Kostnadsdistribusjonspolicyer.</span><span class="sxs-lookup"><span data-stu-id="f4e26-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="f4e26-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f4e26-110">Click New.</span></span>
3. <span data-ttu-id="f4e26-111">Skriv inn en verdi i feltet Policynavn.</span><span class="sxs-lookup"><span data-stu-id="f4e26-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="f4e26-112">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f4e26-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f4e26-113">Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="f4e26-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="f4e26-114">Velg Organisasjon.</span><span class="sxs-lookup"><span data-stu-id="f4e26-114">Select Organization.</span></span>  
6. <span data-ttu-id="f4e26-115">Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="f4e26-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="f4e26-116">Velg CD P/L.</span><span class="sxs-lookup"><span data-stu-id="f4e26-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="f4e26-117">Angi eller velg en verdi i feltet Statistisk dimensjon.</span><span class="sxs-lookup"><span data-stu-id="f4e26-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="f4e26-118">Velg Statistiske elementer.</span><span class="sxs-lookup"><span data-stu-id="f4e26-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="f4e26-119">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f4e26-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="f4e26-120">Opprette regler for policyen</span><span class="sxs-lookup"><span data-stu-id="f4e26-120">Create rules for the policy</span></span>
1. <span data-ttu-id="f4e26-121">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f4e26-121">Click New.</span></span>
2. <span data-ttu-id="f4e26-122">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f4e26-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="f4e26-123">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="f4e26-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="f4e26-124">Utvid hierarkiet for å velge 094.</span><span class="sxs-lookup"><span data-stu-id="f4e26-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="f4e26-125">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="f4e26-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="f4e26-126">Velg Andre driftsutgifter, og velg deretter 605110 rengjøring.</span><span class="sxs-lookup"><span data-stu-id="f4e26-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="f4e26-127">Velg et alternativ i feltet Kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="f4e26-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="f4e26-128">Velg Fast kostnad.</span><span class="sxs-lookup"><span data-stu-id="f4e26-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="f4e26-129">Angi eller velg en verdi i feltet Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="f4e26-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="f4e26-130">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f4e26-130">Click New.</span></span>
8. <span data-ttu-id="f4e26-131">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f4e26-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="f4e26-132">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="f4e26-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="f4e26-133">Utvid hierarkiet for å velge 094.</span><span class="sxs-lookup"><span data-stu-id="f4e26-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="f4e26-134">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="f4e26-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="f4e26-135">Velg Andre driftsutgifter, og velg deretter 605150 leie.</span><span class="sxs-lookup"><span data-stu-id="f4e26-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="f4e26-136">Velg et alternativ i feltet Kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="f4e26-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="f4e26-137">Velg Fast kostnad.</span><span class="sxs-lookup"><span data-stu-id="f4e26-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="f4e26-138">Angi eller velg en verdi i feltet Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="f4e26-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="f4e26-139">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f4e26-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="f4e26-140">Tilordne regler til en kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="f4e26-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="f4e26-141">Klikk Policytilordninger for kostnadskontrollenhet.</span><span class="sxs-lookup"><span data-stu-id="f4e26-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="f4e26-142">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f4e26-142">Click New.</span></span>
3. <span data-ttu-id="f4e26-143">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f4e26-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f4e26-144">Angi en dato i feltet Gyldig fra regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="f4e26-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="f4e26-145">Velg 1. September i gyldige regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="f4e26-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="f4e26-146">Angi eller velg en verdi i feltet Kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="f4e26-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="f4e26-147">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f4e26-147">Click Save.</span></span>


