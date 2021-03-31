---
title: Bankkontoutdrag og betalingsavstemming for EU
description: Dette emnet gir en oversikt over funksjonaliteten som du kan bruke til å avstemme betalingsinformasjon fra banker i formatene som brukes av europeiske land.
author: neserovleo
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, CustPaymMode, VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.custom: 267994
ms.search.region: Belgium, Norway, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5410cd29c59c6c655c22e82eca43b5132b98ff0f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209879"
---
# <a name="bank-statement-and-payment-reconciliation-for-the-eu"></a><span data-ttu-id="abe7f-103">Bankkontoutdrag og betalingsavstemming for EU</span><span class="sxs-lookup"><span data-stu-id="abe7f-103">Bank statement and payment reconciliation for the EU</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="abe7f-104">Dette emnet gir en oversikt over funksjonaliteten som du kan bruke til å avstemme betalingsinformasjon fra banker i formatene som brukes av europeiske land.</span><span class="sxs-lookup"><span data-stu-id="abe7f-104">This topic provides an overview of the functionality that you can use to reconcile payment information from banks in formats that are used by European countries.</span></span> <span data-ttu-id="abe7f-105">Du kan importere transaksjoner fra banker og utligne disse transaksjonene mot eksisterende transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="abe7f-105">You can import transactions from banks and settle these transactions against existing transactions.</span></span> <span data-ttu-id="abe7f-106">I Europa kan du gjøre dette for følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="abe7f-106">In Europe, you can do this for the following scenarios:</span></span>

-   <span data-ttu-id="abe7f-107">Import av bankkontoutdrag</span><span class="sxs-lookup"><span data-stu-id="abe7f-107">Importing bank statements</span></span>
-   <span data-ttu-id="abe7f-108">Import av betalinger</span><span class="sxs-lookup"><span data-stu-id="abe7f-108">Importing payments</span></span>
-   <span data-ttu-id="abe7f-109">Import av returfiler</span><span class="sxs-lookup"><span data-stu-id="abe7f-109">Importing return files</span></span>

## <a name="bank-statements"></a><span data-ttu-id="abe7f-110">Bankkontoutdrag</span><span class="sxs-lookup"><span data-stu-id="abe7f-110">Bank statements</span></span>
<span data-ttu-id="abe7f-111">A *bankkontoutdrag* eller *kontoutdrag* er et sammendrag av økonomiske transaksjoner som har forekommet i en gitt periode på en bankkonto som holdes av et firma med en finansinstitusjon.</span><span class="sxs-lookup"><span data-stu-id="abe7f-111">A *bank statement* or *account statement* is a summary of financial transactions that have occurred over a given period on a bank account held by a company with a financial institution.</span></span> <span data-ttu-id="abe7f-112">Du kan importere et bankkontoutdrag i Finance.</span><span class="sxs-lookup"><span data-stu-id="abe7f-112">In Finance, you can import a bank statement.</span></span> <span data-ttu-id="abe7f-113">Det er viktig å utligne importerte transaksjoner med eksisterende transaksjoner, i tillegg til å kontrollere start- og sluttsaldoen for bankkontoene.</span><span class="sxs-lookup"><span data-stu-id="abe7f-113">It is important to settle imported transactions with existing transactions as well as verify the opening and ending balance of the bank accounts.</span></span> <span data-ttu-id="abe7f-114">Følgende liste inneholder de europeiske formatene som støttes.</span><span class="sxs-lookup"><span data-stu-id="abe7f-114">The following list includes the supported European formats.</span></span>

-   <span data-ttu-id="abe7f-115">Europeiske filformater for avansert bankavstemming.</span><span class="sxs-lookup"><span data-stu-id="abe7f-115">Advanced bank reconciliation European file formats.</span></span> <span data-ttu-id="abe7f-116">Hvis du vil ha mer informasjon, se [Oversikt over avansert bankavstemming](../cash-bank-management/advanced-bank-reconciliation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="abe7f-116">For more information, see [Advanced bank reconciliation overview](../cash-bank-management/advanced-bank-reconciliation-overview.md).</span></span>
-   <span data-ttu-id="abe7f-117">ISO 20022 camt.053 filformat for bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="abe7f-117">ISO 20022 camt.053 bank statement message file format.</span></span>
-   <span data-ttu-id="abe7f-118">Filformat for CODA-bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="abe7f-118">CODA bank statement file format.</span></span> <span data-ttu-id="abe7f-119">Hvis du vil ha mer informasjon, kan du se [CODA-bankkontoutdrag](emea-bel-coda-bank-statement-import.md).</span><span class="sxs-lookup"><span data-stu-id="abe7f-119">For more information, see [CODA bank statement](emea-bel-coda-bank-statement-import.md).</span></span>

## <a name="customer-and-vendor-payments-import-and-return-messages"></a><span data-ttu-id="abe7f-120">Kunde- og leverandørbetalinger – import og returmeldinger</span><span class="sxs-lookup"><span data-stu-id="abe7f-120">Customer and vendor payments import and return messages</span></span>
<span data-ttu-id="abe7f-121">I tillegg til et bankkontoutdrag kan banker gi bestemte meldinger som inneholder informasjon om kunde- og leverandørbetalinger, som kan importeres til Finance og avstemmes med kunde- og leverandørtransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="abe7f-121">In addition to a bank statement, banks can provide specific messages, containing information about customer and vendor payments, which can be imported into Finance and reconciled with customer and vendor transactions.</span></span> <span data-ttu-id="abe7f-122">Når et firma må motta informasjon om innkommende kundebetalingstransaksjoner fra banken, kan importformatene brukes.</span><span class="sxs-lookup"><span data-stu-id="abe7f-122">When a company needs to receive information about incoming customer payments transactions from the bank, the import formats can be used.</span></span> <span data-ttu-id="abe7f-123">For firmaer som bruker direkte debet og kredittoverføring, kan returmeldinger mottas for å oppdatere status for betalinger som er eksportert tidligere.</span><span class="sxs-lookup"><span data-stu-id="abe7f-123">For companies that use direct debit and credit transfer, the return messages can be received to update the status of payments that were previously exported.</span></span> <span data-ttu-id="abe7f-124">Forskjellen mellom importformater og returformater er at returer hovedsakelig brukes for å oppdatere allerede opprettede betalingsjournallinjer (de kan opprettes når direkte debet eller kreditoverføring ble startet) i stedet for å opprette nye linjer.</span><span class="sxs-lookup"><span data-stu-id="abe7f-124">The difference between import formats and return formats is that returns are targeted mostly to update already created payment journal lines (they can be created when direct debit or credit transfer were initiated) instead of creating new lines.</span></span> <span data-ttu-id="abe7f-125">Noen komplekse importformater kan også inkludere returscenarier.</span><span class="sxs-lookup"><span data-stu-id="abe7f-125">Some complex import formats can also include return scenarios.</span></span> <span data-ttu-id="abe7f-126">Eksemplet nedenfor viser hvordan denne inndelingen skal implementeres.</span><span class="sxs-lookup"><span data-stu-id="abe7f-126">The following example shows how this division should be implemented.</span></span>

### <a name="import-formats"></a><span data-ttu-id="abe7f-127">Importformater</span><span class="sxs-lookup"><span data-stu-id="abe7f-127">Import formats</span></span>

-   <span data-ttu-id="abe7f-128">[ISO 20022 camt.054](emea-ISO20022-file-formats.md) bankvarslingsmelding</span><span class="sxs-lookup"><span data-stu-id="abe7f-128">[ISO 20022 camt.054](emea-ISO20022-file-formats.md) bank notification message</span></span>
-   <span data-ttu-id="abe7f-129">[Nets-importformat](emea-nor-nets-import-format.md) - kompleks funksjon for norske betalingsformater</span><span class="sxs-lookup"><span data-stu-id="abe7f-129">[Nets import format](emea-nor-nets-import-format.md) - Complex feature for Norwegian payment formats</span></span>
-   [<span data-ttu-id="abe7f-130">Import av ESR-kundebetalinger</span><span class="sxs-lookup"><span data-stu-id="abe7f-130">ESR customer payments import</span></span>](emea-che-esr-customer-payments-import.md) 
-   <span data-ttu-id="abe7f-131">Importere betalingsformatene for Sverige - BankGirot Max og BankGirot OCR-formater</span><span class="sxs-lookup"><span data-stu-id="abe7f-131">Import payment formats for Sweden - BankGirot Max and BankGirot OCR formats</span></span>

### <a name="return-formats"></a><span data-ttu-id="abe7f-132">Returformater</span><span class="sxs-lookup"><span data-stu-id="abe7f-132">Return formats</span></span>

-   <span data-ttu-id="abe7f-133">[ISO 20022 pain.002](emea-ISO20022-file-formats.md) betalingsstatusrapport</span><span class="sxs-lookup"><span data-stu-id="abe7f-133">[ISO 20022 pain.002](emea-ISO20022-file-formats.md) payment status report</span></span>
-   <span data-ttu-id="abe7f-134">(DNK) BetalingsserviceBasis-returformat – Returformat for Betalingsservice-eksportformat for kunder</span><span class="sxs-lookup"><span data-stu-id="abe7f-134">(DNK) BetalingsserviceBasis-returformat – Return format for customer Betalingsservice export format</span></span>
-   <span data-ttu-id="abe7f-135">[Importere betalingsformater for Sverige](emea-swe-payment-formats-import.md) - Bankgirot Autogiro-returer</span><span class="sxs-lookup"><span data-stu-id="abe7f-135">[Import payment formats for Sweden](emea-swe-payment-formats-import.md) - Bankgirot Autogiro returns</span></span>
-   <span data-ttu-id="abe7f-136">(SVE) BankGirot-retur – returformat for leverandørbetalinger, som tilsvarer Bankgirot-eksportformat</span><span class="sxs-lookup"><span data-stu-id="abe7f-136">(SWE) BankGirot return – Vendor payments return format, which corresponds to Bankgirot export format</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]