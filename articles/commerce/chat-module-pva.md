---
title: Commerce-nettprat med Power Virtual Agents-modul
description: Denne artikkelen beskriver Commerce-nettprat med Power Virtual Agents-modulen som integrerer Microsoft Power Virtual Agents med Dynamics 365 Commerce-webområder.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-07
ms.openlocfilehash: 838990cb638479c9c90ba0e38794ecedd55e95b3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691082"
---
# <a name="commerce-chat-with-power-virtual-agents-module"></a>Commerce-nettprat med Power Virtual Agents-modul

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver Commerce-nettprat med Power Virtual Agents-modulen som integrerer Microsoft Power Virtual Agents med Dynamics 365 Commerce-webområder.

Ved hjelp av Commerce-nettprat med Power Virtual Agents-funksjonen kan Dynamics 365-e-handelskunder bruke Power Virtual Agents-chatrobotfunksjoner til å håndtere spørringene. Fra og med Dynamics 365 Commerce 10.0.30-versjonen kan denne funksjonen inkluderes i e-handel-webområder ved å bruke Commerce-nettprat med Power Virtual Agents-modulen som er en del av Commerce-modulbiblioteket.

Ved hjelp av Commerce-nettprat med Power Virtual Agents-funksjonen kan du oppnå følgende mål:

- Øke personalisert engasjement med kundene og forbedre tilfredshet.
- Forbedre kundeservice gjennom integreringen av selvbetjeningsnettpratroboter.
- Få bedre kundetilfredshet og dermed øke salget.

> [!NOTE]
> Hvis du vil lære om forskjellene mellom Dynamics 365 Omnikanal for Customer Service og Power Virtual Agents-programmer, kan du se [Oversikt over Commerce-nettpratfunksjoner](/commerce-chat-modules-overview.md).

## <a name="prerequisites-for-using-power-virtual-agents"></a><a id="prereq"></a>Forutsetninger for å bruke Power Virtual Agents

Hvis du vil bruke Commerce-nettprat med funksjonen Power Virtual Agents, må du først opprette en Power Virtual Agents-chatrobot for webområdet for e-handel. Hvis du vil ha instruksjoner, kan du se [Opprette en power virtual agent-robot](/power-virtual-agents/authoring-first-bot).

Når du har konfigurert chatroboten, må du kopiere verdiene til chatrobotparametrene for **Robot-ID** og **Leier-ID** for å konfigurere Commerce-nettpratopplevelsen. Hvis du vil ha informasjon om hvordan du kopierer disse verdiene, kan du se [Hente Power Virtual Agents-robotparametere](/power-virtual-agents/publication-connect-bot-to-custom-application#retrieve-your-power-virtual-agents-bot-parameters).

## <a name="configure-your-e-commerce-site"></a>Konfigurere e-handelsområde 

En anbefalt måte å implementere nettprat for e-handelsområdet er å legge til Commerce-nettprat med Power Virtual Agents-modulen i det delte hodefragmentet som brukes på netthandelsidene.

Følg denne fremgangsmåten for å legge til nettpratmodulen på nettstedets hodefragment i Commerce-områdebygger.

1. I Commerce-områdebyggeren for området går du til **Fragmenter**.
1. Velg **Ny**.
1. I dialogboksen **Velg et fragment** velger du **Commerce-nettprat med Power Virtual Agents**-modulen, angir et navn på fragmentet og velger deretter **OK**.
1. I disposisjonsvisningen velger du sporet **Msdyn365 pva-nettpratkontakt**.
1. Følg denne fremgangsmåten i ruten for egenskaper til høyre:

    1. Under **Robotparametere**, i feltet **CDN URL for Bot Framework-nettprat**, lar du standardverdien stå (for eksempel `https://cdn.botframework.com/botframework-webchat/latest/webchat.js`).
    1. I feltet **URL-adressene for Bot Framework Direct Line-godkjenning** lar du standardverdien stå (for eksempel`https://powerva.microsoft.com/api/botmanagement/v1/directline/directlinetoken`).
    1. I feltet **Robot-ID** angir du Power Virtual Agents **Robot-ID**-verdien som du kopierte i delen [Forutsetninger for bruk av Power Virtual Agents](#prereq).
    1. I feltet **Leietaker-ID** angir du **Leier-ID**-verdien du kopierte.

1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.
1. Gå til **Fragmenter** og åpne hodefragmentet for området.
1. I **Standardbeholder**-sporet i modulen velger du ellipsen (**…**), og deretter velger du **Legg til fragment**.
1. I dialogboksen **Velg moduler** velger du nettpratfragmentet du opprettet tidligere, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.

## <a name="proactive-chat-parameters"></a>Proaktive nettpratparametere

Hvis du vil ha en fullstendig liste over konfigurasjonsparametere for proaktiv nettprat, kan du se [Proaktive nettpratparametere for Commerce-nettpratmodulen](chat-proactive-chat-parameters.md).

> [!NOTE]
> Power Virtual Agents støtter for øyeblikket ikke Azure Active Directory B2C (Azure AD B2C)-godkjenning. Det støtter bare anonyme Retail Cloud Scale Unit (RCSU)-kall for å få produkttilgjengelighet eller samarbeide med andre anonyme APIer. Samtaler til godkjente APIer via Power Virtual Agents-nettpratroboter krever en eksplisitt kundepålogging.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over Commerce-nettpratfunksjoner](commerce-chat-overview.md)

[Commerce-nettprat med Omnikanal for Customer Service-modul](commerce-chat-module.md)

[Proaktive nettpratparametere for Commerce-nettpratmodulen](chat-proactive-chat-parameters.md)
