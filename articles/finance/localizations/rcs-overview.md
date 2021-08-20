---
title: Regulatory Configuration Service
description: Dette emnet gir en oversikt over funksjonene i RCS (Regulatory Configuration Service), og forklarer hvordan du får tilgang til tjenesten.
author: JaneA07
ms.date: 06/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 4ee68b691bba7f3314b5278b0bcc26504c1583335914a1e7c645abd5303f02c6
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012019"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

RCS (Regulatory Configuration Service) er en frittstående designer og livssyklusadministrasjonstjeneste for globaliseringsfunksjonalitet med ingen kode / lav kode. RCS lar globaliseringspartnere utvide og tilpasse viktige globaliseringsområder for skatt, e-fakturering, forskriftsmessige rapportering, bank- og forretningsdokumenter uten at de trenger å involvere utviklere. Denne globaliseringsmåten med ingen kode / lav kode gjør globaliseringen enklere, raskere og mer kostnadseffektivt å opprette eller forlenge.

RCS har følgende funksjoner:

- Støtte for all funksjonalitet som leveres av Elektronisk rapportering (ER).
- En forutsetning for å konfigurere nye globaliseringsmikrotjenester.
- Støtte for elektronisk fakturering. For mer informasjon, se [Elektronisk fakturering](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).
- Støtte for avgiftsberegning. Hvis du vil ha mer informasjon, kan du se [Avgiftstjeneste](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).
- Støtte for ny globaliseringsfunksjonalitet som forenkler livssyklusadministrasjon av funksjoner for flere komponenter og gir ekstra funksjoner til å konfigurere handlinger og definere funksjonsparametere. Hvis du vil ha mer informasjon, kan du se [Regulatory Configuration Service – forenklet administrasjon av globaliseringsfunksjon for globaliseringstjenester](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).
- Støtte for sentralisert publisering, lagring og deling av egendefinerte konfigurasjoner i det globale repositoriet for å forenkle konfigurasjonsadministrasjon uten å kreve bruk av Microsoft Dynamics Lifecycle Services (LCS).

## <a name="access-rcs"></a>Tilgang til RCS

Du kan registrere deg for eller logge deg på RCS fra [Regulatory Configuration Service-siden](https://marketing.configure.global.dynamics.com/).

![Registrering for / pålogging på RCS.](media/202103_RCS%20Marketing%20page_updated_1.jpg)

På **Regulatory Configuration Service**-siden må du gå gjennom og godta tilleggsbetingelsene for bruk av tjenesten, og deretter velger du en av følgende knapper:

- **Registrer deg** hvis du er en førstegangsbruker av tjenesten, og du bruker en e-postadresse for forretningsvirksomhet til å klargjøre organisasjonen for et servicemiljø.
- **Logg på** hvis du tidligere har registrert deg for tjenesten, og du ønsker å få tilgang til organisasjonsmiljøet

> [!NOTE] 
> Når du har registrert deg, anbefaler vi at du legger til en ekstra SysAdmin-bruker i RCS-miljøet. Denne brukeren blir klargjort som medadministrator for miljøet. Dette vil bidra til å sørge for at tilgangen til RCS-miljøet opprettholdes, fordi SysAdmin-rollen er å administrere brukere i dette miljøet. Du kan legge til brukere ved hjelp **RCS-arbeidsområde > Systemadministrasjon**.

## <a name="regional-availability"></a>Regional tilgjengelighet

RCS er allment tilgjengelig i følgende områder:

- USA
- India
- Frankrike
- Europa

For en komplett liste over områder kan du se [Dynamics 365 og Power Platform: Tilgjengelighet, dataplassering, språk og lokalisering](https://aka.ms/dynamics_365_international_availability_deck).

## <a name="rcs-default-company"></a>Standardfirma for RCS

Funksjonaliteten for utformingstid som brukes i RCS, deles på tvers av alle firmaer. Det finnes ingen firmaspesifikk funksjonalitet. Vi anbefaler derfor at du bruker ett firma, **DAT**, med RCS-miljøet.

I enkelte scenarioer ønsker du imidlertid kanskje at ER-formater bruker parametere som er knyttet til en bestemt juridisk enhet. Det er bare i disse scenarioene du bør bruke bryteren for standardfirma. Hvis du vil ha et eksempel, kan du se [Konfigurere ER-formater slik at de brukere parametere som angis per juridisk enhet](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).

## <a name="related-rcs-documentation"></a>Relatert RCS-dokumentasjon

Hvis du vil ha mer informasjon om relaterte komponenter, kan du se følgende emner:

- **RCS:**

    - [Opprette ER-konfigurasjoner i RCS og laste dem opp til det globale repositoriet](rcs-global-repo-upload.md)

- **Globalt repositorium:**

    - [Opprett ER-konfigurasjon og last opp til globalt repositorium](rcs-global-repo-upload.md)
    - [Del konfigurasjon i globalt repositorium](rcs-global-repo-share-configuration.md)
    - [Forbedret filtrering i globalt repositorium](enhanced-filtering-global-repo.md)
    - [Last ned ER-konfigurasjoner fra det globale repositoriet](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [Avslutt konfigurasjoner i globalt repositorium](discontinuing-configurations-rcs-global-repo.md)
    - [Regulatory Configuration Service (RCS) – avskrivning av lager for Lifecycle Services (LCS)](rcs-lcs-repo-dep-faq.md)

- **Globaliseringsfunksjon:**

    - [Regulatory Configuration Service (RCS) – globaliseringsfunksjon](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a>Feilsøke RCS-registrering

Når du registrerer deg for RCS på tjenestesiden, kan det oppstå et problem knyttet til Azure Active Directory (Azure AD). Feilmeldingen du får, angir at registreringen for RCS er deaktivert og må aktiveres før du kan fullføre registreringsprosessen.

![Feilmelding ved RCS-registrering.](media/01_RCSSignUpError.jpg)

Problemet oppstår fordi du er blokkert fra å registrere deg for adhocabonnementer, og egenskapen `AllowAdHocSubscriptions` må aktiveres i leieren din. 

- Hvis IT-avdelingen administrerer organisasjonens Azure-leiere, kan du kontakte denne avdelingen for å rapportere problemet.
- Hvis du er ansvarlig for å administrere Azure-leiere, kan du løse problemene ved å følge trinnene i [Hva er selvbetjent registrering for Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).
