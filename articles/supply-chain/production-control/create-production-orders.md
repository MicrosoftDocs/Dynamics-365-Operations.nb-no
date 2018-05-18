---
title: Opprett produksjonsordrer
description: "Når en produksjonsordre opprettes, startes en forespørsel om å starte produksjonen av en vare. Produksjonsordren inneholder informasjon om hva som skal produseres, antallet som skal produseres og den planlagte sluttdatoen. Den inneholder også informasjon om hvilke materialer som skal brukes og prosessen som skal følges for å produsere varen."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d962dbf5a5a4e3847252171d3631f78341640bc7
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="create-production-orders"></a>Opprett produksjonsordrer

[!include [banner](../includes/banner.md)]

Når en produksjonsordre opprettes, startes en forespørsel om å starte produksjonen av en vare. Produksjonsordren inneholder informasjon om hva som skal produseres, antallet som skal produseres og den planlagte sluttdatoen. Den inneholder også informasjon om hvilke materialer som skal brukes og prosessen som skal følges for å produsere varen.

En produksjonsordre går gjennom stadiene i livssyklusen til produksjonen. Når en ordre opprettes, tilordnes statusen **Opprettet**. Når en ordre avsluttes, tilordnes statusen **Avsluttet**. En parameterinnstilling i hvert trinn tillater en bruker å konfigurere hvert trinn. Innstillingen kan defineres for en enkeltbruker eller for alle brukere.

Produksjonsstykklisten og produksjonsruten er primærenhetene i produksjonsordren. De er kopiert til produksjonsordren basert på den valgte varen og antallet som skal produseres. Før produksjonsordren startes kan du redigere produksjonsstykklisten og ruten.

En produksjonsordre kan opprettes i følgende scenarier:

-   Opprettet av hovedplanleggingsutførelse basert på materialbehov.
-   Opprettet direkte fra en salgsordrelinje eller når en overordnet produksjonsordre er opprettet og estimert (tilknyttet forsyning).
-   Opprettet manuelt.





