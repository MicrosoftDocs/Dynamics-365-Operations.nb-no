---
title: Overvåkingspolicyregler
description: Du kan bruke overvåkingspolicyer for å evaluere reiseregninger, leverandørfakturaer og bestillinger for å være sikker på at de samsvarer med policyregler du oppretter. Alle reglene som er knyttet til en overvåkingspolicy, kjøres i satsvis modus i henhold til en tidsplan du angir.  Hver policyregel er en forekomst av en policyregeltype. For hver policyregeltype kan bare én policyregel være aktiv om gangen.
author: panolte
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbf93f5b8b2f8d95102a52178b096d7e334894483c0ac0bacc62653aea845022
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744312"
---
# <a name="audit-policy-rules"></a>Overvåkingspolicyregler

[!include [banner](../includes/banner.md)]

Du kan bruke overvåkingspolicyer for å evaluere reiseregninger, leverandørfakturaer og bestillinger for å være sikker på at de samsvarer med policyregler du oppretter. Alle reglene som er knyttet til en overvåkingspolicy, kjøres i satsvis modus i henhold til en tidsplan du angir.  Hver policyregel er en forekomst av en policyregeltype. For hver policyregeltype kan bare én policyregel være aktiv om gangen. 

## <a name="queries-and-query-types"></a>Spørringer og spørringstyper

Når du oppretter en overvåkingspolicyregel, velger du først en policyregeltype. Policyregeltypen angir applikasjonsobjekttre (AOT)-spørringen som skal brukes som utgangpunkt for å opprette policyregelen. Det angir også hvilken spørringstype som skal brukes for policyregelen. Spørringen bestemmer kildedokumentet som policyregelen evaluerer. Det angir også feltene du velger i kildedokumentet, som identifiserer den juridiske enheten og datoen som skal brukes når dokumenter velges for overvåking. Spørringstypen styrer standardfeltene på spørringssiden og siden Overvåkingspolicyregel. Tabellen nedenfor viser de spørringstypene som er tilgjengelige for overvåkingspolicyregler.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Spørringstype</th>
<th>Formål</th>
<th>Mer informasjon</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Betinget</td>
<td>Evaluere kildedokumentattributter mot angitte verdier.</td>
<td></td>
</tr>
<tr class="even">
<td>Aggreger</td>
<td>Evaluere flere kildedokumenter eller kildedokumentlinjer mot en policyregel ved å aggregere numeriske verdier.</td>
<td></td>
</tr>
<tr class="odd">
<td>Prøve</td>
<td>Velg tilfeldig en angitt prosent av kildedokumentene som skal evalueres med hensyn til policybrudd.</td>
<td>Når du velger dette alternativet, bruker du siden Overvåkingspolicyregel til å angi prosentandelen av dokumenter som skal velges vilkårlig for overvåking.</td>
</tr>
<tr class="even">
<td>Duplikat</td>
<td>Evaluere kildedokumenter for å avgjøre om de inneholder duplikatoppføringer i angitte felt.</td>
<td>Når du velger dette alternativet, bruker du siden Overvåkingspolicyregel til å angi hvor mange dager som skal legges til ved starten av datoområdet for dokumentvalg når dokumenter evalueres for duplikatoppføringer.</td>
</tr>
<tr class="odd">
<td>Listesøk</td>
<td>Evaluere kildedokumenter for bestemte entiteter.</td>
<td>Rotdokumentet for spørringen definerer dokumentet som overvåkes. Spørringen må være en listespørring som inneholder en referanse til tabellen DirPartyTable. Dette alternativet kan bare brukes med følgende AOT-spørringer:
<ul>
<li><span class="ui">AuditPolicyExpenseList</span> (Overvåkede ansatte i utgiftsrapport)</li>
<li><span class="ui">AuditPolicyPurchList</span> (Overvåkede leverandører i bestilling)</li>
<li><span class="ui">AuditPolicyVendInvoiceList</span> (Overvåkede leverandører i leverandørfaktura)</li>
</ul>
Når du velger dette alternativet, angir du de overvåkede enhetene i på siden Overvåkingspolicyregel.</td>
</tr>
<tr class="even">
<td>Nøkkelordsøk</td>
<td>Evaluere kildedokumenter for å avgjøre om de inneholder bestemte ord.</td>
<td>Når du velger dette alternativet, skriver du inn ordene du vil se etter på siden Overvåkingspolicyregel. Siden Overvåkingspolicyregel inneholder også alternativer som lar deg angi tabellene og feltene som skal evalueres for ordene du skrev inn.</td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a>Vanlige parametere
Alle policyreglene for en bestemt overvåkingspolicy deler de samme satsvise parameterne og det samme datoområdet for dokumentutvalget. Disse parameterne er angitt for policyen på Tilleggsalternativer-siden.



## <a name="additional-resources"></a>Tilleggsressurser

[Brudd på og saker for overvåkingspolicy](audit-policy-violations-cases.md)
[Definere overvåkingspolicyer for kildedokumenter](tasks/define-audit-policies-source-documents.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]