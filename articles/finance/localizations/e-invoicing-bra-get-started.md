---
title: Komme i gang med tillegget Elektronisk fakturering for Brasil
description: Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med tillegget Elektronisk fakturering for Brasil i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 0320bd1d9e93cc30ed75f28e387ac2ec8dbfc226
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962841"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>Komme i gang med tillegget Elektronisk fakturering for Brasil 

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> Tillegget Elektronisk fakturering for Brasil støtter ikke alle funksjonene som er tilgjengelige i regnskapsdokumentet som er innebygd i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.

Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med tillegget Elektronisk fakturering for Brasil. Det leder deg gjennom konfigurasjonstrinnene som er landsavhengige i Regulatory Configuration Services (RCS) og i Finance og Supply Chain Management. Det leder deg også gjennom prosessen med å sende et NF-e-regnskapsdokument (elektronisk regnskapsdokumentmodell 55) gjennom tjenesten, og det forklarer hvordan du gjennomgår behandlingsresultatene og statusen til regnskapsdokumentene.

## <a name="prerequisites"></a>Forutsetninger

Før du fullfører trinnene i dette emnet må du fullføre trinnene i [Komme i gang med tillegget Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>RCS-oppsett

Under RCS-oppsettet vil du fullføre disse oppgavene:

1. Importer funksjonen for e-fakturering for NF-e-regnskapsdokumenter.
2. Gå gjennom filformatene som kreves for å sende NF-e-regnskapsdokumenter for godkjenning.
3. Se gjennom filformatene som kreves for å be om annullering av en godkjent NF-e.
4. Konfigurer hendelse som kreves for å sende NF-e-regnskapsdokumenter for godkjenning.
5. Konfigurer hendelse som kreves for å be om annullering av en godkjent NF-e.
6. Tilordne funksjonen for e-fakturering til et miljø for tillegget Elektronisk fakturering.
7. Publiser funksjonen for e-fakturering.

> [!NOTE]
> "E-fakturering-funksjonen" er det generelle navnet på ressursen som er konfigurert og publisert til å bruke serveren for tillegget Elektronisk fakturering. Oppsettet av funksjonen for E-fakturering kombinerer, blant annet, bruken av konfigurasjonsformater for Elektronisk rapportering (ER) for å opprette konfigurerbare eksport- og importfiler, og bruken av handlinger og handlingsflyter for å gjøre det mulig å opprette konfigurerbare regler for å sende forespørsler, importere svar og analysere svarinnholdet.

## <a name="import-the-e-invoicing-feature"></a>Importere funksjonen for e-fakturering

1. Logge på RCS-kontoen
2. I **Globaliseringsfunksjoner**-arbeidsområder i delen **Funksjoner**, velger du flisen **E-fakturering**.
3. På siden for **e-faktureringsfunksjoner** velger du **Importer** for å importere en e-faktureringsfunksjon for et NF-e-regnskapsdokument fra det globale repositoriet.

    ![Importer-knappen](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. Velg funksjonen for NF-e-regnskapsdokument, og velg deretter **Importer**.

    ![Importere NF-e-funksjonen](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a>Opprette en ny versjon av funksjonen for NF-e-regnskapsdokument

- På siden for **E-faktureringsfunksjoner**, i kategorien **Versjoner**, velger du **Ny**.

![Legge til en ny versjon av e-fakturafunksjonen](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a>Oppdatere konfigurasjonsversjonen

1. På siden **E-faktureringsfunksjoner**, i kategorien **Konfigurasjoner**, velger du **Legg til** eller **Slett** for å behandle konfigurasjonsversjonene (ER-filformatkonfigurasjoner).

    ![Behandle konfigurasjoner for e-faktureringsfunksjon](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - Når du oppretter en ny versjon av funksjonen for NF-e-regnskapsdokument, arves alle konfigurasjonsversjoner (ER-filformater) fra den nyeste versjonen.
    - Hvis du vil sende NF-e-regnskapsdokumentet for godkjenning, kreves følgende konfigurasjonsversjoner:

        - Eksportformat for NFe-innsending
        - Import av NFe-svarmelding
        - Import av NFe-feillogg

    - Hvis du vil sende NF-e-avbrytelsen, kreves følgende konfigurasjonsversjon:

        - Eksportformat for NFe-annullering

2. Velg en konfigurasjonsversjon fra listen, og velg deretter **Rediger** eller **Vis** for å åpne siden **Formatutforming**, der du kan redigere eller vise konfigurasjonen.

    ![Åpne Formatutforming-siden](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. Bruk siden **Formatutforming** til å redigere eller vise ER-formatfilkonfigurasjoner. Hvis du vil ha mer informasjon, kan du se [Opprette konfigurasjoner for elektronisk dokument](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).

    ![Formatutformingsside](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a>Administrere oppsett for e-faktureringsfunksjonen

- På siden for **E-postfunksjoner**, i kategorien **Oppsett**, velger du **Legg til** eller **Slett** for å behandle e-faktureringsoppsettene (dvs. NF-e-hendelsene).

![Administrere oppsett for e-faktureringsfunksjonen](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

Når du oppretter en ny versjon av NF-e-regnskapsdokumentfunksjonen som er avledet fra en annen e-faktureringsfunksjon, arves alle funksjonsoppsett (NF-e-hendelser) fra den nyeste versjonen.

Funksjonen **Send** kreves for å sende NF-e-regnskapsdokumenter for godkjenning.

Hvis du skal sende NF-e-annullering, kreves oppsett av funksjonen for **Annullering**.

#### <a name="configure-the-submit-feature-setup"></a>Konfigurere oppsett av Send-funksjonen

1. På siden for **e-fakturafunksjoner**, i kategorien **Oppsett** i kolonnen **Funksjonsoppsett**, velger du **Send**.
2. Velg **Rediger**.

    ![Redigere oppsett for e-faktureringsfunksjon](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. På siden for **oppsett av funksjonsversjon** velger du kategorien **Handlinger** for å behandle listen over handlinger.

    ![Kategorien Handlinger](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. Gå gjennom handlingene som kreves for å sende en NF-e for godkjenning.

    | Handlings-ID | Handlingsnavn                  | Handlingsbeskrivelse                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | 1         | Transformere dokument           | Opprett NF-e-XML-filen for sending.                          |
    | 2         | Signer dokument                | Bruk den digitale signaturen på XML-filen.                    |
    | 3         | Kalle opp brasiliansk SEFAZ-tjeneste | Send den signerte XML-filen til webtjenestene for godkjenning. |
    | 4         | Behandle svar             | Hent webtjenestesvaret.                                     |
    | 5         | Transformere dokument           | Analyser innholdet i filen som er mottatt som et svar.     |
    | 6         | Transformere dokument           | Opprett XML-filen for å spørre om statusen for sendingen.    |
    | 7         | Kalle opp brasiliansk SEFAZ-tjeneste | Send XML-filen som ber om sendestatusen.          |
    | 8         | Behandle svar             | Hent webtjenestesvaret.                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>Konfigurere URL-adressen for SEFAZ-webtjenester 

1. På siden for **funksjonsversjonsoppsett**, i kategorien **Handlinger** i hurtigkategorien **Handlinger**, velger du å **Kalle opp meksikansk PAC-tjeneste** (handlings-ID **3**).
2. I hurtigkategorien **Parametere** i feltet for **URL-adresseparameter**, angir du URL-adressen til webtjenesten for SEFAZ for NF-e-sending.
3. I hurtigfanen **Handlinger** velger du å **Kalle opp brasiliansk SEFAZ-tjeneste** (handlings-ID **7**).
4. I hurtigkategorien **Parametere** i feltet for **URL-adresseparameter**, angir du URL-adressen til webtjenesten for SEFAZ for NF-e-sending.

#### <a name="configure-the-cancellation-feature-setup"></a>Konfigurere oppsett av kaselleringsfunksjonen

1. På siden for **e-fakturafunksjoner**, i kategorien **Oppsett** i kolonnen **Funksjonsoppsett**, velger du **Annullering**.
2. Velg **Rediger**.
3. På siden for **oppsett av funksjonsversjon** velger du kategorien **Handlinger** for å behandle listen over handlinger.
4. Se gjennom handlingene som kreves for å be om anullering av en godkjent NF-e.

    | Handlings-ID | Handlingsnavn                  | Handlingsbeskrivelse                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | 1         | Transformere dokument           | Opprett XML-filen for NF-e-annullering for innsending.            |
    | 2         | Signer dokument                | Bruk den digitale signaturen på XML-filen.                   |
    | 3         | Kalle opp brasiliansk SEFAZ-tjeneste | Send den signerte XML-filen til webtjenestene for annullering. |
    | 4         | Behandle svar             | Hent webtjenestesvaret.                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>Konfigurere URL-adressen for SEFAZ-webtjenester

1. På siden for **funksjonsversjonsoppsett**, i kategorien **Handlinger** i hurtigkategorien **Handlinger**, velger du å **Kalle opp meksikansk PAC-tjeneste** (handlings-ID **3**).
2. I hurtigkategorien **Parametere** i feltet for **URL-adresseparameter** angir du URL-adressen til webtjenesten for SEFAZ for annullering av en godkjent NF-e.

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a>Gjøre et e-faktureringsmiljø tilgjengelig og tilordne en kladdeversjon

1. På siden for **E-faktureringsfunksjoner**, i kategorien **Miljøer**, velger du **Aktiver**.
2. I feltet **Miljø** velger du miljøet.
3. I **Gyldig fra**-feltet angir du datoen for når miljøet skal tre i kraft.
4. Velg **Aktiver**.

![Aktivere et e-faktureringsmiljø](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a>Endre statusen til Fullført

1. På siden for **e-fakturafunksjoner** i kategorien **Versjoner** velger du versjonen av e-fakturafunksjonen med statusen **Utkast**.
2. Velg **Endre status \> Fullført**.

### <a name="change-the-status-to-publish"></a>Endre statusen til Publiser

1. På siden for **e-fakturafunksjoner**, i kategorien **Versjoner**, velger du versjonen av e-fakturafunksjonen med statusen **Fullført**.
2. Velg **Endre status \> Publiser**.

![Publisere funksjonen for e-fakturering](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Konfigurere integrasjon av tillegget Elektronisk fakturering i Finance eller Supply Chain Management

Under oppsettet vil du fullføre disse oppgavene:

1. Slå på funksjonen for føderal NF-e for Brasil.
2. Importer den spesifikke ER-datamodellen, datamodelltilordningen og formatene som kreves for NF-e-regnskapsdokumenter.
3. Importer ER-konfigurasjonen og konfigurer svartypene som kreves for å oppdatere statusen til regnskapsdokumentet etter sendingsprosessen er returnert.

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a>Slå på funksjonen for føderal NF-e for Brasil

1. Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.
2. I kategorien **Funksjoner** merker du av for **Aktiver** i raden for funksjonsreferanse **BR00053**.

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a>Importere ER-datamodelltilordningen som er nødvendig for NF-e-regnskapsdokumenter

1. Logg på Finance.
2. I delen **Konfigurasjonsleverandører** i arbeidsområdet **Elektronisk rapportering** velger du flisen **Microsoft**. Kontroller at konfigurasjonsleverandøren er satt til **Aktiv**. Hvis du ha mer informasjon om hvordan du setter en leverandør til **Aktiv**, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Velg **Repositorier**.
4. Velg **Global ressurs \> Åpne**.
5. Importer konfigurasjoner for **regnskapsdokumenttilordning**.

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a>Importere ER-konfigurasjoner og konfigurere svartypene for regnskapsdokumenter

1. I delen **Konfigurasjonsleverandører** i arbeidsområdet **Elektronisk rapportering** velger du flisen **Microsoft**.
2. Velg **Repositorier**.
3. Velg **Global ressurs \> Åpne**.
4. Importer **Import av NF-e-feillogg (BR)**, **Format for dataimport av NF-e-svar (BR)** og **Import av NF-e-svarmelding (BR)**.
5. Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.
6. I kategorien **Elektronisk dokument** velger du **Legg til**.
6. I feltet **Tabellnavn** angir du **regnskapsdokumenthode**.
7. I feltet **Dokumentkontekst** velger du **kontekstmodell for kundefaktura – regnskapsdokumentkontekst**.
8. Velg **Svartyper**.
9. Velg **Ny**, og deretter, i **Svartype**-feltet, velg **Svar**.
10. I feltet for **innsendingsstatus** velger du **Venter**.
11. I feltet **Modelltilordning** velg **svarmeldingsimportformat – modelltilordning fra svarmelding**.
12. Velg **Lagre**.
13. Velg **Ny** og deretter, i **Svartype**-feltet, angir du **ResponseData**.
14. I feltet for **innsendingsstatus** velger du **Venter**.
15. I **Modelltilordning**-feltet velger du **Format for dataimport av NFe-svar – dataimport av svar**.
16. Velg **Lagre**.

## <a name="electronic-invoice-processing"></a>Behandle elektronisk faktura

Under behandlingen i Finance vil du fullføre disse oppgavene:

1. Send et regnskapsdokument via tillegget Elektronisk fakturering.
2. Vise utførelsesloggene for sending og se gjennom resultatene av behandlingen.
3. Send annulleringen for et regnskapsdokument via tillegget Elektronisk fakturering.

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a>Sende NF-e-regnskapsdokumenter for SEFAZ-autorisasjon 

Når du har aktivert funksjonen for **Konfigurerbar integrasjon for tillegget Elektronisk fakturering**, kan ikke den gamle prosessen for sending av NF-e-regnskapsdokumenter for godkjenning (**Eksport/import av NF-e-prosess**) brukes lenger. Den erstattes av en ny prosess som kalles **Send elektroniske dokumenter**.

> [!NOTE]
> Før du fortsetter må du kontrollere at du har én eller flere kunderegnskapsdokumenter modell 55 som ble utstedt av kundens regnskapsfirma. Retningen for disse regnskapsdokumentene må settes til **Utgående**, og statusen må være **Opprettet**. Hvis du vil ha mer informasjon, kan du se [Utstede regnskapsdokumenter for kunde (Brasil)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).

1. Gå til **Organisasjonsstyring \> Periodiske \> Elektroniske dokumenter \> Send elektroniske dokumenter**.
2. For første innsending av et dokument må du alltid sette alternativet **Send dokumenter på nytt** til **Nei**. Hvis du må sende et dokument på nytt via tjenesten, setter du dette alternativet til **Ja**.
3. I hurtigfanen **Poster som skal inkluderes** velger du **Filter** for å åpne **Forespørsel**-dialogboksen, der du kan bygge en spørring for å velge dokumenter for innsending.
4. Velg **Legg til** i kategorien **Område**.
5. I feltet **Tabellnavn** velger du **regnskapsdokumenthode**.
6. I feltet **Avledet tabell** velger du **regnskapsdokumenthode**.
6. Velg **Nummer** i feltet **Felt**.
7. I **Vilkår**-feltet angir du nummeret på regnskapsdokumentet som skal sendes.
8. Velg **OK** for å lukke dialogboksen **Forespørsel**.
8. Velg **OK** for å sende de valgte dokumentene.

> [!NOTE]
> Under det første forsøket på å sende et dokument via tjenesten, blir du bedt om å bekrefte tilkoblingen til tillegget Elektronisk fakturering. Velg **Klikk her for å koble til innsendingstjeneste for elektronisk dokument**.

### <a name="view-all-submission-logs"></a>Vise alle sendelogger

Når du har aktivert funksjonen **Konfigurerbar integrasjon av tillegget Elektronisk fakturering**, er en ny side tilgjengelig der du kan følge opp dokumentsendingsprosessen. Du kan bruke denne siden til å vise sendelogger for alle sendte dokumenter.

1. Gå til **Organisasjonsstyring \> Periodisk \> Elektroniske dokumenter \> sendingslogg for elektronisk dokument**.
2. I **Dokumenttype**-feltet velger **regnskapsdokumenthode** for å filtrere bare etter regnskapsdokumenter.
3. I handlingsruten velger du **Forespørsler \> Innsendingsdetaljer** for å vise detaljene for sendeutførelsesloggene.

![Vise detaljene for innsendingsloggen](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> For NF-e-regnskapsdokumenter er viser kolonnen **Feilkode** returkoden som ble returnert av webtjenesten SEFAZ.

### <a name="view-submission-logs-through-the-fiscal-document-page"></a>Vise sendelogger via regnskapsdokumentsiden

Når du har aktivert funksjonen for **Konfigurerbar integrasjon for tillegget Elektronisk fakturering**, kan du også vise sendeloggene fra regnskapsdokumentsiden.

1. Gå til **Økonomimodul \> Forespørsler og rapporter \> Regnskapsdokumenter \> Alle regnskapsdokumenter**.
2. Velg et regnskapsdokument som tidligere ble sendt via tillegget Elektronisk fakturering.
3. Velg **logg for elektronisk dokument** i kategorien for **føderal NF-e** i handlingsruten.

![Vise sendelogger fra regnskapsdokumentsiden](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a>Sende godkjente NF-e-regnskapsdokumenter for SEFAZ-annullering

Når du har aktivert funksjonen for **Konfigurerbar integrasjon for tillegget Elektronisk fakturering**, kan ikke lenger den gamle prosessen for annullering av føderale NF-e-dokumenter brukes. Den erstattes av en ny avlysningsprosess som er innebygd på siden for **sendingslogg for elektronisk dokument**.

> [!NOTE]
> Kontroller at du har kjørt annulleringen av kunderegnskapsdokumentet for et godkjent NF-e-regnskapsdokument. Hvis du vil ha mer informasjon, kan du se [Annullere regnskapsdokument for kunde (Brasil)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).

1. Gå til **Organisasjonsstyring \> Periodisk \> Elektroniske dokumenter \> sendingslogg for elektronisk dokument**.
2. Velg regnskapsdokumentet, og velg deretter **Funksjoner \> Send relaterte innsendinger**.
3. Angi en beskrivelse for den tilknyttede sendingen, og velg deretter **OK**.

### <a name="view-cancellation-submission-logs"></a>Vise sendelogger for annullering

1. Gå til **Organisasjonsstyring \> Periodisk \> Elektroniske dokumenter \> sendingslogg for elektronisk dokument**.
2. I **Dokumenttype**-feltet velger **regnskapsdokumenthode** for å filtrere bare etter regnskapsdokumenter.
3. Velg regnskapsdokumentet, og velg deretter **Forespørsler \> Relatert sending** i handlingsruten.

    Tilknyttede sendinger er sendinger som er relatert til en hovedsending som ble opprettet først. Eksempelvis er innsendingen som autoriserer en bestemt NF-e, hovedinnsendingen. Innsendingen som ber om annullering av den samme NF-e i SEFAZ, er en relatert sending. Den finnes bare fordi den ber om å annullere jobben som ble gjort gjennom en annen innsending.

    Siden **Relatert innsendinger** viser alle tilknyttede innsendinger, og sendestatusen, for et gitt regnskapsdokument. I illustrasjonen nedenfor representerer den første linjen innsendingen som ber om godkjenning av regnskapsdokumentet. Den andre linjen representerer innsendingen som avbrøt regnskapsdokumentet.

    ![Vise sendeloggene for annullering](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. I handlingsruten velger du **Forespørsler \> Innsendingsdetaljer** for å vise detaljene for sendeutførelsesloggene.

    ![Vise detaljer for sendeloggen for annullering](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a>Personvernerklæring
Aktivering av funksjonen for BR-00053 (føderal NF-e) kan kreve sending av begrensede data, som inkluderer registrerings-IDen for organisasjonen. Dette overføres til tredjepartsleverandører autorisert av skattemyndigheten for å sende elektroniske fakturaer til skattemyndighetene i det forhåndsdefinerte formatet som kreves for integrering med myndighetenes webtjeneste. En administrator kan aktivere og deaktivere funksjonen BR-00053 (føderal NF-e) ved å navigere til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**. Velg kategorien **Funksjoner**, velg raden som inneholder BR-00053-funksjonen, og velg deretter riktig valg. Data som er importert fra disse eksterne systemene til denne Dynamics 365-elektroniske tjenesten, er underlagt vår [personvernerklæring](https://go.microsoft.com/fwlink/?LinkId=512132). Hvis du vil ha mer informasjon, kan du se delene om personvernerklæring i dokumentasjon for landspesifikke funksjoner.


## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over tillegget Elektronisk fakturering](e-invoicing-service-overview.md)
- [Komme i gang med tillegget Elektronisk fakturering](e-invoicing-get-started.md)
- [Konfigurere tillegget Elektronisk fakturering](e-invoicing-setup.md)
