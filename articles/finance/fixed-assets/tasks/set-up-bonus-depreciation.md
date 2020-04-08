---
title: Definere bonusavskrivning
description: Denne fremgangsmåten viser hvordan du oppretter et særskilt avskrivningsfradrag og knytter det til et anleggsmiddeltablå.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91243a4cee44410a221902990d31a10f1805eb08
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138259"
---
# <a name="set-up-bonus-depreciation"></a>Definere bonusavskrivning

[!include [banner](../../includes/banner.md)]

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

