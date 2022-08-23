---
title: Vanlige spørsmål om Dynamics 365 Commerce- og Microsoft Teams-integrering
description: Denne artikkelen inneholder svar på vanlige spørsmål knyttet til Microsoft Dynamics 365 Commerce- og Microsoft Teams-integrering.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 79e8c6899d84c3d6147c0a0c2834a7ad2f7b6927
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292061"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a>Vanlige spørsmål om Dynamics 365 Commerce- og Microsoft Teams-integrering

[!include [banner](includes/banner.md)]

Denne artikkelen inneholder svar på vanlige spørsmål knyttet til Microsoft Dynamics 365 Commerce- og Microsoft Teams-integrering.

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a>Hvem i butikken blir eier av et team under klargjøring av Teams fra Commerce? 

Alle butikksjefer legges automatisk til som eiere i den tilsvarende gruppen, slik at de kan utføre operasjoner, for eksempel legge til en privat kanal og legge til eller slette medlemmer. 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a>Hvordan tilordner jeg rollen "kommunikasjonsansvarlig" til en ansatt i Commerce Headquarters? 

Kommunikasjonsledere i Microsoft Teams har muligheten til å opprette og publisere oppgavelister. Organisasjonsansatte som må bli kommunikasjonsansvarlige, må ha tilordnet rollen "Retail-oppgaveleder" i Commerce Headquarters.

Følg denne fremgangsmåten for å tilordne rollen Retail-oppgaveleder til en ansatt i Commerce Headquarters.

1. Gå til **Retail og Commerce \> Ansatte \> Brukere**.
1. Velg en ansatt.
1. På hurtigfanen **Brukerens roller** velger du **Tilordne roller**.
1. I dialogboksen **Tilordne roller til bruker** velger du rollen **Retail-oppgaveleder** og velger deretter **OK**.

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a>Hvordan gjør jeg et bestemt organisasjonshierarki tilgjengelig for opplasting til Microsoft Teams?

I Commerce Headquarters er hver organisasjons hierarki knyttet til ett eller flere formål. Kontroller at hierarkiet du vil klargjøre i Microsoft Teams, har formålet **Detaljhandelsrapportering** knyttet til seg, som vist i følgende eksempelbilde. 

![Eksempel på et organisasjonshierarkiformål i Commerce Headquarters.](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a>Hvordan aktiverer jeg detaljhandelsarbeidere for å logge seg på Commerce POS (salgssted) ved hjelp av Azure Active Directory (Azure AD)?

Hvis du vil ha mer informasjon om hvordan du konfigurerer påloggingsopplevelsen for Commerce POS for å bruke Azure AD-godkjenning, kan du se [Aktiver Azure Active Directory-godkjenning for POS-pålogging](aad-pos-logon.md).

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a>Hvordan tilordner jeg butikker og tilsvarende grupper i Commerce Headquarters hvis organisasjonen allerede har opprettet grupper i Microsoft Teams?

Hvis du vil ha informasjon om hvordan du tilordner butikker og grupper hvis det finnes allerede eksisterende grupper, kan du se [Tilordne butikker og tilsvarende grupper hvis organisasjonen allerede har eksisterende grupper i Microsoft Teams](map-stores-existing-teams.md).

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a>Hvordan fjerner jeg merket for Microsoft Graph API-tokenet som er lagret i øktlageret?

En bruker som har logget seg på salgsstedet med en Azure Active Directory-konto (Azure AD), må logge seg ut fra POS-systemet eller lukke programmet for å tømme øktlageret. 

> [!TIP]
> En anbefalt fremgangsmåte er at butikkarbeidere alltid låser salgsstedsterminalen eller logger seg ut fra en økt når terminalen ikke brukes. 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a>Hva skjer hvis en butikk ikke har butikksjefer?

Hvis en butikk ikke har ledere, opprettes det ikke en gruppe for butikken eller i Teams. 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a>Hva skjer hvis en butikksjef forlater firmaet?

Alle som har eierrollen, kan legge til en ny butikksjef i Commerce Headquarters og klargjøre Teams på nytt, slik at den nye lederen får de nødvendige rettighetene i Teams for gruppen. 

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over Dynamics 365 Commerce- og Microsoft Teams-integrering](commerce-teams-integration.md)

[Aktiver Dynamics 365 Commerce- og Microsoft Teams-integrering](enable-teams-integration.md)

[Klargjøring av Microsoft Teams fra Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Synkroniser oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Behandle brukerroller i Microsoft Teams](manage-user-roles-teams.md)

[Tilordne butikker og grupper hvis det finnes eksisterende grupper i Microsoft Teams](map-stores-existing-teams.md)
