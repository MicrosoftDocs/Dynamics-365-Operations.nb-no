---
title: Grunnlagsendring i ICMS-DIF-avgiftsberegninger for produkter fra leverandører i andre delstater
description: Denne artikkelen beskriver konfigurasjonen for beregninger av ICMS-DIF-avgiftstypen når et regnskapsdokument mottas i den delstaten Rio Grande do Sul (RS) or São Paulo (SP) i Brasil.
author: Kai-Cloud
ms.date: 06/21/2022
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
ms.openlocfilehash: 1bd9982a3804778a27203b4311682ee8bc3c4841
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218658"
---
# <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Grunnlagsendring (dobbelt grunnlag) i ICMS-DIF-avgiftsberegninger for produkter fra leverandører i andre delstater

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
    - Velg **Nettobeløp per linje** i **Marginalbase**-feltet.
    - Definer avgiftskoden slik at den har en regnskapsverdi på **3**. På denne måten blir justeringstransaksjonen automatisk opprettet når modulen **Regnskapsbøker** er aktivert.
    - I konfigurasjonen til mva-gruppen velger du alternativet **Bruk avgift** for mva-koden **ICMS-DIF**.

### <a name="use-the-delta-tax-rate-in-the-configuration-of-dual-base-icms-dif-sales-tax-codes"></a>Bruk deltaavgiftssatsen i konfigurasjonen av dobbel base ICMS-DIF-merverdiavgiftskoder

Når innstillingene som er beskrevet tidligere blir brukt, blir **ICMS-DIF**-merverdiavgiftskoden beregnet i den doble basisregelen. Den påminte avgiftssatsen blir 18 prosent, som er forskjellig fra satsen på 6 prosent i den enkle basisregelen. Denne forskjellen forårsaker inkonsekvensproblemer i regnskapsdokumenter og avgiftsrapportering. Per Microsoft Dynamics 365 Finance, versjon 10.0.29 kan du aktivere **(Brasil) Konfigurer deltaavgiftssatsen i ICMS-DIF-avgiftskode for dobbel basissak**-funksjonen i **Funksjonsbehandling** for å fjerne inkonsekvensen.

- I tillegg til å fullføre trinnene i den forrige delen, velger du mva-koden for **ICMS 12** i feltet **Merverdiavgift på merverdiavgift**.
- Angi avgiftssatsen for **ICMS-DIF**-mva-koden til 18 prosent. I **Prosent/beløp**-feltet vises den nominelle avgiftssatsen som 6 prosent.

> [!NOTE]
> Mva-kodene **ICMS-DIF** og **ICMS 12** må tildeles i samme mva-gruppe.

## <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-to-non-taxpayer-consumers-difal-in-other-states"></a>Grunnlagsendring (dobbelt grunnlag) i ICMS-DIF-avgiftsberegninger for produkter til ikke-avgiftsbetalerforbrukere (DIFAL) fra leverandører i andre delstater

Aktiver funksjonen **(Brasil) Beregning av dobbeltgrunnlag for ICMS-DIFAL i salgstransaksjoner** i **Funksjonsbehandling** for å støtte basisendringen ICMS-DIF på handel til ikke-avgiftsbetalerforbrukere fra en annen stat. Eksempelet ICMS-DIF-mva-kode blir gyldig i salgsordre- og fritekstfakturatransaksjoner.

Aktiver **(Brasil) Beregning av dobbeltgrunnlag for ICMS-DIFAL i salgstransaksjoner**-funksjonen i **Funksjonsbehandling** for å støtte scenarioer der handel til ikke-avgiftsbetalerforbrukere fra en annen stat er ansvarlig for Imposto sobre Produtos Industrializzos (IPI). Avgiftsbeløpet til IPI-mva-koden gjenkjennes og brukes i avgiftsgrunnlaget ICMS-DIFAL.

- I hodet til salgsordren eller fritekstfakturaen i hurtigfanen **Regnskapsinformasjon** må alternativet **Endelig bruker** settes til **Ja**.
- I hodet til bestillingen eller leverandørfakturaen i hurtigfanen **Regnskapsinformasjon** må alternativet **Bruk og forbruk** settes til **Ja**.
