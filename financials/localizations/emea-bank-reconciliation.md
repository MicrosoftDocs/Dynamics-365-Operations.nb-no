---
title: Oversikt over avstemming for setningen og betaling for bank for EU
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

# <a name="bank-statement-and-payment-reconciliation-overview-for-the-eu"></a>Oversikt over avstemming for setningen og betaling for bank for EU

Dette emnet gir en oversikt over funksjonaliteten som du kan bruke til å avstemme betalingsinformasjon fra banker i formatene som brukes av europeiske land.

I Microsoft Dynamics 365 for operasjoner, kan du importere transaksjoner fra banker og utligne disse transaksjonene mot eksisterende transaksjoner. I Europa, kan du gjøre dette for følgende scenarier:

-   Import av bankkontoutdrag
-   Import av betalinger.
-   Returfiler å importere.

## <a name="bank-statements"></a>Bankkontoutdrag
A *bankkontoutdrag* eller *konto setningen* er et sammendrag av økonomiske transaksjoner som har forekommet i en gitt periode på en bankkonto som holdes av et selskap med en finansinstitusjon. Du kan importere et bankkontoutdrag i Dynamics 365 for operasjoner. Det er viktig å utligne importerte transaksjoner med eksisterende transaksjoner, i tillegg til å kontrollere begynnende og avsluttende saldoen for bankkontoene. Følgende liste inneholder de europeiske formatene som støttes.

-   Avanserte bankavstemming europeiske filformater. Hvis du vil ha mer informasjon, se [avanserte bankavstemming oversikt](../cash-bank-management/advanced-bank-reconciliation-overview.md).
-   ISO 20022 camt.053 melding filen bankkontoutdragsformat
-   CODA-banktransaksjonen filformat for setningen. Hvis du vil ha mer informasjon, se [CODA-bankkontoutdrag](emea-bel-coda-bank-statement-import.md).

## <a name="customer-and-vendor-payments-import-and-return-messages"></a>Kunde- og leverandørbetalinger importere og returnerer meldinger
I tillegg til et bankkontoutdrag kan banker gir bestemte meldinger, som inneholder informasjon om kunde- og leverandørbetalinger, som kan importeres til Dynamics 365 for operasjoner og avstemt med kunde-og leverandørtransaksjoner. Når et firma må motta informasjon om innkommende kundetransaksjoner for betalinger fra banken, kan import formatene brukes. For firmaer som bruker direkte debet og kredittoverføring, kan returmeldinger mottas for å oppdatere status for betalinger som tidligere ble eksportert. Forskjellen mellom importformater og retur formater er at returnerer er rettet hovedsakelig for å oppdatere allerede opprettet betalingskladdelinjene (de kan opprettes når direkte debet eller kredit-overføring ble startet) i stedet for å opprette nye linjer. Noen komplekse importformater kan også inkludere retur scenarier. Eksemplet nedenfor viser hvordan denne inndelingen skal implementeres.

##### <a name="import-formats"></a>Importere formater

-   ISO 20022 camt.054 bank-melding
-   [Nett importere format](emea-nor-nets-import-format.md) -omfattende funksjon for norske betalingsformater
-   Importere ESR kundebetalinger
-   Importere betalingsformatene for Sverige - BankGirot Max og BankGirot OCR-formater

##### <a name="return-formats"></a>Returnere formater

-   Statusrapport for ISO 20022 pain.002 betaling
-   (DNK) BetalingsserviceBasis-returformat – Return format for kunden Betalingsservice eksportformat
-   [Importere betalingsformatene for Sverige](emea-swe-payment-formats-import.md) -returnerer Bankgirot Autogiro
-   (SVENSK) BankGirot tilbake – leverandørbetalinger returnere-format, som tilsvarer Bankgirot eksportformat

