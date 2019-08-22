---
title: Definere posteringsprofiler for anleggsmidler
description: Denne oppgaveveiledninegn definerer posteringsprofiler for anleggsmiddel.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 494af854d408f0b0c02d753ff3d24eb3d6216fd9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839815"
---
# <a name="set-up-fixed-asset-posting-profiles"></a>Definere posteringsprofiler for anleggsmidler

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaveveiledninegn definerer posteringsprofiler for anleggsmiddel.  Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.  Eksemplene i oppgaveveiledningen er for en enkel posteringsprofil, men posteringsprofiler må opprettes for den bestemte kontoplanen og kravene til økonomisk rapportering.

1. I navigasjonsruten går du til **Moduler > Anleggsmidler > Oppsett > Posteringsprofiler for anleggsmidler**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i feltet **Posteringsprofil**.
4. Skriv inn en verdi i **Beskrivelse**-feltet. Du må opprette en posteringsprofil for hver transaksjonstype for anleggsmiddel som du vil bruke når du arbeider med anleggsmidler. Denne oppgaveveiledningen starter med anskaffelsestransaksjonstypen.  
5. Klikk på **Legg til** på verktøylinjen.
6. Angi eller velg en verdi i feltet **Tablå**. Ved hjelp av **Grupperinger**-feltet kan du definere posteringsprofilen til tabellen (én konto konfigurert for hvert anleggsmiddel) eller gruppen (én konto er definert for hver anleggsmiddelgruppe). I denne oppgaveveiledningen beholder du verdien "Alle" for alle anleggsmidler med det angitte tablået.  
7. Angi de ønskede verdiene i **Hovedkonto**-feltet. Du kan angi en motkonto for anskaffelser eller la feltet stå tomt for å fylle det ut for den bestemte transaksjonen.    
8. I rullegardinmenyen under hurtigfanen **Finanskontoer** velger du "Anskaffelsesjustering". For anskaffelsesjusteringstransaksjoner vil vi bruke de samme kontoene som brukes for anskaffelsestransaksjoner.  
9. Klikk **Legg til**.
10. Angi eller velg en verdi i feltet **Tablå**.
11. Angi de ønskede verdiene i **Hovedkonto**-feltet. Du kan angi en motkonto for anskaffelsesjusteringer eller la feltet stå tomt for å fylle det ut for den bestemte transaksjonen.    
12. I rullegardinmenyen under hurtigfanen **Finanskontoer** velger du "Avskrivning".
13. Klikk **Legg til**.
14. Angi eller velg en verdi i feltet **Tablå**.
15. Angi de ønskede verdiene i **Hovedkonto**-feltet.
16. Angi ønskede verdier i **Motkonto**-feltet.
17. I rullegardinmenyen under hurtigfanen **Finanskontoer** velger du "Avskrivningsjustering". For avskrivningsjusteringstransaksjoner vil vi bruke de samme kontoene som brukes for avskrivingstransaksjoner.  
18. Klikk **Legg til**.
19. Angi eller velg en verdi i feltet **Tablå**.
20. Angi de ønskede verdiene i **Hovedkonto**-feltet.
21. Angi ønskede verdier i **Motkonto**-feltet.
22. I rullegardinmenyen under hurtigfanen **Finanskontoer** velger du "Avhendingssalg".
23. Klikk **Legg til**.
24. Angi eller velg en verdi i feltet **Tablå**.
25. Angi de ønskede verdiene i **Hovedkonto**-feltet. Du kan angi en motkonto for avhendinger eller la feltet stå tomt for å fylle det ut for den bestemte transaksjonen.  
26. I rullegardinmenyen under hurtigfanen **Finanskontoer** velger du "Avhendingssvinn". Bruk de samme kontoene for Avhendingssalg og Avhendingssvinn.  
27. Klikk **Legg til**.
28. Angi eller velg en verdi i feltet **Tablå**.
29. Angi de ønskede verdiene i **Hovedkonto**-feltet. Du kan angi en motkonto for avhendinger eller la feltet stå tomt for å fylle det ut for den bestemte transaksjonen.  
30. Vis hurtigfanen **Avhending**. Du må definere posteringsprofiler for avhending for både både salg og svinn.  Vi starter med avhendingstransaksjoner for salg.  
31. Klikk **Legg til**.
32. Angi eller velg en verdi i feltet **Tablå**.
33. Velg "Anskaffelsesverdi" i feltet **Poster verdi**.
    * Anskaffelsesverdien håndterer justeringsverdier for anskaffelse og anskaffelsesjustering for alle år. Du kan også definere kontoer for disse transaksjonstypene separat.  
    * Du kan angi avhendingsprosessen til å bruke forskjellige kontoer avhengig av om salget resulterer i tap eller vinning. Jeg vil angi Salgsverditypen til "Alle" for å bruke de samme kontoene for alle typer avhendinger.  
34. Angi de ønskede verdiene i **Hovedkonto**-feltet.
35. Angi ønskede verdier i **Motkonto**-feltet.
36. Klikk **Legg til**.
37. Angi eller velg en verdi i feltet **Tablå**.
38. I **Poster verdi**-feltet velger du Avskrivning (foregående år).  
38. Angi de ønskede verdiene i **Hovedkonto**-feltet.
39. Angi ønskede verdier i **Motkonto**-feltet.
40. Klikk **Legg til**.
41. Angi eller velg en verdi i feltet **Tablå**.
42. I **Poster verdi**-feltet velger du "Avskrivning (inneværende år)".
43. Angi de ønskede verdiene i **Hovedkonto**-feltet.
44. Angi ønskede verdier i **Motkonto**-feltet.
45. Klikk **Legg til**.
46. Angi eller velg en verdi i feltet **Tablå**.
47. I **Poster verdi**-feltet velger du "Avskrivningsjusteringer (foregående år)".
48. Angi de ønskede verdiene i **Hovedkonto**-feltet.
49. Angi ønskede verdier i **Motkonto**-feltet.
50. Klikk **Legg til**.
51. Angi eller velg en verdi i feltet **Tablå**.
52. I **Poster verdi**-feltet velger du "Avskrivningsjusteringer (inneværende år)".
53. Angi de ønskede verdiene i **Hovedkonto**-feltet.
54. Angi ønskede verdier i **Motkonto**-feltet.
55. Klikk **Legg til**.
56. Angi eller velg en verdi i feltet **Tablå**.
57. Velg "Netto bokført verdi" i feltet **Poster verdi**.
58. Angi de ønskede verdiene i **Hovedkonto**-feltet.
59. Angi ønskede verdier i **Motkonto**-feltet.
60. Velg "Svinn" i feltet **Salg eller svinn**.
61. Klikk **Legg til**.
62. Angi eller velg en verdi i feltet **Tablå**.
63. Velg "Anskaffelsesverdi" i feltet **Poster verdi**.
64. Angi de ønskede verdiene i **Hovedkonto**-feltet.
65. Angi ønskede verdier i **Motkonto**-feltet.
66. Klikk **Legg til**.
67. Angi eller velg en verdi i feltet **Tablå**.
67. I **Poster verdi**-feltet velger du Avskrivning (foregående år).  
68. Angi de ønskede verdiene i **Hovedkonto**-feltet.
69. Angi ønskede verdier i **Motkonto**-feltet.
70. Klikk **Legg til**.
71. Angi eller velg en verdi i feltet **Tablå**.
72. I **Poster verdi**-feltet velger du "Avskrivning (inneværende år)".
73. Angi de ønskede verdiene i **Hovedkonto**-feltet.
74. Angi ønskede verdier i **Motkonto**-feltet.
75. Klikk **Legg til**.
76. Angi eller velg en verdi i feltet **Tablå**.
77. I **Poster verdi**-feltet velger du "Avskrivningsjusteringer (foregående år)".
78. Angi de ønskede verdiene i **Hovedkonto**-feltet.
79. Angi ønskede verdier i **Motkonto**-feltet.
80. Klikk **Legg til**.
81. Angi eller velg en verdi i feltet **Tablå**.
82. I **Poster verdi**-feltet velger du "Avskrivningsjusteringer (inneværende år)".
83. Angi de ønskede verdiene i **Hovedkonto**-feltet.
84. Angi ønskede verdier i **Motkonto**-feltet.
85. Klikk **Legg til**.
86. Angi eller velg en verdi i feltet **Tablå**.
87. Velg "Netto bokført verdi" i feltet **Poster verdi**.
88. Angi de ønskede verdiene i **Hovedkonto**-feltet.
89. Angi ønskede verdier i **Motkonto**-feltet.

