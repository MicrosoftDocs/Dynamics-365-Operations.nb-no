---
title: Opprette et avskrivningsforslag
description: Dette emnet beskriver hvordan satsvise avskrivningsforslag fungerer, og forklarer hvordan du foreslår avskrivning for anleggsmidler.
author: abruer
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6cf285e8764af8c6525fb3f9cbec7306917e57e832777588e8c2c1d4aeed818
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719252"
---
# <a name="create-a-depreciation-proposal"></a>Opprette et avskrivningsforslag

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan satsvise avskrivningsforslag fungerer, og forklarer hvordan du foreslår avskrivning for anleggsmidler. Denne oppgaven bruker demonstrasjonsfirmaet USMF og regnskapsførerrollen.


## <a name="create-a-depreciation-proposal"></a>Opprette et avskrivningsforslag
1. I navigasjonsruten går du til **Moduler > Anleggsmidler > Journaloppføringer > Opprette avskrivningsforslag**.
2. I **Journalnavn**-feltet velger du et alternativ fra rullegardinmenyen.
3. Angi en dato i **Til dato**-feltet.

    - Velg alternativet **Summer avskrivning** for å summere månedlige avskrivninger i én journallinje.  
    - Hvis for eksempel verdien for Til-dato er 31. mars 2015, genereres følgende beskrivelse: "Avskrivninger siden 31. januar 2015." **Dato**-feltet i de foreslåtte journallinjene settes deretter til 31. mars 2015.  
    - Avskrivningsforslaget kan filtreres etter anleggsmiddel, anleggsmiddelgruppe eller andre kriterier ved hjelp av alternativet for **filtrering**.  
    - Når du bruker skjemaet **Opprett anskaffelses- eller avskrivningsforslag for anleggsmiddel**, kan du foreslå avskrivning i grupper. Dette anbefales for større forslag som bruker flere systemressurser. Hvis du velger partialternativet, kan du fortsatt fullføre andre oppgaver i denne perioden. Når du foreslår avskrivning på denne måten, beregnes avskrivning for verdimodeller for anleggsmidler.  

4. Velg **Opprett journal**.

## <a name="review-depreciation-entries"></a>Vise avskrivningsposter
1. I navigasjonsruten går du til **Moduler > Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal**.
2. Finn og velg ønsket post i listen.
3. Velg **Linjer**.
4. Velg **Poster**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]