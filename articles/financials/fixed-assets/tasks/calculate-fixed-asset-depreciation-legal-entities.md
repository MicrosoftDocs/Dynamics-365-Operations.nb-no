---
title: Beregne avskrivning av anleggsmidler på tvers av juridiske enheter
description: Avskrivning av anleggsmidler kan kjøres på tvers av juridiske enheter i ett enkelt trinn.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2575354af322827972ffa650e9c732170c5a6eb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "316999"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Beregne avskrivning av anleggsmidler på tvers av juridiske enheter

[!include [task guide banner](../../includes/task-guide-banner.md)]

Avskrivning av anleggsmidler kan kjøres på tvers av juridiske enheter i ett enkelt trinn. Denne prosedyren viser deg hvordan du definerer og kjører prosessen for flere juridiske enheter. Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.


## <a name="set-up-cross-company-depreciation-run-journals"></a>Definere journaler for avskrivningskjøring på tvers av firmaet
1. Gå til Anleggsmidler > Oppsett > Parametere for anleggsmidler.
2. Vis delen Forslag til anleggsmidler.
3. Klikk Legg til.
4. Angi eller velg en verdi i Posteringslag-feltet.
5. Angi eller velg en verdi i feltet Journalnavn.
    * Gjenta journaloppsettet på siden Parametere for anleggsmidler i hver juridiske enhet.  

## <a name="depreciation-run"></a>Avskrivningskjøring
1. Gå til Anleggsmidler > Journaloppføringer > Opprett avskrivningsforslag.
2. Angi eller velg en verdi i Posteringslag-feltet.
    * Journalnavnet brukes som standard fra Parametere for anleggsmidler. Det kan endres her for gjeldende juridiske enhet.  
3. Angi en dato i Til dato-feltet.
    * Velg de juridiske enhetene som skal inkluderes i avskrivningskjøringen.  
    * Bare juridiske enheter med journaler som er definert for Forslag til anleggsmidler på siden Parametere for anleggsmidler vises i listen.  
4. Velg Ja i feltet Poster journaler.
    * Filtreringsfeltene inkluderer alle anleggsmidler, grupper og tablåer for de juridiske enhetene som er valgt for denne avskrivningskjøringen.  
    * Alternativet Satsvis behandling er aktivert som standard. Når dette alternativet er aktivert, vil oppretting og postering av avskrivningsjournalen kjøres i bakgrunnen.  
5. Klikk Opprett journal.
6. Gå til Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal.

