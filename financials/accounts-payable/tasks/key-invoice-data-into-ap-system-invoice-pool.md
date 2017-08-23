--- 
title: Registrere fakturadata i AP-systemet ved hjelp av fakturapulje
description: "Denne oppgaveveiledningen viser hvordan du bruker ankomstregistreringen til å opprette fakturaer."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 08f66db0f62d5d985177b1d4ec0161df0b9961b3
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Registrere fakturadata i AP-systemet ved hjelp av fakturapulje

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaveveiledningen viser hvordan du bruker ankomstregistreringen til å opprette fakturaer.  Bruk deretter fakturapuljen for å samsvare fakturaen med en bestilling og fullføre kostnaden på leverandørens fakturaside.


## <a name="create-a-purchase-order"></a>Opprette en bestilling
1. Gå til Leverandører > Bestillinger > Bestillinger.
2. Klikk Ny for å opprette en ny bestilling.
3. Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.
4. Velg leverandøren fra listen. For eksempel leverandør 1001.
5. Klikk OK.
6. Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.
7. Finn varenummeret for tjenesten i listen. Velg for eksempel S0001.
8. Klikk på varenummeret og velg det.
    * Nettbeløpet er USD 75.00.  Dette er beløpet vi forventer å se på fakturaen.  
9. Klikk Innkjøp i handlingsruten.
10. Klikk Bekreft.

## <a name="create-and-post-and-invoice"></a>Opprette og postere en faktura
1. Gå til Leverandører > Fakturaer > Ankomstregistrering.
2. Klikk Ny.
3. Åpne oppslaget for å velge navnet på ankomstregistreringen du vil bruke.
4. Velg navnet på ankomstregistreringen du vil bruke.
5. Klikk Linjer for å åpne registeret og angi utgiftslinjer.
6. Velg en leverandør i oppslaget. Klikk for eksempel på leverandør 1001.
7. I Faktura-feltet angir du fakturanummeret.
8. Skriv inn en verdi i Beskrivelse-feltet.
9. Angi et tall i Kredit-feltet.
10. Klikk rullegardinknappen i Bestilling-feltet for å åpne oppslaget.
11. Velg bestillingen du opprettet tidligere.
12. Klikk rullegardinknappen i Godkjent av-feltet for å åpne oppslaget.
13. Merk en godkjenner, og klikk Velg for å velge denne godkjenneren.
14. Klikk Poster.
15. Lukk skjemaet.
16. Lukk skjemaet.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Åpne en faktura fra utvalget og sammenlign den med en bestilling for å fullføre fakturaprosessen
1. Gå til Leverandører > Fakturaer > Fakturapulje.
2. Klikk Bestilling for å opprette en leverandørfaktura fra fakturaen i puljen.
3. Velg fakturaen du vil se gjennom.
4. Klikk Oppdater samsvarsstatus for å fullføre samsvaret.
5. Klikk Alternativer i handlingsruten.
6. Klikk Bytt visning.
7. Klikk Rutenettvisning.
8. Klikk Poster.
9. Lukk skjemaet.
10. Gå til Leverandører > Leverandører > Leverandører.
11. Velg leverandøren som var på bestillingen. Velg for eksempel leverandør 1001.
12. Klikk koblingen i den valgte raden i listen.
13. Klikk Leverandør i handlingsruten.
14. Klikk Transaksjoner.
15. Merk fakturaen som du opprettet.
    * Ankomstregistreringsavsetningen ble tilbakeført og postert til den aktuelle kontoen for utgiften.  


