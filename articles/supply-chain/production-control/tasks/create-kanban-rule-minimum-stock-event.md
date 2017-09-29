--- 
title: Opprette en Kanban-regel ved hjelp av en hendelse for minste beholdning
description: "Denne fremgangsmåten fokuserer på oppsettet for å opprette en Kanban-regel som bruker en minste beholdning-hendelse for å sikre at et bestemt produkt alltid er tilgjengelig på em bestemt lokasjon."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0c480b518925a8536ebb77d60fcf1f1a548b097f
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# Opprette en Kanban-regel ved hjelp av en hendelse for minste beholdning

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten fokuserer på oppsettet for å opprette en Kanban-regel som bruker en minste beholdning-hendelse for å sikre at et bestemt produkt alltid er tilgjengelig på em bestemt lokasjon. Det opprettes en Kanban-regel for å overføre materiale til lokasjonen når lagernivået faller under 200 enheter. Ved å kjøre Behandling av utligningshendelse, opprettes de nødvendige Kanbanene. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven. Denne oppgaven er ment for prosessingeniøren eller verdistrømlederen, når de klargjør produksjon av et nytt eller endret produkt i et lean-miljø.


## Opprett en ny Kanban-regel
1. Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.
2. Klikk Ny.
3. Velg Uttak i Type-feltet.
    * Denne typen brukes til å opprette Kanbaner for overføring.  
4. Velg Hendelse i feltet Etterfyllingsstrategi.
    * Hendelsesstrategien brukes for å opprette overføringen av Kanbaner basert på en hendelse. Senere i fremgangsmåten utløser du Kanbaner for overføring ved hjelp av lageretterfylling.  
5. Angi eller velg en verdi i feltet Første planaktivitet.
    * Angi eller velg ReplenishSpeakerComponents. Denne overføringsaktiviteten har mottakslager (utdata), og lokasjon 12, noe som innebærer at materialer vil bli flyttet til lokasjon 12 i lager 12.  
6. Vis delen Detaljer.
7. Angi eller velg en verdi i feltet Produkt.
    * Velg M0007.  
8. Utvid delen Hendelser.
9. Velg Parti i feltet Hendelse for lageretterfylling.
    * Dette oppretter Kanbaner for å oppfylle materialbehov på den tilknyttede plasseringen under behandling av utligningshendelse.  

## Sette minimumsantallet for varen
1. Klikk for å følge koblingen i Produkt-feltet.
2. Klikk for å følge koblingen i Varenummer-feltet.
3. Vis Produktbilde-faktaboksen.
4. Klikk Plan i handlingsruten.
5. Klikk Varedekning.
6. Klikk Ny.
7. Merk den valgte raden i listen.
8. Angi eller velg en verdi i feltet Lager.
    * Sett Lager til 12.  
9. Sett Minimum til 200.

## Kjøre den satsvise jobben for oppretting av hendelse
1. Gå til Produksjonskontroll > Periodiske oppgaver > Satsvis behandling av Kanban-jobb > Behandling av utligningshendelse.
2. Klikk OK.
3. Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.
4. Klikk koblingen i den valgte raden i listen.
    * Velg Kanban-regelen som du opprettet tidligere.  
5. Vis delen Kanbaner.
    * Legg merke til at en Kanban ble opprettet for å overføre det nødvendige materialet til lager 12.  


