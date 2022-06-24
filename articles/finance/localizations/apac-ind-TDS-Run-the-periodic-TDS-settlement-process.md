---
title: Kjøre den periodiske TDS-utligningsprosessen
description: Denne artikkelen beskriver hvordan du utligner periodisk TDS (Tax Deducted at Source).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1376e2ae342aedb8fe44d95a11dd47f906a4ca48
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864249"
---
# <a name="run-the-periodic-tds-settlement-process"></a>Kjøre den periodiske TDS-utligningsprosessen

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du utligner periodisk TDS (Tax Deducted at Source).

1. Gå til **Avgift \> Deklareringer \> Kildeskatt \> Kildeskattbetaling**.

    [![Dialogboksen Kildeskattbetaling.](./media/apac-ind-TDS-47.png)](./media/apac-ind-TDS-47.png)

2. Velg **TDS** i feltet **Avgiftstype** i dialogboksen **Kildeskattbetaling**.
3. Velg TAN-nummeret (Tax Account Number) i feltet **TAN-nummer (Tax Account Number)** som utligningsprosessen skal kjøres for.
4. Velg TDS-komponentgruppen som utligningsprosessen skal kjøres for, i feltet **Komponentgruppe for kildeskatt**.
5. Velg TDS-utligningsperioden du vil kjøre utligningsprosessen for, i feltet **Utligningsperiode**.

    > [!NOTE]
    > TDS-utligningsprosessen kjøres for alle perioder som er definert for TDS-utligningsperioden i **Perioder**-fanen på siden **Utligningsperioder for kildeskatt** (**Avgift \> Indirekte avgifter \> Kildeskatt \> Utligningsperioder for kildeskatt**).

6. Velg startdatoen for kjøringen av TDS-utligningsprosessen i feltet **Fra-dato**.

    Når det gjelder en bestemt periode i utligningsperioden, regnes startdatoen som er definert for perioden, som fra-datoen. La oss si at TDS-utligningsperioden har to perioder: 1. april til og med 30. april 2009, og 1. mai til og med 31. mai 2009. Hvis du velger **06.04.2009** (6. april 2009) som startdato i feltet **Fra-dato**, kjøres utligningsprosessen likevel fra 1. april 2009.

    Hvis du angir en senere periode i feltet **Fra-dato**, men uten å utligne en tidligere periode innen utligningsperioden, foretas ikke utligningen for noen tidligere perioder. La oss si at TDS-utligningsperioden har tre perioder: 1. april til og med 30. april 2009, 1. mai til og med 31. mai 2009 og 1. juni til og med 30. juni 2009. Hvis du velger **01.05.2009** (1. mai 2009) som startdato i feltet **Fra-dato**, kjøres utligningsprosessen bare fra 1. mai til og med 31. mai 2009. Utligningen foretas ikke for 1. april til og med 30. april 2009.

7. Velg datoen for postering av TDS-utligningstransaksjonen i feltet **Transaksjonsdato**.
8. Velg TDS-utligningsversjonen i feltet **Kildeskattbetalingsversjon**.

     - **Opprinnelig** – Bruk dette alternativet til å kjøre TDS-utligningsprosessen for første gang. Den opprinnelige betalingsversjonen brukes bare én gang til å kjøre TDS-utligningsprosessen for en kombinasjon av et TAN-nummer, en komponentgruppe for kildeskatt og en utligningsperiode for kildeskatt.
    - **Siste versjoner** – Bruk dette alternativet hvis TDS-utligningsprosessen allerede er kjørt for den angitte perioden. Ta med tilbakedaterte transaksjoner som ble postert etter at utligningsprosessen tidligere ble kjørt for perioden. Du kan bruke dette alternativet til å kjøre utligningsprosessen mange ganger.

9. Merk av for **Oppdater** for å kjøre TDS-utligningsprosessen og postere beløpene på finanskontoene. Hvis du fjerner merket for alternativet, kjøres ikke utligningsprosessen, og finansoppføringene genereres ikke.
10. Velg **OK** for å kjøre TDS-utligningsprosessen og generere rapporten for kildeskattbetaling. Statusen for TDS-transaksjoner som er tatt med i utligningsprosessen, vises som **Utlignet** på **Utligning**-siden (gå til **Leverandører \> Betalinger \> Leverandørbetalingsjournal**, velg **Linjer**, velg **Funksjoner** og velg deretter **Utligning**).

### <a name="important-points"></a>Viktig å være oppmerksom på

- Hvis en komponentgruppe for kildeskatt ikke velges i løpet av utligningsprosessen, foretas utligningen for alle komponentgruppene for kildeskatt for det valgte TAN-nummeret og den valgte utligningsperioden. Det opprettes en egen linje for hver komponentgruppe for kildeskatt på siden **Åpen transaksjonsredigering**.
- Utligningsprosessen er basert på kategorien for skattebetalertype for en utligningsperiode. Transaksjoner der kategorien for skattebetalertype er **Selskap**, utlignes og vises som én linje på siden **Åpen transaksjonsredigering**. Transaksjoner der kategorien for skattebetalertype er en annen enn **Selskap**, utlignes og vises som én linje på siden **Åpen transaksjonsredigering**.
- Forfallsdatoen for de utlignede TDS-transaksjonslinjene på siden **Åpen transaksjonsredigering** er basert på betalingsbetingelsene som er definert for TDS-myndighetsleverandøren på **Leverandører**-siden. Hvis betalingsbetingelsene ikke er definert for TDS-myndighetsleverandøren, vises den siste dagen i utligningsperioden som forfallsdatoen.
