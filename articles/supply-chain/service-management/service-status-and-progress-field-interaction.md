---
title: Servicestatus og fremdriftsfeltinteraksjon
description: I Serviceordrer-skjemaet viser Fremdrift-feltet på serviceordrehodet statusen til hele serviceordren, og Status rapporterer statusen til individuelle serviceordrelinjer.
author: sorenva
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
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e83df9ca8ee19b5e29d4eccf2bd883ee6ddff62
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677653"
---
# <a name="service-status-and-progress-field-interaction"></a>Servicestatus og fremdriftsfeltinteraksjon

[!include [banner](../includes/banner.md)]

I **Serviceordrer**-skjemaet viser **Fremdrift**-feltet på serviceordrehodet statusen til hele serviceordren, og **Status** rapporterer statusen til individuelle serviceordrelinjer.

<table>
<colgroup>
<col />
<col />
<col />
<col />
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
