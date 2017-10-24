--- 
title: Opprette en Kanban-regel for hendelse for stykklistelinje
description: "Denne oppgaven fokuserer på oppsettet som kreves for å opprette en kanban-regel for hendelse for å sikre forsyning for stykklistelinjer for produksjon i et blandet lean-produksjonsmiljø og klassisk produksjonsmiljø."
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 452cc5cf6060b71f91ad43e39e756dc23d759448
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-bom-line-event-kanban-rule"></a>Opprette en Kanban-regel for hendelse for stykklistelinje

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaven fokuserer på oppsettet som kreves for å opprette en kanban-regel for hendelse for å sikre forsyning for stykklistelinjer for produksjon i et blandet lean-produksjonsmiljø og klassisk produksjonsmiljø. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven. Denne oppgaven er ment for prosessingeniøren eller verdistrømsbehandling, når de klargjør produksjon av et nytt eller endret produkt.


## <a name="create-a-new-kanban-rule"></a>Opprett en ny Kanban-regel
1. Gå til Produksjonskontroll > Periodiske oppgaver > Kanban-antallsberegning > Kanban-regler.
2. Klikk Ny.
3. Velg Uttak i Type-feltet.
    * Typen Uttak brukes til å opprette Kanbaner for overføring.  
4. Velg Hendelse i feltet Etterfyllingsstrategi.
    * Hendelsesstrategien velges for å opprette overføringen av Kanbaner basert på en hendelse. Senere i denne aktivitetsveiledningen vil vi utløse den ved å beregne en produksjonsordre.  
5. Angi eller velg en verdi i feltet Første planaktivitet.
    * Angi eller velg ReplenishSpeakerComponents. Denne overføringsaktiviteten har mottakslager (utdata), og lokasjon 12, noe som innebærer at materiale vil bli flyttet til lokasjon 12 i lager 12.  
6. Vis delen Detaljer.
7. Angi eller velg M0001 i Produkt-feltet.
8. Utvid delen Hendelser.
9. Velg Automatisk i hendelsesfeltet Stykklistelinje.
    * Med hendelsesfeltet for stykklistelinje satt til Automatisk, vil en kanban opprettes for å oppfylle materialbehov for stykklistelinjer for produksjonsordre.  
10. Lukk siden.

## <a name="create-and-modify-a-new-production-order"></a>Opprette og endre en ny produksjonsordre
1. Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.
2. Klikk Ny produksjonsordre.
3. Angi eller velg en verdi i Varenummer-feltet.
    * Angi eller velg L0001. Vi bruker vare L0001 fordi vare M0001 inngår i stykklisten for vare L0001.  
4. Klikk Opprett.
5. Klikk koblingen i raden for L0001 i listen.
6. Klikk Stykkliste.
7. Klikk koblingen i den valgte raden i listen.
8. Klikk Rediger.
9. Velg Tilknyttet forsyning i Linjetype-feltet.
    * Tilknyttet forsyning velges for å utløse forsyningsopprettelsen av en kanban.  
10. Velg Nei i Ressursforbruk-feltet.
    * Hvis du fjerner merket for Ressursforbruk, kan vi endre lageret.  
11. Vis delen Lagerdimensjoner.
12. Skriv inn 12 i Lager-feltet.
    * Lageret er satt til 12, fordi dette er utleveringslager for uttaksaktiviteten.  
13. Skriv inn 12 i Lokasjon-feltet.
    * Lokasjonen er satt til 12, fordi dette er utleveringslokasjonen for uttaksaktiviteten.  
14. Lukk siden.
15. Lukk siden.

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a>Beregne produksjonsordren og vise opprettet kanban
1. Klikk Estimer.
    * Estimering av produksjonsordren utløser oppretting av tilknyttet kanban for å levere M0001.  
2. Klikk OK.
3. Lukk siden.
4. Lukk siden.
5. Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.
6. Klikk koblingen i den valgte raden i listen.
    * Velg Kanban-regel for hendelse som ble opprettet for vare M0001.  
7. Vis delen Kanbaner.
8. Merk den valgte raden i listen.
    * Legg merke til kanbanen som er opprettet for å levere M0001 for den estimerte produksjonsordren.  
    * Dette er det siste trinnet!  


