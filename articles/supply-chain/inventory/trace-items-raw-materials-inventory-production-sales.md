---
title: "Sporing av varer og råmaterialer i beholdning, produksjon og salg"
description: "Dette emnet beskriver hvordan du kan bruke varesporing til å identifisere hvor varer eller råmaterialer er brukt, er i bruk, eller vil bli brukt i produksjon og salgsprosesser."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30191
ms.assetid: fdd0939a-855c-430f-a684-94f3baea1df4
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7af00d0c66f70aa41cfab0ffccef39ba4c115803
ms.openlocfilehash: 98f5696cd6a279bdf0f8d9026a74e5a9bccd2f13
ms.contentlocale: nb-no
ms.lasthandoff: 03/09/2018

---

# <a name="item-and-raw-material-tracing-in-inventory-production-and-sales"></a>Sporing av varer og råmaterialer i beholdning, produksjon og salg

[!include[banner](../includes/banner.md)]


Dette emnet beskriver hvordan du kan bruke varesporing til å identifisere hvor varer eller råmaterialer er brukt, er i bruk, eller vil bli brukt i produksjon og salgsprosesser.

Sporingsfunksjonalitet for varer finnes på **Varesporing**-siden. Delene nedenfor beskriver hvordan du kan bruke varesporing og hva alternativene og begrensninger er.

## <a name="what-is-item-tracing"></a>Hva er varesporing?
Varesporing er et forretningsintelligensverktøy som gir oversikt over kilden og målet for varer og råmaterialer i forsyningskjeden. Produsenter kan spore varer, råvarer eller ingredienser tilbake til leverandøren, og fremover gjennom produksjon og salg av det ferdige produktet. Varesporing hjelper produsenter med å samsvare med forskriftsmessige krav, og hjelper også kvalitetsansvarlige og produksjonsledere med å analysere og utføre handlinger for å løse avvik i kvaliteten på produkter og materialer. Her er noen eksempler på hvordan produsenter kan bruke varesporing:

-   Finn ut hvor mange varer eller råvarer som som er på lager, og hvor på lageret de er.
-   Finne ut hvor mye av varen eller råvaren som er sendt, og til hvilke kunder den ble sendt til.
-   Identifiser eventuelle planlagte forsendelser som omfatter varen eller råvaren.
-   Finn produksjonsordrer som bruker varen eller råvaren og som er planlagt, pågår eller som er ferdigmeldt.
-   Finn ut hvor varen eller råvaren ble kjøpt.
-   Undersøke hvor en vare eller råvarer ble brukt i produksjonen av en annen vare.

## <a name="what-can-i-trace-and-are-there-any-limitations"></a>Hva kan jeg spore, og er det noen begrensninger?
Du kan spore historiske lagertransaksjoner for varer og råmaterialer basert på et varenummer og en sporingsdimensjon, for eksempel et serienummer, partinummer eller partinummer for leverandør. Du kan bare spore en vare eller råvare hvis den ikke har en tilordnet sporingsdimensjon. Siden sporing er basert på lagertransaksjoner, gjelder enkelte begrensninger når du skal spore varer. Det er for eksempel begrensninger knyttet til transaksjoner for prosjekter, anleggsmidler og detaljhandel. I tillegg vises koprodukter i sporingsdetaljene, men biprodukter er ikke inkludert. Sporingen omfatter alle lagertransaksjoner fra én plassering til en annen. Brukerne kan derfor synes at informasjonsmengden er overveldende. Sporingen vises for én juridisk enhet om gangen. Det finnes ingen funksjoner på tvers av konserner i en konsernintern kontekst. Du må starte en ny sporing for hvert firma der en vare er mottatt eller utløst.

## <a name="what-criteria-can-i-specify-for-an-item-trace"></a>Hvilke kriterier kan jeg angi for en varesporing?
Kriteriene som er nødvendige for en varesporing, er varenummeret, en sporingsdimensjon, for eksempel et partinummer- eller serienummer, og retningen. Følgende tabell beskriver kriteriene du kan bruke i en varesporing.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Feltgruppe</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Varenummer</td>
<td>Angi IDen for varen eller råvaren som du sporer.</td>
</tr>
<tr class="even">
<td>Produktdimensjoner</td>
<td>Valgfritt: Spor bestemte aspekter av produktdefinisjonen, for eksempel en konfigurasjon, størrelse, farge eller stil.</td>
</tr>
<tr class="odd">
<td>Sporingsdimensjoner</td>
<td>Angi et partinummer, partinummer for leverandør eller nummersporingsdimensjon. Når du bruker partinummeret som kriterium, vises partinummeret for leverandør hvis du har registrert denne informasjonen.</td>
</tr>
<tr class="even">
<td>Lagringsdimensjoner</td>
<td>Valgfritt: Spor varer som er lagret på et bestemt sted.</td>
</tr>
<tr class="odd">
<td>Periode</td>
<td>Valgfritt: Angi datoer for å begrense sporingen til en bestemt periode. Sporingsdetaljene viser bare dokumenter og transaksjoner som er opprettet mellom disse datoene.</td>
</tr>
<tr class="even">
<td>Forover eller bakover</td>
<td>Velg retningen for sporet. Du kan spore fremover eller bakover:
<ul>
<li><strong>Bakover</strong> – Spor nedstrøms for å identifisere kilden, antallet som blir værende på lager og alle produksjonsordrer som er minst delvis ferdigmeldt.</li>
<li><strong>Forover</strong> – Spor oppstrøms for å identifisere målet. Du kan finne salgsordrene og kundene som den sporede varen eller råvaren minst er delvis sendt til.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="what-information-is-included-in-the-trace-details"></a>Hvilken informasjon er inkludert i sporingsdetaljene?
Resultatene av en sporing vises i kronologisk rekkefølge i treet i hurtigkategorien **Detaljer** på siden **Varesporing**. Rekkefølgen varierer, avhengig av sporingsretningen. Detaljene omfatter alle transaksjoner fra innkjøp av varen fra leverandøren til salget av varen til kunden. Sporingsresultater omfatter også midlertidige produkter som er knyttet til varen eller sporingsdimensjonen som ble angitt i sporingskriteriene. Den øverste noden viser antallet av varen, i lagerenheten, som blir værende på lager, basert på lagringsdimensjonen som ble angitt i sporingskriteriene. **Obs!** Sporingsdetaljene er et øyeblikksbilde av informasjonen som var tilgjengelig da sporingen ble utført. Sporingsdetaljene oppdateres ikke hvis informasjonen endres etter at sporingen er utført.

## <a name="why-dont-some-nodes-contain-any-details"></a>Hvorfor inneholder ikke enkelte noder noen detaljer?
For å redusere mengden informasjon i sporingsdetaljene inneholder bare noden for den første forekomsten for varen eller råvaren detaljer. Hvis en valgt node ikke inneholder detaljer, kan du vise noden som inneholder detaljer, ved å klikke **Gå til sporet linje**. Du kan deretter gå tilbake til noden du forlot, ved å klikke **Gå tilbake**.

## <a name="can-i-view-only-a-particular-type-of-document-for-example-can-i-view-only-production-orders-customers-or-vendors"></a>Kan jeg vise bare en bestemt type dokument? Kan jeg for eksempel bare vise produksjonsordrer, kunder eller leverandører?
Ja, du kan åpne listesider som inneholder bare en bestemt type dokument eller transaksjon fra sporingsdetaljene. Du får tilgang til disse sidene fra menyelementet **Sporing** i handlingsruten, i gruppene **Vare**, **Salg**, **Kjøp**, **Produksjon** og **Kvalitet**. Hvis du for eksempel vil vise en liste over leverandørene i sporingsdetaljene, klikker du **Sporing** &gt; **Kjøp** &gt; **Leverandører**. Listesidene oppsummer dokumenter eller transaksjoner fra sporingsdetaljene. Listesidene **Ventende transaksjoner**, **Ventende ordrer** og **Ikke leverte salgsordrer** viser også informasjon som ikke er inkludert i sporingsdetaljene for salgsordrer. I tillegg viser de alltid resultatene per gjeldende dato, selv om et datointervall er angitt. Tabellen nedenfor beskriver tilleggsinformasjonen disse sidene kan inneholde.

| Lister                    | Beskrivelse                                                                                                                                                                                                                                                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ikke leverte salgsordrer | Vis salgsordrelinjer som ikke har blitt plukket, og som derfor ikke vises i sporingsdetaljene.                                                                                                                                                                                                                        |
| Ventende ordrer           | Vis alle ventende produksjonsordrer for den sporede varen, uavhengig av sporingsdimensjonene som ble brukt i sporingskriteriene. Du kan også vise ventende produksjonsordrer, der den sporede varen er en ingrediens og der ingen registreringer er gjort og ingen transaksjoner er ferdigmeldt for ordren. |
| Ventende transaksjoner     | Vis ventende lagertransaksjoner for den sporede varen som inneholder de angitte sporingsdimensjonene eller en tom sporingsdimensjon. Du kan også vise ventende lagertransaksjoner for varer og kombinasjoner av sporingsdimensjon eller en tom verdi i sporingsdetaljene.                                                |

## <a name="how-many-levels-can-i-trace-up-or-down-in-a-bom-or-formula"></a>Hvor mange nivåer kan jeg spore opp eller ned i en stykkliste eller formel?
Du kan spore ett nivå opp eller ned i en stykkliste eller formel. Hvis du for eksempel kjører en sporing på råmaterialer, kan du se det ferdige produktet og eventuelle koprodukter. Hvis du imidlertid sporer et koprodukt, omfatter ikke sporingsdetaljene det ferdige produktet.

## <a name="how-can-i-view-more-details-about-a-document-or-transaction-in-the-trace-details"></a>Hvordan kan jeg vise flere detaljer om et dokument eller en transaksjon i sporingsdetaljene?
I hurtigfanen **Detaljer** kan du på to måter vise mer informasjon om valgt dokument eller transaksjon i sporingsdetaljene, på følgende måter:

-   Når du velger en node i sporingsdetaljene i hurtigfanen **Detaljer**, viser de andre hurtigfanene på siden informasjon om dokumentet eller transaksjonen i noden.
-   Åpne siden med detaljer for dokumentet i en valgt node ved å klikke **Vis detaljer**. Hvis du for eksempel velger en node som beskriver en produksjonsordre og du klikker **Vis detaljer**, vises siden **Detaljer for produksjonsordrer**.

Enkelte hurtigfaner gir deg tilgang til mer informasjon om den valgte noden. På **Avvik**-hurtifganen kan du for eksempel klikke **Forespørsler** for å undersøke om det finnes en logg over avvik. I **Parti**-hurtigfanen kan du klikke **Beholdningsliste** for å vise faktisk beholdning som finnes på lager, og alle lagertransaksjonene for partiet.

## <a name="can-i-run-more-than-one-trace-and-then-compare-the-details"></a>Kan jeg kjøre flere sporinger og deretter sammenligne detaljene?
Når du har kjørt sporingen, kan du bruke følgende alternativer på knappen **Spor fra node** til å kjøre en ny sporing på transaksjonen i den valgte noden:

-   **Bakover** eller **Forover** – Start en ny sporing for den valgte noden og overskriv detaljene for gjeldende spor.
-   **Ny bakover** eller **Ny forover** – Start en ny sporing i et nytt vindu, og behold detaljene for gjeldende spor.

Hvis du vil bruke alternativet **Ny bakover** eller **Ny forover**, må du bruke funksjonen **Åpne i et nytt vindu** til å vise en ny sporing i et nytt vindu.

## <a name="can-i-save-the-trace-details"></a>Kan jeg lagre sporingsdetaljene?
Du kan lagre informasjonen i kategorien **Detaljer** som en XML-fil, ved å klikke på **Eksporter** under ****Sporing****-handlingen i handlingsruten. I tillegg til sporingsdetaljene inkluderer XML-filen også sporingskriteriene, den overordnede noden og beholdningsantallet. Det er nyttig å lagre sporingsdetaljer, for eksempel hvis du vil knytte informasjonen til en kvalitetsordre eller annen dokumentasjon for overensstemmelse. Du kan angi hvor filen skal lagres. Hvis du vil vise filen umiddelbart, merker du av for **Vis dokument**. **Obs!** Filen lagres alltid, selv om du bare vil vise den. XML-filen åpnes som standard i et nettleservindu. Du kan imidlertid høyreklikke filen, velge **Åpne med** og deretter velge programmet som skal brukes til å vise innholdet.

## <a name="can-i-calculate-a-balance-for-a-particular-item-or-ingredient"></a>Kan jeg beregne en saldo for en bestemt vare eller ingrediens?
Du kan eksportere informasjonen fra sammendragssidene til Microsoft Excel. Åpne den aktuelle siden, klikk ikonet **Åpne i Microsoft Office**, og velg deretter **Eksporter til Microsoft Excel**. Denne funksjonaliteten er spesielt nyttig når du vil beregne en massesaldo for en vare eller ingrediens fra siden **Transaksjonsammendrag**. På siden **Transaksjonssammendrag** kan du filtrere varen eller ingrediensen, og partiet hvis du vil, og deretter eksportere informasjonen til Excel. I Excel kan du for eksempel finne beholdningsantallet, antallet som ble solgt, og beløpet som ble brukt i produksjon.

## <a name="can-i-investigate-whether-there-is-a-history-of-issues-with-items-or-raw-materials"></a>Kan jeg undersøke om det er problemer med varer eller råvarer som går igjen?
Sporingsdetaljene inkluderer informasjon om kvalitetsordrer og avvik som gjelder varen eller råvarer. Du kan vise et sammendrag av kvalitetsordrer og avvik ved å klikke **Kvalitetsordrer** eller **Avvik** i handlingsruten. **Obs!** Destruktive kvalitetsordrer kan forekomme flere ganger i sporingsdetaljene. Når en destruktiv kvalitetsordre opprettes for et dokument, for eksempel en bestilling, vises den for hver transaksjon for dokumentet.

## <a name="are-there-any-reporting-capabilities-that-are-related-to-item-tracing"></a>Finnes det rapporteringsfunksjoner som er relatert til varesporing?
Du kan generere rapporten **Levert til kunder** for å identifisere hvor mye av varen eller råvaren som er sendt, og hvilke kunder den er sendt til. For en spørring som er knyttet til samsvar, kan du generere rapporten for alle kunder. For en spørring som er knyttet til kundeservice, kan du generere rapporten for en valgt kunde. Hvis produktet var råvare som ble brukt i produksjonen av en ferdigvare, blir ferdigvaren også tatt med. **Obs!** Hvis du bruker funksjonene for sletting eller arkivering av salgsordrer, inneholder rapportresultatene også salgsordrer som er slettet eller arkivert.

## <a name="can-i-trace-coproducts-and-byproducts"></a>Kan jeg spore koprodukter og biprodukter?
Du kan spore koprodukter, men du kan ikke spore et biprodukt fordi sporingsdimensjoner vanligvis ikke er tilordnet til biprodukter. Når du sporer en vare, inkluderes eventuelle relaterte koprodukter i sporingsdetaljene. En node som inneholder et koprodukt inneholder ordet "koprodukt" i detaljene. Du kan også vise detaljer om et koprodukt ved å velge noden i sporingsdetaljene og deretter klikke hurtigfanen **Produksjon**.

