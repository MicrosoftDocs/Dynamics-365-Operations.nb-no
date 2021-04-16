---
title: Opprette et nytt avtalegiromandat for en kunde
description: Denne oppgaveveiledningen beskriver hvordan du oppretter et avtalegiromandat og bruker det på en faktura.
author: ShivamPandey-msft
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3bbf3703941255dfd82b8fb501ba8a9d1f3a2ec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835082"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Opprette et nytt avtalegiromandat for en kunde

[!include [banner](../../includes/banner.md)]

Denne oppgaveveiledningen beskriver hvordan du oppretter et avtalegiromandat og bruker det på en faktura.


## <a name="create-a-bank-account"></a>Opprette en bankkonto
1. I **navigasjonsruten** går du **Moduler > Kunder > Kunder > Alle kunder**.
2. Velg en post i listen. Velg for eksempel US-001.
3. Klikk **Kunde** i handlingsruten.
4. Klikk **Bankkontoer**.
5. Klikk på **Ny**.
6. Skriv inn en verdi i **Bankkonto**-feltet.
7. Skriv inn en verdi i **Navn**-feltet.
8. Skriv inn en verdi i **IBAN**-feltet.
9. Skriv inn en verdi i **Valuta**-feltet.
10. Klikk **Lagre**.
11. Lukk siden.
12. I **navigasjonsruten** går du til **Moduler > Kontant- og bankbehandling > Bankkontoer > Bankkontoer**.
13. Finn og velg ønsket post i listen.
14. Klikk koblingen i den valgte raden i listen.
15. Klikk **Rediger**.
16. Vis hurtigfanen **Tilleggsidentifikasjon**.
17. Skriv inn en verdi i feltet **Direkte debet-ID**.
18. Skriv inn en verdi i **IBAN**-feltet.
19. Lukk siden.
20. Lukk siden.

## <a name="define-the-electronic-payment-method"></a>Definere den elektroniske betalingsmåten
1. I **navigasjonsruten** går du til **Moduler > Kunder > Betalingsoppsett > Betalingsmåter**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i **Betalingsmåte**-feltet.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Velg Elektronisk betaling i **Betalingstype**-feltet. Betalingstypen for betalingsmåten avtalegiromandat må være elektronisk betaling.
6. I feltet **Krever mandat** velger du Ja.
7. Lukk siden.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Legg til et avtalegiromandat for en kunde.
1. I **navigasjonsruten** går du **Moduler > Kunder > Kunder > Alle kunder**.
2. Velg en post i listen. Velg for eksempel US-001.
3. Klikk **Rediger**.
4. Utvid hurtigfanen **Betalingstandarder**.
5. Angi eller velg en verdi i **Betalingsmåte**-feltet.
6. Utvid hurtigfanen **Betalingstandarder**.
7. Utvid hurtigfanen **Avtalegiromandater**.
8. Klikk **Legg til**.
9. Angi eller velg en verdi i **Bankkonto**-feltet.
10. Angi eller velg en verdi i **Kreditors bankkonto**-feltet.
11. Angi antall betalinger som du forventer å behandle for dette mandatet, i feltet **Betalingsfrekvens**.
12. Klikk **OK**.
13. Klikk **Skriv ut**.
14. Klikk **Mandatrapport**.
15. Lukk siden.
16. Klikk **Rediger**.
17. Angi en dato i **Signaturdato**-feltet.
18. Klikk **Ja**.
19. Angi stedet mandatet ble signert.
20. Klikk **OK**.
21. Lukk siden.

## <a name="create-a-free-text-invoice-with-mandate"></a>Opprette en fritekstfaktura med mandat
1. I **navigasjonsruten** går du til **Moduler > Kunder > Fakturaer > Alle fritekstfakturaer**.
2. Klikk på **Ny**.
3. Velg kunden du har lagt til mandatet til.
4. Angi eller velg en verdi i feltet **ID for avtalegiromandat**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]