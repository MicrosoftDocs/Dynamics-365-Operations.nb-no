---
title: Kundeposteringsprofiler
description: Kundeposteringsprofiler styrer postering av kundetransaksjoner til økonomimodulen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: roschlom
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 71134331eae2c25f242915d63d8a4ef1dd33ed3f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991098"
---
# <a name="customer-posting-profiles"></a><span data-ttu-id="be225-103">Kundeposteringsprofiler</span><span class="sxs-lookup"><span data-stu-id="be225-103">Customer posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be225-104">Kundeposteringsprofiler styrer postering av kundetransaksjoner til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="be225-104">Customer posting profiles control the posting of customer transactions to the general ledger.</span></span>

<a name="customer-posting-profiles"></a><span data-ttu-id="be225-105">Kundeposteringsprofiler</span><span class="sxs-lookup"><span data-stu-id="be225-105">Customer posting profiles</span></span>
-------------------------

<span data-ttu-id="be225-106">Kundeposteringsprofiler gjør det mulig å tilordne finanskontoer og dokumentinnstillingene til alle kunder, en kundegruppe eller en enkelt kunde.</span><span class="sxs-lookup"><span data-stu-id="be225-106">Customer posting profiles enable you to assign general ledger accounts and document settings to all customers, a group of customers or a single customer.</span></span> <span data-ttu-id="be225-107">Disse innstillingene brukes når du oppretter salgsordrer, fritekstfakturaer, utbetalinger, purringer og rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="be225-107">These settings will be used when you create sales orders, free text invoices, cash payments, collection letters, and interest notes.</span></span> <span data-ttu-id="be225-108">For noen transaksjoner kan du velge en posteringsprofil som er forskjellig fra og har forrang for posteringsprofilene som er definert for transaksjoner på denne siden.</span><span class="sxs-lookup"><span data-stu-id="be225-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> 

<span data-ttu-id="be225-109">Standard posteringsprofil er definert i hurtigfanen Finans og merverdiavgift på siden Kundeparametere.</span><span class="sxs-lookup"><span data-stu-id="be225-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts receivable parameters page.</span></span> <span data-ttu-id="be225-110">Standardposteringsprofilen inkluderes deretter automatisk i hodet på nye dokumenter, der du kan endre den til en annen posteringsprofil om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="be225-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="be225-111">Du kan også knytte posteringsdefinisjoner til transaksjonsposteringstyper på siden Definisjoner for transaksjonspostering.</span><span class="sxs-lookup"><span data-stu-id="be225-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="be225-112">Posteringsdefinisjoner styrer posteringen av kundetransaksjoner til økonomimodulen i stedet for posteringsprofiler.</span><span class="sxs-lookup"><span data-stu-id="be225-112">Posting definitions control the posting of customer transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="be225-113">Opprette en posteringsprofil</span><span class="sxs-lookup"><span data-stu-id="be225-113">Creating a posting profile</span></span>
<span data-ttu-id="be225-114">Angi finanskontoene som brukes ved posteringen av transaksjoner som bruker den valgte posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="be225-114">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="be225-115">Velg en kontokode og, hvis mulig, et konto- eller gruppenummer for den valgte posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="be225-115">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="be225-116">Under posteringsprosessen hentes den mest korrekte posteringsprofilen for hver transaksjon ved å søke etter den mest spesifikke kontokoden, gruppenummeret eller kombinasjonen gruppe og nummer etter følgende prioritering:</span><span class="sxs-lookup"><span data-stu-id="be225-116">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="be225-117">**Kontokode**-feltverdi</span><span class="sxs-lookup"><span data-stu-id="be225-117">**Account code** field value</span></span> | <span data-ttu-id="be225-118">**Konto/gruppenummer**-feltverdi</span><span class="sxs-lookup"><span data-stu-id="be225-118">**Account/Group number** field value</span></span>            | <span data-ttu-id="be225-119">Søkeprioritet</span><span class="sxs-lookup"><span data-stu-id="be225-119">Search priority</span></span> |
|------------------------------|-------------------------------------------------|-----------------|
| <span data-ttu-id="be225-120">**Tabell**</span><span class="sxs-lookup"><span data-stu-id="be225-120">**Table**</span></span>                    | <span data-ttu-id="be225-121">Spesifikk kundekonto</span><span class="sxs-lookup"><span data-stu-id="be225-121">Specific customer account</span></span>                       | <span data-ttu-id="be225-122">1</span><span class="sxs-lookup"><span data-stu-id="be225-122">1</span></span>               |
| <span data-ttu-id="be225-123">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="be225-123">**Group**</span></span>                    | <span data-ttu-id="be225-124">Kundegruppe som tilordnes kunden</span><span class="sxs-lookup"><span data-stu-id="be225-124">Customer group that is assigned to the customer</span></span> | <span data-ttu-id="be225-125">2</span><span class="sxs-lookup"><span data-stu-id="be225-125">2</span></span>               |
| <span data-ttu-id="be225-126">**Alle**</span><span class="sxs-lookup"><span data-stu-id="be225-126">**All**</span></span>                      | <span data-ttu-id="be225-127">Tom</span><span class="sxs-lookup"><span data-stu-id="be225-127">Blank</span></span>                                           | <span data-ttu-id="be225-128">3</span><span class="sxs-lookup"><span data-stu-id="be225-128">3</span></span>               |

<span data-ttu-id="be225-129">Hvis du vil ha samme posteringsprofil for alle kundetransaksjoner, definerer du bare én posteringsprofil med Alle i Kontokode-feltet.</span><span class="sxs-lookup"><span data-stu-id="be225-129">If you want all customer transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="be225-130">Angi følgende verdier for å definere posteringsprofilen:</span><span class="sxs-lookup"><span data-stu-id="be225-130">Specify the following values to set up your posting profile:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="be225-131">Felt</span><span class="sxs-lookup"><span data-stu-id="be225-131">Field</span></span></th>
<th><span data-ttu-id="be225-132">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="be225-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="be225-133"><strong>Posteringsprofil</strong></span><span class="sxs-lookup"><span data-stu-id="be225-133"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="be225-134">Angi en kode for posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="be225-134">Enter a code for the posting profile.</span></span> <span data-ttu-id="be225-135">Du kan for eksempel opprette to posteringsprofiler for å hente én konto for kundesaldoer i den nasjonale valutaen og en annen for kundesaldoer i en utenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="be225-135">For example, you could create two posting profiles to obtain one account for customer balances in the national currency and another for customer balances in a foreign currency.</span></span> <span data-ttu-id="be225-136">Du kan kalle den ene kontoen Nasjonal og den andre Utenlandsk.</span><span class="sxs-lookup"><span data-stu-id="be225-136">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be225-137"><strong>Beskrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="be225-137"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="be225-138">Angi en beskrivelse av posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="be225-138">Enter a description of the posting profile.</span></span> <span data-ttu-id="be225-139">Dette brukes bare til å identifisere posteringsprofilen mer nøyaktig når du viser den på denne siden.</span><span class="sxs-lookup"><span data-stu-id="be225-139">This is only used to better identify the posting profile when you view it in this page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="be225-140"><strong>Kontokode</strong></span><span class="sxs-lookup"><span data-stu-id="be225-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="be225-141">Angi om posteringsprofilen gjelder en enkeltkunde, en gruppe kunder eller alle kunder:</span><span class="sxs-lookup"><span data-stu-id="be225-141">Specify whether the posting profile applies to a single customer, a group of customers, or all customers:</span></span>
<ul>
<li><span data-ttu-id="be225-142"><strong>Tabell</strong> – Posteringsprofilen gjelder for en enkelt kunde.</span><span class="sxs-lookup"><span data-stu-id="be225-142"><strong>Table</strong> – The posting profile applies to a single customer.</span></span> <span data-ttu-id="be225-143">Velg kundekontoen i feltet Konto/gruppenummer.</span><span class="sxs-lookup"><span data-stu-id="be225-143">Select the customer account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="be225-144"><strong>Gruppe</strong> – Posteringsprofilen gjelder for en kundegruppe.</span><span class="sxs-lookup"><span data-stu-id="be225-144"><strong>Group</strong> – The posting profile applies to a customer group.</span></span> <span data-ttu-id="be225-145">Velg kundegruppen i feltet Konto/gruppenummer.</span><span class="sxs-lookup"><span data-stu-id="be225-145">Select the customer group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="be225-146"><strong>Alle</strong> – Posteringsprofilen gjelder for alle kunder.</span><span class="sxs-lookup"><span data-stu-id="be225-146"><strong>All</strong> – The posting profile applies to all customers.</span></span> <span data-ttu-id="be225-147">La feltet Konto/gruppenummer stå tomt.</span><span class="sxs-lookup"><span data-stu-id="be225-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be225-148"><strong>Konto/gruppenummer</strong></span><span class="sxs-lookup"><span data-stu-id="be225-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="be225-149">Hvis Tabell velges i feltet Kontokode, velger du kontonummeret til kunden som er knyttet til posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="be225-149">If Table is selected in the Account code field, select the account number of the customer who is associated with the posting profile.</span></span> <span data-ttu-id="be225-150">Hvis Gruppe er valgt, velger du kundegruppen.</span><span class="sxs-lookup"><span data-stu-id="be225-150">If Group is selected, select the customer group.</span></span> <span data-ttu-id="be225-151">Hvis Alle er valgt, lar du feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="be225-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="be225-152"><strong>Samlekonto</strong></span><span class="sxs-lookup"><span data-stu-id="be225-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="be225-153">Velg finanskontoen som skal brukes som kundesamlekonto for kunder som er knyttet til posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="be225-153">Select the ledger account that will be used as the customer summary account for the customers who are associated with the posting profile.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be225-154"><strong>Utligningskonto</strong></span><span class="sxs-lookup"><span data-stu-id="be225-154"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="be225-155">Velg likviditetsfinanskontoen som brukes for kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="be225-155">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="be225-156">Dette feltet vises bare hvis kontantstrømprognoser er aktivert.</span><span class="sxs-lookup"><span data-stu-id="be225-156">This field will only appear if cash flow forecasts are enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="be225-157"><strong>Mva-forskuddsbetalinger</strong></span><span class="sxs-lookup"><span data-stu-id="be225-157"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="be225-158">Velg kontoen for merverdiavgift for forskuddsbetalte betalinger.</span><span class="sxs-lookup"><span data-stu-id="be225-158">Select the account for sales tax for payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Merk" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="be225-160"><strong>Obs!</strong></span><span class="sxs-lookup"><span data-stu-id="be225-160"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="be225-161">Bruk siden Kundeparametere for å angi posteringsprofilen som skal brukes når en betaling er merket som en forskuddsbetaling.</span><span class="sxs-lookup"><span data-stu-id="be225-161">Use the Accounts receivable parameters page to specify the posting profile to use when a payment is marked as a prepayment.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be225-162"><strong>Konto for rabattavsetning</strong></span><span class="sxs-lookup"><span data-stu-id="be225-162"><strong>Liabilities for discount account</strong></span></span></td>
<td><span data-ttu-id="be225-163">Velg finanskontoen for diskontoforpliktelser.</span><span class="sxs-lookup"><span data-stu-id="be225-163">Select the ledger account for liabilities of discount.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="be225-164"><strong>Purreforløp</strong></span><span class="sxs-lookup"><span data-stu-id="be225-164"><strong>Collection letter sequence</strong></span></span></td>
<td><span data-ttu-id="be225-165">Velg identifikatoren for purreforløpet som skal brukes for kunder som er tilordnet posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="be225-165">Select the identifier of the collection letter sequence to use for customers to whom the posting profile is assigned.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be225-166"><strong>Rentekode</strong></span><span class="sxs-lookup"><span data-stu-id="be225-166"><strong>Interest code</strong></span></span></td>
<td><span data-ttu-id="be225-167">Velg rentekoden som skal brukes for beregning av rente for kunder som er tilordnet posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="be225-167">Select the interest code to use for the calculation of interest for customers to whom the posting profile is assigned.</span></span></td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a><span data-ttu-id="be225-168">**Tabellrestriksjoner**</span><span class="sxs-lookup"><span data-stu-id="be225-168">**Table restrictions**</span></span>

<span data-ttu-id="be225-169">For transaksjoner med den valgte posteringsprofilen kan du angi om transaksjonene skal utlignes automatisk, om rente skal beregnes, og om purringer blir utstedt.</span><span class="sxs-lookup"><span data-stu-id="be225-169">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="be225-170">Du kan også velge kontoen som brukes når transaksjoner med den valgte posteringsprofilen er lukket.</span><span class="sxs-lookup"><span data-stu-id="be225-170">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="be225-171">Angi følgende verdier for å definere posteringsprofilen:</span><span class="sxs-lookup"><span data-stu-id="be225-171">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="be225-172">Felt</span><span class="sxs-lookup"><span data-stu-id="be225-172">Field</span></span>                 | <span data-ttu-id="be225-173">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="be225-173">Description</span></span>                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be225-174">**Utligning**</span><span class="sxs-lookup"><span data-stu-id="be225-174">**Settlement**</span></span>        | <span data-ttu-id="be225-175">Merk av for dette valget for å aktivere automatisk utligning for transaksjoner med denne posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="be225-175">Select this toggle to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="be225-176">Hvis merket fjernes for dette valget, må du manuelt utligne transaksjoner ved hjelp av Utlign åpne transaksjoner-siden eller Angi kundebetalinger-siden.</span><span class="sxs-lookup"><span data-stu-id="be225-176">If this toggle is cleared, you must manually settle transactions by using the Settle open transactions page or the Enter customer payments page.</span></span> |
| <span data-ttu-id="be225-177">**Rente**</span><span class="sxs-lookup"><span data-stu-id="be225-177">**Interest**</span></span>          | <span data-ttu-id="be225-178">Merk av for dette valget hvis rente skal beregnes på utestående saldoer for kundekontoer som bruker denne profilen.</span><span class="sxs-lookup"><span data-stu-id="be225-178">Select this toggle if interest should be calculated on outstanding balances for customer accounts that use this profile.</span></span> <span data-ttu-id="be225-179">Hvis merket fjernes for dette valget, vil det ikke beregnes renter for disse kundene.</span><span class="sxs-lookup"><span data-stu-id="be225-179">If this toggle is cleared, interest will not be calculated for these customers.</span></span>                                           |
| <span data-ttu-id="be225-180">**Purring**</span><span class="sxs-lookup"><span data-stu-id="be225-180">**Collection letter**</span></span> | <span data-ttu-id="be225-181">Merk av for dette valget hvis purrebrev skal genereres for kundekontoer som bruker denne profilen.</span><span class="sxs-lookup"><span data-stu-id="be225-181">Select this toggle if collection letters should be generated for customer accounts that use this profile.</span></span> <span data-ttu-id="be225-182">Hvis merket fjernes for dette valget, vil det ikke genereres purrebrev for disse kundene.</span><span class="sxs-lookup"><span data-stu-id="be225-182">If this toggle is cleared, collection letters will not be generated for these customers.</span></span>                                                 |
| <span data-ttu-id="be225-183">**Lukke**</span><span class="sxs-lookup"><span data-stu-id="be225-183">**Close**</span></span>             | <span data-ttu-id="be225-184">Velg en posteringsprofil som du vil bytte til når transaksjoner med denne posteringsprofilen er lukket.</span><span class="sxs-lookup"><span data-stu-id="be225-184">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="be225-185">En transaksjon anses som lukket når den er fullstendig utlignet.</span><span class="sxs-lookup"><span data-stu-id="be225-185">A transaction is regarded as closed when it has been settled in full.</span></span>                                                                           |



<span data-ttu-id="be225-186">Hvis du vil ha mer informasjon, kan du se [Oversikt over kundebetaling](../cash-bank-management/tasks/customer-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="be225-186">For more information, see [Customer payment overview](../cash-bank-management/tasks/customer-payment-overview.md).</span></span>

