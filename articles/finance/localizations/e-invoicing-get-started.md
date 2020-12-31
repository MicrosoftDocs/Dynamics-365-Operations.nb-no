---
title: Komme i gang med tillegget Elektronisk fakturering
description: Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med tillegget Elektronisk fakturering i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 10/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 7b2a3aae43d42060c7fcd9e1ea3db814fc5d8f22
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/19/2020
ms.locfileid: "4446578"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Komme i gang med tillegget Elektronisk fakturering

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med tillegget Elektronisk fakturering. Først veileder den deg gjennom konfigurasjonstrinnene i Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Services (RCS) og Dynamics 365 Finance. Deretter beskrives prosessen for sending av dokumenter via tjenesten ved hjelp av Dynamics 365 Finance eller Dynamics 365 Supply Chain Management. Du vil også lære hvordan du tolker de sendte loggene.

## <a name="availability"></a>Tilgjengelighet

Tillegget Elektroniske fakturering er opprinnelig tilgjengelig for flere land. Tillegget støtter oppretting av elektroniske fakturaer og sending av følgende forretningsdokumenter:

| Land/område  | Forretningsdokument                          |
|-----------------|--------------------------------------------|
| Østerrike         | Salgs- og prosjektfakturaer                 |
| Belgia         | Salgs- og prosjektfakturaer                 |
| Brasil          | Elektronisk regnskapsdokumentmodell 55 (NF-e) |
| Danmark         | Salgs- og prosjektfakturaer                 |
| Estland         | Salgs- og prosjektfakturaer                 |
| Finland         | Salgs- og prosjektfakturaer                 |
| Frankrike          | Salgs- og prosjektfakturaer                 |
| Tyskland         | Salgs- og prosjektfakturaer                 |
| Italia           | Salgs- og prosjektfakturaer                 |
| Mexico          | CFDI-faktura                               |
| Nederland     | Salgs- og prosjektfakturaer                 |
| Norge          | Salgs- og prosjektfakturaer                 |
| Spania           | Salgs- og prosjektfakturaer                 |
| Europa          | PEPPOL Salgs- og prosjektfakturaer          |
    
## <a name="licensing"></a>Lisensiering

Du kan bruke tillegget Elektroniske fakturering med den gjeldende lisensen. Ingen flere lisenser er nødvendig for å bruke tjenesten.

## <a name="prerequisites"></a>Forutsetninger

Før du kan fullføre trinnene i dette emnet må du ha følgende forutsetninger på plass:

- Tilgang til LCS-kontoen din.
- Et LCS-distribusjonsprosjekt som omfatter Finance eller Supply Chain Management versjon 10.0.13 eller senere.
- Tilgang til RCS-kontoen din.
- Slå på globaliseringsfunksjonen for kontoen for RCS via modulen **Funksjonsbehandling**. Hvis du vil ha mer informasjon, kan du se [Regulatory Configuration Services (RCS) – globaliseringsfunksjoner](rcs-globalization-feature.md)
- Opprett en Key Vault-ressurs og en lagringskonto i Azure. Hvis du vil ha mer informasjon, kan du se [Opprette en Azure Storage-konto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="overview"></a>Oversikt

Illustrasjonen nedenfor viser de fem hovedtrinnene du vil fullføre i dette emnet.

![Oversikt over de fem trinnene i dette emnet](media/e-invoicing-services-get-started-overview-5-steps.png)

1. **Innstillinger for Azure-ressurser:** Konfigurer Azure Storage og opplasting av digitale sertifikater i Azure Key Vault.
2. **LCS-oppsett:** Installer tillegget for mikrotjenestene.
3. **RCS-oppsett:** Definer funksjonene for miljø, brukertilgang og e-faktureringsfunksjoner.
4. **Klientoppsett:** Konfigurer forbindelsen mellom klienten og tillegget Elektronisk fakturering, og slå av de gamle funksjonene for innsending og mottak av svar for elektroniske dokumenter.
5. **Sende fakturaer:** Send elektroniske dokumenter via tillegget Elektronisk fakturering, og motta svar.

> [!NOTE]
> Noen konfigurasjonstrinn i dette emnet er vanlige og land/område-agnostiske. Fremgangsmåtene og oppsettsprosedyrene som er land/område-spesifikke, er beskrevet i land/område-spesifikke emner.

## <a name="lcs-setup"></a>LCS-oppsett

1. Logg på LCS-kontoen.
2. Velg ruten **Administrasjon av forhåndsvisningsfunksjoner**, og i feltgruppen **Offentlig forhåndsversjon** velger du **BusinessDocumentSubmission**.
3. Merk av for **Forhåndsversjon aktivert**.
4. Velg LCS-distribusjonsprosjektet. Du må kjøre et prosjekt før du kan velge det.
5. I hurtigfanen **Miljøtillegg** velger du **Installer et nytt tillegg**.
6. Velg alternativet for **Innsending av forretningsdokument**.
7. I dialogboksen **Konfigurer tillegg** i feltet **AAD-program-ID** angir du **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Denne verdien er en fast verdi.
8. I feltet **AAD-leier-ID** angir du IDen til kontoen for Azure-abonnementet.

    ![Dialogboksen Konfigurer tillegg i LCS](media/e-invoicing-services-get-started-lcs-addin-setup.png)

9. Merk av i avmerkingsboksen for å godta vilkårene og betingelsene.
10. Velg **Installer**.

## <a name="rcs-setup"></a>RCS-oppsett

Under RCS-oppsettet vil du fullføre disse oppgavene:

1. Konfigurer Key Vault i RCS.
2. Konfigurer RCS-integreringen med serveren for tillegget Elektronisk fakturering.
3. Opprett et miljø for tillegget Elektronisk fakturering for organisasjonen.

### <a name="set-up-the-key-vault-in-rcs"></a>Konfigurere Key Vault i RCS

1. Logg på RCS-kontoen.
2. I **Globaliseringsfunksjoner**-arbeidsområder i delen **Miljøer**, velger du flisen **E-fakturering**.
3. Velg **Servicemiljøer**.

    ![Velge Servicemiljøer](media/e-invoicing-services-get-started-select-service-environments.png)

> [!NOTE]
> Alternativet **Tilkoblede programmer** gir tilgang til automatisk konfigurasjon av tillegget Elektronisk fakturering i Finance eller Supply Management via RCS. Denne funksjonen er imidlertid fortsatt under utvikling.

4. Velg **Key Vault-parametere** i handlingsruten.

    ![Velge Key Vault-parameter](media/e-invoicing-services-get-started-select-key-vault-parameters.png)

5. I handlingsruten velger du **Ny** for legge til et Key Vault.
6. I **URI for Key Vault**-feltet angir du **DNS-navn**-attributtverdien for Key Vault-ressursen du konfigurerte i Azure. Hvis du vil ha informasjon om hvor du finner **DNS-navn**-verdien, kan du se [Opprette en Azure Storage-konto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).

    ![Feltet URI for Key Vault](media/e-invoicing-services-get-started-enter-key-vault-uri.png)

7. I hurtigfanen **Sertifikater** velger du **Legg til** for å angi navn på alle digitale sertifikater og Key Vault-hemmeligheter som er nødvendige for å opprette klarerte tilkoblinger. I **Type**-kolonnen kan du angi om det er et sertifikat eller en hemmelighet. Begge settene med verdier konfigureres på Key Vault-ressursen i Azure.

    ![Legge til sertifikater](media/e-invoicing-services-get-started-add-digital-certificates.png)

8. Hvis den land/område-spesifikke fakturaen krever en sertifikatkjede for å bruke en digital signatur, velger du **Kjede av sertifikater** i handlingsruten, og deretter angir du rekkefølgen av sertifikater eller Key Vault-hemmeligheter som utgjør kjeden.

### <a name="set-up-the-rcs-integration-with-the-electronic-invoicing-add-on-server"></a>Konfigurere RCS-integreringen med serveren for tillegget Elektronisk fakturering

1. I arbeidsområdet **Globaliseringsfunksjoner** i delen **Relaterte innstillinger** velger du koblingen **Parametere for elektronisk rapportering**.
2. Velg **Klikk her for å koble til Lifecycle Service**. Hvis du ikke vil koble til LCS, velger du **Avbryt**.
3. I kategorien **E-faktureringstjenester** i feltet **URI for endepunkt for tjeneste**, angir du verdien i samsvar med de tilgjengelige områdene: `https://businessdocumentsubmission.us.operations365.dynamics.com/` eller `https://businessdocumentsubmission.eu.operations365.dynamics.com/`.
4. I feltet **Program-ID** kontrollerer du at IDen **0cdb527f-a8d1-4bf8-9436-b352c68682b2** vises. Denne verdien er en fast verdi.
5. I feltet **ID for LCS-miljø** angir du IDen for LCS-abonnementskontoen.

![Angi parametere for tillegget Elektronisk fakturering](media/e-invoicing-services-get-started-enter-e-invoicing-parameters.png)

### <a name="add-an-electronic-invoicing-add-on-environment"></a>Legge til et miljø for tillegget Elektronisk fakturering

Du kan opprette ulike miljøer for tillegget Elektronisk fakturering, for eksempel utvikling-, test eller produksjonsmiljøer.

1. I **Globaliseringsfunksjoner**-arbeidsområder i delen **Miljøer**, velger du flisen **E-fakturering**.
2. Velg **Ny** for å opprette et miljø.
3. I feltet for **Feltet lagringskonto for SAS-token** angir du navnet på KEY VAULT-hemmeligheten du konfigurerte i KEY VAULT i RCS.

    ![Feltet for konto for lagrings-SAS-token](media/e-invoicing-services-get-started-enter-sas-token-secret.png)

4. I hurtigfanen **Brukere** velger du **Ny** for å gi tilgang til brukere for dette miljøet.

    ![Legge til tjenestebrukere](media/e-invoicing-services-get-started-enter-service-users.png)

5. Velg **Publiser** i handlingsrutenfor å publisere miljøet på serveren for tillegget Elektronisk fakturering.

    ![Publiser-knapp](media/e-invoicing-services-get-started-publish-service-environment.png)

### <a name="e-invoicing-feature-setup"></a>Oppsett for e-faktureringsfunksjon

"E-fakturering-funksjonen" er det generelle navnet på ressursen som er konfigurert og publisert til å bruke serveren for tillegget Elektronisk fakturering. Oppsettet av funksjonen for E-fakturering kombinerer, blant annet, bruken av konfigurasjonsformater for Elektronisk rapportering (ER) for å opprette konfigurerbare eksport- og importfiler, og bruken av handlinger og handlingsflyt for å gjøre det mulig å opprette konfigurerbare regler for å sende forespørsler, importere svar og analysere svarinnholdet.

På grunn av variasjoner i fakturaformater og handlingsflyter er oppsettet for e-postfakturaen land/område-avhengig.

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Konfigurere integrasjon av tillegget Elektronisk fakturering i Finance eller Supply Chain Management 

I dette oppsettet skal du utføre følgende oppgaver:

1. Åpne ny funksjon som er gjort tilgjengelig
2. Slå på funksjonen for integrering av tillegget Elektronisk fakturering for å aktivere integrasjon med Finance.
3. Konfigurer URLen for endepunktet for tillegget Elektronisk fakturering.
4. Importer ER-konfigurasjonene som er knyttet til den land/område-spesifikke e-faktureringsfunksjonen.
5. Aktiver den aktuelle land/område-spesifikke funksjonen for e-fakturering.
6. Importer ER-konfigurasjonene og konfigurer svartypene som kreves for å oppdatere det land/område-spesifikke fakturadokumentet som et resultat av sendingsprosessen.

### <a name="open-flighted-feature"></a>Åpne ny funksjon som er gjort tilgjengelig
Funksjonen for integrasjon av elektronisk faktura aktiveres via testversjonering. Testversjonering er et konsept som gjør at en funksjon kan være PÅ eller AV som standard. Fremgangsmåten nedenfor aktiverer en testversjonering i et ikke-produksjonsmiljø. 

1. Utfør følgende SQL-kommando:

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)
    
2. Etter at du har gjort endringene ovenfor, utfører du en IISReset på alle AOSer

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Aktivere funksjonen for integrering av tillegget Elektronisk fakturering

1. Logg på Finance eller Supply Chain Management.
2. I arbeidsområdet **Funksjonsbehandling** søker du etter den nye funksjonen, **Konfigurerbar integrasjon for tillegget Elektronisk fakturering**. Hvis funksjonen fremdeles ikke vises på siden for Funksjonsbehandling, kjører du funksjonen **Se etter oppdateringer**
3. Velg funksjonen, og velg deretter **Aktiver nå**.

### <a name="set-up-the-service-endpoint-url"></a>Konfigurer URL-adressen for endepunkt for tjeneste

1. Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.
2. I kategorien for **Innsendingstjeneste** i feltet for **URL for endepunkt for tjeneste** angir du `https://businessdocumentsubmission.us.operations365.dynamics.com/`.
3. I **Miljø**-feltet angir du navnet på miljøet for tillegget Elektronisk fakturering som du opprettet under RCS-oppsettet.

![Angi serviceparametere](media/e-invoicing-services-get-started-enter-service-endpoint.png)

### <a name="import-the-er-configurations"></a>Importere ER-konfigurasjonene

Hvis du vil aktivere forretningsdata som skal samles inn og sendes til tillegget Elektroniske fakturering, må du importere ER-datamodellen og ER-datamodellkonfigurasjonen som relatert til den land/område-spesifikke e-postfaktureringsfunksjonen du vil bruke.

1. I delen **Konfigurasjonsleverandører** i arbeidsområdet **Elektronisk rapportering** velger du flisen **Microsoft**. Kontroller at konfigurasjonsleverandøren er satt til **Aktiv**. Hvis du ha mer informasjon om hvordan du setter en leverandør til **Aktiv**, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Velg **Repositorier**.
4. Velg **Global ressurs**, og velg deretter **Åpne**.
5. I dialogboksen **Koble til Lifecycle Services** velger du **Klikk her for å koble til Lifecycle Service**.
6. Avhengig av landet eller regionen der du vil bruke e-faktureringsfunksjonen, må du importere den gjeldende datamodellen, datamodelltilordningen og formatene. Hvis du vil ha mer informasjon om ER-konfigurasjonene du bør importere, se emnet det land/område-spesifikke emnet Komme i gang med tillegget Elektronisk fakturering.
7. Importer **kontekstmodell for kundefaktura**. Denne modellen inneholder tilleggsparametere som beskriver, blant annet, miljøet i Finance som brukes for tillegget Elektronisk fakturering under sending av forretningsdata.

### <a name="turn-on-countryregion-specific-e-invoicing-features"></a><a name="region-specific"></a>Aktivere land/område-spesifikke funksjoner for e-fakturering

Hvis du vil aktivere land/område-spesifikke funksjoner for e-fakturering, slik at de fungerer med tillegget Elektronisk fakturering, må du aktivere funksjonen i hver juridiske enhet der du vil bruke den. Etterpå kan ikke den gamle integrasjonen for elektronisk fakturering lenger brukes, og integreringen med det nye tillegget Elektronisk fakturering slås på.

1. Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.
2. I kategorien **Funksjoner**, i raden for funksjonen som er knyttet til din land/område-spesifikke e-postfaktureringsfunksjon, merker du av i **Aktivert**-kolonnen. Hvis du vil ha mer informasjon om hvilken funksjon du må slå på, se det land/område-spesifikke emnet Komme i gang med tillegget Elektronisk fakturering.

![Aktivere funksjonen for e-fakturering](media/e-invoicing-services-get-started-enable-invoicing-feature.png)

> [!NOTE]
> Hvis du har flere juridiske enheter som er konfigurert for forskjellige land eller regioner, kan du aktivere funksjonen for land/område-spesifikk e-postfakturering for hver juridiske enhet.

### <a name="import-er-configurations-and-set-up-the-response-types-to-update-your-countryregion-specific-invoice-document"></a>Importere ER konfigurasjoner og definere svartypene for å oppdatere det land/område-spesifikke fakturadokumentet

Hvis det sendte fakturadokumentet krever en oppdatering etter svaret på innsendingen til de myndighetsgodkjente tjenestene, må du importere en spesiell ER-datamodell og konfigurasjoner for å aktivere statusen for fakturadokumentet eller andre felt som skal oppdateres.

1. I delen **Konfigurasjonsleverandører** i arbeidsområdet **Elektronisk rapportering** velger du flisen **Microsoft**.
2. Velg **Repositorier**.
3. Velg **Global ressurs**, og velg deretter **Åpne**.
4. Importer **Svarmeldingsmodell**, **Format for import av svarmelding**, **Tilknytning av svarmeldingsmodell til mål** og **Format for import av filinnhold**.
5. Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.
6. I kategorien **Elektronisk dokument** velger du **Legg til** for å angi navnet på tabellen som er relatert til ditt land/område-spesifikke fakturadokument. Hvis du vil ha mer informasjon om hvilke tabellnavn du bør velge, kan du se det land/område-spesifikke emnet Komme i gang med tillegget Elektronisk fakturering.
7. Velg **Svartyper** for å konfigurere svartypen. Hvis du vil ha mer informasjon om hvilke tabellnavn du bør velge, kan du se det land/område-spesifikke emnet Komme i gang med tillegget Elektronisk fakturering.

![Konfigurere svartyper](media/e-invoicing-services-get-started-set-up-response-types.png)

## <a name="e-invoicing-feature-names-by-country"></a>E-fakturafunksjonsnavn etter land 
Følgende tabell beskriver andre e-fakturafunksjoner som er tilgjengelige for nedlasting fra det globale repositoriet for elektronisk rapportering for å generere elektroniske fakturaer.
I RCS kan du laste ned funksjonene for e-fakturering som er oppført i denne tabellen, ER-konfigurasjonene og de tilgjengelige oppsettene for e-fakturafunksjoner.
I Finance kan du aktivere tilknyttede funksjonsreferanser på siden for **parametere for elektronisk dokument** for å utstede elektroniske fakturaer for disse landene. Hvis du vil ha mer informasjon, kan du se delen [Aktivere land/område-spesifikke funksjoner for e-fakturering](#region-specific) tidligere i dette emnet.

| Funksjonsnavn                      | Beskrivelse                                 | ER-konfigurasjoner                                                                                                  | Oppsett                                                                                                                                                         | Land/område  | Funksjonsreferanse      |
|-----------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|------------------------|
| Østerrikske elektroniske fakturaer (AT) | Salgs- og prosjektfakturaer for Østerrike      | - OIOUBL Salgsfaktura <br>- OIOUBL Prosjektfaktura <br>- OIOUBL Salgskreditnota <br>- OIOUBL Prosjektkreditnota | - Salgsfakturagenerering (AT) <br>- Prosjektfakturagenerering (AT) <br>- Salgskreditnotagenerering (AT) <br>- Prosjektkreditnotagenerering (AT)         | Østerrike         | EUR-00023              |
| Belgisk elektronisk faktura (BE)   | Salgs- og prosjektfakturaer for Belgia      | - UBL salgsfaktura BE <br>- UBL prosjektfaktura BE <br>- UBL prosjektkreditnota BE <br>- UBL salgskreditnota BE | - Salgsfakturagenerering (BE)<br>- Prosjektfakturagenerering (BE) <br>- Salgskreditnotagenerering (BE) <br>- Prosjektkreditnotagenerering (BE)         | Belgia         | EUR-00023              |
| Dansk elektronisk faktura (DK)    | Salgs- og prosjektfakturaer for Danmark      | - OIOUBL Salgsfaktura <br>- OIOUBL Prosjektfaktura <br>- OIOUBL Salgskreditnota <br>- OIOUBL Prosjektkreditnota | - Salgsfakturagenerering (DK) <br>- Prosjektfakturagenerering (DK) <br>- Salgskreditnotagenerering (DK)<br>- Prosjektkreditnotagenerering (DK)         | Danmark         | EUR-00023<br> DK-00001 |
| Nederlandsk elektronisk faktura (NL)     | Salgs- og prosjektfakturaer for Nederland  | - UBL salgsfaktura NL <br>- UBL prosjektfaktura NL <br>- UBL salgskreditnota NL <br>- UBL prosjektkreditnota NL | - Salgsfakturagenerering (NL) <br> - Prosjektfakturagenerering (NL) <br> - Salgskreditnotagenerering (NL) <br>- Prosjektkreditnotagenerering (NL)          | Nederland | EUR-00023              |
| Estisk elektronisk faktura (EE)  | Salgs- og prosjektfakturaer for Estland      | - Salgsfaktura (EE) <br> - Prosjektfaktura (EE)                                                                     | - Salgsfakturagenerering (EE) <br>- Prosjektfakturagenerering (EE)                                                                                           | Estland         | EUR-00023              |
| Finsk elektronisk faktura (FI)   | Salgs- og prosjektfakturaer for Finland      | - Salgsfaktura (FI) <br>- Prosjektfakturagenerering (FI)                                                          | - Salgsfakturagenerering (FI) <br>- Prosjektfakturagenerering (FI)                                                                                           | Finland         | EUR-00023              |
| Fransk elektronisk faktura (FR)    | Salgs- og prosjektfakturaer for Frankrike    | - UBL salgsfaktura FR <br> - UBL prosjektfaktura FR <br> - UBL salgskreditnota FR <br>- UBL prosjektkreditnota FR | - Salgsfakturagenerering (FR) <br> - Prosjektfakturagenerering (FR) <br>- Salgskreditnotagenerering (FR) <br>- Prosjektkreditnotagenerering (FR)         | Frankrike          | EUR-00023              |
| Tysk elektronisk faktura (DE)    | Salgs- og prosjektfakturaer for Tyskland      |- Salgsfaktura (DE) <br> - Prosjektfaktura <DE>                                                                     | - Salgsfakturagenerering (DE) <br>- Prosjektfakturagenerering (DE)                                                                                           | Tyskland         | EUR-00023              |
| Norsk elektronisk faktura (NO) | Salgs- og prosjektfakturaer for Norge       | - OIOUBL Salgsfaktura <br>- OIOUBL Prosjektfaktura <br>- OIOUBL Salgskreditnota <br>- OIOUBL Prosjektkreditnota | - Salgsfakturagenerering (NO) <br>- Prosjektfakturagenerering (NO) <br>- Salgskreditnotagenerering (NO) <br>- Prosjektkreditnotagenerering (NO)          | Norge          | EUR-00023<br> NO-00010 |
| Spansk elektronisk faktura (ES)   | Salgs- og prosjektfakturaer for Spania        | - Salgsfaktura (ES) <br>- Prosjektfaktura (ES)                                                                     | - Salgsfakturagenerering (ES) <br>- Prosjektfakturagenerering (ES)                                                                                           | Spania           | EUR-00023 <br>ES-00025 |
| Italiensk elektronisk faktura (IT)   | Salgs- og prosjektfakturaer for Italia        | - (Forhåndsversjon) Salgsfaktura (IT) <br> - Prosjektfaktura (IT)                                                           | - Salgsfaktura <br> - Prosjektfaktura                                                                                                                           | Italia           | EUR-00023 <br>IT-00036 |
| Elektronisk faktura i PEPPOL-format         | PEPPOL Salgs- og prosjektfakturagenerering | - PEPPOL-salgsfaktura <br>- PEPPOL-prosjektfaktura <br>- PEPPOL-salgskreditnota <br> - PEPPOL-prosjektkreditnota | - PEPPOL-salgsfakturagenerering <br>- PEPPOL-prosjektfakturagenerering <br>- PEPPOL-salgskreditnotagenerering <br>- PEPPOL-prosjektkreditnotagenerering |                 | EUR-00023              |


## <a name="electronic-invoice-processing-in-finance-and-supply-chain-management"></a>Elektronisk fakturabehandling i Finance og Supply Chain Management

Under behandlingen vil du fullføre disse oppgavene:

1. Send et forretningsdokument (faktura) via tillegget Elektronisk fakturering.
2. Vis utførelsesloggene for sending.

### <a name="submit-business-documents"></a>Send forretningsdokumenter

Under den vanlige innsendingsprosessen er kommunikasjon mellom klienten og tillegget Elektronisk fakturering toveis. Formålet er å utføre to hovedoppgaver under sending av elektroniske dokumenter:

1. Send alle elektroniske dokumenter som venter på sending fra Finance, og som har riktig status for innsending og oppfyller utvalgskriteriene.
2. Importere, til Finance, svaret som tillegget Elektronisk fakturering returnerer for tidligere sendte elektroniske dokumenter. Etter importen blir svarene analysert, og statusen for forretningsdokumentene oppdateres i henhold til dette.

Du kan sende forretningsdokumenter enten manuelt eller basert på dine tidsplanbehov.

1. Gå til **Organisasjonsstyring \> Periodiske \> Elektroniske dokumenter \> Send elektroniske dokumenter**.
2. For første innsending av et dokument må du alltid sette alternativet **Send dokumenter på nytt** til **Nei**. Hvis du må sende et dokument på nytt via tjenesten, setter du dette alternativet til **Ja**.
3. I hurtigfanen **Poster som skal inkluderes** velger du **Filter** for å åpne **Forespørsel**-dialogboksen, der du kan bygge en spørring for å velge dokumenter for innsending.

![Dialogboksen Send elektroniske dokumenter](media/e-invoicing-services-get-started-submission-form.png)

### <a name="filter-query"></a>Filterspørring

1. I dialogboksen **Forespørsel** i kategorien **Område** angir du filterkriterier ved hjelp av feltene **Tabell**, **Avledet tabell**, **Felt** og **Vilkår**.
2. Velg **Legg til** for å legge til så mange tilleggskriterier du trenger for å velge forretningsdokumentene.

    ![Definere filterkriterier for sending](media/e-invoicing-services-get-started-set-up-submission-filter-criteria.png)

3. Velg **OK** for å lukke dialogboksen **Forespørsel**.
4. Velg **OK** for å sende de valgte forretningsdokumentene til tillegget Elektronisk fakturering.

    > [!NOTE]
    > Under det første forsøket på å sende et dokument via tjenesten, blir du bedt om å bekrefte tilkoblingen til tillegget Elektronisk fakturering. Velg **Klikk her for å koble til innsendingstjeneste for elektronisk dokument**.
    >
    > ![Koble til meldingsboksen for innsendingstjeneste for elektronisk dokument](media/e-invoicing-services-get-started-dialog-form-connect-e-Invoicing-services.png)
    >
    > Hvis tilkoblingen er vellykket, får du en bekreftelsesmelding.
    >
    > ![Bekreft tilkobling til tillegget Elektronisk fakturering](media/e-invoicing-services-get-started-confirmation-connection-e-invoicing-services.png)

5. Lukk dialogboksen.

> [!NOTE]
> Etter hver innsending viser handlingssenteret antallet sendte dokumenter.
>
> ![Handlingssentermeldinger](media/e-invoicing-services-get-started-view-action-center-messages.png)

### <a name="submission-by-batch"></a>Innsending etter parti

I stedet for å sende dokumenter manuelt, kan du automatisere sendingsprosessen og kjøre den i bakgrunnen, basert på en konfigurert frekvens for satsvis utførelse.

1. I dialogboksen **Send elektroniske dokumenter** i hurtigfanen **Kjør i bakgrunnen** setter du alternativet for **Satsvis behandling** til **Ja**.
2. I kategorien **Regelmessighet** konfigurerer du frekvensen for satsvis behandling.

![Definere innsending etter parti](media/e-invoicing-services-get-started-set-up-submission-batch.png)

### <a name="view-all-submission-logs"></a>Vise alle sendelogger

1. Gå til **Organisasjonsstyring \> Periodisk \> Elektroniske dokumenter \> sendingslogg for elektronisk dokument**.
2. I feltet **Dokumenttype** velger du dokumenttypen det skal filtreres etter.

    ![Velge dokumenttypen som det skal vises sendelogger for](media/e-invoicing-services-get-started-select-document-type-for-viewing-submission-log.png)

    > [!IMPORTANT]
    > Verdien som vises i kolonnen **Status for sending**, representerer statusen som er relatert til fullføringen av innsendingsprosessen. Den viser om flyten av handlinger som er konfigurert i RCS, ble kjørt til slutten, uansett om det elektroniske dokumentet ble godkjent eller avvist. Verdien i kolonnen for **innsendingsstatus** representerer ikke statusen til det sendte dokumentet. Du kan vise statusen til det sendte dokumentet (det vil si om dokumentet ble godkjent eller avvist) på hurtigfanen for **handlingslogg for behandling** i detaljene for sendingsloggen, som beskrevet nedenfor.

3. Velg **Forespørsler \> Innsendingsdetaljer** i handlingsruten.
4. Vis detaljene for innsendingsloggen.

    ![Detaljer for innsendingsloggen](media/e-invoicing-services-get-started-view-submission-log-form.png)

Resultatene som vises i innsendingsloggen, avhenger av hvordan funksjonen for e-fakturering ble konfigurert i RCS. Men uavhengig av oppsettet, har sendingsloggen alltid tre hurtigfaner:

- **Behandlingshandlinger** – Denne hurtigfanen viser utførelsesloggen for handlingene som er konfigurert i funksjonsversjonen som er definert i RCS. **Status**-kolonnen viser om handlingen ble kjørt uten feil.
- **Handlingsfiler** – Denne hurtigfanen viser de mellomliggende filene som ble generert under utføring av handlingene. Du kan velge **Vis** for å laste ned filen og vise innholdet.
- **Handlingslogg for behandling** – Denne hurtigfanen viser resultatet av kommunikasjonen mellom tillegget Elektronisk fakturering og målwebtjenesten. Den viser også hva som ble returnert av webtjenestebehandlingen.

## <a name="related-topics"></a>Relaterte emner

- [Oversikt over tillegget Elektronisk fakturering](e-invoicing-service-overview.md)
- [Komme i gang med tillegget Elektronisk fakturering for Brasil](e-invoicing-bra-get-started.md)
- [Komme i gang med tillegget Elektronisk fakturering for Mexico](e-invoicing-mex-get-started.md)
- [Komme i gang med tillegget Elektronisk fakturering for Italia](e-invoicing-ita-get-started.md)
- [Konfigurere tillegget Elektronisk fakturering](e-invoicing-setup.md)
