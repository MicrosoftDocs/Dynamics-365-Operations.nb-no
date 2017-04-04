---
title: Rapportere produksjonsordrer som ferdigmeldt
description: "Ferdigmelding er et trinn i produksjonen. På dette stadiet, er et ferdig produkt rapportert og flyttet fra produksjonsordren til lageret."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 19a777a8e58e3c8b848e878956b457a4a730f6e2
ms.lasthandoff: 03/31/2017


---

# <a name="report-production-orders-as-finished"></a>Rapportere produksjonsordrer som ferdigmeldt

Ferdigmelding er et trinn i produksjonen. På dette stadiet, er et ferdig produkt rapportert og flyttet fra produksjonsordren til lageret.

Når et antall av ferdigvarene rapporteres som ferdig i en produksjonsordre, oppdateres antallet som beholdning på lageret. Delvise antall for det opprinnelig planlagte ordreantallet kan rapporteres som fullført. Det er også mulig å rapportere antall feil med en tilknyttet feilårsak når antall rapporteres som ferdig. Når produksjonsordren når stadiet Ferdigmeldt, angir det at ingen flere antall skal rapporteres for produksjonsordren.
Følgende kjennetegn er også knyttet til **Rapporter som fullført**-prosessen:
-   Det er mulig å definere forbruk av råvarer og tiden som er proporsjonal med rapportert antall (rensing)
-   Plasseringsarbeid kan genereres for varer som er aktivert for lagerprosesser.
-   Planlagt eller standard kostverdi for de ferdige varene kan defineres for å bli rapportert til finanskontoer.
-   En kvalitetsordre kan opprettes for det rapporterte antallet basert på oppsettet for en kvalitetstilknytning.

Antallet rapporteres til utleveringsstedet. Lagerarbeid blir deretter generert for å flytte antallet fra utleveringsstedet til det endelige målet som er definert av lokasjonsdirektivet for plasseringsarbeidet.

-   En kvalitetsordre kan opprettes når en produksjonsordre er rapportert som fullført, hvis en kvalitetstilknytning er definert.

## <a name="set-a-production-order-to-reporting-as-finished"></a>Angi en produksjonsordre som Ferdigmelding
Du kan sette en produksjonsordre til **Ferdigmeld** ved hjelp av standard oppdateringsfunksjonen for produksjonsordre eller via rute- og jobbkortjournaler eller via journalen **Ferdigmeld**. Du kan også oppdatere stadiet til **Ferdigmeld** via sidene for jobbkortterminalen og jobbkortenheten når du rapporterer om den siste jobben i produksjonsordren. Til slutt kan du aktivere alternativet **Ferdigmeld** som en prosess for den håndholdte lagerenhetsløsningen.  


