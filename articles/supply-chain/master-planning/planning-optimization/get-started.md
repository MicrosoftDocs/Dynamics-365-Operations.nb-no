---
title: Kom i gang med hovedplanlegging
description: Denne artikkelen forklarer hvordan du begynner å bruke funksjonen for hovedplanlegging i Dynamics 365 Supply Chain Management.
author: t-benebo
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
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 958de3f9ae6ead6cb6914bd3b7a4560e768013ab
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740336"
---
# <a name="get-started-with-master-planning"></a>Kom i gang med hovedplanlegging

[!include [banner](../../includes/banner.md)]

Hovedplanlegging i Supply Chain Management leveres av en ekstern tjeneste kalt tilleggsprogrammet for planleggingsoptimalisering for Dynamics 365 Supply Chain Management. Dette emnet forklarer hvordan du skaffer og konfigurerer denne tjenesten.

## <a name="availability"></a>Tilgjengelighet

Planleggingsoptimalisering er for øyeblikket tilgjengelig i følgende Azure-områder: USA, Canada, Brasil, Europa, Frankrike, Storbritannia, Australia, Asia/Stillehavskysten, Japan og India. Hvis du prøver å installere tillegget fra et annet geografisk område, vil LCS vise en melding om at dette området ikke støttes. Hvis du vil ha mer informasjon om geografiske områder for Azure og tilknyttede områder, kan du se [Azure-geografier](https://azure.microsoft.com/global-infrastructure/geographies/#geographies).

Legg merke til at planleggingsoptimalisering ikke støtter lokale distribusjoner av Dynamics 365 Supply Chain Management.

## <a name="licensing"></a>Lisensiering

Hvis du kan kjøre hovedplanlegging ved hjelp av den gjeldende lisensen, trenger du ikke kjøpe en tilleggslisens for å bruke planleggingsoptimalisering.

## <a name="install-and-enable-planning-optimization"></a>Installere og aktivere planleggingsoptimalisering

For å kunne bruke planleggingsoptimalisering må du kontrollere at alle forutsetningene er på plass i systemet, og deretter aktivere lisensnøkkelen og installere tillegget for planleggingsoptimalisering for Dynamics 365 Supply Chain Management.

### <a name="prerequisites"></a>Forutsetninger

Før du kan installere tillegget for planleggingsoptimalisering, må følgende forutsetninger være på plass:

- Du må kjøre Supply Chain Management i et LCS-aktivert miljø med høy tilgjengelighet, lag 2 eller høyere (ikke et OneBox-miljø), med Dynamics 365 Supply Chain Management versjon 10.0.7 eller nyere. Hvis du prøver å installere tillegget i et OneBox-miljø, vil ikke installasjonen bli fullført, og du må avbryte installasjonen.

- Systemet må være konfigurert for Power Platform-integrering. Hvis du vil ha mer informasjon, se [Microsoft Power Platform-integrering med økonomi- og driftsapper](../../../fin-ops-core/dev-itpro/power-platform/overview.md).

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
| Frakoblet | Det er ingen forbindelse til planleggingsoptimaliseringstjenesten. Tilkoblingen kan aktiveres fra LCS, som beskrevet tidligere i denne artikkelen. | Nei |
| Deaktiverer tilkobling | En forespørsel om å deaktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår. | Nei |
| Henter status | Systemet venter på statusinformasjon fra planleggingsoptimaliseringstjenesten. | Nei |

### <a name="the-use-planning-optimization-option"></a>Alternativet Bruk planleggingsoptimalisering

Innstillingen for alternativet **Bruk planleggingsoptimalisering** bestemmer hvilken planleggingsmotor som skal brukes til hovedplanlegging:

- **Ja** – planleggingsoptimalisering brukes til hovedplanlegging.
- **Nei** – den avskrevne hovedplanleggingsmotoren brukes til hovedplanlegging.

Denne innstillingen gjelder for alle juridiske enheter (firmaer). Det er ikke mulig å bruke planleggingsoptimalisering i noen juridiske enheter, og den avskrevne hovedplanleggingsmotoren i andre juridiske enheter.

> [!NOTE]
> Hvis eksisterende satsvise planleggingsjobber for den avskrevne hovedplanleggingsmotoren utløses når alternativet **Bruk planleggingsoptimalisering** er satt til **Ja**, vil disse jobbene mislykkes.

### <a name="integration-with-the-setup"></a>Integrering med oppsettet

Hvis Planleggingsoptimalisering er aktivert, utføres hovedplanlegging ved hjelp av tillegget for planleggingsoptimalisering. I dette tilfellet berøres resultater og funksjoner for hovedplanlegging.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
