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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 8eb19ac9ded4dc2a091ff733f2f43cb6cafa1b43
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="monitor-a-master-planning-run"></a>Overvåke en kjøring av hovedplanlegging

[!include[task guide banner](../../includes/task-guide-banner.md)]

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

