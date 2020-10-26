---
title: Opprette et hierarki for organisasjonsrapport
description: Bruk denne fremgangsmåten til å opprette en rapport hierarki for rapportering av organisasjonen.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57203a7ddbacd631cbf800fb3a98e35a485cb74f
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976265"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="3682d-103">Opprette et hierarki for organisasjonsrapport</span><span class="sxs-lookup"><span data-stu-id="3682d-103">Create an organization report hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3682d-104">Bruk denne fremgangsmåten til å opprette en rapport hierarki for rapportering av organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="3682d-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="3682d-105">Formålet med denne registreringen er å føre deg gjennom dimensjonshierarkiet slik at du kan fortsette til hele organisasjonen rapporteringsstrukturen er opprettet.</span><span class="sxs-lookup"><span data-stu-id="3682d-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="3682d-106">Denne registreringen bruker USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="3682d-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="3682d-107">Gå til Kostnadsregnskap > Dimensjoner > Dimensjonshierarkier.</span><span class="sxs-lookup"><span data-stu-id="3682d-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="3682d-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3682d-108">Click New.</span></span>
3. <span data-ttu-id="3682d-109">Velg "Dimensjonshierarki for klassifisering" i HierarchyTypeComboBox-feltet.</span><span class="sxs-lookup"><span data-stu-id="3682d-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="3682d-110">Velg Hierarki for dimensjonsklassifisering.</span><span class="sxs-lookup"><span data-stu-id="3682d-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="3682d-111">Hierarki for dimensjonklassifisering brukes til å definere regler og til rapporteringsformål.</span><span class="sxs-lookup"><span data-stu-id="3682d-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="3682d-112">Det støtter alle dimensjoner, for eksempel kostnadsobjekter, kostnadselementer og statistiske dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="3682d-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="3682d-113">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="3682d-113">Click Create.</span></span>
5. <span data-ttu-id="3682d-114">Skriv inn "Organisasjon USP2" i feltet Dimensjonshierarkinavn.</span><span class="sxs-lookup"><span data-stu-id="3682d-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="3682d-115">Angi eller velg en verdi i feltet Dimensjon.</span><span class="sxs-lookup"><span data-stu-id="3682d-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="3682d-116">Velg Kostsentra.</span><span class="sxs-lookup"><span data-stu-id="3682d-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="3682d-117">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3682d-117">Click Save.</span></span>
8. <span data-ttu-id="3682d-118">Klikk Vis hierarki.</span><span class="sxs-lookup"><span data-stu-id="3682d-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="3682d-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3682d-119">Click New.</span></span>
10. <span data-ttu-id="3682d-120">Skriv inn "CEO" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="3682d-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="3682d-121">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3682d-121">Click Save.</span></span>
12. <span data-ttu-id="3682d-122">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3682d-122">Click New.</span></span>
13. <span data-ttu-id="3682d-123">Skriv inn "CEO-kostsentra" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="3682d-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="3682d-124">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3682d-124">Click Save.</span></span>
15. <span data-ttu-id="3682d-125">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3682d-125">Click New.</span></span>
16. <span data-ttu-id="3682d-126">Skriv inn "Region Øst" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="3682d-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="3682d-127">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3682d-127">Click Save.</span></span>
18. <span data-ttu-id="3682d-128">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3682d-128">Click New.</span></span>
19. <span data-ttu-id="3682d-129">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3682d-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="3682d-130">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="3682d-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="3682d-131">Velg dimensjonsmedlemmet som tilsvarer noden.</span><span class="sxs-lookup"><span data-stu-id="3682d-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="3682d-132">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3682d-132">Click Save.</span></span>
22. <span data-ttu-id="3682d-133">Velg 'Oganisasjon USP2\CEO\CEO-kostnadssentre' i treet.</span><span class="sxs-lookup"><span data-stu-id="3682d-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="3682d-134">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3682d-134">Click New.</span></span>
24. <span data-ttu-id="3682d-135">Skriv inn "Region Vest" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="3682d-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="3682d-136">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3682d-136">Click Save.</span></span>
26. <span data-ttu-id="3682d-137">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3682d-137">Click New.</span></span>
27. <span data-ttu-id="3682d-138">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3682d-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="3682d-139">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="3682d-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="3682d-140">Velg dimensjonsmedlemmet som tilsvarer noden.</span><span class="sxs-lookup"><span data-stu-id="3682d-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="3682d-141">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3682d-141">Click Save.</span></span>
30. <span data-ttu-id="3682d-142">Velg 'Oganisasjon USP2\CEO' i treet.</span><span class="sxs-lookup"><span data-stu-id="3682d-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="3682d-143">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3682d-143">Click New.</span></span>
32. <span data-ttu-id="3682d-144">Skriv inn "CFO-kostsentra" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="3682d-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="3682d-145">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3682d-145">Click Save.</span></span>
34. <span data-ttu-id="3682d-146">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3682d-146">Click New.</span></span>
35. <span data-ttu-id="3682d-147">Skriv inn "Markedsføringskampanje" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="3682d-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="3682d-148">Skriv inn "Markedsføringskampanje" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="3682d-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="3682d-149">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3682d-149">Click Save.</span></span>
38. <span data-ttu-id="3682d-150">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3682d-150">Click New.</span></span>
39. <span data-ttu-id="3682d-151">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3682d-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="3682d-152">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="3682d-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="3682d-153">Velg dimensjonsmedlemmet som tilsvarer noden.</span><span class="sxs-lookup"><span data-stu-id="3682d-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="3682d-154">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3682d-154">Click Save.</span></span>
42. <span data-ttu-id="3682d-155">Velg Oganisasjon USP2\CEO\CFO-kostnadssentre i treet.</span><span class="sxs-lookup"><span data-stu-id="3682d-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="3682d-156">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3682d-156">Click New.</span></span>
44. <span data-ttu-id="3682d-157">Skriv inn "Varemesser" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="3682d-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="3682d-158">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3682d-158">Click Save.</span></span>
46. <span data-ttu-id="3682d-159">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3682d-159">Click New.</span></span>
47. <span data-ttu-id="3682d-160">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3682d-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="3682d-161">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="3682d-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="3682d-162">Velg dimensjonsmedlemmet som tilsvarer noden.</span><span class="sxs-lookup"><span data-stu-id="3682d-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="3682d-163">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3682d-163">Click Save.</span></span>
50. <span data-ttu-id="3682d-164">Velg 'Oganisasjon USP2\CEO' i treet.</span><span class="sxs-lookup"><span data-stu-id="3682d-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="3682d-165">Skriv inn "CIO-kostsentra" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="3682d-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="3682d-166">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3682d-166">Click Save.</span></span>
53. <span data-ttu-id="3682d-167">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3682d-167">Click New.</span></span>
54. <span data-ttu-id="3682d-168">Skriv inn "Telefonsentre" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="3682d-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="3682d-169">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3682d-169">Click Save.</span></span>
56. <span data-ttu-id="3682d-170">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3682d-170">Click New.</span></span>
57. <span data-ttu-id="3682d-171">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3682d-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="3682d-172">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="3682d-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="3682d-173">Velg dimensjonsmedlemmet som tilsvarer noden.</span><span class="sxs-lookup"><span data-stu-id="3682d-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="3682d-174">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3682d-174">Click Save.</span></span>

