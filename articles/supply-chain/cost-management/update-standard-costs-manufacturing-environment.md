---
title: Oppdatere standard kostpris i et produksjonsmiljø
description: Denne artikkelen gir veiledning for hvordan du kan oppdatere standardkostnader i et produksjonsmiljø.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66d08888e426c55fc775a1f2505772bca45e7802
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842135"
---
# <a name="update-standard-costs-in-a-manufacturing-environment"></a>Oppdatere standard kostpris i et produksjonsmiljø

[!include [banner](../includes/banner.md)]

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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]