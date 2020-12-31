---
title: Regnskapsdistribusjoner og underfinansjournaloppføringer for leverandørfakturaer
description: Regnskapsdistribusjoner brukes til å definere hvordan beløp skal gjøres rede for, for eksempel hvordan utgiften, avgiften eller gebyrene skal gjøres rede for på en leverandørfaktura. Alle beløp som må redegjøres for når leverandørfakturaen er journalføres, har én eller flere regnskapsdistribusjoner.
author: abruer
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8e38e6a571bb7f08b32548bcb4af823807a4340
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446540"
---
# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a><span data-ttu-id="5e893-104">Regnskapsdistribusjoner og underfinansjournaloppføringer for leverandørfakturaer</span><span class="sxs-lookup"><span data-stu-id="5e893-104">Accounting distributions and subledger journal entries for vendor invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e893-105">Regnskapsdistribusjoner brukes til å definere hvordan beløp skal gjøres rede for, for eksempel hvordan utgiften, avgiften eller gebyrene skal gjøres rede for på en leverandørfaktura.</span><span class="sxs-lookup"><span data-stu-id="5e893-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="5e893-106">Alle beløp som må redegjøres for når leverandørfakturaen er journalføres, har én eller flere regnskapsdistribusjoner.</span><span class="sxs-lookup"><span data-stu-id="5e893-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

<a name="accounting-distributions"></a><span data-ttu-id="5e893-107">Regnskapsdistribusjoner</span><span class="sxs-lookup"><span data-stu-id="5e893-107">Accounting distributions</span></span> 
-------------------------

<span data-ttu-id="5e893-108">Du kan bruke følgende knapper på Leverandørfaktura-siden til å vise, og eventuelt endre, regnskapsdistribusjonene for hvert beløp i leverandørfakturaen.</span><span class="sxs-lookup"><span data-stu-id="5e893-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="5e893-109">**Fordel beløp** – Vis og endre regnskapsdistribusjonene for en enkelt linje og eventuelle underordnede linjer, for eksempel avgifter eller gebyrer.</span><span class="sxs-lookup"><span data-stu-id="5e893-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="5e893-110">Du kan også vise og endre regnskapsdistribusjonene for den underordnede linjen direkte fra Mva-transaksjoner- eller Tilleggstransaksjoner-siden.</span><span class="sxs-lookup"><span data-stu-id="5e893-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="5e893-111">Endre topptekstbeløp for topptekstbeløp, for eksempel tillegg eller avrundingsbeløp for valuta.</span><span class="sxs-lookup"><span data-stu-id="5e893-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="5e893-112">Endre linjebeløp for leverandørfaktur.</span><span class="sxs-lookup"><span data-stu-id="5e893-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="5e893-113">**Vis distribusjoner** – Vis regnskapsdistribusjonene for alle linjer i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="5e893-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="5e893-114">Du kan ikke endre regnskapsdistribusjonene fra denne visningen.</span><span class="sxs-lookup"><span data-stu-id="5e893-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="5e893-115">Vis overskrift og linjebeløp.</span><span class="sxs-lookup"><span data-stu-id="5e893-115">View header and line amounts.</span></span>

<span data-ttu-id="5e893-116">Hvis leverandørfakturaen refererer til en bestilling, kan du dele opp og endre regnskapsdistribusjonene for linjer som inneholder en vare som ikke er lagerført.</span><span class="sxs-lookup"><span data-stu-id="5e893-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="5e893-117">Hvis leverandørfakturalinjen ikke refererer til en bestillingslinje, kan du også slette en regnskapsdistribusjon.</span><span class="sxs-lookup"><span data-stu-id="5e893-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="5e893-118">Du kan ikke dele eller slette linjer for gebyrer, avgifter og linjerabatter.</span><span class="sxs-lookup"><span data-stu-id="5e893-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="5e893-119">Du kan endre finanskontoen, men du kan ikke endre beløpene eller prosentandelene.</span><span class="sxs-lookup"><span data-stu-id="5e893-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="5e893-120">Hvis den overordnede linjen inneholder en vare som ikke er lagerført, og regnskapsdistribusjonene er delt, deles den underordnede linjen automatisk for å samsvare med finansdimensjonene for den overordnede linjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="5e893-121">Regnskapsdistribusjonene for den underordnede linjen ikke kan deles ytterligere eller slettes, men avhengig av oppsettet for den underordnede linjen, kan det hende du kan endre finanskontoen for regnskapsdistribusjonene i den underordnede linjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="5e893-122">Distribuere beløp</span><span class="sxs-lookup"><span data-stu-id="5e893-122">Distributing amounts</span></span>
<span data-ttu-id="5e893-123">Når du registrerer en leverandørfaktura, fordeles beløpene på følgende måte.</span><span class="sxs-lookup"><span data-stu-id="5e893-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5e893-124">Type leverandørfakturalinje</span><span class="sxs-lookup"><span data-stu-id="5e893-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="5e893-125">Rekkefølge som bestemmer hvor hovedkontoen vises fra</span><span class="sxs-lookup"><span data-stu-id="5e893-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="5e893-126">Rekkefølge som bestemmer hvilken standard finansdimensjon som vises</span><span class="sxs-lookup"><span data-stu-id="5e893-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5e893-127">Lagerført produkt</span><span class="sxs-lookup"><span data-stu-id="5e893-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="5e893-128">Regnskapsdistribusjonen for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-129">Hovedkonto-feltet når Innkjøpsutgift for produktet velges på siden Postering.</span><span class="sxs-lookup"><span data-stu-id="5e893-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="5e893-130">Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-131">Bruk standard finansdimensjonsverdier for leverandørfakturaen.</span><span class="sxs-lookup"><span data-stu-id="5e893-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e893-132">Innkjøpskategori eller et produkt som ikke er lagerført</span><span class="sxs-lookup"><span data-stu-id="5e893-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="5e893-133">Regnskapsdistribusjonen for bestillingslinjen, hvis leverandørfakturalinjen refererer til en bestillingslinje.</span><span class="sxs-lookup"><span data-stu-id="5e893-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-134">Hovedkonto-feltet når Innkjøpsutgift for utgiften velges på siden Postering.</span><span class="sxs-lookup"><span data-stu-id="5e893-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="5e893-135">Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-136">Hvis hovedkontoen er en tildelingskonto, bruker du standardverdien fra tildelingskontodefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="5e893-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="5e893-137">Bruk standard finansdimensjonsverdier for leverandørfakturaen.</span><span class="sxs-lookup"><span data-stu-id="5e893-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="5e893-138">Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="5e893-139">Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</span><span class="sxs-lookup"><span data-stu-id="5e893-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e893-140">Anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="5e893-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="5e893-141">Regnskapsdistribusjonen for bestillingslinjen, hvis leverandørfakturalinjen refererer til en bestillingslinje.</span><span class="sxs-lookup"><span data-stu-id="5e893-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-142">Hvis Anskaffelse velges i Transaksjonstype-feltet i skjemaet Leverandørfaktura, Hovedkonto-feltet når Anskaffelse velges på siden Posteringsprofil for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="5e893-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="5e893-143">Hvis Anskaffelsesjustering velges i Transaksjonstype-feltet, Hovedkonto-feltet når Anskaffelsesjustering velges på siden Posteringsprofil for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="5e893-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="5e893-144">Bruk kontodistribusjonen for bestillingslinjen hvis fakturalinjereferansen er en bestillingslinje.</span><span class="sxs-lookup"><span data-stu-id="5e893-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-145">Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="5e893-146">Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</span><span class="sxs-lookup"><span data-stu-id="5e893-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e893-147">Prosjekt definert på leverandørfakturalinjen</span><span class="sxs-lookup"><span data-stu-id="5e893-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="5e893-148">Regnskapsdistribusjonen for bestillingslinjen, hvis fakturalinjen refererer til en bestillingslinje.</span><span class="sxs-lookup"><span data-stu-id="5e893-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-149">Hvis Saldo velges i feltet Poster kostnader - vare på siden Prosjektgrupper, Hovedkonto-feltet når Kostnad velges på siden Finansposteringsoppsett.</span><span class="sxs-lookup"><span data-stu-id="5e893-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="5e893-150">Hvis Resultat velges i feltet Poster kostnader - vare på siden Prosjektgrupper, Hovedkonto-feltet når Kostnad - vare velges på siden Finansposteringsoppsett.</span><span class="sxs-lookup"><span data-stu-id="5e893-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="5e893-151">Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e893-152">Linjerabatt</span><span class="sxs-lookup"><span data-stu-id="5e893-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="5e893-153">Regnskapsdistribusjonen for bestillingslinjen, hvis fakturalinjen refererer til en bestillingslinje.</span><span class="sxs-lookup"><span data-stu-id="5e893-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-154">Hovedkonto-feltet når rabatt velges på Postering-siden.</span><span class="sxs-lookup"><span data-stu-id="5e893-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="5e893-155">Hvis en hovedkonto for en rabatt ikke er definert i posteringsprofilen, regnskapsdistribusjonen for den utvidede prisen på bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="5e893-156">Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke regnskapsdistribusjonen for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-157">Bruk finansdimensjonsverdiene fra regnskapsdistribusjonene for den utvidede prisen for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="5e893-158">Bruk finansdimensjonsverdiene for leverandørfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="5e893-159">Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</span><span class="sxs-lookup"><span data-stu-id="5e893-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e893-160">Innkjøpstillegg, som er angitt i kategorien Pris og rabatt i bestillingslinjen</span><span class="sxs-lookup"><span data-stu-id="5e893-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="5e893-161">Regnskapsdistribusjonen for bestillingslinjen, hvis fakturalinjen refererer til en bestillingslinje.</span><span class="sxs-lookup"><span data-stu-id="5e893-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-162">Regnskapsdistribusjonen for den utvidede prisen på bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="5e893-163">Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-164">Bruk finansdimensjonsverdiene fra regnskapsdistribusjonene for den utvidede prisen for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e893-165">Linjetillegg</span><span class="sxs-lookup"><span data-stu-id="5e893-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="5e893-166">Regnskapsdistribusjonen for bestillingslinjen, hvis fakturalinjen refererer til en bestillingslinje.</span><span class="sxs-lookup"><span data-stu-id="5e893-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-167">Hvis finanskontoen velges i Debettype-feltet i skjemaet Tilleggskode, Debetkonto-feltet på siden Tilleggskode.</span><span class="sxs-lookup"><span data-stu-id="5e893-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="5e893-168">Hvis Vare er valgt i Debettype-feltet i Tilleggskode-skjemaet, regnskapsdistribusjonen for den utvidede prisen på bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-169">Hvis Kunde/leverandør velges i Debettype-feltet i skjemaet Tilleggskode, Kreditkonto-feltet på siden Tilleggskode.</span><span class="sxs-lookup"><span data-stu-id="5e893-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="5e893-170">Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-171">Bruk finansdimensjonsverdiene fra regnskapsdistribusjonene for den utvidede prisen for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="5e893-172">Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="5e893-173">Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</span><span class="sxs-lookup"><span data-stu-id="5e893-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e893-174">Avgift med følgende betingelse:</span><span class="sxs-lookup"><span data-stu-id="5e893-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="5e893-175">Alternativet Bruk amerikanske avgiftsregler er valgt på siden Parametere for økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="5e893-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="5e893-176">Regnskapsdistribusjonen for bestillingslinjen, hvis fakturalinjen refererer til en bestillingslinje.</span><span class="sxs-lookup"><span data-stu-id="5e893-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-177">Regnskapsdistribusjonen for den utvidede prisen eller tillegget.</span><span class="sxs-lookup"><span data-stu-id="5e893-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="5e893-178">Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-179">Bruk finansdimensjonsverdiene fra regnskapsdistribusjonene for den utvidede prisen for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="5e893-180">Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e893-181">Avgift med følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="5e893-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="5e893-182">Alternativet Bruk amerikanske avgiftsregler er ikke valgt på siden Parametere for økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="5e893-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="5e893-183">Use tax-feltet for mva-gruppen er ikke avmerket på siden Mva-grupper.</span><span class="sxs-lookup"><span data-stu-id="5e893-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="5e893-184">Hvis avgiftsbeløpet er fradragsberettiget, feltet Innkommende merverdiavgift på siden Finansposteringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="5e893-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="5e893-185">Hvis avgiftsbeløpet ikke er fradragsberettiget, den utvidede prisen eller regnskapsdistribusjonen for tillegget.</span><span class="sxs-lookup"><span data-stu-id="5e893-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="5e893-186">Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-187">Bruk finansdimensjonsverdiene fra den utvidede prisen eller regnskapsdistribusjonene for avgiften på bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="5e893-188">Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="5e893-189">Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</span><span class="sxs-lookup"><span data-stu-id="5e893-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e893-190">Avgift med følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="5e893-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="5e893-191">Alternativet Bruk amerikanske avgiftsregler er ikke valgt på siden Parametere for økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="5e893-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="5e893-192">Use tax-feltet for mva-gruppen er valgt på siden Mva-grupper.</span><span class="sxs-lookup"><span data-stu-id="5e893-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="5e893-193">Hvis avgiftsbeløpet er fradragsberettiget, feltet Innkommende merverdiavgift på siden Finansposteringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="5e893-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="5e893-194">Hvis avgiftsbeløpet ikke er fradragsberettiget, feltet Use tax-utgift på siden Finansposteringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="5e893-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="5e893-195">Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-196">Bruk finansdimensjonsverdiene fra den utvidede prisen eller regnskapsdistribusjonene for avgiften på bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="5e893-197">Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="5e893-198">Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</span><span class="sxs-lookup"><span data-stu-id="5e893-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e893-199">Hodegebyr</span><span class="sxs-lookup"><span data-stu-id="5e893-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="5e893-200">Hvis finanskontoen velges i Debettype-feltet i skjemaet Tilleggskode, Debetkonto-feltet på siden Tilleggskode.</span><span class="sxs-lookup"><span data-stu-id="5e893-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="5e893-201">Hvis Kunde/leverandør velges i Debettype-feltet i skjemaet Tilleggskode, Kreditkonto-feltet på siden Tilleggskode.</span><span class="sxs-lookup"><span data-stu-id="5e893-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="5e893-202">Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-203">Hvis hovedkontoen er en tildelingskonto, bruker du standardverdien fra tildelingskontodefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="5e893-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="5e893-204">Bruk standardmalverdier for finansdimensjon fra leverandørfakturhodet.</span><span class="sxs-lookup"><span data-stu-id="5e893-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="5e893-205">Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="5e893-206">Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</span><span class="sxs-lookup"><span data-stu-id="5e893-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e893-207">Hoderabatt</span><span class="sxs-lookup"><span data-stu-id="5e893-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="5e893-208">Hovedkonto-feltet for posteringstypen Leverandørfakturarabatt på siden Kontoer for automatiske transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="5e893-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="5e893-209">Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="5e893-210">Bruk finansdimensjonsverdiene fra regnskapsdistribusjonene for den utvidede prisen for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="5e893-211">Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="5e893-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="5e893-212">Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</span><span class="sxs-lookup"><span data-stu-id="5e893-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a><span data-ttu-id="5e893-213">Distribusjonsavgifter</span><span class="sxs-lookup"><span data-stu-id="5e893-213">Distributing taxes</span></span>
------------------

<span data-ttu-id="5e893-214">Kan ikke opprette regnskapsdistribusjoner for avgifter før avgifter er beregnet.</span><span class="sxs-lookup"><span data-stu-id="5e893-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="5e893-215">Hvis du vil beregne merverdiavgift, må du fullføre en av de følgende oppgavene på Leverandørfaktura-siden:</span><span class="sxs-lookup"><span data-stu-id="5e893-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="5e893-216">Vis fakturatotalen.</span><span class="sxs-lookup"><span data-stu-id="5e893-216">View the invoice total.</span></span>
-   <span data-ttu-id="5e893-217">Vis merverdiavgiften.</span><span class="sxs-lookup"><span data-stu-id="5e893-217">View the sales tax.</span></span>
-   <span data-ttu-id="5e893-218">Vis underfinansjournalen.</span><span class="sxs-lookup"><span data-stu-id="5e893-218">View the subledger journal.</span></span>
-   <span data-ttu-id="5e893-219">Vis regnskapsdistribusjoner for den fullførte leverandørfakturaen.</span><span class="sxs-lookup"><span data-stu-id="5e893-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="5e893-220">Sett leverandørfakturaen på vent.</span><span class="sxs-lookup"><span data-stu-id="5e893-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="5e893-221">Poster leverandørfakturaen.</span><span class="sxs-lookup"><span data-stu-id="5e893-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="5e893-222">Underfinansjournaler for leverandørfakturaer</span><span class="sxs-lookup"><span data-stu-id="5e893-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="5e893-223">Før du posterer en leverandørfaktura, kan du vise den fullstendige regnskapsoppføringen for fakturaen, som inkluderer debet og kredit, for å bekrefte at fakturaen posteres på de riktige kontoene.</span><span class="sxs-lookup"><span data-stu-id="5e893-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="5e893-224">Denne visningen av den fullstendige regnskapsoppføringen kalles en underfinansjournal.</span><span class="sxs-lookup"><span data-stu-id="5e893-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="5e893-225">Hvis underfinansjournaloppføringen er feil når du forhåndsviser den før du journalfører leverandørfakturaen, kan du ikke endre underfinansjournaloppføringen.</span><span class="sxs-lookup"><span data-stu-id="5e893-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="5e893-226">I stedet må du endre regnskapsdistribusjonene eller posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="5e893-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="5e893-227">Regnskapsdistribusjonene brukes til å definere én side av regnskapsoppføringen, debet eller kredit.</span><span class="sxs-lookup"><span data-stu-id="5e893-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="5e893-228">Motkontooppføringen i underfinansjournalen opprettes ved å bruke posteringsprofilene, for eksempel fra leverandørkontoen eller avgift.</span><span class="sxs-lookup"><span data-stu-id="5e893-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>





