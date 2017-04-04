---
title: "Slå sammen lagerpartier"
description: "Denne emnet gir informasjon om hvordan du konsolidererer to eller flere lagerpartier i et sammenslått parti."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventBatchJournalListPage, InventBatchJournalMerge
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 39782
ms.assetid: 07c5e98b-10fd-4f5c-b471-41d2150f47b0
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 5abf8cf272924669cec6987a96f6565fffa54642
ms.lasthandoff: 03/31/2017


---

# <a name="merge-inventory-batches"></a>Slå sammen lagerpartier

Denne emnet gir informasjon om hvordan du konsolidererer to eller flere lagerpartier i et sammenslått parti. 

Når du slår sammen partier, kan beregninger være med på å optimalisere egenskapene og partiattributtene i det sammenslåtte partiet. Etter at du har kildepartiene, kan du se gjennom og endre det sammenslåtte partiet før du posterer det. Du kan også overføre partisammenslåingen til en lagerjournal for godkjenning. Lageret kan deretter reserveres eller posteres direkte fra denne lagerjournalen. Når du posterer et sammenslått parti, justeres beholdningen for kildepartiene og det sammenslåtte partiet.

## <a name="are-there-any-prerequisites"></a>Er eventuelle forhåndskrav gjeldende?
Ja, det er enkelte ting du må definere før du kan bruke verktøyene for sammenslåing av parti. Tabellen nedenfor beskriver forutsetningene.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Side</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Journalnavn, beholdning</td>
<td>Du må opprette et journalnavn som skal brukes som standard når du posterer partisammenslåinger i lagerjournaler. Valgfritt, men anbefalt: Du kan angi at reserveringer foretas automatisk når partisammenslåingen overføres til lagerjournalen. Ellers er det fare for at det kan gjøres en endring av lagerbeholdning etter at opplysningene om partisammenslåingen er definert og journalen er postert. Hvis du vil aktivere automatiske reserveringer for journalnavnet, velger du <strong>automatisk</strong> i den <strong><strong>reservering</strong></strong> feltet.</td>
</tr>
<tr class="even">
<td>Parametere for beholdnings- og lagerstyring</td>
<td>Du må angi standard journalnavn for lagerjournalen.</td>
</tr>
<tr class="odd">
<td>Frigitte produkter</td>
<td>Her er de anbefalte innstillingene for varen:
<ul>
<li>Hvis du vil generere partinumre for sammenslåtte partier automatisk, må du tilordne det frigitte produktet til en partinummergruppe. Du kan også angi et partinummer manuelt når du oppretter et sammenslått parti, eller velge et eksisterende partinummer. Hvis du velger et eksisterende partinummer, må du kontrollere at det valgte partiet ikke er inkludert i noen lagertransaksjoner.</li>
<li>Hvis du bruker holdbarhet eller best før-datoer for det frigitte produktet, blir datoene for et sammenslått parti beregnet basert på valget i feltet <strong>Datoberegning for partisammenslåing</strong>. Følgende alternativer er tilgjengelige:
<ul>
<li><strong>Tidligst</strong> – Beregningen baseres på den tidligste datoen som er angitt for et kildeparti som er valgt for partisammenslåingen.</li>
<li><strong>Senest</strong> – Beregningen baseres på den seneste datoen som er angitt for et kildeparti som er valgt for partisammenslåingen.</li>
<li><strong>Manuelt</strong> – Ingen beregning utføres. Hvis en dato er den samme i alle kildepartier, foreslås det en dato. Du kan endre denne datoen. Hvis en dato ikke er den samme i kildepartiene, kan du angi datoen manuelt.</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>Partinummergruppe</td>
<td>Valgfritt: Hvis du vil generere et partinummer når du oppretter et sammenslått parti, må du tilordne en partinummergruppe til det frigitte produktet. Ellers kan du angi et partinummer manuelt.</td>
</tr>
</tbody>
</table>

## <a name="when-might-i-want-to-merge-batches-of-inventory"></a>Når er det aktuelt å slå sammen lagerpartier?
Her er noen eksepmpler på scenarier der det kan være nyttig å slå sammen partier:

-   Sammy går gjennom lageret, og legger merke til at det finnes flere partier av den samme varen som har lave antall. Han forventer å motta flere nye forsendelser, og han innser at han kan frigjøre plass ved å slå sammen de ulike antallene til et nytt parti.
-   Sammy mottar beholdning, og ønsker å kombinere det nye partiet met ett han allerede har mottatt, for å forbedre det eksisterende partiets partiattributtverdi.

## <a name="can-i-merge-batches-across-sites-and-legal-entities"></a>Kan jeg slå sammen partier på tvers av områder og juridiske enheter?
Nei, kan du bare flette partier som har samme område og lagringsdimensjoner for lager i én juridisk enhet. Du kan imidlertid angi en annen lokasjon og pall-ID for det sammenslåtte partiet.

## <a name="can-i-merge-partial-quantities"></a>Kan jeg flette delvise antall?
Nei, kan du flette bare hele antallet for partier. Funksjonaliteten for partisammenslåing er ment som en funksjon for lager, ikke en funksjon for produksjon.

## <a name="what-if-the-batches-have-different-batch-attribute-values"></a>Hva om bunkene har forskjellige bunkeattributtverdier?
Når du velger kildepartiene som skal kombineres i det sammenslåtte partiet, kontrollerer Microsoft Dynamics 365 for Operations om egenskapene eller attributtverdiene er like i alle partiene. Når en attributtverdi er den samme, foreslås det en verdi for det sammenslåtte partiet. Du kan endre denne verdien. Attributtverdier som ikke er like, forblir tomme for det sammenslåtte partiet, og du kan angi disse verdiene manuelt. Hvis partiattributtypen for attributtverdien er et heltall eller en brøkdel og verdiene ikke er de samme for alle kildepartiene, beregnes verdien ved hjelp av en beregning av avveid gjennomsnitt. Den beregnede verdien rundes opp eller ned til nærmeste inkrement.. Hvis verdien er tom for et kildeparti, blir ikke partiet og tilhørende antall inkludert i beregningen. **Eksempel** Eksemplet nedenfor viser en beregning av avveid gjennomsnitt for et sammenslått parti. To av kildepartiene har en tom verdi for en partiattributtypen som er et heltall. Følgende attributt er tilordnet til kildepartiene.

| Attributt | Minimum | Økning | Maksimum |
|-----------|---------|-----------|---------|
| Klasse     | 3       | 3         | 30      |

Kildepartiene har følgende attributtverdier for partiattributtet **Klasse**.

| Parti | Antall | Attributt | Attributtverdi |
|-------|----------|-----------|-----------------|
| B1    | 10       | Klasse     | Tom           |
| B2    | 15       | Klasse     | 15              |
| B3    | 20       | Klasse     | 20              |
| B4    | 25       | Klasse     | Tom           |
| B5    | 30       | Klasse     | 25              |

Når du legger til disse partiene som kildepartier, tilordnes følgende verdier til det sammenslåtte partiet.

| Parti | Antall | Attributt | Attributtverdi |
|-------|----------|-----------|-----------------|
| B6    | 100      | Klasse     | 21              |

Verdier og antall for partier B1 og B4 er ikke inkludert i beregningen av avveid gjennomsnitt. Derfor beregnes verdien for det sammenslåtte partiet på følgende måte.

| Verdi | Antall (vekt)                              | Relativ vekt | Relativ vekt x Verdi                                               |
|-------|------------------------------------------------|-----------------|-----------------------------------------------------------------------|
| 15    | 15                                             | 0.230769231     | 3.461538462                                                           |
| 20    | 20                                             | 0.307692308     | 6.153846154                                                           |
| 25    | 30                                             | 0.461538462     | 11.53846154                                                           |
|       | **Totalt:** 65, som er summen av vekten |                 | **Totalt:** 21,5384615, som avrundes til 21 (som er det nærmeste intervallet) |

## <a name="what-if-the-batches-have-different-batch-dates"></a>Hva om bunkene har forskjellige bunkedatoer?
Hvis partiene har forskjellige partidatoer, beregnes noen av datoene basert på verdiene i gruppen **Partidatoer** i hurtigkategorien **Sammenslått parti** på siden **Partisammenslåing**. Systemet beregner verdier for feltene i gruppen **Partidatoer**. Disse verdiene inkluderer produksjonsdato, utløpsdato, anbefalt holdbarhet og best før-dato. Datoer beregnes basert på innstillingene for varen i feltghruppen **Varedata** på siden **Detaljer om frigitt produkt**. Du kan endre verdiene eller angi dem manuelt. Ingen beregninger utføres for alle andre datoer. Det samme prinsippet brukes for partiattributtverdier. Hvis en dato er den samme for alle kildepartiene, foreslås denne datoen for det sammenslåtte partiet. Hvis datoen ikke er den samme for alle kildepartier, er datoen tom for det sammenslåtte partiet, du kan angi den manuelt.

## <a name="what-if-the-dimensions-are-different-on-the-batches-that-i-want-to-merge"></a>Hva om dimensjonene er forskjellige på bunkene som jeg vil slå sammen?
Produktdimensjoner, sporingsdimensjoner og lagringsdimensjoner håndteres på følgende måte:

-   **Produktdimensjoner** – Alle produktdimensjoner for den valgte varen må være like. Du kan ikke slå sammen partier på tvers av produktdimensjoner.
-   **Sporingsdimensjoner** – Et nytt partinummer genereres automatisk hvis det er angitt en partinummergruppe for varen. Hvis en partinummergruppe ikke er tilordnet en vare, kan du velge et eksisterende parti eller angi nummeret manuelt. Serienumre overføres fra kildepartiet til lagerjournallinjene for det sammenslåtte partiet.
-   **Lagringsdimensjoner** – Området og lageret må være de samme for alle kildepartiene og det sammenslåtte partiet. Du kan imidlertid angi en ny lokasjon og pall-ID for det sammenslåtte partiet.

## <a name="how-does-posting-work"></a>Hvordan fungerer postering?
Postering fungerer på to måter, avhengig av om du bruker en godkjenningsprosess for journaler. Du kan bruke knappene **Overfør til journal** og **Poster partisammenslåingen** til å overføre partisammenslåing til en journal der den kan bekreftes og posteres, eller du kan postere partisammenslåingen direkte. Den største forskjellen mellom de to handlingene er at en overføring til en journal ikke posterer partisammenslåingen. Begge handlingene oppretter et nytt parti hvis et eksisterende parti ikke er valgt, oppdaterer alle partidetaljer og attributtverdier og oppretter en lagerjournal.

-   **Overfør til journal** – Overfører informasjon om partisammenslåingen til en lagerjournal. Hvis du har definert automatiske reservasjoner, er antallene i kildepartiene reservert. Detaljene for partisammenslåingen kan ikke endres. Hvis du må endre partisammenslåingen, må du slette journalen. Journalen kan brukes som en oppgave som en annen ansatt må utføre senere. Reservering av partiantallet til journallinjen er sikret. Denne tildelingen gjør det mulig for en kvalitetsplanlegger eller en lagersjef å opprette oppgaver for de ansatte.
-   **Poster partisammenslåingen** – Posterer partisammenslåingen direkte. Denne handlingen kan utføres etter at den fysiske sammenslåingen er foretatt.

Du kan godkjenne lagerjournalen for partisammenslåingen fra listesiden **Alle partisammenslåinger**. Klikk **Journal**&gt;**Post**. Når en journal er bokført, kan du ikke endre detaljene i det sammenslåtte partiet. Når du har overført en partisammenslåing til en lagerjournal, kan du bare endre detaljene hvis journalen er slettet.

## <a name="after-i-merged-a-catchweight-item-why-cant-i-see-the-catchweight-information-in-the-inventory-journal"></a>Etter at jeg har flettet en catchweight vare, Hvorfor kan jeg ikke se catchweight informasjonen i lagerjournalen?
Du kan slå sammen partier med faktisk vekt-varer på samme måte som alle andre varer. Informasjon om faktisk vekt vises imidlertid ikke i lagerjournalen. Vi anbefaler at du kontrollerer informasjonen for faktisk vekt før du overfører pafrtisammenslåingen til lagerjournalen.


