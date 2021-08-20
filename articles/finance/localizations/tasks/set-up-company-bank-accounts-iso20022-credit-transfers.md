---
title: Definere firmaets bankkontoer for ISO20022-kreditoverføringer
description: Denne prosedyren beskriver hvordan du definerer firmaspesifikk bankkontoinformasjon som kreves for generering av betalingsfilen.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a3b3b5ce9d7e24b2b7d3f76e4d770968df897b546df507ba9e3bde5aeac91715
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780776"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>Definere firmaets bankkontoer for ISO20022-kreditoverføringer

[!include [banner](../../includes/banner.md)]

Denne prosedyren beskriver hvordan du definerer firmaspesifikk bankkontoinformasjon som kreves for generering av betalingsfilen. Du kan angi informasjon som kreves for å generere ISO 20022-kredittoverføringsformat, men avhengig av formatet kan det være annen informasjon som kreves, for eksempel firma-ID eller sorteringskode. 

Demonstrasjonsdatafirmaet DEMF brukes til å opprette denne prosedyren.

Dette er den andre prosedyren av fem, som illustrerer leverandørbetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering. Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.


## <a name="set-up-iban-and-swift-code"></a>Konfigurere IBAN- og SWIFT-kode
1. Gå til Kontant- og bankbehandling > Bankkontoer.
2. Bruk hurtigfilteret til å filtrere på Bankkonto-feltet med en verdi lik DEMF OPER.
3. Klikk DEMF OPER for å åpne bankkontodetaljer.
4. Klikk Rediger.
5. Vis delen Tilleggsidentifikasjon.
6. Skriv inn 89370400440532013000 i IBAN-feltet.
7. Skriv inn DEUTDEFF i SWIFT-kode-feltet.
    * Vær oppmerksom på at SWIFT\BIC ikke er nødvendig for mange betalingsformater, men det anbefales at det er registrert for en bankkonto.  
8. Klikk Lagre.

## <a name="set-up-bank-account-for-the-legal-entity"></a>Konfigurere bankkonto for juridisk enhet
1. Gå til Organisasjonsstyring > Organisasjoner > Juridiske enheter.
2. Klikk Rediger.
3. Utvid delen Bankkontoinformasjon.
4. Angi eller velg en verdi i Bankkonto-feltet.
5. Klikk Lagre.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]