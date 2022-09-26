---
title: Brukerdefinerte sertifikatprofiler for detaljhandelsbutikker
description: Denne artikkelen gir en oversikt over sertifikatprofilene som er tilgjengelige i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: v-chgriffin
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.search.industry: Retail
ms.search.form: RetailFormLayout, RetailParameters
ms.openlocfilehash: 5baf043a43210d819b605546089e981c86922ca9
ms.sourcegitcommit: 4f28f262cfb8f047cb5c0070261aa0748835e74b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/21/2022
ms.locfileid: "9558444"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Brukerdefinerte sertifikatprofiler for detaljhandelsbutikker

[!include [banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over sertifikatprofilene som er tilgjengelige i Microsoft Dynamics 365 Commerce. Denne funksjonaliteten utvider funksjonen [Behandle hemmeligheter for detaljhandelskanaler](../dev-itpro/manage-secrets.md) ved å legge til støtte for lokale sertifikater.

Når salgsstedet (POS) kjører i frakoblet modus, har det ikke tilgang til sertifikatene som er lagret i Microsoft Azure Key Vault. Det lokale sertifikatet skal brukes i stedet. Følgende funksjoner støttes:

- Bruke lokale sertifikater i tilbakefallsscenarioer for Key Vault
- Bruke lokale sertifikater uten Key Vault (for eksempel i en lokal installasjon)
- Gradvis oppdatering av sertifikater, der noen butikker og terminaler bruker en ny versjon av sertifikatet, men andre butikker og terminaler fortsatt bruker den forrige versjonen

Ved hjelp av funksjonen for sertifikatprofiler kan du angi et standardsertifikat og angi søkerekkefølgen for sertifikater i samme sertifikatprofil. Denne funksjonaliteten gir også lignende tilnærming for oppsett for lokale sertifikater og Key Vault-sertifikater. Du kan legge til firmaspesifikke innstillinger for sertifikater, men den unike ID-en på tvers av firmaer for hvert sertifikat kan brukes i Commerce-kanalene.

### <a name="scenarios"></a>Scenarier

Funksjonen for sertifikatprofiler støtter følgende scenarier i Commerce-kanaler:

- Bruke lokale sertifikater i tilbakefallsscenarioer for Key Vault. Her er noen eksempler på disse tilbakefallsscenarioene:

    - Lagringsplassen for Key Vault er ikke tilgjengelig.
    - Du finner ikke et sertifikat i lagringsplassen for Key Vault.
    - POS kjører i frakoblet modus.

- Bruke lokale sertifikater, men uten å lagre dem i Key Vault (for eksempel i en lokal installasjon).
- Utfør en gradvis oppdatering av sertifikater, der en ny versjon av sertifikatet bare brukes i butikker eller på terminaler der den nye versjonen allerede er tilgjengelig.
- Bruk samme sertifikat i flere firmaer.

## <a name="set-up-certificate-profiles"></a>Konfigurere sertifikatprofiler

Fremgangsmåten nedenfor forklarer hvordan du konfigurerer sertifikatprofiler.

### <a name="set-up-key-vault"></a>Konfigurer Key Vault

Følgende trinn må være fullført før du kan bruke et digitalt sertifikat som er lagret i Key Vault.

1. Opprett en Azure-lagringskonto. Vi anbefaler at du distribuerer lagringskontoen i det samme geografiske området som Commerce Scale Unit.
1. Last opp det digitale sertifikatet til Key Vault-lagringskontoen.
1. Autoriser AOS-applikasjonen (Application Object Server) til å lese hemmeligheter fra Key Vault-lagringskontoen.

Hvis du vil ha mer informasjon om hvordan du arbeider med Key Vault, kan du se [Kom i gang med Azure Key Vault](/azure/key-vault/key-vault-get-started).

### <a name="set-up-system-parameters"></a>Definer systemparametere

Før du kan konfigurere sertifikatprofiler i Commerce-kanalene, må du aktivere Commerce til å bruke både sertifikater som er lagret i Key Vault, og sertifikatprofiler.

Følg denne fremgangsmåten for å definere systemparametre i Commerce headquarters.

1. På siden **Systemparametere** setter du alternativet **Bruk Avansert sertifikatlager** til **Ja**.
1. I arbeidsområdet **Funksjonsbehandling** slår du på funksjonen **Brukerdefinerte sertifikatprofiler for detaljhandelsbutikker**.

### <a name="set-up-key-vault-parameters"></a>Konfigurer Key Vault-parametere

Angi følgende parametere for tilgang til Key Vault-lagringen på siden **Key Vault-parametere**:

- **Navn** og **Beskrivelse** – Navnet på og beskrivelsen av Key Vault-lagringskontoen.
- **URL-adresse for Key Vault** – URL-adressen til Key Vault-lagringskontoen.
- **Key Vault-klient** – En interaktiv klient-ID til Azure Active Directory-programmet (Azure AD) som er tilknyttet Key Vault-lagringskontoen for godkjenningsformål. Denne klienten bør ha tilgang til å lese hemmeligheter fra lagringskontoen.
- **Hemmelig nøkkel for Key Vault** – En hemmelig nøkkel tilknyttet Azure AD-programmet som brukes til godkjenning i Key Vault-lagringskontoen.
- **Navn**, **Beskrivelse** og **Hemmelig referanse** – Navnet, beskrivelsen og hemmelig referanse til sertifikatet.

Hvis du vil ha mer informasjon, se [Konfigurere Azure Key Vault-klienten](../../finance/localizations/setting-up-azure-key-vault-client.md).

### <a name="configure-a-certificate-profile"></a>Konfigurer en sertifikatprofil

Følg denne fremgangsmåten for å konfigurere en sertifikatprofil i Commerce headquarters.

1. Gå til **Systemadministrasjon \> Oppsett \> Sertifikatprofiler**.
1. I handlingsruten velger du **Ny** for å opprette en post.
1. Angi verdier i feltene **Sertifikatprofil**, **Navn** og **Beskrivelse**.

    > [!NOTE]
    > Sertifikatprofilen er en unik identifikator for et sertifikat på tvers av alle firmaer og Commerce-komponenter.

1. På hurtigfanen **Juridiske enheter** velger du **Legg til** for å legge til en linje.
1. Under **Juridisk enhet** velger du den juridiske enheten (selskapet) som gjeldende sertifikatprofil skal brukes for.

    Hvis sertifikatprofilen skal brukes for flere juridiske enheter, gjentar du trinn 4 og 5 for å legge til en linje for hver juridiske enhet.

1. Velg **Innstillinger** for å åpne siden **Innstillinger for sertifikatprofil**, der du kan angi firmaspesifikke innstillinger for sertifikatprofilen. Angi hvilke sertifikater som kan brukes når gjeldende sertifikatprofil kalles i Commerce-kanalene. Legg til så mange sertifikater du trenger, og angi prioritet for dem. Hvis det ikke finnes et sertifikat som har høyere prioritet, brukes det neste sertifikatet basert på prioritet. Hvis du vil ha mer informasjon, kan du se delen [Arbeidsflyt: Søke etter sertifikater i Commerce Runtime](#workflow-searching-certificates-in-the-commerce-runtime).

    > [!NOTE]
    > **Prioritet**-feltet angis automatisk. Verdien **1** representerer den høyeste prioriteten. Når en ny linje legges til på siden **Innstillinger for sertifikatprofil**, blir prioriteten satt til et tall som er én mer enn prioriteten til den forrige linjen. Hvis du vil endre prioriteten for en bestemt linje, velger du linjen og deretter enten **Flytt opp** for å øke prioriteten eller **Flytt ned** for å redusere prioriteten.

1. Når du legger til en ny linje på siden **Innstillinger for sertifikatprofil**, angir du følgende felter:

    - **Plasseringstype** – Velg plasseringen der sertifikatet skal lagres. Dette feltet har to mulige verdier: **lokalt sertifikat** og **Key Vault**.
    - **Key Vault-sertifikat** – Dette feltet er obligatorisk hvis du setter feltet **Plasseringstype** til **Key Vault**. Bruk det til å angi en sertifikathemmelighet for Key Vault.
    - **Butikknavn** – Dette feltet er valgfritt, og er bare tilgjengelig hvis du setter **Plasseringstype**-feltet til **Lokalt sertifikat**. Bruk det til å angi et standard butikknavn som skal brukes til å søke i lokale sertifikater.
    - **Butikkplassering** – Dette feltet er valgfritt, og er bare tilgjengelig hvis du setter **Plasseringstype**-feltet til **Lokalt sertifikat**. Bruk det til å angi et standard butikkplassering som skal brukes til å søke i lokale sertifikater.

        > [!NOTE]
        > Standard butikknavn og butikkplassering blir lagt til for å forenkle prosessen med å søke i lokale sertifikater i Commerce Runtime. X509StoreProvider har en liste over mapper der sertifikater er lagret. Hvis standard butikknavn og standard butikkplassering ikke er angitt, prøver X509StoreProvider å finne et sertifikat i de andre mappene på listen. Hvis du vil ha mer informasjon om tilgjengelige verdier for butikknavnet og butikklokasjonen, kan du se [StoreName Enum](/dotnet/api/system.security.cryptography.x509certificates.storename) og [StoreLocation Enum](//dotnet/api/system.security.cryptography.x509certificates.storelocation).

    - **Avtrykk** – Dette feltet er obligatorisk, og er bare tilgjengelig hvis du setter **Plasseringstype**-feltet til **Lokalt sertifikat**. Bruk det til å angi sertifikatavtrykk.

        > [!IMPORTANT]
        > Du må sikre at brukeren som kjører appen som må bruke det lokale sertifikatet (for eksempel Modern POS i frakoblet modus), minst har skrivebeskyttet tilgang til den private nøkkelen for sertifikatet.

    - **Kommentarer** – Dette feltet er valgfritt, og lar brukere angi merknader.

## <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Arbeidsflyt: Søke etter sertifikater i Commerce Runtime

Her er den grunnleggende arbeidsflyten som brukes til å søke etter et sertifikat når en sertifikatprofil kalles i Commerce Runtime.

1. Systemet identifiserer om sertifikatprofilen har firmaspesifikke innstillinger for gjeldende juridiske enhet.
1. Systemet prøver å finne sertifikatet ved hjelp av verdiene på siden **Innstillinger for sertifikatprofil** for linjen der **Prioritet**-feltet er satt til **1**.

    - Hvis **Plasseringstype**-feltet er satt til **Key Vault**, brukes verdien til **Sertifikathemmelighet for Key Vault** til å søke etter sertifikatet på siden **Parametere for Key Vault**. Det søkes deretter etter sertifikatet på lagringsplassen for Key Vault.
    - Hvis **Plasseringstype**-feltet er satt til **Lokalt sertifikat**, må X509StoreProvider først søke etter sertifikatet ved hjelp av standard butikknavn og butikkplassering hvis disse parameterne er angitt. Deretter søkes det i alle andre mapper i listen over mapper.

1. Hvis sertifikatet ikke blir funnet, gjentas prosessen for linjen der **Prioritet**-feltet er satt til **2** og så videre.

> [!NOTE]
> Hvis sertifikatprofilen ikke har innstillinger for gjeldende juridiske enhet, eller hvis sertifikatsøket ikke lykkes for alle linjer på siden **Innstillinger for sertifikatprofil**, blir ikke sertifikatet funnet.

### <a name="caching-the-results-of-certificate-searches"></a>Hurtigbufre resultatene av sertifikatsøk

Resultatene av sertifikatsøk blir hurtigbufret. Standard utløpstid for en buffer er én time. Denne tidsperioden kan imidlertid tilpasses og kan settes til en maksimumsverdi på 24 timer.

## <a name="gradual-update"></a>Gradvis oppdatering

Hvis en ny versjon av sertifikatet introduseres, men det ikke kan oppdateres i alle butikker samtidig, gjør funksjonaliteten for sertifikatprofiler det mulig å oppdatere sertifikatet gradvis.

1. Finn en sertifikatprofil og linjen som skal oppdateres, og velg deretter **Innstillinger**.
1. Legg til en linje, og angi innstillinger som er knyttet til den nyeste versjonen av sertifikatet.
1. Øk **Prioritet**-verdien for den nye linjen. Bruk **Flytt opp**-knappen til å flytte linjen, slik at den er over linjen for den forrige versjonen av det samme sertifikatet.
> [!NOTE]
> I Commerce Runtime kalles den nye versjonen av sertifikatet først. Hvis sertifikatet ennå ikke er oppdatert i en bestemt butikk eller på en bestemt terminal, vil den tidligere versjonen bli kalt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
