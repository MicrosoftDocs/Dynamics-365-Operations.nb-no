---
title: Regnskapsdistribusjoner og journaloppføringer for leverandørfakturaer
description: Regnskapsdistribusjoner brukes til å definere hvordan beløp skal gjøres rede for, for eksempel hvordan utgiften, avgiften eller gebyrene skal gjøres rede for på en leverandørfaktura. Alle beløp som må redegjøres for når leverandørfakturaen er journalføres, har én eller flere regnskapsdistribusjoner.
author: abruer
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df40d25e2027cf484e3f596fd315dca1c5b8809137aad9948da228245ad85f50
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749252"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a>Regnskapsdistribusjoner og journaloppføringer for leverandørfakturaer

[!include [banner](../includes/banner.md)]

Regnskapsdistribusjoner brukes til å definere hvordan beløp skal gjøres rede for, for eksempel hvordan utgiften, avgiften eller gebyrene skal gjøres rede for på en leverandørfaktura. Alle beløp som må redegjøres for når leverandørfakturaen er journalføres, har én eller flere regnskapsdistribusjoner. 

## <a name="accounting-distributions"></a>Regnskapsdistribusjoner 

Du kan bruke følgende knapper på Leverandørfaktura-siden til å vise, og eventuelt endre, regnskapsdistribusjonene for hvert beløp i leverandørfakturaen.
-   **Fordel beløp** – Vis og endre regnskapsdistribusjonene for en enkelt linje og eventuelle underordnede linjer, for eksempel avgifter eller gebyrer. Du kan også vise og endre regnskapsdistribusjonene for den underordnede linjen direkte fra Mva-transaksjoner- eller Tilleggstransaksjoner-siden.
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
<li>Hovedkonto-feltet når Innkjøpsutgift for produktet velges på siden Postering.</li>
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
<li>Hovedkonto-feltet når Innkjøpsutgift for utgiften velges på siden Postering.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</li>
<li>Hvis hovedkontoen er en tildelingskonto, bruker du standardverdien fra tildelingskontodefinisjonen.</li>
<li>Bruk standard finansdimensjonsverdier for leverandørfakturaen.</li>
<li>Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Anleggsmiddel</td>
<td><ol>
<li>Regnskapsdistribusjonen for bestillingslinjen, hvis leverandørfakturalinjen refererer til en bestillingslinje.</li>
<li>Hvis Anskaffelse velges i Transaksjonstype-feltet i skjemaet Leverandørfaktura, Hovedkonto-feltet når Anskaffelse velges på siden Posteringsprofil for anleggsmidler.</li>
<li>Hvis Anskaffelsesjustering velges i Transaksjonstype-feltet, Hovedkonto-feltet når Anskaffelsesjustering velges på siden Posteringsprofil for anleggsmidler.</li>
</ol></td>
<td><ol>
<li>Bruk kontodistribusjonen for bestillingslinjen hvis fakturalinjereferansen er en bestillingslinje.</li>
<li>Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</li>
</ol></td>
</tr>
<tr class="even">
<td>Prosjekt definert på leverandørfakturalinjen</td>
<td><ol>
<li>Regnskapsdistribusjonen for bestillingslinjen, hvis fakturalinjen refererer til en bestillingslinje.</li>
<li>Hvis Saldo velges i feltet Poster kostnader - vare på siden Prosjektgrupper, Hovedkonto-feltet når Kostnad velges på siden Finansposteringsoppsett.</li>
<li>Hvis Resultat velges i feltet Poster kostnader - vare på siden Prosjektgrupper, Hovedkonto-feltet når Kostnad - vare velges på siden Finansposteringsoppsett.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Linjerabatt</td>
<td><ol>
<li>Regnskapsdistribusjonen for bestillingslinjen, hvis fakturalinjen refererer til en bestillingslinje.</li>
<li>Hovedkonto-feltet når rabatt velges på Postering-siden.</li>
<li>Hvis en hovedkonto for en rabatt ikke er definert i posteringsprofilen, regnskapsdistribusjonen for den utvidede prisen på bestillingslinjen.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke regnskapsdistribusjonen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra regnskapsdistribusjonene for den utvidede prisen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene for leverandørfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</li>
</ol></td>
</tr>
<tr class="even">
<td>Innkjøpstillegg, som er angitt i kategorien Pris og rabatt i bestillingslinjen</td>
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
<li>Hvis finanskontoen velges i Debettype-feltet i skjemaet Tilleggskode, Debetkonto-feltet på siden Tilleggskode.</li>
<li>Hvis Vare er valgt i Debettype-feltet i Tilleggskode-skjemaet, regnskapsdistribusjonen for den utvidede prisen på bestillingslinjen.</li>
<li>Hvis Kunde/leverandør velges i Debettype-feltet i skjemaet Tilleggskode, Kreditkonto-feltet på siden Tilleggskode.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra regnskapsdistribusjonene for den utvidede prisen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</li>
</ol></td>
</tr>
<tr class="even">
<td>Avgift med følgende betingelse:
<ul>
<li>Alternativet Bruk amerikanske avgiftsregler er valgt på siden Parametere for økonomimodul.</li>
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
<li>Alternativet Bruk amerikanske avgiftsregler er ikke valgt på siden Parametere for økonomimodul.</li>
<li>Use tax-feltet for mva-gruppen er ikke avmerket på siden Mva-grupper.</li>
</ul></td>
<td><ol>
<li>Hvis avgiftsbeløpet er fradragsberettiget, feltet Innkommende merverdiavgift på siden Finansposteringsgrupper.</li>
<li>Hvis avgiftsbeløpet ikke er fradragsberettiget, den utvidede prisen eller regnskapsdistribusjonen for tillegget.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra den utvidede prisen eller regnskapsdistribusjonene for avgiften på bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</li>
</ol></td>
</tr>
<tr class="even">
<td>Avgift med følgende betingelser:
<ul>
<li>Alternativet Bruk amerikanske avgiftsregler er ikke valgt på siden Parametere for økonomimodul.</li>
<li>Use tax-feltet for mva-gruppen er valgt på siden Mva-grupper.</li>
</ul></td>
<td><ol>
<li>Hvis avgiftsbeløpet er fradragsberettiget, feltet Innkommende merverdiavgift på siden Finansposteringsgrupper.</li>
<li>Hvis avgiftsbeløpet ikke er fradragsberettiget, feltet Use tax-utgift på siden Finansposteringsgrupper.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra den utvidede prisen eller regnskapsdistribusjonene for avgiften på bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Hodegebyr</td>
<td><ol>
<li>Hvis finanskontoen velges i Debettype-feltet i skjemaet Tilleggskode, Debetkonto-feltet på siden Tilleggskode.</li>
<li>Hvis Kunde/leverandør velges i Debettype-feltet i skjemaet Tilleggskode, Kreditkonto-feltet på siden Tilleggskode.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</li>
<li>Hvis hovedkontoen er en tildelingskonto, bruker du standardverdien fra tildelingskontodefinisjonen.</li>
<li>Bruk standardmalverdier for finansdimensjon fra leverandørfakturhodet.</li>
<li>Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</li>
</ol></td>
</tr>
<tr class="even">
<td>Hoderabatt</td>
<td><ol>
<li>Hovedkonto-feltet for posteringstypen Leverandørfakturarabatt på siden Kontoer for automatiske transaksjoner.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen refererer til en bestillingslinje, kan du bruke kontodistribusjonen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra regnskapsdistribusjonene for den utvidede prisen for bestillingslinjen.</li>
<li>Bruk finansdimensjonsverdiene fra leverandørfakturalinjen.</li>
<li>Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="distributing-taxes"></a>Distribusjonsavgifter

Kan ikke opprette regnskapsdistribusjoner for avgifter før avgifter er beregnet. Hvis du vil beregne merverdiavgift, må du fullføre en av de følgende oppgavene på Leverandørfaktura-siden:
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