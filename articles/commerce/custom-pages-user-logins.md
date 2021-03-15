---
title: Definere egendefinerte sider for brukerpålogginger
description: Dette emnet beskriver hvordan du bygger egendefinerte sider i Microsoft Dynamics 365 Commerce som håndterer tilpassede pålogginger for brukere av Azure Active Directory (Azure AD)-firma-til-kunde-leiere (B2C).
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a55da9683c43ac75109fd256e481b02a4d565914
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970084"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>Definere egendefinerte sider for brukerpålogginger


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du bygger egendefinerte sider i Microsoft Dynamics 365 Commerce som håndterer tilpassede pålogginger for brukere av Azure Active Directory (Azure AD)-firma-til-kunde-leiere (B2C).

## <a name="overview"></a>Oversikt

Hvis du vil bruke egendefinerte sider som er forfattet i Dynamics 365 Commerce, til å håndtere brukerpåloggingsflyter, må du definere Azure AD-policyene som det skal refereres til i handelsmiljøet. Du kan konfigurere Azure AD B2C-policyer for registrering og pålogging, profilredigering og tilbakestilling av passord ved hjelp av Azure AD B2C-programmet. Azure AD B2C-leieren og policynavnene kan deretter refereres til under klargjøringsprosessen som utføres for handelsmiljøet, ved å bruke Microsoft Dynamics Lifecycle Services (LCS).

De egendefinerte handelssidene kan bygges ved hjelp av modulen for pålogging, registrering, kontoprofilredigering og tilbakestilling av passord. Det bør deretter refereres til side-URL-adressene som publiseres for disse egendefinerte sidene, i Azure AD B2C-policykonfigurasjoner på Azure-portalen.

## <a name="set-up-b2c-policies"></a>Definere B2C-policyer

Når du konfigurerer Azure AD B2C-leieren og knytter den til handelsmiljøet, går du til **Azure AD B2C**-siden i Azure-portalen, og deretter, på menyen under **Policyer**, velger du **Brukerflyter (policyer)**.

![Brukerflyter (policyer)-kommandoen på menyen](./media/B2C_CustomPage_PoliciesMenu.png)

Nå kan du konfigurere brukerpåloggingsflytene for registrering og pålogging, profilredigering og tilbakestilling av passord.

### <a name="configure-the-sign-up-and-sign-in-policy"></a>Konfigurere policy for registrering og pålogging

Følg denne fremgangsmåten for å konfigurere policyen for registrering og pålogging

1. Velg **Ny brukerflyt**, og deretter, på fanen **Anbefalt**, velger du policyen for **Registrering og pålogging**.
1. Angi et navn for policyen (for eksempel **B2C\_1\_RegistreringPålogging**).
1. I delen **Identitetsleverandører** velger du ID-leverandørene som skal brukes for policyen. Som et minimum må **E-postregistrering** velges.
1. I kolonnen **Innhent attributt** merker du av for avmerkingsboksene for **E-postadresse**, **Gitt navn** og **Etternavn**.
1. I kolonnen **Returkrav** merker du av for **E-postadresser**, **Gitt navn**, **Identitetsleverandør**, **Etternavn** og **Brukers objekt-ID**.

    ![Valgte attributter og krav](./media/B2C_SignInSignUp_Attributes.png)

1. Velg **OK** for å opprette policyen.
1. Dobbeltklikk det nye policynavnet, og velg deretter **Egenskaper** i navigasjonsruten.
1. Sett alternativet for **Aktiver JavaScript-valg av sideoppsett (forhåndsvisning)** til **På**.

    ![Egenskapsside for den nye policyen](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> Policynavnet blir fullstendig referert til i handelsmiljøet. (**B2C\_1\_** vil bli inkludert i referansen.) Policyer kan ikke endres etter at de er opprettet. Hvis du erstatter en eksisterende policy for handelsmiljøet ditt, kan du slette den opprinnelige policyen og bygge en ny policy som har samme navn. Hvis miljøet allerede er klargjort, er det også mulig å sende det nye policynavnet via en tjenesteforespørsel.

Du kommer tilbake til denne policyen for å fullføre oppsettet etter at du har bygget de egendefinerte sidene. Foreløpig lukker du policyen for å gå tilbake til siden **Brukerflyt (policyer)** i Azure-portalen.

### <a name="configure-the-profile-editing-policy"></a>Konfigurere policyen for profilredigering

Hvis du vil konfigurere policyen for profilredigering, gjør du følgende.

1. Velg **Ny brukerflyt**, og deretter, på fanen **Anbefalt**, velger du policyen for **Profilredigering**.
1. Angi et navn for policyen (for eksempel **B2C\_1\_RedigerProfil**).
1. I delen **Identitetsleverandører** velger du ID-leverandørene som skal brukes for policyen. Du må minimum velge **Logg på lokal konto**.
1. I kolonnen **Innhent attributt** merker du av for **E-postadresser** og **Etternavn**.
1. I kolonnen **Returkrav** merker du av for **E-postadresser**, **Gitt navn**, **Identitetsleverandør**, **Etternavn** og **Brukers objekt-ID**.
1. Velg **OK** for å opprette policyen.
1. Dobbeltklikk det nye policynavnet, og velg deretter **Egenskaper** i navigasjonsruten.
1. Sett alternativet for **Aktiver JavaScript-valg av sideoppsett (forhåndsvisning)** til **På**.

Du kommer tilbake til denne policyen for å fullføre oppsettet etter at du har bygget de egendefinerte sidene. Foreløpig lukker du policyen for å gå tilbake til siden **Brukerflyt (policyer)** i Azure-portalen.

### <a name="configure-the-password-reset-policy"></a>Konfigurere policyen for tilbakestilling av passord

Hvis du vil konfigurere policyen for tilbakestilling av passord, gjør du følgende.

1. Velg **Ny brukerflyt**, og deretter, på fanen **Forhåndsvisning**, velger du policyen for **Tilbakestilling av passord v1.1**.

    ![Policy for tilbakestilling av passord v1.1 valgt i kategorien Forhåndsvisning](./media/B2C_ForgetPassword_Menu.png)

1. Angi et navn for policyen (for eksempel **B2C\_1\_GlemPassord**).
1. I delen **Identitetsleverandører** velger du **Tilbakestill passord ved hjelp av e-postadresse**.
1. I kolonnen **Returkrav** merker du av for **E-postadresser**, **Gitt navn**, **Etternavn** og **Brukers objekt-ID**.

    ![Valgte krav](./media/B2C_ForgetPassword_Attributes.png)

1. Velg **OK** for å opprette policyen.
1. Dobbeltklikk det nye policynavnet, og velg deretter **Egenskaper** i navigasjonsruten.
1. Sett alternativet for **Aktiver JavaScript-valg av sideoppsett (forhåndsvisning)** til **På**.

Du kommer tilbake til denne policyen for å fullføre oppsettet etter at du har bygget de egendefinerte sidene. Foreløpig lukker du policyen for å gå tilbake til siden **Brukerflyt (policyer)** i Azure-portalen.

## <a name="build-the-custom-pages"></a>Utarbeide de egendefinerte sidene

Følg denne fremgangsmåten for å bygge egendefinerte sider for å håndtere brukerpålogginger.

1. Gå til området ditt i redigeringsverktøyene for handel.
1. Lag følgende fem maler og fem sider:

    - En mal og side for **Registrering** som bruker registreringsmodulen.
    - En mal og side for **Pålogging** som bruker påloggingsmodulen.
    - En mal og side for **Tilbakestill passord** som bruker modulen for tilbakestilling av passord.
    - En mal og side for **Tilbakestill passord-kontroll** som bruker modulen for kontroll av tilbakestilling av passord.
    - En mal og side for **Profilredigering** som bruker modulen for profilredigering av konto

Følg disse retningslinjene når du bygger sidene:

- Bruk oppsettet og stilen som passer best til dine forretningsbehov, for hver side eller modul.
- Publiser alle sider og URL-adresser som må brukes i Azure AD B2C-oppsettet.
- Når sidene og URL-adressene er publisert, samler du inn URL-adressene som må brukes for Azure AD B2C-policykonfigurasjonene. Et **?preloadscripts=true**-suffiks blir lagt til hver URL-adresse når den brukes.

> [!IMPORTANT]
> Ikke bruk universelle topptekster og bunntekster som har relative koblinger, på nytt. Siden disse sidene vil være vert på Azure AD B2C-domenet når de brukes, bør bare absolutte URL-adresser brukes for alle koblinger.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Konfigurere Azure AD B2C-policyer med egendefinert sideinformasjon 

I Azure-portal går du tilbake til **Azure AD B2C**-siden og deretter, på menyen, under **Policyer**, velger du **Brukerflyter (policyer)**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>Oppdater policyen for registrering og pålogging med egendefinert sideinformasjon

Følg disse trinnene for å oppdatere policyen for registrering og pålogging med egendefinert sideinformasjon

1. I policyen for **Pålogging og registrering** som du konfigurerte tidligere, velger du **Sideoppsett** i navigasjonsruten.
1. Velg oppsettet for **Side for enhetlig registrering og pålogging**.
1. Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.
1. I feltet **Egendefinert side-URI** angir du URL-adressen for full pålogging. Inkluder suffikset **?preloadscripts=true**. Skriv for eksempel inn ``www.<my domain>.com/sign-in?preloadscripts=true``.
1. I feltet for **Sideoppsettversjon (forhåndsvisning)** velger du **1.2.0** .
1. Velg oppsettet **Registreringsside for lokal konto**.
1. Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.
1. I feltet **Egendefinert side-URI** angir du URL-adressen for full registrering. Inkluder suffikset **?preloadscripts=true**. Skriv for eksempel inn ``www.<my domain>.com/sign-up?preloadscripts=true``.
1. I feltet for **Sideoppsettversjon (forhåndsvisning)** velger du **1.2.0** .
1. I delen **Brukerattributter** følger du disse trinnene:

    1. For attributtene **E-postadresse**, **Gitt navn** og **Etternavn** velger du **Nei** i feltet **Krever godkjenning**.
    1. For attributtene **Gitt navn** og **Etternavn** velger du **Nei** i feltet **Valgfri**.

    ![Konfigurasjon av policy for registreringsside for lokal konto](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>Oppdater policyen for profilredigering med egendefinert sideinformasjon

Følg disse trinnene for å oppdatere policyen for profilredigering med egendefinert sideinformasjon

1. I policyen for **Profilredigering** som du konfigurerte tidligere, velger du **Sideoppsett** i navigasjonsruten.
1. Velg oppsettet **Profilredigeringsside**.
1. Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.
1. I feltet **Egendefinert side-URI** angir du URL-adressen for profilredigering. Inkluder suffikset **?preloadscripts=true**. Skriv for eksempel inn ``www.<my domain>.com/profile-edit?preloadscripts=true``.
1. I feltet for **Sideoppsettversjon (forhåndsvisning)** velger du **1.2.0** .
1. I delen **Brukerattributter** følger du disse trinnene:

    1. For attributtene **E-postadresse**, **Gitt navn** velger du **Nei** i feltet **Krever godkjenning**.
    1. For attributtene **Gitt navn** og **Etternavn** velger du **Nei** i feltet **Valgfri**.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>Oppdater policyen for tilbakestilling av passord med egendefinert sideinformasjon

Følg disse trinnene for å oppdatere policyen for tilbakestilling av passord med egendefinert sideinformasjon

1. I policyen for **Tilbakestilling av passord** som du konfigurerte tidligere, velger du **Sideoppsett** i navigasjonsruten.
1. Velg oppsettet **Side for nytt passord**.
1. Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.
1. I feltet **Egendefinert side-URI** angir du URL-adressen for fullstendig tilbakestilling av passord. Inkluder suffikset **?preloadscripts=true**. Skriv for eksempel inn ``www.<my domain>.com/passwordreset?preloadscripts=true``.
1. I feltet for **Sideoppsettversjon (forhåndsvisning)** velger du **1.2.0** .
1. Velg oppsettet **Side for kontoverifisering**.
1. Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.
1. I feltet **Egendefinert side-URI** angir du URL-adressen for fullstendig verifisering av passord. Inkluder suffikset **?preloadscripts=true**. Skriv for eksempel inn ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.
1. I feltet for **Sideoppsettversjon (forhåndsvisning)** velger du **1.2.0** .



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Tilpasse standard tekststrenger for etiketter og beskrivelser

I modulbiblioteket er påloggingsmoduler forhåndsutfylt med standard tekststrenger for etikettene og beskrivelsene. Du kan tilpasse disse strengene i programvareutviklingssettet (SDK) ved å oppdatere verdiene i global.json-filen for påloggingsmodulen.

Standardteksten for den glemte passordkoblingen er **Glemt passordet?**. Nedenfor vises denne standardteksten på påloggingssiden.

![Standardtekst for koblingen for glemt passord på påloggingssiden](./media/B2C_SignUp_ModuleFace.png)

I global.json-filen for påloggingsmodulen for modulbiblioteket kan du redigere teksten til **Glemt passord?**, som vist i følgende illustrasjon.

![Oppdatere koblingstekst i påloggingsmodulens global.json-fil](./media/B2C_CustomizingStringsForModule.png)

Når du har oppdatert global.json-filen og publisert endringene, vises den nye koblingsteksten i påloggingsmodulen både på Commerce-siden og på den aktive påloggingssiden.

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere domenenavnet](configure-your-domain-name.md)

[Distribuere en ny e-handelsleier](deploy-ecommerce-site.md)

[Opprette et e-handelsområde](create-ecommerce-site.md)

[Knytte et Dynamics 365 Commerce-nettsted til en nettkanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Laste opp masseomdirigeringer for URL-adresse](upload-bulk-redirects.md)

[Konfigurere en B2C-leier i Commerce](set-up-B2C-tenant.md)

[Konfigurere flere B2C-leiere i et Commerce-miljø](configure-multi-B2C-tenants.md)

[Legge til støtte for et innholdsleveringsnettverk (CDN)](add-cdn-support.md)

[Aktivere stedsbasert butikkregistrering](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]