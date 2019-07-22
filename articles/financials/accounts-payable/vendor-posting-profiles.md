---
title: Leverandørposteringsprofiler
description: Leverandørposteringsprofiler styrer postering av leverandørtransaksjoner til økonomimodulen.
author: abruer
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3f62df7ec5627556561db950d54ff4347d2b4d6
ms.sourcegitcommit: ce84a1faeda6013ef6a90038d811a72f375b604e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/12/2019
ms.locfileid: "1625901"
---
# <a name="vendor-posting-profiles"></a>Leverandørposteringsprofiler

[!include [banner](../includes/banner.md)]

Leverandørposteringsprofiler styrer postering av leverandørtransaksjoner til økonomimodulen.

<a name="vendor-posting-profiles"></a>Leverandørposteringsprofiler
-----------------------

Leverandørposteringsprofiler gjør det mulig å tilordne finanskontoer og dokumentinnstillinger til alle leverandører, en gruppe med leverandører eller en enkelt leverandør. Disse innstillingene brukes når du oppretter bestillinger, leverandørfakturaer og kontantbetalinger. For noen transaksjoner kan du velge en posteringsprofil som er forskjellig fra og har forrang for posteringsprofilene som er definert for transaksjoner på denne siden. Standard posteringsprofil er definert i hurtigfanen **Finans og merverdiavgift** på siden **Leverandørparametere**. Standard posteringsprofil inkluderes deretter automatisk i hodet på nye dokumenter, der du kan endre den til en annen posteringsprofil om nødvendig.

Du kan også knytte posteringsdefinisjoner til transaksjonsposteringstyper på siden **Definisjoner for transaksjonspostering**. Posteringsdefinisjoner styrer posteringen av leverandørtransaksjoner til økonomimodulen i stedet for posteringsprofiler.

## <a name="creating-a-posting-profile"></a>Opprette en posteringsprofil
### <a name="setup"></a>**Oppsett**

Angi finanskontoene som brukes ved posteringen av transaksjoner som bruker den valgte posteringsprofilen. Velg en kontokode og, hvis mulig, et konto- eller gruppenummer for den valgte posteringsprofilen. Under posteringsprosessen hentes den mest aktuelle posteringsprofilen for hver transaksjon ved å søke etter den mest spesifikke kontokoden, gruppenummeret eller kombinasjonen gruppe og nummer etter følgende prioritering.

| **Kontokode**-feltverdi | **Konto/gruppenummer**-feltverdi        | Søkeprioritet |
|------------------------------|---------------------------------------------|-----------------|
| **Tabell**                    | Bestemt leverandørkonto                     | 1               |
| **Gruppere**                    | Leverandørgruppe som er knyttet til leverandøren | 2               |
| **Alle**                      | Tom                                       | 3               |

Hvis du vil ha samme posteringsprofil for alle leverandørtransaksjoner, definerer du bare én posteringsprofil med **Alle** i **Kontokode**-feltet. Angi følgende verdier for å definere posteringsprofilen.

<table>
<thead>
<tr class="header">
<th>Felt</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Posteringsprofil</strong></td>
<td>Angi en kode for posteringsprofilen. Du kan for eksempel opprette to posteringsprofiler for å hente én konto for leverandørsaldoer i nasjonal valuta og en annen for leverandørsaldoer i en utenlandsk valuta. Du kan kalle den ene kontoen Nasjonal og den andre Utenlandsk.</td>
</tr>
<tr class="even">
<td><strong>Beskrivelse</strong></td>
<td>Angi en beskrivelse av posteringsprofilen.</td>
</tr>
<tr class="odd">
<td><strong>Kontokode</strong></td>
<td>Angi om posteringsprofilen gjelder for en spesifikk leverandør, en gruppe leverandører eller alle leverandører:
<ul>
<li><strong>Tabell</strong> – Posteringsprofilen gjelder for en enkelt leverandør. Velg leverandørkontoen i feltet <strong>Konto/gruppenummer</strong>.</li>
<li><strong>Gruppe</strong> – Posteringsprofilen gjelder for en leverandørgruppe. Velg leverandørgruppen i feltet <strong>Konto/gruppenummer</strong>.</li>
<li><strong>Alle</strong> – Posteringsprofilen gjelder for alle leverandører. La feltet <strong>Konto/gruppenummer</strong> stå tomt.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Konto/gruppenummer</strong></td>
<td>Hvis <strong>Tabell</strong> er valgt i feltet <strong>Kontokode</strong>, velger du kontonummeret til leverandøren som er knyttet til posteringsprofilen. Hvis <strong>Gruppe</strong> er valgt, velger du en leverandørgruppe. Hvis <strong>Alle</strong> er valgt, lar du feltet stå tomt.</td>
</tr>
<tr class="odd">
<td><strong>Samlekonto</strong></td>
<td>Velg finanskontoen som skal brukes som samlekonto for leverandørene som posteringsprofilen er relatert til. Parameteren <strong>Ikke tillat manuell registrering</strong> for denne hovedkontoen blir merket. Hvis du senere fjerner denne kontoen fra posteringsprofilen, må du validere innstillingen for <strong>Ikke tillat manuell registrering</strong> på <strong>Hovedkontoer</strong>-siden. 
<p><strong>Obs!</strong> Hvis alternativet <strong>Bruk posteringsdefinisjoner</strong> er valgt på siden <strong>Parametere for økonomimodul</strong>, brukes transaksjonsposteringsdefinisjonen for leverandørfakturaer i stedet for samlekontoen.</p>
</td>
</tr>
<tr class="even">
<td><strong>Utligningskonto</strong></td>
<td>Velg likviditetsfinanskontoen som brukes for kontantstrømprognoser. Dette feltet er bare tilgjengelig når kontantstrømprognoser er aktivert.</td>
</tr>
<tr class="odd">
<td><strong>Mva-forskuddsbetalinger</strong></td>
<td>Velg kontoen for merverdiavgift for forskuddsbetalte betalinger.
<p><strong>Obs!</strong> Posteringsprofilen som brukes når betalingen er merket som en forskuddsbetaling, velges i <strong>Postering</strong>-profilen med feltet <strong>Journalbilag for forskuddsbetaling</strong> i området <strong>Finans og merverdiavgift</strong> på siden <strong>Leverandørparametere</strong>.</p>
</td>
</tr>
<tr class="even">
<td><strong>Ankomst</strong></td>
<td>Velg finanskontoen som informasjon om ikke-godkjente leverandørfakturaene er postert til. Informasjonen angis i ankomstregistreringsjournalen. En bruker kan for eksempel angi svært enkel informasjon om leverandørfakturaer når de mottas i fakturaregisteret. Når fakturaregisteret posteres, blir transaksjonene postert til kontoen som er angitt her og i <strong>Motkonto</strong>-feltet. Når fakturaene er godkjent, blir gjelden overført fra ankomstkontoen til samlekontoen for leverandør.</td>
</tr>
<tr class="odd">
<td><strong>Motkonto</strong></td>
<td>Velg finanskontoen som brukes til å motpostere ikke-godkjente leverandørfakturaer som oppdateres via fakturaregisteret. Motposteringskontoen fungerer som motposteringskontoen for transaksjoner som posteres til ankomstkontoer. Kontoen inneholder derfor leverandørinnkjøp som ennå ikke er godkjent.</td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a>**Tabellrestriksjoner**

For transaksjoner med den valgte posteringsprofilen kan du angi om transaksjonene skal utlignes automatisk, om rente skal beregnes, og om purringer blir utstedt. Du kan også velge kontoen som brukes når transaksjoner med den valgte posteringsprofilen er lukket.

Angi følgende verdier for å definere posteringsprofilen

| Felt          | Beskrivelse                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Utligning** | Merk av for dette valget for å aktivere automatisk utligning for transaksjoner med denne posteringsprofilen. Hvis merket fjernes for dette valget, må du manuelt utligne transaksjoner ved hjelp av siden **Utlign åpne transaksjoner**. |
| **Avbryt**     | Merk av for dette valget hvis du ønsker å ha muligheten til å avbryte transaksjoner med denne posteringsprofilen.                                                                                                               |
| **Lukke**      | Velg en posteringsprofil som du vil bytte til når transaksjoner med denne posteringsprofilen er lukket. En transaksjon anses som lukket når den er fullstendig utlignet.                                       |
