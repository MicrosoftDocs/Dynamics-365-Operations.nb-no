---
title: Scenarioer for justeringsdato
description: Dette emnet gir eksempler som viser hvordan justeringsdatoer fungerer i Abonnementsfakturering.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 91480fecd16cf8417722df73c28bbd81d029fb07
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690480"
---
# <a name="alignment-date-scenarios"></a>Scenarioer for justeringsdato

Dette emnet gir eksempler som viser hvordan justeringsdatoer fungerer i Abonnementsfakturering.

I disse eksemplene har en fakturadetalj for en fakturaplan en justeringsdato den 31. oktober 2019. Den første fakturadetaljen for linjen slutter den 31. oktober 2019, og gjelder i henhold til dette. Linjen fornyes automatisk ved hjelp av en fornyelsesstartdato 11. november.

> [!NOTE]
> Året er relevant fordi det kan føre til at justeringsdatoen blir mer eller mindre enn et år. Fr disse eksemplene angis fordelingsberegningsperioden til **Månedlig** på siden **Parametere for gjentakende kontraktfakturering**. Hvis satt til **Daglig**, vil noen delbeløp være forskjellige.

## <a name="scenario-1-no-alignment"></a>Scenario 1: Ingen justering

Faktureringsplanen er satt opp med følgende data:

- **Startdato:** 1. mai 2019
- **Sluttdato:** 31. desember 2024
- **Beløp:** $ 1 000

| Startdato for fakturering | Sluttdato for fakturering | Forrige avlesning | Gjeldende avlesning | Angitt antall | Gratis antall | Fakturerbart antall | Enhetspris |
|---|---|---|---|---|---|---|---|
| 01.05.2019 | 30.04.2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.05.2020 | 30.04.2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.05.2021 | 30.04.2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.05.2022 | 30.04.2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.05.2023 | 30.04.2024 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.05.2024 | 31.12.2024 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-2-shortened-alignment"></a>Scenario 2: Forkortet justering

Faktureringsplanen er satt opp med følgende data:

- **Startdato:** 1. mai 2019
- **Sluttdato:** 31. desember 2024
- **Beløp:** $ 1 000
- **Justeringsdato:** 31. desember 2019

Det første fornyelsesbeløpet er mindre enn ett år.

| Startdato for fakturering | Sluttdato for fakturering | Forrige avlesning | Gjeldende avlesning | Angitt antall | Gratis antall | Fakturerbart antall | Enhetspris |
|---|---|---|---|---|---|---|---|
| 01.05.2019 | 31.12.2019 | | | 1.00 | | 1.00 | 666.67 |
| 01.01.2020 | 31.12.2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2021 | 31.12.2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2022 | 31.12.2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2023 | 31.12.2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2024 | 31.12.2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-3-extended-alignment"></a>Scenario 3: Forlenget justering

Faktureringsplanen er satt opp med følgende data:

- **Startdato:** 1. mai 2019
- **Sluttdato:** 31. desember 2024
- **Beløp:** $ 1 000
- **Justeringsdato:** 31. desember 2020

Det første fornyelsesbeløpet er mer enn ett år.

| Startdato for fakturering | Sluttdato for fakturering | Forrige avlesning | Gjeldende avlesning | Angitt antall | Gratis antall | Fakturerbart antall | Enhetspris |
|---|---|---|---|---|---|---|---|
| 01.05.2019 | 31.12.2020 | | | 1.00 | | 1.00 | 1,666.67 |
| 01.01.2021 | 31.12.2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2022 | 31.12.2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2023 | 31.12.2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2024 | 31.12.2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-4-alignment-with-a-different-end-month"></a>Scenario 4: Justering med en annen sluttmåned

Faktureringsplanen er satt opp med følgende data:

- **Startdato:** 1. mai 2019
- **Sluttdato:** 31. oktober 2024
- **Beløp:** $ 1 000
- **Justeringsdato:** 31. desember 2019

> [!NOTE]
> Dette scenarioet er ikke vanlig.

| Startdato for fakturering | Sluttdato for fakturering | Forrige avlesning | Gjeldende avlesning | Angitt antall | Gratis antall | Fakturerbart antall | Enhetspris |
|---|---|---|---|---|---|---|---|
| 01.05.2019 | 31.12.2019 | | | 1.00 | | 1.00 | 666.67 |
| 01.01.2020 | 31.12.2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2021 | 31.12.2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2022 | 31.12.2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2023 | 31.12.2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2024 | 31.10.2024 | | | 1.00 | | 1.00 | 833.33 |

## <a name="scenario-5-single-partial-year"></a>Scenario 5: Enkelt delvis år

Faktureringsplanen er satt opp med følgende data:

- **Startdato:** 1. mai 2019
- **Sluttdato:** 31. desember 2019
- **Beløp:** $ 1 000
- **Justeringsdato**: 31. desember 2019

I dette scenarioet er ikke justeringsdatoen nødvendig. Dette scenarioet er vanlig for automatiske fornyelser.

| Startdato for fakturering | Sluttdato for fakturering | Forrige avlesning | Gjeldende avlesning | Angitt antall | Gratis antall | Fakturerbart antall | Enhetspris |
|---|---|---|---|---|---|---|---|
| 01.05.2019 | 31.12.2019 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-6-calculated-dates"></a>Scenario 6: Beregnede datoer

Støtte og fornyelse er satt opp med følgende data:

- **Overstyr startdato:** Nei
- **Startdatoer for støtte og fornyelse:** Begynnelsen av neste måned
- **Fakturaposteringsdato:** 22. juni 2019
- **Justeringsdato:** 31. desember 2020

| Startdato for fakturering | Sluttdato for fakturering | Forrige avlesning | Gjeldende avlesning | Angitt antall | Gratis antall | Fakturerbart antall | Enhetspris |
|---|---|---|---|---|---|---|---|
| 01.07.2019 | 31.07.2019 | | | 1.00 | | 1.00 | 297.60 |
| 01.08.2019 | 31.12.2020 | | | 1.00 | | 1.00 | 6,936.00 |

## <a name="scenario-7-calculated-dates-and-future-posting"></a>Scenario 7: Beregnede datoer og fremtidig postering

Støtte og fornyelse er satt opp med følgende data:

- **Overstyr startdato:** Nei
- **Startdatoer for støtte og fornyelse:** Begynnelsen av neste måned
- **Fakturaposteringsdato:** 22. juni 2019
- **Justeringsdato:** 31. desember 2020

I dette scenarioet endres justeringsdatoen til 31. desember 2021.

| Startdato for fakturering | Sluttdato for fakturering | Forrige avlesning | Gjeldende avlesning | Angitt antall | Gratis antall | Fakturerbart antall | Enhetspris |
|---|---|---|---|---|---|---|---|
| 22.06.2019 | 22.06.2019 | | | 1.00 | | 1.00 | 0.00 |
| 01.08.2019 | 31.12.2020 | | | 1.00 | | 1.00 | 4,250.00 |

## <a name="scenario-8-manual-dates-and-multiple-years"></a>Scenario 8: Manuelle datoer og flere år

Støtte og fornyelse er satt opp med følgende data:

- **Overstyr startdato:** Ja
- **Startdato for fornying:** 1. juli 2020
- **Sluttdatoen for fornying:** 31. desember 2024
- **Justeringsdato:** 31. desember 2021

| Startdato for fakturering | Sluttdato for fakturering | Forrige avlesning | Gjeldende avlesning | Angitt antall | Gratis antall | Fakturerbart antall | Enhetspris |
|---|---|---|---|---|---|---|---|
| 22.06.2019 | 22.06.2019 | | | 1.00 | | 1.00 | 0.00 |
| 01.07.2020 | 31.12.2021 | | | 1.00 | | 1.00 | 375.00 |
| 1/1/2022 | 31.12.2022 | | | 1.00 | | 1.00 | 250,00 |
| 01.01.2023 | 31.12.2023 | | | 1.00 | | 1.00 | 250,00 |
| 01.01.2024 | 31.12.2024 | | | 1.00 | | 1.00 | 250,00 |

## <a name="scenario-9-manual-dates-multiple-years-and-a-different-end-month"></a>Scenario 9: Manuelle datoer, flere år og en annen sluttmåned

Støtte og fornyelse er satt opp med følgende data:

- **Overstyr startdato:** Ja
- **Startdato for fornying:** 1. juli 2020
- **Sluttdatoen for fornying:** 31. oktober 2024
- **Justeringsdato:** 31. desember 2021

| Startdato for fakturering | Sluttdato for fakturering | Forrige avlesning | Gjeldende avlesning | Angitt antall | Gratis antall | Fakturerbart antall | Enhetspris |
|---|---|---|---|---|---|---|---|
| 22.06.2019 | 22.06.2019 | | | 1.00 | | 1.00 | 0.00 |
| 01.07.2020 | 31.12.2021 | | | 1.00 | | 1.00 | 375.00 |
| 1/1/2022 | 31.12.2022 | | | 1.00 | | 1.00 | 250,00 |
| 01.01.2023 | 31.12.2023 | | | 1.00 | | 1.00 | 250,00 |
| 01.01.2024 | 31.10.2024 | | | 1.00 | | 1.00 | 208.33 |

## <a name="scenario-10-alignment-without-proration"></a>Scenario 10: Justering uten fordeling

Støtte og fornyelse er satt opp med følgende data:

- **Overstyr startdato:** Nei
- **Fakturaposteringsdato:** 22. juni 2019
- **Justeringsdato:** 31. desember 2019

Startdatoen for fornyelse og justeringsdatoene justeres slik at begge startdatoene er etter posteringsdatoen.

- **Startdato for fornying:** 1. januar 2020
- **Sluttdatoen for fornying:** 31. desember 2020
