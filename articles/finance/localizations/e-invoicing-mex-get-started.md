---
title: Komme i gang med tillegget Elektronisk fakturering for Mexico
description: Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med tillegget Elektronisk fakturering for Mexico i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
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
ms.openlocfilehash: d719c3ba68458130d415c50319fdcdeafcfc783e
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2020
ms.locfileid: "3836009"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-mexico"></a>Komme i gang med tillegget Elektronisk fakturering for Mexico

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Det kan hende at tillegget Elektronisk fakturering for Mexico ikke støtter alle funksjonene som er tilgjengelige i CFDI-dokumentet (Comprobante Fiscal Digital por Internet) og i den relaterte integrasjonen som er innebygd i Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management.

Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med tillegget Elektronisk fakturering for Mexico. Det leder deg gjennom konfigurasjonstrinnene som er landsavhengige i Regulatory Configuration Services (RCS) og Finance. Den leder deg også gjennom trinnene du må følge i Finance for å sende CFDI-fakturaer gjennom tjenesten, og forklarer hvordan du gjennomgår behandlingsresultatene og statusen for CFDI-fakturaer.

## <a name="prerequisites"></a>Forutsetninger

Før du fullfører trinnene i dette emnet må du fullføre trinnene i [Komme i gang med tillegget Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>RCS-oppsett

Under RCS-oppsettet vil du fullføre disse oppgavene:

1. Importer funksjonen for e-fakturering for behandling av CFDI-fakturaer.
2. Gå gjennom formatkonfigurasjonene som kreves for å generere, sende og motta svar om CFDI-fakturaer, og for å sende og motta svar om annullering.
3. Konfigurer hendelsene som støtter innsendingsscenarioene for CFDI-faktura.
4. Publiser funksjonen for e-fakturering for CFDI-fakturaer.

> [!NOTE]
> "E-fakturering-funksjonen" er det generelle navnet på ressursen som er konfigurert og publisert til å bruke serveren for tillegget Elektronisk fakturering. I dette tilfellet er CFDI-fakturaer (MX) e-faktureringsfunksjonen du vil definere.

## <a name="import-the-e-invoicing-feature"></a>Importere funksjonen for e-fakturering

1. Logg på RCS-kontoen.
2. I **Globaliseringsfunksjoner**-arbeidsområder i delen **Funksjoner**, velger du flisen **E-fakturering**.
3. På siden **E-faktureringsfunksjoner** velger du **Importer** for å importere **CFDI-fakturaer (MX)** fra det globale repositoriet.

    > [!NOTE]
    > Hvis du ikke ser funksjonen i listen, velger du **Synkroniser**, og deretter gjentar du trinn 3.

![Importere funksjonen for CFDI-fakturaer (MX)](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

Når du importerer funksjonen for **CFDI-fakturaer (MX)** fra det globale repositoriet, importeres alle funksjonsinnstillinger, inkludert konfigurasjoner og handlinger.

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a>Opprette en ny versjon av funksjonen CFDI-fakturaer (MX)

Du kan opprette en ny versjon hvis for eksempel URL-adresser må oppdateres. Hvis du vil ha mer informasjon, se [E-fakturering av CFDI](tasks/mx-00010-e-invoicing-cfdi.md).

- På siden for **E-faktureringsfunksjoner**, i kategorien **Versjoner**, velger du **Ny**.

![Legge til en ny versjon av e-fakturafunksjonen](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a>Oppdatere konfigurasjonsversjonen

1. På siden **E-faktureringsfunksjoner**, i kategorien **Konfigurasjoner**, velger du **Legg til** eller **Slett** for å behandle konfigurasjonsversjonene (ER-filformatkonfigurasjoner).

    ![Behandle konfigurasjoner for e-faktureringsfunksjon](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    Når du oppretter en ny versjon, arves alle konfigurasjoner fra den siste publiserte versjonen. Hvis du skal behandle CFDI-fakturaer, kreves følgende konfigurasjoner:

    - CFDI-faktura (BusinessDocumentService)
    - Import av CFDI-svarmelding
    - Import av CFDI-feillogg
    - CFDI-avbruddsforespørsel (MX) (BusinessDocumentService)
    - CFDI-faktura (BusinessDocumentService)

2. Velg en konfigurasjonsversjon fra listen, og velg deretter **Rediger** eller **Vis** for å åpne siden **Formatutforming**, der du kan redigere eller vise konfigurasjonen.

    ![Åpne Formatutforming-siden](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. Bruk siden **Formatutforming** til å redigere og vise ER-formatfilkonfigurasjoner. Hvis du vil ha mer informasjon, kan du se [Opprette konfigurasjoner for elektronisk dokument](../../dev-itpro/analytics/electronic-reporting-configuration.md).

    ![Formatutformingsside](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>Administrere oppsett for e-faktureringsfunksjonen

- På siden for **E-postfunksjoner**, i kategorien **Oppsett**, velger du **Legg til**, **Slett** eller **Rediger** for å behandle e-faktureringsoppsettene.

![Administrere oppsett for e-faktureringsfunksjonen](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

Hvis du vil sende CFDI-fakturaer for autorisasjon (generere XML-filen, sende XML-filen og behandle svaret), kreves funksjonsoppsettet **Salgsfaktura**.

Hvis du vil sende CFDI-fakturaannullering, kreves funksjonsoppsett for **Annullering** og **Avbryt**.

### <a name="configure-the-sales-invoice-feature-setup"></a>Konfigurere oppsettet av salgsfakturafunksjonen

1. På siden for **e-fakturafunksjoner**, i kategorien **Oppsett** i kolonnen **Funksjonsoppsett**, velger du **Salgsfaktura**.
2. Velg **Rediger** for å konfigurere handlinger, relevansregler og variabler.

    ![Redigere oppsettet for e-postfakturafunksjonen](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. På siden for **oppsett av funksjonsversjon** velger du kategorien **Handlinger** for å behandle listen over handlinger. Handlinger definerer en liste over operasjoner som må kjøres i sekvensiell rekkefølge for å oppnå full utførelse av hendelsen.

    ![Kategorien Handlinger](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | Handlings-ID | Handling                   | Handlingsnavn                                  | Handlingsbeskrivelse                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | 1         | Transformere dokument       | Generere CFDI-e-faktura uten digital signatur | Generer CFDI-e-fakturaen.                                |
    | 2         | Signer dokument            | Digital signatur                                 | Signer e-fakturaen digitalt for innsending.                |
    | 3         | Kalle opp meksikansk PAC-tjeneste | Sende CFDI -e-faktura                        | Windows Communication Foundation (WCF)-klienten sender CFDI-e-faktura. |
    | 4         | Behandle svar         | Analysere webtjenestesvar                 | Analyser webtjenestesvaret, og returner feilloggen. |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a>Konfigurere URL-adressen for meksikanske PAC-webtjenester 

1. På siden for **funksjonsversjonsoppsett**, i kategorien **Handlinger** i hurtigkategorien **Handlinger**, velger du **Kalle opp meksikansk PAC-tjeneste**.
2. I hurtigkategorien **Parametere** i feltet **URL-adresse**, angir du URL-adressen til webtjenesten for CFDI-fakturainnsending.

> [!NOTE]
> Bruk de samme trinnene til å oppdatere URL-adressen for handlingen **Kalle opp meksikansk PAC-tjeneste** for funksjonsoppsettet for **Avbryt** og **Annulleringsforespørsel**.

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a>Tilordne kladdeversjonen til et e-faktureringsmiljø

1. På siden for **E-faktureringsfunksjoner**, i kategorien **Miljøer**, velger du **Aktiver**.
2. I feltet **Miljø** velger du miljøet.
3. I **Gyldig fra**-feltet angir du datoen for når miljøet skal tre i kraft.
3. Velg **Aktiver**.

![Aktivere et e-faktureringsmiljø](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a>Endre versjonsstatusen til Fullført

1. På siden for **e-fakturafunksjoner** i kategorien **Versjoner** velger du versjonen av e-fakturafunksjonen med statusen **Utkast**.
2. Velg **Endre status \> Fullført**.

## <a name="change-the-version-status-to-published"></a>Endre versjonsstatusen til Publisert

- På siden **E-faktureringsfunksjoner**, i kategorien **Versjoner**, velger du **Endre status \> Publiser**.

## <a name="publish-the-e-invoicing-feature"></a>Publisere funksjonen for e-fakturering

1. På siden **E-faktureringsfunksjoner** velger du kategorien **Versjoner** for å administrere statusen for funksjonen **CFDI-fakturaer (MX)**.
2. Velg **Endre status** for å endre statusen for funksjonen.

![Endre statusen for e-fakturafunksjonen](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance"></a>Konfigurere integrasjon av tillegget Elektronisk fakturering i Finance

Hvis du vil definere tillegget Elektronisk fakturering i Finance, må du fullføre disse oppgavene:

1. Importer ER-datamodellen, ER-datamodelltilordningen og formatene som kreves for CFDI-fakturaer.
2. Konfigurer svartyper for oppdatering av CFDI-fakturaer. Disse svartypene brukes til svaret fra PAC-serveren (autorisert sertifiseringstjeneste).

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a>Importere ER-datamodellen, ER-datamodelltilordning og kontekstkonfigurasjoner for CFDI-fakturaer

1. Logg på Finance.
2. I delen **Konfigurasjonsleverandører** i arbeidsområdet **Elektronisk rapportering** velger du tittelen **Microsoft**. Kontroller at konfigurasjonsleverandøren er satt til **Aktiv**. Hvis du ha mer informasjon om hvordan du setter en leverandør til **Aktiv**, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Velg **Repositorier**.
4. Velg **Global ressurs \> Åpne**.
5. Importer **Fakturamodell**, **Fakturamodelltilordning**, **CFDI-fakturaformat (MX)**, **CFDI-fakturaannulleringsforespørselsformat (MX)** og **CFDI-fakturaavbruddsformat (MX)**.

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a>Aktivere funksjonen for behandling av CFDI-fakturaer

1. Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.
2. I kategorien **Funksjoner** merker du av for **Aktiver** i radene for funksjonsreferanser **MX-00010** og **MX-00016**.

![Aktivere funksjonene for behandling av CFDI-fakturaer](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a>Importere ER-konfigurasjoner og konfigurere svartypene for oppdatering av CFDI-fakturaer

#### <a name="import-er-configurations"></a>Importere ER-konfigurasjoner

1. I delen **Konfigurasjonsleverandører** i arbeidsområdet **Elektronisk rapportering** velger du tittelen **Microsoft**.
3. Velg **Repositorier**.
4. Velg **Global ressurs \> Åpne**.
5. Importer **svarmeldingsmodell**, **import av CFDI-feillogg (MX)**, **import av CFDI-feillogg (MX)** og **import av CFD-svarmelding (MX)**.

#### <a name="set-up-the-response-types"></a>Definere svartypene

1. Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.
2. I kategorien **Elektronisk dokument** velger du **Legg til**.
3. Angi kundefakturajournalen, og deretter, i feltet **Tabellnavn**, velger du prosjektfakturaen.
4. For hver tabell definerer du en relatert dokumentkontekst:

    - For **Kundefakturajournal** angir du **kundefakturakontekst**.
    - I **Prosjektfaktura** angir du **prosjektfakturakontekst**.

4. Velg **Svartyper** for å konfigurere svartypene som kan returneres fra tillegget Elektronisk fakturering og inkluderes i en kundefakturajournal eller prosjektfaktura.
5. Velg **Ny**, og deretter, i **Svartype**-feltet, velg **Svar**.
6. I feltet for **innsendingsstatus** velger du **Venter**.
7. I feltet **Modelltilordning** velg **svarmeldingsimportformat – modelltilordning fra svarmelding**.
8. Velg **Lagre**.
9. Velg **Ny**, og deretter, i **Svartype**-feltet, velg **ResponseData**.
10. I feltet for **innsendingsstatus** velger du **Venter**.
11. I **Modelltilordning**-feltet velger du **Format for dataimport av CFDI-svar (detaljer) – dataimport av svar**.
12. Velg **Lagre**.

## <a name="process-electronic-invoices-in-finance"></a>Behandle elektroniske fakturaer i Finance 

Under behandlingen av CFDI-fakturaer i Finance via tillegget Elektronisk fakturering kan du utføre følgende oppgaver:

- Sende CFDI-fakturaer.
- Vis utførelsesloggene for sending.
- Send annullering for en CFDI-faktura.

### <a name="submit-cfdi-invoices"></a>Sende CFDI-fakturaer

Når du har aktivert funksjonen for **Konfigurerbar integrasjon av tillegget Elektronisk fakturering**, kan ikke prosessen for **eksport/import av elektronisk faktura** (**Kunder \> Fakturaer \> E-fakturaer**) for sending av CFDI-fakturaer brukes lenger. Den erstattes av en ny prosess som kalles **Send elektroniske dokumenter**.

> [!NOTE]
> Før du bruker den nye prosessen **Send elektroniske dokumenter**, må du kontrollere at oppsettet som kreves for meksikanske e-fakturaer, ble fullført. Hvis du vil ha mer informasjon, se [CFDI-oppsettversjon 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).

1. Gå til **Organisasjonsstyring \> Periodiske \> Elektroniske dokumenter \> Send elektroniske dokumenter**.
2. For første innsending av et dokument må du alltid sette alternativet **Send dokumenter på nytt** til **Nei**. Hvis du må sende et dokument på nytt via tjenesten, setter du dette alternativet til **Ja**.
3. I hurtigfanen **Poster som skal inkluderes** velger du **Filter** for å åpne **Forespørsel**-dialogboksen, der du kan bygge en spørring for å velge dokumenter for innsending.

![Sende et CFDI-dokument](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> Under det første forsøket på å sende et dokument via tjenesten, blir du bedt om å bekrefte tilkoblingen til tillegget Elektronisk fakturering. Velg **Klikk her for å koble til innsendingstjeneste for elektronisk dokument**.

### <a name="view-submission-logs"></a>Vise sendelogger

Du kan vise sendeloggene for alle sendte dokumenter eller bare for ett sendt dokument.

#### <a name="view-all-submission-logs"></a>Vise alle sendelogger

Når du har aktivert funksjonen **Konfigurerbar integrasjon av tillegget Elektronisk fakturering**, er en ny side tilgjengelig der du kan følge opp dokumentsendingsprosessen. Du kan bruke denne siden til å vise sendelogger for alle sendte dokumenter.

1. Gå til **Organisasjonsstyring \> Periodisk \> Elektroniske dokumenter \> sendingslogg for elektronisk dokument**.
2. I feltet **Dokumenttype** velger du **Kundefakturajournal** for å filtrere etter de påkrevde elektroniske dokumentene.

    ![Velge en dokumenttype for å vise sendelogger](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. I handlingsruten velger du **Forespørsler \> Innsendingsdetaljer** for å vise detaljene for sendeutførelsesloggene.

    ![Vise detaljene for innsendingsloggen](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

Informasjonen i sendeloggene deles mellom tre hurtigfaner:

- **Behandlingshandlinger** – Denne hurtigfanen viser utførelsesloggen for handlingene som er konfigurert i funksjonsversjonen som er definert i RCS. **Status**-kolonnen viser om handlingen ble kjørt uten feil.
- **Handlingsfiler** – Denne hurtigfanen viser de mellomliggende filene som ble generert under utføring av handlingene. Du kan velge **Vis** for å laste ned filen og vise filen.
- **Handlingslogg for behandling** – Denne hurtigfanen viser resultatet av kommunikasjonen mellom tillegget Elektronisk fakturering og målwebtjenesten. Den viser også hva som ble returnert av behandlingen fra webtjenesten. Kolonnen **Feilkode** viser returkoden som ble returnert av webtjenesten for godkjenning.

Når den sendte CFDI-fakturaen godkjennes, oppdateres statusen til **Godkjent**.

#### <a name="view-submission-logs-from-cfdi-invoices"></a>Vise sendelogger fra CFDI-fakturaer

Når du har aktivert funksjonen for **Konfigurerbar integrasjon av tillegget Elektronisk fakturering**, kan du også vise sendingsloggene fra CFDI-fakturaer.

1. Gå til **Kunder \> Forespørsler og rapporter \> CFDI (elektroniske fakturaer)**.
2. Velg en CFDI-faktura som ble sendt etter at funksjonen for **Konfigurerbar integrasjon av tillegget Elektronisk fakturering** er aktivert.
3. Velg **logg for elektronisk dokument** i kategorien **Logg** i handlingsruten.

![Vise sendelogger fra CFDI-fakturaer](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> For CFDI-fakturaer som ble sendt før funksjonen for **Konfigurerbar integrasjon av tillegget Elektronisk fakturering** var aktivert, er **Logg**-knappen tilgjengelig. **Logg**-knappen ikke tilgjengelig for CFDI-fakturaer som ble sendt etter funksjonen for **Konfigurerbar integrasjon for tillegget Elektronisk fakturering** var aktivert.

### <a name="submit-cancellation-of-cfdi-invoices"></a>Sende annullering for CFDI-fakturaer

Når du har aktivert funksjonen for **Konfigurerbar integrasjon av tillegget Elektronisk fakturering**, kan ikke lenger den gamle prosessen for avbryting av CFDI-fakturaer brukes. Den erstattes av en ny avlysningsprosess som er innebygd på siden for **sendingslogg for elektronisk dokument**.

1. Gå til **Kunder \> Forespørsler og rapporter \> CFDI (elektroniske fakturaer)**.
2. Hvis CFDI-fakturaen har statusen **Godkjent**, velger du **Funksjoner \> Avbryt CFDI**.
3. Gå til **Organisasjonsstyring \> Periodisk \> Elektroniske dokumenter \> sendingslogg for elektronisk dokument**.
4. Velg CFDI-fakturaen, og velg deretter **Funksjoner \> Send relaterte innsendinger**.
5. Angi en beskrivelse for den tilknyttede sendingen, og velg deretter **OK**.

#### <a name="view-cancellation-submission-logs"></a>Vise sendelogger for annullering

1. Gå til **Organisasjonsstyring \> Periodisk \> Elektroniske dokumenter \> sendingslogg for elektronisk dokument**.
2. I feltet **Dokumenttype** velger du **Kundefakturajournal** for å filtrere etter bare kundefakturajournaldokumenter.
3. Velg CFDI-fakturaen, og velg deretter **Forespørsler \> Relatert sending** i handlingsruten.

    Siden **Relatert innsendinger** viser alle tilknyttede innsendinger, og sendestatusen, for en gitt CFDI-faktura. I illustrasjonen nedenfor representerer den første linjen innsendingen som ber om godkjenning av CFDI-fakturaen. Den andre linjen representerer innsendingen som avbrøt CFDI-fakturaen.

    ![Vise sendeloggene for annullering](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. I handlingsruten velger du **Forespørsler \> Innsendingsdetaljer** for å vise detaljene for sendeutførelsesloggene.

    ![Vise detaljer for sendeloggen for annullering](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a>Personvernerklæring
Hvis du aktiverer funksjonene MX-00010 og MX-00016 (CFDI-faktura og CFDI-annullering), kan det kreve sending av begrensede data, som inkluderer avgiftsregistrerings-IDen for organisasjonen. Dette overføres til tredjepartsleverandører autorisert av skattemyndigheten for å sende elektroniske fakturaer til skattemyndighetene i det forhåndsdefinerte formatet som kreves for integrering med myndighetenes webtjeneste. En administrator kan aktivere og deaktivere funksjonene MX-00010 og MX-00016 (CFDI-faktura og CFDI-annullering) ved å navigere til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**. Velg kategorien **Funksjoner**, velg radene som inneholder MX-00010- og MX-00016-funksjoner, og velg deretter riktig valg. Data som er importert fra disse eksterne systemene til denne Dynamics 365-elektroniske tjenesten, er underlagt vår [personvernerklæring](https://go.microsoft.com/fwlink/?LinkId=512132). Hvis du vil ha mer informasjon, kan du se delene om personvernerklæring i dokumentasjon for landspesifikke funksjoner.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over tillegget Elektronisk fakturering](e-invoicing-service-overview.md)
- [Komme i gang med tillegget Elektronisk fakturering](e-invoicing-get-started.md)
- [Konfigurere tillegget Elektronisk fakturering](e-invoicing-setup.md)
