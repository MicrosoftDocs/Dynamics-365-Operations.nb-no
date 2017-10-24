--- 
title: "Definere gebyrer for hubtilbehør og tilbehørsmaler"
description: "Denne fremgangsmåten viser hvordan du oppretter en tilbehørsmal for en hub og bruker denne malen til å opprette et gebyr for hubtilbehør."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6381416640ffacf0a9d96d7da96bc33612ca7137
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a>Definere gebyrer for hubtilbehør og tilbehørsmaler

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en tilbehørsmal for en hub og bruker denne malen til å opprette et gebyr for hubtilbehør. Fremgangsmåten bruker USMF-datasettet. Dette oppsettet utføres vanligvis av en transportkoordinator.


## <a name="set-up-a-hub-master"></a>Definere en hubmal
1. Gå til Transportstyring > Oppsett > Vurdering > Tilbehørsmaler.
2. Klikk Ny.
3. Angi en verdi i Tilbehørsmal-feltet.
4. Skriv inn en verdi i Navn-feltet.
5. Velg Hub i Tilbehørstype-feltet.
6. Klikk Lagre.
7. Lukk siden.

## <a name="set-up-a-hub-accessorial-charge"></a>Definer et gebyr for hubtilbehør
1. Gå til Transportstyring > Oppsett > Vurdering > Gebyrer for hubtilbehøret.
2. Klikk Ny.
3. Skriv inn en verdi i feltet ID for hubtilbehør.
4. Klikk rullegardinknappen i Hub-feltet for å åpne oppslaget.
5. Finn og velg ønsket post i listen.
6. Velg et alternativ i feltet Hubposisjon.
    * Du kan opprette tillegget som en henting eller levering. Avhengig av valget gjelder tillegget for det tilsvarende transportsegmentet i din rute.  
7. Klikk rullegardinknappen i feltet Tilbehørsmal for å åpne oppslaget.
8. Klikk koblingen i den valgte raden i listen.
    * Velg malen du nettopp opprettet.  
9. Klikk Lagre.
10. Lukk siden.


