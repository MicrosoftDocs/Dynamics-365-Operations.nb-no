---
title: Rapportere produksjonsordre som ferdigstilt
description: Rapportere som ferdigstilt er et produksjonsstadium. På dette stadiet blir et ferdigstilt produkt rapportert og flyttet fra produksjonsordren til lageret.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 61c12ee3a831abcb46af18645eba55fe100c99c9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567404"
---
# <a name="report-production-orders-as-finished"></a>Rapportere produksjonsordre som ferdigstilt

[!include [banner](../includes/banner.md)]

Rapportere som ferdigstilt er et produksjonsstadium. På dette stadiet blir et ferdigstilt produkt rapportert og flyttet fra produksjonsordren til lageret.

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



