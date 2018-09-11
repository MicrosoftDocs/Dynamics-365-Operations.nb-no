--- 
title: Opprette et nytt avtalegiromandat for en kunde
description: "Denne oppgaveveiledningen beskriver hvordan du oppretter et avtalegiromandat og bruker det på en faktura."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d01c7c19925a3c7064ab3f845b92b610b162066c
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Opprette et nytt avtalegiromandat for en kunde

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaveveiledningen beskriver hvordan du oppretter et avtalegiromandat og bruker det på en faktura.


## <a name="create-a-bank-account"></a>Opprette en bankkonto
1. Gå til Kunder > Kunder > Alle kunder.
2. Velg for eksempel US-001.
3. Klikk Kunde i handlingsruten.
4. Klikk Bankkontoer.
5. Klikk Ny.
6. Skriv inn en verdi i Bankkonto-feltet.
7. Skriv inn en verdi i Navn-feltet.
8. Skriv inn en verdi i IBAN-feltet.
9. Skriv inn en verdi i Valuta-feltet.
10. Klikk Lagre.
11. Lukk siden.
12. Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.
13. Finn og velg ønsket post i listen.
14. Klikk koblingen i den valgte raden i listen.
15. Klikk Rediger.
16. Vis delen Tilleggsidentifikasjon.
17. Skriv inn en verdi i feltet Direkte debet-ID.
18. Skriv inn en verdi i IBAN-feltet.
19. Lukk siden.
20. Lukk siden.

## <a name="define-the-electronic-payment-method"></a>Definere den elektroniske betalingsmåten
1. Gå til Kunder > Betalingsoppsett > Betalingsmåter.
2. Klikk Ny.
3. Skriv inn en verdi i Betalingsmåte-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Betalingstypen for betalingsmåten avtalegiromandat må være elektronisk betaling.
6. I feltet Krever mandat velger du Ja.
7. Lukk siden.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Legg til et avtalegiromandat for en kunde.
1. Gå til Kunder > Kunder > Alle kunder.
2. Velg for eksempel US-001.
3. Klikk Rediger.
4. Utvid delen Betalingstandarder.
5. Angi eller velg en verdi i Betalingsmåte-feltet.
6. Utvid delen Betalingstandarder.
7. Utvid delen Avtalegiromandater.
8. Klikk Legg til.
9. Angi eller velg en verdi i Bankkonto-feltet.
10. Angi eller velg en verdi i Kreditors bankkonto-feltet.
11. Angi antall betalinger som du forventer å behandle for dette mandatet.
12. Klikk OK.
13. Klikk Skriv ut.
14. Klikk Mandatrapport.
15. Lukk siden.
16. Klikk Rediger.
17. Angi en dato i Signaturdato-feltet.
18. Klikk Ja.
19. Angi stedet mandatet ble signert.
20. Klikk OK.
21. Lukk siden.

## <a name="create-a-free-text-invoice-with-mandate"></a>Opprette en fritekstfaktura med mandat
1. Gå til Kunder > Fakturaer > Alle fritekstfakturaer.
2. Klikk Ny.
3. Velg kunden du har lagt til mandatet til.
4. Angi eller velg en verdi i feltet ID for avtalegiromandat.


