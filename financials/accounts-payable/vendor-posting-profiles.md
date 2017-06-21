---
title: "Leverandørposteringsprofiler"
description: "Leverandørposteringsprofiler styrer postering av leverandørtransaksjoner til økonomimodulen."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 2dbb8874323631a9bddb226834adf87d014c1c2f
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="vendor-posting-profiles"></a>Leverandørposteringsprofiler

[!include[banner](../includes/banner.md)]


Leverandørposteringsprofiler styrer postering av leverandørtransaksjoner til økonomimodulen.

<a name="vendor-posting-profiles"></a>Leverandørposteringsprofiler
-----------------------

Leverandørposteringsprofiler gjør det mulig å tilordne finanskontoer og dokumentinnstillinger til alle leverandører, en gruppe med leverandører eller en enkelt leverandør. Disse innstillingene brukes når du oppretter bestillinger, leverandørfakturaer og kontantbetalinger. For noen transaksjoner kan du velge en posteringsprofil som er forskjellig fra og har forrang for posteringsprofilene som er definert for transaksjoner på denne siden. Standard posteringsprofil er definert i hurtigfanen Finans og merverdiavgift på siden Leverandørparametere. Standardposteringsprofilen inkluderes deretter automatisk i hodet på nye dokumenter, der du kan endre den til en annen posteringsprofil om nødvendig.

Du kan også knytte posteringsdefinisjoner til transaksjonsposteringstyper på siden Definisjoner for transaksjonspostering. Posteringsdefinisjoner styrer posteringen av leverandørtransaksjoner til økonomimodulen i stedet for posteringsprofiler.

## <a name="creating-a-posting-profile"></a>Opprette en posteringsprofil
### <a name="setup"></a>**Oppsett**

Angi finanskontoene som brukes ved posteringen av transaksjoner som bruker den valgte posteringsprofilen. Velg en kontokode og, hvis mulig, et konto- eller gruppenummer for den valgte posteringsprofilen. Under posteringsprosessen hentes den mest korrekte posteringsprofilen for hver transaksjon ved å søke etter den mest spesifikke kontokoden, gruppenummeret eller kombinasjonen gruppe og nummer etter følgende prioritering:

| **Kontokode**-feltverdi | **Konto/gruppenummer**-feltverdi        | Søkeprioritet |
|------------------------------|---------------------------------------------|-----------------|
| **Tabell**                    | Bestemt leverandørkonto                     | 1               |
| **Gruppe**                    | leverandørgruppe som er tilknyttet leverandøren | 2               |
| **Alle**                      | Tom                                       | 3               |

Hvis du vil ha samme posteringsprofil for alle leverandørtransaksjoner, definerer du bare én posteringsprofil med Alle i Kontokode-feltet. Angi følgende verdier for å definere posteringsprofilen:

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
<li><strong>Tabell</strong> – Posteringsprofilen gjelder for en enkelt leverandør. Velg leverandørkontoen i feltet Konto/gruppenummer.</li>
<li><strong>Gruppe</strong> – Posteringsprofilen gjelder for en leverandørgruppe. Velg leverandørgruppen i feltet Konto/gruppenummer.</li>
<li><strong>Alle</strong> – Posteringsprofilen gjelder for alle leverandører. La feltet Konto/gruppenummer stå tomt.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Konto/gruppenummer</strong></td>
<td>Hvis Tabell velges i feltet Kontokode, velger du kontonummeret til leverandøren som er knyttet til posteringsprofilen. Hvis Gruppe er valgt, velger du en leverandørgruppe. Hvis Alle er valgt, lar du feltet stå tomt.</td>
</tr>
<tr class="odd">
<td><strong>Samlekonto</strong></td>
<td>Velg finanskontoen som skal brukes som samlekonto for leverandørene som posteringsprofilen er relatert til.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Obs!</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hvis Bruk posteringsdefinisjoner (på/av) velges på siden Parametere for økonomimodul, brukes transaksjonsposteringsdefinisjonen for leverandørfakturaer i stedet samlekontoen.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Utligningskonto</strong></td>
<td>Velg likviditetsfinanskontoen som brukes for kontantstrømprognoser. Dette feltet er bare tilgjengelig når kontantstrømprognoser er aktivert.</td>
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
<td>Posteringsprofilen som brukes når betalingen er merket som en forskuddsbetaling, velges i Postering-profilen med journalbilag for forskuddsbetaling i Finans og merverdiavgift-området på siden Leverandørparametere.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Ankomst</strong></td>
<td>Velg finanskontoen som informasjon om ikke-godkjente leverandørfakturaene er postert til. Informasjonen angis i ankomstregistreringsjournalen. En bruker kan for eksempel angi svært enkel informasjon om leverandørfakturaer når de mottas i fakturaregisteret. Når fakturaregisteret posteres, blir transaksjonene postert til kontoen som er angitt her og i Motkonto-feltet. Når fakturaene er godkjent, blir gjelden overført fra ankomstkontoen til samlekontoen for leverandør.</td>
</tr>
<tr class="odd">
<td><strong>Motkonto</strong></td>
<td>Velg finanskontoen som brukes til å motpostere ikke-godkjente leverandørfakturaer som oppdateres via fakturaregisteret. Motposteringskontoen fungerer som motposteringskontoen for transaksjoner som posteres til ankomstkontoer. Kontoen inneholder derfor leverandørinnkjøp som ennå ikke er godkjent.</td>
</tr>
</tbody>
</table>
 

### <a name="table-restrictions"></a>**Tabellrestriksjoner**

For transaksjoner med den valgte posteringsprofilen kan du angi om transaksjonene skal utlignes automatisk, om rente skal beregnes, og om purringer blir utstedt. Du kan også velge kontoen som brukes når transaksjoner med den valgte posteringsprofilen er lukket.

Angi følgende verdier for å definere posteringsprofilen:

| Felt          | Beskrivelse                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Utligning** | Merk av for dette valget for å aktivere automatisk utligning for transaksjoner med denne posteringsprofilen. Hvis merket fjernes for dette valget, må du manuelt utligne transaksjoner ved hjelp av Utlign åpne transaksjoner-siden. |
| **Avbryt**     | Merk av for dette valget hvis du ønsker å ha muligheten til å avbryte transaksjoner med denne posteringsprofilen.                                                                                                               |
| **Lukke**      | Velg en posteringsprofil som du vil bytte til når transaksjoner med denne posteringsprofilen er lukket. En transaksjon anses som lukket når den er fullstendig utlignet.                                       |






