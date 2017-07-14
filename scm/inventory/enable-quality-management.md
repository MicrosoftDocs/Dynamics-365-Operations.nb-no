---
title: Oversikt over kvalitetsstyring
description: "Denne artikkelen beskriver hvordan du kan bruke kvalitetsstyring i Microsoft Dynamics 365 for Finance and Operations for å forbedre produktkvalitet i forsyningskjeden."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: 255035bf13155190e59088a7f64f798c7462b885
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017


---

# Oversikt over kvalitetsstyring
<a id="quality-management-overview" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan du kan bruke kvalitetsstyring i Microsoft Dynamics 365 for Finance and Operations for å forbedre produktkvalitet i forsyningskjeden.

Kvalitetsstyring kan hjelpe deg med å administrere behandlingstiden når du håndterer produkter med avvik, uavhengig av opprinnelsespunktet. Fordi diagnosetyper er knyttet til rettelsesrapportering, kan Microsoft Dynamics 365 for Finance and Operations planlegge oppgaver for å rette opp problemer og hindre at de skjer igjen.

I tillegg til funksjonalitet for håndtering av avvik inneholder kvalitetsstyring funksjonalitet for å spore problemer etter problemtype (selv interne problemer) og identifisere løsninger som kortsiktige eller langsiktige. Statistikk om nøkkelytelsesindikator (KPI-er) gir innsikt i loggen for tidligere avviksproblemer og løsninger som ble brukt til å rette feilene. Du kan bruke historiske data for å undersøke effektiviteten til tidligere kvalitetsmål og bestemme nødvendige tiltak som skal brukes i fremtiden.

Når du definerer en kvalitetstilknytning, kan Finance and Operations generere kvalitetsordrer for diverse forretningsprosesser, hendelser og betingelser. Kvalitetstilknytningen kan dekke en bestemt vare, en bestemt varegruppe eller alle varer.

## Eksempler på bruk av kvalitetsstyring
<a id="examples-of-the-use-of-quality-management" class="xliff"></a>
Kvalitetsstyring er fleksibelt og kan implementeres på forskjellige måter for å oppfylle kravene til bestemte typer forsyningskjedeoperasjoner. Følgende eksempel viser mulig bruk av disse funksjonene.

-   Start en prosess for kvalitetskontroll automatisk basert på forhåndsdefinerte kriterier (ved lagerregistrering av en bestilling fra en bestemt leverandør).
-   Blokker lageret under inspeksjon for å hindre bruk av ikke-godkjent lager (full blokkering av bestillingsantall).
-   Bruk vareprøver som en del av en kvalitetstilknytning for å definere hvor mye av det fysiske lageret som må kontrolleres. Prøver kan være basert på faste antall eller en prosentdel.
-   Opprett testtyper med minimums-, maksimums-, og måltestverdier, og utfør kvalitative kontra kvantitative tester som har forhåndsdefinerte valideringsresultater.
-   Angi et akseptabelt kvalitetsnivå for å kontrollere kvalitetsmåltoleranser.
-   Angi ressursene som en inspeksjonsoperasjon krever, for eksempel et testområde og testinstrumenter.

## Arbeide med kvalitetstilknytninger
<a id="working-with-quality-associations" class="xliff"></a>
Forretningsprosessen som bruker en kvalitetstilknytning, kan knyttes til ulike kildedokumenter, for eksempel bestillinger, salgsordrer eller produksjonsordrer. 

Hver kvalitetstilknytningspost definerer settet med tester, det akseptable kvalitetsnivået og samplingplanen som gjelder for kvalitetsordrene som genereres. Du må definere en kvalitetstilknytningspost for hver variasjon i en forretningsprosess. Du kan for eksempel definere en kvalitetstilknytning som genererer en kvalitetsordre når et produkt for bestillingsmottak oppdateres. Avhengig av oppsettet for utførelsesplanen kan selve utløsingsprosessen blokkeres når det finnes en åpen kvalitetsordre, eller de neste prosessene, for eksempel bestillingsfakturering, kan blokkeres. 

**Merk:** Når det finnes åpne kvalitetsordrer, blokkeres lagerantall automatisk fra å bli utstedt. Avhengig av **Full blokkering**-innstillingen på siden **Vareprøver** er antallet enten antallet på kvalitetsordren eller antallet på kildedokumentlinjen. 

For en gitt forretningsprosess identifiserer kvalitetstilknytningspost hendelsen og betingelsene som en kvalitetsordre genereres for. Betingelsene kan være spesifikke for et område eller en juridisk enhet. En kvalitetsordre som omfatter destruktive tester, kan bare genereres når hvis det finnes lagerbeholdning for hendelsen. 

De følgende eksemplene illustrerer hvordan en kvalitetstilknytningspost er definert for variasjonene innen ulike forretningsprosesser. For hvert eksempel oppsummere følgende tabell hendelsene og betingelsene som er definert av en kvalitetstilknytningspost.

<table>
<tbody>
<tr>
<th>Referansetype</th>
<th>Hendelsestype</th>
<th>Utførelse</th>
<th>Hendelsesblokkering</th>
<th>Dokumentreferanse</th>
</tr>
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
<td>Ingen</td>
<td rowspan="3">Bestemt ID, Gruppe eller Alle, og Ressursspesifikk, Gruppe eller Alle</td>
</tr>
<tr>
<td>Ferdigmeld</td>
</tr>
<tr>
<td>Etter</td>
<td>Ingen</td>
</tr>
<tr>
<td rowspan="3">Koproduktproduksjon</td>
<td>Registrering</td>
<td>Gjelder ikke her</td>
<td rowspan="3">Ingen</td>
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

Tabellen nedenfor inneholder mer informasjon om hvordan kvalitetsordrer kan genereres for bestemte typer prosesser.
<div class="tableSection">

<table>
<tbody>
<tr>
<th>Type av prosess</th>
<th>Når kvalitetsordrer kan genereres automatisk</th>
<th>Når kvalitetsordrer kan genereres hvis destruktiv testing kreves</th>
<th>Betingelsesinformasjon</th>
<th>Informasjon om manuell generering</th>
</tr>
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
<td>Behovet for en kvalitetsordre kan reflektere et bestemt område eller en vare, eller en kombinasjon av disse betingelsene.</td>
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
<td>Beholdning</td>
<td>En kvalitetsordre kan ikke genereres automatisk for en transaksjon innen en lagerjournal eller for overføringsordretransaksjoner.</td>
<td></td>
<td></td>
<td>En kvalitetsordre må opprettes manuelt for en vares lagerantall. Varens fysiske lagerbeholdning kreves.</td>
</tr>
</tbody>
</table>

## Kvalitetsstyringssider
<a id="quality-management-pages" class="xliff"></a>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Side</th>
<th>Beskrivelse</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kvalitetstilknytninger</td>
<td>Se tidligere deler av denne artikkelen.</td>
<td>En kvalitetstilknytning definerer alle følgende opplysninger om en kvalitetsordre som er generert:
<ul>
<li>Transaksjonshendelsen</li>
<li>Settet med tester som må utføres på elementene</li>
<li>Det akseptable kvalitetsnivået</li>
<li>Prøveplanen</li>
</ul>
Du må definere en kvalitetstilknytning for hver variasjon i en forretningsprosess som krever automatisk generering av kvalitetsordrer. Eksempelvis kan en kvalitetsordre genereres i forretningsprosessen for bestillinger, karanteneordrer, salgsordrer og produksjonsordrer.</td>
</tr>
<tr class="even">
<td>Tester</td>
<td>Bruk denne siden til å definere og vise de individuelle testene som fastslår om produktene oppfyller kvalitetsspesifikasjoner. Du kan tilordne én eller flere individuelle tester til en testgruppe. I dette tilfellet må også angi testspesifikk informasjon, for eksempel de akseptable målingsverdiene. Målingsverdiene brukes for kvantitative tester, og testvariablene brukes for kvalitative tester.
<ul>
<li>En kvantitativ test har testtypen <strong>Heltall</strong> eller <strong>Brøk</strong> og har også en angitt måleenhet. Kvalitetsspesifikasjoner og testresultater uttrykkes som tall.</li>
<li>En kvalitativ test har testtypen <strong>Alternativ</strong>. Kvalitative tester krever mer informasjon om testvariabelen som måles, og de tilhørende opplistede alternativene. Kvalitetsspesifikasjoner og testresultater uttrykkes i henhold til et resultat.</li>
</ul></td>
<td>Et produksjonsfirma utfører to tester på innkjøpt materiale: en kvantitativ test om materialkvalitet og en kvalitativ test om emballasjeskade. Firmaet definerer tilleggsinformasjon om den kvalitative testen for å identifisere testvariabelen (skadet emballasje) og resultatene. Firmaet bruker <strong>Testgrupper</strong>-siden til å tilordne de to testene til en testgruppe og angi testspesifikk informasjon. Testgruppen tilordnes til en kvalitetsordre, slik at firmaet kan rapportere testresultater for de to testene.</td>
</tr>
<tr class="odd">
<td>Testgrupper</td>
<td>Bruk denne siden til å definere, redigere og vise testgrupper og de individuelle testene som er tilordnet til en testgruppe. Den øvre ruten viser testgrupper, og den nedre ruten viser testene som er tilordnet til en valgt testgruppe. Du tilordner flere policyer til en testgruppe, for eksempel en prøveplan, et akseptabelt kvalitetsnivå og kravet til destruktiv testing. Når du tilordner en individuell test til en testgruppe, definerer du tilleggsinformasjon, for eksempel sekvensen, dokumenter og gyldighetsdatoer. For en kvantitativ test inkluderer informasjonen du definerer, også de akseptable målingsverdiene. For en kvalitativ test inkluderer informasjonen testvariabelen og standardresultatet. Testgruppen som er tilordnet en kvalitetsordre, definerer standardsettet med tester som må utføres for den bestemte varen. Du kan imidlertid legge til, slette eller endre tester i kvalitetsordren. Testresultater rapporteres for hver test på en kvalitetsordre.</td>
<td>Et produksjonsfirma definerer en testgruppe for hver variasjon av retningslinjene for kvalitet. De ulike testgruppene gjenspeiler forskjeller i prøveplanene, settet med tester som må utføres sammen, det akseptable kvalitetsnivået og andre faktorer. For kvantitative tester er det også forskjeller i de akseptable målingsverdiene. Hvis du vil fremtvinge retningslinjene for kvalitet, tilordner firmaet en testgruppe til hver regel for automatisk generering av kvalitetsordrer på siden <strong>Kvalitetstilknytninger</strong>, og tilordner også en testgruppe til kvalitetsordrer som opprettes manuelt.</td>
</tr>
<tr class="even">
<td>Varekvalitetsgrupper</td>
<td>Bruk denne siden til å definere, redigere og vise varene som er tilordnet til en kvalitetsgruppe, eller kvalitetsgruppene som er tilordnet til en vare. En kvalitetsgruppe representerer felles testkrav for varer. Når du har definert testkravene på siden <strong>Testgrupper</strong>, kan du definere reglene for automatisk generering av kvalitetsordrer. For å forenkle prosessen kan du ikke definerer reglene for individuelle varer. I stedet definere du regler for en kvalitetsgruppe ved hjelp av siden <strong>Kvalitetstilknytninger</strong>. Du kan også bruke siden <strong>Varekvalitetsgrupper</strong> for en valgt kvalitetsgruppe for å tilordne relevante varer til denne gruppen. Du kan også bruke siden <strong>Varekvalitetsgrupper</strong> for en valgt vare for å tilordne relevante kvalitetsgrupper til varen.</td>
<td>Et produksjonsfirma kjøper inn ulike råmaterialer som har samme testkrav for innkommende inspeksjon. Firmaet definerer en kvalitetsgruppe og tilordner deretter varenumrene som er tilknyttet råvarene til denne gruppen. Senere kjøper selskapet en ny type råvarer som har samme testkrav. I stedet for å opprette nye testkrav for det nye materialet, legger firmaet til varenummeret for det nye materialet i den eksisterende kvalitetsgruppen. Det samme produksjonsfirmaet produserer også varer med samme krav til produksjonstesting, og leverer varer med samme krav til utføring av tester før forsendelse. Firmaet definerer to ekstra kvalitetsgrupper, og tilordner deretter de aktuelle varenumrene til hver gruppe.</td>
</tr>
<tr class="odd">
<td>Testvariabler</td>
<td>Bruk denne siden til å definere og vise variablene som er tilknyttet en kvalitativ test. For hver variabel kan du definere opplistede resultater som representerer de mulige alternativene. Du definerer testene på siden <strong>Tester</strong>. Du må sette testtypen for kvalitative tester til <strong>Alternativ</strong>. Bruk siden <strong>Testgrupper</strong> til å tilordne en testvariabel til en enkelt test.</td>
<td>En produksjonsfirma som produserer kjeks, bruker en inspeksjonstest til det ferdige produktet. Denne inspeksjonstesten har flere variabler. Én variabel er smak, og de mulige resultatene for denne variabelen er god og dårlig. En annen variabel er farge, og de mulige resultatene er for mørk, for lys og riktig.</td>
</tr>
<tr class="even">
<td>Testvariabelresultater</td>
<td>Bruk denne siden til å definere, redigere og vise de mulige testresultatene for en testvariabel som er knyttet til en kvalitetstest. For hvert resultat tilordner du statusen <strong>bestått</strong> eller <strong>mislykket</strong>. Du må definere en variabel og resultatene for hver kvalitative test som defineres på siden <strong>Tester</strong>. (For kvalitative tester er testtypen satt til <strong>Alternativ</strong> på <strong>Tester</strong>-siden.) Bruk <strong>Testgrupper</strong>-siden til å tilordne en testvariabel og standardresultatet til en enkelt kvalitetstest.</td>
<td>En produksjonsfirma som produserer kjeks, bruker en inspeksjonstest til det ferdige produktet. Denne inspeksjonstesten har flere variabler. Én variabel er smak, og de mulige resultatene for denne variabelen er god og dårlig. En annen variabel er farge, og de mulige resultatene er for mørk, for lys og riktig. Statusen <strong>bestått</strong> eller <strong>mislykket</strong> tilordnes hvert resultat. Under inspeksjonstesten for hver variabel rapporterer inspektøren testresultatet ved å velge ett av resultatene.</td>
</tr>
</tbody>
</table>



Se også
<a id="see-also" class="xliff"></a>
--------

[Kvalitetsstyringsprosesser](quality-management-processes.md)

[Aktivere behandling av avvik](enable-nonconformance-management.md)




