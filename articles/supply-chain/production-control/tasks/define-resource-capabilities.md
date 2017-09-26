--- 
title: Definere ressursfunksjoner
description: "Ressursfunksjoner beskriver hva operasjonsressursene kan utføre."
author: sorenva
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 4a7d342eeb16fd76f2dde58151bfc7973de76e2d
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="define-resource-capabilities"></a>Definere ressursfunksjoner

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ressursfunksjoner beskriver hva operasjonsressursene kan utføre. Under planlegging sammenlignes kravene for hver jobb og en operasjon mot mulighetene i de tilgjengelige ressursene. Denne oppgaveveiledning hjelper deg med å opprette en ressursfunksjon og tilordne den til en ressurs. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.


## <a name="create-a-resource-capability"></a>Opprett en ressursfunksjon
1. Gå til Ressursfunksjoner.
2. Klikk Ny.
3. Skriv inn IDen til ressursfunksjonen i Funksjon-feltet.
    * For en bestemt operasjon kan du bruke funksjons-IDen til å angi at ressurser må ha denne muligheten til å utføre operasjonen.  
4. Angi en kort beskrivelse av funksjonen i Beskrivelse-feltet.

## <a name="assign-capability-to-a-resource"></a>Tilordne funksjon til en ressurs
1. Klikk Legg til.
2. Skriv inn IDen til ressursen i Ressurs-feltet.
    * En ressursfunksjon kan tilordnes til én eller flere ressurser.  
3. Angi en dato i Utløp-feltet.
    * Du kan bruke dette feltet til å angi at en ressurs har funksjonen i en begrenset periode.  
4. Angi et tall i Prioritet-feltet.
    * Når du planlegger jobber og operasjoner, kan du angi om du velger ressursene etter prioritet. Hvis du vil gjøre dette, og mer enn én ressurs kan utføre jobben eller operasjonen etter ønsket dato, velges ressursen som har lavest prioritet i forhold til den nødvendige kapasiteten.  
5. Angi et nummer i Nivå-feltet.
    * Når du angir at en jobb eller operasjon krever en bestemt funksjon, kan du også angi det minste tillatelsesnivå som kreves. Bruk ressursnivået til å skille mellom ressurser som kan utføre den samme jobben, men med forskjellige hastigheter, styrker, størrelser og så videre.  


