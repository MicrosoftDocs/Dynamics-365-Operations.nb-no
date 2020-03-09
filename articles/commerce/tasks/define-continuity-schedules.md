---
title: " Definere kontinuitetsplaner"
description: Dette emnet hjelper med å konfigurere et kontinuitetsprogram (også kjent som regelmessige ordrer).
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a438656730863f345080bc99fef24cfff724f528
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023539"
---
# <a name="define-continuity-schedules"></a><span data-ttu-id="9b056-103"> Definere kontinuitetsplaner</span><span class="sxs-lookup"><span data-stu-id="9b056-103">Define continuity schedules</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9b056-104">Dette emnet hjelper med å konfigurere et kontinuitetsprogram (også kjent som regelmessige ordrer).</span><span class="sxs-lookup"><span data-stu-id="9b056-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="9b056-105">Dette emnet bruker demonstrasjonsdata i firmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="9b056-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="9b056-106">Opprette kontinuitetsprogram</span><span class="sxs-lookup"><span data-stu-id="9b056-106">Create continuity program</span></span>
1. <span data-ttu-id="9b056-107">Gå til Detaljhandel og handel > Kontinuitet > Kontinuitetsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="9b056-107">Go to Retail and Commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="9b056-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9b056-108">Click New.</span></span>
3. <span data-ttu-id="9b056-109">I plan-ID-feltet skriver du inn ID-en for kontinuitetsplanen.</span><span class="sxs-lookup"><span data-stu-id="9b056-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="9b056-110">Velg Første hendelse i Ordrestart-feltet.</span><span class="sxs-lookup"><span data-stu-id="9b056-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="9b056-111">Hvis en kunde legger inn en ny ordre for kontinuitetsprogrammet, er det to alternativer for å sende produktet:  1.</span><span class="sxs-lookup"><span data-stu-id="9b056-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="9b056-112">Første hendelse: det første produktet i kontinuitetsprogrammet vil bli levert.</span><span class="sxs-lookup"><span data-stu-id="9b056-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="9b056-113">2</span><span class="sxs-lookup"><span data-stu-id="9b056-113">2.</span></span> <span data-ttu-id="9b056-114">Gjeldende hendelse: gjeldende produkt vil bli sendt.</span><span class="sxs-lookup"><span data-stu-id="9b056-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="9b056-115">For eksempel.</span><span class="sxs-lookup"><span data-stu-id="9b056-115">For example.</span></span> <span data-ttu-id="9b056-116">Tre måneder inn i programmet vil kunden motta det tredje i programmet.</span><span class="sxs-lookup"><span data-stu-id="9b056-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="9b056-117">Velg Ja for å be om ordrestartdato.</span><span class="sxs-lookup"><span data-stu-id="9b056-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="9b056-118">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="9b056-118">Click Add line.</span></span>
7. <span data-ttu-id="9b056-119">Skriv inn varenummeret for det første produktet (0013) i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="9b056-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="9b056-120">Skriv inn CP.</span><span class="sxs-lookup"><span data-stu-id="9b056-120">Type 'CP'.</span></span>
9. <span data-ttu-id="9b056-121">Angi datoen da det første produktet skal være tilgjengelig for ordre.</span><span class="sxs-lookup"><span data-stu-id="9b056-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="9b056-122">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="9b056-122">Click Add line.</span></span>
11. <span data-ttu-id="9b056-123">Skriv inn 0014 i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="9b056-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="9b056-124">Fjern verdien i feltet Datointervallkode slik at feltet er tomt.</span><span class="sxs-lookup"><span data-stu-id="9b056-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="9b056-125">I denne prosedyren, fjern datointervallet.</span><span class="sxs-lookup"><span data-stu-id="9b056-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="9b056-126">Du angir datoen som trinnvis fra startdatoen for den første varen.</span><span class="sxs-lookup"><span data-stu-id="9b056-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="9b056-127">Her skal du angi intervallet for levering av produktene.</span><span class="sxs-lookup"><span data-stu-id="9b056-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="9b056-128">Skriv inn 30.</span><span class="sxs-lookup"><span data-stu-id="9b056-128">Type '30'.</span></span>
    * <span data-ttu-id="9b056-129">For et månedlig program, skal du angi 30 dager for intervallet.</span><span class="sxs-lookup"><span data-stu-id="9b056-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="9b056-130">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="9b056-130">Click Add line.</span></span>
15. <span data-ttu-id="9b056-131">Skriv inn 0015 i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="9b056-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="9b056-132">Skriv inn Slutt.</span><span class="sxs-lookup"><span data-stu-id="9b056-132">Type 'End'.</span></span>
17. <span data-ttu-id="9b056-133">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9b056-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="9b056-134">Tilordne til kontinuitetsvare</span><span class="sxs-lookup"><span data-stu-id="9b056-134">Assign to continuity item</span></span>
1. <span data-ttu-id="9b056-135">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="9b056-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="9b056-136">Velg vare 0016.</span><span class="sxs-lookup"><span data-stu-id="9b056-136">Select item '0016'.</span></span>
    * <span data-ttu-id="9b056-137">For denne fremgangsmåten velger du varenummer 0016.</span><span class="sxs-lookup"><span data-stu-id="9b056-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="9b056-138">Du vil vanligvis ha opprettet et frigitt produkt med mer kontinuitetsforretningslogikk når det legges inn på en salgsordre i telefonsenteret.</span><span class="sxs-lookup"><span data-stu-id="9b056-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="9b056-139">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9b056-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9b056-140">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="9b056-140">Click Edit.</span></span>
5. <span data-ttu-id="9b056-141">Vis eller skjul delen Selg.</span><span class="sxs-lookup"><span data-stu-id="9b056-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="9b056-142">Her skal du angi kontinuitetsprogrammet som denne varen representerer.</span><span class="sxs-lookup"><span data-stu-id="9b056-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="9b056-143">Skriv inn tidsplan-ID-en du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="9b056-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="9b056-144">Når denne varen selges i et telefonsenter, brukes mer forretningslogikk fra det valgte kontinuitetsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="9b056-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="9b056-145">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9b056-145">Click Save.</span></span>
