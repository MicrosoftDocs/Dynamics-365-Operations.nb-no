---
title: "Standard motkontoer for leverandørfakturajournaler og fakturagodkjenningsjournaler"
description: "Dette emnet hjelper deg med å bestemme hvor du vil tilordne standardkontoer for fakturajournaler."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 45a066ff5b884e8cc78b0fc16d1f1eab9cb0f5f3
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="30099-103">Standard motkontoer for leverandørfakturajournaler og fakturagodkjenningsjournaler</span><span class="sxs-lookup"><span data-stu-id="30099-103">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30099-104">Standard motkontoer brukes på følgende sider for leverandørfakturajournaler:</span><span class="sxs-lookup"><span data-stu-id="30099-104">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="30099-105">Fakturajournal</span><span class="sxs-lookup"><span data-stu-id="30099-105">Invoice journal</span></span>
-   <span data-ttu-id="30099-106">Fakturagodkjenningsjournal</span><span class="sxs-lookup"><span data-stu-id="30099-106">Invoice approval journal</span></span>

<span data-ttu-id="30099-107">Bruk tabellen nedenfor for å bestemme hvor du vil tilordne standardkontoer for fakturajournaler.</span><span class="sxs-lookup"><span data-stu-id="30099-107">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30099-108">Definer standardkontoer her</span><span class="sxs-lookup"><span data-stu-id="30099-108">Set up default accounts here</span></span></th>
<th><span data-ttu-id="30099-109">Der standardkontoer er angitt</span><span class="sxs-lookup"><span data-stu-id="30099-109">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="30099-110">Hvordan dette alternativet påvirker behandling</span><span class="sxs-lookup"><span data-stu-id="30099-110">How this option affects processing</span></span></th>
<th><span data-ttu-id="30099-111">Når du bør bruke dette alternativet</span><span class="sxs-lookup"><span data-stu-id="30099-111">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30099-112"><strong>Leverandørgruppe</strong> – Definer standard motkontoer for leverandørgrupper på siden <strong>Standard kontooppsett</strong> som du kan åpne fra <strong>Leverandørgrupper</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="30099-112"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="30099-113">Leverandørnummer</span><span class="sxs-lookup"><span data-stu-id="30099-113">Vendor account</span></span></li>
<li><span data-ttu-id="30099-114">Journaloppføringer for leverandørkontoer i leverandørgruppen, hvis standardkontoer ikke er angitt for leverandørkontoer</span><span class="sxs-lookup"><span data-stu-id="30099-114">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="30099-115">Standard motkontoer for leverandørgrupper vises som standard motkontoer for leverandører på siden <strong>Standard kontooppsett</strong>.</span><span class="sxs-lookup"><span data-stu-id="30099-115">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="30099-116">Du kan åpne denne siden fra <strong>Alle leverandører</strong>-listesiden.</span><span class="sxs-lookup"><span data-stu-id="30099-116">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="30099-117">Bruk dette alternativet hvis du vanligvis betaler for samme type ting fra de samme leverandørgruppene over tid.</span><span class="sxs-lookup"><span data-stu-id="30099-117">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30099-118"><strong>Leverandørkonto</strong> – Definer standardkontoer for leverandørkontoer på siden <strong>Standard kontooppsett</strong> som du kan åpne fra <strong>Leverandører</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="30099-118"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="30099-119">Journaloppføringer for leverandørkontoen</span><span class="sxs-lookup"><span data-stu-id="30099-119">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="30099-120">Standardmotkontoene for leverandørkontoer vises som standardmotkontoer for journaloppføringer for leverandørkontoen.</span><span class="sxs-lookup"><span data-stu-id="30099-120">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="30099-121">Bruk dette alternativet hvis du vanligvis betaler for samme type ting fra de samme leverandørene over tid.</span><span class="sxs-lookup"><span data-stu-id="30099-121">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30099-122"><strong>Journalnavn</strong> – Definer standard motkontoer for journaler på <strong>Journalnavn</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="30099-122"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="30099-123">Velg alternativet <strong>Fast motkonto</strong>.</span><span class="sxs-lookup"><span data-stu-id="30099-123">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="30099-124">Legg merke til at du ikke kan angi standard motkontoer for journalnavn hvis journaltypen for journalnavnene er <strong>Ankomstregistrering</strong> eller <strong>Godkjenning</strong>.</span><span class="sxs-lookup"><span data-stu-id="30099-124">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="30099-125">Journalhode som bruker journalnavnet</span><span class="sxs-lookup"><span data-stu-id="30099-125">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="30099-126">Journaloppføringer i journaler som bruker journalnavnet</span><span class="sxs-lookup"><span data-stu-id="30099-126">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="30099-127">Hvis det er merket av for <strong>Fast motkonto</strong> på siden <strong>Journalnavn</strong>, overstyrer motkontoen for journalnavnet standard motkonto for leverandøren eller leverandørgruppen.</span><span class="sxs-lookup"><span data-stu-id="30099-127">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="30099-128">Bruk dette alternativet for å definere journaler for bestemte kostnader og utgifter som belastes bestemte kontoer, uavhengig av hvilken leverandør eller leverandørgruppe leverandøren er del av.</span><span class="sxs-lookup"><span data-stu-id="30099-128">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30099-129"><strong>Journalnavn</strong> – Definer standard motkontoer for journaler på <strong>Journalnavn</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="30099-129"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="30099-130">Fjern avmerkingen for <strong>Fast motkonto</strong>.</span><span class="sxs-lookup"><span data-stu-id="30099-130">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="30099-131">Legg merke til at du ikke kan angi standard motkontoer for journalnavn hvis journaltypen for journalnavnene er <strong>Ankomstregistrering</strong> eller <strong>Godkjenning</strong>.</span><span class="sxs-lookup"><span data-stu-id="30099-131">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="30099-132">Journalhode</span><span class="sxs-lookup"><span data-stu-id="30099-132">Journal header</span></span></li>
<li><span data-ttu-id="30099-133">Journaloppføringer i journaler som bruker journalnavnet</span><span class="sxs-lookup"><span data-stu-id="30099-133">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="30099-134">Disse standardoppføringene brukes på journalhodesider, og motkontoen på journalhodesiden brukes som en standardoppføring på journalbilagssidene.</span><span class="sxs-lookup"><span data-stu-id="30099-134">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="30099-135">Standardkontoer fra <strong>Journalnavn</strong>-siden brukes bare hvis det ikke er konfigurert standardkontoer for leverandørkontoen.</span><span class="sxs-lookup"><span data-stu-id="30099-135">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="30099-136">Bruk dette alternativet for å definere standardkontoer som skal brukes når det ikke er tilordnet en standard motkonto for leverandøren.</span><span class="sxs-lookup"><span data-stu-id="30099-136">Use this option to set up default accounts that are used when a default vendor offset account isn&#39;t assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30099-137"><strong>Journalhode</strong> – Definer en standard motkonto for en journal som en standardoppføring på journalbilagssidene.</span><span class="sxs-lookup"><span data-stu-id="30099-137"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="30099-138">Legg merke til at du ikke kan angi standard motkontoer på journalhodet hvis journaltypen for journalnavnene er <strong>Ankomstregistrering</strong> eller <strong>Godkjenning</strong>.</span><span class="sxs-lookup"><span data-stu-id="30099-138">Note that you can&#39;t specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="30099-139">Journaloppføringer i journalen</span><span class="sxs-lookup"><span data-stu-id="30099-139">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="30099-140">Standardmotkontoen for en journal brukes som standardoppføring på journalbilagssidene.</span><span class="sxs-lookup"><span data-stu-id="30099-140">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="30099-141">Bruk dette alternativet for å få raskere dataregistrering hvis de fleste poster i en journal har samme motkontoen.</span><span class="sxs-lookup"><span data-stu-id="30099-141">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>






