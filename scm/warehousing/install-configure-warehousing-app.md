---
title: 'Installerer og konfigurerer Microsoft Dynamics 365 for operasjoner & #8211; Lagerstyring'
description: Dette emnet beskriver hvordan du installerer og konfigurerer Microsoft Dynamics 365 for operasjoner - lager.
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 231c087ddc976aa552fc9cd6c89188f82a0247d1
ms.lasthandoff: 03/31/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Installerer og konfigurerer Microsoft Dynamics 365 for operasjoner & #8211; Lagerstyring

Dette emnet beskriver hvordan du installerer og konfigurerer Microsoft Dynamics 365 for operasjoner - lager.

Dynamics 365 for operasjoner - lager er et program som er tilgjengelig på Google spill butikk og Windows butikken. Denne app tilbys for den gjeldende versjonen av Microsoft Dynamics 365 for operasjoner som en frittstående komponent, som betyr selv distribuering på enheter som brukes til oppgaver i lageret. For å bruke programmet i Dynamics-365 for driftsmiljø, må du laste ned app på hver enhet og konfigurere den til å koble til din Dynamics 365 for driftsmiljø. Dette emnet beskriver hvordan du installerer programmet på enhetene. Den forklarer også hvordan du konfigurerer app til å koble til din Dynamics 365 for driftsmiljø.

## <a name="prerequisites"></a>Forutsetninger
Programmet er tilgjengelig på Android og Windows-operativsystemer. Hvis du vil bruke dette programmet, må du ha ett av de følgende støttede operativsystemene som er installert på enhetene. Du må også ha en av følgende støttede versjoner av Dynamics 365 for operasjoner. Bruk informasjonen i tabellen nedenfor til å evaluere hvis miljøet maskinvare og programvare som er klar til å støtte installasjonen.

| Plattform                    | Versjon                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows-10 (alle versjoner)                                                                                                                                                   |
| Dynamics 365 for operasjoner | Microsoft Dynamics-365 for operasjoner 1611 - eller - Microsoft Dynamics Dynamics AX versjon 7.0/7.0.1 og plattform for Microsoft Dynamics AX oppdatere 2 med hurtigreparasjonen KB 3210014 |

## <a name="get-the-app"></a>Få programmet
-   Windows (UWP) - [Dynamics 365 for operasjoner - lager på Windows-butikken](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Dynamics 365 for operasjoner - lager på Google Play-butikken](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Opprette en web-tjenesteprogram i Active Directory
Hvis du vil aktivere app til å kommunisere med en bestemt Dynamics 365 for operasjoner-server, må du registrere et webprogram for tjenesten i en Active Directory Azure for Dynamics-365 for operasjoner leietakeradministrasjon. Av sikkerhetsgrunner anbefaler vi at du oppretter en web-tjenesteprogram for hver enhet du bruker. Hvis du vil opprette en web-tjenesteprogram i Azure Active Directory (AD Azure), kan du gjøre følgende:

1.  I en webleser, kan du gå til <https://manage.windowsazure.com>.
2.  Skriv inn navnet og passordet for brukeren som har tilgang til Azure abonnementet.
3.  Klikk i den venstre navigasjonsruten i Azure Portal **Active Directory**. [](./media/wh-01-active-directory-example.png)[![Hv-01-aktiv-directory-eksempel](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Velg Active Directory-forekomsten som brukes av Dynamics 365 for operasjoner i rutenettet.
5.  Klikk på den øverste verktøylinjen **programmer**. [![Hv-02-aktiv-directory-programmer](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  I den nederste ruten, klikker du **Legg til**. Den **legge til program** startes.
7.  Skriv inn et navn for programmet, og velg **Web-applikasjon og/eller web-APIen**. [![Wh-03-Active-Directory-Add-Application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Angi pålogging URL, som er URL-adressen for programmet i din leier, rot-URL-adressen for operasjoner. Pålogging på URL-adressen aktivt brukes ikke i godkjenning av programmet, men det er et obligatorisk felt. Angi samme URL-adressen i feltet ID for tjenesteprogram-URI. [![Hv-04-ad-Legg til-egenskaper](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  Gå til den **Konfigurer** i kategorien. [![Hv-05-ad-konfigurere-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Rull nedover til du ser den **tillatelser for andre programmer** delen. Klikk **legge til program**. [![Wh-06-AD-App-Add-Permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Velg **Microsoft Dynamics ERP** i listen. Klikk på **fullføre** i høyre hjørne på siden. [![Hv-07-ad-select-tillatelser](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. I den **Representanttillatelser** velger alle avmerkingsboksene. Click **Save**. [![Hv-08-ad--Representanttillatelser](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Noter deg følgende informasjon:
    -   **Klient-ID** - når du ruller opp siden, vil du se **klient-ID** vises.
    -   **Nøkkel** - i den **nøkler** delen oppretter du en nøkkel ved å velge varigheten og kopiere nøkkelen. Denne nøkkelen vil senere bli referert til som den **klient hemmelig**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Opprette og konfigurere en brukerkonto i Dynamics 365 for operasjoner
Hvis du vil aktivere Dynamics 365 for operasjoner å bruke Azure AD-programmet, må du fullføre følgende konfigurasjon:

1.  Opprette en ny brukerkonto i Active Directory-Azure for Dynamics-365 for operasjoner leietakeradministrasjon. Formålet med denne brukerkontoen er tilgang til bestemte egendefinerte tjenesten av datalagerstyring app, som viser Dynamics-365 for serveren for operasjoner. Når du har fullført dette trinnet, vil du ha brukerlegitimasjon for WMDP, som består av en WMDP e-postadresse og et passord for WMDP. Lære mer om de grunnleggende trinnene for å legge til brukere i Azure AD og Dynamics 365 for operasjoner, kan du se denne opplæringen: [registrere deg for en Microsoft Dynamics-365 for operasjoner abonnement](/dynamics365/operations/dev-itpro/sign-up-preview-subscription).
2.  Opprette en Dynamics 365 for operasjoner bruker som tilsvarer datalagerstyring app brukerlegitimasjonen.
    1.  I Dynamics 365 for operasjoner, kan du gå til **systemadministrasjon**&gt;**vanlige**&gt;**brukere**.
    2.  Opprett en ny bruker.
    3.  Tilordne lager mobil enhet bruker, som vist i følgende skjermbilde. [![Wh-09-Add-User-Security-Role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Knytte Azure Active Directory-programmet datalagerstyring app brukeren.
    1.  I Dynamics 365 for operasjoner, kan du gå til **systemadministrasjon**&gt;**Setup**&gt;**Azure Active Directory programmer**.
    2.  Opprett en ny linje.
    3.  Angi de **klient-ID** (fikk tak i den siste delen), gi den et navn, og velg brukeren som opprettet tidligere. Vi anbefaler at du angir koder for alle enheter slik at du kan enkelt fjerne deres tilgang til Dynamics 365 for operasjoner fra denne siden i tilfelle de går tapt. [![Hv-10-ad-programmer-skjema](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Konfigurer programmet
Du må konfigurere programmet på enheten til å koble til Dynamics-365 for operasjoner server gjennom AD Azure-program. Hvis du vil gjøre dette, må du fullføre trinnene nedenfor.

1.  I app, kan du gå til **tilkoblingsinnstillinger**.
2.  Fjern den **demonstrasjonsmodus** feltet. [![Wh-11-App-Connection-Settings-demo-Mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Angi følgende informasjon:- **Azure Active directory-klient-ID** -IDen er hentet i trinn 13 i "Opprette en web-tjenesteprogram i Active Directory" klienten. - **Azure Active directory client hemmelig** -klient-hemmeligheten er hentet i trinn 13 i "Opprette en web-tjenesteprogram i Active Directory". - **Azure Active directory-ressursen** -Azure AD-ressurs viser Dynamics-365 for rot-URL for operasjoner. **Legg merke til**: ikke avslutte dette feltet med en skråstrek (/). - **Azure Active directory leier** -Azure AD directory klientadministrasjon brukes med Dynamics-365 for operasjoner server: https://login.windows.net/&lt;din-AD-leier-ID&gt;. For eksempel: https://login.windows.net/contosooperations.onmicrosoft.com. 
**Legg merke til**: ikke avslutte dette feltet med en skråstrek (/). - **Selskapet** -angir den juridiske enheten i Dynamics 365 for operasjoner som du vil at programmet skal koble til. [![Hv-12-app--tilkoblingsinnstillinger](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Velg den **tilbake** -knappen i hjørnet øverst til venstre i programmet. Programmet vil nå koble til din Dynamics 365 for operasjoner server og påloggingsskjermbildet for Lagermedarbeideren vises. [![Hv-13-login-skjermen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Fjern tilgang for en enhet
Hvis det er en tapt eller utsatt-enhet, må du fjerne tilgang til Dynamics 365 for operasjoner for enheten. Trinnene nedenfor beskriver anbefalte prosessen for å fjerne tilgang.

1.  I Dynamics 365 for operasjoner, kan du gå til **systemadministrasjon**&gt;**Setup**&gt;**Azure Active Directory programmer**.
2.  Slett linjen som svarer til enheten du vil fjerne tilgang. Noter ned den **klient-ID** brukes for den fjernede enheten.
3.  Logg på Azure klassisk portal på <https://manage.windowsazure.com>.
4.  Klikk på **Active Directory** -ikonet på venstre menyen, og klikk deretter ønsket mappe.
5.  I den øverste menyen, velg **programmer**, og klikk deretter programmet du vil konfigurere. Den **Quick Start** siden vises med enkel pålogging og annen konfigurasjonsinformasjon.
6.  Klikk på **Konfigurer** kategorien, Rull ned, og forsikre deg om at den **klient-ID** er den samme som i trinn 2 i denne delen av programmet.
7.  Klikk på **sletter** -knappen i kommandolinjen.
8.  Klikk **Ja** i bekreftelsesmeldingen.



