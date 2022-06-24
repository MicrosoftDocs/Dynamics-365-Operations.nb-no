---
title: Kvalitetstilknytninger
description: Denne artikkelen beskriver hvordan du kan bruke kvalitettilknytninger i Microsoft Dynamics 365 Supply Chain Management til å generere kvalitetsordrer automatisk som er knyttet til salgs-, innkjøps- og produksjonsprosessene.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e96f301d8dec255e57f0f0fbfa9c8e1a5922ae9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887522"
---
# <a name="quality-associations"></a>Kvalitetstilknytninger

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du kan bruke kvalitettilknytninger i Microsoft Dynamics 365 Supply Chain Management til å generere kvalitetsordrer automatisk som er knyttet til salgs-, innkjøps- og produksjonsprosessene.

En kvalitetstilknytning definerer alle følgende opplysninger om en kvalitetsordre som er generert:

- Transaksjonshendelsen
- Settet med tester som må utføres på elementene
- Akseptabelt kvalitetsnivå
- Prøveplanen

Du må definere en kvalitetstilknytning for hver variasjon i en forretningsprosess som krever automatisk generering av kvalitetsordrer. Eksempelvis kan en kvalitetsordre genereres i forretningsprosessen for bestillinger, karanteneordrer, salgsordrer og produksjonsordrer.

## <a name="working-with-quality-associations"></a>Arbeide med kvalitetstilknytninger

Forretningsprosessen som bruker en kvalitetstilknytning, kan knyttes til ulike kildedokumenter, for eksempel bestillinger, salgsordrer eller produksjonsordrer.

Hver kvalitetstilknytningspost definerer settet med tester, det akseptable kvalitetsnivået og samplingplanen som gjelder for kvalitetsordrene som genereres. Du må definere en kvalitetstilknytningspost for hver variasjon i en forretningsprosess. Du kan for eksempel definere en kvalitetstilknytning som genererer en kvalitetsordre når et produkt for bestillingsmottak oppdateres. Avhengig av oppsettet til utførelsesplanen kan selve utløsingsprosessen blokkeres mens det er en åpen kvalitetsordre. Etterfølgende prosesser, for eksempel fakturering av bestillinger, kan eventuelt blokkeres.

> [!NOTE]
> Når det finnes åpne kvalitetsordrer, blokkeres lagerantall automatisk fra å bli utstedt. Avhengig av innstillingen i **Full blokkering**-feltet på siden **Vareprøver** er antallet enten antallet på kvalitetsordren eller antallet på kildedokumentlinjen. Hvis du vil ha mer informasjon, kan du se [Vareprøve for kvalitetsstyring](quality-item-sampling.md).

For en gitt forretningsprosess identifiserer kvalitetstilknytningspost hendelsen og betingelsene som en kvalitetsordre genereres for. Betingelsene kan være spesifikke for et område eller en juridisk enhet. En kvalitetsordre som omfatter destruktive tester, kan bare genereres når hvis det finnes lagerbeholdning for hendelsen.

Hvis du vil arbeide med kvalitetstilknytninger, kan du gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Kvalitetstilknytninger**. De følgende eksemplene illustrerer hvordan en kvalitetstilknytningspost er definert for variasjonene innen ulike forretningsprosesser. For hvert eksempel oppsummere følgende tabell hendelsene og betingelsene som er definert av en kvalitetstilknytningspost.

<table>
<thead>
<tr>
<th>Referansetype</th>
<th>Hendelsestype</th>
<th>Utførelse</th>
<th>Hendelsesblokkering</th>
<th>Dokumentreferanse</th>
</tr>
</thead>
<tbody>
<tr>
<td>Beholdning</td>
<td>Gjelder ikke her</td>
<td>Gjelder ikke her</td>
<td>Ingen</td>
<td>Alle</td>
</tr>
<tr>
<td rowspan="7">Salg</td>
<td rowspan="4">Plukkingsprosess er planlagt</td>
<td rowspan="4">Før</td>
<td>Ingen</td>
<td rowspan="22">Bare Spesifikk ID, Gruppe eller Alle</td>
</tr>
<tr>
<td>Plukkingsprosess</td>
</tr>
<tr>
<td>Følgeseddel</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="3">Følgeseddel</td>
<td rowspan="3">Før</td>
<td>Ingen</td>
</tr>
<tr>
<td>Følgeseddel</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="15">Kjøp</td>
<td rowspan="7">Kvitteringsliste</td>
<td rowspan="4">Før</td>
<td>Ingen</td>
</tr>
<tr>
<td>Kvitteringsliste</td>
</tr>
<tr>
<td>Produktkvittering</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="3">Etter</td>
<td>Ingen</td>
</tr>
<tr>
<td>Produktkvittering</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="3">Registrering</td>
<td rowspan="3">Gjelder ikke her</td>
<td>Ingen</td>
</tr>
<tr>
<td>Produktkvittering</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="5">Produktkvittering</td>
<td rowspan="3">Før</td>
<td>Ingen</td>
</tr>
<tr>
<td>Produktkvittering</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="2">Etter</td>
<td>Ingen</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="8">Produksjon</td>
<td rowspan="3">Registrering</td>
<td rowspan="3">Gjelder ikke her</td>
<td>Ingen</td>
<td rowspan="12">Alle</td>
</tr>
<tr>
<td>Ferdigmeld</td>
</tr>
<tr>
<td>Slutt</td>
</tr>
<tr>
<td rowspan="5">Ferdigmeld</td>
<td rowspan="3">Før</td>
<td>Ingen</td>
</tr>
<tr>
<td>Ferdigmeld</td>
</tr>
<tr>
<td>Slutt</td>
</tr>
<tr>
<td rowspan="2">Etter</td>
<td>Ingen</td>
</tr>
<tr>
<td>Slutt</td>
</tr>
<tr>
<td rowspan="4">Karantene</td>
<td rowspan="3">Ferdigmeld</td>
<td rowspan="2">Før</td>
<td>Ferdigmeld</td>
</tr>
<tr>
<td>Slutt</td>
</tr>
<tr>
<td>Etter</td>
<td>Slutt</td>
</tr>
<tr>
<td>Slutt</td>
<td>Før</td>
<td>Slutt</td>
</tr>
<tr>
<td rowspan="3">Ruteoperasjon</td>
<td rowspan="3">Ferdigmeld</td>
<td rowspan="2">Før</td>
<td>None</td>
<td rowspan="3">Bestemt ID, Gruppe eller Alle, og Ressursspesifikk, Gruppe eller Alle</td>
</tr>
<tr>
<td>Ferdigmeld</td>
</tr>
<tr>
<td>Etter</td>
<td>None</td>
</tr>
<tr>
<td rowspan="3">Koproduktproduksjon</td>
<td>Registrering</td>
<td>Gjelder ikke</td>
<td rowspan="3">None</td>
<td rowspan="3">Alle</td>
</tr>
<tr>
<td rowspan="2">Ferdigmeld</td>
<td>Før</td>
</tr>
<tr>
<td>Etter</td>
</tr>
</tbody>
</table>

> [!NOTE]
> Funksjonen *Kvalitetsstyring for lagerprosesser* legger til funksjoner for kvalitetsordrebehandling for produksjon med feltet **Hendelsestype** satt til *Ferdigmeld* og **Utførelse** satt til *Etter*, og for innkjøp med **Hendelsestype** satt til *Registrering*. For mer informasjon, se [Kvalitetsstyring for lagerprosesser](quality-management-for-warehouses-processes.md).

Tabellen nedenfor inneholder mer informasjon om hvordan kvalitetsordrer kan genereres for bestemte typer prosesser.

<div class="tableSection">
<table>
<thead>
<tr>
<th>Type av prosess</th>
<th>Når kvalitetsordrer kan genereres automatisk</th>
<th>Når kvalitetsordrer kan genereres hvis destruktiv testing kreves</th>
<th>Betingelsesinformasjon</th>
<th>Informasjon om manuell generering</th>
</tr>
</thead>
<tbody>
<tr>
<td>Bestilling</td>
<td>Før eller etter en kvitteringsliste eller produktkvittering for materialet som mottas, posteres</td>
<td>Etter produktkvitteringen for materialet som mottas, er postert, fordi materialet må være tilgjengelig for destruktiv testing</td>
<td>Behovet for en kvalitetsordre kan reflektere et bestemt område, en vare, en leverandør eller en kombinasjon av disse betingelsene.</td>
<td>En manuelt generert kvalitetsordre som viser til en bestilling, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</td>
</tr>
<tr>
<td>Karanteneordre</td>
<td>Før eller etter karanteordren er rapportert som fullført eller avsluttet</td>
<td>Kvalitetsordrer som krever destruktive tester, kan ikke genereres. Det forutsettes at karanteneordrefunksjonaliteten behandler disposisjonen av materialet som blir ødelagt.</td>
<td>Behovet for en kvalitetsordre kan reflektere et bestemt område, en vare, en leverandør eller en kombinasjon av disse betingelsene.</td>
<td>En manuelt generert kvalitetsordre som viser til en karanteneordre, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</td>
</tr>
<tr>
<td>Salgsordre</td>
<td>Før en planlagt plukkeprosessen eller følgeseddeloppdatering for varene som leveres</td>
<td>I alle trinn</td>
<td>Kravet til en kvalitetsordre kan reflektere et bestemt område, en vare, en kunde eller en kombinasjon av disse betingelsene.</td>
<td>En manuelt generert kvalitetsordre som viser til en salgsordre, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</td>
</tr>
<tr>
<td>Produksjonsordre</td>
<td>Før eller etter den ferdige kvaliteten for produksjonsordren er rapportert</td>
<td>Etter den ferdige kvaliteten for produksjonsordren er rapportert</td>
<td>Behovet for en kvalitetsordre kan reflektere et bestemt område eller vare, eller en kombinasjon av disse betingelsene.</td>
<td>En manuelt generert kvalitetsordre som viser til en produksjonsordre, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</td>
</tr>
<tr>
<td>Produksjonsordre som har en ruteoperasjon</td>
<td>Før eller etter at rapporten for en operasjon er fullført</td>
<td>Etter at rapporteringen av produksjonen er fullført for den siste operasjonen</td>
<td>Behovet for en kvalitetsordre kan reflektere et bestemt område, en vare eller en operasjonsressurs eller en kombinasjon av disse betingelsene.</td>
<td>En manuelt generert kvalitetsordre som viser til en ruteoperasjon, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</td>
</tr>
<tr>
<td>Lager</td>
<td>En kvalitetsordre kan ikke genereres automatisk for en transaksjon innen en lagerjournal eller for overføringsordretransaksjoner.</td>
<td></td>
<td></td>
<td>En kvalitetsordre må opprettes manuelt for en vares lagerantall. Varens fysiske lagerbeholdning kreves.</td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Eksempler på automatisk generering av kvalitetsordrer

### <a name="purchasing"></a>Innkjøp

I innkjøp, hvis du du angir feltet **Hendelsestype** til *Produktkvittering* og feltet **Utførelse** til *Etter* på siden **Kvalitetstilknytninger**, får du følgende resultater:

- Hvis alternativet **Per oppdatert mengde** er satt til *Ja*, genereres det en kvalitetsordre for hvert mottak mot bestillingen basert på det mottatte antallet og innstillingene i vareprøven. Hver gang et antall mottas mot bestillingen, genereres nye kvalitetsordrer basert på det nylig mottatte antallet.
- Hvis alternativet **Per oppdatert mengde** er satt til *Nei*, genereres det en kvalitetsordre for det første mottaket mot bestillingen basert på det mottatte antallet. I tillegg blir én eller flere kvalitetsordrer opprettet på grunnlag av restantallet, avhengig av sporingsdimensjonene. Kvalitetsordrer genereres ikke for etterfølgende mottak mot bestillingen.

### <a name="production"></a>Produksjon

I produksjon, hvis du du angir feltet **Hendelsestype** til *Ferdigmeld* og feltet **Utførelse** til *Etter* på siden **Kvalitetstilknytninger**, får du følgende resultater:

- Hvis alternativet **Per oppdatert mengde** er satt til *Ja*, genereres det en kvalitetsordre for hver fullførte antall og innstillingene i vareprøven. Hver gang et antall rapporteres som fullført mot produksjonsordren, genereres nye kvalitetsordrer basert på det nylig fullførte antallet. Denne genereringslogikken er konsekvent med innkjøp.
- Hvis alternativet **Per oppdatert mengde** er satt til *Nei*, genereres det en kvalitetsordre første gang antallet rapporteres som fullført, basert på det fullførte antallet. I tillegg blir én eller flere kvalitetsordrer opprettet på grunnlag av restantallet, avhengig av sporingsdimensjonene for vareprøven. Kvalitetsordrer genereres ikke for etterfølgende ferdigmeldte antall.

<table>
<thead>
<tr>
<th>Kvalitetsspesifikasjon</th>
<th>Per oppdatert mengde</th>
<th>Per sporingsdimensjon</th>
<th>Resultat</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prosent: 10 %</td>
<td>Ja</td>
<td>
<p>Partinummer: Nei</p>
<p>Serienummer: Nei</p>
</td>
<td>
<p>Ordreantall: 100</p>
<ol>
<li>Rapporter som ferdig for 30
<ul>
<li>Kvalitetsordre 1 for 3 (10 % av 30)</li>
</ul>
</li>
<li>Rapporter som ferdig for 70
<ul>
<li>Kvalitetsordre 2 for 7 (10 % av restordreantallet, som er 70 i dette tilfellet)</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Fast antall: 1</td>
<td>Nei</td>
<td>
<p>Partinummer: Nei</p>
<p>Serienummer: Nei</p>
</td>
<td>Ordreantall: 100
<ol>
<li>Rapporter som ferdig for 30
<ul>
<li>Kvalitetsordre 1 for 1 (for det første ferdigmeldte antallet, som har en fast verdi på 1)</li>
<li>Kvalitetsordre 2 for 1 (for det resterende antallet, som fremdeles har en fast verdi på 1)</li>
</ul>
</li>
<li>Rapporter som ferdig for 10
<ul>
<li>Ingen kvalitetsordrer er opprettet.</li>
</ul>
</li>
<li>Rapporter som ferdig for 60
<ul>
<li>Ingen kvalitetsordrer er opprettet.</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Fast antall: 1</td>
<td>Ja</td>
<td>
<p>Partinummer: Ja</p>
<p>Serienummer: Ja</p>
</td>
<td>
<p>Ordreantall: 10</p>
<ol>
<li>Ferdigmeld for 3: 1 for partinummer b1, serienummer s1. 1 for partinummer b2, serienummer s2. og 1 for partinummer b3, serienummer s3
<ul>
<li>Kvalitetsordre 1 for 1 av partinummer b1, serienummer s1</li>
<li>Kvalitetsordre 2 for 1 av partinummer b2, serienummer s2</li>
<li>Kvalitetsordre 3 for 1 av partinummer b3, serienummer s3</li>
</ul>
</li>
<li>Ferdigmeld for 2: 1 for partinummer b4, serienummer 4; og 1 for partinummer b5, serienummer s5
<ul>
<li>Kvalitetsordre 4 for 1 av partinummer b4, serienummer s4</li>
<li>Kvalitetsordre 5 for 1 av partinummer b5, serienummer s5</li>
</ul>
</li>
</ol>
<p><strong>Merk:</strong> Partiet kan brukes på nytt.</p>
</td>
</tr>
<tr>
<td>Fast antall: 2</td>
<td>Nei</td>
<td>
<p>Partinummer: Ja</p>
<p>Serienummer: Ja</p>
</td>
<td>
<p>Ordreantall: 10</p>
<ol>
<li>Ferdigmeld for 4: 1 for partinummer b1, serienummer s1. 1 for partinummer b2, serienummer s2. 1 for partinummer b3, serienummer s3 og 1 for partinummer b4, serienummer s4
<ul>
<li>Kvalitetsordre 1 for 1 av partinummer b1, serienummer s1</li>
<li>Kvalitetsordre 2 for 1 av partinummer b2, serienummer s2</li>
<li>Kvalitetsordre 3 for 1 av partinummer b3, serienummer s3</li>
<li>Kvalitetsordre 4 for 1 av partinummer b4, serienummer s4</li>
</ul>
<ul>
<li>Kvalitetsordre 5 for 2, uten referanse til et partinummer og et serienummer</li>
</ul>
</li>
<li>Ferdigmeld for 6: 1 for partinummer b5, serienummer s5. 1 for partinummer b6, serienummer s6. 1 for partinummer b7, serienummer s7. 1 for partinummer b8, serienummer s8. 1 for partinummer b9, serienummer s9 og 1 for partinummer b10, serienummer s10
<ul>
<li>Ingen kvalitetsordrer er opprettet.</li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Tilleggsressurser

- [Kvalitetsstyringsprosesser](quality-management-processes.md)
- [Aktivere kvalitets- og avviksstyring](enable-quality-management.md)
- [Kvalitetsstyring for lagerprosesser](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
