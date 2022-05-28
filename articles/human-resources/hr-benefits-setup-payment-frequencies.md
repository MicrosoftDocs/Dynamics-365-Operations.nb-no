---
title: Definere betalingshyppigheter
description: Microsoft Dynamics 365 Human Resources bruker betalingsfrekvenser til å beregne den årlige fordelslønnen, bestemme fordelsbonusbeløpet en ansatt betaler hver lønnsperiode, og hvor ofte leverandører blir betalt.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 969369eb0edb7e8cbb9358bc7c3965a0145eaef0
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687142"
---
# <a name="set-up-payment-frequencies"></a>Definere betalingshyppigheter


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources bruker betalingsfrekvenser til å beregne den årlige fordelslønnen, bestemme fordelsbonusbeløpet en ansatt betaler hver lønnsperiode, og hvor ofte leverandører blir betalt.

Fordelsbetalingsfrekvenser bruker omregningsfaktorer til å konvertere fordelsbetalingsperioder mellom månedlig, halvmånedlig, annenhver uke, ukentlig og daglig betalingsfrekvens. Dette gjør at firmaer kan definere gjensidige avhengigheter mellom betalingsfrekvensene i en fordelsplan.

Feltene for omregningsfaktorer identifiserer omregningsfaktoren fra betalingsfrekvensen til standard betalingsperioder og tillater systemet å utføre beregninger mellom betalingsfrekvenser. Omregningsfaktorbeløpet bestemmer også fordelsbonusbeløpet en ansatt skal betale hver lønnsfrekvens.

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Betalingsfrekvenser**.

2. Velg **Ny**.

3. Angi verdier for de følgende feltene:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Betalingsfrekvens** | Et unikt navn på betalingsfrekvensen. |
   | **Beskrivelse** | En beskrivelse av betalingsfrekvensen. |
   | **Periode** | Den aktuelle perioden som best samsvarer med fordelsleverandørens og den ansattes betalingsfrekvens. Periodelisten består av standard betalingsperioder. |
   | **Antall lønnsperioder** | Antall lønnsperioder som representerer hvor ofte fordelsleverandøren eller de ansatte skal betales. Dette beløpet blir brukt til å beregne den ansattes årlige fordelslønnsbeløp. |
   | **Årlig konverteringsfaktor** | Den årlige konverteringsfaktoren for betalingsfrekvensen. Den årlige konverteringsfaktoren for den månedlige betalingsfrekvensen er for eksempel: </br></br>(12 månedlige betalinger / 1 år) = 12 |
   | **Halvårlig omregningsfaktor** | Den halvårlige konverteringsfaktoren for betalingsfrekvensen. Den halvårlige konverteringsfaktoren for den månedlige betalingsfrekvensen er for eksempel: </br></br>(12 månedlige betalinger / 2 ganger per år) = 6 |
   | **Kvartalsvis omregningsfaktor** | Den kvartalsmessige konverteringsfaktoren for betalingsfrekvensen. Den kvartalsmessige konverteringsfaktoren for den månedlige betalingsfrekvensen er for eksempel: </br></br>(12 månedlige betalinger / 4 kvartaler) = 3 |
   | **Månedlig omregningsfaktor** | Den månedlige konverteringsfaktoren for betalingsfrekvensen. Den månedlige konverteringsfaktoren for den månedlige betalingsfrekvensen er for eksempel: </br></br>(12 månedlige betalinger / 12 måneder) = 1 |
   | **Halvmånedlig omregningsfaktor** | Den halvmånedlige konverteringsfaktoren for betalingsfrekvensen. Den halvmånedlige konverteringsfaktoren for den månedlige betalingsfrekvensen er for eksempel: </br></br>(12 månedlige avdrag / 24 (2x per måned)) = 0,5 | 
   | **Omregningsfaktor for annenhver uke** | Den årlige konverteringsfaktoren for betalingsfrekvensen. Den årlige konverteringsfaktoren for den månedlige betalingsfrekvensen er for eksempel: </br></br>(12 månedlige betalinger / 26 uker) = 0,461538 |
   | **Ukentlig konverteringsfaktor** | Den årlige konverteringsfaktoren for betalingsfrekvensen. Den årlige konverteringsfaktoren for den månedlige betalingsfrekvensen er for eksempel: </br></br>(12 månedlige betalinger / 52 uker) = 0,230769 |
   | **Daglig omregningsfaktor** | Den årlige konverteringsfaktoren for betalingsfrekvensen. Den årlige konverteringsfaktoren for den månedlige betalingsfrekvensen er for eksempel: </br></br>(12 månedlige betalinger / 365 dager) = 0,032877 |
   | **Timebasert konverteringsfaktor** | Den årlige konverteringsfaktoren for betalingsfrekvensen. Den årlige konverteringsfaktoren for den månedlige betalingsfrekvensen er for eksempel: </br></br>(12 månedlige betalinger / 2080 timer) = 0,005769

4. Velg **Lagre**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
