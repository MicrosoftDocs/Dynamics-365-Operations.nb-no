---
title: Kom i gang med planleggingsoptimalisering
description: Dette emnet forklarer hvordan du begynner å bruke funksjonen for planleggingsoptimalisering.
author: ChristianRytt
manager: AnnBe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 3e64699005387adcc92e2e7c9fefad68a9de85c0
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076138"
---
# <a name="get-started-with-planning-optimization"></a>Kom i gang med planleggingsoptimalisering

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Planleggingsoptimaliseringsfunksjonaliteten støtter for øyeblikket ikke alle funksjonene som er tilgjengelige i planleggingsmotoren som er innebygd i Microsoft Dynamics 365 Supply Chain Management. Det er derfor viktig at du vurderer om funksjonssettet som for øyeblikket er tilgjengelig i planleggingsoptimalisering, oppfyller kravene dine. Som standard er ikke planleggingsoptimaliseringsfunksjonaliteten aktivert i Dynamics Lifecycle Services (LCS). Du har derfor mulighet til å gjennomføre evalueringen før den er slått på.

Til slutt erstatter planleggingsoptimalisering den eksisterende innebygde planleggingsmotoren Supply Chain Management.

Før du slår på planleggingsoptimalisering, anbefaler vi på det sterkeste at du evaluerer resultatene i tilpassingsanalysen av planleggingsoptimalisering. Hvis du vil ha mer informasjon, se [Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md).

### <a name="licensing"></a>Lisensiering

Hvis du kan kjøre hovedplanlegging ved hjelp av den gjeldende lisensen, trenger du ikke kjøpe en tilleggslisens for å bruke planleggingsoptimalisering.

### <a name="install-the-add-in"></a>Installer tillegget

Hvis du vil bruke planleggingsoptimalisering, må du installere tillegget for planleggingsoptimalisering for Dynamics 365 Supply Chain Management. Du får tilgang til tillegget fra LCS-prosjektet og kan aktivere funksjonaliteten for planleggingsoptimalisering fra brukergrensesnittet for Supply Chain Management.

> [!NOTE]
> Kravet for planleggingsoptimalisering er et LCS-aktivert miljø med høy tilgjengelighet (ikke et OneBox-miljø), med Dynamics 365 Supply Chain Management versjon 10.0.7 eller senere.

1. Logg på LCS, og åpne ønsket miljø.
1. Gå til **Detaljerte opplysninger**.
1. Bla ned til **Miljøtillegg**-hurtigfanen.
1. Velg **Installer et nytt tillegg**.
1. Velg **Planleggingsoptimalisering**.
1. Følg installasjonsveiledningen, og godta vilkårene.
1. Velg **Installer**.
1. I **Miljøtillegg**-hurtigfanen skal du se at planleggingsoptimalisering installeres.
1. Etter noen minutter skal **Installerer** endres til **Installert** (det er mulig at du må oppdatere siden). Når installasjonen er fullført, er du klar til å aktivere planleggingsoptimalisering i Dynamics 365 Supply Chain Management.

### <a name="planning-optimization-integration"></a>Integrering av planleggingsoptimalisering

Hvis du vil konfigurere om planleggingsoptimaliserings-tillegget skal brukes til hovedplanlegging, går du til **Hovedplanlegging** \> **Oppsett** \> **Parametere for planleggingsoptimalisering**.

#### <a name="connection-status"></a>Tilkoblingsstatus

Tilkoblingsstatusen angir gjeldende status for tilkoblingen mellom Supply Chain Management og planleggingsoptimaliseringstjenesten. Tabellen nedenfor viser mulige verdier.

| Tilkoblingsstatus | Beskrivelse | Kan planleggingsoptimalisering brukes? |
|---|---|---|
| Tilkoblet | Det er opprettet en forbindelse mellom planleggingsoptimaliseringstjenesten og Supply Chain Management. | Ja |
| Aktiverer tilkobling | En forespørsel om å aktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår. | Nei |
| Frakoblet | Det er ingen forbindelse til planleggingsoptimaliseringstjenesten. Tilkoblingen kan aktiveres fra LCS, som beskrevet tidligere i dette emnet. | Nei |
| Deaktiverer tilkobling | En forespørsel om å deaktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår. | Nei |
| Henter status | Systemet venter på statusinformasjon fra planleggingsoptimaliseringstjenesten. | Nei |

#### <a name="the-use-planning-optimization-option"></a>Alternativet Bruk planleggingsoptimalisering

Innstillingen for alternativet **Bruk planleggingsoptimalisering** bestemmer hvilken planleggingsmotor som skal brukes til hovedplanlegging:

- **Ja** – planleggingsoptimalisering brukes til hovedplanlegging.
- **Nei** – den innebygde planleggingsmotoren Supply Chain Management brukes til hovedplanlegging.

> [!NOTE]
> Hvis eksisterende satsvise planleggingsjobber for den innebygde planleggingsmotoren Supply Chain Management utløses når alternativet **Bruk planleggingsoptimalisering** er satt til **Ja**, vil disse jobbene mislykkes.

### <a name="integration-with-the-setup"></a>Integrering med oppsettet

Hvis forhåndsvisning av planleggingsoptimalisering er aktivert, utføres hovedplanlegging ved hjelp av tillegget for planleggingsoptimalisering. I dette tilfellet berøres resultater og funksjoner for hovedplanlegging.

## <a name="related-resources"></a>Relaterte ressurser

[Vilkår for forhåndsvisningen](https://go.microsoft.com/fwlink/?linkid=2015274)

[Oversikt over planleggingsoptimalisering](planning-optimization-overview.md)

[Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md)

[Vise planhistorikk og planleggingslogger](plan-history-logs.md)

[Bruke filtre på en plan](plan-filters.md)

[Annullere en planleggingsjobb](cancel-planning-job.md)
