---
title: Vis resultater for automatisering av leverandørfakturaer (forhåndsversjon)
description: Denne artikkelen forklarer hvordan du viser statusen for leverandørfakturaer som er i den automatiserte prosessen for sending til arbeidsflyt.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: dd9b74d2ed34399aff455563504c296a5a25a874
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895174"
---
# <a name="view-vendor-invoice-automation-results"></a>Vise resultater for automatisering av leverandørfaktura

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du viser statusen for leverandørfakturaer som er i den automatiserte prosessen for sending til arbeidsflyt. Detaljer om automatiseringsloggen vedlikeholdes for hver importerte leverandørfaktura. Avhengig av forretningsprosessene du har automatisert, vises siden **Ventende leverandørfakturaer** verdiene **Status for automatisert kvitteringssamsvar** og **Status for automatisert send til arbeidsflyt**. Du kan vise detaljene og lage en plan for å fokusere på fakturaene som mislyktes på et automatisk trinn. Etter at du har rettet problemet, kan du gjenoppta den automatiserte prosessen for den importerte fakturaen.

Før du kan redigere en faktura som er sendt, må du stoppe den automatiserte behandlingen midlertidig. Hvis en faktura i den automatiserte prosessen for sending til arbeidsflyt er stoppet midlertidig, setter du feltet **Inkluder i automatisert behandling** til **Nei** på siden **Leverandørfakturaer**. Automatisering vil da ikke kjøre før **Inkluder i automatisert behandling** er satt til **Ja**. En faktura kan stoppes midlertidig fra ytterligere automatisering hvis den ennå ikke er i arbeidsflytsystemet og ikke brukes av den automatiserte prosessen.

Hvis den importerte fakturaen er underlagt prosessen for sending til arbeidsflyt, kan du vise verdien **Status for automatisering** på siden **Leverandørfakturaer**. Følgende statuser spores:

- **Inkludert** – De automatiserte prosessene som er definert på siden **Leverandørparametere**, kjører på riktig måte, men er ennå ikke fullført.
- **Stoppet midlertidig** – De automatiserte prosessene som er definert på siden **Leverandørparametere**, er kjørt, men minst ett trinn i prosessen mislyktes. Statusen **Stoppet midlertidig** brukes også hvis feltet **Inkluder i automatisert behandling** er satt til **Nei**. Du kan se feilene ved å velge **Vis de siste resultatene**.
- **I arbeidsflyt** – Den importerte fakturaen er sendt til arbeidsflytsystemet, enten av den automatiserte prosessen for sending til arbeidsflyt eller manuelt.
- **Arbeidsflyt fullført** – Arbeidsflytprosessen er fullført for den importerte fakturaen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
