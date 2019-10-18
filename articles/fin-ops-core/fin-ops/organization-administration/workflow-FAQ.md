---
title: Vanlige spørsmål om arbeidsflyt
description: Dette emnet gir svar på vanlige spørsmål om arbeidsflytsystemet.
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
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
ms.openlocfilehash: 14aa9b56da005e8e3ca121589d0e22c60f34343b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189781"
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
Ja, en innsender av en arbeidsflyt kan også godkjenne arbeidsflyten hvis den er konfigurert slik. Du kan unngå denne virkemåten ved å sette **Arbeidsflytparametere > Generelt > Godkjenner > Sperr godkjenning av innsender** til **Ja**.

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

Hvis en bruker ikke får riktig varsling fra handlingssenteret når de tilordnes et arbeidselement for arbeidsflyt, bruker du [Forretningshendelser for arbeidsflyt](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) med Microsoft Flow til å gi flere eller andre varslinger.
