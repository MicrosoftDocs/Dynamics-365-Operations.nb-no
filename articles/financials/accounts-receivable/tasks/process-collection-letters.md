--- 
title: Behandle purrebrev
description: Denne prosedyren viser hvordan du oppretter, skriver ut og posterer purringer.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="process-collection-letters"></a>Behandle purrebrev

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren viser hvordan du oppretter, skriver ut og posterer purringer. Denne oppgaven bruker demonstrasjonsfirmaet USMF.


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Angi et purreforløp på posteringsprofilen
1. Gå til Kreditt og innkreving > Oppsett > Kundeposteringsprofiler.
2. Klikk Rediger.
    * Velg et purreforløp fra rullegardinlisten. Hvis du ikke vil generere purringer for transaksjoner ved hjelp av denne posteringsprofilen, lar du feltet stå tomt.  
    * I fanen Tabellrestriksjoner kan du endre måten purringer behandles på. Hvis dette feltet er satt til Ja, opprettes purringer for denne posteringsprofilen.  
3. Lukk siden.

## <a name="create-collection-letters"></a>Opprett purringer
1. Gå til Kreditt og innkreving > Purring > Opprett purringer.
    * Du må velge transaksjonstypene for purringene. Alle åpne transaksjoner for disse typene inkluderes i beregningen.  
2. Velg et alternativ for Purring-feltet.
3. Angi datoen på purringen.
    * Det er to alternativer for posteringsprofil: Konto – bruk posteringsprofilen som er tilordnet kundekontoen for hver rentenota.   Velg – Bruk posteringsprofilen som du velger i Posteringsprofil-feltet.  
    * Velg en posteringsprofil hvis du har endret Bruk posteringsprofil fra til Velg.  
4. Utvid delen Poster som skal inkluderes.
5. Klikk Filter.
6. Angi en kunde-ID i Kriterier-feltet. Skriv for eksempel inn USA-001.
7. Klikk OK.
8. Klikk OK.

## <a name="print-collection-letters"></a>Skrive ut purringer
1. Gå til Kreditt og innkreving > Purring > Gjennomgå og behandle purrebrev.
2. Velg Opprettet i Status-feltet.
3. Velg Ikke skrevet ut i feltet Utskrevet.
4. Klikk Skriv ut.
5. Klikk Purrenota.
6. Utvid delen Poster som skal inkluderes.
7. Angi fristen for posteringer
8. Klikk OK for å skrive ut den valgte purringen.

## <a name="post-the-collection-letter"></a>Postere purringen
1. Klikk Poster.
2. Angi posteringsdatoen for purringen.
3. Utvid delen Poster som skal inkluderes.
4. Klikk OK.
5. Velg Postert i Status-feltet.
6. Velg et alternativ i feltet Utskrevet.


