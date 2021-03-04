---
title: Mva-rapport for Finland
description: Dette emnet gir informasjon om hvordan du definerer og genererer mva-rapporten for juridiske enheter i Finland.
author: v-lurodi
ms.author: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
manager: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Norway
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2c8524befbfd61e7780f2b83ef96ed05480d4656
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408300"
---
# <a name="sales-tax-report-for-finland"></a>Mva-rapport for Finland

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du definerer og genererer mva-rapporten for juridiske enheter i Finland.

Hvis du vil ha generell informasjon om hvordan du definerer mva-oppgaven, kan du se [Mva-rapportering for Europa](emea-vat-reporting.md).

## <a name="set-up-the-report-layout-for-sales-tax-authorities"></a>Definere rapportoppsettet for skattemyndigheter

Hvis du vil generere mva-oppgaven i det riktige formatet for den aktuelle skattemyndigheten, må du definere rapportoppsettet for skattemyndighetene. På siden **Skattemyndigheter** velger du skattemyndigheten som skal brukes i mva-kodene for mva-utligningsperioden. I **Rapportoppsett**-feltet velger du deretter **Finsk rapportoppsett**.

## <a name="set-up-sales-tax-reporting-codes-for-vat-reporting"></a>Definere mva-rapporteringskoder for mva-rapportering

Definer mva-rapporteringkoder ved å følge instruksjonene i [Definere mva-rapporteringskoder](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md). Følgende tabell viser et eksempel på mva-rapporteringskoder for Finland.

| **Mva-rapporteringskoder** | **Beskrivelse**                                                                                                                                                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 301                          | Avgift på innenlandssalg ved 24 %.                                                                                                                                                                                                      |
| 302                          | Avgift på innenlandssalg ved 14 %.                                                                                                                                                                                                      |
| 303                          | Avgift på innenlandssalg ved 10 %.                                                                                                                                                                                                      |
| 304                          | MVA på import av varer fra utenfor EU.                                                                                                                                                                          |
| 305                          | Avgift på varer som kjøpes fra andre EU-land.                                                                                                                                                                                  |
| 306                          | Avgift på tjenester som kjøpes fra andre EU-land.                                                                                                                                                                               |
| 307                          | Fradragsberettiget avgift for mva-perioden.                                                                                                                                                                                                        |
| 308                          | Skyldig mva/negativ avgift som kvalifiseringer for refundering (-). I mva-rapporten beregnes verdien i denne boksen automatisk som summen av rapporteringskoder 301, 302, 303, 304, 305, 306 og 318, pluss rapporteringskoder 307 og 317. |
| 309                          | Avgiftspliktig salg med en mva-sats på 0 (null).                                                                                                                                                                                                  |
| 310                          | Import av varer fra utenfor EU.                                                                                                                                                                                                     |
| 311                          | Salg av varer til andre EU-land.                                                                                                                                                                                                     |
| 312                          | Salg av tjenester til andre EU-land.                                                                                                                                                                                                  |
| 313                          | Kjøp av varer fra andre EU-land.                                                                                                                                                                                               |
| 314                          | Kjøp av tjenester fra andre EU-land.                                                                                                                                                                                            |
| 315                          | Salg som kvalifiserer for mva-fradrag.                                                                                                                                                                                                        |
| 316                          | Avgift som kvalifiserer for mva-fradrag.                                                                                                                                                                                                        |
| 317                          | Beløp for mva-avdrag.                                                                                                                                                                                                                     |
| 318                          | Avgift på innkjøp av konstruksjonstjenester/skrapmetall (snudd avregning).                                                                                                                                                                   |
| 319                          | Salg av konstruksjonstjenester/skrapmetall.                                                                                                                                                                                               |
| 320                          | Kjøp av konstruksjonstjenester/skrapmetall.                                                                                                                                                                                           |
| 332                          | Beregningsfeil/skrivefeil.                                                                                                                                                                                                           |
| 333                          | Veiledning som mottas under en avgiftsrevisjon.                                                                                                                                                                                             |
| 334                          | Endring i gyldig praksis.                                                                                                                                                                                                                 |
| 335                          | Feil under tolking av skattelover.                                                                                                                                                                                                  |

## <a name="set-up-sales-tax-codes"></a>Definer mva-koder

Definer mva-koder ved å følge instruksjonene i [Mva-koder for mva-rapportering](emea-vat-reporting.md#sales-tax-codes-for-vat-reporting) og [Oversikt over merverdiavgift](../general-ledger/indirect-taxes-overview.md).

## <a name="generate-a-sales-tax-payment-and-print-the-finnish-sales-tax-report"></a><a name="generate-print-finnish"></a>Generere en mva-betaling og skrive ut den finske mva-rapporten

1. Gå til **Avgift** \> **Deklareringer** \> **Merverdiavgift** \> **Utlign og poster merverdiavgift**.
2. I dialogboksen **Rapporter merverdiavgift for utligningsperioden** angir du følgende felt:

| **Felt**                 | **Beskrivelse**                                                                                                                                                                                                                                                                                               |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Utligningsperiode         | Velg gjeldende rapporteringsperiode.                                                                                                                                                                                                                                                                       |
| Fra-dato                 | Angi den første datoen i mva-utligningsperioden du vil beregne mva for. Denne verdien tilsvarer datoen i **Fra**-feltet på siden **Mva-utligningsperioder**.                                                                                                                    |
| Transaksjonsdato          | Angi datoen da mva-rapporten blir beregnet. Standardverdi er gjeldende dato. Mva-betalingen beregnes for alle transaksjoner som ble postert i løpet av utligningsperioden.                                                                                                        |
| Mva-betalingsversjon | Velg typen mva-utligning. Velg **Opprinnelig** hvis denne avgiftsutligningen er den første mva-utligningen for perioden. Velg **Siste rettelser** hvis den **opprinnelige** mva-utligningen for perioden allerede er generert. Hvis du vil ha mer informasjon, kan du se [Opprette en mva-betaling](../general-ledger/tasks/create-sales-tax-payment.md). |

3. Velg **OK**.
4. I dialogboksen **Finsk mva-rapport** angir du følgende felt.

| **Felt**                       | **Beskrivelse**                                                                                                                                                                                                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Avgiftsvaluta                    | Velg valutaen som bestemmer hvilke transaksjoner som skal tas med i rapporten. Rapporten vil inkludere både transaksjoner som genereres ved hjelp av mva-valutaen og transaksjoner som genereres ved hjelp av avgiftskodene som bruker avgiftsvalutaen. |
| Rapporteringsvaluta              | Velg den utenlandske valutaen som rapporten skal genereres i.                                                                                                                                                                                                   |
| Valutakurs på rapporteringsdato | Sett alternativet til **Ja** for å angi at valutakursen på rapporteringsdatoen skal brukes for alle transaksjoner i rapporten.                                                                                                                                 |

5. Velg **OK** for å generere rapport for mva-betaling.

## <a name="print-the-finnish-sales-tax-report-from-the-sales-tax-payment"></a>Skrive ut den finske mva-rapporten fra mva-betalingen

1. Gå til **Avgift \> Forespørsler og rapporter \> Mva-betalinger** for å åpne siden **Mva-betaling**.
2. Velg posten som skal skrives ut, og velg deretter **Skriv ut rapport**.
3. I dialogboksen angir du feltene som beskrevet i den forrige delen, og deretter velger du **OK**.

## <a name="report-sales-tax-for-a-settlement-period"></a>Rapportere merverdiavgift for en utligningsperiode

Du kan generere den finske mva-rapporten ved hjelp av forespørselen **Rapporter merverdiavgift for utligningsperioden**.

1. Gå til **Avgift \> Deklareringer \> Merverdiavgift \> Rapporter merverdiavgift for utligningsperioden**.
2. I dialogboksen angir du feltene **Utligningsperiode**, **Fra-dato**, **Avgiftsvaluta** og **Rapporteringsvaluta** som beskrevet i delen [Generere en mva-betaling og skrive ut den finske mva-rapporten](#generate-print-finnish) tidligere i dette emnet.
3. I feltet **Mva-betalingsversjon** velger du en av følgende verdier:

   - **Opprinnelig** – Generer en rapport for mva-transaksjoner for den første posterte utligningsberegningen for perioden.
   - **Rettelser** – Generer en rapport for mva-transaksjoner for de etterfølgende posterte utligningsberegningene for perioden.
   - **Total liste** – Generer en rapport for alle salgstransaksjoner for perioden, inkludert den opprinnelige og alle rettelsene.

4. Velg **OK**.
5. I dialogboksen **Finsk mva-rapport** angir du feltene **Avgiftsvaluta**, **Rapporteringsvaluta** og **Valutakurs på rapporteringsdato** som beskrevet i delen [Generere en mva-betaling og skrive ut den finske mva-rapporten](#generate-print-finnish) tidligere i dette emnet.

## <a name="example"></a>Eksempel

Følgende eksempel viser hvordan du kan definere mva-koder og koder for mva-rapportering, postere transaksjoner og generere den finske mva-rapporten.

1.  Gå til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Mva-koder**, og konfigurer følgende mva-koder.

| **Mva-kode** | **Prosent** | **Beskrivelse**                                                                        |
|--------------------|----------------|----------------------------------------------------------------------------------------|
| FI24               | 24             | Innenlands salg og kjøp med en sats på 24 prosent                                   |
| FI14               | 14             | Innenlands salg og kjøp med en sats på 14 prosent                                   |
| FI10               | 10             | Innenlands salg og kjøp med en sats på 10 prosent                                   |
| FIEU24             | 24             | EU-kjøp med en sats på 24 prosent der **Use tax**-alternativet er angitt til **Ja**.   |
| FIEU14             | 14             | EU-kjøp med en sats på 14 prosent der **Use tax**-alternativet er angitt til **Ja**.   |
| FIEU10             | 10             | EU-kjøp med en sats på 10 prosent der **Use tax**-alternativet er angitt til **Ja**.  |
| FIImp24            | 24             | Import med en sats på 24 prosent der **Use tax**-alternativet er angitt til **Ja**.         |
| FIImp14            | 14             | Import med en sats på 14 prosent der **Use tax**-alternativet er angitt til **Ja**.         |
| FIImp10            | 10             | Import med en sats på 10 prosent der **Use tax**-alternativet er angitt til **Ja**.         |
| FIRC24             | 24             | Snudd avregning med en sats på 24 prosent der **Use tax**-alternativet er angitt til **Ja**. |
| FIRC14             | 14             | Snudd avregning med en sats på 14 prosent der **Use tax**-alternativet er angitt til **Ja**. |
| FIRC10             | 10             | Snudd avregning med en sats på 10 prosent der **Use tax**-alternativet er angitt til **Ja**. |
| FIEUS              | 0              | EU-salg der **Avgiftsfri**-alternativet er satt til **Ja**.                                |
| FIThird            | 0              | Eksportsalg der **Avgiftsfri**-alternativet er satt til **Ja**.                            |

2. På siden **Mva-koder**, i hurtigfanen **Rapportoppsett** tilordner du rapporteringskoder til mva-koder.

Følgende tabell viser hvordan du tilordner koder for mva-rapportering til mva-koder.

| **Mva-kode** | **Avgiftspliktig salg** | **Avgiftsfritt salg** | **Konto, utgående merverdiavgift** | **Avgiftspliktige innkjøp** | **Konto, innkommende merverdiavgift** | **Avgiftspliktig import** | **Use tax** | **Motregning av use tax** |
|--------------------|-------------------|-------------------|-----------------------|-----------------------|--------------------------|--------------------|-------------|--------------------|
| FI24               |                   |                   | 301                   |                       | 307                      |                    |             |                    |
| FI14               |                   |                   | 302                   |                       | 307                      |                    |             |                    |
| FI10               |                   |                   | 303                   |                       | 307                      |                    |             |                    |
| FIEU24             |                   |                   |                       |                       |                          | 313                | 307         | 305                |
| FIEU14             |                   |                   |                       |                       |                          | 313                | 307         | 305                |
| FIEU10             |                   |                   |                       |                       |                          | 313                | 307         | 305                |
| FIImp24            |                   |                   |                       |                       |                          | 310                | 307         | 304                |
| FIImp14            |                   |                   |                       |                       |                          | 310                | 307         | 304                |
| FIImp10            |                   |                   |                       |                       |                          | 310                | 307         | 304                |
| FIRC24             |                   |                   |                       |                       |                          | 320                | 307         | 318                |
| FIRC14             |                   |                   |                       |                       |                          | 320                | 307         | 318                |
| FIRC10             |                   |                   |                       |                       |                          | 320                | 307         | 318                |
| FIEUS              |                   | 311               |                       |                       |                          |                    |             |                    |
| FIThird            |                   | 309               |                       |                       |                          |                    |             |                    |

> [!NOTE]
> Den foregående konfigurasjonen er bare et eksempel, og er avhengig av strukturen til mva-kodene som brukes. Hvis du vil at verdier skal beregnes og overføres til mva-rapporten, må du angi en relevant kode for mva-rapportering i ett eller flere felt i kategorien **Rapportoppsett** for hver avgiftskode som brukes i betalingsprosessen for merverdiavgift.

3. Poster følgende transaksjoner. For kundefakturaer går du for eksempel til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**, for leverandørfakturaer går du til **Leverandører** \> **Fakturaer** \> **Fakturajournal**.

| **Dato**         | **transaksjonstype**            | **Nettobeløp** | **Mva-beløp** | **Mva-kode** | **Forventet avgiftsgrunnlag – rapporteringskode** | **Forventet avgiftsbeløp – rapporteringskode** |
|------------------|---------------------------------|----------------|----------------|--------------------|----------------------------------------|------------------------------------------|
| 1. februar 2020 | Kundefaktura (innenlands)     | 100            | 24             | FI24               | Gjelder ikke                         | 301                                      |
| 1. februar 2020 | Leverandørfaktura (EU)             | 100            | 14             | FIEU14             | 313                                    | 305 – skyldig mva. 307 – avgiftsfradrag    |
| 1. februar 2020 | Leverandørfaktura (import)         | 100            | 10             | FIImp10            | 310                                    | 304 – skyldig mva. 307 – avgiftsfradrag    |
| 1. februar 2020 | Kundefaktura (EU)           | 100            | 0              | FIEUS              | 311                                    | Gjelder ikke                           |
| 1. februar 2020 | Kundefaktura (eksport)       | 100            | 0              | FIThird            | 309                                    | Gjelder ikke                           |
| 1. februar 2020 | Leverandørfaktura (snudd avregning) | 100            | 24             | FIRC24             | 320                                    | 318 – skyldig mva. 307 – avgiftsfradrag    |

4. Gå til **Avgift** \> **Deklareringer** \> **Merverdiavgift** \> **Utlign og poster merverdiavgift**. I dialogboksen **Rapporter merverdiavgift for utligningsperioden** i feltet **Mva-betalingsversjon** velger du **Opprinnelig**.
5. Skriv ut rapporten og se gjennom dataene.

![Rapporteringsdata for merverdiavgift, opprinnelig versjon](media/1_Sales_tax_reporting.png)

6. Poster den nye transaksjonen. Gå for eksempel til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**.

| **Dato**         | **transaksjonstype**        | **Nettobeløp** | **Mva-beløp** | **Mva-kode** | **Forventet avgiftsgrunnlag – rapporteringskode** | **Forventet avgiftsbeløp – rapporteringskode** |
|------------------|-----------------------------|----------------|----------------|--------------------|----------------------------------------|------------------------------------------|
| 1. februar 2020 | Kundefaktura (innenlands) | 100            | 10             | FI10               | Gjelder ikke                         | 303                                      |

7. Gå til **Avgift** \> **Deklareringer** \> **Merverdiavgift** \> **Utlign og poster merverdiavgift**. I dialogboksen **Rapporter merverdiavgift for utligningsperioden** i feltet **Mva-betalingsversjon** velger du **Siste rettelser**.
8. Gå til **Avgift** \> **Deklareringer** \> **Merverdiavgift** \> **Rapporter merverdiavgift for utligningsperioden**. I dialogboksen **Rapporter merverdiavgift for utligningsperioden** i feltet **Mva-betalingsversjon** velger du **Rettelser**.

![Rettelser av mva-betalingsversjon](media/2_Sales_tax_reporting.png)

9. Gå til **Avgift** \> **Deklareringer** \> **Merverdiavgift** \> **Rapporter merverdiavgift for utligningsperioden**. I dialogboksen **Rapporter merverdiavgift for utligningsperioden** i feltet **Mva-betalingsversjon** velger du **Total liste**.

![Total liste over versjoner av mva-betalinger i utligningsperioden](media/3_Sales_tax_reporting.png)

## <a name="additional-information"></a>Tilleggsinformasjon

Hvis du definerer snudd avregning i henhold til [Snudd avregning](emea-reverse-charge.md), kan du hente data om rapporteringskodene i rapporten **Mva-betaling etter rapporteringskode**.

1. Gå til **Avgift** \> **Forespørsler og rapporter** \> **Merverdiavgiftsrapporter** \> **Mva-betaling etter rapporteringskode**.
2. I dialogboksen angir du feltene **Utligningsperiode** og **Fra-dato**.
3. Velg **OK**, og se over rapportresultatet.

![Mva-betaling etter rapporteringskode](media/4_Reverse_charge.png)


## <a name="report-a-vat-declaration-to-the-tax-authority"></a>Rapportere en mva-deklarering til skattemyndighetene

Når du har generert den finske mva-rapporten, bruker du dataene på den til å fylle ut den selvvurderte avgiftsrapporten for den finske skatteetaten i det offisielle formatet. Illustrasjonen nedenfor viser for eksempel hva den finske egenvurderte avgiftsrapporten har sett ut siden 2019.

![Finsk selvvurdert avgiftsrapport](media/5_Finnish_VAT_declaration.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]