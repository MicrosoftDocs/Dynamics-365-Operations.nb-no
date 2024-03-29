---
title: Vanlige spørsmål om arbeidsflyt
description: Denne artikkelen gir svar på vanlige spørsmål om arbeidsflytsystemet.
author: ChrisGarty
ms.date: 03/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a72fd141bb1178a3a83385c512d1a655064d5b00
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896586"
---
# <a name="workflow-faq"></a>Vanlige spørsmål om arbeidsflyt

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Denne artikkelen gir svar på vanlige spørsmål om arbeidsflytsystemet.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Hvorfor mottas flere varslinger når et arbeidselement avvises?
Når et arbeidselement avvises, fullføres dette arbeidselementet som avvist. Et annet arbeidselement opprettes og tilordnes til avsenderen. Dette betyr at det er en melding til avsenderen for det avviste arbeidselementet og en egen melding til brukeren som er tilordnet til det nye "bedt om endring"-arbeidselementet. 

Hver varsling er for et annet arbeidselement, men likheten kan føre til forvirring. Vi ser på måter å forbedre dette på i fremtidige versjoner.

## <a name="why-are-my-workflow-exports-failing"></a>Hvorfor mislykkes arbeidsflyteksportene mine?
Det er for øyeblikket en begrensning i funksjonen for arbeidsflyteksport som hindrer at arbeidsflytnavn overskrider 48 tegn. Hvis du bruker et navn som er lengre enn 48 tegn, kan det resultere i feilen «Serveren kan ikke godkjenne forespørselen» og/eller hindre at en fil blir eksportert uten en filtype. Følgende blogginnlegg gir mer informasjon: [Feilsøke arbeidsflyteksport](https://community.dynamics.com/365/financeandoperations/b/elandaxdynamicsaxupgradesanddevelopment/posts/workflow-export-troubleshooting).

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
    - [Arbeidsflyter har forretningshendelser](../../dev-itpro/business-events/business-events-workflow.md) som kunden kan bruke til å utløse flyter som har varslingene de ser etter.   

Hvis en bruker ikke får riktig varsling fra handlingssenteret når de tilordnes et arbeidselement for arbeidsflyt, bruker du [Forretningshendelser for arbeidsflyt](../../dev-itpro/business-events/business-events-workflow.md) med Microsoft Power Automate til å gi flere eller andre varslinger.

## <a name="why-is-workflow-editor-not-able-to-start-under-ad-fs"></a>Hvorfor kan ikke arbeidsflytredigering starte under AD FS?
Når du kjører under Active Directory Federation Services (AD FS) i et oppgradert miljø, kan redigeringsprogrammet for arbeidsflyt ha problemer med å starte. I så fall må du kontrollere at URL-en "https://dynamicsaxworkfloweditor/" er lagt til i egenskapen **Microsoft Dynamics 365 for Operations Lokalt - Arbeidsflyt - Opprinnelig program** i ADFS-innstillingene.

## <a name="why-am-i-getting-sql-deadlocks-on-workflow-processing"></a>Hvorfor får jeg SQL-vranglås i arbeidsflytbehandling? 
Standard feltverdi for **Antall arbeidsflytvarer per satsvis oppgave** på siden **Arbeidsflytparametere** er 0. Verdien 0 gjør at standard virkemåte er å endre til 20 elementer per bunke. Vær forsiktig når du justerer denne verdien, fordi et høyt antall varer per parti (> 40) kan forårsake SQL-vranglåser.

## <a name="what-is-the-workflow-enhanced-error-feature"></a>Hva er funksjonen for forbedret feil i arbeidsflyten?
Funksjonen for forbedret feil i arbeidsflyten i versjon 10.0.13 legger til feilkoder for å skille ulike klasser av arbeidsflytfeil. Feilmeldingene som rapporteres, vil for det meste være like, med mindre forskjeller for å få dem til å bli klarere.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
