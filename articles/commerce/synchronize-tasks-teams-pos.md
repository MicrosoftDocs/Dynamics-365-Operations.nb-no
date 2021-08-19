---
title: Synkroniser oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce POS
description: Dette emnet beskriver hvordan du synkroniserer oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce-salgsstedet (POS).
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
ms.openlocfilehash: f9abebbf8d6c5dd6695b9697361e1a9a9e6005dc3ded16c4211c9c5c9e34a0b3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730881"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>Synkroniser oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce POS

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du synkroniserer oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce-salgsstedet (POS).

Et av hovedformålene med Teams-integrering er å aktivere synkronisering av oppgavestyring mellom POS-programmet og Teams. På denne måten kan butikkansatte bruke enten POS-programmet eller Teams til å administrere oppgaver, uten at de må bytte programmer.

Siden Planner brukes som et oppbevaringssted for oppgaver i Teams, må det være en kobling mellom Teams og Dynamics 365 Commerce. Denne koblingen opprettes ved å bruke en bestemt plan-ID for en angitt butikkgruppe.

Fremgangsmåtene nedenfor viser hvordan du konfigurerer oppgavebehandlingssynkronisering mellom POS- og Teams-programmene.

## <a name="publish-a-test-task-list-in-teams"></a>Publiser en testoppgaveliste i Teams

Fremgangsmåten nedenfor forutsetter at butikkgruppene bruker integrering av Microsoft Teams-oppgavebehandling med Commerce for første gang.

Følg denne fremgangsmåten for å publisere en testoppgaveliste i Teams.

1. Logg deg på Teams som en kommunikasjonsleder. Kommunikasjonsledere er vanligvis brukere som har rollen **Regional leder** i Commerce.
1. Velg **Oppgaver etter planlegger** i den venstre navigasjonsruten.
1. På fanen **Publiserte lister** velger du **Ny liste** nederst til venstre og gir den nye listen navnet **Testoppgaveliste**.
1. Velg **Opprett**. Den nye listen vises under **Utkast**.
1. Under **Oppgavetittel** gir du den første oppgaven tittelen **Testing av Teams-integrering**. Velg deretter **Enter**.
1. Velg oppgavelisten i **Utkast**-listen. Velg deretter **Publiser** øverst til høyre.
1. I dialogboksen **Velg hvem det skal publiseres til** velger du teamene som skal motta testoppgavelisten.
1. Velg **Neste** for å gå gjennom publikasjonsplanen. Hvis du må gjøre endringer, velger du **Tilbake**. 
1. Velg **Bekreft for å fortsette**, og velg deretter **Publiser**.
1. Når publiseringen er fullført, viser en melding øverst på fanen **Publiserte lister** om oppgavelisten ble levert.

Hvis du vil ha mer informasjon, kan du se [Publiser oppgavelister for å opprette og spore arbeid i organisasjonen](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).

## <a name="link-pos-and-teams-for-task-management"></a>Koble POS og Teams for oppgavebehandling

Hvis du vil koble POS- og Microsoft Teams-programmene for oppgavebehandling i Commerce Headquarters, følger du trinnene nedenfor.

1. Gå til **Retail og Commerce \> Oppgavebehandling \> Oppgaveintegrering med Microsoft Teams**.
1. I handlingsruten velger du **Rediger**.
1. Sett alternativet **Aktiver integrering av oppgavebehandling** til **Ja**.
1. Velg **Lagre** i handlingsruten.
1. Velg **Konfigurer oppgavebehandling** i handlingsruten. Du skal motta en varsling som angir at en satsvis jobb med navnet **Teams-klargjøring** opprettes.
1. Gå til **Systemadministrasjon \> Forespørsler \> Satsvise jobber**, og finn den nyeste jobben som har beskrivelsen **Teams-klargjøring**. Vent til denne jobben er fullført.
1. Kjør **CDX-jobb 1070** for å publisere plan-ID-en og lagre referanser til Retail Server.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over Dynamics 365 Commerce- og Microsoft Teams-integrering](commerce-teams-integration.md)

[Aktiver Dynamics 365 Commerce- og Microsoft Teams-integrering](enable-teams-integration.md)

[Klargjøring av Microsoft Teams fra Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Behandle brukerroller i Microsoft Teams](manage-user-roles-teams.md)

[Tilordne butikker og grupper hvis det finnes eksisterende grupper i Microsoft Teams](map-stores-existing-teams.md)

[Vanlige spørsmål om Dynamics 365 Commerce- og Microsoft Teams-integrering](teams-integration-faq.md)
