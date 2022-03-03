---
title: Aktiver Dynamics 365 Commerce- og Microsoft Teams-integrering
description: Dette emnet beskriver hvordan du aktiverer Microsoft Dynamics 365 Commerce- og Microsoft Teams-integrering.
author: gvrmohanreddy
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 52b1a889a15cfe2e6e104e38b7d257f80762954f
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323436"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Aktiver Dynamics 365 Commerce- og Microsoft Teams-integrering

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du aktiverer Microsoft Dynamics 365 Commerce- og Microsoft Teams-integrering.

Hvis du vil klargjøre Teams med informasjon fra Dynamics 365 Commerce og synkronisere oppgavebehandlingsfunksjonene mellom Teams og POS-programmet (salgsstedet), må du aktivere integreringsfunksjonene i Commerce Headquarters.

> [!NOTE]
> Når du aktiverer Teams-integrering, godtar du å dele dataene dine med Teams. Data som deles med Teams, kan ligge i et annet land enn Commerce-dataene, og de kan være underlagt andre samsvarsstandarder. Hvis du vil ha mer informasjon om disse endringene, kan du se [Microsoft Trust Center](https://www.microsoft.com/trust-center). Hvis du vil ha informasjon om Microsofts personvernerklæringer, kan du se [Microsofts personvernerklæring](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>Aktiver Teams-integrering

Før du kan aktivere Microsoft Teams-integrering med Commerce, må du registrere Teams-programmet med leieren i Azure-portalen.

Følg denne fremgangsmåten for å registrere Teams-programmet med leieren i Azure-portalen.

1. følg trinnene i [Hurtigstart: Registrer en app i Microsoft-identitetsplattformen](/azure/active-directory/develop/quickstart-register-app) for å registrere Teams-appen med leieren i Azure-portalen.
1. Velg appen du opprettet i forrige trinn, i **Appregistrering**-fanen. Velg deretter **Legg til en plattform** i **Godkjenning**-fanen.
1. Velg **Nett** i dialogboksen. Angi deretter en nettadresse i formatet **\<HQUrl\>/oauth** i feltet **Nettadresser for omadressering**. Erstatt **\<HQUrl\>** med nettadressen for Commerce Headquarters (for eksempel `https://hxennugbjtweufmdeo385f47fadb6aa9a0aos.cloudax.int.dynamics.com/oauth`).
1. Kopier verdien for **Program-ID (klient)** på **Oversikt**-siden for den registrerte appen. Du må oppgi denne verdien for å aktivere Teams-integrering i Commerce Headquarters i den neste delen.
1. Følg instruksjonene i [Legge til en klienthemmelighet](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret) for å legge til en klienthemmelighet. Kopier deretter verdien for **Hemmelig verdi** for klienten. Du må oppgi denne verdien for å aktivere Teams-integrering i Commerce Headquarters i den neste delen.
1. Velg **API-tillatelser**, og velg deretter **Legg til en tillatelse**.
1. Velg **Microsoft Graph** i dialogboksen **Be om API-tillatelser**, velg **Delegerte tillatelser**, utvid **Gruppe**, velg **Group.ReadWrite.All**, og velg deretter **Legg til tillatelser**.
1. Velg **Legg til en tillatelse** i dialogboksen **Be om API-tillatelser**, velg **Microsoft Graph**, velg **Programtillatelser**, utvid **Gruppe**, velg **Group.ReadWrite.All**, og velg deretter **Legg til tillatelser**.
1. Velg **Legg til en tillatelse** i dialogboksen **Be om API-tillatelser**. Søk etter **Microsoft Teams Retail Service** i fanen **API-er organisasjonen min bruker**, og velg den.
1. Velg **Delegerte tillatelser**, utvid **TaskPublishing**, velg **TaskPublising.ReadWrite.All**, og velg deretter **Legg til tillatelser**. Hvis du vil ha mer informasjon, kan du se [Konfigurere et klientprogram for å få tilgang til en nett-API](/azure/active-directory/develop/quickstart-configure-app-access-web-apis).

Følg denne fremgangsmåten for å aktivere Teams-integrering i Commerce Headquarters.

1. Gå til **Retail og Commerce \> Kanaloppsett \> Konfigurasjon av Microsoft Teams-integrering**.
1. I handlingsruten velger du **Rediger**.
1. Sett alternativet **Aktiver Microsoft Teams-integrering** til **Ja**.
1. I feltet **Program-ID** angir du verdien for **Program-ID (klient)** du fikk da du registrerte Teams-programmet i Azure-portalen.
1. I feltet **Programnøkkel** angir du verdien for **Hemmelig verdi** du fikk da du la til en klienthemmelighet i Azure-portalen.
1. Velg **Lagre** i handlingsruten.

Illustrasjonen nedenfor viser et eksempel på konfigurasjonen av Teams-integrering i Commerce Headquarters.

![Konfigurasjon av Teams-integrering i Commerce Headquarters.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>Deaktiver Teams-integrering

Følg denne fremgangsmåten for å deaktivere Microsoft Teams-integrering i Commerce Headquarters.

1. Gå til **Retail og Commerce \> Kanaloppsett \> Konfigurasjon av Microsoft Teams-integrering**.
1. I handlingsruten velger du **Rediger**.
3. Sett alternativet **Aktiver Microsoft Teams-integrering** til **Nei**.
4. Fjern verdiene fra feltene **App-ID** og **Appnøkkel**.
1. Velg **Lagre** i handlingsruten.

> [!NOTE]
> Når du har deaktivert Teams-integrering med Commerce, vil ikke POS-terminaler lenger vise oppgaver som er publisert fra Teams-appen.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over Dynamics 365 Commerce- og Microsoft Teams-integrering](commerce-teams-integration.md)

[Klargjøring av Microsoft Teams fra Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Synkroniser oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Behandle brukerroller i Microsoft Teams](manage-user-roles-teams.md)

[Tilordne butikker og grupper hvis det finnes eksisterende grupper i Microsoft Teams](map-stores-existing-teams.md)

[Vanlige spørsmål om Dynamics 365 Commerce- og Microsoft Teams-integrering](teams-integration-faq.md)
