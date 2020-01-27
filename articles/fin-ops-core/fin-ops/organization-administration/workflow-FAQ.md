---
title: Vanlige spørsmål om arbeidsflyt
description: Dette emnet gir svar på vanlige spørsmål om arbeidsflytsystemet.
author: ChrisGarty
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdddd26a662e9334f6d3c9806871df5b58ec03c7
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934915"
---
# <a name="workflow-faq"></a>Vanlige spørsmål om arbeidsflyt

[!include [banner](../includes/banner.md)]

Dette emnet gir svar på vanlige spørsmål om arbeidsflytsystemet.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Hvorfor mottas flere varslinger når et arbeidselement avvises?
Når et arbeidselement avvises, fullføres dette arbeidselementet som avvist. Et annet arbeidselement opprettes og tilordnes til avsenderen. Dette betyr at det er en melding til avsenderen for det avviste arbeidselementet og en egen melding til brukeren som er tilordnet til det nye "bedt om endring"-arbeidselementet. 

Hver varsling er for et annet arbeidselement, men likheten kan føre til forvirring. Vi ser på måter å forbedre dette på i fremtidige versjoner.

## <a name="why-are-my-workflow-exports-failing"></a>Hvorfor mislykkes arbeidsflyteksportene mine?
Det er for øyeblikket en begrensning i funksjonen for arbeidsflyteksport som hindrer at arbeidsflytnavn overskrider 48 tegn. Hvis du bruker et navn som er lengre enn 48 tegn, kan det resultere i feilen «Serveren kan ikke godkjenne forespørselen» og/eller hindre at en fil blir eksportert uten en filtype. Følgende blogginnlegg gir mer informasjon [Feilsøke arbeidsflyteksport](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Kan innsenderen av en arbeidsflyt også godkjenne arbeidsflyten?
Ja, en innsender av en arbeidsflyt kan også godkjenne arbeidsflyten hvis den er konfigurert slik. Du kan unngå denne virkemåten ved å sette **Systemadministrasjon > Arbeidsflyt >Arbeidsflytparametere > Generelt > Godkjenner > Sperr godkjenning av innsender** til **Ja**.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Kan jeg legge til varsler i arbeidsflyter for å gi brukere varslinger?
Det er viktig å være oppmerksom på følgende vedrørende tilføying av varsler i arbeidsflyter for å gi varslinger:
- Varsler i forhold til arbeidsflytvarsling
    - Du kan konfigurere varsler for postendringer. Arbeidsflyter endrer poster, så du kan konfigurere et varsel som er knyttet til en postendring som skyldes en arbeidsflyt. Siden arbeidsflyter har ulike innebygde varslingsalternativer, er det imidlertid ikke best å bruke varsler.
- Standardvarslinger fra arbeidsflyter 
    - Arbeidsflyter har innebygde e-postvarslinger. En kunde kan konfigurere varslingene slik at brukerne får tilsendt e-post. Disse varslingene resulterer ikke i Handlingssenter-meldinger for brukere.
    - I en fremtidig oppdatering kommer vi til å legge til en Handlingssenter-melding slik at en bruker tilordnes et arbeidselement for arbeidsflyt. 
- Legge til varslinger i arbeidsflyter
    - Handlingssenter-meldinger kan opprettes for bestemte brukere, for eksempel en melding som er opprettet fra en arbeidsflyt i X++.
    - [Arbeidsflyter har forretningshendelser](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) som kunden kan bruke til å utløse flyter som har varslingene de ser etter.   

Hvis en bruker ikke får riktig varsling fra handlingssenteret når de tilordnes et arbeidselement for arbeidsflyt, bruker du [Forretningshendelser for arbeidsflyt](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) med Microsoft Power Automate til å gi flere eller andre varslinger.

## <a name="workflow-editor-has-trouble-starting-under-adfs"></a>Redigeringsprogrammet for arbeidsflyt har problemer med å starte under ADFS 
Når du kjører under Active Directory Federation Services (AD FS) i et oppgradert miljø, kan redigeringsprogrammet for arbeidsflyt ha problemer med å starte. I så fall må du kontrollere at URL-en "https://dynamicsaxworkfloweditor/" er lagt til i egenskapen **Microsoft Dynamics 365 for Operations Lokalt - Arbeidsflyt - Opprinnelig program** i ADFS-innstillingene.
