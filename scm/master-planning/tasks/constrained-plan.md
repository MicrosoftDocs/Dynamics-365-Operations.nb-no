--- 
title: Generere en begrenset plan
description: "Denne fremgangsmåten viser hvordan du oppretter en plan som tar hensyn til både material- og kapasitetsbegrensninger."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 6735f0287e7a61ff494a48c97c44480c6038097c
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="generate-a-constrained-plan"></a>Generere en begrenset plan

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en plan som tar hensyn til både material- og kapasitetsbegrensninger. Planen sikrer at produksjonen ikke starter før materialer er tilgjengelige og ressurser er ikke overbestilt. 

Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne fremgangsmåten er ment for produksjonsplanleggeren.


## <a name="set-up-a-constrained-plan"></a>Definere en begrenset plan
1. Klikk Hovedplanlegging.
2. Klikk Hovedplaner.
3. Finn og velg ønsket post i listen.
    * Eksempel: Statisk plan  
4. Velg Ja i Begrenset kapasitet-feltet.
5. Angi 30 i feltet Begrenset kapasitet.
6. Utvid horisontene i dager-delen.
7. Velg Ja i Kapasitet-feltet.
8. Angi et tall i feltet Kapasitetsplanleggingshorisont (dager).
    * Eksempel: 60  
9. Velg Ja i feltet Beregnede forsinkelser.
10. Angi et tall i feltet Beregn forsinkelseshorisont (dager).
    * Eksempel: 60  
11. Utvid delen Beregnede forsinkelser.
12. Velg Ja i feltet Legg til den beregnede forsinkelsen i behovsdatoen.
13. Velg Ja i feltet Legg til den beregnede forsinkelsen i behovsdatoen.
14. Velg Ja i feltet Legg til den beregnede forsinkelsen i behovsdatoen.
15. Lukk siden.

## <a name="create-a-constrained-plan"></a>Opprette en begrenset plan
1. Klikk Kjør.
2. Angi eller velg en verdi i Hovedplan-feltet.
    * Velg planen som du har definert begrensninger for.  
3. Klikk OK.
    * Dette kan ta en stund.  
4. Klikk Planlagte bestillinger.


