--- 
title: Opprette en Kanban-regel for salgshendelse
description: "Denne prosedyren fokuserer på oppsettet for å opprette en kanban-regel utløses under salgsordreopprettelse."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 2d446b63041e00ae12ecbed501925afc46a90ca7
ms.contentlocale: nb-no
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-sales-event-kanban-rule"></a>Opprette en Kanban-regel for salgshendelse

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren fokuserer på oppsettet for å opprette en kanban-regel utløses under salgsordreopprettelse. Kanban-regelen for hendelse etterfyller behov som stammer fra salgsordrelinjene. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Den er ment for prosessingeniøren eller verdistrømlederen når de klargjør produksjon av et nytt eller endret produkt.




## <a name="create-a-new-kanban-rule"></a>Opprett en ny Kanban-regel
1. Gå til Kanban-regler.
2. Klikk Ny.
3. Velg Hendelse i feltet Etterfyllingsstrategi.
    * Hvis du velger Hendelse betyr det at kanban-regelen blir utløst av en hendelse, for eksempel oppretting av en salgsordrelinje.   Dette brukes for områder der hver kanban skal dekke et bestemt behov.  
4. Angi eller velg en verdi i feltet Første planaktivitet.
    * Velg Endelig sammenstilling.  
5. Vis delen Detaljer.
6. Angi eller velg en verdi i feltet Produkt.
    * Velg L0050.  

## <a name="define-an-event"></a>Definere en hendelse
1. Utvid delen Hendelser.
2. Velg Automatisk i feltet Salgshendelse.
    * Når du velger salgshendelsen Automatisk, utløses denne kanban-regelen automatisk når en salgslinje samsvarer med produkt- og mottakslokasjonen. I denne fremgangsmåten er det produkt L0050 på lager 13.  
3. Sett Minimumsantall for hendelse til 50.
    * Med et minimumsantall for hendelse på 50 utløses kanban-regelen bare av hendelser med et antall på 50 eller flere.  
4. Utvid delen Produksjonsflyt.
    * Legg merke til at mottaksplasseringen er lager 13. Dette betyr at denne kanban-regelen utløses for denne lokasjonen.  
    * I dette eksemplet vil en salgslinje for produktet L0050, med et antall på 50 eller mer, på lager 13, utløse denne kanban-regelen.  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a>Opprette salgslinje for å utløse Kanban-regel for hendelse
1. Gå til Alle salgsordrer.
    * En advarsel vises når kanban-regelen lagres, noe som betyr at Kanbaner opprettes i sanntid under oppretting av salgsordrer.  
2. Klikk Ny.
3. Angi eller velg en verdi i Kundekonto-feltet.
    * Velg for eksempel US-003.  
4. Klikk OK.
5. Skriv inn L0050 i feltet Varenummer.
6. Skriv inn 1 i feltet Område.
    * Velg område 1 fordi lager 13 er i område 1.  
7. Angi eller velg en verdi i feltet Lager.
    * Sett Lager til 13.  
8. Sett verdien for Antall til 75.
    * Angi et antall på 50 eller høyere, for å utløse den opprettede kanban-regelen.  

## <a name="verify-that-kanban-is-created"></a>Kontroller at kanban er opprettet
1. Klikk Produkt og forsyning.
2. Klikk Vis utligningstre.
    * Legg merke til at en kanban med samme antall som salgslinjen er opprettet. Du kan også se materialutstedelsene som trengs for å produsere L0050. Dette er det siste trinnet i prosedyren.  


