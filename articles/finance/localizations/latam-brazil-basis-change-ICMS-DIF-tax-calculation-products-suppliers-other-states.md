---
title: Grunnlagsendring i ICMS-DIF-avgiftsberegninger for produkter fra leverandører i andre delstater
description: Dette emnet beskriver konfigurasjonen for beregninger av ICMS-DIF-avgiftstypen når et regnskapsdokument mottas i den delstaten Rio Grande do Sul (RS) or São Paulo (SP) i Brasil.
author: Kai-Cloud
ms.date: 1/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 63e3cbaaf77456b55f08ea91831ba9d49cb57185
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689163"
---
# <a name="basis-change-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Grunnlagsendring i ICMS-DIF-avgiftsberegninger for produkter fra leverandører i andre delstater

Dette emnet beskriver konfigurasjonen for beregninger av **ICMS-DIF**-avgiftstypen når et regnskapsdokument mottas i den delstaten Rio Grande do Sul (RS) or São Paulo (SP) i Brasil.

I henhold til definisjonen i lovverket i delstaten må Imposto sobre Circulação de Mercadorias e Serviços (ICMS) som samles inn, følge denne regelen:

*ICMS for innsaling* = ([(*Driftsbeløp* – *ICMS fra kilde*) ÷ (1 – *ICMS % internt*)] × *ICMS % internt*) – *ICMS-beløp fra kilde*

## <a name="example"></a>Eksempel

Et brasiliansk firma i RS-delstaten mottar et regnskapsdokument for et kjøp fra en leverandør i SP-staten. Firmaet må samle inn prosentforskjellen i ICMS mellom RS-staten (18 prosent) og SP-staten (12 prosent). Grunnlaget må imidlertid beregnes i henhold til den forrige regelen.

- **Driftsbeløp:** 1000,00 brasilianske real (R$ 1000,00)
- **ICMS mellom stater:** R$ 120,00
- **ICMS-prosent i RS-staten**: 18 prosent
- **ICMS som skal samles inn i RS-staten:** (\[(1000 – 120) ÷ (1 – 0,18)\] × 0,18 ) – 120 = R$ 73,17 

## <a name="resolution"></a>Oppløsning

Hvis du vil beregne differensial for ICMS (ICMS-DIF) i henhold til reglene for RS-delstaten, må du definere mva-koder og en mva-gruppe på følgende måte:

1. Opprett en mva-kode for å motta 12 prosent-ICMS (for den andre staten). Denne koden brukes til å registrere innbetalingsbeløpet for merverdiavgift fra leverandøren.
2. Opprett en mva-kode for å samle inn ICMS-DIF. Denne mva-koden må ha et prosentbeløp på 18 prosent (for din egen stat) for å definere forskjellen mellom 18 prosent og 12 prosent. Angi avgiftstypen til **ICMS-DIF**. Denne mva-koden må defineres på følgende måte i beregningsparameterne:

    - I **Opprinnelse**-feltet velger du **Prosent av bruttobeløp**.
    - I feltet **Marginalgrunnlag** velger du **Nettobeløp per linje** eller **Nettobeløp på fakturasaldo**.
    - Definer avgiftskoden slik at den har en regnskapsverdi på **3**. På denne måten blir justeringstransaksjonen automatisk opprettet når modulen **Regnskapsbøker** er aktivert.
    - I konfigurasjonen til mva-gruppen velger du alternativet **Bruk avgift** for mva-koden **ICMS-DIF**.
