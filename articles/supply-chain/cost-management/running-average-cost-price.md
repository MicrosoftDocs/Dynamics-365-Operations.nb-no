---
title: Løpende gjennomsnittlig kostpris
description: Lagerlukkingsprosessen i utligner avgangstransaksjoner mot tilgangstransaksjoner på grunnlag av lagervurderingsmetoden som er valgt i varens varemodellgruppe. Før lagerlukkingen kjøres, beregner imidlertid systemet en løpende gjennomsnittlig kostpris som vanligvis brukes når avgangstransaksjoner posteres.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 871b3ffce45848f95d132eff3fd327295bc5084c
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092195"
---
# <a name="running-average-cost-price"></a>Løpende gjennomsnittlig kostpris

[!include [banner](../includes/banner.md)]

Lagerlukkingsprosessen i utligner avgangstransaksjoner mot tilgangstransaksjoner på grunnlag av lagervurderingsmetoden som er valgt i varens varemodellgruppe. Før lagerlukkingen kjøres, beregner imidlertid systemet en løpende gjennomsnittlig kostpris som vanligvis brukes når avgangstransaksjoner posteres.

Systemet estimerer denne løpende gjennomsnittlige kostprisen for en vare ved å bruke følgende formel:

Estimert pris = (fysisk beløp + finansielt beløp) / (fysisk antall + finansielt antall)

## <a name="default-item-cost"></a>Standard varekostnad

Standard varekostnad for et frigitt produkt kan konfigureres på to forskjellige måter på siden **Detaljer om frigitt produkt**:

- Opprett en standardkostnad ved å velge **Varepris** i **Oppsett**-gruppen på fanen **Styr kostnader** i handlingsruten. Hvis du bruker denne metoden, må du bruke en standard etterkalkuleringsversjon for kostnad, og kostnaden må være aktivert.
- Definer en standard varekostpris for et frigitt produkt ved å angi en verdi i **Pris**-feltet på hurtigfanen **Styr kostnader**.

I tillegg til å angi eller opprette en pris kan du merke av for **Bruk siste kostpris** på hurtigfanen **Styr kostnader** på siden **Detaljer om frigitt produkt**. I dette tilfellet vil systemet automatisk oppdatere **Pris**-feltet når du posterer en økonomisk oppdatering. Hvis du for eksempel posterer en bestillingsfaktura, blir feltet satt til innkjøpsprisen fra denne fakturaen.

Hvis du har en kostpris i en aktiv etterkalkuleringsversjon, og du angir en pris på hurtigfanen **Styr kostnader**, vil systemet bruke prisen fra den aktive etterkalkuleringsversjonen før det bruker prisen som er definert på hurtigfanen **Styr kostnader**.

## <a name="using-the-running-average-cost-price"></a>Bruke det glidende gjennomsnittet av kostprisen

Følgende tabell viser når systemet posterer lagertransaksjoner ved bruk av løpende gjennomsnittlig kostpris, og når kostprisen som er definert i hovedposten for varen, blir brukt i stedet.

| Betingelse | Systemet bruker den estimerte løpende gjennomsnittlige kostprisen | Systemet bruker standard varekostpris |
| --- | --- | --- |
| Både telleren\* og nevneren\*\* er positive. | Ja | Nei |
| Telleren\*, nevneren\*\* eller begge deler er negative. | Nei | Ja |
| Nevneren\*\* er 0 (null). | Nei | Ja |

\* Teller = (fysisk beløp + finansielt beløp)  
\*\* Nevner = (fysisk antall + finansielt antall)

> [!NOTE]
> Hvis **Ta med fysisk verdi** ikke er merket av for en vare, bruker systemet 0 (null) for både det fysiske beløpet og det fysiske antallet. Hvis du vil ha informasjon om dette alternativet, kan du se [Ta med fysisk verdi](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Unngå prisforsterking

I sjeldne tilfeller prissetter systemet flere avganger før det har mange nok mottak å basere prisen på. Dette scenariet kan føre til at beregninger av løpende gjennomsnittlig kostpris kan bli for høy. Du kan imidlertid utføre tiltak slik at du unngår for høy prising eller reduserer virkingen når det oppstår.

**Scenario:** Følgende transaksjoner skjer for en vare som du har valgt alternativet **Ta med fysisk verdi** for:

1. Du mottar finansielt et antall på 100 for USD 100,00.
2. Du utsteder et antall på 200 finansielt.
3. Du mottar fysisk et antall på 101 for USD 202,00.

Når du undersøker den estimerte løpende gjennomsnittlige kostprisen for varen, kan du forvente en kostpris på USD 1,51. I stedet finner du et estimert løpende gjennomsnitt på USD 102,00, som er basert på følgende formel:

Estimer pris = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102

Denne prisforsterkingen skjer fordi når 200 varer er økonomisk frigitt i trinn 2, må systemet prise 100 av varene før det har tilsvarende mottak. Dette fører til negativ beholdning. Systemet estimerer deretter en enhetspris på USD 1,00, som du kan forvente. Når de tilsvarende 100 mottakene kommer, er de imidlertid på en enhetspris på USD 2,00 hver.

> [!NOTE]
> Selv om avgangene resultater i en negativ beholdning, er beholdningen positiv når avgangsprisen beregnes. Derfor blir løpende gjennomsnittlig kostpris brukt, i stedet for prisen på hovedvaren. På dette stadiet har systemet en lagerverdimotregning på USD 100,00. Selv om motregningen ble bygd opp over 100 artikler, der det var en enhetsmotregning på USD 1,00 hver, har du nå bare én artikkel i beholdningen. Motregningen på USD 100,00 er derfor tilordnet denne ene artikkelen. Resultatet er for høy estimert kostpris.
>
> Til sammenligning kan du legge merke til at hvis trinn 2 og 3 blir snudd om i scenariet, blir 200 varer utstedt til en enhetspris på USD 1,51, og ett stykk blir stående på en enhetspris på USD 1,51. Siden dette prisforsterkingsscenariet kan oppstå når det finnes negativ beholdning, er det vanskelig å unngå i følgende tilfeller:
>
> - Du må estimere avgangspriser for beholdningsverdi og -antall.
> - Du må justere beholdningsverdien og -antallet for avgang og mottak.
> - Forretningsmodellen din tillater utsending av eller prising av flere stykker enn du har.
> - Du må godta alle mottaksverdier og -antall som blir sendt til deg.

Hvis forretningsmodellen din tillater følgende fremgangsmåter, kan de imidlertid hjelpe deg å unngå de negative antallene som gjør prisforsterkingsscenariet mulig:

- Hvis du velger **Ta med fysisk verdi** for en vare, må du fjerne merket for **Fysisk negativt lager** på siden **Varemodellgrupper**.
- Hvis du **ikke** velger **Ta med fysisk verdi** for en vare, må du fjerne merket for **Økonomisk negativt lager** på siden **Varemodellgrupper**.

Tenk også på at den maksimale motregningen til den fysiske lagerverdien, er begrenset av antallet fysiske transaksjoner og forskjellen mellom fysiske og finansielle priser. Så lenge alle fysiske transaksjoner til slutt blir oppdatert finansielt, kan ikke den fysiske verdien stige til ekstreme nivåer. Legg til slutt merke til at forsterkingseffekten vil minske betraktelig når den akkumulerte motregningen blir spredd utover flere varer, i stedet for bare en.

## <a name="avoid-a-zero-cost-price-on-issues"></a>Unngå null kostpris på avganger

Når alternativet **Ta med fysisk verdi** ikke er valgt på siden **Varemodellgruppe**, kan en avgang fra lageret ha null kostpris hvis det ikke er noen økonomisk oppdaterte mottak i lageret. For å unngå dette scenarioet kan du vurdere følgende alternativer:

- Merk av for **Ta med fysisk verdi** på siden **Varemodellgruppe**. Dette alternativet forhindrer en kostpris på null på en avgang, forutsatt at mottaket oppdateres fysisk. Hvis du ikke tillater negativt fysisk lager, beregner avganger glidende gjennomsnitt fra de fysisk oppdaterte transaksjonene.
- Opprett en standard varekostpris ved å aktivere en etterkalkuleringsversjon som har en standard kostpris, eller angi prisen på hurtigfanen **Styr kostnader** på siden **Detaljer om frigitt produkt**. Dette alternativet er best når det ikke er merket av for **Ta med fysisk verdi** på siden **Varemodellgruppe**, fordi systemet alltid vil ha en tilbakefallspris som kan brukes.
- Velg alternativet **Bruk siste kostpris** på hurtigfanen **Styr kostnader** på siden **Detaljer om frigitt produkt**. Dette alternativet vil holde **Pris**-feltet oppdatert hver gang du oppdaterer et mottak økonomisk. Hvis du velger dette alternativet, men du ikke angir en standardpris eller aktiverer en kostnad i en standard kostnadsversjon, kan du likevel ha null i kostpris på en avgang.

Hvis du har avgangstransaksjoner som har null i kostnad, vil prosessen for *lukking og justering av beholdning* korrigere kostprisen ved å opprette en justering etter at mottakene er finansielt oppdatert. Husk at den finansperioden når denne oppdateringen skjer, kan være forskjellig fra finansperioden når varene fysisk ble mottatt eller frigitt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
