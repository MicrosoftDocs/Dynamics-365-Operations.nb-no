---
title: Regulatory Configuration Service
description: Dette emnet gir en oversikt over funksjonene i RCS (Regulatory Configuration Service), og forklarer hvordan du får tilgang til tjenesten.
author: JaneA07
manager: AnnBe
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ec7e0fe07d979b85109605949b6ba33ab6d99b51
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890806"
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

![Registrering for / pålogging på RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

På **Regulatory Configuration Service**-siden må du gå gjennom og godta tilleggsbetingelsene for bruk av tjenesten, og deretter velger du en av følgende knapper:

- **Registrer deg** hvis du er en førstegangsbruker av tjenesten, og du bruker en e-postadresse for forretningsvirksomhet til å klargjøre organisasjonen for et servicemiljø.
- **Logg på** hvis du tidligere har registrert deg for tjenesten, og du ønsker å få tilgang til organisasjonsmiljøet

## <a name="regional-availability"></a>Regional tilgjengelighet

RCS er allment tilgjengelig i følgende områder:

- USA
- India
- Frankrike
- Europa

For en komplett liste over områder kan du se [Dynamics 365 og Power Platform: Tilgjengelighet, dataplassering, språk og lokalisering](https://aka.ms/dynamics_365_international_availability_deck).

## <a name="related-rcs-documentation"></a>Relatert RCS-dokumentasjon

Hvis du vil ha mer informasjon om relaterte komponenter, kan du se følgende dokumentasjon:

- **Globalt repositorium:**

    - [Opprett ER-konfigurasjon og last opp til globalt repositorium](rcs-global-repo-upload.md)
    - [Del konfigurasjon i globalt repositorium](rcs-global-repo-share-configuration.md)
    - [Forbedret filtrering i globalt repositorium](enhanced-filtering-global-repo.md)
    - [Last ned ER-konfigurasjoner fra det globale repositoriet](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [Avslutt konfigurasjoner i globalt repositorium](discontinuing-configurations-rcs-global-repo.md)

- **Globaliseringsfunksjon:**

    - [Regulatory Configuration Service (RCS) – globaliseringsfunksjon](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)