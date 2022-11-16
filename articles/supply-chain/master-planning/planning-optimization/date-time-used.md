---
title: Parametere for dato og klokkeslett som ikke brukes av planleggingsoptimalisering
description: Denne artikkelen gir informasjon om dato- og klokkeslettparameterne som planleggingsoptimalisering bruker under operasjonen.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2ef78c73a1c7033735f9586229ff7ba21daaa5ef
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740911"
---
# <a name="date-and-time-parameters-used-by-planning-optimization"></a>Parametere for dato og klokkeslett som ikke brukes av planleggingsoptimalisering

[!include [banner](../../includes/banner.md)]

Denne artikkelen gir informasjon om dato- og klokkeslettparameterne som planleggingsoptimalisering bruker under operasjonen.

Mens den avskrevne hovedplanleggingsmotoren bruker transaksjonsdatoer i alle beregninger, fungerer planleggingsoptimalisering med dato- og klokkeslettverdier som konverteres til datoer. Denne forskjellen i virkemåte kan føre til situasjoner der for eksempel prognosetransaksjoner som opprettes ved midnatt på dagen når hovedplanlegging kjøres, ikke tas med, fordi planleggingsoptimalisering tar hensyn til at de ble opprettet før gjeldende dato.

## <a name="parameters-for-issue-and-demand-transactions"></a>Parametere for avgangs- og behovstransaksjoner

Tabellen nedenfor viser parameterne som planleggingsoptimalisering bruker når det behandler avgangs- og behovstransaksjoner.

| Parameter | Parameternavn i planleggingsoptimalisering | Beskrivelse | Tilsvarende felt i Microsoft Dynamics 365 Supply Chain Management (i ReqTrans-tabellen) |
|---|---|---|---|
| Planlagt avgangstid | `PlannedIssueTime` | Datoen som avgangen er planlagt for. | **Til dato** (`FuturesDate`) og **Forsinket til klokkeslett** (`FuturesTime`) |
| Ønsket avgangstid | `RequestedIssueTime` | Dato for avgangen som ble forespurt av brukeren og angitt i Supply Chain Management. Denne parameteren gjelder bare for frigitte eller godkjente planlagte bestillinger. For planlagte bestillinger er det tomt som standard. | **Ønsket dato** (`ReqDateDlvOrig`) |
| Nødvendig avgangstid | `RequiredIssueTime` | Den nødvendige avgangsdatoen som er justert ved hjelp av planleggingsoptimalisering. Hvis den ønskede avgangstiden er i fortiden når planleggingsoptimalisering kjøres, blir den nødvendige avgangstiden justert til den første åpne dagen som ikke er tidligere enn dagens dato. Hvis den ønskede avgangstiden er merket som blokkert i kalenderen, justeres den nødvendige avgangstiden til den første åpne dagen før den datoen. | **Behovsdato** (`ReqDate`) og **Behovstid** (`ReqTime`) |
| Forsinkelse for avgang | `IssueTimeDelay` | Tidsforskjellen mellom den planlagte avgangstiden og enten ønsket avgangstid for godkjente og frigitte ordrer eller den nødvendige avgangstiden. | **Forsinkelse (i dager)** (`FuturesDays`) |

## <a name="parameters-for-receipt-and-supply-transactions"></a>Parametere for mottaks- og forsyningstransaksjoner

Tabellen nedenfor viser parameterne som planleggingsoptimalisering bruker når det behandler mottaks- og forsyningstransaksjoner.

| Parameter | Parameternavn i planleggingsoptimalisering | Beskrivelse | Tilsvarende felt i Supply Chain Management (i tabellen ReqTrans eller ReqPO) |
|---|---|---|---|
| Planlagt tilgjengelighetstid | `PlannedAvailabilityTime` | Datoen da mottaket er planlagt å være tilgjengelig. | **Behovsdato** (`ReqDate`) og **Behovstid** (`ReqTime`) |
| Planlagt mottakstid | `PlannedReceiptTime` | Datoen når mottaket ankommer lokasjonen. | **Til dato** (`FuturesDate`), **Forsinket til-klokkeslett** (`FuturesTime`) og **Leveringsdato** (`ReqDateDlv`) eller **Ønsket dato** (`ReqDateDlvOrig`) hvis orden ikke er frigitt ennå. |
| Nødvendig tilgjengelighetstid | `RequiredAvailabilityTime` | Den nødvendige tilgjengelighetsdatoen som er justert ved hjelp av planleggingsoptimalisering. | **Behovsdato** (`ReqDate`) og **Behovstid** (`ReqTime`) |
| Forventet mottakstid | `ExpectedReceiptTime` | Forventet mottaksdato for et frigitt mottak. Verdien angis av brukeren i Supply Chain Management og justeres ikke ved hjelp av planleggingsoptimalisering. Denne parameteren gjelder bare for frigitte mottak. | **Ønsket dato** (`ReqDateDlvOrig`) |
| Nødvendig mottakstid | `RequiredReceiptTime` | Den nødvendige mottaksdatoen som er justert ved hjelp av planleggingsoptimalisering. | **Behovsdato** (`ReqDate`) og **Behovstid** (`ReqTime`) |
| Planlagt bestillingstid | `PlannedOrderingTime` | Bestillingsdatoen som er beregnet ved hjelp av planleggingsoptimalisering. | **Ordredato** (`ReqDateOrder`) og **Ordretid** (`ReqTimeOrder`) |
| Planlagt starttid for aktivitet | `PlannedActivityStartTime` | Datoen når aktiviteten for dette mottaket skal starte. | **Startdato** (`SchedFromDate`) |
| Tidsforsinkelse for mottak | `ReceiptTimeDelay` | Tidsdifferansen mellom den planlagte mottakstiden og den nødvendige mottakstiden. | **Forsinkelse (dager)** (`FuturesDays`) og **Forsinket til klokkeslett** (`FuturesTime`) |

## <a name="examples-of-date-parameter-use-by-planning-optimization"></a>Eksempler på datoparameterbruk ved planleggingsoptimalisering

Planene i følgende illustrasjoner er på dagnivå, men planleggingsoptimaliseringen kjøres på et mer detaljert nivå. Fordi marginer for eksempel kan være i timer, kan planleggingsordretiden være 22. januar, 2021, 11:35 og så videre.

### <a name="example-1-simple-scenario"></a>Eksempel 1: Enkelt scenario

Én salgsordre som har et forespurt avgangstid 22. januar, dekkes av én bestilling. Følgende innstillinger brukes:

- Ingen leveringstid
- Ingen kalendere (Alle dager er åpne.)
- Ingen marginer

Illustrasjonen nedenfor viser dette scenarioet. (Velg illustrasjonen for å åpne en større versjon.)

[![Enkelt scenario.](media/planning-service-dates-1-small.png)](media/planning-service-dates-1.png)

### <a name="example-2-lead-time-scenario"></a>Eksempel 2: Leveringstidsscenario

Én salgsordre som har et forespurt avgangstid 22. januar, dekkes av én bestilling. Følgende innstillinger brukes:

- Tre dager med leveringstid
- Ingen kalendere (Alle dager er åpne.)
- Ingen marginer

Illustrasjonen nedenfor viser dette scenarioet. (Velg illustrasjonen for å åpne en større versjon.)

[![Leveringstidsscenario.](media/planning-service-dates-2-small.png)](media/planning-service-dates-2.png)

### <a name="example-3-margin-scenario"></a>Eksempel 3: Marginscenario

Én salgsordre som har et forespurt avgangstid 22. januar, dekkes av én bestilling. Følgende innstillinger brukes:

- Tre dager med leveringstid
- Bestillingsmargin på fire dager
- Femdagers tilgjengelighetsmargin
- Ingen kalendere (Alle dager er åpne.)

Illustrasjonen nedenfor viser dette scenarioet. (Velg illustrasjonen for å åpne en større versjon.)

[![Marginscenario.](media/planning-service-dates-3-small.png)](media/planning-service-dates-3.png)

### <a name="example-4-delay-scenario"></a>Eksempel 4: Forsinkelsesscenario

Én salgsordre som har et forespurt avgangstid 22. januar, dekkes av én bestilling. I dette eksemplet brukes de samme innstillingene som eksempel 3, men planleggingsdatoen er flyttet til 15. januar. Planlegging bakover (røde indikatorer) mislykkes, fordi planlagt bestillingstid må være før dagens dato. Hovedplanleggingen må derfor planlegges fremover og gi forsinkelser.

Illustrasjonen nedenfor viser dette scenarioet. (Velg illustrasjonen for å åpne en større versjon.)

[![Forsinkelsesscenario.](media/planning-service-dates-4-small.png)](media/planning-service-dates-4.png)

### <a name="example-5-transfer-scenario"></a>Eksempel 5: Overføringsscenario

Én salgsordre fra lager 1 som har en forespurt avgangstid den 22. januar, dekkes av én overføringsordre fra lager 2, som er dekket av et bestillingsforslag. Følgende innstillinger brukes:

- Tre dager med overføringstid (lager 1)
- To dager med leveringstid for innkjøp (lager 2)
- Ingen kalendere (Alle dager er åpne.)

Illustrasjonen nedenfor viser dette scenarioet. (Velg illustrasjonen for å åpne en større versjon.)

[![Overføringsscenario.](media/planning-service-dates-5-small.png)](media/planning-service-dates-5.png)

### <a name="example-6-lead-time-with-calendars-scenario"></a>Eksempel 6: Leveringstid med kalenderscenario

Én salgsordre som har et forespurt avgangstid 22. januar, dekkes av én bestilling. Følgende innstillinger brukes:

- Tre dager med leveringstid
- Avgangskalender (lukket på fredag)
- Tilgjengelighetskalender (lukket på torsdag og fredag)
- Mottakskalender (lukket på tirsdag, onsdag og søndag)
- Leveringstidskalender (lukket på torsdag og fredag)
- Bestillingskalender (åpen på mandag og lørdag)

Illustrasjonen nedenfor viser dette scenarioet. (Velg illustrasjonen for å åpne en større versjon.)

[![Leveringstid med kalenderscenario.](media/planning-service-dates-6-small.png)](media/planning-service-dates-6.png)

### <a name="example-7-delay-with-calendars-scenario"></a>Eksempel 7: Forsinkelse med kalenderscenario

Én salgsordre som har et forespurt avgangstid 22. januar, dekkes av én bestilling. I dette eksemplet brukes de samme innstillingene som eksempel 6, men planleggingsdatoen er flyttet til 13. januar. Planlegging bakover (røde indikatorer) mislykkes, fordi planlagt bestillingstid må være før dagens dato. Hovedplanleggingen må derfor planlegges fremover og gi forsinkelser.

Illustrasjonen nedenfor viser dette scenarioet. (Velg illustrasjonen for å åpne en større versjon.)

[![Forsinkelse med kalenderscenario.](media/planning-service-dates-7-small.png)](media/planning-service-dates-7.png)
