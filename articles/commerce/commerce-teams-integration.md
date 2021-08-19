---
title: Oversikt over Dynamics 365 Commerce- og Microsoft Teams-integrering
description: Dette emnet gir en oversikt over Microsoft Dynamics 365 Commerce- og Microsoft Teams-integrering.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 38235c237f4311a9616f88b56f1503935b25b251d1c2d35d4392418e8c1a357b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714022"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a>Oversikt over Dynamics 365 Commerce- og Microsoft Teams-integrering

[!include [banner](includes/banner.md)]

Dette emnet gir en oversikt over Microsoft Dynamics 365 Commerce- og Microsoft Teams-integrering.

Dynamics 365 Commerce integreres med Teams for å hjelpe kundene og de ansatte med å forbedre produktiviteten ved å synkronisere oppgaveadministrasjon mellom de to programmene. Den sømløse oppgaveadministrasjonen som Commerce- og Teams-integrering gir, lar butikksjefer og ansatte opprette oppgavelister, tilordne oppgaver til flere butikker og spore statusen til oppgaver på tvers av butikker, fra begge programmene.

Commerce- og Teams-integrering er tilgjengelig fra Commerce versjon 10.0.18.

## <a name="key-features"></a>Hovedfunksjoner

Her er noen av nøkkelfunksjonene som Commerce- og Microsoft Teams-integreringen gir:

- Klargjør Teams ved å dra nytte av veldefinert informasjon fra Commerce, for eksempel organisasjonsstrukturen og informasjon om butikker, arbeidere, tillatelser og forretningskontekst.
- Du kan enkelt synkronisere pågående endringer (for eksempel tilføyelse av nye butikker eller ansettelse av nye medarbeidere) mellom Commerce og Teams, men beholde Commerce som hovedkilden for organisasjonsstrukturdata.
- Integrer oppgaveadministrasjon mellom Commerce og Teams for å hjelpe butikkarbeidere, butikksjefer, regionsjefer og kommunikasjonsledere med å håndtere oppgavebehandling fra begge programmene.

## <a name="prerequisites-for-using-integration-features"></a>Forutsetninger for å bruke integreringsfunksjoner

Følgende forutsetninger må være på plass før du kan begynne å bruke Microsoft Teams-integreringsfunksjoner:

- Microsoft 365 Business-standardlisens (Denne lisensen inkluderer Teams.)
- Azure Active Directory-kontoer (Azure AD) for alle butikksjefer og arbeidere
- Systemer på salgsstedet (POS-systemer) som er konfigurert med Azure AD-godkjenning

## <a name="conceptual-architecture"></a>Konseptuell arkitektur

Illustrasjonen nedenfor viser den konseptuelle arkitekturen bak Dynamics 365 Commerce- og Microsoft Teams-integrering, ved å bruke en butikk i San Francisco som et eksempel. Både Teams og Commerce POS-programmet bruker Microsoft Planner som et repositorium, slik at oppgaver som publiseres fra Teams, vises i POS-programmet. og ad hoc-oppgaver som opprettes av butikksjefer i POS-programmet, vises i Teams, noe som resulterer i en sømløs oppgavebehandlingsopplevelse mellom programmene.    

![Arkitekturen bak Commerce og Teams-integrering.](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Aktiver Dynamics 365 Commerce- og Microsoft Teams-integrering](enable-teams-integration.md)

[Klargjøring av Microsoft Teams fra Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Synkroniser oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Behandle brukerroller i Microsoft Teams](manage-user-roles-teams.md)

[Tilordne butikker og grupper hvis det finnes eksisterende grupper i Microsoft Teams](map-stores-existing-teams.md)

[Vanlige spørsmål om Dynamics 365 Commerce- og Microsoft Teams-integrering](teams-integration-faq.md)
