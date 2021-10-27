---
title: Kom i gang med planleggingsoptimalisering
description: Dette emnet forklarer hvordan du begynner å bruke funksjonen for planleggingsoptimalisering.
author: ChristianRytt
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 8681ef80166f7d5f108c9424b53fa5c6f5324467
ms.sourcegitcommit: fcb1aa39e933216dea9e586b552bce6057f416a6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/15/2021
ms.locfileid: "7645788"
---
# <a name="get-started-with-planning-optimization"></a>Komme i gang med planleggingsoptimalisering

[!include [banner](../../includes/banner.md)]

Som [tidligere annonsert](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios) skal Planleggingsoptimalisering erstatte den eksisterende innebygde planleggingsmotoren.

Hvis du bruker den innebygde hovedplanleggingsmotoren, bør du begynne å planlegge migreringen til Planleggingsoptimalisering nå. Det er viktig at du starter migreringsprosessen med én gang, fordi operasjonene kan bli påvirket når avskrivingen fremtvinges. Vi oppfordrer deg på det sterkeste til å fullføre migreringen før 1. desember 2020 for å unngå problemer i siste øyeblikk når avskrivingen fremtvinges. 

Funksjonen Planleggingsoptimalisering støtter for øyeblikket ikke alle funksjonene som er tilgjengelige i planleggingsmotoren som er innebygd i Supply Chain Management. Det er derfor viktig at du vurderer om funksjonssettet som for øyeblikket er tilgjengelig i planleggingsoptimalisering, oppfyller kravene dine. Funksjonen Planleggingsoptimalisering er for øyeblikket ikke aktivert som standard i Dynamics Lifecycle Services (LCS), slik at du kan gjennomføre evalueringen før funksjonen aktiveres.

> [!NOTE]
> Du må be om et unntak fra migreringen til Planleggingsoptimalisering hvis hovedplanleggingsprosessen ikke inkluderer produksjon (hovedplanlegging genererer planlagte produksjonsordrer), og du trenger den innebygde hovedplanleggingsmotoren etter versjon 10.0.15. Fra og med versjon 10.0.16 blir det vist en feil i miljøer ved kjøring av innebygd hovedplanlegging uten generering av planlagte produksjonsordrer. Planleggingsoptimalisering bør brukes for alle nye distribusjoner som ikke genererer planlagte produksjonsordrer under hovedplanlegging. Eiere av eksisterende miljøer som kjører den innebygde hovedplanleggingsmotoren uten generering av planlagte produksjonsordrer, vil motta en e-post med detaljer om unntaksprosessen. Det anbefales at du samarbeider med en partner for å evaluere og planlegge migreringen til Planleggingsoptimalisering.

Før du slår på planleggingsoptimalisering, anbefaler vi på det sterkeste at du evaluerer resultatene i tilpassingsanalysen av planleggingsoptimalisering. Hvis du vil ha mer informasjon, se [Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md).

## <a name="availability"></a>Tilgjengelighet

Planleggingsoptimalisering er for øyeblikket tilgjengelig i følgende Azure-områder: USA, Canada, Europa, Storbritannia, Australia, Asia/Stillehavskysten og Japan. Hvis du prøver å installere tillegget fra et annet geografisk område, vil LCS vise en melding om at dette området ikke støttes. Hvis du vil ha mer informasjon om geografiske områder for Azure og tilknyttede områder, kan du se [Azure-geografier](https://azure.microsoft.com/global-infrastructure/geographies/#geographies).

Legg merke til at planleggingsoptimalisering ikke støtter lokale distribusjoner av Dynamics 365 Supply Chain Management.

## <a name="licensing"></a>Lisensiering

Hvis du kan kjøre hovedplanlegging ved hjelp av den gjeldende lisensen, trenger du ikke kjøpe en tilleggslisens for å bruke planleggingsoptimalisering.

## <a name="install-and-enable-planning-optimization"></a>Installere og aktivere planleggingsoptimalisering

For å kunne bruke planleggingsoptimalisering må du kontrollere at alle forutsetningene er på plass i systemet, og deretter aktivere lisensnøkkelen og installere tillegget for planleggingsoptimalisering for Dynamics 365 Supply Chain Management.

### <a name="prerequisites"></a>Forutsetninger

Før du kan installere tillegget for planleggingsoptimalisering, må følgende forutsetninger være på plass:

- Du må kjøre Supply Chain Management i et LCS-aktivert miljø med høy tilgjengelighet, lag 2 eller høyere (ikke et OneBox-miljø), med Dynamics 365 Supply Chain Management versjon 10.0.7 eller nyere. Hvis du prøver å installere tillegget i et OneBox-miljø, vil ikke installasjonen bli fullført, og du må avbryte installasjonen.

- Systemet må være konfigurert for Power Platform-integrering. Hvis du vil ha mer informasjon, se [Microsoft Power Platform-integrering med Finance and Operations-apper](../../../fin-ops-core/dev-itpro/power-platform/overview.md).

### <a name="enable-the-planning-optimization-license"></a>Aktivere lisensen for planleggingsoptimalisering

Hvis du vil bruke planleggingsoptimalisering, må du aktivere konfigurasjonsnøkkelen. Slik gjør du dette:

1. Sett systemet i vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Gå til **Systemadministrasjon \> Oppsett \> Lisenskonfigurasjon**.
1. Merk av for **Planleggingsoptimalisering** i fanen **Konfigurasjonsnøkler**.
1. Deaktiver vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

### <a name="install-the-planning-optimization-add-in"></a>Installere tillegget for planleggingsoptimalisering

Du må installere tillegget fra LCS-prosjektet og deretter aktivere funksjonaliteten for planleggingsoptimalisering fra brukergrensesnittet for Supply Chain Management.

Slik installerer du tillegget for planleggingsoptimalisering:

1. Logg på LCS, og åpne ønsket miljø.
1. Gå til **Detaljerte opplysninger**.
1. Bla ned til **Miljøtillegg**-hurtigfanen.
1. Velg **Installer et nytt tillegg**.
1. Velg **Planleggingsoptimalisering**.
1. Følg installasjonsveiledningen, og godta vilkårene.
1. Velg **Installer**.
1. I hurtigfanen **Miljøtillegg** skal du se at planleggingsoptimalisering installeres.
1. Etter noen minutter skal **Installerer** endres til **Installert** (det er mulig at du må oppdatere siden). Når installasjonen er fullført, er du klar til å aktivere planleggingsoptimalisering i Dynamics 365 Supply Chain Management.

Hovedformålet med å installere tillegget for planleggingsoptimalisering er å koble til tjenesten og miljøet. Derfor må du installere tillegget separat i hvert miljø der du bruker Planleggingsoptimalisering, uavhengig av hvilken kode som er flyttet mellom miljøene.

## <a name="integrate-planning-optimization-with-your-system"></a>Integrere planleggingsoptimalisering med systemet

Hvis du vil konfigurere om planleggingsoptimaliserings-tillegget skal brukes til hovedplanlegging, går du til **Hovedplanlegging** \> **Oppsett** \> **Parametere for planleggingsoptimalisering**.

### <a name="connection-status"></a>Tilkoblingsstatus

Tilkoblingsstatusen angir gjeldende status for tilkoblingen mellom Supply Chain Management og planleggingsoptimaliseringstjenesten. Tabellen nedenfor viser mulige verdier.

| Tilkoblingsstatus | Beskrivelse | Kan planleggingsoptimalisering brukes? |
|---|---|---|
| Tilkoblet | Det er opprettet en forbindelse mellom planleggingsoptimaliseringstjenesten og Supply Chain Management. | Ja |
| Aktiverer tilkobling | En forespørsel om å aktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår. | Nei |
| Frakoblet | Det er ingen forbindelse til planleggingsoptimaliseringstjenesten. Tilkoblingen kan aktiveres fra LCS, som beskrevet tidligere i dette emnet. | Nei |
| Deaktiverer tilkobling | En forespørsel om å deaktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår. | Nei |
| Henter status | Systemet venter på statusinformasjon fra planleggingsoptimaliseringstjenesten. | Nei |

### <a name="the-use-planning-optimization-option"></a>Alternativet Bruk planleggingsoptimalisering

Innstillingen for alternativet **Bruk planleggingsoptimalisering** bestemmer hvilken planleggingsmotor som skal brukes til hovedplanlegging:

- **Ja** – planleggingsoptimalisering brukes til hovedplanlegging.
- **Nei** – den innebygde planleggingsmotoren Supply Chain Management brukes til hovedplanlegging.

Denne innstillingen gjelder for alle juridiske enheter (firmaer). Det er ikke mulig å bruke planleggingsoptimalisering i noen juridiske enheter, og den innebygde hovedplanleggingen i andre juridiske enheter.

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
