---
title: Kom i gang med planleggingsoptimalisering
description: Dette emnet forklarer hvordan du begynner å bruke funksjonen for planleggingsoptimalisering.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 54ad180b7f4691ead3563b077eadadc3b9b20588
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/29/2020
ms.locfileid: "4434854"
---
# <a name="get-started-with-planning-optimization"></a>Komme i gang med planleggingsoptimalisering

[!include [banner](../../includes/banner.md)]

Som [tidligere annonsert](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios) skal Planleggingsoptimalisering erstatte den eksisterende innebygde planleggingsmotoren.

Hvis du bruker den innebygde hovedplanleggingsmotoren, bør du begynne å planlegge migreringen til Planleggingsoptimalisering nå. Det er viktig at du starter migreringsprosessen med én gang, fordi operasjonene kan bli påvirket når avskrivingen fremtvinges. Vi oppfordrer deg på det sterkeste til å fullføre migreringen før 1. desember 2020 for å unngå problemer i siste øyeblikk når avskrivingen fremtvinges. 

Funksjonen Planleggingsoptimalisering støtter for øyeblikket ikke alle funksjonene som er tilgjengelige i planleggingsmotoren som er innebygd i Supply Chain Management. Det er derfor viktig at du vurderer om funksjonssettet som for øyeblikket er tilgjengelig i planleggingsoptimalisering, oppfyller kravene dine. Funksjonen Planleggingsoptimalisering er for øyeblikket ikke aktivert som standard i Dynamics Lifecycle Services (LCS), slik at du kan gjennomføre evalueringen før funksjonen aktiveres.

> [!NOTE]
> Du må be om et unntak fra migreringen til Planleggingsoptimalisering hvis hovedplanleggingsprosessen ikke inkluderer produksjon (hovedplanlegging genererer planlagte produksjonsordrer), og du trenger den innebygde hovedplanleggingsmotoren etter versjon 10.0.15. Fra og med versjon 10.0.16 blir det vist en feil i miljøer ved kjøring av innebygd hovedplanlegging uten generering av planlagte produksjonsordrer. Planleggingsoptimalisering bør brukes for alle nye distribusjoner som ikke genererer planlagte produksjonsordrer under hovedplanlegging. Eiere av eksisterende miljøer som kjører den innebygde hovedplanleggingsmotoren uten generering av planlagte produksjonsordrer, vil motta en e-post med detaljer om unntaksprosessen. Vi anbefaler at du samarbeider med en partner for å evaluere og planlegge migreringen til Planleggingsoptimalisering.

Før du slår på planleggingsoptimalisering, anbefaler vi på det sterkeste at du evaluerer resultatene i tilpassingsanalysen av planleggingsoptimalisering. Hvis du vil ha mer informasjon, se [Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md).

### <a name="availability"></a>Tilgjengelighet
Planleggingsoptimalisering er for øyeblikket tilgjengelig i følgende Azure-områder: USA, Canada, Europa, Storbritannia og Australia. Hvis du prøver å installere tillegget fra et annet geografisk område, vil LCS vise en melding om at dette området ikke støttes.

Legg merke til at planleggingsoptimalisering ikke støtter lokale distribusjoner av Dynamics 365 Supply Chain Management.

### <a name="licensing"></a>Lisensiering

Hvis du kan kjøre hovedplanlegging ved hjelp av den gjeldende lisensen, trenger du ikke kjøpe en tilleggslisens for å bruke planleggingsoptimalisering.

### <a name="install-the-add-in"></a>Installer tillegget

Hvis du vil bruke planleggingsoptimalisering, må du installere tillegget for planleggingsoptimalisering for Dynamics 365 Supply Chain Management. Du får tilgang til tillegget fra LCS-prosjektet og kan aktivere funksjonaliteten for planleggingsoptimalisering fra brukergrensesnittet for Supply Chain Management.

> [!NOTE]
> Kravet for planleggingsoptimalisering er et LCS-aktivert miljø med høy tilgjengelighet, lag 2 eller høyere (ikke et OneBox-miljø), med Dynamics 365 Supply Chain Management versjon 10.0.7 eller senere. Hvis du prøver å installere tillegget i et OneBox-miljø, vil ikke installasjonen bli fullført, og du må avbryte installasjonen.

1. Logg på LCS, og åpne ønsket miljø.
1. Gå til **Detaljerte opplysninger**.
1. Bla ned til **Miljøtillegg**-hurtigfanen.
1. Velg **Installer et nytt tillegg**.
1. Velg **Planleggingsoptimalisering**.
1. Følg installasjonsveiledningen, og godta vilkårene.
1. Velg **Installer**.
1. I **Miljøtillegg**-hurtigfanen skal du se at planleggingsoptimalisering installeres.
1. Etter noen minutter skal **Installerer** endres til **Installert** (det er mulig at du må oppdatere siden). Når installasjonen er fullført, er du klar til å aktivere planleggingsoptimalisering i Dynamics 365 Supply Chain Management.

Hovedformålet med å installere tilleggsfunksjonen for Planleggingsoptimalisering er å koble til tjenesten og miljøet. Derfor må du installere tillegget separat i hvert miljø der du bruker Planleggingsoptimalisering, uavhengig av hvilken kode som er flyttet mellom miljøene.

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

Hvis Planleggingsoptimalisering er aktivert, utføres hovedplanlegging ved hjelp av tillegget for planleggingsoptimalisering. I dette tilfellet berøres resultater og funksjoner for hovedplanlegging.

## <a name="additional-resources"></a>Tilleggsressurser

[Vilkår for forhåndsvisningen](https://go.microsoft.com/fwlink/?linkid=2015274)

[Oversikt over planleggingsoptimalisering](planning-optimization-overview.md)

[Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md)

[Vise planhistorikk og planleggingslogger](plan-history-logs.md)

[Bruke filtre på en plan](plan-filters.md)

[Annullere en planleggingsjobb](cancel-planning-job.md)
