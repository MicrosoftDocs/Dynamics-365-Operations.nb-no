---
title: Definere overvåkingspolicyer for kildedokumenter
description: Dette emnet forklarer hvordan du angir og kjører overvåkingspolicyregler.
author: ryansandness
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6b0fa28d778a4d9fa1f718b1d50bf1dce00be00
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186124"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="6772d-103">Definere overvåkingspolicyer for kildedokumenter</span><span class="sxs-lookup"><span data-stu-id="6772d-103">Define audit policies for source documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6772d-104">Dette emnet forklarer hvordan du angir og kjører overvåkingspolicyregler.</span><span class="sxs-lookup"><span data-stu-id="6772d-104">This topic explains how to set up and run audit policy rules.</span></span> <span data-ttu-id="6772d-105">Eksemplet bruker reiseregninger med utgiftstypen hotell.</span><span class="sxs-lookup"><span data-stu-id="6772d-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="6772d-106">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="6772d-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="6772d-107">Revisorrollen inneholder de riktige tillatelsene for å kunne utføre disse oppgavene.</span><span class="sxs-lookup"><span data-stu-id="6772d-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="6772d-108">I navigasjonsruten går du til **Moduler > Arbeidsområde for overvåking > Oppsett > Type policyregel**.</span><span class="sxs-lookup"><span data-stu-id="6772d-108">In the navigation pane, go to **Modules > Audit workbench > Setup > Policy rule type**.</span></span>
2. <span data-ttu-id="6772d-109">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6772d-109">Select **New**.</span></span>
3. <span data-ttu-id="6772d-110">Skriv inn en verdi i feltet **Regelnavn**.</span><span class="sxs-lookup"><span data-stu-id="6772d-110">In the **Rule name** field, type a value.</span></span>
4. <span data-ttu-id="6772d-111">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6772d-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="6772d-112">I **Spørringsnavn**-feltet velger du **Utgiftsrapportlinje**</span><span class="sxs-lookup"><span data-stu-id="6772d-112">In the **Query name** field, select **Expense report line**</span></span>
6. <span data-ttu-id="6772d-113">I **Spørringstype**-feltet velger du **Mengde**</span><span class="sxs-lookup"><span data-stu-id="6772d-113">In the **query type** field, select **Aggregate**</span></span>
7. <span data-ttu-id="6772d-114">Velg **Juridisk enhet** i **Juridisk enhet**-feltet</span><span class="sxs-lookup"><span data-stu-id="6772d-114">In the **Legal entity** field, select **Legal entity**</span></span>
8. <span data-ttu-id="6772d-115">I feltet **Referanse til dokumentdato** velger du **Endringsdato og -klokkeslett**</span><span class="sxs-lookup"><span data-stu-id="6772d-115">In the **Document date reference** field, select **Modified date and time**</span></span>
9. <span data-ttu-id="6772d-116">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6772d-116">Select **Save**.</span></span>
10. <span data-ttu-id="6772d-117">I navigasjonsruten går du til **Moduler > Arbeidsområde for overvåking > Oppsett > Overvåkingspolicyer**.</span><span class="sxs-lookup"><span data-stu-id="6772d-117">In the navigation pane, go to **Modules > Audit workbench > Setup > Audit policies**.</span></span>
11. <span data-ttu-id="6772d-118">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6772d-118">Select **New**.</span></span>
12. <span data-ttu-id="6772d-119">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6772d-119">In the **Name** field, type a value.</span></span>
13. <span data-ttu-id="6772d-120">Utvid delen **Policyorganisasjoner**.</span><span class="sxs-lookup"><span data-stu-id="6772d-120">Expand the **Policy organizations** section.</span></span>
14. <span data-ttu-id="6772d-121">Velg **Contoso Entertainment System USA** i treet, og velg deretter **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="6772d-121">In the tree, select **Contoso Entertainment System USA**, then select **Add**.</span></span>
15. <span data-ttu-id="6772d-122">Velg **Contoso Consulting USA** i treet, og velg deretter **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="6772d-122">In the tree, select **Contoso Consulting USA**, then select **Add**.</span></span>
16. <span data-ttu-id="6772d-123">Velg **Contoso Retail USA** i treet, og velg deretter **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="6772d-123">In the tree, select **Contoso Retail USA**, then select **Add**.</span></span>
17. <span data-ttu-id="6772d-124">Skjul delen **Policyorganisasjoner**.</span><span class="sxs-lookup"><span data-stu-id="6772d-124">Collapse the **Policy organizations** section.</span></span>
18. <span data-ttu-id="6772d-125">Utvid delen **Policyregler**.</span><span class="sxs-lookup"><span data-stu-id="6772d-125">Expand the **Policy rules** section.</span></span>
19. <span data-ttu-id="6772d-126">I listen finner og velger du policyregelen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="6772d-126">In the list, find and select the Policy Rule that was created previously.</span></span>
20. <span data-ttu-id="6772d-127">Velg **Opprett policyregel**.</span><span class="sxs-lookup"><span data-stu-id="6772d-127">Select **Create policy rule**.</span></span>
21. <span data-ttu-id="6772d-128">Angi dato og klokkeslett i feltet **Gyldighetsdato**.</span><span class="sxs-lookup"><span data-stu-id="6772d-128">In the **Effective date** field, enter a date and time.</span></span>
22. <span data-ttu-id="6772d-129">Velg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="6772d-129">Select **Filter**.</span></span>
23. <span data-ttu-id="6772d-130">Velg raden for **Utgiftskategori** i listen, og angi detaljene til **Hotell**.</span><span class="sxs-lookup"><span data-stu-id="6772d-130">In the list, select the row for **Expense category**, and set the details to **Hotel**.</span></span>
24. <span data-ttu-id="6772d-131">Angi eller velg en verdi i **Kriterier**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6772d-131">In the **Criteria** field, enter or select a value.</span></span>
25. <span data-ttu-id="6772d-132">Velg fanen **Mengde**.</span><span class="sxs-lookup"><span data-stu-id="6772d-132">Select the **Aggregate** tab.</span></span>
26. <span data-ttu-id="6772d-133">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="6772d-133">Select **Add**.</span></span>
27. <span data-ttu-id="6772d-134">I listen velger du en feltverdi av **transaksjonsbeløpet**.</span><span class="sxs-lookup"><span data-stu-id="6772d-134">In the list, select a field value of **Transaction amount**.</span></span>
28. <span data-ttu-id="6772d-135">Angi eller velg en verdi i **Felt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6772d-135">In the **Field** field, enter or select a value.</span></span>
29. <span data-ttu-id="6772d-136">Velg **Summer** i **AggregateFunction**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6772d-136">In the **AggregateFunction** field, select **Sum**.</span></span>
30. <span data-ttu-id="6772d-137">Velg **Grupper etter**-fanen.</span><span class="sxs-lookup"><span data-stu-id="6772d-137">Select the **Group by** tab.</span></span>
31. <span data-ttu-id="6772d-138">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="6772d-138">Select **Add**.</span></span>
32. <span data-ttu-id="6772d-139">Velg en verdi for **Ansatt** i listen.</span><span class="sxs-lookup"><span data-stu-id="6772d-139">In the list, select a value of **Employee** .</span></span>
33. <span data-ttu-id="6772d-140">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="6772d-140">Select **Add**.</span></span>
34. <span data-ttu-id="6772d-141">Velg en verdi for **Utgiftskategori** i listen.</span><span class="sxs-lookup"><span data-stu-id="6772d-141">In the list, select a value of **Expense category**.</span></span>
35. <span data-ttu-id="6772d-142">Angi eller velg en verdi i **Felt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6772d-142">In the **Field** field, enter or select a value.</span></span>
36. <span data-ttu-id="6772d-143">Velg kategorien **Har**.</span><span class="sxs-lookup"><span data-stu-id="6772d-143">Select the **Having** tab.</span></span>
37. <span data-ttu-id="6772d-144">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="6772d-144">Select **Add**.</span></span>
38. <span data-ttu-id="6772d-145">Velg **Transaksjonsbeløp**.</span><span class="sxs-lookup"><span data-stu-id="6772d-145">Select **Transaction amount**.</span></span>
39. <span data-ttu-id="6772d-146">Angi eller velg en verdi i **Felt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6772d-146">In the **Field** field, enter or select a value.</span></span>
40. <span data-ttu-id="6772d-147">Velg **Summer** i **AggregateFunction**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6772d-147">In the **AggregateFunction** field, select **Sum**.</span></span>
41. <span data-ttu-id="6772d-148">I **Kriterier**-feltet angir du `>2000`.</span><span class="sxs-lookup"><span data-stu-id="6772d-148">In the **Criteria** field, type `>2000`.</span></span>
42. <span data-ttu-id="6772d-149">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6772d-149">Select **OK**.</span></span>
43. <span data-ttu-id="6772d-150">Velg **Test**.</span><span class="sxs-lookup"><span data-stu-id="6772d-150">Select **Test**.</span></span>
44. <span data-ttu-id="6772d-151">Angi dato og klokkeslett i feltet **Startdato for dokumentutvalg**.</span><span class="sxs-lookup"><span data-stu-id="6772d-151">In the **Document selection starting date** field, enter a date and time.</span></span>
45. <span data-ttu-id="6772d-152">Angi dato og klokkeslett i feltet **Sluttdato for dokumentutvalg**.</span><span class="sxs-lookup"><span data-stu-id="6772d-152">In the **Document selection ending date** field, enter a date and time.</span></span>
46. <span data-ttu-id="6772d-153">Velg **Kjør test**.</span><span class="sxs-lookup"><span data-stu-id="6772d-153">Select **Run test**.</span></span>
47. <span data-ttu-id="6772d-154">Klikk **Overvåkingspolicy** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6772d-154">On the Action Pane, select **Audit policy**.</span></span>
48. <span data-ttu-id="6772d-155">Velg **Tilleggsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="6772d-155">Select **Additional options**.</span></span>
49. <span data-ttu-id="6772d-156">Angi dato og klokkeslett i **Startdato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6772d-156">In the **Starting date** field, enter a date and time.</span></span>
50. <span data-ttu-id="6772d-157">Angi dato og klokkeslett i **Sluttdato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6772d-157">In the **Ending date** field, enter a date and time.</span></span>
51. <span data-ttu-id="6772d-158">Velg **Parti**.</span><span class="sxs-lookup"><span data-stu-id="6772d-158">Select **Batch**.</span></span>
52. <span data-ttu-id="6772d-159">Vis delen **Kjør i bakgrunnen**.</span><span class="sxs-lookup"><span data-stu-id="6772d-159">Expand the **Run in the background** section.</span></span>
53. <span data-ttu-id="6772d-160">Velg **Ja** i feltet **Satsvis behandling**.</span><span class="sxs-lookup"><span data-stu-id="6772d-160">Select **Yes** in the **Batch processing** field.</span></span>
54. <span data-ttu-id="6772d-161">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6772d-161">Select **OK**.</span></span>
55. <span data-ttu-id="6772d-162">I navigasjonsruten går du til **Moduler > Arbeidsområde for overvåking > Overvåkingssaker**.</span><span class="sxs-lookup"><span data-stu-id="6772d-162">In the navigation pane, go to **Modules > Audit workbench > Audit cases**.</span></span>
56. <span data-ttu-id="6772d-163">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="6772d-163">In the list, find and select the desired record.</span></span>
57. <span data-ttu-id="6772d-164">Vis delen **Tilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="6772d-164">Expand the **Associations** section.</span></span>
58. <span data-ttu-id="6772d-165">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="6772d-165">In the list, find and select the desired record.</span></span>

