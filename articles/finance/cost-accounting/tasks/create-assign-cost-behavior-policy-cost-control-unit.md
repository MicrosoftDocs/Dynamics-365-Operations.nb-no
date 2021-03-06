---
title: Opprette og tilordne en kostnadsatferdspolicy til en kostnadskontrollenhet
description: Kostnadsatferd er klassifiseringen av kostnader som faste eller variable.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 757e5a5be94e7190f4dbb51d667dc8adec4b824a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826329"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>Opprette og tilordne en kostnadsatferdspolicy til en kostnadskontrollenhet

[!include [banner](../../includes/banner.md)]

Kostnadsatferd er klassifiseringen av kostnader som faste eller variable. En policy og de tilsvarende reglene må tilordnes til en kostnadskontrollenhet for at policyen skal aktiveres. Bruk denne fremgangsmåten til å opprette en policy og deretter tilordne policyen til en kostnadskontrollenhet.


## <a name="create-a-cost-behavior-hierarchy"></a>Opprette et hierarki for kostnadsatferd
1. Gå til Kostnadsregnskap > Dimensjoner > Dimensjonshierarkier.
2. Klikk Ny.
3. Klikk Opprett.
4. Skriv inn "Hierarki for kostnadsatferd" i feltet Dimensjonshierarkinavn.
5. Angi eller velg en verdi i feltet Dimensjon.
    * Velg Kostnadselementer.  
6. Klikk Lagre.
7. Klikk Vis hierarki.
8. Klikk Ny.
9. Skriv inn en verdi i feltet Nodenavn.
    * Angi Fast kostnad.  
10. Velg "Hierarki for kostnadsatferd" i treet.
11. Klikk Ny.
12. Skriv inn en verdi i feltet Nodenavn.
    * Angi Variabel kostnad.  
13. Klikk Lagre.
14. Velg "Hierarki for kostnadsatferd\Fast kostnad" i treet.
15. Klikk Ny.
16. Merk den valgte raden i listen.
17. Angi eller velg en verdi i feltet Fra dimensjonsmedlem.
    * Området for dimensjonsmedlemmene kan inneholde mellomrom, men medlemmene kan ikke overlappe.  
18. Angi eller velg en verdi i feltet Til dimensjonsmedlem.
    * Området for dimensjonsmedlemmene kan inneholde mellomrom, men medlemmene kan ikke overlappe.  
19. Velg "Hierarki for kostnadsatferd\Variabel kostnad" i treet.
20. Klikk Ny.
21. Merk den valgte raden i listen.
22. Angi eller velg en verdi i feltet Fra dimensjonsmedlem.
    * Området for dimensjonsmedlemmene kan inneholde mellomrom, men medlemmene kan ikke overlappe.  
23. Angi eller velg en verdi i feltet Til dimensjonsmedlem.
    * Området for dimensjonsmedlemmene kan inneholde mellomrom, men medlemmene kan ikke overlappe.  
24. Klikk Lagre.

## <a name="create-the-policy-and-rules"></a>Opprette policyen og regler
1. Gå til Kostnadsregnskap > Policyer > Policyer for kostnadsatferd.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Policynavn.
4. Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadselement.
    * Velg policyhierarkiet du nettopp opprettet.  
5. Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadsobjekt.
    * Velg Organisasjon.  
6. Klikk Lagre.
7. Klikk Ny.
8. Merk den valgte raden i listen.
9. Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadselement.
    * Utvid hierarkiet for å velge Variabel kostnad.  
10. Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.
    * Som standard er den variable prosentdelen 100 prosent.  
11. Klikk Policytilordninger for kostnadskontrollenhet.
12. Klikk Ny.
13. Merk den valgte raden i listen.
14. Angi en dato i feltet Gyldig fra regnskapsdato.
    * Reglene er datoeffektive, og en bruker eller systemet kan utløpe en regel hvis det opprettes en nyere versjon.  
15. Angi eller velg en verdi i feltet Kostnadskontrollenhet
16. Klikk Lagre.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]