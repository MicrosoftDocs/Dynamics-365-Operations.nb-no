---
title: Kundeposteringsprofiler
description: Dette emnet beskriver kundeposteringsprofilser, som styrer posteringen av kundetransaksjoner til økonomimodulen.
author: JodiChristiansen
ms.date: 12/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ed5ab24e37c75222080bd242aa72a39ecb476bf
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734639"
---
# <a name="customer-posting-profiles"></a>Kundeposteringsprofiler

[!include [banner](../includes/banner.md)]

Dette emnet beskriver kundeposteringsprofilser, som styrer posteringen av kundetransaksjoner til økonomimodulen.

## <a name="customer-posting-profiles"></a>Kundeposteringsprofiler

Kundeposteringsprofiler gjør det mulig å tilordne finanskontoer og dokumentinnstillingene til alle kunder, en kundegruppe eller en enkelt kunde. Disse innstillingene brukes når du oppretter salgsordrer, fakturaer, fritekstfakturaer, prosjektfakturaer, betalingsjournaler, purringer og rentenotaer. 

Standard posteringsprofil er definert i fanen **Finans og merverdiavgift** på siden **Kundeparametere**. Deretter tas det automatisk med i hodet til nye dokumenter. Du kan endre den der hvis du ønsker en annen posteringsprofil. 

Organisasjoner som godtar forskuddsbetalinger fra kunder, konfigurerer ofte en annen posteringsprofil for forskuddsbetalinger, og kobler den sammen i parameterne som standard posteringsprofil for forskuddsbetalinger. Hvis du vil ha mer informasjon, kan du se [Kundebetalinger](customer-prepayments.md).

Du kan også knytte posteringsdefinisjoner til transaksjonsposteringstyper på siden **Definisjoner for transaksjonspostering**. Posteringsdefinisjoner brukes i stedet for posteringsprofiler til å styre postering av kundetransaksjoner til økonomimodulen. Hvis du vil ha mer informasjon, kan du se [Posteringsdefinisjoner](../general-ledger/posting-definitions.md).

## <a name="creating-a-posting-profile"></a>Opprette en posteringsprofil
Angi finanskontoene som brukes ved posteringen av transaksjoner som bruker den valgte posteringsprofilen. Velg en kontokode og, hvis mulig, et konto- eller gruppenummer for den valgte posteringsprofilen. Under posteringsprosessen hentes den mest korrekte posteringsprofilen for hver transaksjon ved å søke etter den mest spesifikke kontokoden, gruppenummeret eller kombinasjonen gruppe og nummer etter følgende prioritering:

| Kontokode-feltverdi | Konto/gruppenummer-feltverdi                | Søkeprioritet |
|--------------------------|-------------------------------------------------|-----------------|
| Tabell                    | Spesifikk kundekonto                       | 1               |
| Gruppere                    | Kundegruppe som tilordnes kunden | 2               |
| Alle                      | Tom                                           | 3               |

Hvis du vil at alle kundetransaksjoner skal ha samme posteringsprofil, definerer du bare én posteringsprofil der **Alle** angis i **Kontokode**-feltet. Angi følgende verdier for å definere posteringsprofilen.

<table>
<thead>
<tr>
<th>Felt</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr>
<td>Posteringsprofil</td>
<td>Angi en kode for posteringsprofilen. Du kan for eksempel opprette to posteringsprofiler for å hente én konto for kundesaldoer i den nasjonale valutaen og en annen for kundesaldoer i en utenlandsk valuta. Du kan kalle den ene kontoen Nasjonal og den andre Utenlandsk.</td>
</tr>
<tr>
<td>Beskrivelse</td>
<td>Angi en beskrivelse av posteringsprofilen. Dette brukes bare til å identifisere posteringsprofilen mer nøyaktig når du viser den på denne siden.</td>
</tr>
<tr>
<td>Kontokode</td>
<td>Angi om posteringsprofilen gjelder en enkeltkunde, en gruppe kunder eller alle kunder:
<ul>
<li><b>Tabell</b> – Posteringsprofilen gjelder for en enkelt kunde. Velg kundekontoen i feltet <b>Konto/gruppenummer</b>.</li>
<li><b>Gruppe</b> – Posteringsprofilen gjelder for en kundegruppe. Velg kundegruppen i feltet <b>Konto/gruppenummer</b>.</li>
<li><b>Alle</b> – Posteringsprofilen gjelder for alle kunder. La feltet <b>Konto/gruppenummer</b> stå tomt.</li>
</ul>
</td>
</tr>
<tr>
<td>Konto/gruppenummer</td>
<td>Hvis <b>Tabell</b> velges i feltet <b>Kontokode</b>, velger du kontonummeret til kunden som er knyttet til posteringsprofilen. Hvis <b>Gruppe</b> er valgt, velger du kundegruppen. Hvis <b>Alle</b> er valgt, lar du feltet stå tomt.</td>
</tr>
<tr>
<td>Samlekonto</td>
<td>Velg hovedkontoen som skal brukes som kundehandelskonto for kunder som er knyttet til posteringsprofilen. Denne kontoen er kontoen for posteringstypen <b>Kundesaldo</b>.</td>
</tr>
<tr>
<td>Likviditetskonto for betalinger</td>
<td>Velg likviditetsfinanskontoen som brukes for kontantstrømprognoser. Dette feltet vises bare hvis kontantstrømprognoser er aktivert.</td>
</tr>
<tr>
<td>Mva-forskuddsbetalinger</td>
<td><p>Velg kontoen for merverdiavgift for forskuddsbetalte betalinger.</p>
<p><strong>Merk:</strong> Bruk siden <b>Kundeparametere</b> for å angi posteringsprofilen som skal brukes når en betaling er merket som en forskuddsbetaling.</p>
</td>
</tr>
<tr>
<td>Konto for rabattavsetning</td>
<td>Velg finanskontoen for diskontoforpliktelser.</td>
</tr>
<tr>
<td>Purreforløp</td>
<td>Velg identifikatoren for purreforløpet som skal brukes for kunder som er tilordnet posteringsprofilen.</td>
</tr>
<tr>
<td>Rentekode</td>
<td>Velg rentekoden som skal brukes for beregning av rente for kunder som er tilordnet posteringsprofilen.</td>
</tr>
</tbody>
</table>

## <a name="posting-examples"></a>Eksempler på postering

Følgende tabell viser eksempler på standard posteringstyper med eksempelhovedkontoer og -beskrivelser. Kolonnen **Debet/kredit** angir om transaksjonen vanligvis debiterer eller krediterer, eller i noen tilfeller kan postere begge. **Avregningskonto**-kolonnen angir at posteringstypen er en avregningskonto. Dette betyr at beløpet som er postert i denne kontoen, automatisk tilbakeføres når en senere transaksjon posteres. 

| Posteringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/kredit | Avregningskonto | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|--------------|------------------|-------------|
| Kundesaldo | 130100 | Kundehandel | Objekt | Begge | Nei | Angi kontoen i feltet **Samlekonto**.|
| Ingen | 110110 | Bankkonto | Objekt | Begge | Nei | Angi hovedkontoen i feltet **Likviditetskonto for betalinger**. Denne kontoen brukes ikke til postering. Den brukes bare til kontantstrømprognoser. |
| Mva-forskuddsbetalinger | 202900 | Merverdiavgiftavregning | Gjeld | Begge | Ja | Velg kontoen for merverdiavgift for forskuddsbetalte betalinger. |
| Konto for rabattavsetning | 250600 | Utsatt inntekt og rabatter | Gjeld | Begge | Ja | Velg finanskontoen for diskontoforpliktelser.|     

### <a name="table-restrictions"></a>Tabellrestriksjoner

For transaksjoner med den valgte posteringsprofilen kan du angi om transaksjonene skal utlignes automatisk, om rente skal beregnes, og om purringer blir utstedt. Du kan også velge kontoen som brukes når transaksjoner med den valgte posteringsprofilen er lukket.

Angi følgende verdier for å definere posteringsprofilen:

| Felt                 | Beskrivelse                                           |
|-----------------------|-------------------------------------------------------|
| Forlik        | Merk av for dette valget for å aktivere automatisk utligning for transaksjoner med denne posteringsprofilen. Hvis merket fjernes for dette valget, må du manuelt utligne transaksjoner ved hjelp av **Utlign åpne transaksjoner**-siden eller **Angi kundebetalinger**-siden. |
| Rente          | Merk av for dette valget hvis rente skal beregnes på utestående saldoer for kundekontoer som bruker denne profilen. Hvis merket fjernes for dette valget, vil det ikke beregnes renter for disse kundene.                                           |
| Purring | Merk av for dette valget hvis purrebrev skal genereres for kundekontoer som bruker denne profilen. Hvis merket fjernes for dette valget, vil det ikke genereres purrebrev for disse kundene.                                                 |
| Lukk             | Velg en posteringsprofil som du vil bytte til når transaksjoner med denne posteringsprofilen er lukket. En transaksjon anses som lukket når den er fullstendig utlignet.             |



Hvis du vil ha mer informasjon, kan du se [Oversikt over kundebetaling](../cash-bank-management/tasks/customer-payment-overview.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
