---
title: Retningslinjer for distribusjon for kassaapparater for Norge
description: Dette emnet gir veiledning om hvordan du aktiverer kassefunksjonaliteten for Microsoft Dynamics 365 Commerce-lokalisering for Norge.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: c7e64dbfe6a300c097b5b3711ac4310f3386df11
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944746"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>Retningslinjer for distribusjon for kassaapparater for Norge

[!include[banner](../includes/banner.md)]

Dette emnet gir veiledning om hvordan du aktiverer kassefunksjonaliteten for Microsoft Dynamics 365 Commerce-lokalisering for Norge. Lokaliseringen består av flere utvidelser av komponenter. Ved hjelp av disse tilleggene kan du utføre handlinger, for eksempel skrive ut egendefinerte felter på kvitteringer, registrere flere revisjonshendelser, salgstransaksjoner og betalingstransaksjoner i salgsstedet, signere salgstransaksjoner digitalt og skrive ut rapporter i lokale formater. Hvis du vil ha mer informasjon om lokalisering for Norge, kan du se [Kassefunksjon for Norge](./emea-nor-cash-registers.md). Hvis du vil ha mer informasjon om hvordan du konfigurerer Commerce for Norge, kan du se [Definer Commerce for Norge](./emea-nor-cash-registers.md#setting-up-commerce-for-norway).

> [!WARNING]
> På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for denne lokaliseringsfunksjonaliteten. Du må bruke versjonen av det digitale signeringseksemplet for Norge i den forrige versjonen av Retail Software Development Kit (SDK) på en virtuell utviklermaskin (VM) i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for kasser for Norge (eldre)](./emea-nor-loc-deployment-guidelines.md).
>
> Støtte for den nye uavhengige emballasje- og utvidelsesmodellen for regnskapsintegreringseksempler planlegges for senere versjoner.

## <a name="set-up-fiscal-registration-for-norway"></a>Definere regnskapsregistrering for Norge

Eksemplet på regnskapsregistrering for Norge er basert på [regnskapsintegreringsfunksjonaliteten](fiscal-integration-for-retail-channel.md) og er en del av Retail SDK. Eksemplet finnes i **src\\FiscalIntegration\\SequentialSignatureNorway**-mappen i repositoriet for [løsningen for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (for eksempel [eksemplet i release/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34/src/FiscalIntegration/SequentialSignatureNorway)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) av en regnskapsdokumentleverandør og en regnskapskobling, som er utvidelser av Commerce Runtime (CRT). Hvis du vil ha mer informasjon om hvordan du bruker Retail SDK, kan du se [Retail SDK-arkitektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en kompileringskontroll for uavhengig emballasje-SDK](../dev-itpro/build-pipeline.md).

Fullfør fremgangsmåten for registreringsoppsett slik det beskrives i [Oppsett av regnskapsintegrering for Commerce-kanaler](./setting-up-fiscal-integration-for-retail-channel.md):

1. [Definere en regnskapsregistreringsprosess](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Pass på at du noterer deg innstillingene for regnskapsregistreringsprosessen som er [spesifikke for Norge](#configure-the-fiscal-registration-process).
1. [Angi innstillinger for feilbehandling](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Aktiver manuell kjøring av utsatt bilagsregistrering](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurer kanalkomponenter](#configure-channel-components).

### <a name="configure-the-fiscal-registration-process"></a>Konfigurer regnskapsregistreringsprosessen

Følg denne fremgangsmåten for å aktivere regnskapsregistreringsprosessen for Norge i Commerce Headquarters.

1. Last ned konfigurasjonsfiler for regnskapsdokumentleverandøren og regnskapskoblingen fra Commerce SDK:

    1. Open respositoriet for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Åpne den siste tilgjengelige frigivelsesavdelingen (for eksempel **[release/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34)**).
    1. Åpne **src \> FiscalIntegration \> SequentialSignatureNorway \> CommerceRuntime**.
    1. Last ned konfigurasjonsfilen for regnskapsdokumentleverandør under **DocumentProvider.SequentialSignNorway \> Configuration \> DocumentProviderSequentialSignatureNorwaySample.xml** (for eksempel [filen for release/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/DocumentProvider.SequentialSignNorway/Configuration/DocumentProviderSequentialSignatureNorwaySample.xml)).
    1. Last ned konfigurasjonsfilen for regnskapskoblingen under **Connector.SequentialSignNorway \> Configuration \> ConnectorSequentialSignatureNorwaySample.xml** (for eksempel [filen for release/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/Connector.SequentialSignNorway/Configuration/ConnectorSequentialSignatureNorwaySample.xml)).

1. Gå til **Retail og Commerce \> Hovedkvarteroppsett \> Parametere \> Delte parametere**. På **Generelt**-fanen angir du **Aktiver regnskapsintegrering**-alternativet til **Ja**.
1. Gå til **Retail og Commerce \> Kanaloppsett \> Regnskapsintegrering \> Regnskapskoblinger**, og last inn konfigurasjonsfilen for regnskapskobling som du lastet ned tidligere.
1. Gå til **Retail og Commerce \> Kanaloppsett \> Regnskapsintegrering \> Leverandører for regnskapsdokument**, og last inn konfigurasjonsfil for regnskapsdokumentleverandør som du lastet ned tidligere.
1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Regnskapsintegrering \> Funksjonsprofiler for kobling**. Opprett en ny funksjonsprofil for kobling, og velg dokumentleverandøren og koblingen du lastet inn tidligere.
1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Regnskapsintegrering \> Tekniske profiler for kobling**. Opprett en ny teknisk profil for kobling, og velg koblingen du lastet inn tidligere. Sett koblingstypen til **Intern**.
1. Gå til **Retail og Commerce \> Kanaloppsett \> Regnskapsintegrering \> Grupper for regnskapskobling**, og opprett en ny gruppe for regnskapskobling for funksjonsprofilen for koblingen som du opprettet tidligere.
1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Regnskapsintegrering \> Regnskapsregistreringsprosesser**. Opprett en ny regnskapsregistreringsprosess og et trinn i regnskapsregistreringsprosessen, og velg regnskapskoblingsgruppen du opprettet tidligere.
1. Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Funksjonalitetsprofiler**. Velg en funksjonsprofil som er koblet til butikken der registreringsprosessen skal aktiveres. I hurtigfanen **Regnskapsregistreringsprosess** velger du regnskapsregistreringsprosessen du opprettet tidligere. I hurtigganen **Regnskapstjenester** velger du den tekniske profilen for koblingen som du opprettet tidligere. 
1. Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**. Åpne distribusjonsplanen, og velg jobbene **1070** og **1090** for å overføre data til kanaldatabasen.

### <a name="configure-the-digital-signature-parameters"></a>Konfigurer parametere for digital signatur

Du må konfigurere sertifikater som skal brukes ved digital signering av salgstransaksjoner i en butikk. Et digitalt sertifikat som er lagret i Azure Key Vault, brukes til å signere. Når det gjelder frakoblet modus i Modern POS, kan signeringen også utføres ved hjelp av et digitalt sertifikat som er lagret i den lokale lagringen av maskinen som Modern POS er installert på.

Før du kan bruke et digitalt sertifikat som er lagret i Key Vault-lagring, må følgende trinn være fullført.

1. Key Vault-lagring må være opprettet. Vi anbefaler at du distribuerer lagringen i det samme geografiske området som Commerce Scale Unit.
1. Sertifikatet må lastes opp til Key Vault-lagringen som en base64-strenghemmelighet.
1. AOS-applikasjonen (Application Object Server) må ha tillatelse til å lese hemmeligheter fra Key Vault-lagringen.

Hvis du vil ha mer informasjon om hvordan du arbeider med Key Vault, kan du se [Kom i gang med Azure Key Vault](/azure/key-vault/key-vault-get-started).

Deretter angir du parameterne for tilgang til Key Vault-lagringen på siden **Key Vault-parametere**:

- **Navn** og **Beskrivelse** – Navnet på og beskrivelsen av Key Vault-lagringen.
- **URL-adresse for Key Vault** – URL-adressen til Key Vault-lagringen.
- **Key Vault-klient** – En interaktiv klient-ID til Azure Active Directory-programmet (Azure AD) som er tilknyttet Key Vault-lagringen for godkjenningsformål. Denne klienten bør ha tilgang til å lese hemmeligheter fra lagringen.
- **Hemmelig nøkkel for Key Vault** – En hemmelig nøkkel tilknyttet Azure AD-programmet som brukes til godkjenning i Key Vault-lagringen.
- **Navn**, **Beskrivelse** og **Hemmelig referanse** – Navnet, beskrivelsen og hemmelig referanse til sertifikatet.

Deretter må du konfigurere en kobling for sertifikatene som er lagret i Key Vault eller i det lokale sertifikatet. Denne koblingen brukes ved signering på kanalsiden.

1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Regnskapsintegrering \> Tekniske profiler for kobling**.
1. Angi følgende parametere for digitale signaturer i hurtigfanen **Innstillinger**:

    - **Hemmelig navn** – Velg det hemmelige navnet som du konfigurerte tidligere på siden **Key Vault-parametere**.
    - **Lokalt sertifikatavtrykk** – Angi et avtrykk for et sertifikat som er lagret lokalt.
    - **Hash-algoritme** – Angi en av de kryptografiske nummeralgoritmene som støttes av Microsoft .NET, for eksempel **SHA1**.
    - **Navn på sertifikatbutikk** – Dette feltet er valgfritt. Bruk det til å angi et standard butikknavn som skal brukes til å søke i lokale sertifikater.
    - **Plassering av sertifikatbutikk** – Dette feltet er valgfritt. Bruk det til å angi et standard butikkplassering som skal brukes til å søke i lokale sertifikater.
    - **Prøv lokalt sertifikat først** – Velg dette alternativet for å bruke sertifikatet fra den lokale butikken som standard ved signering av data, i stedet for sertifikatet fra Key Vault.
    - **Aktiver tilstandskontroll** – Hvis du vil ha mer informasjon om tilstandskontrollprosedyren, kan du se [Tilstandskontroll for regnskapsregistrering](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

> [!NOTE]
> - Bare den kryptografiske nummeralgoritmen for **SHA1** er i øyeblikket akseptabel for Norge.
> - Standard butikknavn og butikkplassering blir lagt til for å forenkle prosessen med å søke i lokale sertifikater i CRT. X509StoreProvider har en liste over mapper der sertifikater er lagret. Hvis standard butikknavn og standard butikkplassering ikke er angitt, prøver X509StoreProvider å finne et sertifikat i alle mappene på listen.

### <a name="configure-channel-components"></a>Konfigurere kanalkomponenter

### <a name="development-environment"></a>Utviklingsmiljø

Følg denne fremgangsmåten for å definere et distribusjonsmiljø slik at du kan teste og utvide eksemplet.

1. Klon eller last ned repositoriet for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions). Velg riktig frigivelsesavdelingsversjon i henhold til SDK/programversjonen. Hvis du vil ha mer informasjon, kan du se [Last ned eksempler og referansepakker i SDK for Retail fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Åpne løsningen **SequentialSignatureNorway.sln** under **Dynamics365Commerce.Solutions\\FiscalIntegration\\SequentialSignatureNorway**, og bygg den.
1. Installer CRT-utvidelser:

    1. Finn installasjonsprogrammet for CRT-utvidelsen:

        - **Commerce Scale Unit:** I mappen **SequentialSignatureNorway\\ScaleUnit\\ScaleUnit.SequentialSignNorway.Installer\\bin\\Debug\\net461** finner du installasjonsprogrammet **ScaleUnit.SequentialSignNorway.Installer**.
        - **Lokal CRT på Modern POS:** I mappen **SequentialSignatureNorway\\ModernPOS\\ModernPos.SequentialSignNorway.Installer\\bin\\Debug\\net461** finner du installasjonsprogrammet **ModernPos.SequentialSignNorway.Installer**.

    1. Start installeringsprogrammet for CRT-utvidelsen fra kommandolinjen:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **Lokal CRT på Modern POS:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

### <a name="production-environment"></a>Produksjonsmiljø

Følg fremgangsmåten i [Konfigurer en kompileringskontroll for et regnskapsintegreringseksempel](fiscal-integration-sample-build-pipeline.md) for å generere og frigi skyskalaenheten og selvbetjeningsdistribusjonspakker for eksemplet på regnskapsintegrering. Du finner YAML-filen for **SequentialSignatureNorway build-pipeline.yaml**-malen i **Pipeline\\YAML_Files** i repositoriet for [løsningene for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions).

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Aktiver den digitale signaturen i frakoblet modus for Modern POS

Hvis du vil aktivere den digitale signaturen i frakoblet modus for Modern POS, må du følge disse trinnene etter at du har aktivert Modern POS på en ny enhet.

1. Logg på POS.
1. På siden **Status for databasetilkobling** må du kontrollere at den frakoblede databasen er fullstendig synkronisert. Når verdien i feltet **Ventende nedlastinger** er **0** (null), synkroniseres databasen fullstendig.
1. Logg av salgsstedet.
1. Vent til den frakoblede databasen er fullstendig synkronisert.
1. Logg på POS.
1. På siden **Status for databasetilkobling** må du kontrollere at den frakoblede databasen er fullstendig synkronisert. Når verdien i feltet **Ventende transaksjoner i frakoblet database** er **0** (null), synkroniseres databasen fullstendig.
1. Åpne Modern POS på nytt.
