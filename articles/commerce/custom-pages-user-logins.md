---
title: Definere egendefinerte sider for brukerpålogginger
description: Dette emnet beskriver hvordan du bygger egendefinerte sider i Microsoft Dynamics 365 Commerce som håndterer tilpassede pålogginger for brukere av Azure Active Directory (Azure AD)-forretning-til-forbruker-leiere (B2C).
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f4a3c7c3410a903ae7bc0bac27e861a0dbfa19fdd65761628549c403c4e5db16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723269"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>Definere egendefinerte sider for brukerpålogginger

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du bygger egendefinerte sider i Microsoft Dynamics 365 Commerce som håndterer tilpassede pålogginger for brukere av Azure Active Directory (Azure AD)-forretning-til-forbruker-leiere (B2C).

Hvis du vil bruke egendefinerte sider som er forfattet i Dynamics 365 Commerce, til å håndtere brukerpåloggingsflyter, må du definere Azure AD-policyene som det skal refereres til i handelsmiljøet. Du kan konfigurere Azure AD B2C-policyer for registrering og pålogging, profilredigering og tilbakestilling av passord ved hjelp av Azure AD B2C-programmet. Azure AD B2C-leieren og policynavnene kan deretter refereres til under klargjøringsprosessen som utføres for handelsmiljøet, ved å bruke Microsoft Dynamics Lifecycle Services (LCS).

De egendefinerte Commerce-sidene kan bygges ved hjelp av modulen for pålogging, registrering, kontoprofilredigering, tilbakestilling av passord og generelle AAD-moduler. Det bør deretter refereres til side-URL-adressene som publiseres for disse egendefinerte sidene, i Azure AD B2C-policykonfigurasjoner på Azure-portalen.

> [!WARNING] 
> Azure AD B2C avvikler gamle (eldre) brukerflyter innen 1. august 2021. Derfor bør du planlegge å migrere brukerflytene til den nye anbefalte versjonen. Den nye versjonen gir funksjonsparitet og nye funksjoner. Hvis du vil ha mer informasjon, kan du se [Brukerflyter i Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview).

>Modulbiblioteket for Commerce versjon 10.0.15 eller høyere skal brukes med de anbefalte B2C-brukerflytene. De standard brukerpolicysidene som tilbys i Azure AD B2C, kan også brukes, og gjøre det mulig å legge til bakgrunnsbilder, logoer og bakgrunnsfargeendringer i forbindelse med firmamerking. Selv om det er mer begrenset i utformingsfunksjoner, gir de standard brukerpolicysidene funksjonaliteten til Azure AD B2C-policy uten å opprette og konfigurere dedikerte egendefinerte sider. 

## <a name="set-up-b2c-policies"></a>Definere B2C-policyer

Når du konfigurerer Azure AD B2C-leieren og knytter den til handelsmiljøet, går du til **Azure AD B2C**-siden i Azure-portalen, og deretter, på menyen under **Policyer**, velger du **Brukerflyter (policyer)**.

![Brukerflyter (policyer)-kommandoen på menyen.](./media/B2C_CustomPage_PoliciesMenu.png)

Nå kan du konfigurere brukerpåloggingsflytene for registrering og pålogging, profilredigering og tilbakestilling av passord.

### <a name="configure-the-sign-up-and-sign-in-policy"></a>Konfigurere policy for registrering og pålogging

Følg denne fremgangsmåten for å konfigurere policyen for registrering og pålogging

1. Velg **Ny brukerflyt**, velg **Registrering og pålogging**, velg **Anbefalt**-fanen, og velg deretter **Opprett**.
1. Angi et navn for policyen (for eksempel **B2C\_1\_RegistreringPålogging**).
1. I delen **Identitetsleverandører** velger du ID-leverandørene som skal brukes for policyen. Som et minimum må **E-postregistrering** velges.
1. I kolonnen **Innhent attributt** merker du av for avmerkingsboksene for **E-postadresse**, **Gitt navn** og **Etternavn**.
1. I kolonnen **Returkrav** merker du av for **E-postadresser**, **Gitt navn**, **Identitetsleverandør**, **Etternavn** og **Brukers objekt-ID**.

    ![Valgte attributter og krav.](./media/B2C_SignInSignUp_Attributes.png)

1. Velg **OK** for å opprette policyen.
1. Dobbeltklikk det nye policynavnet, og velg deretter **Egenskaper** i navigasjonsruten.
1. Sett alternativet for **Aktiver JavaScript-valg av sideoppsett (forhåndsvisning)** til **På**.

    ![Egenskapsside for den nye policyen.](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> Policynavnet blir fullstendig referert til i handelsmiljøet. (**B2C\_1\_** vil bli inkludert i referansen.) Policyer kan ikke endres etter at de er opprettet. Hvis du erstatter en eksisterende policy for handelsmiljøet ditt, kan du slette den opprinnelige policyen og bygge en ny policy som har samme navn. Hvis miljøet allerede er klargjort, er det også mulig å sende det nye policynavnet via en tjenesteforespørsel.

Du kommer tilbake til denne policyen for å fullføre oppsettet etter at du har bygget de egendefinerte sidene. Foreløpig lukker du policyen for å gå tilbake til siden **Brukerflyt (policyer)** i Azure-portalen.

### <a name="configure-the-profile-editing-policy"></a>Konfigurere policyen for profilredigering

Hvis du vil konfigurere policyen for profilredigering, gjør du følgende.

1. Velg **Ny brukerflyt**, velg **Profilredigering**, velg **Anbefalt**-fanen, og velg deretter **Opprett**.
1. Angi et navn for policyen (for eksempel **B2C\_1\_RedigerProfil**).
1. I delen **Identitetsleverandører** velger du ID-leverandørene som skal brukes for policyen. Du må minimum velge **Logg på lokal konto**.
1. I kolonnen **Innhent attributt** merker du av for **Gitt navn** og **Etternavn**.
1. I kolonnen **Returkrav** merker du av for **E-postadresser**, **Gitt navn**, **Identitetsleverandør**, **Etternavn** og **Brukers objekt-ID**.
1. Velg **OK** for å opprette policyen.
1. Dobbeltklikk det nye policynavnet, og velg deretter **Egenskaper** i navigasjonsruten.
1. Sett alternativet for **Aktiver JavaScript-valg av sideoppsett (forhåndsvisning)** til **På**.

Du kommer tilbake til denne policyen for å fullføre oppsettet etter at du har bygget de egendefinerte sidene. Foreløpig lukker du policyen for å gå tilbake til siden **Brukerflyt (policyer)** i Azure-portalen.

### <a name="configure-the-password-reset-policy"></a>Konfigurere policyen for tilbakestilling av passord

Hvis du vil konfigurere policyen for tilbakestilling av passord, gjør du følgende.

1. Velg **Ny brukerflyt**, velg **Tilbakestill passord**, velg **Anbefalt**-fanen, og klikkk på **Opprett**.
1. Angi et navn for policyen (for eksempel **B2C\_1\_GlemPassord**).
1. I delen **Identitetsleverandører** velger du **Tilbakestill passord ved hjelp av e-postadresse**.
1. I kolonnen **Returkrav** merker du av for **E-postadresser**, **Gitt navn**, **Etternavn** og **Brukers objekt-ID**.
1. Velg **OK** for å opprette policyen.
1. Dobbeltklikk det nye policynavnet, og velg deretter **Egenskaper** i navigasjonsruten.
1. Sett alternativet for **Aktiver JavaScript-valg av sideoppsett (forhåndsvisning)** til **På**.

Du kommer tilbake til denne policyen for å fullføre oppsettet etter at du har bygget de egendefinerte sidene. Foreløpig lukker du policyen for å gå tilbake til siden **Brukerflyt (policyer)** i Azure-portalen.

## <a name="build-the-custom-pages"></a>Utarbeide de egendefinerte sidene

Dedikerte Azure AD-moduler er inkludert i Commerce for å bygge egendefinerte sider for Azure AD B2C-brukerpolicyer. Sider kan bygges spesielt for oppsettet til hver brukerpolicyside ved hjelp av Azure AD B2C-hovedmodulene som vises nedenfor. Alternativt kan modulen **AAD generelt** brukes for alle sideoppsett og policyer i Azure AD B2C (selv for sideoppsettalternativer i policyer som ikke er oppført nedenfor). 

- Sidespesifikke Azure AD-moduler er bundet til inndataelementer som gjengis av Azure AD B2C. Disse modulene gir deg mer kontroll over plasseringen av elementene på sidene. Det kan imidlertid hende at flere sider og modultillegg må bygges for å ta hensyn til avvik utover standardinnstillingene som er beskrevet nedenfor.
- Modulen **AAD generelt** oppretter "div"-elementet for Azure AD B2C for å gjengi alle elementer i sideoppsettet for brukerpolicy, noe som gir mer fleksibilitet til B2C-funksjonene på siden, men mindre kontroll over plasseringen og stilen (selv om CSS kan brukes til å samsvare utseendet til og følelsen på nettstedet).

Du kan opprette en enkelt side med mobulen **AAD generelt** og bruke den for alle brukerpolicysidene, eller du kan bygge ut bestemte sider ved hjelp av de enkelte Azure AD-mobilene for pålogging, registrering, profilredigering, tilbakestilling av passord og verifisering av tilbakestilling av passord. Du kan også bruke en blanding av begge deler ved å bruke de bestemte Azure AD-sidene for sideoppsettene som er angitt nedenfor, og den generiske AAD-modulsiden for gjenværende sideoppsett på disse eller andre brukerpolicysider.

Hvis du vil lære mer om Azure AD-modulene som leveres med modulbiblioteket, kan du lese mer på [Identitetsbehandlingssider og -moduler](identity-mgmt-modules.md).

Følg denne fremgangsmåten for å bygge egendefinerte sider med spesifikke identitetsmoduler for å håndtere brukerpålogginger.

1. Gå til området i Commerce-områdebygger.
1. Bygg følgende fem maler og sider (hvis de ikke allerede finnes på området):
    - En mal og side for **Registrering** som bruker registreringsmodulen.
    - En mal og side for **Pålogging** som bruker påloggingsmodulen.
    - En mal og side for **Tilbakestill passord** som bruker modulen for tilbakestilling av passord.
    - En mal og side for **Tilbakestill passord-kontroll** som bruker modulen for kontroll av tilbakestilling av passord.
    - En mal og side for **Profilredigering** som bruker modulen for profilredigering av konto.

Følg disse retningslinjene når du bygger sidene:

- Bruk oppsettet og stilen som passer best til dine forretningsbehov, for hver side eller modul.
- Publiser alle sider og URL-adresser som må brukes i Azure AD B2C-oppsettet.
- Når sidene og URL-adressene er publisert, samler du inn URL-adressene som må brukes for Azure AD B2C-policykonfigurasjonene. Et **?preloadscripts=true**-suffiks blir lagt til hver URL-adresse når den brukes.

> [!IMPORTANT]
> Sider som det refereres til i Azure AD B2C, leveres direkte fra Azure AD B2C-leierens domene. Ikke bruk universelle topptekster og bunntekster som har relative koblinger, på nytt. Siden disse sidene vil være vert på Azure AD B2C-domenet når de brukes, bør bare absolutte URL-adresser brukes for alle koblinger. Det anbefales at du oppretter en bestemt topp- og bunntekst med absolutte URL-adresser for de Azure AD-relaterte egendefinerte sidene, med Commerce-spesifikke moduler som krever tilkobling til Retail Server, er fjernet. Favorittene, søkelinjen, påloggingskoblingen og handlekurvmodulene bør for eksempel ikke inkluderes på noen som helst sider som vil bli brukt i Azure AD B2C-brukerflyter.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Konfigurere Azure AD B2C-policyer med egendefinert sideinformasjon 

I Azure-portal går du tilbake til **Azure AD B2C**-siden og deretter, på menyen, under **Policyer**, velger du **Brukerflyter (policyer)**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>Oppdater policyen for registrering og pålogging med egendefinert sideinformasjon

Følg disse trinnene for å oppdatere policyen for registrering og pålogging med egendefinert sideinformasjon

1. I policyen for **Pålogging og registrering** som du konfigurerte tidligere, velger du **Sideoppsett** i navigasjonsruten.
1. Velg oppsettet for **Side for enhetlig registrering og pålogging**.
1. Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.
1. I feltet **Egendefinert side-URI** angir du URL-adressen for full pålogging. Inkluder suffikset **?preloadscripts=true**. Skriv for eksempel inn ``www.<my domain>.com/sign-in?preloadscripts=true``.
1. I feltet **Sideoppsettversjon** velger du versjon **2.1.0** eller senere (krever modulbibliotekt for Commerce versjon 10.0.15 eller høyere).
1. Velg **Lagre**.
1. Velg oppsettet **Registreringsside for lokal konto**.
1. Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.
1. I feltet **Egendefinert side-URI** angir du URL-adressen for full registrering. Inkluder suffikset **?preloadscripts=true**. Skriv for eksempel inn ``www.<my domain>.com/sign-up?preloadscripts=true``.
1. I feltet **Sideoppsettversjon** velger du versjon **2.1.0** eller senere (krever modulbibliotekt for Commerce versjon 10.0.15 eller høyere).
1. I delen **Brukerattributter** følger du disse trinnene:
    1. For attributtene **Gitt navn** og **Etternavn** velger du **Nei** i kolonnen **Krever godkjenning**.
    1. For attributtet **E-postadresse** anbefales det å la standardverdien **Ja** være valgt i kolonnen **Krever godkjenning**. Dette alternativet sikrer at brukere som registrerer seg med en angitt e-postadresse, kontrollerer at de eier e-postadressen.
    1. For attributtene **E-postadresse**, **Gitt navn** og **Etternavn** velger du **Nei** i kolonnen **Valgfritt**.
1. Velg **Lagre**.

    ![Konfigurasjon av policy for registreringsside for lokal konto.](./media/B2C_SignInSignUp_Recommended_PageLayoutExample.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>Oppdater policyen for profilredigering med egendefinert sideinformasjon

Følg disse trinnene for å oppdatere policyen for profilredigering med egendefinert sideinformasjon

1. I policyen for **Profilredigering** som du konfigurerte tidligere, velger du **Sideoppsett** i navigasjonsruten.
1. Velg oppsettet **Profilredigeringsside** (kan kreve at du ruller ned forbi andre oppsettalternativer, avhengig av skjermen).
1. Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.
1. I feltet **Egendefinert side-URI** angir du URL-adressen for profilredigering. Inkluder suffikset **?preloadscripts=true**. Skriv for eksempel inn ``www.<my domain>.com/profile-edit?preloadscripts=true``.
1. For **Sideoppsettversjon** velger du versjon **2.1.0** eller høyere (krever modulbibliotek for Commerce versjon 10.0.15 eller høyere).
1. I delen **Brukerattributter** følger du disse trinnene:
    1. For attributtene **Gitt navn** og **Etternavn** velger du **Nei** i kolonnen **Valgfritt**.
    1. For attributtene **Gitt navn** og **Etternavn** velger du **Nei** i kolonnen **Krever godkjenning**.
1. Velg **Lagre**.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>Oppdater policyen for tilbakestilling av passord med egendefinert sideinformasjon

Følg disse trinnene for å oppdatere policyen for tilbakestilling av passord med egendefinert sideinformasjon

1. I policyen for **Tilbakestilling av passord** som du konfigurerte tidligere, velger du **Sideoppsett** i navigasjonsruten.
1. Velg oppsettet **Side for glemt passord**.
1. Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.
1. I feltet **Egendefinert side-URI** angir du URL-adressen for fullstendig verifisering av passord. Inkluder suffikset **?preloadscripts=true**. Skriv for eksempel inn ``www.<my domain>.com/password-reset-verification?preloadscripts=true``.
1. I feltet **Sideoppsettversjon** velger du versjon **2.1.0** eller høyere (krever modulbibliotek for Commerce versjon 10.0.15 eller høyere).
2. Velg **Lagre**.
3. Velg oppsettet **Side for endre passord**.
4. Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.
5. I feltet **Egendefinert side-URI** angir du URL-adressen for fullstendig tilbakestilling av passord. Inkluder suffikset **?preloadscripts=true**. Skriv for eksempel inn ``www.<my domain>.com/password-reset?preloadscripts=true``.
6. I feltet **Sideoppsettversjon** velger du versjon **2.1.0** eller høyere (krever modulbibliotek for Commerce versjon 10.0.15 eller høyere).
7. Velg **Lagre**.

## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Tilpasse standard tekststrenger for etiketter og beskrivelser

I modulbiblioteket er påloggingsmoduler forhåndsutfylt med standard tekststrenger for etikettene og beskrivelsene. Du kan tilpasse strengene i egenskapsruten for modulen du arbeider på. Flere strenger på siden (for eksempel koblingsteksten **Glemt passordet?** eller handlingsteksten **Opprett en konto**) vil kreve Commerce SDK og oppdatering av verdiene i global.json-filen for påloggingsmodulen.

Standardteksten for den glemte passordkoblingen er **Glemt passordet?**. Nedenfor vises denne standardteksten på påloggingssiden.

![Standardtekst for koblingen for glemt passord på påloggingssiden.](./media/B2C_SignUp_ModuleFace.png)

I global.json-filen for påloggingsmodulen for modulbiblioteket kan du redigere teksten til **Glemt passord?**, som vist i følgende illustrasjon.

![Oppdatere koblingstekst i påloggingsmodulens global.json-fil.](./media/B2C_CustomizingStringsForModule.png)

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