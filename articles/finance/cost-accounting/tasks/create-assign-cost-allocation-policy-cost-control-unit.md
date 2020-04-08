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
ms.openlocfilehash: 0a4ba39b5dbba20a58066054da2e24613381cfaa
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144447"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="c8e8f-103">Opprette og tilordne en kostnadsfordelingspolicy til en kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="c8e8f-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c8e8f-104">Bruk denne fremgangsmåten til å opprette og tilordne en policy for tildeling av kostnader og de tilsvarende til en enhet for kontroll av kostnaden.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="c8e8f-105">Denne registreringen bruker USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="c8e8f-106">Opprette en policy</span><span class="sxs-lookup"><span data-stu-id="c8e8f-106">Create a policy</span></span>
1. <span data-ttu-id="c8e8f-107">Gå til Kostnadsregnskap > Policyer > Kostnadsfordelingspolicyer.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="c8e8f-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-108">Click New.</span></span>
3. <span data-ttu-id="c8e8f-109">Skriv inn en verdi i feltet Policynavn.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="c8e8f-110">Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="c8e8f-111">Velg Organisasjon.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-111">Select Organization.</span></span>  
5. <span data-ttu-id="c8e8f-112">Angi eller velg en verdi i feltet Statistisk dimensjon.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="c8e8f-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="c8e8f-114">Opprette fordelingsregler</span><span class="sxs-lookup"><span data-stu-id="c8e8f-114">Create allocation rules</span></span>
1. <span data-ttu-id="c8e8f-115">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-115">Click New.</span></span>
2. <span data-ttu-id="c8e8f-116">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="c8e8f-117">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="c8e8f-118">Velg "Total" i feltet Kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="c8e8f-119">Angi eller velg en verdi i feltet Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="c8e8f-120">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-120">Click New.</span></span>
7. <span data-ttu-id="c8e8f-121">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="c8e8f-122">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="c8e8f-123">Velg "Total" i feltet Kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="c8e8f-124">Angi eller velg en verdi i feltet Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="c8e8f-125">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-125">Click New.</span></span>
12. <span data-ttu-id="c8e8f-126">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="c8e8f-127">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="c8e8f-128">Velg "Total" i feltet Kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="c8e8f-129">Angi eller velg en verdi i feltet Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="c8e8f-130">Fortsett til du har opprettet alle reglene.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="c8e8f-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="c8e8f-132">Tilordne policyen til en kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="c8e8f-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="c8e8f-133">Klikk Policytilordninger for kostnadskontrollenhet.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="c8e8f-134">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-134">Click New.</span></span>
3. <span data-ttu-id="c8e8f-135">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c8e8f-136">Angi en dato i feltet Gyldig fra regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="c8e8f-137">Reglene er datoeffektive.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-137">The rules are date-effective.</span></span> <span data-ttu-id="c8e8f-138">En bruker eller systemet kan utløpe reglene hvis det opprettes en nyere versjon.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="c8e8f-139">Angi eller velg en verdi i feltet Kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="c8e8f-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="c8e8f-140">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c8e8f-140">Click Save.</span></span>

