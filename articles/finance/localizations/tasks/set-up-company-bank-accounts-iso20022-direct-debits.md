---
title: Definere firmaets bankkontoer for ISO20022-avtalegiroer
description: Denne oppgaven hjelper deg med å definere den firmaspesifikke bankkontoinformasjonen som kreves for å generere kundebetalingsfiler.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0faa23193111ed771ccc3a5c7f99ca908a036e9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988142"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a>Definere firmaets bankkontoer for ISO20022-avtalegiroer

[!include [banner](../../includes/banner.md)]

Denne oppgaven hjelper deg med å definere den firmaspesifikke bankkontoinformasjonen som kreves for å generere kundebetalingsfiler. Denne fremgangsmåten bruker ISO 20022-avtalegiroformatet som eksempel. Andre formater kan kreve mer oppsettsinformasjon som firma-ID eller sorteringskode.



Denne oppgaven ble opprettet med demonstrasjonsdatafirmaet DEMF.



Dette er den andre av fem prosedyrer, som viser kundebetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering.


## <a name="set-up-the-iban-and-swift-codes"></a>Definere IBAN- og SWIFT-kodene
1. Gå til Kontant- og bankbehandling > Bankkontoer.
2. Bruk hurtigfilteret til å filtrere på Bankkonto-feltet med en verdi lik DEMF OPER.
3. Klikk koblingen i den valgte raden i listen.
    * For eksempel, klikk DEMF OPER for å åpne bankkontodetaljene.  
4. Klikk Rediger.
5. Vis eller skjul delen Tilleggsidentifikasjon.
6. Skriv inn en verdi i IBAN-feltet.
    * Skriv for eksempel DE89370400440532013000.  
7. Skriv inn en verdi i SWIFT-kode-feltet.
    * Skriv for eksempel DEUTDEFF.    Vær oppmerksom på at SWIFT\BIC ikke er obligatorisk for mange betalingsformater, men det anbefales at det er registrert for en bankkonto.  
8. Klikk Lagre.

## <a name="set-up-a-bank-account-for-the-legal-entity"></a>Definere en bankkonto for juridisk enhet
1. Gå til Organisasjonsstyring > Organisasjoner > Juridiske enheter.
2. Klikk Rediger.
3. Vis eller skjul delen Bankkontoinformasjon.
4. Klikk rullegardinknappen i Bankkonto-feltet for å åpne oppslaget.
5. Klikk koblingen i den valgte raden i listen.
    * For eksempel, velg "DEMF OPER" bankkonto.  
6. Klikk Lagre.

