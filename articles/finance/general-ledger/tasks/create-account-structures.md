---
title: Opprette kontostrukturer
description: Denne oppgaveveiledningen går gjennom oppretting av en kontostruktur.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed8ce37ab642277ff843e6320a880fac40d41acb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235795"
---
# <a name="create-account-structures"></a>Opprette kontostrukturer

[!include [banner](../../includes/banner.md)]

Denne oppgaveveiledningen går gjennom oppretting av en kontostruktur. Trinnene bruker demonstrasjonsdatafirmaet USMF.

1. Gå til **Navigasjonsrute > Moduler > Økonomimodul > Kontoplan > Strukturer > Konfigurer kontostrukturer**.
2. Klikk **Ny** i **handlingsruten** for å åpne dialogboksen for rullegardinlisten.
3. Skriv inn et navn som beskriver formålet med kontostrukturen i feltet **Kontostruktur**.
4. Skriv inn en beskrivelse for å angi formålet med kontostrukturen i feltet **Beskrivelse**.
5. Klikk **Opprett**.
6. I **Segmenter og tillatte verdier** klikker du **Legg til segment**.
7. Velg dimensjonen som skal legges til kontostrukturen i Dimensjoner-listen.
8. Klikk **Legg til segment** på slutten av listen.
9. Gjenta trinn 6 til 9 etter behov.
10. Velg segmentet for å redigere de tillatte verdiene i delen **Tillatte verdidetaljer**.
    Klikk for eksempel i **Hovedkonto**-feltet.  
11. Velg et alternativ, for eksempel er mellom og inkluderer i **Operator**-feltet.
12. Skriv inn en verdi i **Verdi**-feltet. For eksempel 600000.  
13. Skriv inn en verdi i feltet **via**. For eksempel 699999.  
14. I delen **Tillatte verdidetaljer** klikker du **Bruk**.
15. Gjenta trinn 10 til 15 etter behov.  
16. I delen **Tillatte verdidetaljer** klikker du **Legg til nye kriterier**.
17. Velg et alternativ, for eksempel er mellom og inkluderer i Operator-feltet.
18. Skriv inn en verdi i **Verdi**-feltet. For eksempel 033.  
19. Skriv inn en verdi i feltet **via**. For eksempel 034.  
20. Klikk **Bruk**.
21. Velg segmentet for å redigere de tillatte verdiene i rutenettet. For eksempel kostsenter  
22. Skriv inn en verdi i **CostCenter**-feltet. For eksempel 007..021.  
23. I **Segmenter og tillatte verdier** klikker du **Legg til**.
24. Skriv inn en verdi i **MainAccount**-feltet. For eksempel 600000..699999  
25. Velg segmentet for å redigere de tillatte verdiene i rutenettet. For eksempel Avdeling.  
26. Skriv inn en verdi i feltet Avdeling. For eksempel 032.  
27. Skriv inn en verdi i feltet CostCenter. For eksempel 086.  
28. Klikk **Valider** i **handlingsruten**.
29. Klikk **Aktiver** i **handlingsruten**.
30. Klikk **Aktiver**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]