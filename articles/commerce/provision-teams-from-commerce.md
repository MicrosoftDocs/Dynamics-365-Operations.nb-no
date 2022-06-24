---
title: Klargjøring av Microsoft Teams fra Dynamics 365 Commerce
description: Denne artikkelen beskriver hvordan du klargjør Microsoft Teams ved hjelp av organisasjonsdata fra Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3dc9d0f20ec251f0908dda0017adaaeac1b43856
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868941"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a>Klargjøring av Microsoft Teams fra Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du klargjør Microsoft Teams ved hjelp av organisasjonsdata fra Dynamics 365 Commerce.

Dynamics 365 Commerce tilbyr en enkel måte å klargjøre Teams på hvis du ikke har konfigurert team for detaljhandelsbutikker der ennå. Ved å dra nytte av veldefinert informasjon fra Commerce som du vil bruke i Teams, kan du hjelpe butikkansatte med å komme i gang i Teams. Denne informasjonen omfatter organisasjonshierarkiet, butikknavnene, ansattinformasjonen og Azure Active Directory-kontoene (Azure AD). 

Prosessen med å klargjøre Teams har to hovedtrinn:

1. I Teams oppretter du et team for hver detaljhandelsbutikk, og legger til butikkarbeidere som medlemmer av det aktuelle teamet. Hvis en ansatt er knyttet til mer enn én detaljhandelsbutikk, vil teammedlemskapet gjenspeile dette faktumet. Et kommunikasjonsteam som inneholder regionale ledere som medlemmer, vil bli opprettet for å bidra til å publisere oppgaver fra Teams.
1. Last opp organisasjonshierarkiet fra Commerce til Teams.

## <a name="provision-teams-in-commerce-headquarters"></a>Klargjør Teams i Commerce Headquarters

Før du klargjør Microsoft Teams, må du fullføre disse oppgavene:

- Bekreft at alle regionsjefene har blitt kommunikasjonsansvarlige.
- Bekreft at Azure-kontoen for hver butikksjef og arbeider er knyttet til lederens eller arbeiderens arbeiderpost i Commerce Headquarters.

Følg denne fremgangsmåten for å klargjøre Teams i Commerce Headquarters.

1. Gå til **Retail og Commerce \> Kanaloppsett \> Konfigurasjon av Microsoft Teams-integrering**.
1. I handlingsruten velger du **Klargjør Teams**. En satsvis jobb med navnet **Teams-klargjøring** opprettes.
1. Gå til **Systemadministrasjon \> Forespørsler \> Satsvise jobber**, og finn den nyeste jobben som har beskrivelsen **Teams-klargjøring**. Vent til denne jobben er fullført.

> [!TIP]
> Hvis ingen av dine regionsjefer, butikksjefer og butikkarbeidere er tilknyttet en Teams-lisens, kan du få følgende feilmelding: "Kan ikke hente aktuelle SKU-kategorier for brukeren". Hvis du vil rette på problemet, velger du **Synkroniser team og medlemmer** i handlingsruten.

<!-- ![Dynamics 365 Commerce - Teams integration configuration.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a>Valider Teams-klargjøring i Teams-administrasjonssenteret

Når du skal validere Microsoft Teams-klargjøring i Microsoft Teams-administrasjonssenteret, følger du fremgangsmåten nedenfor.
    
1. Gå til [Teams-administrasjonssenteret](https://admin.teams.microsoft.com/), og logg deg på som administrator for e-handel-leieren.
1. I den venstre navigasjonsruten velger du **Team** for å utvide det, og deretter velger du **Administrer team**.
1. Bekreft at ett team er opprettet for hver Commerce-detaljhandelsbutikk.
1. Velg et team, og bekreft at butikkarbeidere er lagt til som medlemmer av det.
1. Velg **Brukere** i den venstre navigasjonsruten, og bekreft at alle butikkansatte i alle butikker er lagt til som brukere.

Illustrasjonen nedenfor viser et eksempel på siden **Administrer team** i Teams-administrasjonssenteret.

![Eksempel på siden Administrer team i Teams-administrasjonsenteret.](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a>Last opp et Commerce-organisasjonshierarki i Teams
    
Commerce-organisasjonshierarkiet kan brukes i Microsoft Teams til å publisere oppgaver i alle eller utvalgte butikker som bruker den samme hierarkistrukturen.

Hvis du vil laste opp et Commerce-organisasjonshierarki i Teams, gjør du følgende:
    
1. I Commerce Headquarters, går du til **Retail og Commerce \> Kanaloppsett \> Konfigurasjon av Microsoft Teams-integrering**.
1. Velg **Last ned målrettingshierarki**, og velg deretter **Detaljhandelsbutikker etter region** for å laste ned en fil med kommaseparerte verdier (CSV-fil) med organisasjonshierarkiet.
1. Installer Microsoft Teams PowerShell-modulen ved å følge trinnene i [Installer Microsoft Teams PowerShell](/microsoftteams/teams-powershell-install).
1. Når du blir spurt i Teams PowerShell-vinduet, logger du deg på med administratorkontoen for Azure AD-leieren.
1. Følg trinnene i [Konfigurer målrettingshierarkiet for teamet](/microsoftteams/set-up-your-team-hierarchy) for å laste opp CSV-filen for målrettingshierarkiet.

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a>Kontroller at organisasjonshierarkiet ble lastet opp til Teams

Følg trinnene nedenfor for å kontroller at organisasjonshierarkiet ble lastet opp til Microsoft Teams.

1. Logg deg på Teams som en kommunikasjonsleder.
1. Velg **Oppgaver etter planlegger** i den venstre navigasjonsruten.
1. På fanen **Publiserte lister** oppretter du en ny liste som har en testoppgave.
1. Velg **Publiser**. Organisasjonshierarkiet skal vises i dialogboksen **Velg hvem det skal publiseres til**, som vist i eksemplet nedenfor.

![Eksempel på et organisasjonshierarki i dialogboksen Velg hvem det skal publiseres til.](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over Dynamics 365 Commerce- og Microsoft Teams-integrering](commerce-teams-integration.md)

[Aktiver Dynamics 365 Commerce- og Microsoft Teams-integrering](enable-teams-integration.md)

[Synkroniser oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Behandle brukerroller i Microsoft Teams](manage-user-roles-teams.md)

[Tilordne butikker og grupper hvis det finnes eksisterende grupper i Microsoft Teams](map-stores-existing-teams.md)

[Vanlige spørsmål om Dynamics 365 Commerce- og Microsoft Teams-integrering](teams-integration-faq.md)