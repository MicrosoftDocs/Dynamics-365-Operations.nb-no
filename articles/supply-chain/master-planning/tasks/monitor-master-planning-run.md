--- 
title: "Overvåke en kjøring av hovedplanlegging"
description: "Produksjonsplanleggeren vil se om det er en kjøring for hovedplanlegging pågår."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1e08d9fd3388561563e6fb982416186a652b4ce2
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="monitor-a-master-planning-run"></a>Overvåke en kjøring av hovedplanlegging

[!include [task guide banner](../../includes/task-guide-banner.md)]

Produksjonsplanleggeren vil se om det er en kjøring for hovedplanlegging pågår. Bruk USMF-demodatafirmaet til å utføre denne prosedyren.


## <a name="run-master-planning"></a>Kjør hovedplanlegging
1. Klikk Hovedplanlegging.
    * Du finner dette på standard instrumentbord.  
2. Angi eller velg en verdi i Plan-feltet.
    * Eksempel: Statisk plan  
3. Klikk Kjør.
4. Velg Ja i feltet Spor behandlingstid.
    * Hvis feltet allerede er valgt, hopper du over trinnet.  
5. Angi et tall i feltet Antall tråder.
6. Utvid delen Poster som skal inkluderes.
7. Klikk Filter.
8. Merk den valgte raden i listen.
    * Merk raden der Felt = Varenummer.  
9. Angi eller velg en verdi i Kriterier-feltet.
    * Eksempel: T0001  
10. Klikk OK.
11. Klikk OK.

## <a name="monitor-the-master-planning-run"></a>Overvåke kjøringen av hovedplanlegging
1. Klikk Logg.
2. Klikk Forespørsler.
3. Klikk Varighet for prosessoppgave.
4. Finn og velg ønsket post i listen.
    * Du kan få en oversikt over hvor lang tid det tok for å fullføre hvert planleggingstrinn for hver vare.  


