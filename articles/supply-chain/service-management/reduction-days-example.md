---
title: Reduksjonsdager – eksempel
description: Reduksjonsdager – eksempel.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87c46cd7ee7410e1c7cb88868cd19f5075482f8c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975662"
---
# <a name="reduction-days-example"></a>Reduksjonsdager – eksempel 

[!include [banner](../includes/banner.md)]


Du har opprettet en abonnementstransaksjon for en kundes vedlikeholdsabonnement som beskrevet i følgende tabell.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fra dato</p></th>
<th><p>Til dato</p></th>
<th><p>Abonnement</p></th>
<th><p>Abonnementstype</p></th>
<th><p>Project</p></th>
<th><p>Kategori</p></th>
<th><p>Salgsvaluta</p></th>
<th><p>Salgspris</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>01. mars 2011</p></td>
<td><p>31. mars 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Vanlig</strong></p></td>
<td><p>9013</p></td>
<td><p>SubCat2</p></td>
<td><p>EUR</p></td>
<td><p>200,00</p></td>
</tr>
</tbody>
</table>


Kunden rapporterer at det ikke behov for service to dager (10. og 11. mars). Dere avtaler å trekke fra disse to dagene på abonnementet.

Du oppretter en ny transaksjon av typen **Reduksjonsdager** som beskrevet i følgende tabell.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fra dato</p></th>
<th><p>Til dato</p></th>
<th><p>Abonnement</p></th>
<th><p>Abonnementstype</p></th>
<th><p>Project</p></th>
<th><p>Kategori</p></th>
<th><p>Salgsvaluta</p></th>
<th><p>Salgspris</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>10. mars 2011</p></td>
<td><p>11. mars 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Reduksjonsdager</strong></p></td>
<td><p>9013</p></td>
<td><p>SubCat2</p></td>
<td><p>EUR</p></td>
<td><p>-12,90</p></td>
</tr>
</tbody>
</table>


Når transaksjonene for mars 2011 blir fakturert, blir salgsprisen på EUR 200 redusert med EUR 12,90. Det fakturerbare beløpet for abonnementstransaksjonen er derfor EUR 187,10, og to transaksjoner faktureres for totalt EUR 187,10.

## <a name="see-also"></a>Se også

[Redusere dagene på abonnementsgebyr](reduce-the-days-on-subscription-fees.md)

  


