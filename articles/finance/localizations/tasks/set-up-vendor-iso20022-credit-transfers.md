---
title: Definere leverandørers bankkontoer for ISO20022-kreditoverføringer
description: Denne fremgangsmåten beskriver hvordan du definerer leverandøren og den leverandørspesifikke bankkontoinformasjonen som kreves for ISO20022-kredittoverføring eller en annen filgenerering for leverandørbetalinger.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47735d41fde4c5f71ec1c3209446a593e1f4180c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813425"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Definere leverandørers bankkontoer for ISO20022-kreditoverføringer

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten beskriver hvordan du definerer leverandøren og den leverandørspesifikke bankkontoinformasjonen som kreves for ISO20022-kredittoverføring eller en annen filgenerering for leverandørbetalinger. 

Demonstrasjonsdatafirmaet DEMF brukes til å opprette denne prosedyren.
Dette er den fjerde prosedyren av fem, som illustrerer leverandørbetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering. Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.


## <a name="set-up-bank-details"></a>Definere bankdetaljer
1. Gå til Leverandører > Leverandører > Alle leverandører.
2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Leverandørkonto-feltet med verdien DE-001.
3. Klikk DE-001 for å åpne leverandørdetaljer.
4. Klikk Leverandør i handlingsruten.
5. Klikk Bankkontoer.
6. Klikk Rediger.
    * Hvis ingen bankkonto er tilgjengelig, må du opprette en ny.  
7. Skriv inn COBADEFFXXX i SWIFT-kode-feltet.
8. Skriv inn 36200400000628808808 i IBAN-feltet.
9. Lukk siden.

## <a name="set-up-a-method-of-payment-for-the-vendor"></a>Definere en betalingsmåte for leverandøren
1. Klikk Rediger.
2. Vis eller skjul delen Betaling.
3. Klikk rullegardinknappen i Betalingsmåte-feltet for å åpne oppslaget.
4. Klikk koblingen i SEPA CT-raden i listen.
5. Klikk Lagre.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]