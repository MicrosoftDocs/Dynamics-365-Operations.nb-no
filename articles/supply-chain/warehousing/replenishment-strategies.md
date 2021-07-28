---
title: Etterfyllingsstrategier
description: Dette emnet inneholder informasjon om etterfyllingsstrategier, og forklarer hvordan du kan bruke Etterfyllingsstrategi-feltet på linje for etterfyllingsmaler for bølgebehov til å velge hvordan etterfylling skal utføres.
author: mirzaab
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-29
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: a8ddc7022a1e9a7db14aaa67efcd442025b0f9d8
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344479"
---
# <a name="replenishment-strategies"></a>Etterfyllingsstrategier

[!include [banner](../includes/banner.md)]

Malene som er definert på siden **Etterfyllingsmaler**, omfatter mallinjer for etterfylling av bølgebehov som lar deg velge hvordan etterfylling skal utføres. Hver linje inneholder nå et **Etterfyllingsstrategi**-felt.

Strategien *Bølgebehovsmengde* er standardstrategien. Det er etterfyllingsstrategien som ble brukt før innføringen av **Etterfyllingsstrategi**-feltet. Det bruker etterfyllingslokasjonsdirektiver til å finne lokasjoner som kan etterfylles. Deretter etterfylles disse lokasjonene til behovet er dekket.

Strategien *Maksimal stedskapasitet* introduserer ny funksjonalitet. På samme måte som strategien *Bølgebehovsmengde* bruker denne strategien etterfyllingslokasjonsdirektivet til å finne lokasjoner som kan etterfylles, og etterfyller deretter disse lokasjonene til behovet er dekket. Det er forskjellig fra strategien *Bølgebehovsmengde* i at alle etterfylte lokasjoner etterfylles til maksimal kapasitet, som definert av lagringsgrensene for lokasjon. Strategien *Maksimal stedskapasitet* prøver å opprette arbeid for å hente det forespurte antallet, pluss et ekstra antall, for å fylle lokasjonene som etterfylles. I noen tilfeller kan det imidlertid hende at forsøket mislykkes. Bulklokasjonene kan for eksempel ikke ha nok lager til å dekke det ekstra antallet. I disse tilfellene oppdager systemet feilen og forsøker å gjenopprette.

Høysesong er et eksempel på en situasjon der strategien *Maksimal stedskapasitet* foretrekkes over strategien *Bølgebehovsmengde*. Under høysesong kan noen varer selge ved høy volum. Derfor vil du kanskje proaktivt etterfylle de aktuelle plukklokasjonene så mye som mulig, for å redusere antall arbeids-ID-er som er opprettet for etterfylling.

> [!IMPORTANT]
> Hvis du vil utnytte strategien *Maksimal stedskapasitet*, må du omdefinere lagringsgrensene for de aktuelle lokasjonene. Hvis ikke fungerer denne strategien på samme måte som strategien *Bølgebehovsmengde*.

## <a name="turn-on-the-replenish-to-max-based-on-stocking-limits-feature"></a>Aktiver funksjonen for å etterfylle til maks. basert på lagringsgrense

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere statusen til denne funksjonen og aktivere den hvis den kreves. Funksjonen vises på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Etterfylle til maks. basert på lagringsgrense*

## <a name="set-up-replenishment-strategies"></a>Konfigurer etterfyllingsstrategier

For å gå tilgang til malene går du til **Lagerstyring \> Oppsett \> Etterfylling \> Etterfyllingsmaler**. I **Oversikt**-delen kan du velge eller opprette en etterfyllingsmal for bølgebehov der feltet **Etterfyllingstype** er satt til *Bølgebehov*. Deretter definerer du linjene for etterfyllingsmalen i delen **Detaljer for etterfyllingsmal**. For hver linje velger du etterfyllingsstrategien du vil bruke, i feltet **Etterfyllingsstrategi**.

![Etterfyllingsmaler-siden.](media/ReplenTempWaveDmdMaxLocCap.png "Etterfyllingsmaler-siden")

Hvis kolonnen **Etterfyllingsstrategi** ikke vises i rutenettet i delen **Detaljer for etterfyllingsmal**, må du kontrollere at funksjonen er aktivert, og at den valgte etter fyllingsmalen har etterfyllingstypen for *Bølgebehov*.

> [!NOTE]
> Strategien *Bølgebehovsmengde* er standardstrategien. Derfor trenger du bare å oppdatere linjene for etterfyllingsmalen der du vil bruke strategien *Maksimal stedskapasitet* i stedet.

## <a name="example-scenarios"></a>Eksempelscenarioer

### <a name="example-1"></a>Eksempel 1

I dette eksemplet finnes det bare én etter fyllingsmal som bare har én etter fyllingsmallinje.

Du oppretter en salgsordre for 130 stykker (stk) av varen A0001. Før du frigir ordren til lageret, konfigureres lageret på følgende måte:

- Det er bare én bulklokasjon, og den har 500 stykker tilgjengelig i lagerbeholdning.
- Det er tre plukklokasjoner, der hver har en lagringsgrense på 100 stk. (Husk at lagringsgrenser kreves for strategien *Maksimal stedskapasitet*.)
- Plasseringslokasjonene for etterfylling er de samme som salgsplukklokasjonene.
- Etterfyllingsenheten er en eske (1 eske = 20 stk.).

På tidspunktet ordren vises følgende lagerbeholdning ved salgsplukklokasjoner:

- **Plukk-001:** 20 stk. (1 eske)
- **Plukk-002:** 0 stk.
- **Plukk-003:** 0 stk.

Først settes etterfyllingsstrategien til *Bølgebehovsmengde*.

Når du har frigitt salgsordren til lageret og bølgebehandling kjører for bølgen, får du følgende etterfyllingsarbeid:

- **Etterfyllingsarbeid 1:** Plukk 4 esker fra bulklokasjonen, og plasser dem på lokasjon Plukk-001.
- **Etterfyllingsarbeid 2:** Plukk 2 esker fra bulklokasjonen, og plasser dem på lokasjon Plukk-002.

Du får to etterfyllingsarbeids-ID-er, fordi du må etterfylle to lokasjoner, og flere plasseringer støttes ikke.

Hvis du angir etterfyllingsstrategien til *Maksimal stedskapasitet* i stedet, får du følgende etterfyllingsarbeid:

- **Etterfyllingsarbeid 1:** Plukk 4 esker fra bulklokasjonen, og plasser dem på lokasjon Plukk-001.
- **Etterfyllingsarbeid 2:** Plukk 5 esker fra bulklokasjonen, og plasser dem på lokasjon Plukk-002.

[![Eksempel 1.](media/ReplenTemp_example_1.png "Eksempel 1")](media/ReplenTemp_example_1_large.png)

### <a name="example-2"></a>Eksempel 2

Dette eksemplet viser hva som skjer når bulklokasjonen ikke har nok lager til å dekke det ekstra antallet. Det bruker samme scenario som eksempel 1, men bulklokasjonen har 160 stk. (8 esker).

Strategien *Bølgebehovsmengde* oppretter det samme arbeidet som i eksempel 1.

Fordi strategien *Maksimal stedskapasitet* prøver å opprette arbeids-ID-ene slik den gjorde i eksempel 1, kan det imidlertid mislykkes. På dette tidspunktet prøver systemet å gjenopprette.

Avhengig av innstillingen for alternativet **Tillat deling** i lokasjonsdirektivene for etterfyllingsplukking, er to utfall mulige:

- Hvis alternativet **Tillat deling** er satt til *Ja*, opprettes følgende etterfyllingsarbeid:

    - **Etterfyllingsarbeid 1:** Plukk 4 esker fra bulklokasjonen, og plasser dem på lokasjon Plukk-001.
    - **Etterfyllingsarbeid 2:** Plukk 4 esker fra bulklokasjonen, og plasser dem på lokasjon Plukk-002.

- Hvis alternativet **Tillat deling** er satt til *Nei*, opprettes følgende etterfyllingsarbeid:

    - **Etterfyllingsarbeid 1:** Plukk 4 esker fra bulklokasjonen, og plasser dem på lokasjon Plukk-001.
    - **Etterfyllingsarbeid 2:** Plukk 2 esker fra bulklokasjonen, og plasser dem på lokasjon Plukk-002.

Resultatene er forskjellige på grunn av informasjonen som er tilgjengelig når du oppretter arbeidet. Når **Tillat deling** er satt til *Ja* i lokasjonsdirektivene for etterfyllingsplukking, vet du at du har klart å finne 160 stk. Du kan derfor opprette arbeid for dette antallet. Når alternativet **Tillat deling** er satt til *Nei*, vet du imidlertid ikke om eksistensen av 160 stk. Fordi det ekstra antallet du har bestemt å etterfylle, var 3 esker, dropper du det ekstra antallet og prøver det opprinnelige antallet på nytt.

[![Eksempel 2.](media/ReplenTemp_example_2.png "Eksempel 2")](media/ReplenTemp_example_2_large.png)

For å få maksimumsantallet til etterfyllingslokasjonene må du derfor sette alternativet **Tillat deling** til *Ja* i lokasjonsdirektivene for etterfyllingsplukking.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]