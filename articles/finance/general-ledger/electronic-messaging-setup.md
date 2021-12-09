---
title: Definere elektroniske meldinger
description: Dette emnet gir informasjon om hvordan du konfigurerer EM-funksjonalitet (Elektroniske meldinger).
author: liza-golub
ms.date: 11/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-23
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a9d623c712de34afd1b38dbc6a8738ebf9613d49
ms.sourcegitcommit: 8c17717b800c2649af573851ab640368af299981
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/23/2021
ms.locfileid: "7860564"
---
# <a name="set-up-electronic-messages"></a>Definere elektroniske meldinger

[!include [banner](../includes/banner.md)]

Funksjonen **Elektroniske meldinger** (EM) kan hjelpe deg med å opprettholde ulike elektroniske rapporteringsprosesser for ulike dokumenttyper. I enkelte komplekse tilfeller som støtter [landspesifikke rapporteringsfunksjoner](electronic-messaging.md#country-specific-regulatory-features-supported-by-the-em-functionality), defineres elektroniske meldinger slik at de har en kombinasjon av mange meldingsstatuser, meldingselementstatuser, handlinger, tilleggsfelt og kjørbare klasser. Pakker med data enheter er tilgjengelige for import for disse scenarioene. Hvis du bruker disse dataenhetspakkene, bør du importere dem til en juridisk enhet ved hjelp av verktøyet for behandling av data. Hvis du vil ha mer informasjon om hvordan du bruker verktøyet for databehandling, kan du se [Databehandling](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

Hvis du ikke importerer en dataenhetspakke, kan du manuelt definere EM-funksjonen. I dette tilfellet må du definere følgende elementer:

- [Nummerserier](#sequences)
- [Typer meldingselement](#types)
- [Statuser for meldingselement](#item)
- [Meldingsstatuser](#statuses)
- [Tilleggsfelt](#additional)
- [Innstillinger for kjørbar klasse](#executable)
- [Handlinger for Fyll ut poster](#populate)
- [Fylle ut poster fra flere firmaer](#multiple-companies-populate)
- [Webprogrammer](#applications)
- [Innstillinger for webtjeneste](#settings)
- [Handlinger for meldingsbehandling](#actions)
- [Behandling av elektronisk melding](#processing)

De følgende delene gir mer informasjon om hver av disse elementene.

## <a name="number-sequences"></a><a id="sequences"></a>Nummerserier

Definere nummerserier for både meldinger og meldingselementer. Nummerseriene brukes deretter til å nummerere meldingene og meldingselementene automatisk. Tallene som er tilordnet, skal brukes som unike identifikatorer for meldingene og meldingselementene i systemet. Du kan definere nummerserier for elektroniske meldinger på siden **Økonomimodul** \> **Finansoppsett** \> **Parametere for økonomimodul**.

## <a name="message-item-types"></a><a id="types"></a>Typer meldingselement

Meldingselementtyper identifiserer typer poster som skal brukes i elektroniske meldinger. Du kan definere meldingselementtyper ved å gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Meldingselementtyper**.

## <a name="message-item-statuses"></a><a id="item"></a>Statuser for meldingselement

Meldingselementstatuser identifiserer statusene som gjelder for meldingselementer i behandlingen som du oppretter. Du kan definere meldingselementstatuser ved å gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Meldingselementstatuser**.

**Tillat sletting**-parameteren for en meldingselementstatus angir om du kan slette meldingselementer med denne statusen via **Elektroniske meldinger**-siden eller **Elektroniske meldingselementer**-siden.

## <a name="message-statuses"></a><a id="statuses"></a>Meldingsstatuser

Definer meldingsstatusene som skal være tilgjengelige i meldingsbehandlingen. Du kan definere meldingsstatuser ved å gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Meldingsstatuser**.

Tabellen nedenfor beskriver feltene på siden **Meldingsstatuser**.

| Feltnavn          | Beskrivelse |
|---------------------|-------------|
| Meldingsstatus      | Angi et unikt navn for meldingsstatusen. Meldingsstatusene brukes til å beskrive tilstanden til en elektronisk melding til enhver tid. Navnet du angir, vises på **Elektroniske meldinger**-siden og i en logg som er relatert til elektroniske meldinger. |
| Beskrivelse         | Angi en beskrivelse av meldingsstatusen. |
| Svartype       | Velg svartypen for meldingsstatusen. Noen handlinger i en behandling kan produsere mer enn én svartype. For eksempel kan handlinger av typen **Webtjeneste** produsere svar av typen **Ble kjørt** eller **Teknisk feil**, avhengig av resultatet av kjøringen. I dette tilfellet må meldingsstatuser for begge svartyper defineres. Se [Handlingstyper for meldingsbehandling](#action-types) senere i dette emnet for mer informasjon om handlingstyper og relaterte svartyper. |
| Status for meldingselement | Noen ganger må statusen for en elektronisk melding påvirke statusen til relaterte meldingselementer. Velg en meldingselementstatus i dette feltet for å knytte den til meldingsstatusen. |
| Tillat sletting        | Merk av i denne avmerkingsboksen hvis brukerne skal kunne slette elektroniske meldinger som har denne statusen på siden **Elektroniske meldinger**. |

## <a name="additional-fields"></a><a id="additional"></a>Tilleggsfelt

Med EM-funksjonen kan du samle inn poster fra transaksjonstabeller i Microsoft Dynamics 365 Finance som meldingselementer. Du kan forberede postene for rapportering og deretter rapportere dem. Transaksjonstabeller har imidlertid noen ganger ikke nok informasjon til å fylle ut poster på en måte som oppfyller rapporteringskravene. Du kan fylle ut alle opplysningene som må rapporteres for en post, ved å definere flere felt. Flere felt kan være knyttet til meldinger og meldingselementer. Du kan definere tilleggsfelt ved å gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Tilleggsfelt**.

Tabellen nedenfor beskriver de generelle feltene på siden **Tilleggsfelt**.

| Felt       | beskrivelse |
|-------------|-------------|
| Feltnavn  | Angi navnet på et tilleggsfelt for elektroniske meldinger eller meldingselementer som er knyttet til prosessen. Dette navnet vises i brukergrensesnittet mens du arbeider med prosessen. Navnet kan også brukes i ER-konfigurasjoner som er knyttet til prosessen. |
| beskrivelse | Angi en beskrivelse av tilleggsfeltet. |
| Brukerredigering   | Sett dette alternativet til **Ja** hvis brukerne skal kunne endre verdien i tilleggsfeltet fra brukergrensesnittet. |
| Teller     | Sett dette alternativet til **Ja** hvis tilleggsfeltet må inneholde en nummerserie i en elektronisk melding. Verdien i tilleggsfeltet fylles ut automatisk når en handling av typen **Eksport av elektronisk rapportering** kjøres. |
| Skjult      | Sett dette alternativet til **Ja** hvis tilleggsfeltet skal skjules i grensesnittet på siden **Elektroniske meldinger** eller siden **Elektroniske meldingselementer**. |

I hurtigfanen **Verdier** kan du forhåndsdefinerte verdier som et tilleggsfelt kan ha. Disse verdiene er da tilgjengelige slik at brukere kan velge dem. De behøver derfor ikke å fylles ut manuelt under behandlingen. Tabellen nedenfor beskriver feltene.

| Felt                | beskrivelse |
|----------------------|-------------|
| Feltverdi          | Angi feltverdien som skal brukes for en melding eller et meldingselement under rapportering. |
| Beskrivelse          | Angi en beskrivelse av feltverdien. |
| Kontotype         | Noen feltverdier kan være begrenset til bestemte kontotyper. Velg et av følgende verdier: **Alle**, **Kunde** eller **Leverandør**. |
| Kontokode         | Hvis du har valgt **Kunde** eller **Leverandør** i feltet **Kontotype**, kan du ytterligere begrense bruken av feltverdien til en bestemt gruppe eller tabell. |
| Konto/gruppenummer | Hvis du har valgt **Kunde** eller **Leverandør** i **Kontotype**-feltet, og hvis du har angitt en gruppe eller tabell i feltet **Kontokode**, kan du angi en bestemt gruppe eller kontrollør i dette feltet. |
| Effektiv            | Angi datoen når verdien skal begynne å vurderes. |
| Utløp           | Angi datoen når verdien skal slutte å vurderes. |

Som standard påvirker ikke kombinasjoner av kriterier som er definert av feltene **Konto/gruppenummer**, **Kontokode**, **Gyldig** og **Utløp**, valget av verdier for tilleggsfelt. Disse kombinasjonene kan imidlertid brukes i en kjørbar klasse for å implementere bestemt logikk som beregner verdier for flere felt.

## <a name="executable-class-settings"></a><a id="executable"></a>Innstillinger for kjørbar klasse

En exe-klasse er en X ++-metode eller -klasse som en elektronisk meldingsbehandling kan kalle i forhold til en handling, hvis en evaluering kreves for prosessen.

Du kan definere en utførbar klasse manuelt som må kalles under behandling, ved å gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Innstillinger for kjørbar klasse**. På siden **Innstillinger for kjørbar klasse** oppretter du en linje og angir følgende felt:

| Felt                 | beskrivelse |
|-----------------------|-------------|
| Kjørbar klasse      | Angi navnet som skal brukes under installasjonen av en meldingsbehandlingshandling som denne klassen kalles i forhold til. |
| Beskrivelse           | Angi en beskrivelse av den kjørbare klassen. |
| Navn på kjørbar klasse | Velg en X++-kjørbar klasse. |
| Utføringsnivå       | Dette feltet angis automatisk, fordi verdien er forhåndsdefinert for den valgte kjørbare klassen. Dette feltet begrenser nivået som relatert evaluering kjøres på. |
| Klassebeskrivelse     | Dette feltet angis automatisk, fordi verdien er forhåndsdefinert for den valgte kjørbare klassen. |
| Handlingstype           | Dette feltet er tilgjengelig når **\[EM\]-funksjonen for handlingstype for kjørbar klasse** er aktivert i arbeidsområdet **Funksjonsbehandling**. Bruk dette feltet til å angi handlingstypen for den kjørbare klassen. Dette feltet gir mer presis kontroll over de neste handlingene som er tilgjengelige for den elektroniske meldingen på siden **Elektroniske meldinger**. |

Noen kjørebare klasser kan ha obligatoriske parametere som må være definert før den kjørebare klassen kjøres for første gang. Hvis du vil definere disse parameterne, velger du **Parametere** i handlingsruten. I dialogboksen som vises, angir du feltene, og deretter velger du **OK**. Det er viktig at du velger **OK**. Hvis ikke lagres ikke parameterne til databasen, og den kjørbare klassen kalles ikke på riktig måte.

## <a name="populate-records-actions"></a><a id="populate"></a>Handlinger for Fyll ut poster

Du bruker handlinger for utfylling av poster til å definere handlinger som legger til poster i tabellen Meldingselementer, slik at de kan legges til i en elektronisk melding. Hvis for eksempel den elektroniske meldingen må rapportere kundefakturaer, må du sette opp en fylle-ut-poster-handling som er koblet til **Datakilde**-feltet i kundefakturajournaltabellen.

Du kan angi handlinger for utfylling av poster ved å gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Handlinger for Fyll ut poster**. Opprett en ny post for alle handlinger som skal legge til poster i tabellen, og angi følgende felt:

| Felt       | Beskrivelse |
|-------------|-------------|
| Navn        | Angi et navn for handlingen som fyller ut poster i prosessen. |
| Beskrivelse | Angi en beskrivelse av fyll-ut-poster-handlingen. |

På hurtigfanen **Oppsett av datakilder** legger du til en linje for hver datakilde som brukes for prosessen, og angir følgende felt:

| Felt                  | Beskrivelse |
|------------------------|-------------|
| Navn                   | Skriv inn et navn for datakilden. |
| Type meldingselement      | Velg hvilken type meldingselement som skal brukes når poster opprettes for datakilden. |
| Kontotype           | Velg kontotypen som skal knyttes til postene fra datakilden. |
| Navn på hovedtabell      | Velg tabellen som skal være en datakilde. |
| Feltet Dokumentnummer  | Velg feltet som dokumentnummeret skal tas fra i den valgte hovedtabellen. Verdien til dette feltet brukes som verdi for **Dokumentnummer**-feltet for meldingselementet. |
| Feltet Dokumentdato    | Velg feltet som dokumentdatoen skal tas fra i den valgte hovedtabellen. Verdien til dette feltet brukes som verdi for feltet **Dato for meldingselement** for meldingselementet. |
| Feltet Dokumentkonto | Velg feltet som dokumentkontoen skal tas fra i den valgte hovedtabellen. Verdien til dette feltet brukes som verdi for **Kontonummer**-feltet for meldingselementet. |
| Bedrift                | Dette feltet er tilgjengelig når funksjonen **Spørringer på tvers av firmaer for Handlinger for fyll ut poster** er aktivert i arbeidsområdet **Funksjonsbehandling**. Bruk denne funksjonen til å definere datakilder på tvers av firmaer for de fylle ut posthandlingene. Data kan hentes fra flere firmaer. |
| Brukerspørring             | <p>Hvis du definerer en spørring ved å velge **Rediger spørring** over rutenettet, og du angir kriteriene som må brukes på den valgte hovedtabellen som data fylles ut fra, merkes det automatisk av for denne avmerkingsboksen. Hvis ikke fylles alle postene ut fra den valgte hovedtabellkilden.</p><p>Når funksjonen **Spørringer på tvers av firmaer for Handlinger for fyll ut poster** er aktivert i arbeidsområdet **Funksjonsbehandling**, og poster må samles inn fra flere firmaer, legger du til en linje for hver ekstra juridiske enhet som må inkluderes i rapportering. For hver nye linje velger du **Rediger spørring** og angir et tilknyttet kriterium som er spesifikk for den juridiske enheten som er angitt i **Firma**-feltet i linjen. Når du er ferdig, vil rutenettet **Oppsett av datakilder** inneholde linjer for alle juridiske enheter som må inkluderes i rapportering.</p> |

## <a name="populate-records-from-multiple-companies"></a><a id="multiple-companies-populate"></a>Fylle ut poster fra flere firmaer

Hvis firmaet må rapportere fra flere juridiske enheter i den samme Finance-databasen, definerer du [Handlinger for Fyll ut poster](#populate) for alle juridiske enheter som data må inkluderes fra i rapportering.

Følg disse trinnene for å aktivere denne funksjonen i Finance-miljøet. 

1. Gå til **Arbeidsområder** \> **Funksjonsbehandling**.
2. Søk etter og velg funksjonen **Spørringer på tvers av firmaer for Handlinger for fyll ut poster** i listen.
3. Velg **Aktiver nå**. 

Følg denne fremgangsmåten for å definere [handlinger for Fyll ut poster](#populate) for flere firmaer som det må inkluderes data fra i rapportering.

1. Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Handlinger for Fyll ut poster**.

    Når funksjonen **pørringer på tvers av firmaer for Handlinger for fyll ut poster** er aktivert, inkluderer **Oppsett av datakilder**-rutenettet på siden **Handling for Fyll ut poster** et **Firma**-felt. For eksisterende poster som ble opprettet under det generelle oppsettet for [handlinger for Fyll ut poster](#populate), viser dette feltet IDen til den gjeldende juridiske enheten.

2. I rutenettet **Oppsett av datakilder** legger du til en linje for hver juridiske enhet for datterselskap som må inkluderes i rapportering, og definerer følgende felt:

    | Feltnavn             | Verdi |
    |------------------------|-------|
    | Navn                   | Angi en tekstverdi som vil hjelpe deg med å forstå hvor denne posten kommer fra. Skriv for eksempel inn **Datakildenavn - Datterselskap 1**. |
    | Type meldingselement      | Velg meldingselementtypen som er nødvendig for EM-behandlingen. |
    | Kontotype           | Angi kontotypen som er nødvendig for EM-behandlingen. Hvis EM-behandlingen ikke har noen bestemte kontotyper, velger du **Alle**. |
    | Navn på hovedtabell      | Angi navnet på hovedtabellen som kreves for EM-behandlingen. |
    | Feltet Dokumentnummer  | Angi feltet som inneholder dokumentnummeret i poster for EM-behandlingen. |
    | Feltet Dokumentdato    | Angi feltet som inneholder dokumentdatoen i poster for EM-behandlingen. |
    | Feltet Dokumentkonto | Angi feltet som inneholder dokumentkontoen i poster for EM-behandlingen. |
    | Selskap                | Velg IDen for den juridiske enheten for datterselskap. |
    | Brukerspørring             | Denne boksen blir automatisk merket når du definerer kriterier ved å velge **Rediger spørring**. |

3. For hver nye linje velger du **Rediger spørring** og angir et tilknyttede kriterier for den juridiske enheten som er angitt i **Firma**-feltet i linjen.

## <a name="web-applications"></a><a id="applications"></a>Webprogrammer

Bruk webprograminnstillingene til å definere et webprogram, slik at det støtter Open Authorization (OAuth) 2.0. OAuth er den åpne standarden som gjør at brukere kan gi "sikker delegert tilgang" til programmet på sine vegne, uten å dele tilgangslegitimasjonen. Du kan også gå gjennom godkjenningsprosessen ved å få en autorisasjonskode og tilgangtoken. Du kan definere innstillinger for webprogram ved å gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Webprogrammer**.

Tabellen nedenfor beskriver feltene på siden **Webprogrammer**.

| Felt                        | Beskrivelse |
|------------------------------|-------------|
| Programnavn             | Skriv inn et navn på webprogrammet. |
| Beskrivelse                  | Angi en beskrivelse av webprogrammet. |
| Primær URL-adresse                     | Angi basisinternettadressen til webprogrammet. |
| URL-bane til autorisasjon       | Angi banen som brukes til å angi URL-adressen for godkjenning. |
| URL-bane til token               | Angi banen som brukes til å angi URL-adressen for tokenet. |
| URL-adresse for omadressering                 | Angi URL-adressen for omadressering. |
| Klient-ID                    | Angi klient-ID-en for webprogrammet. |
| Klienthemmelighet                | Angi klienthemmeligheten for webprogrammet. |
| Servertoken                 | Angi servertokenet for webprogrammet. |
| Tilordning av autorisasjonsformat | Velg ER-formatet som brukes til å generere en forespørsel om godkjenning. |
| Importer tokenmodelltilordning   | Velg ER-importmodelltilordningen som brukes til å lagre tilgangstokenet. |
| Innvilget område                | Området som er gitt for forespørsler til programmet. Dette feltet oppdateres automatisk. |
| Tilgangstoken utløper om  | Resten av tiden før tokenet utløper. Dette feltet oppdateres automatisk. | 
| Aksepter                       | Angi egenskapen **Godta** for webforespørselen. For eksempel angi **application/vnd.hmrc.1.0+json**. |
| Innholdstype                 | Angi innholdstypen. For eksempel angi **application/json**. |

I tillegg er disse knappene er tilgjengelige i handlingsruten på siden **webprogrammer** for å støtte godkjenningsprosessen:

- **Få autorisasjonskode** – Initialisere godkjenning av webprogrammet. Denne funksjonen bruker ER-formatet som er angitt i feltet **Tilordning av autorisasjonsformat** til å generere en autorisasjonsforespørsel.
- **Få tilgangstoken** – Initialiser prossen med henting av et tilgangstoken.
- **Oppdater tilgangstoken** – Oppdater et tilgangstoken. Denne funksjonen bruker ER-formatet som er angitt i feltet **Importer tokenmodelltilordning** til å importere informasjon om det mottatte tilgangstokenet.

Når et tilgangstoken til et webprogram er lagret i systemets database i kryptert format, kan det brukes for forespørsler til en webtjeneste. For sikkerhetsformål må tilgang til tokenet begrenses til sikkerhetsrollene som har tillatelse til å håndtere disse forespørslene. Hvis noen utenfor sikkerhetsgruppen forsøker å adressere en forespørsel, mottar de en feilmelding som sier at de ikke har tillatelse til å samhandle via valgt webprogram. For å konfigurere sikkerhetsroller som har tilgang til tokenet, kan du bruke **Sikkerhetsroller**-hurtigkategorien på **Webprogrammer**-siden. Hvis sikkerhetsroller ikke er definert for et webprogram, kan bare en systemansvarlig samhandle via dette webprogrammet.

For hver handling med det valgte webprogrammet lagrer hurtigfanen **Handlingslogg** informasjon om brukeren og datoen og klokkeslettet.

Enkelte webtjenester krever at ulike hoder er inkludert i forespørslene. Systemadministratoren kan definere flere hoder og deres verdier i hurtigfanen **Tilleggshoder**, og deretter bruke dem under forespørselsgenerering.

## <a name="web-service-settings"></a><a id="settings"></a>Innstillinger for webtjeneste

Bruk innstillinger for webtjeneste til å definere direkte dataoverføring til en webtjeneste. Du kan definere innstillinger for webtjeneste ved å gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Innstillinger for webtjeneste**.

Tabellen nedenfor beskriver feltene på siden **Innstillinger for webtjeneste**.

| Felt                          | Beskrivelse |
|--------------------------------|-------------|
| Webtjeneste                    | Skriv inn et navn på webtjenesten. |
| Beskrivelse                    | Angi en beskrivelse av webtjenesten. |
| Internett-adresse               | <p>Angi internettadressen til webtjenesten. Hvis et webprogram er angitt for webtjenesten, og hvis Internett-adressen til webtjenesten må være den samme som den som er definert for webprogrammet, velger du **Kopier primær URL-adresse**. Primær URL-adresse for webprogrammet blir deretter kopiert til dette feltet.</p><p>**Advarsel:** Tredjepartstjenester eller andre tjenester du konfigurerer her, krever ikke sertifisering og oppfyller kanskje ikke Microsofts personvernstandarder. Du bør se gjennom personverndokumentasjonen for hver tjeneste og samarbeide med hver leverandør for å få mer informasjon om samsvarsnivået som tjenesten tilbyr. Du er ansvarlig for å sikre at disse tjenestene oppfyller sikkerhets-, personvern- og juridiske standarder. Du bærer risikoen ved å bruke tjenestene. Microsoft gir ingen uttrykte garantier eller betingelser. Vi anbefaler på det sterkeste at du bare bruker tjenester som tilbyr sikre og autoriserte tilkoblinger, for eksempel HTTPS.</p> |
| Sertifikat                    | Velg et Azure Key Vault-sertifikat som tidligere er definert. |
| webprogram                | Velg et webprogram som tidligere er definert. |
| Svartypen – XML        | Sett dette alternativet til **Ja** hvis svartypen er XML. |
| Forespørselsmetode                 | Angi metoden for forespørselen. HTTP definerer et sett med forespørselsmetoder som angir handlingen som skal utføres for en gitt ressurs. Forespørselsmetoden kan være **HENT**, **POSTER** eller en annen HTTP-metode. |
| Forespørselshoder                | Angi forespørselshoder. Et forespørselshode er et HTTP-hode som kan brukes i en HTTP-forespørsel. Det er ikke knyttet til innholdet i meldingen. |
| Aksepter                         | Angi egenskapen Godta for webforespørselen. |
| Godta koding                | Angi verdien Godta koding. HTTP-overskriften i Godta koding-forespørselen annonserer innholdskodingen som klienten kan forstå. Denne innholdskoding er vanligvis en komprimeringsalgoritme. |
| Innholdstype                   | Angi innholdstypen. HTTP-enhetshodet for innholdstypen indikerer medietypen for ressursen. |
| Kode for fullført svar       | Angi HTTP-statuskoden som angir at forespørselen var vellykket. |
| Formattilordning for forespørselshoder | Velg ER-formatet som brukes til å generere webforespørselshoder. |

## <a name="message-processing-actions"></a><a id="actions"></a>Handlinger for meldingsbehandling

Du bruker meldingsbehandlingshandlinger til å opprette handlinger for prosessene og sette opp parametere. Du kan angi handlinger for meldingsbehandling ved å gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Handlinger for meldingsbehandling**.

Tabellen nedenfor beskriver feltene på siden **Handlinger for meldingsbehandling**.

### <a name="general-fasttab"></a>Hurtigfanen Generelt

| Felt                                     | Beskrivelse |
|-------------------------------------------|-------------|
| Handlingstype                               | Velg handlingstypen. Hvis du vil ha informasjon om de tilgjengelige alternativene, se delen [Handlingstyper for meldingsbehandling](#action-types) senere i dette emnet. |
| Formattilordning                            | Velg ER-formatet som skal kalles for handlingen. Dette feltet er bare tilgjengelig for handlingene av typen **Eksport av elektronisk rapportering**, **Import av elektronisk rapportering** og **Melding om eksport av elektronisk rapportering**. |
| Formattilordning for URL-bane               | Velg ER-formatet som skal kalles for handlingen. Dette formatet brukes til å skrive banen til URL-adressen som skal legges til den grunnleggende Internett-adressen som er angitt for den valgte webserveren. Dette feltet er bare tilgjengelig for handlingene av typen **Webtjeneste**. |
| Type meldingselement                         | Velg hvilken type poster som skal evalueres for handlingen. Dette feltet er tilgjengelig for handlinger av typen **Utføringsnivå for meldingselement**, **Eksport av elektronisk rapportering**, **Import av elektronisk rapportering** og **Webtjeneste** og noen andre typer. Hvis du lar dette feltet stå tomt, vurderes alle meldingselementtyper som er definert for meldingsbehandlingen. |
| Kjørbar klasse                          | Velg en eksisterende utførbar klasseinnstilling. Dette feltet er bare tilgjengelig for handlingene av typen **Utføringsnivå for meldingselement** og **Utføringsnivå for meldingselement**. |
| Handling for Fyll ut poster                   | Velg en eksisterende handling for ut fylle ut poster. Dette feltet er bare tilgjengelig for handlingene av typen **Fyll ut poster**. |
| Webtjeneste                               | Velg en eksisterende webtjeneste. Dette feltet er bare tilgjengelig for handlingene av typen **Webtjeneste**. |
| Filnavn som skal sendes                         | Angi navnet på vedlegget til en elektronisk melding som må sendes av denne handlingen. Hvis flere vedlegg har samme opprinnelige filnavn, blir det nyeste vedlegget sendt. Hvis det ikke blir funnet noe vedlegg med det angitte opprinnelige filnavnet, sendes forespørselen uten innhold. Dette feltet er bare tilgjengelig for handlingene av typen **Webtjeneste**. |
| Filnavn                                 | Angi navnet på filen som blir resultatet av handlingen. Denne filen kan være svar fra webserveren eller rapporten som genereres. Dette feltet er bare tilgjengelig for handlinger av typene **Webtjeneste** og **Melding om eksport av elektronisk rapportering**. |
| Knytt filer til kildedokumenter          | Merk av i denne avmerkingsboksen for å knytte genererte filer til poster i en referert hovedtabell for EM-varer. Dette feltet er bare tilgjengelig for handlinger av typene **Eksport av elektronisk rapportering** og **Webtjeneste**. |
| Legg til filer fra utdataarkiv til elementer | Merk av i denne boksen for å trekke ut separate XML-filer fra utdataarkivfilen og legge dem ved de tilsvarende elektroniske meldingselementene. Dette feltet er bare tilgjengelig for handlinger av typen **Eksport av elektronisk rapportering**. |
| Antall meldingselementer per eksport        | Angi grensen på antall meldingselementer som må inkluderes i én fil (melding). Dette feltet er bare tilgjengelig for handlinger av typen **Eksport av elektronisk rapportering**. |
| Bruk ER-kilde                             | Merk av i denne boksen for å bruke ER-kildeparametere for import. Hvis ikke brukes vedlegget fra den elektroniske meldingen. Dette feltet er bare tilgjengelig for handlinger av typen **Import av elektronisk rapportering**. |
| Vis dialogboks                               | Sett dette alternativet til **Ja** hvis en dialogboks må vises til brukere før rapporten er generert. Dette feltet er bare tilgjengelig for handlinger av typen **Melding om eksport av elektronisk rapportering**. |

#### <a name="message-processing-action-types"></a><a id="action-types"></a>Handlingstyper for meldingsbehandling

Følgende alternativer er tilgjengelige i **Handlingstyper**-feltet:

- **Opprett melding** – Bruk denne handlingstypen hvis du vil la brukere manuelt opprette meldinger på siden **Elektronisk melding**. En innledende status kan ikke defineres for en handling av denne typen.
- **Fyll ut poster** – Denne handlingstypen må allerede være definert. Knytt den til en handling av typen Fyll ut poster for å aktivere handlingen slik at den inkluderes i behandlingen. Det antas at denne handlingstypen brukes for den første handlingen i meldingsbehandling (når ingen elektronisk melding er opprettet på forhånd) eller for en handling som legger til meldingselementer i en melding som tidligere ble opprettet av en handling av typen **Opprett melding**. Derfor kan en resultatstatus bare settes opp for meldingselementer for handlinger av denne typen. En innledende status kan bare defineres for meldinger.
- **Utføringsnivå for melding** – Bruk denne handlingstypen til å definere en exe-klasse som skal evalueres på meldingsnivået.
- **Utføringsnivå for meldingselement** – Bruk denne handlingstypen til å definere en exe-klasse som skal evalueres på meldingselementnivået.
- **Eksport av elektronisk rapportering** – Bruk denne typen for handlinger som skal generere en rapport som er basert på en eksporterende ER-konfigurasjon på meldingselementnivå.
- **Melding om eksport av elektronisk rapportering** – Bruk denne handlingstypen for handlinger som skal generere en rapport som er basert på en eksporterende ER-konfigurasjon på meldingsnivå (for eksempel når en melding ikke inneholder noen meldingselementer).
- **Import av elektronisk rapportering** – Bruk denne handlingstypen for handlinger som skal generere en rapport som er basert på en importerende ER-konfigurasjon.
- **Behandling av bruker på meldingsnivå** – Bruk denne handslingstypen for handlinger som forutsetter manuell handling av brukeren på meldingsnivå. Brukeren kan for eksempel oppdatere statusen for meldinger.
- **Brukerbehandling** – Bruk denne handslingstypen for handlinger som forutsetter manuell handling av brukeren på meldingselementnivå. Brukeren kan for eksempel oppdatere statusen for meldingselementer.
- **Webtjeneste** – Bruk denne handlingstypen for handlinger som skal overføre en generert rapport til en webtjeneste. Denne handlingstypen brukes ikke for kommunikasjonsrapportering for italienske kjøps- og salgsfakturaer. For denne handlingstypen inkludererer siden **Handlinger for meldingsbehandling** hurtigkategorien **Diverse detaljer**, der du kan angi en bekreftelsestekst. Denne bekreftelsesteksten vises for brukerne før forespørsler adresseres til den valgte webtjenesten.
- **Forespørsel om verifisering** – Bruk denne handlingstypen til å forespørre bekreftelse fra en server.

### <a name="initial-statuses-fasttab"></a>Hurtigfane for opprinnelige statuser

> [!NOTE]
> Hurtigfanen **Opprinnelige statuser** er ikke tilgjengelig for handlinger som har den innledende handlingstypen **Opprett melding**.

| Felt               | Beskrivelse |
|---------------------|-------------|
| Status for meldingselement | Velg meldingselementstatusen som den valgte meldingsbehandlingshandlingen skal evalueres for. |
| Beskrivelse         | En beskrivelse av den valgte meldingselementstatusen. |

### <a name="result-statuses-fasttab"></a>Hurtigfanen Resultatstatuser

| Felt               | Beskrivelse |
|---------------------|-------------|
| Meldingsstatus      | Velg meldingsstatusene som den valgte meldingsbehandlingshandlingen skal evalueres for. Dette feltet er bare tilgjengelig for meldingsbehandlingshandlinger som evalueres på meldingsnivå. For eksempel er den tilgjengelig for handlinger av typen **Eksport av elektronisk rapportering** og **Import av elektronisk rapportering**, men den er ikke tilgjengelig for handlinger av typen **Brukerbehandling** og **Utføringsnivå for meldingselement**. |
| Beskrivelse         | En beskrivelse av den valgte meldingsstatusen. |
| Svartype       | Svartypen for den valgte meldingsstatusen. |
| Status for meldingselement | Velg de resulterende statusene som skal være tilgjengelige etter den valgte meldingsbehandlingshandlingen er evaluert. Dette feltet er bare tilgjengelig for meldingsbehandlingshandlinger som evalueres på meldingselementnivå. For eksempel er det tilgjengelig for handlinger av typene **Brukerbehandling** og **Utføringsnivå for meldingselement**. For meldingsbehandlingshandlinger som evalueres på meldingsnivået, viser dette feltet meldingselementstatusen som ble angitt for den valgte meldingsstatus. |

Følgende tabell viser resultatstatusene som må defineres for ulike handlingstyper og svartyper.

| Handlingstype for elektronisk melding / Svartype | Ble kjørt | Forretningsfeil | Teknisk feil | Brukerdefinert | Annuller |
|----------------------------------------------|-----------------------|----------------|-----------------|--------------|--------|
| Opprett melding                               | X                     |                |                 |              |        |
| Eksport av elektronisk rapportering                  | X                     |                |                 |              |        |
| Import av elektronisk rapportering                  |                       |                |                 |              |        |
| Webtjeneste                                  | X                     |                | X               |              |        |
| Brukerbehandling                              |                       |                |                 |              |        |
| Utføringsnivå for melding                      |                       |                |                 |              |        |
| Fyll ut poster                             |                       |                |                 |              |        |
| Utføringsnivå for meldingselement                 |                       |                |                 |              |        |
| Forespørsel om verifisering                         | X                     | X              | X               |              |        |
| Melding om eksport av elektronisk rapportering          | X                     |                |                 |              |        |
| Behandling av bruker på meldingsnivå                |                       |                |                 |              |        |

## <a name="electronic-message-processing"></a><a id="processing"></a>Behandling av elektronisk melding

Elektronisk meldingsbehandling er et grunnleggende konsept i funksjonen Elektroniske meldinger. Det samler handlinger som skal evalueres for den elektroniske meldingen. Handlingene kan kobles til via en innledende status og en resultatstatus. Eventuelt kan handlinger av typen **Brukerbehandling** startes uavhengig av hverandre. Hvis du vil definere behandling av elektroniske meldinger, kan du gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Behandling av elektronisk melding**.

Hurtigfanen **Handling** lar deg legge til forhåndsdefinerte handlinger til behandlingen. Du kan angi om en handling må kjøres separat, eller om den kan startes av behandlingen. Hvis du vil angi at en handling i behandlingen kan initialiseres bare av en bruker, kan du angi feltet **Kjør separat** til **Ja** for den aktuelle handlingen. Hvis en handling skal startes av behandling av meldinger eller meldingselementer som har statusen som er definert som opprinnelig status for handlingen, settes feltet **Kjør separat** til **Nei**. Handlinger av typen **Brukerhandling** må alltid kjøres separat.

Noen ganger må flere handlinger samles i en sekvens, selv om den første handlingen defineres slik at den kjøres separat. En bruker må for eksempel initialisere rapportgenerering. Men umiddelbart etter at rapporten er generert, må den sendes til en webtjeneste, og svaret fra webtjenesten må vises i systemet. I denne situasjonen kan du opprette en uatskillelig sekvens for handlinger som alltid må kjøres sammen. I **Handlingen**-hurtigkategorien velger du **Uatskillelig rekkefølge** over rutenettet og oppretter en sekvens. For alle handlinger som må kjøres sammen i en sekvens, velger du deretter rekkefølgen i feltet **Uatskillelig rekkefølge**. I dette ekstemplet kan **Kjør separat**-feltet settes til **Ja** for den første handlingen i sekvensen, og **Nei** for alle andre handlinger.

Handlinger av typene **Eksport av elektronisk rapportering** og **Melding om eksport av elektronisk rapportering** kjører et ER-format som har inndataparametere. Hvis den elektroniske meldingsbehandlingen inneholder handlinger av én av disse typene, må du angi verdiene for inndataparameterne før rapportgenerering. På denne måten kan systemet bruke en satsvis forretningsprosess til å generere rapporten. Du kan velge **Parametere** over rutenettet for å definere parameterne for den valgte handlingstypen eller (**Eksport av elektronisk rapportering** eller **Melding om eksport av elektronisk rapportering**). Merk av for **Bruk parametere** for handlingen som må kjøres med de angitte parameterne i en satsvis prosess.

Bruk hurtigfanen **Tilleggsfelt for meldingselement** til å legge til forhåndsdefinerte tilleggsfelt som er knyttet til meldingselementer. Du må legge til flere felt for hver meldingstype som feltene er knyttet til. Du kan angi en standardverdi som skal tilordnes tilleggsfeltet under behandling.

Bruk hurtigfanen **Tilleggsfelt for melding** til å legge til forhåndsdefinerte tilleggsfelt som er knyttet til meldinger. Du kan angi en standardverdi som skal tilordnes tilleggsfeltet under behandling.

Bruk hurtigfanen **Sikkerhetsroller** til å definere sikkerhetsroller som er forhåndsdefinert i systemet for bestemt behandling. Brukere som har en bestemt rolle, ser bare behandling som er definert for denne rollen.

Bruk **Parti**-hurtigfanen til å definere behandlingen til å arbeide i en satsvis prosess. Vi anbefaler at du definerer en satsvis prosess for behandlingen direkte på siden **Elektroniske meldinger** eller **Elektroniske meldingselementer**, når du velger **Kjør behandling** i handlingsruten for å starte behandlingen.
