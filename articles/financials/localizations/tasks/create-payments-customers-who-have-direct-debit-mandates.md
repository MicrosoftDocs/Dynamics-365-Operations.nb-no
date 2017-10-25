--- 
title: Opprette betalinger for en kunde som har avtalegiromandater
description: Denne prosedyren viser hvordan du genererer en betalingsfil for avtalegiro for ISO20022 for en kunde som har konfigurert AvtaleGiro og en faktura som skal betales.
author: mrolecki
manager: AnnBe
ms.date: 10/14/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: acd6a8076288d8d1d1aa05af33e306c6a29780f7
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a>Opprette betalinger for en kunde som har avtalegiromandater

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren viser hvordan du genererer en betalingsfil for avtalegiro for ISO20022 for en kunde som har konfigurert AvtaleGiro og en faktura som skal betales. Oppretting og bokføring av en faktura er valgfritt. I stedet for at en faktura må betales, kan du velge et mandat i en journal før en betalingsfil genereres, for å støtte et scenario med kundeforskuddsbetaling.



Demonstrasjonsdatafirmaet DEMF brukes til å opprette denne prosedyren.



Dette er den femte av fem prosedyrer, som viser kundebetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering. Før du kan gjøre denne oppgaven, må du fullføre de tidligere oppgavene. Du må først importere elektroniske rapporteringskonfigurasjoner for kundebetaling, konfigurere metoder for betalinger, og du må definere informasjonen om firmaet og kunden. 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a>Postere en fritekstfaktura AvtaleGiro-informasjon
1. Gå til Kunder > Fakturaer > Alle fritekstfakturaer.
2. Klikk Ny.
3. Angi eller velg en verdi i Kundekonto-feltet.
    * Velg for eksempel DE-010.  
4. Angi eller velg en verdi i Betalingsmåte-feltet.
    * For eksempel. Velg elektronisk.  
5. Angi eller velg en verdi i feltet ID for avtalegiromandat.
6. Klikk Legg til linje.
7. Skriv inn en verdi i Beskrivelse-feltet.
8. Angi de ønskede verdiene i Hovedkonto-feltet.
9. Angi et tall i feltet Enhetspris.
10. Klikk Poster.
11. Klikk OK.

## <a name="create-a-payment"></a>Opprette en betaling
1. Gå til Kunder > Betalinger > Betalingsjournal.
2. Klikk Ny.
3. Angi eller velg en verdi i Navn-feltet.
4. Klikk Linjer.
5. Klikk Betalingsforslag.
6. Klikk Opprett betalingsforslag.
7. Utvid delen Poster som skal inkluderes.
8. Klikk Filter.
9. I listen velger du raden for Kundetransaksjoner-tabellen og Betalingsmåte-feltet.
    * Du kan bruke hvilke som helst kriterier for valg av kundetransaksjoner for å betale. I dette eksemplet kan du bruke elektronisk som betalingsmetode for å filtrere transaksjoner.  
10. Angi eller velg en verdi i Kriterier-feltet.
11. Klikk OK.
12. Klikk OK.
13. Klikk Opprett betalinger.

## <a name="generate-a-payment-file"></a>Generere en betalingsfil

