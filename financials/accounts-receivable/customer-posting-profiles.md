---
title: Kundeposteringsprofiler
description: "Kundeposteringsprofiler styrer postering av kundetransaksjoner til økonomimodulen."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3eeedc32bd9a07fbd0540111cca304ed36bcd4f2
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="customer-posting-profiles"></a>Kundeposteringsprofiler

[!include[banner](../includes/banner.md)]


Kundeposteringsprofiler styrer postering av kundetransaksjoner til økonomimodulen.

<a name="customer-posting-profiles"></a>Kundeposteringsprofiler
-------------------------

Kundeposteringsprofiler gjør det mulig å tilordne finanskontoer og dokumentinnstillingene til alle kunder, en kundegruppe eller en enkelt kunde. Disse innstillingene brukes når du oppretter salgsordrer, fritekstfakturaer, utbetalinger, purringer og rentenotaer. For noen transaksjoner kan du velge en posteringsprofil som er forskjellig fra og har forrang for posteringsprofilene som er definert for transaksjoner på denne siden. 

Standard posteringsprofil er definert i hurtigfanen Finans og merverdiavgift på siden Kundeparametere. Standardposteringsprofilen inkluderes deretter automatisk i hodet på nye dokumenter, der du kan endre den til en annen posteringsprofil om nødvendig.

Du kan også knytte posteringsdefinisjoner til transaksjonsposteringstyper på siden Definisjoner for transaksjonspostering. Posteringsdefinisjoner styrer posteringen av kundetransaksjoner til økonomimodulen i stedet for posteringsprofiler.

## <a name="creating-a-posting-profile"></a>Opprette en posteringsprofil
Angi finanskontoene som brukes ved posteringen av transaksjoner som bruker den valgte posteringsprofilen. Velg en kontokode og, hvis mulig, et konto- eller gruppenummer for den valgte posteringsprofilen. Under posteringsprosessen hentes den mest korrekte posteringsprofilen for hver transaksjon ved å søke etter den mest spesifikke kontokoden, gruppenummeret eller kombinasjonen gruppe og nummer etter følgende prioritering:

| **Kontokode**-feltverdi | **Konto/gruppenummer**-feltverdi            | Søkeprioritet |
|------------------------------|-------------------------------------------------|-----------------|
| **Tabell**                    | Spesifikk kundekonto                       | 1               |
| **Gruppe**                    | Kundegruppe som tilordnes kunden | 2               |
| **Alle**                      | Tom                                           | 3               |

Hvis du vil ha samme posteringsprofil for alle kundetransaksjoner, definerer du bare én posteringsprofil med Alle i Kontokode-feltet. Angi følgende verdier for å definere posteringsprofilen:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Felt</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Posteringsprofil</strong></td>
<td>Angi en kode for posteringsprofilen. Du kan for eksempel opprette to posteringsprofiler for å hente én konto for kundesaldoer i den nasjonale valutaen og en annen for kundesaldoer i en utenlandsk valuta. Du kan kalle den ene kontoen Nasjonal og den andre Utenlandsk.</td>
</tr>
<tr class="even">
<td><strong>Beskrivelse</strong></td>
<td>Angi en beskrivelse av posteringsprofilen. Dette brukes bare til å identifisere posteringsprofilen mer nøyaktig når du viser den på denne siden.</td>
</tr>
<tr class="odd">
<td><strong>Kontokode</strong></td>
<td>Angi om posteringsprofilen gjelder en enkeltkunde, en gruppe kunder eller alle kunder:
<ul>
<li><strong>Tabell</strong> – Posteringsprofilen gjelder for en enkelt kunde. Velg kundekontoen i feltet Konto/gruppenummer.</li>
<li><strong>Gruppe</strong> – Posteringsprofilen gjelder for en kundegruppe. Velg kundegruppen i feltet Konto/gruppenummer.</li>
<li><strong>Alle</strong> – Posteringsprofilen gjelder for alle kunder. La feltet Konto/gruppenummer stå tomt.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Konto/gruppenummer</strong></td>
<td>Hvis Tabell velges i feltet Kontokode, velger du kontonummeret til kunden som er knyttet til posteringsprofilen. Hvis Gruppe er valgt, velger du kundegruppen. Hvis Alle er valgt, lar du feltet stå tomt.</td>
</tr>
<tr class="odd">
<td><strong>Samlekonto</strong></td>
<td>Velg finanskontoen som skal brukes som kundesamlekonto for kunder som er knyttet til posteringsprofilen.</td>
</tr>
<tr class="even">
<td><strong>Utligningskonto</strong></td>
<td>Velg likviditetsfinanskontoen som brukes for kontantstrømprognoser. Dette feltet vises bare hvis kontantstrømprognoser er aktivert.</td>
</tr>
<tr class="odd">
<td><strong>Mva-forskuddsbetalinger</strong></td>
<td>Velg kontoen for merverdiavgift for forskuddsbetalte betalinger.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Obs!</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bruk siden Kundeparametere for å angi posteringsprofilen som skal brukes når en betaling er merket som en forskuddsbetaling.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Konto for rabattavsetning</strong></td>
<td>Velg finanskontoen for diskontoforpliktelser.</td>
</tr>
<tr class="odd">
<td><strong>Purreforløp</strong></td>
<td>Velg identifikatoren for purreforløpet som skal brukes for kunder som er tilordnet posteringsprofilen.</td>
</tr>
<tr class="even">
<td><strong>Rentekode</strong></td>
<td>Velg rentekoden som skal brukes for beregning av rente for kunder som er tilordnet posteringsprofilen.</td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a>**Tabellrestriksjoner**

For transaksjoner med den valgte posteringsprofilen kan du angi om transaksjonene skal utlignes automatisk, om rente skal beregnes, og om purringer blir utstedt. Du kan også velge kontoen som brukes når transaksjoner med den valgte posteringsprofilen er lukket.

Angi følgende verdier for å definere posteringsprofilen:

| Felt                 | Beskrivelse                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Utligning**        | Merk av for dette valget for å aktivere automatisk utligning for transaksjoner med denne posteringsprofilen. Hvis merket fjernes for dette valget
, må du manuelt utligne transaksjoner ved hjelp av Utlign åpne transaksjoner-siden eller Angi kundebetalinger-siden. |
| **Rente**          | Merk av for dette valget hvis rente skal beregnes på utestående saldoer for kundekontoer som bruker denne profilen. Hvis merket fjernes for dette valget, vil det ikke beregnes renter for disse kundene.                                           |
| **Purring** | Merk av for dette valget hvis purrebrev skal genereres for kundekontoer som bruker denne profilen. Hvis merket fjernes for dette valget, vil det ikke genereres purrebrev for disse kundene.                                                 |
| **Lukke**             | Velg en posteringsprofil som du vil bytte til når transaksjoner med denne posteringsprofilen er lukket. En transaksjon anses som lukket når den er fullstendig utlignet.                                                                           |






