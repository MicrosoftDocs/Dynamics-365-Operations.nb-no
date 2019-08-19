---
title: Opprette og tilordne en kostnadsfordelingspolicy til en kostnadskontrollenhet
description: Bruk denne fremgangsmåten til å opprette og tilordne en policy for tildeling av kostnader og de tilsvarende til en enhet for kontroll av kostnaden.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f0422a9aaf95184b556293bf6ebcaf4dcfb5b59
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841399"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="1d126-103">Opprette og tilordne en kostnadsfordelingspolicy til en kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="1d126-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1d126-104">Bruk denne fremgangsmåten til å opprette og tilordne en policy for tildeling av kostnader og de tilsvarende til en enhet for kontroll av kostnaden.</span><span class="sxs-lookup"><span data-stu-id="1d126-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="1d126-105">Denne registreringen bruker USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="1d126-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="1d126-106">Opprette en policy</span><span class="sxs-lookup"><span data-stu-id="1d126-106">Create a policy</span></span>
1. <span data-ttu-id="1d126-107">Gå til Kostnadsregnskap > Policyer > Kostnadsfordelingspolicyer.</span><span class="sxs-lookup"><span data-stu-id="1d126-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="1d126-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="1d126-108">Click New.</span></span>
3. <span data-ttu-id="1d126-109">Skriv inn en verdi i feltet Policynavn.</span><span class="sxs-lookup"><span data-stu-id="1d126-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="1d126-110">Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="1d126-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="1d126-111">Velg Organisasjon.</span><span class="sxs-lookup"><span data-stu-id="1d126-111">Select Organization.</span></span>  
5. <span data-ttu-id="1d126-112">Angi eller velg en verdi i feltet Statistisk dimensjon.</span><span class="sxs-lookup"><span data-stu-id="1d126-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="1d126-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="1d126-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="1d126-114">Opprette fordelingsregler</span><span class="sxs-lookup"><span data-stu-id="1d126-114">Create allocation rules</span></span>
1. <span data-ttu-id="1d126-115">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="1d126-115">Click New.</span></span>
2. <span data-ttu-id="1d126-116">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="1d126-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="1d126-117">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="1d126-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="1d126-118">Velg "Total" i feltet Kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="1d126-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="1d126-119">Angi eller velg en verdi i feltet Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="1d126-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="1d126-120">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="1d126-120">Click New.</span></span>
7. <span data-ttu-id="1d126-121">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="1d126-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="1d126-122">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="1d126-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="1d126-123">Velg "Total" i feltet Kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="1d126-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="1d126-124">Angi eller velg en verdi i feltet Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="1d126-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="1d126-125">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="1d126-125">Click New.</span></span>
12. <span data-ttu-id="1d126-126">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="1d126-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="1d126-127">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="1d126-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="1d126-128">Velg "Total" i feltet Kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="1d126-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="1d126-129">Angi eller velg en verdi i feltet Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="1d126-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="1d126-130">Fortsett til du har opprettet alle reglene.</span><span class="sxs-lookup"><span data-stu-id="1d126-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="1d126-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="1d126-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="1d126-132">Tilordne policyen til en kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="1d126-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="1d126-133">Klikk Policytilordninger for kostnadskontrollenhet.</span><span class="sxs-lookup"><span data-stu-id="1d126-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="1d126-134">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="1d126-134">Click New.</span></span>
3. <span data-ttu-id="1d126-135">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="1d126-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="1d126-136">Angi en dato i feltet Gyldig fra regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="1d126-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="1d126-137">Reglene er datoeffektive.</span><span class="sxs-lookup"><span data-stu-id="1d126-137">The rules are date-effective.</span></span> <span data-ttu-id="1d126-138">En bruker eller systemet kan utløpe reglene hvis det opprettes en nyere versjon.</span><span class="sxs-lookup"><span data-stu-id="1d126-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="1d126-139">Angi eller velg en verdi i feltet Kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="1d126-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="1d126-140">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="1d126-140">Click Save.</span></span>

