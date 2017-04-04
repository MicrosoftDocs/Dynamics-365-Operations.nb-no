---
title: "Løpende gjennomsnittlig kostpris"
description: "Lagerlukkingsprosessen i utligner avgangstransaksjoner mot tilgangstransaksjoner, på lagervurderingsmetoden som er valgt i varens varemodellgruppe. Før lagerlukkingen kjøres, beregner imidlertid en løpende gjennomsnittlig kostpris som vanligvis brukes ved postering av avgangstransaksjoner i systemet."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-04-07 15 - 11 - 47
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 685dfaa877699db3c36cc1ea77d956461f8e68ec
ms.lasthandoff: 03/29/2017


---

# <a name="running-average-cost-price"></a>Løpende gjennomsnittlig kostpris

Lagerlukkingsprosessen i utligner avgangstransaksjoner mot tilgangstransaksjoner, på lagervurderingsmetoden som er valgt i varens varemodellgruppe. Før lagerlukkingen kjøres, beregner imidlertid en løpende gjennomsnittlig kostpris som vanligvis brukes ved postering av avgangstransaksjoner i systemet.

Systemet Estimerer denne løpende gjennomsnittlig kostpris for en vare ved hjelp av følgende formel: Estimert pris = (fysisk beløp + finansielt beløp) ÷ (fysisk antall + finansielt antall)

## <a name="using-the-running-average-cost-price"></a>Bruke det glidende gjennomsnittet av kostprisen
Følgende tabell viser når posterer systemet lagertransaksjoner ved hjelp av løpende gjennomsnittlig kostpris, og når kostprisen som er definert i hovedposten for varen i stedet brukes.

| Betingelse                                               | Systemet bruker estimert løpende gjennomsnittlig kostpris | Systemet bruker kostprisen som er definert i hovedplanleggingen for varen |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Både telleren\* og Nevner\*\* er positive.  | Ja                                                      | Ingen                                                                |
| Telleren\*, Nevner\*\*, eller begge er negative. | Ingen                                                       | Ja                                                               |
| Nevner\*\* er 0 (null).                        | Ingen                                                       | Ja                                                               |

\*Teller = (fysisk beløp + finansielt beløp) \*\*nevner = (fysisk antall + finansielt antall) **notat:** hvis den **ta med fysisk verdi** alternativet ikke er valgt for en vare, bruker 0 (null) for både fysisk beløp og fysisk antall i systemet. Hvis du vil ha informasjon om dette alternativet, kan du se [Ta med fysisk verdi](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Unngå prisforsterking
I sjeldne tilfeller priser systemet flere avganger før programmet har nok mottak å basere prisen på. Dette scenariet kan føre til at beregninger av løpende gjennomsnittlig kostpris kan bli for høy. Du kan imidlertid utføre tiltak slik at du unngår for høy prising eller reduserer virkingen når det oppstår. **Scenario** Følgende transaksjoner skjer for en vare som du har valgt alternativet **Ta med fysisk verdi** for:

1.  Du mottar finansielt et antall på 100 for USD 100,00.
2.  Du utsteder et antall på 200 finansielt.
3.  Du mottar fysisk et antall på 101 for USD 202,00.

Når du undersøker den estimerte løpende gjennomsnittlige kostprisen for varen, kan du forvente en kostpris på USD 1,51. I stedet må du finne antatt glidende gjennomsnitt av USD 102.00, som er basert på følgende formel: Estimert pris = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102 denne prissetting forsterkning skjer fordi når 200 varer blir utstedt finansielt i trinn 2, må systemet pris 100 av varene før programmet har noen tilsvarende mottak. Dette fører til negativ beholdning. Systemet Estimerer deretter en enhetspris på USD 1.00, som vi kan forvente. Når de tilsvarende 100 mottakene kommer, er de imidlertid på en enhetspris på USD 2,00 hver. **Obs!** Selv om avgangene resultater i en negativ beholdning, er beholdningen positiv når avgangsprisen beregnes. Derfor blir løpende gjennomsnittlig kostpris brukt, i stedet for prisen på hovedvaren. Systemet har nå en lagerverdimotregning på USD 100.00. Selv om motregningen ble bygd opp over 100 artikler, der det var en enhetsmotregning på USD 1,00 hver, har vi nå bare én artikkel i beholdningen. Motregningen på USD 100,00 er derfor tilordnet denne ene artikkelen. Resultatet er for høy estimert kostpris. **Obs!**Til sammenligning kan du legge merke til at hvis trinn 2 og 3 blir snudd om i scenariet, blir 200 varer utstedt til en enhetspris på USD 1,51, og ett stykk blir stående på en enhetspris på USD 1,51. Siden dette prisforsterkingsscenariet kan oppstå når det finnes negativ beholdning, er det vanskelig å unngå i følgende tilfeller:

-   Du må estimere avgangspriser for beholdningsverdi og -antall.
-   Du må justere beholdningsverdien og -antallet for avgang og mottak.
-   Forretningsmodellen din tillater utsending av eller prising av flere stykker enn du har.
-   Du må godta alle mottaksverdier og -antall som blir sendt til deg.

Hvis forretningsmodellen din tillater følgende fremgangsmåter, kan de imidlertid hjelpe deg å unngå de negative antallene som gjør prisforsterkingsscenariet mulig:

-   Hvis du velger **Ta med fysisk verdi** for en vare, må du fjerne merket for **Fysisk negativt lager** på siden **Varemodellgrupper**.
-   Hvis du *ikke* velger **Ta med fysisk verdi** for en vare, må du fjerne merket for **Økonomisk negativt lager** på siden **Varemodellgrupper**.

Tenk også på at den maksimale motregningen til den fysiske lagerverdien, er begrenset av antallet fysiske transaksjoner og forskjellen mellom fysiske og finansielle priser. Så lenge alle fysiske transaksjoner til slutt blir oppdatert finansielt, kan ikke den fysiske verdien stige til ekstreme nivåer. Legg til slutt merke til at forsterkingseffekten vil minske betraktelig når den akkumulerte motregningen blir spredd utover flere varer, i stedet for bare en.


