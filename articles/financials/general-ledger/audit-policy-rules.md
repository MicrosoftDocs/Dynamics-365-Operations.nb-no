---
title: "Overvåkingspolicyregler"
description: "Du kan bruke overvåkingspolicyer for å evaluere reiseregninger, leverandørfakturaer og bestillinger for å være sikker på at de samsvarer med policyregler du oppretter. Alle reglene som er knyttet til en overvåkingspolicy, kjøres i satsvis modus i henhold til en tidsplan du angir.  Hver policyregel er en forekomst av en policyregeltype. For hver policyregeltype kan bare én policyregel være aktiv om gangen."
author: ryansandness
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 273beb0acef51059b40f9842062ed4dbba770160
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="audit-policy-rules"></a><span data-ttu-id="b9564-106">Overvåkingspolicyregler</span><span class="sxs-lookup"><span data-stu-id="b9564-106">Audit policy rules</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="b9564-107">Du kan bruke overvåkingspolicyer for å evaluere reiseregninger, leverandørfakturaer og bestillinger for å være sikker på at de samsvarer med policyregler du oppretter.</span><span class="sxs-lookup"><span data-stu-id="b9564-107">You can use audit policies to evaluate expense reports, vendor invoices, and purchase orders to make sure that they comply with policy rules that you create.</span></span> <span data-ttu-id="b9564-108">Alle reglene som er knyttet til en overvåkingspolicy, kjøres i satsvis modus i henhold til en tidsplan du angir.</span><span class="sxs-lookup"><span data-stu-id="b9564-108">All of the rules that are associated with an audit policy are run in batch mode, according to a schedule that you specify.</span></span>  <span data-ttu-id="b9564-109">Hver policyregel er en forekomst av en policyregeltype.</span><span class="sxs-lookup"><span data-stu-id="b9564-109">Each policy rule is an instance of a policy rule type.</span></span> <span data-ttu-id="b9564-110">For hver policyregeltype kan bare én policyregel være aktiv om gangen.</span><span class="sxs-lookup"><span data-stu-id="b9564-110">For each policy rule type, only one policy rule can be active at a time.</span></span> 

<a name="queries-and-query-types"></a><span data-ttu-id="b9564-111">Spørringer og spørringstyper</span><span class="sxs-lookup"><span data-stu-id="b9564-111">Queries and query types</span></span>
-----------------------

<span data-ttu-id="b9564-112">Når du oppretter en overvåkingspolicyregel, velger du først en policyregeltype.</span><span class="sxs-lookup"><span data-stu-id="b9564-112">When you create an audit policy rule, you first select a policy rule type.</span></span> <span data-ttu-id="b9564-113">Policyregeltypen angir applikasjonsobjekttre (AOT)-spørringen som skal brukes som utgangpunkt for å opprette policyregelen.</span><span class="sxs-lookup"><span data-stu-id="b9564-113">The policy rule type specifies the Application Object Tree (AOT) query to use as the starting point for creating the policy rule.</span></span> <span data-ttu-id="b9564-114">Det angir også hvilken spørringstype som skal brukes for policyregelen.</span><span class="sxs-lookup"><span data-stu-id="b9564-114">It also specifies the query type to use for the policy rule.</span></span> <span data-ttu-id="b9564-115">Spørringen bestemmer kildedokumentet som policyregelen evaluerer.</span><span class="sxs-lookup"><span data-stu-id="b9564-115">The query determines the source document that the policy rule evaluates.</span></span> <span data-ttu-id="b9564-116">Det angir også feltene du velger i kildedokumentet, som identifiserer den juridiske enheten og datoen som skal brukes når dokumenter velges for overvåking.</span><span class="sxs-lookup"><span data-stu-id="b9564-116">It also specifies the fields in the source document that identify both the legal entity and the date to use when documents are selected for audit.</span></span> <span data-ttu-id="b9564-117">Spørringstypen styrer standardfeltene på spørringssiden og siden Overvåkingspolicyregel.</span><span class="sxs-lookup"><span data-stu-id="b9564-117">The query type controls the default fields in the query page and in the Audit policy rule page.</span></span> <span data-ttu-id="b9564-118">Tabellen nedenfor viser de spørringstypene som er tilgjengelige for overvåkingspolicyregler.</span><span class="sxs-lookup"><span data-stu-id="b9564-118">The following table shows the query types that are available for audit policy rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9564-119">Spørringstype</span><span class="sxs-lookup"><span data-stu-id="b9564-119">Query type</span></span></th>
<th><span data-ttu-id="b9564-120">Formål</span><span class="sxs-lookup"><span data-stu-id="b9564-120">Purpose</span></span></th>
<th><span data-ttu-id="b9564-121">Mer informasjon</span><span class="sxs-lookup"><span data-stu-id="b9564-121">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b9564-122">Betinget</span><span class="sxs-lookup"><span data-stu-id="b9564-122">Conditional</span></span></td>
<td><span data-ttu-id="b9564-123">Evaluere kildedokumentattributter mot angitte verdier.</span><span class="sxs-lookup"><span data-stu-id="b9564-123">Evaluate source document attributes against specified values.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b9564-124">Aggreger</span><span class="sxs-lookup"><span data-stu-id="b9564-124">Aggregate</span></span></td>
<td><span data-ttu-id="b9564-125">Evaluere flere kildedokumenter eller kildedokumentlinjer mot en policyregel ved å aggregere numeriske verdier.</span><span class="sxs-lookup"><span data-stu-id="b9564-125">Evaluate multiple source documents or source document lines against a policy rule by aggregating numeric values.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b9564-126">Prøve</span><span class="sxs-lookup"><span data-stu-id="b9564-126">Sampling</span></span></td>
<td><span data-ttu-id="b9564-127">Velg tilfeldig en angitt prosent av kildedokumentene som skal evalueres med hensyn til policybrudd.</span><span class="sxs-lookup"><span data-stu-id="b9564-127">Randomly select a specified percentage of the source documents to evaluate for policy violations.</span></span></td>
<td><span data-ttu-id="b9564-128">Når du velger dette alternativet, bruker du siden Overvåkingspolicyregel til å angi prosentandelen av dokumenter som skal velges vilkårlig for overvåking.</span><span class="sxs-lookup"><span data-stu-id="b9564-128">When you select this option, use the Audit policy rule page to specify the percentage of documents to randomly select for audit.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b9564-129">Duplikat</span><span class="sxs-lookup"><span data-stu-id="b9564-129">Duplicate</span></span></td>
<td><span data-ttu-id="b9564-130">Evaluere kildedokumenter for å avgjøre om de inneholder duplikatoppføringer i angitte felt.</span><span class="sxs-lookup"><span data-stu-id="b9564-130">Evaluate source documents to determine whether they contain duplicate entries in specified fields.</span></span></td>
<td><span data-ttu-id="b9564-131">Når du velger dette alternativet, bruker du siden Overvåkingspolicyregel til å angi hvor mange dager som skal legges til ved starten av datoområdet for dokumentvalg når dokumenter evalueres for duplikatoppføringer.</span><span class="sxs-lookup"><span data-stu-id="b9564-131">When you select this option, use the Audit policy rule page to specify the number of days to add to the start of the document selection date range when documents are evaluated for duplicate entries.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b9564-132">Listesøk</span><span class="sxs-lookup"><span data-stu-id="b9564-132">List search</span></span></td>
<td><span data-ttu-id="b9564-133">Evaluere kildedokumenter for bestemte entiteter.</span><span class="sxs-lookup"><span data-stu-id="b9564-133">Evaluate source documents for specific entities.</span></span></td>
<td><span data-ttu-id="b9564-134">Rotdokumentet for spørringen definerer dokumentet som overvåkes.</span><span class="sxs-lookup"><span data-stu-id="b9564-134">The root document of the query defines the document that is being audited.</span></span> <span data-ttu-id="b9564-135">Spørringen må være en listespørring som inneholder en referanse til tabellen DirPartyTable.</span><span class="sxs-lookup"><span data-stu-id="b9564-135">The query must be a list query that includes a reference to the dirpartytable table.</span></span> <span data-ttu-id="b9564-136">Dette alternativet kan bare brukes med følgende AOT-spørringer:</span><span class="sxs-lookup"><span data-stu-id="b9564-136">This option can be used only with the following AOT queries:</span></span>
<ul>
<li><span data-ttu-id="b9564-137"><span class="ui">AuditPolicyExpenseList</span> (Overvåkede ansatte i utgiftsrapport)</span><span class="sxs-lookup"><span data-stu-id="b9564-137"><span class="ui">AuditPolicyExpenseList</span> (Expense report monitored employees)</span></span></li>
<li><span data-ttu-id="b9564-138"><span class="ui">AuditPolicyPurchList</span> (Overvåkede leverandører i bestilling)</span><span class="sxs-lookup"><span data-stu-id="b9564-138"><span class="ui">AuditPolicyPurchList</span> (Purchase order monitored vendors)</span></span></li>
<li><span data-ttu-id="b9564-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Overvåkede leverandører i leverandørfaktura)</span><span class="sxs-lookup"><span data-stu-id="b9564-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Vendor invoice monitored vendors)</span></span></li>
</ul>
<span data-ttu-id="b9564-140">Når du velger dette alternativet, angir du de overvåkede enhetene i på siden Overvåkingspolicyregel.</span><span class="sxs-lookup"><span data-stu-id="b9564-140">When you select this option, specify the monitored entities in the Audit policy rule page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b9564-141">Nøkkelordsøk</span><span class="sxs-lookup"><span data-stu-id="b9564-141">Keyword search</span></span></td>
<td><span data-ttu-id="b9564-142">Evaluere kildedokumenter for å avgjøre om de inneholder bestemte ord.</span><span class="sxs-lookup"><span data-stu-id="b9564-142">Evaluate source documents to determine whether they contain certain words.</span></span></td>
<td><span data-ttu-id="b9564-143">Når du velger dette alternativet, skriver du inn ordene du vil se etter på siden Overvåkingspolicyregel.</span><span class="sxs-lookup"><span data-stu-id="b9564-143">When you select this option, enter the words to look for in the Audit policy rule page.</span></span> <span data-ttu-id="b9564-144">Siden Overvåkingspolicyregel inneholder også alternativer som lar deg angi tabellene og feltene som skal evalueres for ordene du skrev inn.</span><span class="sxs-lookup"><span data-stu-id="b9564-144">The Audit policy rule page also includes options that let you specify the tables and fields to evaluate for the words you entered.</span></span></td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a><span data-ttu-id="b9564-145">Vanlige parametere</span><span class="sxs-lookup"><span data-stu-id="b9564-145">Common parameters</span></span>
<span data-ttu-id="b9564-146">Alle policyreglene for en bestemt overvåkingspolicy deler de samme satsvise parameterne og det samme datoområdet for dokumentutvalget.</span><span class="sxs-lookup"><span data-stu-id="b9564-146">All of the policy rules for a particular audit policy share the same batch parameters and the same document selection date range.</span></span> <span data-ttu-id="b9564-147">Disse parameterne er angitt for policyen på Tilleggsalternativer-siden.</span><span class="sxs-lookup"><span data-stu-id="b9564-147">These parameters are specified for the policy in the Additional options page.</span></span>



<a name="see-also"></a><span data-ttu-id="b9564-148">Se også</span><span class="sxs-lookup"><span data-stu-id="b9564-148">See also</span></span>
--------

<span data-ttu-id="b9564-149">[Brudd på og saker for overvåkingspolicy](audit-policy-violations-cases.md)
[Definere overvåkingspolicyer for kildedokumenter](tasks/define-audit-policies-source-documents.md)</span><span class="sxs-lookup"><span data-stu-id="b9564-149">[Audit policy violations and cases](audit-policy-violations-cases.md)
[Define audit policies for source documents](tasks/define-audit-policies-source-documents.md)</span></span>



