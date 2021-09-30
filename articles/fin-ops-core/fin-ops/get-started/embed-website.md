---
title: Bygge inn tredjepartsapper
description: Dette emnet forklarer hvordan du bygger inn tredjepartsapper for å øke produktets funksjonalitet.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, UserWorkspaceAdd, UserWorkspaceConfigureWebsite
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 89f101bcf33080f6a73664fe7c3fe6719de04a4e
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488240"
---
# <a name="embed-third-party-apps"></a>Bygge inn tredjepartsapper

[!include [banner](../includes/banner.md)]

Mange kunder bruker en rekke programmer for å drive virksomheten sin. Noen av disse programmene er tredjepartswebapper som fungerer sammen med Finance and Operations-apper. For å gi en mer sømløs brukeropplevelse kan du bruke funksjonen **Helside-apper** til å bygge inn disse tredjepartsappene direkte i Finance and Operations-appene dine (forutsatt at tredjepartsappene tillater at de legges inn). På denne måten kan brukere få tilgang til webområder og apper som de krever, uten at de behøver å bytte kategorier eller vinduer.

Før du kan bygge inn tredjepartsapper i produktet, må du aktivere funksjonen **Helside-apper** i Funksjonsbehandling. Deretter kan du bruke en av følgende metoder til å bygge inn en tredjepartsapp eller et webområde. Disse metodene er analoge til metodene som brukes til å bygge inn lerretsapper fra Microsoft Power Apps til Finance and Operations-apper.

- Bygg inn appen eller webområdet på en eksisterende side som en ny kategoriside (pivotfane, hurtigfane, blad eller arbeidsområde).
- Opprett en ny fullsideopplevelse for appen eller webområdet fra instrumentbordet.

## <a name="embed-a-website-on-an-existing-page"></a>Bygge inn et webområde på en eksisterende side

Bruk denne fremgangsmåten hvis du vil supplere en eksisterende side i systemet med en innebygd app.

1. Åpne siden der du vil bygge inn appen.
2. Åpne **Legg til en app**-ruten:

    1. Velg **Innstillinger** og deretter **Tilpass** for å åpne **Tilpassing**-verktøylinjen.
    2. Velg **Mer \> Legg til en app**.

3. Velg området på siden der du vil legge til appen. Dette området må være en *kategoricontainer* for en pivotfane, hurtigfane, et blad eller et arbeidsområde.
4. Velg **webområde**.
5. Konfigurer den innebygde appen:

    - **Navn** – Angi teksten som skal vises for kategorien som inneholder den innebygde appen. Ofte vil du at denne teksten skal være navnet på appen.
    - **URL-adresse** – Angi plasseringen for appen.

    > [!IMPORTANT]
    > - Av sikkerhetsmessige årsaker må URL-adressen bruke HTTPS (Hypertext Transfer Protocol Secure).
    > - Appen eller webområdet må konfigureres slik at selve appen kan bygges inn.

6. Velg **Lagre** for å bygge inn appen på siden. Appen legges til som den siste kategorien eller delen i gruppen.
7. Bekreft at appen vises som forventet. Hvis appen ikke vises, kan du se delen [Feilsøking](#troubleshooting) senere i dette emnet.
8. Åpne visningsvelgeren, og velg enten **Lagre** (hvis appen skal knyttes til gjeldende visning) eller **Lagre som** (for å lagre appen i en annen visning).

    Hvis siden ikke har en visningsvelger (for eksempel hvis siden er en dialogboks eller et arbeidsområde), kan du hoppe over dette trinnet.

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a>Bygge inn et webområde som en helsideopplevelse fra instrumentbordet

Bruk denne fremgangsmåten hvis appen du vil bygge inn, ikke er relatert til en eksisterende side, eller hvis du bare vil ha en helsideopplevelse for appen i Finance and Operations-appen.

1. Åpne instrumentbordet.
2. Velg og hold på instrumentbodet (eller høyreklikk), velg **Tilpass**, og velg deretter **Legg til en side**.
3. I ruten **Legg til en side** klikker du **Nettsted**.
4. Konfigurer den innebygde appen:

    - **Navn** – Angi teksten som skal vises på brikken som er lagt til for den innebygde appen i instrumentbordet. Ofte vil du at denne teksten skal være navnet på appen.
    - **URL-adresse** – Angi plasseringen for appen.

    > [!IMPORTANT]
    > - Av sikkerhetsmessige årsaker må URL-adressen bruke HTTPS.
    > - Appen eller webområdet må konfigureres slik at selve appen kan bygges inn.

5. Velg **Lagre** for å legge til appen på instrumentbordet som en ny flis.
6. Velg den nye flisen på instrumentbordet, og bekreft at appen vises som forventet. Hvis appen ikke gjengis, kan du se delen [Feilsøking](#troubleshooting) senere i dette emnet.

## <a name="sharing-embedded-apps"></a>Dele innebygde apper

Når du har bygd inn en app ved hjelp av en av metodene som er beskrevet i de forrige delene, kan det hende at du vil dele visningen med andre brukere i systemet. Du kan dele en innebygd app på en av følgende måter:

- **Publiser visningen (anbefales):** Hvis den innebygde appen er lagret i en visning, er den anbefalte og foretrukne måten å dele den på å publisere visningen til brukere som har de riktige sikkerhetsrollene i de målrettede juridiske enhetene. I dette tilfellet vil bare de ønskede brukerne se den innebygde appen på den siden. Hvis du vil ha mer informasjon om hvordan du publiserer en visning, kan du se [Publisere visninger](saved-views.md#publishing-views).

    Du kan også publisere en app som er innebygd som en helsideopplevelse fra instrumentbordet. Velg og hold (eller høyreklikk) flisen som er tilknyttet appen, på instrumentbordet, velg **Tilpass**, og velg deretter **Publiser side**. En opplevelse som ligner på *publiseringsvisninger* vises, og du kan velge sikkerhetsrollene du vil publisere til. Hvis funksjonen **Forbedret støtte for juridiske enheter for lagrede visninger**, i oppdatering 10.0.21 eller senere, er aktivert, kan du også publisere appen til de ønskede juridiske enhetene.

- **Kopier tilpasningen:** For sider som ikke støtter visninger (for eksempel dialogbokser eller arbeidsområder), eller for helsideapperfaring, kan du kopiere tilpasningen til de aktuelle brukerne. Hvis du vil ha mer informasjon, kan du se [Dele tilpasninger](personalize-user-experience.md#sharing-personalizations).

## <a name="viewing-embedded-apps"></a>Vise innebygde apper

Hvis du vil vise en innebygd app på en side i Finance and Operations-apper, åpner du siden med den innebygde appen. Husk at innebygde apper på noen sider kan åpnes ved hjelp av **Power Apps**-knappen i standardhandlingsruten. De kan også vises direkte på siden som en ny fane, hurtigfane eller et blad eller som en ny inndeling i et arbeidsområde.

## <a name="editing-or-removing-embedded-apps"></a>Redigere eller fjerne innebygde apper

Når en app er innebygd på en side, kan det hende at du må redigere konfigurasjonen (for eksempel ved å endre deletiketten eller URL-adressen). Det kan også hende at du må fjerne den fra siden. Bruk en av fremgangsmåtene nedenfor for å redigere konfigurasjonen av en innebygd app eller fjerne den helt.

### <a name="apps-that-are-embedded-on-existing-pages"></a>Apper som er innebygd på eksisterende sider

1. Åpne siden der appen er innebygd.
2. Velg **Innstillinger** og deretter **Tilpass** for å åpne **Tilpassing**-verktøylinjen.
3. Velg **Valg**-verktøyet, og velg deretter den innebygde appen.
4. Hvis du vil redigere appen, gjør du de nødvendige endringene i konfigurasjonen og velger deretter **Lagre**.

    Du kan også fjerne appen ved å velge **Slett**.

5. Lagre eller publisere visningen på nytt. Vær oppmerksom på at hvis du går ut av siden uten å lagre visningen eksplisitt, blir ingen av handlingene du utførte i **Rediger nettsted**-ruten, opprettholdt.

### <a name="apps-that-are-embedded-from-the-dashboard"></a>Apper som er innebygd fra instrumentbordet

1. Åpne instrumentbordet.
2. Velg og hold (eller høyreklikk) flisen som er tilknyttet den innebygde appen, velg deretter **Tilpass**.
3. Hvis du vil redigere appen, velger du **Rediger side**. I ruten **Rediger nettsted** gjør du de nødvendige endringene i appkonfigurasjonen og velger deretter **Lagre**.

    Du kan også fjerne appen ved å velge **Fjern side**.

## <a name="appendix"></a>Tillegg

### <a name="troubleshooting"></a>Feilsøking

Hvis et nettsted ikke blir gjengitt riktig etter at den er innebygd i en Finance and Operations-app, eller hvis du får en feilmelding som angir at URLen ble nektet en tilkobling, konfigureres webområdet sannsynligvis for å hindre at det ikke blir innebygd i en iframe. Følg denne fremgangsmåten for å finne ut om webområdet kan bygges inn.

1. Åpne utviklerverktøyene for webleseren du bruker.
2. Finn og velg svar fra det innebygde området i fanen **Nettverk**.
3. Se etter **alternativer for x-frame** i fanen **Svarhoder** i kategorien **Hoder**. Hvis **alternativer for x-frame** finnes i svarhodene og har verdien **DENY** eller **SAMEORIGIN**, kan webområdet ikke bygges inn på riktig måte. Du må samarbeide med eieren av appen for å gjøre det mulig å bygge den inn på en trygg måte.

### <a name="developer-modeling-a-website-on-a-form"></a>[Utvikler] Modellere et webområde på et skjema

Selv om dette emnet har fokus på å bygge inn tredjepartsapper eller webområder gjennom tilpasning, kan utviklerne også bygge dem inn i et skjema ved hjelp av Visual Studio-utviklingserfaringen. Du kan bare legge til en **WebsiteHostControl**-kontroll i skjemaet. Metadataegenskapene som er tilgjengelige for kontrollen, har de samme egenskapene som tilpasningserfaringen.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
