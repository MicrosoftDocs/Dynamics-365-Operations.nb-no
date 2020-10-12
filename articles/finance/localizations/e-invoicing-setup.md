---
title: Konfigurere tillegget Elektronisk fakturering
description: Dette emnet beskriver hvordan du konfigurerer tillegget Elektronisk fakturering i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 92ffd2076497325fb986478328c4b2584929881d
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2020
ms.locfileid: "3836010"
---
# <a name="set-up-the-electronic-invoicing-add-on"></a>Konfigurere tillegget Elektronisk fakturering

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Funksjonsoppsettet for tillegget Elektronisk fakturering er prosessen med å opprette den nødvendige konfigurasjonen via det RCS-miljøet (Regulatory Configuration Services) og publisere den konfigurasjonen til serveren for tillegget Elektroniske fakturering. Ved hjelp av oppsettet kan du opprette de konfigurerbare reglene som gjør at tillegget Elektronisk fakturering kan bruke en sikker protokoll over Internett til å kommunisere og utveksle data med en tredjepartsenhet via webtjenester.

Konfigureringen er avhengig av konfigurasjonen av formatet for Elektronisk rapportering (ER) som en metode for å bygge innhold som sendes og mottas via digitale filer. Den er også avhengig av orkestrering av kommunikasjonshandlinger for å sende forespørsler til og motta svar fra webtjenester fra tredjeparter uten å kreve at du skriver kode.

## <a name="overview"></a>Oversikt

Funksjonen for tillegget Elektronisk fakturering er det generelle navnet på ressursen som er konfigurert og publisert til å bruke serveren for tillegget Elektronisk fakturering. Funksjonsoppsettet kombinerer, blant annet, bruken av ER-konfigurasjonsformater for å opprette konfigurerbare eksport- og importfiler, og bruken av handlinger og handlingsflyt for å gjøre det mulig å opprette konfigurerbare regler for å sende forespørsler, importere svar og analysere svarinnholdet.

Illustrasjonen nedenfor viser hovedkomponentene i en funksjon for tillegget Elektronisk fakturering.

![Oversikt over funksjon for tillegget Elektronisk fakturering](media/e-Invoicing-services-feature-setup-Overview-e-Invoicing-feature.png)

På grunn av variasjoner i fakturaformater og handlingsflyter kan funksjonsoppsettet variere etter land eller region, eller i henhold til forretningskrav.

## <a name="set-up-the-electronic-invoicing-add-on-feature"></a>Konfigurere funksjonen for tillegget Elektronisk fakturering

Installasjonsprosessen må fullføres i RCS-miljøet. Følg disse trinnene for å opprette en ny funksjon for tillegget Elektronisk fakturering.

1. Logg på RCS-miljøet.
2. I **Globaliseringsfunksjoner**-arbeidsområder, i delen **Funksjoner**, velger du flisen **Elektronisk fakturering-tillegg**.
3. På siden **Funksjoner for tillegget Elektronisk fakturering** velger du **Importer** for å importere ER-datamodellkonfigurasjonen fra det globale repositoriet.
4. Velg **Legg til** for å opprette en funksjon for tillegget Elektronisk fakturering. Du kan enten opprette funksjonen fra grunnen av eller avlede den fra en eksisterende funksjon for tillegget Elektronisk fakturering.

    ![Legge til en funksjon for tillegget Elektronisk fakturering](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature.png)

> [!NOTE]
> Når du oppretter en ny funksjon for tillegget Elektronisk fakturering, har det et versjonsnummer, og standardstatusen er satt til **Utkast**.

### <a name="configurations"></a>Konfigurasjoner

Konfigurasjoner har ER-formatkonfigurasjonene som kreves for transformasjoner og for å opprette filene som skal utveksles i løpet av kommunikasjonen med tredjeparts webtjenester. En funksjon for tillegget Elektronisk fakturering kan ha så mange ER-filformatkonfigurasjoner som kreves, basert på den tekniske spesifikasjonen for integrering som leveres av webtjenesteleverandøren.

Følg disse trinnene for å legge til ER-formater i funksjonen for tillegg for Elektronisk fakturering.

1. På siden for **Funksjoner for tillegget Elektronisk fakturering** i kategorien **Konfigurasjoner** velger du **Legg til** for å legge til ER-filformatkonfigurasjoner for funksjonen for tillegget Elektronisk fakturering.

    ![Legge til en funksjonskonfigurasjoner for tillegget Elektronisk fakturering](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Når du oppretter en funksjon for tillegget Elektronisk fakturering fra grunnen av, må du legge til alle ER-filformatkonfigurasjoner manuelt. Når du avleder en funksjon for tillegget Elektronisk fakturering fra en eksisterende funksjon, opprettes ER-filformatkonfigurasjonene automatisk, fordi de arves fra den opprinnelige funksjonen for tillegget Elektronisk fakturering.

2. Velg **Rediger** for å åpne siden **Formatutforming**, der du kan redigere ER-filformatkonfigurasjonen.

    ![Redigere funksjonskonfigurasjoner for tillegget Elektronisk fakturering](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Når du redigerer formatet, settes statusen for konfigurasjonsversjonen til **Utkast**.

3. Bruk siden **Formatutforming** til å endre filformatkonfigurasjonen. Hvis du vil ha mer informasjon, kan du se [Opprette konfigurasjoner for elektronisk dokument](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).

    ![Formatutformingsside](media/e-Invoicing-services-feature-setup-ER-Format-designer.png)

### <a name="feature-setups"></a>Funksjonsoppsett

Funksjonsoppsett kapsler inn reglene for kommunikasjon og sikkerhet med en webtjeneste fra en tredjepart. En funksjon for tillegget Elektronisk fakturering kan ha så mange funksjonsoppsett som er nødvendig, basert på forretningsregelen du vil oppnå.

Følg disse trinnene for å legge til funksjonsoppsett i funksjonen for tillegget Elektronisk fakturering.

1. På siden for **Funksjoner for tillegget Elektronisk fakturering** i kategorien **Oppsett** velger du **Legg til** for å legge til funksjonsoppsett i funksjonen for tillegget Elektronisk fakturering.

    ![Legge til oppsett for funksjon for tillegget Elektronisk fakturering](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Setups.png)

    > [!NOTE]
    > Når du oppretter en funksjon for tillegget Elektronisk fakturering fra grunnen av, må du legge til alle funksjonsoppsettene du trenger, manuelt. Når du avleder en funksjon for tillegget Elektronisk fakturering fra en eksisterende funksjon, opprettes alle funksjonsoppsett automatisk, fordi de arves fra den opprinnelige funksjonen for tillegget Elektronisk fakturering.

2. Velg **Rediger** for å redigere funksjonsversjonsoppsettet.

    ![Redigere funksjonsoppsett for tillegget Elektronisk fakturering](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Setups.png)

3. Bruk siden for **funksjonsversjonsoppsett** til å konfigurere handlinger, relevansregler og variabler.

    ![Handlinger, relevansregler og variabler](media/e-Invoicing-services-feature-setup-View-Actions-Applicability-Rules-Variables.png)

### <a name="actions"></a>Handlinger

Handlinger er en forhåndsdefinert liste over operasjoner som kjøres i sekvensiell rekkefølge. Denne listen representerer analysen av fremgangsmåten som kreves for full utførelse av funksjonen for tillegget Elektronisk fakturering. Handlingene kan omfatte, i den samme funksjonen for tillegget Elektronisk fakturering, kommunikasjon i begge retninger; sende en forespørsel om et mål og motta et svar og analysere innholdet.

Hver handling inneholder en forhåndsdefinert liste over parametere som kreves for at handlingen skal oppnå sitt formål. Tilleggsparametere kan eventuelt angis.

#### <a name="actions-fasttab"></a>Hurtigfanen Handlinger

På siden for **oppsett av funksjonsversjoner** i kategorien **Handlinger** i hurtigfanen **Handlinger** følger du én av eller begge disse trinnene for å behandle handlinger:

- Velg **Ny** eller **Slett** for å legge til nye handlinger eller slette eksisterende handlinger.
- Velg **Opp** eller **Ned** for å flytte valgte handlinger opp eller ned i rutenettet og dermed endre rekkefølgen som de kjøres i. Handlingene kjøres i den rekkefølgen de vises i, i rutenettet, fra øverst til nederst.

![Behandle handlinger](media/e-Invoicing-services-feature-setup-Manage-Actions.png)

Følgende tabell beskriver feltene som er tilgjengelige i hurtigkategorien **Handlinger**.

| Felt        | beskrivelse |
|--------------|-------------|
| Handling       | Det finnes åtte forhåndsdefinerte handlinger.<ul><li><strong>Signer dokument</strong></li><li><strong>FileStoreActionName</strong></li><li><strong>Transformer dokument</strong></li><li><strong>Behandle svar</strong></li><li><strong>Kalle opp REST-nettjeneste</strong></li><li><strong>Kalle opp meksikansk PAC-tjeneste</strong></li><li><strong>Kalle opp brasiliansk SEFAZ-tjeneste</strong></li><li><strong>Kalle opp italiensk SDI-tjeneste</strong></li></ul> |
| Handlingsnavn  | Navnet på handlingen og utføringsrekkefølgen. |
| beskrivelse  | En beskrivelse av handlingen. |
| Aktiver nytt forsøk | En valgt avmerkingsboks indikerer at handlingen kan utføres på nytt hvis det forrige forsøket mislykkes. |
| Prøv handling på nytt | Ved et nytt forsøk, handlingen som det nye forsøket startes fra. Nytt forsøk avsluttes på gjeldende handling (inklusivt nytt forsøk). For handlinger som har dem, angir parameterne for **minimum tilbaketrekking** og **maksimum tilbaketrekking** det minste antallet og det største antallet nye forsøk. |

#### <a name="parameters-fasttab"></a>Hurtigfanen Parametere

Hurtigfanen **Parametere** viser parameterne for handlingen som er valgt i hurtigfanen **Handlinger**.

![Hurtigfanen Parametere](media/e-Invoicing-services-feature-setup-View-Actions-Parameters.png)

Følgende tabell beskriver feltene som er tilgjengelige i hurtigkategorien **Parametere**.

| Felt       | beskrivelse |
|-------------|-------------|
| Navn        | En forhåndsdefinert liste over parametere. Hvis du vil ha mer informasjon, se delen [Liste over parametere etter handling](#list-of-parameters-by-action). |
| beskrivelse | En beskrivelse av parameteren. |
| Verdi       | Verdien på parameteren. |

#### <a name="list-of-parameters-by-action"></a>Liste over parametere etter handling

De tilgjengelige parameterne varierer avhengig av hvilken handling som er valgt i hurtigfanen **Handlinger**.

###### <a name="action-sign-document"></a>Handling: Signer dokument

| Parameter                             | beskrivelse |
|---------------------------------------|-------------|
| Inndatafil                            | Inndata-XML-dokumentfilen som må signeres ved hjelp av en elektronisk signatur. |
| Sertifikatnavn                      | Navnet på sertifikatet på lager. |
| Signaturtype                        | Signaturtypen som skal brukes. |
| Navn på signaturmetode                 | Navnet på signaturmetoden som brukes til å generere en elektronisk signatur. |
| Navn på sammendragsmetode                    | Sammendragsmetoden som brukes til å generere en sammendragsstreng i den digitale signaturen. |
| Navn på kanoniseringsmetode          | Type kanoniseringsmetode som brukes til å beregne signaturhashen. |
| Navn på referanseattributt              | Attributtnavnet som angir hvor referanse-IDen skal settes inn i signaturelementet. |
| Navn på elementet som skal signeres               | Navnet på XML-elementet i dokumentet som må signeres ved hjelp av en elektronisk signatur. Hvis ingen elementer er angitt, signeres roten av dokumentet. |
| Navn på elementet for innsetting av signatur   | Navnet på XML-elementet der en generert digital signatur skal settes inn. Hvis ingen elementer er angitt, settes signaturen inn i roten av dokumentet. |
| XLST-fil med sammendragstransformering       | XSLT-filen (Extensible Stylesheet Language Transformations) som inneholder regler for sammendragstransformering for å generere sammendragsstrengen for en elektronisk signatur. |
| Bane til innsetting av sammendragsstreng          | Banen, i **\<elementName\> .\<Attribute.Path\>** -format, på stedet der den genererte sammendragsstrengen skal settes inn. |
| Plassering av sertifikatnummer           | Navnet på elementet og attributtet der sertifikatnummeret skal plasseres. |
| Plassering av sertifikatdata          | Navnet på elementet og attributtet der sertifikatdata (base64) må settes inn. |
| Sertifikatnummer er i ASCII-format | En verdi som angir om nummeret på sertifikatet er kodet i ASCII-format. |

###### <a name="action-filestoreactionname"></a>Handling: FileStoreActionName

| Parameter  | beskrivelse |
|------------|-------------|
| Inndatafil | Inndata filen som skal lagres. |

###### <a name="action-transform-document"></a>Handling: Transformer dokument

| Parameter                       | beskrivelse |
|---------------------------------|-------------|
| Inndatafil                      | Kildefilen som inneholder dataene som må kjøres til handlingen. |
| Retning                       | En verdi som angir om importformatet eller eksportformatet skal brukes. |
| Konfigurasjons-ID                | Formatet som skal kjøres. |
| Konfigurasjonsversjon           | Hvis det ikke er angitt noen konfigurasjonsversjon, vil den nyeste versjonen bli brukt. |
| Konfigurasjonsintegrasjonspunkt | Kildefilen som leverer data til rapporteringskjøretiden. |

###### <a name="action-process-response"></a>Handling: Behandle svar

| Parameter                    | beskrivelse |
|------------------------------|-------------|
| Inndatafil                   | Svaret som skal analyseres. |
| Liste over rapporteringskonfigurasjoner | En liste over konfigurasjoner som brukes til å analysere svar. |

###### <a name="action-call-rest-web-service"></a>Handling: Kalle opp REST-nettjeneste

| Parameter                   | beskrivelse |
|-----------------------------|-------------|
| URL for webtjeneste             | URL-adressen det skal sendes forespørsler til. |
| Tidsavbrudd for webforespørsel         | Maksimumstiden (i millisekunder) det skal ventes på et webtjenestesvar. |
| Type forespørselsoperasjon      | Typen HTTP-forespørselsoperasjon (for eksempel **HENT**, **SEND** eller **SLETT**). |
| Sertifikatnavn           | Sertifikatnavnene. |
| Koding av svartekst      | Den forventede kodingen av HTTP-svarteksten, slik at den kan dekodes på riktig måte. |
| Innholdstype for HTTP-forespørsel   | Hodeinndataene for innholdstype for HTTP-forespørsel. |
| Innholdstekst for HTTP-forespørsel   | HTTP-forespørselsteksten. (Brødteksten kan være tom.) |
| Parameterspørringsverdier for HTTP | Parameterspørringsverdier som brukes til å fylle URL-adressen med variable parametere. |
| Forespørselsrute               | Rutebanen for HTTP-forespørselen. De variable parameterne kan skrives i **\{paramName\}**-notasjon. Her er et eksempel: **"api/{id}/submit"**. |
| Ruteparameterliste        | Ruteparameterne, i nøkkelverdinotasjon, som brukes til å sette inn variabler i ruten. |
| Egendefinerte HTTP-hoder         | De egendefinerte HTTP-hodene som plasseres i forespørselen. |
| Informasjonskapsler for HTTP-forespørsel        | En liste over informasjonskapsler, i nøkkelverdinotasjon, som skal plasseres i hodeforespørselen for HTTP-informasjonskapsler. |
| Sikkerhetsprotokoll           | Sikkerhetsprotokollen som skal brukes til HTTP-forespørsler for å kommunisere med serveren. (Som standard brukes Transport Layer Security \[TLS\] 1.2.) |

###### <a name="action-call-mexican-pac-service"></a>Handling: Kalle opp meksikansk PAC-tjeneste

| Parameter                | beskrivelse |
|--------------------------|-------------|
| Inndatafil               | Filen som inneholder XML-data som skal sendes til Webtjenesten som en metodeinndataparameter. |
| URL-adresse              | Webtjenesteadressen (endepunkt). |
| Navn på webmetode (handling) | Navnet på webmetoden (handling) som må kjøres. |
| Attester             | Sertifikatkjeden som kreves for klientgodkjenning av webtjenesten. Klientsertifikatet bør være det siste sertifikatet i kjeden. Rotsertifikater og midlertidige sertifikater skal være først. |
| Tidsavbrudd for webforespørsel      | Maksimumstiden (i millisekunder) det skal ventes på et webtjenestesvar. |
| Intervall mellom forsøk           | Intervallet mellom forsøk på å kalle og motta svar fra webtjenesten. Hvis det ikke er angitt et intervall, vil det ikke bli utført flere nye forsøk etter at den første samtalen er mislykket. |
| Antall nye forsøk              | Maksimalt antall nye forsøk på å kalle opp og hente et svar fra webtjenesten. |
| Tidsfrist for forsøk               | Den maksimale tiden (i millisekunder) som nye kall kan fortsette. |
| Minimum tilbaketrekking         | Minste tilbaketrekkingsrate for eksponentiell beregning av intervall for nye forsøk. |
| Maksimum tilbaketrekking         | Største tilbaketrekkingsrate for eksponentiell beregning av intervall for nye forsøk. |
| Sikkerhetsprotokoll        | Sikkerhetsprotokollen som skal brukes til HTTP-forespørsler for å kommunisere med serveren. (Som standard brukes TLS 1.2.) |

###### <a name="action-call-brazilian-sefaz-service"></a>Handling: Kalle opp brasiliansk SEFAZ-tjeneste

| Parameter                | beskrivelse |
|--------------------------|-------------|
| Inndatafil               | Filen som inneholder XML-data som skal sendes til Webtjenesten som en metodeinndataparameter. |
| URL-adresse              | Webtjenesteadressen (endepunkt). |
| Navn på webmetode (handling) | Navnet på webmetoden (handling) som må kjøres. |
| Attester             | Sertifikatkjeden som kreves for klientgodkjenning av webtjenesten. Klientsertifikatet bør være det siste sertifikatet i kjeden. Rotsertifikater og midlertidige sertifikater skal være først. |
| Tidsavbrudd for webforespørsel      | Maksimumstiden (i millisekunder) det skal ventes på et webtjenestesvar. |
| Intervall mellom forsøk           | Intervallet mellom forsøk på å kalle og motta svar fra webtjenesten. Hvis det ikke er angitt et intervall, vil det ikke bli utført flere nye forsøk etter at den første samtalen er mislykket. |
| Antall nye forsøk              | Maksimalt antall nye forsøk på å kalle opp og hente et svar fra webtjenesten. |
| Tidsfrist for forsøk               | Den maksimale tiden (i millisekunder) som nye kall kan fortsette. |
| Minimum tilbaketrekking         | Minste tilbaketrekkingsrate for eksponentiell beregning av intervall for nye forsøk. |
| Maksimum tilbaketrekking         | Største tilbaketrekkingsrate for eksponentiell beregning av intervall for nye forsøk. |
| Sikkerhetsprotokoll        | Sikkerhetsprotokollen som skal brukes til HTTP-forespørsler for å kommunisere med serveren. (Som standard brukes TLS 1.2.) |

###### <a name="action-call-italian-sdi-service"></a>Handling: Kalle opp italiensk SDI-tjeneste

| Parameter                | beskrivelse |
|--------------------------|-------------|
| Inndatafil               | Filen som inneholder XML-data som skal sendes til Webtjenesten som en metodeinndataparameter. |
| URL-adresse              | Webtjenesteadressen (endepunkt). |
| Navn på webmetode (handling) | Navnet på webmetoden (handling) som må kjøres. |
| Attester             | Sertifikatkjeden som kreves for klientgodkjenning av webtjenesten. Klientsertifikatet bør være det siste sertifikatet i kjeden. Rotsertifikater og midlertidige sertifikater skal være først. |
| Tidsavbrudd for webforespørsel      | Maksimumstiden (i millisekunder) det skal ventes på et webtjenestesvar. |
| Intervall mellom forsøk           | Intervallet mellom forsøk på å kalle og motta svar fra webtjenesten. Hvis det ikke er angitt et intervall, vil det ikke bli utført flere nye forsøk etter at den første samtalen er mislykket. |
| Antall nye forsøk              | Maksimalt antall nye forsøk på å kalle opp og hente et svar fra webtjenesten. |
| Tidsfrist for forsøk               | Den maksimale tiden (i millisekunder) som nye kall kan fortsette. |
| Minimum tilbaketrekking         | Minste tilbaketrekkingsrate for eksponentiell beregning av intervall for nye forsøk. |
| Maksimum tilbaketrekking         | Største tilbaketrekkingsrate for eksponentiell beregning av intervall for nye forsøk. |
| Sikkerhetsprotokoll        | Sikkerhetsprotokollen som skal brukes til HTTP-forespørsler for å kommunisere med serveren. (Som standard brukes TLS 1.2.) |

### <a name="applicability-rules"></a>Relevansregler

Relevansregler gjør det mulig å opprette logiske regler som bestemmer brukskonteksten for funksjonsoppsettet. Samsvaret mellom konteksten som er gitt av forretningsdokumentet som er sendt til behandling, sammen med gyldighetsregelkriteriene, bestemmer dermed hvilken funksjon for tillegget Elektronisk fakturering som brukes til å behandle innsendingen.

#### <a name="set-up-applicability-rules"></a>Konfigurere relevansregler

1. På siden for **funksjonsversjonsoppsett** i kagetorien **Relevansregler** velger du **Ny** for å legge til en gyldighetsregel.

    ![Behandle relevansregler](media/e-Invoicing-services-feature-setup-Manage-Actions-Applicability-rules.png)

2. I rutenettet velger du setningene som skal grupperes.
3. Velg **Grupper setning**.

    ![Gruppere setninger](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-clause.png)

    Når setninger grupperes, legges det til en ny kolonne i rutenettet. Denne kolonnen angir den logiske operatoren for de grupperte setningene.

    ![Logisk operator for grupperte setninger](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-criterias.png)

Hvis du vil fjerne grupperingen av setningene, velger du de grupperte setningene som grupperingen skal oppheves for, og deretter velger du alternativet for **Opphev gruppering av setning**.

![Oppheve gruppering av setninger](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-UnGroup-criterias.png)

> [!NOTE]
> Når du opphever gruppering av en setning, må du alltid starte fra det innerste grupperingsnivået.

Følgende tabell beskriver feltene som er tilgjengelige i kategorien **Relevansregler**.

| Felt         | beskrivelse |
|---------------|-------------|
| Og/eller        | Den logiske operatoren. |
| Felt         | Feltet som skal brukes til å konstruere regelen. |
| Operatortype | Type operator:<ul><li>Lik</li><li>Ikke lik</li><li>Større enn / Mindre enn</li><li>Større enn eller lik / Mindre enn eller lik</li><li>Inneholder</li><li>Begynner med</li></ul> |
| Verdi         | Kriteriet for regelen. |

### <a name="variables"></a>Variabler

Du kan opprette variabler og deretter bruke dem som inndataverdi for en parameter for en bestemt handling. Du kan også bruke dem til utveksling, mellom tjenestene for Elektronisk fakturering-tillegget og klienten, informasjon som er resultatet av utførelsen av en bestemt handling som en del av flyten av innsendinger.

#### <a name="set-up-variables"></a>Konfigurer variabler

- På siden for **funksjonsversjonsoppsett**, i kategorien **Variabler**, velger du **Ny** eller **Slett** for å administrere variabler.

    ![Administrere variabler](media/e-Invoicing-services-feature-setup-Manage-Variables.png)

Følgende tabell beskriver feltene som er tilgjengelige i kategorien **Variabler**.

| Felt       | beskrivelse |
|-------------|-------------|
| Navn        | Navnet på variabelen. |
| beskrivelse | En kort beskrivelse av variabelen. |
| Type        | Type variabel:<ul><li><strong>Konstant</strong> – Innholdet i variabelen er fast.</li><li><strong>Fra klient</strong> – Innholdet i variabelen hentes fra Microsoft Dynamics 365-klienten under utføring av innsendingsprosessen.</li><li><strong>Til klient</strong> – Innholdet i variabelen gjøres tilgjengelig for import av Microsoft Dynamics 365-klienten under utføring av innsendingsprosessen.</li></ul> |
| Datatype   | Datatypen for variabelen:<ul><li>Boolsk</li><li>Dato</li><li>Antall</li><li>UUID</li><li>Streng</li><li>Fil</li></ul> |
| Verdi       | Verdien for variabelen eller navnet på handlingen som angir verdien for variabelen. |

### <a name="validate-the-feature-setup"></a>Validere funksjonsoppsettet

- På siden for **funksjonsversjonsoppsett**, i handlingsruten, velger du **Valider** for å validere funksjonsversjonsoppsettet.

   ![Velge Valider-knappen](media/e-Invoicing-services-feature-setup-Select-Validate-Button.png)

Valideringen kontrollerer konsekvensen for hele konfigurasjonen. Hvis for eksempel en bestemt parameter for en handling er obligatorisk, men verdien forblir tom, oppdager valideringen denne inkonsekvensen, og du får en advarsel.

## <a name="environments"></a>Miljøer

Et miljø for tillegget Elektronisk fakturering må være knyttet til funksjonen for tillegget Elektronisk fakturering og være aktivert for det. Miljøer for tillegget Elektronisk fakturering må opprettes og publiseres på forhånd ved hjelp av konfigurasjon av globaliseringsfunksjoner på organisasjonens RCS-konto.

Følg disse trinnene for å aktivere et miljø for tillegget Elektronisk fakturering for funksjonen for tillegget Elektronisk fakturering.

1. På siden for **Funksjoner for tillegget Elektronisk fakturering**, i kategorien **Miljøer**, velger du **Aktiver** for å legge til et miljø for tillegget Elektronisk fakturering.
2. I **Gyldig fra**-feltet angir du datoen for når det nye miljøet trer i kraft.

![Aktivere et miljø for tillegget Elektronisk fakturering](media/e-Invoicing-services-feature-setup-Select-Enable-e-Invoicing-feature-Environment.png)

## <a name="organizations"></a>Organisasjoner

Funksjonen for tillegget Elektronisk fakturering kan deles på tvers av flere organisasjoner.

- På siden **Funksjoner for tillegget Elektronisk fakturering**, i kategorien **Organisasjoner**, velger du **Del med** for å legge til organisasjonen du vil dele funksjonen for tillegget Elektronisk fakturering med.

Hvis du vil slutte å dele funksjonen for tillegget Elektronisk fakturering med organisasjonen, velger du **Opphev deling**.

## <a name="versions"></a>Versjoner

Versjoner bidrar til å kontrollere livssyklusen til funksjonen for tillegget Elektronisk fakturering ved å styre statusen. Du kan opprette en ny versjon av en eksisterende funksjon for tillegget Elektronisk fakturering, eller, når all konfigurasjon for funksjonen for tillegget Elektronisk fakturering er fullført, kan du endre statusen for funksjonen til **Fullført** og deretter til **Publiser**.

### <a name="create-a-new-version-of-an-existing-electronic-invoicing-add-on-feature"></a>Opprette en ny versjon av en eksisterende funksjon for tillegget Elektronisk fakturering

1. På siden for **Funksjoner for tillegget Elektronisk fakturering**, i rutenettet til venstre, velger du funksjonen for tillegget Elektronisk fakturering.
2. I kategorien **Versjoner** velger du **Ny** for å legge til en ny versjon av funksjonen for tillegget Elektronisk fakturering.

### <a name="change-the-status-of-the-electronic-invoicing-add-on-feature"></a>Endre statusen for funksjonen for tillegget Elektronisk fakturering

Følg disse trinnene for å behandle livssyklusen for funksjonen for tillegget Elektronisk fakturering.

1. På siden for **Funksjoner for tillegget Elektronisk fakturering**, i rutenettet til venstre, velger du funksjonen for tillegget Elektronisk fakturering.
2. I kategorien **Versjoner** velger du **Endre status**, og deretter endrer du statusen fra **Utkast** til **Fullført**.
3. Du blir bedt om å bekrefte at du vil fullføre funksjonen for tillegget Elektronisk fakturering og alle komponentene. Velg **Ja** for å bekrefte handlingen eller **Nei** for å avbryte den.

    > [!NOTE]
    > Når du velger **Ja**, blir statusen for konfigurasjonsversjoner, som er komponenter av funksjonen for tillegget Elektronisk fakturering, automatisk endret fra **Utkast** til **Fullført**.

4. Velg **Endre status**, og deretter endrer du statusen fra **Utkast** til **Publiser**.
5. Du blir bedt om å bekrefte at du vil publisere funksjonen for tillegget Elektronisk fakturering og alle komponentene til Globalt repositorium. Velg **Ja** for å bekrefte handlingen eller **Nei** for å avbryte den.

    > [!NOTE]
    > Når du velger **Ja**, endres statusen for konfigurasjonsversjoner automatisk fra **Fullført** til **Delt**.
