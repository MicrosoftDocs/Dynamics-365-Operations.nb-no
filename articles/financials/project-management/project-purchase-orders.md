---
title: Bestillinger for et prosjekt
description: "Denne artikkelen beskriver flere metoder du kan bruke til å opprette bestillinger for et prosjekt. Hvilken metode du bruker, er avhengig av formålet med bestillingen og når de innkjøpte varene forbrukes og belastes et prosjekt."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 45d28110ca93875eb534c69886ac2074ea4fe737
ms.openlocfilehash: d55c999ed1f506a2d9487c8cc94bf0e9cce3bed1
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2017

---

# <a name="purchase-orders-for-a-project"></a>Bestillinger for et prosjekt

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver flere metoder du kan bruke til å opprette bestillinger for et prosjekt. Hvilken metode du bruker, er avhengig av formålet med bestillingen og når de innkjøpte varene forbrukes og belastes et prosjekt.

Du kan bruke flere metoder til å opprette bestillinger for et prosjekt i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Hvilken metode du bruker, er avhengig av formålet med bestillingen, når de innkjøpte varene forbrukes, og når de innkjøpte varene skal belastes et prosjekt.

### <a name="methods-for-creating-a-purchase-order"></a>Metoder for å opprette en bestilling

Du kan bruke én av følgende metoder til å opprette en bestilling i prosjektstyring og regnskap. Formålet med bestillingen fastsetter når bestillingen skal forbrukes, og derfor når varene skal belastes et prosjekt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metode</th>
<th>Formål</th>
<th>Forbruk av varer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Opprett en bestilling direkte fra et prosjekt.</td>
<td>Bruk denne metoden for å kjøpe varer fra en ekstern leverandør til forbruk på et prosjekt. Du kan opprette bestillingen på to måter:
<ul>
<li>Fra selve prosjektet. I dette tilfellet er prosjekt allerede definert for bestillingen.</li>
<li>Ved å navigere til prosjektbestillingen. Du må velge både leverandøren og prosjektet som bestillingen skal opprettes for.</li>
</ul></td>
<td>Varene forbrukes når leverandørfakturaen oppdateres.</td>
</tr>
<tr class="even">
<td>Opprett en bestilling fra en salgsordre.</td>
<td>Bruk denne metoden til å kjøpe varer når du oppretter en salgsordre fra et prosjekt.</td>
<td>Varene forbrukes når salgsordren faktureres kunden.</td>
</tr>
<tr class="odd">
<td>Opprett en bestilling fra et varebehov.</td>
<td>Bruk denne metoden til å kjøpe varer når du oppretter et varebehov fra et prosjekt.</td>
<td>Varene forbrukes når følgeseddelen for varebehov oppdateres.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Når du oppdaterer leverandørfakturaen eller følgeseddelen, blir du bedt om å oppdatere følgeseddelen for varebehovet.

Hvis du vil ha mer informasjon, se [Motta varer i bestilling fra varebehov](tasks/receive-items-purchase-order-item-requirement.md).

