---
title: Oversikt over livssyklus for produksjonsordre
description: Når en produksjonsordre opprettes, startes en forespørsel om å starte produksjonen av en vare. Produksjonsordren inneholder informasjon om hva som skal produseres, antallet som skal produseres og den planlagte sluttdatoen. Den inneholder også informasjon om hvilke materialer som skal brukes og prosessen som skal følges for å produsere varen.
author: johanhoffmann
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19741"
- intro-internal
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c4c3632d644070f064ec70d3dd7c0d480927eafe
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982883"
---
# <a name="production-order-lifecycle-overview"></a>Oversikt over livssyklus for produksjonsordre

[!include [banner](../includes/banner.md)]

Når en produksjonsordre opprettes, startes en forespørsel om å starte produksjonen av en vare. Produksjonsordren inneholder informasjon om hva som skal produseres, antallet som skal produseres og den planlagte sluttdatoen. Den inneholder også informasjon om hvilke materialer som skal brukes og prosessen som skal følges for å produsere varen.

En produksjonsordre går gjennom stadiene i livssyklusen til produksjonen. Når en ordre opprettes, tilordnes statusen **Opprettet**. Når en ordre avsluttes, tilordnes statusen **Avsluttet**. En parameterinnstilling i hvert trinn tillater en bruker å konfigurere hvert trinn. Innstillingen kan defineres for en enkeltbruker eller for alle brukere.

Produksjonsstykklisten og produksjonsruten er primærenhetene i produksjonsordren. De er kopiert til produksjonsordren basert på den valgte varen og antallet som skal produseres. Før produksjonsordren startes kan du redigere produksjonsstykklisten og ruten.

En produksjonsordre kan opprettes i følgende scenarier:

-   Opprettet av hovedplanleggingsutførelse basert på materialbehov.
-   Opprettet direkte fra en salgsordrelinje eller når en overordnet produksjonsordre er opprettet og estimert (tilknyttet forsyning).
-   Opprettet manuelt.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]