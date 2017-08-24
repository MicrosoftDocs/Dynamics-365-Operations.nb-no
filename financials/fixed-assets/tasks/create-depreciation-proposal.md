--- 
title: Opprette et avskrivningsforslag
description: "Denne fremgangsmåten beskriver hvordan satsvise avskrivningsforslag fungerer, og forklarer hvordan du foreslår avskrivning for anleggsmidler."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ffc358fa7db0ae40fb39d3acdfee7783949f0e1f
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-depreciation-proposal"></a>Opprette et avskrivningsforslag

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten beskriver hvordan satsvise avskrivningsforslag fungerer, og forklarer hvordan du foreslår avskrivning for anleggsmidler. Denne oppgaven bruker demonstrasjonsfirmaet USMF og regnskapsførerrollen.


## <a name="create-depreciation-proposal"></a>Opprett avskrivningsforslag
1. Gå til Anleggsmidler > Journaloppføringer > Opprett avskrivningsforslag.
2. Klikk rullegardinknappen i feltet Journalnavn for å åpne oppslaget.
3. Klikk koblingen i den valgte raden i listen.
4. Angi en dato i Til dato-feltet.
    * Velg alternativet Summer avskrivning for å summere månedlige avskrivninger i én journallinje.  
    * Hvis for eksempel verdien for Til-dato er 31. mars 2015, genereres følgende beskrivelse: "Avskrivninger siden 31. januar 2015." Datofeltet i de foreslåtte journallinjene settes deretter til 31. mars 2015.  
    * Avskrivningsforslaget kan filtreres etter anleggsmiddel, anleggsmiddelgruppe eller andre kriterier ved hjelp av alternativet for filtrering.  
    * Når du bruker Opprett anskaffelses- eller avskrivningsforslag for anleggsmiddelskjemaet, kan du foreslå avskrivning i grupper. Dette anbefales for større forslag som bruker flere systemressurser. Hvis du velger partialternativet, kan du fortsatt fullføre andre oppgaver i denne perioden. Når du foreslår avskrivning på denne måten, beregnes avskrivning for verdimodeller for anleggsmidler.  
5. Klikk Opprett journal.

## <a name="review-depreciation-entries"></a>Vise avskrivningsposter
1. Gå til Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal.
2. Finn og velg ønsket post i listen.
3. Klikk Linjer.
4. Klikk Poster.


