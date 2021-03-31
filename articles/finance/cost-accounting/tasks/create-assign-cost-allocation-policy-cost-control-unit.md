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
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b22dba0106721c095e6ce2e9b76cb9f5267e1c28
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208733"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="7621e-103">Opprette og tilordne en kostnadsfordelingspolicy til en kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="7621e-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7621e-104">Bruk denne fremgangsmåten til å opprette og tilordne en policy for tildeling av kostnader og de tilsvarende til en enhet for kontroll av kostnaden.</span><span class="sxs-lookup"><span data-stu-id="7621e-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="7621e-105">Denne registreringen bruker USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="7621e-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="7621e-106">Opprette en policy</span><span class="sxs-lookup"><span data-stu-id="7621e-106">Create a policy</span></span>
1. <span data-ttu-id="7621e-107">Gå til Kostnadsregnskap > Policyer > Kostnadsfordelingspolicyer.</span><span class="sxs-lookup"><span data-stu-id="7621e-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="7621e-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7621e-108">Click New.</span></span>
3. <span data-ttu-id="7621e-109">Skriv inn en verdi i feltet Policynavn.</span><span class="sxs-lookup"><span data-stu-id="7621e-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="7621e-110">Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="7621e-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="7621e-111">Velg Organisasjon.</span><span class="sxs-lookup"><span data-stu-id="7621e-111">Select Organization.</span></span>  
5. <span data-ttu-id="7621e-112">Angi eller velg en verdi i feltet Statistisk dimensjon.</span><span class="sxs-lookup"><span data-stu-id="7621e-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="7621e-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7621e-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="7621e-114">Opprette fordelingsregler</span><span class="sxs-lookup"><span data-stu-id="7621e-114">Create allocation rules</span></span>
1. <span data-ttu-id="7621e-115">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7621e-115">Click New.</span></span>
2. <span data-ttu-id="7621e-116">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7621e-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="7621e-117">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="7621e-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="7621e-118">Velg "Total" i feltet Kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="7621e-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="7621e-119">Angi eller velg en verdi i feltet Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="7621e-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="7621e-120">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7621e-120">Click New.</span></span>
7. <span data-ttu-id="7621e-121">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7621e-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="7621e-122">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="7621e-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="7621e-123">Velg "Total" i feltet Kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="7621e-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="7621e-124">Angi eller velg en verdi i feltet Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="7621e-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="7621e-125">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7621e-125">Click New.</span></span>
12. <span data-ttu-id="7621e-126">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7621e-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="7621e-127">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="7621e-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="7621e-128">Velg "Total" i feltet Kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="7621e-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="7621e-129">Angi eller velg en verdi i feltet Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="7621e-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="7621e-130">Fortsett til du har opprettet alle reglene.</span><span class="sxs-lookup"><span data-stu-id="7621e-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="7621e-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7621e-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="7621e-132">Tilordne policyen til en kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="7621e-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="7621e-133">Klikk Policytilordninger for kostnadskontrollenhet.</span><span class="sxs-lookup"><span data-stu-id="7621e-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="7621e-134">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7621e-134">Click New.</span></span>
3. <span data-ttu-id="7621e-135">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7621e-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="7621e-136">Angi en dato i feltet Gyldig fra regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="7621e-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="7621e-137">Reglene er datoeffektive.</span><span class="sxs-lookup"><span data-stu-id="7621e-137">The rules are date-effective.</span></span> <span data-ttu-id="7621e-138">En bruker eller systemet kan utløpe reglene hvis det opprettes en nyere versjon.</span><span class="sxs-lookup"><span data-stu-id="7621e-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="7621e-139">Angi eller velg en verdi i feltet Kostnadskontrollenhet</span><span class="sxs-lookup"><span data-stu-id="7621e-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="7621e-140">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7621e-140">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]