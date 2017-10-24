--- 
title: Opprette og tilordne en kostnadsfordelingspolicy til en kostnadskontrollenhet
description: "Bruk denne fremgangsmåten til å opprette og tilordne en policy for tildeling av kostnader og de tilsvarende til en enhet for kontroll av kostnaden."
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 491d8292b7c951be930d2858362c8107caaa76ff
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="03ec8-103">Opprette og tilordne en kostnadsfordelingspolicy til en kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="03ec8-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="03ec8-104">Bruk denne fremgangsmåten til å opprette og tilordne en policy for tildeling av kostnader og de tilsvarende til en enhet for kontroll av kostnaden.</span><span class="sxs-lookup"><span data-stu-id="03ec8-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="03ec8-105">Denne registreringen bruker USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="03ec8-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="03ec8-106">Opprette en policy</span><span class="sxs-lookup"><span data-stu-id="03ec8-106">Create a policy</span></span>
1. <span data-ttu-id="03ec8-107">Gå til Kostnadsregnskap > Policyer > Kostnadsfordelingspolicyer.</span><span class="sxs-lookup"><span data-stu-id="03ec8-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="03ec8-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="03ec8-108">Click New.</span></span>
3. <span data-ttu-id="03ec8-109">Skriv inn en verdi i feltet Policynavn.</span><span class="sxs-lookup"><span data-stu-id="03ec8-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="03ec8-110">Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="03ec8-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="03ec8-111">Velg Organisasjon.</span><span class="sxs-lookup"><span data-stu-id="03ec8-111">Select Organization.</span></span>  
5. <span data-ttu-id="03ec8-112">Angi eller velg en verdi i feltet Statistisk dimensjon.</span><span class="sxs-lookup"><span data-stu-id="03ec8-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="03ec8-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="03ec8-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="03ec8-114">Opprette fordelingsregler</span><span class="sxs-lookup"><span data-stu-id="03ec8-114">Create allocation rules</span></span>
1. <span data-ttu-id="03ec8-115">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="03ec8-115">Click New.</span></span>
2. <span data-ttu-id="03ec8-116">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="03ec8-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="03ec8-117">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="03ec8-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="03ec8-118">Velg "Total" i feltet Kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="03ec8-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="03ec8-119">Angi eller velg en verdi i feltet Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="03ec8-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="03ec8-120">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="03ec8-120">Click New.</span></span>
7. <span data-ttu-id="03ec8-121">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="03ec8-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="03ec8-122">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="03ec8-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="03ec8-123">Velg "Total" i feltet Kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="03ec8-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="03ec8-124">Angi eller velg en verdi i feltet Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="03ec8-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="03ec8-125">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="03ec8-125">Click New.</span></span>
12. <span data-ttu-id="03ec8-126">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="03ec8-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="03ec8-127">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="03ec8-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="03ec8-128">Velg "Total" i feltet Kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="03ec8-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="03ec8-129">Angi eller velg en verdi i feltet Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="03ec8-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="03ec8-130">Fortsett til du har opprettet alle reglene.</span><span class="sxs-lookup"><span data-stu-id="03ec8-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="03ec8-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="03ec8-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="03ec8-132">Tilordne policyen til en kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="03ec8-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="03ec8-133">Klikk Policytilordninger for kostnadskontrollenhet.</span><span class="sxs-lookup"><span data-stu-id="03ec8-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="03ec8-134">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="03ec8-134">Click New.</span></span>
3. <span data-ttu-id="03ec8-135">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="03ec8-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="03ec8-136">Angi en dato i feltet Gyldig fra regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="03ec8-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="03ec8-137">Reglene er datoeffektive.</span><span class="sxs-lookup"><span data-stu-id="03ec8-137">The rules are date-effective.</span></span> <span data-ttu-id="03ec8-138">En bruker eller systemet kan utløpe reglene hvis det opprettes en nyere versjon.</span><span class="sxs-lookup"><span data-stu-id="03ec8-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="03ec8-139">Angi eller velg en verdi i feltet Kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="03ec8-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="03ec8-140">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="03ec8-140">Click Save.</span></span>


