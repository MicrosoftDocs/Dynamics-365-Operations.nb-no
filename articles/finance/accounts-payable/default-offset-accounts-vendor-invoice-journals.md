---
title: Standard motkontoer for leverandørfaktura- og fakturagodkjenningsjournaler
description: Dette emnet hjelper deg med å bestemme hvor du vil tilordne standardkontoer for fakturajournaler.
author: abruer
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e859d166d19cd97d4b19c989b7a1bbe6832d218b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820743"
---
# <a name="default-offset-accounts-for-vendor-invoice-and-invoice-approval-journals"></a><span data-ttu-id="e1dbb-103">Standard motkontoer for leverandørfaktura- og fakturagodkjenningsjournaler</span><span class="sxs-lookup"><span data-stu-id="e1dbb-103">Default offset accounts for vendor invoice and invoice approval journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1dbb-104">Standard motkontoer brukes på følgende sider for leverandørfakturajournaler:</span><span class="sxs-lookup"><span data-stu-id="e1dbb-104">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="e1dbb-105">Fakturajournal</span><span class="sxs-lookup"><span data-stu-id="e1dbb-105">Invoice journal</span></span>
-   <span data-ttu-id="e1dbb-106">Fakturagodkjenningsjournal</span><span class="sxs-lookup"><span data-stu-id="e1dbb-106">Invoice approval journal</span></span>

<span data-ttu-id="e1dbb-107">Bruk tabellen nedenfor for å bestemme hvor du vil tilordne standardkontoer for fakturajournaler.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-107">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1dbb-108">Definer standardkontoer her</span><span class="sxs-lookup"><span data-stu-id="e1dbb-108">Set up default accounts here</span></span></th>
<th><span data-ttu-id="e1dbb-109">Der standardkontoer er angitt</span><span class="sxs-lookup"><span data-stu-id="e1dbb-109">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="e1dbb-110">Hvordan dette alternativet påvirker behandling</span><span class="sxs-lookup"><span data-stu-id="e1dbb-110">How this option affects processing</span></span></th>
<th><span data-ttu-id="e1dbb-111">Når du bør bruke dette alternativet</span><span class="sxs-lookup"><span data-stu-id="e1dbb-111">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1dbb-112"><strong>Leverandørgruppe</strong> – Definer standard motkontoer for leverandørgrupper på siden <strong>Standard kontooppsett</strong> som du kan åpne fra <strong>Leverandørgrupper</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-112"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="e1dbb-113">Leverandørnummer</span><span class="sxs-lookup"><span data-stu-id="e1dbb-113">Vendor account</span></span></li>
<li><span data-ttu-id="e1dbb-114">Journaloppføringer for leverandørkontoer i leverandørgruppen, hvis standardkontoer ikke er angitt for leverandørkontoer</span><span class="sxs-lookup"><span data-stu-id="e1dbb-114">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="e1dbb-115">Standard motkontoer for leverandørgrupper vises som standard motkontoer for leverandører på siden <strong>Standard kontooppsett</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-115">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="e1dbb-116">Du kan åpne denne siden fra <strong>Alle leverandører</strong>-listesiden.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-116">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="e1dbb-117">Bruk dette alternativet hvis du vanligvis betaler for samme type ting fra de samme leverandørgruppene over tid.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-117">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1dbb-118"><strong>Leverandørkonto</strong> – Definer standardkontoer for leverandørkontoer på siden <strong>Standard kontooppsett</strong> som du kan åpne fra <strong>Leverandører</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-118"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="e1dbb-119">Journaloppføringer for leverandørkontoen</span><span class="sxs-lookup"><span data-stu-id="e1dbb-119">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="e1dbb-120">Standardmotkontoene for leverandørkontoer vises som standardmotkontoer for journaloppføringer for leverandørkontoen.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-120">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="e1dbb-121">Bruk dette alternativet hvis du vanligvis betaler for samme type ting fra de samme leverandørene over tid.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-121">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1dbb-122"><strong>Journalnavn</strong> – Definer standard motkontoer for journaler på <strong>Journalnavn</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-122"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="e1dbb-123">Velg alternativet <strong>Fast motkonto</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-123">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="e1dbb-124">Legg merke til at du ikke kan angi standard motkontoer for journalnavn hvis journaltypen for journalnavnene er <strong>Ankomstregistrering</strong> eller <strong>Godkjenning</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-124">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="e1dbb-125">Journalhode som bruker journalnavnet</span><span class="sxs-lookup"><span data-stu-id="e1dbb-125">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="e1dbb-126">Journaloppføringer i journaler som bruker journalnavnet</span><span class="sxs-lookup"><span data-stu-id="e1dbb-126">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="e1dbb-127">Hvis det er merket av for <strong>Fast motkonto</strong> på siden <strong>Journalnavn</strong>, overstyrer motkontoen for journalnavnet standard motkonto for leverandøren eller leverandørgruppen.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-127">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="e1dbb-128">Bruk dette alternativet for å definere journaler for bestemte kostnader og utgifter som belastes bestemte kontoer, uavhengig av hvilken leverandør eller leverandørgruppe leverandøren er del av.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-128">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1dbb-129"><strong>Journalnavn</strong> – Definer standard motkontoer for journaler på <strong>Journalnavn</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-129"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="e1dbb-130">Fjern avmerkingen for <strong>Fast motkonto</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-130">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="e1dbb-131">Legg merke til at du ikke kan angi standard motkontoer for journalnavn hvis journaltypen for journalnavnene er <strong>Ankomstregistrering</strong> eller <strong>Godkjenning</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-131">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="e1dbb-132">Journalhode</span><span class="sxs-lookup"><span data-stu-id="e1dbb-132">Journal header</span></span></li>
<li><span data-ttu-id="e1dbb-133">Journaloppføringer i journaler som bruker journalnavnet</span><span class="sxs-lookup"><span data-stu-id="e1dbb-133">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="e1dbb-134">Disse standardoppføringene brukes på journalhodesider, og motkontoen på journalhodesiden brukes som en standardoppføring på journalbilagssidene.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-134">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="e1dbb-135">Standardkontoer fra <strong>Journalnavn</strong>-siden brukes bare hvis det ikke er konfigurert standardkontoer for leverandørkontoen.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-135">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="e1dbb-136">Bruk dette alternativet for å definere standardkontoer som skal brukes når det ikke er tilordnet en standard motkonto for leverandøren.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-136">Use this option to set up default accounts that are used when a default vendor offset account isn&#39;t assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1dbb-137"><strong>Journalhode</strong> – Definer en standard motkonto for en journal som en standardoppføring på journalbilagssidene.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-137"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="e1dbb-138">Legg merke til at du ikke kan angi standard motkontoer på journalhodet hvis journaltypen for journalnavnene er <strong>Ankomstregistrering</strong> eller <strong>Godkjenning</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-138">Note that you can&#39;t specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="e1dbb-139">Journaloppføringer i journalen</span><span class="sxs-lookup"><span data-stu-id="e1dbb-139">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="e1dbb-140">Standardmotkontoen for en journal brukes som standardoppføring på journalbilagssidene.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-140">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="e1dbb-141">Bruk dette alternativet for å få raskere dataregistrering hvis de fleste poster i en journal har samme motkontoen.</span><span class="sxs-lookup"><span data-stu-id="e1dbb-141">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]