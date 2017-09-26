---
title: Bankkontoutdrag og betalingsavstemming for EU
description: "Dette emnet gir en oversikt over funksjonaliteten som du kan bruke til å avstemme betalingsinformasjon fra banker i formatene som brukes av europeiske land."
author: neserovleo
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, CustPaymMode, VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267994
ms.search.region: Belgium, Norway, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 48cf0926cd8b440459f71e5a72044585cb73e5dc
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---

# <a name="bank-statement-and-payment-reconciliation-for-the-eu"></a>Bankkontoutdrag og betalingsavstemming for EU

[!include[banner](../includes/banner.md)]


Dette emnet gir en oversikt over funksjonaliteten som du kan bruke til å avstemme betalingsinformasjon fra banker i formatene som brukes av europeiske land.

I Microsoft Enterprise-utgaven av Dynamics 365 for Finance and Operations kan du importere transaksjoner fra banker og utligne disse transaksjonene mot eksisterende transaksjoner. I Europa kan du gjøre dette for følgende scenarier:

-   Import av bankkontoutdrag
-   Import av betalinger
-   Import av returfiler

## <a name="bank-statements"></a>Bankkontoutdrag
A *bankkontoutdrag* eller *kontoutdrag* er et sammendrag av økonomiske transaksjoner som har forekommet i en gitt periode på en bankkonto som holdes av et firma med en finansinstitusjon. Du kan importere et bankkontoutdrag i Finance and Operations. Det er viktig å utligne importerte transaksjoner med eksisterende transaksjoner, i tillegg til å kontrollere start- og sluttsaldoen for bankkontoene. Følgende liste inneholder de europeiske formatene som støttes.

-   Europeiske filformater for avansert bankavstemming. Hvis du vil ha mer informasjon, se [Oversikt over avansert bankavstemming](../cash-bank-management/advanced-bank-reconciliation-overview.md).
-   ISO 20022 camt.053 filformat for bankkontoutdrag.
-   Filformat for CODA-bankkontoutdrag. Hvis du vil ha mer informasjon, kan du se [CODA-bankkontoutdrag](emea-bel-coda-bank-statement-import.md).

## <a name="customer-and-vendor-payments-import-and-return-messages"></a>Kunde- og leverandørbetalinger – import og returmeldinger
I tillegg til et bankkontoutdrag kan banker gi bestemte meldinger som inneholder informasjon om kunde- og leverandørbetalinger, som kan importeres til Finance and Operations og avstemmes med kunde- og leverandørtransaksjoner. Når et firma må motta informasjon om innkommende kundebetalingstransaksjoner fra banken, kan importformatene brukes. For firmaer som bruker direkte debet og kredittoverføring, kan returmeldinger mottas for å oppdatere status for betalinger som er eksportert tidligere. Forskjellen mellom importformater og returformater er at returer hovedsakelig brukes for å oppdatere allerede opprettede betalingsjournallinjer (de kan opprettes når direkte debet eller kreditoverføring ble startet) i stedet for å opprette nye linjer. Noen komplekse importformater kan også inkludere returscenarier. Eksemplet nedenfor viser hvordan denne inndelingen skal implementeres.

### <a name="import-formats"></a>Importformater

-   ISO 20022 [camt.054](emea-ISO20022-file-formats.md) bankvarslingsmelding
-   [Nets-importformat](emea-nor-nets-import-format.md) - kompleks funksjon for norske betalingsformater
-   [Import av ESR](emea-che-esr-customer-payments-import.md)-kundebetalinger
-   Importere betalingsformatene for Sverige - BankGirot Max og BankGirot OCR-formater

### <a name="return-formats"></a>Returformater

-   ISO 20022 [pain.002](emea-ISO20022-file-formats.md) betalingsstatusrapport
-   (DNK) BetalingsserviceBasis-returformat – Returformat for Betalingsservice-eksportformat for kunder
-   [Importere betalingsformater for Sverige](emea-swe-payment-formats-import.md) - Bankgirot Autogiro-returer
-   (SVE) BankGirot-retur – returformat for leverandørbetalinger, som tilsvarer Bankgirot-eksportformat



