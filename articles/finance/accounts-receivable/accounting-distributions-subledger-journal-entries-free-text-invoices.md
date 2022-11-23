---
title: Regnskapsdistribusjoner og journaloppføringer for fritekstfakturaer
description: Regnskapsdistribusjoner brukes til å definere hvordan beløp skal gjøres rede for, for eksempel hvordan omsetning, avgiften eller gebyrene skal gjøres rede for på en fritekstfaktura. Alle beløp som må redegjøres for når fritekstfakturaen er journalføres, har én eller flere regnskapsdistribusjoner.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5120c4e75e821776201d5add2d498feb94d0297
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778418"
---
# <a name="accounting-distributions-and-subledger-entries-for-free-text-invoices"></a>Regnskapsdistribusjoner og underfinansoppføringer for fritekstfakturaer

[!include [banner](../includes/banner.md)]

Regnskapsdistribusjoner brukes til å definere hvordan beløp skal gjøres rede for, for eksempel hvordan omsetning, avgiften eller gebyrene skal gjøres rede for på en fritekstfaktura. Alle beløp som må redegjøres for når fritekstfakturaen er journalføres, har én eller flere regnskapsdistribusjoner.

## <a name="accounting-distributions"></a>Regnskapsdistribusjoner

Du kan bruke følgende knapper på **Fritekstfaktura**-siden for å vise, og eventuelt endre, regnskapsdistribusjonene for hvert beløp i fritekstfakturaen.

-   **Fordel beløp** – Vis og endre regnskapsdistribusjonene for en enkelt linje og eventuelle underordnede linjer, for eksempel avgifter eller gebyrer. Du kan også vise og endre regnskapsdistribusjonene for den underordnede linjen direkte fra siden **Mva-transaksjoner** eller **Tilleggstransaksjoner**.
    -   Endre fritekstfakturahodebeløp, for eksempel tillegg eller avrundingsbeløp for valuta.
    -   Endre fritekstfakturalinjebeløp.
-   **Vis distribusjoner** – Vis regnskapsdistribusjonene for alle linjer i dokumentet. Du kan ikke endre regnskapsdistribusjonene fra denne visningen.
    -   Vis overskrift og linjebeløp.

## <a name="distributing-amounts"></a>Distribuere beløp
Når du registrerer en fritekstfaktura, fordeles hvert beløp på følgende måte.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Angi et pengebeløp</th>
<th>Der hovedkontoen vises fra</th>
<th>Rekkefølge som bestemmer hvilken standard finansdimensjon som vises</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Fritekstfakturalinje</td>
<td>Finanskontoen på fritekstfakturalinjen.</td>
<td><ol>
<li>Hvis hovedkontoen er en tildelingskonto, bruker du standardverdien fra tildelingskontodefinisjonen.</li>
<li>Hvis hovedkontoen ikke er en tildelingskonto, bruk standardmalen for finansdimensjon på fritekstfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier på fritekstfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</li>
</ol></td>
</tr>
<tr class="even">
<td>Fritekstfakturalinje for en anleggsmiddelnummer- og verdimodellkombinasjon
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>Obs! </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hovedkontoen på fritekstfakturalinjen blir avhendingskonto for anleggsmiddel.</td>
</tr>
</tbody>
</table>
</div></td>
<td>Finanskontoen på fritekstfakturalinjen.</td>
<td><ol>
<li>Bruk standard finansdimensjonsverdier på fritekstfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Rabattbeløp for fritekstfaktura</td>
<td>Hovedkontoen for Kunderabatt-felt på Kontantrabatt-siden.</td>
<td><ol>
<li>Hvis hovedkontoen er en tildelingskonto, bruker du standardverdien fra tildelingskontodefinisjonen.</li>
<li>Hvis hovedkontoen ikke er en tildelingskonto, bruk standardmalen for finansdimensjon på fritekstfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier på fritekstfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</li>
</ol></td>
</tr>
<tr class="even">
<td>Mva-beløp for fritekstfaktura</td>
<td>Feltet Konto, utgående mva på siden Finansposteringsgrupper.</td>
<td><ol>
<li>Bruk finansdimensjonene som er definert for linjebeløpet for fritekstfakturaen eller distribusjonene for gebyrlinjebeløpet.</li>
<li>Bruk standard finansdimensjonsverdier på fritekstfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Gebyrlinjebeløp for fritekstfaktura</td>
<td>Kreditkonto-feltet på siden Tilleggskode.</td>
<td><ol>
<li>Hvis hovedkontoen er en tildelingskonto, bruker du standardverdien fra tildelingskontodefinisjonen.</li>
<li>Hvis hovedkontoen ikke er en tildelingskonto, bruk standardmalen for finansdimensjon på fritekstfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier på fritekstfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a>Distribusjonsavgifter
Kan ikke opprette regnskapsdistribusjoner for avgifter før avgifter er beregnet. Hvis du vil beregne merverdiavgift, må du fullføre en av de følgende oppgavene i **Fritekstfaktura**-siden:
-   Vis merverdiavgiften.
-   Vis fakturatotalen.
-   Vis kontantstrømmen.
-   Vis regnskapsdistribusjoner for hele fritekstfakturaen.
-   Vis underfinansjournalen.

## <a name="subledger-journals-for-free-text-invoices"></a> Underfinansjournaler for fritekstfakturaer
Før du posterer en fritekstfaktura, kan du vise den fullstendige regnskapsoppføringen for fakturaen, som inkluderer debet og kredit, for å bekrefte at fakturaen posteres på de riktige kontoene. Denne visningen av den fullstendige regnskapsoppføringen kalles en underfinansjournal. Hvis underfinansjournaloppføringen er feil når du forhåndsviser den før du journalfører fritekstfakturaen, kan du ikke endre underfinansjournaloppføringen. I stedet må du endre regnskapsdistribusjonene eller posteringsprofilen. Regnskapsdistribusjonene brukes til å definere én side av regnskapsoppføringen, debet eller kredit. Motkontooppføringen i underfinansjournalen opprettes fra posteringsprofilene, for eksempel fra kundekontoen eller avgiften.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
