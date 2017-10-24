--- 
title: "Opprette og eksportere leverandørbetalinger ved hjelp av ISO20022-betalingsformat"
description: "Denne prosedyren viser hvordan du oppretter betalingslinjer i leverandørbetalingsjournalen og genererer en leverandørbetalingsfil ved hjelp av eksemplet med ISO2022-kredittoverføring."
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
ms.openlocfilehash: 7cc90bc86cd489b124a806c480632dd53ba47f3f
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Opprette og eksportere leverandørbetalinger ved hjelp av ISO20022-betalingsformat

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren viser hvordan du oppretter betalingslinjer i leverandørbetalingsjournalen og genererer en leverandørbetalingsfil ved hjelp av eksemplet med ISO2022-kredittoverføring. 

Demonstrasjonsdatafirmaet DEMF brukes til å opprette denne prosedyren.

Dette er den femte prosedyren av fem, som illustrerer leverandørbetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering. Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.


## <a name="create-payment-lines"></a>Opprette betalingslinjer
1. Gå til Leverandører > Betalinger > Betalingsjournal.
2. Klikk Ny.
3. Merk den valgte raden i listen.
4. Angi eller velg en verdi i Navn-feltet.
5. Klikk Linjer.
6. Klikk Betalingsforslag.
7. Klikk Opprett betalingsforslag.
8. Utvid delen Poster som skal inkluderes.
9. Klikk Filter.
10. I listen velger du raden for Leverandører-tabellen og Leverandørkonto-feltet.
11. Angi eller velg en verdi i Kriterier-feltet.
    * Du kan bruke hvilke som helst kriterier for å velge leverandørtransaksjoner som skal betales, men i dette eksemplet bruker du DE-001 som en leverandørkonto.  
12. Klikk OK.
13. Klikk OK.
14. Klikk Opprett betalinger.

## <a name="generate-an-iso20022-payment-file"></a>Generere en ISO20022-betalingsfil


