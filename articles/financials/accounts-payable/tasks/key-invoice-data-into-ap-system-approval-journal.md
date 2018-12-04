--- 
title: Hovedfakturadata inn i AP-systemet ved hjelp av godkjenningsjournal
description: "Denne oppgaveveiledningen viser hvordan du bruker ankomstregistreringen til opprette fakturaer, og deretter bruke godkjenningsjournalen for å oppdatere utgiftskontoene."
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 048eda77064b6aa3f666e998a8e551d2f7adc385
ms.contentlocale: nb-no
ms.lasthandoff: 10/16/2018

---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a>Hovedfakturadata inn i AP-systemet ved hjelp av godkjenningsjournal

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


