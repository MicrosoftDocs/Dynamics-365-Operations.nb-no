---
title: Definere en B2C-leier i Commerce
description: Dette emnet beskriver hvordan du konfigurerer Azure Active Directory (Azure AD) bedrift-til-kunde (B2C)-leietakere for godkjenning av brukerområde i Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4ee667bb49e70e0c881a2db1248b3f0c7fc017ce
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478146"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>Definere en B2C-leier i Commerce

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer Azure Active Directory (Azure AD) bedrift-til-kunde (B2C)-leietakere for godkjenning av brukerområde i Dynamics 365 Commerce.

Dynamics 365 Commerce bruker Azure AD B2C til å støtte brukerlegitimasjon og godkjenningsflyt. En bruker kan registrere seg, logge inn og tilbakestille passordet ved hjelp av disse flytene. Azure AD B2C lagrer sensitiv brukergodkjenningsinformasjon, for eksempel brukernavn og passord. Brukerposten i B2C-leieren vil lagre enten en B2C-post for lokal forretningsforbindelse eller en B2C-post for sosial identitetsleverandør. Disse B2C-postene vil koble tilbake til kundeoppføringen i Commerce-miljøet.

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a>Opprett eller koble til en eksisterende AAD B2C-leier i Azure-portalen

1. Logg på [Azure-portalen](https://portal.azure.com/).
1. Velg **Opprett en ressurs** fra menyen for Azure-portal. Pass på at du bruker abonnementet og katalogen som skal kobles til Commerce-miljøet.

    ![Opprette en ressurs i Azure-portalen](./media/B2CImage_1.png)

1. Gå til **Identitet \> Azure Active Directory B2C**.
1. På siden **Opprett ny B2C-leier eller koble til en eksisterende leier** bruker du et av alternativene nedenfor som passer best til firmaets behov:

    - **Opprett en ny Azure AD B2C-leier**: Bruk dette alternativet til å opprette en ny AAD B2C-leier.
        1. Velg **Opprett en ny Azure AD B2C-leier**.
        1. Under **Organisasjonsnavn** angir du organisasjonsnavnet.
        1. Skriv inn det opprinnelige domenenavnet under **Opprinnelig domenenavn**.
        1. For **Land eller område** velger du aktuelt land eller område.
        1. Velg **Opprett** for å opprette leieren.

     ![Opprette en ny Azure AD-leier](./media/B2CImage_2.png)

     - **Koble en eksisterende Azure AD B2C-leier til Azure-abonnementet**: Bruk dette alternativet hvis du allerede har en Azure AD B2C-leier du vil koble til.
        1. Velg **Koble en eksisterende Azure AD B2C-leier til Azure-abonnementet**.
        1. For **Azure AD B2C-leier** velger du den riktige B2C-leieren. Hvis det vises en melding i valgboksen om at det ikke ble funnet noen kvalifiserte B2C-leiere, har du ikke en eksisterende kvalifisert B2C-leier, og må opprette en ny.
        1. For **Ressursgruppe** velger du **Opprett ny**. Angi et **navn** på ressursgruppen som skal inneholde leieren, velg **ressursgruppelokasjonen**, og velg deretter **Opprett**.

    ![Koble en eksisterende Azure AD B2C-leier til Azure-abonnementet](./media/B2CImage_3.png)

1. Når den nye Azure AD B2C-katalogen er opprettet (dette kan ta litt tid), vil det vises en kobling til den nye katalogen på instrumentbordet. Denne koblingen fører deg til siden "Velkommen til Azure Active Directory B2C".

    ![Kobling til ny AAD-katalog](./media/B2CImage_4.png)

> [!NOTE]
> Hvis du har flere abonnementer i Azure-kontoen eller har konfigurert B2C-leieren uten å koble til et aktivt abonnement, vil et **Feilsøking**-banner gi deg beskjed om å koble leieren til et abonnement. Velg feilsøkingsmeldingen, og følg instruksjonene for å løse problemet med abonnement.

Bildet nedenfor viser et eksempel på et Azure AD B2C **Feilsøking**-banner.

![Advarsel som viser at katalogen ikke har et aktivt abonnement](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a>Opprette B2C-programmet

Når B2C-leieren er opprettet, oppretter du et B2C-program i leieren for å samhandle med Commerce-handlingene.

Hvis du vil opprette B2C-programmet, gjør du følgende:

1. Velg **Programmer (eldre)** i Azure-portalen, og velg deretter **Legg til**.
1. Under **Navn** angir du navnet på det ønskede AAD B2C-programmet.
1. Under **Webapp/Web-API** for **Inkluder webapp / web-API** velger du **Ja**.
1. For **Tillat implisitt flyt** velger du **Ja** (standardverdien).
1. Under **Svar-URL** angir du de dedikerte svar-URL-adressene. Se [URL-adresser for svar](#reply-urls) nedenfor for informasjon om URL-adresser for svar, og hvordan du kan formatere dem her.
1. Velg **Nei** for **Inkluder opprinnelig klient** (standardverdi).
1. Velg **Opprett**.

### <a name="reply-urls"></a>URL-adresser for svar

Svar-URL-adresser er viktige, fordi de gir en tillatelsesliste for returdomener når området kaller Azure AD B2C for å godkjenne en bruker. Dette tillater retur av den godkjente brukeren til domenet de logger seg på fra (områdedomenet). 

I boksen **Svar-URL** på skjermen **Azure AD B2C-programmer \> Nytt program** må du legge til separate linjer for både områdedomet og (når miljøet er klargjort) den Commerce-genererte URL-en. Disse URL-adressene må alltid bruke et gyldig URL-format og må være basis-URLer (ingen etterfølgende skråstreker eller baner). Strengen ``/_msdyn365/authresp`` må deretter legges til de primære URL-adressene, som i følgende eksempler.

- ``https://www.fabrikam.com/_msdyn365/authresp`` (Domenet skal samsvare med hele e-handelsdomenet. Hvis du har flere domener, må du legge til denne URL-adressen for hvert domene.)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a>Opprette brukerflytpolicyer

Brukerflyter er policyene som Azure AD B2C bruker for å gi sikker pålogging, registrering, redigering av profil og brukeopplevelser ved glemt passord. Dynamics 365 Commerce bruker disse flytene til å utføre policyhandlinger for å kommunisere med Azure AD B2C-leieren. Når en bruker samhandler med disse policyene, omdirigeres de til Azure AD B2C-leieren for å utføre handlingene.

Azure AD B2C gir tre enkle flyttyper for brukere:
- Registrering og pålogging
- Profilredigering
- Tilbakestill passord

Du kan velge å bruke standard brukerflyter i Azure AD, som vil vise en side som ligger på AAD-B2C. Du kan også opprette en HTML-side for å kontrollere utseendet og funksjonaliteten til brukerflytopplevelsene. 

Hvis du vil tilpasse brukerpolicysidene for Dynamics 365 Commerce, kan du se [Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md). Hvis du vil ha mer informasjon, se [Tilpasse grensesnittet til brukeropplevelser i Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Opprette en brukerflytpolicy for registrering og pålogging

Følg denne fremgangsmåten for å opprette en brukerflytpolicy for registrering og pålogging.

1. Velg **Brukerflyter (policyer)** i den venstre navigasjonsruten i Azure-portalen.
1. På siden **Azure AD B2C – brukerflyter (policyer)** velger du **Ny brukerflyt**.
1. Velg **Registrering og pålogging** i fanen **Anbefalt**.
1. Under **Navn** skriver du inn et policynavn. Dette navnet vil vises etterpå med et prefiks som portalen tilordner (for eksempel "B2C_1_").
1. Under **Identitetsleverandører** merker du av for den aktuelle avmerkingsboksen.
1. Velg ønsket valg for firmaet under **Godkjenning med flere faktorer**. 
1. Under **Brukerattributter og krav** velger du alternativer for å samle attributter eller returkrav etter behov. Commerce krever følgende standard alternativer:

    | **Innhent attributt** | **Returkrav** |
    | ---------------------- | ----------------- |
    | E-postadresse          | E-postadresser   |
    | Gitt navn             | Gitt navn        |
    |                        | Identitetsleverandør |
    | Etternavn                | Etternavn           |
    |                        | Brukers objekt-ID  |

1. Velg **Opprett**.

Bildet nedenfor er et eksempel på brukerflyt for Azure AD B2C registrering og pålogging.

![Policyinnstillinger for registrering og pålogging](./media/B2CImage_11.png)

Bildet nedenfor viser alternativet **Kjør brukerflyt** i brukerflyten Azure AD B2C registering og pålogging.

![Kjør brukerflyt-alternativet policyflyt](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a>Opprette en brukerflytpolicy for profilredigering

Følg denne fremgangsmåten for å opprette en brukerflytpolicy for profilredigering.

1. Velg **Brukerflyter (policyer)** i den venstre navigasjonsruten i Azure-portalen.
1. På siden **Azure AD B2C – brukerflyter (policyer)** velger du **Ny brukerflyt**.
1. Velg **Profilredigering** i fanen **Anbefalt**.
1. Under **Navn** angir du brukerflyten for profilredigering. Dette navnet vil vises etterpå med et prefiks som portalen tilordner (for eksempel "B2C_1_").
1. Under **Identitetsleverandører** velger du **Logg på lokal konto**.
1. Under **Brukerattributter** merker du av følgende avmerkingsbokser:
    - **E-postadresser** (bare **Returkrav**)
    - **Gitt navn** (**Innhent attributt** og **Returkrav**)
    - **Identitetsleverandør** (bare **Returkrav**)
    - **Etternavn** (**Innhent attributt** og **Returkrav**)
    - **Brukers objekt-ID** (**bare Returkrav**)
1. Velg **Opprett**.

Det følgende bildet viser et eksempel på brukerflyten for Azure AD B2C-profilredigering.

![Opprette brukerflyten for profilredigering](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Opprette en brukerflytpolicy for tilbakestilling av passord

Følg denne fremgangsmåten for å opprette en brukerflytpolicy for tilbakestilling av passord.

1. Velg **Brukerflyter (policyer)** i den venstre navigasjonsruten i Azure-portalen.
1. På siden **Azure AD B2C – brukerflyter (policyer)** velger du **Ny brukerflyt**.
1. Velg **Tilbakestill passord** i fanen **Anbefalt**.
1. Under **Navn** skriver du inn et navn på brukerflyten for tilbakestilling av passord.
1. Under **Identitetsleverandører** velger du **Tilbakestill passord ved hjelp av e-postadresse**.
1. Velg **Opprett**.
1. Under **Programkrav** merker du av følgende avmerkingsbokser:
    - **E-postadresser**
    - **Gitt navn**
    - **Etternavn**
    - **Brukers objekt-ID**
1. Velg **Opprett**.

Det følgende bildet viser hvor du kan angi at **passordet skal tilbakestilles ved å bruke e-postadresse** i brukerflyten for tilbakestilling av passord i Azure AD B2C.

![Angi Tilbakestill passord med e-postadresse i policy for tilbakestilling av passord](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a>Legg til leverandører av sosiale identiteter (valgfritt)

Leverandører av sosiale identiteter gjør det mulig for brukere å bruke sine sosiale kontoer for godkjenning. Det er valgfritt å legge til leverandør for godkjenning av sosiale identiteter i Dynamics 365 Commerce. 

Hvis godkjenning av sosial identitetsleverandør ikke er lagt til, vil standard Azure AD B2C-profiler være hovedprofilene til brukerbasen. Brukerne velger sine egne brukernavn (foretrukket e-postadresse) og angir et passord. Azure AD B2C vil godkjenne brukere direkte. 

Hvis godkjenning av sosial identitetsleverandør er lagt til og en bruker velger en av de tilbudte sosiale identitetsleverandørene, opprettes fremdeles en enhet i Azure AD B2C-leieren. Azure AD B2C vil deretter godkjenne brukerens legitimasjonsbeskrivelser med den sosiale identitetsleverandøren.

> [!NOTE]
> Påloggingen av identitetsleverandøren oppretter en post i B2C-leieren, men i et annet format enn lokale kontoer, ettersom den kaller den eksterne referansen for sosial identitetsleverandør for godkjenning. Brukeren kan bruke samme e-postadresse på tvers av sosiale identitetsleverandører, som betyr at e-postbrukernavnet som brukes til godkjenning, ikke kan være unikt for leieren. Azure AD B2C vil bare sørge for at brukere har en unik e-postadresse på lokale B2C-kontoer.

Før du kan legge til en sosial identitetsleverandør for godkjenning, må du gå til identitetsleverandørens portal og konfigurere et identitetsleverandørprogram som beskrevet i Azure AD i B2C-dokumentasjonen. Nedenfor finner du en liste over koblinger til dokumentasjonen.

- [Amazon](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (Én leier)](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Microsoft-konto](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Legge til og konfigurere en leverandør av sosiale identiteter

Følg denne fremgangsmåten for å legge til og konfigurere en leverandør av sosiale identiteter.  

1. I Azure-portalen går du til **Identitetsleverandører**.
1. Velg **Legg til**. Skjermbildet **Legg til identitetsleverandør** vises.
1. Under **Navn** skriver du inn navnet som skal vises for brukere på påloggingsskjermen.
1. Under **Type identitetsleverandør** velger du en identitetsleverandør fra listen.
1. Velg **OK**.
1. Velg **Konfigurer denne identitetsleverandøren** for å få tilgang til skjermbildet for **oppsett av sosial identitetsleverandør** .
1. Under **Klient-ID** angir du klient-IDen som hentes fra oppsettet for identitetsleverandørprogram.
1. Under **Klienthemmelighet** angir du klienthemmeligheten som hentes fra oppsettet for identitetsleverandørprogram.
1. Tilknytt brukerflyt for policyer for pålogging/registrering:
1. Gå til **Azure AD B2C – brukerflyter (policyer) \> {policyen for pålogging/registrering} \> Identitetsleverandører**.
1. Hvis du vil tilknytte brukerflytpolicyen for pålogging/registrering, velger du hver identitetsleverandør du har angitt for kontoen. Hvis du vil teste disse, velger du **Kjør brukerflyt** for hver identitetsleverandør. En ny kategori viser påloggingssiden som viser den nye valgboksen for identitetsleverandør.

Følgende bilde viser eksempler på skjermbildene **Legg til identitetsleverandør** og **Konfigurere sosial identitetsleverandør** i Azure AD B2C.

![Legge til en leverandør av sosiale identiteter i programmet](./media/B2CImage_14.png)

Det følgende bildet viser et eksempel på hvordan du kan velge identitetsleverandører på siden Azure AD B2C **identitetsleverandører**.

![Velg hver sosial identitetsleverandør du vil aktivere for policyen](./media/B2CImage_16.png)

Bildet nedenfor viser et eksempel på et standard påloggingsskjermbilde med en påloggingsknapp for sosial identitetsleverandør.

![Eksempel på standard påloggingsskjerm med påloggingsknappen for sosial identitetsleverandør](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Oppdater Commerce Headquarters med den nye Azure AD B2C-informasjonen

Når Azure AD B2C-klargjøringstrinnene ovenfor er fullført, må Azure AD B2C-programmet registreres i Dynamics 365 Commerce-miljøet.

Følg denne fremgangsmåten for å oppdatere Headquarters med den nye Azure AD B2C-informasjonen:

1. I Commerce går du til **Delte handelsparametere** og velger **Identitetsleverandører** på den venstre menyen.
1. Under **Identitetsleverandører** gjør du følgende:
    1. I **Utsteder**-boksen angir du URL-adressen til utstederen av identitetsleverandør. Du finner utstederens URL-adresse ved å se [Hent utsteders URL-adresse](#obtain-issuer-url) nedenfor.
    1. I **Navn**-boksen angir du et navn på utstederposten.
    1. I **Type**-boksen angir du **Azure AD B2C (id_token)**.
1. Gjør følgende med ovenstående element for B2C-identitetsleverandør valgt under **Beroende parter**:
    1. I **Klient-ID**-boksen skriver du inn B2C-program-IDen. Du finner dette i **Program-ID**-boksen på egenskapssiden for B2C-programmet.
    1. I **Type**-boksen angir du **Offentlig**.
    1. I **Brukertype**-boksen angir du **Kunde**.
1. Velg **Lagre** i handlingsruten.
1. I Commerce-søkeboksen søker du etter **Distribusjonsplan**
1. I den venstre navigasjonsmenyen på siden **Distribusjonsplaner** velger du jobben **1110 Global konfigurasjon**.
1. Velg **Kjør nå** i handlingsruten.

### <a name="obtain-issuer-url"></a>Hente utsteders URL-adresse

Følg denne fremgangsmåten for å hente URL-adressen for utsteder av identitetsleverandør.

1. Opprett en URL-adresse for metadata i følgende format ved hjelp av B2C-leieren og-policyen: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Eksempel: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Angi URL-adressen for metadata på adresselinjen i en leser.
1. I metadataene kopierer du URL-adressen for utsteder av identitetsleverandør (verdien for **"utsteder"**).
    - Eksempel: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>Konfigurere B2C-leieren i områdebygger for Commerce

Når installasjonen av Azure AD B2C-leieren er fullført, må du konfigurere B2C-leieren i områdebyggeren for Commerce. Ved hjelp av konfigurasjonstrinnene kan du samle inn B2C-programinformasjon fra Azure-portalen, angi B2C-programinformasjon i områdebyggeren, og deretter knytte B2C-programmet til området og kanalen.

### <a name="collect-the-required-application-information"></a>Samle inn nødvendig programinformasjon

Følg denne fremgangsmåten for å samle inn nødvendig programinformasjon.

1. I Azure-portalen går du til **Hjem \> Azure AD B2C-programmer**.
1. Velg programmet, og velg deretter **Egenskaper** i navigasjonsruten til venstre for å hente programdetaljene.
1. I **Program-ID**-boksen samler du inn program-IDen til B2C-programmet som ble opprettet i B2C-leieren. Dette vil senere angis som **Klient-GUID** i områdebygger.
1. Under **Svar-URL** samler du inn URL-adressen for svar.
1. Gå til **Hjem \> Azure AD B2C – brukerflyter (policyer)**, og hent deretter navnene på hver brukerflytpolicy.

Bildet nedenfor viser et eksempel på siden **Azure AD B2C-programmer**.

![Gå til B2C-programmet i leieren](./media/B2CImage_19.png)

Bildet nedenfor viser et eksempel på et programs **Egenskaper**-side i Azure AD B2C. 

![Kopier program-IDen fra egenskapene for B2C-programmet](./media/B2CImage_21.png)

Bildet nedenfor viser et eksempel på brukerflytpolicyer på siden **Azure AD B2C – brukerflyter (policyer)**.

![Samle navnene på hver B2C-policyflyt](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a>Skriv inn programinformasjon om AAD-B2C-leieren i Commerce

Du må angi detaljer for Azure AD B2C-leieren i Commerce-områdebygger før du knytter B2C-leieren til områdene.

Følg denne fremgangsmåten for å legge til programinformasjon om AAD-B2C-leier i Commerce.

1. Logg på som administrator for Commerce-områdebygger for miljøet.
1. Velg **Leierinnstillinger** i navigasjonsruten til venstre for å utvide den.
1. Velg **B2C-innstillinger** under **Leierinnstillinger**. 
1. Velg **Behandle** i hovedvinduet ved siden av **B2C-programmer**. (Hvis leieren vises i listen over B2C-programmer, var den allerede lagt til av en administrator. Kontroller at elementene i trinn 6 nedenfor samsvarer med B2C-programmet.)
1. Velg **Legg til B2C-program**.
1. Skriv inn følgende obligatoriske elementer i skjemaet som vises, ved hjelp av verdier fra B2C-leieren og -programmet. Felt som ikke er påkrevd (de uten en stjerne) kan være tomme.

    - **Programnavn**: Navnet på B2C-programmet, for eksempel "Fabrikam B2C".
    - **Navn på leietaker**: Navnet på B2C-leieren din (bruk for eksempel "fabrikam" hvis domenet vises som "fabrikam.onmicrosoft.com" for B2C-leieren). 
    - **Policy-ID for glemt passord**: Brukerflytpolicy-ID for glemt passord, for eksempel "B2C_1_PasswordReset".
    - **Policy-ID for registrering/pålogging**: Brukerflytpolicy-ID for registrering/pålogging, for eksempel "B2C_1_signup_signin".
    - **Klient-GUID**: ID for B2C-program, for eksempel "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".
    - **Rediger profilpolicy-ID**: Brukerflytpolicy-ID for profilredigering, for eksempel "B2C_1A_ProfileEdit".

1. Velg **OK**. Du skal nå se navnet på B2C-programmet ditt i listen.
1. Velg **Lagre** for å lagre endringene.

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>Knytte B2C-programmet til området og kanalen

> [!WARNING]
> Hvis området allerede er knyttet til et B2C-program, vil endring i et annet B2C-program fjerne gjeldende referanser som er opprettet for brukere som allerede er registrert i dette miljøet. Hvis de er endret, vil ingen av legitimasjoner som er knyttet til det tilordnede B2C-programmet, være tilgjengelig for brukerne. 
> 
> Bare oppdater B2C-programmet hvis du konfigurerer kanalens B2C-program for første gang, eller hvis du vil at brukere skal registrere seg på nytt med ny legitimasjon for denne kanalen med det nye B2C-programmet. Vær forsiktig når du knytter kanaler til B2C-programmer, og navngi programmer tydelig. Hvis en kanal ikke er knyttet til et B2C-program i trinnene nedenfor, vil brukere som logger seg på den kanalen for området, bli lagt inn i B2C-programmet og vises som **standard** i listen **Leierinnstillinger \> B2C-innstillinger** for B2C-programmer.

Følg denne fremgangsmåten for å knytte B2C-programmet til området og kanalen.

1. Naviger til området i Commerce-områdebygger.
1. Velg **Områdeinnstillinger** i navigasjonsruten til venstre for å utvide den.
1. Velg **Kanaler** under **Områdeinnstillinger**.
1. Velg din kanal i hovedvinduet under **Kanaler**.
1. I ruten kanalegenskaper til høyre velger du B2C-programnavnet fra rullegardinmenyen **Velg B2C-program**.
1. Velg **Lukk**, og velg deretter **Lagre og publiser**.

## <a name="additional-b2c-information"></a>Ekstra B2C-informasjon

### <a name="customer-migration"></a>Kundeoverføring

Hvis du vurderer å overføre kundeposter fra en tidligere identitetsleverandørplattform, kan du arbeide med Dynamics 365 Commerce-teamet for å gjennomgå kundeoverføringsbehovene dine.

Hvis du vil ha mer Azure AD B2C-dokumentasjon om kundeoverføring, kan du se [Overføre brukere til Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Egendefinerte policyer

Hvis du vil ha mer informasjon om tilpassing av Azure AD B2C-samhandlinger og policyflyter utover hva som tilbys av B2C-standardpolicyer, kan du se [Egendefinerte policyer i Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Sekundær administrator

En valgfri, sekundær administratorkonto kan legges til i **Brukere**-delen av B2C-leieren. Dette kan være en direkte konto eller en generell konto. Hvis du må dele en konto på tvers av teamressurser, kan du også opprette en felles konto. På grunn av følsomheten til dataene som er lagret i Azure AD B2C, bør en felles konto overvåkes nøye i henhold til firmaets sikkerhetspraksis.

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere domenenavnet](configure-your-domain-name.md)

[Distribuere en ny e-handelsleier](deploy-ecommerce-site.md)

[Opprette et e-handelsområde](create-ecommerce-site.md)

[Knytte et Dynamics 365 Commerce-nettsted til en nettkanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Last opp masseomdirigeringer for URL-adresse](upload-bulk-redirects.md)Tilknytt et Dynamics 365 Commerce-område med en nettkanal

[Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md)

[Konfigurere flere B2C-leiere i et Commerce-miljø](configure-multi-B2C-tenants.md)

[Legge til støtte for et innholdsleveringsnettverk (CDN)](add-cdn-support.md)

[Aktivere stedsbasert butikkregistrering](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
