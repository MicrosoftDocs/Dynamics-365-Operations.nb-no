--- 
title: Definere kunders bankkontoer for ISO20022-avtalegiroer
description: "Dette hjelper deg med å definere en kundebankkonto og et avtalegiromandat for kunde som kreves for å generere kundebetalingsfilen som ISO20022-avtalegiro."
author: mrolecki
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5b4652b76e089d6beb2ce1513d06cf07a5ea3195
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a>Definere kunders bankkontoer for ISO20022-avtalegiroer

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


