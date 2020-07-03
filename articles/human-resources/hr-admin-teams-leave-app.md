---
title: Human Resources-app i Teams
description: Dette emnet gir en innføring i Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
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
ms.openlocfilehash: 36684710e39c27840cc4aaa259a85579104fd8d6
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431136"
---
# <a name="human-resources-app-in-teams"></a>Human Resources-app i Teams

[!include [banner](includes/preview-feature.md)]

Med Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams kan ansatte raskt be om fridager og vise saldoinformasjon for fridager i Microsoft Teams. Ansatte kan samhandle med en robot for å be om informasjon. Kateogrien **Fridager** gir mer detaljert informasjon.

![Robot for permisjonsapp i Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![Kategorien Fridager i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a>Installere og konfigurere

Du kan finne Human Resources-appen i Teams-butikken. Hvis du vil ha informasjon om hvordan du installerer Teams-appen, kan du se [Behandle permisjonsforespørsler i Teams](hr-teams-leave-app.md).

Hvis du vil ha informasjon om hvordan du administrerer apptillatelser i Teams, kan du se [Behandle policyer for apptillatelse i Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="known-issues"></a>Kjente problemer

| Avgang | Status |
| --- | --- |
| Feil: Det oppstod et problem under søk etter et miljø å koble til. | Du kan få denne feilmeldingen selv om du har bekreftet at brukeren har tilgang til ett eller flere HR-miljøer. I tillegg vil du kanskje ikke se alle de forventede miljøene. Til vi har løst problemet, sletter du brukeren og importerer vedkommende på nytt for å løse problemet. |
| Balansen er feil når du sender inn fridager for en fremtidig dato. | Prognoser er ennå ikke tilgjengelige. Saldoen vises for den gjeldende datoen. |
| Når antall timer i en eksisterende forespørsel reduseres, vil den **gjenværende saldoen** gå ned i stedet for opp. | Vi vil håndtere dette kjente problemet i fremtiden. Visningen er feil, men de riktige beløpene justeres ved innsending. |
| To kort for **Kommende fridager** vises for samme dato. | Kortene representerer atskilte innsendinger. Vi vil fortsette å registrere tilbakemeldinger og gjøre justeringer. |
| Kan ikke avbryte en forespørsel med statusen **Til vurdering**. | Denne funksjonaliteten støttes ikke for øyeblikket og blir lagt til i en fremtidig versjon. |
| Saldoinformasjon beregnes per i dag. | Systemet viser ikke saldoer i løpet av avsetningsperioden, selv om det er konfigurert i permisjons- og fraværsparametere. |

## <a name="privacy-notice"></a>Personvernerklæring

Ved hjelp av Dynamics 365 Human Resources-roboten i Microsoft Teams blir brukerens tekstinndata analysert for å forstå den underliggende spørringen/hensikten. Brukerens inndata, for eksempel "Søk i konto i Contoso", rutes til en av Microsofts kognitive tjenester, kalt Language Understanding Intelligent Service (LUIS). Les mer om LUIS  [her](https://www.luis.ai/). LUIS-tjenesten skiller eller forstår gjengivelsen av brukerens inndata (i dette tilfellet er hensikten å finne informasjon) og målenheten (i dette tilfellet er den tiltenkte enheten en konto kalt Contoso). Denne informasjonen sendes deretter videre til Microsofts [Azure-robotrammeverk](https://azure.microsoft.com/services/bot-service/) som kommuniserer med data fra Dynamics 365 Human Resources, og henter den ønskede informasjonen for brukerspørringen. 

Ved å installere og tillate tilgang til bruk av robot, godtar du at LUIS-tjenesten og Azure-robotrammeverket behandler hensikten bak inndataene, noe som resulterer i en forbedret samtalebasert brukeropplevelse. LUIS-tjenesten og Azure-robotrammeverket kan ha forskjellige samsvarsnivåer sammenlignet med Dynamics 365 Human Resources. Selv om LUIS-tjenesten har tilgang bare til brukerspørringene og ikke er utformet for å være koblet til brukerens Dynamics 365 Human Resources-data eller konto, kan en bruker av Dynamics 365 Human Resources-roboten frivillig angi en spørring som inneholder kundedata, personlige data eller andre data, og denne typen spørringsinnhold kan sendes til LUIS-tjenesten og det profesjonelle Azure-robotrammeverket. 

Innholdet i brukerens spørringer og meldinger beholdes i LUIS-systemet i maksimalt 30 dager, blir kryptert når inaktive, og brukes ikke til opplæring eller forbedring av tjenesten. Les mer om kognitive tjenester [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Hvis du vil behandle administrasjonsinnstillinger for apper i Microsoft Teams, går du til [administrasjonssenteret for Microsoft Teams](https://admin.teams.microsoft.com/). 

## <a name="see-also"></a>Se også 

[Laste ned og installere Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Hjelpesenter for Microsoft Teams](https://support.office.com/teams)</br>
[Behandle permisjonsforespørsler i Teams](hr-teams-leave-app.md)

