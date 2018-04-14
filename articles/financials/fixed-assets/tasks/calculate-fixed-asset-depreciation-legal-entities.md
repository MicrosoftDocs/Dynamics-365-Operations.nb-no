--- 
title: "Beregne avskrivning av anleggsmidler på tvers av juridiske enheter"
description: "Denne prosedyren viser deg hvordan du definerer og kjører avskrivningsprosessen for flere juridiske enheter."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d804480167414cd038f8229db312dc9c52d131f8
ms.openlocfilehash: 4c45da124136b7fecb916d2ff9098c8ffeff6cb1
ms.contentlocale: nb-no
ms.lasthandoff: 11/02/2017

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Beregne avskrivning av anleggsmidler på tvers av juridiske enheter

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Avskrivning av anleggsmidler kan kjøres på tvers av juridiske enheter i ett enkelt trinn. Denne prosedyren viser deg hvordan du definerer og kjører prosessen for flere juridiske enheter. Den bruker regnskapsførerrollen.  

Denne registreringen bruker demonstrasjonsfirmaet USMF.


Underoppgave trinn (16): Definer journaler for avskrivningskjøring på tvers av firmaet. 

1. Du må først definere journalene som skal brukes i avskrivningskjøring på tvers av firmaet for hver juridiske enhet. Gå til Anleggsmidler > Oppsett > Parametere for anleggsmidler. 
2. Vis delen Forslag til anleggsmidler. 
3. Opprette en post med journalnavnet som skal brukes for hvert posteringslag i den juridiske enheten. Hvis tablåer ikke posterer til finans, skal Ingen postering-laget velges med tilhørende journal. Klikk Legg til. 
4. Angi eller velg en verdi i Posteringslag-feltet. 
5. Angi eller velg en verdi i feltet Journalnavn. 
6. Gjenta journaloppsettet på siden Parametere for anleggsmidler i hver juridiske enhet. 

Underoppgave: Beregne avskrivining.

1. Bruk siden Opprett avskrivningsforslag til å starte avskrivning på tvers av juridiske enheter. Gå til Anleggsmidler > Journaloppføringer > Opprett avskrivningsforslag. 
2. Angi eller velg en verdi i Posteringslag-feltet. 
3. Journalnavnet brukes som standard fra Parametere for anleggsmidler. Det kan endres her for gjeldende juridiske enhet. 
4. Angi en dato i Til dato-feltet. 
5. Velg de juridiske enhetene som skal inkluderes i avskrivningskjøringen. Bare juridiske enheter med journaler som er definert for Forslag til anleggsmidler på siden Parametere for anleggsmidler vises i listen. 
6. Når aktivert, vil alternativet Poster journaler automatisk postere avskrivningsjournalene når de opprettes. Når det ikke er merket, vil journalene bli opprettet, men ikke postert, slik at du kan se gjennom detaljene før postering. Velg Ja i feltet Poster journaler. 
7. Filtreringsfeltene inkluderer alle anleggsmidler, grupper og tablåer for de juridiske enhetene som er valgt for denne avskrivningskjøringen. 
8. Alternativet Satsvis behandling er aktivert som standard. Når dette alternativet er aktivert, vil oppretting og postering av avskrivningsjournalen kjøres i bakgrunnen. 
9. Klikk Opprett journal. 
10. Du må vise avskrivningsjournalene som er opprettet i de respektive juridiske enhetene. Gå til Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal.

