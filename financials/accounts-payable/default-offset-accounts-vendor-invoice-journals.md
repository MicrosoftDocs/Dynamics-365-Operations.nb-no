---
title: "Standard motkontoer for leverandørfakturajournaler og fakturagodkjenningsjournaler"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c2b62eafc71b5d1ad4eaaf252efd1dcbb97b86f3
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="4936a-102">Standard motkontoer for leverandørfakturajournaler og fakturagodkjenningsjournaler</span><span class="sxs-lookup"><span data-stu-id="4936a-102">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="4936a-103">Standard motkontoer brukes på følgende sider for leverandørfakturajournaler:</span><span class="sxs-lookup"><span data-stu-id="4936a-103">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="4936a-104">Fakturajournal</span><span class="sxs-lookup"><span data-stu-id="4936a-104">Invoice journal</span></span>
-   <span data-ttu-id="4936a-105">Fakturagodkjenningsjournal</span><span class="sxs-lookup"><span data-stu-id="4936a-105">Invoice approval journal</span></span>

<span data-ttu-id="4936a-106">Bruk tabellen nedenfor for å bestemme hvor du vil tilordne standardkontoer for fakturajournaler.</span><span class="sxs-lookup"><span data-stu-id="4936a-106">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4936a-107">Definer standardkontoer her</span><span class="sxs-lookup"><span data-stu-id="4936a-107">Set up default accounts here</span></span></th>
<th><span data-ttu-id="4936a-108">Der standardkontoer er angitt</span><span class="sxs-lookup"><span data-stu-id="4936a-108">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="4936a-109">Hvordan dette alternativet påvirker behandling</span><span class="sxs-lookup"><span data-stu-id="4936a-109">How this option affects processing</span></span></th>
<th><span data-ttu-id="4936a-110">Når du bør bruke dette alternativet</span><span class="sxs-lookup"><span data-stu-id="4936a-110">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4936a-111"><strong>Leverandørgruppe</strong> – Definer standard motkontoer for leverandørgrupper på siden <strong>Standard kontooppsett</strong> som du kan åpne fra <strong>Leverandørgrupper</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="4936a-111"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="4936a-112">Leverandørnummer</span><span class="sxs-lookup"><span data-stu-id="4936a-112">Vendor account</span></span></li>
<li><span data-ttu-id="4936a-113">Journaloppføringer for leverandørkontoer i leverandørgruppen, hvis standardkontoer ikke er angitt for leverandørkontoer</span><span class="sxs-lookup"><span data-stu-id="4936a-113">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="4936a-114">Standard motkontoer for leverandørgrupper vises som standard motkontoer for leverandører på siden <strong>Standard kontooppsett</strong>.</span><span class="sxs-lookup"><span data-stu-id="4936a-114">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="4936a-115">Du kan åpne denne siden fra <strong>Alle leverandører</strong>-listesiden.</span><span class="sxs-lookup"><span data-stu-id="4936a-115">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="4936a-116">Bruk dette alternativet hvis du vanligvis betaler for samme type ting fra de samme leverandørgruppene over tid.</span><span class="sxs-lookup"><span data-stu-id="4936a-116">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4936a-117"><strong>Leverandørkonto</strong> – Definer standardkontoer for leverandørkontoer på siden <strong>Standard kontooppsett</strong> som du kan åpne fra <strong>Leverandører</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="4936a-117"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="4936a-118">Journaloppføringer for leverandørkontoen</span><span class="sxs-lookup"><span data-stu-id="4936a-118">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="4936a-119">Standardmotkontoene for leverandørkontoer vises som standardmotkontoer for journaloppføringer for leverandørkontoen.</span><span class="sxs-lookup"><span data-stu-id="4936a-119">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="4936a-120">Bruk dette alternativet hvis du vanligvis betaler for samme type ting fra de samme leverandørene over tid.</span><span class="sxs-lookup"><span data-stu-id="4936a-120">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4936a-121"><strong>Journalnavn</strong> – Definer standard motkontoer for journaler på <strong>Journalnavn</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="4936a-121"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="4936a-122">Velg alternativet <strong>Fast motkonto</strong>.</span><span class="sxs-lookup"><span data-stu-id="4936a-122">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="4936a-123">Legg merke til at du ikke kan angi standard motkontoer for journalnavn hvis journaltypen for journalnavnene er <strong>Ankomstregistrering</strong> eller <strong>Godkjenning</strong>.</span><span class="sxs-lookup"><span data-stu-id="4936a-123">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="4936a-124">Journalhode som bruker journalnavnet</span><span class="sxs-lookup"><span data-stu-id="4936a-124">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="4936a-125">Journaloppføringer i journaler som bruker journalnavnet</span><span class="sxs-lookup"><span data-stu-id="4936a-125">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="4936a-126">Hvis det er merket av for <strong>Fast motkonto</strong> på siden <strong>Journalnavn</strong>, overstyrer motkontoen for journalnavnet standard motkonto for leverandøren eller leverandørgruppen.</span><span class="sxs-lookup"><span data-stu-id="4936a-126">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="4936a-127">Bruk dette alternativet for å definere journaler for bestemte kostnader og utgifter som belastes bestemte kontoer, uavhengig av hvilken leverandør eller leverandørgruppe leverandøren er del av.</span><span class="sxs-lookup"><span data-stu-id="4936a-127">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4936a-128"><strong>Journalnavn</strong> – Definer standard motkontoer for journaler på <strong>Journalnavn</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="4936a-128"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="4936a-129">Fjern avmerkingen for <strong>Fast motkonto</strong>.</span><span class="sxs-lookup"><span data-stu-id="4936a-129">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="4936a-130">Legg merke til at du ikke kan angi standard motkontoer for journalnavn hvis journaltypen for journalnavnene er <strong>Ankomstregistrering</strong> eller <strong>Godkjenning</strong>.</span><span class="sxs-lookup"><span data-stu-id="4936a-130">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="4936a-131">Journalhode</span><span class="sxs-lookup"><span data-stu-id="4936a-131">Journal header</span></span></li>
<li><span data-ttu-id="4936a-132">Journaloppføringer i journaler som bruker journalnavnet</span><span class="sxs-lookup"><span data-stu-id="4936a-132">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="4936a-133">Disse standardoppføringene brukes på journalhodesider, og motkontoen på journalhodesiden brukes som en standardoppføring på journalbilagssidene.</span><span class="sxs-lookup"><span data-stu-id="4936a-133">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="4936a-134">Standardkontoer fra <strong>Journalnavn</strong>-siden brukes bare hvis det ikke er konfigurert standardkontoer for leverandørkontoen.</span><span class="sxs-lookup"><span data-stu-id="4936a-134">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="4936a-135">Bruk dette alternativet for å definere standardkontoer som skal brukes når det ikke er tilordnet en standard motkonto for leverandøren.</span><span class="sxs-lookup"><span data-stu-id="4936a-135">Use this option to set up default accounts that are used when a default vendor offset account isn't assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4936a-136"><strong>Journalhode</strong> – Definer en standard motkonto for en journal som en standardoppføring på journalbilagssidene.</span><span class="sxs-lookup"><span data-stu-id="4936a-136"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="4936a-137">Legg merke til at du ikke kan angi standard motkontoer på journalhodet hvis journaltypen for journalnavnene er <strong>Ankomstregistrering</strong> eller <strong>Godkjenning</strong>.</span><span class="sxs-lookup"><span data-stu-id="4936a-137">Note that you can't specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="4936a-138">Journaloppføringer i journalen</span><span class="sxs-lookup"><span data-stu-id="4936a-138">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="4936a-139">Standardmotkontoen for en journal brukes som standardoppføring på journalbilagssidene.</span><span class="sxs-lookup"><span data-stu-id="4936a-139">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="4936a-140">Bruk dette alternativet for å få raskere dataregistrering hvis de fleste poster i en journal har samme motkontoen.</span><span class="sxs-lookup"><span data-stu-id="4936a-140">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>






