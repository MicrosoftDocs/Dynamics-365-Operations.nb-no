---
title: Definere overvåkingspolicyer for kildedokumenter
description: Denne fremgangsmåten viser hvordan du angir og kjører overvåkingspolicyregler.
author: ryansandness
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a82c3e8e8787beb309b75b73cda36f4ca8031d6f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558889"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="2952a-103">Definere overvåkingspolicyer for kildedokumenter</span><span class="sxs-lookup"><span data-stu-id="2952a-103">Define audit policies for source documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2952a-104">Denne fremgangsmåten viser hvordan du angir og kjører overvåkingspolicyregler.</span><span class="sxs-lookup"><span data-stu-id="2952a-104">This procedure shows how to set up and run audit policy rules.</span></span> <span data-ttu-id="2952a-105">Eksemplet bruker reiseregninger med utgiftstypen hotell.</span><span class="sxs-lookup"><span data-stu-id="2952a-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="2952a-106">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="2952a-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="2952a-107">Revisorrollen inneholder de riktige tillatelsene for å kunne utføre disse oppgavene.</span><span class="sxs-lookup"><span data-stu-id="2952a-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="2952a-108">Gå til Arbeidsområde for overvåking > Oppsett > Type policyregel.</span><span class="sxs-lookup"><span data-stu-id="2952a-108">Go to Audit workbench > Setup > Policy rule type.</span></span>
2. <span data-ttu-id="2952a-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2952a-109">Click New.</span></span>
3. <span data-ttu-id="2952a-110">Skriv inn en verdi i feltet Regelnavn.</span><span class="sxs-lookup"><span data-stu-id="2952a-110">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="2952a-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="2952a-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2952a-112">I Spørringsnavn-feltet velger du Utgiftsrapportlinje</span><span class="sxs-lookup"><span data-stu-id="2952a-112">In the Query name field, select Expense report line</span></span>
6. <span data-ttu-id="2952a-113">I Spørringstype-feltet velger du Mengde</span><span class="sxs-lookup"><span data-stu-id="2952a-113">In the query type field, select Aggregate</span></span>
7. <span data-ttu-id="2952a-114">Velg Juridisk enhet i Juridisk enhet-feltet.</span><span class="sxs-lookup"><span data-stu-id="2952a-114">In the Legal entity field, select Legal entity</span></span>
8. <span data-ttu-id="2952a-115">I feltet Referanse til dokumentdato velger du Endringsdato og -klokkeslett</span><span class="sxs-lookup"><span data-stu-id="2952a-115">In the Document date reference field, select Modified date and time</span></span>
9. <span data-ttu-id="2952a-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="2952a-116">Click Save.</span></span>
10. <span data-ttu-id="2952a-117">Gå til Arbeidsområde for overvåking > Oppsett > Overvåkingspolicyer.</span><span class="sxs-lookup"><span data-stu-id="2952a-117">Go to Audit workbench > Setup > Audit policies.</span></span>
11. <span data-ttu-id="2952a-118">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2952a-118">Click New.</span></span>
12. <span data-ttu-id="2952a-119">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="2952a-119">In the Name field, type a value.</span></span>
13. <span data-ttu-id="2952a-120">Utvid delen Policyorganisasjoner.</span><span class="sxs-lookup"><span data-stu-id="2952a-120">Expand the Policy organizations section.</span></span>
14. <span data-ttu-id="2952a-121">Velg "Contoso Entertainment System USA" i treet.</span><span class="sxs-lookup"><span data-stu-id="2952a-121">In the tree, select 'Contoso Entertainment System USA'.</span></span>
15. <span data-ttu-id="2952a-122">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="2952a-122">Click Add.</span></span>
16. <span data-ttu-id="2952a-123">Velg "Contoso Consulting USA" i treet.</span><span class="sxs-lookup"><span data-stu-id="2952a-123">In the tree, select 'Contoso Consulting USA'.</span></span>
17. <span data-ttu-id="2952a-124">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="2952a-124">Click Add.</span></span>
18. <span data-ttu-id="2952a-125">Velg "Contoso Retail USA" i treet.</span><span class="sxs-lookup"><span data-stu-id="2952a-125">In the tree, select 'Contoso Retail USA'.</span></span>
19. <span data-ttu-id="2952a-126">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="2952a-126">Click Add.</span></span>
20. <span data-ttu-id="2952a-127">Skjul delen Policyorganisasjoner.</span><span class="sxs-lookup"><span data-stu-id="2952a-127">Collapse the Policy organizations section.</span></span>
21. <span data-ttu-id="2952a-128">Utvid delen Policyregler.</span><span class="sxs-lookup"><span data-stu-id="2952a-128">Expand the Policy rules section.</span></span>
22. <span data-ttu-id="2952a-129">I listen finner og velger du policyregelen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="2952a-129">In the list, find and select the Policy Rule that was created previously.</span></span>
23. <span data-ttu-id="2952a-130">Klikk Opprett policyregel.</span><span class="sxs-lookup"><span data-stu-id="2952a-130">Click Create policy rule.</span></span>
24. <span data-ttu-id="2952a-131">Angi dato og klokkeslett i feltet Gyldighetsdato.</span><span class="sxs-lookup"><span data-stu-id="2952a-131">In the Effective date field, enter a date and time.</span></span>
25. <span data-ttu-id="2952a-132">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="2952a-132">Click Filter.</span></span>
26. <span data-ttu-id="2952a-133">Velg raden for Utgiftskategori i listen, og angi detaljene til Hotell</span><span class="sxs-lookup"><span data-stu-id="2952a-133">In the list, select the row for Expense category, and set the details to Hotel</span></span>
27. <span data-ttu-id="2952a-134">Angi eller velg en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="2952a-134">In the Criteria field, enter or select a value.</span></span>
28. <span data-ttu-id="2952a-135">Klikk kategorien Mengde.</span><span class="sxs-lookup"><span data-stu-id="2952a-135">Click the Aggregate tab.</span></span>
29. <span data-ttu-id="2952a-136">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="2952a-136">Click Add.</span></span>
30. <span data-ttu-id="2952a-137">I listen velger du en feltverdi av transaksjonsbeløpet</span><span class="sxs-lookup"><span data-stu-id="2952a-137">In the list, select a field value of Transaction amount</span></span>
31. <span data-ttu-id="2952a-138">Angi eller velg en verdi i Felt-feltet.</span><span class="sxs-lookup"><span data-stu-id="2952a-138">In the Field field, enter or select a value.</span></span>
32. <span data-ttu-id="2952a-139">Velg Summer i AggregateFunction-feltet.</span><span class="sxs-lookup"><span data-stu-id="2952a-139">In the AggregateFunction field, select 'Sum'.</span></span>
33. <span data-ttu-id="2952a-140">Klikk kategorien Grupper etter.</span><span class="sxs-lookup"><span data-stu-id="2952a-140">Click the Group by tab.</span></span>
34. <span data-ttu-id="2952a-141">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="2952a-141">Click Add.</span></span>
35. <span data-ttu-id="2952a-142">Velg en verdi for Ansatt i listen.</span><span class="sxs-lookup"><span data-stu-id="2952a-142">In the list, select a value of Employee</span></span> 
36. <span data-ttu-id="2952a-143">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="2952a-143">Click Add.</span></span>
37. <span data-ttu-id="2952a-144">Velg en verdi for Utgiftskategori i listen.</span><span class="sxs-lookup"><span data-stu-id="2952a-144">In the list, select a value of Expense category</span></span>
38. <span data-ttu-id="2952a-145">Angi eller velg en verdi i Felt-feltet.</span><span class="sxs-lookup"><span data-stu-id="2952a-145">In the Field field, enter or select a value.</span></span>
39. <span data-ttu-id="2952a-146">Klikk kategorien Har.</span><span class="sxs-lookup"><span data-stu-id="2952a-146">Click the Having tab.</span></span>
40. <span data-ttu-id="2952a-147">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="2952a-147">Click Add.</span></span>
41. <span data-ttu-id="2952a-148">Velg Transaksjonsbeløp</span><span class="sxs-lookup"><span data-stu-id="2952a-148">Select Transaction amount</span></span>
42. <span data-ttu-id="2952a-149">Angi eller velg en verdi i Felt-feltet.</span><span class="sxs-lookup"><span data-stu-id="2952a-149">In the Field field, enter or select a value.</span></span>
43. <span data-ttu-id="2952a-150">Velg Summer i AggregateFunction-feltet.</span><span class="sxs-lookup"><span data-stu-id="2952a-150">In the AggregateFunction field, select 'Sum'.</span></span>
44. <span data-ttu-id="2952a-151">Skriv inn >2000 i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="2952a-151">In the Criteria field, type '>2000'.</span></span>
45. <span data-ttu-id="2952a-152">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2952a-152">Click OK.</span></span>
46. <span data-ttu-id="2952a-153">Klikk Test.</span><span class="sxs-lookup"><span data-stu-id="2952a-153">Click Test.</span></span>
47. <span data-ttu-id="2952a-154">Angi dato og klokkeslett i feltet Startdato for dokumentutvalg.</span><span class="sxs-lookup"><span data-stu-id="2952a-154">In the Document selection starting date field, enter a date and time.</span></span>
48. <span data-ttu-id="2952a-155">Angi dato og klokkeslett i feltet Sluttdato for dokumentutvalg.</span><span class="sxs-lookup"><span data-stu-id="2952a-155">In the Document selection ending date field, enter a date and time.</span></span>
49. <span data-ttu-id="2952a-156">Klikk Kjør test.</span><span class="sxs-lookup"><span data-stu-id="2952a-156">Click Run test.</span></span>
50. <span data-ttu-id="2952a-157">Klikk Overvåkingspolicy i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2952a-157">On the Action Pane, click Audit policy.</span></span>
51. <span data-ttu-id="2952a-158">Klikk Tilleggsalternativer.</span><span class="sxs-lookup"><span data-stu-id="2952a-158">Click Additional options.</span></span>
52. <span data-ttu-id="2952a-159">Angi dato og klokkeslett i Startdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="2952a-159">In the Starting date field, enter a date and time.</span></span>
53. <span data-ttu-id="2952a-160">Angi dato og klokkeslett i Sluttdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="2952a-160">In the Ending date field, enter a date and time.</span></span>
54. <span data-ttu-id="2952a-161">Klikk Parti.</span><span class="sxs-lookup"><span data-stu-id="2952a-161">Click Batch.</span></span>
55. <span data-ttu-id="2952a-162">Utvid Kjør i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="2952a-162">Expand the Run in the background section.</span></span>
56. <span data-ttu-id="2952a-163">Velg Ja i feltet Satsvis behandling.</span><span class="sxs-lookup"><span data-stu-id="2952a-163">Select Yes in the Batch processing field.</span></span>
57. <span data-ttu-id="2952a-164">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2952a-164">Click OK.</span></span>
58. <span data-ttu-id="2952a-165">Gå til Arbeidsområde for overvåking > Overvåkingssaker.</span><span class="sxs-lookup"><span data-stu-id="2952a-165">Go to Audit workbench > Audit cases.</span></span>
59. <span data-ttu-id="2952a-166">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="2952a-166">In the list, find and select the desired record.</span></span>
60. <span data-ttu-id="2952a-167">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2952a-167">In the list, click the link in the selected row.</span></span>
61. <span data-ttu-id="2952a-168">Vis delen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="2952a-168">Expand the Associations section.</span></span>
62. <span data-ttu-id="2952a-169">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="2952a-169">In the list, find and select the desired record.</span></span>
63. <span data-ttu-id="2952a-170">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2952a-170">In the list, click the link in the selected row.</span></span>

