---
title: Opprette og eksportere leverandørbetalinger ved hjelp av ISO20022-betalingsformat
description: Denne prosedyren viser hvordan du oppretter betalingslinjer i leverandørbetalingsjournalen og genererer en leverandørbetalingsfil ved hjelp av eksemplet med ISO2022-kredittoverføring.
author: mrolecki
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18c7d0b6c5c6a7f598f4b94f4dcf02df498d74cf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822711"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Opprette og eksportere leverandørbetalinger ved hjelp av ISO20022-betalingsformat

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du oppretter betalingslinjer i leverandørbetalingsjournalen og genererer en leverandørbetalingsfil ved hjelp av eksemplet med ISO2022-kredittoverføring.

Dette er den femte prosedyren av fem, som illustrerer leverandørbetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering. Bruk DEMF-demodata til å utføre dette eksemplet.

## <a name="example"></a>Eksempel

1.    Gå til **Leverandører > Betalinger > Betalingsjournal**.
2.    Klikk **Ny**.
3.    Angi eller velg en verdi i **Navn**-feltet.
4.    Klikk **Linjer > Betalingsforslag > Opprett betalingsforslag**.
5.    Utvid delen **Poster som skal inkluderes**.
6.    Klikk **Filter**.
7.    I listen velger du raden for **Leverandører-tabellen** og **Leverandørkonto-feltet**.
8.    Angi eller velg en verdi i **Kriterier**-feltet. Du kan bruke hvilke som helst kriterier for å velge leverandørtransaksjoner som skal betales, men i dette eksemplet bruker du DE-001 som en leverandørkonto.
12.    Klikk **OK**.
13.    Klikk **OK**.
14.    Klikk **Opprett betalinger**.
15. Generere en ISO20022-betalingsfil.
    1.    Klikk **Generer betalinger**.
    2.    Angi eller velg en verdi i **Betalingsmåte**-feltet.
    3.    Skriv inn en verdi i feltet **Filnavn**. I dette eksemplet blir den genererte filen SEPA-kompatibel på grunn av EUR-betalingen. ISO20022 kredittoverføring i tillegg til andre leverandørbetalingsformater kan også brukes for å generere betalinger i andre valutaer.
    4.    Angi eller velg en verdi i **Bankkonto**-feltet.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]