---
title: Ønske leverandører velkommen
description: Dette emnet beskriver prosessen for å ønske nye leverandører velkommen. Det forklarer handlingene som kreves av forskjellige roller under denne prosessen.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests,SysUserRequestListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 5fda191a41300eea7f3036af54852857d8ff653d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "322151"
---
# <a name="onboard-vendors"></a>Ønske leverandører velkommen
[!include [banner](../includes/banner.md)]

---

Nye leverandører kan ønskes velkommen og registreres som leverandører i Microsoft Dynamics 365 for Finance and Operations basert på informasjonen som samles inn fra en person som representerer leverandøren.

Prosessen består av følgende trinn, der forskjellige roller utfører handlinger i systemet.

1. **Behandling av OData** – Enhetsimport – Den innledende forespørselen er registreringsforespørselen fra en potensiell leverandør. Denne forespørselen kommer vanligvis fra en kilde, for eksempel et nettsted som drives av en kunde, som tillater anonym tilgang. Leverandører kan registrere seg ved å angi grunnleggende opplysninger, for eksempel leverandørnavn, begrunnelse, organisasjonsnummer og kontaktpersonens navn og e-postadresse. Forespørslene importeres via grensesnittet for databehandling.
2. **Listeside for registreringsforespørselen fra potensielle leverandører** – Basert på informasjonen som er angitt i registreringsforespørselen fra den potensielle leverandøren, bestemmer en innkjøpsansvarlig om leverandøren skal ønskes velkommen. Innkjøpsansvarlig ser den innkommende forespørselen på listesiden **Registreringsforespørsler fra potensielle leverandører** i Finance and Operations.
3. **Arbeidsflyt for brukerklargjøring** – Når en innkjøpsansvarlig har bekreftet informasjonen i den innkommende forespørselen og har bestemt seg for å fortsette med velkomstprosessen, klargjør arbeidsflyten for brukerforespørsler den nye brukeren og sender en e-postinvitasjonen om å godta kontaktpersonen som en godkjent bruker av Microsoft Dynamics 365.
4. **Veiviser for registrering av leverandører** – Leverandørens kontaktpersoner logger seg på Finance and Operations ved hjelp av den nye brukerkontoen. Han eller hun fullfører veiviseren for registrering av leverandører for å oppgi informasjon, som adresser, forretningsinformasjon, innkjøpskategorier og svar på et spørreskjema.
5. **Arbeidsflyt for godkjenning** – En leverandørforespørsel som inneholder informasjon om registreringen, opprettes. Denne leverandørforespørselen blir sendt til en arbeidsflyt, og rutes til gjennomgang og godkjenning.
6. **Oppretting av en original for leverandør og endring av brukerrolle** – Når leverandørforespørselen er godkjent, opprettes en leverandørpost. Brukerkontoen til leverandørens kontaktperson får enten tillatelse til å samarbeide med leverandøren, eller den deaktiveres.

Tabellen nedenfor viser trinnene og rollene som er involvert i prosessen.

| Rolle og "prosess"       | Behandling av OData – Enhetsimport | Listesiden Forespørsel om registrering av potensiell leverandør | Arbeidsflyt for brukerklargjøring | Veiviser for registrering av leverandører | Arbeidsflyt for godkjenning | Oppretting av en original for leverandør og endring av brukerrolle |
|--------------------------|---|---|---|---|---|---|
| System                   | Forespørselen for en ny leverandør er importert. | | | | | Når leverandørforespørselen er godtatt, opprettes leverandørposten. |
| Innkjøpsansvarlig | | Start velkomstprosessen. | | | Se gjennom og godta eller avvis leverandørforespørselen. | |
| Administrator            | | | Opprett en bruker i Finance and Operations og Microsoft Azure. | | | |
| Leverandørens kontaktperson    | | | Send e-post til kontaktpersonen. | Registrer leverandørinformasjon. | | |

For en rask demonstrasjon av leverandørintroduksjonsprosessen, kan du se denne korte YouTube-videoen: [Introdusere en ny leverandør i Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=0KUc3AGaTKk}.

## <a name="importing-the-prospective-vendor-registration-request"></a>Importere forespørselen om registrering av potensiell leverandør

Forespørselen om registrering av potensiell leverandør er en enhet i Finance and Operations. Du kan sette opp systemet til å importere data via denne entiteten. 

Tabellen nedenfor viser informasjonen som denne enheten inneholder, og som kan importeres.

| Felt                        | beskrivelse |
|------------------------------|-------------|
| Navn på leverandør                  | Navnet på leverandøren. |
| Bestillingsårsak       | Årsak(er) til leverandørforespørselen. |
| Organisasjonsnummer          | Et offisielt kjent registreringsnummer. |
| Bransje             | Bransjen leverandøren er i. |
| Kontaktens fornavn.  | Fornavnet til personen som inviteres til å registrere leverandørinformasjonen. |
| Kontaktens mellomnavn | Mellomnavnet til personen som inviteres til å registrere leverandørinformasjonen. |
| Kontaktens etternavn   | Etternavnet til personen som inviteres til å registrere leverandørinformasjonen. |
| Kontaktens e-post       | E-postadressen som skal brukes til å opprette en ny bruker i Finance and Operations, og som skal registreres i leierens Azure Active Directory (Azure AD)-konto (Azure Active Directory). |
| Sendt dato               | Datoen da forespørselen ble opprettet i et eksternt system. |
| Juridisk enhet                 | Den juridiske enheten der leverandøren ber om å bli en leverandør. Denne verdien må være en kode for juridisk enhet som er registrert i Finance and Operations. Hvis ingen verdi er mottatt gjennom importprosessen, en verdi fra innkjøp og leverandører parametere brukes. |
| Leverandørtype                  | Leverandøren kan være enten en organisasjon eller en person. Leverandørtypen bestemmer hvordan leverandøren opprettes til slutt. |

Når den registreringsforespørselen fra den potensielle leverandøren er importert, vises den på listesiden **Forespørsel om registrering av potensiell leverandør**. Fra denne listesiden kan en innkjøpsansvarlig invitere brukeren. En brukerforespørsel for klargjøring av brukeren sendes til en arbeidsflyt.

## <a name="submitting-a-prospective-vendor-user-request"></a>Sende inn en brukerforespørsel for potensiell leverandør

Formålet med en brukerforespørsel for potensiell leverandør er å klargjøre personen som sendte den første forespørselen, slik at han eller hun kan logge på Finance and Operations ved hjelp av e-kontoen som er angitt i registreringsforespørselen for potensiell leverandør.

Brukerforespørselen for potensiell leverandør behandles av arbeidsflyten for brukerforespørsel. Denne arbeidsflyten kommuniseres via Azure AD B2B-samarbeid. Den oppretter en bruker i Finance and Operations som har de aktuelle sikkerhetsinnstillingene.

Nye brukere som er definert, har følgende sikkerhetsroller:

- Systemekstern bruker
- Leverandørprospekt (eksternt)

Den nye brukeren mottar en e-postmelding som genereres ved hjelp av arbeidsflyt. Denne e-postmeldingen inviterer brukeren logge seg på systemet.

Hvis du vil ha informasjon om konfigurasjonen av e-postmeldingen og arbeidsflyten Generelt, se beskrivelsen av en arbeidsflyt i [Definere og vedlikeholde leverandørsamarbeid](set-up-maintain-vendor-collaboration.md).

## <a name="vendor-registration"></a>Leverandørregistrering

En potensiell leverandørbruker som logger på Finance and Operations, ser den første siden i registreringsveiviseren for en leverandør, der han eller hun kan angi leverandørinformasjon.

Veiviseren gjenspeiler konfigurasjonen av leverandørforespørselen. Landet eller regionen der leverandøren har forretningsforbindelser, bestemmer hvilken informasjon som kreves i veiviseren, og hvilken informasjon som er obligatorisk.

Hvis du vil ha mer informasjon om hvordan du konfigurerer leverandørforespørselen, kan du se [Konfigurere og vedlikehold leverandørsamarbeid](set-up-maintain-vendor-collaboration.md). Tabellen nedenfor gir en oversikt over sidene i veiviseren og formålet med hver side.

| Side                       | beskrivelse |
|----------------------------|-------------|
| Land/område             | Landet eller regionen bestemmer konfigurasjonen av leverandørforespørselen som skal brukes på de gjenværende veivisersidene. Den bestemmer også verdiene i oppslager **Mva-tilstand**. |
| Vilkår og betingelser       | Denne siden kan være tilgjengelige, avhengig av konfigurasjonen av leverandørforespørselen. Hvis den er tilgjengelig, må brukeren godta betingelsene for å fortsette. |
| Leverandøropplysninger         | Denne siden inneholder leverandørnavnet, som angis automatisk fra den opprinnelige registreringsforespørselen for potensiell leverandør. Den inneholder også organisasjonsnummeret, leverandørens telefonnummer, faksnummer, og e-postadresse og leverandørens adresser til forskjellige formål. |
| Informasjon om kontaktperson | Denne siden inneholder navnet på kontaktpersonen, som angis automatisk fra den opprinnelige registreringsforespørselen for potensiell leverandør. Den inneholder også kontaktpersonens telefonnummer og e-postadresse og kontaktpersonens adresser til forskjellige formål. |
| Firmainformasjon       | Denne siden inneholder mva-numre (for ulike land eller regioner) og antall ansatte. Den angir også om virksomheten er minoritetseid. |
| Innkjøpskategorier     | Denne siden inneholder innkjøpskategoriene som leverandøren ber om godkjenning for. Brukeren kan velge kategorier i innkjøpskategorihierarkiet. Du kan konfigurere hvor mange nivåer som vises i hierarkiet, under **Parametere for innkjøp og leverandører** &gt; **Leverandørsamarbeid** under **Innkjøp og leverandører** &gt; **Oppsett**. |
| Spørreskjemaer             | Veiviseren kan inneholde et sett med spørreskjemaer for leverandøren. Spørreskjemaer som vises i veiviseren er konfigurert på leverandørforespørselen eller per innkjøpskategorien. Hvis spørreskjemaer konfigureres per innkjøpskategorien, bestemmer innkjøpskategoriene som leverandøren ber om godkjenning for spørreskjemaene som vises i veiviseren. På siden **Innkjøpskategorier** kan du legge til et spørreskjema under relevant kategori og sette aktivitetstypen til **Jobbintroduksjon for leverandør**. |

Når den potensielle leverandørbrukeren fullfører registreringsveiviseren for leverandører, opprettes en leverandørforespørsel.

## <a name="manually-or-automatically-submit-a-vendor-request"></a>Sende en leverandørforespørsel manuelt eller automatisk

En leverandørforespørsel kan opprettes som en kladd og sendes til en arbeidsflyt manuelt. Leverandørforespørselen kan også sendes automatisk til en arbeidsflyt når registreringsveiviseren for leverandører er fullført. En forespørsel kan sendes manuelt hvis for eksempel en innkjøpsansvarlig ønsker å vurdere om forespørselen skal rutes gjennom en godkjenningsprosess før den sendes til arbeidsflyten.

- Velg **Parametere for innkjøp og leverandører** &gt; **Leverandørsamarbeid**, og velg deretter **Automatisk sending av registrering av potensiell leverandør til arbeidsflyt** for å konfigurere leverandørforespørselen slik at den sendes automatisk til en arbeidsflyt når registreringsveiviseren for leverandører er fullført.

## <a name="vendor-requests"></a>Leverandørforespørsler

Leverandørforespørsler er tilgjengelige på siden **Brukerforespørsler for leverandørsamarbeid**.

En leverandørforespørsel inneholder informasjonen som den potensielle leverandørbrukeren har angitt i registreringsveiviseren for leverandører.

I forespørselen kan du se leverandørinformasjonen og bestemme om leverandøren skal bli en registrert leverandør i Finance and Operations.

Leverandørforespørselen må sendes til en arbeidsflyt, og den må rutes til relevante godkjennere. For grunnleggende informasjon om hvordan du konfigurerer arbeidsflyter, se [Arbeidsflyter for innkjøp og leverandører](procurement-sourcing-workflows.md).

Tabellen nedenfor viser statusene leverandørforespørsler kan ha.

| Status                     | beskrivelse |
|----------------------------|-------------|
| Utkast                      | Leverandørforespørselen er ennå ikke sendt. |
| Forespørsel sendt          | Leverandørforespørselen er sendt, og det første trinnet i arbeidsflyten blir behandlet. |
| Venter på gjennomgang             | Hvis det er flere korrekturlesere i en arbeidsflytoppgave, kan en kontrollør godta oppgaven med å se gjennom leverandørforespørselen og deretter fullfører gjennomgangen. Hvis det er bare én korrekturleser, kan denne deltakeren fullføre gjennomgangen ved å velge **Fullført** i handlingen. Han eller hun trenger ikke å godta arbeidselementet først. |
| Forespørsel venter på godkjenning   | Leverandørforespørselen er distribuert til deltakerne for godkjenning, og det er mulig å søke etter mer informasjon. En forespørsel om tilleggsinformasjon fører til at arbeidselementet rutes returneres til avsenderen. Leverandørforespørselen kan også godkjennes eller forkastes når den er i denne statusen. |
| Forespørsel om søknadsendring | Tilleggsinformasjon er forespurt av godkjenneren, og leverandørforespørselen er distribuert til personen som sendte leverandørforespørselen. Innsenderen kan legge til påkrevde informasjon og deretter sende inn leverandørforespørselen på nytt. Hvis en leverandørforespørsel er sendt inn på nytt, endres statusen tilbake til **Forespørsel venter på godkjenning**. |
| Forespørsel godkjent           | Denne statusen er en endelig tilstand. |
| Forespørsel avvist           | Denne statusen er en endelig tilstand. |

## <a name="approving-a-vendor-request"></a>Godkjenne en leverandørforespørsel

Når en leverandørforespørsel er godkjent, opprettes en leverandørkonto, og statusen **Godkjent** vises på både innledende potensiell leverandør registreringsforespørsel og leverandørforespørselen.

Før du godkjenner en leverandørforespørsel, på siden **Ny leverandør**, på hurtigfanen **Generelt** velger du **Leverandørgruppe** for å velge en leverandørgruppe.

Hvis den potensielle leverandørbrukeren skal ha tilgang til Finance and Operations som en leverandørsamarbeidsbruker som representerer leverandøren, setter du den tilgangstillatelsen for leverandørsamarbeid til **Ja**. Hvis du vil deaktivere brukerkontoen som den potensielle leverandøren bruker til å registrere, setter du denne tillatelsen til **Nei**.

Hvis tilgangtillatelsen for leverandørensamarbeid er satt til **Ja**, når leverandørforespørselen er godkjent, sendes en forespørsel om å endre brukerens roller, slik at brukeren har rollene som er definert for typen **Leverandør** i **Eksterne roller**. Hvis denne tillatelsen er satt til **Nei**, når leverandørforespørselen er godkjent, sendes en forespørsel om å deaktivere brukeren. I så fall må arbeidsflyten for å deaktivere en brukerforespørsel, settes opp.

Nummerserien for opprettelse av leverandører fra leverandørforespørsler for en leverandørkonto som skal opprettes når leverandørforespørselen er godkjent, må settes til **Automatisk**.

For en oversikt over tilgangstillatelser til en leverandørsamarbeidsbruker, se [Definere og vedlikeholde leverandørsamarbeid](set-up-maintain-vendor-collaboration.md).

## <a name="rejecting-a-vendor-request"></a>Avvise en leverandørforespørsel

Hvis en leverandørforespørsel avvises, må en årsak til avvisningen velges i leverandørforespørselen.

Når en leverandørforespørsel avvises, sendes en forespørsel om å deaktivere brukeren. I så fall må arbeidsflyten for å deaktivere en brukerforespørsel, settes opp. Hvis du vil ha mer informasjon, se [Definere og vedlikeholde leverandørsamarbeid](set-up-maintain-vendor-collaboration.md).

Når en leverandørforespørsel er avvist, vises statusen **Avvist** på både innledende potensiell leverandør registreringsforespørsel og leverandørforespørselen.

## <a name="deleting-a-prospective-vendor-registration-request-in-various-statuses"></a>Slette en registreringsforespørsel for potensiell leverandør i forskjellige statuser

De forskjellige statusene til en registreringsforespørsel for potensiell leverandør viser en oversikt over fremdriften for forespørselen.

Ved hjelp av **Slett**-handlingen i registreringsforespørselen om potensiell leverandør kan du rydde og fjerne kjeden med poster som er opprettet, og du kan deaktivere brukerkontoen. Resultatet av **Slett**-handlingen varierer, avhengig av statusen for registreringsforespørselen for potensiell leverandør, som vist i følgende tabell.


|          Status          |                                                                                     Statusbeskrivelse                                                                                      |                                                                                                                                                            Resultatet av Slett-handlingen                                                                                                                                                             |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|           Nytt            |                                                                         Ingen handlinger er utført i forespørselen.                                                                          |                                                                                                                                              Forespørselen om registrering av potensiell leverandør er slettet.                                                                                                                                               |
|      Bruker forespurt      | Når du velger <strong>Inviter bruker</strong>, endres statusen til <strong>Bruker forespurt</strong>, og en potensiell brukerforespørsel opprettes og sendes til en arbeidsflyt. |                                                                                                          Du kan ikke slette en registreringsforespørsel for potensiell leverandør som har denne statusen, fordi arbeidsflyten ikke er avsluttet.                                                                                                          |
|       Bruker invitert       |                                                               Arbeidsflyten er godkjent, og brukeren blir opprettet.                                                               |                                                                                                                      En forespørsel om å deaktivere brukeren opprettes, og registreringsforespørselen for potensiell leverandør slettes.                                                                                                                      |
| Registrering pågår |                                                         Den nye brukeren har logget seg på og har startet veiviseren for registrering av leverandøren.                                                          |                                                                                     En forespørsel om å deaktivere brukeren opprettes, og av registreringsforespørselen for potensiell leverandør slettes, og dataene som ble angitt i registreringsveiviseren for leverandøren, slettes.                                                                                      |
|  Leverandørforespørsel opprettet  |                                                                     Registreringsveiviseren for leverandører er fullført.                                                                      | En forespørsel om å deaktivere brukeren opprettes, og av registreringsforespørselen for potensiell leverandør slettes, og dataene som ble angitt i registreringsveiviseren for leverandøren, og leverandørforespørselen slettes.<blockquote>[!NOTE]<br>Du kan ikke bruke <strong>Slett</strong>-handlingen når leverandørforespørselen er i en kontrollprosess i arbeidsflyten.</blockquote> |
|         Godkjent         |                                                                               Leverandørforespørselen er godkjent.                                                                               |                                                                                                   Registreringsforespørselen for potensiell leverandør slettes, dataene som ble angitt i registreringsveiviseren for leverandøren, og leverandørforespørselen slettes.                                                                                                    |
|         Avslått         |                                                                               Leverandørforespørselen er avvist.                                                                               |                                                                                                   Registreringsforespørselen for potensiell leverandør slettes, dataene som ble angitt i registreringsveiviseren for leverandøren, og leverandørforespørselen slettes.                                                                                                    |

