---
title: Sentraliserte betalinger for Leverandører
description: Organisasjoner som omfatter flere juridiske enheter, kan opprette og administrere betalinger ved hjelp av én juridisk enhet som håndterer alle betalinger. Derfor trenger ikke de samme betalingene angis i flere juridiske enheter. Denne artikkelen inneholder eksempler som viser hvordan postering for sentralisert betaling skal håndteres i ulike scenarier.
author: abruer
manager: AnnBe
ms.date: 02/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14341
ms.assetid: 7bd02e32-2416-4ac6-8a60-85525267fdb7
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a4632056d6873cfeb748251c77becc410f5cf54
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837426"
---
# <a name="centralized-payments-for-accounts-payable"></a>Sentraliserte betalinger for Leverandører

[!include [banner](../includes/banner.md)]

Organisasjoner som omfatter flere juridiske enheter, kan opprette og administrere betalinger ved hjelp av én juridisk enhet som håndterer alle betalinger. Derfor trenger ikke de samme betalingene angis i flere juridiske enheter. Denne artikkelen inneholder eksempler som viser hvordan postering for sentralisert betaling skal håndteres i ulike scenarier.

Organisasjoner som omfatter flere juridiske enheter, kan opprette og administrere betalinger ved hjelp av en juridisk enhet som håndterer alle betalinger. Derfor trenger ikke de samme betalingene angis i flere juridiske enheter. I tillegg sparer organisasjonen tid, fordi betalingsprosessen er strømlinjeformet.

Det finnes mange juridiske enheter for operasjoner i en sentralisert betalingsorganisasjon, og hver juridiske enhet administrerer sine egne leverandørfakturaer. Betalinger for alle de operative juridiske enhetene genereres fra en juridisk enhet, som kalles den juridiske enheten for betalingen. Under utligningsprosessen genereres de aktuelle "skal betales til"- og "skal betales fra"-transaksjonene. Du kan angi hvilken juridisk enhet i organisasjonen som skal motta de realiserte gevinst- eller tapstransaksjonene og hvordan kontantrabattransaksjoner i forbindelse med betalinger mellom firmaer skal håndteres. På linjen for sentralisert betaling settes **Kontotype** til Leverandør. **Motkontotype** settes til Bank eller Finans. Bankkontoen må være i gjeldende firma. 

I eksemplene nedenfor ser du hvordan postering håndteres i ulike scenarier. Følgende konfigurasjon antas for alle disse eksemplene:

-   De juridiske enhetene er Fabrikam, Fabrikam Øst og Fabrikam Vest. Betalingene blir gjort fra Fabrikam.
-   Feltet **Poster kontantrabatt** på siden **Konserninternt regnskap** er satt til **Juridisk enhet for faktura**.
-   Feltet **Poster valutakursgevinst eller -tap** på siden **Konserninternt regnskap** er satt til **Juridisk enhet for betaling**.
-   Leverandøren Fourth Coffee defineres som en leverandør i hver juridiske enhet. Leverandørene fra de forskjellige juridiske enhetene er identifisert som samme leverandør, fordi de har den samme globale adressebok-IDen.

| Katalog-ID | Leverandørnummer | Navn          | Juridisk enhet  |
|--------------|----------------|---------------|---------------|
| 1050         | 3004           | Fourth Coffee | Fabrikam      |
| 1050         | 100            | Fourth Coffee | Fabrikam øst |
| 1050         | 3004           | Fourth Coffee | Fabrikam vest |

## <a name="example-1-vendor-payment-of-invoice-from-another-legal-entity"></a>Eksempel 1: Leverandørbetaling av faktura fra en annen juridisk enhet
Fabrikam Øst har en åpen faktura for leverandørkonto 100, Fourth Coffee. Fabrikam legger inn og posterer betaling til Fabrikams leverandørkonto 3004, Fourth Coffee. Betalingen utlignes med den åpne fakturaen.

### <a name="invoice-is-posted-in-fabrikam-east-for-vendor-100"></a>Fakturaen er postert i Fabrikam Øst for leverandør 100

| Konto                          | Debetbeløp | Kreditbeløp |
|----------------------------------|--------------|---------------|
| Utgift (Fabrikam Øst)          | 600,00       |               |
| Leverandører (Fabrikam Øst) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Betalingen genereres og posteres i Fabrikam for leverandør 3004

| Konto                     | Debetbeløp | Kreditbeløp |
|-----------------------------|--------------|---------------|
| Leverandører (Fabrikam) | 600,00       |               |
| Kontant (Fabrikam)             |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam-betalingen utlignes med Fabrikam Øst-fakturaen

**Fabrikam-postering**

| Konto                           | Debetbeløp | Kreditbeløp |
|-----------------------------------|--------------|---------------|
| Skal betales fra Fabrikam Øst (Fabrikam) | 600,00       |               |
| Leverandører (Fabrikam)       |              | 600,00        |

**Fabrikam Øst-postering**

| Konto                          | Debetbeløp | Kreditbeløp |
|----------------------------------|--------------|---------------|
| Leverandører (Fabrikam Øst) | 600,00       |               |
| Skal betales til Fabrikam (Fabrikam Øst)  |              | 600,00        |

## <a name="example-2-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>Eksempel 2: Leverandørbetaling av faktura fra en annen juridisk enhet med kontantrabatt
Fabrikam Øst har en åpen faktura for leverandør 100, Fourth Coffee. Fakturaen har en mulighet for en kontantrabatt på 20,00. Fabrikam legger inn og posterer en betaling på 580,00 for Fabrikam-leverandør 3004, Fourth Coffee. Betalingen utlignes med de åpne Fabrikam Øst-fakturaene. Kontantrabatten posteres til den juridiske enheten for fakturaen, Fabrikam Øst.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Fakturaen posteres i Fabrikam Øst for Fabrikam Øst-leverandør 100

| Konto                          | Debetbeløp | Kreditbeløp |
|----------------------------------|--------------|---------------|
| Utgift (Fabrikam Øst)          | 600,00       |               |
| Leverandører (Fabrikam Øst) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Betalingen genereres og posteres i Fabrikam for Fabrikam-leverandør 3004

| Konto                     | Debetbeløp | Kreditbeløp |
|-----------------------------|--------------|---------------|
| Leverandører (Fabrikam) | 580,00       |               |
| Kontant (Fabrikam)             |              | 580,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam-betalingen utlignes med Fabrikam Øst-fakturaen

**Fabrikam-postering**

| Konto                           | Debetbeløp | Kreditbeløp |
|-----------------------------------|--------------|---------------|
| Skal betales fra Fabrikam Øst (Fabrikam) | 580,00       |               |
| Leverandører (Fabrikam)       |              | 580,00        |

**Fabrikam Øst-postering**

| Konto                          | Debetbeløp | Kreditbeløp |
|----------------------------------|--------------|---------------|
| Leverandører (Fabrikam Øst) | 580,00       |               |
| Skal betales til Fabrikam (Fabrikam Øst)  |              | 580,00        |
| Leverandører (Fabrikam Øst) | 20,00        |               |
| Kontantrabatt (Fabrikam Øst)    |              | 20,00         |

## <a name="example-3-vendor-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-loss"></a>Eksempel 3: Leverandørbetaling av faktura fra en annen juridisk enhet med realisert kurstap
Fabrikam Øst har en åpen faktura for leverandør 100, Fourth Coffee. Fabrikam legger inn og posterer betaling for Fabrikams leverandør 3004, Fourth Coffee. Betalingen utlignes med den åpne Fabrikam Øst-fakturaen. En kurstapstransaksjon genereres under utligningsprosessen.

-   Vekslingskursen mellom EUR og USD på fakturadatoen: 1,2062
-   Vekslingskursen mellom EUR og USD på betalingsdatoen: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Fakturaen posteres i Fabrikam Øst for Fabrikam Øst-leverandør 100

| Konto                          | Debetbeløp            | Kreditbeløp           |
|----------------------------------|-------------------------|-------------------------|
| Utgift (Fabrikam Øst)          | EUR 600,00 / USD 723,72 |                         |
| Leverandører (Fabrikam Øst) |                         | EUR 600,00 / USD 723,72 |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Betalingen genereres og posteres i Fabrikam for Fabrikam-leverandør 3004

| Konto                     | Debetbeløp            | Kreditbeløp           |
|-----------------------------|-------------------------|-------------------------|
| Leverandører (Fabrikam) | EUR 600,00 / USD 736.62 |                         |
| Kontant (Fabrikam)             |                         | EUR 600,00 / USD 736.62 |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam-betalingen utlignes med Fabrikam Øst-fakturaen

**Fabrikam-postering**

| Konto                           | Debetbeløp            | Kreditbeløp           |
|-----------------------------------|-------------------------|-------------------------|
| Skal betales fra Fabrikam Øst (Fabrikam) | EUR 600,00 / USD 736.62 |                         |
| Leverandører (Fabrikam)       |                         | EUR 600,00 / USD 736.62 |
| Realisert tap (Fabrikam)          | EUR 0,00 / USD 12,90    |                         |
| Skal betales fra Fabrikam Øst (Fabrikam) |                         | EUR 0,00 / USD 12,90    |

**Fabrikam Øst-postering**

| Konto                          | Debetbeløp            | Kreditbeløp           |
|----------------------------------|-------------------------|-------------------------|
| Leverandører (Fabrikam Øst) | EUR 600,00 / USD 736,62 |                         |
| Skal betales til Fabrikam (Fabrikam Øst)  |                         | EUR 600,00 / USD 736,62 |
| Skal betales til Fabrikam (Fabrikam Øst)  | EUR 0,00 / USD 12,90    |                         |
| Leverandører (Fabrikam Øst) |                         | EUR 0,00 / USD 12,90    |

## <a name="example-4-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-loss"></a>Eksempel 4: Leverandørbetaling av faktura fra en annen juridisk enhet med kontantrabatt og realisert kurstap
Fabrikam Øst har en åpen faktura for leverandør 100, Fourth Coffee. Fakturaen har en kontantrabatt tilgjengelig, og det genereres en mva-transaksjon. Fabrikam legger inn en betaling for Fabrikams leverandør 3004, Fourth Coffee. Betalingen utlignes med den åpne Fabrikam Øst-fakturaen. En kurstapstransaksjon genereres under utligningsprosessen. Kontantrabatten posteres til den juridiske enheten for faktura (Fabrikam Øst), og kurstapet posteres til den juridiske enheten for betaling (Fabrikam).

-   Vekslingskursen mellom EUR og USD på fakturadatoen: 1,2062
-   Vekslingskursen mellom EUR og USD på betalingsdatoen: 1,2277

### <a name="invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-vendor-100"></a>Fakturaen posteres og en avgiftstransaksjon genereres i Fabrikam Øst for leverandør 100

| Konto                          | Debetbeløp            | Kreditbeløp           |
|----------------------------------|-------------------------|-------------------------|
| Utgift (Fabrikam Øst)          | EUR 564,07 / USD 680,38 |                         |
| Omsetningsavgift (Fabrikam Øst)        | EUR 35,93 / USD 43,34   |                         |
| Leverandører (Fabrikam Øst) |                         | EUR 600,00 / USD 723,72 |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Betalingen genereres og posteres i Fabrikam for leverandør 3004

| Konto                     | Debetbeløp            | Kreditbeløp           |
|-----------------------------|-------------------------|-------------------------|
| Leverandører (Fabrikam) | EUR 588,72 / USD 722,77 |                         |
| Kontant (Fabrikam Øst)        |                         | EUR 588,72 / USD 722,77 |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam-betalingen utlignes med Fabrikam Øst-fakturaen

**Fabrikam-postering**

| Konto                           | Debetbeløp            | Kreditbeløp           |
|-----------------------------------|-------------------------|-------------------------|
| Skal betales fra Fabrikam Øst (Fabrikam) | EUR 588,72 / USD 722,77 |                         |
| Leverandører (Fabrikam)       |                         | EUR 588,72 / USD 722,77 |
| Realisert tap (Fabrikam)          | EUR 0,00 / USD 12,66    |                         |
| Skal betales fra Fabrikam Øst (Fabrikam) |                         | EUR 0,00 / USD 12,66    |

**Fabrikam Øst-postering**

| Konto                          | Debetbeløp            | Kreditbeløp           |
|----------------------------------|-------------------------|-------------------------|
| Leverandører (Fabrikam Øst) | EUR 588,72 / USD 722,77 |                         |
| Skal betales til Fabrikam (Fabrikam Øst)  |                         | EUR 588,72 / USD 722,77 |
| Skal betales til Fabrikam (Fabrikam Øst)   | EUR 0,00 / USD 12,66    |                         |
| Leverandører (Fabrikam Øst) |                         | EUR 0,00 / USD 12,66    |
| Leverandører (Fabrikam Øst) | EUR 11,28 / USD 13,61   |                         |
| Kontantrabatt (Fabrikam Øst)    |                         | EUR 11,28 / USD 13,61   |

## <a name="example-5-vendor-credit-note-with-primary-payment"></a>Eksempel 5: Leverandørkreditnota med hovedbetaling
Fabrikam genererer en betaling på 75,00 for leverandør 3004, Fourth Coffee. Betalingen utlignes med en åpen faktura for Fabrikam Vest-leverandør 3004 og en åpen kreditnota for Fabrikam Øst-leverandør 100. Betalingen velges som hovedbetaling på siden **Utlign transaksjoner**.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Fakturaen posteres til Fabrikam West for leverandør 3004

| Konto                          | Debetbeløp | Kreditbeløp |
|----------------------------------|--------------|---------------|
| Utgift (Fabrikam Vest)          | 100,00       |               |
| Leverandører (Fabrikam Vest) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Kreditnotaen posteres til Fabrikam Øst for leverandør 100

| Konto                          | Debetbeløp | Kreditbeløp |
|----------------------------------|--------------|---------------|
| Leverandører (Fabrikam Øst) | 25,00        |               |
| Kjøpsreturer (Fabrikam Øst) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Betalingen posteres til Fabrikam for leverandør 3004

| Konto                     | Debetbeløp | Kreditbeløp |
|-----------------------------|--------------|---------------|
| Leverandører (Fabrikam) | 75,00        |               |
| Kontant (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam-betalingen utlignes med Fabrikam Vest-fakturaen og Fabrikam Øst-kreditnotaen

**Fabrikam-postering**

| Konto                           | Debetbeløp | Kreditbeløp |
|-----------------------------------|--------------|---------------|
| Leverandører (Fabrikam)       | 25,00        |               |
| Skal betales til Fabrikam Øst (Fabrikam)   |              | 25,00         |
| Skal betales fra Fabrikam Vest (Fabrikam) | 100,00       |               |
| Leverandører (Fabrikam)       |              | 100,00        |

**Fabrikam Øst-postering**

| Konto                           | Debetbeløp | Kreditbeløp |
|-----------------------------------|--------------|---------------|
| Skal betales fra Fabrikam (Fabrikam Øst) | 25,00        |               |
| Leverandører (Fabrikam Øst)  |              | 25,00         |

**Fabrikam Vest-postering**

| Konto                          | Debetbeløp | Kreditbeløp |
|----------------------------------|--------------|---------------|
| Leverandører (Fabrikam Vest) | 100,00       |               |
| Skal betales til Fabrikam (Fabrikam Vest)  |              | 100,00        |

## <a name="example-6-vendor-credit-note-without-primary-payment"></a>Eksempel 6: Leverandørkreditnota uten hovedbetaling
Fabrikam genererer en betaling på 75,00 for leverandør 3004, Fourth Coffee. Betalingen utlignes med en åpen faktura for Fabrikam Vest-leverandør 3004 og en åpen kreditnota for Fabrikam Øst-leverandør 100. Betalingen velges ikke som hovedbetaling på siden **Utlign transaksjoner**.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Fakturaen posteres til Fabrikam West for leverandør 3004

| Konto                          | Debetbeløp | Kreditbeløp |
|----------------------------------|--------------|---------------|
| Utgift (Fabrikam Vest)          | 100,00       |               |
| Leverandører (Fabrikam Vest) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Kreditnotaen posteres til Fabrikam Øst for leverandør 100

| Konto                          | Debetbeløp | Kreditbeløp |
|----------------------------------|--------------|---------------|
| Leverandører (Fabrikam Øst) | 25,00        |               |
| Kjøpsreturer (Fabrikam Øst) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Betalingen posteres til Fabrikam for leverandør 3004

| Konto                     | Debetbeløp | Kreditbeløp |
|-----------------------------|--------------|---------------|
| Leverandører (Fabrikam) | 75,00        |               |
| Kontant (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam-betalingen utlignes med Fabrikam Vest-fakturaen og Fabrikam Øst-kreditnotaen

**Fabrikam-postering**

| Konto                           | Debetbeløp | Kreditbeløp |
|-----------------------------------|--------------|---------------|
| Skal betales fra Fabrikam Vest (Fabrikam) | 75,00        |               |
| Leverandører (Fabrikam)       |              | 75,00         |

**Fabrikam Øst-postering**

| Konto                                | Debetbeløp | Kreditbeløp |
|----------------------------------------|--------------|---------------|
| Skal betales fra Fabrikam Vest (Fabrikam Øst) | 25,00        |               |
| Leverandører (Fabrikam Øst)       |              | 25,00         |

**Fabrikam Vest-postering**

| Konto                              | Debetbeløp | Kreditbeløp |
|--------------------------------------|--------------|---------------|
| Leverandører (Fabrikam Vest)     | 75,00        |               |
| Skal betales til Fabrikam (Fabrikam Vest)      |              | 75,00         |
| Leverandører (Fabrikam Vest)     | 25,00        |               |
| Skal betales til Fabrikam Øst (Fabrikam Vest) |              | 25,00         |





