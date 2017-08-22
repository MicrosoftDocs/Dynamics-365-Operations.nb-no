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
ms.author: Shiva.Pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4691ac4456b08084bcd93f7a8447719a15299c93
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a>Standard motkontoer for leverandørfakturajournaler og fakturagodkjenningsjournaler

[!include[banner](../includes/banner.md)]




Standard motkontoer brukes på følgende sider for leverandørfakturajournaler:

-   Fakturajournal
-   Fakturagodkjenningsjournal

Bruk tabellen nedenfor for å bestemme hvor du vil tilordne standardkontoer for fakturajournaler.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Definer standardkontoer her</th>
<th>Der standardkontoer er angitt</th>
<th>Hvordan dette alternativet påvirker behandling</th>
<th>Når du bør bruke dette alternativet</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Leverandørgruppe</strong> – Definer standard motkontoer for leverandørgrupper på siden <strong>Standard kontooppsett</strong> som du kan åpne fra <strong>Leverandørgrupper</strong>-siden.</td>
<td><ul>
<li>Leverandørnummer</li>
<li>Journaloppføringer for leverandørkontoer i leverandørgruppen, hvis standardkontoer ikke er angitt for leverandørkontoer</li>
</ul></td>
<td>Standard motkontoer for leverandørgrupper vises som standard motkontoer for leverandører på siden <strong>Standard kontooppsett</strong>. Du kan åpne denne siden fra <strong>Alle leverandører</strong>-listesiden.</td>
<td>Bruk dette alternativet hvis du vanligvis betaler for samme type ting fra de samme leverandørgruppene over tid.</td>
</tr>
<tr class="even">
<td><strong>Leverandørkonto</strong> – Definer standardkontoer for leverandørkontoer på siden <strong>Standard kontooppsett</strong> som du kan åpne fra <strong>Leverandører</strong>-siden.</td>
<td>Journaloppføringer for leverandørkontoen</td>
<td>Standardmotkontoene for leverandørkontoer vises som standardmotkontoer for journaloppføringer for leverandørkontoen.</td>
<td>Bruk dette alternativet hvis du vanligvis betaler for samme type ting fra de samme leverandørene over tid.</td>
</tr>
<tr class="odd">
<td><strong>Journalnavn</strong> – Definer standard motkontoer for journaler på <strong>Journalnavn</strong>-siden. Velg alternativet <strong>Fast motkonto</strong>. Legg merke til at du ikke kan angi standard motkontoer for journalnavn hvis journaltypen for journalnavnene er <strong>Ankomstregistrering</strong> eller <strong>Godkjenning</strong>.</td>
<td><ul>
<li>Journalhode som bruker journalnavnet</li>
<li>Journaloppføringer i journaler som bruker journalnavnet</li>
</ul></td>
<td>Hvis det er merket av for <strong>Fast motkonto</strong> på siden <strong>Journalnavn</strong>, overstyrer motkontoen for journalnavnet standard motkonto for leverandøren eller leverandørgruppen.</td>
<td>Bruk dette alternativet for å definere journaler for bestemte kostnader og utgifter som belastes bestemte kontoer, uavhengig av hvilken leverandør eller leverandørgruppe leverandøren er del av.</td>
</tr>
<tr class="even">
<td><strong>Journalnavn</strong> – Definer standard motkontoer for journaler på <strong>Journalnavn</strong>-siden. Fjern avmerkingen for <strong>Fast motkonto</strong>. Legg merke til at du ikke kan angi standard motkontoer for journalnavn hvis journaltypen for journalnavnene er <strong>Ankomstregistrering</strong> eller <strong>Godkjenning</strong>.</td>
<td><ul>
<li>Journalhode</li>
<li>Journaloppføringer i journaler som bruker journalnavnet</li>
</ul></td>
<td>Disse standardoppføringene brukes på journalhodesider, og motkontoen på journalhodesiden brukes som en standardoppføring på journalbilagssidene. Standardkontoer fra <strong>Journalnavn</strong>-siden brukes bare hvis det ikke er konfigurert standardkontoer for leverandørkontoen.</td>
<td>Bruk dette alternativet for å definere standardkontoer som skal brukes når det ikke er tilordnet en standard motkonto for leverandøren.</td>
</tr>
<tr class="odd">
<td><strong>Journalhode</strong> – Definer en standard motkonto for en journal som en standardoppføring på journalbilagssidene. Legg merke til at du ikke kan angi standard motkontoer på journalhodet hvis journaltypen for journalnavnene er <strong>Ankomstregistrering</strong> eller <strong>Godkjenning</strong>.</td>
<td>Journaloppføringer i journalen</td>
<td>Standardmotkontoen for en journal brukes som standardoppføring på journalbilagssidene.</td>
<td>Bruk dette alternativet for å få raskere dataregistrering hvis de fleste poster i en journal har samme motkontoen.</td>
</tr>
</tbody>
</table>






