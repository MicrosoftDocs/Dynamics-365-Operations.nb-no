---
title: Servicestatus og fremdriftsfeltinteraksjon
description: I Serviceordrer-skjemaet viser Fremdrift-feltet på serviceordrehodet statusen til hele serviceordren, og Status rapporterer statusen til individuelle serviceordrelinjer.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a767f4fddb79e720e5466791e984025de16a932a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824468"
---
# <a name="service-status-and-progress-field-interaction"></a>Servicestatus og fremdriftsfeltinteraksjon 

[!include [banner](../includes/banner.md)]


I **Serviceordrer**-skjemaet viser **Fremdrift**-feltet på serviceordrehodet statusen til hele serviceordren, og **Status** rapporterer statusen til individuelle serviceordrelinjer.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fremdrift</p></th>
<th><p>Status for linje 1</p></th>
<th><p>Status for linje 2</p></th>
<th><p>Status for linje 3</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Pågår</strong></p></td>
<td><p><strong>Opprettet</strong></p></td>
<td><p><strong>Opprettet</strong></p></td>
<td><p><strong>Opprettet</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Pågår</strong></p></td>
<td><p><strong>Avbrutt</strong></p></td>
<td><p><strong>Opprettet</strong></p></td>
<td><p><strong>Opprettet</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Pågår</strong></p></td>
<td><p><strong>Opprettet</strong></p></td>
<td><p><strong>Avbrutt</strong></p></td>
<td><p><strong>Postert</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Avbrutt</strong></p></td>
<td><p><strong>Avbrutt</strong></p></td>
<td><p><strong>Avbrutt</strong></p></td>
<td><p><strong>Avbrutt</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Postert</strong></p></td>
<td><p><strong>Postert</strong></p></td>
<td><p><strong>Postert</strong></p></td>
<td><p><strong>Postert</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Postert</strong></p></td>
<td><p><strong>Postert</strong></p></td>
<td><p><strong>Avbrutt</strong></p></td>
<td><p><strong>Avbrutt</strong></p></td>
</tr>
</tbody>
</table>


Fremdriften til en serviceordre er i gang hvis alle linjer har statusen **Created**. Den er fremdeles i gang hvis noen har linjene har statusen **Annullert** eller **Postert**.

Hvis alle linjer i en serviceordre er merket som **Postert**, er fremdriften til statusordren **Postert** . Hvis noen linjer er **Postert** og noen er **Annullert**, er fremdriften fremdeles **Postert**.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]