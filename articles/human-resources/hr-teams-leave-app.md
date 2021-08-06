---
title: Behandle permisjonsforespørsler i Teams
description: Dette emnet viser hvordan du ber om fridager Dynamics 365 Human Resources-appen i Microsoft Teams.
author: andreabichsel
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2a74b895052d017ccbe397bfb9a45609646b2f93
ms.sourcegitcommit: 86d38cf57abe768e5bccde48b28280bc2224080c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/19/2021
ms.locfileid: "6639444"
---
# <a name="manage-leave-requests-in-teams"></a>Behandle permisjonsforespørsler i Teams

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Med Dynamics 365 Human Resources-appen i Microsoft Teams kan du raskt be om fridager og vise saldoinformasjon for fridager i Microsoft Teams. Du kan samhandle med en robot for å be om informasjon og starte en permisjonsforespørsel. Kateogrien **Fridager** gir mer detaljert informasjon. Du kan også sende personinformasjon om kommende fritid i Teams og samtaler utenfor Human Resources-appen.

## <a name="install-the-app"></a>Installere appen

Du finner Dynamics 365 Human Resources-appen i Teams-butikken.

1. I Microsoft Teams navigerer du til listen over apper.
 
2. Søk etter Dynamics 365 Human Resources, og velg deretter flisen **Human Resources**.

3. Velg **Legg til** for å installere appen.

Hvis appen ikke logger deg på automatisk, velger du kategorien **Innstillinger** for å logge på.

> [!NOTE]
> Hvis du ikke ser en påloggingsdialogboks, må du kontrollere innstillingene for nettleseren for å tillate popup-vinduer. 

Hvis du har tilgang til mer enn én forekomst av Human Resources, kan du velge hvilket miljø du vil koble til, i kategorien **Innstillinger**.

> [!NOTE]
> Appen støtter nå sikkerhetsrollen systemadministrator.
 
## <a name="use-the-bot"></a>Bruke roboten

Når appen er installert, vises det en velkomstmelding med informasjon om hvilke handlingstyper roboten kan utføre på dine vegne.

> [!NOTE]
> Når du først samhandler med roboten, må du kanskje logge på. Hvis du ikke ser en påloggingsdialogboks, må du kontrollere innstillingene for nettleseren for å tillate popup-vinduer.

Du kan be roboten om å:

- Vis gjeldende permisjonssaldoer. Du kan for eksempel sende en meldingen "Vis permisjonssaldoer".

- Starte en permisjonsforespørsel for deg. Send for eksempel en melding som sier: "Ta fri" eller "Jeg vil ta fri neste torsdag og fredag" for å være mer spesifikk for å be om permisjon for feriepermisjonstypen. 

  ![Starte en permisjonsforespørsel i Teams-samtaler.](./media/hr-teams-leave-app-initiate.png)

- Samtalen fylles ut en permisjonsforespørsel for deg. Velg **Be om fravær** og rediger detaljene for forespørselen.

   Hvis du vil sende permisjonsforespørsler for flere permisjonstyper for samme dato, velger du **Del dag med**-alternativet på menyen **Flere alternativer**. 

   Hvis du velger en halvdagspermisjon når permisjonsenheten er i dager, kan du angi om du vil be om fri første halve dag eller den andre halve dagen ved å velge alternativet **Halvdagsdefinisjon** på **Flere alternativer**-menyen.
   
   ![Halvdagsdefinisjoner.](./media/HalfDayDefinitions.png)

- Når du er ferdig med å redigere detaljene for permisjonsforespørselen, velger du **Send** for å sende den til godkjenning.

  ![Sende permisjonsforespørsel.](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a>Behandle permisjonen i Teams

I kategorien **Fridager** kan du vise: 

- Saldoinformasjon om fridager for hver permisjonstype du er registrert i

- Forespørsler om kommende permisjoner

- Forespørsler om fridager

- Utkast til permisjonsforespørsler
 
### <a name="create-a-new-request"></a>Opprette en ny forespørsel

1. Hvis du vil opprette en ny permisjonsforespørsel, velger du **Ny forespørsel**.

2. Angi dagen eller dagene du vil ha fri, og velg deretter **Legg til**.

   ![Tillegg av fridager i permisjonsapp for Human Resources Teams.](./media/TimeOffHours.png)

3. Angi en årsakskode hvis det er aktuelt. Skriv også inn kommentarer og legg til eventuelle vedlegg.

4. Hvis du vil sende flere permisjonsforespørsler for samme dato for ulike permisjonstyper, velger du **Del dag med**-alternativet på menyen **Flere alternativer**.

5. Velg alternativet for **Halvdagsdefinisjon** for å angi om du vil be om fri for den første halve dagen eller den andre halve dagen. Dette alternativet er tilgjengelig når permisjonsforespørselenheten er i dager og den ønskede mengden er 0,5 dager.

6. Når du er ferdig med å angi informasjon, angir du **Send** for å sende den til godkjenning. Du kan også angi **Lagre som utkast** for å komme tilbake til den senere.

### <a name="manage-draft-requests"></a>Behandle utkast til forespørsler

1. Velg kategorien **Utkast**.

2. Velg blyanten for å redigere forespørselen, eller velg papirkurven for å slette forespørselen.

3. Gjør nødvendige endringer. Når du er ferdig med å angi informasjon, skriver du inn **Send** for å sende den til godkjenning. Du kan også velge **Lagre som utkast** for å komme tilbake til den senere.
   
### <a name="respond-to-teams-notifications"></a>Svare på Teams-varslinger

Når du eller en arbeider du er godkjenner for, sender en permisjonsforespørsel, vil du motta en melding i Human Resources-appen i Teams. Du kan merke varslingen for å vise den. Varslinger vises også i **Chat**-området.

Hvis du er godkjenner, kan du velge **Godkjenn** eller **Avvis** i varslingen. Du kan også angi en valgfri melding.

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a>Sende kommende informasjon om fritid til kollegene

Når du har installert Human Resources-appen for Teams, kan du enkelt sende informasjon om kommende fritid til kollegene i grupper eller samtaler.

1. Velg Human Resources-knappen under chattevinduet i et team eller en chat i Teams.

   ![Human Resources-knapp under chattevinduet.](./media/hr-teams-leave-app-chat-button.png)

2. Velg permisjonsforespørselen du vil dele. Hvis du vil dele et utkast av en permisjonsforespørsel, velger du **Utkast** først.

Permisjonsforespørselen vises i chatten.

Hvis du delte en utkastforespørsel, vil den vises som et utkast.

## <a name="view-your-teams-leave-calendar"></a>Vise teamets persmisjonskalender

Hvis du er leder med direkterapporter, kan du vise gruppens godkjente og uavsluttede fritid.

1. I Human Resources-appen i Teams velger du **Fritid**.

2. Velg **Teamkalender**. Kalenderen viser de godkjente og uavsluttede fritidene for direkterapporter.

   > [!NOTE]
   > Hvis du ikke kan se gruppekalenderen, ber du administratoren om å aktivere den. Hvis du vil ha mer informasjon, kan du se [Installere og konfigurere](hr-admin-teams-leave-app.md#install-and-setup).

## <a name="supported-languages"></a>Språk som støttes

Appen Dynamics 365 Human Resources i Teams støtter følgende språk:

| ID for nasjonal innstilling | Språk |
| --- | --- |
| de-DE | Tysk (Tyskland) |
| es-ES | Spansk (Spania) |
| es-MX | Spansk (Mexico) |
| fr-CA | Fransk (Canada) |
| fr-FR | Fransk (Frankrike) |
| it-IT | Italiensk (Italia) |
| nl-NL | Nederlandsk (Nederland) |
| pt-BR | Portugisisk (Brasil) |
| tr-TR | Tyrkisk (Tyrkia) |
| zh-CN | Kinesisk (forenklet) |

## <a name="troubleshooting"></a>Feilsøking

Hvis du har problemer med å logge på eller bruke Dynamics 365 Human Resources Teams-appen, kan du prøve å følge disse instruksjonene for feilsøking. Hvis du fortsatt har problemer etter feilsøking, kontakter du kundestøtte. For mer informasjon, se [Få kundestøtte](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Kan ikke logge på Human Resources-appen i Teams

Hvis du ikke kan logge på appen, kan det hende at kontoen du bruker til å logge på Microsoft Teams, ikke er tilknyttet en ansattpost i Dynamics 365 Human Resources. Kontakt systemadministrator for å kontrollere at ansattposten er riktig tilknyttet.

### <a name="cant-find-the-dynamics-365-human-resources-environment-in-settings"></a>Finner ikke Dynamics 365 Human Resources-miljøet i Innstillinger

Hvis du ikke kan velge det riktige Dynamics 365-miljøet, er det ikke sikkert at brukerposten er riktig synkronisert. Kontakt systemadministratoren for å opprette brukerposten på nytt og knytte den til brukerlegitimasjonen. Deretter prøver du å logge deg på Human Resources-appen Microsoft Teams om noen minutter.

### <a name="translations-dont-display-correctly"></a>Oversettelser vises ikke riktig

Hvis oversettelsene ikke vises som forventet, må du kontrollere at språket du velger i Teams, samsvarer med språket som er valgt i **Brukeralternativer** for Human Resources.

I Teams kan du se på **Appspråk** i **Innstillinger**.

![Teams-innstillinger.](./media/hr-teams-leave-app-settings.png)

Velg **Innstillinger** og deretter **Brukeralternativer** i Human Resources. Kontroller at feltet **Språk** samsvarer med feltet **Appspråk** i Teams.

![Brukeralternativer for Human Resources.](./media/hr-teams-leave-app-user-options.png)

Gi oss beskjed hvis du fremdeles opplever oversettelsesproblemer. Hvis du vil ha informasjon, kan du se [Få støtte for Finance and Operations-apper eller Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Feil under godkjenning av permisjonsforespørsler i Human Resources-appen i Teams

Hvis du får en feilmelding under forsøk på å godkjenne permisjonsforespørsler i Teams-appen, kan du prøve følgende feilsøkingstrinn:

1. Kontroller at kontoen du bruker til å logge på Microsoft Teams, er den samme som du bruker til å få tilgang til Dynamics 365 Human Resources.

2. Kontroller at du er en gyldig godkjenner for forespørselen ved å kontrollere arbeidsflytinnstillingene for permisjonsgodkjenning. Hvis du vil ha mer informasjon om arbeidsflyter for permisjonsforespørsel, kan du se [Opprette en permisjonsforespørsel](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Permisjonsgodkjennere mottar ikke Teams-chatmeldinger for å godkjenne permisjonsforespørsler

1. Sikre at varslinger er aktivert for miljøet og brukeren. Hvis du vil ha mer informasjon, kan du se [Aktiver varslinger for Human Resources-appen i Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) og [Aktivere eller deaktivere Teams-varslinger for individuelle brukere](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Kontroller at brukere blir logget på **Chatter**-kategorien med samme legitimasjon som de bruker for godkjenning av permisjonsforespørsler. Bruk meldingene "logg av" og deretter "logg på" for å logge deg på med riktig legitimasjon.

3. Hvis problemet vedvarer, må du kontrollere statusen til den satsvise jobben for forretningshendelser som systemadministrator. Hvis den er i et ventende stadium eller utførelsesstadium, må du sjekke tilbake om et par minutter. Hvis statusen forblir uendret, kan du logge en støtteforespørsel, slik at teamet kan bidra til å løse problemet.

## <a name="known-accessibility-issues"></a>Kjente tilgjengelighetsproblemer

Human Resources-appen i Teams har følgende tilgjengelighetsproblemer som vi jobber med å rette opp i fremtidige versjoner.

| Problem | Midlertidig løsning eller forklaring |
| --- | --- |
| Hvis du zoomer til 400 % på skrivebordet, skjules noen av handlingsknappene fra visningen. | Det anbefales bruk av et forstørrelsesprogram i stedet til vi kan støtte dette zoomenivået. |
| I fanen **Fridager** annonserer VoiceOver en knappehandling ved å lese toppteksen for fridagerrutenettet. | Toppteksten og elementene i rutenettet er gruppert etter år, og de kan skjules. VoiceOver tolker dette som et handlingselement, men det er ikke det. |
| I fanen **Fridager** er det en ekstra sveipebevegelse når du navigerer til **Årsakskode** i en ny forespørsel. | Det finnes ingen skjult kontroll som sveipenavigeringen prøver å komme til. |
| På fanen **Fridager** hvis du sveiper mens kalenderen er åpen, kan du havne utenfor kontrollen i stedet for øverst i en ny forespørsel eller mens du redigerer en forespørsel. | Når du kommer **Gå til i dag**, bør du anse det som slutten på kontrollen, og sveipe i motsatt retning for å komme tilbake toppen. |
| I fanen **Chat** hopper fokuset tilbake til toppen når du angir en dato ved bruk av hjelpeverktøyet eller tastaturnavigasjonen. | Bruk tabulator til du kommer til inndataområdet igjen. |

## <a name="privacy-notice"></a>Personvernerklæring

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Ved hjelp av Dynamics 365 Human Resources-roboten i Microsoft Teams blir brukerens tekstinndata analysert for å forstå den underliggende spørringen/hensikten. Brukerens inndata, for eksempel "Søk i konto i Contoso", rutes til en av Microsofts kognitive tjenester, kalt Language Understanding Intelligent Service (LUIS). Les mer om LUIS  [her](https://www.luis.ai/). LUIS-tjenesten skiller eller forstår gjengivelsen av brukerens inndata (i dette tilfellet er hensikten å finne informasjon) og målenheten (i dette tilfellet er den tiltenkte enheten en konto kalt Contoso). Denne informasjonen sendes deretter videre til Microsofts  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), som kommuniserer med data fra Dynamics 365 Human Resources og henter den ønskede informasjonen for brukerspørringen. 

Ved å installere og tillate tilgang til bruk av robot, godtar du at LUIS-tjenesten og Azure-robotrammeverket behandler hensikten bak inndataene, noe som resulterer i en forbedret samtalebasert brukeropplevelse. LUIS-tjenesten og Azure-robotrammeverket kan ha forskjellige samsvarsnivåer sammenlignet med Dynamics 365 Human Resources. Selv om LUIS-tjenesten har tilgang bare til brukerspørringene og ikke er utformet for å være koblet til brukerens Dynamics 365 Human Resources-data eller konto, kan en bruker av Dynamics 365 Human Resources-roboten frivillig angi en spørring som inneholder kundedata, personlige data eller andre data, og denne typen spørringsinnhold kan sendes til LUIS-tjenesten og det profesjonelle Azure-robotrammeverket. 

Innholdet i brukerens spørringer og meldinger beholdes i LUIS-systemet i maksimalt 30 dager, blir kryptert når inaktive, og brukes ikke til opplæring eller forbedring av tjenesten. Les mer om kognitive tjenester [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Hvis du vil behandle administrasjonsinnstillinger for apper i Microsoft Teams, går du til [administrasjonssenteret for Microsoft Teams](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, Azure Event Grid og Azure Cosmos DB

Når du bruker varslingsfunksjonen for Dynamics 365 Human Resources-appen i Microsoft Teams, kan bestemte kundedata flyte utenfor det geografiske området der firmaets Human Resources-service blir distribuert.

Dynamics 365 Human Resources sender informasjon om den ansattes permisjonsforespørsel og arbeidsflytoppgave til Microsoft Azure Event Grid og Microsoft Teams. Disse dataene kan være lagret i Microsoft Azure Event Grid i opptil 24 timer og behandles i USA, krypteres i transitt og ved inaktivitet, og brukes ikke av Microsoft eller dets underprosesser til opplærings- eller serviceforbedringer. Hvis du vil forstå hvor dataene er lagret i Teams, kan du se: [Plassering av data i Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).

Mens du samtaler med chatroboten i Human Resources-appen, kan samtaleinnholdet lagres i Azure Cosmos DB og overføres til Microsoft Teams. Disse dataene kan være lagret i Azure Cosmos DB i opptil 24 timer, og kan behandles utenfor det geografiske området der leierens Human Resources-tjeneste distribueres, krypteres i transitt og når inaktiv og brukes ikke brukes av Microsoft eller dets underprosesser for opplærings- eller tjenesteforbedringer. Hvis du vil forstå hvor dataene er lagret i Teams, kan du se: [Plassering av data i Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).
 
Hvis du vil begrense tilgangen til Human Resources-appen i Microsoft Teams for organisasjonen eller brukere i organisasjonen, kan du se [Behandle policyer for apptillatelse i Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Se også

[Laste ned og installere Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Hjelpesenter for Microsoft Teams](https://support.office.com/teams)</br>
[Human Resources-app i Teams](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
