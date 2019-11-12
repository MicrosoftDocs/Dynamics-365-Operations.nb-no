---
title: Løpende gjennomsnittlig kostpris
description: Lagerlukkingsprosessen i utligner avgangstransaksjoner mot tilgangstransaksjoner på grunnlag av lagervurderingsmetoden som er valgt i varens varemodellgruppe. Før lagerlukkingen kjøres, beregner imidlertid systemet en løpende gjennomsnittlig kostpris som vanligvis brukes når avgangstransaksjoner posteres.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7957b2a9cb24dcc61e3113bfd3cc3b1fa1e6d0a6
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569254"
---
# <a name="running-average-cost-price"></a>Løpende gjennomsnittlig kostpris

[!include [banner](../includes/banner.md)]

Lagerlukkingsprosessen i utligner avgangstransaksjoner mot tilgangstransaksjoner på grunnlag av lagervurderingsmetoden som er valgt i varens varemodellgruppe. Før lagerlukkingen kjøres, beregner imidlertid systemet en løpende gjennomsnittlig kostpris som vanligvis brukes når avgangstransaksjoner posteres.

Systemet estimerer denne løpende gjennomsnittlige kostprisen for en vare ved å bruke følgende formel: 

Estimert pris = (fysisk beløp + finansielt beløp) / (fysisk antall + finansielt antall)

## <a name="using-the-running-average-cost-price"></a>Bruke det glidende gjennomsnittet av kostprisen
Følgende tabell viser når systemet posterer lagertransaksjoner ved bruk av løpende gjennomsnittlig kostpris, og når kostprisen som er definert i hovedposten for varen, blir brukt i stedet.

| Betingelse                                               | Systemet bruker den estimerte løpende gjennomsnittlige kostprisen | Systemet bruker kostprisen som er definert i hovedposten for varen |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Både telleren\* og nevneren\*\* er positive.  | Ja                                                      | Ingen                                                                |
| Telleren\*, nevneren\*\* eller begge deler er negative. | Ingen                                                       | Ja                                                               |
| Nevneren\*\* er 0 (null).                        | Ingen                                                       | Ja                                                               |

\* Teller = (fysisk beløp + finansielt beløp) \*\* Nevner = (fysisk antall + finansielt antall) 

**Obs!** Hvis **Ta med fysisk verdi** ikke er merket av for en vare, bruker systemet 0 (null) for både det fysiske beløpet og det fysiske antallet. Hvis du vil ha informasjon om dette alternativet, kan du se [Ta med fysisk verdi](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Unngå prisforsterking
I sjeldne tilfeller prissetter systemet flere avganger før det har mange nok mottak å basere prisen på. Dette scenariet kan føre til at beregninger av løpende gjennomsnittlig kostpris kan bli for høy. Du kan imidlertid utføre tiltak slik at du unngår for høy prising eller reduserer virkingen når det oppstår. **Scenario** Følgende transaksjoner skjer for en vare som du har valgt alternativet **Ta med fysisk verdi** for:

1.  Du mottar finansielt et antall på 100 for USD 100,00.
2.  Du utsteder et antall på 200 finansielt.
3.  Du mottar fysisk et antall på 101 for USD 202,00.

Når du undersøker den estimerte løpende gjennomsnittlige kostprisen for varen, kan du forvente en kostpris på USD 1,51. Du finner i stedet antatt glidende gjennomsnitt på USD 102,00, som er basert på følgende formel: Estimert pris = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102. Denne prissettingsforhøyelsen skjer fordi når 200 varer blir utstedt finansielt i trinn 2, må systemet prise 100 av varene før det har noen tilsvarende mottak. Dette fører til negativ beholdning. Systemet estimerer deretter en enhetspris på USD 1,00, som vi kan forvente. Når de tilsvarende 100 mottakene kommer, er de imidlertid på en enhetspris på USD 2,00 hver. 

**Obs!** Selv om avgangene resultater i en negativ beholdning, er beholdningen positiv når avgangsprisen beregnes. Derfor blir løpende gjennomsnittlig kostpris brukt, i stedet for prisen på hovedvaren. På dette stadiet har systemet en lagerverdimotregning på USD 100,00. Selv om motregningen ble bygd opp over 100 artikler, der det var en enhetsmotregning på USD 1,00 hver, har vi nå bare én artikkel i beholdningen. Motregningen på USD 100,00 er derfor tilordnet denne ene artikkelen. Resultatet er for høy estimert kostpris. 

**Obs!** Til sammenligning kan du legge merke til at hvis trinn 2 og 3 blir snudd om i scenariet, blir 200 varer utstedt til en enhetspris på USD 1,51, og ett stykk blir stående på en enhetspris på USD 1,51. Siden dette prisforsterkingsscenariet kan oppstå når det finnes negativ beholdning, er det vanskelig å unngå i følgende tilfeller:

-   Du må estimere avgangspriser for beholdningsverdi og -antall.
-   Du må justere beholdningsverdien og -antallet for avgang og mottak.
-   Forretningsmodellen din tillater utsending av eller prising av flere stykker enn du har.
-   Du må godta alle mottaksverdier og -antall som blir sendt til deg.

Hvis forretningsmodellen din tillater følgende fremgangsmåter, kan de imidlertid hjelpe deg å unngå de negative antallene som gjør prisforsterkingsscenariet mulig:

-   Hvis du velger **Ta med fysisk verdi** for en vare, må du fjerne merket for **Fysisk negativt lager** på siden **Varemodellgrupper**.
-   Hvis du *ikke* velger **Ta med fysisk verdi** for en vare, må du fjerne merket for **Økonomisk negativt lager** på siden **Varemodellgrupper**.

Tenk også på at den maksimale motregningen til den fysiske lagerverdien, er begrenset av antallet fysiske transaksjoner og forskjellen mellom fysiske og finansielle priser. Så lenge alle fysiske transaksjoner til slutt blir oppdatert finansielt, kan ikke den fysiske verdien stige til ekstreme nivåer. Legg til slutt merke til at forsterkingseffekten vil minske betraktelig når den akkumulerte motregningen blir spredd utover flere varer, i stedet for bare en.



