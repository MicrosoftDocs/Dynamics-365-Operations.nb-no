---
title: Opprett avskrivningsforslag
description: Denne fremgangsmåten beskriver hvordan satsvise avskrivningsforslag fungerer, og forklarer hvordan du foreslår avskrivning for anleggsmidler.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07146adfe1ead2b6e06e3c323963f8c012381b76
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840007"
---
# <a name="create-depreciation-proposal"></a>Opprett avskrivningsforslag

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

