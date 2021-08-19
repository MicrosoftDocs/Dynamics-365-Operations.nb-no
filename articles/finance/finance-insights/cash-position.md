---
title: Likviditetsbeholdning (forhåndsversjon)
description: Dette emnet beskriver hvordan funksjonen Kontantstrømprognose forutsier en organisasjons likviditetsbeholdning for bestemte tider. Det beskriver også alternativene som er tilgjengelige for å vise prognoser for forskjellige perioder.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 457dd34a2ccddce0e94f956ba2b854c27a270f13341047e508ac702aa1281d25
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717479"
---
# <a name="cash-position-preview"></a>Likviditetsbeholdning (forhåndsversjon)

[!include [banner](../includes/banner.md)]

Likviditetsbeholdning er prosjekteringen av kontantstrøm som forutsies på kort sikt. Den er basert på prosjekteringen av kontantkvitteringer fra kunder som betaler utestående fakturaer og ordrer, og også på prosjekteringen av kontantutbetalinger som betales til leverandører for innkjøpsfakturaer og -ordrer.

Når systemet forutsier kundebetalinger, bruker det betalingsprognosene fra funksjonen for kundebetalingsprognose. Uten betalingsprognoser blir gjennomsnittstiden som kreves for å konvertere en kundefaktura til en betaling for hver kunde, brukt til å beregne en betalingsdato. Når det gjelder åpne kundeordrer, beregner systemet fakturadatoen ved hjelp av gjennomsnittlig antall dager for ordrelinjer per kunde som skal faktureres. Deretter bruker det fakturadatoen som inndata for funksjonen for betalingsprognose. Funksjonen for kundebetalingsprognose beregner en betalingsdato for hver ordrelinje. 

Betalingsdatoen for utestående fakturaer blir anslått fra betalingsprognosene ved å velge en dato som samsvarer med det 50. persentil av den kumulative distribusjonsfunksjonen som er hentet fra sannsynlighetene for den forutsagte samlingen.

En lignende tilnærming brukes til å forutsi betalinger til leverandører. For hver leverandør beregner systemet gjennomsnittstiden det tar å konvertere en leverandørfaktura til en betaling. Dette antallet dager brukes deretter til å beregne betalingsdatoen. Når det gjelder åpne leverandørordrer, beregner systemet fakturadatoen ved å vurdere gjennomsnittlig antall dager som kreves for å konvertere ordrelinjer til en faktura for hver leverandør. Systemet beregner deretter betalingsdatoen ved hjelp av gjennomsnittstiden det tar å konvertere en leverandørfaktura til en betaling for hver leverandør.

Den øvre delen av fanen **Likviditetsbeholdning** omfatter et diagram for likviditetsbeholdning. Dette diagrammet viser inngående og utgående kontantstrøm og innvirkningen på den totale likviditetssaldoen. Detaljene i diagrammet for likviditetsbeholdning kan vises i daglige, ukentlige, månedlige eller kvartalsvise perioder. Når du velger **Daglig**, kan du vise prognoser for de neste 21 dagene. Når du velger **Ukentlig**, kan du vise prognoser for de neste 20 ukene. Når du velger **Månedlig**, kan du vise prognoser for de neste 12 månedene. Når du velger **Kvartalsvis**, kan du vise prognoser for de neste 12 kvartalene. Du kan skjule diagrammet hvis du trenger mer plass på skjermen for å vise innholdet i fanen **Likviditetsbeholdning**.

Den nedre delen av fanen **Likviditetsbeholdning** viser detaljer for stillingen, kontantstrømmen, prosjekterte betalinger og bankkonto.

- Informasjon i rutenettet **Stillingsdetaljer** vises i tre deler: en liste over likviditetskontoer, en liste over dokumenter som utgjør inngående kontantstrømmer, og en liste over dokumenter som utgjør utgående kontantstrømmer. Rutenettet viser også likviditetsbeholdningssaldoer. Når det gjelder den første perioden du viser, er saldoen for likviditetskontoene åpningssaldoen. Når det gjelder etterfølgende perioder, beregnes saldoene for likviditetskontoene basert på tilføyingen av inngående kontantstrømmer og subtraksjon av utgående kontantstrømmer fra tidligere perioder. Hvis du vil vise detaljer om transaksjonene som utgjør saldoen, velger du **Saldo**-koblingen.
- Rutenettet **Kontantstrøm** viser inngående kontantstrømmer og utgående kontantstrømmer aggregert per periode og hvordan de virker inn på saldoer på likviditetskontoen. Når det gjelder den første perioden, er saldoen for likviditetskontoene åpningssaldoen. Når det gjelder etterfølgende perioder, beregnes saldoene for likviditetskontoene basert på tilføyingen av inngående kontantstrømmer og subtraksjon av utgående kontantstrømmer fra tidligere perioder.
- Rutenettet **Prosjektert banksaldo** viser forventede utgående kontantstrømmer og innvirkning de har på likviditetskontoer.
- Rutenettet **Bankkonto** viser innvirkningen av forventede inngående og utgående kontantstrømmer på banksaldoen.

Hvis du vil lagre og redigere likviditetsbeholdningen, oppretter du et øyeblikksbilde. Du finner mer informasjon om hvordan du arbeider med øyeblikksbilder, ved å se [Oversikt over øyeblikksbilder](payment-snapshots.md).

#### <a name="privacy-notice"></a>Personvernerklæring
Forhåndsversjoner (1) kan ha redusert personvern og færre sikkerhetstiltak enn Dynamics 365 Finance and Operations-tjenesten, (2) er ikke inkludert i serviceavtalen (SLA) for denne tjenesten, (3) må ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) har begrenset støtte.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
