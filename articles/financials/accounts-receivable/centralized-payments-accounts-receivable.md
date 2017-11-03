---
title: Sentraliserte betalinger for kunder
description: "Organisasjoner som omfatter flere juridiske enheter, kan opprette og administrere betalinger ved hjelp av én juridisk enhet som håndterer alle betalinger. Derfor trenger ikke den samme transaksjonen angis i flere juridiske enheter. Denne artikkelen inneholder eksempler som viser hvordan postering for sentralisert betaling skal håndteres i ulike scenarier."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6327d9cab1651d22cd411f718f6e3a2f8733e13e
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="centralized-payments-for-accounts-receivable"></a>Sentraliserte betalinger for kunder

[!include[banner](../includes/banner.md)]


Organisasjoner som omfatter flere juridiske enheter, kan opprette og administrere betalinger ved hjelp av én juridisk enhet som håndterer alle betalinger. Derfor trenger ikke den samme transaksjonen angis i flere juridiske enheter. Denne artikkelen inneholder eksempler som viser hvordan postering for sentralisert betaling skal håndteres i ulike scenarier.

Organisasjoner som omfatter flere juridiske enheter, kan opprette og administrere betalinger ved hjelp av en juridisk enhet som håndterer alle betalinger. Derfor trenger ikke den samme transaksjonen angis i flere juridiske enheter. I tillegg sparer organisasjonen tid, fordi prosessene for betalingsforslag, utligninger og redigering av åpne og lukkede transaksjoner for sentraliserte betalinger er strømlinjeformet. 

Det finnes mange juridiske enheter for operasjoner i en sentralisert betalingsorganisasjon, og hver juridiske enhet administrerer sin egen kundefakturainformasjon. Betalinger for alle de operative juridiske enhetene mottas av en juridisk enhet, som kalles den juridiske enheten for betalingen. Under utligningsprosessen genereres de aktuelle "skal betales til"- og "skal betales fra"-transaksjonene. Du kan angi hvilken juridisk enhet i organisasjonen som skal motta de realiserte gevinst- eller tapstransaksjonene, og hvordan kontantrabattransaksjoner i forbindelse med sentraliserte betalinger skal håndteres. 

I eksemplene nedenfor ser du hvordan postering håndteres i ulike scenarier. Følgende konfigurasjon antas for alle disse eksemplene:

-   De juridiske enhetene er Fabrikam, Fabrikam Øst og Fabrikam Vest. Kundebetalinger registreres i Fabrikam.
-   Feltet **Poster kontantrabatt** på siden **Konserninternt regnskap** er satt til **Juridisk enhet for faktura**.
-   Feltet **Poster valutakursgevinst eller -tap** på siden **Konserninternt regnskap** er satt til **Juridisk enhet for betaling**.
-   Leverandøren Gastronor Delikatesser defineres som en kunde i hver juridiske enhet. Kundene fra de forskjellige juridiske enhetene er identifisert som samme kunde, fordi de har den samme globale adressebok-ID.

| Adressebok-ID | Kundekonto | Navn              | Juridisk enhet  |
|-----------------|------------------|-------------------|---------------|
| 4050            | 4000             | Gastronor Delikatesser | Fabrikam      |
| 4050            | 4000             | Gastronor Delikatesser | Fabrikam Øst |
| 4050            | 10000            | Gastronor Delikatesser | Fabrikam vest |

## <a name="example-1-customer-payment-of-invoice-from-another-legal-entity"></a>Eksempel 1: Kundebetaling av faktura fra en annen juridisk enhet
Fabrikam mottar en betaling på 600,00 til Fabrikams kundekonto 4000, Gastronor Delikatesser. Betalingen utlignes med en åpen faktura for kundekonto 4000 hos Fabrikam Øst.

### <a name="invoice-is-posted-in-fabrikam-east-for-customer-4000"></a>Fakturaen posteres i Fabrikam Øst for kunde 4000

| Konto                             | Debetbeløp | Kreditbeløp |
|-------------------------------------|--------------|---------------|
| Kunder (Fabrikam Øst) | 600,00       |               |
| Salg (Fabrikam Øst)               |              | 600,00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Betalingen mottas og posteres i Fabrikam for kunde 4000

| Konto                        | Debetbeløp | Kreditbeløp |
|--------------------------------|--------------|---------------|
| Kontant (Fabrikam)                | 600,00       |               |
| Kunder (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam-betalingen utlignes med Fabrikam Øst-fakturaen

**Fabrikam-postering**

| Konto                         | Debetbeløp | Kreditbeløp |
|---------------------------------|--------------|---------------|
| Kunder (Fabrikam)  | 600,00       |               |
| Skal betales til Fabrikam Øst (Fabrikam) |              | 600,00        |

**Fabrikam Øst-postering**

| Konto                             | Debetbeløp | Kreditbeløp |
|-------------------------------------|--------------|---------------|
| Skal betales fra Fabrikam (Fabrikam Øst)   | 600,00       |               |
| Kunder (Fabrikam Øst) |              | 600,00        |

## <a name="example-2-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>Eksempel 2: Kundebetaling av faktura fra en annen juridisk enhet med kontantrabatt
Fabrikam mottar en betaling på 580,00 til Fabrikams kundekonto 4000, Gastronor Delikatesser. Fabrikam Øst har en åpen faktura for kunde 4000. Fakturaen har en mulighet for en kontantrabatt på 20,00. Betalingen utlignes med de åpne Fabrikam Øst-fakturaene. Kontantrabatten posteres til den juridiske enheten for fakturaen, Fabrikam Øst.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Fakturaen posteres i Fabrikam Øst for Fabrikam Øst-kunde 4000

| Konto                             | Debetbeløp | Kreditbeløp |
|-------------------------------------|--------------|---------------|
| Kunder (Fabrikam Øst) | 600,00       |               |
| Salg (Fabrikam Øst)               |              | 600,00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Betalingen mottas og posteres i Fabrikam for Fabrikam-kunde 4000

| Konto                        | Debetbeløp | Kreditbeløp |
|--------------------------------|--------------|---------------|
| Kontant (Fabrikam)                | 600,00       |               |
| Kunder (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam-betalingen utlignes med Fabrikam Øst-fakturaen

**Fabrikam-postering**

| Konto                         | Debetbeløp | Kreditbeløp |
|---------------------------------|--------------|---------------|
| Kunder (Fabrikam)  | 580,00       |               |
| Skal betales til Fabrikam Øst (Fabrikam) |              | 580,00        |

**Fabrikam Øst-postering**

| Konto                             | Debetbeløp | Kreditbeløp |
|-------------------------------------|--------------|---------------|
| Skal betales fra Fabrikam (Fabrikam Øst)   | 580,00       |               |
| Kunder (Fabrikam Øst) |              | 580,00        |
| Kontantrabatt (Fabrikam Øst)       | 20,00        |               |
| Kunder (Fabrikam Øst) |              | 20,00         |

## <a name="example-3-customer-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-gain"></a>Eksempel 3: Kundebetaling av faktura fra en annen juridisk enhet med realisert kursgevinst
Fabrikam mottar en betaling på 600,00 euro (EUR) for Fabrikams kundekonto 4000, Gastronor Delikatesser. Betalingen utlignes med en åpen faktura for kunde 4000 hos Fabrikam Øst. En kursgevinsttransaksjon genereres under utligningsprosessen.

-   Vekslingskursen mellom EUR og USD på fakturadatoen: 1,2062
-   Vekslingskursen mellom EUR og USD på betalingsdatoen: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Fakturaen posteres i Fabrikam Øst for Fabrikam Øst-kunde 4000

| Konto                             | Debetbeløp            | Kreditbeløp           |
|-------------------------------------|-------------------------|-------------------------|
| Kunder (Fabrikam Øst) | EUR 600,00 / USD 723,72 |                         |
| Salg (Fabrikam Øst)               |                         | EUR 600,00 / USD 723,72 |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Betalingen mottas og posteres i Fabrikam for Fabrikam-kunde 4000

| Konto                        | Debetbeløp            | Kreditbeløp           |
|--------------------------------|-------------------------|-------------------------|
| Kontant (Fabrikam)                | EUR 600,00 / USD 736,62 |                         |
| Kunder (Fabrikam) |                         | EUR 600,00 / USD 736,62 |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam-betalingen utlignes med Fabrikam Øst-fakturaen

**Fabrikam-postering**

| Konto                         | Debetbeløp            | Kreditbeløp           |
|---------------------------------|-------------------------|-------------------------|
| Kunder (Fabrikam)  | EUR 600,00 / USD 736,62 |                         |
| Skal betales til Fabrikam Øst (Fabrikam) |                         | EUR 600,00 / USD 736,62 |
| Skal betales til Fabrikam Øst (Fabrikam) | EUR 0,00 / USD 12,90    |                         |
| Realisert gevinst (Fabrikam)        |                         | EUR 0,00 / USD 12,90    |

**Fabrikam Øst-postering**

| Konto                             | Debetbeløp            | Kreditbeløp           |
|-------------------------------------|-------------------------|-------------------------|
| Skal betales fra Fabrikam (Fabrikam Øst)   | EUR 600,00 / USD 736,62 |                         |
| Kunder (Fabrikam Øst) |                         | EUR 600,00 / USD 736,62 |
| Kunder (Fabrikam Øst) | EUR 0,00 / USD 12,90    |                         |
| Skal betales fra Fabrikam (Fabrikam Øst)   |                         | EUR 0,00 / USD 12,90    |

## <a name="example-4-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-gain"></a>Eksempel 4: Kundebetaling av faktura fra en annen juridisk enhet med kontantrabatt og realisert kursgevinst
Fabrikam Øst posterer en betaling fra Fabrikam-kunde 4000, Gastronor Delikatesser, for en åpen faktura i Fabrikam Øst. Fakturaen har en kontantrabatt tilgjengelig, og det genereres en mva-transaksjon. Betalingen utlignes med den åpne Fabrikam Øst-fakturaen. En kursgevinsttransaksjon genereres under utligningsprosessen. Kontantrabatten posteres til den juridiske enheten for faktura (Fabrikam Øst), og kursgevinsten posteres til den juridiske enheten for betaling (Fabrikam).

-   Vekslingskursen mellom EUR og USD på fakturadatoen: 1,2062
-   Vekslingskursen mellom EUR og USD på betalingsdatoen: 1,2277

### <a name="free-text-invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-customer-4000"></a>En fritekstfaktura posteres og en avgiftstransaksjon genereres i Fabrikam Øst for kunde 4000

| Konto                             | Debetbeløp            | Kreditbeløp           |
|-------------------------------------|-------------------------|-------------------------|
| Kunder (Fabrikam Øst) | EUR 638,22 / USD 769,82 |                         |
| Salg (Fabrikam Øst)               |                         | EUR 600,00 / USD 723,72 |
| Merverdiavgift (Fabrikam Øst)           |                         | EUR 38,22 / USD 46,10   |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Betalingen mottas og posteres i Fabrikam for kunde 4000

| Konto                        | Debetbeløp            | Kreditbeløp           |
|--------------------------------|-------------------------|-------------------------|
| Kontant (Fabrikam)                | EUR 626,22 / USD 768,81 |                         |
| Kunder (Fabrikam) |                         | EUR 626,22 / USD 768,81 |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam-betalingen utlignes med Fabrikam Øst-fakturaen

**Fabrikam-postering**

| Konto                         | Debetbeløp            | Kreditbeløp           |
|---------------------------------|-------------------------|-------------------------|
| Kunder (Fabrikam)  | EUR 626,22 / USD 768,81 |                         |
| Skal betales til Fabrikam Øst (Fabrikam) |                         | EUR 626,22 / USD 768,81 |
| Skal betales til Fabrikam Øst (Fabrikam) | EUR 0,00 / USD 13,46    |                         |
| Realisert gevinst (Fabrikam)        |                         | EUR 0,00 / USD 13,46    |

**Fabrikam Øst-postering**

| Konto                             | Debetbeløp            | Kreditbeløp           |
|-------------------------------------|-------------------------|-------------------------|
| Skal betales fra Fabrikam (Fabrikam Øst)   | EUR 626,22 / USD 768,81 |                         |
| Kunder (Fabrikam Øst) |                         | EUR 626,22 / USD 768,81 |
| Kunder (Fabrikam Øst)  | EUR 0,00 / USD 13,46    |                         |
| Skal betales fra Fabrikam (Fabrikam Øst)   |                         | EUR 0,00 / USD 13,46    |
| Kontantrabatt (Fabrikam Øst)       | EUR 12,00 / USD 14,47   |                         |
| Kunder (Fabrikam Øst) |                         | EUR 12,00 / USD 14,47   |

## <a name="example-5-customer-credit-note-with-primary-payment"></a>Eksempel 5: Kundekreditnota med hovedbetaling
Fabrikam mottar en betaling på 75,00 fra kunde 4000, Gastronor Delikatesser. Betalingen utlignes med en åpen faktura for Fabrikam Vest-kunde 10000 og en åpen kreditnota for Fabrikam Øst-kunde 4000. Betalingen velges som hovedbetaling på siden **Utlign transaksjoner**.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Fakturaen posteres til Fabrikam Vest for kunde 10000

| Konto                             | Debetbeløp | Kreditbeløp |
|-------------------------------------|--------------|---------------|
| Kunder (Fabrikam Vest) | 100,00       |               |
| Salg (Fabrikam Vest)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Kreditnotaen posteres til Fabrikam Øst for kunde 4000

| Konto                             | Debetbeløp | Kreditbeløp |
|-------------------------------------|--------------|---------------|
| Salgsretur (Fabrikam Øst)       | 25,00        |               |
| Kunder (Fabrikam Øst) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Betalingen posteres til Fabrikam for kunde 4000

| Konto                        | Debetbeløp | Kreditbeløp |
|--------------------------------|--------------|---------------|
| Kontant (Fabrikam)                | 75,00        |               |
| Kunder (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam-betalingen utlignes med Fabrikam Vest-fakturaen og Fabrikam Øst-kreditnotaen

**Fabrikam-postering**

| Konto                           | Debetbeløp | Kreditbeløp |
|-----------------------------------|--------------|---------------|
| Skal betales fra Fabrikam Øst (Fabrikam) | 25,00        |               |
| Kunder (Fabrikam)    |              | 25,00         |
| Kunder (Fabrikam)    | 100,00       |               |
| Skal betales til Fabrikam Vest (Fabrikam)   |              | 100,00        |

**Fabrikam Øst-postering**

| Konto                             | Debetbeløp | Kreditbeløp |
|-------------------------------------|--------------|---------------|
| Kunder (Fabrikam Øst) | 25,00        |               |
| Skal betales til Fabrikam (Fabrikam Øst)     |              | 25,00         |

**Fabrikam Vest-postering**

| Konto                             | Debetbeløp | Kreditbeløp |
|-------------------------------------|--------------|---------------|
| Skal betales fra Fabrikam (Fabrikam Vest)   | 100,00       |               |
| Kunder (Fabrikam Vest) |              | 100,00        |

## <a name="example-6-customer-credit-note-without-primary-payment"></a>Eksempel 6: Kundekreditnota uten hovedbetaling
Fabrikam mottar en betaling på 75,00 fra kunde 4000, Gastronor Delikatesser. Betalingen utlignes med en åpen faktura for Fabrikam Vest-kunde 10000 og en åpen kreditnota for Fabrikam Øst-kunde 4000. Betalingen velges ikke som hovedbetaling på siden **Utlign transaksjoner**.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Fakturaen posteres til Fabrikam Vest for kunde 10000

| Konto                             | Debetbeløp | Kreditbeløp |
|-------------------------------------|--------------|---------------|
| Kunder (Fabrikam Vest) | 100,00       |               |
| Salg (Fabrikam Vest)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Kreditnotaen posteres til Fabrikam Øst for kunde 4000

| Konto                             | Debetbeløp | Kreditbeløp |
|-------------------------------------|--------------|---------------|
| Salgsretur (Fabrikam Øst)       | 25,00        |               |
| Kunder (Fabrikam Øst) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Betalingen posteres til Fabrikam for kunde 4000

| Konto                        | Debetbeløp | Kreditbeløp |
|--------------------------------|--------------|---------------|
| Kontant (Fabrikam)                | 75,00        |               |
| Kunder (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam-betalingen utlignes med Fabrikam Vest-fakturaen og Fabrikam Øst-kreditnotaen

**Fabrikam-postering**

| Konto                         | Debetbeløp | Kreditbeløp |
|---------------------------------|--------------|---------------|
| Kunder (Fabrikam)  | 75,00        |               |
| Skal betales til Fabrikam Vest (Fabrikam) |              | 75,00         |

**Fabrikam Øst-postering**

| Konto                              | Debetbeløp | Kreditbeløp |
|--------------------------------------|--------------|---------------|
| Kunder (Fabrikam Øst)  | 25,00        |               |
| Skal betales til Fabrikam Vest (Fabrikam Øst) |              | 25,00         |

**Fabrikam Vest-postering**

| Konto                                | Debetbeløp | Kreditbeløp |
|----------------------------------------|--------------|---------------|
| Skal betales fra Fabrikam (Fabrikam Vest)      | 75,00        |               |
| Kunder (Fabrikam Vest)    |              | 75,00         |
| Skal betales fra Fabrikam Øst (Fabrikam Vest) | 25,00        |               |
| Kunder (Fabrikam Vest)    |              | 25,00         |






