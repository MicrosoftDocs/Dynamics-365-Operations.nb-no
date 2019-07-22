---
title: Leverandørposteringsprofiler
description: Leverandørposteringsprofiler styrer postering av leverandørtransaksjoner til økonomimodulen.
author: abruer
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3f62df7ec5627556561db950d54ff4347d2b4d6
ms.sourcegitcommit: ce84a1faeda6013ef6a90038d811a72f375b604e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/12/2019
ms.locfileid: "1625901"
---
# <a name="vendor-posting-profiles"></a><span data-ttu-id="3c715-103">Leverandørposteringsprofiler</span><span class="sxs-lookup"><span data-stu-id="3c715-103">Vendor posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c715-104">Leverandørposteringsprofiler styrer postering av leverandørtransaksjoner til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="3c715-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="3c715-105">Leverandørposteringsprofiler</span><span class="sxs-lookup"><span data-stu-id="3c715-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="3c715-106">Leverandørposteringsprofiler gjør det mulig å tilordne finanskontoer og dokumentinnstillinger til alle leverandører, en gruppe med leverandører eller en enkelt leverandør.</span><span class="sxs-lookup"><span data-stu-id="3c715-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors, or a single vendor.</span></span> <span data-ttu-id="3c715-107">Disse innstillingene brukes når du oppretter bestillinger, leverandørfakturaer og kontantbetalinger.</span><span class="sxs-lookup"><span data-stu-id="3c715-107">These settings will be used when you create purchase orders, vendor invoices, and cash payments.</span></span> <span data-ttu-id="3c715-108">For noen transaksjoner kan du velge en posteringsprofil som er forskjellig fra og har forrang for posteringsprofilene som er definert for transaksjoner på denne siden.</span><span class="sxs-lookup"><span data-stu-id="3c715-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions on this page.</span></span> <span data-ttu-id="3c715-109">Standard posteringsprofil er definert i hurtigfanen **Finans og merverdiavgift** på siden **Leverandørparametere**.</span><span class="sxs-lookup"><span data-stu-id="3c715-109">The default posting profile is defined on the **Ledger and Sales Tax** FastTab on the **Accounts payable parameters** page.</span></span> <span data-ttu-id="3c715-110">Standard posteringsprofil inkluderes deretter automatisk i hodet på nye dokumenter, der du kan endre den til en annen posteringsprofil om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="3c715-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile, if needed.</span></span>

<span data-ttu-id="3c715-111">Du kan også knytte posteringsdefinisjoner til transaksjonsposteringstyper på siden **Definisjoner for transaksjonspostering**.</span><span class="sxs-lookup"><span data-stu-id="3c715-111">You can also associate posting definitions with transaction posting types on the **Transaction posting definitions** page.</span></span> <span data-ttu-id="3c715-112">Posteringsdefinisjoner styrer posteringen av leverandørtransaksjoner til økonomimodulen i stedet for posteringsprofiler.</span><span class="sxs-lookup"><span data-stu-id="3c715-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="3c715-113">Opprette en posteringsprofil</span><span class="sxs-lookup"><span data-stu-id="3c715-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="3c715-114">**Oppsett**</span><span class="sxs-lookup"><span data-stu-id="3c715-114">**Setup**</span></span>

<span data-ttu-id="3c715-115">Angi finanskontoene som brukes ved posteringen av transaksjoner som bruker den valgte posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="3c715-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="3c715-116">Velg en kontokode og, hvis mulig, et konto- eller gruppenummer for den valgte posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="3c715-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="3c715-117">Under posteringsprosessen hentes den mest aktuelle posteringsprofilen for hver transaksjon ved å søke etter den mest spesifikke kontokoden, gruppenummeret eller kombinasjonen gruppe og nummer etter følgende prioritering.</span><span class="sxs-lookup"><span data-stu-id="3c715-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority.</span></span>

| <span data-ttu-id="3c715-118">**Kontokode**-feltverdi</span><span class="sxs-lookup"><span data-stu-id="3c715-118">**Account code** field value</span></span> | <span data-ttu-id="3c715-119">**Konto/gruppenummer**-feltverdi</span><span class="sxs-lookup"><span data-stu-id="3c715-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="3c715-120">Søkeprioritet</span><span class="sxs-lookup"><span data-stu-id="3c715-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="3c715-121">**Tabell**</span><span class="sxs-lookup"><span data-stu-id="3c715-121">**Table**</span></span>                    | <span data-ttu-id="3c715-122">Bestemt leverandørkonto</span><span class="sxs-lookup"><span data-stu-id="3c715-122">Specific vendor account</span></span>                     | <span data-ttu-id="3c715-123">1</span><span class="sxs-lookup"><span data-stu-id="3c715-123">1</span></span>               |
| <span data-ttu-id="3c715-124">**Gruppere**</span><span class="sxs-lookup"><span data-stu-id="3c715-124">**Group**</span></span>                    | <span data-ttu-id="3c715-125">Leverandørgruppe som er knyttet til leverandøren</span><span class="sxs-lookup"><span data-stu-id="3c715-125">Vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="3c715-126">2</span><span class="sxs-lookup"><span data-stu-id="3c715-126">2</span></span>               |
| <span data-ttu-id="3c715-127">**Alle**</span><span class="sxs-lookup"><span data-stu-id="3c715-127">**All**</span></span>                      | <span data-ttu-id="3c715-128">Tom</span><span class="sxs-lookup"><span data-stu-id="3c715-128">Blank</span></span>                                       | <span data-ttu-id="3c715-129">3</span><span class="sxs-lookup"><span data-stu-id="3c715-129">3</span></span>               |

<span data-ttu-id="3c715-130">Hvis du vil ha samme posteringsprofil for alle leverandørtransaksjoner, definerer du bare én posteringsprofil med **Alle** i **Kontokode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3c715-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with **All** in the **Account code** field.</span></span> <span data-ttu-id="3c715-131">Angi følgende verdier for å definere posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="3c715-131">Specify the following values to set up your posting profile.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3c715-132">Felt</span><span class="sxs-lookup"><span data-stu-id="3c715-132">Field</span></span></th>
<th><span data-ttu-id="3c715-133">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="3c715-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3c715-134"><strong>Posteringsprofil</strong></span><span class="sxs-lookup"><span data-stu-id="3c715-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="3c715-135">Angi en kode for posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="3c715-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="3c715-136">Du kan for eksempel opprette to posteringsprofiler for å hente én konto for leverandørsaldoer i nasjonal valuta og en annen for leverandørsaldoer i en utenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="3c715-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="3c715-137">Du kan kalle den ene kontoen Nasjonal og den andre Utenlandsk.</span><span class="sxs-lookup"><span data-stu-id="3c715-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c715-138"><strong>Beskrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="3c715-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="3c715-139">Angi en beskrivelse av posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="3c715-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c715-140"><strong>Kontokode</strong></span><span class="sxs-lookup"><span data-stu-id="3c715-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="3c715-141">Angi om posteringsprofilen gjelder for en spesifikk leverandør, en gruppe leverandører eller alle leverandører:</span><span class="sxs-lookup"><span data-stu-id="3c715-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="3c715-142"><strong>Tabell</strong> – Posteringsprofilen gjelder for en enkelt leverandør.</span><span class="sxs-lookup"><span data-stu-id="3c715-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="3c715-143">Velg leverandørkontoen i feltet <strong>Konto/gruppenummer</strong>.</span><span class="sxs-lookup"><span data-stu-id="3c715-143">Select the vendor account in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="3c715-144"><strong>Gruppe</strong> – Posteringsprofilen gjelder for en leverandørgruppe.</span><span class="sxs-lookup"><span data-stu-id="3c715-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="3c715-145">Velg leverandørgruppen i feltet <strong>Konto/gruppenummer</strong>.</span><span class="sxs-lookup"><span data-stu-id="3c715-145">Select the vendor group in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="3c715-146"><strong>Alle</strong> – Posteringsprofilen gjelder for alle leverandører.</span><span class="sxs-lookup"><span data-stu-id="3c715-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="3c715-147">La feltet <strong>Konto/gruppenummer</strong> stå tomt.</span><span class="sxs-lookup"><span data-stu-id="3c715-147">Leave the <strong>Account/Group number</strong> field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c715-148"><strong>Konto/gruppenummer</strong></span><span class="sxs-lookup"><span data-stu-id="3c715-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="3c715-149">Hvis <strong>Tabell</strong> er valgt i feltet <strong>Kontokode</strong>, velger du kontonummeret til leverandøren som er knyttet til posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="3c715-149">If <strong>Table</strong> is selected in the <strong>Account code</strong> field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="3c715-150">Hvis <strong>Gruppe</strong> er valgt, velger du en leverandørgruppe.</span><span class="sxs-lookup"><span data-stu-id="3c715-150">If <strong>Group</strong> is selected, select a vendor group.</span></span> <span data-ttu-id="3c715-151">Hvis <strong>Alle</strong> er valgt, lar du feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="3c715-151">If <strong>All</strong> is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c715-152"><strong>Samlekonto</strong></span><span class="sxs-lookup"><span data-stu-id="3c715-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="3c715-153">Velg finanskontoen som skal brukes som samlekonto for leverandørene som posteringsprofilen er relatert til.</span><span class="sxs-lookup"><span data-stu-id="3c715-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span> <span data-ttu-id="3c715-154">Parameteren <strong>Ikke tillat manuell registrering</strong> for denne hovedkontoen blir merket.</span><span class="sxs-lookup"><span data-stu-id="3c715-154">The <strong>Do not allow manual entry</strong> parameter for this main account will be marked.</span></span> <span data-ttu-id="3c715-155">Hvis du senere fjerner denne kontoen fra posteringsprofilen, må du validere innstillingen for <strong>Ikke tillat manuell registrering</strong> på <strong>Hovedkontoer</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="3c715-155">If you subsequently remove this account from the posting profile, validate the <strong>Do not allow manual entry</strong> setting on the <strong>Main accounts</strong> page.</span></span> 
<p><span data-ttu-id="3c715-156"><strong>Obs!</strong> Hvis alternativet <strong>Bruk posteringsdefinisjoner</strong> er valgt på siden <strong>Parametere for økonomimodul</strong>, brukes transaksjonsposteringsdefinisjonen for leverandørfakturaer i stedet for samlekontoen.</span><span class="sxs-lookup"><span data-stu-id="3c715-156"><strong>Note:</strong> If the <strong>Use posting definitions</strong> option is selected on the <strong>General ledger parameters</strong> page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c715-157"><strong>Utligningskonto</strong></span><span class="sxs-lookup"><span data-stu-id="3c715-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="3c715-158">Velg likviditetsfinanskontoen som brukes for kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="3c715-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="3c715-159">Dette feltet er bare tilgjengelig når kontantstrømprognoser er aktivert.</span><span class="sxs-lookup"><span data-stu-id="3c715-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c715-160"><strong>Mva-forskuddsbetalinger</strong></span><span class="sxs-lookup"><span data-stu-id="3c715-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="3c715-161">Velg kontoen for merverdiavgift for forskuddsbetalte betalinger.</span><span class="sxs-lookup"><span data-stu-id="3c715-161">Select the account for sales tax payments that are received in advance.</span></span>
<p><span data-ttu-id="3c715-162"><strong>Obs!</strong> Posteringsprofilen som brukes når betalingen er merket som en forskuddsbetaling, velges i <strong>Postering</strong>-profilen med feltet <strong>Journalbilag for forskuddsbetaling</strong> i området <strong>Finans og merverdiavgift</strong> på siden <strong>Leverandørparametere</strong>.</span><span class="sxs-lookup"><span data-stu-id="3c715-162"><strong>Note:</strong> The posting profile that is used when the payment is marked as a prepayment is selected in the <strong>Posting</strong> profile with <strong>Prepayment journal voucher</strong> field in the <strong>Ledger and sales tax</strong> area on the <strong>Accounts payable parameters</strong> page.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c715-163"><strong>Ankomst</strong></span><span class="sxs-lookup"><span data-stu-id="3c715-163"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="3c715-164">Velg finanskontoen som informasjon om ikke-godkjente leverandørfakturaene er postert til.</span><span class="sxs-lookup"><span data-stu-id="3c715-164">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="3c715-165">Informasjonen angis i ankomstregistreringsjournalen.</span><span class="sxs-lookup"><span data-stu-id="3c715-165">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="3c715-166">En bruker kan for eksempel angi svært enkel informasjon om leverandørfakturaer når de mottas i fakturaregisteret.</span><span class="sxs-lookup"><span data-stu-id="3c715-166">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="3c715-167">Når fakturaregisteret posteres, blir transaksjonene postert til kontoen som er angitt her og i <strong>Motkonto</strong>-feltet.</span><span class="sxs-lookup"><span data-stu-id="3c715-167">When the invoice register is posted, the transactions are posted to the account that is entered here and in the <strong>Offset account</strong> field.</span></span> <span data-ttu-id="3c715-168">Når fakturaene er godkjent, blir gjelden overført fra ankomstkontoen til samlekontoen for leverandør.</span><span class="sxs-lookup"><span data-stu-id="3c715-168">When the invoices are approved, the debt is transferred from the arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c715-169"><strong>Motkonto</strong></span><span class="sxs-lookup"><span data-stu-id="3c715-169"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="3c715-170">Velg finanskontoen som brukes til å motpostere ikke-godkjente leverandørfakturaer som oppdateres via fakturaregisteret.</span><span class="sxs-lookup"><span data-stu-id="3c715-170">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="3c715-171">Motposteringskontoen fungerer som motposteringskontoen for transaksjoner som posteres til ankomstkontoer.</span><span class="sxs-lookup"><span data-stu-id="3c715-171">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="3c715-172">Kontoen inneholder derfor leverandørinnkjøp som ennå ikke er godkjent.</span><span class="sxs-lookup"><span data-stu-id="3c715-172">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a><span data-ttu-id="3c715-173">**Tabellrestriksjoner**</span><span class="sxs-lookup"><span data-stu-id="3c715-173">**Table restrictions**</span></span>

<span data-ttu-id="3c715-174">For transaksjoner med den valgte posteringsprofilen kan du angi om transaksjonene skal utlignes automatisk, om rente skal beregnes, og om purringer blir utstedt.</span><span class="sxs-lookup"><span data-stu-id="3c715-174">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="3c715-175">Du kan også velge kontoen som brukes når transaksjoner med den valgte posteringsprofilen er lukket.</span><span class="sxs-lookup"><span data-stu-id="3c715-175">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="3c715-176">Angi følgende verdier for å definere posteringsprofilen</span><span class="sxs-lookup"><span data-stu-id="3c715-176">Specify the following values to set up your posting profile</span></span>

| <span data-ttu-id="3c715-177">Felt</span><span class="sxs-lookup"><span data-stu-id="3c715-177">Field</span></span>          | <span data-ttu-id="3c715-178">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="3c715-178">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c715-179">**Utligning**</span><span class="sxs-lookup"><span data-stu-id="3c715-179">**Settlement**</span></span> | <span data-ttu-id="3c715-180">Merk av for dette valget for å aktivere automatisk utligning for transaksjoner med denne posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="3c715-180">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="3c715-181">Hvis merket fjernes for dette valget, må du manuelt utligne transaksjoner ved hjelp av siden **Utlign åpne transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="3c715-181">If this option is cleared, you must manually settle transactions by using the **Settle open transactions** page.</span></span> |
| <span data-ttu-id="3c715-182">**Avbryt**</span><span class="sxs-lookup"><span data-stu-id="3c715-182">**Cancel**</span></span>     | <span data-ttu-id="3c715-183">Merk av for dette valget hvis du ønsker å ha muligheten til å avbryte transaksjoner med denne posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="3c715-183">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="3c715-184">**Lukke**</span><span class="sxs-lookup"><span data-stu-id="3c715-184">**Close**</span></span>      | <span data-ttu-id="3c715-185">Velg en posteringsprofil som du vil bytte til når transaksjoner med denne posteringsprofilen er lukket.</span><span class="sxs-lookup"><span data-stu-id="3c715-185">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="3c715-186">En transaksjon anses som lukket når den er fullstendig utlignet.</span><span class="sxs-lookup"><span data-stu-id="3c715-186">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |
