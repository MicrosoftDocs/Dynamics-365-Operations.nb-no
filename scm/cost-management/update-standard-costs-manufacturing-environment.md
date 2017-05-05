---
title: "Oppdatere standard kostpris i et produksjonsmiljø"
description: "Denne artikkelen gir veiledning for hvordan du kan oppdatere standardkostnader i et produksjonsmiljø."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9a7199b62ea0037e709da983b6fd53aaadeca4ad
ms.lasthandoff: 03/31/2017


---

# <a name="update-standard-costs-in-a-manufacturing-environment"></a>Oppdatere standard kostpris i et produksjonsmiljø

[!include[banner](../includes/banner.md)]


Denne artikkelen gir veiledning for hvordan du kan oppdatere standardkostnader i et produksjonsmiljø. 

Oppdateringer kan gjenspeile nye varer, kostnadskategorier eller formler for beregning av indirekte kostnader. De kan også gjenspeile korrigeringer og kostnadsendringer. Typen oppdatering påvirker trinnene som må fullføres for å oppdatere standard kostpris, som vist i følgende tilfeller:

-   Angi forventede endringer i standard kostpris for innkjøpte varer, og endre deretter status for varekostnadspostene til **Aktive** på den aktuelle datoen. Du må imidlertid ikke omberegne kostnadene for produserte varer som bruker de innkjøpte varene.
-   Angi standard kostpris for en nyinnkjøpt vare, men ikke omberegn kostnadene for produserte varer som har en stykklisteversjon som har den nyinnkjøpte varen som komponent.
-   Rett opp eller endre kostprisen for en innkjøpt vare, eller endre kostgruppen som er tilordnet en innkjøpt vare, og beregn kostnadene for alle produserte varer som har en stykklisteversjon som har den innkjøpte varen som komponent.
-   Endre kostprisen for en kostnadskategori, og beregn kostnadene for alle produserte varer som har en ruteversjon som inneholder rutingoperasjoner som bruker kostnadskategorien.
-   Endre kostnadskategoriene som er tilordnet til ruteoperasjoner eller kostgruppen som er tilordnet kostnadskategorier. Beregn deretter kostnadene for alle produserte varer som har en ruteversjon som inneholder rutingoperasjoner som bruker kostnadskategorien.
-   Endre en beregningsformel for indirekte kostnader, og beregn kostnadene for alle produserte varer som påvirkes av endringen.
-   Endre eller legg til et produksjonsanlegg for en produsert vare, og beregn varens produserte kostpris for anlegget.
-   Beregn, eller omberegn, kostnadene for en produsert vare, og omberegn kostnadene for alle produserte varer som har en stykklisteversjon som har den produserte varen som komponent.
-   Beregn kostnadene for en nyprodusert vare på grunnlag av den definerte, godkjente og aktive stykklisten og ruteinformasjonen.

Hvert tilfelle krever nøye overveielse om hvordan standard kostpris skal oppdateres.



