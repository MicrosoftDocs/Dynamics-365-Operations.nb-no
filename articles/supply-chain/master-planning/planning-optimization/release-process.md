---
title: Frigivelsesprosess for planleggingsoptimalisering og utgivelseslogg
description: Dette emnet inneholder informasjon om utgivelsesprosessen og utgivelsesloggen for planleggingsoptimalisering.
author: crytt
ms.date: 8/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fcd18341629afcf3092a457ae711e27b0bbfeb2a
ms.sourcegitcommit: 03f53980a4bc67b73ac2be76a3b3e7331d0db705
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/18/2021
ms.locfileid: "7394423"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Frigivelsesprosess for planleggingsoptimalisering og utgivelseslogg

[!include [banner](../../includes/banner.md)]

Microsoft oppdaterer planleggingsoptimalisering månedlig. Basert på forretningskrav gir vi imidlertid av og til ut flere oppdateringer mellom de planlagte utgivelsene.

Hver utgivelse publiseres i de enkelte områdene der planleggingsoptimalisering er tilgjengelig. Prosessen tar vanligvis tre dager.

Mens planleggingsoptimalisering oppdateres, kan hovedplanleggingen kjøre litt saktere enn vanlig.

Miljøer som bruker planleggingsoptimalisering, mottar automatisk den nyeste versjonen. Ingen brukerhandling er nødvendig: Tjenesten oppdateres automatisk. Ingen endringsfunksjonalitet skyves imidlertid automatisk til miljøer. Endringer som anses som brudd, deaktiveres som standard og må aktiveres eksplisitt ved hjelp av [funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Derfor vises ikke disse endringene i miljøer før du velger å aktivere dem.

Siden varslinger ikke vises når planleggingsoptimalisering oppdateres i miljøet ditt, kan du se gjennom produktmerknadene i tabellen nedenfor for å finne ut når endringene ble utgitt, og hvilken funksjonalitet de introduserte. Denne tabellen viser endringene som ble utgitt for planleggingsoptimalisering, om disse endringene er knyttet til en funksjon fra funksjonsbehandling og datoen for utgivelsen.

| Endringer | Detaljer for funksjonsbehandling | Frigivelsesdato |
|---|---|---|
| <p>La til feltet **Leveringstid** i planlagte bestillinger.</p><p>Generelle ytelses-, kvalitets- og stabilitetsforbedringer.</p> | Ingen funksjonsbehandling er nødvendig. | 16. august 2021 |
| <p>La til ressurstypekrav for uendelig kapasitetsplanlegging.</p><p>Forbedret ressurseffektivitet og kalendereffektivitet for uendelig kapasitetsplanlegging.</p><p>Hvis du vil ha mer informasjon, kan du se [Planlegge med uendelig kapasitet](infinite-capacity-planning.md). | <p>Tilgjengelig i funksjonsbehandling fra og med versjon 10.0.20.</p><p>Funksjonsnavn: *Uendelig kapasitetsplanlegging for Planleggingsoptimalisering*</p> | 6. juli 2021 |
| Generelle kvalitetsforbedringer. | Ingen funksjonsbehandling er nødvendig. | 6. juli 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
