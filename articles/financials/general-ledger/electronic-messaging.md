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
ms.openlocfilehash: 082ad886f40a52457900523f44158da3ed939458
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "357939"
---
# <a name="electronic-messaging"></a>Elektronisk meldingssystem

[!include [banner](../includes/banner.md)]

Dette emnet gir oversikt og oppsettinformasjon for elektroniske meldinger i Microsoft Dynamics 365 for Finance and Operations.

Myndigheter og lovgivende myndighetene i forskjellige land og områder over hele verden har nylig implementert rapporteringskrav for firmaer som er registrert i disse landene eller regionene. Formålet med kravene er å aktivere data som hentes fra disse firmaene, i elektronisk format direkte fra systemene der de ble beregnet, lagret og behandlet.

Funksjonen for elektroniske meldinger i Finance and Operations støtter forskjellige prosesser for elektronisk samhandling mellom Finance and Operations og systemene som myndigheter og juridiske myndigheter tilbyr for rapportering, sending og mottak av offisiell informasjon.

Funksjonen for elektroniske meldinger er integrert i modulen **Elektronisk rapportering**-modulen (ER). Derfor kan du definere ER-formater for elektroniske meldinger. For mer informasjon, se [Elektronisk rapportering (ER)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

Elektroniske meldinger er basert på følgende enheter:

- **Elektronisk melding** – en rapport eller deklarasjon som skal rapporteres og/eller overføres internt. Et eksempel er en rapport som er sendt til et skattekontor.
- **Elektroniske meldingselementer** – poster som skal inkluderes i meldingen som rapporteres.
- **Behandling av elektronisk melding** – en handlingskjede, enten koblet eller ikke koblet, som må kjøres for å samle de nødvendige dataene, generere rapporter, lagre data i Microsoft Azure Blob-lagring, sende rapporter utenfor systemet, få svar fra utenfor systemet og oppdatere databasen, basert på informasjonen som mottas.

Illustrasjonen nedenfor viser flyten av data for elektroniske meldinger.

![Dataflyt for elektroniske meldinger](media/electronic-messaging-data-flow.png)

Funksjonen for elektroniske meldinger støtter følgende scenarioer:

- Manuelt opprette meldinger og generere rapporter som er basert på tilknyttede eksporterende ER-formater av ulike typer: Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, tekst og Microsoft Word.
- Automatisk opprette og behandle meldinger som er basert på informasjonen som ble forespurt og hentet fra en myndighet via et tilknyttet importerende ER-format.
- Samle inn og behandle informasjon fra en datakilde (Finance and Operations-tabell) som meldingselementer.
- Lagre mer informasjon og evaluere ulike verdier ved å kalle spesielt definerte kjørbare klasser i forhold til meldinger eller meldingselementer.
- Aggregere informasjon som samles inn, i meldingselementer, dele informasjonen inn i meldinger og generere rapporter som er i tilknyttede eksporterende ER-formater.
- Sende rapporter som genereres, til en webtjeneste ved hjelp av sikkerhetsinformasjon som lagres i Azure Key Vault.
- Få et svar fra en webtjeneste, tolke svaret og oppdatere data i Finance and Operations etter behov.
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
- [Innstillinger for webtjeneste](#web-service-settings)
- [Handlinger for meldingsbehandling](#message-processing-actions)
- [Behandling av elektronisk melding](#electronic-message-processing)

De følgende delene gir mer informasjon om hver av disse elementene.

### <a name="number-sequences"></a>Nummerserier

Definere nummerserier for både meldinger og meldingselementer. Nummerserier brukes til å nummerere meldinger og meldingselementer automatisk, og tallene som er tilordnet, brukes som unike IDer for meldingene og meldingselementene i systemet. Du kan definere nummerserier for elektroniske meldinger på siden **Økonomiparametere** (**Økonomimodul** \> **Finansoppsett** \> **Parametere for økonomimodul**).

### <a name="message-item-types-and-statuses"></a>Meldingselementtyper og -statuser

Meldingselementtyper identifiserer typer poster som skal brukes i elektroniske meldinger. Du kan definere meldingselementtyper på siden **Typer meldingselement** (**Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Typer meldingselement**).

Meldingselementstatuser identifiserer statusene som gjelder for meldingselementer i behandlingen som du oppretter. Du kan definere meldingselementtyper på siden **Statuser for meldingselement** (**Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Statuser for meldingselement**).

### <a name="message-statuses"></a>Meldingsstatuser

Definer meldingsstatusene som skal være tilgjengelige i meldingsbehandlingen. Du kan definere meldingsstatuser på siden **Meldingsstatuser** (**Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Meldingsstatuser**).

### <a name="additional-fields"></a>Tilleggsfelt

Funksjonen Elektroniske meldinger lar deg fylle inn poster fra en transaksjonell tabell. Du kan forberede postene for rapportering og deretter rapportere dem. Noen ganger er det ikke nok informasjon i transaksjonstabellen til å rapportere en post i samsvar med rapporteringskravene. Du kan fylle ut alle opplysningene som må rapporteres for en post, ved å definere flere felt. Flere felt kan være knyttet til både meldinger og meldingselementer. Du kan definere flere felt på siden **Tilleggsfelt** (**Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Tilleggsfelt**).

Tabellen nedenfor beskriver feltene på siden **Tilleggsfelt**.

| Felt                | beskrivelse |
|----------------------|-------------|
| Feltnavn           | Angi navnet på en tilleggsattributt for meldingselementer som er knyttet til prosessen. Dette navnet vises i brukergrensesnittet mens du arbeider med prosessen. Det kan også brukes i ER-konfigurasjoner som er knyttet til prosessen. |
| beskrivelse          | Angi en beskrivelse av tilleggsattributtet for meldingselementer som er knyttet til prosessen. |
| Feltverdi          | Angi feltverdien som skal brukes i forbindelse med meldingselementet under rapportering. |
| Feltbeskrivelse    | Angi en beskrivelse av feltverdien som skal brukes i forbindelse med meldingselementet under rapportering. |
| Kontotype         | Noen tilleggsfeltverdier kan være begrenset til bestemte kontotyper. Velg et av følgende verdier: **Alle**, **Kunde** eller **Leverandør**. |
| Kontokode         | Hvis du har valgt **Kunde** eller **Leverandør** i feltet **Kontotype**, kan du ytterligere begrense bruken av feltverdier til en bestemt gruppe eller tabell. |
| Konto/gruppenummer | Hvis du har valgt **Kunde** eller **Leverandør** i **Kontotype**-feltet, og hvis du har angitt en gruppe eller tabell i feltet **Kontokode**, kan du angi en bestemt gruppe eller kontrollør i dette feltet. |
| Effektiv            | Angi datoen når verdien skal begynne å vurderes. |
| Utløp           | Angi datoen når verdien skal slutte å vurderes. |

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

### <a name="populate-records-actions"></a>Handlinger for Fyll ut poster

Du bruker handlinger for utfylling av poster til å definere handlinger som legger til poster i tabellen Meldingselementer, slik at de kan legges til i en elektronisk melding. Hvis for eksempel den elektroniske meldingen må rapportere kundefakturaer, må du sette opp en **Fyll ut poster**-handling som er koblet på **Kundefakturajournal**-tabellen (i **Datakilde**-feltet). Du kan angi handlinger for utfylling av poster på siden **Handling for Fyll ut poster** (**Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Handlinger for Fyll ut poster**). Opprett en ny post for alle handlinger som skal legge til poster i tabellen, og angi følgende felt:

| Felt       | beskrivelse                                                               |
|-------------|---------------------------------------------------------------------------|
| Navn        | Angi et navn for handlingen som fyller ut poster i prosessen.       |
| beskrivelse | Angi en beskrivelse av handlingen som fyller ut poster i prosessen. |

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
| Brukerspørring             | Hvis det er merket av i denne avmerkingsboksen, du kan definere en spørring ved å velge **Rediger spørring** over rutenettet. Hvis ikke fylles alle postene fra datakilden ut. |

### <a name="web-service-settings"></a>Innstillinger for webtjeneste

Du bruker innstillinger for webtjeneste til å definere direkte dataoverføring til en webtjeneste. Du kan definere innstillinger for webtjenester på siden **Innstillinger for webtjeneste** (**Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Innstillinger for webtjeneste**) .

Tabellen nedenfor beskriver feltene på siden **Innstillinger for webtjeneste**.

| Felt                   | beskrivelse |
|-------------------------|-------------|
| Webtjeneste             | Skriv inn et navn på webtjenesten. |
| beskrivelse             | Angi en beskrivelse av webtjenesten. |
| Internett-adresse        | Angi internettadressen til webtjenesten. |
| Sertifikat             | Velg et Key Vault-sertifikat som tidligere er definert. |
| Svartypen – XML | Sett dette alternativet til **Ja** hvis svartypen er XML. |
| Forespørselsmetode          | Angi metoden for forespørselen. HTTP definerer et sett med forespørselsmetoder som angir handlingen som skal utføres for en gitt ressurs. Metoden kan være **HENT**, **POSTER** eller en annen HTTP-metode. |
| Forespørselshoder         | Angi forespørselshoder. Et forespørselshode er en HTTP-overskrift som kan brukes i en HTTP-forespørsel, og som ikke er knyttet til innholdet i meldingen. |
| Godta koding         | Angi Godta koding. HTTP-overskriften i Godta koding-forespørselen annonserer innholdskodingen som klienten kan forstå. Denne innholdskoding er vanligvis en komprimeringsalgoritme. |
| Innholdstype            | Angi innholdstypen. Enhetshodet for innholdstypen indikerer medietypen for ressursen. |

### <a name="message-processing-actions"></a>Handlinger for meldingsbehandling

Du bruker meldingsbehandlingshandlinger til å opprette handlinger for prosessene og sette opp parametere. Du kan definere handlinger for meldingsbehandling på siden **Handlinger for meldingsbehandling** (**Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Handlinger for meldingsbehandling**).

Tabellen nedenfor beskriver feltene på siden **Handlinger for meldingsbehandling**.

#### <a name="general-fasttab"></a>Hurtigfanen Generelt

| Felt                   | beskrivelse |
|-------------------------|-------------|
| Handlingstype             | Velg handlingstypen. Hvis du vil ha informasjon om de tilgjengelige alternativene, se delen [Handlingstyper for meldingsbehandling](#message-processing-action-types). |
| Formattilordning          | Velg ER-formatet som skal kalles for handlingen. Dette feltet er bare tilgjengelig for handlingene av typen **Eksport av elektronisk rapportering**, **Import av elektronisk rapportering** og **Melding om eksport av elektronisk rapportering**. |
| Type meldingselement       | Velg hvilken type poster som skal evalueres for handlingen. Dette feltet er tilgjengelig for handlinger av typen **Utføringsnivå for meldingselement**, **Eksport av elektronisk rapportering** og **Import av elektronisk rapportering** noen andre typer. Hvis du lar dette feltet stå tomt, vurderes alle meldingselementtyper som er definert for meldingsbehandlingen. |
| Kjørbar klasse        | Velg innstillinger for kjørbare klasser som ble opprettet tidligere. Dette feltet er bare tilgjengelig for handlingene av typen **Utføringsnivå for meldingselement** og **Utføringsnivå for meldingselement**. |
| Handling for Fyll ut poster | Velg en fyll ut poster-handling som ble konfigurert tidligere. Dette feltet er bare tilgjengelig for handlingene av typen **Fyll ut poster**. |

##### <a name="message-processing-action-types"></a>Handlingstyper for meldingsbehandling

Følgende alternativer er tilgjengelige i **Handlingstyper**-feltet:

- **Fyll ut poster** – En **Fyll ut poster**-handlingen må være definert tidligere. Knytt den til en handling av typen **Fyll ut poster** for å aktivere den slik at den inkluderes i behandlingen. Det antas at denne handlingstypen brukes for den første handlingen i meldingsbehandlingen. Derfor kan bare en resultatstatus defineres for en handling av denne typen. En innledende status kan ikke defineres.
- **Opprett melding** – Bruk denne typen hvis du vil la brukere manuelt opprette meldinger på siden **Elektronisk melding**. En innledende status kan ikke defineres for en handling av denne typen.
- **Utføringsnivå for melding** – Bruk denne typen til å definere en exe-klasse som skal evalueres på meldingsnivået.
- **Utføringsnivå for meldingselement** – Bruk denne typen til å definere en exe-klasse som skal evalueres på meldingselementnivået.
- **Eksport av elektronisk rapportering** – Bruk denne typen for handlinger som skal generere en rapport som er basert på en eksporterende ER-konfigurasjon på meldingselementnivå.
- **Melding om eksport av elektronisk rapportering** – Bruk denne typen for handlinger som skal generere en rapport som er basert på en eksporterende ER-konfigurasjon på meldingsnivå (for eksempel når en melding ikke inneholder noen meldingselementer).
- **Import av elektronisk rapportering** – Bruk denne typen for handlinger som skal generere en rapport som er basert på en importerende ER-konfigurasjon.
- **Behandling av bruker på meldingsnivå** – Bruk denne typen for handlinger som forutsetter noen manuelle handlinger av brukeren. Brukeren kan for eksempel oppdatere statusen for meldinger.
- **Brukerbehandling** – Bruk denne typen for handlinger som forutsetter noen manuelle handlinger av brukeren. Brukeren kan for eksempel oppdatere statusen for meldingselementer.
- **Webtjeneste** – Bruk denne typen for handlinger som skal overføre en genererte rapporten til en webtjeneste. Denne handlingstypen brukes ikke for kommunikasjonsrapportering for italienske kjøps- og salgsfakturaer.
- **Forespørsel om verifisering** – Bruk denne typen til å forespørre bekreftelse fra en server.

#### <a name="initial-statuses-fasttab"></a>Hurtigfane for opprinnelige statuser

> [!NOTE]
> Hurtigfanen **Opprinnelige statuser** er ikke tilgjengelig for handlinger som har den innledende typen **Fyll ut poster** eller **Opprett melding**.

| Felt               | beskrivelse                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| Status for meldingselement | Velg meldingselementstatusen som den valgte meldingsbehandlingshandlingen skal evalueres for. |
| beskrivelse         | En beskrivelse av den valgte meldingselementstatusen.                                                  |

#### <a name="result-statuses-fasttab"></a>Hurtigfanen Resultatstatuser

| Felt               | beskrivelse |
|---------------------|-------------|
| Meldingsstatus      | Velg meldingsstatusene som den valgte meldingsbehandlingshandlingen skal evalueres for. Dette feltet er bare tilgjengelig for meldingsbehandlingshandlinger som evalueres på meldingsnivå. Det er for eksempel tilgjengelig for typene **Eksport av elektronisk rapportering** og **Import av elektronisk rapportering**. Det er ikke tilgjengelig for handlingene av typen **Brukerbehandling** og **Utføringsnivå for meldingselement**. |
| beskrivelse         | En beskrivelse av den valgte meldingsstatusen. |
| Svartype       | Svartypen for den valgte meldingsstatusen. |
| Status for meldingselement | Velg de resulterende statusene som skal være tilgjengelige etter den valgte meldingsbehandlingshandlingen er evaluert. Dette feltet er bare tilgjengelig for meldingsbehandlingshandlinger som evalueres på meldingselementnivå. For eksempel er det tilgjengelig for handlinger av typene **Brukerbehandling** og **Utføringsnivå for meldingselement**. For meldingsbehandlingshandlinger som evalueres på meldingsnivået, viser dette feltet meldingselementstatusen som ble angitt for den valgte meldingsstatus. |

### <a name="electronic-message-processing"></a>Behandling av elektronisk melding

Elektronisk meldingsbehandling er et grunnleggende konsept i funksjonen Elektroniske meldinger. Det samler handlinger som skal evalueres for den elektroniske meldingen. Handlingene kan kobles til via en innledende status og en resultatstatus. Eventuelt kan handlinger av typen **Brukerbehandling** startes uavhengig av hverandre. På siden **Behandling av elektronisk melding** (**Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Elektronisk meldingsbehandling**) kan du også velge flere felt som skal støttes for behandlingen.

Hurtigfanen **Handling** lar deg legge til forhåndsdefinerte handlinger til behandlingen. Du kan angi om en handling må kjøres separat, eller om den kan startes av behandlingen. (Brukerhandlinger må kjøres hver for seg.)

Hurtigfanen **Tilleggsfelt for meldingselement** lar deg legge til forhåndsdefinerte tilleggsfelt som er knyttet til meldingselementer. Du må legge til flere felt for hver meldingstype som feltene er knyttet til.

Hurtigfanen **Tilleggsfelt for melding** lar deg legge til forhåndsdefinerte tilleggsfelt som er knyttet til meldinger.

Hurtigfanen **Sikkerhetsroller** lar deg definere sikkerhetsroller som er forhåndsdefinert i systemet for bestemt behandling. Brukere som har en bestemt rolle, ser bare behandling som er definert for denne rollen.

Med **Parti**-hurtigfanen kan du definere behandlingen til å arbeide i en satsvis prosess.

## <a name="work-with-electronic-messages-functionality"></a>Arbeide med funksjonen Elektroniske meldinger

Hvis du arbeider på meldingsnivå, er siden **Elektroniske meldinger** (**Mva** \> **Forespørsler og rapporter** \> **Elektroniske meldinger** \> **Elektronisk meldinger**) mer nyttig. Hvis du arbeider på datainnsamlingsnivå (meldingselement), er siden **Elektroniske meldingselementer** (**Mva** \> **Forespørsler og rapporter** \> **Elektroniske meldinger** \> **Elektronisk meldinger**) mer nyttig.

### <a name="electronic-messages"></a>Elektroniske meldinger

Siden **Elektroniske meldinger** presenterer behandlingen som er tilgjengelig for deg, basert på din rolle. Sikkerhetsroller er knyttet til behandling i oppsettet av denne behandlingen. For hver behandling som er tilgjengelig for deg, viser siden elektroniske meldinger og informasjon som er knyttet til disse.

**Meldinger**-hurtigfanen viser elektroniske meldinger for den valgte behandlingen. Avhengig av statusen for den valgte meldingen og forhåndsdefinert behandling, kan du kjøre noen handlinger ved å velge knappene over rutenettet:

- **Ny** – Denne knappen er knyttet til handlinger for **Opprett melding**-typen.
- **Slett** – Denne knappen er tilgjengelig hvis det er merket av for **Tillat sletting** for den gjeldende statusen for den valgte meldingen.
- **Generer rapport** – Denne knappen er knyttet til handlinger av typen **Melding om eksport av elektronisk rapportering**.
- **Send rapport** – Denne knappen er knyttet til handlinger av **Webtjeneste**-typen.
- **Oppdater status** – Denne knappen er knyttet til handlinger av typen **Behandling av bruker på meldingsnivå**.
- **Meldingselementer** – Åpne siden **Elektroniske meldingselementer**.

Hurtigfanen **Handlingslogg** viser informasjon om alle handlingene som er kjørt for den valgte meldingen.

Hurtigfanen **Tilleggsfelt for melding** viser alle tilleggsfeltene som er definert for meldinger i behandlingsoppsettet. Den viser også verdiene i disse tilleggsfeltene.

Hurtigfanen **Meldingselementer** viser alle meldingselementer som er relatert til den valgte meldingen.

Du kan se gjennom alle vedlegg for den valgte meldingen. Disse vedleggene er rapporter som allerede er generert og mottatt. Velg meldingen som vedlegg skal gjennomgås for, og velg deretter **Vedlegg**-knappen i handlingsruten.

![Vedlegg-knappen](media/attachment-icon.png)

Siden **Vedlegg** viser alle vedleggene som er knyttet til meldingen. Hvis du vil vise en fil, velger du den i listen til venstre, og deretter velger du **Åpne** i handlingsruten.

![Åpne-knappen](media/open-button.png)

Hvis du vil gå gjennom et vedlegg som er knyttet til en bestemt handling som tidligere ble kjørt for en melding, velger du meldingen på siden **Elektroniske meldinger**, og deretter velger du handlingen på hurtigfanen **Handlingslogg**. Deretter velger du **Vedlegg**-knappen i handlingsruten.

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
<td>Kontonummeret til en kunde eller leverandør (eller en annen feltverdi, avhengig av feltet som er definert i handlingen <strong>Fyll ut poster</strong>). Dette feltet kan fylles ut automatisk bare når en faktura blir lagt til meldingselementtabellen.</td>
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

Velg **Oppdater status** i handlingsruten for å oppdatere statusen til én eller flere meldingselementer. I **Oppdater status**-dialogboksen bruker du **Poster som skal inkluderes**-hurtigkategorien til å velge meldingselementer for oppdatering. Pass på at du definerer valgkriteriene riktig, fordi meldingselementstatuser oppdateres i henhold til disse kriteriene, den innledende statusen for den valgte handlingen, og **Ny status**-verdien du angir. Når en statusoppdatering er fullført, vil det være vanskelig å avgjøre hvilke elementer som nettopp ble oppdatert. Derfor blir det vanskelig å tilbakestille statusoppdateringer.

#### <a name="electronic-messages"></a>Elektroniske meldinger

Velg **Elektronisk melding** i handlingsruten for å se gjennom en elektronisk melding som er knyttet til det valgte meldingselementet.

Du kan også se gjennom alle filene som samsvarer med meldingselementet. Velg **Melding**-feltet i meldingselementet, eller velg **Elektronisk melding** i handlingsruten. På siden **Elektronisk melding** velger du meldingen du vil vise en rapport for, og deretter velger du **Vedlegg**-knappen i handlingsruten.

![Vedlegg-knappen](media/attachment-icon.png)

Siden **Vedlegg** viser alle vedleggene som er knyttet til meldingen. Hvis du vil vise en fil, velger du den i listen til venstre, og deretter velger du **Åpne** i handlingsruten.

![Åpne-knappen](media/open-button.png)

#### <a name="original-document"></a>Opprinnelig dokument

Velg **Opprinnelig dokument** i handlingsruten for å åpne det opprinnelige dokumentet for det valgte meldingselementet.

## <a name="example"></a>Eksempel

Når du har opprettet ER-formatet, tilordnet det til datakilder og fullført det, kan du kjøre det ved hjelp av arbeidsområdet **Elektronisk rapportering**. En rapport genereres som du kan lagre lokalt.

For å kontrollere følgende aspekter av rapporteringsprosessen, må du definere behandling av elektroniske meldinger:

- Logginformasjon om hvem som genererte rapporten.
- Logg da rapporten ble generert.
- Lagre rapportene som er generert for tidligere perioder.

Denne delen inneholder et eksempel som viser hvordan du kan sette opp funksjonen Elektroniske meldinger for å bygge en rapporteringsprosess.

### <a name="set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Definere og kjøre behandling for å kalle et enkelt ER-eksportformat for å generere en Excel-rapport

Denne delen inneholder et eksempel som viser hvordan du kan definere elektroniske meldinger for å generere en rapport som er basert på et ER-eksportformat for Excel. Når du skal følge dette eksemplet, må ER Excel-eksportformatet allerede være opprettet, tilordnet datakilder og fullført. En nummerserie må allerede være definert for elektroniske meldinger.

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
    - I hurtigfanen **Resultatstatuser**, i feltet **Meldingsstatus**, velger du **Klargjort** eller (og) **Ny**. I feltet **Svartype** angir du **Ble kjørt**.

#### <a name="electronic-message-processing"></a>Behandling av elektronisk melding

I dette eksemplet må alle handlingene settes opp slik at de kjører separat. Det antas at alle handlinger vil bli initialisert av brukeren.

1. Gå til **Mva \> Oppsett \> Elektroniske meldinger \> Behandling av elektronisk melding**.
2. Legg til en post for din behandling, og legg til alle tidligere definerte handlinger og et ekstra felt.
3. Valgfritt: På hurtigfanen **Sikkerhetsroller** definerer du sikkerhetsroller for behandlingen din for å begrense tilgangen til bestemt rapportering.
4. Gå til **Mva \> Forespørsler og rapporter \> Elektroniske meldinger \> Elektroniske meldinger**.
5. Velg **Ny** for å opprette en melding. Nå kan du legge til datoer og en beskrivelse. Du kan også oppdatere verdien i tilleggsfeltet etter behov.

    ![Opprette en elektronisk melding](media/create-electronic-message.png)

Rutenettet i hurtigfanen **Handlingslogg** fylles automatisk ut med en logg over alle handlinger som utføres på meldingen.

Du kan nå slette eller oppdatere meldingsstatusen. Hvis du vil oppdatere meldingsstatusen, velger du **Oppdater status** og deretter, i feltet **Ny status**, velger du **Klargjort**. Velg deretter **OK**.

![Oppdatere meldingsstatusen](media/update-status.png)

Meldingsstatusen oppdateres til **Klargjort**, og du kan nå generere rapporten ved å velge **Generer rapport**. Rapporten genereres, og meldingsstatusen og -loggen oppdateres. Hvis du vil vise den genererte rapporten, velger du **Vedlegg**-knappen i handlingsruten.
