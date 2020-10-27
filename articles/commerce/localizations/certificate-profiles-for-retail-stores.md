---
title: Brukerdefinerte sertifikatprofiler for detaljhandelsbutikker
description: Dette emnet gir en oversikt over hvordan sertifikater brukes i detaljhandelsbutikker.
author: josaw
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0b8bf49a8eb78d0557ef105b40dd4cb5f0d24ce4
ms.sourcegitcommit: 83ec80382bfeb693d5c5949b6f65296bd50eed12
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973939"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Brukerdefinerte sertifikatprofiler for detaljhandelsbutikker

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

## <a name="overview"></a>Oversikt

Dette emnet gir en oversikt over sertifikatprofilene som er tilgjengelige i Microsoft Dynamics 365 Commerce. Denne funksjonaliteten utvider funksjonen [Behandle hemmeligheter for detaljhandelskanaler](../dev-itpro/manage-secrets.md) ved å legge til støtte for lokale sertifikater.

Når salgsstedet (POS) kjører i frakoblet modus, har det ikke tilgang til sertifikatene som er lagret i Key Vault. Det lokale sertifikatet skal brukes i stedet. Følgende funksjoner støttes:

- Bruke lokale sertifikater i tilbakefallsscenarioer for Key Vault
- Bruke lokale sertifikater uten et Key Vault (for eksempel i en lokal installasjon)
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

Fremgangsmåten nedenfor forklarer hvordan du konfigurerer sertifikatprofiler. Før du bruker sertifikat profiler i Commerce-kanalene, følger du denne Fremgangsmåten for å konfigurere innstillingene.

1. I arbeidsområdet **Funksjonsbehandling** slår du på funksjonen **Brukerdefinerte sertifikatprofiler for detaljhandelsbutikker** .
2. Gå til **Systemadministrasjon \> Oppsett \> Sertifikatprofiler** .
3. Opprett en post, og fyll ut feltene for **Sertifikatprofil** , **Navn** og **Beskrivelse** for den.

    > [!NOTE]
    > Sertifikatprofilen er en unik identifikator for et sertifikat på tvers av alle firmaer og Commerce-komponenter.

3. I kategorien **Juridiske enheter** legger du til en linje i den juridiske enheter (selskapet) som gjeldende sertifikatprofil skal brukes for. Hvis sertifikatprofilen skal brukes for flere juridiske enheter, gjentar du dette trinnet for å legge til en linje for hver juridiske enhet.
4. Velg **Innstillinger** for å åpne siden **Innstillinger for sertifikatprofil** , der du kan angi firmaspesifikke innstillinger for sertifikatprofilen.

### <a name="certificate-profile-settings"></a>Sertifikatprofilinnstillinger

Når du velger **Innstillinger** for sertifikatprofillinjer, vises siden **Innstillinger for sertifikat profil** . På denne siden kan du angi hvilke sertifikater som kan brukes når gjeldende sertifikatprofil kalles i Commerce-kanalene. Du kan også angi søkerekkefølgen for sertifikater.

> [!NOTE]
> **Prioritet** -feltet angis automatisk. Verdien **1** representerer den høyeste prioriteten. Når en ny linje legges til på siden **Innstillinger for sertifikatprofil** , blir prioriteten satt til et tall som er én mer enn prioriteten til den forrige linjen. Hvis du vil endre prioriteten for en bestemt linje, velger du linjen og deretter enten **Flytt opp** for å øke prioriteten eller **Flytt ned** for å redusere prioriteten.

Når du legger til en ny linje på siden **Innstillinger for sertifikatprofil** , angir du følgende felt:

- **Plasseringstype** – Velg plasseringen der sertifikatet skal lagres. Dette feltet har to mulige verdier: **lokalt sertifikat** og **Key Vault** .
- **Key Vault-sertifikat** – Dette feltet er obligatorisk hvis du setter feltet **Plasseringstype** til **Key Vault** . Bruk det til å angi en sertifikathemmelighet for Key Vault.

    > [!NOTE]
    > Før du bruker et Key Vault-sertifikat i sertifikatprofiler, må du laste opp et sertifikat til lagringsplassen for Key Vault og følge instruksjonene i [Konfigurere Azure Key Vault-klient](https://docs.microsoft.com/dynamics365/finance/localizations/setting-up-azure-key-vault-client).

- **Butikknavn** – Dette feltet er valgfritt, og er bare tilgjengelig hvis du setter **Plasseringstype** -feltet til **Lokalt sertifikat** . Bruk det til å angi et standard butikknavn som skal brukes til å søke i lokale sertifikater.
- **Butikkplassering** – Dette feltet er valgfritt, og er bare tilgjengelig hvis du setter **Plasseringstype** -feltet til **Lokalt sertifikat** . Bruk det til å angi et standard butikkplassering som skal brukes til å søke i lokale sertifikater.

    > [!NOTE]
    > Standard butikknavn og butikkplassering blir lagt til for å forenkle prosessen med å søke i lokale sertifikater i Commerce Runtime. X509StoreProvider har en liste over mapper der sertifikater er lagret. Hvis standard butikknavn og standard butikkplassering ikke er angitt, prøver X509StoreProvider å finne et sertifikat i de andre mappene på listen.

- **Avtrykk** – Dette feltet er obligatorisk, og er bare tilgjengelig hvis du setter **Plasseringstype** -feltet til **Lokalt sertifikat** . Bruk det til å angi sertifikatavtrykk.
- **Kommentarer** – Dette feltet er valgfritt, og lar brukere angi merknader.

### <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Arbeidsflyt: Søke etter sertifikater i Commerce Runtime

Her er den grunnleggende arbeidsflyten som brukes til å søke etter et sertifikat når en sertifikatprofil kalles i Commerce Runtime.

1. Systemet identifiserer om sertifikatprofilen har firmaspesifikke innstillinger for gjeldende juridiske enhet.
1. Systemet prøver å finne sertifikatet ved hjelp av verdiene på siden **Innstillinger for sertifikatprofil** for linjen der **Prioritet** -feltet er satt til **1** .

    - Hvis **Plasseringstype** -feltet er satt til **Key Vault** , brukes verdien til **Sertifikathemmelighet for Key Vault** til å søke etter sertifikatet på siden **Parametere for Key Vault** . Det søkes deretter etter sertifikatet på lagringsplassen for Key Vault.
    - Hvis **Plasseringstype** -feltet er satt til **Lokalt sertifikat** , må X509StoreProvider først søke etter sertifikatet ved hjelp av standard butikknavn og butikkplassering hvis disse parameterne er angitt. Deretter søkes det i alle andre mapper i listen over mapper.

1. Hvis sertifikatet ikke blir funnet, gjentas prosessen for linjen der **Prioritet** -feltet er satt til **2** og så videre.

> [!NOTE]
> Hvis sertifikatprofilen ikke har innstillinger for gjeldende juridiske enhet, eller hvis sertifikatsøket ikke lykkes for alle linjer på siden **Innstillinger for sertifikatprofil** , blir ikke sertifikatet funnet.

#### <a name="caching-the-results-of-certificate-searches"></a>Hurtigbufre resultatene av sertifikatsøk

Resultatene av sertifikatsøk blir hurtigbufret. Standard utløpstid for en buffer er én time. Denne tidsperioden kan imidlertid tilpasses og kan settes til en maksimumsverdi på 24 timer.

### <a name="gradual-update"></a>Gradvis oppdatering

Hvis en ny versjon av sertifikatet introduseres, men det ikke kan oppdateres i alle butikker samtidig, gjør funksjonaliteten for sertifikatprofiler det mulig å oppdatere sertifikatet gradvis.

1. Finn en sertifikatprofil og linjen som skal oppdateres, og velg deretter **Innstillinger** .
1. Legg til en linje, og angi innstillinger som er knyttet til den nyeste versjonen av sertifikatet.
1. Øk **Prioritet** -verdien for den nye linjen. Bruk **Flytt opp** -knappen til å flytte linjen, slik at den er over linjen for den forrige versjonen av det samme sertifikatet.

> [!NOTE]
> I Commerce Runtime kalles den nye versjonen av sertifikatet først. Hvis sertifikatet ennå ikke er oppdatert i en bestemt butikk eller på en bestemt terminal, vil den tidligere versjonen bli kalt.
