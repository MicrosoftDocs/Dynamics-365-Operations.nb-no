---
title: Common Data Service-enheter
description: Microsoft Dynamics 365 Human Resources bruker Common Data Service til å aktivere scenarioer for utvidbarhet og integrering.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85dd95e8209fff28f214986f7960372db200351b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010119"
---
# <a name="common-data-service-entities"></a>Common Data Service-enheter

Microsoft Dynamics 365 Human Resources bruker Common Data Service til å aktivere scenarioer for utvidbarhet og integrering.

Hvis du vil ha mer informasjon om Common Data Service, kan du se [Hva er Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Følgende Human Resources-enheter er tilgjengelige i Common Data Service.

## <a name="benefit-entities"></a>Fordelsenheter

**Fordelsberegningsfrekvens**

| **Felt**        | **Datatype** | **Obligatorisk** | **Søkbar** |
|-------------------|---------------|--------------|----------------|
| Beskrivelse       | Text          |              | X              |
| Frekvenskontroll | Alternativsett    | X            | X              |
| Er uforanderlig      | To alternativer   |              | X              |
| Navn              | Text          | X            | X              |


**Beregningssats for fordeler**

| **Felt**  | **Datatype** | **Obligatorisk** | **Søkbar** |
|-------------|---------------|--------------|----------------|
| Beskrivelse | Text          |              | X              |
| Navn        | Text          | X            | X              |
| TierType    | Alternativsett    | X            | X              |


**Detaljer om beregningssats for fordeler**

| **Felt**                             | **Datatype**  | **Obligatorisk** | **Søkbar** |
|----------------------------------------|----------------|--------------|----------------|
| Detaljnummer for beregningssats for fordeler | Text           | X            | X              |
| ID for beregningssats                    | Oppslag         | X            | X              |
| Bidragsmetode                    | Alternativsett     | X            | X              |
| Effektiv                              | Bare dato      | X            | X              |
| Arbeidsgiverbidrag                  | Desimaltall |              | X              |
| Utløp                             | Bare dato      | X            | X              |
| WorkerDeduction                        | Desimaltall |              | X              |


**Fordelstype**

| **Felt**           | **Datatype** | **Obligatorisk** | **Søkbar** |
|----------------------|---------------|--------------|----------------|
| ConcurrentEnrollment | Alternativsett    |              | X              |
| Beskrivelse          | Text          |              | X              |
| Navn                 | Text          | X            | X              |
| PayrollCategory      | Alternativsett    |              | X              |


**Fordelsplan**

| **Felt**                               | **Datatype**  | **Obligatorisk** | **Søkbar** |
|------------------------------------------|----------------|--------------|----------------|
| Metode for etterskuddsgrense                      | Alternativsett     |              | X              |
| Fordelstype                             | Oppslag         | X            | X              |
| Metode for bidragsgrense                | Alternativsett     |              | X              |
| Bidragsmetode                      | Alternativsett     |              | X              |
| Valuta                                 | Oppslag         |              | X              |
| Fradragsprioritet                       | Heltall   |              | X              |
| Standard bidragsgrensebeløp        | Valuta       |              | X              |
| Standard bidragsgrensebeløp (basis) | Valuta       |              | X              |
| Standard bidragsgrenseperiode        | Alternativsett     |              | X              |
| Standard fradragsgrensebeløp           | Valuta       |              | X              |
| Standard fradragsgrensebeløp (basis)    | Valuta       |              | X              |
| Standard fradragsgrenseperiode           | Alternativsett     |              | X              |
| Beskrivelse                              | Text           |              | X              |
| Valutakurs                            | Desimaltall |              | X              |
| Er ekstra lønnskjøring                | To alternativer    |              | X              |
| Er rapporteringsplikt for lov om Affordable Care        | To alternativer    |              | X              |
| Er etterskuddsgenerert                      | To alternativer    |              | X              |
| Er brutto                              | To alternativer    |              | X              |
| Er primær                               | To alternativer    |              | X              |
| Navn                                     | Text           | X            | X              |
| Lønnsinnvirkning                           | Alternativsett     |              | X              |
| Pensjonstype                          | Alternativsett     |              | X              |


**Ansettelsesenhet**

| **Felt**                     | **Datatype**  | **Obligatorisk** | **Søkbar** |
|--------------------------------|----------------|--------------|----------------|
| Justert startdato for arbeider     | Dato og klokkeslett  |              | X              |
| Bedrift                        | Oppslag         | X            | X              |
| Arbeidsgiverenhet for oppsigelsesvarsel | Desimaltall |              | X              |
| Oppsigelsesenhet for arbeidsgiver        | Alternativsett     |              | X              |
| Sluttdato for ansettelse            | Dato og klokkeslett  |              | X              |
| Ansettelsesnummer              | Text           | X            | X              |
| Startdato for ansettelse          | Dato og klokkeslett  |              | X              |
| Siste arbeidsdag              | Dato og klokkeslett  |              | X              |
| Overgangsdato                | Dato og klokkeslett  |              | X              |
| Gyldig fra                     | Dato og klokkeslett  | X            | X              |
| Gyldig til                       | Dato og klokkeslett  |              | X              |
| Arbeider                         | Oppslag         | X            | X              |
| Oppsigelsesvarsel for arbeider           | Desimaltall |              | X              |
| Arbeiderens startdato             | Dato og klokkeslett  |              | X              |
| Arbeidertype                    | Alternativsett     | X            | X              |
| Oppsigelsesenhet for arbeider          | Alternativsett     |              | X              |

## <a name="worker-entities"></a>Arbeiderenheter

**Etnisk opprinnelse**

| **Felt**         | **Datatype** | **Obligatorisk** | **Søkbar** |
|--------------------|---------------|--------------|----------------|
| Beskrivelse        | Text          |              | X              |
| Navn på etnisk opprinnelse | Text          | X            | X              |


**Språk**

| **Felt**    | **Datatype** | **Obligatorisk** | **Søkbar** |
|---------------|---------------|--------------|----------------|
| Beskrivelse   | Text          |              | X              |
| Navn på språk | Text          | X            | X              |


**Veteranstatus**

| **Felt**           | **Datatype** | **Obligatorisk** | **Søkbar** |
|----------------------|---------------|--------------|----------------|
| Beskrivelse          | Text          |              | X              |
| Er beskyttet veteran | To alternativer    |              | X              |
| Navn på språk        | Text          | X            | X              |


**Arbeider**

| **Felt**                | **Datatype** | **Obligatorisk** | **Søkbar** |
|---------------------------|---------------|--------------|----------------|
| Fødselsdato                 | Bare dato     |              | X              |
| Beskrivelse               | Text          |              | X              |
| E-postadresse 1           | E-post         |              | X              |
| E-postadresse 2           | E-post         |              | X              |
| Facebook-ID         | Text          |              | X              |
| Fornavn                | Text          |              | X              |
| Fullt navn                 | Text          |              | X              |
| Kjønn                    | Alternativsett    |              | X              |
| Generering                | Text          |              | X              |
| Er e-postkontakt tilllatt  | To alternativer   |              | X              |
| Er telefonkontakt tilllatt  | To alternativer   |              | X              |
| Etternavn                 | Text          |              | X              |
| LinkedIn-ID         | Text          |              | X              |
| Leder                   | Oppslag        |              | X              |
| Mellomnavn               | Text          |              | X              |
| Mobiltelefon              | Telefon         |              | X              |
| Office Graph-ID   | Text          |              | X              |
| Primær e-postadresse     | E-post         |              | X              |
| Hovedtelefon         | Telefon         |              | X              |
| Yrke                | Text          |              | X              |
| Sosiale nettverk 1          | Alternativsett    |              | X              |
| Sosiale nettverk 2          | Alternativsett    |              | X              |
| ID for sosialt nettverk 1 | Text          |              | X              |
| ID for sosialt nettverk 2 | Text          |              | X              |
| Kilde                    | Alternativsett    | X            | X              |
| Status                    | Alternativsett    | X            | X              |
| Telefon 1               | Telefon         |              | X              |
| Telefon 2               | Telefon         |              | X              |
| Telefon 3               | Telefon         |              | X              |
| Twitter-identitet          | Text          |              | X              |
| Bruker                      | Oppslag        |              | X              |
| URL-adresse til nettsted               | URL-adresse           |              | X              |
| Arbeidernummer             | Text          | X            | X              |
| Arbeidertype               | Alternativsett    | X            | X              |
| Yomi fornavn           | Text          |              | X              |
| Yomi fullt navn            | Text          |              | X              |
| Yomi etternavn            | Text          |              | X              |
| Yomi mellomnavn          | Text          |              | X              |


**Arbeideradresse**

| **Felt**           | **Datatype**  | **Obligatorisk** | **Søkbar** |
|----------------------|----------------|--------------|----------------|
| Adressenummer       | Text           | X            | X              |
| Adressetype         | Alternativsett     | X            | X              |
| By                 | Text           |              | X              |
| Land eller område    | Text           |              | X              |
| Kommune               | Text           |              | X              |
| Faks                  | Telefon          |              | X              |
| Er foretrukket         | To alternativer    |              | X              |
| Breddegrad             | Desimaltall |              | X              |
| Linje 1               | Text           |              | X              |
| Linje 2               | Text           |              | X              |
| Linje 3               | Text           |              | X              |
| Lengdegrad            | Desimaltall |              | X              |
| Postnummer          | Text           |              | X              |
| Postboks      | Text           |              | X              |
| Kode for forsendelsesmåte | Heltall   |              | X              |
| Delstat eller provins    | Text           |              | X              |
| Telefon 1          | Telefon          |              | X              |
| Telefon 2          | Telefon          |              | X              |
| Telefon 3          | Telefon          |              | X              |
| UPS-sone             | Text           |              | X              |
| UTC-motregning           | Heltall   |              | X              |
| Arbeider               | Oppslag         | X            | X              |


**Arbeiderens personopplysninger**

| Felt                             | Datatype    | Obligatorisk | Søkbar |
|------------------------------------|--------------|----------|------------|
| Fødeby                         | Text         |          | X          |
| Fødested            | Alternativsett   |          | X          |
| Fødselsdato                          | Bare dato    |          | X          |
| Statsborgerskap      | Alternativsett   |          | X          |
| Dødsdato                      | Bare dato    |          | X          |
| Bekreftelsesdato for deaktivert veteran | Bare dato    |          | X          |
| Utdanning                          | Text         |          | X          |
| Etnisk opprinnelse                     | Oppslag       |          | X          |
| ExpatriateEndDate                  | Bare dato    |          | X          |
| ExpatriateStartDate                | Bare dato    |          | X          |
| Fars fødested     | Alternativsett   |          | X          |
| Kjønn                             | Alternativsett   |          | X          |
| Er deaktivert                        | To alternativer  |          | X          |
| Er ufør veteran                | To alternativer  |          | X          |
| Gjelder kjennelse om skattefradrag for personer som bor i utlandet    | To alternativer  |          | X          |
| Er fulltidsstudent               | To alternativer  |          | X          |
| Sivilstand                     | Alternativsett   |          | X          |
| Sluttdato for militærtjeneste          | Bare dato    |          | X          |
| Startdato for militærtjeneste        | Bare dato    |          | X          |
| Mors fødested     | Alternativsett   |          | X          |
| Nasjonalitet      | Alternativsett   |          | X          |
| Morsmål                    | Oppslag       |          | X          |
| Antall avhengige               | Heltall |          |            |
| Veteranstatus                     | Oppslag       |          | X          |
| Arbeider                             | Oppslag       | X        | X          |
| Personalnummer for arbeider      | Text         | X        | X          |


**Bankkonto for arbeider**

| **Felt**                 | **Datatype** | **Obligatorisk** | **Søkbar** |
|----------------------------|---------------|--------------|----------------|
| Kontoinnehaver             | Text          |              | X              |
| Kontoidentifikasjon     | Text          |              | X              |
| Adressebeskrivelse        | Text          |              | X              |
| Bankkontotype          | Alternativsett    |              | X              |
| Banklokasjonskode         | Text          |              | X              |
| Avdelingsnavn                | Text          |              | X              |
| Avdelingsnummer              | Text          |              | X              |
| By                       | Text          |              | X              |
| Land eller område          | Text          |              | X              |
| Kommune                     | Text          |              | X              |
| Beskrivelse                | Text          |              | X              |
| Distriktsnavn              | Text          |              | X              |
| E-post                      | Text          |              | X              |
| Direktenummer                  | Text          |              | X              |
| Faks                        | Text          |              | X              |
| IBAN                       | Text          |              | X              |
| Linje 1                     | Text          |              | X              |
| Linje 2                     | Text          |              | X              |
| Linje 3                     | Text          |              | X              |
| Mobiltelefon               | Text          |              | X              |
| Navn på personen             | Text          |              | X              |
| Postnummer                | Text          |              | X              |
| Postboks            | Text          |              |                |
| Registreringsnummer             | Text          |              | X              |
| Rutingsnummertype        | Alternativsett    |              | X              |
| Delstat eller provins          | Text          |              | X              |
| SWIFT-kode                 | Text          |              | X              |
| Telefon                  | Text          |              | X              |
| Teleksnummer               | Text          |              | X              |
| URL-adresse til nettsted                | Text          |              | X              |
| Arbeider                     | Oppslag        | X            | X              |
| Bankkontonummer for arbeider | Text          |              | X              |
| Bankkontonummer for arbeider | Text          | X            | X              |

**Fast kompensasjon for arbeider**

| Felt                                | Datatype      | Obligatorisk | Søkbar |
|---------------------------------------|----------------|----------|------------|
| Bedrift                               | Oppslag         | X        | X          |
| Kompensasjonstype                     | Alternativsett     |          | X          |
| Valuta                              | Oppslag         |          | X          |
| Ikrafttredelsesdato                        | Bare dato      |          | X          |
| Hendelse                                 | Oppslag         | X        | X          |
| Valutakurs                         | Desimaltall |          | X          |
| Utløpsdato                       | Bare dato      |          | X          |
| Linjenummer                           | Desimaltall |          | X          |
| Lønnsfrekvens                         | Oppslag         | X        | X          |
| Lønnssats                              | Valuta       |          | X          |
| Lønnssats (grunnlag)                       | Valuta       |          | X          |
| Plan                                  | Oppslag         | X        | X          |
| Posisjon                              | Oppslag         | X        | X          |
| Prosesstype                          | Alternativsett     | X        | X          |
| Linje i referansepunktoppsett            | Oppslag         |          | X          |
| Arbeider                                | Oppslag         | X        | X          |
| Fast kompensasjonstall for arbeidere      | Text           | X        | X          |

**Personidentifikasjonsnummer for arbeider**

| Felt                 | Datatype   | Obligatorisk | Søkbar |
|------------------------|-------------|----------|------------|
| Beskrivelse            | Text        |          | X          |
| Oppføringstype             | Text        |          | X          |
| Utløpsdato        | Bare dato   |          | X          |
| Identifikasjonsnummer  | Text        | X        | X          |
| Identifikasjonstype    | Oppslag      | X        | X          |
| Er primær             | To alternativer |          | X          |
| Utstedelsesdato             | Bare dato   |          | X          |
| Utstedende byrå         | Oppslag      | X        | X          |
| Arbeider                 | Oppslag      | X        | X          |


## <a name="position-entities"></a>Stillingsenheter

**Stilling**

| **Felt**               | **Datatype**  | **Obligatorisk** | **Søkbar** |
|--------------------------|----------------|--------------|----------------|
| Aktivering               | Dato og klokkeslett  |              | X              |
| Tilgjengelig for tilordning | Dato og klokkeslett  |              | X              |
| Avdeling               | Oppslag         |              | X              |
| Beskrivelse              | Text           |              | X              |
| Fulltidsekvivalent     | Desimaltall |              | X              |
| Stilling                      | Oppslag         | X            | X              |
| Stillingsnummer      | Text           | X            | X              |
| Overordnet jobbstilling      | Oppslag         |              | X              |
| Stillingstype            | Oppslag         |              | X              |
| Avgang ved pensjon               | Dato og klokkeslett  |              | X              |
| Stillingstittel                    | Alternativsett     |              | X              |
| Gyldig fra               | Dato og klokkeslett  | X            | X              |
| Gyldig til                 | Dato og klokkeslett  |              | X              |


**Stillingstype**

| **Felt**         | **Datatype** | **Obligatorisk** | **Søkbar** |
|--------------------|---------------|--------------|----------------|
| Klassifisering     | Alternativsett    |              | X              |
| Beskrivelse        | Text          |              | X              |
| Navn på stillingstype | Text          | X            | X              |


**Arbeidertilordninger for stilling**

| **Felt**                        | **Datatype** | **Obligatorisk** | **Søkbar** |
|-----------------------------------|---------------|--------------|----------------|
| Jobbstilling                      | Oppslag        | X            | X              |
| Tilordningsnummer for stilling for arbeider | Text          | X            | X              |
| Gyldig fra                        | Text          | X            | X              |
| Gyldig til                          |               |              | X              |
| Arbeider                            |               | X            | X              |

## <a name="job-entities"></a>Jobbenheter

**Jobb**

| **Felt**                   | **Datatype**  | **Obligatorisk** | **Søkbar** |
|------------------------------|----------------|--------------|----------------|
| Tillat ubegrensede stillinger    | To alternativer    |              | X              |
| Standard fulltidsekvivalent | Desimaltall |              | X              |
| Beskrivelse                  | Text           |              | X              |
| Jobbeskrivelse              | Text           |              | X              |
| Jobbfunksjon                 | Oppslag         |              | X              |
| Jobbtype                     | Oppslag         |              | X              |
| Maksimalt antall stillinger  | Heltall   |              | X              |
| Navn                         | Text           | X            | X              |
| Stillingstittel                        | Alternativsett     |              | X              |
| Gyldig fra                   | Dato og klokkeslett  | X            | X              |
| Gyldig til                     | Dato og klokkeslett  |              | X              |


**Jobbfunksjon**

| **Felt**        | **Datatype** | **Obligatorisk** | **Søkbar** |
|-------------------|---------------|--------------|----------------|
| Beskrivelse       | Text          | X            | X              |
| Jobbfunksjonsnavn | Text          | X            | X              |


**Jobbtype**

| **Felt**    | **Datatype** | **Obligatorisk** | **Søkbar** |
|---------------|---------------|--------------|----------------|
| Beskrivelse   | Text          | X            | X              |
| Fritatt-status | Alternativsett    | X            | X              |
| Jobbtypenavn | Text          | X            | X              |

## <a name="leave-and-absence-entities"></a>Permisjons- og fraværsenheter

**Permisjonsregistrering**

| **Felt**            | **Datatype** | **Obligatorisk** | **Søkbar** |
|-----------------------|---------------|--------------|----------------|
| Datogrunnlag for avsetning    | Bare dato     | X            | X              |
| Startdato for avsetning    | Bare dato     | X            | X              |
| Egendefinert dato           | Bare dato     | X            | X              |
| Er avsetning suspendert  | To alternativer   |              | X              |
| LeaveEnrollmentNumber | Text          | X            | X              |
| Permisjonsplan            | Oppslag        | X            | X              |
| Startdato            | Bare dato     | X            | X              |
| Basis for lag            | Alternativsett    | X            | X              |
| Arbeider                | Oppslag        | X            | X              |


**Permisjonsbanktransaksjon**

| **Felt**                    | **Datatype**  | **Obligatorisk** | **Søkbar** |
|-------------------------------|----------------|--------------|----------------|
| Beløp                        | Desimaltall | X            | X              |
| Bedrift                       | Oppslag         | X            | X              |
| Transaksjonsnummer for permisjonsbank | Text           | X            | X              |
| Permisjonsplan                    | Oppslag         |              | X              |
| Permisjonstype                    | Oppslag         | X            | X              |
| Transaksjonsdato              | Bare dato      | X            | X              |
| Transaksjonsnummer            | Desimaltall | X            | X              |
| Transaksjonstype              | Alternativsett     | X            | X              |
| Arbeider                        | Oppslag         | X            | X              |


**Permisjonsplan**

| **Felt**        | **Datatype** | **Obligatorisk** | **Søkbar** |
|-------------------|---------------|--------------|----------------|
| Avsetningshyppighet | Alternativsett    | X            | X              |
| Bedrift           | Oppslag        | X            | X              |
| Beskrivelse       | Text          |              | X              |
| Permisjonstype        | Oppslag        | X            | X              |
| Navn              | Text          | X            | X              |
| Startdato        | Bare dato     | X            | X              |


**Permisjonsforespørsel**

| **Felt**           | **Datatype** | **Obligatorisk** | **Søkbar** |
|----------------------|---------------|--------------|----------------|
| Kommentar              | Text          | X            | X              |
| Bedrift              | Oppslag        | X            | X              |
| Permisjonsforespørselsnummer | Text          |              | X              |
| Forespørselsdato         | Dato og klokkeslett | X            | X              |
| Status               | Alternativsett    | X            | X              |
| Arbeider               | Oppslag        | X            | X              |


**Detaljer for fraværsforespørsel**

| **Felt**                  | **Datatype**  | **Obligatorisk** | **Søkbar** |
|-----------------------------|----------------|--------------|----------------|
| Beløp                      | Desimaltall | X            | X              |
| Permisjonsdato                  | Dato og klokkeslett  | X            | X              |
| Permisjonsforespørsel               | Oppslag         | X            | X              |
| Detaljnummer for fraværsforespørsel | Text           | X            | X              |
| Permisjonstype                  | Oppslag         | X            | X              |


**Permisjonstype**

| **Felt**      | **Datatype** | **Obligatorisk** | **Søkbar** |
|-----------------|---------------|--------------|----------------|
| Bedrift         | Oppslag        | X            | X              |
| Beskrivelse     | Text          |              | X              |
| Inntektskode    | Oppslag        |              | X              |
| Navn på permisjonstype | Text          | X            | X              |


**Arbeidskalender**

| **Felt**  | **Datatype** | **Obligatorisk** | **Søkbar** |
|-------------|---------------|--------------|----------------|
| Bedrift     | Oppslag        | X            | X              |
| Beskrivelse | Text          |              | X              |
| Navn        | Text          | X            | X              |


**Arbeidskalenderdag**

| **Felt**               | **Datatype** | **Obligatorisk** | **Søkbar** |
|--------------------------|---------------|--------------|----------------|
| Kalenderdato            | Bare dato     | X            | X              |
| Bedrift                  | Oppslag        |              | X              |
| Status                   | Text          |              | X              |
| Arbeidskalender            | Oppslag        | X            | X              |
| Arbeidskalenderdagnummer | Text          | X            | X              |


**Helligdag i arbeidskalender**

| **Felt**  | **Datatype** | **Obligatorisk** | **Søkbar** |
|-------------|---------------|--------------|----------------|
| Navn        | Text          |              | X              |
| Beskrivelse | Text          | X            | X              |


**Ferielinje for arbeidskalender**

| **Felt**                        | **Datatype** | **Obligatorisk** | **Søkbar** |
|-----------------------------------|---------------|--------------|----------------|
| Dato for helligdag                      | Bare dato     | X            | X              |
| Navn                              | Text          |              | X              |
| Helligdag i arbeidskalender             | Oppslag        | X            | X              |
| Ferielinjenummer for arbeidskalender | Text          | X            | X              |


**Tidsintervall for arbeidskalender**

| **Felt**                         | **Datatype** | **Obligatorisk** | **Søkbar** |
|------------------------------------|---------------|--------------|----------------|
| Bedrift                            | Oppslag        |              | X              |
| Sluttidspunkt                           | Heltall  |              | X              |
| Starttidspunkt                         | Heltall  |              | X              |
| Arbeidskalender                      | Oppslag        | X            | X              |
| Arbeidskalenderdag                  | Oppslag        | X            | X              |
| Tidsintervallnummer for arbeidskalender | Text          | X            | X              |

## <a name="organization-entities"></a>Organisasjonsenheter

**Firma**

| **Felt**   | **Datatype** | **Obligatorisk** | **Søkbar** |
|--------------|---------------|--------------|----------------|
| Firmakode | Text          | X            | X              |
| Navn         | Text          | X            | X              |


**Avdeling**

| **Felt**        | **Datatype** | **Obligatorisk** | **Søkbar** |
|-------------------|---------------|--------------|----------------|
| Avdelingsnummer | Text          | X            | X              |
| Beskrivelse       | Text          |              | X              |
| Navn              | Text          | X            | X              |
| Overordnet avdeling | Oppslag        |              | X              |


**Valuta**

| **Felt**         | **Datatype**  | **Obligatorisk** | **Søkbar** |
|--------------------|----------------|--------------|----------------|
| Valutakode      | Text           | X            | X              |
| Valutanavn      | Text           | X            | X              |
| Valutapresisjon | Heltall   | X            | X              |
| Valutasymbol    | Text           | X            | X              |
| Enhetsbilde       | Bilde          |              |                |
| Valutakurs      | Desimaltall | X            | X              |
| Organisasjon       | Oppslag         | X            | X              |
| Status             | Alternativsett     |              | X              |

## <a name="payroll-entities"></a>Lønnsenheter

**Lønnssyklus**

| **Felt**  | **Datatype** | **Obligatorisk** | **Søkbar** |
|-------------|---------------|--------------|----------------|
| Beskrivelse | Text          | X            | X              |
| Frekvens   | Alternativsett    | X            | X              |
| Navn        | Text          | X            | X              |


**Lønnsperiode**

| **Felt**           | **Datatype** | **Obligatorisk** | **Søkbar** |
|----------------------|---------------|--------------|----------------|
| Standard betalingsdato | Bare dato     |              | X              |
| Beskrivelse          | Text          |              | X              |
| Lønnssyklus            | Søk          | X            | X              |
| Lønnsperiodenummer    | Text          | X            | X              |
| Periodens sluttdato      | Bare dato     | X            | X              |
| Periodens startdato    | Bare dato     | X            | X              |
| Status               | Alternativsett    |              | X              |


**Inntektskode for lønn**

| **Felt**              | **Datatype** | **Obligatorisk** | **Søkbar** |
|-------------------------|---------------|--------------|----------------|
| Beskrivelse             | Text          | X            | X              |
| Inkluder i betalingstype | Alternativsett    | X            | X              |
| Er produktiv           | To alternativer   | X            | X              |
| Navn                    | Text          |              | X              |
| Antallsenhet           | Alternativsett    |              | X              |
| Spor FMLA-timer        | To alternativer   |              | X              |


**Avgiftsområde**

| **Felt**        | **Datatype** | **Obligatorisk** | **Søkbar** |
|-------------------|---------------|--------------|----------------|
| By              | Text          |              | X              |
| Land eller område | Text          |              | X              |
| Kommune            | Text          |              | X              |
| Navn              | Text          | X            | X              |
| Delstat eller provins | Text          |              | X              |


**Lønnsperiode i fordelsberegningsfrekvens**

| **Felt**                                      | **Datatype** | **Obligatorisk** | **Søkbar** |
|-------------------------------------------------|---------------|--------------|----------------|
| Fordelsberegningsfrekvens                   | Oppslag        | X            | X              |
| Lønnsperiodenummer i fordelsberegningsfrekvens | Text          | X            | X              |
| Lønnsperiode                                      | Oppslag        | X            | X              |


**Bankkontobetaling**

| **Felt**                       | **Datatype**  | **Obligatorisk** | **Søkbar** |
|----------------------------------|----------------|--------------|----------------|
| Beløp                           | Valuta       |              | X              |
| Beløp (basisvaluta)                    | Valuta       |              | X              |
| Bankkonto                     | Oppslag         | X            | X              |
| Bankkontobetalingsnummer | Text           | X            | X              |
| Bedrift                          | Oppslag         | X            | X              |
| Valuta                         | Oppslag         |              | X              |
| Valutakurs                    | Desimaltall |              | X              |
| Er gjenstående                     | To alternativer    |              | X              |
| Prioritet                         | Heltall   |              | X              |

**Utstedende byrå for personidentifikasjon**

| **Felt**           | **Datatype** | **Obligatorisk** | **Søkbar** |
|----------------------|---------------|--------------|----------------|
| Adressebeskrivelse  | Text          |              | X              |
| Adresselinje 1       | Text          |              | X              |
| Adresselinje 2       | Text          |              | X              |
| Adresselinje 3       | Text          |              | X              |
| By                 | Text          |              | X              |
| Land eller område    | Alternativsett    |              | X              |
| Kommune               | Text          |              | X              |
| Beskrivelse          | Text          |              | X              |
| E-post                | Text          |              | X              |
| Direktenummer            | Text          |              | X              |
| Faks                  | Text          |              | X              |
| Navn på utstedende byrå  | Text          | X            | X              |
| Mobiltelefon         | Text          |              | X              |
| Side                 | Text          |              | X              |
| Postnummer          | Text          |              | X              |
| Postboks      | Text          |              | X              |
| SMS                  | Text          |              | X              |
| Delstat eller provins    | Text          |              | X              |
| Telefon            | Text          |              | X              |
| Teleks                | Text          |              | X              |
| URL-adresse til nettsted          | Text          |              | X              |

**Personidentifikasjonstype for arbeider**

| **Felt**                        | **Datatype**  | **Obligatorisk** | **Søkbar** |
|-----------------------------------|----------------|--------------|----------------|
| Tillatte verdier                    | Alternativsett     |              | X              |
| Land eller område                 | Text           |              | X              |
| Beskrivelse                       | Text           |              | X              |
| Fast lengde                      | Heltall   |              | X              |
| Identifikasjonsnummerformat      | Text           |              | X              |
| Type                              | Alternativsett     |              | X              |
| Personidentifikasjonstype for arbeider | Text           | X            | X              |

## <a name="fixed-compensation-entities"></a>Enheter for fast kompensasjon

**Fast plan for kompensasjon**

| **Felt**                  | **Datatype** | **Obligatorisk** | **Søkbar** |
|-----------------------------|---------------|--------------|----------------|
| Bedrift                     | Oppslag        | X            | X              |
| Kompensasjonsrutenett           | Oppslag        |              | X              |
| Valuta                    | Oppslag        | X            | X              |
| Beskrivelse                 | Text          | X            | X              |
| Ikrafttredelsesdato              | Bare dato     | X            | X              |
| Utløpsdato             | Bare dato     | X            | X              |
| Ansettelsesregel                   | Alternativsett    | X            | X              |
| Navn                        | Text          | X            | X              |
| Utenfor område-toleranse      | Alternativsett    | X            | X              |
| Lønnsfrekvens               | Oppslag        | X            | X              |
| Anbefaling tillatt      | To alternativer   | X            | X              |
| Oppsett av referansepunktlinje  | Oppslag        |              | X              |
| Type                        | Alternativsett    | X            | X              |

**Kompensasjonsrutenett**

| **Felt**                  | **Datatype** | **Obligatorisk** | **Søkbar** |
|-----------------------------|---------------|--------------|----------------|
| Bedrift                     | Oppslag        | X            | X              |
| Valuta                    | Oppslag        |              | X              |
| Beskrivelse                 | Text          | X            | X              |
| Ikrafttredelsesdato              | Bare dato     |              | X              |
| Utløpsdato             | Bare dato     |              | X              |
| Navn                        | Text          | X            | X              |
| Referansepunktoppsett       | Oppslag        | X            | X              |
| Type                        | Alternativsett    | X            | X              |

**Kompensasjonsnivå**

| **Felt**      | **Datatype** | **Obligatorisk** | **Søkbar** |
|-----------------|---------------|--------------|----------------|
| Beskrivelse     | Text          |              | X              |
| Navn            | Text          | X            | X              |
| Type            | Alternativsett     | X            | X              |

**Kompensasjon, lønnsfrekvens**

| **Felt**                  | **Datatype**   | **Obligatorisk** | **Søkbar** |
|-----------------------------|-----------------|--------------|----------------|
| Årlig konverteringsfaktor    | Desimaltall  |              | X              |
| Bedrift                     | Oppslag          | X            | X              |
| Beskrivelse                 | Text            |              | X              |
| Timebasert konverteringsfaktor    | Desimaltall  |              | X              |
| Månedlig omregningsfaktor   | Desimaltall  |              | X              |
| Navn                        | Text            | X            | X              |
| Periode                      | Alternativsett      |              | X              |
| Ukentlig omregningsfaktor    | Alternativsett      |              | X              |


**Oppsett av referansepunkt for kompensasjon**

| **Felt**          | **Datatype**   | **Obligatorisk** | **Søkbar** |
|---------------------|-----------------|--------------|----------------|
| Bedrift             | Oppslag          | X            | X              |
| Kompensasjonstype   | Alternativsett      | X            | X              |
| Beskrivelse         | Text            | X            | X              |
| Navn                | Text            | X            | X              |

**Oppsettslinje for referansepunkt for kompensasjon**

| **Felt**            | **Datatype**   | **Obligatorisk** | **Søkbar** |
|-----------------------|-----------------|--------------|----------------|
| Bedrift               | Oppslag          | X            | X              |
| Beskrivelse           | Text            | X            | X              |
| Linjenummer           | Desimaltall  | X            | X              |
| Navn                  | Text            | X            | X              |
| Referansepunktoppsett | Oppslag          | X            | X              |

**Kompensasjonsområde**

| **Felt**      | **Datatype** | **Obligatorisk** | **Søkbar** |
|-----------------|---------------|--------------|----------------|
| Beskrivelse     | Text          | X            | X              |
| Navn            | Text          | X            | X              |

**Kompensasjonsstruktur**

| **Felt**                    | **Datatype**   | **Obligatorisk** | **Søkbar** |
|-------------------------------|---------------  |--------------|----------------|
| Beløp                        | Valuta        |              | X              |
| Beløpsgrunnlag                   | Valuta        |              | X              |
| Bedrift                       | Oppslag          | X            | X              |
| Kompensasjonsstrukturnummer | Text            | X            | X              |
| Valuta                      | Oppslag          |              | X              |
| Valutakurs                 | Desimaltall  |              | X              |
| Rutenett                          | Oppslag          | X            | X              |
| Nivå                         | Oppslag          | X            | X              |
| Referansepunkt               | Oppslag          | X            | X              |
| Oppsett av referansepunktlinje    | Oppslag          | X            | X              |

**Fast kompensasjonshendelse**

| **Felt**            | **Datatype**   | **Obligatorisk** | **Søkbar** |
|-----------------------|-----------------|--------------|----------------|
| Bedrift               | Oppslag          | X            | X              |
| Beskrivelse           | Text            | X            | X              |
| Hendelsestype            | Alternativsett      | X            | X              |
| Er aktiv             | To alternativer     | X            |                |
| Navn                  | Text            | X            | X              |

## <a name="entity-relationship-models"></a>Enhetsrelasjonsmodeller

### <a name="worker"></a>Arbeider
![Arbeider](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Jobb og stilling
![Jobb og stilling](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Fordeler
![Fordeler](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensasjon
![Kompensasjon](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Permisjon
![Permisjon](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Arbeidskalender
![Arbeidskalender](./media/HCMCommon-work-calendar-entity-diagram.png)
