---
title: "Kostnadsoppføringer"
description: "Denne artikkelen inneholder informasjon om kostnadsoppføringer og når de opprettes. En kostnadsoppføring er en oppføring som registrerer antall og kostnad for en bestemt hendelse."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 55f5ee731c40acc40e8fe20c24d4ed707fe2c81a
ms.lasthandoff: 03/31/2017


---

# <a name="cost-entries"></a>Kostnadsoppføringer

Denne artikkelen inneholder informasjon om kostnadsoppføringer og når de opprettes. En kostnadsoppføring er en oppføring som registrerer antall og kostnad for en bestemt hendelse.

Kostnadsoppføringer er aggregeringer av lagertransaksjoner som er registrert for aktive økonomiske lagerdimensjoner.

## <a name="examples"></a>Eksempler
### <a name="example-1-no-cost-entries-are-created"></a>Eksempel 1: Ingen kostnadsoppføringer opprettes

En overføringsjournalhendelse registreres. Hendelsen overfører ett stykk av vare A fra lokasjon A til lokasjon B. Lokasjonslagerdimensjonen regnes ikke som en del av kostnadsobjektet. Derfor oppretter hendelsen to lagertransaksjoner og ingen kostnadsoppføringer.

### <a name="example-2-cost-entries-are-created"></a>Eksempel 2: Kostnadsoppføringer opprettes

En overføringsjournalhendelse registreres. Hendelsen overfører ett stykk av vare A fra området 1 til 2-området. Områdedimensjonen er en del av kostobjektet. Derfor oppretter hendelsen to lagertransaksjoner og to kostnadsoppføringer.

### <a name="example-3-one-cost-entry-is-created"></a>Eksempel 3: Én kostnadsoppføring opprettes

En produktkvitteringshendelse registreres for en bestilling. Hendelsen registrerer 100 stykk av vare A med en enhetskostnad på NOK 100,00. Siden vare A bruker et serienummer til å spore formålet med lagerstyring, opprettes et unikt serienummer for hver vare som mottas. Derfor oppretter hendelsen 100 lagertransaksjoner og én kostnadsoppføring.

## <a name="cost-entries-page"></a>Kostnadsoppføringer-siden
Den nye **Kostnadsoppføringer**-siden lar deg vise og styre registrering av antall og kostnader. Denne siden kompletterer sidene **Lagertransaksjon** og **Lagerutligning**. Poster registreres i kronologisk rekkefølge for en hendelse. Derfor kan du raskt finne og styre de akkumulerte kostnadene for en bestemt hendelse eller alle hendelsene som er knyttet til et dokument. Her er et eksempel:

-   En produktkvitteringshendelse er registrert for vare A. 100 stykker mottas med en enhetskostnad på NOK 100,00.
-   Noen dager etter at fakturahendelsen er registrert, øker kostnadene til NOK 110,00. Derfor er totalbeløpet NOK 11 000. Det opprettes et andre bilag for å gjøre rede for differansen på NOK 1 000.
-   Noen dager senere registreres et tilleggsgebyr på NOK 150,00 på bestillingen for å dekke transportkostnadene.

| Bilag | Dato       | Referanse      | Nummer | Parti-ID  | Referanseparti | Returparti-ID | Antall | Beløp  |
|---------|------------|----------------|--------|---------|---------------|---------------|----------|---------|
| 00001   | 01.01.2015 | Bestilling | 100001 | 0000101 |               |               | 1 00,00   | 1000,00 |
| 00002   | 20.01.2015 | Bestilling | 100001 | 0000101 |               |               |          | 100,00  |
| 00003   | 31.01.2015 | Justering     | 100001 | 0000101 |               |               |          | 15,00   |

**Kostnadsoppføringer**-siden aktiverer filtrering etter dokument-ID og dokumentdato. **Merk:** kostposter er bare tilgjengelige for [kostsentre](cost-object.md) eller frigitte produkter.

<a name="see-also"></a>Se også
--------

[Cost objects](cost-object.md)


