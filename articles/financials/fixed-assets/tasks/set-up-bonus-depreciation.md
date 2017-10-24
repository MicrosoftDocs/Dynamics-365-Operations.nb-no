--- 
title: Definere bonusavskrivning
description: "Denne fremgangsmåten viser hvordan du oppretter et særskilt avskrivningsfradrag og knytter det til et anleggsmiddeltablå."
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7e6ebb13084626b477b6e0b24acdc09e2c0d3d6d
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-bonus-depreciation"></a>Definere bonusavskrivning

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter et særskilt avskrivningsfradrag og knytter det til et anleggsmiddeltablå. Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.


## <a name="create-a-special-depreciation-allowance"></a>Opprette et særskilt avskrivningsfradrag
1. Gå til Anleggsmidler > Oppsett > Særskilte avskrivningsfradrag.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Særskilte avskrivningsfradrag.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Angi et tall i Prosent-feltet.
    * Hvis det ikke er angitt en prosent, angir du et beløp.  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a>Tilknytte et særskilt avskrivningsfradrag til et anleggsmiddelgruppetablå
1. Gå til Anleggsmidler > Oppsett > Anleggsmiddelgrupper.
2. I listen velger du anleggsmiddelgruppen som er tilknyttet det særskilte avskrivningsfradraget.
3. Klikk Tablåer.
4. I listen velger du tablået som er tilknyttet det særskilte avskrivningsfradraget.
5. Klikk Særskilt avskrivningsfradrag.
6. Klikk Ny.
7. Skriv inn eller velg en verdi i feltet Særskilte avskrivningsfradrag.
    * Standard for prosenten eller beløpet hentes fra oppsettet for særskilte avskrivningsfradrag.  
8. Angi et tall i Prioritet-feltet.


