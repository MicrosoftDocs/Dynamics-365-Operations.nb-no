---
title: Definere rentesatser for en rentekode
description: "Rentekoder inneholder innstillinger som bestemmer nå renter belastes og hvordan de beregnes på forfalte kontoer."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 9656718d7afbcc6d89e650ab9379900c083507fe
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-interest-rates-for-an-interest-code"></a>Definere rentesatser for en rentekode

Rentekoder inneholder innstillinger som bestemmer nå renter belastes og hvordan de beregnes på forfalte kontoer.

Du kan definere en enkelt rentekode og bruke den på flere kundeposteringsprofiler, faktureringskoder eller på bestemte fakturalinjer. Når rentekodedetaljene er endret vil alle funksjonene som bruker koden implementere endringene for nye transaksjoner. For hver rentekode kan du definere to typer satser:
-   Satser for renteinntekter − Disse representerer inntekt som er tjent ved å belaste renter på fakturaer eller rentenotaer.
-   Satser for rentebetalinger − Disse representerer en kostnad som er betalt for renter på kreditnotaer.

Begge disse satstypene kan eksistere på samme tid og i den samme rentekoden. Rentesatser kan baseres på tre beregningstyper:
-   Rente i prosent.
-   Rente i beløp.
-   Rente etter intervall, som resulterer i en enkelt prosent eller et enkelt beløp.

Når en rente brukes til å beregne rente, opprettes det en egen rentenota for hver rentesats som er aktiv i løpet av det tidsrommet som betalingen overskrider forfallsdatoen for transaksjonen. Du bruker fanen **Inntekter** på siden **Rentekode** for å definere rentesatser for rente som får du ved å belaste rente. Bruk **Betalinger**-fanen til å definere rentesatser for renter du betaler.

## <a name="interest-rates-based-on-a-percentage"></a>Rentesatser basert på en prosent
Du kan definere rentesatser som beregner en bestemt prosent.

-   Rentebeløp gjelder for alle valutaer.
-   Valgfrie rentebeløpsgrenser kan angis.
-   **Prosent** er valgt ** ** i den **beregner renten som er basert på** i den **Sett opp rentekoder** siden.

For eksempel vil angi en rentekode som vurderer 5 prosent rente for hver to måneder at fakturabetalingen overskrider transaksjonen forfallsdatoen, skriver du inn 2 i den **beregne rente hver** -feltet og velger **måned**.

## <a name="interest-rates-based-on-amounts"></a>Rentesatser basert på beløp
Du kan definere rentesatser som beregner et bestemt beløp per valuta.
-   Et rentebeløp angis for hver valuta i rentekoden.
-   Valgfrie rentebeløpsgrenser kan angis.
-   ** Beløp ** er valgt i den **beregner renten som er basert på** i den **Sett opp rentekoder** siden.

For eksempel vil angi en rentekode som vurderer interesse 25,00 for hver 20 dager at fakturabetalingen overskrider transaksjonen forfallsdatoen, skriver du inn 20 i den **beregne rente hver** -feltet og velger **dag**.

## <a name="interest-rates-based-on-ranges"></a>Rentesatser basert på intervaller
Du kan definere rentesatser som varierer avhengig av forfalt beløp, antall dager beløpet er forsinket eller antall måneder beløpet er forsinket.
-   Du kan bruke **Inntjening etter valuta**-fanene for å definere bestemte renteinnstillinger for hver valuta. Dette er også der du definerer området.
-   Bruk **Områder**-knappen til å legge til linjer som representerer områdene som du vil definere. **Fra**-verdien representerer begynnelsen på området, og **Renteverdi**-tallet representerer en prosent eller et beløp, avhengig av valget i **Beregn rente basert på**-feltet på **Definer rentekoder**-siden.

## <a name="example-1-interest-by-range--amount"></a>Eksempel 1: Rente etter intervall = Beløp
Du definerer en rentekode som setter rente én gang for hver tredje måned fakturabetalingen overskrider transaksjonens forfallsdato. Du vil basere beregningen på en renteverdiprosent, ifølge trinnvise beløpsintervaller. Renteverdien vil være 1 prosent for fakturabeløp opptil 1 000,00, 2 prosent for beløp fra 1 001,00 til 5 000,00 og 3 prosent for beløp større enn 5 000,00. Slik definerer du verdiene i rentekodefeltene.

| **Feltnavn**                  | **Feltverdi** |
|---------------------------------|-----------------|
| **Rentekode**               | 3M%ByAmt        |
| **Beregn renter hver**    | 3/måned         |
| **Rente etter intervall**           | Beløp          |
| **Beregn rente basert på** | Prosent      |

Slik definerer du intervallinformasjonen.

| **From value** | **Interest value** |
|----------------|--------------------|
| 0              | 1                  |
| 1,001          | 2                  |
| 5,001          | 3                  |

 
## <a name="example-2-interest-by-range--days"></a>Eksempel 2: Rente etter intervall = Dager
--------------------------------------------------

Du definerer en rentekode som setter rente én gang for hver 15. dag fakturabetalingen overskrider transaksjonens forfallsdato. Du vil basere beregningen på et renteverdibeløp, ifølge trinnvise dagsintervaller. Renteverdien vil være 10,00 per 15 dager for de 60 første dagene, 15,00 per 15 dager fra dag 61 til 90 og 20,00 per 15 dager fra dag 91 og senere. Slik definerer du verdiene i rentekodefeltene.

| **Feltnavn**                  | **Feltverdi** |
|---------------------------------|-----------------|
| **Rentekode**               | 15DBelXDag      |
| **Beregn renter hver**    | 15/dag          |
| **Rente etter intervall**           | Dager            |
| **Beregn rente basert på** | Beløp          |

Slik definerer du intervallinformasjonen.

| **From value** | **Interest value** |
|----------------|--------------------|
| 0              | 10                 |
| 61             | sept.                 |
| 91             | 20                 |

 
## <a name="example-3-interest-by-range--months"></a>Eksempel 3: Rente etter intervall = Måneder
----------------------------------------------------

Du definerer en rentekode som setter rente én gang for hver måned fakturabetalingen overskrider transaksjonens forfallsdato. Du vil basere beregningen på en renteverdiprosent, ifølge trinnvise månedsintervaller. Renteverdien vil være 1,5 prosent per måned de første tre månedene etter forfall, 2,0 prosent per måned for de neste tre månedene og 2,5 prosent per måned for hver måned etter de første seks månedene. Slik definerer du verdiene i rentekodefeltene.

| **Feltnavn**                  | **Feltverdi** |
|---------------------------------|-----------------|
| **Rentekode**               | 1M%EtMnd        |
| **Beregn renter hver**    | 1/måned         |
| **Rente etter intervall**           | Måneder          |
| **Beregn rente basert på** | Prosent      |

Slik definerer du intervallinformasjonen.

| **From value** | **Interest value** |
|----------------|--------------------|
| 0              | 1.5                |
| 4              | 2                  |
| 7              | 2,5                |

## <a name="new-versions"></a>Nye versjoner
Rentekoder har gyldighet fra en dato. Hvis du vil endre rentesatsen, kan du opprette en **ny versjon** som gjelder fra og med en fremtidig dato.

For å vise forskjellige versjoner, kan du bruke **Per dato**-menyvalget for å velge fristen. Du kan også velge **Vis alle poster** for å vise alle rentekoder på siden.


