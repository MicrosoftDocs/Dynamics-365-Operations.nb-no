---
title: Distribuere en ny e-handelsleier
description: Dette emnet beskriver hvordan du distribuerer en ny e-handelsleier ved å bruke Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2632632b9b21dd3a88e9a4df0e65cfd28e579d2
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697457"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Distribuere en ny e-handelsleier

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du distribuerer et nytt e-handelsområde ved å bruke Microsoft Dynamics Lifecycle Services (LCS).

## <a name="overview"></a>Oversikt
    
Microsoft Dynamics Lifecycle Services (LCS) er et skybasert samarbeidsområde som partnere og kunder kan bruke til å administrere sine prosjekter og miljøer, vise nyeste informasjon om Microsoft Dynamics-produkter og -funksjoner og opprette, spore og bla gjennom kundestøttehendelser. Funksjoner for e-handelsadministrasjon er integrert i LCS.

Hvis du vil vite mer om LCS, se [Brukerveiledning for Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).
    
## <a name="get-started"></a>Komme i gang

Før du kan initialisere e-handel, må du initialisere et prosjekt, et miljø og en Retail Cloud Scale Unit (RCSU). Hvis du vil utføre initialiseringen i LCS, må du ha tillatelse til rollen Prosjekteier eller rollen Miljøadministrator. Produksjons- og sandkassemiljøtopologiene støttes.

Hvis du vil ha mer informasjon om miljøene, se [Miljøplanlegging](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning). Hvis du vil ha mer informasjon om RCSU, se [Initialisere Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).

## <a name="initialize-e-commerce"></a>Initialisere e-handel

Bruk denne fremgangsmåten for å initialisere e-handel-funksjonen i et eksisterende miljø.

Før du begynner må du kontrollere at du har følgende nødvendige informasjon:

- RCSU som blir brukt.
- Microsoft Azure Active Directory-sikkerhetsgruppen som skal brukes til systemansvarlige i e-handel.
- Microsoft Azure Active Directory-sikkerhetsgruppen som skal brukes for vurderings- og omtalemoderatorer.
- Domenene som skal knyttes til miljøet.

I tillegg kan du samle inn følgende valgfrie opplysninger:

- Azure AD-forretning-til-forbruker-informasjon (B2C):

    - Navn på leietaker.
    - Klient-ID.
    - Egendefinert domene for pålogging.
    - Svar-URL.
    - Policy-ID for registrering/pålogging.
    - Policy-ID for tilbakestilling av passord.
    - Policy-ID for redigering av profil.

[!NOTE]
Denne informasjonen kan legges til senere, via en serviceforespørsel.

Når du har samlet inn den nødvendige informasjonen, følger du denne fremgangsmåten for å initialisere e-handel.

1. Logg på [LCS](https://lcs.dynamics.com).
1. Åpne prosjektet som inneholder miljøet der du vil initialisere e-handel.
1. Velg miljøet i delen **Miljøer**.
1. Under **Miljøfunksjoner** velger du koblingen **Detaljhandelsstyring**.
1. Velg **Oppsett** i kategorien **e-handel**. Det vises en dialogboks der du må skrive inn informasjonen som kreves for klargjøring.
1. Fyll inn nødvendig informasjon, og gå deretter til neste side.
1. På neste side fyller du ut nødvendig informasjon, og deretter sender du inn skjemaet. Du kommer tilbake til kategorien **e-handel**, der du skal se at initialiseringen er startet.
1. Hvis du vil vise initialiseringsegenskaper, kan du velge **Oppdater** eller gå tilbake til **e-handel**.
    
Når e-handel startes fra LCS, klargjør systemet flere komponenter som kreves for e-handel, og knytter dem til miljøet. Når klargjøringen er fullført, oppdateres kategorien **e-handel** på siden **Detaljhandelsstyring** for å gjenspeile klargjøringen. Siden viser de siste tilpasningsdistribusjonene og statusen til eventuelle andre pågående distribusjoner. Den inneholder også koblinger til webområdet for e-handel og områdeadministrasjonsverktøyet for e-handel (redigeringsverktøyet).

## <a name="access-the-authoring-environment"></a>Få tilgang til redigeirngsmiljøet

Du får tilgang til redigeringsmiljøet ved å gå til kategorien **e-handel** på siden **Detaljhandelsstyring**. Der finner du koblinger til e-handelsområdet og områdebehandlingsverktøyet.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over nettbutikk](online-store-overview.md)

[Opprette et e-handelsområde](create-ecommerce-site.md)

[Knytte et nettområde til en kanal](associate-site-online-store.md)

[Konfigurere domenenavnet](configure-your-domain-name.md)

[Legge til støtte for et innholdsleveringsnettverk (CDN)](add-cdn-support.md)

[Aktivere stedsbasert butikkregistrering](enable-store-detection.md)

[Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md)
