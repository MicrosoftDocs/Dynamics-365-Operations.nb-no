---
title: Oversikt over Installere og konfigurere lagerappen
description: Dette emnet beskriver hvordan du installerer og konfigurerer Dynamics 365 Supply Chain Management – Warehousing-appen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b8eb8dee88d8664391d2dcf485dff9dee4722cac
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251506"
---
# <a name="install-and-configure-the-warehousing-app-overview"></a>Oversikt over Installere og konfigurere lagerappen

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> Dette emnet beskriver hvordan du konfigurerer lager for skydistribusjoner. Hvis du leter etter hvordan du konfigurerer lager for lokale distribusjoner, kan du se [Lager for lokale distribusjoner](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


Dette emnet beskriver hvordan du installerer og konfigurerer Dynamics 365 Supply Chain Management – Warehousing-appen.

Warehousing-appen er tilgjengelig på Google Play-butikken og Windows Store. Denne appen tilbys for gjeldende versjon av Dynamics 365 Supply Chain Management som en frittstående komponent, som betyr selvdistribuering på enheter som brukes til lageroppgaver. For å bruke appen må du laste ned appen på hver enkelt enhet og konfigurere den til å koble til Supply Chain Management-miljøet. Dette emnet beskriver hvordan du installerer appen på enhetene. Det forklarer også hvordan du konfigurerer appen til å koble til Supply Chain Management-miljøet.

## <a name="prerequisites"></a>Forutsetninger
Appen er tilgjengelig på Android- og Windows-operativsystemer. For å bruke denne appen må du ha ett av de følgende støttede operativsystemene installert på enhetene. Du må også ha én av følgende versjoner som støttes: Bruk informasjonen i tabellen nedenfor til å evaluere om maskinvare- og programvaremiljøet er klar til å støtte installasjonen.

| Plattform                    | Versjon                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0, 9.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10 (alle versjoner)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations, versjon 1611 <br>- eller - <br>Microsoft Dynamics AX versjon 7.0/7.0.1 og Microsoft Dynamics AX plattformoppdatering 2 med hurtigreparasjon KB 3210014 |

## <a name="get-the-app"></a>Få appen
-   Windows (UWP)
     - [Finance and Operations - Lager i Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Finance and Operations - Warehousing på Google Play-butikken](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

> [!NOTE]
> Zebra App Gallery har utgått, noe som betyr at Warehousing-appen ikke lenger er tilgjengelig for nedlasting fra dette stedet.

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Opprette et webtjenesteprogram i Azure Active Directory
For at appen skal kunne kommunisere med en bestemt Supply Chain Management-server, må du registrere et webtjenesteprogram i en Azure Active Directory for Supply Chain Management-leietaker. Av sikkerhetsgrunner anbefaler vi at du oppretter et webtjenesteprogram for hver enhet du bruker. Hvis du vil opprette et webtjenesteprogram i Azure Active Directory (Azure AD), følger du denne fremgangsmåten:

1.  I en webleser kan du gå til <https://portal.azure.com>.
2.  Skriv inn navnet og passordet for brukeren som har tilgang til Azure-abonnementet.
3.  I den venstre navigasjonsruten i Azure-portalen klikker du **Azure Active Directory**.[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-eksempel](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  Kontroller at Active Directory-forekomsten er den som brukes av Supply Chain Management.
5.  I listen klikker du **Appregistreringer**. [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  I den øverste ruten klikker du på **Ny registrering**. Veiviseren **Legge til program** startes.
7.  Angi et navn på programmet, og velg **Bare kontoer i denne organisasjonskatalogen**. Klikk på **Registrer**.  [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  Den nye appregistreringen åpnes. [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  Husk **Program-ID**-en, du trenger den senere. **Program-ID**-en blir senere referert til som **klient-ID**.
10. Klikk på **Sertifikat og hemmeligheter** i **Behandle**-ruten. Klikk på **Ny klienthemmelighet**. [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)
11. Opprett en nøkkel ved å angi en beskrivelse og en varighet i **Passord**-delen. Klikk på **Legg til**, og kopier nøkkelen. Denne nøkkelen vil senere bli referert til som **klienthemmeligheten**. [![WMA-06-active-directory-save-key](./media/WMA-06-active-directory-save-key.png)](./media/WMA-06-active-directory-save-key.png)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Opprette og konfigurere en brukerkonto i Supply Chain Management
Hvis du vil aktivere Supply Chain Management til å bruke Azure AD-programmet, må du fullføre følgende konfigurasjonstrinn:

1.  Opprett en bruker som tilsvarer brukerlegitimasjonen for lagerappen.
    1.  Gå til **Systemadministrasjon** &gt; **Felles** &gt; **Brukere**.
    2.  Opprett en ny bruker.
    3.  Tilordne brukeren av lagermobilenhet, som vist i følgende skjermbilde. [![wh-09-legg til-bruker-sikkerhetsrolle](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

2.  Knytt Azure Active Directory-programmet til brukeren av lagerappen.
    1.  I Supply Chain Management går du til **Systemadministrasjon** &gt; **Oppsett** &gt; **Azure Active Directory-programmer**.
    2.  Opprett en ny linje.
    3.  Angi **klient-IDen** (hentet i den siste delen), gi den et navn og velg brukeren som er opprettet tidligere. Vi anbefaler at du angir koder for alle enheter slik at du enkelt kan fjerne tilgangen til Supply Chain Management fra denne siden i tilfelle de går tapt. [![wh-10-ad-programmer-skjema](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Konfigurer programmet
Du må konfigurere appen på enheten til å koble til Supply Chain Management-serveren gjennom Azure AD-programmet. Følg fremgangsmåten nedenfor for å gjøre dette:

1.  I appen går du til **Tilkoblingsinnstillinger**.
2.  Slett feltet **Demonstrasjonsmodus**. <br>[![wh-11-app-tilkobling-innstillinger-demo-modus](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Angi følgende informasjon: 
    + **Klient-ID for Azure Active Directory** - Klient-ID hentes i trinn 9 i "Opprette et webtjenesteprogram i Active Directory". 
    + **Klienthemmelighet for Azure Active Directory** - Klienthemmeligheten hentes i trinn 11 i "Opprette et webtjenesteprogram i Active Directory". 
    + **Azure Active Directory-ressurs** – Azure AD Directory-ressursen viser rot-URL-adressen for Supply Chain Management. **Obs!** Ikke avslutt dette feltet med en skråstrek (/). 
    + **Azure Active Directory-leietaker** – Azure AD Directory-leietakeren som brukes med Supply Chain Management-serveren: `https://login.windows.net/your-AD-tenant-ID` For eksempel: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**Obs!** Ikke avslutt dette feltet med en skråstrek (/). 
    + **Firma** – Angi den juridiske enheten i Supply Chain Management du vil koble programmet til. <br>[![wh-12-app-tilkobling-innstillinger](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Velg **Tilbake**-knappen øverst til venstre i programmet. Programmet vil nå koble til Supply Chain Management-serveren, og påloggingsskjermbildet for lagermedarbeideren vises. <br>[![wh-13-pålogging-skjerm](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

Du finner informasjon om hvordan du konfigurerer Warehousing-appen for å skanne strekkoder ved hjelp av et kamera på en mobil enhet, under [Skanne strekkoder ved hjelp av et kamera i Dynamics 365 for Finance and Operations – Warehousing](scan-bar-codes-using-a-camera.md)

## <a name="remove-access-for-a-device"></a>Fjern tilgangen for en enhet
Hvis en enhet går tapt eller settes på spill, må du fjerne tilgangen til Supply Chain Management for enheten. Trinnene nedenfor beskriver den anbefalte prosessen for å fjerne tilgang.

1.  Gå til **Systemadministrasjon** &gt; **Oppsett** &gt; **Azure Active Directory-programmer**.
2.  Slett linjen som svarer til enheten du vil fjerne tilgang til. Husk **klient-ID**-en som ble brukt for den fjernede enheten. Du trenger den senere.
3.  Logg på Azure-portalen på <https://portal.azure.com>.
4.  Klikk **Active Directory**-ikonet på venstre meny, og kontroller at du er i riktig mappe.
5.  I listen klikker du **Appregistreringer**, og deretter klikker du programmet du vil konfigurere. **Innstillinger**-siden vises med konfigurasjonsinformasjon.
6.  Pass på at **klient-ID**-en for programmet er den samme som i trinn 2 i denne delen.
7.  Klikk **Slett**-knappen i den øverste ruten.
8.  Klikk **Ja** i bekreftelsesmeldingen.
