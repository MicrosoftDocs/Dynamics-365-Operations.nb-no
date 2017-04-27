---
title: Oversikt over bankkontoutdrag og betalingsavstemming for EU
description: "Dette emnet gir en oversikt over funksjonaliteten som du kan bruke til å avstemme betalingsinformasjon fra banker i formatene som brukes av europeiske land."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankAccountTable, CustPaymMode, VendPaymMode
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267994
ms.assetid: 2bfb8ecc-e850-43cb-9a96-deb11716a391
ms.search.region: Belgium, Norway, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 22d93d7b3618d4f5931c6a7e39d681173734b0b9
ms.lasthandoff: 03/31/2017


---

# <a name="bank-statement-and-payment-reconciliation-overview-for-the-eu"></a>Oversikt over bankkontoutdrag og betalingsavstemming for EU

[!include[banner](../includes/banner.md)]


Dette emnet gir en oversikt over funksjonaliteten som du kan bruke til å avstemme betalingsinformasjon fra banker i formatene som brukes av europeiske land.

I Microsoft Dynamics 365 for Operations kan du importere transaksjoner fra banker og utligne disse transaksjonene mot eksisterende transaksjoner. I Europa kan du gjøre dette for følgende scenarier:

-   Import av bankkontoutdrag
-   Import av betalinger.
-   Import av returfiler.

## <a name="bank-statements"></a>Bankkontoutdrag
A *bankkontoutdrag* eller *kontoutdrag* er et sammendrag av økonomiske transaksjoner som har forekommet i en gitt periode på en bankkonto som holdes av et firma med en finansinstitusjon. Du kan importere et bankkontoutdrag i Dynamics 365 for Operations. Det er viktig å utligne importerte transaksjoner med eksisterende transaksjoner, i tillegg til å kontrollere start- og sluttsaldoen for bankkontoene. Følgende liste inneholder de europeiske formatene som støttes.

-   Europeiske filformater for avansert bankavstemming. Hvis du vil ha mer informasjon, se [Oversikt over avansert bankavstemming](../cash-bank-management/advanced-bank-reconciliation-overview.md).
-   ISO 20022 camt.053 filformat for bankkontoutdrag
-   Filformat for CODA-bankkontoutdrag. Hvis du vil ha mer informasjon, kan du se [CODA-bankkontoutdrag](emea-bel-coda-bank-statement-import.md).

## <a name="customer-and-vendor-payments-import-and-return-messages"></a>Kunde- og leverandørbetalinger – import og returmeldinger
I tillegg til et bankkontoutdrag kan banker gi bestemte meldinger som inneholder informasjon om kunde- og leverandørbetalinger, som kan importeres til Dynamics 365 for Operations og avstemmes med kunde- og leverandørtransaksjoner. Når et firma må motta informasjon om innkommende kundebetalingstransaksjoner fra banken, kan importformatene brukes. For firmaer som bruker direkte debet og kredittoverføring, kan returmeldinger mottas for å oppdatere status for betalinger som er eksportert tidligere. Forskjellen mellom importformater og returformater er at returer hovedsakelig brukes for å oppdatere allerede opprettede betalingsjournallinjer (de kan opprettes når direkte debet eller kreditoverføring ble startet) i stedet for å opprette nye linjer. Noen komplekse importformater kan også inkludere returscenarier. Eksemplet nedenfor viser hvordan denne inndelingen skal implementeres.

##### <a name="import-formats"></a>Importformater

-   ISO 20022 camt.054 bankvarslingsmelding
-   [Nets-importformat](emea-nor-nets-import-format.md) - kompleks funksjon for norske betalingsformater
-   Import av ESR-kundebetalinger
-   Importere betalingsformatene for Sverige - BankGirot Max og BankGirot OCR-formater

##### <a name="return-formats"></a>Returformater

-   ISO 20022 pain.002 betalingsstatusrapport
-   (DNK) BetalingsserviceBasis-returformat – Returformat for Betalingsservice-eksportformat for kunder
-   [Importere betalingsformater for Sverige](emea-swe-payment-formats-import.md) - Bankgirot Autogiro-returer
-   (SVE) BankGirot-retur – returformat for leverandørbetalinger, som tilsvarer Bankgirot-eksportformat



