--- 
title: "Definere leverandørers bankkontoer for ISO20022-kreditoverføringer"
description: "Denne fremgangsmåten beskriver hvordan du definerer leverandøren og den leverandørspesifikke bankkontoinformasjonen som kreves for ISO20022-kredittoverføring eller en annen filgenerering for leverandørbetalinger."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f01947840553a65af4aba1309d89f9b3e9ced872
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Definere leverandørers bankkontoer for ISO20022-kreditoverføringer

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten beskriver hvordan du definerer leverandøren og den leverandørspesifikke bankkontoinformasjonen som kreves for ISO20022-kredittoverføring eller en annen filgenerering for leverandørbetalinger. 

Demonstrasjonsdatafirmaet DEMF brukes til å opprette denne prosedyren.
Dette er den fjerde prosedyren av fem, som illustrerer leverandørbetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering. Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.


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


