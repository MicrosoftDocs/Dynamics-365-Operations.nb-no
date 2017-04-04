---
title: Lager objektverdier
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

# <a name="inventory-object-values"></a>Lager objektverdier

Denne artikkelen inneholder informasjon om hvordan verdiene for et beholdningsobjekt beregnes. 

En ny funksjon som heter ** fysisk antall ** kan du se verdiene for et bestemt lager-objekt. Et kostnadsobjekt representerer enhetsnivået der lagerregnskapet gjøres. Hvis du vil ha mer informasjon om kostnadsobjekter, kan du se [Kostnadsobjekter](cost-object.md). Hvis du vil se verdiene for et bestemt lager-objekt, klikker du **fysisk antall** på den **kostobjekt** siden. Her er hvordan verdien av et objekt på lager beregnes: Inventory-objektet. Verdi = kostnader-objekt. Gjennomsnittlig enhetskost × Inventory-objektet. Antallet i følgende eksempel viser hvordan verdiene for et lager-objekt og et objekt med kostnaden beregnes. To produktkvitteringshendelser er registrert for vare A:

-   Produktkvittering 1: antall = 100 PCer., beløp = $1,000.00, området = 1, lager = 11, satsvis Nr. = B1
-   Produktkvittering 2: antall = 50 PCer., beløp = $800.00, området = 1, lager = 11, satsvis Nr. = B2

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

[Cost objects](cost-object.md)

[Cost entries](cost-entries.md)

[Hva er nye og endrede i Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)


