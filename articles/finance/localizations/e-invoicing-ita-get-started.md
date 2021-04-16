---
title: Komme i gang med Elektronisk fakturering for Italia
description: Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med elektronisk fakturering for Italia.
author: gionoder
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 23cb0523b6d6d065ad19f6c3bddf881b0dc82a7d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840106"
---
# <a name="get-started-with-electronic-invoicing-for-italy"></a>Komme i gang med Elektronisk fakturering for Italia

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> Det er ikke sikkert at Elektronisk fakturering for Italia støtter alle funksjonene som er tilgjengelige for elektroniske fakturaer i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management. 

Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med elektronisk fakturering for Italia. Det leder deg gjennom konfigurasjonstrinnene som er landsavhengige i Regulatory Configuration Services (RCS) og Finance. Det leder deg også gjennom prosessen med å sende elektroniske fakturaer som genereres i det Italia-spesifikke **FatturaPA**-formatet via tjenesten, og det forklarer hvordan du gjennomgår resultatene av behandlingen.

## <a name="prerequisites"></a>Forutsetninger

Før du fullfører trinnene i dette emnet må du fullføre trinnene i [Komme i gang med Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>RCS-oppsett

Under RCS-oppsettet vil du fullføre disse oppgavene:

1. Importer funksjonen for e-fakturering for eksport av elektroniske fakturaer for kunder i **FatturaPA**-formatet.
2. Gå gjennom formatkonfigurasjonene som kreves for å generere, sende og motta svar om elektroniske fakturaer.
3. Konfigurer hendelsene som støtter innsendingsscenarioene for elektronisk faktura.
4. Publiser funksjonen for e-fakturering.

> [!NOTE]
> "E-fakturering-funksjonen" er det generelle navnet på ressursen som er konfigurert og publisert til å bruke serveren for Elektronisk fakturering. I dette tilfellet er eksport av elektroniske fakturaer for kunder e-fakturafunksjonen du skal konfigurere.

## <a name="import-the-e-invoicing-feature"></a>Importere funksjonen for e-fakturering

1. Logg på RCS-kontoen.
2. I **Globaliseringsfunksjoner**-arbeidsområder i delen **Funksjoner**, velger du flisen **E-fakturering**.
3. På siden for **e-faktureringsfunksjoner** velger du **Importer** for å importere e-faktureringsfunksjonen fra det globale repositoriet.

    > [!NOTE]
    > Hvis du ikke ser listen over tilgjengelige funksjoner, velger du **Synkroniser**. 

4. Velg funksjonen for **e-fakturaeksport (IT)**, og velg deretter **Importer**.

![Importere funksjonen for e-fakturaeksport (IT)](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

Når du importerer funksjonen for **e-fakturaeksport (IT)** fra det globale lageret, blir alle innstillingene som er beskrevet i de neste delene, også importert.

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a>Opprette en ny versjon av funksjonen for e-fakturaeksport

1. På siden for **E-faktureringsfunksjoner**, i kategorien **Versjoner**, velger du **Ny**. 

    ![Legge til en ny versjon av e-fakturafunksjonen](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    Deretter konfigurerer du formatene for Elektronisk rapportering (ER) som er knyttet til e-fakturafunksjonen.

2. I kategorien **Konfigurasjoner** velger du **Legg til** for å administrere konfigurasjonsversjonene.

    ![Behandle konfigurasjonsversjonene av e-faktureringsfunksjonen](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    På dette trinnet skal du legge til og konfigurere ER-formater av forskjellige filer som brukes til å eksportere italienske e-fakturaer. For italienske FatturaPA-e-fakturaer bruker du enten følgende standardkonfigurasjoner eller de faktiske egendefinerte konfigurasjonene du bruker for e-fakturering:

    - Salgsfaktura (IT)
    - Prosjektfaktura (IT)

    Når du oppretter en e-faktureringsfunksjon som er avledet fra en annen e-faktureringsfunksjon, arves alle ER-formatene fra den opprinnelige funksjonen.

3. Velg en bestemt ER-formatfilkonfigurasjon.
4. Velg **Rediger** eller **Vis** for å åpne **Formatutforming**-siden.

    ![Åpne Formatutforming-siden](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. Bruk siden **Formatutforming** til å redigere og vise ER-formatfilkonfigurasjoner.

    ![Formatutformingsside](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>Administrere oppsett for e-faktureringsfunksjonen

- På siden for **E-postfunksjoner**, i kategorien **Oppsett**, velger du **Legg til**, **Slett** eller **Rediger** for å behandle e-faktureringsoppsettene.

![Administrere oppsett for e-faktureringsfunksjonen](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

I dette trinnet konfigurerer du hendelsene som gjelder elektroniske fakturaer, inkludert generering av XML-utdatafilene i **FatturaPA**-format og digital signering (om nødvendig).

### <a name="configure-the-sales-invoice-feature-setup"></a>Konfigurere oppsettet av salgsfakturafunksjonen

1. På siden for **e-fakturafunksjoner**, i kategorien **Oppsett** i kolonnen **Funksjonsoppsett**, velger du **Salgsfaktura**.
2. Velg **Rediger**.
3. På siden for **oppsett av funksjonsversjon** velger du kategorien **Handlinger** for å behandle listen over handlinger. Handlinger definerer en liste over operasjoner som må kjøres i sekvensiell rekkefølge for å oppnå full utførelse av hendelsen.

    ![Kategorien Handlinger](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | Handlings-ID | Handlingsnavn        | Handlingsbeskrivelse                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | 1         | Transformere dokument | Opprett XML-filen for e-faktura i **FatturaPA**-format. |
    | 2         | Signer dokument      | Bruk en digital signatur på XML-filen.             |

4. Velg **Relevansregler**-kategorien for å vise og vedlikeholde de gjeldende reglene. Relevansregler definerer konteksten der handlingen skal kjøres.

    ![Kategorien Relevansregler](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. Velg kategorien **Variabler** for å vise og vedlikeholde variablene.

    ![Kategorien Variabler](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. Definer de offentlige variablene som kreves for å kjøre handlingene.

### <a name="configure-the-project-invoice-feature-setup"></a>Konfigurere oppsettet av prosjektfakturafunksjonen 

Trinnene og innstillingene som kreves for å konfigurere oppsettet av funksjonen **Prosjektfaktura**, er svært like fremgangsmåten og innstillingene for oppsett av funksjonen **Salgsfaktura**. Når du arbeider med prosjektfakturaer, kan du se fremgangsmåtene for salgsfakturaer.

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a>Tilordne e-postfakturafunksjonen til-miljøet

1. På siden for **E-faktureringsfunksjoner**, i kategorien **Miljøer**, velger du **Aktiver**.
2. I feltet **Miljø** velger du miljøet.
3. I **Gyldig fra**-feltet angir du datoen for når miljøet skal tre i kraft.
4. Velg **Aktiver**. 

![Aktivere e-faktureringsmiljøet](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a>Publisere funksjonen for e-fakturering

Du kan publisere funksjonen for e-fakturering ved å endre versjonsstatusen til **Fullført** eller **Publisert**.

### <a name="change-the-version-status-to-completed"></a>Endre versjonsstatusen til Fullført

1. På siden for **e-fakturafunksjoner** i kategorien **Versjoner** velger du versjonen av e-fakturafunksjonen med statusen **Utkast**.
2. Velg **Endre status \> Fullført**. 

### <a name="change-the-version-status-to-published"></a>Endre versjonsstatusen til Publisert 

1. På siden for **e-fakturafunksjoner**, i kategorien **Versjoner**, velger du versjonen av e-fakturafunksjonen med statusen **Fullført**.
2. Velg **Endre status \> Publiser**.

![Endre statusen for e-fakturafunksjonen](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-integration-in-finance"></a>Konfigurere integrasjon av Elektronisk fakturering i Finance

Under Finance-oppsettet vil du fullføre disse oppgavene:

1. Importer ER-datamodellen, ER-datamodelltilordningen og kontekstkonfigurasjonene for FatturaPA-e-fakturaer.
2. Konfigurer sertifikatet som kreves for å signere italienske e-fakturaer digitalt.

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a>Importere datamodellen, datamodelltilordningen og formatene for ER

1. I arbeidsområdet for **Elektronisk rapportering** kontrollerer du at konfigurasjonsleverandøren for **forretningsdokumenttjenesten** er satt til **Aktiv**.
2. Velg **Repositorier**.
3. Velg **Global ressurs \> Åpne**.
4. Importer **Fakturamodell**, **Fakturamodelltilordning** og **kontekstmodell for kundefaktura**.

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a>Slå på funksjonen for eksport av elektroniske fakturaer for kunder for Italia

1. Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.
2. I kategorien **Funksjoner** merker du av for **Aktivert** i raden for funksjonsreferanse **IT00036**.

![Slå på FatturaPA-funksjonen](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a>Konfigurere elektroniske dokumenter

1. Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.
2. I kategorien **Elektronisk dokument** velger du **Legg til** og angir tabellene som kreves for å generere italienske e-fakturaer:

    - **Tabellnavn:** Kundefakturajournal
    - **Tabellnavn:** Prosjektfaktura

3. For hver tabell definerer du en relatert dokumentkontekst:

    - For **Kundefakturajournal** velger du **Kundefakturakontekst**.
    - I **Prosjektfaktura** velger du **Prosjektfakturakontekst**.

![Konfigurere svartyper](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a>Behandle elektronisk faktura

Under behandlingen i Finance vil du fullføre disse oppgavene:

1. Generere italienske e-fakturaer ved hjelp av Elektronisk fakturering
2. Vise utførelsesloggene og se gjennom resultatene av behandlingen

### <a name="generate-electronic-invoices"></a>Generere elektroniske fakturaer

Når du har aktivert funksjonen for **konfigurerbar integrasjon av Elektronisk fakturering** og aktivert **IT00036**-funksjonen, kan ikke den gamle Finance-prosessen for generering av italienske e-fakturaer lenger brukes. Den erstattes av en ny prosess som kalles **Send elektroniske dokumenter**.

Du kan sende dokumentene manuelt, basert på etterspørselen etter e-fakturadokumenter.

> [!NOTE]
> Før du fortsetter må du kontrollere at oppsettet som kreves for italienske e-fakturaer, ble fullført. Hvis du vil ha mer informasjon, kan du se [Elektroniske fakturaer for kunde](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices). Vær oppmerksom på at noen av oppsettrinnene som beskrives i dette emnet, kanskje ikke er tilgjengelige på grunn av aktivering av Elektronisk fakturering.

1. Gå til **Organisasjonsstyring \> Periodiske \> Elektroniske dokumenter \> Send elektroniske dokumenter**.
2. For første innsending av et dokument må du sette alternativet **Send dokumenter på nytt** til **Nei**. Hvis du må sende et dokument på nytt via tjenesten, setter du dette alternativet til **Ja**.
3. I hurtigfanen **Poster som skal inkluderes** velger du **Filter** for å åpne **Forespørsel**-dialogboksen, der du kan bygge en spørring for å velge dokumenter for innsending.

![Dialogboksen Send elektroniske dokumenter](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a>Filterspørring

1. I dialogboksen **Forespørsel** konfigurerer du filtreringsbetingelser for både salgsfakturaer og prosjektfakturaer, eller lar betingelsene stå tomme for å inkludere alle fakturaer som ikke er sendt.

    ![Definere filterkriterier for sending](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. Velg **OK** for å lukke dialogboksen **Forespørsel**.
3. Velg **OK** for å sende de valgte dokumentene.

> ![Merk] Under det første forsøket på å sende et dokument via tjenesten, blir du bedt om å bekrefte tilkoblingen til Elektronisk fakturering. Velg **Klikk her for å koble til innsendingstjeneste for elektronisk dokument**.

#### <a name="view-submission-logs"></a>Vise sendelogger

Du kan vise sendelogger for alle sendte dokumenter.

1. Gå til **Organisasjonsstyring \> Periodisk \> Elektroniske dokumenter \> sendingslogg for elektronisk dokument**.
2. I feltet **Dokumenttype** velger du **Kundefakturajournal** eller **Prosjektfaktura** for å filtrere etter de påkrevde elektroniske dokumentene.

    ![Velge en dokumenttype for å vise sendelogger](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    Verdien som vises i kolonnen **Status for sending**, representerer statusen for innsendingsprosessen. Den viser om prosessen kjørte som konfigurert, og om det kreves tilleggshandling.

3. I handlingsruten velger du **Forespørsler \> Innsendingsdetaljer** for å vise detaljene for sendeutførelsesloggene.

    ![Vise detaljene for innsendingsloggen](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. I hurtigfanen **Behandlingshandlinger** kan du vise utførelsesloggen for handlingene som er konfigurert i funksjonsversjonen som er definert i RCS. **Status**-kolonnen viser om handlingen ble kjørt uten feil.
5. I hurtigfanen **Handlingsfiler** kan du vise de mellomliggende filene som ble generert under utføring av handlingene. Du kan velge **Vis** for å laste ned XML-filen for utdata i **FatturaPA**-format og vise innholdet i den.

## <a name="related-topics"></a>Relaterte emner

- [Oversikt over elektronisk fakturering](e-invoicing-service-overview.md)
- [Komme i gang med Elektronisk fakturering](e-invoicing-get-started.md)
- [Definere Elektronisk fakturering](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
