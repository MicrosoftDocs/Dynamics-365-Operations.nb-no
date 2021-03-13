---
title: Human Resources-app i Teams
description: Dette emnet gir en innføring i Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams.
author: andreabichsel
manager: tfehr
ms.date: 09/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba520f873de5b20111f9134e87281bcdf4025785
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113709"
---
# <a name="human-resources-app-in-teams"></a>Human Resources-app i Teams

[!include [banner](includes/preview-feature.md)]

Med Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams kan ansatte raskt be om fridager og vise saldoinformasjon for fridager i Microsoft Teams. Ansatte kan samhandle med en robot for å be om informasjon. Kateogrien **Fridager** gir mer detaljert informasjon. I tillegg kan de sende personinformasjon om kommende fritid i grupper og samtaler utenfor Human Resources-appen.

![Robot for permisjonsapp i Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![Kategorien Fridager i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources-permisjonsforespørselskort](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>Installere og konfigurere

Du kan finne Human Resources-appen i Teams-butikken. Hvis du vil ha informasjon om hvordan du installerer Teams-appen, kan du se [Behandle permisjonsforespørsler i Teams](hr-teams-leave-app.md).

Hvis du vil ha informasjon om hvordan du administrerer apptillatelser i Teams, kan du se [Behandle policyer for apptillatelse i Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Aktiver varslinger for Human Resources-appen i Teams

Hvis du vil at brukere skal motta permisjonsforespørselsvarsler i Teams-appen, må du aktivere varslinger i Human Resources.

>[!NOTE]
>Det er bare brukere som er logget på Teams og som bruker Teams-appen i Human Resources, som mottar varslinger.

1. Velg **Systemadministrasjon** i Human Resources.

2. Velg **Koblinger**.

3. Under **Oppsett** velger du **Systemparametere**.

4. I kategorien **Generelt** setter du **Aktiver varslinger for Teams-app** til **Ja**.

   ![Aktivere varslinger for Teams-appen i Systemparametere](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Hvis du vil aktivere Teams-varslinger for alle brukere, velger du **Ja** i ledeteksten.

   ![Aktivere Teams-varslinger for alle brukere](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>Aktivere eller deaktivere Teams-varslinger for individuelle brukere

Når du har aktivert varsler for Teams-appen i Human Resources, kan du aktivere eller deaktivere varslinger for individuelle brukere.

1. Velg **Systemadministrasjon** i Human Resources.

2. Velg **Koblinger**.

3. Under **Brukere** velger du **Brukeralternativer**.

4. Velg kategorien **Arbeidsflyt**.

5. Sett **Aktiver varslinger for Teams-app** til **Ja** for å aktivere varslinger for brukeren, eller **Nei** for å deaktivere varslinger for brukeren.

   ![Aktivere varslinger for Teams-appen i kategorien Arbeidsflyt i Brukeralternativer](./media/hr-admin-teams-leave-app-notifications.png)

6. Velg **Lagre**.

## <a name="known-issues"></a>Kjente problemer

| Problem | Status |
| --- | --- |
| Balansen er feil når du sender inn fridager for en fremtidig dato. | Prognoser er ennå ikke tilgjengelige. Saldoen vises for den gjeldende datoen. |
| Kan ikke avbryte en forespørsel med statusen **Til vurdering**. | Denne funksjonaliteten støttes ikke for øyeblikket og blir lagt til i en fremtidig versjon. |
| Saldoinformasjon beregnes per i dag. | Systemet viser ikke saldoer i løpet av avsetningsperioden, selv om det er konfigurert i permisjons- og fraværsparametere. |

## <a name="troubleshooting"></a>Feilsøking

Hvis en bruker har problemer med å logge på eller bruke Human Resources Teams-appen, kan du prøve å følge disse instruksjonene for feilsøking. Hvis du fortsatt har problemer etter feilsøking, kontakter du kundestøtte. For mer informasjon, se [Få kundestøtte](hr-admin-troubleshooting-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Kan ikke logge på Human Resources-appen i Teams

Hvis en bruker kontakter deg fordi vedkommende ikke kan logge på appen, må du kontrollere at brukeren har en tilknyttet ansattpost i Human Resources.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Feil under godkjenning av permisjonsforespørsler i Human Resources-appen i Teams

Hvis en bruker får en feilmelding under forsøk på å godkjenne permisjonsforespørsler i Teams-appen, kan du utføre følgende feilsøkingstrinn:

1. Kontroller at Teams-kontoen er den samme som de bruker for å få tilgang til Human Resources.

2. Kontroller at de er en gyldig godkjenner for forespørselen ved å kontrollere arbeidsflytinnstillingene for permisjonsgodkjenning. Hvis du vil ha mer informasjon om arbeidsflyter for permisjonsforespørsel, kan du se [Opprette en permisjonsforespørsel](hr-leave-and-absence-workflow.md).

## <a name="privacy-notice"></a>Personvernerklæring

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Ved hjelp av Dynamics 365 Human Resources-roboten i Microsoft Teams blir brukerens tekstinndata analysert for å forstå den underliggende spørringen/hensikten. Brukerens inndata, for eksempel "Søk i konto i Contoso", rutes til en av Microsofts kognitive tjenester, kalt Language Understanding Intelligent Service (LUIS). Les mer om LUIS  [her](https://www.luis.ai/). LUIS-tjenesten skiller eller forstår gjengivelsen av brukerens inndata (i dette tilfellet er hensikten å finne informasjon) og målenheten (i dette tilfellet er den tiltenkte enheten en konto kalt Contoso). Denne informasjonen sendes deretter videre til Microsofts  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), som kommuniserer med data fra Dynamics 365 Human Resources og henter den ønskede informasjonen for brukerspørringen. 

Ved å installere og tillate tilgang til bruk av robot, godtar du at LUIS-tjenesten og Azure-robotrammeverket behandler hensikten bak inndataene, noe som resulterer i en forbedret samtalebasert brukeropplevelse. LUIS-tjenesten og Azure-robotrammeverket kan ha forskjellige samsvarsnivåer sammenlignet med Dynamics 365 Human Resources. Selv om LUIS-tjenesten har tilgang bare til brukerspørringene og ikke er utformet for å være koblet til brukerens Dynamics 365 Human Resources-data eller konto, kan en bruker av Dynamics 365 Human Resources-roboten frivillig angi en spørring som inneholder kundedata, personlige data eller andre data, og denne typen spørringsinnhold kan sendes til LUIS-tjenesten og det profesjonelle Azure-robotrammeverket. 

Innholdet i brukerens spørringer og meldinger beholdes i LUIS-systemet i maksimalt 30 dager, blir kryptert når inaktive, og brukes ikke til opplæring eller forbedring av tjenesten. Les mer om kognitive tjenester [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Hvis du vil behandle administrasjonsinnstillinger for apper i Microsoft Teams, går du til [administrasjonssenteret for Microsoft Teams](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, Azure Event Grid og Azure Cosmos DB

Når du bruker varslingsfunksjonen for Dynamics 365 Human Resources-appen i Microsoft Teams, kan bestemte kundedata flyte utenfor det geografiske området der firmaets Human Resources-service blir distribuert.

Dynamics 365 Human Resources sender informasjon om den ansattes permisjonsforespørsel og arbeidsflytoppgave til Microsoft Azure Event Grid og Microsoft Teams. Disse dataene kan være lagret i Microsoft Azure Event Grid i opptil 24 timer og behandles i USA, krypteres i transitt og ved inaktivitet, og brukes ikke av Microsoft eller dets underprosesser til opplærings- eller serviceforbedringer. Hvis du vil forstå hvor dataene er lagret i Teams, kan du se: [Plassering av data i Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).

Mens du samtaler med chatroboten i Human Resources-appen, kan samtaleinnholdet lagres i Azure Cosmos DB og overføres til Microsoft Teams. Disse dataene kan være lagret i Azure Cosmos DB i opptil 24 timer, og kan behandles utenfor det geografiske området der leierens Human Resources-tjeneste distribueres, krypteres i transitt og når inaktiv og brukes ikke brukes av Microsoft eller dets underprosesser for opplærings- eller tjenesteforbedringer. Hvis du vil forstå hvor dataene er lagret i Teams, kan du se: [Plassering av data i Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).
 
Hvis du vil begrense tilgangen til Human Resources-appen i Microsoft Teams for organisasjonen eller brukere i organisasjonen, kan du se [Behandle policyer for apptillatelse i Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Se også 

[Laste ned og installere Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Hjelpesenter for Microsoft Teams](https://support.office.com/teams)</br>
[Behandle permisjonsforespørsler i Teams](hr-teams-leave-app.md)

