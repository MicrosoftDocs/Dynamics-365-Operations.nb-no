---
title: Retningslinjer for distribusjon for kassaapparater for Norge (eldre)
description: Denne artikkelen er en distribusjonshåndbok som viser hvordan du aktiverer Microsoft Dynamics 365 Commerce-lokalisering for Norge.
author: EvgenyPopovMBS
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-2-28
ms.openlocfilehash: fb597add48ac3508a88142e63d80f405b6b5f8b4
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346052"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway-legacy"></a>Retningslinjer for distribusjon for kassaapparater for Norge (eldre)

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Dette eksemplet på regnskapsintegreringsfunksjon benytter seg ikke av [regnskapsintegreringsrammeverket](./fiscal-integration-for-retail-channel.md) og blir avskrevet i senere oppdateringer. Du bør i stedet bruke [funksjonaliteten som er basert på regnskapsintegreringsrammeverket](./emea-nor-fi-deployment.md).

Denne artikkelen er en distribusjonshåndbok som viser hvordan du aktiverer Microsoft Dynamics 365 Commerce-lokalisering for Norge. Lokaliseringen består av flere utvidelser av Commerce-komponenter. Ved hjelp av utvidelsene kan du for eksempel skrive ut egendefinerte felter på kvitteringer, registrere flere revisjonshendelser, salgstransaksjoner og betalingstransaksjoner i salgsstedet, digitalt signere salgstransaksjoner og skrive ut X- og Y-rapporter i lokale formater. Hvis du vil ha mer informasjon om lokalisering for Norge, kan du se [Kassefunksjon for Norge](./emea-nor-cash-registers.md).

Denne eksemplet er en del av Retail Software Development Kit (SDK). Hvis du vil ha informasjon om SDK, kan du se [Arkitektur for Retail Software Development Kit (SDK)](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Dette eksemplet består av utvidelser for Commerce Runtime (CRT), Retail Server og salgssted. Hvis du vil kjøre dette eksemplet, må du endre og bygge CRT, Retail Server og salgsstedsprosjektene. Vi anbefaler at du bruker en uendret Retail SDK til å foreta endringene som er beskrevet i denne artikkelen. Vi anbefaler også at du bruker et kildekontrollsystem for eksempel Microsoft Visual Studio Online (VSO) der ingen filer er endret ennå.

> [!NOTE]
> I Commerce 10.0.8 og nyere kalles Retail Server Commerce Scale Unit. Siden denne artikkelen gjelder for flere tidligere versjoner av appen, brukes *Retail Server* i hele artikkelen.
>
> Fremgangsmåtene i denne artikkelen er forskjellige, avhengig av hvilken versjon av Commerce du bruker. Hvis du vil ha mer informasjon, kan du se [Nyheter eller endringer i Dynamics 365 Retail](../get-started/whats-new.md).

### <a name="using-certificate-profiles-in-commerce-channels"></a>Bruke sertifikatprofiler i Commerce-kanaler

I Commerce-versjoner 10.0.15 og nyere kan du bruke funksjonene for de [brukerdefinerte sertifikatprofilene for detaljhandelsforretninger](./certificate-profiles-for-retail-stores.md) som støtter failover til frakoblet når Key Vault eller Commerce Headquarters ikke er tilgjengelig. Funksjonen utvider funksjonen [Administrer utvidelser for detaljhandelskanaler](../dev-itpro/manage-secrets.md).

Følg denne fremgangsmåten for å bruke denne funksjonaliteten i CRT-utvidelsen.

1. Opprette et nytt CRT-utvidelsesprosjekt (prosjekttype for C#-klassebibliotek). Bruk eksempelmalene fra Retail Software Development Kit (SDK) (RetailSDK\SampleExtensions\CommerceRuntime).

2. Legg til egendefinert behandler for CertificateSignatureServiceRequest i prosjektet SequentialSignatureRegister.

3. Hvis du vil lese en hemmelig samtale, `GetUserDefinedSecretCertificateServiceRequest` ved hjelp av en konstruktør med profileId-parameter. Det vil starte funksjonaliteten ved hjelp av innstillinger fra sertifikatprofiler. Sertifikatet hentes enten fra Azure Key Vault eller fra den lokale maskinlagringen, basert på innstillingene.

    ```csharp
    GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);
    GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);

    X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;
    ```

4. Når sertifikatet hentes, kan du fortsette med datasignering.

5. Bygg CRT-utvidelsesprosjektet.

6. Kopier utdataklassebiblioteket og lim det inn i ...\RetailServer\webroot\bin\Ext for manuell testing.

7. Oppdater informasjon om utvidelsessammensetning i CommerceRuntime.Ext.config-filen med informasjonen om egendefinerte biblioteker.

## <a name="development-environment"></a>Utviklingsmiljø

Fullfør denne fremgangsmåten for å definere et distribusjonsmiljø slik at du kan teste og utvide eksemplet.

### <a name="the-crt-extension-components"></a>CRT-utvidelseskomponentene

CRT-utvidelseskomponentene er inkludert i CRT-eksemplene. Du kan fullføre følgende fremgangsmåter ved å åpne CRT-løsningen **CommerceRuntimeSamples.sln** under **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="receiptsnorway-component"></a>ReceiptsNorway-komponent

1. Finn prosjektet **Runtime.Extensions.ReceiptsNorway**, og bygg det.
2. I mappen **Extensions.ReceiptsNorway\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.ReceiptsNorway.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under Microsoft Internet Information Services (IIS) Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

#### <a name="salespaymenttransext-component"></a>SalesPaymentTransExt-komponent

1. Finn prosjektet **Runtime.Extensions.SalesPaymentTransExt**, og bygg det.
2. I mappen **Extensions.SalesPaymentTransExt\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

#### <a name="xzreportsnorway-component"></a>XZReportsNorway-komponent

1. Finn prosjektet **Runtime.Extensions.XZReportsNorway**, og bygg det.
2. I mappen **Extensions.XZReportsNorway\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.XZReportsNorway.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

# <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent-eksempelkomponenten

1. Finn prosjektet **Runtime.Extensions.RegisterAuditEventSample**, og bygg det.
2. I mappen **Extensions.RegisterAuditEventSample\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature-eksempelkomponenten

1. Finn prosjektet **Runtime.Extensions.SalesTransactionSignatureSample**, og bygg det.
2. Endre **App.config**-filen ved å angi avtrykket, butikklokasjonen og butikknavnet for sertifikatet som skal brukes til å signere salgstransaksjoner.
3. Bygg prosjektet.
4. Finn følgende samlingsfiler i mappen **Extensions.SalesTransactionSignatureSample\\bin\\Debug**:

    - Samlingsfilen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - Konfigurasjonsfilen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. Kopier filene til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

6. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

7. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

# <a name="application-update-5-and-later"></a>[Appoppdatering 5 og senere](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent-eksempelkomponenten

1. Finn prosjektet **Runtime.Extensions.RegisterAuditEventSample**, og bygg det.
2. I mappen **Extensions.RegisterAuditEventSample\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature-eksempelkomponenten

1. Finn prosjektet **Runtime.Extensions.SalesTransactionSignatureSample**, og bygg det.
2. Endre **App.config**-filen ved å angi avtrykket, butikklokasjonen og butikknavnet for sertifikatet som skal brukes til å signere salgstransaksjoner.
3. Bygg prosjektet.
4. Finn følgende samlingsfiler i mappen **Extensions.SalesTransactionSignatureSample\\bin\\Debug**:

    - Samlingsfilen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - Konfigurasjonsfilen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. Kopier filene til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

6. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

7. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

#### <a name="salestransactionsignaturesamplemessages-component"></a>SalesTransactionSignatureSample.Messages-komponenten

1. Finn prosjektet **Runtime.Extensions.SalesTransactionSignatureSample.Messages**, og bygg det.
2. I mappen **Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

# <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent-eksempelkomponenten

1. Finn prosjektet **Runtime.Extensions.RegisterAuditEventSample**, og bygg det.
2. I mappen **Extensions.RegisterAuditEventSample\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature-eksempelkomponenten

1. Finn prosjektet **Runtime.Extensions.SalesTransactionSignatureSample**, og bygg det.
2. Endre **App.config**-filen ved å angi avtrykket, butikklokasjonen og butikknavnet for sertifikatet som skal brukes til å signere salgstransaksjoner.
3. Bygg prosjektet.
4. Finn følgende samlingsfiler i mappen **Extensions.SalesTransactionSignatureSample\\bin\\Debug**:

    - Samlingsfilen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - Konfigurasjonsfilen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. Kopier filene til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

6. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

7. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts-komponenten

1. Finn prosjektet **Runtime.Extensions.SequentialSignatureRegister.Contracts**, og bygg det.
2. I mappen **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

# <a name="retail-732-and-later"></a>[Retail 7.3.2 og senere](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent-eksempelkomponenten

1. Finn prosjektet **Runtime.Extensions.RegisterAuditEventSample**, og bygg det.
2. I mappen **Extensions.RegisterAuditEventSample\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister-komponenten

1. Finn prosjektet **Runtime.Extensions.SequentialSignatureRegister**, og bygg det.
2. Endre **App.config**-filen ved å angi avtrykket, butikklokasjonen og butikknavnet for sertifikatet som skal brukes til å signere salgstransaksjoner.
3. Bygg prosjektet.
4. Finn følgende samlingsfiler i mappen **Extensions.SequentialSignatureRegister\\bin\\Debug**:

    - Samlingsfilen **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - Konfigurasjonsfilen **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Kopier filene til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

6. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

7. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway-komponenten

1. Finn prosjektet **Runtime.Extensions.SalesTransactionSignatureNorway**, og bygg det.
2. I mappen **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts-komponenten

1. Finn prosjektet **Runtime.Extensions.SequentialSignatureRegister.Contracts**, og bygg det.
2. I mappen **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway-komponent

1. Finn prosjektet **Runtime.Extensions.SalesPaymentTransExtNorway**, og bygg det.
2. I mappen **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

# <a name="retail-735-and-later"></a>[Retail 7.3.5 og senere](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEventNorway-komponenten

1. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

2. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister-komponenten

1. Finn prosjektet **Runtime.Extensions.SequentialSignatureRegister**, og bygg det.
2. Endre **App.config**-filen ved å angi avtrykket, butikklokasjonen og butikknavnet for sertifikatet som skal brukes til å signere salgstransaksjoner.
3. Bygg prosjektet.
4. Finn følgende samlingsfiler i mappen **Extensions.SequentialSignatureRegister\\bin\\Debug**:

    - Samlingsfilen **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - Konfigurasjonsfilen **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Kopier filene til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

6. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

7. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway-komponenten

1. Finn prosjektet **Runtime.Extensions.SalesTransactionSignatureNorway**, og bygg det.
2. I mappen **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts-komponenten

1. Finn prosjektet **Runtime.Extensions.SequentialSignatureRegister.Contracts**, og bygg det.
2. I mappen **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway-komponent

1. Finn prosjektet **Runtime.Extensions.SalesPaymentTransExtNorway**, og bygg det.
2. I mappen **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

# <a name="retail-811-and-later"></a>[Retail 8.1.1 og senere](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEventNorway-komponenten

1. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

2. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister-komponenten

1. Finn prosjektet **Runtime.Extensions.SequentialSignatureRegister**, og bygg det.
2. Endre **App.config**-filen ved å angi avtrykket, butikklokasjonen og butikknavnet for sertifikatet som skal brukes til å signere salgstransaksjoner.
3. Bygg prosjektet.
4. Finn følgende samlingsfiler i mappen **Extensions.SequentialSignatureRegister\\bin\\Debug**:

    - Samlingsfilen **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - Konfigurasjonsfilen **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Kopier filene til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

6. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

7. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway-komponenten

1. Finn prosjektet **Runtime.Extensions.SalesTransactionSignatureNorway**, og bygg det.
2. I mappen **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts-komponenten

1. Finn prosjektet **Runtime.Extensions.SequentialSignatureRegister.Contracts**, og bygg det.
2. I mappen **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway-komponent

1. Finn prosjektet **Runtime.Extensions.SalesPaymentTransExtNorway**, og bygg det.
2. I mappen **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Retail Server:** Kopier samlingen til **\\bin\\ext**-mappen under IIS Retail Server-områdeplasseringen.
    - **Lokal CRT på Modern POS:** Kopier samlingen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Retail Server:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Retail Server-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > **Ikke** rediger filene commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

---

### <a name="the-retail-server-extension-components"></a>Retail Server-utvidelseskomponentene

#### <a name="salestransactionsignature-retail-server-sample-component"></a>SalesTransactionSignature Retail Server-eksempelkomponenten

1. I mappen **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** finner du prosjektet **RetailServer.Extensions.SalesTransactionSignatureSample** og bygger det.
2. I mappen **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** finner du samlingsfilen **Contoso.RetailServer.SalesTransactionSignatureSample.dll**.
3. Kopier samlingsfilen til Retail Server-utvidelsesmappen.

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    Mappen er **\\bin**-mappen under IIS Retail Server-området.

    # <a name="application-update-5-and-later"></a>[Appoppdatering 5 og senere](#tab/app-update-5-and-later)

    Mappen er **\\bin**-mappen under IIS Retail Server-området.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    Mappen er **\\bin\\ext**-mappen under IIS Retail Server-området.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og senere](#tab/retail-7-3-2)

    Mappen er **\\bin\\ext**-mappen under IIS Retail Server-området.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og senere](#tab/retail-7-3-5)

    Mappen er **\\bin\\ext**-mappen under IIS Retail Server-området.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og senere](#tab/retail-8-1-1)

    Mappen er **\\bin\\ext**-mappen under IIS Retail Server-området.

    ---

4. Finn konfigurasjonsfilen for Retail Server. Filen heter **web.config** og ligger i rotmappen under plasseringen av IIS Retail Server-området.
5. Registrer Retail Server-utvidelsene i **extensionComposition**-delen i konfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. Registrer avhengighetene til Retail Server-utvidelsene.

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4/)

    1. Finn følgende samlingsfiler i mappen **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**:

        - Samlingsfilen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
        - Konfigurasjonsfilen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

    2. Kopier filene til mappen **\\bin** under IIS Retail Server-området.
    3. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen for CRT. Denne filen heter **commerceruntime.ext.config**, og ligger i **bin**-mappen under plasseringen av IIS Retail Server-området.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-later"></a>[Appoppdatering 5 og senere](#tab/app-update-5-and-later/)

    1. I mappen **CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll**.
    2. Kopier filen til mappen **\\bin** under IIS Retail Server-området.
    3. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen for CRT. Denne filen heter **commerceruntime.ext.config**, og ligger i **bin**-mappen under plasseringen av IIS Retail Server-området.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Ingen handlinger kreves.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og senere](#tab/retail-7-3-2)

    > [!NOTE]
    > Ingen handlinger kreves.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og senere](#tab/retail-7-3-5)

    > [!NOTE]
    > Ingen handlinger kreves.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og senere](#tab/retail-8-1-1)

    > [!NOTE]
    > Ingen handlinger kreves.

    ---

### <a name="the-modern-pos-extension-components"></a>Modern POS-utvidelseskomponentene

#### <a name="implement-the-proxy-code-for-offline-mode"></a>Implementer proxy-koden for frakoblet modus

Denne delen tilsvarer Retail Server-kontrolleren, men utvider den lokale CRT som brukes når klienten ikke er tilkoblet.

1. I filen **customization.settings** file endrer du delen **@(RetailServerLibraryPathForProxyGeneration)** slik at den bruker den nye Retail Server-samlingen til proxy-generering.
2. Implementere følgende grensesnittmetoder i klassen **StoreOperationsManager**. For den første gjentakelsen legger du til følgende kode:

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="application-update-5-and-later"></a>[Appoppdatering 5 og senere](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Dette trinnet gjelder ikke for denne versjonen.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og senere](#tab/retail-7-3-2)

    > [!NOTE]
    > Dette trinnet gjelder ikke for denne versjonen.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og senere](#tab/retail-7-3-5)

    > [!NOTE]
    > Dette trinnet gjelder ikke for denne versjonen.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og senere](#tab/retail-8-1-1)

    > [!NOTE]
    > Dette trinnet gjelder ikke for denne versjonen.

    ---

3. Hvis du vil generere proxy-koden på nytt, bygger du **Proxyer**-mappen fra kommandolinjen ved å bruke kommandoen **msbuild /t:Rebuild**.
4. Løs prosjektavhengighetene for **Proxies.RetailProxy**:

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    Åpne **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, legg til prosjektet **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** i løsningen og legg til en prosjektreferanse i prosjektet **RetailProxy** for å henvise til **SalesTransactionSignatureSample**.

    # <a name="application-update-5-and-later"></a>[Appoppdatering 5 og senere](#tab/app-update-5-and-later)

    Åpne **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, legg til prosjektet **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** i løsningen og legg til en prosjektreferanse i prosjektet **RetailProxy** for å henvise til **SalesTransactionSignatureSample.Messages**.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Dette trinnet gjelder ikke for denne versjonen.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og senere](#tab/retail-7-3-2)

    > [!NOTE]
    > Dette trinnet gjelder ikke for denne versjonen.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og senere](#tab/retail-7-3-5)

    > [!NOTE]
    > Dette trinnet gjelder ikke for denne versjonen.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og senere](#tab/retail-8-1-1)

    > [!NOTE]
    > Dette trinnet gjelder ikke for denne versjonen.

    ---

5. Juster grensesnittmetodene i klassen **StoreOperationsManager**:

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="application-update-5-and-later"></a>[Appoppdatering 5 og senere](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Dette trinnet gjelder ikke for denne versjonen.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og senere](#tab/retail-7-3-2)

    > [!NOTE]
    > Dette trinnet gjelder ikke for denne versjonen.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og senere](#tab/retail-7-3-5)

    > [!NOTE]
    > Dette trinnet gjelder ikke for denne versjonen.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og senere](#tab/retail-8-1-1)

    > [!NOTE]
    > Dette trinnet gjelder ikke for denne versjonen.

    ---

6. Oppdater filen **dllhost.exe.config** slik at klientmeglingen laster inn den nye RetailProxy-samlingen.

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a>Utvidelseskomponent for Retail-proxy (Retail 7.3.1 og senere)

Fullfør følgende fremgangsmåte bare hvis du bruker Retail 7.3.1 og senere.

1. I mappen **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxyServer.Extensions.SalesTransactionSignatureSample** finner du prosjektet **RetailServer.Extensions.SalesTransactionSignatureSample** og bygger det.
2. I mappen **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample**.
3. Kopier samlingsfilene til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.
4. Registrer Retail-proxyendringen i utvidelseskonfigurasjonsfilen. Filen heter **RetailProxy.MPOSOffline.ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a>Modern POS-utvidelseskomponenter

1. Åpne løsningen under **RetailSdk\\POS\\ModernPOS.sln**, og kontroller at den kan kompileres uten feil. I tillegg må du passe på at du kan kjøre Modern POS fra Microsoft Visual Studio ved hjelp av kommandoen **Kjør**.

    > [!NOTE]
    > Modern POS må ikke tilpasses. Du må aktivere Brukerkontokontroll (UAC), og du må avinstallere tidligere installerte forekomster av Modern POS etter behov.

2. Inkluder følgende eksisterende kildekodemapper i **Pos.Extensions**-prosjektet.

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Appoppdatering 5 og senere](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og senere](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og senere](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og senere](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. Aktiver at utvidelsene skal kompileres i **tsconfig.json** ved å fjerne følgende mapper fra utelatelseslisten.

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Appoppdatering 5 og senere](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og senere](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og senere](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og senere](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. Aktiver utvidelsene som skal lastes inn i **extensions.json**, ved å legge til følgende linjer på riktig sted.

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Appoppdatering 5 og senere](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og senere](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og senere](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og senere](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Hvis du vil ha mer informasjon og eksempler som viser hvordan du inkluderer kildekodemapper og aktiverer tillegg som skal lastes, kan du se instruksjonene i filen readme.md i **Pos.Extensions**-prosjektet.

5. Bygg løsningen på nytt.
6. Kjør Modern POS i feilsøkingen, og test funksjonaliteten.

### <a name="cloud-pos-extension-components"></a>Utvidelseskomponenter for skybasert salgssted

1. Åpne løsningen under **RetailSdk\\POS\\CloudPOS.sln**, og kontroller at den kan kompileres uten feil.
2. Inkluder følgende eksisterende kildekodemapper i **Pos.Extensions**-prosjektet.

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Appoppdatering 5 og senere](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og senere](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og senere](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og senere](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. Aktiver at utvidelsene skal kompileres i **tsconfig.json** ved å fjerne følgende mapper fra utelatelseslisten.

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Appoppdatering 5 og senere](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og senere](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og senere](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og senere](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. Aktiver utvidelsene som skal lastes inn i **extensions.json**, ved å legge til følgende linjer på riktig sted.

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Appoppdatering 5 og senere](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og senere](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og senere](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og senere](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Hvis du vil ha mer informasjon og eksempler som viser hvordan du inkluderer kildekodemapper og aktiverer tillegg som skal lastes, kan du se instruksjonene i filen readme.md i **Pos.Extensions**-prosjektet.

5. Bygg løsningen på nytt.
6. Kjør løsningen ved å bruke kommandoen **Kjør**, og følg trinnene i Retail SDK-håndboken.
7. Test funksjonaliteten.

### <a name="set-up-required-parameters-in-headquarters"></a>Definer nødvendige parametere i Headquarters

Hvis du vil ha mer informasjon, se [Kassefunksjonalitet for Norge](./emea-nor-cash-registers.md).

## <a name="production-environment"></a>Produksjonsmiljø

Følg denne fremgangsmåten for å opprette distribuerbare pakker som inneholder Commerce-komponenter, og for å bruke disse pakkene i et produksjonsmiljø.

1. Fullfør fremgangsmåten i delen [Utvidelseskomponenter for skybasert salgssted](#cloud-pos-extension-components) eller [Moderne POS-utvidelseskomponenter](#modern-pos-extension-components) tidligere i denne artikkelen.
2. Gjør følgende endringer i konfigurasjonsfilene for pakker i mappen **RetailSdk\\Assets**:

    1. I konfigurasjonsfilene **commerceruntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** legger du til følgende linjer i **sammensetningsdelen**:

        # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-later"></a>[Appoppdatering 5 og senere](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 og senere](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 og senere](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 og senere](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. Aktiver proxy-tilpasning for Commerce:

        # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

        Legg til følgende linjer i delen **appSettings** under delen **configuration** i konfigurasjonsfilen **dllhost.exe.config**.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-later"></a>[Appoppdatering 5 og senere](#tab/app-update-5-and-later)

        Legg til følgende linjer i delen **appSettings** under delen **configuration** i konfigurasjonsfilen **dllhost.exe.config**.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        I konfigurasjonsfilen **RetailProxy.MPOSOffline.ext.config** legger du til følgende linjer i **sammensetningsdelen**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 og senere](#tab/retail-7-3-2)

        I konfigurasjonsfilen **RetailProxy.MPOSOffline.ext.config** legger du til følgende linjer i **sammensetningsdelen**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 og senere](#tab/retail-7-3-5)

        I konfigurasjonsfilen **RetailProxy.MPOSOffline.ext.config** legger du til følgende linjer i **sammensetningsdelen**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 og senere](#tab/retail-8-1-1)

        I konfigurasjonsfilen **RetailProxy.MPOSOffline.ext.config** legger du til følgende linjer i **sammensetningsdelen**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. Gjør følgende endringer i pakkekonfigurasjonsfilen **Customization.settings**:

    1. Aktiver proxy-tilpasning for Retail.

        # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

        Legg til følgende linjer i delen **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;**.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-later"></a>[Appoppdatering 5 og senere](#tab/app-update-5-and-later)

        Legg til følgende linjer i delen **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;**.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        Legg til følgende linjer i **ItemGroup**-delen for å ta med proxyutvidelsen for Retail i de distribuerbare pakkene:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 og senere](#tab/retail-7-3-2)

        Legg til følgende linjer i **ItemGroup**-delen for å ta med proxyutvidelsen for Retail i de distribuerbare pakkene:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 og senere](#tab/retail-7-3-5)

        Legg til følgende linjer i **ItemGroup**-delen for å ta med proxyutvidelsen for Retail i de distribuerbare pakkene:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 og senere](#tab/retail-8-1-1)

        Legg til følgende linjer i **ItemGroup**-delen for å ta med proxyutvidelsen for Retail i de distribuerbare pakkene:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. Legg til følgende linjer i **ItemGroup**-delen for å ta med CRT-utvidelsen i de distribuerbare pakkene:

        # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-later"></a>[Appoppdatering 5 og senere](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 og senere](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 og senere](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 og senere](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        ---

    3. Legg til følgende linjer i **ItemGroup**-delen for å ta med utvidelsen for Retail Server i de distribuerbare pakkene:

        # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-later"></a>[Appoppdatering 5 og senere](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 og senere](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 og senere](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 og senere](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. Endre følgende filer slik at de inneholder ressursfilene for Norge i distribuerbare pakker:
    - Packages\_SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj
    - Packages\RetailServer\Sdk.RetailServerSetup.proj
  
  - For filen **Sdk.ModernPos.Shared.csproj** 
    - Legg til linje i **ItemGroup**-delen
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > [!Note]
    > I stedet for <File_name> angir du navnet på ressursfilen. Det samme er relevant for de andre eksemplene som vises nedenfor.
 
    - Legg til linjen i delen **Target Name="CopyPackageFiles"**
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - For filen **Sdk.RetailServerSetup.proj** 
    - Legg til linje i **ItemGroup**-delen
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - Legg til linjen i delen **Target Name="CopyPackageFiles"**
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. Endre sertifikatets konfigurasjonsfil ved å angi avtrykket, butikklokasjonen og butikknavnet for sertifikatet som skal brukes til å signere salgstransaksjoner. Deretter kopierer du konfigurasjonsfilen til **Referanser**-mappen.

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    Filen heter **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** og ligger under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="application-update-5-and-later"></a>[Appoppdatering 5 og senere](#tab/app-update-5-and-later)

    Filen heter **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** og ligger under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    Filen heter **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** og ligger under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og senere](#tab/retail-7-3-2)

    Filen heter **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** og ligger under **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og senere](#tab/retail-7-3-5)

    Filen heter **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** og ligger under **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og senere](#tab/retail-8-1-1)

    Filen heter **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** og ligger under **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    ---

6. Oppdater konfigurasjonsfilen for Retail Server. I filen **RetailSDK\\Packages\\RetailServer\\Code\\web.config** legger du til følgende linjer i delen **extensionComposition**.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

7. Kjør **msbuild** for hele Retail SDK for å opprette distribuerbare pakker.
8. Ta i bruk pakkene via Microsoft Dynamics Lifecycle Services (LCS) eller manuelt. Hvis du vil ha mer informasjon, kan du se [Opprette distribuerbare pakker](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Aktiver den digitale signaturen i frakoblet modus for Modern POS

Hvis du vil aktivere den digitale signaturen i frakoblet modus for Modern POS, må du følge disse trinnene etter at du har aktivert Modern POS på en ny enhet.

1. Logg på POS.
2. På siden **Status for databasetilkobling** må du kontrollere at den frakoblede databasen er fullstendig synkronisert. Når verdien i feltet **Ventende nedlastinger** er **0** (null), synkroniseres databasen fullstendig.
3. Logg av salgsstedet.
4. Vent litt til den frakoblede databasen er fullstendig synkronisert.
5. Logg på POS.
6. På siden **Status for databasetilkobling** må du kontrollere at den frakoblede databasen er fullstendig synkronisert. Når verdien i feltet **Ventende transaksjoner i frakoblet database** er **0** (null), synkroniseres databasen fullstendig.
7. Start Modern POS på nytt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
