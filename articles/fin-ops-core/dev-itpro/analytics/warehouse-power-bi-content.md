---
title: Lagerytelse-innhold for Power BI
description: Dette emnet beskriver hva som er inkludert i Lagerytelse-innhold for Power BI. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.
author: Mirzaab
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: WHSWarehousePerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 272953
ms.assetid: 4e4d4323-78cf-4ffa-8d5a-05e856c33db6
ms.search.region: Global
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: b5fbe5ffa74953588a2357948319f5cf21f7ad36
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769767"
---
# <a name="warehouse-performance-power-bi-content"></a>Lagerytelse-innhold for Power BI

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hva som er inkludert i **Lagerytelse**-innhold for Microsoft Power BI. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="overview"></a>Oversikt

**Lagerytelse**-innholdet for Power BI ble opprettet, slik at lager- og driftsledere kan overvåke viktige mål for inngående, utgående og beholdning. Det bruker data for lagerstyring, produkt og andre transaksjonsdata fra systemet, og inneholder både en aggregert visning av lagerytelse og en analyse for leverandører, produktgrupper og varer, og område og lagre.

Lagerledere kan bruke **Lagerytelse**-innholdet for Power BI til å måle følgende tre områder:

- **Innkommende ytelse** – Måler leverandørytelse i forhold til kundekrav (altså måler leveringsytelse), måler leveringsytelse og måler plasseringsytelse, slik at du kan identifisere problemer som omfatter arbeidere eller varer i en periode. Det er viktig at du vet om leverandører leverer i tide, for tidlig eller for sent, slik at du kan fastslå hvordan leverandørytelse påvirker overordnet plasseringsytelse. En leverandør som leverer utenfor datoene som ble avtalt, kan legge ekstra press på lageret på grunn av uventet arbeid og kan øke gjennomsnittstiden for plassering.
- **Leveringsytelse** – Måler om lageret leverer i sin helhet og innenfor tidsfristen til kunder (altså måler utgående forsendelses- og leveringsytelse), slik at du kan identifisere problemer som omfatter produkter, områder, lagre eller dedikerte kunder. Hvis du finner ut at du har forsinkede forsendelser til bestemte områder og byer, må du kanskje være mer oppmerksom på transport- eller kontostyring.
- **Lagerpresisjon for lokasjon** – Lagerpresisjon er viktig, intern lagerforretningsanalyse (BI). Det er svært viktig at du fastslår hvor nøyaktig du teller generelt. Det er imidlertid også viktig at du fastslår hvor nøyaktig du med hensyn til lagring av varer på riktig sted, og at du merker avviksdata, slik at du kan finne bedre posisjoner for varer eller starte totalantall på bestemte varer. (For øyeblikket leveres den nye varebaserte tellefunksjonaliteten som en hurtigreparasjon.) Hvis du bruker dette Power BI-innholdet til å fastslå korrektheten til lagerbeholdningsdata per lokasjon, kan du også identifisere tyveri i butikkene dine. Du kan også fastslå om lokasjoner har lagerbeholdningsantall som avviker fra ERP-data. Disse lokasjonene kan være for store, eller de kan være umulig å telle. Noen av de fysiske plasseringene kan også være dårlige, slik at det er vanskelig å synkronisere én enkelt type vare med beholdningsdata.

## <a name="accessing-the-power-bi-content-pack"></a>Tilgang til Power BI-innholdspakken
Power BI-innholdet **Lagerytelse** vises på **Lagerytelse**-siden (**Lagerstyring** \> **Forespørsler og rapporter** \> **Analyse av lagerytelse** \> **Lagerytelse**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mål som er inkludert i Power BI-innholdet
**Lagerytelse**-innholdet for Power BI omfatter en rapport. Denne rapporten består av et sett med mål som er visualisert som diagrammer, fliser og tabeller. Tabellen nedenfor gir en oversikt over visualiseringene i Power BI-innholdet **Lagerytelse**.

| Rapportside                 | Diagrammer                                   | beskrivelse |
|-----------------------------|------------------------------------------|-------------|
| Innkommende ytelse         | Plasseringer totalt                          | Antall arbeidslinjer for plassering som behandles i en gitt tidsperiode. |
| Innkommende ytelse         | Gjennomsnittstid for plassering                    | Gjennomsnittstid, i timer, for alle bestillingslinjer for plassering som behandles, fra registrering av varene til den siste plasseringen er behandlet. |
| Innkommende ytelse         | Mottatt tidlig                           | Antall bestillingslinjer som blir mottatt tidlig. |
| Innkommende ytelse         | Mottatt i tide                         | Antall bestillingslinjer som blir mottatt til planlagt tid. |
| Innkommende ytelse         | Mottatt sent                            | Antall bestillingslinjer som blir mottatt for sent. |
| Innkommende ytelse         | Til planlagt tid etter leverandør                        | En visning av prosentdelen av bestillingslinjene som er mottatt til fra en leverandør eller leverandørgruppe for tidlig, til planlagt tid for sent. |
| Innkommende ytelse         | Gjennomsnittlig mottakssone til lager-plassering (timer) | Gjennomsnittlig tid for mottakssone til lager-plassering i timer over tid. |
| Innkommende ytelse         | Gjennomsnitt plassering etter arbeider               | Gjennomsnittstid, i timer, som en arbeider har brukt på plasseringsbehandling av bestillingslinjer. |
| Innkommende ytelse         | Gjennomsnittlig plasseringstid i timer for plassering etter leverandør          | Gjennomsnittlig plasseringstid i timer etter leverandør eller leverandørgruppe. |
| Innkommende ytelse         | Gjennomsnittlig plasseringstid i timer for plassering etter produkt         | Gjennomsnittlig plasseringstid i timer etter vare eller varegruppe. |
| Lagerpresisjon for lokasjon | Totalt antall                              | Antall tellende arbeidslinjer som behandles i en gitt periode. |
| Lagerpresisjon for lokasjon | Avvikssats                         | Total avvikssats som en prosent av alle linjene som telles for en gitt periode. |
| Lagerpresisjon for lokasjon | Antall uten avvik                | Av det totale antallet av tellende arbeidslinjer som behandles, antall linjer som behandles uten avvik. |
| Lagerpresisjon for lokasjon | Varer talt over tid                  | Prosenten av varene som er talt opp med og uten avvik over tid. |
| Lagerpresisjon for lokasjon | Antallsavvik for vare som er større enn % | En tabellvisning av tellende linjer med avvik som overskrider en angitt prosent. Tabellen inneholder informasjon om lokasjoner, varer, gjennomsnittlig avvik, totalt antall tellende arbeidslinjer som er talt opp, antall tellende linjer med avvik for lokasjonen, gjennomsnittsantall som er talt, forventet totalt antall som skal telles, og faktisk vareantall som er talt. |
| Lagerpresisjon for lokasjon | Vareantall etter arbeider                     | Opptellingsytelsen til arbeidere. Ytelsen er uttrykt som en prosent av tellende arbeidslinjer som har og ikke har avvik. |
| Lagerpresisjon for lokasjon | Vareopptelling etter område/lager           | Opptellingsytelse per antall behandlede tellende arbeidslinjer etter område eller lager som har og ikke har avvik. |
| Lagerpresisjon for lokasjon | Avvikssats etter produkt              | Avvikssats for opptellingsytelse. Satsen uttrykkes som en prosent av behandlede tellende arbeidslinjer etter vare eller varegruppe. |
| Leveringsytelse        | Linjer sendt                            | Totalt antall forsendelseslinjer som er sendt i en gitt periode. |
| Leveringsytelse        | For tidlig                                    | Prosenten av forsendelseslinjene som er sendt tidlig. |
| Leveringsytelse        | Til planlagt tid                                  | Prosenten av forsendelseslinjene som er sendt til planlagt tid. |
| Leveringsytelse        | For sent                                     | Prosenten av forsendelseslinjene som er sendt for sent. |
| Leveringsytelse        | Forsendelser over tid                      | Prosenten av forsendelseslinjer som er levert til planlagt tid, tidlig eller for sent i en gitt periode. En trendlinje viser trenden for linjer som er levert til planlagt tid. |
| Leveringsytelse        | Sendt for sent etter poststed                     | En kartvisning av byer og områder som påvirkes av forsinkede leveringer. |
| Leveringsytelse        | Sendt etter produkt                       | Prosentandelen som er sendt ut tidlig, til planlagt tid eller for sent, etter vare eller varegruppe. |
| Leveringsytelse        | Levering etter kunder                      | Prosentandelen som er sendt ut tidlig, til planlagt tid eller for sent etter kunde eller kundegruppe. |
| Leveringsytelse        | Levert etter område/lager              | Prosentandelen som er sendt ut tidlig, til planlagt tid eller for sent, etter område eller lager. |

## <a name="understanding-the-data-model-and-calculations"></a>Forstå datamodellen og beregningene
Følgende data brukes til å fylle ut rapportsidene i **Lagerytelse**-innholdet for Power BI. Disse dataene vises som aggregerte mål som er oppsamlet i enhetslageret. Enhetslageret er en Microsoft SQL Server-database som er optimalisert for analyse. Hvis du vil ha mer informasjon, se [Power BI-integrering med enhetslager](power-bi-integration-entity-store.md).

De aggregerte nøkkelmålingene som du finner nedenfor, brukes som grunnlag for innholdet.

| Rapportside                 | Diagrammer                                   | Tabeller                                | Beskrivelser for beregning |
|-----------------------------|------------------------------------------|---------------------------------------|--------------------------|
| Innkommende ytelse         | Plasseringer totalt                          | WHSWorkLine                           | Antall arbeidslinjer av arbeidstypen **plassert**. |
| Innkommende ytelse         | Gjennomsnittstid for plassering                    | WHSWorkLine                           | Summen av arbeidslinjers maks.tid delt på maks.tid for antall arbeidslinjer, der maks.tid for arbeidslinjer er den største forskjellen mellom endringsdato og lukkingsdato for arbeidet. |
| Innkommende ytelse         | Mottatt tidlig                           | WHSWorkLine                           | Antall arbeidslinjer der opprettingsdato for arbeidet er før leveringsdatoen som brukes. Hvis bekreftelsesdatoen for levering ikke er angitt, kan du bruke standard leveringsdato. |
| Innkommende ytelse         | Mottatt i tide                         | WHSWorkLine                           | Antall arbeidslinjer der opprettingsdato for arbeidet er lik leveringsdatoen som brukes. Hvis bekreftelsesdatoen for levering ikke er angitt, kan du bruke standard leveringsdato. |
| Innkommende ytelse         | Mottatt sent                            | WHSWorkLine                           | Antall arbeidslinjer der opprettingsdato for arbeidet er senere enn leveringsdatoen som brukes. Hvis bekreftelsesdatoen for levering ikke er angitt, kan du bruke standard leveringsdato. |
| Innkommende ytelse         | Til planlagt tid etter leverandør                        | WHSWorkLine                           | Mottatt tidlig, Mottatt i tide og Mottatt sent (se beskrivelsene tidligere i denne tabellen). |
| Innkommende ytelse         | Gjennomsnittlig mottakssone til lager-plassering (timer)   | WHSWorkLine                           | Gjennomsnittstid for plassering (se beskrivelsen tidligere i denne tabellen). |
| Innkommende ytelse         | Gjennomsnitt plassering etter arbeider               | WHSWorkLine                           | Gjennomsnittstid for plassering (se beskrivelsen tidligere i denne tabellen). |
| Innkommende ytelse         | Gjennomsnittlig plasseringstid i timer for plassering etter leverandør          | WHSWorkLine                           | Gjennomsnittstid for plassering (se beskrivelsen tidligere i denne tabellen). |
| Innkommende ytelse         | Gjennomsnittlig plasseringstid i timer for plassering etter produkt         | WHSWorkLine                           | Gjennomsnittstid for plassering (se beskrivelsen tidligere i denne tabellen). |
| Lagerpresisjon for lokasjon | Totalt antall                              | WHSWorkLineCycleCount                 | Syklusantall der absolutt avviksantall er lik eller større enn 0 (null). |
| Lagerpresisjon for lokasjon | Avvikssats                         | WHSWorkLineCycleCount                 | Syklusantall med avvik, delt på hvor totalantall. Et syklusantall anses å ha avvik hvis det absolutte avviksantallet er større enn 0 (null). |
| Lagerpresisjon for lokasjon | Antall uten avvik                | WHSWorkLineCycleCount                 | Syklusantall der absolutt avviksantall er større enn 0 (null). |
| Lagerpresisjon for lokasjon | Antall med avvik                   | WHSWorkLineCycleCount                 | Syklusantall der absolutt avviksantall er lik 0 (null). |
| Lagerpresisjon for lokasjon | Varer talt over tid                  | WHSWorkLineCycleCount                 | Antall uten avvik og antall med avvik (se beskrivelsene tidligere i denne tabellen.) |
| Lagerpresisjon for lokasjon | Antallsavvik for vare som er større enn % | WHSWorkLineCycleCount                 | Gjennomsnittlig avviket er det absolutte avviksantallet dividert med det forventede antallet der det absolutte avviksantallet er større enn 0 (null). Gjennomsnittlig avviksantall er det gjennomsnittlige absolutte avviksantallet der det absolutte avviksantallet er større enn 0 (null). Antall med avvik, totalt antall, forventet antall og opptalt antall der hele antallet er gruppert etter vare og lokasjon (se beskrivelsene tidligere i denne tabellen). |
| Lagerpresisjon for lokasjon | Vareantall etter arbeider                     | WHSWorkLineCycleCount                 | Antall uten avvik og antall med avvik (se beskrivelsene tidligere i denne tabellen). |
| Lagerpresisjon for lokasjon | Vareopptelling etter område/lager           | WHSWorkLineCycleCount                 | Antall uten avvik og antall med avvik (se beskrivelsene tidligere i denne tabellen). |
| Lagerpresisjon for lokasjon | Avvikssats etter produkt              | WHSWorkLineCycleCount                 | Avvikssats (se beskrivelsen tidligere i denne tabellen). |
| Leveringsytelse        | Linjer sendt                            | SalesLine               | Antall salgslinjer der salgslinjer er levert. |
| Leveringsytelse        | For tidlig                                    | CustPackingSlipOnTimeStatus           | Salgslinjer der statusen for forsendelsesdato er **1 (tidlig)**. Tidlig betyr at forsendelsesdatoen for følgeseddelen er tidligere enn den bekreftede forsendelsesdatoen på salgslinjen. Hvis bekreftet forsendelsesdato ikke er satt, bruker du ønsket forsendelsesdato. |
| Leveringsytelse        | Til planlagt tid                                  | CustPackingSlipOnTimeStatus           | Salgslinjer der statusen for forsendelsesdato er **2 (til planlagt tid)**. Til planlagt tid betyr at forsendelsesdatoen for følgeseddelen er lik den bekreftede forsendelsesdatoen på salgslinjen. Hvis bekreftet forsendelsesdato ikke er satt, bruker du ønsket forsendelsesdato. |
| Leveringsytelse        | For sent                                     | CustPackingSlipOnTimeStatus           | Salgslinjer der statusen for forsendelsesdato er **3 (sent)**. Sent betyr at forsendelsesdatoen for følgeseddelen er senere enn den bekreftede forsendelsesdatoen på salgslinjen. Hvis bekreftet forsendelsesdato ikke er satt, bruker du ønsket forsendelsesdato. |
| Leveringsytelse        | Forsendelser over tid                      | SalesLine CustPackingSlipOnTimeStatus | Bestillinger som er fullstendig levert, der alle salgslinjene er levert, pluss Tidlig, Til planlagt tid og Sent (se beskrivelsene tidligere i denne tabellen). |
| Leveringsytelse        | Sendt for sent etter poststed                     | CustPackingSlipOnTimeStatus           | Sent (se beskrivelsene tidligere i denne tabellen). |
| Leveringsytelse        | Sendt etter produkt                       | CustPackingSlipOnTimeStatus           | Tidlig, Til planlagt tid og Sent (Se beskrivelsene tidligere i denne tabellen). |
| Leveringsytelse        | Levering etter kunder                      | CustPackingSlipOnTimeStatus           | Tidlig, Til planlagt tid og Sent (Se beskrivelsene tidligere i denne tabellen). |
| Leveringsytelse        | Levert etter område/lager              | CustPackingSlipOnTimeStatus           | Tidlig, Til planlagt tid og Sent (Se beskrivelsene tidligere i denne tabellen). |
