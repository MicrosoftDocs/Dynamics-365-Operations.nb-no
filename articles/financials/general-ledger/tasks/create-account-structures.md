---
title: Opprette kontostrukturer
description: Denne oppgaveveiledningen går gjennom oppretting av en kontostruktur.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b100d5da6ec26dc386c0c6cb0793245531eb0d8
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916236"
---
# <a name="create-account-structures"></a><span data-ttu-id="7860f-103">Opprette kontostrukturer</span><span class="sxs-lookup"><span data-stu-id="7860f-103">Create account structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7860f-104">Denne oppgaveveiledningen går gjennom oppretting av en kontostruktur.</span><span class="sxs-lookup"><span data-stu-id="7860f-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="7860f-105">Trinnene bruker demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="7860f-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="7860f-106">Gå til **Navigasjonsrute > Moduler > Økonomimodul > Kontoplan > Strukturer > Konfigurer kontostrukturer**.</span><span class="sxs-lookup"><span data-stu-id="7860f-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="7860f-107">Klikk **Ny** i **handlingsruten** for å åpne dialogboksen for rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="7860f-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="7860f-108">Skriv inn et navn som beskriver formålet med kontostrukturen i feltet **Kontostruktur**.</span><span class="sxs-lookup"><span data-stu-id="7860f-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="7860f-109">Skriv inn en beskrivelse for å angi formålet med kontostrukturen i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="7860f-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="7860f-110">Klikk **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="7860f-110">Click **Create**.</span></span>
6. <span data-ttu-id="7860f-111">I **Segmenter og tillatte verdier** klikker du **Legg til segment**.</span><span class="sxs-lookup"><span data-stu-id="7860f-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="7860f-112">Velg dimensjonen som skal legges til kontostrukturen i Dimensjoner-listen.</span><span class="sxs-lookup"><span data-stu-id="7860f-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="7860f-113">Klikk **Legg til segment** på slutten av listen.</span><span class="sxs-lookup"><span data-stu-id="7860f-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="7860f-114">Gjenta trinn 6 til 9 etter behov.</span><span class="sxs-lookup"><span data-stu-id="7860f-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="7860f-115">Velg segmentet for å redigere de tillatte verdiene i delen **Tillatte verdidetaljer**.</span><span class="sxs-lookup"><span data-stu-id="7860f-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="7860f-116">Klikk for eksempel i **Hovedkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7860f-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="7860f-117">Velg et alternativ, for eksempel er mellom og inkluderer i **Operator**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7860f-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="7860f-118">Skriv inn en verdi i **Verdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7860f-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="7860f-119">For eksempel 600000.</span><span class="sxs-lookup"><span data-stu-id="7860f-119">For example, 600000.</span></span>  
13. <span data-ttu-id="7860f-120">Skriv inn en verdi i feltet **via**.</span><span class="sxs-lookup"><span data-stu-id="7860f-120">In the **through** field, type a value.</span></span> <span data-ttu-id="7860f-121">For eksempel 699999.</span><span class="sxs-lookup"><span data-stu-id="7860f-121">For example, 699999.</span></span>  
14. <span data-ttu-id="7860f-122">I delen **Tillatte verdidetaljer** klikker du **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="7860f-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="7860f-123">Gjenta trinn 10 til 15 etter behov.</span><span class="sxs-lookup"><span data-stu-id="7860f-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="7860f-124">I delen **Tillatte verdidetaljer** klikker du **Legg til nye kriterier**.</span><span class="sxs-lookup"><span data-stu-id="7860f-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="7860f-125">Velg et alternativ, for eksempel er mellom og inkluderer i Operator-feltet.</span><span class="sxs-lookup"><span data-stu-id="7860f-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="7860f-126">Skriv inn en verdi i **Verdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7860f-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="7860f-127">For eksempel 033.</span><span class="sxs-lookup"><span data-stu-id="7860f-127">For example, 033.</span></span>  
19. <span data-ttu-id="7860f-128">Skriv inn en verdi i feltet **via**.</span><span class="sxs-lookup"><span data-stu-id="7860f-128">In the **through** field, type a value.</span></span> <span data-ttu-id="7860f-129">For eksempel 034.</span><span class="sxs-lookup"><span data-stu-id="7860f-129">For example, 034.</span></span>  
20. <span data-ttu-id="7860f-130">Klikk **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="7860f-130">Click **Apply**.</span></span>
21. <span data-ttu-id="7860f-131">Velg segmentet for å redigere de tillatte verdiene i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="7860f-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="7860f-132">For eksempel kostsenter</span><span class="sxs-lookup"><span data-stu-id="7860f-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="7860f-133">Skriv inn en verdi i **CostCenter**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7860f-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="7860f-134">For eksempel 007..021.</span><span class="sxs-lookup"><span data-stu-id="7860f-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="7860f-135">I **Segmenter og tillatte verdier** klikker du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="7860f-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="7860f-136">Skriv inn en verdi i **MainAccount**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7860f-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="7860f-137">For eksempel 600000..699999</span><span class="sxs-lookup"><span data-stu-id="7860f-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="7860f-138">Velg segmentet for å redigere de tillatte verdiene i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="7860f-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="7860f-139">For eksempel Avdeling.</span><span class="sxs-lookup"><span data-stu-id="7860f-139">For example, Department.</span></span>  
26. <span data-ttu-id="7860f-140">Skriv inn en verdi i feltet Avdeling.</span><span class="sxs-lookup"><span data-stu-id="7860f-140">In the Department field, type a value.</span></span> <span data-ttu-id="7860f-141">For eksempel 032.</span><span class="sxs-lookup"><span data-stu-id="7860f-141">For example, 032.</span></span>  
27. <span data-ttu-id="7860f-142">Skriv inn en verdi i feltet CostCenter.</span><span class="sxs-lookup"><span data-stu-id="7860f-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="7860f-143">For eksempel 086.</span><span class="sxs-lookup"><span data-stu-id="7860f-143">For example, 086.</span></span>  
28. <span data-ttu-id="7860f-144">Klikk **Valider** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="7860f-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="7860f-145">Klikk **Aktiver** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="7860f-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="7860f-146">Klikk **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="7860f-146">Click **Activate**.</span></span>

