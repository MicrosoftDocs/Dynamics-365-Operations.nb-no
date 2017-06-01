---
title: Installere og konfigurere Microsoft Dynamics 365 for Operations &#8211;
description: Dette emnet beskriver hvordan du installerer og konfigurerer Microsoft Dynamics 365 for Operations - Warehousing.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 46b4809ae89f90295766e95ce78a8f019de0cdae
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Installere og konfigurere Microsoft Dynamics 365 for Operations &#8211;

[!include[banner](../includes/banner.md)]


Dette emnet beskriver hvordan du installerer og konfigurerer Microsoft Dynamics 365 for Operations - Warehousing.

Dynamics 365 for Operations - Warehousing er et program som er tilgjengelig på Google Play-butikken og Windows Store. Denne appen tilbys for den gjeldende versjonen av Microsoft Dynamics 365 for Operations som en frittstående komponent, som betyr selvdistribuering på enheter som brukes til lageroppgaver. For å bruke appen i Dynamics 365 for Operations-miljøet, må du laste ned appen på hver enhet og konfigurere den til å koble til Dynamics 365 for Operations-miljøet. Dette emnet beskriver hvordan du installerer appen på enhetene. Det forklarer også hvordan du konfigurerer appen til å koble til Dynamics 365 for Operations-miljøet.

## <a name="prerequisites"></a>Forutsetninger
Appen er tilgjengelig på Android- og Windows-operativsystemer. For å bruke denne appen må du ha ett av de følgende støttede operativsystemene installert på enhetene. Du må også ha en av de følgende støttede versjonene av Dynamics 365 for Operations. Bruk informasjonen i tabellen nedenfor til å evaluere om maskinvare- og programvaremiljøet er klar til å støtte installasjonen.

| Plattform                    | Versjon                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (alle versjoner)                                                                                                                                                   |
| Dynamics 365 for Operations | Microsoft Dynamics 365 for Operations versjon 1611 -eller- Microsoft Dynamics Dynamics AX versjon 7.0/7.0.1 og Microsoft Dynamics AX-plattformoppdatering 2 med hurtigreparasjonen KB 3210014 |

## <a name="get-the-app"></a>Få appen
-   Windows (UWP) - [Dynamics 365 for Operations - Warehousing i Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Dynamics 365 for Operations - Warehousing på Google Play-butikken](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Opprette et webtjenesteprogram i Active Directory
For at appen skal kunne kommunisere med en bestemt Dynamics 365 for Operations-server, må du registrere et webtjenesteprogram i en Azure Active Directory for Dynamics-365 for Operations-leietaker. Av sikkerhetsgrunner anbefaler vi at du oppretter et webtjenesteprogram for hver enhet du bruker. Hvis du vil opprette et webtjenesteprogram i Azure Active Directory (Azure AD), kan du gjøre følgende:

1.  I en nettleser går du til <https://manage.windowsazure.com>.
2.  Skriv inn navnet og passordet for brukeren som har tilgang til Azure-abonnementet.
3.  I den venstre navigasjonsruten i Azure-portalen klikker du **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-eksempel](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Velg Active Directory-forekomsten som brukes av Dynamics 365 for Operations, i rutenettet.
5.  Klikk **Programmer** på den øverste verktøylinjen. [![wh-02-active-directory-programmer](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Klikk **Legg til** i den nedre ruten. Veiviseren **Legge til program** startes.
7.  Skriv inn et navn for programmet, og velg **Webapplikasjon og/eller web-API**. [![wh-03-active-directory-legg til-program](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Angi URL-adressen for pålogging, som er URL-adressen for app i leieren, rot-URL-adressen for Operations. URL-adressen for pålogging brukes ikke aktivt i godkjenning av appen, men det er et obligatorisk felt. Angi den samme URL-adressen i feltet App-ID/-URI. [![wh-04-ad-legg til-egenskaper](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  Gå til kategorien **Konfigurer**. [![wh-05-ad-konfigurer-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Rull nedover til du ser delen **Tillatelser til andre programmer**. Klikk **Legg til program**. [![wh-06-ad-app-legg til-tillatelser](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Velg **Microsoft Dynamics ERP** i listen. Klikk knappen **Fullfør sjekk** i høyre hjørne på siden. [![wh-07-ad-velg-tillatelser](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. I listen **Representanttillatelser** merker du av i alle avmerkingsboksene. Klikk **Lagre**. [![wh-08-ad-representant-tillatelser](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Noter deg følgende informasjon:
    -   **Klient-ID** - Når du ruller opp siden, vil du se at **Klient-ID** vises.
    -   **Nøkkel** - I **Nøkler**-delen oppretter du en nøkkel ved å velge varighet og kopiere nøkkelen. Denne nøkkelen vil senere bli referert til som **klienthemmeligheten**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Opprette og konfigurere en brukerkonto i Dynamics 365 for Operations
Hvis du vil aktivere Dynamics 365 for Operations til å bruke Azure AD-programmet, må du fullføre følgende konfigurasjonstrinn:

1.  Opprett en ny brukerkonto i Azure Active Directory for Dynamics 365 for Operations-leietakeren. Formålet med denne brukerkontoen er å gi tilgang til den bestemte egendefinerte tjenesten i lagerappen, som Dynamics 365 for Operations-serveren viser. Når du har fullført dette trinnet, vil du ha brukerlegitimasjon for WMDP, som består av en WMDP-e-postadresse og et WMDP-passord. Hvis du vil lære mer om de grunnleggende trinnene for å legge til brukere i Azure AD og Dynamics 365 for Operations, kan du se denne opplæringen: [Registrere deg for et abonnement for Microsoft Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/dev-tools/sign-up-preview-subscription).
2.  Opprett en Dynamics 365 for Operations-bruker som tilsvarer brukerlegitimasjonen for lagerappen.
    1.  I Dynamics 365 for Operations går du til **Systemadministrasjon** &gt; **Felles** &gt; **Brukere**.
    2.  Opprett en ny bruker.
    3.  Tilordne brukeren av lagermobilenhet, som vist i følgende skjermbilde. [![wh-09-legg til-bruker-sikkerhetsrolle](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Knytt Azure Active Directory-programmet til brukeren av lagerappen.
    1.  I Dynamics 365 for Operations går du til **Systemadministrasjon** &gt; **Oppsett** &gt; **Azure Active Directory-programmer**.
    2.  Opprett en ny linje.
    3.  Angi **klient-IDen** (hentet i den siste delen), gi den et navn og velg brukeren som er opprettet tidligere. Vi anbefaler at du angir koder for alle enheter slik at du enkelt kan fjerne tilgangen til Dynamics 365 for Operations fra denne siden i tilfelle de går tapt. [![wh-10-ad-programmer-skjema](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Konfigurer programmet
Du må konfigurere appen på enheten til å koble til Dynamics 365 for Operations-serveren gjennom Azure AD-programmet. Følg fremgangsmåten nedenfor for å gjøre dette:

1.  I appen går du til **Tilkoblingsinnstillinger**.
2.  Slett feltet **Demonstrasjonsmodus**. [![wh-11-app-tilkobling-innstillinger-demo-modus](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Angi følgende informasjon: **Klient-ID for Azure Active Directory** - IDen er hentet i trinn 13 i "Opprette et webtjenesteprogram i Active Directory". - **Klienthemmelighet for Azure Active Directory** - Klienthemmeligheten er hentet i trinn 13 i "Opprette et webtjenesteprogram i Active Directory". - **Azure Active Directory-ressurs** - Azure AD Directory-ressursen viser rot-URL-adressen for Dynamics 365 for Operations. **Obs!** Ikke avslutt dette feltet med en skråstrek (/). - **Azure Active Directory-leietaker** - Azure AD Directory-leietakeren som brukes med Dynamics 365 for Operations-serveren: https://login.windows.net/&lt;din-AD-leietaker-ID&gt;. Eksempel: https://login.windows.net/contosooperations.onmicrosoft.com. 
**Obs!** Ikke avslutt dette feltet med en skråstrek (/). - **Firma** - Angi den juridiske enheten i Dynamics 365 for Operations du vil koble programmet til. [![wh-12-app-tilkobling-innstillinger](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Velg **Tilbake**-knappen øverst til venstre i programmet. Programmet vil nå koble til Dynamics 365 for Operations-serveren, og påloggingsskjermbildet for lagermedarbeideren vises. [![wh-13-pålogging-skjerm](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Fjern tilgangen for en enhet
Hvis en enhet går tapt eller settes på spill, må du fjerne tilgangen til Dynamics 365 for Operations for enheten. Trinnene nedenfor beskriver den anbefalte prosessen for å fjerne tilgang.

1.  I Dynamics 365 for Operations går du til **Systemadministrasjon** &gt; **Oppsett** &gt; **Azure Active Directory-programmer**.
2.  Slett linjen som svarer til enheten du vil fjerne tilgang til. Noter **klient-IDen** som brukes for den fjernede enheten.
3.  Logg på den klassiske portalen for Azure på <https://manage.windowsazure.com>.
4.  Klikk på **Active Directory**-ikonet på den venstre menyen, og klikk deretter ønsket mappe.
5.  I den øverste menyen klikker du **Programmer**, og deretter klikker du programmet du vil konfigurere. **Introduksjonssiden** vises med enkel pålogging og annen konfigurasjonsinformasjon.
6.  Klikk kategorien **Konfigurer**, rull ned, og forsikre deg om at **klient-ID** for programmet er den samme som i trinn 2 i denne delen.
7.  Klikk **Slett**-knappen på kommandolinjen.
8.  Klikk **Ja** i bekreftelsesmeldingen.





