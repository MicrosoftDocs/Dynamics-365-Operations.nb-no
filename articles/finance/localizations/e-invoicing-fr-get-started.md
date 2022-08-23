---
title: Komme i gang med tillegget Elektronisk fakturering for Frankrike
description: Denne artikkelen emnet inneholder informasjon som vil hjelpe deg med å komme i gang med tillegget Elektronisk fakturering for Frankrike.
author: dkalyuzh
ms.date: 07/07/2022
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-00-02
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: 365316b204b6d76fa6ee6b2402fefee50c8ff3ef
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220658"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-france"></a>Komme i gang med tillegget Elektronisk fakturering for Frankrike

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Denne artikkelen inneholder informasjon som vil hjelpe deg med å komme i gang med elektronisk fakturering for Frankrike. Det leder deg gjennom konfigurasjonstrinnene som er landsavhengige i Regulatory Configuration Service (RCS). Denne fremgangsmåten utfyller fremgangsmåten som beskrives i [Kom i gang med tillegget for elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Landspesifikk konfigurasjon for funksjon for elektronisk fakturering for innsending av French Chorus Pro (FR)

Du må konfigurere den elektroniske faktureringsfunksjonen **French Chocor Pro-innsending (FR)** for elektronisk fakturering. Noen av parameterne fra konfigurasjonen er publisert med standardverdier. Disse verdiene må gjennomgås og oppdateres slik at de gjenspeiler forretningsoperasjonene dine på en bedre måte.

### <a name="prerequisites"></a>Forutsetninger

Før du begynner fremgangsmåtene i denne artikkelen, må følgende forutsetninger være fullført:

- Gjør deg kjent med elektronisk fakturering. For mer informasjon kan du se [Oversikt over elektronisk fakturering](e-invoicing-service-overview.md).
- Registrer deg for RCS, og definer elektronisk fakturering. Hvis du vil ha mer informasjon, kan du se følgende artikler:

    - [Registrere deg for og installere tjenesten for elektronisk fakturering](e-invoicing-sign-up-install.md)
    - [Konfigurere Azure-ressurser for elektronisk fakturering](e-invoicing-set-up-azure-resources.md)
    - [Installere tilleggsprogrammet for mikrotjenester i Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md)
    - [Aktiver og konfigurer integrering med elektronisk fakturering](e-invoicing-activate-setup-integration.md) – Bruk informasjonen i denne artikkelen for å aktivere integreringen mellom Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management og tjenesten for elektronisk fakturering.
    - [NAF-koder og siret-numre](emea-fra-naf-codes-siret-numbers.md) og [Definer NAF-koder og Siret-numre](tasks/fr-00003-naf-codes-siret-numbers.md) – Bruk informasjonen i disse artikler til å definere NAF-koder og Siret-numre i juridiske enheter. 

- Organisasjonen må være registrert for at de skal kunne fungere med Chorus Pro. Microsoft tilbyr integrasjon med Chorus Pro i OAuth2-modus via et programmeringsgrensesnitt (API). Hvis du vil ha detaljert informasjon om Cho Pro-registrering og programaktivering, kan du se den [offisielle dokumentasjonen](https://communaute.chorus-pro.gouv.fr/documentation/help-for-api-developers-in-oauth2-mode/).

    Følg denne fremgangsmåten for å registrere deg med Chorus Pro.

    1. Gå til [PISTE-portalen](https://piste.gouv.fr/en/component/apiportal/registration) for å starte registreringen. 
    2. Registrer et program og aktiver Open Authorization-legitimasjon (OAuth).
    3. Kopier og lagre klient-ID-en for OAuth-legitimasjonen og den hemmelige nøkkelen. Du vil bruke denne informasjonen i senere trinn.
    4. Gå til [Chorus Pro-portalen for](https://portail.chorus-pro.gouv.fr/aife_csm/?id=aife_enrollment) å registrere deg. 
    5. Opprett en teknisk konto for API-tilgang. Hvis du vil ha mer informasjon , kan du se [Oppretting av en teknisk konto for API-tilgang i produksjon](https://communaute.chorus-pro.gouv.fr/documentation/creation-of-a-technical-account-for-an-api-access-in-production/).
    6. Kopier bruker-ID-en for den tekniske kontoen og passordet. Du vil bruke denne informasjonen i senere trinn.

## <a name="country-specific-configuration-of-the-application-setup-for-the-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Landspesifikk konfigurasjon for programoppsettet for funksjon for elektronisk fakturering for fransk Chorus Pro-innsending (FR)

Noen av parameterne fra den elektroniske faktureringsfunksjonen **Fransk Chorus Pro-innsending (FR)** publiseres med standardverdier. Før du ruller ut den elektroniske faktureringsfunksjonen til tjenestemiljøet, går du gjennom og oppdaterer standardverdiene etter behov, slik at de bedre gjenspeiler forretningsoperasjonene.

1. I Azure Key Vault oppretter du hemmelighet eller den tilsvarende referansen til dem. Hvis du vil ha mer informasjon , kan du se [Kundesertifikater og hemmeligheter](e-invoicing-customer-certificates-secrets.md).
2. Importer den nyeste versjonen av globaliseringsfunksjonen **Fransk Chorus Pro-innsending (FR)** som beskrevet i [Importere funksjoner fra det globale repositoriet](e-invoicing-import-feature-global-repository.md).
3. Lag en kopi av den importerte globaliseringsfunksjonen, og velg konfigurasjonsleverandøren. For mer informasjon kan du se [Opprett en globaliseringsfunksjon](e-invoicing-create-new-globalization-feature.md).
4. I fanen **Versjoner** kontrollerer du at versjonen **Utkast** er valgt.
5. Velg konfigurasjonen for funksjonen **UBL-salgsfaktura avledet** i rutenettet i **Konfigurasjoner**-fanen.
6. Velg **Rediger**, og deretter på fanen **Behandlingsforløp**, i delen **Behandlingsforløp** velger du **(Forhåndsversjon) Integrer med fransk Chorus Pro** med handlingsnavnet **Fransk Chorus Pro-innsending**.
7. I feltet **Navn på klient-ID-hemmelighet** i **Parametere**-delen velger du det hemmelige navnet du opprettet for klient-ID-en i nøkkelhvelvet.
8. I feltet **Hemmelig navn på klienthemmelighet** velger du det hemmelige navnet du opprettet for klienthemmeligheten i nøkkelhvelvet.
9. I feltet **Hemmelig navn for teknisk pålogging** velger du det hemmelige navnet du opprettet for den tekniske kontopåloggingen i nøkkelhvelvet.
10. I feltet **Hemmelig navn for teknisk passord** velger du det hemmelige navnet du opprettet for den tekniske kontopassordet i nøkkelhvelvet.
11. På fanen **Behandlingsforløp**, i delen **Behandlingsforløp** velger du **Integrer med fransk Chorus Pro** med handlingsnavnet **Fransk Chorus Pro-forespørselsstatus**.
12. I feltet **Navn på klient-ID-hemmelighet** i **Parametere**-delen velger du det hemmelige navnet du opprettet for klient-ID-en i nøkkelhvelvet.
13. I feltet **Hemmelig navn på klienthemmelighet** velger du det hemmelige navnet du opprettet for klienthemmeligheten i nøkkelhvelvet.
14. I feltet **Hemmelig navn for teknisk pålogging** velger du det hemmelige navnet du opprettet for den tekniske kontopåloggingen i nøkkelhvelvet.
15. I feltet **Hemmelig navn for teknisk passord** velger du det hemmelige navnet du opprettet for den tekniske kontopassordet i nøkkelhvelvet.
16. Velg **Lagre**, og lukk deretter siden.
17. Gjenta trinn 6 til og med 16 for funksjonsoppsettet **UBL-prosjektfaktura avledet**, funksjonsoppsettet **UBL-salgskreditnota avledet** og funksjonsoppsettet **UBL-prosjektkreditnota avledet**.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over tillegg for elektronisk fakturering](e-invoicing-service-overview.md)
- [Komme i gang med tjenesteadministrasjon for tillegget for elektronisk fakturering](e-invoicing-get-started-service-administration.md)
- [Komme i gang med Elektronisk fakturering-tillegget](e-invoicing-get-started.md)
