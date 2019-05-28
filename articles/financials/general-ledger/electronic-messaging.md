---
title: Elektroniske meldinger
description: Dette emnet gir oversikt og oppsettinformasjon for elektroniske meldinger i Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 2753f2828b4890d9893a1538e905bd7061e1bc33
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536877"
---
# <a name="electronic-messaging"></a>Elektronisk meldingssystem

[!include [banner](../includes/banner.md)]
[!include [preview-banner](../includes/preview-banner.md)]

Dette emnet gir oversikt og oppsettinformasjon for elektroniske meldinger i Microsoft Dynamics 365 for Finance and Operations.

Myndigheter og lovgivende myndighetene i forskjellige land og områder over hele verden har nylig implementert rapporteringskrav for firmaer som er registrert i disse landene eller regionene. Formålet med kravene er å aktivere data som hentes fra disse firmaene, i elektronisk format direkte fra systemene der de ble beregnet, lagret og behandlet.

Funksjonen for elektroniske meldinger i Finance and Operations støtter forskjellige prosesser for elektronisk samhandling mellom Finance and Operations og systemene som myndigheter og juridiske myndigheter tilbyr for rapportering, sending og mottak av offisiell informasjon.

Funksjonen for elektroniske meldinger er integrert i modulen **Elektronisk rapportering**-modulen (ER). Derfor kan du definere ER-formater for elektroniske meldinger. For mer informasjon, se [Elektronisk rapportering (ER)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

Elektroniske meldinger er basert på følgende enheter:

- **Elektronisk melding** – en rapport eller deklarasjon som skal rapporteres og/eller overføres internt. Et eksempel er en rapport som er sendt til et skattekontor.
- **Elektroniske meldingselementer** – poster som skal inkluderes i meldingen som rapporteres.
- **Behandling av elektronisk melding** – en handlingskjede som må kjøres for å samle de nødvendige dataene, generere rapporter, lagre data i Microsoft Azure Blob-lagring, sende rapporter utenfor systemet, motta svar fra utenfor systemet og, basert på informasjonen som mottas, oppdatere databasen. Handlingene i kjeden kan være tilkoblet eller frakoblet

Illustrasjonen nedenfor viser flyten av data for elektroniske meldinger.

![Dataflyt for elektroniske meldinger](media/electronic-messaging-data-flow.png)

Funksjonen for elektroniske meldinger støtter følgende scenarioer:

- Manuelt opprette meldinger og generere rapporter som er basert på tilknyttede eksporterende ER-formater av ulike typer: Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, tekst og Microsoft Word.
- Automatisk opprette og behandle meldinger som er basert på informasjonen som ble forespurt og mottatt fra en myndighet via et tilknyttet importerende ER-format.
- Samle inn og behandle informasjon fra en datakilde som meldingselementer. Datakilden er en Finance and Operations-tabell.
- Lagre mer informasjon og evaluere ulike verdier ved å kalle spesielt definerte kjørbare klasser i forhold til meldinger eller meldingselementer.
- Aggregere informasjon som samles inn, i meldingselementer, dele informasjonen inn i meldinger og generere rapporter som er i tilknyttede eksporterende ER-formater.
- Sende rapportene som genereres, til en webtjeneste ved hjelp av sikkerhetsinformasjon som lagres i Azure Key Vault.
- Motta et svar fra en webtjeneste, tolke svaret og oppdatere data i Finance and Operations etter behov.
- Lagre og gå gjennom alle rapportene som genereres.
- Lagre og gå gjennom all logginformasjon som er knyttet til handlinger som utføres for en melding eller et meldingselement.
- Styre behandlingen gjennom forskjellige meldingsstatuser og meldingselementstatuser.

## <a name="set-up-electronic-messaging"></a>Opprette elektroniske meldinger

Elektroniske meldinger kan hjelpe deg med å opprettholde ulike elektroniske rapporteringsprosesser for ulike dokumenttyper. I enkelte komplekse tilfeller defineres elektroniske meldinger slik at de har en kombinasjon av mange meldingsstatuser, meldingselementstatuser, handlinger, tilleggsfelt og kjørbare klasser. Pakker med data enheter er tilgjengelige for import for disse scenarioene. Hvis du bruker disse dataenhetspakkene, bør du importere dem til en juridisk enhet ved hjelp av verktøyet for behandling av data. Hvis du vil ha mer informasjon om hvordan du bruker verktøyet for databehandling, kan du se [Databehandling](../../dev-itpro/data-entities/data-entities-data-packages.md).

Hvis du ikke importerer en dataenhetspakke, kan du manuelt definere funksjonen Elektroniske meldinger. I dette tilfellet må du definere følgende elementer:

- [Nummerserier](#number-sequences)
- [Meldingselementtyper og -statuser](#message-item-types-and-statuses)
- [Meldingsstatuser](#message-statuses)
- [Tilleggsfelt](#additional-fields)
- [Innstillinger for kjørbar klasse](#executable-class-settings)
- [Handlinger for Fyll ut poster](#populate-records-actions)
- [Webprogrammer](#web-applications)
- [Innstillinger for webtjeneste](#web-service-settings)
- [Handlinger for meldingsbehandling](#message-processing-actions)
- [Behandling av elektronisk melding](#electronic-message-processing)

De følgende delene gir mer informasjon om hver av disse elementene.

### <a name="number-sequences"></a>Nummerserier

Definere nummerserier for både meldinger og meldingselementer. Nummerseriene brukes til å nummerere meldingene og meldingselementene automatisk. Tallene som er tilordnet, skal brukes som unike identifikatorer for meldingene og meldingselementene i systemet. Du kan definere nummerserier for elektroniske meldinger på siden **Økonomiparametere** (**Økonomimodul** \> **Finansoppsett** \> **Parametere for økonomimodul**).

### <a name="message-item-types-and-statuses"></a>Meldingselementtyper og -statuser

Meldingselementtyper identifiserer typer poster som skal brukes i elektroniske meldinger. Du kan definere meldingselementtyper på siden **Typer meldingselement** (**Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Typer meldingselement**).

Meldingselementstatuser identifiserer statusene som gjelder for meldingselementer i behandlingen som du oppretter. Du kan definere meldingselementtyper på siden **Statuser for meldingselement** (**Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Statuser for meldingselement**).

**Tillat sletting**-parameteren for en meldingselementstatus angir om brukere kan slette meldingselementer med denne statusen via **Elektroniske meldinger**-siden eller **Elektroniske meldingselementer**-siden.

### <a name="message-statuses"></a>Meldingsstatuser

Definer meldingsstatusene som skal være tilgjengelige i meldingsbehandlingen. Du kan definere meldingsstatuser på siden **Meldingsstatuser** (**Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Meldingsstatuser**).

Tabellen nedenfor beskriver feltene på siden **Meldingsstatuser**.

| Feltnavn          | Beskrivelse |
|---------------------|-------------|
| Meldingsstatus      | Angi et unikt navn for meldingsstatusen. Meldingsstatusene brukes til å beskrive tilstanden til en elektronisk melding til enhver tid. Navnet du angir, vises på **Elektroniske meldinger**-siden og i en logg som er relatert til elektroniske meldinger. |
| Beskrivelse         | Angi en beskrivelse av meldingsstatusen. |
| Svartype       | Velg svartypen for meldingsstatusen. Noen handlinger i en behandling kan produsere mer enn én svartype. For eksempel kan handlinger av typen **Webtjeneste** produsere svar av typen **Ble kjørt** eller **Teknisk feil**, avhengig av resultatet av kjøringen. I dette tilfellet må definere meldingsstatuser for begge svartyper. Se [Handlingstyper for meldingsbehandling](#message-processing-action-types) for mer informasjon om handlingstyper og relaterte svartyper. |
| Status for meldingselement | Noen ganger må statusen for en elektronisk melding påvirke statusen til relaterte meldingselementer. Velg en meldingselementstatus i dette feltet for å knytte den til meldingsstatusen. |
| Tillat sletting        | Merk av i denne avmerkingsboksen hvis brukerne skal kunne slette elektroniske meldinger som har denne statusen på siden **Elektroniske meldinger**. |

### <a name="additional-fields"></a>Tilleggsfelt

Funksjonen Elektroniske meldinger lar deg fylle inn poster fra en transaksjonell tabell. Du kan forberede postene for rapportering og deretter rapportere dem. Transaksjonstabeller har imidlertid noen ganger ikke nok informasjon til å fylle ut poster på en måte som oppfyller rapporteringskravene. Du kan fylle ut alle opplysningene som må rapporteres for en post, ved å definere flere felt. Flere felt kan være knyttet til både meldinger og meldingselementer. Du kan definere flere felt på siden **Tilleggsfelt** (**Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Tilleggsfelt**).

Tabellen nedenfor beskriver de generelle feltene på siden **Tilleggsfelt**.

| Felt       | Beskrivelse |
|-------------|-------------|
| Feltnavn  | Angi navnet på en tilleggsattributt for meldingselementer som er knyttet til prosessen. Dette navnet vises i brukergrensesnittet mens du arbeider med prosessen. Det kan også brukes i ER-konfigurasjoner som er knyttet til prosessen. |
| Beskrivelse | Angi en beskrivelse av tilleggsfeltet. |
| Brukerredigering   | Sett dette alternativet til **Ja** hvis brukerne skal kunne endre verdien i tilleggsfeltet fra brukergrensesnittet. |
| Teller     | Sett dette alternativet til **Ja** hvis tilleggsfeltet må inneholde en nummerserie i en elektronisk melding. Verdien i tilleggsfeltet fylles ut automatisk når en handling av typen **Eksport av elektronisk rapportering** kjøres. |
| Skjult      | Sett dette alternativet til **Ja** hvis ekstrafeltet skal skjules i brukergrensesnittet. |

Hvert tilleggsfelt kan ha forskjellige verdier for behandlingen. Du kan definere disse verdiene i **Verdier**-hurtigkategorien. Tabellen nedenfor beskriver feltene.

| Felt                | Beskrivelse |
|----------------------|-------------|
| Feltverdi          | Angi feltverdien som skal brukes for en melding eller et meldingselement under rapportering. |
| Beskrivelse          | Angi en beskrivelse av feltverdien. |
| Kontotype         | Noen feltverdier kan være begrenset til bestemte kontotyper. Velg et av følgende verdier: **Alle**, **Kunde** eller **Leverandør**. |
| Kontokode         | Hvis du har valgt **Kunde** eller **Leverandør** i feltet **Kontotype**, kan du ytterligere begrense bruken av feltverdien til en bestemt gruppe eller tabell. |
| Konto/gruppenummer | Hvis du har valgt **Kunde** eller **Leverandør** i **Kontotype**-feltet, og hvis du har angitt en gruppe eller tabell i feltet **Kontokode**, kan du angi en bestemt gruppe eller kontrollør i dette feltet. |
| Effektiv            | Angi datoen når verdien skal begynne å vurderes. |
| Utløp           | Angi datoen når verdien skal slutte å vurderes. |

Som standard påvirker ikke kombinasjoner av kriterier som er definert av feltene **Konto/gruppenummer**, **Kontokode**, **Gyldig** og **Utløp**, valget av verdier for tilleggsfelt. Disse kombinasjonene kan imidlertid brukes i en kjørbar klasse for å implementere bestemt logikk som beregner verdier for flere felt.

### <a name="executable-class-settings"></a>Innstillinger for kjørbar klasse

En exe-klasse er en X ++-metode eller -klasse som en elektronisk meldingsbehandling kan kalle i forhold til en handling, hvis en evaluering kreves for prosessen.

Du kan manuelt definere en exe-klasse på siden **Innstillinger for kjørbar klasse** (**Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Innstillinger for kjørbar klasse**). Opprett en linje, og angi følgende felt.

| Felt                 | beskrivelse |
|-----------------------|-------------|
| Kjørbar klasse      | Angi navnet som skal brukes under installasjonen av en meldingsbehandlingshandling som denne klassen kalles i forhold til. |
| beskrivelse           | Angi en beskrivelse av den kjørbare klassen. |
| Navn på kjørbar klasse | Velg en X++-kjørbar klasse. |
| Utføringsnivå       | Dette feltet angis automatisk, fordi verdien må forhåndsdefineres for den valgte kjørbare klassen. Dette feltet begrenser nivået som relatert evaluering kjøres på. |
| Klassebeskrivelse     | Dette feltet angis automatisk, fordi verdien må forhåndsdefineres for den valgte kjørbare klassen. |

Noen kjørebare klasser kan ha obligatoriske parametere som må være definert før den kjørebare klassen kjøres for første gang. Du definerer disse parameterne ved å velge **Parametere** i handlingsruten, angi feltene i dialogboksen som vises, og deretter velge **OK**. Det er viktig at du velger **OK**. Hvis ikke lagres ikke parameterne til databasen, og den kjørbare klassen kalles ikke på riktig måte.

### <a name="populate-records-actions"></a>Handlinger for Fyll ut poster

Du bruker handlinger for utfylling av poster til å definere handlinger som legger til poster i tabellen Meldingselementer, slik at de kan legges til i en elektronisk melding. Hvis for eksempel den elektroniske meldingen må rapportere kundefakturaer, må du sette opp en fylle-ut-poster-handling som er koblet til **Datakilde**-feltet i kundefakturajournaltabellen. Du kan angi handlinger for utfylling av poster på siden **Handling for Fyll ut poster** (**Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Handlinger for Fyll ut poster**). Opprett en ny post for alle handlinger som skal legge til poster i tabellen, og angi følgende felt:

| Felt       | Beskrivelse |
|-------------|-------------|
| Navn        | Angi et navn for handlingen som fyller ut poster i prosessen. |
| Beskrivelse | Angi en beskrivelse av fyll-ut-poster-handlingen. |

På hurtigfanen **Oppsett av datakilder** legger du til en linje for hver datakilde som brukes for prosessen, og angir følgende felt:

| Felt                  | beskrivelse |
|------------------------|-------------|
| Navn                   | Skriv inn et navn for datakilden. |
| Type meldingselement      | Velg hvilken type meldingselement som skal brukes når poster opprettes for datakilden. |
| Kontotype           | Velg kontotypen som skal knyttes til postene fra datakilden. |
| Navn på hovedtabell      | Velg tabellen i Finance and Operations som skal være en datakilde. |
| Feltet Dokumentnummer  | Velg feltet som dokumentnummeret skal tas fra i den valgte tabellen. |
| Feltet Dokumentdato    | Velg feltet som dokumentdatoen skal tas fra i den valgte tabellen. |
| Feltet Dokumentkonto | Velg feltet som dokumentkontoen skal tas fra i den valgte tabellen. |
| Brukerspørring             | Hvis det er merket av i denne avmerkingsboksen, du kan definere en spørring ved å velge **Rediger spørring** over rutenettet. Hvis ikke fylles alle postene ut fra den valgte datakilden. |

### <a name="web-applications"></a>Webprogrammer

Du bruker webprograminnstillingene til å definere et webprogram, slik at det støtter Open Authorization (OAuth) 2.0. OAuth er den åpne standarden som gjør at brukere kan gi "sikker delegert tilgang" til programmet på sine vegne, uten å dele tilgangslegitimasjonen. Du kan også gå gjennom godkjenningsprosessen ved å få en autorisasjonskode og tilgangtoken. Du kan definere innstillinger for webprogram på siden **Webprogrammer** (**Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Webprogrammer**).

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
| Tilgangstoken utløper om  | Resten av tiden før tokenet utløper. | 
| Aksepter                       | Angi egenskapen **Godta** for webforespørselen. For eksempel angi **application/vnd.hmrc.1.0+json**. |
| Innholdstype                 | Angi innholdstypen. For eksempel angi **application/json**. |

I tillegg er disse knappene er tilgjengelige i handlingsruten på siden **webprogrammer** for å støtte godkjenningsprosessen:

- **Få autorisasjonskode** – Initialisere godkjenning av webprogrammet.
- **Få tilgangstoken** – Initialiser prossen med henting av et tilgangstoken.
- **Oppdater tilgangstoken** – Oppdater et tilgangstoken.

Når et tilgangstoken til et webprogram er lagret i systemets database i kryptert format, kan det brukes for forespørsler til en webtjeneste. For sikkerhetsformål må tilgang for tilgangstokenet begrenses til sikkerhetsrollene som må ha tillatelse til å håndtere disse forespørslene. Hvis brukere utenfor sikkerhetsgruppen forsøker å adressere en forespørsel, mottar de en feilmelding som sier at de ikke har tillatelse til å samhandle via valgt webprogram. For å konfigurere sikkerhetsroller som må ha tilgang til tokenet, kan du bruke **Sikkerhetsroller**-hurtigkategorien på **Webprogrammer**-siden. Hvis sikkerhetsroller ikke er definert for et webprogram, kan bare en systemansvarlig samhandle via dette webprogrammet.

### <a name="web-service-settings"></a>Innstillinger for webtjeneste

Du bruker innstillinger for webtjeneste til å definere direkte dataoverføring til en webtjeneste. Du kan definere innstillinger for webtjenester på siden **Innstillinger for webtjeneste** (**Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Innstillinger for webtjeneste**) .

Tabellen nedenfor beskriver feltene på siden **Innstillinger for webtjeneste**.

| Felt                          | beskrivelse |
|--------------------------------|-------------|
| Webtjeneste                    | Skriv inn et navn på webtjenesten. |
| beskrivelse                    | Angi en beskrivelse av webtjenesten. |
| Internett-adresse               | Angi internettadressen til webtjenesten. Hvis et webprogram er angitt for webtjenesten, og hvis Internett-adressen til webtjenesten må være den samme som den som er definert for webprogrammet, velger du **Kopier primær URL-adresse** for å kopiere den primære URL-adressen for webapplikasjonen til dette feltet. |
| Sertifikat                    | Velg et Key Vault-sertifikat som tidligere er definert. |
| webprogram                | Velg et Key Vault-sertifikat som tidligere er definert. |
| Svartypen – XML        | Sett dette alternativet til **Ja** hvis svartypen er XML. |
| Forespørselsmetode                 | Angi metoden for forespørselen. HTTP definerer et sett med forespørselsmetoder som angir handlingen som skal utføres for en gitt ressurs. Forespørselsmetoden kan være **HENT**, **POSTER** eller en annen HTTP-metode. |
| Forespørselshoder                | Angi forespørselshoder. Et forespørselshode er en HTTP-overskrift som kan brukes i en HTTP-forespørsel, og som ikke er knyttet til innholdet i meldingen. |
| Aksepter                         | Angi egenskapen **Godta** for webforespørselen. |
| Godta koding                | Angi verdien **Godta koding**. HTTP-overskriften i Godta koding-forespørselen annonserer innholdskodingen som klienten kan forstå. Denne innholdskoding er vanligvis en komprimeringsalgoritme. |
| Innholdstype                   | Angi innholdstypen. HTTP-enhetshodet for innholdstypen indikerer medietypen for ressursen. |
| Kode for fullført svar       | Angi HTTP-statuskoden som angir at forespørselen var vellykket. |
| Formattilordning for forespørselshoder | Velg ER-formatet som brukes til å generere webforespørselshoder. |

### <a name="message-processing-actions"></a>Handlinger for meldingsbehandling

Du bruker meldingsbehandlingshandlinger til å opprette handlinger for prosessene og sette opp parametere. Du kan definere handlinger for meldingsbehandling på siden **Handlinger for meldingsbehandling** (**Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Handlinger for meldingsbehandling**).

Tabellen nedenfor beskriver feltene på siden **Handlinger for meldingsbehandling**.

#### <a name="general-fasttab"></a>Hurtigfanen Generelt

| Felt                       | beskrivelse |
|-----------------------------|-------------|
| Handlingstype                 | Velg handlingstypen. Hvis du vil ha informasjon om de tilgjengelige alternativene, se delen [Handlingstyper for meldingsbehandling](#message-processing-action-types). |
| Formattilordning              | Velg ER-formatet som skal kalles for handlingen. Dette feltet er bare tilgjengelig for handlingene av typen **Eksport av elektronisk rapportering**, **Import av elektronisk rapportering** og **Melding om eksport av elektronisk rapportering**. |
| Formattilordning for URL-bane | Velg ER-formatet som skal kalles for handlingen. Dette feltet er bare tilgjengelig for handlingene av typen **Webtjeneste**. Den brukes til å skrive banen til URL-adressen som skal legges til den grunnleggende Internett-adressen som er angitt for den valgte webserveren. |
| Type meldingselement           | Velg hvilken type poster som skal evalueres for handlingen. Dette feltet er tilgjengelig for handlinger av typen **Utføringsnivå for meldingselement**, **Eksport av elektronisk rapportering**, **Import av elektronisk rapportering** og **Webtjeneste** og noen andre typer. Hvis du lar dette feltet stå tomt, vurderes alle meldingselementtyper som er definert for meldingsbehandlingen. |
| Kjørbar klasse            | Velg innstillinger for kjørbare klasser som ble opprettet tidligere. Dette feltet er bare tilgjengelig for handlingene av typen **Utføringsnivå for meldingselement** og **Utføringsnivå for meldingselement**. |
| Handling for Fyll ut poster     | Velg en fyll ut poster-handling som ble konfigurert tidligere. Dette feltet er bare tilgjengelig for handlingene av typen **Fyll ut poster**. |
| Webtjeneste                 | Velg en webtjeneste som ble konfigurert tidligere. Dette feltet er bare tilgjengelig for handlingene av typen **Webtjeneste**. |
| Filnavn                   | Angi navnet på filen som blir resultatet av handlingen. Denne filen kan være svar fra webserveren eller rapporten som genereres. Dette feltet er bare tilgjengelig for handlinger av typene **Webtjeneste** og **Melding om eksport av elektronisk rapportering**. |
| Vis dialogboks                 | Sett dette alternativet til **Ja** hvis en dialogboks må vises til brukere før rapportgenerering. Dette feltet er bare tilgjengelig for handlinger av typen **Melding om eksport av elektronisk rapportering**. |

##### <a name="message-processing-action-types"></a>Handlingstyper for meldingsbehandling

Følgende alternativer er tilgjengelige i **Handlingstyper**-feltet:

- **Opprett melding** – Bruk denne handlingstypen hvis du vil la brukere manuelt opprette meldinger på siden **Elektronisk melding**. En innledende status kan ikke defineres for en handling av denne typen.
- **Fyll ut poster** – En handling av typen **Fyll ut poster** må være definert tidligere. Knytt denne handlingen til en fyll-ut-poster-handling for å aktivere handlingen, slik at den inkluderes i behandlingen. Det antas at denne handlingstypen brukes for den første handlingen i meldingsbehandling (når ingen elektronisk melding er opprettet på forhånd) eller for en handling som legger til meldingselementer i en melding som tidligere ble opprettet av en handling av typen **Opprett melding**. Derfor kan en resultatstatus bare settes opp for meldingselementer for handlinger av denne typen. En innledende status kan bare defineres for meldinger.
- **Utføringsnivå for melding** – Bruk denne handlingstypen til å definere en exe-klasse som skal evalueres på meldingsnivået.
- **Utføringsnivå for meldingselement** – Bruk denne handlingstypen til å definere en exe-klasse som skal evalueres på meldingselementnivået.
- **Eksport av elektronisk rapportering** – Bruk denne handlingstypen for handlinger som skal generere en rapport som er basert på en eksporterende ER-konfigurasjon på meldingselementnivå.
- **Melding om eksport av elektronisk rapportering** – Bruk denne handlingstypen for handlinger som skal generere en rapport som er basert på en eksporterende ER-konfigurasjon på meldingsnivå (for eksempel når en melding ikke inneholder noen meldingselementer).
- **Import av elektronisk rapportering** – Bruk denne handlingstypen for handlinger som skal generere en rapport som er basert på en importerende ER-konfigurasjon.
- **Behandling av bruker på meldingsnivå** – Bruk denne handslingstypen for handlinger som forutsetter manuell handling av brukeren på meldingsnivå. Brukeren kan for eksempel oppdatere statusen for meldinger.
- **Brukerbehandling** – Bruk denne handslingstypen for handlinger som forutsetter manuell handling av brukeren på meldingselementnivå. Brukeren kan for eksempel oppdatere statusen for meldingselementer.
- **Webtjeneste** – Bruk denne handlingstypen for handlinger som skal overføre en generert rapport til en webtjeneste. Denne handlingstypen brukes ikke for kommunikasjonsrapportering for italienske kjøps- og salgsfakturaer. For handlinger av typen **Webtjeneste** inkludererer siden **Handlinger for meldingsbehandling** hurtigkategorien **Diverse detaljer**, der du kan angi en bekreftelsestekst. Denne bekreftelsesteksten vises for brukerne før forespørsler til den valgte webtjenesten håndteres.
- **Forespørsel om verifisering** – Bruk denne handlingstypen til å forespørre bekreftelse fra en server.

#### <a name="initial-statuses-fasttab"></a>Hurtigfane for opprinnelige statuser

> [!NOTE]
> Hurtigfanen **Opprinnelige statuser** er ikke tilgjengelig for handlinger som har den innledende handlingstypen **Opprett melding**.

| Felt               | Beskrivelse |
|---------------------|-------------|
| Status for meldingselement | Velg meldingselementstatusen som den valgte meldingsbehandlingshandlingen skal evalueres for. |
| beskrivelse         | En beskrivelse av den valgte meldingselementstatusen. |

#### <a name="result-statuses-fasttab"></a>Hurtigfanen Resultatstatuser

| Felt               | beskrivelse |
|---------------------|-------------|
| Meldingsstatus      | Velg meldingsstatusene som den valgte meldingsbehandlingshandlingen skal evalueres for. Dette feltet er bare tilgjengelig for meldingsbehandlingshandlinger som evalueres på meldingsnivå. For eksempel er den tilgjengelig for handlinger av typen **Eksport av elektronisk rapportering** og **Import av elektronisk rapportering**, men den er ikke tilgjengelig for handlinger av typen **Brukerbehandling** og **Utføringsnivå for meldingselement**. |
| beskrivelse         | En beskrivelse av den valgte meldingsstatusen. |
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

### <a name="electronic-message-processing"></a>Behandling av elektronisk melding

Elektronisk meldingsbehandling er et grunnleggende konsept i funksjonen Elektroniske meldinger. Det samler handlinger som skal evalueres for den elektroniske meldingen. Handlingene kan kobles til via en innledende status og en resultatstatus. Eventuelt kan handlinger av typen **Brukerbehandling** startes uavhengig av hverandre. På siden **Behandling av elektronisk melding** (**Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Elektronisk meldingsbehandling**) kan du også velge flere felt som skal støttes for behandlingen, enten på meldingsnivå eller meldingselementnivå.

Hurtigfanen **Handling** lar deg legge til forhåndsdefinerte handlinger til behandlingen. Du kan angi om en handling må kjøres separat, eller om den kan startes av behandlingen. Hvis du vil angi at en handling i behandlingen kan initialiseres bare av en bruker, kan du angi feltet **Kjør separat** til **Ja** for den aktuelle handlingen. Hvis en handling skal startes av behandling av meldinger eller meldingselementer som har statusen som er definert som opprinnelig status for handlingen, settes feltet **Kjør separat** til **Nei**. Handlinger av typen **Brukerhandling** må alltid kjøres separat.

Noen ganger må flere handlinger samles i en sekvens, selv om den første handlingen defineres slik at den kjøres separat. For eksempel må en bruker starte rapportgenerering, men umiddelbart etter at rapporten er generert, må den sendes til en webtjeneste, og svaret fra webtjenesten må vises i systemet. I denne situasjonen kan du opprette en uatskillelig sekvens for handlinger som alltid må kjøres sammen. I **Handlingen**-hurtigkategorien velger du **Uatskillelig rekkefølge** over rutenettet og oppretter en sekvens. For alle handlinger som må kjøres sammen, velger du deretter rekkefølgen i feltet **Uatskillelig rekkefølge**. I dette tilfellet kan **Kjør separat**-feltet settes til **Ja** for den første handlingen i sekvensen, men **Nei** for alle andre handlinger.

Hurtigfanen **Tilleggsfelt for meldingselement** lar deg legge til forhåndsdefinerte tilleggsfelt som er knyttet til meldingselementer. Du må legge til flere felt for hver meldingstype som feltene er knyttet til.

Hurtigfanen **Tilleggsfelt for melding** lar deg legge til forhåndsdefinerte tilleggsfelt som er knyttet til meldinger.

Hurtigfanen **Sikkerhetsroller** lar deg definere sikkerhetsroller som er forhåndsdefinert i systemet for bestemt behandling. Brukere som har en bestemt rolle, ser bare behandling som er definert for denne rollen.

Med **Parti**-hurtigfanen kan du definere behandlingen til å arbeide i en satsvis prosess.

## <a name="work-with-the-electronic-messages-functionality"></a>Arbeide med funksjonen Elektroniske meldinger

Hvis du arbeider på meldingsnivå, er siden **Elektroniske meldinger** (**Mva** \> **Forespørsler og rapporter** \> **Elektroniske meldinger** \> **Elektronisk meldinger**) mer nyttig. Hvis du arbeider på datainnsamlingsnivå (meldingselement), er siden **Elektroniske meldingselementer** (**Mva** \> **Forespørsler og rapporter** \> **Elektroniske meldinger** \> **Elektronisk meldinger**) mer nyttig.

### <a name="electronic-messages"></a>Elektroniske meldinger

Siden **Elektroniske meldinger** presenterer behandlingen som er tilgjengelig for deg, basert på din rolle. Sikkerhetsroller er knyttet til behandling i oppsettet av denne behandlingen. For hver behandling som er tilgjengelig for deg, viser siden elektroniske meldinger og informasjon som er knyttet til disse.

**Meldinger**-hurtigfanen viser elektroniske meldinger for den valgte behandlingen. Avhengig av statusen for den valgte meldingen og forhåndsdefinert behandling, kan du kjøre noen handlinger ved å bruke knappene over rutenettet:

- **Ny** – Denne knappen er knyttet til handlinger for **Opprett melding**-typen.
- **Slett** – Denne knappen er tilgjengelig hvis det er merket av for **Tillat sletting** for den gjeldende statusen for den valgte meldingen.
- **Samle inn data** – Denne knappen er knyttet til handlinger av typen **Fyll ut poster**.
- **Generer rapport** – Denne knappen er knyttet til handlinger av typen **Melding om eksport av elektronisk rapportering**.
- **Send rapport** – Denne knappen er knyttet til handlinger av **Webtjeneste**-typen.
- **Importer svar** – Denne knappen er knyttet til handlinger av typen **Import av elektronisk rapportering**.
- **Oppdater status** – Denne knappen er knyttet til handlinger av typen **Behandling av bruker på meldingsnivå**.
- **Meldingselementer** – Åpne siden **Elektroniske meldingselementer**.

Hurtigfanen **Handlingslogg** viser informasjon om alle handlingene som er kjørt for den valgte meldingen. Hvis en handling har resultert i en feil, vil informasjon om feilen knyttes til den relaterte linjen i rutenettet. Hvis du vil se informasjon om feilen, velger du linjen i rutenettet, og velg deretter **Vedlegg**-knappen (bindersikonet) øverst i høyre hjørne på siden.

Hurtigfanen **Tilleggsfelt for melding** viser alle tilleggsfeltene som er definert for meldinger i behandlingsoppsettet. Den viser også verdiene i disse tilleggsfeltene.

Hurtigfanen **Meldingselementer** viser alle meldingselementer som er relatert til den valgte meldingen. Avhengig av statusen for det valgte meldingselementet kan du kjøre noen handlinger ved å bruke knappene over rutenettet:

- **Slett** – Denne knappen er tilgjengelig hvis det er merket av for **Tillat sletting** for den gjeldende statusen for det valgte meldingselementet.
- **Oppdater status** – Denne knappen er knyttet til handlinger av typen **Brukerbehandling**.
- **Opprinnelig dokument** – Åpne en side som viser det opprinnelige dokumentet for det valgte meldingselementet.

Alle rapporter som allerede er generert og mottatt for en melding, er knyttet til denne meldingen. Hvis du vil se vedleggene som er relatert til en melding, velger du meldingen, og deretter velger du **Vedlegg**-knappen (bindersikonet) øverst i høyre hjørne på siden.

![Vedlegg-knappen](media/attachment-icon.png)

Siden **Vedlegg** viser alle vedleggene som er knyttet til den valgte meldingen. Hvis du vil vise en fil, velger du den i listen til venstre, og deretter velger du **Åpne** i handlingsruten.

![Åpne-knappen](media/open-button.png)

Du kan også vise vedlegg som er knyttet til en bestemt aktivitet som tidligere ble kjørt for en melding. På siden **Elektroniske meldinger** velger du meldingen på hurtigfanen **Meldinger**, velger handlingen på hurtigfanen **Handlingslogg** og deretter **Vedlegg**-knappen i øvre høyre hjørne på siden.

Du kan også kjøre enten hele behandlingen eller bare en bestemt handling ved å velge **Kjør behandling** i handlingsruten.

### <a name="electronic-message-items"></a>Elektroniske meldingselementer

Siden **Elektroniske meldingselementer** viser alle meldingselementer og en logg over handlingene som er kjørt for hvert meldingselement. Den viser også tilleggsfeltene som er definert for meldingselementene, og verdiene for disse tilleggsfeltene.

Tabellen nedenfor beskriver feltene i fanen **Meldingselementer**.

<table>
<thead>
<tr>
<th>Felt</th>
<th>beskrivelse</th>
</tr>
</thead>
<tbody>
<tr>
<td>Behandling</td>
<td>Navnet på behandling som ble brukt til å opprette meldingselementet.</td>
</tr>
<tr>
<td>Meldingselement</td>
<td>ID-en til meldingselementet. Denne ID-en tildeles automatisk basert på <strong>Meldingselement</strong>-nummerserien som er definert på siden <strong>Parametere for økonomimodul</strong>.</td>
</tr>
<tr>
<td>Dato for meldingselement</td>
<td>Datoen da meldingselementet ble opprettet.</td>
</tr>
<tr>
<td>Type meldingselement</td>
<td>Typen meldingselement. Flere typer meldingselementer kan defineres for den samme behandlingen (for eksempel <strong>Innkommende fakturaer</strong> og <strong>Utgående fakturaer</strong>). Dette feltet kan fylles ut automatisk bare når en faktura blir lagt til meldingselementtabellen.</td>
</tr>
<tr>
<td>Status for meldingselement</td>
<td>Den faktiske statusen for meldingselementet. De tilgjengelige statusene varierer avhengig av meldingselementtypen. Her er noen eksempler:
<ul>
<li><strong>Utfylt</strong> – En post ble lagt til Meldingselementer-tabellen.</li>
<li><strong>Evaluert</strong> – Tilleggsattributter ble beregnet for meldingselementet.</li>
<li><strong>Rapportert</strong> – Meldingselementet ble lagt til en rapport.</li>
<li><strong>Utelukket</strong> – Denne statusen kan være nyttig hvis må du utelukke noen meldingselementer fra en rapport før den blir eksportert.</li>
</ul>
</td>
</tr>
<tr>
<td>Overføringsdato</td>
<td>For behandling som automatisk sender en genererte rapport utenfor systemet, datoen da meldingselementet ble sendt.</td>
</tr>
<tr>
<td>Dokumentnr.</td>
<td>Dette feltet fylles ut automatisk basert på oppsettet for handlingen for utfylling av poster. Dette feltet kan fylles ut automatisk bare når en faktura blir lagt til meldingselementtabellen.</td>
</tr>
<tr>
<td>Kontonummer</td>
<td>Kontonummeret til en kunde eller leverandør (eller en annen feltverdi, avhengig av feltet som er definert i handlingen for utfyllingen av poster). Dette feltet kan fylles ut automatisk bare når en faktura blir lagt til meldingselementtabellen.</td>
</tr>
<tr>
<td>Melding</td>
<td>Nummeret på meldingen. Dette nummeret tildeles automatisk basert på <strong>Melding</strong>-nummerserien som er definert på siden <strong>Parametere for økonomimodul</strong>.</td>
</tr>
<tr>
<td>Meldingsstatus</td>
<td>Den faktiske statusen for den elektroniske meldingen.</td>
</tr>
<tr>
<td>Neste handling</td>
<td>De neste handlingene som kan startes for den gjeldende statusen for meldingselementet.</td>
</tr>
</tbody>
</table>

**Tilleggsfelt**-kategorien viser flere felt for det valgte meldingselementet og deres verdier.

#### <a name="run-processing"></a>Kjør behandling

Velg **Kjør behandling** i handlingsruten for å utføre behandlingen for meldingselementer. For å kjøre en bestemt handling, sett **Velg handling** til **Ja** i dialogboksen **Kjør behandling**, og velg deretter en handling. Hvis du vil kjøre hele behandlingen, setter du alternativet **Velg handling** til **Nei**.

#### <a name="generate-report"></a>Generer rapport

Velg **Generer rapport** i handlingsruten for å generere en rapport. Denne knappen er knyttet til handlinger av typen **Eksport av elektronisk rapportering**.

#### <a name="update-status"></a>Oppdater status

Velg **Oppdater status** i handlingsruten for å oppdatere statusen til én eller flere meldingselementer. I **Oppdater status**-dialogboksen bruker du **Poster som skal inkluderes**-hurtigkategorien til å velge meldingselementer for oppdatering. Pass på at du definerer valgkriteriene riktig, fordi meldingselementstatuser oppdateres i henhold til disse kriteriene, den innledende statusen for den valgte handlingen, og **Ny status**-verdien du angir. Når en statusoppdatering er fullført, vil det være vanskelig å avgjøre hvilke elementer som ble oppdatert. Derfor blir det vanskelig å tilbakestille statusoppdateringen.

#### <a name="electronic-messages"></a>Elektroniske meldinger

Velg **Elektroniske meldinger** i handlingsruten for å se gjennom en elektronisk melding som er knyttet til det valgte meldingselementet.

Du kan også se gjennom alle filene som er relatert til et bestemt meldingselement. Velg **Melding**-feltet for meldingselementet, eller velg **Elektroniske meldinger** i handlingsruten. Deretter, på siden **Elektronisk melding**, velger du meldingen du vil se gjennom filer for, og deretter velger du **Vedlegg**-knappen (bindersikonet) øverst i høyre hjørne på siden.

![Vedlegg-knappen](media/attachment-icon.png)

Siden **Vedlegg** viser alle vedleggene som er knyttet til meldingen. Hvis du vil vise en fil, velger du den i listen til venstre, og deretter velger du **Åpne** i handlingsruten.

![Åpne-knappen](media/open-button.png)

#### <a name="original-document"></a>Opprinnelig dokument

Velg **Opprinnelig dokument** i handlingsruten for å åpne det opprinnelige dokumentet for det valgte meldingselementet.

## <a name="example-set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Eksempel: Definere og kjøre behandling for å kalle et enkelt ER-eksportformat for å generere en Excel-rapport

Når du har opprettet ER-formatet, tilordnet det til datakilder og fullført det, kan du kjøre det ved hjelp av arbeidsområdet **Elektronisk rapportering**. En rapport genereres, og du kan lagre den lokalt.

For å kontrollere følgende aspekter av rapporteringsprosessen, må du definere behandling av elektroniske meldinger:

- Logginformasjon om hvem som genererte rapporten.
- Logginformasjon om når rapporten ble generert.
- Lagre rapportene som er generert for tidligere perioder.

Denne delen inneholder et eksempel som viser hvordan du kan definere elektroniske meldinger for å generere en rapport som er basert på et ER-eksportformat for Excel. Hvis du vil følge dette eksemplet, må ER Excel-eksportformatet allerede være opprettet, tilordnet datakilder og fullført. I tillegg må en nummerserie allerede være definert for elektroniske meldinger.

Når du bygger behandling, er det nyttig hvis du først definerer behandlingshandlingene og -statuser som skal opprettes. Illustrasjonen nedenfor viser hvordan behandlingen ser ut i dette eksemplet.

![Oppsett for behandling](media/processing-scheme.png)

#### <a name="create-message-statuses"></a>Opprette meldingsstatuser

1. Gå til **Mva \> Oppsett \> Elektroniske meldinger \> Meldingsstatuser**.
2. Opprett følgende meldingsstatuser:

    - Nytt
    - Forberedt
    - Generert

    ![Meldingsstatuser](media/message-statuses.png)

3. På linjen for **Ny**-status merker du av for **Tillat sletting** for å la brukere slette meldinger som har denne statusen.

#### <a name="create-additional-fields"></a>Opprette tilleggsfelt

1. Gå til **Mva \> Oppsett \> Elektroniske meldinger \> Tilleggsfelt**.
2. Legge til et ekstra felt og tilhørende verdier. Her er et eksempel:

    ![Tilleggsfelt](media/additional-fields.png)

3. Sett alternativet **Brukerredigering** til **Ja**, slik at brukere kan redigere feltet.

#### <a name="create-message-processing-actions"></a>Opprette meldingsbehandlingshandlinger

I dette eksemplet oppretter du følgende handlinger:

- **Opprett melding**
- **Oppdater til Klargjort**
- **Generer rapport**
- **Oppdater til innledende status** (valgfritt)

1. Gå til **Mva \> Oppsett \> Elektroniske meldinger \> Handlinger for meldingsbehandling**.
2. Opprett en handling som heter **Opprett melding**. På hurtigfanen **Generelt** i feltet **Handlingstype** velger du **Opprett melding**.
3. Opprett en handling som heter **Oppdater til Klargjort**, og angi følgende felt:

    - På hurtigfanen **Generelt** i feltet **Handlingstype** velger du **Behandling av bruker på meldingsnivå**.
    - I hurtigfanen **Opprinnelige statuser**, i feltet **Meldingsstatus**, velger du **Ny**.
    - I hurtigfanen **Resultatstatuser**, i feltet **Meldingsstatus**, velger du **Klargjort**. I feltet **Svartype** angir du **Ble kjørt**.

4. Opprett en handling som heter **Generer rapport**, og angi følgende felt:

    - På hurtigfanen **Generelt** i feltet **Handlingstype** velger du **Eksport av elektronisk rapportering**. I feltet **Formattilordning** velger du ER-eksportformatet. Alternativene er **Excel**, **XML**, **JSON**, **Tekst** og **Annet**.
    - I hurtigfanen **Opprinnelige statuser**, i feltet **Meldingsstatus**, velger du **Klargjort**.
    - I hurtigfanen **Resultatstatuser**, i feltet **Meldingsstatus**, velger du **Generert**. I feltet **Svartype** angir du **Ble kjørt**.

    ![Generer rapporthandling](media/generate-report-action.png)

5. Valgfritt: Hvis du vil la brukerne generere en rapport flere ganger, kan du opprette en **Oppdater til innledende status**-handling og angi følgende felt:

    - På hurtigfanen **Generelt** i feltet **Handlingstype** velger du **Behandling av bruker på meldingsnivå**.
    - I hurtigfanen **Opprinnelige statuser**, i feltet **Meldingsstatus**, velger du **Generert**.
    - I **Resultatstatuser**-hurtigkategorien legger du til en egen linje for hver av de to meldingsstatusene (**Klargjort** og **Ny**). For begge linjene angir du feltet **Svartype** til **Ble kjørt**.

#### <a name="electronic-message-processing"></a>Behandling av elektronisk melding

I dette eksemplet må alle handlingene settes opp slik at de kjører separat. Det antas at brukeren vil initialisere alle handlinger.

1. Gå til **Mva \> Oppsett \> Elektroniske meldinger \> Behandling av elektronisk melding**.
2. Legg til en post for din behandling, og legg til alle tidligere definerte handlinger og et ekstra felt.
3. Valgfritt: På hurtigfanen **Sikkerhetsroller** definerer du sikkerhetsroller for behandlingen din for å begrense tilgangen til bestemt rapportering.
4. Gå til **Mva \> Forespørsler og rapporter \> Elektroniske meldinger \> Elektroniske meldinger**.
5. Velg **Ny** for å opprette en melding. Nå kan du legge til datoer og en beskrivelse. Du kan også oppdatere verdien i tilleggsfeltet etter behov.

    ![Opprette en elektronisk melding](media/create-electronic-message.png)

Rutenettet i hurtigfanen **Handlingslogg** fylles automatisk ut med en logg over alle handlinger som utføres på meldingen.

Du kan nå slette eller oppdatere meldingsstatusen. Hvis du vil oppdatere meldingsstatus, velger du **Oppdater status**. I feltet **Ny status** velger du **Klargjort**, og deretter velger du **OK**.

![Oppdatere meldingsstatusen](media/update-status.png)

Meldingsstatusen oppdateres til **Klargjort**, og du kan nå generere rapporten ved å velge **Generer rapport**. Rapporten genereres, og meldingsstatusen og -loggen oppdateres. Hvis du vil vise den genererte rapporten, velger du **Vedlegg**-knappen (bindersikonet) i øvre høyre hjørne på siden.
