---
title: "Reduksjonsnøkler"
description: "Denne artikkelen inneholder eksempler som viser hvordan du definerer en reduksjonsnøkkel. Den inneholder informasjon om de ulike innstillingene for reduksjonsnøkler for og resultatene av hver. Du kan bruke en reduksjonsnøkkel til å definere hvordan du kan redusere prognosebehov."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 30634b0af343ad171c385a95c4ba0934180f70cf
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="reduction-keys"></a>Reduksjonsnøkler

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder eksempler som viser hvordan du definerer en reduksjonsnøkkel. Den inneholder informasjon om de ulike innstillingene for reduksjonsnøkler for og resultatene av hver. Du kan bruke en reduksjonsnøkkel til å definere hvordan du kan redusere prognosebehov.

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a>Eksempel 1: Prosent - reduksjonsprinsipp for reduksjonsnøkkelprognose
---------------------------------------------------------------

Dette eksemplet viser hvordan en reduksjonsnøkkel reduserer behovene i behovsprognosen i henhold til prosentene og tidsperiodene som er definert av reduksjonsnøkkelen.

1.  På siden **Reduksjonsnøkler** definerer du følgende linjer.
    | Vekslepenger | Enhet  | Prosent |
    |--------|-------|---------|
    | 1      | Måned | 100     |
    | 2      | Måned | 75      |
    | 3      | Måned | 50      |
    | 4      | Måned | 25      |

2.  Koble reduksjonsnøkkelen til varens dekningsgruppe.
3.  På **Hovedplaner**-siden, i **Reduksjonsprinsipp**-feltet, velger du **Prosent - reduksjonsnøkkel**.
4.  Opprett en behovsprognose på 1 000 stykker per måned.

Hvis du kjører prognoseplanlegging 1. januar, forbrukes behovene i behovsprognosen i henhold til prosentene du definerer på **Reduksjonsnøkler**-siden. Følgende behovsantall overføres til hovedplanen.

| Måned                | Antall stykker som kreves |
|----------------------|---------------------------|
| Januar              | 0                         |
| Februar             | 250                       |
| Mars                | 500                       |
| April                | 750                       |
| Mai til desember | 1 000                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a>Eksempel 2: Transaksjoner - reduksjonsprinsipp for reduksjonsnøkkelprognose
Dette eksemplet viser hvordan faktiske ordrer som skjer i periodene som er definert av reduksjonsnøkkelen, reduserer behovene i behovsprognosen.

-   På **Hovedplaner**-siden, i **Reduksjonsprinsipp**-feltet, velger du **Transaksjoner - reduksjonsnøkkel**.

Følgende salgsordrer finnes den 1. januar.

| Måned    | Antall stykker som er bestilt |
|----------|--------------------------|
| Januar  | 956                      |
| Februar | 1,176                    |
| Mars    | 451                      |
| April    | 119                      |

Hvis du bruker den samme behovsprognosen på 1 000 stykker per måned, overføres følgende behovsantall til hovedplanen:

| Måned                | Antall stykker som kreves |
|----------------------|---------------------------|
| Januar              | 44                        |
| Februar             | 0                         |
| Mars                | 549                       |
| April                | 881                       |
| Mai til desember | 1 000                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a>Eksempel 3: Transaksjoner - reduksjonsprinsipp for dynamisk periodeprognose
I de fleste tilfeller er systemer er satt opp slik at transaksjoner reduserer behovsprognose i bestemte perioder for prognose: uker, måneder og så videre. Disse er definert i reduksjonsnøkkelen. Tiden mellom to behovsprognoselinjer kan imidlertid også *angi* en periode.

1.  Opprett en behovsprognose for følgende datoer og antall.
    | Dato       | Behovsprognose |
    |------------|-----------------|
    | 1. januar  | 1 000           |
    | 5. januar  | 500             |
    | 12. januar | 1 000           |

    I denne prognosen er det ikke en ledig periode mellom prognosedatoene: det finnes en periode på fire dager mellom første og andre dato, og det er et tidsintervall på sju dager mellom andre og tredje dato. Disse ulike intervallene er dynamiske perioder.
2.  Opprett salgsordrelinjer på følgende måte.
    | Dato                             | Salgsordreantall |
    |----------------------------------|----------------------|
    | 15. desember i fjor | 500                  |
    | 3. januar                        | 100                  |
    | 10. januar                       | 200                  |

Prognosen reduseres på følgende måte:

-   Den første salgsordren er ikke innenfor noen perioden, så den vil ikke redusere noen prognoser.
-   Den andre salgsordren er mellom 1. og 5. januar, så den vil redusere prognosen for 1. januar med 100.
-   Den tredje salgsordren er mellom 5. og 12. januar, så den vil redusere prognosen for 5. januar med 200.

Følgende planlagte ordre opprettes for å oppfylle prognosen.

| Behovsprognosedato | Redusert antall |
|----------------------|------------------|
| 1. januar            | 900              |
| 5. januar            | 300              |
| 12. januar           | 1 000            |

Her er et sammendrag av reduksjonen **Transaksjoner - dynamisk periode**:

-   Prognosebehov reduseres med de faktiske ordretransaksjonene som forekommer i løpet av en dynamiske perioden. Den dynamiske perioden dekker gjeldende prognosedatoer og slutter ved starten av neste prognose.
-   Denne metoden bruker eller krever ikke en reduksjonsnøkkel.
-   Når dette alternativet brukes, skjer følgende:
    -   Hvis prognosen reduseres fullstendig, blir behovene i prognosen for nåværende prognose 0 (null).
    -   Hvis det ikke er noen fremtidig prognose, reduseres behovene i prognosen fra den siste prognosen som ble angitt.
    -   Horisonter er inkludert i beregningen av prognosereduksjon.
    -   Positive dager er inkludert i beregningen av prognosereduksjon.
    -   Hvis faktiske ordretransaksjoner overskrider de prognoseberegnede kravene, videresendes ikke de gjenværende transaksjonene til neste prognoseperiode.


<a name="see-also"></a>Se også
--------

[Hovedplaner](master-plans.md)




