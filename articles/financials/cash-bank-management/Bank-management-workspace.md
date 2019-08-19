---
title: Arbeidsområde for bank
description: Dette emnet gir informasjon om arbeidsområdet for bank. Dette arbeidsområdet viser informasjon som er knyttet til firmaets bankkontoer, og inneholder en sammendragsvisning og en Analyse-side. Sammendragsvisningen viser sammendragsfliser, bankkontoinformasjon, et saldodiagram og relatert informasjon. Analyse-siden bruker funksjonene i Microsoft Power BI til å vise bilder som er knyttet til bankkontosaldoer.
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 20847ea4651b816fc95135ca03667ae297cde5be
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842743"
---
# <a name="bank-management-workspace"></a><span data-ttu-id="0d6d4-106">Arbeidsområde for bank</span><span class="sxs-lookup"><span data-stu-id="0d6d4-106">Bank management workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d6d4-107">Arbeidsområdet **Bank** viser informasjon som er knyttet til firmaets bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-107">The **Bank management** workspace shows information that is related to company bank accounts.</span></span> <span data-ttu-id="0d6d4-108">Arbeidsområdet inneholder en **Sammendrag**-visning og en **Analyse**-side.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-108">This workspace includes a **Summary** view and an **Analytics** page.</span></span> <span data-ttu-id="0d6d4-109">**Sammendrag**-visningen viser sammendragsfliser, bankkontoinformasjon, et saldodiagram og relatert informasjon.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-109">The **Summary** view shows summary tiles, bank account information, a balance chart, and related information.</span></span> <span data-ttu-id="0d6d4-110">**Analyse**-siden bruker funksjonene i Microsoft Power BI til å vise bilder som er knyttet til bankkontosaldoer.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-110">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to bank account balances.</span></span>

## <a name="summary-view"></a><span data-ttu-id="0d6d4-111">Sammendrag-visningen</span><span class="sxs-lookup"><span data-stu-id="0d6d4-111">Summary view</span></span>

### <a name="summary"></a><span data-ttu-id="0d6d4-112">Sammendrag</span><span class="sxs-lookup"><span data-stu-id="0d6d4-112">Summary</span></span>

<span data-ttu-id="0d6d4-113">Flisene i **Sammendrag**-delen gir en oversikt over bankkontoene og rask tilgang til sidene du oftest må bruke.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-113">The tiles in the **Summary** section give an overview of your bank accounts and provide quick access to the pages that you most often have to use.</span></span> <span data-ttu-id="0d6d4-114">Informasjon om bankavstemming gjeler spesifikt for funksjonen Avansert bankavstemming.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-114">The bank reconciliation information is specific to the Advanced bank reconciliation functionality.</span></span> <span data-ttu-id="0d6d4-115">Informasjon tas bare med for de bankkontoene som har alternativet **Avansert bankavstemming** satt til **Ja** på **Bankkonto**-siden.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-115">Information is included only for those bank accounts that have the **Advanced bank reconciliation** option set to **Yes** on the **Bank account** page.</span></span> <span data-ttu-id="0d6d4-116">Fra **Sammendrag**-delen kan du importere elektroniske bankfiler for bankkontoer på tvers av alle juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-116">From the **Summary** section, you can import electronic bank files for bank accounts across all legal entities.</span></span>

### <a name="bank-accounts"></a><span data-ttu-id="0d6d4-117">Bankkontoer</span><span class="sxs-lookup"><span data-stu-id="0d6d4-117">Bank accounts</span></span>

<span data-ttu-id="0d6d4-118">Hver bankkonto i den juridiske enheten representeres av et kort i **Bankkontoer**-delen.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-118">Each bank account in the legal entity is represented by a card in the **Bank accounts** section.</span></span> <span data-ttu-id="0d6d4-119">Gjeldende saldo vises, og du kan drille ned til transaksjonene som utgjør dette sammendragssaldobeløpet.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-119">The current balance is shown, and you can drill down to the transactions that make up that summary balance amount.</span></span> <span data-ttu-id="0d6d4-120">**Mellomtransaksjoner**-beløpet gjør også at du kan drille ned til transaksjonene som utgjør dette sammendragsbeløpet.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-120">The **Bridged transactions** amount also lets you drill down to the transactions that make up that summary amount.</span></span> <span data-ttu-id="0d6d4-121">Mellomtransaksjoner er alle utestående transaksjoner som er postert ved hjelp av funksjonen for mellompostering, men som ikke er fjernet ennå.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-121">Bridged transactions are any pending transactions that have been posted by using bridging functionality, but that haven't yet been cleared.</span></span> <span data-ttu-id="0d6d4-122">**Ventende saldo**-beløpet er gjeldende saldo minus de mellomposterte, eller ventende, transaksjonene.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-122">The **Pending balance** amount is the current balance minus the bridged, or pending, transactions.</span></span>

<span data-ttu-id="0d6d4-123">Kortet viser også da bankkontoen sist ble avstemt.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-123">The card also shows when the bank account was last reconciled.</span></span> <span data-ttu-id="0d6d4-124">Denne informasjonen vises bare hvis Avansert bankavstemming er aktivert for bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-124">This information is shown only if Advanced bank reconciliation is enabled for the bank account.</span></span>

### <a name="balance"></a><span data-ttu-id="0d6d4-125">Beholdning</span><span class="sxs-lookup"><span data-stu-id="0d6d4-125">Balance</span></span>

<span data-ttu-id="0d6d4-126">Diagrammet **Saldo** viser historisk saldoinformasjon for bankkontoen som er valgt i **Bankkontoer**-delen eller et sammendrag av historisk saldoinformasjon for alle bankkontoer i den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-126">The **Balance** chart shows either historic balance information for the bank account that is selected in the **Bank accounts** section or a summary of historic balance information for all bank accounts in the legal entity.</span></span> <span data-ttu-id="0d6d4-127">Denne informasjonen er tilgjengelig for ulike perioder: gjeldende uke, gjeldende måned, gjeldende år, de siste fem årene og alle perioder (hele loggen for bankkontoen).</span><span class="sxs-lookup"><span data-stu-id="0d6d4-127">This information is available for various periods: the current week, the current month, the current year, the last five years, and all periods (the full history of the bank account).</span></span> 

<span data-ttu-id="0d6d4-128">Hvis du viser diagrammet **Saldo** for én bankkonto, vises de historiske saldoene i bankkontovalutaen.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-128">If you're viewing the **Balance** chart for a single bank account, the historic balances are shown in the bank account currency.</span></span> <span data-ttu-id="0d6d4-129">Hvis du viser diagrammet for alle bankkontoer i den juridiske enheten, vises de historiske saldoene i regnskapsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-129">If you're viewing the chart for all bank accounts in the legal entity, the historic balances are shown in the accounting currency.</span></span>

<span data-ttu-id="0d6d4-130">Informasjon om da dataene sist ble oppdatert, vises øverst i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-130">Information about when the data was last updated appears at the top of the chart.</span></span> <span data-ttu-id="0d6d4-131">Du kan oppdatere dataene du trenger.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-131">You can update the data as you require.</span></span>

### <a name="related-information"></a><span data-ttu-id="0d6d4-132">Beslektet informasjon</span><span class="sxs-lookup"><span data-stu-id="0d6d4-132">Related information</span></span>

<span data-ttu-id="0d6d4-133">Fra delen **Beslektet informasjon** kan du åpne **Økonomijournal**-siden for å fullføre bankoverføringer.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-133">From the **Related information** section, you can open the **General journal** page to complete bank transfers.</span></span> <span data-ttu-id="0d6d4-134">Du kan også raskt åpne sidene **Banktransaksjoner** og **Mellomtransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-134">You can also quickly open the **Bank transactions** and **Bridged transactions** pages.</span></span>

## <a name="analytics-view"></a><span data-ttu-id="0d6d4-135">Analyse-visningen</span><span class="sxs-lookup"><span data-stu-id="0d6d4-135">Analytics view</span></span>

<span data-ttu-id="0d6d4-136">**Analyse**-siden inneholder viktige mål om bankkontoene i gjeldende firma.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-136">The **Analytics** page provides important metrics about the bank accounts in the current company.</span></span> <span data-ttu-id="0d6d4-137">Følgende visualiseringer er tilgjengelige på siden:</span><span class="sxs-lookup"><span data-stu-id="0d6d4-137">The following visualizations are available on the page:</span></span>

-   <span data-ttu-id="0d6d4-138">Total banksaldo i systemvaluta</span><span class="sxs-lookup"><span data-stu-id="0d6d4-138">Total bank balance in system currency</span></span>
-   <span data-ttu-id="0d6d4-139">Saldo etter juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="0d6d4-139">Balance by legal entity</span></span>
-   <span data-ttu-id="0d6d4-140">Dagens faktiske saldo i forhold til anslått saldo i bankkontovaluta</span><span class="sxs-lookup"><span data-stu-id="0d6d4-140">Today’s actual vs forecasted balance in bank account currency</span></span>
-   <span data-ttu-id="0d6d4-141">Saldo etter bankkonto</span><span class="sxs-lookup"><span data-stu-id="0d6d4-141">Balance by bank account</span></span>
-   <span data-ttu-id="0d6d4-142">Saldo etter valuta</span><span class="sxs-lookup"><span data-stu-id="0d6d4-142">Balance by currency</span></span>

<span data-ttu-id="0d6d4-143">Du kan vise bankanalyse på tvers av alle firmaer fra arbeidsområdet **Kontantstrømoversikt – alle firmaer**.</span><span class="sxs-lookup"><span data-stu-id="0d6d4-143">You can view bank analytics across all companies from the **Cash overview – all companies** workspace.</span></span>
