---
title: Mottak av kombinerte skiltnumre
description: "Dette emnet beskriver hvordan du bruker mottak av kombinerte skiltnumre til å registrere og opprette arbeid for flere varer med en mobilenhet."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0e785d71e7ae3c5f60d36d8b190001b5e356c626
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="mixed-license-plate-receiving"></a>Mottak av kombinerte skiltnumre

[!include[banner](../includes/banner.md)]

Med mottak av kombinerte nummerskilt kan du bygge et nummerskiltsom  består av flere varer før du kan registrere og opprette plasseringsarbeid. 

Et nummerskilt som består av flere varer trenger ikke deles i mottakssonenf or at du skal kunne registrere av hver vare. 

Når du bruker en varerelaterte flyt til å identifisere kildedokumentlinjene, kan du skanne strekkoder på varekontrollen. Varen og antallet vil automatisk bli lagt til i det kombinerte nummerskiltet hvis strekkoden har et konfigurert antall og en enhet (åleenhet), og du kommer tilbake til skjermbildet til å skanne en annen vare. Dermed kan du raskt skanne alle varene uten å måtte bekrefte for hvert trinn. 

I flyten for mottak av kombinerte skiltnumre kan du vise listen over varer som allerede er skannet for nummerskiltet, og herfra kan du endre eller korrigere antallet for en vare.

## <a name="where-it-applies"></a>Der det er aktuelt

Mottak av kombinerte skiltnumre er en mottaksflyt i en mobilenhet for å registrere og opprette arbeid for flere linjer/varer samtidig. Dette er nyttig hvis du mottar innkommende nummerskilt med flere varer. 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a>Slik definerer du mottak av kombinerte skiltnumre
Mottak av kombinerte skiltnumre defineres som et menyelement i en mobilenhet.

Du må opprette et nytt menyelement med modus for arbeid som ikke bruker eksisterende arbeid, og som bruker en av følgende metoder:

- Mottak av kombinerte skiltnumre
- Mottak og plassering av kombinerte skiltnumre

Alternativene for å identifisere kildedokumentlinjene er bestillingsvare, bestillingslinje, returordre, overføringsordrevare og overføringsordrelinje. Disse alternativene kan endre mottaksordren på et enkelt nummerskilt. Det siste alternativet er etter lastvare. Du kan legge til flere elementer i et nummerskilt, men du kan ikke bytte mellom flere laster.

