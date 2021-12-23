---
title: Kontrolliste for oppsett av elektroniske meldinger for mva-returer med direkte innsending til Altinn
description: Dette emnet inneholder en kontrolliste for oppsett av funksjonen Elektroniske meldinger for mva-returer for Norge.
author: liza-golub
ms.date: 11/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Norway
ms.author: elgolu
ms.search.validFrom: 2021-11-18
ms.dyn365.ops.version: AX 10.0.22
ms.openlocfilehash: b5373c52a8c255e1823347381b5bd3e8a755c9eb
ms.sourcegitcommit: a11e8f4e764ff0bb210875401ae0671bc6412bde
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/29/2021
ms.locfileid: "7866809"
---
# <a name="checklist-for-electronic-messages-setup-for-vat-returns-with-direct-submission-to-altinn"></a>Kontrolliste for oppsett av elektroniske meldinger for mva-returer med direkte innsending til Altinn

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om hvordan funksjonaliteten for [elektroniske meldinger](../general-ledger/electronic-messaging.md) er satt opp for behandling av mva-returer med direkte innsending til Altinn i Norge. Du kan bruke informasjonen i dette emnet til å finne ut om funksjonaliteten for elektroniske meldinger er riktig konfigurert.

Selv om dette emnet inneholder den viktigste informasjonen om oppsettet, innholder den ikke informasjon om alle dataene. Vi anbefaler at du bruker en pakke med dataenheter som inneholder et forhåndsdefinert oppsett av funksjonaliteten, og som omfatter alle dataene som kreves for å konfigurere behandling for samhandling med Altinn.

- Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Behandling av elektronisk melding** og se gjennom oppsettet. Følgende behandlingstype er definert for å støtte samarbeid med Altinn.

    | Behandler | Navn (norsk) | Beskrivelse |
    |---|---|---|
    | NO mva-retur | Momsoppgave med direkte innsending | Behandlingen for å klargjøre og sende mva-tilbakebealing til Altinn. |

    > [!IMPORTANT]
    > Hvis du vil aktivere tilgang på postnivå for forretningsbrukere, må du definere sikkerhetsroller for behandlingen.

## <a name="web-applications"></a>Webprogrammer

- Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Webprogrammer** og se gjennom oppsettet. **NO mva-retur** bruker følgende webprogrammer.

    | Programnavn | Beskrivelse |
    |---|---|
    | NO Altinn | Webprogram for samhandling med Altinn-APIer. |
    | NO ID-Porten | Webprogram for samarbeid med integreringspunktet som du opprettet i ID-porten. |

Tabellen nedenfor viser parametrene for webprogrammene som **NO mva-retur** bruker.

| Parameter | Verdi for NO Altinn | Verdi for NO ID-Porten |
|---|---|---|
| Primær URL-adresse | `https://platform.tt02.altinn.no/authentication/api/v1/exchange/id-porten` | `https://oidc-ver2.difi.no/idporten-oidc-provider` |
| URL-bane til autorisasjon | Blank | **/authorize** |
| URL-bane til token | Blank | **/token** |
| Nettadresse for omadressering | Blank | Definer verdien i henhold til informasjonen i [Definere internettadressen til webtjenestene ID-porten og Altinn](emea-nor-vat-return-setup.md#internet-address). |
| Tilordning av autorisasjonsformat | **Altinn mva-autorisasjonsformat (NO)** | **Altinn mva-autorisasjonsformat (NO)** |
| Importer tokenmodelltilordning | **Altinn-mva-import Altinn-tokenformat (NO)** | **Altinn-mva-import ID-porten-tokenformat (NO)** |
| Godta | Blank | Blank |
| Innholdstype | **program/json** | **application/x-www-form-urlencoded** |

> [!IMPORTANT]
> Hvis du vil aktivere tilgangstoken og samarbeid med ID-porten og Altinn-APIer for forretningsbrukere, må du definere sikkerhetsroller for begge webprogrammene.

Internett-adresser (basis-URL) kan endres av norske skattemyndigheter. Vi anbefaler at du ser etter faktiske URL-adresser på det offisielle Altinn- og ID-porten-webområdet.

## <a name="web-service-settings"></a>Innstillinger for webtjeneste

- Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Innstillinger for webtjeneste** og se gjennom oppsettet. **NO mva-retur** bruker følgende webtjenester:

    - NO Altinn GET-vedlegg
    - NO Altinn GET JSON
    - NO Altinn POST JSON
    - NO Altinn POST XML
    - NO Altinn PUT JSON
    - NO Altinn PUT XML
    - NO Valider mva-retur

Tabellene nedenfor viser parametrene og parameterverdiene for webtjenestene som **NO mva-retur** bruker.

### <a name="web-service-no-altinn-get-attachments"></a>Webtjeneste: NO Altinn GET-vedlegg

| Parameternavn | Parameterverdi |
|---|---|
| Nettjeneste | **NO Altinn GET-vedlegg** |
| Beskrivelse | **Altinn-webtjeneste for GET-vedlegg som lastes ned (XML, PDF)** |
| Internett-adresse | Blank |
| Nettsøknad | **NO Altinn** |
| Bruk proxy-server | **Nei** |
| Bruk avanserte parametere | Blank |
| Sertifikat | Blank |
| Svartypen – XML | **Nei** |
| Forespørselsmetode | **GET** |
| Godta | Blank |
| Godta koding | Blank |
| Forespørselshoder | Blank |
| Innholdstype | Blank |
| Formattilordning for forespørselshode | **Format for webforespørselshoder for Altinn mva (NO)** |
| Kode for fullført svar | **200** |

### <a name="web-service-no-altinn-get-json"></a>Webtjeneste: NO Altinn GET JSON

| Parameternavn | Parameterverdi |
|---|---|
| Nettjeneste | **NO Altinn GET JSON** |
| Beskrivelse | **Altinn-webtjeneste for GET-forespørsler av JSON-type innhold** |
| Internett-adresse | `https://skd.apps.tt02.altinn.no/skd/mva-melding-innsending-etm2/instances` |
| Nettsøknad | **NO Altinn** |
| Bruk proxy-server | **Nei** |
| Bruk avanserte parametere | Blank |
| Sertifikat | Blank |
| Svartypen – XML | **Nei** |
| Forespørselsmetode | **GET** |
| Godta | **program/json** |
| Godta koding | Blank |
| Forespørselshoder | Blank |
| Innholdstype | Blank |
| Formattilordning for forespørselshode | **Format for webforespørselshoder for Altinn mva (NO)** |
| Kode for fullført svar | **200** |

### <a name="web-service-no-altinn-post-json"></a>Webtjeneste: NO Altinn POST JSON

| Parameternavn | Parameterverdi |
|---|---|
| Nettjeneste | **NO Altinn POST JSON** |
| Beskrivelse | **Altinn-webtjeneste for POST-forespørsler av JSON-type innhold** |
| Internett-adresse | `https://skd.apps.tt02.altinn.no/skd/mva-melding-innsending-etm2/instances` |
| Nettsøknad | **NO Altinn** |
| Bruk proxy-server | **Nei** |
| Bruk avanserte parametere | Blank |
| Sertifikat | Blank |
| Svartypen – XML | **Nei** |
| Forespørselsmetode | **POST** |
| Godta | Blank |
| Godta koding | Blank |
| Forespørselshoder | Blank |
| Innholdstype | **program/json** |
| Formattilordning for forespørselshode | **Format for webforespørselshoder for Altinn mva (NO)** |
| Kode for fullført svar | **201** |

### <a name="web-service-no-altinn-post-xml"></a>Webtjeneste: NO Altinn POST XML

| Parameternavn | Parameterverdi |
|---|---|
| Nettjeneste | **NO Altinn POST XML** |
| Beskrivelse | **Altinn-webtjeneste for POST-forespørsler av XML-type innhold** |
| Internett-adresse | `https://skd.apps.tt02.altinn.no/skd/mva-melding-innsending-etm2/instances` |
| Nettsøknad | **NO Altinn** |
| Bruk proxy-server | **Nei** |
| Bruk avanserte parametere | Blank |
| Sertifikat | Blank |
| Svartypen – XML | **Nei** |
| Forespørselsmetode | **POST**|
| Godta | Blank |
| Godta koding | Blank |
| Forespørselshoder | Blank |
| Innholdstype | **tekst/xml** |
| Formattilordning for forespørselshode | **Format for webforespørselshoder for Altinn mva (NO)** |
| Kode for fullført svar | **201** |

### <a name="web-service-no-altinn-put-json"></a>Webtjeneste: NO Altinn PUT JSON

| Parameternavn | Parameterverdi |
|---|---|
| Nettjeneste | **NO Altinn PUT JSON** |
| Beskrivelse | **Altinn-webtjeneste for PUT-forespørsler av JSON-type innhold** |
| Internett-adresse | `https://skd.apps.tt02.altinn.no/skd/mva-melding-innsending-etm2/instances` |
| Nettsøknad | **NO Altinn** |
| Bruk proxy-server | **Nei** |
| Bruk avanserte parametere | Blank |
| Sertifikat | Blank |
| Svartypen – XML | **Nei** |
| Forespørselsmetode | **PUT** |
| Godta | Blank |
| Godta koding | Blank |
| Forespørselshoder | Blank |
| Innholdstype | **program/json** |
| Formattilordning for forespørselshode | **Format for webforespørselshoder for Altinn mva (NO)** |
| Kode for fullført svar | **200** |

### <a name="web-service-no-altinn-put-xml"></a>Webtjeneste: NO Altinn PUT XML

| Parameternavn | Parameterverdi |
|---|---|
| Nettjeneste | **NO Altinn PUT XML** |
| Beskrivelse | **Altinn-webtjeneste for PUT-forespørsler av XML-type innhold** |
| Internett-adresse | `https://skd.apps.tt02.altinn.no/skd/mva-melding-innsending-etm2/instances` |
| Nettsøknad | **NO Altinn** |
| Bruk proxy-server | **Nei** |
| Bruk avanserte parametere | Blank |
| Sertifikat | Blank |
| Svartypen – XML | **Nei** |
| Forespørselsmetode | **PUT** |
| Godta | Blank |
| Godta koding | Blank |
| Forespørselshoder | Blank |
| Innholdstype | **application/xml** |
| Formattilordning for forespørselshode | **Format for webforespørselshoder for Altinn mva (NO)** |
| Kode for fullført svar | **201** |

### <a name="web-service-no-validate-vat-return"></a>Webtjeneste: NO Valider mva-retur

| Parameternavn | Parameterverdi |
|---|---|
| Nettjeneste | **NO Valider mva-retur** |
| Beskrivelse | **Webtjenesten for skatteadministrasjon for å validerer mva-innbetaling** |
| Internett-adresse | `https://mp-test.sits.no/api/mva/grensesnittstoette/mva-melding/valider` |
| Nettsøknad | **NO ID-Porten** |
| Bruk proxy-server | **Nei** |
| Bruk avanserte parametere | Blank |
| Sertifikat | Blank |
| Svartypen – XML | **Nei** |
| Forespørselsmetode | **POST** |
| Godta | Blank |
| Godta koding | Blank |
| Forespørselshoder | Blank |
| Innholdstype | **application/xml** |
| Formattilordning for forespørselshode | **Format for webforespørselshoder for Altinn mva (NO)** |
| Kode for fullført svar | **200** |

## <a name="additional-fields"></a>Tilleggsfelter

- Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Tilleggsfelt**, og se gjennom oppsettet. **NO mva-retur** bruker følgende tilleggsfelt.

    | Felt | Beskrivelse (norsk) | Brukerredigering | Teller | Skjult |
    |---|---|---|---|---|
    | NO mva Data-GUID | Data-GUID | Nei | Nei | Ja |
    | NO mva Forekomst-GUID | Forekomst-GUID | Nei | Nei | Ja |
    | NO mva-notat for mva-retur | Merknad på meldingsnivå: har en kan velge mellom en predefinert liste av merknader eller fylle ut fritekst | Ja | Nei | Nei |
    | NO mva part-ID | Part-ID | Nei | Nei | Ja |
    | NO mva Betalingsinformasjon | Betalingsinformasjon | Nei | Nei | Ja |
    | NO mva Kvittering | Kvittering | Nei | Nei | Ja |
    | NO mva Valideringsresultat | Valideringsresultat | Nei | Nei | Ja |
    | Avgiftsregistreringsnummer | Skatteregistreringsnummer | Nei | Nei | Ja |

    > [!NOTE]
    > Brukeren kan ikke endre innstillingene i noen av disse feltene.

## <a name="electronic-message-item-types"></a>Typer elektronisk meldingselement

- Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Typer meldingselement**, og se gjennom oppsettet. Behandlingen **NO mva-retur** bruker én type elektronisk meldingselement: **NO mva-retur**.

## <a name="electronic-message-item-statuses"></a>Statuser for elektronisk meldingselement

- Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Statuser for meldingselement**, og se gjennom oppsettet. Behandlingen **NO mva-retur** bruker følgende statuser for elektronisk meldingselement.

    | Status | Beskrivelse | Tillat sletting |
    |---|---|---|
    | NO mva innkrevd | Mva-betalingspost som er inkludert for mva-retur (Momsregistrering inkludert for mva-retur). | Ja |
    | NO mva ekskludert | Mva-betaling ekskludert fra mva-retur (Innbetaling av merverdiavgift ekskludert fra mva). | Ja |
    | Som skal rapporteres | Mva-betalingspost klar for mva-retur (Momsregistrering er klar for merverdiavgift). | Nei |

## <a name="electronic-message-statuses"></a>Statuser for elektronisk melding

- Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Meldingsstatuser**, og se gjennom oppsettet. Behandlingen **NO mva-retur** bruker følgende elektroniske meldingsstatuser.

    | Status | Beskrivelse (norsk) | Svartype | Tillat sletting |
    |---|---|---|---|
    | NO mva-feil ved gjennomf;ring av mva-innsending | Feil ved gjennomføring av innsending av mva | TechnicalError | Nei |
    | NO mva Feil nedlasing av fil | Feil nedlasting av fil | TechnicalError | Nei |
    | NO MVA Feil generering av forespørsel | Feil generering av forespørsel | TechnicalError | Nei |
    | NO mva Feil generering av momsoppgave | Feil generering av momsoppgave | TechnicalError | Nei |
    | NO MVA Feil under import av opprettelsesforekomster | Feil under import av opprettelsesforekomster | TechnicalError | Nei |
    | NO MVA Tilbakemelding ved importfeil | Tilbakemelding ved importfeil | TechnicalError | Nei |
    | NO mva Feil ved import av tilbakemeldingsstatusrespons | Feil ved import av tilbakemeldingsstatusrespons | TechnicalError | Nei |
    | NO MVA Feil ved import av endelig valideringsresultat | Feil ved import av endelig valideringsresultat | TechnicalError | Nei |
    | NO mva Feil under import av mva-returvalideringsresultat | Feil under import av mva-returvalideringsresultat | TechnicalError | Nei |
    | NO mva Feil ved fullføring av data | Feil ved fullføring av data | TechnicalError | Nei |
    | NO mva Feil ved opprettelse av forekomst | Feil ved opprettelse av forekomst | BusinessError | Nei |
    | NO mva Feil ved sending av forespørsel om tilbakemelding | Feil ved sending av forespørsel om tilbakemelding | TechnicalError | Nei |
    | NO mva Feil ved sending av forespørsel om status for tilbakemelding | Feil ved sending av forespørsel om status for tilbakemelding | TechnicalError | Nei |
    | NO mva Feil ved sending av forespørsel for å opprette en forekomst | Feil ved sending av forespørsel for å opprette en forekomst | TechnicalError | Nei |
    | NO mva Feil ved sending av forespørsel om validering av mva | Feil ved sending av forespørsel om validering av mva | TechnicalError | Nei |
    | NO mva Feilvalidering av opplastet MVA-melding | Feilvalidering av opplastet MVA-melding | BusinessError | Nei |
    | NO mva Mva-returgenereringsfeil | Mva-returgenereringsfeil | TechnicalError | Ja |
    | NO mva Melding om opplasting av mva | Melding om opplasting av mva | TechnicalError | Nei |
    | NO mva Mva-returvalideringsfeil | Mva-returvalideringsfeil | BusinessError | Nei |
    | NO MVA Tilbakemeldinger importert | Tilbakemeldinger importert | Vellykket | Nei |
    | NO MVA Tilbakemelding tilbys ikke | Tilbakemelding tilbys ikke | Vellykket | Nei |
    | NO MVA Tilbakemelding tilbys | Tilbakemelding tilbys | Vellykket | Nei |
    | NO MVA Forekomst opprettet | Forekomst opprettet | Vellykket | Nei |
    | NO MVA Ny elektronisk melding opprettet | Ny elektronisk melding opprettet | Vellykket | Ja |
    | NO MVA Klar til å generere mva | Klar til å generere mva | Vellykket | Nei |
    | NO MVA Mva-meldingen er levert og mottatt av Skatteetaten | Mva-meldingen er levert og mottatt av Skatteetaten | Vellykket | Nei |
    | NO MVA Mva-returnering fullført | Mva-returnering fullført | Vellykket | Nei |
    | NO MVA Mva-returinnleveringsforespørsel generert | Mva-returinnleveringsforespørsel generert | Vellykket | Nei |
    | NO MVA Innlevering av merverdiavgift ble lastet opp | Innlevering av merverdiavgift ble lastet opp | Vellykket | Nei |
    | NO MVA Melding om returopplastingsfeil | Melding om returopplastingsfeil | TechnicalError | Nei |
    | NO MVA Mva-retur lastet opp | Mva-retur lastet opp | Vellykket | Nei |
    | NO MVA-retur validert og klar til å lastes opp | Momsangivelsen ble godkjent av Skatteetaten og klar til å lastes opp til Altinn | Vellykket | Nei |
    | NO MVA-returvalidering bestått | Mva-returvalidering bestått | Vellykket | Nei |
    | NO MVA XML-generert mva-retur er vellykket | Mva-retur er vellykket generert i XML-format | Vellykket | Ja |
    | NO MVA Sendt forespørsel om tilbakemelding | Sendt forespørsel om tilbakemelding | Vellykket | Nei |
    | NO MVA Sendt forespørsel om status for tilbakemelding | Sendt forespørsel om status for tilbakemelding | Vellykket | Nei |
    | NO MVA Returvalideringsforespørsel sendt | Returvalideringsforespørsel sendt | Vellykket | Nei |
    | NO MVA Vellykket nedlasting av endelig validering | Vellykket nedlasting av endelig validering | Vellykket | Nei |
    | NO MVA Last ned filen vellykket | Last ned filen vellykket | Vellykket | Nei |
    | NO MVA Sendingen oppretter forespørsel om vellykket sending | Sendingen oppretter forespørsel om vellykket sending | Vellykket | Nei |
    | NO MVA MVA-meldingen lastet opp til Skatteetaten ble validert | MVA-meldingen lastet opp til Skatteetaten ble validert | Vellykket | Nei |

## <a name="action-populate-records"></a>Handlingen Fyll ut poster

- Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Handlinger for Fyll ut poster**, og se gjennom oppsettet. **NO mva-retur** bruker én **NO MVA Samle inn mva-betaling**-handling for utfylling av poster.

Tabellen nedenfor viser oppsettet til datakilden for **NO MVA Samle inn mva-betaling**-handling for utfylling av poster som **NO mva-retur** bruker.

| Egenskap | Verdi |
|---|---|
| Navn | NO mva-retur |
| Type meldingselement | NO mva-retur |
| Kontotype | Alle |
| Navn på hovedtabell | TaxReportVoucher |
| Feltet Dokumentnummer | Bilag |
| Feltet Dokumentdato | TransDate |
| Feltet Dokumentkonto | TaxPeriod |
| Brukerspørring | Ja |

> [!IMPORTANT]
> Definer utligningsperioden ved å velge **Rediger spørring**. Hvis du vil ha mer informasjon, kan du se [Definer en mva-utligningsperiode](emea-nor-vat-return-setup.md#settlement-period).

## <a name="electronic-message-actions"></a>Elektroniske meldinger-handlinger

1. Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Behandling av elektronisk melding** og se gjennom oppsettet. Behandlingen **NO mva-retur** bruker følgende elektronisk melding-handlinger.

    | Rekkefølge | Handling | Beskrivelse (norsk) | Sekvens som ikke kan skilles | Kjør separat |
    |---|---|---|---|---|
    | 1 | NO MVA Opprett melding | Lag melding | Blank | **Nei** |
    | 2 | NO MVA Samle inn mva-betaling | Samle momsregistreringer for merverdiavgift | Blank | **Nei** |
    | 3 | NO MVA Klar til å generere mva | Klar til å generere mva | Blank | **Ja** |
    | 4 | NO MVA Ikke klar til å generere mva | Elektronisk melding er ikke klar til å generere merverdiavgi | Blank | **Ja** |
    | 5 | NO MVA Forhåndsvisning av mva-retur i Excel | Forhåndsvis mva-retur i Excel | Blank | **Ja** |
    | 6 | NO MVA Generer MVA-innbetaling | Generer merverdiavgift i XML | **NO MVA Validering** | **Ja** | 
    | 7 | NO MVA Send forespørsel om validering | Send forespørsel om validering | **NO MVA Validering** | **Ja** | 
    | 8 | NO MVA Importer valideringssvar | Importer valideringssvar | **NO MVA Validering** | **Nei** |
    | 9 | NO MVA Generer forespørsel om forekomst | Generer forespørsel om å opprette forekomst | **NO MVA Validering** | **Nei** |
    | 10 | NO MVA Send forespørsel om å opprette forekomst | Send forespørsel for å opprette forekomst | **NO MVA Innsending** | **Ja** |
    | 11 | NO MVA Importer opprettelsessvar for forekomst | Importer opprettelsessvar for forekomst | **NO MVA Innsending** | **Nei** |
    | 12 | NO MVA Generer innsending av mva | Generer innsending av mva | **NO MVA Innsending** | **Nei** |
    | 13 | NO MVA Last opp innsending av mva | Last opp innsending av merverdiavgift | **NO MVA Innsending** | **Nei** |
    | 14 | NO MVA Last opp mva-retur | Last opp mva-retur | **NO MVA Innsending** | **Nei** |
    | sept. | NO MVA Fullstendig datafylling | Fullstendige datafylling | **NO MVA Innsending** | **Nei** |
    | 16 | NO MVA Fullfør innsending av MVA-retur | Fullfør momsoppgaven | **NO MVA Innsending** | **Nei** |
    | 17 | NO MVA Send statusforespørsel om tilbakemelding | Send statusforespørsel om tilbakemelding | **NO MVA Innsending** | **Nei** |
    | 18 | NO MVA Importer tilbakemeldingsstatusrespons | Importer tilbakemeldingsstatusrespons | **NO MVA Innsending** | **Nei** |
    | 19 | NO MVA Send forespørsel om tilbakemelding | Send forespørsel om tilbakemelding | **NO MVA Innsending** | **Nei** |
    | 20 | NO MVA Importer tilbakemeldingssvar | Importer tilbakemeldingssvar | **NO MVA Innsending** | **Nei** |
    | 21 | NO MVA Last ned valideringsresultat | Siste ned valideringsresultat | **NO MVA Innsending** | **Nei** |
    | 22 | NO MVA Import endelig valideringsresultat | Import endelig valideringsresultat | **NO MVA Innsending** | **Nei** |
    | 23 | NO MVA Last ned betalingsinformasjon | Last ned betalingsinformasjon | Blank | **Ja** |
    | 24 | NO MVA Last ned kvittering | Last ned kvittering | Blank | **Ja** |
    | 25 | NO MVA Ekskluder fra MVA-retur | Innbetaling av merverdiavgift ekskludert fra mva | Blank | **Ja** |
    | 26 | NO MVA Inkluder til MVA-retur | Inkluder betaling av omsetningsavgift til mva | Blank | **Ja** |

2. Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Handlinger for meldingsbehandling** og se gjennom oppsettet. Følgende parametere må defineres for handlingene.

    | Handling | Handlingstype | Parametere |
    |---|---|---|
    | NO MVA Opprett melding | Opprett melding | <ul><li>**Fra-statuser:** No</li><li>**Til-statuser:** NO MVA Ny melding opprettet</li></ul> |
    | NO MVA Samle inn mva-betaling | Fyll ut poster | <ul><li>**Handling for Fyll ut poster:** NO MVA Samle inn mva-betaling</li><li>**Fra-statuser:** NO MVA Ny melding opprettet</li><li>**Til-statuser:** NO MVA Innkrevd</li></ul> |
    | NO MVA Klar til å generere mva | Behandling av bruker på meldingsnivå | <ul><li>**Fra-statuser:** NO MVA Ny melding opprettet</li><li>**Til-statuser:** NO MVA Klar til å generere mva</li></ul> |
    | NO MVA Ikke klar til å generere mva | Behandling av bruker på meldingsnivå | <ul><li>**Fra-statuser:** NO MVA Klar til å generere, NO MVA-retur validert og klar til å lastes opp, NO MVA XML-generert mva-retur er vellykket</li><li>**Til-statuser:** NO MVA Ny melding opprettet</li></ul> |
    | NO MVA Forhåndsvisning av mva-retur i Excel | Melding om eksport av elektronisk rapportering | <ul><li>**Meldingselementtype:** NO mva-retur</li><li>**Formattilordning:** MVA-deklarering Excel (NO)</li><li>**Fra-statuser:** NO MVA Mva-returgenereringsfeil, NO MVA Mva-returvalideringsfeil, NO MVA Klar til å generere mva</li><li>**Til-statuser:** NO MVA Mva-returgenereringsfeil, NO MVA Klar til å generere mva</li></ul> |
    | NO MVA Generer MVA-innbetaling | Melding om eksport av elektronisk rapportering | <ul><li>**Filnavn:** mvamelding</li><li>**Meldingselementtype:** NO mva-retur</li><li>**Formattilordning:** MVA-deklarering XML (NO)</li><li>**Fra-statuser:** NO MVA Feil ved sending av forespørsel om validering av mva, NO MVA Feilvalidering av opplastet MVA-melding, NO MVA Mva-returgenereringsfeil, NO MVA Mva-returvalideringsfeil, NO MVA Klar til å generere mva, NO MVA XML-generert mva-retur er vellykket</li><li>**Til-statuser:** NO MVA XML-generert mva-retur er vellykket, NO MVA Mva-returgenereringsfeil</li></ul> |
    | NO MVA Send forespørsel om validering | Nettjeneste | <ul><li>**Webtjeneste:** NO Valider mva-retur</li><li>**Filnavn:** valideringsresultat.xml</li><li>**Filnavn som skal sendes:** mvamelding.xml</li><li>**Fra-statuser:** NO MVA Feil ved sending av forespørsel om validering av mva, NO MVA Mva-returvalideringsfeil, NO MVA XML-generert mva-retur er vellykket</li><li>**Til-statuser:** NO MVA Feil ved sending av forespørsel om validering av mva, NO MVA Returvalideringsforespørsel sendt</li></ul> |
    | NO MVA Importer valideringssvar | Import av elektronisk rapportering | <ul><li>**Modelltilordning:** Resultatformat for Altinn-importvalidering (NO)</li><li>**Fra-statuser:** NO MVA Feil under import av mva-returvalideringsresultat, NO MVA Returvalideringsforespørsel sendt</li><li>**Til-statuser:** NO MVA Feil under import av mva-returvalideringsresultat, NO MVA Mva-returvalideringsfeil, NO MVA-returvalidering bestått</li></ul> |
    | NO MVA Generer forespørsel om forekomst | Melding om eksport av elektronisk rapportering | <ul><li>**Filnavn:** createInstanceRequest.json</li><li>**Formattilordning:** Altinn mva-samhandling (NO)</li><li>**Frasstatuser:** NO MVA Feil generering av forespørsel, NO MVA Feil ved opprettelse av forekomst, NO MVA Feil ved sending av forespørsel for å opprette en forekomst, NO MVA-returvalidering bestått</li><li>**Til-statuser:** NO MVA Feil generering av forespørsel, NO MVA-retur validert og klar til å lastes opp</li></ul> |
    | NO MVA Send forespørsel om å opprette forekomst | Nettjeneste | <ul><li>**Filnavn:** createInstanceResponse.json</li><li>**Webtjeneste:** NO Altinn POST JSON</li><li>**Fra-statuser:** NO MVA Feil ved sending av forespørsel for å opprette en forekomst, NO MVA-retur validert og klar til å lastes opp</li><li>**Til-statuser:** NO MVA Feil ved sending av forespørsel for å opprette en forekomst, NO MVA Sendingen oppretter forespørsel om vellykket sending</li></ul> |
    | NO MVA Importer opprettelsessvar for forekomst | Import av elektronisk rapportering | <ul><li>**Modelltilordning:** Altinn mva-importforekomstformat (NO)</li><li>**Fra-statuser:** NO MVA Feil under import av opprettelsesforekomster, NO MVA Sendingen oppretter forespørsel om vellykket sending</li><li>**Til-statuser:** NO MVA Feil under import av opprettelsesforekomster, NO MVA Feil ved opprettelse av forekomst, NO MVA Forekomst opprettet</li></ul> |
    | NO MVA Generer innsending av mva | Melding om eksport av elektronisk rapportering | <ul><li>**Filnavn:** konvolutt.xml</li><li>**Formattilordning:** MVA-deklarering XML (NO)</li><li>**Fra-statuser:** NO MVA Feil generering av momsoppgave, NO MVA Forekomst opprettet</li><li>**Til-statuser:** NO MVA Feil generering av momsoppgave, NO MVA Mva-returinnleveringsforespørsel generert</li></ul> |
    | NO MVA Last opp innsending av mva | Nettjeneste | <ul><li>**Formattilordning for URL-bane:** Altinn mva-samhandling (NO)</li><li>**Webtjeneste:** NO Altinn PUT XML</li><li>**Filnavn:** uploadVATReturnSubmissionResponse.json</li><li>**Fra-statuser:** NO MVA Mva-returinnleveringsforespørsel generert, NO MVA Melding om returopplastingsfeil</li><li>**Til-statuser:** NO MVA Innlevering av merverdiavgift ble lastet opp, NO MVA Melding om returopplastingsfeil</li></ul> |
    | NO MVA Last opp mva-retur | Nettjeneste | <ul><li>**Formattilordning for URL-bane:** Altinn mva-samhandling (NO)</li><li>**Webtjeneste:** NO Altinn POST XML</li><li>**Filnavn:** uploadVATReturnResponse.json</li><li>**Filnavn som skal sendes:** mvamelding.xml</li><li>**Fra-statuser:** NO MVA Melding om opplasting av mva, NO MVA Innlevering av merverdiavgift ble lastet opp</li><li>**Til-statuser:** NO MVA Melding om opplasting av mva, NO MVA Mva-retur lastet opp</li></ul> |
    | NO MVA Fullstendig datafylling | Nettjeneste | <ul><li>**Formattilordning for URL-bane:** Altinn mva-samhandling (NO)</li><li>**Webtjeneste:** NO Altinn PUT JSON</li><li>**Filnavn:** completeDataFillingResponse.json</li><li>**Filnavn som skal sendes:** *Gjelder ikke*</li><li>**Fra-statuser:** NO MVA Feil ved fullføring av data, NO MVA Mva-retur lastet opp</li><li>**Til-statuser:** NO MVA Datautfylling fullført, NO MVA Feil ved fullføring av data</li></ul> |
    | NO MVA Fullfør innsending av MVA-retur | Nettjeneste | <ul><li>**Formattilordning for URL-bane:** Altinn mva-samhandling (NO)</li><li>**Webtjeneste:** NO Altinn PUT JSON</li><li>**Filnavn:** completeVATReturnSubmissionResponse.json</li><li>**Filnavn som skal sendes:** *Gjelder ikke*</li><li>**Fra-statuser:** NO MVA Datautfylling fullført, NO MVA Feil generering av momsoppgave</li><li>**Til-statuser:** NO MVA Feil generering av momsoppgave, NO MVA Mva-returnering fullført</li></ul> |
    | NO MVA Send statusforespørsel om tilbakemelding | Nettjeneste | <ul><li>**Formattilordning for URL-bane:** Altinn mva-samhandling (NO)</li><li>**Webtjeneste:** NO Altinn GET JSON</li><li>**Filnavn:** feedbackStatusResponse.json</li><li>**Filnavn som skal sendes:** *Gjelder ikke*</li><li>**Fra-statuser:** NO MVA Feil ved sending av forespørsel om status for tilbakemelding, NO MVA Tilbakemelding tilbys ikke, NO MVA Mva-returnering fullført</li><li>**Til-statuser:** NO MVA Feil ved sending av forespørsel om status for tilbakemelding, NO MVA Sendt forespørsel om status for tilbakemelding</li></ul> |
    | NO MVA Importer tilbakemeldingsstatusrespons | Import av elektronisk rapportering | <ul><li>**Modelltilordning:** Format for tilbakemelding om Altinn mva-import (NO)</li><li>**Fra-statuser:** NO MVA Feil ved import av tilbakemeldingsstatusrespons, NO MVA Sendt forespørsel om status for tilbakemelding</li><li>**Til-statuser:** NO MVA Feil ved import av tilbakemeldingsstatusrespons, NO MVA Tilbakemelding tilbys ikke, NO MVA Tilbakemelding tilbys</li></ul> |
    | NO MVA Send forespørsel om tilbakemelding | Nettjeneste | <ul><li>**Formattilordning for URL-bane:** Altinn mva-samhandling (NO)</li><li>**Webtjeneste:** NO Altinn GET JSON</li><li>**Filnavn som skal sendes:** *Gjelder ikke*</li><li>**Filnavn:** feedbackResponse.json</li><li>**Fra-statuser:** NO MVA Feil ved sending av forespørsel om tilbakemelding, NO MVA Tilbakemelding tilbys</li><li>**Til-statuser:** NO MVA Feil ved sending av forespørsel om tilbakemelding, NO MVA Sendt forespørsel om tilbakemelding</li></ul> |
    | NO MVA Importer tilbakemeldingssvar | Import av elektronisk rapportering | <ul><li>**Modelltilordning:** Altinn mva-importforekomstformat (NO)</li><li>**Fra-statuser:** NO MVA Tilbakemelding ved importfeil, NO MVA Sendt forespørsel om tilbakemelding</li><li>**Til-statuser:** NO MVA Tilbakemelding ved importfeil, NO MVA Tilbakemeldinger importert, NO MVA Mva-meldingen er levert og mottatt av Skatteetaten</li></ul> |
    | NO MVA Last ned valideringsresultat | Nettjeneste | <ul><li>**Formattilordning for URL-bane:** Altinn mva-samhandling (NO)</li><li>**Webtjeneste:** NO Altinn GET-vedlegg</li><li>**Filnavn:** valideringsresultat.xml</li><li>**Filnavn som skal sendes:** *Gjelder ikke*</li><li>**Fra-statuser:** NO MVA Feil nedlasting av fil, NO MVA Tilbakemeldinger importert, NO MVA Mva-meldingen er levert og mottatt av Skatteetaten, NO MVA Last ned filen vellykket, NO MVA MVA-meldingen lastet opp til Skatteetaten ble validert</li><li>**Til-statuser:** NO MVA Feil nedlasing av fil, NO MVA Vellykket nedlasting av endelig validering</li></ul> |
    | NO MVA Import endelig valideringsresultat | Import av elektronisk rapportering | <ul><li>**Modelltilordning:** Resultatformat for Altinn-importvalidering (NO)</li><li>**Fra-statuser:** NO MVA Feil ved import av endelig valideringsresultat, NO MVA Vellykket nedlasting av endelig validering</li><li>**Til-statuser:** NO MVA Feil ved import av endelig valideringsresultat, NO MVA Feilvalidering av opplastet MVA-melding, NO MVA MVA-meldingen lastet opp til Skatteetaten ble validert</li></ul> |
    | NO MVA Last ned betalingsinformasjon | Nettjeneste | <ul><li>**Formattilordning for URL-bane:** Altinn mva-samhandling (NO)</li><li>**Webtjeneste:** NO Altinn GET-vedlegg</li><li>**Filnavn:** vbetalingsinformasjon.xml</li><li>**Filnavn som skal sendes:** *Gjelder ikke*</li><li>**Fra-statuser:** NO MVA Feil nedlasing av fil, NO MVA Last ned filen vellykket, NO MVA MVA-meldingen lastet opp til Skatteetaten ble validert</li><li>**Til-statuser:** NO MVA Feil nedlasing av fil, NO MVA Last ned filen vellykket</li></ul> |
    | NO MVA Last ned kvittering | Nettjeneste | <ul><li>**Formattilordning for URL-bane:** Altinn mva-samhandling (NO)</li><li>**Webtjeneste:** NO Altinn GET-vedlegg</li><li>**Filnavn:** kvittering.pdf</li><li>**Filnavn som skal sendes:** *Gjelder ikke*</li><li>**Fra-statuser:** NO MVA Feil nedlasing av fil, NO MVA Last ned filen vellykket, NO MVA MVA-meldingen lastet opp til Skatteetaten ble validert</li><li>**Til-statuser:** NO MVA Feil nedlasing av fil, NO MVA Last ned filen vellykket</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
