---
title: Installer og koble til mobilappen Warehouse Management
description: Denne artikkelen beskriver hvordan du installerer Warehouse Management-mobilappen på hver av mobilenhetene og konfigurerer den slik at den kobler til Microsoft Dynamics 365 Supply Chain Management-miljøet ditt.
author: Mirzaab
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ec2a9f5ca6d6735e675defda6782738da7814c01
ms.sourcegitcommit: f2501d93ffc1c7bf4e0daa78e63bc37528ef2358
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/18/2022
ms.locfileid: "9171463"
---
# <a name="install-and-connect-the-warehouse-management-mobile-app"></a>Installer og koble til mobilappen Warehouse Management

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du laster ned og installerer Warehouse Management-mobilappen på hver av mobilenhetene, og hvordan du konfigurerer appen slik at den kobler til Supply Chain Management-miljøet ditt. Du kan konfigurere hver enhet manuelt, eller du kan importere tilkoblingsinnstillinger via en fil eller ved å skanne en QR-kode.

## <a name="system-requirements"></a>Systemkrav

Mobilappen Lagerstyring er tilgjengelig for operativsystemene Windows og Google Android. For å kunne bruke appen må et av de følgende støttede operativsystemene være installert på mobilenhetene:

- Windows 10 (Universal Windows Platform \[UWP\]) oktober 2018-oppdatering 1809 (build 10.0.17763) eller nyere
- Android 4.4 eller nyere

## <a name="turn-warehouse-management-mobile-app-features-on-or-off-in-supply-chain-management"></a>Aktivere eller deaktivere funksjoner for mobilappen Warehouse Management i Supply Chain Management

Du må aktivere funksjonen *Brukerinnstillinger, ikoner og trinntitler for den nye lagerappen* for systemet for å kunne bruke mobilappen Warehouse Management. Denne funksjonen er obligatorisk fra og med Supply Chain Management 10.0.25 og kan ikke deaktiveres. Hvis du kjører en eldre versjon enn 10.0.25, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Brukerinnstillinger, ikoner og trinntitler for den nye lagerappen* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="get-the-warehouse-management-mobile-app"></a>Hente mobilappen Lagerstyring

For mindre distribusjoner kan det ofte være lurt å installere appen på hver enhet fra den relevante butikken og deretter konfigurere tilkoblingen manuelt til miljøene du bruker.

For større distribusjoner kan du automatisere distribusjon og/eller konfigurasjon av appen, noe som gjør det mer hensiktsmessig å administrere mange enheter. Du kan for eksempel bruke en administrasjonsløsning for mobilenhet og en administrasjonsløsning for mobilprogram, for eksempel [Microsoft Intune](/mem/intune/fundamentals/what-is-intune). Hvis du vil ha informasjon om hvordan du bruker Intune til å legge til apper, kan du se [Legge til apper i Microsoft Intune](/mem/intune/apps/apps-add).

### <a name="install-the-app-from-an-app-store"></a>Installere appen fra en appbutikk

Den enkleste måten å installere appen på én enhet på, er å installere den fra en appbutikk, som alltid har den nyeste versjonen som er generelt tilgjengelig. Microsoft Intune kan også hente apper fra appbutikkene. Bruk en av koblingene nedenfor til å installere appen fra en appbutikk:

- **Windows (UWP):** [Lagerstyring i Microsoft Store](https://www.microsoft.com/store/apps/9pd35cdqcmg3)

- **Android:** [Lagerstyring i Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.WarehouseManagement)

### <a name="download-the-app-from-microsoft-app-center"></a>Laste ned appen fra Microsoft App Center

Som et alternativ til å installere fra en appbutikk, kan du i stedet laste ned appen fra Microsoft App Center. App Center inneholder installerbare pakker du kan legge ved siden av. I tillegg til den gjeldende versjonen kan du også laste ned tidligere versjoner, og du kan få forhåndsvisningsversjoner med kommende funksjoner som du kan prøve ut. Hvis du vil laste ned gjeldende, tidligere eller forhåndsvise versjoner av lagerstyringsappen fra Microsoft App Center, bruker du én av følgende koblinger:

- **Windows (UWP):** [Lagerstyring (Windows)](https://go.microsoft.com/fwlink/?linkid=2154406)  
    Hvis du vil ha instruksjoner om hvordan du installerer en nedlastet pakke på en Windows-enhet og deretter konfigurerer de nødvendige sertifikatene, kan du se [Installere en build fra App Center](/appcenter/distribution/installation).

- **Android:** [Lagerstyring (Android)](https://go.microsoft.com/fwlink/?linkid=2154613)  
    Hvis du laster ned en forhåndsversjon, må du gå gjennom noen ekstra trinn for å installere den. Hvis du vil ha mer informasjon, kan du se [Teste Android-apper](/appcenter/distribution/testers/testing-android).

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Opprette en webtjenesteapp i Azure Active Directory

For at mobilappen Lagerstyring skal kunne kommunisere med en bestemt Supply Chain Management-server, må du registrere et nettjenesteprogram for Supply Chain Management-leieren i Azure Active Directory (Azure AD). Følgende prosedyre viser én måte å fullføre denne oppgaven på. Hvis du vil ha detaljert informasjon og alternativer, kan du se koblingene etter prosedyren.

1. I en nettleser går du til [https://portal.azure.com](https://portal.azure.com/).
1. Skriv inn navnet og passordet for brukeren som har tilgang til Azure-abonnementet.
1. I Azure-portalen velger du **Azure Active Directory** i navigasjonsruten til venstre.

    ![Azure Active Directory.](media/app-connect-azure-aad.png "Azure Active Directory")

1. Sørg for at du arbeider med forekomsten av Azure AD som brukes av Supply Chain Management.
1. I listen **Behandle** velger du **Appregistreringer**.

    ![Appregistreringer.](media/app-connect-azure-register.png "Appregistreringer")

1. På verktøylinjen velger du **Ny registrering** for å åpne veiviseren **Registrere en app**.
1. Angi et navn for appen, velg alternativet **Bare kontoer i denne organisasjonskatalogen**, og velg deretter **Registrer**.

    ![Veiviseren Registrere en app.](media/app-connect-azure-register-wizard.png "Veiviseren Registrere en app")

1. Den nye appregistreringen åpnes. Noter verdien i **App-ID (klient)** ettersom du vil trenge den senere. Det vil bli referert til denne ID-en senere i denne artikkelen som *klient-ID-en*.

    ![App-ID (klient).](media/app-connect-azure-app-id.png "App-ID (klient)")

1. I listen **Behandle** velger du **Sertifikat og hemmeligheter**. Deretter velger du en av de følgende knappene, avhengig av hvordan du vil konfigurere appen for godkjenning. (Hvis du vil ha mer informasjon, kan du se delen [Godkjenne ved å bruke et sertifikat eller en klienthemmelighet](#authenticate) senere i denne artikkelen.)

    - **Laste opp sertifikat** – Last opp et sertifikat som skal brukes som hemmelighet. Denne metoden anbefales ettersom den er sikrere og også kan automatiseres fullstendig. Hvis du kjører mobilappen Lagerstyring på Windows-enheter, noterer du verdien for **Avtrykk** som vises etter at du har lastet opp sertifikatet. Du vil trenge denne verdien når du konfigurerer sertifikatet på Windows-enheter.
    - **Ny klient hemmelighet** – Opprett en nøkkel ved å angi en nøkkelbeskrivelse og en varighet i delen **Passord**, og velg deretter **Legg til**. Ta en kopi av nøkkelen og lagre den på en sikker måte.

    ![Sertifikat og hemmeligheter.](media/app-connect-azure-authentication.png "Sertifikat og hemmeligheter")

Hvis du vil ha mer informasjon om hvordan du definerer webtjenesteapper i Azure AD, kan du se følgende ressurser:

- Hvis du vil ha instruksjoner som viser hvordan du bruker Windows PowerShell til å konfigurere webtjenesteapper i Azure AD, kan du se [Fremgangsmåte: Bruke Azure PowerShell til å opprette en tjenestekontohaver med et sertifikat](/azure/active-directory/develop/howto-authenticate-service-principal-powershell).
- Hvis du vil ha fullstendig informasjon om hvordan du oppretter en webtjenesteapp manuelt i Azure AD, kan du se følgende artikler:

    - [Hurtigstart: Registrere en app med Microsoft-identitetsplattformen](/azure/active-directory/develop/quickstart-register-app)
    - [Fremgangsmåte: Bruke portalen til å opprette en Azure AD-app og tjenestekontohaver som har tilgang til ressurser](/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a><a name="user-azure-ad"></a>Opprette og konfigurere en brukerkonto i Supply Chain Management

Hvis du vil at Supply Chain Management skal kunne bruke Azure AD-appen, gjør du følgende.

1. Opprett en bruker som er knyttet til brukerlegitimasjonen for mobilappen Lagerstyring:

    1. I Supply Chain Management går du til **Systemadministrasjon \> Brukere \> Brukere**.
    1. Opprett en bruker.
    1. Tilordne rollen som *bruker av lagermobilenhet* til brukeren.

    ![Tilordne mobilenhetsbrukeren for lagerstyring.](media/app-connect-app-users.png "Tilordne mobilenhetsbrukeren for lagerstyring")

1. Knytt Azure AD-programmet til brukeren av mobilappen Lagerstyring:

    1. Gå til **Systemadministrasjon \> Oppsett \> Azure Active Directory-apper**.
    1. Velg **Ny** i handlingsruten for å opprette en linje.
    1. I **Klient-ID**-feltet angir du klient-IDen du noterte deg i forrige del.
    1. Angi et navn i **Navn**-feltet.
    1. Velg bruker-IDen du nettopp opprettet i **Bruker-ID**-feltet.

    ![Azure Active Directory-apper.](media/app-connect-aad-apps.png "Azure Active Directory-bruksområder")

> [!TIP]
> En måte å bruke disse innstillingene på, er å opprette en klient-ID i Azure for hver av de fysiske enhetene dine, og deretter legge til hver klient-ID på **Azure Active Directory-programmer**-siden. Hvis en enhet går tapt, kan du enkelt fjerne dens tilgang til Supply Chain Management ved å fjerne klient-ID fra denne siden. (Denne fremgangsmåten fungerer fordi tilkoblingslegitimasjonen som lagres på hver enhet, også angir en klient-ID, som beskrevet senere i denne artikkelen.)
>
> I tillegg er standardspråket, nummerformatet og tidssoneinnstillingene for hver klient-ID fastsatt av innstillingene som er angitt for **bruker-ID**-verdien som er tilordnet her. Derfor kan du bruke disse innstillingene til å opprette standardinnstillinger for hver enhet eller samling enheter, basert på klient-IDen. Disse standardinnstillingene vil imidlertid overstyres hvis de også er definert for *lagerappbrukerkontoen* som en arbeider bruker til å logge på enheten. (Hvis du vil ha mer informasjon, kan du se [Brukerkontoer for mobilenhet](mobile-device-work-users.md).)

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Godkjenne ved hjelp av et sertifikat eller en klienthemmelighet

Godkjenning med Azure AD er en sikker metode for å koble en mobil enhet til Supply Chain Management. Du kan godkjenne ved hjelp av en klienthemmelighet eller et sertifikat. Hvis du vil importere tilkoblingsinnstillinger, anbefales det at du bruker et sertifikat i stedet for et klienthemmelighet. Ettersom klienthemmeligheten alltid må lagres på en sikker måte, kan du ikke importere den fra en fil for tilkoblingsinnstillinger eller en QR-kode, som beskrevet senere i denne artikkelen.

Sertifikater kan brukes som hemmeligheter for å bevise appens identitet når det bes om en token. Fellesdelen av sertifikatet lastes opp til appregistreringen i Azure-portalen, mens det fullstendige sertifikatet må distribueres på hver enhet der mobilappen Lagerstyring er installert. Organisasjonen din er ansvarlig for å administrere sertifikatet når det gjelder rotasjon og så videre. Du kan bruke selvsignerte sertifikater, men du bør alltid bruke sertifikater som ikke kan eksporteres.

Du må angi at sertifikatet skal være tilgjengelig lokalt på hver enhet der du kjører mobilappen Lagerstyring. Hvis du vil ha informasjon om hvordan du behandler sertifikater for Intune-kontrollerte enheter hvis du bruker Intune, kan du se [Bruke sertifikater til godkjenning i Microsoft Intune](/mem/intune/protect/certificates-configure).

## <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Konfigurer Warehouse Management-mobilappen for sky- og kantskalaenheter

Det kreves noen ekstra trinn hvis du planlegger å kjøre Warehouse Management-mobilappen mot en sky- eller kantskalaenhet. For instruksjoner kan du se [Konfigurere Warehouse Management-mobilappen for sky- og kantskalaenheter](../cloud-edge/cloud-edge-workload-setup-warehouse-app.md).

## <a name="configure-the-application-by-importing-connection-settings"></a>Konfigurere appen ved å importere tilkoblingsinnstillinger

Hvis du vil gjøre det enklere å vedlikeholde og distribuere appen på mange mobile enheter, kan du importere tilkoblingsinnstillingene i stedet for å angi dem manuelt på hver enhet. Denne delen forklarer hvordan du oppretter og importerer innstillingene.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Opprette en fil for tilkoblingsinnstillinger eller QR-kode

Du kan importere tilkoblingsinnstillinger fra enten en fil eller en QR-kode. I begge fremgangsmåtene må du først opprette en innstillingsfil som bruker JSON-format (JavaScript Object Notation) og JSON-syntaks. Filen må inneholde en tilkoblingsliste som inneholder de enkelte tilkoblingene som må legges til. Følgende tabell viser en oversikt over parameterne du må angi i filen tilkoblingsinnstillinger.

| Parameter | beskrivelse |
|---|---|
| ConnectionName | Angi navnet på tilkoblingsstrengen. Maksimumslengden er 20 tegn. Ettersom denne verdien er den unike identifikatoren for en tilkoblingsinnstilling, må du kontrollere at den er unik i listen. Hvis det allerede finnes en tilkobling med samme navn på enheten, vil den bli overstyrt av innstillingene fra den importerte filen. |
| ActiveDirectoryClientAppId | Angi klient-ID-en du noterte deg da du konfigurerte Azure AD i delen [Opprette en webtjenesteapp i Azure Active Directory](#create-service). |
| ActiveDirectoryResource | Angi rot-URL-adressen til Supply Chain Management. |
| ActiveDirectoryTenant | Angi Azure AD-domenenavnet du bruker med Supply Chain Management-serveren. Denne verdien har formen `https://login.windows.net/<your-Azure-AD-domain-name>`. Her er et eksempel: `https://login.windows.net/contosooperations.onmicrosoft.com`. Hvis du vil ha mer informasjon om hvordan du finner Azure AD-domenenavnet, kan du se [Finn viktige ID-er for en bruker](/partner-center/find-ids-and-domain-names). |
| Bedrift | Angi den juridiske enheten i Supply Chain Management du vil koble appen til. |
| ConnectionType | (Valgfritt) Angi om tilkoblingsinnstillingen skal bruke et sertifikat eller klienthemmelighet til å koble til et miljø. Gyldige verdier er *certificate* og *clientsecret*. Standardverdien er *certificate*.<p>**Obs!** Klienthemmeligheter kan ikke importeres.</p> |
| IsEditable | (Valgfritt) Angi om appbrukeren skal kunne redigere tilkoblingsinnstillingen. Gyldige verdier er *true* og *false*. Standardverdien er *true*. |
| IsDefault | (Valgfritt) Angi om tilkoblingen er standardtilkoblingen. En tilkobling som er angitt som standardtilkobling, blir automatisk forhåndsmerket når appen åpnes. Bare én tilkobling kan angis som standardtilkoblingen. Gyldige verdier er *true* og *false*. Standardverdien er *false*. |
| CertificateThumbprint | (Valgfritt) For Windows-enheter kan du angi sertifikatavtrykket for tilkoblingen. For Android-enheter må appbrukeren velge sertifikatet første gang en tilkobling brukes. |

Følgende eksempel viser en gyldig fil for tilkoblingsinnstillinger som inneholder to tilkoblinger. Som du kan se, er tilkoblingslisten (kalt *ConnectionList* i filen) et objekt som har en matrise som lagrer hver tilkobling som et objekt. Hvert objekt må settes i klammeparenteser ({}) og atskilles med komma, og matrisen må settes i hakeparenteser (\[\]).

```json
{
    "ConnectionList": [
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection1",
            "ActiveDirectoryResource": "https://yourenvironment.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": false,
            "IsDefaultConnection": true,
            "CertificateThumbprint": "aaaabbbbcccccdddddeeeeefffffggggghhhhiiiii",
            "ConnectionType": "certificate"
        },
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection2",
            "ActiveDirectoryResource": "https://yourenvironment2.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": true,
            "IsDefaultConnection": false,
            "ConnectionType": "clientsecret"
        }
    ]
}
```

Du kan enten lagre informasjonen som en JSON-fil, eller generere en QR-kode som har samme innhold. Hvis du lagrer informasjonen som en fil, anbefales det at du lagrer den ved hjelp av standardnavnet, *connections.json*, spesielt hvis du skal lagre den på standardplasseringen på hver mobile enhet.

### <a name="save-the-connection-settings-file-on-each-device"></a>Lagre filen for tilkoblingsinnstillinger på hver enhet

Vanligvis vil du bruke et verktøy eller skript for enhetsbehandling til å distribuere filene for tilkoblingsinnstillinger til hver enhet du administrerer. Hvis du bruker standardnavnet og -plasseringen når du lagrer filen for tilkoblingsinnstilling på hver enhet, vil mobilappen Lagerstyring automatisk importere den, også i den første kjøringen etter at appen er installert. Hvis du bruker et egendefinert navn eller en plassering for filen, må appbrukeren angi verdiene under første kjøring. Appen vil imidlertid fortsette å bruke det angitte navnet og den valgte plasseringen etterpå.

Hver gang appen startes, importeres tilkoblingsinnstillingene på nytt fra den forrige plasseringen for å fastslå om det har blitt gjort endringer. Appen vil bare oppdatere tilkoblinger som har samme navn som tilkoblingene i filen for tilkoblingsinnstilling. Brukeropprettede tilkoblinger som bruker andre navn, blir ikke oppdatert.

Du kan ikke fjerne en tilkobling ved hjelp av filen for tilkoblingsinnstillinger.

Som er nevnt, er standard filnavn *connections.json*. Standard filplassering avhenger av om du bruker en Windows-enhet eller en Android-enhet:

- **Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.WarehouseManagement_8wekyb3d8bbwe\LocalState`
- **Android:** `Android\data\com.Microsoft.WarehouseManagement\files`

Vanligvis opprettes banene automatisk etter første kjøring av appen. Du kan imidlertid opprette dem manuelt hvis du må overføre filen for tilkoblingsinnstillinger til enheten før du installerer.

> [!NOTE]
> Hvis appen avinstalleres, fjernes standardbanen og innholdet i den.

### <a name="import-the-connection-settings"></a>Importere tilkoblingsinnstillingene

Gjør følgende for å importere tilkoblingsinnstillinger fra en fil eller en QR-kode.

1. Start mobilappen Lagerstyring på mobilenheten. Første gang du starter appen, vises det en velkomstmelding. Velg **Velg en tilkobling**.

    ![Velkomstmelding.](media/app-configure-welcome-screen.png "Velkomstmelding")

1. Hvis du importerer tilkoblingsinnstillingene fra en fil og standardnavnet og -plasseringen ble brukt da filen ble lagret, kan det hende at appen allerede har funnet filen. I dette tilfellet kan du gå videre til trinn 4. Hvis ikke velger du **Konfigurer tilkobling** og fortsetter deretter til trinn 3.

    ![Konfigurer tilkobling.](media/app-configure-set-up-connection.png "Konfigurer tilkobling")

1. Velg **Legg til fra fil** eller **Legg til fra QR-kode** i dialogboksen **Tilkoblingsoppsett**, avhengig av hvordan du vil importere innstillingene:

    - Hvis du importerer tilkoblingsinnstillingene fra en fil, velger du **Legg til fra fil**, blar til filen på den lokale enheten og velger den. Hvis du velger en egendefinert plassering, lagrer appen den og bruker den automatisk neste gang.
    - Hvis du importerer tilkoblingsinnstillingene ved å skanne en QR-kode, velger du **Legg til fra QR-kode**. Appen ber deg om å få tillatelse til å bruke enhetens kamera. Når du har gitt tillatelse, startes kameraet slik at du kan bruke det til skanning. Avhengig av kvaliteten på enhetens kamera og kompleksiteten i QR-koden, kan det være vanskelig å få en riktig skanning. I så fall kan du forsøke å redusere kompleksiteten i QR-koden ved bare å generere én tilkobling per QR-kode. (For øyeblikket kan du bare bruke enhetskameraet til å skanne QR-koden.)

    ![Menyen Tilkoblingsoppsett.](media/app-configure-connection-setup-flyout.png "Menyen Tilkoblingsoppsett")

1. Etter at tilkoblingsinnstillingene er lastet inn, vises den valgte tilkoblingen.

    ![Tilkoblingsinnstillinger lastet.](media/app-configure-select-connection.png "Tilkoblingsinnstillinger lastet")

1. Hvis du bruker en Android-enhet og bruker et sertifikat for godkjenning, ber enheten deg om å velge sertifikatet.

    ![Velge sertifikatledetekst på en Android-enhet.](media/app-configure-select-certificate.png "Velge sertifikatledetekst på en Android-enhet")

1. Appen kobler seg til Supply Chain Management-serveren og viser påloggingssiden.

    ![Påloggingsside.](media/app-configure-sign-in-page.png "Påloggingsside")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>Konfigurere appen manuelt

Hvis du ikke har en fil eller QR-kode, kan du konfigurere appen manuelt på enheten slik at den kobler til Supply Chain Management-serveren via Azure AD-programmet.

1. Start mobilappen Lagerstyring på mobilenheten.
1. Hvis appen startes i **Demonstrasjonsmodus**, velger du **Tilkoblingsinnstillinger**. Hvis **Pålogging**-siden vises når appen startes, velger du **Bytt tilkobling**.
1. Velg **Konfigurer tilkobling**.

    ![Konfigurer tilkobling.](media/app-configure-set-up-connection.png "Konfigurer tilkobling")

1. Velg **Angi manuelt**.

    ![Menyen Tilkoblingsoppsett.](media/app-configure-connection-setup-flyout.png "Menyen Tilkoblingsoppsett")

    Siden **Ny tilkobling** vises og inneholder innstillingene som kreves for å angi tilkoblingsdetaljene manuelt.

    ![Manuelle tilkoblingsfelt.](media/app-configure-input-manually.png "Manuelle tilkoblingsfelt")

1. Angi følgende informasjon:

    - **Bruk klient hemmelighet** – Sett dette alternativet til _Ja_ for å bruke et klienthemmelighet til å godkjenne med Supply Chain Management. Sett den til _Nei_ for å bruke et sertifikat for godkjenning. (Hvis du vil ha mer informasjon, kan du se delen [Opprette et nettjenesteprogram i Azure Active Directory](#create-service) tidligere i denne artikkelen.)
    - **Tilkoblingsnavn** – Angi et navn for den nye tilkoblingen. Dette navnet vil vises i feltet **Velg tilkobling** neste gang du åpner tilkoblingsinnstillingene. Navnet du angir, må være unikt. (Det må med andre ord være forskjellig fra alle andre tilkoblingsnavn som er lagret på enheten, hvis andre tilkoblingsnavn er lagret der.)
    - **Klient-ID for Active Directory** – Angi klient-ID-en du noterte deg under konfigurasjon av Azure AD i delen [Opprette en webtjenesteapp i Azure Active Directory](#create-service).
    - **Klienthemmelighet for Active Directory** – Dette feltet er bare tilgjengelig når alternativet **Bruk klienthemmelighet** er satt til _Ja_. Angi klienthemmeligheten du noterte deg da du konfigurerte Azure AD i delen [Opprette en webtjenesteapp i Azure Active Directory](#create-service).
    - **Sertifikatavtrykk for Active Directory** – Dette feltet er bare tilgjengelig for Windows-enheter og bare når alternativet **Bruk klienthemmelighet** er satt til _Nei_. Angi sertifikatavtrykket du noterte deg da du konfigurerte Azure AD i delen [Opprette en webtjenesteapp i Azure Active Directory](#create-service).
    - **Active Directory-ressurs** – Angi rot-URL-adressen til Supply Chain Management.

        > [!IMPORTANT]
        > Ikke avslutt denne verdien med en skråstrek (/).

    - **Active Directory-leier** – Angi Azure AD-domenenavnet du bruker med Supply Chain Management-serveren. Denne verdien har formen `https://login.windows.net/<your-Azure-AD-domain-name>`. Her er et eksempel: `https://login.windows.net/contosooperations.onmicrosoft.com`. Hvis du vil ha mer informasjon om hvordan du finner Azure AD-domenenavnet, kan du se [Finn viktige ID-er for en bruker](/partner-center/find-ids-and-domain-names).

        > [!IMPORTANT]
        > Ikke avslutt denne verdien med en skråstrek (/).

    - **Firma** – Angi den juridiske enheten (firmaet) i Supply Chain Management som du vil koble programmet til.

1. Velg knappen **Lagre** i hjørnet øverst til høyre på siden.
1. Hvis du bruker en Android-enhet og bruker et sertifikat for godkjenning, ber enheten deg om å velge sertifikatet.
1. Appen kobler seg til Supply Chain Management-serveren og viser påloggingssiden.

## <a name="remove-access-for-a-device"></a>Fjern tilgangen for en enhet

Hvis en enhet går tapt eller blir en sikkerhetsrisiko, må du fjerne tilgangen til Supply Chain Management for den. Trinnene nedenfor beskriver den anbefalte prosessen for å fjerne tilgang.

1. Gå til **Systemadministrasjon \> Oppsett \> Azure Active Directory-apper**.
1. Slett linjen som er knyttet til enheten du vil fjerne tilgang for. Noter deg hvilken klient-ID som brukes for enheten, siden du trenger den senere.

    Hvis du har registrert bare én klient-ID, og flere enheter bruker samme klient-ID, må du bruke de nye tilkoblingsinnstillingene på disse enhetene. Hvis ikke vil de miste tilgang.

1. Logg på Azure-portalen på [https://portal.azure.com](https://portal.azure.com/).
1. Velg **Active Directory** i navigasjonsruten til venstre, og kontroller at du er i riktig mappe.
1. I listen **Behandle** velger du **Appregistreringer**, og deretter velger du appen du vil konfigurere. Siden **Innstillinger** vises med konfigurasjonsinformasjon.
1. Kontroller at klient-ID-en til appen samsvarer med klient-ID-en du noterte i trinn 2.
1. Velg **Slett** på verktøylinjen.
1. Velg **Ja** i bekreftelsesmeldingen som vises.

## <a name="additional-resources"></a>Tilleggsressurser

- [Brukinnstillinger for mobilenhet](mobile-device-user-settings.md)
- [Tilordne trinnikoner og -titler for mobilappen Warehouse Management](step-icons-titles.md)
- [Konfigurer Warehouse Management-mobilappen for sky- og kantskalaenheter](../cloud-edge/cloud-edge-workload-setup-warehouse-app.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
