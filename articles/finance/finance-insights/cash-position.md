---
title: Likviditetsbeholdning
description: Dette emnet beskriver hvordan funksjonen Kontantstrømprognose forutsier en organisasjons likviditetsbeholdning for bestemte tider. Det beskriver også alternativene som er tilgjengelige for å vise prognoser for forskjellige perioder.
author: ShivamPandey-msft
ms.date: 12/21/2021
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
ms.openlocfilehash: 6bb99084a2ffef067dd0d7158ecb5e57d6d97d75
ms.sourcegitcommit: c8dc60bb760553f166409c2e06dd2377f601c006
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/23/2021
ms.locfileid: "7945807"
---
# <a name="cash-position"></a>Likviditetsbeholdning

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

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

## <a name="details-of-the-cash-position-capability"></a>Detaljer om likviditetsbeholdningsfunksjonen 

Funksjonen for likviditetsbeholdning omfatter følgende funksjonalitet. 

- Likviditetsbeholdningsfunksjonen viser kontantstrømmen basert på eksisterende dokumenter i systemet, og kontantstrøm inn og utflytlinjer som er importert fra eksterne systemer.
- Gjør det enkelt å integrere kontantstrømdata fra eksterne systemer i Dynamics 365 Finance. Likviditetsbeholdning kan også bruke rammeverket for import/eksport av data. Dette rammeverket gjør det enkelt å integrere med Excel OData. Du kan også kombinere data fra flere kilder for å opprette en omfattende likviditetsbeholdningsløsning.
- Innfører intelligent likviditetsbeholdning. Likviditetsbeholdning opprettes på grunnlag av kundens betalingsatferd for å forutsi når et firma kan forvente kontanter på kontoene.
- For kundeordrer og fakturaer brukes KI-funksjonaliteten for kundebetalingsforutsigelse til å fastslå den historiske kundebetalingsvirkemåten når en ordre eller faktura vil bli betalt.
- For leverandørordrer og fakturaer bruker vi gjennomsnittstiden mellom forsendelse og faktura og betaling av en faktura per leverandør til å finne ut når en leverandørordre eller faktura vil bli betalt for å gjøre kontantstrømmen mer nøyaktig.

Dette gir en mer nøyaktig visning av kontantstrømmen basert på historisk betalingsoppførsel for ekskredøren. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
