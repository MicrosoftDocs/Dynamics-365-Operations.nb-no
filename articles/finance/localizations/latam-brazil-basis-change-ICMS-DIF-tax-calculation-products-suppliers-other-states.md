---
title: Grunnlagsendring i ICMS-DIF-avgiftsberegninger for produkter fra leverandører i andre delstater
description: Denne artikkelen beskriver konfigurasjonen for beregninger av ICMS-DIF-avgiftstypen når et regnskapsdokument mottas i den delstaten Rio Grande do Sul (RS) or São Paulo (SP) i Brasil.
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
ms.openlocfilehash: 1fde18c79f375db4db6bc52cdb5c40a61625ae63
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868269"
---
# <a name="basis-change-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Grunnlagsendring i ICMS-DIF-avgiftsberegninger for produkter fra leverandører i andre delstater

Denne artikkelen beskriver konfigurasjonen for beregninger av **ICMS-DIF**-avgiftstypen når et regnskapsdokument mottas i den delstaten Rio Grande do Sul (RS) or São Paulo (SP) i Brasil.

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
