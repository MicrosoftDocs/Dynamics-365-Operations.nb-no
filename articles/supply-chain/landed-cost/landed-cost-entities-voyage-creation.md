---
title: Enheter for reiseoppretting
description: Dette emnet gir informasjon om dataenheter for reiseoppretting, som grupperer dataenhetene som er nødvendige for å opprette en arbeidsgruppe.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 17f63af3ce1f858ed3e2086fc81c5e17c5e76be0
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813128"
---
# <a name="voyage-creation-entities"></a>Enheter for reiseoppretting

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

Dataenheter for sjøreiseoppretting grupperer dataenhetene som er nødvendige for å opprette en arbeidsgruppe. Du eller fraktforsenderen kan bruke disse dataenhetene til å opprette oppføringer for reise, forsendelsescontainer, folio og reiselinje som refererer til eksisterende innkjøperordrer eller overføringsordrelinjer.

## <a name="voyages-itmtableentity"></a>Reiser (ITMTableEntity)

Reisen representerer reisen til innkommende varer og fungerer som kostnadsområdet på høyeste nivå i Landingskostnad. Den inneholder hodenivåinformasjon som er knyttet til fartøy, opprinnelseshavn og målport. Denne funksjonen støttes av `ITMTableEntity`-enheten. I tabellen nedenfor finner du en oversikt over felt og tilordninger som utgjør denne enheten.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Leveringsmåte | ITMTable.DlvModeId | Nvarchar(10) | Nei | Nei |
| Megler informert | ITMTable.ITMBrokerAdvised | Dato/klokkeslett | Nei | Nei |
| Kundeavtale | ITMTable.ITMCustomerAppointment | Dato/klokkeslett | Nei | Nei |
| Levert ved lager | ITMTable.ITMDelAtWarehouse | Dato/klokkeslett | Nei | Nei |
| Leveringsinstruksjoner | ITMTable.ITMDeliveryInstructions | Dato/klokkeslett | Nei | Nei |
| Avreisedato | ITMTable.ITMDepartureDate | Dato/klokkeslett | Nei | Nei |
| Varer frigitt | ITMTable.ITMGoodsReleased | Dato/klokkeslett | Nei | Nei |
| Dato for lokal transport | ITMTable.ITMLocalTransportDate | Dato/klokkeslett | Nei | Nei |
| Klokkeslett for lokal transport | ITMTable.ITMLocalTransportTime | Int | Nei | Nei |
| Opprinnelig fraktbrev sendt | ITMTable.ITMOriginalBOLSebt | Dato/klokkeslett | Nei | Nei |
| Opprinnelige dokumenter mottatt | ITMTable.ITMOriginalDocsReceived | Dato/klokkeslett | Nei | Nei |
| Bestillingsstatus | ITMTable.ITMPurchStatus | Int | Nei | Nei |
| Bekreftelsesdato | ITMTable.ITMVerificationDate | Dato/klokkeslett | Nei | Nei |
| Identifikator for tollinngang | ITMTable.ShipCustomsEntryId | Nvarchar(20) | Nei | Nei |
| Forsendelsesdato | ITMTable.ShipDate | Dato/klokkeslett | Nei | Nei |
| Beskrivelse | ITMTable.ShipDescription | Nvarchar(60) | Nei | Nei |
| Dokumenter mottatt | ITMTable.ShipDocReceived | Int | Nei | Nei |
| Estimert leveringsdato | ITMTable.ShipEstDlvDate | Dato/klokkeslett | Nei | Nei |
| Beregnet ankomst ved forsendelseshavn | ITMTable.ShipEstPortDate | Dato/klokkeslett | Nei | Nei |
| Fra-havn | ITMTable.ShipFromPort | Nvarchar(20) | Nei | Nei |
| Flyfraktseddelen/fraktbrev | ITMTable.ShipHAWB | Nvarchar(20) | Nei | Nei |
| Sjøreise | ITMTable.ShipId | Nvarchar(20) | **Ja** | **Ja** |
| Bestillingsreferanse | ITMTable.ShipIdExternal | Nvarchar(20) | Nei | Nei |
| Reisemal | ITMTable.ShipJourneyId | Nvarchar(20) | Nei | Nei |
| Lokal videresender | ITMTable.ShipLocalForwarder | Nvarchar(20) | Nei | Nei |
| MAWB/fraktbrev | ITMTable.ShipMAWB | Nvarchar(20) | Nei | Nei |
| Mål | ITMTable.ShipMeasurement | Numeric(32, 6) | Nei | Nei |
| Måleenhet | ITMTable.ShipMeasurementUnit | Int | Nei | Nei |
| Antall paller | ITMTable.ShipNoOfPallets | Int | Nei | Nei |
| Ventende sjøreise | ITMTable.ShipPending | Int | Nei | Nei |
| Kommentarer | ITMTable.ShipRemarks | Nvarchar(MAX) | Nei | Nei |
| Utleie | ITMTable.ShipRental | Int | Nei | Nei |
| Sjøreisestatus | ITMTable.ShipStatusId | Nvarchar(20) | Nei | Nei |
| Telling i nummer | ITMTable.ShipTallyInNumber | Nvarchar(20) | Nei | Nei |
| Til-havn | ITMTable.ShipToPort | Nvarchar(20) | Nei | Nei |
| Verdisettingsdato | ITMTable.ShipValuationDate | Dato/klokkeslett | Nei | Nei |
| Forsendelsesfirma | ITMTable.ShipVendAccount | Nvarchar(20) | Nei | Nei |
| Fartøy | ITMTable.ShipVesselId | Nvarchar(20) | Nei | **Ja** |
| Ekstern sjøreise-ID | ITMTable.ShipVoyage | Nvarchar(20) | Nei | Nei |

### <a name="number-sequences-for-voyages"></a>Nummerserier for reiser

Den delte nummerserien for reiser kontrollerer tildelingen av reise-IDer.

Verdien som sendes til dataenheten når verdien **Reise-ID** (`ShipId`) brukes til å identifisere en eksisterende post for oppdatering. Hvis posten ikke finnes, avhenger virkemåten av om den tilordnede nummerserien er konfigurert til å tillate manuell registrering:

- Hvis manuell registrering er aktivert, opprettes det en ny post som bruker den sendte verdien.
- Hvis nummeret på den manuelle registreringen ikke er aktivert, brukes neste nummer i den tilordnede nummerserien i stedet for den sendte verdien.

Under importøkten beholdes plassholderverdien som importeres som flytte-IDen. Denne virkemåten sikrer at forsendelsescontainer- og reiselinjer som refererer til plassholderen, inkluderes i forløpet, og at de oppdateres for å gjenspeile verdien som er tilordnet fra nummerserien.

### <a name="automatic-cost-transactions"></a>Automatiske kostnadstransaksjoner

Automatiske kostnader kan legges til en reise fra siden **Automatiske kostnader** i Microsoft Dynamics 365 Supply Chain Management (**Landingskostnad \> Etterkalkuleringsoppsett \> Automatiske kostnader**). Poster for automatiske kostnader kan også opprettes ved å bruke dataenheter for kostnadstransaksjoner for hvert kostnadsområde som støtter landingskostnader.

Automatiske kostnader som konfigureres i Supply Chain Management, brukes på reisen når en reiselinje opprettes. Ingen kostnader vil være synlige mot posten før hodeposten er knyttet til linjeinformasjon.

## <a name="shipping-containers-itmcontainersentity"></a>Forsendelsescontainere (ITMContainersEntity)

En forsendelsescontainer representerer en fysisk container som varer transporteres i. Denne fysiske containeren kan være en fraktcontainer for sjøfrakt eller en enkelt pall for flyfrakt. Forsendelsescontaineren inneholder informasjon på hodenivå som er knyttet til forsendelsescontainer-ID, forseglingsnummer og forsendelsescontainertype. (Forsendelsescontainertypen gir dimensjonsinformasjon.) Denne funksjonaliteten støttes av `ITMContainersEntity`-enheten. I tabellen nedenfor finner du en oversikt over felt og tilordninger som utgjør denne enheten.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Avreisedato | ITMContainers.ITMDepartureDate | Dato/klokkeslett | Nei | Nei |
| Dato for lokal transport | ITMContainers.ITMLocalTransportDate | Dato/klokkeslett | Nei | Nei |
| Klokkeslett for lokal transport | ITMContainers.ITMLocalTransportTime | Int | Nei | Nei |
| Original sjøreise | ITMContainers.OrigShipId | Nvarchar(20) | Nei | Nei |
| Faktisk vekt | ITMContainers.ShipActualWeight | Numeric(32, 6) | Nei | Nei |
| Megler informert | ITMContainers.ShipBrokerAdvised | Dato/klokkeslett | Nei | Nei |
| Fraktcontainer | ITMContainers.ShipContainerId | Nvarchar(20) | **Ja** | **Ja** |
| Fraktcontainertype | ITMContainers.ShipContainerTypeId | Nvarchar(20) | Nei | Nei |
| Enhetstype | ITMContainers.ShipContainerUnitTypeId | Nvarchar(10) | Nei | Nei |
| Konvertert til leie | ITMContainers.ShipConvertedToRental | Int | Nei | Nei |
| Kundeavtale | ITMContainers.ShipCustomerAppointment | Dato/klokkeslett | Nei | Nei |
| Forsendelsesdato | ITMContainers.ShipDate | Dato/klokkeslett | Nei | Nei |
| Levert ved lager | ITMContainers.ShipDelAtWarehouse | Dato/klokkeslett | Nei | Nei |
| Leveringsinstruksjoner | ITMContainers.ShipDeliveryInstructions | Dato/klokkeslett | Nei | Nei |
| Ikrafttredelsesdato for undersøkelsessertifikat | ITMContainers.ShipECAppliedDate | Dato/klokkeslett | Nei | Nei |
| Utløpsdato for undersøkelsessertifikat | ITMContainers.ShipECExpiryDate | Dato/klokkeslett | Nei | Nei |
| Undersøkelsessertifikatnummer | ITMContainers.ShipECNum | Nvarchar(20) | Nei | Nei |
| Mottaksdato for undersøkelsessertifikat | ITMContainers.ShipECReceivedDate | Dato/klokkeslett | Nei | Nei |
| Estimert leveringsdato | ITMContainers.ShipEstDlvDate | Dato/klokkeslett | Nei | Nei |
| Beregnet ankomst ved forsendelseshavn | ITMContainers.ShipEstPortDate | Dato/klokkeslett | Nei | Nei |
| Forventet lastedato | ITMContainers.ShipExpectedLoadingDate | Dato/klokkeslett | Nei | Nei |
| Fra-havn | ITMContainers.ShipFromPort | Nvarchar(20) | Nei | Nei |
| Beskrivelse av varer | ITMContainers.ShipGoodsDesc | Nvarchar(60) | Nei | Nei |
| Varer frigitt | ITMContainers.ShipGoodsReleased | Dato/klokkeslett | Nei | Nei |
| Enhet for GPS-sporing | ITMContainers.ShipGPSUnit | Nvarchar(30) | Nei | Nei |
| Flyfraktseddelen/fraktbrev | ITMContainers.ShipHAWB | Nvarchar(20) | Nei | Nei |
| Sjøreise | ITMContainers.ShipId | Nvarchar(20) | **Ja** | **Ja** |
| Reisemal | ITMContainers.ShipJourneyId | Nvarchar(20) | Nei | Nei |
| Lokal videresender | ITMContainers.ShipLocalForwarder | Nvarchar(20) | Nei | Nei |
| Mål | ITMContainers.ShipMeasurement | Numeric(32, 6) | Nei | Nei |
| Måleenhet | ITMContainers.ShipMeasurementUnit | Int | Nei | Nei |
| Antall kartonger | ITMContainers.ShipNoOfCartons | Numeric(32, 6) | Nei | Nei |
| Opprinnelig fraktbrev sendt | ITMContainers.ShipOriginalBOLSebt | Dato/klokkeslett | Nei | Nei |
| Opprinnelige dokumenter mottatt | ITMContainers.ShipOriginalDocsReceived | Dato/klokkeslett | Nei | Nei |
| Vårt forseglingsnummer | ITMContainers.ShipOurSealNum | Nvarchar(20) | Nei | Nei |
| Brukt | ITMContainers.ShipPendingUsed | Int | Nei | Nei |
| Bestillingsstatus | ITMContainers.ShipPurchStatus | Int | Nei | Nei |
| Kjøletype | ITMContainers.ShipRefrigerationTypeId | Nvarchar(10) | Nei | Nei |
| Kommentarer | ITMContainers.ShipRemarks | Nvarchar(MAX) | Nei | Nei |
| Utleie | ITMContainers.ShipRental | Int | Nei | Nei |
| Returnerbar | ITMContainers.ShipReturnable | Int | Nei | Nei |
| Sjøreisestatus | ITMContainers.ShipStatusId | Nvarchar(20) | Nei | Nei |
| Forseglingsnummer for forsendelsesfirma | ITMContainers.ShipTheirSealNum | Nvarchar(20) | Nei | Nei |
| Til-havn | ITMContainers.ShipToPort | Nvarchar(20) | Nei | Nei |
| Bekreftelsesdato | ITMContainers.ShipVerificationDate | Dato/klokkeslett | Nei | Nei |
| Fartøy | ITMContainers.ShipVesselId | Nvarchar(20) | Nei | **Ja** |

### <a name="voyage-id-validation"></a>Validering av reise-ID

Forsendelsescontainer-IDen som kontrolleres av en nummerserie. Den er bare unik i konteksten av reisen som den brukes på.

Hvis forsendelsescontainerenheten (`ITMContainersEntity`) brukes uavhengig av enheten (`ITMTableEntity`entity entity), må **Reise-ID** (`ShipId`) samsvare med en eksisterende post i reisetabellen. Hvis ikke vil importen mislykkes.

Hvis forsendelsescontainerenheten (`ITMContainersEntity`) og reiseenheten (`ITMTableEntity`) brukes som en del av samme importøkt, må reiseenheten skje før opprettelsen av en forsendelsescontainer. Hvis ikke kan **Reise-ID**-veriden (`ShipId`) ikke valideres riktig. Hvis en plassholderverdi brukes for **Reise-ID**-verdien (`ShipId`), kan tilknytningen bare opprettes hvis den samme plassholderen brukes som **Reise-ID** (`ShipId`) i forsendelsescontainerenheten.

### <a name="other-field-validations"></a>Andre feltvalideringer

Følgende tabell viser feltene i containertabellen for forsendelse (`ITMContainers`) som valideres mot tabeller oppsett for landingskostnad. Den viser også dataenhetene for landede kostnader som en fraktforsender kan bruke til å lese de eksisterende verdiene og sikre at gyldige verdier mottas i miljøet ditt.

| Felt i ITMContainers-tabellen | Dataenhet for landede kostnader |
|---|---|
| Fraktcontainertype | ITMShippingContainerTypeEntity |
| Beskrivelse av varer | ITMGoodsDescriptionEntity |
| Kjøletype | ITMShippingContainerRefrigerationTypeEntity |

## <a name="folios-itmfolioentity"></a>Folioer (ITMFolioEntity)

En folio representerer en gruppering av varer i en forsendelsescontainer til formålet med tolldeklarasjoner. Megleren inneholder hodenivåinformasjon som er knyttet til tollmekleren og en beskrivelse av varene. Denne funksjonen støttes av `ITMFolioEntity`-enheten. I tabellen nedenfor finner du en oversikt over felt og tilordninger som utgjør denne enheten.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Megler informert | ITMFolioTable.ShipBrokerAdvised | Dato/klokkeslett | Nei | Nei |
| Godskontrollnummer | ITMFolioTable.ShipCargoControlNumber | Nvarchar(20) | Nei | Nei |
| Kundeavtale | ITMFolioTable.ShipCustomerAppointment | Dato/klokkeslett | Nei | Nei |
| Tollmegler | ITMFolioTable.ShipCustomsBroker | Nvarchar(20) | Nei | Nei |
| Toll-ID | ITMFolioTable.ShipCustomsId | Nvarchar(60) | Nei | Nei |
| Selskap | ITMFolioTable.ShipDataArea | Nvarchar(4) | Nei | **Ja** |
| Levert ved lager | ITMFolioTable.ShipDelAtWarehouse | Dato/klokkeslett | Nei | Nei |
| Leveringsinstruksjoner | ITMFolioTable.ShipDeliveryInstructions | Dato/klokkeslett | Nei | Nei |
| Dokumenter mottatt | ITMFolioTable.ShipDocReceived | Int | Nei | Nei |
| Estimert leveringsdato | ITMFolioTable.ShipEstDlvDate | Dato/klokkeslett | Nei | Nei |
| Beregnet ankomst ved forsendelseshavn | ITMFolioTable.ShipEstPortDate | Dato/klokkeslett | Nei | Nei |
| Eksportør | ITMFolioTable.ShipExporterId | Nvarchar(20) | Nei | Nei |
| Navn | ITMFolioTable.ShipExporterName | Nvarchar(60) | Nei | Nei |
| Foliodato | ITMFolioTable.ShipFolioDate | Dato/klokkeslett | Nei | Nei |
| Folio | ITMFolioTable.ShipFolioId | Nvarchar(20) | **Ja** | **Ja** |
| Fra-havn | ITMFolioTable.ShipFromPort | Nvarchar(20) | Nei | Nei |
| Beskrivelse av varer | ITMFolioTable.ShipGoodsDesc | Nvarchar(60) | Nei | Nei |
| Varer frigitt | ITMFolioTable.ShipGoodsReleased | Dato/klokkeslett | Nei | Nei |
| Flyfraktseddelen/fraktbrev | ITMFolioTable.ShipHAWB | Nvarchar(20) | Nei | Nei |
| Sjøreise | ITMFolioTable.ShipId | Nvarchar(20) | Nei | **Ja** |
| Mål | ITMFolioTable.ShipMeasurement | Numeric(32, 6) | Nei | Nei |
| Måleenhet | ITMFolioTable.ShipMeasurementUnit | Int | Nei | Nei |
| Antall kartonger | ITMFolioTable.ShipNoOfCartons | Numeric(32, 6) | Nei | Nei |
| Opprinnelig fraktbrev sendt | ITMFolioTable.ShipOriginalBOLSebt | Dato/klokkeslett | Nei | Nei |
| Opprinnelige dokumenter mottatt | ITMFolioTable.ShipOriginalDocsReceived | Dato/klokkeslett | Nei | Nei |
| Bestillingsstatus | ITMFolioTable.ShipPurchStatus | Int | Nei | Nei |
| Kommentarer | ITMFolioTable.ShipRemarks | Nvarchar(MAX) | Nei | Nei |
| Sjøreisestatus | ITMFolioTable.ShipStatusId | Nvarchar(20) | Nei | Nei |
| Tariffkode | ITMFolioTable.ShipTariffCode | Nvarchar(10) | Nei | Nei |
| Til-havn | ITMFolioTable.ShipToPort | Nvarchar(20) | Nei | Nei |
| Verdisettingsdato | ITMFolioTable.ShipValuationDate | Dato/klokkeslett | Nei | Nei |
| Bekreftelsesdato | ITMFolioTable.ShipVerificationDate | Dato/klokkeslett | Nei | Nei |
| Leverandørnummer | ITMFolioTable.VendAccount | Nvarchar(20) | Nei | Nei |

### <a name="number-sequences-for-folios"></a>Nummerserier for folier

Nummerserien for folioer kontrollerer tildelingen av folio-IDer.

Verdien som sendes til dataenheten når verdien **Folio-ID** (`FolioId`) brukes til å identifisere en eksisterende post for oppdatering. Hvis posten ikke finnes, avhenger virkemåten av om den tilordnede nummerserien er konfigurert til å tillate manuell registrering:

- Hvis manuell registrering er aktivert, opprettes det en ny post som bruker den sendte verdien.
- Hvis nummeret på den manuelle registreringen ikke er aktivert, brukes neste nummer i den tilordnede nummerserien i stedet for den sendte verdien.

Under importøkten beholdes plassholderverdien som importeres som folio-IDen. Denne virkemåten sikrer at reiselinjer som refererer til plassholderen, tilknyttes på riktig måte, og at de oppdateres for å gjenspeile verdien som er tilordnet fra nummerserien.

### <a name="field-validations"></a>Feltvalideringer

**Beskrivelsen av varer**-feltet i foliotabellen (`ITMFolioTable`) valideres mot kostnadsoppsetttabellen for Landingskostnad med samme navn. En fraktforsender kan bruke dataenhet for landede kostnader for `ITMGoodsDescriptionEntity` til å lese de eksisterende verdiene og sikre at gyldige verdier mottas i miljøet ditt.

## <a name="voyage-lines-for-purchase-orders-itmpurchaselineentity"></a>Reiselinjer for bestillinger (ITMPurchaseLineEntity)

Reiselinjen representerer én enkelt bestillingslinje som inngår i reisen. Denne relasjonen etableres ved hjelp av feltene **Bestillingsnummer** og **Innkjøpslinjenummer**. Reiselinjen refererer til hver tidligere post som ble opprettet for reisen, forsendelsescontaineren og folioen. Denne funksjonen støttes av `ITMPurchaseLineEntity`-enheten. I tabellen nedenfor finner du en oversikt over felt og tilordninger som utgjør denne enheten.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Valuta | ITMLine.CurrencyCode | Nvarchar(3) | Nei | Nei |
| Nettobeløp | ITMLine.LineAmountMST | Numeric(32, 6) | Nei | Nei |
| Kjøpslinjenummer | ITMLine.RefRecId | Numeric(32, 6) | **Ja** | Nei |
| Fraktcontainer | ITMLine.ShipContainerId | Int | Nei | Nei |
| Selskap | ITMLine.ShipDataArea | Nvarchar(20) | **Ja** | Nei |
| Deklarert antall | ITMLine.ShipDeclaredQty | Nvarchar(4) | Nei | Nei |
| Folio | ITMLine.ShipFolioId | Numeric(32, 6) | Nei | Nei |
| Sjøreise | ITMLine.ShipId | Nvarchar(20) | **Ja** | Nei |
| Varenummer | ITMLine.ShipItemId | Nvarchar(20) | Nei | Nei |
| Mål | ITMLine.ShipMeasurement | Nvarchar(20) | Nei | Nei |
| Måleenhet | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | Nei | Nei |
| Antall kartonger | ITMLine.ShipNoOfCartons | Int | Nei | Nei |
| Plassering | ITMLine.ShipPosition | Numeric(32, 6) | Nei | Nei |
| Antall | ITMLine.ShipQty | Int | Nei | Nei |
| Bestillingsnummer | ITMLine.TransRefId | Numeric(32, 6) | **Ja** | Nei |
| Enhet | ITMLine.UnitId | Int | Nei | Nei |
| Volum | ITMLine.Volume | Nvarchar(10) | Nei | Nei |
| Tykkelse | ITMLine.Weight | Numeric(32, 6) | Nei | Nei |

## <a name="voyage-lines-for-transfer-orders-itmtransferlineentity"></a>Reiselinjer for overføringsordrer (ITMTransferLineEntity)

Reiselinjen representerer én enkelt overføringsordrelinje som inngår i reisen. Denne relasjonen etableres ved hjelp av feltene **Overføringsordrenummer** og **Overføringslinjenummer**. Reiselinjen refererer til hver tidligere post som ble opprettet for reisen, forsendelsescontaineren og folioen. Denne funksjonen støttes av `ITMTransferLineEntity`-enheten. I tabellen nedenfor finner du en oversikt over felt og tilordninger som utgjør denne enheten.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Valuta | ITMLine.CurrencyCode | Nvarchar(3) | Nei | Nei |
| Nettobeløp | ITMLine.LineAmountMST | Numeric(32, 6) | Nei | Nei |
| Fraktcontainer | ITMLine.ShipContainerId | Int | Nei | Nei |
| Selskap | ITMLine.ShipDataArea | Nvarchar(20) | **Ja** | Nei |
| Deklarert antall | ITMLine.ShipDeclaredQty | Nvarchar(4) | Nei | Nei |
| Folio | ITMLine.ShipFolioId | Numeric(32, 6) | Nei | Nei |
| Sjøreise | ITMLine.ShipId | Nvarchar(20) | **Ja** | Nei |
| Varenummer | ITMLine.ShipItemId | Nvarchar(20) | Nei | Nei |
| Mål | ITMLine.ShipMeasurement | Nvarchar(20) | Nei | Nei |
| Måleenhet | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | Nei | Nei |
| Antall kartonger | ITMLine.ShipNoOfCartons | Int | Nei | Nei |
| Plassering | ITMLine.ShipPosition | Numeric(32, 6) | Nei | Nei |
| Antall | ITMLine.ShipQty | Int | Nei | Nei |
| Overføringslinjenummer | ITMLine.TransferLineNumber | Numeric(32, 6) | **Ja** | Nei |
| Overføringsordrenummer | ITMLine.TransRefId | Numeric(32, 6) | **Ja** | Nei |
| Enhet | ITMLine.UnitId | Int | Nei | Nei |
| Volum | ITMLine.Volume | Nvarchar(10) | Nei | Nei |
| Tykkelse | ITMLine.Weight | Numeric(32, 6) | Nei | Nei |

### <a name="reference-table"></a>Referansetabell

Reiselinjer opprettes gjennom en tilknytning med en åpen innkommende ordrelinje. Denne linjen kan være på en bestilling, eller den kan være mottakstransaksjonen på en overføringsordre. Feltet `RefTableId` i tilknytningslinjetabellen (`ITMLine`) angir hvilken ordretype linjen er relatert til, ved å referere til tabellnummeret. Hvis det refereres til bestemte tabellnumre i tabellen der dataene opprettes, deles enhetene basert på disse verdiene.

Verdiene til referansetabellen (`RefTableId`) og transaksjonstypen (`TransType`) er implisitte i valget av enten innkjøpslinjeenhet for landingskostnad eller linjeenheten landingskostnad.

### <a name="validation"></a>Validering

En reiselinje refererer direkte til en reisepost, en forsendelsescontainerpost og en foliopost. Hvis innkjøpslinjeenheten (`ITMPurchaseLinesEntity`) eller overføringslinjeenheten (`ITMPurchaseLinesEntity`) brukes uavhengig av enhetene som brukes til å opprette disse referansepostene, må verdiene for **Reise-ID** (`ShipId`), **Forsendelsescontainer** (`ShipContainerId`) og **Folio** (`ShipFolioId`) en eksisterende post i de tilsvarende tabellene. Hvis ikke vil importen mislykkes.

Hvis én av linjeenhetene brukes som del av den samme importøkten, må disse andre enhetene komme før opprettelsen av en salgslinje. Hvis ikke kan verdiene ikke valideres riktig. Hvis en plassholderverdi brukes for reisen eller folienummeret, kan tilknytningen bare opprettes hvis den samme plassholderen brukes for reisen eller folionummeret i reiselinjeenheten.

Hvis bestillingen eller overføringsordrelinjen allerede er tilordnet en eksisterende salgsordelinje, opprettes ikke den nye linjen. Før ordrelinjen kan tilordnes en ny bestilling, må den fjernes fra gjeldende reise.

### <a name="order-line-identification"></a>Identifikasjon av ordrelinje

Reiselinjer viser direkte til verdiene for **Referansepost-ID** (`RefRecId`), **Lagerdimensjons-ID** (`InventDimId`) og **Lagertransaksjons-ID (**`InventTransId`). Disse verdiene må ikke lenger tas med når dataenheten brukes. I stedet må ordrelinjenummeret nå inkluderes. Til sammen gjør ordrelinjenummeret og ordrenummeret at hver av disse referanseverdiene kan identifiseres.

### <a name="voyage-line-quantity"></a>Antall reiselinjer

Fordi en avtalelinje er direkte tilknyttet en ordrelinje, krever **Antall**-verdien (`ShipQty`) som angis ved hjelp av enheten, at verdiene samsvarer. Validering kjøres mot antallet på enten bestillingslinjen eller overføringslinjen. Hvis valideringen mislykkes, behandles ikke posten.

### <a name="calculated-fields"></a>Beregnede felt

De beregnede feltene for **Vekt** og **Volum** godtar verdiene som mottas via dataenheten. Hvis det ikke finnes noen verdier, brukes systemverdiene til å oppdatere disse feltene hvis systemverdier er tilgjengelige. For Landingskostnad beregnes verdiene på følgende måte:

- *Vekt* = *Antall* × *Varens bruttovekt*
- *Volum* = *Antall* × (*Varens bruttodybde* × *Varens bruttohøyde*  × *Varens bruttobredde*)

## <a name="sequencing"></a>Sekvensering

På grunn av avhengigheter mellom tabellene må innleggingsposten opprettes først. Reiselinjen kan opprettes etter at reisen, forsendelsescontaineren og folioer er opprettet.

Hvis du vil opprette en reise uten valideringsadvarsler, må systemet behandle enhetene i følgende rekkefølge:

1. Reiser (`ITMTableEntity`)
1. Fraktcontainere (`ITMContainersEntity`)
1. Folioer (`ITMFolioTableEntity`)
1. Reiselinjer (`ITMPurchaseLinesEntity` eller `ITMTransferLinesEntity`)
