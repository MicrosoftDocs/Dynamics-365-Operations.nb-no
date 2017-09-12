--- 
title: Opprette et hierarki for organisasjonsrapport
description: "Bruk denne fremgangsmåten til å opprette en rapport hierarki for rapportering av organisasjonen."
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f593c59660abcf5b0d5771ddd9daced6ec5fbfb4
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="5bae7-103">Opprette et hierarki for organisasjonsrapport</span><span class="sxs-lookup"><span data-stu-id="5bae7-103">Create an organization report hierarchy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5bae7-104">Bruk denne fremgangsmåten til å opprette en rapport hierarki for rapportering av organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="5bae7-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="5bae7-105">Formålet med denne registreringen er å føre deg gjennom dimensjonshierarkiet slik at du kan fortsette til hele organisasjonen rapporteringsstrukturen er opprettet.</span><span class="sxs-lookup"><span data-stu-id="5bae7-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="5bae7-106">Denne registreringen bruker USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="5bae7-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="5bae7-107">Gå til Kostnadsregnskap > Dimensjoner > Dimensjonshierarkier.</span><span class="sxs-lookup"><span data-stu-id="5bae7-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="5bae7-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5bae7-108">Click New.</span></span>
3. <span data-ttu-id="5bae7-109">Velg "Dimensjonshierarki for klassifisering" i HierarchyTypeComboBox-feltet.</span><span class="sxs-lookup"><span data-stu-id="5bae7-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="5bae7-110">Velg Hierarki for dimensjonsklassifisering.</span><span class="sxs-lookup"><span data-stu-id="5bae7-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="5bae7-111">Hierarki for dimensjonklassifisering brukes til å definere regler og til rapporteringsformål.</span><span class="sxs-lookup"><span data-stu-id="5bae7-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="5bae7-112">Det støtter alle dimensjoner, for eksempel kostnadsobjekter, kostnadselementer og statistiske dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="5bae7-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="5bae7-113">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="5bae7-113">Click Create.</span></span>
5. <span data-ttu-id="5bae7-114">Skriv inn "Organisasjon USP2" i feltet Dimensjonshierarkinavn.</span><span class="sxs-lookup"><span data-stu-id="5bae7-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="5bae7-115">Angi eller velg en verdi i feltet Dimensjon.</span><span class="sxs-lookup"><span data-stu-id="5bae7-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="5bae7-116">Velg Kostsentra.</span><span class="sxs-lookup"><span data-stu-id="5bae7-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="5bae7-117">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5bae7-117">Click Save.</span></span>
8. <span data-ttu-id="5bae7-118">Klikk Vis hierarki.</span><span class="sxs-lookup"><span data-stu-id="5bae7-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="5bae7-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5bae7-119">Click New.</span></span>
10. <span data-ttu-id="5bae7-120">Skriv inn "CEO" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="5bae7-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="5bae7-121">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5bae7-121">Click Save.</span></span>
12. <span data-ttu-id="5bae7-122">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5bae7-122">Click New.</span></span>
13. <span data-ttu-id="5bae7-123">Skriv inn "CEO-kostsentra" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="5bae7-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="5bae7-124">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5bae7-124">Click Save.</span></span>
15. <span data-ttu-id="5bae7-125">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5bae7-125">Click New.</span></span>
16. <span data-ttu-id="5bae7-126">Skriv inn "Region Øst" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="5bae7-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="5bae7-127">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5bae7-127">Click Save.</span></span>
18. <span data-ttu-id="5bae7-128">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5bae7-128">Click New.</span></span>
19. <span data-ttu-id="5bae7-129">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5bae7-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="5bae7-130">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="5bae7-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="5bae7-131">Velg dimensjonsmedlemmet som tilsvarer noden.</span><span class="sxs-lookup"><span data-stu-id="5bae7-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="5bae7-132">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5bae7-132">Click Save.</span></span>
22. <span data-ttu-id="5bae7-133">Velg 'Oganisasjon USP2\CEO\CEO-kostnadssentre' i treet.</span><span class="sxs-lookup"><span data-stu-id="5bae7-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="5bae7-134">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5bae7-134">Click New.</span></span>
24. <span data-ttu-id="5bae7-135">Skriv inn "Region Vest" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="5bae7-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="5bae7-136">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5bae7-136">Click Save.</span></span>
26. <span data-ttu-id="5bae7-137">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5bae7-137">Click New.</span></span>
27. <span data-ttu-id="5bae7-138">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5bae7-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="5bae7-139">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="5bae7-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="5bae7-140">Velg dimensjonsmedlemmet som tilsvarer noden.</span><span class="sxs-lookup"><span data-stu-id="5bae7-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="5bae7-141">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5bae7-141">Click Save.</span></span>
30. <span data-ttu-id="5bae7-142">Velg 'Oganisasjon USP2\CEO' i treet.</span><span class="sxs-lookup"><span data-stu-id="5bae7-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="5bae7-143">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5bae7-143">Click New.</span></span>
32. <span data-ttu-id="5bae7-144">Skriv inn "CFO-kostsentra" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="5bae7-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="5bae7-145">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5bae7-145">Click Save.</span></span>
34. <span data-ttu-id="5bae7-146">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5bae7-146">Click New.</span></span>
35. <span data-ttu-id="5bae7-147">Skriv inn "Markedsføringskampanje" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="5bae7-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="5bae7-148">Skriv inn "Markedsføringskampanje" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="5bae7-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="5bae7-149">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5bae7-149">Click Save.</span></span>
38. <span data-ttu-id="5bae7-150">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5bae7-150">Click New.</span></span>
39. <span data-ttu-id="5bae7-151">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5bae7-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="5bae7-152">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="5bae7-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="5bae7-153">Velg dimensjonsmedlemmet som tilsvarer noden.</span><span class="sxs-lookup"><span data-stu-id="5bae7-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="5bae7-154">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5bae7-154">Click Save.</span></span>
42. <span data-ttu-id="5bae7-155">Velg 'Oganisasjon USP2\CEO\CFO-kostnadssentre' i treet.</span><span class="sxs-lookup"><span data-stu-id="5bae7-155">In the tree, select 'Oganization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="5bae7-156">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5bae7-156">Click New.</span></span>
44. <span data-ttu-id="5bae7-157">Skriv inn "Varemesser" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="5bae7-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="5bae7-158">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5bae7-158">Click Save.</span></span>
46. <span data-ttu-id="5bae7-159">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5bae7-159">Click New.</span></span>
47. <span data-ttu-id="5bae7-160">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5bae7-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="5bae7-161">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="5bae7-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="5bae7-162">Velg dimensjonsmedlemmet som tilsvarer noden.</span><span class="sxs-lookup"><span data-stu-id="5bae7-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="5bae7-163">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5bae7-163">Click Save.</span></span>
50. <span data-ttu-id="5bae7-164">Velg 'Oganisasjon USP2\CEO' i treet.</span><span class="sxs-lookup"><span data-stu-id="5bae7-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="5bae7-165">Skriv inn "CIO-kostsentra" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="5bae7-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="5bae7-166">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5bae7-166">Click Save.</span></span>
53. <span data-ttu-id="5bae7-167">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5bae7-167">Click New.</span></span>
54. <span data-ttu-id="5bae7-168">Skriv inn "Telefonsentre" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="5bae7-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="5bae7-169">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5bae7-169">Click Save.</span></span>
56. <span data-ttu-id="5bae7-170">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5bae7-170">Click New.</span></span>
57. <span data-ttu-id="5bae7-171">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5bae7-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="5bae7-172">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="5bae7-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="5bae7-173">Velg dimensjonsmedlemmet som tilsvarer noden.</span><span class="sxs-lookup"><span data-stu-id="5bae7-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="5bae7-174">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5bae7-174">Click Save.</span></span>


