---
title: Organisere rapportkomponenter i rapportutforming
description: Denne artikkelen beskriver hvordan du organiserer eksisterende rapporter, byggeblokker og objekter i rapportutforming.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 29fdb6ac6b200956383386c42ccb7627314ea7a2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898718"
---
# <a name="organize-report-components-in-report-designer"></a>Organisere rapportkomponenter i rapportutforming

[!include [banner](../includes/banner.md)]

Når du har utformet byggeblokker og genererte rapporter, er det nyttig å organisere disse objektene slik at de blir enklere for brukerne å finne. Denne artikkelen beskriver hvordan du organiserer eksisterende rapporter, byggeblokker og objekter i rapportutforming.

Du kan gi nytt navn til mapper, rapporter, byggeblokker og andre objekter i rapportutforming, for å bidra til å organisere filene dine. Avhengig av hvilken type objekt du gir nytt navn, må du kanskje oppdatere tilknytninger til dette objektet.

## <a name="rename-a-folder-or-building-block-in-report-designer"></a>Gi nytt navn til en mappe eller byggeblokk i Rapportutforming
I Rapportutforming kan du gi nytt navn til mapper, rapportdefinisjoner, raddefinisjoner, kolonnedefinisjoner og rapporteringstredefinisjoner.

### <a name="rename-a-folder-or-building-block-in-report-designer"></a>Gi nytt navn til en mappe eller byggeblokk i Rapportutforming

1. Bruk navigasjonsruten i Rapportutforming til å finne mappen eller objektet som skal gis nytt navn.
2. Høyreklikk mappen eller objektet, og klikk deretter **Gi nytt navn**. **Navn**-feltet i navigasjonsruten blir tilgjengelig.
3. Skriv inn et nytt navn, og trykk deretter Enter.
4. Hvis byggeblokken er en raddefinisjon, kolonnedefinisjon eller rapporteringstredefinisjon, må du oppdatere andre byggeblokker som er knyttet til det. Høyreklikk byggeblokken du ga nytt navn i trinn 3, velg **Tilknytninger** og velg deretter et element i listen for å oppdatere det.
5. Gjenta trinn 4 til alle tilknyttede elementer er oppdaterte.

## <a name="create-and-manage-report-groups"></a>Opprette og administrere rapportgrupper.
Du kan gruppere rapportdefinisjoner for å generere flere rapporter samtidig. Hvis du vil opprette, endre, slette og generere rapportgrupper, må du ha rolle som utformer eller administrator. Brukere som har generatorrollen kan generere rapportgrupper og kan også endre innstillingen for brukerrapportdefinisjonene for rapportgrupper.

### <a name="create-a-report-group"></a>Opprette en rapportgruppe

1. Klikk på **Rapportgrupper** i navigasjonsruten i Rapportutforming.
2. På **Fil**-menhyen klikker du **Ny** &gt; **Rapportgruppedefinisjon** for å åpne en ny rapportgruppe i visningsvinduet. Du kan også klikke **Rapportgruppe**-knappen ![Rapportgruppe.](media/report-group.gif "Rapportgruppe") på verktøylinjen.
3. Klikk på fanen **Rapportgruppe**. For å overstyre informasjonen om de enkelte rapportdefinisjonene for genereringen av denne rapporten, merker du av for **Overstyr selskap, detalj og datoinnstillinger fra de enkelte rapportdefinisjonene**. Innstillingene for firmanavnet, detaljnivået, provisorisk og datoinformasjon, fylles ut automatisk, men du kan foreta oppdateringer.
4. Hvis du vil generere flere rapporter som viser rapporteringsvalutaene, merker du av for **Inkluder alle rapporteringsvalutaer**. Du kan deretter gå til flere visninger ved å klikke **Valuta** i webvisningen når du viser rapporten.
5. I feltet **Rapporter i gruppen** klikker du **Legg til** for å velge rapportene som skal tas med i rapportgruppen. Hvis du vil velge flere rapporter i dialogboksen **Legg til**, holder du nede CTRL-tasten mens du merker rapporter. Når du er ferdig med å velge rapporter, klikker du **OK**.
6. Klikk på **Fil** &gt; **Lagre** for å lagre den nye rapportgruppen.

### <a name="modify-a-report-group"></a>Endre en rapportgruppe

1. Klikk på **Rapportgrupper** i navigasjonsruten i Rapportutforming.
2. Dobbeltklikk rapportgruppen du vil endre.
3. I fanen **Rapportgruppe** gjør du de ønskede endringene.
4. På **Fil**-menyen klikker du **Lagre** for å lagre den endrede rapportgruppen, eller du kan alternativt klikke **Lagre**-knappen ![Lagre.](media/save.gif "Lagre") på verktøylinjen.

> [OBS!] Hvis du har planlagt rapporter slik at de genereres med jevne mellomrom, kan du overstyre disse innstillingene og generere en rapport umiddelbart.

### <a name="generate-a-report-group-report"></a>Generere en rapport for en rapportgruppe

1. Klikk på **Rapportgrupper** i navigasjonsruten i Rapportutforming.
2. Åpne rapportgruppen som skal genereres.
3. Klikk på **Generer rapport**-knappen ![Generer rapport.](media/generate-report.gif "Generer rapport") for å generere rapporter.

### <a name="delete-a-report-group"></a>Slette en rapportgruppe

1. Klikk på **Rapportgrupper** i navigasjonsruten i Rapportutforming.
2. Høyreklikk rapportgruppen som skal slettes, og velg deretter **Slett**.
3. Når det vises en bekreftelsesmelding, klikker du **Ja**.

## <a name="report-group-tab-controls"></a>Kontroller i fanen Rapportgruppe
Tabellen nedenfor beskriver kontrollene i fanen **Rapportgruppe**.

<table>
<thead>
<tr>
<th>Styring</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr>
<td>Overstyre firma, detaljer og datoinnstillinger fra individuelle rapportdefinisjoner</td>
<td>Merk av for dette alternativet for å overstyre individuelle rapportdefinisjoner av rapportene i denne rapportgruppen for generering av bare disse rapportene.</td>
</tr>
<tr>
<td>Firmanavn</td>
<td>Velg firmaet som skal brukes for rapportene.</td>
</tr>
<tr>
<td>Detaljnivå</td>
<td>Angi detaljnivået som rapportene inneholder.
<ul>
<li><strong>Økonomi</strong>– En sammendragsrapport på høyt nivå. Du kan ikke drille ned til kontoer og dimensjoner, bortsett fra kontoene og dimensjonene som lagt til gjennom et rapporteringstre.</li>
<li><strong>Økonomisk og Konto</strong> − En rapport som inneholder et overordnet sammendrag og kontodetaljer.</li>
<li><strong>Økonomisk, Konto og Transaksjon</strong> − En rapport som inneholder et overordnet sammendrag og transaksjonsdetaljer.</li>
</ul></td>
</tr>
<tr>
<td>Provisorisk</td>
<td>Angi aktivitetstypene som rapportene inneholder.
<ul>
<li><strong>Bare postert aktivitet</strong>− Inkluderer bare transaksjonene og saldoene som er postert i finansdataene.</li>
<li><strong>Postert og upostert aktivitet</strong>− Inkluderer alle transaksjonene og saldoene som er registrert og postert i finansdataene.</li>
<li><strong>Bare upostert aktivitet</strong>− Inkluderer bare transaksjonene som er registrert, men som ennå ikke er postert i finansdataene.</li>
</ul></td>
</tr>
<tr>
<td>Ta med alle rapporteringsvalutaer</td>
<td>Alle tilleggsrapporteringsvalutaer som er konfigurert i Microsoft Dynamics ERP-systemet, vises her. Merk av for dette alternativet for å generere tilleggsrapporter i valutaene som er angitt. For å vise rapportene i nettvisningsprogrammet ved å klikke <strong>Valuta</strong>-knappen og velge en valuta.</td>
</tr>
<tr>
<td>Datoinformasjon ikke lagret med rapportdefinisjon</td>
<td><ul>
<li>Basisperiode</li>
<li>Basisår</li>
<li>Periode som er dekket</li>
</ul>
Bare innstillingene for standard basisperiode lagres med rapportdefinisjonen.</td>
</tr>
<tr>
<td>Datoinformasjon lagret med rapportdefinisjon</td>
<td><ul>
<li>Rapportdato</li>
<li>Standard basisperiode</li>
</ul></td>
</tr>
<tr>
<td>Rapporter i gruppen</td>
<td>Legg til, fjerne og endre rapportrekkefølgen i rapportgruppen.
<ul>
<li>Hvis du vil legge til rapportdefinisjoner i rapportgruppen, dobbeltklikker du rapportgruppen for å åpne den og klikker deretter <strong>Legg til</strong>. Velg rapportene som skal inkluderes i rapportgruppen, og klikk deretter <strong>OK</strong>.</li>
<li>Hvis du vil fjerne en rapport fra rapportgruppen, velger du den og klikker deretter <strong>Fjern</strong>.</li>
<li>Hvis du vil endre rekkefølgen som rapportene genereres i, velger du en rapport i listen og klikker deretter <strong>Flytt opp</strong> eller <strong>Flytt ned</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Tilleggsressurser

[Finansrapportering](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]