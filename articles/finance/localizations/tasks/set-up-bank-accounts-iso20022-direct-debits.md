---
title: Definere kunders bankkontoer for ISO20022-avtalegiroer
description: Dette hjelper deg med å definere en kundebankkonto og et avtalegiromandat for kunde som kreves for å generere kundebetalingsfilen som ISO20022-avtalegiro.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 595e89faa1e24ca937d399994e15ce53e3f5308b1c6fd7f43e4e831e70c15ad8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736873"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a>Definere kunders bankkontoer for ISO20022-avtalegiroer

[!include [banner](../../includes/banner.md)]

Dette hjelper deg med å definere en kundebankkonto og et avtalegiromandat for kunde som kreves for å generere kundebetalingsfilen som ISO20022-avtalegiro. Avhengig av kundebetalingsformatene som er satt opp, kan det hende at det kreves ytterligere informasjon for en kunde eller en kundebankkonto (dette dekkes ikke i denne prosedyren). 

Denne oppgaven ble opprettet med demodatafirmaet DEMF med en primæradresse for juridisk enhet i Tyskland.



Dette er den fjerde av fem prosedyrer, som viser kundebetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering.


## <a name="set-up-a-customer-bank-account"></a>Definere en kundebankkonto
1. Gå til Kunder > Kunder > Alle kunder.
2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Konto-feltet med verdien DE-010.
3. Klikk koblingen i den valgte raden i listen.
4. Klikk Kunde i handlingsruten.
5. Klikk Bankkontoer.
6. Klikk Ny.
7. Skriv inn en verdi i Bankkonto-feltet.
8. Skriv inn en verdi i Navn-feltet.
    * Skriv for eksempel EURO-bank.  
9. Angi eller velg en verdi i Bankgrupper-feltet.
10. Skriv inn en verdi i IBAN-feltet.
    * Skriv for eksempel DE36200400000628808808.  
11. Skriv inn en verdi i SWIFT-kode-feltet.
    * Skriv for eksempel inn COBADEFFXXX.  Vær oppmerksom på at SWIFT\BIC ikke er obligatorisk for mange betalingsformater, men det anbefales at det er registrert for en bankkonto.  
12. Klikk Lagre.
13. Lukk siden.
14. Klikk Rediger.
15. Utvid delen Betalingstandarder.
16. Angi eller velg en verdi i Bankkonto-feltet.

## <a name="add-a-direct-debit-mandate"></a>Legg til et avtalegiromandat
1. Utvid delen Avtalegiromandater.
2. Klikk Legg til.
3. Angi eller velg en verdi i Kreditors bankkonto-feltet.
    * Velg for eksempel DEMF OPER.  
4. Angi en dato i Signaturdato-feltet.
5. Klikk Ja for å bekrefte datooppdateringen.
6. Angi eller velg en verdi i Signatursted-feltet.
7. Angi et tall i feltet Forventet antall betalinger.
8. Klikk OK.
9. Klikk Lagre.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]