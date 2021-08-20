---
title: Lagerbeholdningsliste
description: Dette emnet beskriver hvordan du bruker siden Beholdningsliste til å kontrollere lagerbeholdningsdetaljer. Den viser noen av måtene de ulike filtrerings- og sorteringsalternativene fungerer sammen, og hvordan disse alternativene kan føre til uventede resultater når de kombineres.
author: sherry-zheng
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnhandItem, InventOnHandItemListPage, WHSOnHand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cd90b3c8b84aa969f93015f8c953105db1636902c7dcf1d3150356284efa302b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780228"
---
# <a name="inventory-on-hand-list"></a>Lagerbeholdningsliste

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du bruker siden **Beholdningsliste** til å kontrollere lagerbeholdningsdetaljer. Den viser noen av måtene de ulike filtrerings- og sorteringsalternativene fungerer sammen, og hvordan disse alternativene kan føre til uventede resultater når de kombineres.

## <a name="query-your-on-hand-inventory"></a>Spørre lagerbeholdningen

Hvis du vil kontrollere tilgjengeligheten av lagerbeholdningen, kan du gå til **Lagerstyring \> Forespørsler og rapporter \> Beholdningsliste**.

Siden **Beholdningsliste** oppdateres automatisk når det gjøres transaksjoner i lageret. Disse transaksjonene kan være prognostiserte, fysiske eller finansielle transaksjoner.

Bruk følgende verktøy til å finne produktsettet du søker etter:

- I handlingsruten velger du [**Dimensjoner**](#dimensions) for å åpne en dialogboks der du kan legge til eller fjerne kolonner som vises i rutenettet **Beholdning**.
- I [**Filtre**-ruten](#filters-pane) angir du verdier for bestemte felt for å vise bare poster som samsvarer med disse verdiene. Legg merke til at filtre som du definerer her, gjelder for kildetabeller som kan aggregeres senere, i henhold til dimensjonene du har valgt å vise. Hvis du vil ha informasjon om hvordan denne virkemåten kan påvirke resultatene, se [eksemplene](#examples) senere i dette emnet.
- I **Filtre**-ruten velger du **Bruk** for å generere listen over samsvarende lagerbeholdning i rutenettet **Beholdning**.
- I rutenettet **Beholdning** velger du en kolonneoverskrift for å sortere eller filtrere etter verdier i denne kolonnen. Et hurtigfilter øverst i rutenettet inneholder flere filtreringsalternativer. Disse filtrene gjelder for resultatene, ikke for kildetabellene. Hvis du vil ha informasjon om hvordan denne virkemåten kan påvirke resultatene, se [eksemplene](#examples) senere i dette emnet.

For hver samsvarende vare inneholder **Beholdning**-rutenettet følgende kolonner med lagerinformasjon:

| Stående stolpe | beskrivelse |
|---|---|
| Aktuell beholdning | Fysisk antall som er tilgjengelig på lageret. |
| Fysisk reservert | Det totale antallet som er fysisk reservert. |
| Fysisk tilgjengelig | Det tilgjengelige (ikke reserverte) antallet som er tilgjengelig på det fysiske lageret.<p>**Fysisk tilgjengelig** er et beregnet felt. Verdien er lik verdien for **Fysisk lager** minus verdien for **Fysisk reservert**.</p> |
| Fysisk tilgjengelig på ekstra dimensjoner | Det fysisk tilgjengelige antallet for alle dimensjonene som vises i rutenettet. |
| Bestilt i alt | Det totale antallet som er inkludert på inngående ordrer, eller som har et positivt antall i forskjellige lagerjournaler. |
| I ordre/bestilling | Det totale antallet som er inkludert på utgående ordrer, eller som har et negativt antall i forskjellige lagerjournaler. |
| Reservert av bestilt | Det totale antallet som er reservert på bestilte mottak. Verdien i dette feltet representerer totalt antall varer i utgående transaksjoner med statusen _Reservert av bestilt_. Varer som er reservert som bestilt, er fysisk ikke tilgjengelig på lageret. De kan derfor ikke plukkes og leveres direkte. |
| Tilgjengelig for reservasjon | Det totale antallet lagerbeholdning som kan reserveres.<p>**Obs!** Hvis det er merket av for **Reserver bestilte varer** på siden **Parametere for beholdnings- og lagerstyring**, inneholder verdien i dette feltet forventede mottak. Hvis merket er fjernet i avmerkingsboksen, utelater verdien forventede mottak.</p> |
| Totalt tilgjengelig | Det totalt tilgjengelige antallet.<p>**Totalt tilgjengelig** er et beregnet felt. Verdien er lik verdien for **Fysisk tilgjengelig** pluss verdien for **Bestilt i alt** minus verdien for **På bestilling**.</p> |

## <a name="apply-filters-to-find-the-records-that-youre-looking-for"></a><a name="filters-pane"></a>Bruke filtre til å finne postene du leter etter

Bruk **Filtre**-ruten til å filtrere lagerbeholdningslisten slik at den bare inkluderer poster der feltverdiene samsvarer med filtreringskriteriene. Følg trinnene for å definere et filter.

1. Finn feltet du vil filtrere på, i **Filtre**-ruten.
2. I feltet under navnet på målfeltet velger du en logisk operator (for eksempel *begynner med*, *er lik* eller *større enn*).
3. Angi eller elg verdien du skal lete etter.

> [!IMPORTANT]
> Siden **Beholdningsliste** er satt sammen fra en detaljert lagerbeholdningstabell som inkluderer alle tilgjengelige dimensjoner. Listen på denne siden er imidlertid et sammendrag. Derfor kan den kombinere rader fra kildetabellen ved å samle verdier i henhold til dimensjonene som vises.
>
> Filtrene du definerer i **Filtre**-ruten, gjelder for kildetabellen, ikke for den aggregerte listen. Denne virkemåten kan noen ganger gi uventede resultater. Hvis du vil ha informasjon om hvordan denne virkemåten kan påvirke resultatene, se [eksemplene](#examples) senere i dette emnet.
> 
> [Filtrene som oppgis i rutenettet](#grid-filters), *gjelder* imidlertid for den aggregerte listen. Disse filtrene inkluderer både hurtigfilteret øverst i rutenettet og filteret for hver kolonneoverskrift.

Du kan endre filtersettet som er tilgjengelig i **Filtre**-ruten, ved å følge disse trinnene.

- Hvis du vil fjerne et filter fra ruten, velger du **Lukk**-knappen (**X**).
- Hvis du vil legge til et filter, velger du **Legg til** øverst i **Filtre**-ruten. Dialogboksen **Legg til filterfelt** som vises, viser en liste over de tilgjengelige feltene. Den viser også informasjon om datatypen og tabellen for hvert felt. Bruk kolonneoverskriftene til å filtrere og sortere listen etter behov, og merk deretter av for hvert felt du vil legge til i **Filter**-ruten. Når du er ferdig, velger du **Sett inn** for å bruke endringene.

## <a name="select-which-dimensions-to-show"></a><a name="dimensions"></a>Velg hvilke dimensjoner som skal vises

Dimensjoner forteller deg mer om hver vare i lagerbeholdningslisten, og gir deg flere måter å sortere og filtrere listen på. Dimensjonene du velger å vise, påvirker også hvordan rader samles på siden **Beholdningsliste**. Denne aggregeringen kan i sin tur påvirke hvordan rader fra kildetabellene kombineres i resultatene du ser. Hvis du vil ha informasjon om hvordan denne virkemåten kan påvirke resultatene, se [eksemplene](#examples) senere i dette emnet.

Hvis du vil tilpasse valget av lagerdimensjonene som vises, følger du disse trinnene.

1. Klikk på **Dimensjoner** i handlingsruten.

    Dialogboksen **Dimensjonsvisning** som vises, viser hver dimensjon.

2. Merk av i avmerkingsboksen for hver dimensjon du vil ta med i rutenettet.
3. Hvis du vil at ditt valg skal brukes som standard neste gang du åpner siden **Beholdningsliste**, setter du alternativet for **Lagre oppsett** til **Ja**. Hvis du setter dette alternativet til **Nei**, vil valget bare bli brukt i gjeldende økt. Neste gang du åpner siden, brukes derfor gjeldende standardvalg.
4. Velg **OK** for å lukke dialogboksen og ta i bruk endringene.

## <a name="filter-on-the-output-of-the-inventory-on-hand-list"></a><a name="grid-filters"></a>Filtrere på utdataene til lagerbeholdningslisten

Du kan velge enhver kolonneoverskrift i rutenettet **Beholdning** for å sortere eller filtrere etter verdier i denne kolonnen. Et hurtigfilter øverst i rutenettet inneholder flere filtreringsalternativer. Disse filtrene gjelder for resultatene, ikke for kildetabellene. Hvis du vil ha informasjon om hvordan denne virkemåten kan påvirke resultatene, se [eksemplene](#examples) senere i dette emnet.

> [!NOTE]
> Du kan ikke filtrere og sortere etter alle kolonner. De fleste av antallskolonnene inkluderer ikke sorterings- og filtreringskontroller, fordi de er beregnede felt. Kolonnen **I bestilling** er et unntak.

## <a name="examples"></a><a name="examples"></a>Eksempler

Systemet inneholder en detaljert (ikke oppsamlet) lagertabell som viser følgende lagerbeholdning.

| Varenummer | Nettsted | Lager | Aktuell beholdning | Fysisk tilgjengelig |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 2 | 2 | 2 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-1"></a>Scenario 1

Siden **Beholdningsliste** er satt opp til å vise følgende endelige dimensjoner:

- Varenummer
- Nettsted
- Lager

I **Filtre**-ruten er følgende filtreringskriterier definert:

- **Varenummer** \| **er nøyaktig** \| _IA0001_
- **Fysisk tilgjengelig** \| **er mindre enn eller lik** \| _1_

Dette er resultatet.

| Varenummer | Nettsted | Lager | Aktuell beholdning | Fysisk tilgjengelig |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-2"></a>Scenario 2

Siden **Beholdningsliste** er satt opp til å vise følgende endelige dimensjoner:

- Varenummer
- Nettsted

I **Filtre**-ruten er følgende filtreringskriterier definert:

- **Varenummer** \| **er nøyaktig** \| _IA0001_
- **Fysisk tilgjengelig** \| **er mindre enn eller lik** \| _1_

Dette er resultatet.

| Varenummer | Nettsted | Aktuell beholdning | Fysisk tilgjengelig |
|---|---|---|---|
| IA0001 | 1 | 2 | 2 |

Legg merke til at innstillingene i **Filtre**-ruten gjelder for den detaljerte (ikke oppsamlede) lagertabellen som vises i begynnelsen av denne delen. Vilkåret **Fysisk tilgjengelig** \| **er mindre enn eller lik** \| _1_ finner derfor to rader ra denne tabellen (første og tredje rad, som hver viser en verdi for **Fysisk tilgjengelig** på _1_). I dette scenariet er imidlertid ikke siden **Beholdningsliste** konfigurert til å vise **Lager**-dimensjonen. Derfor samler den de to opprinnelige radene til én resultatrad, fordi begge radene har identiske verdier i alle dimensjonene som vises. Denne raden ser ut til å være et brudd på filtreringskriteriet, fordi verdien for **Fysisk tilgjengelig** vises som _2_. Resultatet er imidlertid riktig, fordi innstillingene i **Filtre**-ruten gjelder for kildetabellen, ikke for den aggregerte tabellen som vises på siden **Beholdningsliste**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]