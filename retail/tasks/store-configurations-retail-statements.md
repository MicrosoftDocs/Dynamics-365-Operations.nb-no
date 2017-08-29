--- 
title: " Butikkonfigurasjoner for detaljhandelsutdrag"
description: "Denne prosedyren beskriver konfigurasjoner for detaljhandelsbutikken som påvirker hvordan detaljhandelsutdrag opprettes og posteres."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 2f73bca3bd1699ee1c2e98706a4d69f8b0b25052
ms.contentlocale: nb-no
ms.lasthandoff: 07/28/2017

---
# <a name="store-configurations-for-retail-statements"></a> Butikkonfigurasjoner for detaljhandelsutdrag

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne prosedyren beskriver konfigurasjoner for detaljhandelsbutikken som påvirker hvordan detaljhandelsutdrag opprettes og posteres. Finansdimensjoner i detaljhandelsbutikker dekkes i en annen prosedyre. Denne prosedyren bruker demonstrasjonsfirmaet USRT.

1. Gå til Detaljhandel og handel > Kanaler > Detaljhandelbutikker > Alle detaljhandelsbutikker.
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
    * Innstillingene i delen Utdrag/avslutning kan påvirke opprettingen av utdrag, validering og postering for butikken.  Åpne delen Utdrag/avslutning.  
    * Velg metoden du vil bruke for å gruppere utdragslinjene.  
    * Velg Ja hvis det bare skal opprettes ett utdrag per dag når utdrag opprettes fra den satsvise jobben for utdragsoppretting.  
    * Feltet Beregning av kasseoppgjør definerer om kasseoppgjør skal legges sammen, eller om den siste skal brukes.  
    * Velg finanskontoen som avrundingsdifferanser skal posteres mot.  
    * I feltet for maksimal avrundingsdifferanse kan du angi maksimalt tillatt avrundingsdifferanse.  
    * Du kan angi den maksimale totale posteringsdifferansen som er tillatt for et utdrag, i Postering-feltet.  
    * Du kan angi den maksimale totale differansen i et skift i et utdrag, i Skift-feltet.  
    * I Transaksjon-feltet kan du angi den maksimale totale differansen i en utdragslinje.  
    * I feltet Avslutningsmetode kan du definere om transaksjonene som skal inkluderes i et utdrag, skal være en del av en lukket skift, eller om de kan være enhver transaksjon i det definerte dato-/klokkeslettintervallet.  
    * I feltet Slutt på arbeidsdag kan du angi et tidspunkt hvis transaksjoner som skjer etter midnatt, skal posteres på forrige dag.  
    * Velg Ja hvis transaksjoner som skjer etter midnatt, skal posteres som en del av dagen før.  
    * Velg Ja hvis du vil at utdrag skal opprettes for hver definerte utdragsmetode. Dette kan være nyttig hvis resultatet av posteringen må forbedres for butikker med høye transaksjonsvolumer siden det vil opprette mange mindre utdrag som kan behandles parallelt.  
    * I feltet Standardkunde kan du velge kundekontoen som skal brukes for salg til kunder som kommer inn i butikken.  


