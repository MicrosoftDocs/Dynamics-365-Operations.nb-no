---
title: Regnskapsdistribusjoner og journaloppføringer for leverandørfakturaer
description: Regnskapsdistribusjoner brukes til å definere hvordan beløp skal gjøres rede for, for eksempel hvordan utgiften, avgiften eller gebyrene skal gjøres rede for på en leverandørfaktura. Alle beløp som må redegjøres for når leverandørfakturaen er journalføres, har én eller flere regnskapsdistribusjoner.
author: sunfzam
ms.date: 02/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f10ddf113f59da4800a97a48300ab1310bfb42dd
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358187"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a>Regnskapsdistribusjoner og journaloppføringer for leverandørfakturaer

[!include [banner](../includes/banner.md)]

Regnskapsdistribusjoner brukes til å definere hvordan beløp skal gjøres rede for, for eksempel hvordan utgiften, avgiften eller gebyrene skal gjøres rede for på en leverandørfaktura. Alle beløp som må redegjøres for når leverandørfakturaen er journalføres, har én eller flere regnskapsdistribusjoner. 

## <a name="accounting-distributions"></a>Regnskapsdistribusjoner 

Du kan bruke følgende knapper på Leverandørfaktura-siden til å vise, og eventuelt endre, regnskapsdistribusjonene for hvert beløp i leverandørfakturaen.
-   **Fordel beløp** – Vis og endre regnskapsdistribusjonene for en enkelt linje og eventuelle underordnede linjer, for eksempel avgifter eller gebyrer. Du kan også vise og endre regnskapsdistribusjonene for den underordnede linjen direkte fra siden **Mva-transaksjoner** eller **Tilleggstransaksjoner**.
    -   Endre topptekstbeløp for topptekstbeløp, for eksempel tillegg eller avrundingsbeløp for valuta.
    -   Endre linjebeløp for leverandørfaktur.
-   **Vis distribusjoner** – Vis regnskapsdistribusjonene for alle linjer i dokumentet. Du kan ikke endre regnskapsdistribusjonene fra denne visningen.
    -   Vis overskrift og linjebeløp.

Hvis leverandørfakturaen refererer til en bestilling, kan du dele opp og endre regnskapsdistribusjonene for linjer som inneholder en vare som ikke er lagerført. Hvis leverandørfakturalinjen ikke refererer til en bestillingslinje, kan du også slette en regnskapsdistribusjon. Du kan ikke dele eller slette linjer for gebyrer, avgifter og linjerabatter. Du kan endre finanskontoen, men du kan ikke endre beløpene eller prosentandelene.
> [!NOTE]                                                                                                                                 
> Hvis den overordnede linjen inneholder en vare som ikke er lagerført, og regnskapsdistribusjonene er delt, deles den underordnede linjen automatisk for å samsvare med finansdimensjonene for den overordnede linjen. Regnskapsdistribusjonene for den underordnede linjen ikke kan deles ytterligere eller slettes, men avhengig av oppsettet for den underordnede linjen, kan det hende du kan endre finanskontoen for regnskapsdistribusjonene i den underordnede linjen.

## <a name="distributing-amounts"></a>Distribuere beløp
Når du registrerer en leverandørfaktura, fordeles beløpene på følgende måte.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Type leverandørfakturalinje</th>
<th>Rekkefølge som bestemmer hvor hovedkontoen vises fra</th>
<th>Rekkefølge som bestemmer hvilken standard finansdimensjon som vises</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lagerført produkt</td>
<td><ol>
<li>Regnskapsdistribusjonen for bestillingslinjen.</li>
<li><strong>Hovedkonto</strong>-feltet når Innkjøpsutgift for produktet velges på <strong>Postering</strong>-siden.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</li>
<li>Bruk standard finansdimensjonsverdier for leverandørfakturaen.</li>
</ol></td>
</tr>
<tr class="even">
<td>Innkjøpskategori eller et produkt som ikke er lagerført</td>
<td><ol>
<li>Regnskapsdistribusjonen for bestillingslinjen, hvis leverandørfakturalinjen refererer til en bestillingslinje.</li>
<li><strong>Hovedkonto</strong>-feltet når Innkjøpsutgift for utgiften velges på <strong>Postering</strong>-siden.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</li>
<li>Hvis hovedkontoen er en tildelingskonto, bruker du standardverdien fra tildelingskontodefinisjonen.</li>
<li>Bruk standard finansdimensjonsverdier for leverandørfakturaen.</li>
<li>Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på <strong>Kontoplan</strong>-siden.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Anleggsmiddel</td>
<td><ol>
<li>Regnskapsdistribusjonen for bestillingslinjen, hvis leverandørfakturalinjen refererer til en bestillingslinje.</li>
<li>Hvis <strong>Anskaffelse</strong> velges i <strong>Transaksjonstype</strong>-feltet på siden <strong>Leverandørfaktura</strong>, <strong>Hovedkonto</strong>-feltet når <strong>Anskaffelse</strong> velges på siden <strong>Posteringsprofiler for anleggsmidler</strong>.</li>
<li>Hvis <strong>Anskaffelsesjustering</strong> velges i <strong>Transaksjonstype</strong>-feltet, <strong>Hovedkonto</strong>-feltet når <strong>Anskaffelsesjustering</strong> velges på siden <strong>Posteringsprofiler for anleggsmidler</strong>.</li>
</ol></td>
<td><ol>
<li>Bruk kontodistribusjonen for bestillingslinjen hvis fakturalinjereferansen er en bestillingslinje.</li>
<li>Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på <strong>Kontoplan</strong>-siden.</li>
</ol></td>
</tr>
<tr class="even">
<td>Prosjekt definert på leverandørfakturalinjen</td>
<td><ol>
<li>Regnskapsdistribusjonen for bestillingslinjen, hvis fakturalinjen refererer til en bestillingslinje.</li>
<li>Hvis <strong>Saldo</strong> velges i feltet <strong>Poster kostnader – vare</strong> på siden <strong>Prosjektgrupper</strong>, <strong>Hovedkonto</strong>-feltet når <strong>Kostnad</strong> velges på siden <strong>Finansposteringsoppsett</strong>.</li>
<li>Hvis <strong>Resultat</strong> velges i feltet <strong>Poster kostnader – vare</strong> på siden <strong>Prosjektgrupper</strong>, <strong>Hovedkonto</strong>-feltet når <strong>Kostnad – vare</strong> velges på siden <strong>Finansposteringsoppsett</strong>.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Linjerabatt</td>
<td><ol>
<li>Regnskapsdistribusjonen for bestillingslinjen, hvis fakturalinjen refererer til en bestillingslinje.</li>
<li><strong>Hovedkonto</strong>-feltet når <strong>Rabatt</strong> velges på <strong>Postering</strong>-siden.</li>
<li>Hvis en hovedkonto for en rabatt ikke er definert i posteringsprofilen, regnskapsdistribusjonen for den utvidede prisen på bestillingslinjen.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke regnskapsdistribusjonen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra regnskapsdistribusjonene for den utvidede prisen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene for leverandørfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på <strong>Kontoplan</strong>-siden.</li>
</ol></td>
</tr>
<tr class="even">
<td>Innkjøpstillegg, som er angitt i fanen <strong>Pris og rabatt</strong> på bestillingslinjen</td>
<td><ol>
<li>Regnskapsdistribusjonen for bestillingslinjen, hvis fakturalinjen refererer til en bestillingslinje.</li>
<li>Regnskapsdistribusjonen for den utvidede prisen på bestillingslinjen.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra regnskapsdistribusjonene for den utvidede prisen for bestillingslinjen.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Linjetillegg</td>
<td><ol>
<li>Regnskapsdistribusjonen for bestillingslinjen, hvis fakturalinjen refererer til en bestillingslinje.</li>
<li>Hvis <strong>Finanskonto</strong> velges i <strong>Debettype</strong>-feltet på <strong>Tilleggskode</strong>-siden, <strong>Debetkonto</strong>-feltet på <strong>Tilleggskode</strong>-siden.</li>
<li>Hvis <strong>Vare</strong> er valgt i <strong>Debettype</strong>-feltet på <strong>Tilleggskode</strong>-siden, regnskapsdistribusjonen for den utvidede prisen på bestillingslinjen.</li>
<li>Hvis <strong>Kunde/leverandør</strong> velges i <strong>Debettype</strong>-feltet på <strong>Tilleggskode</strong>-siden, <strong>Kreditkonto</strong>-feltet på <strong>Tilleggskode</strong>-siden.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra regnskapsdistribusjonene for den utvidede prisen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på <strong>Kontoplan</strong>-siden.</li>
</ol></td>
</tr>
<tr class="even">
<td>Avgift med følgende betingelse:
<ul>
<li>Alternativet <strong>Bruk amerikanske avgiftsregler</strong> er valgt på siden <strong>Parametere for økonomimodul</strong>.</li>
</ul></td>
<td><ol>
<li>Regnskapsdistribusjonen for bestillingslinjen, hvis fakturalinjen refererer til en bestillingslinje.</li>
<li>Regnskapsdistribusjonen for den utvidede prisen eller tillegget.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra regnskapsdistribusjonene for den utvidede prisen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Avgift med følgende betingelser:
<ul>
<li>Alternativet <strong>Bruk amerikanske avgiftsregler</strong> er ikke valgt på siden <strong>Parametere for økonomimodul</strong>.</li>
<li><strong>Use tax</strong>-feltet for mva-gruppen er ikke avmerket på siden <strong>Mva-grupper</strong>.</li>
</ul></td>
<td><ol>
<li>Hvis avgiftsbeløpet er fradragsberettiget, feltet <strong>Innkommende merverdiavgift</strong> på siden <strong>Finansposteringsgrupper</strong>.</li>
<li>Hvis avgiftsbeløpet ikke er fradragsberettiget, den utvidede prisen eller regnskapsdistribusjonen for tillegget.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra den utvidede prisen eller regnskapsdistribusjonene for avgiften på bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på <strong>Kontoplan</strong>-siden.</li>
</ol></td>
</tr>
<tr class="even">
<td>Avgift med følgende betingelser:
<ul>
<li>Alternativet Bruk amerikanske avgiftsregler er ikke valgt på siden <strong>Parametere for økonomimodul</strong>.</li>
<li><strong>Use tax</strong>-feltet for mva-gruppen er valgt på siden <strong>Mva-grupper</strong>.</li>
</ul></td>
<td><ol>
<li>Hvis avgiftsbeløpet er fradragsberettiget, feltet <strong>Innkommende merverdiavgift</strong> på siden <strong>Finansposteringsgrupper</strong>.</li>
<li>Hvis avgiftsbeløpet ikke er fradragsberettiget, feltet <strong>Use tax-utgift</strong> på siden <strong>Finansposteringsgrupper</strong>.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra den utvidede prisen eller regnskapsdistribusjonene for avgiften på bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på <strong>Kontoplan</strong>-siden.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Hodegebyr</td>
<td><ol>
<li>Hvis <strong>Finans</strong>-konto velges i <strong>Debettype</strong>-feltet på <strong>Tilleggskode</strong>-siden, <strong>Debetkonto</strong>-feltet på <strong>Tilleggskode</strong>-siden.</li>
<li>Hvis <strong>Kunde/leverandør</strong> velges i <strong>Debettype</strong>-feltet på <strong>Tilleggskode</strong>-siden, <strong>Kreditkonto</strong>-feltet på <strong>Tilleggskode</strong>-siden.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</li>
<li>Hvis hovedkontoen er en tildelingskonto, bruker du standardverdien fra tildelingskontodefinisjonen.</li>
<li>Bruk standardmalverdier for finansdimensjon fra leverandørfakturhodet.</li>
<li>Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på <strong>Kontoplan</strong>-siden.</li>
</ol></td>
</tr>
<tr class="even">
<td>Hoderabatt</td>
<td><ol>
<li><strong>Hovedkonto</strong>-feltet for <strong>Posteringstype for leverandørfakturarabatt</strong> på siden <strong>Kontoer for automatiske transaksjoner</strong>.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra regnskapsdistribusjonene for den utvidede prisen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på <strong>Kontoplan</strong>-siden.</li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="distributing-taxes"></a>Distribusjonsavgifter

Kan ikke opprette regnskapsdistribusjoner for avgifter før avgifter er beregnet. Hvis du vil beregne merverdiavgift, må du fullføre en av de følgende oppgavene på siden **Leverandørfaktura**:
-   Vis fakturatotalen.
-   Vis merverdiavgiften.
-   Vis underfinansjournalen.
-   Vis regnskapsdistribusjoner for den fullførte leverandørfakturaen.
-   Sett leverandørfakturaen på vent.
-   Poster leverandørfakturaen.

## <a name="subledger-journals-for-vendor-invoices"></a>Underfinansjournaler for leverandørfakturaer
Før du posterer en leverandørfaktura, kan du vise den fullstendige regnskapsoppføringen for fakturaen, som inkluderer debet og kredit, for å bekrefte at fakturaen posteres på de riktige kontoene. Denne visningen av den fullstendige regnskapsoppføringen kalles en underfinansjournal. 

Hvis underfinansjournaloppføringen er feil når du forhåndsviser den før du journalfører leverandørfakturaen, kan du ikke endre underfinansjournaloppføringen. I stedet må du endre regnskapsdistribusjonene eller posteringsprofilen. Regnskapsdistribusjonene brukes til å definere én side av regnskapsoppføringen, debet eller kredit. Motkontooppføringen i underfinansjournalen opprettes ved å bruke posteringsprofilene, for eksempel fra leverandørkontoen eller avgift.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
