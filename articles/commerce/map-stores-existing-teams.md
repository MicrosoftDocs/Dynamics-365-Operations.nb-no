---
title: Tilordne butikker og grupper hvis det finnes eksisterende grupper i Microsoft Teams
description: Dette emnet beskriver hvordan du tilordner butikker og tilsvarende grupper i Dynamics 365 Commerce-hovedkontoret hvis organisasjonen allerede har opprettet grupper i Microsoft Teams før Commerce-integrering.
author: gvrmohanreddy
ms.date: 03/31/2021
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
ms.openlocfilehash: c75525749d9015387cc112beda104238a93698e9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346698"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a>Tilordne butikker og grupper hvis det finnes eksisterende grupper i Microsoft Teams

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du tilordner butikker og tilsvarende grupper i Dynamics 365 Commerce-hovedkontoret hvis organisasjonen allerede har opprettet grupper i Microsoft Teams før Commerce-integrering.

Organisasjonen kan ha grupper som er opprettet for noen av eller alle butikkene, før integrering av Dynamics 365 Commerce og Microsoft Teams. Hvis dette er tilfelle, og hvis du skal opprette oppgavesynkronisering mellom Commerce POS og Microsoft Teams, må du angi tilordningen av butikker og tilsvarende team i Commerce Headquarters.

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a>Tilordne butikker og tilsvarende grupper i Commerce Headquarters 

Følg denne fremgangsmåten for å tilordne butikker og tilsvarende grupper i Commerce Headquarters.

1. Gå til **Systemadministrasjon \> Arbeidsområde \> Dataadministrasjon**.
1. Velg **Eksporter**. 
1. Velg **Ny** i handlingsruten.
1. Under **Gruppenavn** angir du "Eksporter Teams-tilordning".
1. På **Valgte enheter**-hurtigfanen velger du **Legg til enhet**. Dialogboksen **Legg til enhet** vises.  
1. I rullegardinlisten **Enhetsnavn** velger du **Teams-tilordning mellom kilde og team**.
1. I rullegardinlisten **Måldataformat** velger du **CSV**.
1. Velg **Legg til**, og velg deretter **Lukk**.
1. Velg **Eksporter nå** øverst til venstre under handlingsruten.
1. Under **Behandlingsstatus for enhet** velger du **Last ned fil**.
1. I den eksporterte CSV-filen angir du verdier for **SOURCETYPE**, **SOURCEID** og **TEAMID** som følger:
    - For **SOURCETYPE** angir du "RetailStore". 
    - For **SOURCEID** angir du butikknummeret (for eksempel "000135" for butikken i San Francisco). Du finner butikknumre under **Retail og Commerce \> Kanaler \> Butikker**.
    - For **TEAMID** angir du tilsvarende team-ID fra Microsoft Teams (for eksempel "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c"). Du finner informasjon om team-ID-er på [admin.teams.microsoft.com](https://admin.teams.microsoft.com).
1. Lagre CSV-filen på den lokale maskinen.
1. Gå til **Systemadministrasjon \> Arbeidsområde \> Dataadministrasjon**, og velg deretter **Importer**.
1. På **Valgte enheter**-hurtigfanen velger du **Legg til fil**. Dialogboksen **Legg til fil** vises.
1. I rullegardinlisten **Enhetsnavn** velger du **Teams-tilordning mellom kilde og team**.
1. I rullegardinlisten **Kildedataformat** velger du **CSV**.
1. Velg **Last opp og legg til**, velg CSV-filen du lagret tidligere, og velg deretter **Åpne**.
1. I dialogboksen **Legg til fil** velger du **Lukk**.
1. Velg **Lagre** i handlingsruten , og velg deretter **Importer**.

Følgende eksempelbilde viser gruppen **Eksporter Teams-tilordning** i Commerce med **Legg til enhet**-elementer og de eksporterte CSV-filhodene uthevet.

![Eksporter Teams-tilordning i Commerce med Legg til enhet-elementer og de eksporterte CSV-filhodene uthevet.](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> Når du har fullført trinnene ovenfor, følger du trinnene i [Synkroniser oppgavebehandling mellom Microsoft Teams og POS](synchronize-tasks-teams-pos.md) for å synkronisere oppgavebehandling. 

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over Dynamics 365 Commerce- og Microsoft Teams-integrering](commerce-teams-integration.md)

[Aktiver Dynamics 365 Commerce- og Microsoft Teams-integrering](enable-teams-integration.md)

[Klargjøring av Microsoft Teams fra Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Synkroniser oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Behandle brukerroller i Microsoft Teams](manage-user-roles-teams.md)

[Vanlige spørsmål om Dynamics 365 Commerce- og Microsoft Teams-integrering](teams-integration-faq.md)
