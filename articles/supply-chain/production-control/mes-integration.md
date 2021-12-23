---
title: Integrer med tredjeparts produksjonsutførelsessystemer
description: Dette emnet beskriver hvordan du kan integrere Microsoft Dynamics 365 Supply Chain Management med et MES-system (tredjeparts produksjonsutførelsessystem).
author: t-benebo
ms.date: 10/01/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 43814023474d44b8c95bae087c7b6a4d52d21471
ms.sourcegitcommit: 7cbd53617af179a0de74aae30c149edc95e86684
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2021
ms.locfileid: "7891932"
---
# <a name="integrate-with-third-party-manufacturing-execution-systems"></a>Integrer med tredjeparts produksjonsutførelsessystemer

[!include [banner](../includes/banner.md)]

Enkelte produksjonsorganisasjoner som bruker Microsoft Dynamics 365 Supply Chain Management, bruker den opprinnelige funksjonaliteten i Dynamics 365 til å kontrollere produksjonsaktivitetene for maskiner, utstyr og personale. Andre produksjonsorganisasjoner, spesielt de som har avanserte produksjonskrav, bruker i stedet et MES-system (produksjonstuførelsessystem) fra en tredjepart. Organisasjoner kan velge en MES-løsning fra en tredjepart, fordi den for eksempel er spesielt tilpasset den vertikale bransjen.

I den integrerte løsningen er datautveksling fullstendig automatisert og skjer i nær sanntid. Dataene holdes derfor oppdatert i begge systemene, og det kreves ingen manuell dataregistrering. Når for eksempel materialforbruk registreres i MES, sikrer integreringen at samme forbruk også registreres i Dynamics 365. Derfor er oppdaterte lagerposter tilgjengelige for andre viktige prosesser, for eksempel planlegging og salg.

Løsningen gjør det raskere, enklere og gjør det lettere for brukerne i Supply Chain Management å integrere med MES-er fra en tredjepart. Den har følgende egenskaper:

- Forretningshendelser og grensesnitt som støtter [viktige produksjonsutførelsesprosesser](#processes-available-for-mes-integration)
- Sentralisert instrumentbord der du kan spore hendelsesbehandlingshistorikken og feilsøke og korrigere prosesser som mislykkes

Illustrasjonen nedenfor viser en vanlig samling forretningshendelser, prosesser og meldinger som utveksles i en integrert løsning.

![Typisk integreringsscenario.](media/3p-mes-scenario.png "Typisk integreringsscenario.")

## <a name="turn-on-the-mes-integration-feature"></a>Aktiver funksjonen for MES-integrering

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Produksjonskontroll*
- **Funksjonsnavn:** *Integrering av produksjonsutførelsessystem*

## <a name="processes-available-for-mes-integration"></a>Tilgjengelige prosesser for MES-integrering

Du kan aktivere noen av eller alle de følgende prosessene for integrering.

| Prosessnavn | Beskrivelse |
|---|---|
| Frigi produksjonsordrer og produksjonsordrestatus endre forretningshendelser | Denne prosessen inneholder et forretningshendelse som MES kan høre til, for å få informasjon om produksjonsordrene som skal produseres. Referansedata som er relatert til produksjonsordren, forventes å bli delt fra Supply Chain Management til MES via Open Data Protocol (OData) eller dataenheter. |
| Start produksjonsordre | Denne prosessen gir Supply Chain Management informasjon om produksjonsordrer som startes ved hjelp av MES. Den sikrer at begge systemene har en oppdatert oversikt over alle produksjonsaktiviteter. |
| Rapporter produsert eller kassert antall | Denne prosessen gir Supply Chain Management informasjon om antallet gode produkter og produkter med feil som rapporteres for en produksjonsjobb ved hjelp av MES. Den sikrer at produksjonsarbeidsledere har en oppdatert oversikt over produksjonsplanfremdriften. |
| Rapporter råvareforbruk | Denne prosessen gir Supply Chain Management informasjon fra MES om antallet materialer som forbrukes. Den gjør oppdaterte lagerposter tilgjengelige for andre viktige prosesser, for eksempel planlegging og salg. |
| Rapporter forbrukt tid for operasjonen | Denne prosessen gir Supply Chain Management informasjon om tiden som brukes til en bestemt operasjon. |
| Avslutt produksjonsordre | Denne prosessen informerer Supply Chain Management om at MES har oppdatert en produksjonsordre til den endelige statusen *Avsluttet*. Denne statusen angir at det ikke vil bli produsert flere antall i produksjonsordren. |

## <a name="monitor-incoming-messages"></a>Overvåk innkommende meldinger

Hvis du vil overvåke innkommende meldinger til systemet, åpner du siden **Integrering av produksjonsutførelsessystemer**. Der kan du vise, behandle og feilsøke problemer.

## <a name="call-the-api"></a>Kall API-en

Hvis du vil kalle API-en for MES-integrering, sender du en `POST`-forespørsel til følgende endepunkts-URL:

`/api/services/SysMessageServices/SysMessageService/SendMessage`

Teksten i forespørselen du sender, skal ligne på følgende eksempel. Erstatt verdiene for `_companyId`, `_messageType` og `_messageContent` etter behov. Hvis du vil ha informasjon om de ulike meldingstypene som API-en støtter, og hvordan du utformer innholdet, kan du se neste del.

```json
{
    "_companyId": "USMF",
    "_messageQueue": "JmgMES3P",
    "_messageType": "ProdProductionOrderReportFinished",
    "_messageContent":
    "{\"ProductionOrderNumber\": \"P000123\", \"ReportFinishedLines\": [{\"ItemNumber\": \"A0001\", \"ReportedGoodQuantity\": 10, \"ReportAsFinishedDate\": \"2021-01-01\"}]}"
}
```

## <a name="api-message-types-and-content"></a>API-meldingstyper og -innhold

Denne delen beskriver hver meldingstype som kan utveksles via API-en for MES-integrering.

### <a name="start-production-order-message"></a>Melding om start av produksjonsordre

For meldingen om *start av produksjonsordre* er `_messageType`-verdien `ProdProductionOrderStart`. Tabellen nedenfor viser feltene som denne meldingen støtter.

| Feltnavn | Status | Type |
|---|---|---|
| `ProductionOrderNumber` | Obligatorisk | Streng |
| `StartedQuantity` | Valgfri | Kommatall |
| `StartedDate` | Valgfri | Dato |
| `AutomaticBOMConsumptionRule` | Valgfri | Enum (FlushingPrincip \| Alltid \| Aldri) |

### <a name="report-as-finished-message"></a>Ferdigmelding

For *ferdigmeldingen* er `_messageType`-verdien `ProdProductionOrderReportFinished`. Tabellen nedenfor viser feltene som denne meldingen støtter.

| Feltnavn | Status | Type |
|---|---|---|
| `ProductionOrderNumber` | Obligatorisk | Streng |
| `ReportFinishedLines` | Obligatorisk | En liste over linjer (minst én), der hver linje inneholder nyttelasten som er beskrevet i neste tabell |

Følgende tabell viser feltene som hver linje i `ReportFinishedLines`-delen av `ProdProductionOrderReportFinished`-meldingen støtter.

| Feltnavn | Status | Type |
|---|---|---|
| `LineNumber` | Valgfri | Kommatall |
| `ItemNumber` | Valgfri | Streng|
| `ProductionType` | Valgfri | Enum (MainItem \| Formel \| Stykkliste \| Co_Product \| By_Product \| Ingen), utvidbar |
| `ReportedErrorQuantity` | Valgfri | Kommatall|
| `ReportedGoodQuantity` | Valgfri | Kommatall|
| `ReportedErrorCatchWeightQuantity` | Valgfri | Kommatall |
| `ReportedGoodCatchWeightQuantity` | Valgfri | Kommatall |
| `AcceptError` | Valgfri |Boolsk |
| `ErrorCause` | Valgfri | Enum (Ingen \| Materiale \| Maskin \| OperatingStaff), utvidbar |
| `ExecutedDateTime` | Valgfri | dato/klokkeslett |
| `ReportAsFinishedDate` | Valgfri | Dato |
| `AutomaticBOMConsumptionRule` | Valgfri | Enum (FlushingPrincip \| Alltid \| Aldri) |
| `AutomaticRouteConsumptionRule` | Valgfri |Enum (RouteDependent \| Alltid \| Aldri) |
| `RespectFlushingPrincipleDuringOverproduction` | Valgfri | Boolsk |
| `ProductionJournalNameId` | Valgfri | Streng |
| `PickingListProductionJournalNameId` | Valgfri | Streng|
| `RouteCardProductionJournalNameId` | Valgfri | Streng |
| `FromOperationNumber` | Valgfri | Heltall|
| `ToOperationNumber` | Valgfri | Heltall|
| `InventoryLotId` | Valgfri | Streng |
| `BaseValue` | Valgfri | Streng |
| `EndJob` | Valgfri | Boolsk |
| `EndPickingList` | Valgfri | Boolsk |
| `EndRouteCard` | Valgfri | Boolsk |
| `PostNow` | Valgfri | Boolsk |
| `AutoUpdate` | Valgfri | Boolsk |
| `ProductColorId` | Valgfri | Streng|
| `ProductConfigurationId` | Valgfri | Streng |
| `ProductSizeId` | Valgfri | Streng |
| `ProductStyleId` | Valgfri | Streng |
| `ProductVersionId` | Valgfri | Streng |
| `ItemBatchNumber` | Valgfri | Streng |
| `ProductSerialNumber` | Valgfri | Streng |
| `LicensePlateNumber` | Valgfri | Streng |
| `InventoryStatusId` | Valgfri | Streng |
| `ProductionWarehouseId` | Valgfri | Streng |
| `ProductionSiteId` | Valgfri | Streng |
| `ProductionWarehouseLocationId` | Valgfri | Streng |
| `InventoryDimension1` til `InventoryDimension12` | Valgfri | Streng |

De 12 utvidbare dimensjonene (`InventoryDimension1` til `InventoryDimension12`) krever tilpasning og innhold som ikke alltid er brukt. Hvis du vil ha mer informasjon om dem, kan du se [Legg til nye lagerdimensjoner via utvidelse](../../fin-ops-core/dev-itpro/extensibility/inventory-dimensions.md).

### <a name="material-consumption-picking-list-message"></a>Melding om materialforbruk (plukkliste)

For meldingen *om materialforbruk (plukkliste)* er `_messageType`-verdien `ProdProductionOrderPickingList`. Tabellen nedenfor viser feltene som denne meldingen støtter.

| Feltnavn | Status | Type |
|---|---|---|
| `ProductionOrderNumber` | Obligatorisk | Streng |
| `JournalNameId` | Valgfri | Streng |
| `PickingListLines` | Obligatorisk | En liste over linjer (minst én), der hver linje inneholder nyttelasten som er beskrevet i neste tabell |

Følgende tabell viser feltene som hver linje i `PickingListLines`-delen av `ProdProductionOrderPickingList`-meldingen støtter.

| Feltnavn | Status | Type |
|---|---|---|
| `ItemNumber` | Obligatorisk | Streng |
| `ConsumptionBOMQuantity` | Valgfri | Kommatall |
| `ProposalBOMQuantity` | Valgfri | Kommatall |
| `ScrapBOMQuantity` | Valgfri | Kommatall |
| `BOMUnitSymbol` | Valgfri | Streng |
| `ConsumptionInventoryQuantity` | Valgfri | Kommatall |
| `ProposalInventoryQuantity` | Valgfri | Kommatall |
| `ConsumptionCatchWeightQuantity` | Valgfri | Kommatall |
| `ProposalCatchWeightQuantity` | Valgfri | Kommatall |
| `ConsumptionDate` | Valgfri | Dato |
| `OperationNumber` | Valgfri | Heltall |
| `LineNumber` | Valgfri | Kommatall |
| `PositionNumber` | Valgfri | Streng |
| `IsConsumptionEnded` | Valgfri | Boolsk |
| `ErrorCause` | Valgfri | Enum (Ingen \| Materiale \| Maskin \| OperatingStaff), utvidbar |

### <a name="time-used-for-operation-route-card-message"></a>Melding om tid brukt til operasjon (rutekort)

For meldingen om *tid brukt til operasjon (rutekort)* er `_messageType`-verdien `ProdProductionOrderRouteCard`. Tabellen nedenfor viser feltene som denne meldingen støtter.

| Feltnavn | Status | Type |
|---|---|---|
| `ProductionOrderNumber` | Obligatorisk | Streng |
| `JournalNameId` | Valgfri | Streng |
| `RouteCardLines` | Obligatorisk | En liste over linjer (minst én), der hver linje inneholder nyttelasten som er beskrevet i neste tabell |

Følgende tabell viser feltene som hver linje i `RouteCardLines`-delen av `ProdProductionOrderRouteCard`-meldingen støtter.

| Feltnavn | Status | Type |
|---|---|---|
| `OperationNumber` | Obligatorisk | Heltall |
| `OperationPriority` | Valgfri | Enum (Primary \| Secondary1 \| Secondary2 \| ... \| Secondary20) |
| `OperationId` | Valgfri | Streng |
| `OperationsResourceId` | Valgfri | Streng |
| `Worker` | Valgfri | Streng |
| `HoursRouteCostCategoryId` | Valgfri | Streng |
| `QuantityRouteCostCategoryId` | Valgfri | Streng |
| `HourlyRate` | Valgfri | Kommatall |
| `Hours` | Valgfri | Kommatall |
| `GoodQuantity` | Valgfri | Kommatall |
| `ErrorQuantity` | Valgfri | Kommatall |
| `CatchWeightGoodQuantity` | Valgfri | Kommatall |
| `CatchWeightErrorQuantity` | Valgfri | Kommatall |
| `QuantityPrice` | Valgfri | Kommatall |
| `ProcessingPercentage` | Valgfri | Kommatall |
| `ConsumptionDate` | Valgfri | Dato |
| `TaskType` | Valgfri | Enum (QueueBefore \| Setup \| Process \| Overlap \| Transport \| QueueAfter \| Burden) |
| `ErrorCause` | Valgfri | Enum (Ingen \| Materiale \| Maskin \| OperatingStaff), utvidbar |
| `OperationCompleted` | Valgfri | Boolsk |
| `BOMConsumption` | Valgfri | Boolsk |
| `ReportAsFinished` | Valgfri | Boolsk |

### <a name="end-production-order-message"></a>Melding om avslutning av produksjonsordre

For meldingen om *avslutning av produksjonsordre* er `_messageType`-verdien `ProdProductionOrderEnd`. Tabellen nedenfor viser feltene som denne meldingen støtter.

| Feltnavn | Status | Type |
|---|---|---|
| `ProductionOrderNumber` | Obligatorisk | Streng |
| `ExecutedDateTime` | Valgfri | dato/klokkeslett |
| `EndedDate` | Valgfri | Dato |
| `UseTimeAndAttendanceCost` | Valgfri | Boolsk |
| `AutoReportAsFinished` | Valgfri | Boolsk |
| `AutoUpdate` | Valgfri | Boolsk |

## <a name="receive-feedback-about-the-state-of-a-message"></a>Motta tilbakemelding om tilstanden til en melding

Etter at MES har sendt en melding til Supply Chain Management, kan det være relevant for Supply Chain Management å returnere en tilbakemelding om tilstanden til meldingen. Her er noen eksempler på tilfeller der denne virkemåten kan være relevant:

- Det er ingen person som er ansvarlig for konstant overvåking av MES-integreringen.
- Personen som er ansvarlig for overvåking av MES-integreringen, ønsker å bli varslet via e-post når en melding mislykkes, slik at de vet at de må gjøre noe.
- MES må vise en feilmelding for å kunne informere produksjonsoperatøren eller en person fra IT-avdelingen om at de må gjøre noe.
- MES må beregne ordreplanen på nytt etter at den har mottatt en feilmelding (for eksempel fordi en produksjonsordre ikke kunne starte).

I slike tilfeller kan du dra nytte av standard varslingsfunksjonen i Supply Chain Management. Hvis du vil ha informasjon om hvordan standardvarsler fungerer, kan du se følgende ressurser:

- Hjelpeemne: [Oversikt over varsler](../../fin-ops-core/fin-ops/get-started/alerts-overview.md)
- Video: [Alternativer for varslingsregel i Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=cpzimwOjicM&ab_channel=MicrosoftDynamics365)

Du kan for eksempel angi følgende varsler for å gi tilbakemelding om tilstanden til en melding:

- Opprett en forretningshendelse ("Send eksternt") som brukes når en melding er *mislykket*.
- Send et varsel og en e-post til IT-administratoren eller produksjonslederen.
