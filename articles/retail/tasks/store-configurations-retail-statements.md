---
title: " Butikkonfigurasjoner for detaljhandelsutdrag"
description: Denne prosedyren beskriver konfigurasjoner for detaljhandelsbutikken som påvirker hvordan detaljhandelsutdrag opprettes og posteres.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbedcda59f503b103d5448e59038e4ed8ca0b51d
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916536"
---
# <a name="store-configurations-for-retail-statements"></a> Butikkonfigurasjoner for detaljhandelsutdrag

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne prosedyren beskriver konfigurasjoner for detaljhandelsbutikken som påvirker hvordan detaljhandelsutdrag opprettes og posteres. Finansdimensjoner i detaljhandelsbutikker dekkes i en annen prosedyre. Denne prosedyren bruker demonstrasjonsfirmaet USRT.

1. I **navigasjonsruten** går du til **Moduler > Detaljhandel og handel > Kanaler > Detaljhandelbutikker > Alle detaljhandelbutikker**.
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
4. Klikk **Rediger**.
5. Innstillingene i hurtigfanen **Utdrag/avslutning** kan påvirke opprettingen av utdrag, validering og postering for butikken. Utvid hurtigfanen **Utdrag/avslutning**.  
6. Velg metoden du vil bruke for å gruppere utdragslinjene, i **Utdragsmetode**-feltet.  
7. Velg Ja i **Ett utdrag per dag** hvis det bare skal opprettes ett utdrag per dag når utdrag opprettes fra den satsvise jobben for utdragsoppretting.  
8. Feltet **Beregning av kasseoppgjør** definerer om kasseoppgjør skal legges sammen, eller om den siste skal brukes.  
9. Velg finanskontoen som avrundingsdifferanser skal posteres mot, i **Avrunding**-feltet.  
10. I feltet **Maksimal avrundingsdifferanse** angir du maksimalt tillatt avrundingsdifferanse.
11. Angi den maksimale totale posteringsdifferansen som er tillatt for et utdrag, i **Postering**-feltet.
12. Angi den maksimale totale differansen i et skift i et utdrag, i **Skift**-feltet.  
13. I **Transaksjon**-feltet angir du den maksimale totale differansen i en utdragslinje.  
14. I feltet **Avslutningsmetode** definerer du om transaksjonene som skal inkluderes i et utdrag, skal være en del av en lukket skift, eller om de kan være enhver transaksjon i det definerte dato-/klokkeslettintervallet.  
15. I feltet **Slutt på arbeidsdag** angir du et tidspunkt hvis transaksjoner som skjer etter midnatt, skal posteres på forrige dag.  
16. Velg Ja i **Poster som arbeidsdag** hvis transaksjoner som skjer etter midnatt, skal posteres som en del av dagen før.  
17. Velg Ja i **Del etter utdragsmetode** hvis du vil at utdrag skal opprettes for hver definerte utdragsmetode. Dette kan være nyttig hvis resultatet av posteringen må forbedres for butikker med høye transaksjonsvolumer siden det vil opprette mange mindre utdrag som kan behandles parallelt.  
18. I hurtigfanen **Generelt** i feltet **Standardkunde** kan du velge kundekontoen som skal brukes for salg til kunder som kommer inn i butikken.  

