---
title: Regulatory Configuration Service (RCS) – avskrivning av lager for Lifecycle Services (LCS)
description: Dette emnet gir informasjon om avskrivning av lager for Microsoft Dynamics Lifecycle Services (LCS) som er planlagt som en del av utrullingen av det globale repositoriet for Regulatory Configuration Service (RCS).
author: JaneA07
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, LCS storage, LCS storage deprecation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.19
ms.openlocfilehash: 68f1ed6a6d6bb0d15a81539da7f483ad71a4d696
ms.sourcegitcommit: 477efa4cb138f41d4f68bcd82552af3473bcc3d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/29/2021
ms.locfileid: "7715236"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>Regulatory Configuration Service (RCS) – avskrivning av lager for Lifecycle Services (LCS)

[!include [banner](../includes/banner.md)]

Bruken av Microsoft Dynamics Lifecycle Services (LCS) som et lagringsrepositorium for konfigurasjoner for elektronisk rapportering (ER) blir avskrevet. Denne avskrivningen omfatter følgende endringer:

- Microsoft-produserte konfigurasjoner som brukes i Microsoft Dynamics 365-programmer, publiseres ikke lenger i det delte aktivabiblioteket i LCS. De blir i stedet bare publisert via det globale RCS-repositoriet. Konfigurasjonene for Dynamics AX 2012 blir imidlertid fortsatt publisert i det delte aktivabiblioteket i LCS til kundestøttelivssyklusen for AX 2012 slutter.
- Funksjonaliteten som lar deg laste opp konfigurasjoner til prosjektaktivabiblioteket i LCS fra Finance and Operations-apper og RCS, deaktiveres. Du kan imidlertid fortsatt bruke nettleseren i LCS til å laste opp konfigurasjoner til prosjektaktivabiblioteket. Du kan derfor fortsatt legge til konfigurasjoner i LCS, slik at de kan tas med i løsningspakker.
- Import av konfigurasjoner fra LCS er fortsatt tilgjengelig og støttes i Finance and Operations-apper og RCS en stund. Funksjonaliteten kommer imidlertid omsider til å bli avskrevet. (Den nøyaktige avskrivningsdatoen blir kunngjort senere.)

## <a name="deprecation-notice"></a>Avskrivningsvarsel

Avskrivning av bruken av LCS som lager ble meddelt i [Funksjoner som er fjernet eller avskrevet i Dynamics 365 Finance – avskrivningsvarsel for LCS](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Den planlagte avskrivningsdatoen er 1. april 2022.

## <a name="key-features"></a>Hovedfunksjoner

- Bruk RCS til å opprette og redigere ER-konfigurasjoner og globaliseringsfunksjoner.
- Skyv konfigurasjoner direkte fra RCS-designeren til et tilkoblet program, for eksempel et Dynamics 365 Finance miljø, slik at du raskt kan foreta og teste endringer i konfigurasjonene.
- Lagre, del og administrer livssyklusen sentralt for både ER-konfigurasjoner og globaliseringsfunksjoner via det globale repositoriets sentraliserte lagring.

## <a name="guidance-for-one-time-and-ongoing-actions"></a>Veiledning for engangshandlinger og pågående handlinger

Denne delen beskriver et sett med trinn som må fullføres én gang. Den beskriver også trinn som må fullføres fortløpende etterpå.

### <a name="one-time-action"></a>Engangshandling

Importer alle nødvendige konfigurasjoner fra LCS til RCS, og publiser dem deretter i det globale repositoriet fra RCS. Hvis du bruker prosjektspesifikke aktivabibliotek til å lagre avledede konfigurasjoner i LCS, må følgende trinn fullføres mens LCS fortsatt er tilgjengelig.

1. Hvis en RCS-forekomst ikke allerede er tilgjengelig, klargjør du en. Hvis du vil ha mer informasjon, kan du se [Oversikt over RCS](rcs-overview.md).
2. I den klargjorte RCS-forekomsten registrerer du det aktuelle LCS-repositoriet for hvert LCS-prosjekt i aktivabiblioteket som omfatter avledede ER-konfigurasjoner.
3. Importer ER-konfigurasjonene fra LCS-repositoriene til RCS. Hvis du vil ha mer informasjon, kan du se [Importere konfigurasjoner fra LCS](../../dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services.md).
4. Hvis det globale repositoriet ikke gis automatisk, registrerer du det i RCS.
5. Last opp alle avledede konfigurasjoner fra den gjeldende RCS-forekomsten til det globale repositoriet. Bruk funksjonen **Konfigurasjonspakker** som hjelp til opplastingen. Hvis du vil ha mer informasjon, kan du se [Opplasting til globalt RCS-repositorium](rcs-global-repo-upload.md).

### <a name="going-forward"></a>De neste trinnene

Bruk de visuelle designerne i RCS til følgende formål:

- Utvid malene som følger med Microsoft.
- Opprett nye konfigurasjoner som organisasjonen krever.
- Tilpass globaliseringsfunksjoner for elektronisk fakturering og avgiftsberegningstjenesten.

Bruk globaliseringsrepositoriet i RCS til følgende formål:

- Få tilgang til Microsoft-produserte konfigurasjoner og globaliseringsfunksjoner.
- Last opp konfigurasjoner du har opprettet eller utvidet til det globale repositoriet for lagring, og del dem på tvers av organisasjonens Dynamics 365-programmiljøer eller med eksterne organisasjoner. Hvis du vil ha mer informasjon, kan du se [Opprette ER-konfigurasjon i RCS og laste opp til globalt repositorium](rcs-global-repo-upload.md).

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>Betyr denne endringen at LCS ikke kan brukes som sentralt lager for konfigurasjoner?

Ja. Funksjonaliteten som lar deg laste opp konfigurasjoner til prosjektaktivabiblioteket i LCS fra Finance and Operations-apper, kommer til å bli avskrevet. Du kan imidlertid fortsatt bruke nettleseren i LCS til å laste opp konfigurasjoner til prosjektaktivabiblioteket etter behov.

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>Jeg trodde at RCS var et erstatningsrepositorium for import av globale malfiler. Jeg trodde ikke det ble brukt til å lagre konfigurasjoner. Hva er riktig?

RCS er en utformingstjeneste for oppretting og redigering av ER-konfigurasjoner. RCS har et eget repositorium som kalles for det globale repositoriet. Dette repositoriet brukes til å lagre konfigurasjoner som opprettes i RCS. Etter at bruken av LCS som lager, er avskrevet, blir det globale repositoriet enkeltkilden for Microsoft-konfigurasjoner. Du må fullføre en engangshandling for å importere alle konfigurasjonene du har behov for, fra LCS til RCS, og deretter publisere dem i det globale repositoriet fra RCS.

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>Hvordan kan konfigurasjoner lagres uten LCS slik at test- og produksjonskonfigurasjoner enkelt kan administreres og overføres?

RCS bruker konseptet *tilkoblet program*. Et tilkoblet program danner en tilkobling mellom RCS og enhver forekomst av Finance and Operations-apper. Siden RCS kan brukes til å redigere konfigurasjoner, kan det tilkoblede programmet brukes til å sende konfigurasjonene direkte fra utformingen til miljøer for Finance and Operations-apper. Du kan derfor raskt endre og teste konfigurasjonene i stedet for å måtte gå gjennom lager for LCS på prosjektnivå.

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>Finnes det noen eksempler der konfigurasjon og administrasjon vises?

Det finnes ingen eksempler, men du kan fullføre trinnene tidligere i dette emnet for å overføre konfigurasjonene til det globale RCS-repositoriet.

### <a name="is-rcs-a-prerequisite-to-configure-electronic-reporting"></a>Er RCS en forutsetning for å konfigurere elektronisk rapportering?

Ja. RCS inneholder funksjoner som støtter oppsettet av globaliseringsfunksjoner som brukes av globaliseringstjenester som elektronisk fakturering og Skatteberegningstjenesten. Tjenesten har imidlertid samme funksjonalitet for visuell utforming som gjør det mulig å utvide eller opprette nye ER-konfigurasjoner. RCS gir også styring av livssykluser for både ER-konfigurasjoner og globaliseringsfunksjoner.

### <a name="which-regions-can-rcs-be-deployed-in"></a>Hvilke områder kan RCS distribueres i?

RCS er tilgjengelig i følgende Azure-områder:

- USA
- India
- Frankrike
- Europa

Hvis du vil ha mer informasjon om produktstøtte, kan du se [oversikten over dynamiske globaliseringstjenester](globalization-services-overview.md). Hvis du vil ha mer informasjon om geografisk støtte, kan du se [Dynamics 365 og Power Platform: Tilgjengelighet, dataplassering, språk og lokalisering](https://aka.ms/rcs/D365Productavailabilityguide).

### <a name="whats-the-cost-of-using-rcs"></a>Hva er kostnaden ved å bruke RCS?

RCS og Globaliseringsrepositoriet leveres gratis som del av eksisterende Finance and Operations-applisenser. Ingen separate kostnader er tilknyttet bruk av RCS-designtjenesten eller lagring av konfigurasjoner i det globale repositoriet. Det er for øyeblikket ingen grense for antall konfigurasjoner eller tilkoblede programmer.
