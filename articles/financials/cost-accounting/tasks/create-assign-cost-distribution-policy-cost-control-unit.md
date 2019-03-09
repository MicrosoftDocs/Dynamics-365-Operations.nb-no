---
title: Opprette og tilordne en kostnadsdistribusjonspolicy til en kostnadskontrollenhet
description: Kostnadsfordelingsregler brukes til å distribuere kostnader som er økonomisk opptelt i et kollektivt kostsenter.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46ba6322f2cea7828033c214502accdf73f073be
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "308466"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="7fe79-103">Opprette og tilordne en kostnadsdistribusjonspolicy til en kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="7fe79-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7fe79-104">Kostnadsfordelingsregler brukes til å distribuere kostnader som er økonomisk opptelt i et kollektivt kostsenter.</span><span class="sxs-lookup"><span data-stu-id="7fe79-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="7fe79-105">Regnskapsføreren sørger for at kostnaden fordeles til kostsentrene, basert på den valgte fordelingen grunnleggende.</span><span class="sxs-lookup"><span data-stu-id="7fe79-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="7fe79-106">En policy og de tilsvarende reglene er tilordnet en kontrollenhet for kost.</span><span class="sxs-lookup"><span data-stu-id="7fe79-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="7fe79-107">Denne håndboken oppgaven bruker et eksempel for å vise hvordan du oppretter en policy for distribusjon av kostnadene og de tilsvarende.</span><span class="sxs-lookup"><span data-stu-id="7fe79-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="7fe79-108">Opprette en policy</span><span class="sxs-lookup"><span data-stu-id="7fe79-108">Create a policy</span></span>
1. <span data-ttu-id="7fe79-109">Gå til Kostnadsregnskap > Policyer > Kostnadsdistribusjonspolicyer.</span><span class="sxs-lookup"><span data-stu-id="7fe79-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="7fe79-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7fe79-110">Click New.</span></span>
3. <span data-ttu-id="7fe79-111">Skriv inn en verdi i feltet Policynavn.</span><span class="sxs-lookup"><span data-stu-id="7fe79-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="7fe79-112">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="7fe79-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7fe79-113">Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="7fe79-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="7fe79-114">Velg Organisasjon.</span><span class="sxs-lookup"><span data-stu-id="7fe79-114">Select Organization.</span></span>  
6. <span data-ttu-id="7fe79-115">Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="7fe79-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="7fe79-116">Velg CD P/L.</span><span class="sxs-lookup"><span data-stu-id="7fe79-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="7fe79-117">Angi eller velg en verdi i feltet Statistisk dimensjon.</span><span class="sxs-lookup"><span data-stu-id="7fe79-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="7fe79-118">Velg Statistiske elementer.</span><span class="sxs-lookup"><span data-stu-id="7fe79-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="7fe79-119">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7fe79-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="7fe79-120">Opprette regler for policyen</span><span class="sxs-lookup"><span data-stu-id="7fe79-120">Create rules for the policy</span></span>
1. <span data-ttu-id="7fe79-121">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7fe79-121">Click New.</span></span>
2. <span data-ttu-id="7fe79-122">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7fe79-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="7fe79-123">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="7fe79-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="7fe79-124">Utvid hierarkiet for å velge 094.</span><span class="sxs-lookup"><span data-stu-id="7fe79-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="7fe79-125">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="7fe79-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="7fe79-126">Velg Andre driftsutgifter, og velg deretter 605110 rengjøring.</span><span class="sxs-lookup"><span data-stu-id="7fe79-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="7fe79-127">Velg et alternativ i feltet Kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="7fe79-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="7fe79-128">Velg Fast kostnad.</span><span class="sxs-lookup"><span data-stu-id="7fe79-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="7fe79-129">Angi eller velg en verdi i feltet Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="7fe79-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="7fe79-130">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7fe79-130">Click New.</span></span>
8. <span data-ttu-id="7fe79-131">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7fe79-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="7fe79-132">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="7fe79-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="7fe79-133">Utvid hierarkiet for å velge 094.</span><span class="sxs-lookup"><span data-stu-id="7fe79-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="7fe79-134">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="7fe79-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="7fe79-135">Velg Andre driftsutgifter, og velg deretter 605150 leie.</span><span class="sxs-lookup"><span data-stu-id="7fe79-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="7fe79-136">Velg et alternativ i feltet Kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="7fe79-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="7fe79-137">Velg Fast kostnad.</span><span class="sxs-lookup"><span data-stu-id="7fe79-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="7fe79-138">Angi eller velg en verdi i feltet Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="7fe79-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="7fe79-139">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7fe79-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="7fe79-140">Tilordne regler til en kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="7fe79-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="7fe79-141">Klikk Policytilordninger for kostnadskontrollenhet.</span><span class="sxs-lookup"><span data-stu-id="7fe79-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="7fe79-142">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7fe79-142">Click New.</span></span>
3. <span data-ttu-id="7fe79-143">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7fe79-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="7fe79-144">Angi en dato i feltet Gyldig fra regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="7fe79-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="7fe79-145">Velg 1. September i gyldige regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="7fe79-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="7fe79-146">Angi eller velg en verdi i feltet Kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="7fe79-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="7fe79-147">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7fe79-147">Click Save.</span></span>

