---
title: "Kostnadsoppføringer"
description: "Denne artikkelen inneholder informasjon om kostnadsoppføringer og når de opprettes. En kostnadsoppføring er en oppføring som registrerer antall og kostnad for en bestemt hendelse."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1045ecbf7080f12bc60336609180173544e4e0eb
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017

---

# <a name="cost-entries"></a>Kostnadsoppføringer

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder informasjon om kostnadsoppføringer og når de opprettes. En kostnadsoppføring er en oppføring som registrerer antall og kostnad for en bestemt hendelse.

Kostnadsoppføringer er aggregeringer av lagertransaksjoner som er registrert for aktive økonomiske lagerdimensjoner.

## <a name="examples"></a>Eksempler
### <a name="example-1-no-cost-entries-are-created"></a>Eksempel 1: Ingen kostnadsoppføringer opprettes

En overføringsjournalhendelse registreres. Hendelsen overfører ett stykk av vare A fra lokasjon A til lokasjon B. Lokasjonslagerdimensjonen regnes ikke som en del av kostnadsobjektet. Derfor oppretter hendelsen to lagertransaksjoner og ingen kostnadsoppføringer.

### <a name="example-2-cost-entries-are-created"></a>Eksempel 2: Kostnadsoppføringer opprettes

En overføringsjournalhendelse registreres. Hendelsen overfører ett stykk av vare A fra område 1 til område 2. Områdelagerdimensjonen regnes som en del av kostnadsobjektet. Derfor oppretter hendelsen to lagertransaksjoner og to kostnadsoppføringer.

### <a name="example-3-one-cost-entry-is-created"></a>Eksempel 3: Én kostnadsoppføring opprettes

En produktkvitteringshendelse registreres for en bestilling. Hendelsen registrerer 100 stykk av vare A med en enhetskostnad på NOK 100,00. Siden vare A bruker et serienummer til å spore formålet med lagerstyring, opprettes et unikt serienummer for hver vare som mottas. Derfor oppretter hendelsen 100 lagertransaksjoner og én kostnadsoppføring.

## <a name="cost-entries-page"></a>Kostnadsoppføringer-siden
Den nye **Kostnadsoppføringer**-siden lar deg vise og styre registrering av antall og kostnader. Denne siden kompletterer sidene **Lagertransaksjon** og **Lagerutligning**. Poster registreres i kronologisk rekkefølge for en hendelse. Derfor kan du raskt finne og styre de akkumulerte kostnadene for en bestemt hendelse eller alle hendelsene som er knyttet til et dokument. Her er et eksempel:

-   En produktkvitteringshendelse er registrert for vare A. 100 stykker mottas med en enhetskostnad på NOK 100,00.
-   Noen dager etter at fakturahendelsen er registrert, øker kostnadene til NOK 110,00. Derfor er totalbeløpet NOK 11 000. Det opprettes et andre bilag for å gjøre rede for differansen på NOK 1 000.
-   Noen dager senere registreres et tilleggsgebyr på NOK 150,00 på bestillingen for å dekke transportkostnadene.

| Bilag | Dato       | Referanse      | Tall | Parti-ID  | Antall | Beløp  |
|---------|------------|----------------|--------|---------|---------------|----|
| 00001   | 01.01.2015 | Bestilling | 100001 | 0000101 | 1 00,00   | 1000,00 |
| 00002   | 20.01.2015 | Bestilling | 100001 | 0000101 |          | 100,00  |
| 00003   | 31.01.2015 | Justering     | 100001 | 0000101 |          | 15,00   |

**Kostnadsoppføringer**-siden aktiverer filtrering etter dokument-ID og dokumentdato. 

> [!NOTE]
> Kostnadsoppføringer er bare tilgjengelige for [kostnadsobjekter](cost-object.md) eller frigitte produkter.

<a name="see-also"></a>Se også
--------

[Kostnadsobjekter](cost-object.md)



