---
title: Definer direkte integrering av italiensk FatturaPA med SDI
description: Denne artikkelen gir informasjon som vil hjelpe deg med å komme i gang med elektronisk fakturering for Italia og definere direkte integrering av italiensk FatturaPA med utvekslingssystemet (SDI).
author: abaryshnikov
ms.date: 07/27/2022
ms.topic: article
audience: Application User, Developer
ms.reviewer: kfend
ms.search.region: Global
ms.author: abaryshnikov
ms.search.validFrom: 2021-10-18
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 363b7b5e3d5abbb990fea8f8ad4d0c1bebf80102
ms.sourcegitcommit: 6d9fcb52d723ac5022a3002e0ced8e7b56e9bc2a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/27/2022
ms.locfileid: "9203177"
---
# <a name="set-up-direct-integration-of-italian-fatturapa-with-sdi"></a>Definer direkte integrering av italiensk FatturaPA med SDI

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Det er ikke sikkert at Elektronisk fakturering for Italia støtter alle funksjonene som er tilgjengelige for elektroniske fakturaer i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.

Denne artikkelen inneholder informasjon som vil hjelpe deg med å komme i gang med elektronisk fakturering for Italia i Finance and Supply Chain Management. Det leder deg gjennom konfigurasjonstrinnene som er lands-/områdeavhengige i Regulatory Configuration Services (RCS). Denne fremgangsmåten utfyller fremgangsmåten som beskrives i [Kom i gang med elektronisk fakturering](e-invoicing-get-started.md).

## <a name="prerequisites"></a>Forutsetninger

Før du kan fullføre fremgangsmåten i denne artikkelen, må følgende forutsetninger oppfylles:

- Fullfør fremgangsmåten i [Kom i gang med elektronisk fakturering](e-invoicing-get-started.md).
- Importer den elektroniske faktureringsfunksjonen **italienske FatturaPA(IT)** til RCS fra det globale repositoriet. Hvis du vil ha mer informasjon, kan du se delen [Importer en elektronisk faktureringsfunksjon fra Microsoft-konfigurasjonsleverandøren](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider) i den ovennevnte artikkelen Kom i gang med elektronisk fakturering.
- Legg til koblinger fra de nødvendige sertifikatene i servicemiljøet. De nødvendige sertifikatene omfatter sertifikatet for digital signatur, CA-sertifikatet (Certificate Authority) og klientsertifikatet. Hvis du vil ha mer informasjon, kan du se delen [Opprette en digital sertifikathemmelighet](e-invoicing-get-started-service-administration.md#create-a-digital-certificate-secret) i artikkelen Kom i gang med tjenesteadministrasjon for elektronisk fakturering.

## <a name="country-specific-configuration-for-the-italian-fatturapa-it-electronic-invoicing-feature"></a>Landspesifikk konfigurasjon for den elektroniske faktureringsfunksjonen for italiensk FatturaPA (IT)

Fullfør følgende fremgangsmåte før du distribuerer programoppsettet til den tilkoblede appen i Finans eller Supply Chain Management.

Denne delen utfyller delen [Landspesifikk konfigurasjon for programoppsett](e-invoicing-get-started.md#country-specific-configuration-of-application-setup) i artikkelen Kom i gang med elektronisk fakturering.

### <a name="create-a-new-feature"></a>Opprett en ny funksjon

1. Logg på RCS.
2. Merk firmaets konfigurasjonsleverandør som aktiv i delen **Konfigurasjonsleverandører** i arbeidsområdet for **elektronisk rapportering**.
3. I arbeidsområdet **Globaliseringsfunksjon**, i **Funksjoner**-delen velger du flisen **Elektronisk fakturering**.
4. Velg **Legg til** \> **Basert på eksisterende funksjon** på siden **Funksjoner for elektronisk fakturering**.
5. Under **Microsoft-konfigurasjonsleverandør** velger du **Italiensk FatturaPA (IT)** som basisfunksjon, angir et navn og velger deretter **Opprett funksjon**.

### <a name="set-up-application-specific-parameters"></a>Konfigurere programspesifikke parametere

1. Velg funksjonen du vil redigere på siden **Funksjoner for elektronisk fakturering**.
2. I fanen **Versjoner** kontrollerer du at versjonen **Utkast** er valgt.
3. Velg konfigurasjonen, og velg deretter **Programspesifikke parametere** på fanen **Konfigurasjoner**.
4. I **Oppslag**-delen må du kontrollere at oppslaget **Liste over underkategorier for snudd avregning for Natura** er valgt.
5. Velg **Legg til** i delen **Betingelser**.
6. Legg til spesifikke betingelser for hver underkategori som er definert i systemet, og lagre endringene.

    > [!NOTE]
    > I **Navn**-kolonnen kan du velge plassholderverdien **\*Tom\*** eller **\*Ikke tom\*** i stedet for en bestemt verdi.

### <a name="configure-a-processing-pipeline-for-export"></a>Konfigurer et behandlingsforløp for eksport

1. Velg funksjonen du vil redigere på siden **Funksjoner for elektronisk fakturering**.
2. Velg **Salgsfakturaer** og velg deretter **Rediger** i fanen **Oppsett**.
3. I **Behandlingsforløp**-delen kan du gå gjennom handlingene og angi alle de obligatoriske feltene:

    - For **Signer dokument**-handlingen angir du det digitale signatursertifikatet for i **Sertifikatnavn**-feltet.
    - For **Send**-handlingen angir du **URL-adressen** og **Sertifikater**-feltene. Verdien til **Sertifikater**-feltet er en kjede av sertifikater, den første som er roten av CA-sertifikatet (caentrate.cer), og det andre er Klienter-sertifikatet.

4. I delen **Relevansregler** kan du gå gjennom klausulene og se gjennom eller angi de obligatoriske feltene:
    - Gå gjennom **LegalEntityID**-klausulen, og oppdater den med riktig verdi fra den juridiske enheten.

5. Velg **Valider** for å sikre at alle obligatoriske felter er angitt.
6. Lagre endringene, og lukk siden.
7. Velg **Prosjektfakturaer** og velg deretter **Rediger** i fanen **Oppsett**.
8. Gjenta trinn 3 til og med 6 for prosjektfakturaer.

### <a name="configure-the-processing-pipeline-for-import"></a>Konfigurer behandlingsforløpet for import

1. Velg funksjonen du vil redigere på siden **Funksjoner for elektronisk fakturering**.
2. Velg **Importfakturaer** og velg deretter **Rediger** i fanen **Oppsett**.
3. Angi en strengverdi i **Datakanal**-delen i **Parameter**-fanen i **Datakanal**-feltet.
4. Angi feltene for oppsettet i fanen **Relevansregler**. Du kan bruke standard **kanalsetning** ved å sende verdien du definerte for **Datakanal**-feltet i det forrige trinnet, til **Verdi**-feltet.

    ![Konfigurer relevansregler.](media/e-invoicing-ita-fatturapa-get-started-apprules-setup.png)

5. Velg **Valider** for å sikre at alle obligatoriske felter er angitt.

### <a name="deploy-the-feature"></a>Distribuer funksjonen

1. Fullfør, publiser og distribuer funksjonen for servicemiljøet. Hvis du vil ha mer informasjon, kan du se delen [Distribuer den elektronisk faktureringsfunksjonen til servicemiljøet](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment) i den ovennevnte artikkelen Kom i gang med elektronisk fakturering.
2. Distribuer funksjonen for det tilkoblede programmet. Hvis du vil ha mer informasjon, kan du se delen [Distribuer den elektronisk faktureringsfunksjonen til tilkoblet program](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application) i den ovennevnte artikkelen Kom i gang med elektronisk fakturering.

### <a name="set-up-finance"></a>Definer Finance

1. Logg på Finance-miljøet.
2. I delen **Konfigurasjonsleverandører** i arbeidsområdet **Elektronisk rapportering** velger du flisen **Microsoft**.
3. Velg **Repositorier** \> **Globalt** \> **Åpne**.
4. Velg og importer konfigurasjoner for **kundefakturakontekstmodell** og **Leverandørfaktura (IT)**.
5. Gå til **Organisasjonsstyring** \> **Oppsett** \> **Parametere for elektronisk dokument**.
6. I fanen **Funksjoner** finner og velger du funksjonen **Italiensk elektronisk faktura**, og merker deretter av for **Aktiver**.
7. I fanen **Elektronisk dokument** kontrollerer du at feltene for **kundefakturajournal** og **prosjektfaktura** er angitt i henhold til informasjonen i [Konfigurer programoppsettet](e-invoicing-get-started.md#configure-the-application-setup).

### <a name="set-up-vendor-invoice-import"></a>Definere leverandørfakturaimport 

1. Merk firmaets konfigurasjonsleverandør som aktiv i delen **Konfigurasjonsleverandører** i arbeidsområdet for **elektronisk rapportering** i Finance.
2. Velg **Rapporteringskonfigurasjoner**.
3. Velg **Kontekstmodell for kundefaktura** og velg deretter **Opprett konfigurasjon**.
4. Velg **Avled fra navn: Kundefakturakontekst, Microsoft** for å opprette en avledet konfigurasjon.
5. Velg **Utforming** i **Utkast**-versjonen.
6. I **Datamodell**-treet velger du **Tilordne modell til datakilde**.
7. Velg **DataChannel** i **Definisjoner**-treet, og velg deretter **Utforming**.
8. I **Datakilder**-treet utvider du **\$Context\_Channel**-containeren.
9. Velg **Rediger** i **Verdi**-feltet. 
10. Angi navnet på datakanalen. Navnet må ha maksimum 10 tegn. Den bør samsvare med verdien til **Datakanal**-parameteren til datakanalen for funksjonen elektronisk fakturering i RCS.
11. Lagre endringene og gå deretter til **Rapporteringskonfigurasjon** \> **Fullfør konfigurasjonsversjon**.
12. Velg **Legg til** i fanen **Eksterne kanaler** i delen **Kanaler**.
13. I **Kanal**-feltet angir du **\$Context Channel**-verdien.
14. Angi verdier i feltene **Beskrivelse** og **Selskap**.
15. Velg **Kontekstmodell for kundefaktura** som du avledet fra i **Dokumentkontekst**-feltet. Tilordningsbeskrivelsen må være **Datakanalkontekst**.
16. Velg **Legg til** i fanen **Importer kilder**, og angi deretter følgende verdier:

    - **Navn:** OutputFile
    - **Navn på dataenhet:** Leverandørfakturahode (**Dataenhet:** VendorInvoiceHeaderEntity)
    - **Modelltilordning:** Leverandørfakturaimport (IT)

> [!NOTE]
> Hvis du har importert leverandørfakturaer fra forskjellige kilder, kan du opprette flere eksterne kanaler og flere avledede konfigurasjoner som har forskjellige **\$Context Channel**-verdier. Det kan for eksempel hende at du vil importere leverandørfakturaer for ulike juridiske enheter.

## <a name="proxy-server-setup"></a>Proxy-serveroppsett

Denne delen inneholder informasjon som vil hjelpe deg med å definere og konfigurere proxy-tjenesten for kommunikasjon mellom utvekslingssystemet (SDI) og tjenesten for elektronisk fakturering.

### <a name="create-an-app-registration"></a>Opprett en appregistrering

1. Bruk dette Windows PowerShell-skriptet til å opprette et selvsignert sertifikat for tjeneste-til-tjeneste-godkjenning (S2S).

    ```powershell
    $certOutputLocation = "C:\certs\proxytest"
    $certName = "sdiProxyClientS2SCert"
    $certPassword = "123"

    $certCerFile = Join-Path $certOutputLocation "$certName.cer"
    $certPfxFile = Join-Path $certOutputLocation "$certName.pfx"

    $securePassword = ConvertTo-SecureString $certPassword -AsPlainText -Force

    $cert = New-SelfSignedCertificate -KeyLength 2048 -KeyExportPolicy Exportable -FriendlyName "CN=$certName" -CertStoreLocation Cert:\CurrentUser\My -Subject $certName -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider"

    Export-Certificate -Cert $cert -FilePath $certCerFile -type CERT | Out-Null
    Export-PfxCertificate -Cert $cert -FilePath $certPfxFile -Password $securePassword | Out-Null
    ```

2. Lagre .pfx-sertifikatfilen i nøkkelhvelvet, og slett deretter den lokale kopien.
3. Logg deg på [Azure Portal](https://portal.azure.com) som administrator.
4. Opprett en appregistrering for SDI Proxy-tjenesten.

    1. Gå til **Appregistreringer**, opprett en registrering, og angi deretter følgende verdier for den:

        - **Navn:** SDI-proxy-klient
        - **Kontotyper som støttes:** Kontoer bare i denne organisasjonskatalogen (enkelt leietaker)

    2. Velg **Registrer**, og velg deretter appregistreringen som du akkurat opprettet.
    3. Gå til **API-tillatelser** og velg **Gi administrator tillatelse**.
    4. Gå til **Sertifikater og hemmeligheter**, velg **Last opp sertifikat**, og last opp .cer-sertifikatfilen for S2S-godkjenning.
    5. Gå til **Bedriftsprogrammer**, og velg appen du opprettet.
    6. Lagre verdiene for **program-ID-en** (klient-ID) og **objekt-ID** for appen.
    7. Faktureringstjenestegruppen må gi appen tilgang til tjenesten. Send verdiene fra følgende parametere til <D365EInvoiceSupport@microsoft.com>:

        - AAD-leietaker-ID
        - LCS-miljø-ID
        - App-ID
        - Objekt-ID

5. I RCS legger du til appen i listen for servicemiljøet.

    1. Gå til **Globaliseringsfunksjoner** \> **Miljøer** \> **Elektronisk fakturering** \> **Servicemiljøer**, og velg miljøet.
    2. I **Programmer**-delen legger du til en rad i rutenettet, og angir navnet og objekt-ID-en for appen.

        ![Legge til programmet i servicemiljøet.](media/e-invoicing-ita-fatturapa-get-started-add-app-to-env.png)

    3. Velg **Lagre**, og velg deretter **Publiser**.

### <a name="create-an-azure-virtual-machine"></a>Opprette en virtuell Azure-maskin

1. Gå til **Virtuelle maskiner** i [Azure Portal](https://portal.azure.com), og velg deretter **Opprett ny**.
2. Velg abonnementet og ressursgruppen i fanen **Grunnleggende**. Verdiene skal være abonnements- og ressursgruppen der nøkkelhvelvet og Blob-lagringen er plassert.
3. Velg området. Denne verdien bør være området der Finance-miljøet er distribuert.
4. Legg til administratorens brukernavn og passord, og lagre dem i nøkkelhvelvet.
5. Velg **HTTPS (443)** og **RPD (3389)** i feltet **Velg innkommende porter**.

    > [!NOTE]
    > Vi anbefaler at du deaktiverer porten **RDP (3389)** når systemet går til produksjon. Du kan aktivere den på nytt hvis du må koble til VM (virtuell maskin) for feilsøking.

    ![Definer feltene i fanen Grunnleggende for å opprette en Azure VM.](media/e-invoicing-ita-fatturapa-get-started-create-vm-1.png)

6. Merk av for **Bruk administrerte disker** i fanen **Avansert**-hurtigfanen på fanen **Disker**. La avmerkingsboksen **Ephemeral OS-disk** være tom.

    ![Definer feltene i fanen Disker for å opprette en Azure VM.](media/e-invoicing-ita-fatturapa-get-started-create-vm-2.png)

7. Velg **Opprett ny** under **Offentlig IP**-feltet i fanen **Nettverk**.

    ![Definer feltene i fanen Nettverk for å opprette en Azure VM.](media/e-invoicing-ita-fatturapa-get-started-create-vm-3.png)

8. I **Opprett offentlig IP-adresse**-dialogboksen i **SKU**-feltet velger du **Standard**-alternativet. I feltet **Tilordning** velger du alternativet **Statisk**.

    ![Opprette en offentlig IP-adresse.](media/e-invoicing-ita-fatturapa-get-started-create-vm-4.png)

9. I fanen **Behandling** fjerner du merket for **Automatisk avslutning** for å deaktivere automatisk avslutning.
10. Sett feltet **Gjeste-OS-oppdateringer** til **Manuell**, og angi deretter eventuelle andre policyer.
11. Se gjennom og opprett VM.
12. I den nye VM-en kan du gå til **Identitet** \> **Systemtilordnet**, og sette **Status**-alternativet til **På**.
13. Gi VM-tilgang til nøkkelhvelvet.

    1. I nøkkelhvelvet kan du gå til **Tilgangskontroll (IAM)** \> **Rolletilordninger**.
    2. Velg **Legg til rolletilordning**, og deretter angi følgende felter:

        1. I **Rolle**-feltet angir du **Bruker av nøkkelhvelvhemmeligheter**.
        2. I feltet **Tilordne tilgang til** angir du **Virtuell maskin**.
        3. Angi abonnementet i **Abonnement**-feltet.
        4. Angi VM i **Velg**-feltet.

    3. Gå til **Tilgangspolicyer**.
    4. Velg **Legg til tilgangspolicy**, og deretter angi følgende felter:

        1. I feltet **Valgt sikkerhetskontohaver** velger du VM-en.
        2. Angi tillatelsene **Hent** og **Liste** i delen **Sertifikat**.

14. Gå til **Offentlige IP-adresser** i [Azure Portal](https://portal.azure.com), og velg IP-adressen som ble opprettet i VM-en.
15. Gå til **Konfigurasjon**, og angi DNS-navnet (Domain Name System).

### <a name="prepare-the-proxy-service-environment"></a>Klargjøre proxy-servicemiljøet

Følg denne fremgangsmåten på maskinen som er vert for proxy-tjenesten.

1. Koble til VM ved hjelp av Tilkobling til eksternt skrivebord.
2. Åpne snapin for det lokale maskinsertifikatet. Hvis du vil ha mer informasjon, kan du se [Veiledning: Vis attester med MMC-snapin](/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in) .
3. Importer **caentrate.cer**-sertifikatet for produksjon og **CAEntratetest.cer** for testing til [butikken for klarerte rotsertifiseringsinstanser](/dotnet/framework/wcf/feature-details/working-with-certificates#certificate-stores). (**CAEntratetest.cer** er roten av CA-sertifikatet som ble angitt av myndighetene.)
4. I Kontrollpanel åpner du **Slå Windows-funksjoner på eller av**, eller går til **Serveradministrasjon** \> **Legg til roller og funksjoner** for serveroperativsystemet (OS), og slår på IIS-funksjoner (Internet Information Services):

    - Nettadministrasjonsverktøy
        - IIS-administrasjonskonsoll
    - World Wide Web Services
        - Programutviklingsfunksjoner
            - .NET Extensibility 4.7 (eller 4.8)
            - ASP
            - ASP.NET 4.7 (eller 4.8)
            - CGI
            - ISAPI-tillegg
            - ISAPI-filtre
        - Vanlige HTTP-funksjoner
            - Standarddokument
            - Mappevisning
            - HTTP-feil
            - Statisk innhold
        - Tilstand og diagnostikk
            - HTTP-logging
            - Sporing
        - Ytelsesfunksjoner
            - Statisk innholdskomprimering
        - Sikkerhet
            - Be om filtrering

    ![Aktiver IIS-funksjonene.](media/e-invoicing-ita-fatturapa-get-started-turnon-features.png)

### <a name="set-up-the-sdi-proxy-service-in-iis"></a>Konfigurer SDI-proxy-tjenesten i IIS

1. I Microsoft Dynamics Lifecycle Services (LCS) går du til Delt aktivabibliotek og velger **Datapakke** som aktivatype.
2. Finn **Sdi-proxy for elektronisk faktureringstjeneste**, og last den ned til VM.
3. Konfigurer tjenesten.

    1. Pakk ut arkivmappen for **Sdi-proxy-arkiv for elektronisk fakturering** som du lastet ned.
    2. I mappen **src\\FattureService** åpner du filen **appsettings.json**, og angir følgende parametere:

        - **KeyVaultUri** – Angi adressen til nøkkelhvelvet som lagrer klientsertifikatet for faktureringstjenesten.
        - **TenantId** – Angi den globalt unike identifikatoren (PST) for kundens leietaker.
        - **EnvironmentId** – Angi ID-en for LCS-miljøet.
        - **ClientId** – Angi app-ID-en for appregistreringen for mellomliggende tjenester i kundens leietaker.
        - **ClientCertificateName** – Angi navnet på S2S-sertifikatet i nøkkelhvelvet.
        - **SecurityServiceClientOptions.Endpoint** – Angi URL-adressen til sikkerhetstjenesten.
        - **SecurityServiceClientOptions.Resource** – Angi området du vil hente tokenet for.
        - **InvoicingServiceClientOptions.Endpoint** – Angi sluttpunktet for faktureringstjenesten. Denne verdien skal være det samme sluttpunktet som brukes for RCS og Finance.
        - **InvoicingServiceClientOptions.ServiceEnvironmentId** – Angi navnet på tjenestemiljøet. Denne verdien bør være navnet på Finance-miljøet.
        - **NotificationsFolder** – Angi mappen innkommende varslingsfiler skal lagres i.

    3. I **web.config**-filen finner du følgende linje, og legger til oppsigelsesuttrykket for proxy-serversertifikatet.

        `<serviceCertificate findValue="[certificate thumbprint]" storeLocation="LocalMachine" storeName="My" x509FindType="FindByThumbprint">`

        > [!TIP]
        > Når systemet går til produksjon, kan du endre noen verdier i web.config-filen for å redusere mengden logginformasjon som samles inn, og bidra til å spare diskplass. I noden **\<system.diagnostics\>\<source\>** endrer du verdien for **switchValue** til **Critical,Error**. Hvis du vil ha mer informasjon, kan du se [MS Service Trace Viewer](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe).

4. Åpne IIS Manager. I treet til venstre blir du værende i rotnoden. Velg **Serversertifikater** til høyre.

    ![Velg servicesertifikater i IIS Manager.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-1.png)

5. Åpne menyen, og velg **Importer**.
6. I feltet **Sertifikatfil (.pfx)** i dialogboksen **Importsertifikat** angir du banen til PFX-filen for proxy-serversertifikatet.

    ![Angi proxy-servicesertifikatfilen.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-2.png)

7. Velg og hold (eller høyreklikk på) **Områder**, og velg deretter **Legg til nettsted**.
8. I dialogboksen **Legg til nettsted** skriver du inn et navn på oppgaven i **Områdenavn**-feltet.
9. I feltet **Fysisk bane** peker du på **src\\FattureService**-mappen.
10. Velg **https** i feltet **Bindingstype**.
11. I **Vertsnavn**-feltet angir du vertsnavnet.
12. La feltene **IP-adresse** og **Port** være satt til standardverdiene.
13. Kontroller at det ikke er merket av for **Krev servernavnangivelse**, fordi SDI ikke støtter denne teknologien.
14. Velg proxy-serversertifikatet du importerte, i feltet **SSL-sertifikat**.
15. I **Programutvalg**-feltet angir du en pulje for området, og noterer navnet (for eksempel **SdiAppPool**).

    ![Legg til et nettsted.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-1.png)

16. Når du er ferdig med å opprette nettstedet, åpner du menyen for **SSL-innstillinger**.

    ![Åpne menyen for SSL-innstillinger.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-2.png)

17. Merk av for **Krev SSL**, og velg deretter alternativet **Krev** i feltgruppen **Klientsertifikater**.

    ![Konfigurer SSL-innstillinger.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-3.png)

18. Åpne **Mappevisning** og velg **Aktiver**.
19. I en hvilken som helst nettleser kan du gå til **serverDNS/TrasmissioneFatture.svc**. Det må vises en standardside om tjenesten.

    ![Kontroller tjenesten i en nettleser.](media/e-invoicing-ita-fatturapa-get-started-proxy-open-browser.png)

20. Opprett følgende mapper for å lagre logger og filer:

    - **C:\\Logger\\** – Butikkloggfiler her. Disse filene kan vises av [MS Service Trace Viewer](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe).
    - **C:\\Filer\\** – Lagre alle svarfilene her.

21. I Filutforsker gir du **NETWORK SERVICE** og **IIS AppPool\\SdiAppPool** (eller **IIS AppPool\\DefaultAppPool** hvis du bruker standardpuljen) tilgang til amppene **Logger** og **Filer**.

    1. Velg og hold (eller høyreklikk på) på en av mappene, og velg deretter **Egenskaper**.
    2. Velg **Rediger** i fanen **Sikkerhet** i dialogboksen **Egenskaper**.
    3. Legg til brukerne hvis de ikke er oppført.
    4. Gjenta trinn 1 til 3 for alle den andre mappen.

    ![Legg til tillatelser til tjenestebrukeren.](media/e-invoicing-ita-fatturapa-get-started-proxy-add-user.png)

## <a name="privacy-notice"></a>Personvernerklæring 

Hvis du aktiverer funksjonen for **italiensk elektronisk faktura**, kan det hende at det må sendes begrensede data. Disse dataene inkluderer organisasjonens avgiftsregistrerings-ID. En administrator kan aktivere og deaktivere den italienske elektroniske fakturafunksjonen. Følg denne fremgangsmåten for å deaktivere denne funksjonen.

1. Gå til **Organisasjonsstyring** \> **Oppsett** \> **Parametere for elektronisk dokument**.
2. I fanen **Funksjoner** finner og velger du radene som inneholder funksjonen **Italiensk elektronisk faktura**, og merker deretter av for **Deaktiver nå**.

Data som er importert fra disse eksterne systemene til denne Dynamics 365-elektroniske tjenesten, er underlagt vår [personvernerklæring](https://go.microsoft.com/fwlink/?LinkId=512132). Hvis du vil ha mer informasjon, kan du se delene Personvernmerknad i dokumentasjon for landspesifikke funksjoner.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk fakturering](e-invoicing-service-overview.md)
- [Komme i gang med tjenesteadministrasjon for elektronisk fakturering](e-invoicing-get-started-service-administration.md)
- [Komme i gang med Elektronisk fakturering](e-invoicing-get-started.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
