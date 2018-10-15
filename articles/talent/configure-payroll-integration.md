---
title: "Konfigurere lønnsintegreringen mellom Talent og Dayforce"
description: "Dette emnet forklarer hvordan du konfigurerer integrasjonen mellom Microsoft Dynamics 365 for Talent og Ceridian Dayforce slik at du kan behandle en lønnskjøring."
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---

# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a>Konfigurere lønnsintegreringen mellom Talent og Dayforce

[!include [banner](includes/banner.md)]

Integrasjonen mellom Microsoft Dynamics 365 for Talent og Ceridian Dayforce bruker flere konfigurasjonstrinn som er beskrevet i dette emnet. Du må konfigurere integreringen i både Talent og Dayforce før du kan behandle en lønnskjøring.

Når du bruker en tjeneste som Dayforce til å fullføre lønnskjøringer, må du aktivere integrering i Talent. Integreringen krever bestemte data fra Talent. Derfor må du kontrollere at data som tilordnes til Dayforce, er konfigurert i Talent på en måte som støtter integreringen. Integrasjonen bruker følgende brede datakategorier:

- Personaldata
- Kompensasjonsdata
- Lønnsdata, for eksempel lønnssykluser, lønnsperioder og inntektskoder
- Arbeiderdata

Dette emnet beskriver trinnene du må følge for å aktivere integreringen. Den beskriver også hvilke typer data og konfigurasjonsdetaljer som integreringen krever.

## <a name="enable-the-integration"></a>Aktivere integrasjonen

I Talent må du aktivere integreringen og angi konfigurasjonsinformasjonen for å koble til Dayforce. Hvis du vil at økonomimodultransaksjonen som produseres, skal importeres til Microsoft Dynamics 365 for Finance and Operations, må du også definere en Microsoft Azure-lagringskonto og angi Azure Storage-tilkoblingsstrengen i Finance and Operations.

Følg denne fremgangsmåten for å aktivere integrasjonen i Talent.

1. Velg **Konfigurasjon av integrering** på siden **Systemadministrasjon**.
2. Angi sikkert FTP-sluttpunkt og sikker FTP-mappebane.
3. Angi brukernavnet og passordet til brukeren som skal ha tilgang til sikkert FTP-sluttpunkt og sikker FTP-mappebane.
4. Test tilkoblingen etter behov, og sett alternativet **Aktiver lønnsintegrering** til **Ja**.

Når integreringen er slått på, opprettes dataeksportpakken og -filene, og frekvensen angis. Du kan endre denne frekvensen etter behov.

Hvis du vil ha mer informasjon om Azure Storage-kontoer og Azure Storage-tilkoblingsstrenger, kan du se følgende Azure-emner:

- [Om Azure Storage-kontoer](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [Konfigurere Azure Storage-tilkoblingsstrenger](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a>Konfigurere dataene dine 

For å behandle lønn må du konfigurere Personaldata i Talent. Du må definere organisasjonsdata, for eksempel jobber og stillinger, samt informasjon om fordeler og kompensasjon. Denne informasjonen gir informasjon om ansettelse, lønn og trekk som kreves for å kunne generere lønn for den ansatte.

### <a name="human-resource-data"></a>Personaldata

#### <a name="benefits"></a>Fordeler 

Personale inneholder verktøy for oppsett og vedlikehold av fordeler, fradrag og arbeiderkompensasjonsplaner som en organisasjon tilbyr eller behandler for sine arbeidere.

Når du oppretter fordeler, husk følgende data og konfigurasjoner som brukes i Dayforce.

##### <a name="benefit-plans"></a>Fordelsplaner

- Plan (obligatorisk)
- Type (obligatorisk)
- Lønnsinnvirkning (obligatorisk)
- Gjenopprett etterskudd
- Fradragsmetode
- Fradragsprioritet
- Begrens periode
- Grensebeløp

##### <a name="benefits"></a>Fordeler

- Plan (obligatorisk)
- Type (obligatorisk)
- Alternativ (obligatorisk)
- Fordel-ID (obligatorisk)
- Frekvens
- Grunnlag
- Beløp eller sats
- Inntektskode

##### <a name="supported-frequencies"></a>Støttede frekvenser 

- Ukentlig
- Annenhver uke
- Halvmånedlig
- Månedlig

##### <a name="supported-bases"></a>Støttede grunnlag 

- Fast beløp
- Prosentandel av inntekter
- Produktive timer

Dayforce oppretter følgende fradrag, basert på lønnsinnvirkning som er definert på fordelsplanen.

| Valg i Talent        | Resultat i Dayforce                            |
|----------------------------|-----------------------------------------------|
| None                       | Ingen fradrag opprettes.                      |
| Bare fradrag             | Et ansattfradrag opprettes.             |
| Bare bidrag          | Et arbeidsgiverfradrag opprettes.             |
| Fradrag og bidrag | Fradrag for ansatte og arbeidsgivere opprettes. |

Hvis du vil ha mer informasjon om hvordan du definerer og administrerer et program for fordeler, kan du se følgende emner:

- [Levere et program for ansattfordeler](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [Opprette en ny fordel](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [Definere rettighetsregler og policyer for fordel](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [Registrere og fjerne fordeler fra arbeidere](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a>Kompensasjon 

Kompensasjonsstyring brukes til å kontrollere levering av grunnlønn og bonuser. En ansatts faste grunnlønn og personlige tilleggsøkninger styres via faste kompensasjonsplaner. Betaling av insitamentutbetalinger, for eksempel bonuser, ytelsestillegg, aksjeopsjoner og tilskudd, og også engangsbonuser, kontrolleres via variable kompensasjonsplaner.

Dayforce bruker kompensasjonsinformasjon til å beregne timesats eller årlig sats for en ansatt. Planer for faste kompensasjoner og konverteringer av lønnssats er påkrevd. Ansatte må tilknyttes en plan for fast kompensasjon.

Hvis du vil ha mer informasjon om kompensasjonsplaner, kan du se følgende emner:

- [Opprette planer for fast kompensasjon](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [Opprette variable kompensasjonsplaner](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [Utvikle struktur og planer for lønn/kompensasjon](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [Behandle kompensasjon](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [Definere kompensasjonsprosess og beregne resultater](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [Registrere en ansatt i en fast kompensasjonsplan](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [Registrere en ansatt i en variabel kompensasjonsplan](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a>Jobber 

En jobb er en samling oppgaver og ansvarsområder som kreves av en person som utfører en jobb. Hvis du vil ha mer informasjon, se følgende emner:

- [Definere komponentene for en jobb](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [Definere nye jobber](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a>Stillinger

En stilling er én enkeltforekomst av en jobb. "Salgssjef (øst)"-stillingen er for eksempel én av stillingene som er knyttet til jobben "Salgssjef". Det finnes en stilling i en avdeling. Bare én arbeider kan være tilknyttet hvert område.

Ha følgende data og konfigurasjon i bakhodet når du definerer stillinger:

- Stilling (obligatorisk)
- Beskrivelse (obligatorisk)
- Jobb (obligatorisk)
- Avdeling (obligatorisk)
- Stillingstype (obligatorisk)
- Fulltidsekvivalent
- Årlige vanlige timer (obligatorisk)
- Betalt av juridisk enhet (obligatorisk)
- Betalingssyklus (obligatorisk)
- Standard finansdimensjon – kostsenter (obligatorisk)
- Arbeidertilordning – arbeider, start for tilordning, slutt for tilordning, årsakskode

Hvis flere stillinger i samme avdeling er knyttet til den samme jobben, konsolideres de til én stilling i Dayforce.

Hvis du vil ha mer informasjon, se følgende emner:

- [Organisere arbeidsstyrken ved bruk av avdelinger, jobber og stillinger](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [Definere stillinger](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a>Avdelinger

En avdeling er en driftsenhet som representerer en kategori eller et funksjonsområde i en organisasjon. En avdeling er ansvarlig for et bestemt område i organisasjonen, for eksempel salg, regnskap eller Personale. Du kan bruke avdelinger til å rapportere om funksjonsområder. Avdelinger kan ha ansvar for fortjeneste og tap.

Hvis du vil ha mer informasjon, se følgende emner:

- [Opprette en avdeling og knytte den til avdelingshierarkiet](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [Definere nye avdelinger](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a>Lønnssykluser og lønnsperioder

En betalingssyklus avgjør hvor ofte lønnskjøring utføres, og de spesifikke dagene arbeidere lønnes. For eksempel kan en lønnssyklus være månedlig, og ansatte kan betales på den siste dagen i måneden. En lønnssyklus kan også være ukentlig, og ansatte kan betales tirsdagen etter slutten av lønnsperioden. Lønnssykluser tilordnes til stillinger for å styre når arbeidere i disse stillingene lønnes.

Når du oppretter lønnssykler, kan du generere lønnsperioder for hver enkelt syklus. Hver lønnsperiode inkluderer en standard betalingsdato som er basert på informasjonen du angir. Du kan imidlertid endre standard betalingsdato i en lønnsperiode for å tillate unntak, for eksempel når betalingsdatoen faller på en helligdag.

Informasjonen nedenfor brukes i Dayforce:

- Betalingssyklus (obligatorisk)
- Lønnssyklusfrekvens (obligatorisk)
- Periodens startdato (første lønnsperiode er obligatorisk)
- Standard betalingsdato (første lønnsperiode er obligatorisk)

Denne informasjonen er integrert med Dayforce som lønnsgrupper og er inndelt etter land eller område for hver lønnssyklus. Minst én lønnsperiode må genereres før integrasjon. Dayforce genererer lønnsgruppekalendere og betalingsdatoer basert på startdatoen for den første lønnsperioden og standard betalingsdato som er definert i Talent.

#### <a name="earning-codes"></a>Inntektskoder

Inntektskoder sørger for unik identifisering av alle typer inntekter som ansatte mottar. Kodene har forskjellige parametere som er knyttet til inntekter, for eksempel regnskapsregler, skattelover, rapporteringkrav og bruttofunksjon.

Informasjonen nedenfor brukes i Dayforce:

- Inntektskode (obligatorisk)
- beskrivelse
- Måleenhet
- Produktiv

### <a name="worker-data"></a>Arbeiderdata

Poster for ulike typer arbeidere som du har, er viktig for personal. og lønnsystemene dine. Informasjonen du legger inn, kan brukes til å spore arbeidere og personlig informasjon.

Du kan vedlikeholde følgende informasjon om arbeidere:

- **Grunnleggende** – Vedlikehold grunnleggende informasjon om en arbeider, for eksempel kontaktinformasjon, demografisk informasjon, identifikasjonsinformasjon, familieinformasjon, militærtjenestestatus, informasjon om personer som bor i utlandet, og personlige kontakter og kontakter i nødfall.
- **Ansettelse** – Vedlikehold informasjon om en arbeiders ansettelse, for eksempel informasjon om firma- eller organisasjonstilknytning, stillingstilordning, start- og sluttdatoer, arbeidstillatelse, vilkår for ansettelse, pensjon, ferie og flytting.
- **Lønn og fravær** – Vedlikehold opplysninger om en arbeiders fravær, for eksempel arbeidskalendere, fraværstransaksjoner og fraværsoppsett.
- **Kompensasjon og lønn** – Vedlikehold informasjon om en arbeiders kompensasjonsplaner og lønn, for eksempel planregistrering, priser, ytelse, provisjon, avgiftsinformasjon, pensjonering og lønnstrekk.

Når du legger inn arbeiderinformasjon, husk følgende data og konfigurasjoner som brukes i Dayforce.

#### <a name="general-information"></a>Generell informasjon

- Personalnummer (obligatorisk)
- Fornavn (obligatorisk)
- Etternavn (obligatorisk)
- Mellomnavn
- Ansiennitetsdato
- Kalt

#### <a name="personal-information"></a>Personlige opplysninger

- Sivilstand (obligatorisk)
- Fødselsdato (obligatorisk)
- Kjønn (obligatorisk)
- Person med funksjonshemminger
- Nasjonalitet land/område (bare for Mexico)

#### <a name="address-information"></a>Adresseopplysninger

- Primær (obligatorisk)
- Land/område (obligatorisk)
- Postnummer (obligatorisk)
- Gatenummer (obligatorisk) (bare for Mexico)
- Bygningsnavn (bare for Mexico)
- By (obligatorisk)
- Stat (obligatorisk)
- Land (obligatorisk)

#### <a name="contact-information"></a>Kontaktinformasjon 

- Primær (obligatorisk)
- Kontaktnummer (obligatorisk)
- Utvidelse

#### <a name="payroll-information-and-earning-codes"></a>Lønnsinformasjon og inntektskoder

Ansatte kan tilordnes spesifikke inntekter med en gitt betalingfrekvens og med en foretrukket betalingsmåte. Følgende felt brukes i Dayforce for å sørge for at disse valgene og innstillingene brukes.

##### <a name="earning-codes"></a>Inntektskoder

- Stilling (obligatorisk)
- Inntektskode (obligatorisk)
- Frekvens (obligatorisk)
- Beløp (obligatorisk)

##### <a name="payroll-information"></a>Lønnsinformasjon

- Betalingsmåte
- Økonomisk område (obligatorisk)
- ID for ansattfordeler
- Nasjonalt ID-nummer (obligatorisk)
- Militærtjenestenummer
- Skift-ID (obligatorisk)
- Avgiftsnummer (obligatorisk)
- Fagforenings-ID (obligatorisk)
- Arbeidsdag-ID (obligatorisk)
- Arbeidstillatelsesnummer

> [!NOTE]
> Når det gjelder betalingsmåte støtter Mexico **Kontanter**, **Sjekk** (firmaets fysisk sjekk) og **Elektronisk betaling**. Hvis betalingsmåte ikke er angitt, brukes **Sjekk** som standard.

#### <a name="employment-details"></a>Ansettelsesdetaljer

Ansettelsesdetaljhistorikk brukes som nøkkelinformasjon til å avlede en ansatts ansettelse-, oppsigelses- og nyansettelsesstatuser i Dayforce. Dayforce støtter bare én aktiv ansettelsespost om gangen.

- Startdato for ansettelse (obligatorisk)
- Sluttdato for ansettelse
- Startdato
- Justert startdato
- Avslutningsdato (kreves ved avslutning)
- Avslutningsårsak (kreves ved avslutning)

En ansatts nøkkeldatoer avledes ved å bruke følgende informasjon.

| Talent                | Dayforce                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| Den siste ansettelsesdatoen | Ansettelsesstart for gjeldende ikke-avsluttede ansettelsesloggpost                                 |
| Avslutningsdato      | Avslutningsdato for gjeldende ikke-avsluttede ansettelsesloggpost                                 |
| Startdato            | Justert startdato, startdato eller ansettelsesstart for gjeldende ikke-aktive ansettelseloggpost |
| Opprinnelig ansettelsesdato    | Ansettelsesstart for tidligste ansettelsesloggpost                                               |

#### <a name="compensation"></a>Kompensasjon

En fast kompensasjonsplan må være knyttet til hver ansatts primære stilling i en ansattperiode. Denne perioden begynner på datoen da den ansatte ble ansatt (eller startdatoen for ansettelsen), og fortsetter til avslutning.

- Gyldighetsdato (obligatorisk)
- Utløpsdato
- Lønnssats (obligatorisk)
- Konverteringer av lønnssats (obligatorisk)
- Tilsvarende årlig (obligatorisk)
- Tilsvarende per time (obligatorisk)

Hvis en timebaserte ansatt har flere stillinger, importeres fast kompensasjon for den primære stillingen til Dayforce som basissats/lønn for ansattnivå. For ikke-primære stillinger lagres timeprisen til den tilsvarende stillingen i Dayforce.

Hvis en lønnsansatt har flere stillinger, avledes kumulativ timepris og årslønn på tvers av alle aktive stillinger og brukes som basissats/lønn for ansattnivå.

#### <a name="identification-numbers"></a>Identifikasjonsnumre

##### <a name="social-security-identifier"></a>Personnummeridentifikator 

Alle ansatte må ha én primær identifikator. Identifikatoren må være av identifikasjonstypen **SSN**. I Dayforce hentes den automatisk som den ansattes personnummeridentifikator som kreves for ansettelse.

- Primær (obligatorisk)
- Identifikasjonstype = "SSN"
- Utstedelsesdato
- Utløpsdato

Ansatte kan angi flere identifikasjonsnumre for identifikasjonstypen **SSN**. Det er imidlertid bare posten som er merket som **Primær**, som er integrert i Dayforce, uansett om nummeret er aktivt eller utløpt.

#### <a name="bank-accounts-and-disbursements"></a>Bankkontoer og -utlegg

Gyldig bankkontoinformasjon må angis for alle ansatte som velger å betales via bankkontooverføringer.

| Talent                         | Dayforce                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| Bankkontonummer (obligatorisk) |                                                                                                             |
| SWIFT-kode (obligatorisk)          | **Bank-ID**-felt som brukes ved behandling av lønninger i Mexico.                                                             |
| Avdelingsnummer (obligatorisk)       |                                                                                                             |
| Bankkontotype (obligatorisk)   | **Kontotoype**-felt som brukes ved behandling av lønninger i Mexico. Støttede verdier inkluderer **Kontroll** og **Lønn**. |

> [!NOTE]
> Ansatte som velger å betales via bankkontooverføringer, må oppgi en kobling til en restkonto som er under en juridisk enhet som har primær adresse i Mexico og er knyttet til en gyldig bankkonto fra en meksikansk bank. Alle andre ikke-restkontoer ignoreres.

#### <a name="address-information"></a>Adresseopplysninger

Alle ansatte må ha ett primært sted. I Dayforce brukes dette stedet til å fastslå den ansattes primære bosted for skatte- og avgiftsformål.

- Primær (obligatorisk)
- Land/område (obligatorisk)
- Postnummer (obligatorisk)
- Gate (obligatorisk)
- Gatenummer (obligatorisk)
- Bygningsnavn
- By (obligatorisk)
- Stat (obligatorisk)
- Land (oblitagorisk)

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a>Konfigurer dataene for å generere lønn i USA og Canada

Hvis du skal generere lønn for ansatte i USA og Canada, konfigureres følgende elementer:

- Avdelinger må oppgis for stillinger.
- Kostnadssentre må være angitt som finansdimensjoner og må være det første elementet i standard finansdimensjonsstreng.

### <a name="job-types"></a>Jobbtyper

Jobbtyper brukes til å gruppere lignende jobber i kategorier. Jobbtyper kreves for å kunne behandle lønn i USA og Canada. Eksempler på jobbtyper er heltid og deltid, eller lønn og timelønn. Jobbtyper er tilordnet til Dayforce som lønnstyper som angir om en ansatt er hver time eller lønn.

Følgende jobbtyper og beskrivelser er påkrevd.

| Jobbtype   | beskrivelse |
|------------|-------------|
| Per time     | Per time      |
| Lønnsbasert   | Lønnsbasert    |

### <a name="position-types"></a>Stillingstyper 

Du kan bruke stillingstyper til å beskrive om stillingen er heltid, deltid eller et annet navn. Posisjonstyper er tilordnet til Dayforce som lønnsklasser som angir om en ansatt er fulltid eller deltid.

Følgende jobbposisjonstyper og -beskrivelser er påkrevd.

| Stillingstype   | beskrivelse        |
|-----------------|--------------------|
| Heltid       | Heltidsansatt |
| Deltid       | Deltidsansatt |

### <a name="reason-codes"></a>Årsakskoder

Årsakskoder inneholder informasjon om statusen for en ansatt. Årsakskoder er tilordnet til Dayforce som statusårsaker som angir årsaken til endringer i en ansatts stilling eller status.

Følgende årsakskoder og beskrivelser er påkrevd.

| Årsakskode    | beskrivelse      | Gjeldende scenarier |
|----------------|------------------|----------------------|
| OPPSIGELSE    | Oppsigelse      | Avslutt arbeider     |
| AVSLUTNING    | Avslutning      | Avslutt arbeider     |
| AVGANG VED PENSJON     | Avgang ved pensjon       | Avslutt arbeider     |
| ANNET          | Andre årsaker    | Avslutt arbeider     |
| DØDSFALL          | Dødsfall            | Avslutt arbeider     |
| PERMISJON | Permisjon | Avslutt arbeider     |
| KONTRAKTSLUTT    | Slutt på kontrakt  | Avslutt arbeider     |
| LØNNSENDRING   | Lønnsendring | Kompensasjon         |

### <a name="marital-status"></a>Sivilstand

Sivilstandverdier tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.

Tabellen nedenfor viser hvordan sivilstandverdiene tilordnes i Dayforce.

| Talent                 | Dayforce             |
|------------------------|----------------------|
| Gift                | Gift              |
| Én                 | Én               |
| Enke/enkemann                | Enke/enkemann              |
| Skilt               | Skilt             |
| Registrert ekteskapelig partnerskap | Ekteskapelig partnerskap |
| None                   | None                 |
| Samboer             | Samboer           |

### <a name="gender"></a>Kjønn

Kjønnsangivelser tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.

Tabellen nedenfor viser hvordan kjønnsangivelser tilordnes i Dayforce.

| Talent       | Dayforce        |
|--------------|-----------------|
| Mann         | Mann            |
| Kvinne       | Kvinne          |
| Ikke spesifikt | *Støttes ikke* |

### <a name="earning-codes"></a>Inntektskoder

Inntektskoder sørger for unik identifisering av alle typer inntekter som ansatte mottar. Kodene dekker flere parametere som er knyttet til inntekter, for eksempel regnskapsregler, skattelover, rapporteringkrav og bruttofunksjon. Hvis det brukes en frekvens som ikke støttes, brukes frekvensen **Hver betaling** som standard for beregningen.

#### <a name="supported-frequencies"></a>Støttede frekvenser

- Alle
- HVERBET
- HVERBETPERIODE
- ANNENHVBETODD
- ANNENHVBETPAR
- 1IMND
- SISTEIMND
- 2IMDN
- 3IMND
- 4IMND
- 5IMND
- 1OG2IMND
- 3OG4IMND
- 1OG3IMND
- 1OG4IMND
- 2OG3IMND
- 2OG4IMND
- 1OG2OG3IMND
- 1OG2OG4IMND
- 1OG3OG4IMND
- 2OG3OG4IMND
- 1OG2OG3OG4IMND - 1OG2OG3OG4IMND
- 2OG3OG4OG5IMND - 2OG3OG4OG5IMND
- 1IKVRT - 1IKVRT
- SISTIKVART – SISTIKVART
- SISTEMNDIKVRT – SISTEMNDIKVRT
- 1IÅR - 1IÅR
- SISTEIÅR – SISTEIÅR
- NOVOGDESIÅR - NOVOGDESIÅR

### <a name="addresses"></a>Adresser

Identifikasjon av bestemte koder for land eller område, delstat og fylke (kommune) krever spesifikke formater som Dayforce og leverandører i landet/området kan gjenkjenne. Selv om formatet for byer er fleksibelt, må hver by være knyttet en stat.

| Talent          | Dayforce              |
|-----------------|-----------------------|
| Land/område  | Landskode          |
| Postnummer  | Postnummer           |
| Delstat           | Statskode            |
| By            | By                  |
| Kommune          | Fylke (kommune) |
| Gate          | Adresselinje 1        |

### <a name="tax-regions"></a>Avgiftsområder

Avgiftsområder brukes til å bestemme den gjeldende avgiften som skal brukes ved generering av lønn. Avgiftsområder er tilordnet Dayforce som stedsadresser. Standard avgiftområde må være knyttet til arbeiderens aktive stilling. 

- Avgiftsområde (obligatorisk)
- Land/område (obligatorisk)
- Stat (obligatorisk)
- Kommune 
- By (obligatorisk)

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a>Konfigurere data for å generere lønn i Mexico

Hvis du skal generere lønn for ansatte i Mexico, konfigureres følgende elementer:

- Avdelinger må oppgis for stillinger.
- Kostnadssentre må være angitt som finansdimensjoner og må være det første elementet i standard finansdimensjonsstreng.

### <a name="job-types"></a>Jobbtyper

Jobbtyper brukes til å gruppere lignende jobber i kategorier. Jobbtype kreves for å kunne behandle lønn i Mexico. Eksempler på jobbtyper er heltid og deltid, eller lønn og timelønn. Jobbtyper er tilordnet til Dayforce som lønnstyper som angir om en ansatt er hver time eller lønn.

Følgende jobbtyper og beskrivelser er påkrevd.

| Jobbtype   | beskrivelse |
|------------|-------------|
| Per time     | MX per time   |
| Lønnsbasert   | MX lønnsbasert |

### <a name="position-types"></a>Stillingstyper 

Du kan bruke stillingstyper til å beskrive om stillingen er heltid, deltid eller et annet navn. Posisjonstyper er tilordnet til Dayforce som lønnsklasser som angir om en ansatt er fulltid eller deltid.

Følgende jobbposisjonstyper og -beskrivelser er påkrevd.

| Stillingstype   | beskrivelse        |
|-----------------|--------------------|
| Heltid       | Heltidsansatt |
| Deltid       | Deltidsansatt |

### <a name="reason-codes"></a>Årsakskoder

Årsakskoder inneholder informasjon om statusen for en ansatt. Årsakskoder er tilordnet til Dayforce som statusårsaker som angir årsaken til endringer i en ansatts stilling eller status.

Følgende årsakskoder og beskrivelser er påkrevd.

| Årsakskode            | beskrivelse                    | Gjeldende scenarier |
|------------------------|--------------------------------|----------------------|
| AVGANGFØRBETALING | Avgang før første lønn | Avslutt arbeider     |
| OPPSIGELSE            | Oppsigelse                    | Avslutt arbeider     |
| PENSJON                | Pensjon                        | Avslutt arbeider     |
| AVSLUTNING            | Avslutning                    | Avslutt arbeider     |
| AVGANGVEDPENSJON             | Avgang ved pensjon                     | Avslutt arbeider     |
| FRAVÆRENDEPERSON               | Fraværende person                       | Avslutt arbeider     |
| ANNET                  | Andre årsaker                  | Avslutt arbeider     |
| STENGNING                | Forretning stenger               | Avslutt arbeider     |
| DØDSFALL                  | Dødsfall                          | Avslutt arbeider     |
| PERMISJON         | Permisjon               | Avslutt arbeider     |
| KONTRAKTSLUTT            | Slutt på kontrakt                | Avslutt arbeider     |
| LØNNSENDRING           | Lønnsendring               | Kompensasjon         |

### <a name="terms-of-employment"></a>Ansettelsesbetingelser

Ansettelsesbetingelser brukes til å opprette kategorier for ansettelsesbetingelser. Vilkårene tilordnes til Dayforce som ansettelseindikatorverdier.

Følgende betingelsene for ansettelse og beskrivelser kreves.

| Ansettelsesbetingelser   | beskrivelse |
|-----------------------|-------------|
| Vanlig               | Vanlig     |
| Direkte                | Direkte      |
| Praktikantstilling            | Praktikantstilling  |
| Permanent             | Permanent   |

### <a name="marital-status"></a>Sivilstand

Sivilstandverdier tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.

Tabellen nedenfor viser hvordan sivilstandverdiene tilordnes i Dayforce.

| Talent                 | Dayforce                  |
|------------------------|---------------------------|
| Gift                | Gift                   |
| Én                 | Én                    |
| Enke/enkemann                | Enke/enkemann                   |
| Skilt               | Skilt                  |
| Registrert ekteskapelig partnerskap | Ekteskapelig partnerskap      |
| None                   | *Støttes ikke i Mexico* |
| Samboer             | *Støttes ikke i Mexico* |

### <a name="gender"></a>Kjønn

Kjønnsangivelser tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.

Tabellen nedenfor viser hvordan kjønnsangivelser tilordnes i Dayforce.

| Talent       | Dayforce                  |
|--------------|---------------------------|
| Mann         | Mann                      |
| Kvinne       | Kvinne                    |
| Ikke spesifikt | *Støttes ikke i Mexico* |

### <a name="payment-method"></a>Betalingsmetode

Betalingsmåter gir den ansatte og firmaet en måte å beskrive hvordan ansatte skal betales. Betalingsmåter tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.

Tabellen nedenfor viser hvordan betalingsmåter tilordnes i Dayforce.

| Talent             | Dayforce                  |
|--------------------|---------------------------|
| Kontanter               | Kontanter                      |
| Elektronisk betaling | Overfør                  |
| Kontroll              | Sjekk                    |
| Bankoverføring         | *Støttes ikke i Mexico* |
| Annet              | *Støttes ikke i Mexico* |

### <a name="bank-account-type"></a>Bankkontotype

Bankkontotypene brukes for elektroniske betalinger til ansatte. Bankkontotypene tilordnes til Dayforce som overføringskontoinformasjon. Bankkontotypene oversettes, etter behov, til de godkjente verdiene ved integrering.

| Talent            | Dayforce                  |
|-------------------|---------------------------|
| Sjekkonto  | Sjekkonto           |
| Lønnskonto   | Lønnskonto            |
| Sparekonto   | *Støttes ikke i Mexico* |
| BankGirot-konto | *Støttes ikke i Mexico* |
| PlusGirot-konto | *Støttes ikke i Mexico* |

### <a name="earning-codes"></a>Inntektskoder

Inntektskoder sørger for unik identifisering av alle typer inntekter som ansatte mottar. Kodene dekker flere parametere som er knyttet til inntekter, for eksempel regnskapsregler, skattelover, rapporteringkrav og bruttofunksjon. Hvis det brukes en frekvens som ikke støttes, brukes frekvensen **Hver betaling** som standard for beregningen.

#### <a name="supported-frequencies"></a>Støttede frekvenser

- Alle
- HVERBET
- HVERBETPERIODE
- ANNENHVBETODD
- ANNENHVBETPAR
- 1IMND
- SISTEIMND
- 2IMDN
- 3IMND
- 4IMND
- 5IMND
- 1OG2IMND
- 3OG4IMND
- 1OG3IMND
- 1OG4IMND
- 2OG3IMND
- 2OG4IMND
- 1OG2OG3IMND
- 1OG2OG4IMND
- 1OG3OG4IMND
- 2OG3OG4IMND
- 1OG2OG3OG4IMND - 1OG2OG3OG4IMND
- 2OG3OG4OG5IMND - 2OG3OG4OG5IMND
- 1IKVRT - 1IKVRT
- SISTIKVART – SISTIKVART
- SISTEMNDIKVRT – SISTEMNDIKVRT
- 1IÅR - 1IÅR
- SISTEIÅR – SISTEIÅR
- NOVOGDESIÅR - NOVOGDESIÅR

### <a name="addresses"></a>Adresser

Identifikasjon av bestemte koder for land eller område, delstat og fylke (kommune) krever spesifikke formater som Dayforce og leverandører i landet/området kan gjenkjenne. Selv om formatet for byer er fleksibelt, må hver by være knyttet en stat.

| Talent              | Dayforce              |
|---------------------|-----------------------|
| Land/område      | Landskode          |
| Postnummer     | Postnummer           |
| Delstat               | Statskode            |
| By                | By                  |
| Kommune              | Fylke (kommune) |
| Gate              | Adresselinje 1        |
| Gatenummer       | Adresselinje 2        |
| Bygningsnavn | Adresselinje 5        |

### <a name="passport-number"></a>Passnummer

Ansatte kan deklarere passinformasjon. Denne informasjonen er av **Pass**-identifikasjonstypen og er integrert i Dayforce som en del av en ansatts Mexico-spesifikke informasjon.

- Identifikasjonstype = "Pass"
- Utstedelsesdato
- Utløpsdato

Ansatte kan angi flere identifikasjonsnumre for identifikasjonstypen **Pass**. Men bare den gjeldende aktive passoppføringen er integrert i Dayforce. Hvis alle passoppføringer er utløpt, er passet som sist ble utstedt, integrert i Dayforce.
