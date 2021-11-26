---
title: Frigivelsesprosess for planleggingsoptimalisering og utgivelseslogg
description: Dette emnet inneholder informasjon om utgivelsesprosessen og utgivelsesloggen for planleggingsoptimalisering.
author: ChristianRytt
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b2e0145c28b40f4fbfb54ad7e7ed32fbc130c569
ms.sourcegitcommit: 8afd0cdb39ec443fb7631c39401967cce0fac34e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727438"
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
| <p>Ekstra støtte for beregningsformler for prosesstid, produksjonsrute med overlapping og operasjonsnummer for produksjon på behovstransaksjoner.</p><p>Utvidede feilmeldinger for produksjonsplanlegging relatert til tidsavbrudd, kapasitet kan ikke blir funnet og rutekort.</p><p>Forbedret konsistens ved beregning av mottaksdatoer og avgangsdatoer på både planlagte ordrer og autoriserte ordrer.</p><p>Generelle ytelses-, kvalitets- og stabilitetsforbedringer. | Funksjonsnavn: *Uendelig kapasitetsplanlegging for Planleggingsoptimalisering* | 22. til 27. oktober 2021 |
| <p>Lagt til støtte for å vurdere svinnprosent i behandlingstidsberegningen.</p><p>Lagt til støtte for bruk av operasjonsnummer og materialer under planlegging. | Funksjonsnavn: *Uendelig kapasitetsplanlegging for Planleggingsoptimalisering* | 5. til 7. oktober 2021 |
| <p>Lagt til støtte for jobbtyper for produksjonsrute: **Kø før**, **Kø etter** og **Transporttid**.</p><p>Generelle ytelses-, kvalitets- og stabilitetsforbedringer. | Funksjonsnavn: *Uendelig kapasitetsplanlegging for Planleggingsoptimalisering* | 25. til 30. september 2021 |
| <p>Lagt til støtte for hovedplaner med **Planleggingsmetode** satt til *Grovplanlegging*.</p><p>På **Rutegrupper**-siden overholder du innstillingene for avmerkingsboksene **Aktivering**, **Driftstid** og **Kapasitet** for rader med **Rute-/jobbtype** *Oppsett* eller *Prosess*. </p><p>Generelle ytelses-, kvalitets- og stabilitetsforbedringer. | <p>Grovplanlegging er tilgjengelig i funksjonsbehandling fra og med versjon 10.0.20.</p><p>Funksjonsnavn: *Uendelig kapasitetsplanlegging for Planleggingsoptimalisering*</p>  | 9.-17. september 2021 |
| Generelle ytelses-, kvalitets- og stabilitetsforbedringer. | Ingen funksjonsbehandling er nødvendig. | 25.–30. august 2021 |
| <p>La til feltet **Leveringstid** i planlagte bestillinger.</p><p>Generelle ytelses-, kvalitets- og stabilitetsforbedringer.</p> | Ingen funksjonsbehandling er nødvendig. | 12.–17. august 2021 |
| <p>La til ressurstypekrav for uendelig kapasitetsplanlegging.</p><p>Forbedret ressurseffektivitet og kalendereffektivitet for uendelig kapasitetsplanlegging.</p><p>Hvis du vil ha mer informasjon, kan du se [Planlegge med uendelig kapasitet](infinite-capacity-planning.md). | <p>Tilgjengelig i funksjonsbehandling fra og med versjon 10.0.20.</p><p>Funksjonsnavn: *Uendelig kapasitetsplanlegging for Planleggingsoptimalisering*</p> | 6.–12. juli 2021 |
| Generelle kvalitetsforbedringer. | Ingen funksjonsbehandling er nødvendig. | 6.–12. juli 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
