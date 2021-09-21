---
title: Frigivelsesprosess for planleggingsoptimalisering og utgivelseslogg
description: Dette emnet inneholder informasjon om utgivelsesprosessen og utgivelsesloggen for planleggingsoptimalisering.
author: crytt
ms.date: 09/02/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d0f7a9f59d1034451c5c2dec1150c017bda27ad4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474706"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Frigivelsesprosess for planleggingsoptimalisering og utgivelseslogg

[!include [banner](../../includes/banner.md)]

Microsoft oppdaterer planleggingsoptimalisering månedlig. Basert på forretningskrav gir vi imidlertid av og til ut flere oppdateringer mellom de planlagte utgivelsene.

Hver utgivelse publiseres i de enkelte områdene der planleggingsoptimalisering er tilgjengelig. Prosessen tar vanligvis tre dager.

Mens planleggingsoptimalisering oppdateres, kan hovedplanleggingen kjøre litt saktere enn vanlig.

Miljøer som bruker planleggingsoptimalisering, mottar automatisk den nyeste versjonen. Ingen brukerhandling er nødvendig: Tjenesten oppdateres automatisk. Ingen endringsfunksjonalitet skyves imidlertid automatisk til miljøer. Endringer som anses som brudd, deaktiveres som standard og må aktiveres eksplisitt ved hjelp av [funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Derfor vises ikke disse endringene i miljøer før du velger å aktivere dem.

Siden varslinger ikke vises når planleggingsoptimalisering oppdateres i miljøet ditt, kan du se gjennom produktmerknadene i tabellen nedenfor for å finne ut når endringene ble utgitt, og hvilken funksjonalitet de introduserte. Denne tabellen viser endringene som ble utgitt for planleggingsoptimalisering, om disse endringene er knyttet til en funksjon fra funksjonsbehandling og datoen for utgivelsen.

| Endringer | Detaljer for funksjonsbehandling | Frigivelsesdatoer |
|---|---|---|
| Generelle ytelses-, kvalitets- og stabilitetsforbedringer. | Ingen funksjonsbehandling er nødvendig. | 25.–30. august 2021 |
| <p>La til feltet **Leveringstid** i planlagte bestillinger.</p><p>Generelle ytelses-, kvalitets- og stabilitetsforbedringer.</p> | Ingen funksjonsbehandling er nødvendig. | 12.–17. august 2021 |
| <p>La til ressurstypekrav for uendelig kapasitetsplanlegging.</p><p>Forbedret ressurseffektivitet og kalendereffektivitet for uendelig kapasitetsplanlegging.</p><p>Hvis du vil ha mer informasjon, kan du se [Planlegge med uendelig kapasitet](infinite-capacity-planning.md). | <p>Tilgjengelig i funksjonsbehandling fra og med versjon 10.0.20.</p><p>Funksjonsnavn: *Uendelig kapasitetsplanlegging for Planleggingsoptimalisering*</p> | 6.–12. juli 2021 |
| Generelle kvalitetsforbedringer. | Ingen funksjonsbehandling er nødvendig. | 6.–12. juli 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
