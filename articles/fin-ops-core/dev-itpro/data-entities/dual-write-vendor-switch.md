---
title: Bytte mellom leverandørutforminger
description: ''
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772370"
---
# <a name="switch-between-vendor-designs"></a>Bytte mellom leverandørutforminger

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>Flyt for leverandørdata 

Hvis du vil bruke andre Dynamics 365-apper for leverandørkontroll, og du vil isolere leverandørinformasjon fra kunder, kan du bruke denne grunnleggende leverandørutformingen.  

![Grunnleggende leverandørflyt](media/dual-write-switch-1.png)
 
Hvis du bruker andre Dynamics 365-apper for leverandørkontroll, og du vil fortsatt bruke **konto**-enheten til å lagre leverandørinformasjon, kan du bruke denne utvidede leverandørutformingen. I denne utformingen blir utvidet leverandørinformasjon som leverandør på vent-status og leverandørprofil lagret i **leverandører**-enheten i Common Data Service. 

![Utvidet flyt for leverandør](media/dual-write-switch-2.png)
 
Følg fremgangsmåten nedenfor for å bruke den utvidede leverandørutformingen: 
 
1. **SupplyChainCommon**-løsningspakken inneholder malene for arbeidsflytprosessen, som vist i følgende bilde.
    > [!div class="mx-imgBorder"]
    > ![Maler for arbeidsflytprosess](media/dual-write-switch-3.png)
2. Opprett nye arbeidsflytprosesser ved hjelp av malene for arbeidsflytprosess: 
    1. Opprett en ny arbeidsflytprosess for **leverandør**-enheten ved hjelp av malen for arbeidsflytprosess **Opprett leverandører i kontoenhet**, og klikk **OK**. Denne arbeidsflyten håndterer leverandøropprettelsesscenarioet for **Konto**-enheten.
        > [!div class="mx-imgBorder"]
        > ![Opprette leverandører i kontoenhet](media/dual-write-switch-4.png)
    2. Opprett en ny arbeidsflytprosess for **leverandør**-enheten ved hjelp av malen for arbeidsflytprosess **Oppdater kontoenhet**, og klikk **OK**. Denne arbeidsflyten håndterer oppdateringsscenarioet for **Konto**-enheten. 
        > [!div class="mx-imgBorder"]
        > ![Oppdater kontoenhet](media/dual-write-switch-5.png)
    3. Opprett nye arbeidsflytprosesser fra malene som ble opprettet i **Kontoer**-enheten. 
        > [!div class="mx-imgBorder"]
        > ![Opprette leverandører i leverandørenhet](media/dual-write-switch-6.png)
        > [!div class="mx-imgBorder"]
        > ![Oppdater leverandørenhet](media/dual-write-switch-7.png)
    4. Du kan konfigurere arbeidsflytene som sanntids- eller bakgrunns-arbeidsflyter basert på dine behov. 
        > [!div class="mx-imgBorder"]
        > ![Konverter til en bakgrunnsarbeidsflyt](media/dual-write-switch-8.png)
    5. Aktiver arbeidsflytene du opprettet for **konto**- og **leverandør**-enhetene for å begynne å bruke Customer Engagement **Konto**-enheten for lagring av leverandørinformasjon. 
 
