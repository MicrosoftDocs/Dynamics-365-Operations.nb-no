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
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d228c387e8a6bf956f729a69e2296130db32dbd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210053"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Beregne avskrivning av anleggsmidler på tvers av juridiske enheter

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]