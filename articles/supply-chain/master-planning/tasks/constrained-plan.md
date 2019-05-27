---
title: Generere en begrenset plan
description: Denne fremgangsmåten viser hvordan du oppretter en plan som tar hensyn til både material- og kapasitetsbegrensninger.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e2265f7788fd2a4a37f6fb96d7562649dbc5b1c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556029"
---
# <a name="generate-a-constrained-plan"></a>Generere en begrenset plan

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

