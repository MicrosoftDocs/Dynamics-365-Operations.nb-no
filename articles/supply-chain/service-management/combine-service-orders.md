---
title: Kombiner serviceordrer
description: Du kan kombinere serviceordrer.
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
ms.openlocfilehash: f89c60561746ac9f1c2e9d611089bfac69089081
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676782"
---
# <a name="combine-service-orders"></a>Kombiner serviceordrer   

[!include [banner](../includes/banner.md)]


Når du oppretter serviceordrelinjer automatisk i **Serviceavtaler**-skjemaet, kan du velge ett av følgende alternativer for å angi hvordan du vil gruppere dem:

  - **Etter serviceavtale**

  - **Etter servicoppgave**

  - **Etter ansatt**

  - **Etter serviceobjekt**

## <a name="example"></a>Eksempel

Du kan opprette en serviceavtale med startdatoen 31. mars 2007. I **Kombiner serviceordrer**-feltet angir du **Etter serviceobjekt**. Deretter oppretter du følgende serviceavtalelinjer:

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Avtalelinjenummer</p></th>
<th><p>transaksjonstype</p></th>
<th><p>beskrivelse</p></th>
<th><p>Intervall</p></th>
<th><p>Serviceobjekt</p></th>
<th><p>Startdato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p><strong>Time</strong></p></td>
<td><p>SAL1</p></td>
<td><p>Ukentlig</p></td>
<td><p>X-1</p></td>
<td><p>01.04.2007</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p><strong>Time</strong></p></td>
<td><p>SAL2</p></td>
<td><p>Annenhver uke</p></td>
<td><p>X-2</p></td>
<td><p>01.04.2007</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p><strong>Time</strong></p></td>
<td><p>SAL3</p></td>
<td><p>Ukentlig</p></td>
<td><p>X-2</p></td>
<td><p>01.04.2007</p></td>
</tr>
</tbody>
</table>


Du angir ikke tidsvinduer for noen av serviceavtalelinjene. Dermed flyttes ikke serviceordrelinjene fra den beregnede datoen de faller på.

Deretter genererer du serviceordrelinjer fra skjemaet **Opprett serviceordrer** fra 01.04.07 til 30.04.07.

Totalt sett opprettes det ti serviceordrer. Fordi du valgte kombinasjonsinnstillingen **Etter serviceobjekt**, får alle serviceordrer som opprettes, bare serviceordrelinjer med ett bestemt serviceobjekt. Serviceordrelinjer som genereres fra serviceavtalen og har samme servicedato og samme objekt, kombineres på samme serviceordre.


> [!NOTE]
> <P>I dette eksemplet har kalenderen som er angitt i skjemaet <STRONG>Servicestyringsparametere</STRONG>, ingen lukkede dager.</P>



Serviceordrelinjene blir gruppert ytterligere i serviceordrer i henhold til eventuelle tidsvinduer som du angir i serviceavtalelinjene.

## <a name="see-also"></a>Se også

[Opprette serviceordrer automatisk](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]