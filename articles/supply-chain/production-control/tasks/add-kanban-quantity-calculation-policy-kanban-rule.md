--- 
title: Legge til en policy for beregning av Kanban-antall i en Kanban-regel
description: "Denne prosedyren fokuserer på å opprette en policy for Kanban-antallsberegning og legge den til i en kanban-regel for å optimalisere kanban-størrelse og -antall."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f9e0ccf25a346d54e48f51b0866f0c11e98bf0a0
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Legge til en policy for beregning av Kanban-antall i en Kanban-regel

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren fokuserer på å opprette en policy for Kanban-antallsberegning og legge den til i en kanban-regel for å optimalisere kanban-størrelse og -antall. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne fremgangsmåten er ment for verdistrømsbehandling. Denne prosedyren er en forutsetning for oppretting av prosedyren Beregne forslag til Kanban-antall. 


## <a name="create-a-kanban-quantity-calculation-policy"></a>Opprett en policy for Kanban-antallsberegning
1. Gå til Produksjonskontroll > Periodiske oppgaver > Kanban-antallsberegning > Policyer for Kanban-antallsberegning.
2. Klikk Ny.
3. Skriv inn en verdi i Navn-feltet.
    * Skriv for eksempel inn Høyttaler2016.  
4. Klikk rullegardinknappen i feltet Hovedplan for å åpne oppslaget.
5. Finn og velg ønsket post i listen.
    * Velg Statisk plan for å beregne behov.  
6. Klikk koblingen i den valgte raden i listen.
7. Klikk Lagre.
8. Angi 1 i feltet Minste Kanban-antall.
    * Dette er det ekstra antallet Kanbaner som er tatt med i Kanban-antallsberegningen.  
9. Angi Sikkerhetsfaktor til 1.
    * Dette er faktoren som brukes til å beregne tilleggsantall for sikkerhetslager.  
10. Angi 30 i Dager foran-feltet.
    * Dette er antall dager bakover fra beregningsdatoen for Kanban-antall som behov er inkludert i behovsberegningen.  
11. Angi 30 i Dager etter-feltet.
    * Dette er antall dager fremover fra beregningsdatoen for Kanban-antall som behov er inkludert i behovsberegningen.  Formelen som brukes i beregningen, vises med de faktiske verdiene. Eksempel: Kanban-antall = ((gjennomsnittlig daglig behov x leveringstid x 2.00) / produktantall per håndteringsenhet) + 1  
12. Lukk siden.

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Legg til Kanban-beregningspolicyen i en Kanban-regel
1. Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.
2. Finn og velg ønsket post i listen.
    * Velg kanban-regel 000020 for denne fremgangsmåten.  
3. Klikk koblingen i den valgte raden i listen.
4. Aktiver utvidelsen av delen Policyer for Kanban-antallsberegning.
5. Klikk Legg til.
    * Legg til policyen for Kanban-antallsberegning som du nettopp opprettet i den forrige delaktiviteten.  
6. Merk den valgte raden i listen.
7. Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.
8. Klikk koblingen i den valgte raden i listen.
    * Velg policyen Speaker2016 som du nettopp opprettet i den forrige delaktiviteten.  

