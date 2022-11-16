---
title: Konfigurer CPOS for å bruke en egendefinert Azure AD-app
description: Denne artikkelen beskriver hvordan du konfigurerer Cloud POS (CPOS) for å bruke en egendefinert Azure Active Directory-app (Azure AD).
author: boycez
ms.date: 11/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 5e4ff797410e1e94869cc37684e7622ec0d97842
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746267"
---
# <a name="configure-cpos-to-use-a-custom-azure-ad-app"></a>Konfigurer CPOS for å bruke en egendefinert Azure AD-app

[!include [banner](includes/banner.md)]

Som standard peker Cloud POS (CPOS) i Microsoft Dynamics 365 Commerce peker til en registrert førsteparts Microsoft-app i Azure Active Directory (Azure AD). Derfor kan du bruke CPOS uten å gjøre noen endringer i Azure AD. Det kan imidlertid være at du vil peke forekomsten av CPOS til en egendefinert Azure AD-app du styrer. Denne artikkelen beskriver hvordan du konfigurerer Cloud POS for å bruke en egendefinert Azure AD-app.

## <a name="set-up-a-custom-retail-server-app-in-azure-ad"></a>Konfigurer en egendefinert Retail Server-app i Azure AD

Følg denne fremgangsmåten for å opprette og konfigurere en egendefinert Retail Server-app i Azure AD.

1. Logg deg på [Azure Active Directory-administrasjonssenteret](https://aad.portal.azure.com) med en Azure AD-brukerkonto. Brukerkontoen behøver ikke å ha administratortillatelser.
1. Velg **Azure Active Directory**.
1. Velg **Appregistreringer**, og velg deretter **Ny registrering** for å åpne dialogboksen **Registrer en søknad**.
1. Angi følgende felter:

    - **Navn** – Angi et egendefinert navn for appen. Skriv for eksempel inn **Egendefinert Retail Server**.
    - **Støttekontotyper** – Velg standardalternativet, **Bare kontoer i denne organisasjonskatalogen (bare Microsoft – enkelt leietaker)**.
    - **URI for omdirigering** – Dette feltet er valgfritt. La den stå tom.
    - **Tjenestetre-ID** – Dette feltet er valgfritt. La den stå tom.
    
1. Velg **Registrer**. Konfigurasjonssiden for den nyregistrerte appen vises.
1. Velg **Legg til en app-ID-URI** i delen **Oversikt \> Essentials**, og velg deretter **Angi** ved siden av **App-ID-URI**. Noter den foreslåtte verdien, og velg deretter **Lagre** for å godta denne verdien. 
1. Velg **Legg til et område**, og deretter angi følgende felter:

    - **Områdenavn** – Angi et egendefinert navn for området. Skriv for eksempel inn **Legacy.Access.Full**.
    - **Hvem kan samtykke** – Angi om både administratorer og brukere eller bare administratorer kan gi tillatelse, basert på organisasjonens sikkerhetsretningslinjer.
    - **Visningsnavn for administratortillatelse** – Angi et visningsnavn. Skriv for eksempel inn **Få tilgang til Retail Server**.
    - **Administratorsamtykkebeskrivelse** – Angi en beskrivelse. Skriv for eksempel inn **Gir tilgang til Retail Server-API-er**.

1. Velg **Legg til område** for å fullføre områdeopprettingsprosessen.

## <a name="set-up-a-custom-cpos-app-in-azure-ad"></a>Definer en egendefinert CPOS-app i Azure AD

> [!IMPORTANT]
> Hvis du oppgraderer en eksisterende egendefinert CPOS Azure AD-app som ble laget før Commerce versjon 10.0.21, følger du fremgangsmåten i [Oppgrader en eksisterende egendefinert CPOS Azure AD-app laget før Commerce versjon 10.0.21](#upgrade-an-existing-custom-cpos-azure-ad-app-created-before-commerce-version-10021).

Følg denne fremgangsmåten for å opprette og konfigurere en egendefinert CPOS-app i Azure AD.

1. Logg deg på [Azure Active Directory-administrasjonssenteret](https://aad.portal.azure.com) med en Azure AD-brukerkonto. Brukerkontoen behøver ikke å ha administratortillatelser.
1. Velg **Azure Active Directory**.
1. Velg **Appregistreringer**, og velg deretter **Ny registrering** for å åpne dialogboksen **Registrer en søknad**.
1. Angi følgende felter:

    - **Navn** – Angi et navn for appen. Skriv for eksempel inn **Egendefinert Cloud POS**.
    - **Støttekontotyper** – Velg standardalternativet, **Bare kontoer i denne organisasjonskatalogen (bare Microsoft – enkelt leietaker)**.
    - **Omdirigerings-URI** – Velg **App med én side (SPA)** i rullegardinlisten, og angi deretter CPOS-URI-en.
    - **Tjenestetre-ID** – Dette feltet er valgfritt. La den stå tom.

1. Velg **Registrer**. Konfigurasjonssiden for den nyregistrerte appen vises.
1. Sett parameterne **oauth2AllowIdTokenImplicitFlow** og **oauth2AllowImplicitFlowtil** **sann**, og velg deretter **Lagre** i delen **Manifest**.
1. I **Tokenkonfigurasjon**-delen følger du disse trinnene for å legge til to krav:

    1. Velg **Legg til tilleggskrav**. Sett **Tokentype**-feltet til **ID**, og velg deretter **sid**-kravet . Velg **Legg til**.
    1. Velg **Legg til tilleggskrav**. Sett **Tokentype**-feltet til **Tilgang**, og velg deretter **sid**-kravet . Velg **Legg til**.

1. I delen **API-tillatelser** velger du **Legg til en tillatelse**.
1. I fanen **API-er organisasjonen bruker** søker du etter Retail Server-appen som du opprettet i delen [Konfigurer en egendefinert Retail Server-app Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad). Velg deretter **Legg til tillatelser**.
1. I **Oversikt**-delen noterer du deg verdien i feltet **App-ID (klient)**.

### <a name="upgrade-an-existing-custom-cpos-azure-ad-app-created-before-commerce-version-10021"></a>Oppgrader en eksisterende egendefinert CPOS Azure AD-app laget før Commerce versjon 10.0.21

Følg denne fremgangsmåten for å oppgradere en eksisterende egendefinert CPOS Azure AD-app laget før Commerce versjon 10.0.21. 

1. Åpne den egendefinerte CPOS Azure AD-appen i Azure-portalen.
1. Velg fanen **Godkjenning**.
1. Kopier og lagre den opprinnelige URI-en for omdirigering fra **Nett**-typen til senere bruk, og slett den deretter.
1. Velg **Legg til en plattform**, og velg deretter **App med én side (SPA)**.
1. Legg til den opprinnelige URI-en for nettomdirigering du kopierte ovenfor, på SPA-plattformen.
1. I **Tokenkonfigurasjon**-delen følger du disse trinnene for å legge til to krav:
    1. Velg **Legg til tilleggskrav**. Sett **Tokentype**-feltet til **ID**, og velg deretter **sid**-kravet . Velg **Legg til**.
    1. Velg **Legg til tilleggskrav**. Sett **Tokentype**-feltet til **Tilgang**, og velg deretter **sid**-kravet . Velg **Legg til**.

## <a name="update-the-cpos-configuration-file"></a>Oppdater CPOS-konfigurasjonsfilen

Åpne filen CPOS config.json, og gjør følgende oppdateringer i den.

1. Erstatt **AADClientId**-nøkkelverdien med verdien **App-ID (klient)** for den egendefinerte CPOS-appen som du opprettet i delen [Angi en egendefinert CPOS-app i Azure AD](#set-up-a-custom-cpos-app-in-azure-ad).
1. Erstatt **AADRetailServerResourceId**-nøkkelverdien med verdien **App-ID-URI** for den egendefinerte Retail Server-appen som du opprettet i delen [Angi en egendefinert Retail Server-app i Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad).

CPOS vil bruke begge parameterne når det sender forespørsler til Azure AD om å skaffe et sikkerhetstoken.

## <a name="update-identity-providers-settings-in-commerce-headquarters"></a>Oppdater innstillinger for identitetsleverandører i Commerce headquarters

Deretter må du oppdatere innstillinger for identitetsleverandører i Commerce headquarters.

1. I Commerce Headquarters åpner du siden **Commerce-delte parametere**.
1. I fanen **Identitetsleverandører** i delen **Identitetsleverandører** velger du raden der **Type**-feltet er angitt til **Azure Active Directory**, og **Utsteder**-feltet peker til Azure AD-leieren. Denne innstillingen deklarerer at du skal arbeide med underordnede rutenett som inneholder dataene som er relatert til identitetsleverandøren som tilsvarer Azure AD-leieren din.
1. Velg **Legg til** for å legge til en rad i delen **Avhengige parter**.
1. Angi følgende felter:

    - **ClientId** – Angi verdien **App-ID (klient)** for den egendefinerte CPOS-appen som du opprettet i delen [Angi en egendefinert CPOS-app i Azure AD](#set-up-a-custom-cpos-app-in-azure-ad).
    - **Type** – Velg **Offentlig**.
    - **UserType** – Velg **Arbeider**.

1. Merk raden du la til. Delen **Serverressurs-ID-er** under delen **Avhengige parter** viser Retail Server-app-ID-ene som du får tilgang til av appen du valgte i rutenettet **Avhengige parter**.
1. Velg **Legg til** for å legge til en rad i delen **Serverressurs-ID-er**.
1. I feltet **Serverressurs-ID** angir du verdien **App-ID-URI** for den egendefinerte Retail Server-appen som du opprettet i delen [Angi en egendefinert Retail Server-app i Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad).

    > [!IMPORTANT]
    > Alle feltene som er nevnt i de foregående trinnene, skiller mellom store og små bokstaver. Verdiene du angir, må samsvare med verdiene som er konfigurert i Azure AD-administrasjonssenteret.

1. Gå til **IT for Retail og Commerce \> Distribusjonsplan**, og kjør jobben **1110** (**Global konfigurasjon**).

Du kan nå aktivere CPOS-enheter ved hjelp av din egen Azure AD-app.

## <a name="additional-resources"></a>Tilleggsressurser

[Salgspunktenhetsaktivering](dev-itpro/retail-device-activation.md)

[Administrere aktiveringskontoer og validere enheter](set-up-activation-accounts-validate-devices-hq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
