---
title: Beholdningsobjektverdier
description: Denne artikkelen inneholder informasjon om hvordan verdiene for et beholdningsobjekt beregnes.
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 09 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8898d5d91ffb4f73ea68f1251e1a99440e81bcd4
ms.lasthandoff: 03/29/2017


---

# <a name="inventory-object-values"></a>Beholdningsobjektverdier

Denne artikkelen inneholder informasjon om hvordan verdiene for et beholdningsobjekt beregnes. 

En ny funksjon kalt **fysisk antall** gjør at du kan se verdiene til et bestemt beholdningsobjekt. Et kostnadsobjekt representerer enhetsnivået der lagerregnskapet gjøres. Hvis du vil ha mer informasjon om kostnadsobjekter, kan du se [Kostnadsobjekter](cost-object.md). Hvis du vil se verdiene for et bestemt beholdningsobjekt, klikker du **Fysisk antall** på **Kostobjekt**-siden. Slik beregnes verdien til et beholdningsobjekt: beholdningsobjekt.verdi = kostnadsobjekt.gjennomsnittlig enhetskostnad × beholdningsobjekt.antall. Eksemplet nedenfor viser hvordan verdiene til et beholdningsobjekt og et kostnadsobjekt beregnes. To produktkvitteringshendelser er registrert for vare A:

-   Produktkvittering 1: Antall = 100 stk., Beløp = USD 1 000,00, Område = 1, Lager = 11, Partinr. = B1
-   Produktkvittering 2: Antall = 50 stk., Beløp = USD 800,00, Område = 1, Lager = 11, Partinr. = B2

Følgende tabell viser resultatet av beregningen for et kostnadsobjekt. Du kan vise resultatet på **Kostnadsobjekt**-siden.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th>Objekttype</th>
<th>Varenummer</th>
<th>Område</th>
<th>Antall</th>
<th>Lagerenhet</th>
<th>Verdi</th>
<th>Gjennomsnittlig enhetskostnad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kostnadsobjekt</td>
<td>A</td>
<td>1</td>
<td>150</td>
<td>Stk.</td>
<td><p>USD 1 800,00</p></td>
<td><p>USD 12,00</p></td>
</tr>
</tbody>
</table>

Følgende tabell viser resultatet av beregningen for et beholdningsobjekt. Du kan vise resultatet ved å klikke **Fysisk antall** på **Kostnadsobjekt**-siden.

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th>Objekttype</th>
<th>Varenummer</th>
<th>Område</th>
<th>Lager</th>
<th>Partinr.</th>
<th>Antall</th>
<th>Lagerenhet</th>
<th>Verdi</th>
<th>Gjennomsnittlig enhetskostnad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Beholdningsobjekt</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B1</td>
<td>100</td>
<td>Stk.</td>
<td><p>USD 1 200,00</p></td>
<td><p>USD 12,00</p></td>
</tr>
<tr class="even">
<td>Beholdningsobjekt</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B2</td>
<td>50</td>
<td>Stk.</td>
<td><p>USD 600,00</p></td>
<td><p>USD 12,00</p></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Se også
--------

[Kostnadsobjekter](cost-object.md)

[Kostnadsoppføringer](cost-entries.md)

[Hva er nytt og endret i Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)


