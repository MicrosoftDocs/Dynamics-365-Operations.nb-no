---
title: Leverandørfakturarenheter
description: Denne artikkelen gir informasjon om leverandørfakturaenheter, som gjør det mulig å konfigurere kostnadstypekoder for interne kostnader eller eksternt avledede kostnader.
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
ms.openlocfilehash: 171b383e1549babd76fd18e4932436a66aa62cc1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873934"
---
# <a name="vendor-invoice-entities"></a>Leverandørfakturaenheter

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

Ved hjelp av modulen **Landingskostnad** er det mulig å konfigurere kostnadstypekoder for interne kostnader eller eksternt avledede kostnader. Hvis en kostnad er ekstern for en virksomhet, forventes det en faktura fra tjenesteleverandør. Denne fakturaen behandles som en fakturajournal som kan knyttes til en reise, og verdien av fakturaen kan distribueres på tvers av én eller flere kostnader for reisen.

Ved hjelp av leverandørfakturaenhetene kan verdien til en journallinje fordeles på tvers av én eller flere kostnader ved en avgift som deler samme kosttypekode.

En kostnad kan bare fordeles hvis det finnes fakturajournalhode og fakturajournallinjer.

## <a name="vendor-voyage-cost-allocations-itmledgerjournalcostlinesvoyagesentity"></a>Kostnadsfordelinger for leverandørreise (ITMLedgerJournalCostLinesVoyagesEntity)

Ved hjelp av dataenheten for kostnadstildelinger for leverandørreise kan en leverandørfakturalinje fordeles på tvers av én eller flere kostnader som gjelder kostnadsområdet for reisen. Denne funksjonen støttes av `ITMLedgerJournalCostLinesVoyagesEntity`-enheten. I tabellen nedenfor finner du en oversikt over felt og tilordninger som utgjør denne enheten.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Tilordnet beløp | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nei | Nei |
| Linjenummer for kostnadstransaksjon | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nei |
| Journallinjenummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nei |
| Journalnummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nei |
| Sjøreise | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nei |

## <a name="vendor-shipping-container-cost-allocations-itmledgerjournalcostlinescontainersentity"></a>Kostnadsfordelinger for leverandørforsendelsescontainer (ITMLedgerJournalCostLinesContainersEntity)

Ved hjelp av dataenheten for kostnadsfordelinger for leverandørforsendelsescontaineren kan en leverandørfakturalinje fordeles på tvers av én eller flere kostnader som gjelder kostnadsområdet for forsendelsescontaineren. Denne funksjonen støttes av `ITMLedgerJournalCostLinesContainersEntity`-enheten. I tabellen nedenfor finner du en oversikt over felt og tilordninger som utgjør denne enheten.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Tilordnet beløp | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nei | Nei |
| Fraktcontainer | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nei |
| Linjenummer for kostnadstransaksjon | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nei |
| Journallinjenummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nei |
| Journalnummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nei |
| Sjøreise | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nei |

## <a name="vendor-folio-cost-allocations-itmledgerjournalcostlinesfoliosentity"></a>Kostnadsfordelinger for leverandørfolio (ITMLedgerJournalCostLinesFoliosEntity)

Ved hjelp av dataenheten for kostnadstildelinger for leverandørfolio kan en leverandørfakturalinje fordeles på tvers av én eller flere kostnader som gjelder kostnadsområdet for folio. Denne funksjonen støttes av `ITMLedgerJournalCostLinesFoliosEntity`-enheten. I tabellen nedenfor finner du en oversikt over felt og tilordninger som utgjør denne enheten.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Tilordnet beløp | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nei | Nei |
| Linjenummer for kostnadstransaksjon | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nei |
| Folio | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nei |
| Journallinjenummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nei |
| Journalnummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nei |

## <a name="vendor-purchase-order-cost-allocations-itmledgerjournalcostlinespurchtableentity"></a>Kostnadsfordelinger for leverandørbestilling (ITMLedgerJournalCostLinesPurchTableEntity)

Ved hjelp av dataenheten for kostnadsfordelinger for leverandørbestillinger kan en leverandørfakturalinje fordeles på tvers av én eller flere kostnader som gjelder kostnadsområdet for bestilling. Denne funksjonen støttes av `ITMLedgerJournalCostLinesPurchTableEntity`-enheten. I tabellen nedenfor finner du en oversikt over felt og tilordninger som utgjør denne enheten.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Tilordnet beløp | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nei | Nei |
| Linjenummer for kostnadstransaksjon | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nei |
| Journallinjenummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nei |
| Journalnummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nei |
| Bestilling | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nei |

## <a name="vendor-item-cost-allocations-itmledgerjournalcostlinespurchlineentity"></a>Kostnadsfordelinger for leverandørvare (ITMLedgerJournalCostLinesPurchLineEntity)

Ved hjelp av dataenheten for kostnadstildelinger for leverandørvare kan en leverandørfakturalinje fordeles på tvers av én eller flere kostnader som gjelder kostnadsområdet for vare. Varekostnadsområdet dekker kostnadene på bestillingslinjen. Denne funksjonen støttes av `ITMLedgerJournalCostLinesPurchLineEntity`-enheten. I tabellen nedenfor finner du en oversikt over felt og tilordninger som utgjør denne enheten.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Tilordnet beløp | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nei | Nei |
| Linjenummer for kostnadstransaksjon | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nei |
| Journallinjenummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nei |
| Journalnummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nei |
| Bestilling | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nei |
| Bestillingslinjenummer | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nei |

## <a name="vendor-transfer-order-line-cost-allocations-itmledgerjournalcostlinestransferlineentity"></a>Kostnadsfordelinger for leverandøroverføringsordre (ITMLedgerJournalCostLinesTransferLineEntity)

Ved hjelp av dataenheten for kostnadsfordelinger for leverandøroverføringsordrelinje kan en leverandørfakturalinje fordeles på tvers av én eller flere kostnader som gjelder kostnadsområdet for overføringslinje. Denne funksjonen støttes av `ITMLedgerJournalCostLinesTransferLineEntity`-enheten. I tabellen nedenfor finner du en oversikt over felt og tilordninger som utgjør denne enheten.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Tilordnet beløp | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nei | Nei |
| Linjenummer for kostnadstransaksjon | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nei |
| Journallinjenummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nei |
| Journalnummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nei |
| Overføringsordre | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nei |
| Nummer på overføringsordrelinje | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nei |

### <a name="reference-table"></a>Referansetabell

Linjer for reisekostnad har en direkte tilknytning til en kostnadstransaksjonspost. Denne posten inneholder verdien for **Referansetabell-ID**. Denne verdien er unik for hvert kostnadsområde (reise, forsendelsescontainer og så videre). Når det refereres til bestemte tabellnumre for data som opprettes ved hjelp av dataenheter, deles enhetene opp basert på verdiene **Referansetabell-ID**.

Verdiene til referansetabellen (`RefTableId`) og transaksjonstypen (`TransType`) er implisitte i valget av bestillingslinjen Landingskostnad eller overføringslinjen Landingskostnad.

## <a name="vendor-invoice-journal-lines-vendorinvoicejournallineentity"></a>Leverandørfakturajournallinjer (VendorInvoiceJournalLineEntity)

Før en journallinjeverdi kan fordeles til én eller flere kostnader i modulen **Landingskostnad**, må journallinjen være knyttet til et kostnadsområde. Hvis du vil ha støtte for denne funksjonaliteten , legger modulen **Landingskostnad** til noen nye felt i journallinjetabellen (`LedgerJournalTrans`).

### <a name="fields-added-to-the-vendor-invoice-journal-line-entity"></a>Felt som er lagt til i linjeenheten i leverandørfakturajournalen

Tabellen nedenfor viser feltene som modulen **Landingskostnad** legger til i journallinjeenheten for leverandørfaktura (`VendorInvoiceJournalLineEntity`). Ved bruk av disse feltene kan systemet opprette journallinjer og fordele kostnader mot dem.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Kostnadsområde | LedgerJournalTrans.ITMCostArea | Int | Nei | Nei |
| Kosttypekode | LedgerJournalTrans.ITMCostTypeId | Nvarchar(20) | Nei | Nei |

### <a name="mainoffset-account"></a>Hovedkonto/motkonto

Hovedkonto/motkontoen for en fakturajournallinje som er knyttet til Landingskostnadsreisen, bestemmes av kostnadstypekoden. Når kostnadstypekoden er inkludert på fakturajournallinjen, brukes avregningskontoen for koden som enten hovedkontoen eller motkontoen, avhengig av scenariet:

- **Enkeltlinjejournal** – Hvis det er definert en hovedkonto (med andre ord leverandørkontoen), og det oppgis en kostnadstypekode, angis avregningskontoverdien for denne kostnadstypekoden i motkontoen.
- **Flerlinjejournal** – Hvis det ikke er definert en hovedkonto, men kostnadstypekoden er angitt, angis avregningskontoverdien for kostnadstypekoden i hovedkontoen. Journallinjen som krediterer leverandøren, vil ikke referere til en kostnadstypekode.

## <a name="sequencing"></a>Sekvensering

På grunn av avhengigheter mellom journal- og journallinjetabellene må reiseposten opprettes først. Reiselinjer kan opprettes etter at reisen, forsendelsescontaineren og folioer er opprettet.

For å tilordne en reisefaktura må systemet behandle enhetene i følgende rekkefølge:

1. Fakturajournalhode (`VendInvoiceJournalHeaderEntity`)
1. Fakturajournallinje (`VendInvoiceJournalLineEntity`)
1. Landingskostnadstildelinger (`ITMLedgerJournalEntities`)
