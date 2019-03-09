---
title: Innbetale kundebetalinger
description: Betale inn kundebetalinger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f58cebce20e8516dc918e0bad1e020ffd7f791ee
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "313388"
---
# <a name="deposit-customer-payments"></a>Innbetale kundebetalinger

[!include [task guide banner](../../includes/task-guide-banner.md)]

Betale inn kundebetalinger. Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. Gå til Kunder > Betalinger > Betalingsjournal.
2. Klikk Ny.
3. Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.
4. Velg betalingsjournalen. 
5. Klikk Linjer.
6. Velg kunden du registrerer betalingen for, i Konto-feltet.
7. Angi betalingsbeløpet i Kredit-feltet.
    * Du kan velge å la beløpet stå tomt, og la programmet beregne det ved å velge fakturaene som ble betalt.  
8. Skriv inn en verdi i Betalingsreferanse-feltet.
    * Betalingsreferansen kan være sjekknummeret for betalingen du angir. Betalingsreferansen er nødvendig hvis du skal inkludere betalingen på et betalingsbilag.  
9. Merk av for Bruk et betalingsbilag.
    * Hvis betalingen skal inkluderes i innbetalingen, kan du endre denne innstillingen til Ja.  
10. Klikk Ny.
11. Velg kunden for den neste betalingen i Konto-feltet.
12. Angi betalingsbeløpet i Kredit-feltet.
13. Skriv inn en verdi i Betalingsreferanse-feltet.
14. Merk av for Bruk et betalingsbilag.
15. Klikk Poster.
    * Betalinger må være postert før betalingsbilaget kan genereres. Dette sikrer at betalingene ikke endres etter at betalingsbilaget er generert.  
16. Klikk Funksjoner.
17. Klikk betalingsbilag.
18. Klikk OK.
    * Den første siden brukes til å opprette betalingsbilaget.  
19. Klikk OK.
    * Det andre trinnet er å skrive ut betalingsbilaget, men dette trinnet er ikke nødvendig.  

