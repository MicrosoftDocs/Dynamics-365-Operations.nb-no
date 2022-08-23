---
title: Arbeid med funksjonen Elektroniske meldinger
description: Denne artikkelen gir informasjon om hvordan du arbeider med EM-funksjonalitet (Elektroniske meldinger).
author: AdamTrukawka
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 929d3d3aad249007264204a3fd51377c8bb42377
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279280"
---
# <a name="work-with-the-electronic-messages-functionality"></a>Arbeide med funksjonen Elektroniske meldinger

[!include [banner](../includes/banner.md)]

Hvis du arbeider på meldingsnivå, er siden **Elektroniske meldinger** (**Mva** \> **Forespørsler og rapporter** \> **Elektroniske meldinger** \> **Elektronisk meldinger**) mer nyttig. Hvis du arbeider på datainnsamling- eller meldingselementnivå, er siden **Elektroniske meldingselementer** (**Mva** \> **Forespørsler og rapporter** \> **Elektroniske meldinger** \> **Elektronisk meldinger**) mer nyttig.

## <a name="electronic-messages"></a>Elektroniske meldinger

Siden **Elektroniske meldinger** presenterer behandlingen som er tilgjengelig for deg, basert på din rolle. Sikkerhetsroller er knyttet til behandling i oppsettet av denne behandlingen. For hver behandling som er tilgjengelig for deg, viser siden elektroniske meldinger og informasjon som er knyttet til disse.

**Meldinger**-hurtigfanen viser elektroniske meldinger for den valgte behandlingen. Avhengig av statusen for den valgte meldingen og forhåndsdefinert behandling, kan du kjøre noen handlinger ved å bruke knappene over rutenettet:

- **Ny** – Denne knappen er knyttet til handlinger for **Opprett melding**-typen.
- **Slett** – Denne knappen er tilgjengelig hvis det er merket av for **Tillat sletting** for den gjeldende statusen for den valgte meldingen.
- **Samle inn data** – Denne knappen er knyttet til handlinger av typen **Fyll ut poster**.
- **Generer rapport** – Denne knappen er knyttet til handlinger av typen **Melding om eksport av elektronisk rapportering**.
- **Send rapport** – Denne knappen er knyttet til handlinger av **Webtjeneste**-typen.
- **Importer svar** – Denne knappen er knyttet til handlinger av typen **Import av elektronisk rapportering**.
- **Oppdater status** – Denne knappen er knyttet til handlinger av typen **Behandling av bruker på meldingsnivå**.
- **Meldingselementer** – Åpne siden **Elektroniske meldingselementer**.

Hurtigfanen **Handlingslogg** viser informasjon om alle handlingene som er kjørt for den valgte meldingen. Hvis en handling har resultert i en feil, vil informasjon om feilen knyttes til den relaterte linjen i rutenettet. Hvis du vil se informasjon om feilen, velger du linjen i rutenettet, og velg deretter **Vedlegg**-knappen (bindersikonet) øverst i høyre hjørne på siden.

Hurtigfanen **Tilleggsfelt for melding** viser alle tilleggsfeltene som er definert for meldinger i behandlingsoppsettet. Hurtigfanen viser også verdiene i disse tilleggsfeltene.

Hurtigfanen **Meldingselementer** viser alle meldingselementer som er relatert til den valgte meldingen. Avhengig av statusen for det valgte meldingselementet kan du kjøre noen handlinger ved å bruke knappene over rutenettet:

- **Slett** – Denne knappen er tilgjengelig hvis det er merket av for **Tillat sletting** for den gjeldende statusen for det valgte meldingselementet.
- **Oppdater status** – Denne knappen er knyttet til handlinger av typen **Brukerbehandling**.
- **Opprinnelig dokument** – Åpne en side som viser det opprinnelige dokumentet for det valgte meldingselementet.

Rapportene som allerede er generert og mottatt for en melding, er knyttet til denne meldingen. Hvis du vil se vedleggene som er relatert til en melding, velger du meldingen, og deretter velger du **Vedlegg**-knappen (bindersikonet) øverst i høyre hjørne på siden.

![Vedlegg-knappen](media/attachment-icon.png)

Siden **Vedlegg** viser vedleggene som er knyttet til den valgte meldingen. Hvis du vil vise en fil, velger du den i listen til venstre, og deretter velger du **Åpne** i handlingsruten.

![Åpne-knappen](media/open-button.png)

Du kan vise vedlegg som er knyttet til en bestemt aktivitet som tidligere ble kjørt for en melding. Velg meldingen på siden **Elektroniske meldinger** i hurtigfanen **Meldinger**. Velg handlingen i hurtigoppføringen **Handlingslogg**, og velg deretter **Vedlegg**-knappen (papirklippsymbol) i øvre høyre hjørne på siden.

Du kan kjøre hele behandlingen eller bare en bestemt handling ved å velge **Kjør behandling** i handlingsruten.

## <a name="electronic-message-items"></a>Elektroniske meldingselementer

Siden **Elektroniske meldingselementer** viser alle meldingselementer og en logg over handlingene som er kjørt for hvert meldingselement. Den viser også tilleggsfeltene som er definert for meldingselementene, og verdiene for disse tilleggsfeltene.

Tabellen nedenfor beskriver feltene i fanen **Meldingselementer**.

<table>
<thead>
<tr>
<th>Felt</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr>
<td>Behandling</td>
<td>Navnet på behandling som ble brukt til å opprette meldingselementet.</td>
</tr>
<tr>
<td>Meldingselement</td>
<td>ID-en til meldingselementet. Denne ID-en tildeles automatisk basert på <b>Meldingselement</b>-nummerserien som er definert på siden <b>Parametere for økonomimodul</b>.</td>
</tr>
<tr>
<td>Dato for meldingselement</td>
<td>Datoen da meldingselementet ble opprettet.</td>
</tr>
<tr>
<td>Type meldingselement</td>
<td>Typen meldingselement. Flere typer meldingselementer kan defineres for den samme behandlingen (for eksempel <b>Innkommende fakturaer</b> og <b>Utgående fakturaer</b>). Dette feltet kan fylles ut automatisk bare når en faktura blir lagt til meldingselementtabellen.</td>
</tr>
<tr>
<td>Status for meldingselement</td>
<td><p>Den faktiske statusen for meldingselementet. De tilgjengelige statusene varierer avhengig av meldingselementtypen. Her er noen eksempler:</p>
<ul>
<li><b>Utfylt</b> – En post ble lagt til Meldingselementer-tabellen.</li>
<li><b>Evaluert</b> – Tilleggsattributter ble beregnet for meldingselementet.</li>
<li><b>Rapportert</b> – Meldingselementet ble lagt til en rapport.</li>
<li><b>Utelukket</b> – Denne statusen er nyttig hvis du bør utelukke noen meldingselementer fra en rapport før den blir eksportert.</li>
</ul>
</td>
</tr>
<tr>
<td>Overføringsdato</td>
<td>For behandling som automatisk sender en genererte rapport utenfor systemet, datoen da meldingselementet ble sendt.</td>
</tr>
<tr>
<td>Dokumentnr.</td>
<td>Dette feltet angis automatisk basert på oppsettet for handlingen for utfylling av poster. Dette feltet kan fylles ut automatisk bare når en faktura blir lagt til meldingselementtabellen.</td>
</tr>
<tr>
<td>Kontonummer</td>
<td>Kontonummeret til en kunde eller leverandør (eller en annen feltverdi, avhengig av feltet som er definert i handlingen for utfyllingen av poster). Dette feltet kan fylles ut automatisk bare når en faktura blir lagt til meldingselementtabellen.</td>
</tr>
<tr>
<td>Melding</td>
<td>Nummeret på meldingen. Dette nummeret tildeles automatisk basert på <b>Melding</b>-nummerserien som er definert på siden <b>Parametere for økonomimodul</b>.</td>
</tr>
<tr>
<td>Meldingsstatus</td>
<td>Den faktiske statusen for den elektroniske meldingen.</td>
</tr>
<tr>
<td>Neste handling</td>
<td>De neste handlingene som kan startes for den gjeldende statusen for meldingselementet.</td>
</tr>
</tbody>
</table>

**Tilleggsfelt**-kategorien viser flere felt for det valgte meldingselementet og deres verdier.

### <a name="run-processing"></a>Kjør behandling

Velg **Kjør behandling** i handlingsruten for å utføre behandlingen for meldingselementer. For å kjøre en bestemt handling, sett **Velg handling** til **Ja** i dialogboksen **Kjør behandling**, og velg deretter en handling. Hvis du vil kjøre hele behandlingen, setter du alternativet **Velg handling** til **Nei**.

### <a name="generate-report"></a>Generer rapport

Velg **Generer rapport** i handlingsruten. Denne knappen er knyttet til handlinger av typen **Eksport av elektronisk rapportering**.

### <a name="update-status"></a>Oppdater status

Velg **Oppdater status** i handlingsruten for å oppdatere statusen til én eller flere meldingselementer. I **Oppdater status**-dialogboksen bruker du **Poster som skal inkluderes**-hurtigkategorien til å velge meldingselementer for oppdatering. Pass på at du definerer valgkriteriene riktig, fordi meldingselementstatuser oppdateres i henhold til disse kriteriene, den innledende statusen for den valgte handlingen, og verdien du angir i feltet **Ny status**. Når en statusoppdatering er fullført, vil det være vanskelig å avgjøre hvilke elementer som ble oppdatert. Derfor blir det vanskelig å tilbakestille statusoppdateringen.

### <a name="electronic-messages"></a>Elektroniske meldinger

Velg **Elektroniske meldinger** i handlingsruten for å se gjennom en elektronisk melding som er knyttet til det valgte meldingselementet.

Du kan også se gjennom filene som er relatert til et bestemt meldingselement. Velg **Melding**-feltet for meldingselementet, eller velg **Elektroniske meldinger** i handlingsruten. Deretter, på siden **Elektronisk melding**, velger du meldingen du vil se gjennom filer for, og deretter velger du **Vedlegg**-knappen (bindersikonet) øverst i høyre hjørne på siden.

Siden **Vedlegg** viser vedleggene som er knyttet til meldingen. Hvis du vil vise en fil, velger du den i listen til venstre, og deretter velger du **Åpne** i handlingsruten.

### <a name="original-document"></a>Opprinnelig dokument

Velg **Opprinnelig dokument** i handlingsruten for å åpne det opprinnelige dokumentet for det valgte meldingselementet.
