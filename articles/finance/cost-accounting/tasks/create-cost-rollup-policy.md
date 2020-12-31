---
title: Opprette en policy for opprullet kost
description: Denne prosedyren viser hvordan du oppretter en policy for opprullet kost og oppretter regler for policyen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b6d32cc2c1844c6c334dd00b249c736e153f13d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446533"
---
# <a name="create-a-cost-rollup-policy"></a>Opprette en policy for opprullet kost

[!include [banner](../../includes/banner.md)]

Denne prosedyren viser hvordan du oppretter en policy for opprullet kost og oppretter regler for policyen. Demonstrasjonsdataene USP2 brukes til å opprette denne fremgangsmåten.


## <a name="create-a-policy"></a>Opprette en policy
1. Gå til Kostnadsregnskap > Policyer > Policyer for opprullet kost.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Policynavn.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadsobjekt.
    * Velg Opprullet kost CC.  
6. Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadselement.
    * Velg Opprullet kost CC.  
7. Klikk Lagre.

## <a name="create-rules-for-the-cost-rollup-policy"></a>Opprette regler for policyen for opprullet kostnad
1. Klikk Ny.
2. Merk den valgte raden i listen.
3. Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.
    * Velg 007.  
4. Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadselement.
    * Velg Opprullet kost CE.  
5. Angi eller velg en verdi i feltet Sekundært kostnadselement.
    * I dette eksemplet kan du tilordne det sekundære kostnadselementet CC-007 til kostsenteret.  
6. Klikk Ny.
7. Merk den valgte raden i listen.
8. Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.
    * Velg 008.  
9. Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadselement.
    * Velg Opprullet kost CE.  
10. Angi eller velg en verdi i feltet Sekundært kostnadselement.
    * I dette eksemplet kan du tilordne det sekundære kostnadselementet CC-008 til kostsenteret.  
11. Klikk Ny.
12. Merk den valgte raden i listen.
13. Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.
    * Velg 009.  
14. Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadselement.
    * Velg Opprullet kost CE.  
15. Angi eller velg en verdi i feltet Sekundært kostnadselement.
    * I dette eksemplet kan du tilordne det sekundære kostnadselementet CC-009 til kostsenteret.  
    * Fortsett til alle kostsentre er tilordnet de tilhørende sekundære kostnadselementer.  
16. Klikk Lagre.

