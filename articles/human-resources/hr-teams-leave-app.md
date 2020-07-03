---
title: Behandle permisjonsforespørsler i Teams
description: Dette emnet viser hvordan du ber om fridager Dynamics 365 Human Resources-appen i Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b3daa76385518ad4c7150fa93ce33be0351bfd57
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428834"
---
# <a name="manage-leave-requests-in-teams"></a>Behandle permisjonsforespørsler i Teams

[!include [banner](includes/preview-feature.md)]

Med Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams kan du raskt be om fridager og vise saldoinformasjon for fridager i Microsoft Teams. Du kan samhandle med en robot for å be om informasjon. Kateogrien **Fridager** gir mer detaljert informasjon.

## <a name="install-the-app"></a>Installere appen

Du kan finne Human Resources-appen i Teams-butikken.

1. I Microsoft Teams klikker du på ellipsene.

   ![Ellipser for permisjonsapp i Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. Søk etter Dynamics 365 Human Resources, og velg deretter flisen **Human Resources**.

   ![HR-flis for permisjonsapp i Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. Velg **Legg til** for å installere appen.

   ![Installasjon av permisjonsapp i Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

Hvis appen ikke logger deg på automatisk, velger du kategorien **Innstillinger** for å logge på.

![Kategorien Innstillinger i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> Hvis du ikke ser en påloggingsdialogboks, må du kontrollere innstillingene for nettleseren for å tillate popup-vinduer. 

Hvis du har tilgang til mer enn én forekomst av Human Resources, kan du velge hvilket miljø du vil koble til, i kategorien **Innstillinger**.

> [!WARNING]
> Appen støtter for øyeblikket ikke sikkerhetsrollen Systeadministrator, og vil vise en feilmelding hvis du logger på med en systemadministratorkonto. Hvis du vil logge på med en annen konto, velger du **Bytt kontoer** i kategorien **Innstillinger**, og deretter logger du på med en brukerkonto som ikke har rettigheter som systemadministrator.
 
## <a name="use-the-bot"></a>Bruke roboten

Når appen er installert, vises det en velkomstmelding med informasjon om hvilke handlingstyper roboten kan utføre på dine vegne.

![Velkomstmelding for robot i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> Når du først samhandler med roboten, må du kanskje logge på. Hvis du ikke ser en påloggingsdialogboks, må du kontrollere innstillingene for nettleseren for å tillate popup-vinduer.

Du kan be roboten om å:

- Vise saldoinformasjon om fridager for hver permisjonstype du er registrert i.

   ![Vise saldoer i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- Vise flere detaljer om en bestemt permisjonstype.

   ![Vise detaljer i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot-details.png)

- Starte en permisjonsforespørsel for deg.

   ![Be om permisjon i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot-request.png)
 
Etter at du har startet en permisjonsforespørsel, kan du justere dagene på kortet, eller du kan velge **Rediger detaljer** for å legge til mer informasjon i forespørselen.

![Redigering av forespørsel i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot-edit.png)
 
Når du er ferdig med å angi informasjon, skriver du inn **Send** for å sende den til godkjenning. Du kan også skrive inn **Lagre som utkast** for å komme tilbake til den senere.

![Innsending av forespørsel i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a>Behandle permisjonen i Teams

I kategorien **Fridager** kan du vise:

- Saldoinformasjon om fridager for hver permisjonstype du er registrert i

- Forespørsler om kommende permisjoner

- Forespørsler om fridager

- Utkast til permisjonsforespørsler

![Kategorien Fridager i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a>Opprette en ny forespørsel

1. Hvis du vil opprette en ny permisjonsforespørsel, velger du **Ny forespørsel**.

   ![Ny forespørsel i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. Angi dagen eller dagene du vil ha fri, og velg deretter **Legg til**.

   ![Tillegg av fridager i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. Angi en årsakskode hvis det er aktuelt. Skriv også inn kommentarer og legg til eventuelle vedlegg.

4. Når du er ferdig med å angi informasjon, skriver du inn **Send** for å sende den til godkjenning. Du kan også skrive inn **Lagre som utkast** for å komme tilbake til den senere.

### <a name="manage-draft-requests"></a>Behandle utkast til forespørsler

1. Velg kategorien **Utkast**.

   ![Kategorien Utkast i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. Velg blyanten for å redigere forespørselen, eller velg papirkurven for å slette forespørselen.

3. Gjør nødvendige endringer. Når du er ferdig med å angi informasjon, skriver du inn **Send** for å sende den til godkjenning. Du kan også velge **Lagre som utkast** for å komme tilbake til den senere.

   ![Redigering av utkast i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
## <a name="privacy-notice"></a>Personvernerklæring

Ved hjelp av Dynamics 365 Human Resources-roboten i Microsoft Teams blir brukerens tekstinndata analysert for å forstå den underliggende spørringen/hensikten. Brukerens inndata, for eksempel "Søk i konto i Contoso", rutes til en av Microsofts kognitive tjenester, kalt Language Understanding Intelligent Service (LUIS). Les mer om LUIS  [her](https://www.luis.ai/). LUIS-tjenesten skiller eller forstår gjengivelsen av brukerens inndata (i dette tilfellet er hensikten å finne informasjon) og målenheten (i dette tilfellet er den tiltenkte enheten en konto kalt Contoso). Denne informasjonen sendes deretter videre til Microsofts [Azure-robotrammeverk](https://azure.microsoft.com/services/bot-service/) som kommuniserer med data fra Dynamics 365 Human Resources, og henter den ønskede informasjonen for brukerspørringen. 

Ved å installere og tillate tilgang til bruk av robot, godtar du at LUIS-tjenesten og Azure-robotrammeverket behandler hensikten bak inndataene, noe som resulterer i en forbedret samtalebasert brukeropplevelse. LUIS-tjenesten og Azure-robotrammeverket kan ha forskjellige samsvarsnivåer sammenlignet med Dynamics 365 Human Resources. Selv om LUIS-tjenesten har tilgang bare til brukerspørringene og ikke er utformet for å være koblet til brukerens Dynamics 365 Human Resources-data eller konto, kan en bruker av Dynamics 365 Human Resources-roboten frivillig angi en spørring som inneholder kundedata, personlige data eller andre data, og denne typen spørringsinnhold kan sendes til LUIS-tjenesten og det profesjonelle Azure-robotrammeverket. 

Innholdet i brukerens spørringer og meldinger beholdes i LUIS-systemet i maksimalt 30 dager, blir kryptert når inaktive, og brukes ikke til opplæring eller forbedring av tjenesten. Les mer om kognitive tjenester [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Hvis du vil behandle administrasjonsinnstillinger for apper i Microsoft Teams, går du til [administrasjonssenteret for Microsoft Teams](https://admin.teams.microsoft.com/). 

## <a name="see-also"></a>Se også

[Laste ned og installere Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Hjelpesenter for Microsoft Teams](https://support.office.com/teams)</br>
[Human Resources-app i Teams](hr-admin-teams-leave-app.md)
