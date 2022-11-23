---
title: Konfigurere B2C-leieren i områdebygger for Commerce
description: Denne artikkelen beskriver hvordan du konfigurerer bedrift-til-kunde (B2C)-leieren i Microsoft Dynamics 365 Commerce-områdebyggeren.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 181edf1570f1a9d071a7fae38ff9d73ff3c068fa
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785317"
---
# <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>Konfigurere B2C-leieren i områdebygger for Commerce

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer bedrift-til-kunde (B2C)-leieren i Microsoft Dynamics 365 Commerce-områdebyggeren.

Når installasjonen av Azure AD B2C-leieren er fullført, må du konfigurere B2C-leieren i områdebyggeren for Commerce. Ved hjelp av konfigurasjonstrinnene kan du samle inn B2C-programinformasjon fra Azure-portalen, angi B2C-programinformasjon i områdebyggeren, og deretter knytte B2C-programmet til området og kanalen.

### <a name="collect-the-required-application-information"></a>Samle inn nødvendig programinformasjon

Følg denne fremgangsmåten for å samle inn nødvendig programinformasjon.

1. I Azure-portalen går du til **Hjem \> Azure AD B2C-appregistreringer**.
1. Velg appen, og velg deretter **Oversikt** i navigasjonsruten til venstre for å hente appdetaljene.
1. I referansen for **App-ID (klient)** samler du inn app-ID-en til B2C-appen som ble opprettet i B2C-leieren. Dette vil senere angis som **Klient-GUID** i områdebygger.
1. Velg **URI-er for omadressering**, og samle inn svaradressen som vises for området ditt (svaradressen som angis i oppsettet).
1. Gå til **Hjem \> Azure AD B2C – brukerflyter**, og hent deretter de fullstendige navnene på hver brukerflytpolicy.

Bildet nedenfor viser et eksempel på oversiktssiden **Azure AD B2C-appregistreringer**.

![Oversiktssiden Azure AD B2C-appregistreringer med app-ID-en (klient) uthevet](./media/ClientGUID_Application_AzurePortal.png)

Bildet nedenfor viser et eksempel på brukerflytpolicyer på siden **Azure AD B2C – brukerflyter (policyer)**.

![Samle navnene på hver B2C-policyflyt.](./media/B2CImage_22.png)

### <a name="enter-your-azure-ad-b2c-tenant-application-information-into-commerce"></a>Skriv inn programinformasjon om Azure AD-B2C-leieren i Commerce

Du må angi detaljer for Azure AD B2C-leieren i Commerce-områdebygger før du knytter B2C-leieren til områdene.

Følg denne fremgangsmåten for å legge til programinformasjon om Azure AD B2C-leieren i Commerce.

1. Logg på som administrator for Commerce-områdebygger for miljøet.
1. Velg **Leierinnstillinger** i navigasjonsruten til venstre for å utvide den.
1. Velg **Oppsett av områdegodkjenning** under **Innstillinger for leier**. 
1. Velg **Administrer** i hovedvinduet ved siden av **Områdegodkjenningsprofiler**. (Hvis leieren vises i listen over Bområdegodkjenningsprofiler, var den allerede lagt til av en administrator. Kontroller at elementene i trinn 6 nedenfor samsvarer med de for det planlagte B2C-oppsettet. Du kan også opprette en ny profil ved hjelp av lignende Azure AD B2C-leiere eller -programmer for å ta hensyn til små ulikheter, for eksempel ulike brukerpolicy-ID-er.)
1. Velg **Legg til områdegodkjenningsprofil**.
1. Skriv inn følgende obligatoriske elementer i skjemaet som vises, ved hjelp av verdier fra B2C-leieren og -programmet. Felt som ikke er påkrevd (de uten en stjerne) kan være tomme.

    - **Programnavn**: Navnet på B2C-programmet, for eksempel "Fabrikam B2C".
    - **Navn på leietaker**: Navnet på B2C-leieren din (bruk for eksempel "fabrikam" hvis domenet vises som "fabrikam.onmicrosoft.com" for B2C-leieren). 
    - **Policy-ID for glemt passord**: Brukerflytpolicy-ID for glemt passord, for eksempel "B2C_1_PasswordReset".
    - **Policy-ID for registrering/pålogging**: Brukerflytpolicy-ID for registrering/pålogging, for eksempel «B2C_1_signup_signin».
    - **Klient-GUID**: ID for B2C-program, for eksempel "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".
    - **Rediger profilpolicy-ID**: Brukerflytpolicy-ID for profilredigering, for eksempel "B2C_1A_ProfileEdit".

1. Velg **OK**. Du skal nå se navnet på B2C-programmet ditt i listen.
1. Velg **Lagre** for å lagre endringene.

Du bør bare bruke det valgfrie feltet **Egendefinert domene for pålogging** hvis du konfigurerer et egendefinert domene for Azure AD B2C-leieren. Hvis du vil ha mer informasjon og flere overveielser vedrørende bruk av feltet **Egendefinert domene for pålogging**, kan du se [Ekstra B2C-informasjon](additional-b2c-info.md).

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>Knytte B2C-programmet til området og kanalen

> [!WARNING]
> - Hvis området allerede er knyttet til et B2C-program, vil endring i et annet B2C-program fjerne gjeldende referanser som er opprettet for brukere som allerede er registrert i dette miljøet. Hvis de er endret, vil ingen av legitimasjoner som er knyttet til det tilordnede B2C-programmet, være tilgjengelig for brukerne. 
> - Bare oppdater B2C-programmet hvis du konfigurerer kanalens B2C-program for første gang, eller hvis du vil at brukere skal registrere seg på nytt med ny legitimasjon for denne kanalen med det nye B2C-programmet. Vær forsiktig når du knytter kanaler til B2C-programmer, og navngi programmer tydelig. Hvis en kanal ikke er knyttet til et B2C-program i trinnene nedenfor, vil brukere som logger seg på den kanalen for området, bli lagt inn i B2C-programmet og vises som **standard** i listen **Leierinnstillinger \> B2C-innstillinger** for B2C-programmer.

Følg denne fremgangsmåten for å knytte B2C-programmet til området og kanalen.

1. Naviger til området i Commerce-områdebygger.
1. Velg **Områdeinnstillinger** i navigasjonsruten til venstre for å utvide den.
1. Velg **Kanaler** under **Områdeinnstillinger**.
1. Velg din kanal i hovedvinduet under **Kanaler**.
1. I ruten kanalegenskaper til høyre velger du B2C-appnavnet fra rullegardinmenyen **Velg B2C-app**.
1. Velg **Lukk**, og velg deretter **Lagre og publiser**.

## <a name="next-steps"></a>Neste trinn

Hvis du vil fortsette prosessen med å konfigurere en B2C-leietaker i Commerce, går du videre til [Ekstra B2C-informasjon](additional-b2c-info.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere en B2C-leier i Commerce](set-up-b2c-tenant.md)

[Opprette eller koble til en eksisterende Azure AD B2C-leier i Azure-portalen](create-link-aad-b2c-tenant.md)

[Opprette B2C-programmet](create-b2c-app.md)

[Opprette brukerflytpolicyer](create-user-flow-policies.md)

[Legg til leverandører av sosiale identiteter (valgfritt)](add-social-identity-providers.md)

[Oppdater Commerce Headquarters med den nye Azure AD B2C-informasjonen](update-hq-aad-b2c-info.md)

[Ekstra B2C-informasjon](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
