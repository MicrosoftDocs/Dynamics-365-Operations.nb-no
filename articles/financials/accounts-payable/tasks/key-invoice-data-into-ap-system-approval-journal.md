--- 
title: "Registrere fakturadata i Leverandører ved hjelp av en godkjenningsjournal"
description: "Denne oppgaveveiledningen viser hvordan du bruker ankomstregistreringen til opprette fakturaer, og deretter bruke godkjenningsjournalen for å oppdatere utgiftskontoene."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 604345d357e5019e334017b2b6d0413f40818acc
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Registrere fakturadata i Leverandører ved hjelp av en godkjenningsjournal

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaveveiledningen viser hvordan du bruker ankomstregistreringen til opprette fakturaer, og deretter bruke godkjenningsjournalen for å oppdatere utgiftskontoene.


## <a name="create-and-post-and-invoice"></a>Opprette og postere en faktura
1. Gå til Leverandører > Fakturaer > Ankomstregistrering.
2. Klikk Ny.
3. Velg navnet på ankomstregistreringen du vil bruke.
4. Klikk koblingen i den valgte raden i listen.
5. Klikk Linjer for å åpne registeret og angi utgiftslinjer.
6. Velg en leverandør. Du kan for eksempel angi eller velge USA – 104
7. Skriv inn en verdi i Faktura-feltet.
8. Skriv inn en verdi i Beskrivelse-feltet.
9. Angi et tall i Kredit-feltet.
10. Klikk rullegardinknappen i Godkjent av-feltet for å åpne oppslaget.
11. Merk en godkjenner, og klikk Velg for å velge denne godkjenneren.
12. Klikk Poster.
13. Lukk siden.
14. Lukk siden.

## <a name="approve-an-invoice"></a>Godkjenne en faktura
1. Gå til Leverandører > Fakturaer > Fakturagodkjenning.
2. Klikk Ny.
3. Velg navnet på fakturagodkjenningsjournalen du vil bruke.
4. Klikk koblingen i den valgte raden i listen.
5. Klikk linjer for å vise en side der du kan velge fakturaene som du vil godkjenne.
6. Velg Finn bilag for å vise alle fakturaer som er klare til godkjenning.
7. Merk fakturaen som du opprettet.
8. Klikk Velg.
    * Bilagene som du valgte ovenfor, flyttes til denne listen når du merker dem.  
9. Klikk OK.
10. Klikk på kontonummerfeltet for å legge til en utgiftskonto i fakturaen.
11. Skriv inn et kontonummer og gå ut av feltet. Skriv for eksempel inn 600120.
12. Klikk Poster.
13. Velg Bilag for å vise oppføringene som ble postert.
    * Kontoen for fakturaen som venter på godkjenning, tilbakeføres og erstattes med den faktiske utgiftskontoen.  


