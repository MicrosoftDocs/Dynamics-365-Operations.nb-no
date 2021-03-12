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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51cd97ac2b78035224db543e3bcc5d606a16ffde
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969409"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="6f005-103">Opprette et hierarki for organisasjonsrapport</span><span class="sxs-lookup"><span data-stu-id="6f005-103">Create an organization report hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f005-104">Bruk denne fremgangsmåten til å opprette en rapport hierarki for rapportering av organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="6f005-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="6f005-105">Formålet med denne registreringen er å føre deg gjennom dimensjonshierarkiet slik at du kan fortsette til hele organisasjonen rapporteringsstrukturen er opprettet.</span><span class="sxs-lookup"><span data-stu-id="6f005-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="6f005-106">Denne registreringen bruker USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="6f005-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="6f005-107">Gå til Kostnadsregnskap > Dimensjoner > Dimensjonshierarkier.</span><span class="sxs-lookup"><span data-stu-id="6f005-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="6f005-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6f005-108">Click New.</span></span>
3. <span data-ttu-id="6f005-109">Velg "Dimensjonshierarki for klassifisering" i HierarchyTypeComboBox-feltet.</span><span class="sxs-lookup"><span data-stu-id="6f005-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="6f005-110">Velg Hierarki for dimensjonsklassifisering.</span><span class="sxs-lookup"><span data-stu-id="6f005-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="6f005-111">Hierarki for dimensjonklassifisering brukes til å definere regler og til rapporteringsformål.</span><span class="sxs-lookup"><span data-stu-id="6f005-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="6f005-112">Det støtter alle dimensjoner, for eksempel kostnadsobjekter, kostnadselementer og statistiske dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="6f005-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="6f005-113">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="6f005-113">Click Create.</span></span>
5. <span data-ttu-id="6f005-114">Skriv inn "Organisasjon USP2" i feltet Dimensjonshierarkinavn.</span><span class="sxs-lookup"><span data-stu-id="6f005-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="6f005-115">Angi eller velg en verdi i feltet Dimensjon.</span><span class="sxs-lookup"><span data-stu-id="6f005-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="6f005-116">Velg Kostsentra.</span><span class="sxs-lookup"><span data-stu-id="6f005-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="6f005-117">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6f005-117">Click Save.</span></span>
8. <span data-ttu-id="6f005-118">Klikk Vis hierarki.</span><span class="sxs-lookup"><span data-stu-id="6f005-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="6f005-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6f005-119">Click New.</span></span>
10. <span data-ttu-id="6f005-120">Skriv inn "CEO" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="6f005-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="6f005-121">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6f005-121">Click Save.</span></span>
12. <span data-ttu-id="6f005-122">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6f005-122">Click New.</span></span>
13. <span data-ttu-id="6f005-123">Skriv inn "CEO-kostsentra" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="6f005-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="6f005-124">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6f005-124">Click Save.</span></span>
15. <span data-ttu-id="6f005-125">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6f005-125">Click New.</span></span>
16. <span data-ttu-id="6f005-126">Skriv inn "Region Øst" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="6f005-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="6f005-127">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6f005-127">Click Save.</span></span>
18. <span data-ttu-id="6f005-128">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6f005-128">Click New.</span></span>
19. <span data-ttu-id="6f005-129">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6f005-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="6f005-130">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="6f005-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6f005-131">Velg dimensjonsmedlemmet som tilsvarer noden.</span><span class="sxs-lookup"><span data-stu-id="6f005-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="6f005-132">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6f005-132">Click Save.</span></span>
22. <span data-ttu-id="6f005-133">Velg 'Oganisasjon USP2\CEO\CEO-kostnadssentre' i treet.</span><span class="sxs-lookup"><span data-stu-id="6f005-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="6f005-134">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6f005-134">Click New.</span></span>
24. <span data-ttu-id="6f005-135">Skriv inn "Region Vest" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="6f005-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="6f005-136">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6f005-136">Click Save.</span></span>
26. <span data-ttu-id="6f005-137">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6f005-137">Click New.</span></span>
27. <span data-ttu-id="6f005-138">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6f005-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="6f005-139">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="6f005-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6f005-140">Velg dimensjonsmedlemmet som tilsvarer noden.</span><span class="sxs-lookup"><span data-stu-id="6f005-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="6f005-141">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6f005-141">Click Save.</span></span>
30. <span data-ttu-id="6f005-142">Velg 'Oganisasjon USP2\CEO' i treet.</span><span class="sxs-lookup"><span data-stu-id="6f005-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="6f005-143">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6f005-143">Click New.</span></span>
32. <span data-ttu-id="6f005-144">Skriv inn "CFO-kostsentra" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="6f005-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="6f005-145">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6f005-145">Click Save.</span></span>
34. <span data-ttu-id="6f005-146">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6f005-146">Click New.</span></span>
35. <span data-ttu-id="6f005-147">Skriv inn "Markedsføringskampanje" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="6f005-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="6f005-148">Skriv inn "Markedsføringskampanje" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="6f005-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="6f005-149">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6f005-149">Click Save.</span></span>
38. <span data-ttu-id="6f005-150">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6f005-150">Click New.</span></span>
39. <span data-ttu-id="6f005-151">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6f005-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="6f005-152">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="6f005-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6f005-153">Velg dimensjonsmedlemmet som tilsvarer noden.</span><span class="sxs-lookup"><span data-stu-id="6f005-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="6f005-154">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6f005-154">Click Save.</span></span>
42. <span data-ttu-id="6f005-155">Velg Oganisasjon USP2\CEO\CFO-kostnadssentre i treet.</span><span class="sxs-lookup"><span data-stu-id="6f005-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="6f005-156">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6f005-156">Click New.</span></span>
44. <span data-ttu-id="6f005-157">Skriv inn "Varemesser" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="6f005-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="6f005-158">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6f005-158">Click Save.</span></span>
46. <span data-ttu-id="6f005-159">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6f005-159">Click New.</span></span>
47. <span data-ttu-id="6f005-160">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6f005-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="6f005-161">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="6f005-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6f005-162">Velg dimensjonsmedlemmet som tilsvarer noden.</span><span class="sxs-lookup"><span data-stu-id="6f005-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="6f005-163">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6f005-163">Click Save.</span></span>
50. <span data-ttu-id="6f005-164">Velg 'Oganisasjon USP2\CEO' i treet.</span><span class="sxs-lookup"><span data-stu-id="6f005-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="6f005-165">Skriv inn "CIO-kostsentra" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="6f005-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="6f005-166">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6f005-166">Click Save.</span></span>
53. <span data-ttu-id="6f005-167">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6f005-167">Click New.</span></span>
54. <span data-ttu-id="6f005-168">Skriv inn "Telefonsentre" i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="6f005-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="6f005-169">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6f005-169">Click Save.</span></span>
56. <span data-ttu-id="6f005-170">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6f005-170">Click New.</span></span>
57. <span data-ttu-id="6f005-171">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6f005-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="6f005-172">Angi eller velg en verdi i feltet Fra dimensjonsmedlem.</span><span class="sxs-lookup"><span data-stu-id="6f005-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6f005-173">Velg dimensjonsmedlemmet som tilsvarer noden.</span><span class="sxs-lookup"><span data-stu-id="6f005-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="6f005-174">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6f005-174">Click Save.</span></span>

