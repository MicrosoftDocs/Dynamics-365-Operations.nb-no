--- 
title: Behandle rente
description: Denne prosedyren viser hvordan du oppretter, skriver ut og posterer rentenotaer.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
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
ms.openlocfilehash: 543ac29ac1b1cbad52f1c155ac90b04d0c122a1f
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="process-interest"></a>Behandle rente

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren viser hvordan du oppretter, skriver ut og posterer rentenotaer. Denne oppgaven bruker demonstrasjonsfirmaet USMF.


## <a name="set-up-interest-on-the-posting-profile"></a>Konfigurere rente i posteringsprofilen
1. Gå til Kreditt og innkreving > Oppsett > Kundeposteringsprofiler.
2. Klikk Rediger.
    * Velg en rentekode fra rullegardinlisten. Hvis du ikke vil beregne rente for transaksjoner ved hjelp av denne posteringsprofilen, lar du feltet stå tomt.  
    * I fanen Tabellrestriksjoner kan du endre måten renter behandles på. Hvis dette feltet er satt til Ja, beregnes rente for denne posteringsprofilen.  

## <a name="calculate-interest"></a>Beregn rente
1. Gå til Kreditt og innkreving > Rente > Opprett rentenotaer.
    * Du må velge transaksjonstypene du vil beregne rente for. Alle åpne transaksjoner for disse typene inkluderes i beregningen.  
    * Hvis du velger Rente, vil du beregne rente på rente. Du bør kontrollere lovene som gjelder for beregning av rente på rente før du inkluderer disse transaksjonene.  
    * Rente beregnes fra denne datoen til "Til dato". Hvis du ikke angir en "Fra dato", blir alle uposterte rentenotaer avbrutt og rente beregnes på nytt fra transaksjonsdatoen.  
2. Angi datoen for rentenotaen.
    * Det er tre alternativer for posteringsprofil: Konto – bruk posteringsprofilen som er tilordnet kundekontoen for hver rentenota.   Velg – Bruk posteringsprofilen som du velger i Posteringsprofil-feltet.   Transaksjon – Bruk den individuelle posteringsprofilen fra transaksjoner der rente er beregnet for hver rentenota. Transaksjoner som ikke har en tilordnet posteringsprofil, bruker posteringsprofilen som er angitt i Finans og merverdiavgift-området i Kundeparametere-skjemaet).  
    * Velg en posteringsprofil her hvis du har endret "Bruk posteringsprofil fra" til "Velg".  
3. Vis eller skjul delen Poster som skal inkluderes.
4. Klikk Filter.
5. Angi en kunde-ID i Kriterier-feltet. Skriv for eksempel inn USA-001.
6. Klikk OK.
7. Klikk OK.

## <a name="print-interest-notes"></a>Skriv ut rentenotaer
1. Gå til Kreditt og innkreving > Rente > Gjennomgå og behandle rentenotaer.
2. Velg Opprettet i Status-feltet.
3. Velg Ikke skrevet ut i feltet Utskrevet.
4. Klikk Skriv ut.
5. Vis eller skjul delen Poster som skal inkluderes.
6. Klikk OK.
7. Lukk siden.

## <a name="post-the-interest-note"></a>Postere rentenotaen
1. Velg en rentenota som er klar til å posteres (statusen er opprettet).
2. Klikk Poster.
3. Angir posteringsdatoen for rentenotaen.
    * Velg Ja hvis du vil opprette en økonomimodultransaksjon for hver rentenota.     Hvis du ikke velger Ja, akkumuleres renten på alle rentenotaene for kunden og posteres til økonomimodulen i én transaksjon.  
4. Vis eller skjul delen Poster som skal inkluderes.
5. Klikk OK.
6. Velg Postert i Status-feltet.


